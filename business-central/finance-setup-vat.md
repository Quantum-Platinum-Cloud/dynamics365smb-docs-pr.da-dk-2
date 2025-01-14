---
title: Konfigurere moms
description: Sørg for at beregne, bogføre og rapportere moms på køb og salg korrekt. Du anbefales at bruge den assisterede opsætningsvejledning, når du konfigurerer moms.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, posting, tax, value-added tax
ms.search.form: 10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,
ms.date: 12/01/2022
ms.author: bholtorf
ms.openlocfilehash: d401e6d9a0b8fb4f05bcc379322b2f81bfc03c57
ms.sourcegitcommit: 12ff9dcbefb47f2280479cceb656ea7e6ac2cfa1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/02/2022
ms.locfileid: "9822410"
---
# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Konfigurere beregnings- og bogføringsmetoder for moms

Forbrugere og virksomheder betaler moms, når de køber varer eller tjenesteydelser. Momsbeløbet, der skal betales, kan variere afhængigt af flere faktorer. I [!INCLUDE[prod_short](includes/prod_short.md)] konfigurerer du moms til at angive de satser, der bruges til at beregne momsbeløb baseret på følgende parametre:

* Hvem du sælger til  
* Hvem du køber fra  
* Hvad du sælger  
* Hvad du køber.  

Du kan konfigurere momsberegninger manuelt, men der kan være svært og tidskrævende. Det er fordi, det er nemt at bruge forskellige momssatser utilsigtet og gøre rapporter vedrørende moms unøjagtige. Det anbefales, at du bruger den assisterende **momsopsætnings**-vejledning i produktet for at gøre moms opsætningen nemmere. 

Hvis du selv vil konfigurere momsberegninger eller bare vil vide mere om de enkelte trin, indeholder i denne artikel beskrivelser af de enkelte trin:  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Konfigurer moms ved hjælp af den assisterede momsopsætningsvejledning (anbefales)

> [!NOTE]
> Du kan kun bruge **momsopsætningsvejledningen**, hvis du har oprettet *Min virksomhed* og endnu ikke har bogført transaktioner, der omfatter moms.

For at starte vejledningen skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og skriv **Assisteret opsætning**. 
2. Vælg **Konfigurer moms**, og fuldfør trinnene.
3. Når du har fuldført den assisterede opsætning, skal du gå til siden **Momsbogf.opsætning** og kontrollere, om du er nødt til at udfylde flere felter i henhold til de landespecifikke krav for din version af [!INCLUDE [prod_short](includes/prod_short.md)]. Flere oplysninger i [Lokal funktionalitet i Business Central](about-localization.md).  

### <a name="check-the-vat-posting-setup"></a>Kontrollere momsbogføringsopsætningen

For at understøtte dig i hurtig start viser [!INCLUDE [prod_short](includes/prod_short.md)] notifikationer, hvis du mangler finanskonti i bogføringsgrupper eller bogføringsopsætninger, f. eks siden **Momsbogføringsopsætning**. Du kan skifte denne type notifikation til eller fra ved hjælp af *finanskonti, der mangler i bogføringsgruppe eller installationsmeddelelse* på siden **Mine notifikationer**. Gå til siden **Mine indstillinger**, og vælg *Ændr, når jeg modtager notifikationer.* link.  

Hvis du vælger en sådan notifikation, opretter [!INCLUDE [prod_short](includes/prod_short.md)] automatisk disse bogføringsopsætninger på basis af bogføringsgrupperne i det dokument eller den kladde, du arbejder på.  

På dette tidspunkt kan du nøjes med at udfylde de manglende finanskonti. Men når du senere indsnævrer installationen yderligere, kan du muligvis se, at denne første installation er forkert. Og [!INCLUDE [prod_short](includes/prod_short.md)] tillader ikke sletning af Momsbogføringsopsætning og Bogføringsopsætning, når der er oprettet poster, der er oprettet på baggrund af sådanne varianter. Så fra 2022 udgivelsesbølge 1 kan du bruge feltet **Spærret** på **Bogføringsopsætnings**-siden til at forhindre, at brugere kommer til at følge med en opsætning, der ikke længere er relevant for nye posteringer.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>Oprette en standardmomsdato for dokumenter og kladder
Momsrapportering i [!INCLUDE [prod_short](includes/prod_short.md)] er baseret på **momsdatoen** for at medtage momsposter i momsrapporter i en momsperiode. Momsdatoen kan ændres på alle dokumenter og kladder, men du skal angive en standardværdi for momsdatoen.

> [!NOTE]
> Efter bogføring af dokumentet eller kladden, vises som **momsdatoen** på **momsposter** og **finansposter** samt på det bogførte dokument, hvis det findes.

Benyt følgende fremgangsmåde for at angive en standardværdi for en momsdato:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 1.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, og skriv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. I oversigtspanelet **Generelt** i feltet **Standardmomsdato** skal du vælge **Bogføringsdato** eller **Bilagsdato**.
3. Luk siden.  

> [!NOTE]
> Som standard er **standardmomsdatoen** **bogføringsdatoen**.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Konfigurere momsregistreringsnumre for dit land eller område

For at sikre, at brugere angiver gyldige momsregistreringsnumre, kan du definere formater til momsregistreringsnumre, som bruges i de lande eller områder, hvor du handler. [!INCLUDE[prod_short](includes/prod_short.md)] viser en fejlmeddelelse, hvis en bruger laver en fejl eller bruger et format, der er forkert for landet eller området.

For at oprette momsregistreringsnumre, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 2.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Lande/områder**.
2. Vælg landet eller området, og vælg derefter handlingen **SE/CVR-nr.formater**.
3. I feltet **Formater** skal du angive formatet ved at angive et eller flere af følgende tegn:  

* **#** Kræver et etcifret tal.  
* **@** Kræver et bogstav. Dette format skelner ikke mellem store og små bogstaver.  
* **?** Tillader alle tegn.  

    > [!TIP]
    > Du kan bruge andre tegn, så længe de er altid findes i formatet for landet eller området. Hvis du f.eks. vil medtage et punktum eller en bindestreg mellem sæt af tal, kan du angive formatet som ##.####.### eller @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Konfigurere momsvirksomhedsbogføringsgrupper

Formålet med momsvirksomhedsbogføringsgrupper er at repræsentere de markeder, hvor du handler med debitorer og kreditorer, og definere, hvordan moms beregnes og bogføres på hvert enkelt marked. Eksempler på momsvirksomhedsbogføringsgrupper er **Danmark** og **Den Europæiske Union (EU)**.  

Brug koder, der er lette at huske, og som beskriver virksomhedsbogføringsgruppen, f.eks. **EU**, **Ikke-EU** eller **Danmark**. Hver kode skal være unik, så du kan oprette lige så mange koder, som du har brug for, men du kan kun bruge den samme kode én gang i en tabel.

Når du vil oprette en momsvirksomhedsbogføringsgruppe, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 3.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsvirksomhedsbogf.grupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

Du kan oprette standardmomsvirksomhedsbogføringsgrupper ved at linke dem til virksomhedsbogføringsgrupper. [!INCLUDE[prod_short](includes/prod_short.md)] tildeler automatisk momsvirksomhedsbogføringsgruppen, når du tildeler virksomhedsbogføringsgruppen til en debitor, kreditor eller finanskonto.

## <a name="set-up-vat-product-posting-groups"></a>Konfigurere momsproduktbogføringsgrupper

Momsproduktbogføringsgrupper repræsenterer de varer eller ressourcer, du køber eller sælger, og bestemmer, hvordan moms beregnes og bogføres i overensstemmelse med typen af vare eller ressource.

Det anbefales at bruge koder, der er lette at huske, og som beskriver satsen, som f.eks. **FRITAGET** eller **Nul**, **MOMS10** eller **Reduceret** for 10 procent moms og **MOMS25** eller **Standard** for 25 procent.

Når du vil oprette en momsvirksomhedsbogføringsgruppe, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 4.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsproduktbogf.grupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Kombinere momsbogføringsgrupper i momsbogføringsopsætninger

[!INCLUDE[prod_short](includes/prod_short.md)] beregner momsbeløb af køb og salg baseret på momsbogføringsgrupper, der er kombinationer af momsvirksomheds- og -produktbogføringsgrupper. For hver kombination kan du angive momsprocenten, momsberegningstypen og finanskontonumre for bogføring af købs-, salgs- og modtagermoms. Du kan også angive, om moms skal genberegnes, når en kontantrabat anvendes eller modtages.  

Du kan definere et ubegrænset antal kombinationer. Hvis du vil gruppere kombinationer af momsbogføringsopsætninger med lignende attributter, kan du angive et **Moms-id** for hver enkelt gruppe og tildele id'et til gruppemedlemmerne.

Hvis du vil kombinere momsbogføringsopsætninger, skal du gøre følgende:

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 5.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Tildele momsbogføringsgrupper til flere enheder som standard

Hvis du vil anvende de samme momsbogføringsgrupper på flere enheder, kan du konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at gøre det som standard. Dette kan gøres på flere måder:

* Du kan tildele momsvirksomhedsbogføringsgrupper til generelle virksomhedsbogføringsgrupper eller debitor- eller kreditorskabeloner
* Du kan tildele momsproduktbogføringsgrupper til generelle produktbogføringsgrupper  

Momsvirksomheds- eller produktbogføringsgruppen tildeles, når du vælger en virksomheds- eller produktbogføringsgruppe til en debitor, kreditor, vare eller ressource.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Tildele momsbogføringsgrupper til konti, debitorer, kreditorer, varer og ressourcer

I følgende afsnit beskrives, hvordan du tildeler momsbogføringsgrupper til individuelle poster.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Sådan tildeles momsbogføringsgrupper til individuelle finanskonti

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 6.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
2. Åbn **Finanskonto**-kortet for kontoen.  
3. I oversigtspanelet **Bogføring** i feltet **Bogføringstype** skal du vælge enten **Salg** eller **Køb**.  
4. Vælg de momsbogføringsgrupper, du vil bruge til salgs- eller købskontoen.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Sådan tildeles momsvirksomhedsbogføringsgrupper til debitorer og kreditorer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 7.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.  
2. Udvid oversigtspanelet **Fakturering** på **Debitor**- eller **Kreditor**-kortet.  
3. Vælg momsvirksomhedsbogføringsgruppen.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Sådan tildeles momsproduktbogføringsgrupper til individuelle varer og ressourcer

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 8.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Vare** eller **Ressource**, og vælg derefter det relaterede link.  
2. Gør ét af følgende:  

    * På kortet **Vare** skal du udvide oversigtspanelet **Pris og bogføring** og derefter vælge **Vis mere** for at se feltet **Momsproduktbogf.gruppe**.  
    * Udvid oversigtspanelet **Fakturering** på **Ressource**-kortet.  
3. Vælg momsproduktbogføringsgruppen.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Konfigurere klausuler, der forklarer momsfritagelse eller ikke-standard-momssatser

Du konfigurerer en momsklausul til at beskrive oplysninger om den moms, der skal anvendes. Oplysningerne kan være påkrævet som påbudt af myndighederne. Når du har konfigureret en momsklausul og tilknyttet den til en momsbogføringsgruppe, vises momsklausulen på udskrevne salgsdokumenter, der bruger momsbogføringsopsætningsgruppen.

Hvis det er nødvendigt, kan du også angive, hvordan momsklausuler skal oversættes til andre sprog. Når du derefter opretter og udskriver et salgsdokument, der indeholder et moms-id, vil det udskrevne dokument indeholde den oversatte momsklausul. Den sprogkode, der er angivet på debitorkortet, bestemmer sproget.

Når ikke-standard-momssatsen anvendes i forskellige typer dokumenter, f.eks. fakturaer eller kreditnotaer, skal virksomheder normalt angive en fritagelsestekst (momsklausul) om, hvorfor der er beregnet en nedsat moms eller ingen moms. Du kan definere forskellige momsklausuler, der skal indgå i forretningsdokumenter, f.eks. faktura eller kreditnota. Dette gøres på siden **Momsklausuler efter dok.type**.

Du kan redigere eller slette en momsklausul, og dine ændringer afspejles i en genereret rapport. Men [!INCLUDE[prod_short](includes/prod_short.md)] bevarer ikke en oversigt over ændringen. På rapporten udskrives og vises momsklausulbeskrivelserne for alle linjer i rapporten sammen med momsbeløbet og momsgrundbeløbet. Hvis en momsklausul ikke er defineret for alle linjer i salgsdokumentet, så udelades hele sektionen, når rapporten udskrives.

### <a name="to-set-up-vat-clauses"></a>Sådan konfigureres momsklausuler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 9.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Oprette en ny linje på siden **Momsklausuler**.  
3. Angiv et id for klausulen i feltet **Kode**. Du bruger koden til at tildele klausulen til momsbogføringsgrupper.  
4. I feltet **Beskrivelse** skal du angive den momsfritagelse, du vil have vist i dokumenter, som kan inkludere moms. I feltet **Beskrivelse 2** skal du angive mere tekst, hvis det er nødvendigt. Teksten vises på nye dokumentlinjer.
5. Vælg handlingen **Beskrivelse efter dokumenttype**.
6. Udfyld felterne på siden **Momsklausuler efter dok.type** for at angive, hvilken momsfritagelsestekst der skal vises for hvilken dokumenttype.  
7. Valgfrit: Hvis du vil tildele momsklausulen til en momsbogføringsopsætning med det samme, skal du vælge **Opsætning** og derefter vælge klausulen. Hvis du vil vente, kan du tildele klausulen senere på siden **Momsbogf.opsætning**.  
8. Valgfrit: Hvis du vil angive, hvordan momsklausulen skal oversættes, skal du vælge handlingen **Oversættelser**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Sådan tildeles en momsklausul til en momsbogføringsopsætning

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 10.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.  
2. I kolonnen **Momsklausul** skal du vælge den klausul, der skal bruges til hver momsbogføringsopsætning, den gælder for.  

### <a name="to-specify-translations-for-vat-clauses"></a>Sådan angives oversættelser af momsklausuler

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 11.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Oversættelser**.  
3. I feltet **Sprogkode** skal du vælge det sprog, du vil oversætte til.  
4. I felterne **Beskrivelse** og **Beskrivelse 2** skal du angive oversættelserne af beskrivelserne. Teksten vises i de oversatte momsrapportdokumenter.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>Sådan angives udvidet tekst til momsklausuler

> [!NOTE]  
> Hvis dit land eller område kræver længere tekst til momsklausuler end standardversionen, kan du angive en længere tekst for moms delsætningen som *udvidet tekst*, så den udskrives på salgs-og købsrapporterne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 11.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsklausuler**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Udvidede tekster**.  
3. Vælg handlingen **Ny**.  
4. Udfyld felterne **Sprogkode** og **Beskrivelse**.  
5. Alternativt kan du vælge feltet **Alle sprogkoder** eller angive det relevante sprog i feltet **Sprogkode**, hvis du bruger sprogkoder.  
6. Udfyld felterne **Startdato** og **Slutdato**, hvis du vil begrænse den tid, hvor den udvidede tekst bruges.  
7. Skriv den udvidede tekst til moms klausulerne på **Tekst**-linjerne.  
8. Markér de relevante felter for de dokumenttyper, hvor den udvidede tekst skal udskrives.  
9. Luk siden.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Oprette en momsbogføringsopsætning for at håndtere importmoms

Du kan bruge funktionen *Importmoms*, når du skal bogføre et dokument, hvor hele beløbet er moms. Du skal bruge funktionen, hvis du modtager en faktura fra skattemyndighederne for moms på importerede varer.  

Når du vil konfigurere koder for importmoms, skal du gøre følgende:  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 12.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Momsproduktbogf.grupper**, og vælg derefter det relaterede link.  
2. På siden Momsproduktbogf.grupper. skal du oprette en ny momsproduktbogføringsgruppe for importmoms.  
3. Vælg ![Lightbulb, der åbner funktionen Fortæl mig 13.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Momsbogf.opsætning**, og vælg derefter det relaterede link.  
4. På siden Opsætning af momsbogføring skal du oprette en ny linje eller bruge en eksisterende momsvirksomhedsbogføringsgruppe kombineret med den nye momsproduktbogføringsgruppe til importmoms.  
5. I feltet **Momsberegningstype** skal du vælge **Momskorrektion**.  
6. Angiv den finanskonto, der skal bruges til bogføring af importmoms, i feltet **Købsmomskonto**. Alle andre konti er valgfrie.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Bruge modtagermoms for handel mellem EU-lande eller -områder

Nogle virksomheder skal bruge modtagermoms, når de handler med andre virksomheder. Denne regel gælder f.eks. for køb fra EU-lande/områder og salg til EU-lande/områder.  

> [!NOTE]  
> Reglen gælder, når der handles med de virksomheder, som er registreret som momspligtige i et andet EU-land. Hvis du handler direkte med forbrugere i andre EU-lande/område, skal du kontakte skattemyndighederne for at få oplyst de gældende momsregler.  

> [!TIP]  
> Du kan kontrollere, at en virksomhed er registreret som momspligtig i et andet EU-land ved hjælp af tjenesten til kontrol af SE/CVR-nr. for EU. Tjenesten er tilgængelig og gratis i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan finde flere oplysninger i [Kontrollere CVR-numre](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Salg til EU-lande eller -områder

Moms beregnes ikke på salg til momspligtige virksomheder i andre EU-lande/regioner. Du skal rapportere værdien af disse salg til EU-lande/områder separat på momsangivelsen.  

For at beregne moms på salg til EU-lande/områder korrekt, skal du:  

* Opret linjer for salg med de samme oplysninger for køb. Hvis du allerede har oprettet linjer på siden **Momsbogf.opsætning** for køb fra EU-lande/områder, kan du også bruge disse linjer til salg.  
* Tildele momsvirksomhedsbogføringsgrupperne i feltet **Momsvirksomhedsbogf.gruppe** på oversigtspanelet **Fakturering** på kreditorkort for hver EU-kreditor. Du skal også angive debitorens CVR-nummer i feltet **SE/CVR-nr.** på oversigtspanelet **Udenrigshandel**.  

Når du bogfører salg til en debitor i et andet EU-land/område, beregnes momsbeløbet, og der oprettes en momspost med oplysningerne om modtagermomsen og momsgrundbeløbet, som er det beløb, der bruges til at beregne momsbeløbet. Der bogføres ingen poster på momskontoen i finansposterne.

Hvis du vil bruge en kombination af momsvirksomheds- og momsproduktbogføringsgruppe til rapportering som tjenester i de periodiske momsrapporter, skal du markere feltet **EU-tjeneste**.

> [!NOTE]  
> Feltet **EU-tjeneste** gælder kun for momsrapporter. Feltet er ikke relateret til funktionerne **Servicedeklaration** eller **Intrastat for service** .

## <a name="vat-rounding-for-documents"></a>Momsafrunding for bilag

Beløb i de bilag, som endnu ikke er blevet bogført, afrundes og vises, så de svarer til de endelige afrundingsbeløb, som bogføres. Moms beregnes for et helt dokument, hvilket betyder, at moms, der beregnes, er baseret på summen af alle linjer med samme moms-id i dokumentet.  

## <a name="set-up-vat-reporting"></a>Konfigurer momsrapportering

Du skal angive oplysninger om, hvordan skattemyndighederne i dit land kræver, at du indsender momsrapporter. Følgende fremgangsmåde viser de mest almindeligt brugte oplysninger. Dit land eller område kan dog kræve yderligere trin. Du kan finde flere oplysninger i den relevante artikel i afsnittet *lokal funktionalitet* i panelet til venstre.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-related-microsoft-training"></a>Se relateret [Microsoft-træning](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also"></a>Se også

[Konfigurere momsangivelsestyper og momsangivelsesnavne](finance-how-setup-vat-statement.md)  
[Konfigurere ikke-realiseret moms](finance-setup-unrealized-vat.md)  
[Rapportere moms til skattemyndighederne](finance-how-report-vat.md)  
[Arbejde med moms af salg og køb](finance-work-with-vat.md)  
[Arbejde med Momssatsændringsværktøj](finance-how-use-vat-rate-change-tool.md)  
[Kontrollere SE/CVR-numre](finance-how-validate-vat-registration-number.md)  
[Lokal funktionalitet i Business Central](about-localization.md)  
[Momslisterapportering i den tyske version](LocalFunctionality/Germany/vat-reporting.md)  
[Belgisk moms](LocalFunctionality/Belgium/belgian-vat.md)  
[Italiensk moms](LocalFunctionality/Italy/italian-vat.md)  
[Oprette elektroniske moms-og ICP-opgørelser i den hollandske version](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[Momslisterapportering i den spanske version](LocalFunctionality/Spain/vat-reports.md)  
[Konfigurere momsbogføring af varer og ydelser i den australske version](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[Moms i den tjekkiske version](LocalFunctionality/Czech/finance-vat.md)  
[Momsindberetning i den norske version](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Rapportering af vare- og tjenestemoms og harmoniseret salgsmoms i Canada](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
