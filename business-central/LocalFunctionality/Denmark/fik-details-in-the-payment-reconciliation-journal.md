---
title: FIK-detaljer i betalingsudligningskladden | Microsoft Docs
description: "Feltet **Transaktionstekst** i vinduet **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c7fc4386f291326435ed532ab399d050646ad311
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="fik-details-in-the-payment-reconciliation-journal"></a>FIK-detaljer i betalingsudligningskladden
Feltet **Transaktionstekst** i vinduet **Betalingsudligningskladde** viser oplysninger om automatisk udligning af betalinger ved hjælp af den danske FIK-standard. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md).  

 I følgende tabel beskrives seks værdier, der kan vises i feltet **Transaktionstekst**.  

|Transaktionstekst|Description|  
|-----------------------------------------|---------------------------------------|  
|**Tilsvarende beløb**|Det betalte beløb dækker nøjagtigt det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.|  
|**Delvist beløb**|Det betalte beløb er mindre end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.|  
|**Overskydende beløb**|Det betalte beløb er mere end det resterende beløb på en ubetalte salgsfaktura, der er identificeret af FIK-nummeret.|  
|**Ingen matchende FIK-kode**|Systemet har ikke fundet nogen skyldige eller betalte salgsfakturaer med et FIK-nummer, der svarer til FIK-nummeret på betalingen.|  
|**FIK-dubletnummer**|Systemet har registreret, at der er betalinger, der har lignende FIK-numre.|  
|**Fakturaen er allerede betalt**|Systemet har registreret, at nogle FIK-numre på en betaling svarer til en salgsfaktura, som er fuldt udlignet og lukket.|  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
[Afstemme betalinger ved hjælp af automatisk udligning](../../receivables-how-reconcile-payments-auto-application.md)
