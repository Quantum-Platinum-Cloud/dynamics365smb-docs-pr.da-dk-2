---
title: "Bruge finanskladder, der skal bogføres direkte til Finans | Microsoft Docs"
description: "Lær, hvordan du kan bruge finanskladder til at bogføre økonomisk transaktioner på finanskonti og andre konti, f.eks. bank- og kreditorkonti."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 090a0141583795757a0d59b358ba4d553100d976
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="working-with-general-journals"></a>Arbejde med finanskladder
De fleste finansposteringer bogføres i finansregnskabet ved hjælp af dedikerede forretningsdokumenter, f.eks. købsfakturaer og salgsordrer. Du kan oprette relaterede transaktioner for aktiviteter, der ikke er repræsenteret af et dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. mindre udgifter eller indbetalinger, ved at bogføre kladdelinjer i vinduet **Finanskladde**. Du kan finde flere oplysninger i [Bogføre transaktioner direkte i finansregnskabet](finance-how-post-transactions-directly.md).

For eksempel kan du bogføre medarbejdernes udgifter af egne penge på forretningsrelaterede udgifter for senere refusion. Du kan finde flere oplysninger i [Registrere og refundere medarbejdernes udgifter](finance-how-record-reimburse-employee-expenses.md).

Du bruger finanskladder til at bogføre økonomiske transaktioner direkte på finanskonti og andre konti, f.eks. bank-, debitor-, kreditor- og medarbejderkonti. Når du bogfører via en finanskonto, oprettes der altid poster i finanskonti. Det gælder også, når du bogfører f.eks. en kladdelinje på en debitorkonto, fordi der bogføres en post på en finanskonto for tilgodehavende via en bogføringsgruppe.

De oplysninger, du angiver i en kladde, er midlertidige og kan ændres, mens de er i kladden. Når du bogfører kladden, overføres oplysningerne til poster på individuelle konti, hvor de ikke kan ændres. Du kan imidlertid annullere udligningen af bogførte poster, og du kan bogføre tilbageførsels- eller rettelsesposter. Du kan finde flere oplysninger i [Tilbageføre poster](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Bruge kladdetyper og -navne
Der er forskellige finanskladdetyper. Hver kladdetype er repræsenteret af et dedikeret vindue med bestemte funktioner og de felter, der kræves for at understøtte disse funktioner, f.eks. vinduet **Betalingsudligningskladde** til behandling af bankbetalinger og vinduet **Udbetalingskladde** til betaling af kreditorer eller refusion af medarbejdere. Du kan finde flere oplysninger i [Foretage indbetalinger](payables-make-payments.md) og [Udligne debitorbetalinger manuelt](receivables-how-apply-sales-transactions-manually.md).

For hver kladdetype kan du angive din egen private kladde som kladdenavn. F.eks. kan du angive din egen kladdetype som udbetalingskladden med dit personlige layout og dine indstillinger. Følgende tip er et eksempel på, hvordan du kan tilpasse en kladde.

> [!TIP]  
> Hvis du markerer afkrydsningsfeltet **Foreslå modkontobeløb** på linjen for dit kladdenavn i vinduet **Finanskladdenavne**, udfyldes feltet **Beløb** på f.eks. finanskladdelinjer for samme bilagsnummer automatisk med den værdi, der er nødvendig for at afstemme dokumentet. Du kan finde flere oplysninger i [Lade [!INCLUDE[d365fin](includes/d365fin_md.md)] foreslå værdier](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Om hovedkonti og modkonti
Hvis du har oprettet modkonti for kladdenavnene, udfyldes modkontoen automatisk på siden **Finanskladder**, når du udfylder feltet **Kontonr.**. Hvis ikke, skal du udfylde både feltet **Kontonr.** og feltet **Modkontonr.** manuelt. Et positivt beløb i feltet **Beløb** debiteres på hovedkontoen og krediteres på modkontoen. Et negativt beløb krediteres på hovedkontoen og debiteres på modkontoen.

> [!NOTE]  
>   Moms beregnes separat for hovedkontoen og modkontoen, så der kan bruges forskellige momsprocentsatser.

## <a name="working-with-recurring-journals"></a>Arbejde med gentagelseskladder
En gentagelseskladde er en finanskladde med specifikke felter til styring af transaktioner, som bogføres ofte med få eller ingen ændringer, f.eks. leje, abonnementer, elektricitet og varme. Med disse felter til gentagelsestransaktioner kan du bogføre både faste og variable beløb. Du kan også angive automatiske tilbageførselsposter dagen efter bogføringsdatoen. Du kan også bruge fordelingsnøgler til at opdele de gentagne poster mellem forskellige konti. Du kan finde yderligere oplysninger i afsnittet "Fordeling af gentagelsesposter på flere konti".

Med gentagelseskladder skal poster, der bogføres regelmæssigt, kun indtastes én gang. Det vil sige, at de konti, dimensioner og dimensionsværdier osv., som angives, bevares i kladden efter bogføringen. Hvis du vil foretage ændringer, kan du gøre det ved hver bogføring.

### <a name="recurring-method-field"></a>Feltet Gentagelsesmetode
Dette felt bestemmer, hvordan beløbet på kladdelinjen bliver behandlet efter bogføringen. Hvis du f.eks. bogfører det samme beløb, hver gang du bogfører linjen, kan du vælge at lade beløbet stå. Eller du kan vælge at lade det slette, fordi konti og tekst i linjen kan genbruges ved hver bogføring, men beløbet hver gang varierer.

| Hvis du vil | Skal du se |
| --- | --- |
|Fast|Beløbet på kladdelinjen vil blive stående i posten efter bogføring.|
|Variabel|Beløbet på kladdelinjen slettes efter bogføring.|
|Saldo til dato|Det bogførte beløb på kontoen på linjen bliver fordelt mellem de konti, der er defineret for linjen i tabellen Fordeling. Saldoen på kontoen bliver derfor angivet til nul. Husk at udfylde feltet **Fordelingspct.** i vinduet **Fordelinger**. Du kan finde yderligere oplysninger i afsnittet "Fordeling af gentagelsesposter på flere konti".|
|Fast med tilbageføring|Beløbet i kladdelinjen bliver stående på linjen efter bogføringen, og der bliver bogført en modpost den følgende dag.|
|Variabel med tilbageføring|Beløbet i kladdelinjen bliver slettet efter bogføringen, og der bliver bogført en modpost den følgende dag.|
|Saldo med tilbageføring|Det bogførte beløb på kontoen på linjen bliver fordelt mellem de konti, der er defineret for linjen i vinduet **Fordelinger**. Saldoen på kontoen angives til nul, og der posteres en modpost den følgende dag.|

> [!NOTE]  
>  Momsfelter kan kun være udfyldt på gentagelseskladdelinjen eller på allokeringkladdelinjen. Det vil sige, at disse kun kan udfyldes i vinduet **Fordelinger**, hvis de tilsvarende linjer i gentagelseskladden ikke er udfyldt.

### <a name="recurring-frequency-field"></a>Feltet Gentagelsesinterval
Dette felt bestemmer, hvor ofte posten på kladdelinjen bogføres. Det er en datoformelfelt, og det skal være udfyldt for tilbagevendende kladdelinjer. Du kan finde flere oplysninger i afsnittet "Bruge datoformler" i [Angivelse af data](ui-enter-data.md).

#### <a name="examples"></a>Eksempler
Hvis kladdelinjen skal bogføres hver måned, skal du angive "1M". Efter hver bogføring bliver datoen i feltet **Bogføringsdato** opdateret til samme dato i den efterfølgende måned.

Hvis du vil bogføre en post den sidste dag i hver måned, kan du vælge én af følgende muligheder:

- Bogfør den første post på den sidste dag i måneden ved at indtaste 1D+1M-1D (dvs. 1 dag plus 1 måned minus 1 dag). Med denne formel beregnes posteringsdatoen korrekt, uanset antallet af dage i måneden.

- Bogfør den første post på en hvilken som helst dag i en måned ved at indtaste 1M+LM. Med denne formel vil posteringsdatoen være efter én hel måned plus de resterende dage i den indeværende måned.

### <a name="expiration-date-field"></a>Feltet Udløbsdato
Dette felt bestemmer, på hvilken dato kladdelinjen bliver bogført for sidste gang. Linjen bogføres ikke efter denne dato.

Fordelen ved dette felt er, at linjen ikke straks slettes fra kladden, og at du altid kan erstatte den nuværende udløbsdato, så linjen kan bruges i fremtiden.

Hvis feltet er tomt, bogføres linjen, hver gang du bogfører, indtil den slettes fra kladden.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Tildeling af tilbagevendende kladdebeløb til flere konti
I vinduet **Finansgentagelseskladde**, kan du vælge handlingen **Fordelinger** for at se eller styre, hvordan beløbene i gentagelseskladdelinjen fordeles på flere konti og dimensioner. Bemærk, at en fordeling fungerer som en modkontolinje til gentagelseskladdelinjen.

Ligesom i en gentagelseskladde kan du nøjes med at indtaste en fordeling én gang. Derefter vil fordelingen blive stående i fordelingskladden efter bogføringen, så du ikke behøver at indtaste beløb og fordeling hver gang, men kan nøjes med at bogføre gentagelseskladdelinjen.

Hvis gentagelsesmetoden i gentagelseskladden er sat til **Saldo** eller **Saldo med tilbageføring**, bliver der ikke taget hensyn til eventuelle dimensionsværdikoder i gentagelseskladden, når kontoen nulstilles. Så hvis du fordeler en gentagelseslinje på forskellige globale dimensionsværdier i vinduet **Fordelinger**, så vil der kun blive lavet en tilbageførselspost. Hvis du derfor fordeler en gentagelseskladdelinje, som indeholder en dimensionsværdikode, må du ikke indtaste den samme kode i vinduet **Fordelinger**. Hvis du gør det, vil dimensionsværdierne ikke blive korrekte.

####<a name="example-allocating-rent-payments-to-different-departments"></a>Eksempel: Fordeling af huslejebetalinger til forskellige afdelinger
Du betaler husleje hver måned, så du kan indtaste huslejen i indbetalingskonto på en gentagelseskladdelinje. I vinduet **Fordelinger** kan du opdele udgiften på flere afdelinger (afdelingsdimension), i forhold til det antal kvadratmeter hver afdeling optager. Beregningen er baseret på allokeringsprocenten på hver linje. Du kan f.eks. indtaste forskellige konti på forskellige fordelingslinjer (hvis huslejen også skal fordeles på flere konti) eller indtaste den samme konto, men med forskellige dimensionsværdikoder for dimensionen Afdeling på hver linje.


## <a name="working-with-standard-journals"></a>Arbejde med standardkladder
Når du har oprettet kladdelinjer, som du ved, at du sandsynligvis skal oprette igen senere, kan du gemme dem som en standardkladde, inden du bogfører kladden. Denne funktion gælder for varekladder og finanskladder.

> [!NOTE]  
>   Følgende procedure beskriver varekladden, men oplysningerne gælder også for finanskladden.

### <a name="to-save-a-standard-journal"></a>Sådan gemmes en standardkladde
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varekladder**, og vælg derefter det relaterede link.
2. Indsæt en eller flere kladdelinjer.
3. Vælg de kladdelinjer, der skal genbruges.
4. Vælg handlingen **Gem som standardkladde**.
5. I vinduet **Gem som standardvarekladde** skal du definere en ny eller eksisterende standardvarekladde, som linjerne skal gemmes i.

    Hvis du allerede har oprettet en eller flere standardvarekladder og vil erstatte en af dem med det nye sæt varekladdelinjer, skal du vælge den ønskede kode i feltet Kode.
6. Vælg knappen **OK** for at bekræfte, at du vil overskrive den eksisterende standardvarekladde og erstatte alt indholdet.
7. Vælg feltet **Gem pris**, hvis værdierne i feltet **Pris** skal gemmes for standardvarekladden.
8. Vælg feltet **Gem antal**, hvis værdierne i feltet **Antal** skal gemmes.
9. Vælg knappen **OK** for at gemme standardvarekladden.

Når du har gemt standardvarekladden, vises vinduet Varekladde, så du kan bogføre varekladden. Nu kan du hurtigt oprette varekladden, næste gang du har brug for at bogføre de samme eller lignende linjer.

### <a name="to-reuse-a-standard-journal"></a>Sådan genbruges en standardkladde
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varekladder**, og vælg derefter det relaterede link.
2. Vælg handlingen **Hent standardkladder**.

    Vinduet Standardvarekladder åbner med koder og beskrivelser for alle eksisterende standardvarekladder.
3. Vælg handlingen **Vis kladde**, hvis du vil gennemse en standardvarekladde, inden du vælger den til genbrug.

    De ændringer, du foretager i en standardvarekladde implementeres straks. De vil være der, næste gang du åbner eller genbruger standardvarekladden. Den pågældende standardvarekladde vil indeholde ændringerne, næste gang du åbner eller genbruger den. Ændringerne skal derfor være vigtige nok til, at de skal gælde generelt. Hvis det ikke er tilfældet, kan du foretage ændringerne i varekladden, efter at linjerne i standardvarekladden er indsat. Se trin 4 herunder.
4. Vælg den standardvarekladde i vinduet **Standardvarekladder**, du vil genbruge, og vælg derefter knappen **OK**.

    Varekladden udfyldes nu med de linjer, der er gemt i standardvarekladden. Hvis varekladden allerede indeholdt kladdelinjer, placeres de indsatte linjer under de eksisterende kladdelinjer.

    Hvis du ikke markerede feltet **Gem pris**, da du brugte funktionen **Gem som standardkladde**, indsættes varens aktuelle værdi automatisk i feltet **Pris**, værdien kopieres fra feltet **Kostpris** på varekortet.

    > [!NOTE]  
    >   Hvis du markerede feltet **Gem pris** eller **Gem antal**, skal du kontrollere, at de indsatte værdier er korrekt for denne lagerregulering, inden du bogfører varekladden.

    Hvis indsatte varekladdelinjer indeholder gemte kostpriser, som du ikke vil bogføre, kan du hurtigt ændre dem til varernes aktuelle værdi på følgende måde:

6. Vælg de varekladdelinjen, som du vil regulere, og vælg derefter handlingen **Genberegn pris**. Derved opdateres feltet Pris med varens aktuelle pris.
7. Vælg handlingen **Bogfør**.

## <a name="to-renumber-document-numbers-in-journals"></a>Omnummerere bilagsnumre i kladder
Hvis du vil sikre dig, at du ikke får bogføringsfejl pga. bilagets nummerrækkefølge, kan du bruge funktionen **Omnummerer bilagsnumre**, før du bogfører en kladde.

I alle kladder, der er baseret på finanskladden, kan feltet **Bilagsnr** redigeres, så du kan angive forskellige bilagsnumre til forskellige kladdelinjer eller det samme bilagsnummer til relaterede kladdelinjer.

Hvis feltet **Nummerserie** i kladdenavnet er udfyldt, kræver bogføringsfunktionen i finanskladder, at bilagsnummeret på individuelle eller grupperede kladdelinjer er i rækkefølge. Hvis du vil sikre dig, at du ikke får bogføringsfejl pga. bilagets nummerrækkefølge, kan du bruge funktionen **Omnummerer bilagsnumre**, før du bogfører kladden. Hvis relaterede kladdelinjer er grupperet efter bilagsnummer, før du har brugt funktionen, forbliver de grupperet men kan være tildelt et andet bilagsnummer.

Denne funktion fungerer også i filtrerede visninger.

Ved enhver omnummerering af bilagsnumre respekteres relaterede udligninger, f.eks. en betalingsudligning, der er foretaget fra bilaget på kladdelinjen til en kreditorkonto. Derfor opdateres felterne **Udligningsid** og **Udligningsbilagsnr.** muligvis i de berørte finansposteringer.

Følgende procedure er baseret på vinduet **Kassekladde**, men gælder for alle andre kladder, der er baseret på finanskladden, f.eks. vinduet **Udbetalingskladde**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladder**, og vælg derefter det relaterede link.
2. Når du er klar til at bogføre kladden, skal du vælge handlingen **Omnummerer bilagsnumre**.

Værdier i feltet **Bilagsnr.** ændres, hvor det kræves, så bilagsnummeret på individuelle eller grupperede journallinjer er i rækkefølge. Når bilag omnummereres, kan du fortsætte med at bogføre kladden.

## <a name="see-also"></a>Se også
[Bogføre transaktioner direkte i finansposterne](finance-how-post-transactions-directly.md)  
[Tilbageføre poster](finance-how-reverse-journal-posting.md)  
[Fordele omkostninger og indtægter](year-allocate-costs-income.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
