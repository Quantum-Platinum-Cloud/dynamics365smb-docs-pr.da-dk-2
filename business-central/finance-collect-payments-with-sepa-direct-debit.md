---
title: SEPA-direkte debitering i Business Central
description: Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet med kundens samtykke.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '371, 423, 424, 427, 1208, 1207, 1230'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="collect-payments-with-sepa-direct-debit" />Indhente betalinger med SEPA Direct Debit

Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet med kundens samtykke.  

Opret først eksportformatet for bankfilen, der instruerer din bank i at udføre en Direct Debit. Derefter konfigureres kundens betalingsform. Til sidst oprettes den Direct Debit-betalingsaftale, der afspejler din aftale med kunden om opkrævning af deres betalinger i en bestemt periode i aftalen.  

For at instruere banken i at overføre det indbetalte beløb fra kundens bankkonto til din virksomheds konto, opretter du en post i den Direct Debit-opkrævning, der indeholder oplysninger om bankkonti, de berørte salgsfakturaer og den Direct Debit-betalingsaftale. Derefter eksporterer du en XML-fil, der er baseret på opkrævningsposten, som du sender til din bank til behandling. Du får besked fra banken om alle betalinger, der ikke kunne behandles af banken, og derefter skal du manuelt afvise de pågældende poster i den Direct Debit-opkrævning.  

Du kan angive standarddebitorsalgskoder med oplysninger om Direct Debit-betalingsform og -bemyndigelse. Du kan derefter bruge kørslen **Opret standardkundefakturaer** til at generere flere salgsfakturaer med oplysninger om Direct Debit udfyldt på forhånd. Dette kan udføres manuelt eller automatisk, alt efter betalingens forfaldsdato.  

Når betalinger er behandlet, og banken har informeret om det, kan du bogføre betalingskvitteringer enten direkte fra siden **Poster i Direct Debit-opkrævning** eller ved at flytte betalingslinjerne til den kladde, hvor du bogfører betalingskvitteringer, f.eks. siden **Indbetalingskladde**. Alternativt kan du, afhængigt af hvordan din likviditetsstyring foregår, vente og kun anvende betalingerne som en del af bankafstemningen.  

> [!NOTE]  
> Hvis du vil samle betalinger ved hjælp af SEPA Direct Debit, skal valutaen på salgsfakturaen være i EURO.  

## <a name="setting-up-sepa-direct-debit" />Konfigurere SEPA Direct Debit

Fra siden **Direct Debit-opkrævninger** kan du eksportere instruktioner til din netbank for at udføre en direkte debiteringsopkrævning fra debitorens bankkonto til din bankkonto ifølge SEPA Direct Debit-format.

> [!NOTE]
> Den globale version af [!INCLUDE[prod_short](includes/prod_short.md)] understøtter kun SEPA-debetformatet. Versionen for dit land/område kan understøtte andre formater til elektronisk betaling. Se under **Lokal funktionalitet** i indholdsfortegnelsen.  

For at aktivere eksport af bankfilformater, der ikke umiddelbart understøttes i [!INCLUDE[prod_short](includes/prod_short.md)], kan du konfigurere en dataudvekslingsdefinition ved hjælp af dataudvekslingsstrukturen. Du kan finde flere oplysninger i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

Før du kan behandle debitorbetalinger elektronisk ved eksport af instruktioner for direkte debitering i SEPA Direct Debit-format, skal du udføre følgende konfigurationstrin:  

* Konfigurer eksportformatet for den bankfil, der instruerer din bank i at udføre en Direct Debit-opkrævning fra kundens bankkonto til din bankkonto.  
* Konfigurer debitorens betalingsform.  
* Konfigurer den Direct Debit-betalingsaftale, der afspejler din aftale med kunden om opkrævning af deres betalinger i en bestemt periode i aftalen.  

### <a name="to-set-up-your-bank-account-for-sepa-direct-debit" />Sådan konfigureres din bankkonto til SEPA-Direct Debit

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Bankkonti**, og vælg derefter det relaterede link.  
2. Åbn den bankkonto, du vil bruge til Direct Debit.  
3. I oversigtspanelet **Overfør** i feltet **SEPA Direct Debit-format** skal du vælge indstillingen for SEPA Direct Debit.  

### <a name="to-set-up-the-customers-payment-method-for-sepa-direct-debit" />Sådan konfigureres kundens betalingsform til SEPA-Direct Debit

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Betalingsformer**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Definer en betalingsform. Udfyld de Direct Debit\-specifikke felter som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit**|Angiv, om betalingsformen er til SEPA-Direct Debit-opkrævning.|  
    |**Kode for Direct Debit-betalingsbetingelser**|Angiv betalingsbetingelser, f.eks. BETAL IKKE, der vises på salgsfakturaer, som betales med SEPA-Direct Debit for at angive over for kunden, at betalingen opkræves automatisk. Alternativt kan du lade feltet være tomt.|  

    > [!NOTE]  
    >  Angiv ikke en værdi i feltet **Kontonr.**.  

4. Vælg knappen **OK** for at lukke siden **Betalingsformer**.  
5. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
6. Åbn kortet for den kunde, som du vil konfigurere til SEPA Direct Debit-opkrævning.  
7. Vælg feltet **Betalingsformskode**, og vælg derefter den betalingsformskode, du har angivet i trin 3.  
8. Gentag trin 6 og 7 for alle de debitorer, som du vil konfigurere til SEPA Direct Debit-opkrævning.  

#### <a name="to-set-up-the-direct-debit-mandate-that-represents-the-customer-agreement" />Sådan konfigureres den Direct Debit-betalingsaftale, der repræsenterer kundeaftalen

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Kunder**, og vælg derefter det relaterede link.  
2. Åbn kortet for den kunde, som du vil konfigurere til SEPA Direct Debit.  
3. Vælg handlingen **Bankkonti**.  
4. På siden **Debitors bankkontooversigt** skal du vælge den debitorbankkonto, som skal bruge Direct Debiter, og derefter vælge handlingen **Direct Debit-betalingsaftaler** under fanen Startside i gruppen Proces.  
5. På siden **SEPA Direct Debit-betalingsaftaler** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Debitors bankkontokode**|Angiver den bankkonto, hvorfra der opkræves Direct Debit\-betalinger. Dette felt udfyldes automatisk.|  
    |**Gyldig fra**|Angiv den dato, hvor Direct Debit\-betalingsaftalen starter.|  
    |**Gyldig til**|Angiv den dato, hvor Direct Debit\-betalingsaftalen slutter.|  
    |**Underskriftsdato**|Angiv den dato, når kunden har underskrevet Direct Debit\-betalingsaftalen.|  
    |**Betalingstype**|Angiv, om aftalen dækker flere (**Tilbagevendende betaling**) eller en enkelt (**Engangsbetaling**) Direct Debit-opkrævning.|  
    |**Forventet antal debiteringer**|Angiv, hvor mange Direct Debit-opkrævninger du forventer at foretage. Dette felt er kun relevant, hvis du har markeret **Tilbagevendende betaling** i feltet **Betalingstype**.|  
    |**Debettæller**|Angiver, hvor mange Direct Debit\-opkrævninger, der er foretaget ved hjælp af denne Direct Debit\-betalingsaftale. Dette felt opdateres automatisk.|  
    |**Spærret**|Angiv, at der ikke kan foretages Direct Debit\-opkrævninger ved hjælp af denne Direct Debit\-betalingsaftale.|  

6. Gentag trin 1 til 5 for alle de debitorer, som du vil konfigurere til SEPA Direct Debit.  

 Direct Debit-betalingsaftalen indsættes automatisk i feltet **Id for Direct Debit-betalingsaftale**, når du opretter en salgsfaktura til den debitor, som du valgte i trin 2. Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).

## <a name="creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file" />Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil

For at instruere banken i at overføre det indbetalte beløb fra kundens bankkonto til din virksomheds konto, opretter du en post i den Direct Debit-opkrævning, der indeholder oplysninger om kundens bankkonto, de berørte salgsfakturaer og den Direct Debit-betalingsaftale. Fra posten i den direkte debiteringsopkrævning, som fås som resultat, kan du derefter eksportere en XML-fil, som du sender eller overfører til din elektroniske bank til behandling. Du får besked fra banken om alle betalinger, der ikke kunne behandles af banken, og derefter skal du manuelt afvise de pågældende poster i Direct Debit-opkrævningen.  

 > [!NOTE]  
 > Hvis du vil samle betalinger ved hjælp af SEPA Direct Debit, skal valutaen på salgsfakturaen være i EURO.  

### <a name="to-create-a-direct-debit-collection" />Sådan oprettes en direkte debiteringsopkrævning

 1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.  
 2. På siden **Direct Debit-opkrævninger** skal du vælge handlingen **Opret Direct Debit-opkrævning**.  
 3. På siden **Opret Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Fra forfaldsdato**|Angiv den tidligste forfaldsdato for betaling på salgsfakturaer, som du vil oprette en direkte debiteringsopkrævning for.|  
    |**Til forfaldsdato**|Angiv den seneste forfaldsdato for betaling på salgsfakturaer, som du vil oprette en direkte debiteringsopkrævning for.|  
    |**Partnertype**|Angiver, om der foretages direkte debiteringsopkrævning for debitorer af typen **Virksomhed** eller **Person**.|  
    |**Kun kunder med gyldig bemyndigelse**|Angiv, om der oprettes en Direct Debit-opkrævning for debitorer, der har en gyldig Direct Debit-betalingsaftale. **Bemærk:** Der oprettes en Direct Debit-opkrævning, også selvom feltet **Id for Direct Debit-betalingsaftale** ikke er udfyldt på salgsfakturaen.|  
    |**Kun fakturaer med gyldig betalingsaftale**|Angiv, om der kun oprettes en Direct Debit-opkrævning for salgsfakturaer, hvis der er valgt en gyldig Direct Debit-betalingsaftale i feltet **Id for Direct Debit-betalingsaftale** på salgsfakturaen.|  
    |**Bankkontonr.**|Angiv, hvilke af firmaets bankkonti den opkrævede betaling skal overføres til fra debitors bankkonto.|  
    |**Bankkontonavn**|Angiver navnet på den bankkonto, som du vælger i feltet **Bankkontonr.**. Dette felt udfyldes automatisk.|  

 4. Vælg knappen **OK**.  

Der føjes en Direct Debit-opkrævning til siden **Direct Debit-opkrævninger**, og der oprettes en eller flere poster med Direct Debit-opkrævning.  

### <a name="to-export-a-direct-debit-collection-entry-to-a-bank-file" />Sådan eksporteres en post i en direkte debiteringsopkrævning til en bankfil

 1. På siden **Direct Debit-opkrævninger** skal du vælge handlingen **Poster i Direct Debit-opkrævning**.  
 2. På siden **Poster i Direct Debit-opkrævning** skal du markere den post, du vil eksportere, og derefter vælge handlingen **Opret fil til Direct Debit**.  
 3. Gem eksportfilen på det sted, hvorfra du sender eller overfører den til din elektroniske bank.  

      På siden **Poster i Direct Debit-opkrævning** ændres feltet **Status for Direct Debit-opkrævning** til Fil oprettet. På siden **SEPA Direct Debit-betalingsaftaler** opdateres feltet **Debettæller** med et styk.  

 Hvis den eksporterede fil ikke kan behandles, f.eks. fordi debitoren er insolvent, kan du afvise posten i den direkte debiteringsopkrævning. Hvis den eksporterede fil er blevet behandlet af banken, opkræves forfaldne betalinger for de involverede salgsfakturaer automatisk fra de berørte debitorer. I så fald kan du lukke opkrævningen.  

### <a name="to-reject-a-direct-debit-collection-entry" />Sådan afvises en post i en direkte debiteringsopkrævning

* På siden **Poster i Direct Debit-opkrævning** skal du markere den post, der ikke blev behandlet korrekt, og derefter vælge handlingen **Afvis post**.  

    På siden **Poster i Direct Debit-opkrævning** ændres feltet **Status** til **Afvist**.  

### <a name="to-close-a-direct-debit-collection" />Sådan lukkes en direkte debiteringsopkrævning

* På siden **Poster i Direct Debit-opkrævning** skal du markere den post, der ikke blev behandlet korrekt, og derefter vælge handlingen **Luk opkrævning**.  

    Den relaterede direkte debiteringsopkrævning er lukket.  

 Du kan nu fortsætte med at bogføre kvitteringer for betalinger for de involverede salgsfakturaer. Du kan gøre dette, mens du typisk bogfører betalingskvitteringer, f.eks. på siden **Betalingsregistrering**, eller du kan bogføre de relaterede betalingskvitteringer direkte fra siden **Poster i Direct Debit-opkrævning**. Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

## <a name="posting-sepa-direct-debit-payment-receipts" />Bogføring af SEPA Direct Debit-betalingskvitteringer

Når en Direct Debit-opkrævning er behandlet af din bank, kan du fortsætte med at bogføre kvittering for betaling for de involverede salgsfakturaer. Du kan finde flere oplysninger i [Oprette poster i SEPA Direct Debit-opkrævning og eksportere til en bankfil](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file).  

Du kan bogføre betalingskvitteringen direkte fra siden **Direct Debit-opkrævninger** eller siden **Poster i Direct Debit-opkrævning**. Alternativt kan du overføre arbejdet til en anden bruger ved at udarbejde de relaterede kladdelinjer.  

### <a name="to-post-a-direct-debit-payment-receipt-from-the-direct-debit-collections-page" />Sådan bogføres en betalingskvittering i Direct Debit fra siden Direct Debit-opkrævninger

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Direct Debit-opkrævninger**, og vælg derefter det relaterede link.  
2. Vælg en linje for en Direct Debit-opkrævning, der er eksporteret til en bankfil og er blevet behandlet af banken.
3. Vælg handlingen **Bogfør betalingskvitteringer**.  
4. På siden **Bogfør Direct Debit-opkrævning** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Direct Debit-opkrævningsnr.**|Angiv den Direct Debit-samling, som du vil bogføre betalingskvittering for.|  
    |**Finanskladdetype**|Angiv, hvilken finanskladdeskabelon der skal bruges til bogføring af betalingskvitteringen, f.eks. skabelonen til indbetalinger.|  
    |**Finanskladdenavn**|Angiv, hvilket finanskladdenavn der skal bruges til bogføring af betalingskvitteringen.|  
    |**Opret kun kladde**|Markér dette afkrydsningsfelt, hvis du ikke vil bogføre betalingskvitteringen, når du vælger knappen **OK**. Kvitteringen for betalingen forberedes i den angivne journal og vil ikke blive bogført, før nogen bogfører de pågældende kladdelinjer.|  

5. Vælg knappen **OK**.

## <a name="see-also" />Se også

[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Service Management](service-service.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
