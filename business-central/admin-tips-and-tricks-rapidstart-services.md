---
title: Tip - RapidStart Service | Microsoft Docs
description: "Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4e8dc4436b01f69292a01afbc7a5d0381b544a77
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a>Tip: RapidStart Services
Når du konfigurerer virksomheder ved hjælp af RapidStart Services, er der nogle tip og tricks, som du kan bruge til at hjælpe dig med, at implementeringen går problemfrit.  

## <a name="take-advantage-of-configuration-templates"></a>Udnytte fordelen ved konfigurationsskabeloner  
Konfigurationsskabeloner kan hjælpe dig med at strømline implementeringsprocessen. Ved hjælp af dem kan du inkludere lignende kunder i segmenter og derefter udarbejde en protokol til implementering, der behandler alle kunder i et segment på samme måde. På denne måde kan du anvende et niveau af forudkonfiguration til hvert segment og fortsætte med en hurtig implementering.  

## <a name="configuration-questionnaires"></a>Konfigurationsspørgeskemaer  
Du skal overveje at definere standardsvar for at angive de bedste fremgangsmåder, som en støtte til processen med at udfylde et konfigurationsspørgeskema.  

## <a name="batch-creation-of-journal-lines"></a>Batchoprettelse af kladdelinjer  
Vi anbefaler, at du bruger de leverede værktøjer til dataoverflytning til at overflytte journalposter. Hvis du bruger et batchjob til at oprette kladdelinjer, har dette et begrænset omfang og opretter kun præ-standardfelter i en kladde. Resten af kladden skal derefter udfyldes manuelt.  

## <a name="migrating-transactions"></a>Overflytning af transaktioner  
Vi anbefaler, at du overflytter startsaldoer i følgende rækkefølge.  

1.  Overflytte startsaldoer for regnskab uden brug af underregnskaber i finans. Brug af specifikke primosaldo modregningskonti, én opsat for hvert underregnskab. Konfigurer modregningskontiene til at aktivere direkte bogføring.  
2.  Overflyt åbne debitorposter.  
3.  Overflyt åbne vareposter.  
4.  Overflyt åbne anlægsposter.  

## <a name="see-also"></a>Se også  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
