---
title: "Sådan sælges lagervarer i montage til ordre-flows | Microsoft Docs"
description: "Hvis varen er konfigureret til kortet til montage til ordre, vil standardsalgsordreprocessen forudsætte, at varen ikke er på lageret, og at den skal monteres til denne specifikke salgsordre. Derfor oprettes en sammenkædet montageordre automatisk, når du føjer elementet til en salgsordrelinje."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 97b79683ba6c770912349c772f1f7adb443b94ed
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="sell-inventory-items-in-assemble-to-order-flows"></a>Sælge lagervarer i montage til ordre-forløb
Hvis feltet **Montagepolitik** på varekortet til et montageelement indeholder **Montage efter ordre**, vil standardsalgsordreprocessen forudsætte, at elementet ikke er på lageret, og at det skal monteres til denne specifikke salgsordre. Derfor oprettes en sammenkædet montageordre automatisk, når du føjer elementet til en salgsordrelinje. Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md). Men hvis en del af salgsordremængden allerede er tilgængelig på lageret, kan du sænke montageordremængden ved at ændre feltet **Antal til montage efter ordre** på salgsordrelinjen.  

Dette scenario er sjældent, da montage efter ordre-varer forventes altid tilpasses, og chancen for, at de er på lager i den konfiguration, der anmodes om fra en anden kunde, er lav. Men hvis en virksomhed har montage efter ordre-mængder på lager på grund af returnerer eller for aflysninger, skal disse mængder plukkes og sælges, inden nye samles.  

> [!NOTE]  
>  Der findes ingen funktionalitet på salgsordrer, der automatisk påminder eller hjælper dig med at modregne montageordrer, der allerede er tilgængelige. I stedet skal du overvåge disponeringsoplysninger som i faktaboksen **Salgslinjedetaljer**.  

Lignende funktionalitet er tilgængelig, når du sælger montageelementer fra lageret, og en del af eller alle er ikke tilgængelig og kan leveres med en montageordre. Du kan finde flere oplysninger i [Sælge montage til ordre-varer og lagervarer sammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).  

> [!NOTE]  
>  Der gælder bestemte regler for feltet **Lever antal** på salgsordrelinjer, der indeholder en kombination af montage til ordre-antal og lagerantal. Du kan finde flere oplysninger i afsnittet Kombinationsscenarier i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).  

I denne procedure skal du erstatte montage efter ordre-mængder med lagerantal på en salgsordrelinje. Fremgangsmåden omfatter registrering af, at tilgængelighed findes med fradrag af mængden fra tilknyttet montageordre og derefter reservere lagerantal for at sikre, at det er plukkes og leveres til ordren.  

## <a name="to-sell-inventory-items-in-assemble-to-order-flows"></a>Sådan sælges lagervarer i montage efter ordre-forløb  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2.  Oprette en salgsordre. Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).  
3.  På en salgsordrelinje til et montage efter ordre-element i feltet **Antal** skal du angive det ønskede antal.  
4.  I faktaboksen **Salgslinjedetaljer** skal du afgøre, om hele eller noget af den påkrævede mængde er tilgængelig.  
5.  I feltet **Antal til montage efter ordre** skal du fratrække den disponible mængde, så kun den utilgængelige mængde er samlet til ordren. Feltet **Reserveret antal** faldt tilsvarende og afspejler, at ordre-til-ordre-linket eller -reservation kun gælder for den mængde, der skal samles.  
6.  I oversigtspanelet **Linjer** skal du vælge **Funktioner** og derefter vælge handlingen **Reservér**.  
7.  I vinduet **Reservation** skal du markere den eller de finanspostvarelinjer, der indeholder de tilgængelige mængder, vælge handlingen **Reservér fra aktuel linje** og derefter klikke på knappen **OK**.  

    I vinduet **Salgsordre** viser feltet **Reserveret antal** nu, at hele ordrelinjemængden er reserveret. Feltet **Antal til montage efter ordre** afspejler stadig de undermængder, der skal samles.  

8.  Frigiv salgsordren til pluk af lagervarer og montage af utilgængelige elementer. Du kan finde flere oplysninger i [Montere varer](assembly-how-to-assemble-items.md).  

> [!CAUTION]  
>  Feltet **Placeringskode** på salgsordren kan være udfyldt på forhånd i henhold til feltet **Pla.kode til ordremontagelev.** eller feltet **Placeringskode til fra-montage** på lokationskortet. I så fald kan feltet **Placeringskode** på salgsordrelinjen være forkert i denne kombination af mængder til montage efter ordre og montage til lager. Det er en god idé at undersøge feltet **Placeringskode** og kontrollere, at placeringen fungerer for alle mængder. Du kan også angive de to forskellige mængder på separate salgsordrelinjer.  

## <a name="see-also"></a>Se også  
[Montagestyring](assembly-assemble-items.md)  
[Reservere varer](inventory-how-to-reserve-items.md)  
[Arbejde med styklister](inventory-how-work-BOMs.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
