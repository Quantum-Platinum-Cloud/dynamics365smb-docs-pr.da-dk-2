---
title: 'Oversigt over de opgaver, der afslutter regnskaberne'
description: 'Få mere at vide om processen med at afslutte regnskaberne for et regnskabsår eller en -periode, og hvad der sker, når du lukker ved årets afslutning.'
author: jswymer
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'year closing, close accounting period, close fiscal year, bank account detailed trial balance'
m.search.form: 100
ms.date: 04/01/2021
ms.author: jswymer
---
# <a name="closing-the-books" />Afslutte regnskaberne
Når du har kontrolleret, at alle dine konti er opdaterede, og når du har allokeret omkostninger og indtægter, så kan du afslutte regnskabet for et regnskabsår eller en regnskabsperiode.

Du behøver ikke at lukke et år, men hvis du gør det, bliver det nemmere at arbejde i systemet, da du vil kunne udnytte de filtreringsfunktioner, der er. Du vil heller ikke skulle bekymre dig om at miste transaktionsoplysninger, når du lukker, fordi alle detaljerne bevares, selv efter at du lukker året.

## <a name="closing-book-process" />Regnskabsafslutningsproces
Processen til afslutning af regnskabet omfatter disse hovedopgaver:

1. Afslutning af regnskabsperioden.

    Et regnskabsår er defineret som en eller flere åbne perioder som angivet på siden **Regnskabsperioder**. Et typisk regnskabsår indeholder 12 perioder på hver en måned, men du kan også vælge en anden metode til at definere et år på.

    Du kan finde flere oplysninger i [Afslutte regnskabsperioder](year-close-account-periods.md).
2. Registrering af efterposter.

    Når du afslutter et regnskabsår, skal du angive et antal administrative transaktioner, f.eks. forudbetalte og periodiserede varer. Disse transaktioner kaldes reguleringsposter. Der er ikke særlige regler for bogføring af disse poster, og de indeholder - som andre poster - en markering i feltet **Efterposter**, hvis de bogføres på en dato i et lukket regnskabsår. Selvom et regnskabsår er afsluttet, kan du stadig bogføre finansposter i det.
3. Overførsel af saldi fra resultatopgørelseskontiene til balancen.

    Når et regnskabsår er blevet lukket og alle efterposterne er bogført, skal resultatopgørelseskontoen lukkes, og årets nettoindkomst skal overføres til en konto under ejers egenkapital på balancen. Brug kørslen Nulstil resultatopgørelse til dette formål. Ved kørslen behandles alle finansposter af typen Resultatopgørelse, og der oprettes poster, som tilbagefører balancerne. Disse poster placeres i en kladde, hvorfra de kan bogføres. De bogføres ikke automatisk ved kørslen, undtagen når der bruges en ekstra rapporteringsvaluta. Når der bruges ekstra rapporteringsvaluta, bogfører kørslen direkte til finansposterne.

    Du kan finde flere oplysninger i [Nulstil resultatopgørelse](year-close-income-statement.md).
4. Bogføring af årsafslutningsposten sammen med modregningsposterne på egenkapitalkontoen.

    Når kørslen Nulstil resultatopgørelse er afsluttet, skal du bogføre de poster, der er blev oprettet under kørslen. Hvis du ikke har angivet en resultatkonto til kørslen, så skal du angive én linje med en modpost, der bogfører nettoindkomsten til den korrekte finanskonto under ejers egenkapital på balancen. Til slut skal du bogføre kladden.

    Du kan finde flere oplysninger i [Bogføre årsafslutningsposten](year-how-post-year-end-close-entry.md).

## <a name="what-happens-when-you-close" />Hvad der sker, når du afslutter
Når du lukker i slutningen af året, flytter systemet indtjeningen fra den beregnede indtjening, eller kontoen med den aktuelle indtjening, til en bogført konto eller resultatkontoen. Regnskabsåret mærkes også som "lukket", og alle posterne for det lukkede år som "poster fra tidligere år".

Der oprettes derefter en ultimopost, men posten bogføres ikke automatisk. Du får mulighed for at oprette en eller flere modregningsposter på egenkapitalkontoen, hvilket gør det muligt for dig at bestemme, hvordan ultimoposten skal allokeres. Hvis virksomheden f.eks. har flere afdelinger, kan du lade systemet oprette en enkelt ultimopost for alle afdelingerne, og du kan derefter oprette en modregningspost på hver afdelings egenkapitalkonto.

Du kan bogføre i et tidligere regnskabsår, selv efter at resultatopgørelseskontiene er blevet lukket, hvis du udfører kørslen Nulstil resultatopgørelse igen bagefter.

## <a name="see-also" />Se også

[Arbejd med regnskabsperioder og regnskabsår](finance-accounting-periods-and-fiscal-years.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
