---
title: Forsikring af anlægsaktiver
description: Du kan knytte et eller flere anlægsaktiver til en forsikringspolice ved at bogføre forsikringsposterne fra siden **Forsikringskladde**.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'policy, coverage'
ms.search.form: '5647, 5644, 5653, 5651, 5655, 5652, 5645, 5656, 5646, 5648, 9275'
ms.date: 06/29/2021
ms.author: edupont
---
# <a name="insure-fixed-assets" />Forsikring af anlægsaktiver
En forsikringspolice for et anlægsaktiv repræsenteres af et forsikringskort. Du kan knytte et anlægsaktiv til en forsikringspolice eller flere anlægsaktiver til en forsikringspolice.

Du kan knytte et anlægsaktiv til en forsikringspolice ved at bogføre forsikringsposterne fra siden **Forsikringskladde**.

Du kan også knytte et anlægsaktiv til en forsikringspolice og oprette forsikringsposter, når du bogfører anskaffelsesprisen. Dette gøres ved at bogføre en anskaffelsespris fra anlægskladden, hvor feltet **Forsikringsnr.** er udfyldt. Afkrydsningsfeltet **Aut. forsikr.bogføring** på siden **Anlægsopsætning** skal være markeret. Du kan finde flere oplysninger i [Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

Hvis afkrydsningsfeltet **Aut. forsikr.bogføring** på siden **Anlægsopsætning** ikke er markeret, vil bogføring af anskaffelser fra anlægskladden oprette linjer på siden **Forsikringskladde**, som du derefter skal bogføre manuelt.

> [!WARNING]  
>   Hvis du ikke markerer afkrydsningsfeltet **Aut. forsikr.bogføring** på siden **Anlægsopsætning**, skal din forsikringskladde være baseret på en kladdetype uden en nummerserie. Det skyldes, at de indsatte dokumentnumre fra anlægskladdelinjen ellers er i konflikt med nummerserien for forsikringskladden. Du kan finde flere oplysninger om kladdetyper og -kørsler i [Angive generelle oplysninger om anlægsaktiver](fa-how-setup-general.md).

Når du har tildelt et anlægsaktiv til en forsikringspolice, er afkrydsningsfeltet **Forsikret** markeret på anlægskortet. Når du sælger anlægsaktivet, fjernes markeringen i afkrydsningsfeltet automatisk.

## <a name="to-create-or-modify-an-insurance-card" />Sådan oprettes og redigeres et forsikringskort
En forsikringspolice for et anlægsaktiv skal være repræsenteret af et forsikringskort.

Når du får oplysninger om ændringer i forsikringsbeløbet, kan du angive de nye oplysninger på siden **Forsikringskort** for at sikre dig, at du analyserer forsikringsposterne korrekt.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikring**, og vælg derefter det relaterede link.
2. Vælge handlingen **By** for at oprette et nyt kort til en forsikringspolice. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Du kan også vælge den forsikringspolice, du vil ændre, og derefter vælge handlingen **Rediger**.

## <a name="to-assign-a-fixed-asset-to-an-insurance-policy-by-posting-from-the-insurance-journal" />Sådan tildeles et anlægsaktiv til en forsikringspolice ved at bogføre forsikringskladden
Du tildeler et anlægsaktiv til en forsikringspolice ved at bogføre det til forsikringsposten.  

Følgende procedure beskriver, hvordan du kan oprette en forsikringskladdelinje manuelt. Hvis afkrydsningsfeltet **Aut. forsikr.bogføring** er markeret på siden **Anlægsopsætning**, oprettes forsikringskladdelinjerne automatisk, når du bogfører anskaffelsespriserne. I så fald skal du blot bogføre kladden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladder**, og vælg derefter det relaterede link.  
2. Åbn den relevante kladde, og udfyld kladdelinjerne efter behov.  
3. Du kan tildele flere anlægsaktiver til én forsikringspolice ved at oprette kladdelinjer med samme værdi i feltet **Forsikringsnr.** og forskellige værdier i feltet **Anlægsnr.**  
4. Vælg handlingen **Bogfør**.  

    > [!NOTE]  
    >   Posterne fra en forsikringskladde bogføres kun til forsikringsposterne.  

## <a name="to-update-the-insurance-value-of-a-fixed-asset" />Sådan opdateres forsikringsværdien af et anlægsaktiv
Du kan bruge kørslen **Indekser forsikring** til at opdatere værdien af de anlægsaktiver, der er dækket af forsikringen.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Indekser forsikring**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov.

    > [!NOTE]  
    >   I feltet **Indekstal** kan du f.eks. angive en reduktion på 5 % som 95, mens du angiver en stigning på 2 % som 102.  
3. Vælg knappen **OK**.  

   Ved kørslen beregnes det nye beløb som en procent af den samlede forsikringsværdi ifølge siden **Forsikringsstatistik**, og derefter oprettes der en linje i forsikringskladden.  
4. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladder**, og vælg derefter det relaterede link.  
5. Åbn den relevante forsikringskladde, gennemse de oprettede værdier, og bogfør dem til forsikringsposterne.  

## <a name="to-monitor-insurance-coverage" />Sådan overvåges forsikringsdækning
[!INCLUDE[prod_short](includes/prod_short.md)] indeholder dedikerede rapporter og statistiksider, så du kan analysere forsikringspolicerne og om anlægsaktiverne er over- eller underforsikrede.  

### <a name="overview-of-insurance-policies" />Oversigt over forsikringspolicer
Hvis du vil have et overblik over dine forsikringspolicer, skal du åbne en eksempelvisning af rapporten **Forsikring - stamoplysninger** eller udskrive rapporten. Rapporten indeholder alle policer og de vigtigste felter fra forsikringskortene.  

### <a name="insurance-coverage" />Forsikringsposter
Hvis du vil have vist, hvilke forsikringspolicer der dækker det enkelte anlægsaktiv og med hvilket beløb, kan du få vist eller udskrive rapporten **Forsikring - forsikret i alt**.  

### <a name="overunder-coverage" />Over/underforsikring
Du kan kontrollere, om anlægsaktiver er over- eller underforsikrede på følgende måder:  

* Siden **Forsikringsstatistik**. Et positivt beløb i feltet **Over/underforsikret** betyder, at anlægsaktivet er overforsikret. Et negativt beløb betyder, at det er underforsikret.  
* Siden **Anlægsstatistik**. Vælg feltet **Forsikret i alt** for at få vist siden **Forsikringsposter**.  
* Rapporten **Over/underforsikring**.  
* Rapporten **Forsikringsanalyse**.  

### <a name="uninsured-fixed-assets" />Ikke-forsikrede anlægsaktiver
Hvis du vil kontrollere, om du har glemt at knytte et anlægsaktiv til en forsikringspolice, kan du udskrive eller se rapporten **Forsikring - ikke-fors. anlæg**. Rapporten viser de anlægsaktiver, hvor ingen beløb er bogført til forsikringsposten.  

## <a name="to-view-insurance-coverage-ledger-entries" />Sådan får du vist forsikringsposter
Du kan få vist de forsikringsposter, du har oprettet i forsikringsposterne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikring**, og vælg derefter det relaterede link.  
2. Vælg den relevante forsikringspolice, og vælg derefter handlingen **Forsikringsposter**.  

## <a name="to-view-the-total-insurance-value-of-fixed-assets" />Sådan får du vist den samlede forsikringsværdi for anlægsaktiver
En dedikeret matrixside viser de forsikringsværdier, der er registreret for hver forsikringspolice for de enkelt anlægsaktiver, som resultat af de forsikringsrelaterede beløb, du har bogført.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikring**, og vælg derefter det relaterede link.  
2. Vælg den relevante forsikringspolice, og vælg derefter handlingen **Forsikringssummer pr. anlæg**.  
3. Udfyld felterne efter behov.  
4. Vælg handlingen **Vis matrix**.  
5. Hvis du vil se de underliggende forsikringsposter, skal du vælge en værdi i matrixen.  

## <a name="to-correct-insurance-coverage-entries" />Sådan rettes forsikringsposter
Hvis et anlægsaktiv er knyttet til den forkerte forsikringspolice, kan du rette det ved at oprette to omposteringsposterne fra forsikringskladden.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Forsikringskladder**, og vælg derefter det relaterede link.  
2. Opret en kladdelinje for anlægsaktivet og den korrekte forsikringspolice, hvor værdien i feltet **Beløb** er positivt.  
3. Opret en anden kladdelinje for anlægsaktivet og den forkerte forsikringspolice, hvor værdien i feltet **Beløb** er negativt.  
4. Vælg handlingen **Bogfør**.  

Anlægsaktivet vil blive skilt fra den forkerte forsikringspolice på den anden linje og knyttet til den rette forsikringspolice på den første linje.  

## <a name="see-also" />Se også
[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
