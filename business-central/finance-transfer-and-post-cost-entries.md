---
title: Overførsel og bogføring af omkostningsposter
description: 'Inden du definerer omkostningsfordelinger, skal du forstå de forskellige kilder, omkostningsposterne kommer fra.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '1100, 1103, 1104, 1108, 1113, 1135'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="transferring-and-posting-cost-entries" />Overførsel og bogføring af omkostningsposter

Inden du definerer omkostningsfordelinger, skal du forstå, hvordan omkostningsposter kommer fra følgende kilder:  

- Automatisk overførsel af finansposter.  
- Manuel kostprisbogføring for rene omkostningsposter, interne afgifter og manuelle allokeringer.  
- Automatisk tildeling af bogføringer for faktiske omkostninger.  
- Overførsel af budgetposter til faktiske.

## <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries" />Kriterier for overførsel af finansposter til omkostningsposter

Det er vigtigt at forstå kriterierne for overførsel af finansposter til prisposter. Under overførslen bruger kørslen **Overfør finansposter til CA** følgende kriterier til at fastslå, om og hvordan finansposterne overføres.  

Finansposter overføres i følgende tilfælde:  

- Posterne har dimensionsværdier, der svarer til enten et omkostningssted eller et omkostningsobjekt.  
- Posterne har dimensionsværdier, der svarer til et omkostningssted og et omkostningsobjekt. For disse poster har omkostningsstedet forrang. Dette hjælper med at undgå en situation, hvor en omkostningstype vises i både et omkostningsobjekt og et omkostningssted og derfor tælles to gange i statistikken.  
- Dokumentnummeret i posterne er tomt, så det vises med dokumentnummeret 0000 i omkostningsposterne.  
- Posterne overføres til en omkostningstype, der giver mulighed for samlede poster, og disse poster overføres som en samlet post enten hver måned eller hver dag.  

Finansposter overføres ikke i følgende tilfælde:  

- Posterne har dimensionsværdier, der ikke svarer til et omkostningssted eller et omkostningsobjekt.  
- Posterne har værdien nul.  
- Posterne har en finanskonto, der er blevet slettet.  
- Posterne har en finanskonto, der ikke er af typen **Resultatopgørelse**.  
- Posterne har en finanskonto, der ikke er tildelt en omkostningstype.  
- Posterne har en bogføringsdato før **Startdato for finansoverførsel**.  
- Posterne er blevet bogført med en ultimodato. De er typisk poster, der fører resultatopgørelsens saldo tilbage i slutningen af året.

## <a name="transferring-general-ledger-entries-to-cost-entries" />Overførsel af finansposter til omkostningsposter

Du kan overføre finansposter til omkostningsposter.  

Inden du kører processen til overførsel af finansposter til omkostningsposter, skal du forberede overførslen for at undgå manuel korrektionsbogføring.  

### <a name="to-prepare-the-transfer" />Sådan forberedes overførslen

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Konfiguration af omkostningsregnskab**, og vælg derefter det relaterede link.  
2.  På siden **Konfiguration af omkostningsregnskab** skal du kontrollere, at feltet **Startdato for finansoverførsel** er angivet til den korrekte værdi.  
3.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Omkostningstyper**, og vælg derefter det relaterede link.  
4.  På siden **Omkostningstypekort** skal du kontrollere, at feltet **Finanskontointerval** er sammenkædet korrekt for hver pristype for at tage poster fra regnskabet.  
5.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kontoplan**, og derefter vælge det relaterede link.  
6.  For hver relevant finanskonto skal du på siden **Finanskontokort** kontrollere, at feltet **Omkostningstypenr.** er korrekt knyttet til en omkostningstype. Du kan finde flere oplysninger i [Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md).  
7.  Kontroller, at alle relevante finansposter har dimensionsværdier, der svarer til et omkostningssted og et omkostningsobjekt.  

### <a name="to-transfer-general-ledger-entries-to-cost-entries" />Sådan overføres finansposter til omkostningsposter

1.  Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Overfør finansposter til omkostningsregnskab** , og vælg derefter det relaterede link.  
2.  Vælg knappen **Ja** for at starte overførslen. Processen overfører alle finansposter, der ikke allerede er overført.  

Under overførslen opretter processen forbindelser i posterne i tabellen **Omkostningspost** og tabellen **Omkostningsregister**. Dette gør det muligt at spore kilden til omkostningsposter.

## <a name="automatic-transfer-and-combined-entries" />Automatisk overførsel og kombinerede poster

I omkostningsregnskab kan du overføre finansposter til en pristype ved hjælp af kombineret bogføring. Du kan angive, om en pristype modtager samlede poster i feltet **Saml poster** i pristypedefinitionen. Den følgende tabel beskriver de forskellige indstillinger.  

|Saml poster|Beskrivelse|  
|---------------------|-----------------|  
|Ingen|Alle finansposter overføres individuelt til den tilsvarende pristype.|  
|DAG|Finansposter med den samme bogføringsdato overføres som én post til den tilsvarende pristype.|  
|Måned|Alle finansposter i den samme kalendermåned overføres som én post til den tilsvarende pristype.|  

> [!IMPORTANT]  
>  Hvis du har markeret afkrydsningsfeltet **Automatisk overførsel fra finans** på siden **Konfiguration af omkostningsregnskab**, opdaterer [!INCLUDE[prod_short](includes/prod_short.md)] omkostningsregnskabet efter hver bogføring i regnskabet. Kombinerede poster er ikke mulige.

## <a name="results-of-transferring-general-ledger-entries-to-cost-entries" />Resultater af overførsel af finansposter til omkostningsposter.

Under overførslen af regnskabsposter til omkostningsposter opretter [!INCLUDE[prod_short](includes/prod_short.md)] forbindelser i posterne i tabellen **Finanspost**, tabellen **Omkostningspost** og tabellen **Omkostningsregister** for at gøre det muligt at spore forbindelserne mellem omkostningsposter og regnskabsposter.  

### <a name="general-ledger-entries" />Finansposter

For hver regnskabspost, der overføres til omkostningsregnskab, udfylder [!INCLUDE[prod_short](includes/prod_short.md)] omkostningsfeltet **Løbenr.**.  

### <a name="cost-entries" />Omkostningsposter

For hver omkostningspost gemmer [!INCLUDE[prod_short](includes/prod_short.md)] løbenummeret på den tilsvarende regnskabspost i feltet **Finansløbenr.** i tabellen **Omkostningspost**.  

For samlede omkostningsposter gemmer [!INCLUDE[prod_short](includes/prod_short.md)] løbenummer på den sidste regnskabspost, som er posten med det højeste løbenummer.  

Feltet **Finanskonto** i tabellen **Omkostningspost** indeholder nummeret på den finanskonto, som omkostningsposten stammer fra.  

For enkelte omkostningsposter overfører [!INCLUDE[prod_short](includes/prod_short.md)] bogføringsteksten fra regnskabsposten til tekstfeltet **Beskrivelse**. For kombinerede poster viser tekstfeltet, at disse poster er overfører som kombinerede poster. For eksempel kan teksten for en kombineret post for oktober 2013 være **Kombinerede poster, oktober 2013**.  

### <a name="cost-register" />Omkostningsregister

I tabellen **Omkostningsregister** opretter [!INCLUDE[prod_short](includes/prod_short.md)] en post med kildeoverførsel fra regnskabet. Posten registrerer det første og sidste løbenummer for de finansposter, der overføres, foruden første og sidste postnummer på de omkostningsposter, der er oprettet.

## <a name="see-related-microsoft-trainingtrainingmodulestransfer-gl-entries-dynamics-365-business-central" />Se relateret [Microsoft-træning](/training/modules/transfer-gl-entries-dynamics-365-business-central/)

## <a name="see-also" />Se også

 [Om omkostningsregnskab](finance-about-cost-accounting.md)  
 [Konfigurere omkostningsregnskab](finance-set-up-cost-accounting.md)  
 [Definere og allokere omkostninger](finance-define-and-allocate-costs.md)  
 [Regnskab for omkostninger](finance-manage-cost-accounting.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
