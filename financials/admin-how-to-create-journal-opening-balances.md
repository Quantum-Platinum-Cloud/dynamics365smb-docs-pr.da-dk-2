---
title: "Sådan oprettes kladden Primosaldi | Microsoft Docs"
description: "Business Central indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed. Du kan nemt overføre disse data med posteringer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: be45ed1de52c92722d801da344163fdffc2a9073
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-journal-opening-balances"></a>Oprette kladden Primosaldi
[!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder flere batchjob, der kan hjælpe dig med at overføre ældre kontosaldi til en nylig konfigureret virksomhed. Du kan nemt overføre disse data til debitorkladden, kreditorkladden, varekladden og finanskladden.

Det første trin er at oprette en konfigurationspakke, der omfatter konfigurationstabellerne for disse kladder. I følgende procedure antages det, at dette trin er udført. Du kan finde flere oplysninger i [Konfigurere virksomhedskonfiguration](admin-set-up-company-configuration.md). Proceduren beskriver de efterfølgende trin, som omfatter anvendelse af den pakke, der leveres af en partner.  

Før du starter, skal du kontrollere, at du er på rollecentersiden RapidStart Services-implementering, som indeholder den korrekte kontekst til dit konfigurationsarbejde. Du kan finde flere oplysninger under [Ændring af grundlæggende indstillinger](ui-change-basic-settings.md).

## <a name="to-apply-the-entries-in-a-journal-to-a-new-company"></a>Udligne posterne i en kladde til en ny virksomhed  
1. Konfigurer en ny virksomhed, og anvend en konfigurationspakke på den. Du kan finde flere oplysninger i [Konfigurere en virksomhed med guiden RapidStart](admin-how-to-configure-a-company-with-the-rapidstart-wizard.md).  

    Den nye virksomhed indeholder ikke oplysninger om kladdeprimosaldi.  

2. Åbn konfigurationsregnearket, og importér eksisterende data om debitorer, varer, kreditorer og regnskabet. Du kan finde flere oplysninger i [Overflytte debitordata](admin-migrate-customer-data.md).  
3. Vælg f.eks. handlingen **Opret sagskladdelinjer**.  
4. Udfyld oversigtspanelet **Indstillinger**, og angiv filtre efter behov. Skriv f.eks. et navn i feltet **Kladdetype**.  
5. Vælg knappen **OK**. Posterne er nu i kladden, men beløbene er tomme.  
6. Eksportér kladdetabellen til Excel, og angiv manuelt bogførings- og modkontooplysninger fra ældre data.
7. Importér og anvend tabeloplysningerne i den nye virksomhed. Kladdelinjerne er klar til bogføring.  
8. I konfigurationsregnearket skal du vælge kladdelinjetabellen og derefter vælge handlingen **Databasedata**.  
9. Gennemgå oplysningerne, og vælg derefter handlingen **Bogfør**.  
10. Gentag trinene for at importere og bogføre eventuelle andre primosaldi.  

## <a name="see-also"></a>Se også  
[Anvende konfigurationer på nye virksomheder](admin-apply-configuration-to-new-companies.md)  
[Oprette en virksomhed med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Opsætning](admin-setup-and-administration.md)
