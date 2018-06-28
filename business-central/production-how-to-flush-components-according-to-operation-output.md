---
title: "Sådan udtrækkes komponenter i henhold til operationsafgang | Microsoft Docs"
description: "For varer, der er konfigureret med baglæns trækmetode, er standardfunktionsmåden at beregne og bogføre komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Afsluttet**. Du kan finde flere oplysninger i Trækmetode."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4d2109a462d5d1a755cf7ffaf45129bec2234376
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="flush-components-according-to-operation-output"></a>Udtrække komponenter i henhold til operationsafgang
For varer, der er konfigureret med baglæns trækmetode, er standardfunktionsmåden at beregne og bogføre komponentforbrug, når du ændrer status på en frigivet produktionsordre til **Afsluttet**.  

Hvis du også definerer rutebindingskoder, forekommer beregning og bogføring, når hver operation er afsluttet, og den mængde, der rent faktisk er forbrugt i handlingen, der er bogført. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).  

Hvis f.eks. en produktionsordre om at fremstille 800 meter kræver 8 kg af en komponent, bogføres derefter, når du bogfører 200 meter som afgang, 2 kg automatisk som forbrug.  

Denne funktion er nyttig, af følgende årsager:  

-   **Lagerværdi** -værdiposterne for afgang og forbrug oprettes parallelt, efterhånden som produktionsordren skrider frem. Uden rutebindingskoder vil lagerværdien forøges efterhånden som afgangen bogføres, og derefter formindsk på et senere tidspunkt, når værdien af komponentforbruget bogføres sammen med den færdige produktionsordre.  
-   **Varedisponering** - med gradvis bogføring af forbrug, vil tilgængeligheden af komponentvarer være mere opdateret, hvilket er vigtigt for at opretholde den interne balance mellem efterspørgsel og udbud. Uden rutebindingskoder vil andre efterspørgsler efter komponenten mene, at den er tilgængelig, så længe der ventes på et forsinket bogføring af forbruget.  
-   **Just-in-Time** – med muligheden for at tilpasse produkter til debitorbehov, kan du minimere affald ved at sørge for, at arbejde og ændringer i systemet kun forekomme, når det er nødvendigt.  

Følgende procedure viser, hvordan du kombinerer Bagudtrækning og rutebindingskode, så den mængde, der udtrækkes for hver operation er proportional med den faktiske afgang af den afsluttede operation.  

## <a name="to-flush-components-according-to-operation-output"></a>Udtrække komponenter i henhold til operationsafgang  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Rediger**.  
3.  Vælg **Fremad** i feltet **Trækmetode** oversigtspanel under fanen **Genopfyldning**.  

    > [!NOTE]  
    >  Vælg **Pluk + Fremad**, hvis komponenten bruges på en placering, der er sat op til styret læg-på-lager og pluk.  

4.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ruter**, og vælg derefter det relaterede link.  
5.  Definer rutebindingskoder for hver operation, der bruger komponenten. Du kan finde flere oplysninger i [Oprette ruter](production-how-to-create-routings.md).  
6.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Produktionsstykliste**, og vælg derefter det relaterede link.  
7.  Definer rutebindingskoder fra hver forekomst af komponenten til den operation, hvor den forbruges.

    > [!IMPORTANT]  
    >  Komponenten skal have en rutebinding til den sidste operation i ruten.  

## <a name="see-also"></a>Se også  
[Oprette produktionsstyklister](production-how-to-create-production-boms.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Planlægning](production-planning.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
