---
title: Anskaffede anlægsaktiver
description: 'Du kan oprette et anlægsaktiv, tildele en afskrivningsprofil og registrere anlægsaktivets anskaffelsespris.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 12/03/2021
ms.author: edupont
---
# <a name="acquire-fixed-assets" />Anskaffede anlægsaktiver

For hvert anlægsaktiv skal du definere et kort med oplysninger om aktivet. Du kan angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste, og du kan gruppere dem på forskellige måder, f.eks efter art, afdeling eller lokation. Der skal oprettes en afskrivningsprofil, og den skal tildeles til hvert enkelt anlægsaktiv, før du kan hente det.

Når der er oprettet et anlægsaktiv, og der er tildelt en afskrivningsprofil, skal du anskaffe anlægsaktivet. For at få et anlægsaktiv skal du registrere dens anskaffelsespris i den relevante finanskonto, bankkonto eller leverandør ved at bogføre en anskaffelsestransaktion fra siden **Anlægskassekladde**. Du kan bruge siden **Bistået anskaffelse af anlægsaktiv** til at oprette og bogføre de nødvendige finanskladdelinjer automatisk.

Skrapværdien er restværdien af et anlæg, der ikke længere kan bruges. Du kan bogføre skrapværdien samtidigt med, at du bogfører anskaffelsesprisen. Du kan finde flere oplysninger i [Afskrive eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md).

Indeksering anvendes til at justere for ændringer af det generelle prisniveau. Kørslen **Indekser anlæg** kan bruges til at beregne anskaffelsespriser som genanskaffelsespriser.

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically" />Sådan oprettes og anskaffes et anlægsaktiv automatisk

Følgende procedure beskriver, hvordan du opretter et anlægsaktiv og derefter anskaffer det ved hjælp af siden **Bistået anskaffelse af anlægsaktiver** for at oprette og bogføre de nødvendige anlægskassekladdelinjer. Du kan også oprette og bogføre linjerne manuelt. Du kan finde flere oplysninger i [Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** handling, og udfyld felterne på oversigtspanelet **Generelt** efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. I oversigtspanelet **Afskrivningsprofil** skal du udfylde felterne efter behov. I dette trin tildeles en afskrivningsprofil til anlægsaktivet.  
4. Hvis du vil tildele mere end én afskrivningsprofil til anlægsaktivet, skal du vælge handlingen **Tilføj flere afskrivningsprofiler**. Du kan finde flere oplysninger i [Sådan tildeles en afskrivningsprofil til et anlægsaktiv](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Når alle felter, der kræves for at anskaffe et anlægsaktiv, er udfyldt, vises beskeden **Du er klar til at anskaffe anlægsaktivet. Anskaf** øverst på siden.
5. Vælg handlingen **Anskaf** i beskeden.
6. Følg trinnene på siden **Bistået anskaffelse af anlægsaktiver** for at fuldføre automatisk anskaffelse af anlægsaktivet.

> [!NOTE]  
>   Du kan også bogføre anskaffelsespriser som kreditposter. I så fald skal du huske, at værdien i feltet **Anskaffelsespris inkl. moms** skal have et minustegn for at angive en kredit.

Når du vælger **Udfør**, udfyldes feltet **Bogført værdi** på siden **Anlægskort**, hvilket angiver, at anlægsaktivet er anskaffet til den angivne anskaffelsespris.  

## <a name="to-set-up-a-component-list-for-a-main-asset" />Sådan konfigureres en komponentliste for et hovedanlæg

Du kan gruppere anlægsaktiverne i hovedanlæg og de tilhørende komponenter. Du kan f.eks. have en produktionsmaskine, som består af mange dele, som du vil gruppere på denne måde.  

Både hovedanlægget og alle dets komponenter skal oprettes som individuelle anlægskort. Når du har oprettet en komponentliste, udfylder [!INCLUDE[prod_short](includes/prod_short.md)] felterne **Hovedanlæg/underanl.** og **Hovedanlæg/underanl.** på anlægskortene.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, der er hovedanlægget, og vælg derefter handlingen **Hovedanlæg**.
3. På siden **Hovedanlæg** skal du vælge feltet **Anlægsnr**. og derefter vælge de anlægsaktiver, der skal tilføjes som en komponent i hovedanlægget.
4. Luk siden.
5. Gentag trin 3 til 4 for hver underdel til anlægget, du vil tilføje.
6. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsopsætning**, og vælg derefter det relaterede link.
7. Markér afkrydsningsfeltet **Tillad bogf. på hovedanlæg**.

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal" />Sådan bogføres anskaffelse af et anlægsaktiv manuelt med finanskassekladden

Følgende fremgangsmåde bruges til at anskaffe et anlægsaktiv manuelt ved at oprette og bogføre linjerne på siden **Anlægsfinanskladde**. Du kan også anskaffe et anlægsaktiv automatisk ved hjælp af siden **Bistået anskaffelse af anlægsaktiver**. Flere oplysninger under trin 5 i [Sådan oprettes og anskaffes et anlægsaktiv automatisk](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically).

> [!NOTE]  
>   Du kan også bogføre anskaffelsespriser som kreditposter. I så fald skal du huske, at værdien i feltet **Beløb** skal have et minustegn for at angive en kredit.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægsfinanskladder**, og vælg derefter det relaterede link.
2. På siden **Anlægskassekladde** i feltet **Anlægsbogføringstype** skal du vælge **Anskaffelsespris**.
3. Udfyld de resterende felter efter behov.
4. Vælg handlingen **Bogfør**.  

> [!TIP]  
>   Hvis du udfylder feltet **Forsikringsnr.** i anlægskassekladden, når du bogfører en anskaffelse, vil [!INCLUDE[prod_short](includes/prod_short.md)] også bogføre anskaffelsesprisen på anlægsaktivet på forsikringsposterne. Du kan finde flere oplysninger i [Forsikre anlægsaktiver](fa-how-insure.md).

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset" />Sådan annulleres bogføringen af en anskaffelsespris for et anlægsaktiv

Hvis du laver en fejl under bogføring af en anskaffelsespris, kan du fjerne posten vha. kørslen **Annuller anlægsposter** og derefter bogføre den korrekte anskaffelsespost. De forkerte poster overføres til siden **Anlægsfejlposter**.

Hvis du f.eks, bogfører en anskaffelse med den forkerte dato, skal du rette den snarest muligt, fordi bogføringsdatoen for anlægsaktivet bruges i mange vigtige beregninger.

> [!IMPORTANT]  
> Du kan ikke bruge funktionen **Tilbagefør transaktioner** for anlægsposter.

1. Vælg ikonet ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, indtast **Anlægsfinansposter**, og vælg derefter det relaterede link.  
2. Vælg den eller de poster, du vil annullere, på siden **Anlægsfinansposter**.  
3. Vælg menuen **Handlinger**, og vælg derefter handlingen **Annuller poster**.
4. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Vælg **OK** for at eksekvere kørslen.
6. Når den eller de forkerte poster annulleres, kan du fortsætte med at bogføre den korrekte anskaffelsespris.

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost" />Sådan bogføres skrapværdien sammen med anskaffelsesprisen

Du kan bogføre skrapværdien sammen med anskaffelsesprisen fra en anlægskladde.

> [!NOTE]
> Denne proces kan kræve, at du tilpasser siden Anlægsaktivkladder ved at tilføje feltet Skrapværdi. Feltet vises ikke som standard på siden. Du kan finde flere oplysninger i [Tilpasse dit arbejdsområde](ui-personalization-user.md).

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Anlægskassekladder**, og vælg derefter det relaterede link.
2. Opret anskaffelseslinjen på siden **Anlægskladde**. Du kan finde flere oplysninger i [Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal).
3. Angiv beløbet for skrapværdien som en kreditpost (med et minustegn, f.eks. **-** 100) i feltet **Skrapværdi** på kladdelinjen.
4. Vælg handlingen **Bogfør**.

> [!NOTE]
> Hvis der findes en skrapværdi for et anlægsaktiv, bruges denne værdi i afskrivningsbogføringen i stedet for værdien i feltet **Slutbogført værdi** på siden **Anlægsafskrivningsprofiler**. Du kan finde flere oplysninger i [Sådan administrerer du den slutbogførte værdi](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## <a name="see-related-microsoft-trainingtrainingmodulespurchase-fixed-assets" />Se relateret [Microsoft-træning](/training/modules/purchase-fixed-assets/)

## <a name="see-also" />Se også

[Anlægsaktiver](fa-manage.md)  
[Opsætning af Anlægsaktiver](fa-setup.md)  
[Finans](finance.md)  
[Blive køreklar](ui-get-ready-business.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
