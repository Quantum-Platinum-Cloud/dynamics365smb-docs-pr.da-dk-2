---
title: "Bruge udvidelsen C5-dataoverførsel | Microsoft Docs"
description: "Du kan bruge denne udvidelse til at overføre debitorer, kreditorer, varer og omkostninger på finanskonti fra Microsoft Dynamics C5 2012 til Business Central."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, C5, import
ms.date: 04/09/208
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: 698bde6949c6053501881d07135586810fc81bdd
ms.contentlocale: da-dk
ms.lasthandoff: 04/11/2018

---

# <a name="the-c5-data-migration-extension-for-business-central"></a>Udvidelsen Overførsel af C5-data til Business Central
Denne udvidelse gør det let at overføre debitorer, kreditorer, varer og finanskonti fra Microsoft Dynamics C5 2012 til [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan også overføre gamle poster for finanskonti.

> [!Note]
> Virksomheden i [!INCLUDE[d365fin](includes/d365fin_md.md)] må ikke indeholde data. Når du starter en overførsel, må du desuden ikke oprette debitorer, kreditorer, varer eller konti, før overflytningen er afsluttet.

## <a name="what-data-is-migrated"></a>Hvilke data overføres?
Følgende data overføres for hver enhed:

**Kunder (Debitorer)**
* Sted
* Land
* Kundedimensioner (afdeling, arbejdscenter og formål)
* Leveringsform
* Sælger
* Betalingsbetingelser
* Betalingsform
* Debitorprisgruppe
* Debitorfakturarabat

Hvis du overfører konti, overføres følgende data også:

* Opsætning for debitorbogføring
* Finanskladdenavn
* Åbne transaktioner (debitorposter)

**Leverandører (Kreditorer)**
* Sted
* Land
* Kreditordimensioner (afdeling, arbejdscenter og formål)
* Fakturarabat
* Leveringsform
* Indkøber
* Betalingsbetingelser
* Betalingsform
* Kreditorfakturarabat

Hvis du overfører konti, overføres følgende data også:

* Opsætning af kreditorbogføring
* Finanskladdenavn
* Åbne transaktioner (kreditorposter)

**Varer**
* Sted
* Land
* Varedimensioner (afdeling, arbejdscenter og formål)
* Salgslinjerabatter
* Debitorrabatgrupper
* Varerabatgrupper
* Salgspris
* Tarifnummer
* Enheder
* Varesporingskode
* Debitorprisgruppe

Hvis du overfører konti, overføres følgende data også:

* Opsætning af lagerbogføring
* Bogføringsopsætning
* Varekladdenavn
* Åbne transaktioner (vareposter)

> [!Note]
> Hvis der er åbne transaktioner, der bruger udenlandske valutaer, overføres valutakursen også for disse valutaer. Andre valutakurser overflyttes ikke.

**Kontoplan**  
* Standarddimensioner: afdeling, omkostningssted og formål  
* Historiske finanstransaktioner  

> [!Note]
> Historisk finanstransaktioner behandles lidt anderledes. Når du overfører data, angiver du en **Nuværende periode**-parameter. Denne parameter angiver, hvordan du skal behandle finanstransaktioner. Transaktioner efter denne dato overføres enkeltvis. Transaktioner inden denne dato lægges sammen pr. konto og overføres som et enkelt beløb. Lad os antage, at der er transaktioner i 2015, 2016, 2017, 2018, og du angiver den 1. januar 2017 i feltet Nuværende periode. For hver konto samles beløb for alle transaktioner på eller før den 31. december 2106 på en enkelt finanskladdelinje for hver finanskonto. Alle transaktioner efter denne dato overføres enkeltvis.

## <a name="to-migrate-data"></a>Sådan overføres data
Der er nogle få trin til at eksportere data fra C5 og indlæse dem i [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

1. I C5 skal du bruge funktionen **Eksportér databasen** til at eksportere dataene. Send derefter eksportmappen til en komprimeret (zippet) mappe.  
2. I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Dataoverførsel** og derefter vælg **Dataoverførsel**.  
3. Udfør trinnene i guiden til assisteret opsætning. Sørg for at vælge **Indlæs fra Microsoft Dynamcis C5 2012** som datakilde.  

> [!Note]
> Virksomheder tilføje ofte felter for at tilpasse C5 til deres specifikke branche. [!INCLUDE[d365fin](includes/d365fin_md.md)] overflytter ikke data fra brugerdefinerede felter. Overførslen mislykkes også, hvis du har mere end 10 brugerdefinerede felter.

## <a name="viewing-the-status-of-the-migration"></a>Få vist status for overførslen
Brug siden **Dataoverførselsoversigt** til at overvåge status for overførslen. Siden viser oplysninger, f.eks. antallet af enheder overførslen skal medtage, status for overførslen, og antallet af elementer, der er blevet overført, og om de var vellykket. Den viser også antallet af fejl, giver dig mulighed for at finde ud af, hvad der gik galt, og gør det, hvis det er muligt, nemt at gå til enheden for at løse problemerne. Du kan finde flere oplysninger i næste afsnit i dette emne.  

> [!Note]
> Mens du venter på resultaterne af overførslen, skal du opdatere siden for at få vist resultaterne.

## <a name="how-to-avoid-double-posting"></a>Sådan undgås dobbeltbogføring
For at undgå dobbeltbogføring i finansregnskabet bruges følgende modkonti til åbne posteringer:  
  
* For kreditorer bruger vi kreditorkontoen fra kreditorbogføringsgruppen.  
* For debitorer bruger vi debitorkontoen fra debitorbogføringsgruppen.  
* For varer opretter vi en bogføringsopsætning, hvor reguleringskontoen er den konto, der er angivet som lagerkontoen i varebogføringsopsætningen.  

## <a name="correcting-errors"></a>Rette fejl
Hvis noget går galt, og der opstår en fejl, viser feltet **Status** teksten **Udført med fejl**, og feltet **Antal fejl** viser hvor mange. For at få vist en liste over fejlene, kan du åbne siden **Dataoverførselsfejl** side ved at vælge:  

* Nummeret i feltet **Antal fejl** for enheden.  
* Enheden og derefter handlingen **Vis fejl**.  

På siden **Dataoverførselsfejl** kan du for at rette en fejl vælge en fejlmeddelelse, og derefter vælge **Rediger post** for at åbne en side, der viser de overførte data for objektet. Når du retter en eller flere fejl, kan du vælge **Overfør** for kun at overføre de enheder, du rettede, uden at genstarte hele overførslen.  

> [!Tip]
> Hvis du har rettet mere end én fejl, kan du bruge funktionen **Markér flere** til at markere flere linjer, der skal overføres. Hvis der omvendt er fejl, det ikke er vigtigt at løse, kan du vælge dem og derefter vælge **Spring valg over**.

> [!Note]
> Hvis du har varer, der indgår i en stykliste, kan du være nødt til at overføre mere end én gang, hvis den oprindelige vare ikke er oprettet før de varianter, der refererer til den. Hvis en varevariant oprettes først, kan det medføre, at referencen til den oprindelige vare giver en fejlmeddelelse.  

## <a name="verifying-data-after-migrating"></a>Kontrol af data efter overførsel
En måde til at kontrollere, at dine data overføres korrekt, er ved at se på følgende sider i C5 og [!INCLUDE[d365fin](includes/d365fin_md.md)].

|Microsoft Dynamics C5 2012 | [!INCLUDE[d365fin](includes/d365fin_md.md)]| Den kørsel, der skal bruges |
|-----|-----|-----|
|Debitorposter| Finanskladder| CUSTMIGR |
|Kreditorposter| Finanskladder| VENDMIGR|
|Vareposter| Varekladder| ITEMMIGR |
|Finansposter| Finanskladder| GLACMIGR |

## <a name="stopping-data-migration"></a>Stoppe dataoverførslen
Du kan stoppe overførslen af data ved at vælge **Stop alle overførsler**. Hvis du gør det, stoppes alle ventende overførsler også.

## <a name="see-also"></a>Se også
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  
[Introduktion](product-get-started.md) 
