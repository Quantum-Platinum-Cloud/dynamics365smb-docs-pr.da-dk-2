---
title: "Behandle indgående bilag | Microsoft Docs"
description: "Når du vil registrere et eksternt dokument, f.eks. en PDF, i Business Central, skal du først oprette eller fuldføre en indgående dokumentpost."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b6de34be2f16cf0b9130bc88495f27536a9d5080
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="processing-incoming-documents"></a>Behandle indgående bilag
Når du vil registrere et eksternt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du først oprette eller fuldføre en indgående dokumentpost. Du kan gøre dette manuelt, eller du kan tage et billede af det eksterne dokument og derefter oprette den indgående dokumentpost med billedfilen vedhæftet.

Fra PDF-filer eller billedfiler, som du modtager fra dine handelspartnere, kan du få en ekstern OCR-tjeneste (Optical Character Recognition) til at oprette elektroniske dokumenter, der kan konverteres til dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. når du modtager en faktura i PDF-format fra en leverandør, kan du sende den til tjenesten OCR fra vinduet **Indgående bilag**. Du kan også vælge at sende filen til OCR-tjenesten via mail. Når du får det elektroniske dokument retur, oprettes der automatisk en relateret indgående dokumentpost. Efter nogle sekunder får du filen tilbage fra OCR-tjenesten som en elektronisk faktura, der kan konverteres til en købsfaktura til kreditoren.

| Hvis du vil | Se |
| --- | --- |
| Opret indgående dokumentposter manuelt eller automatisk ved at tage et billede af en papirkvittering, f.eks. |[Oprette indgående dokumentposter](across-how-create-income-document-records.md) |
| Bruge en OCR-tjeneste til at konvertere PDF- og billedfiler til elektroniske dokumenter, der igen kan konverteres til købsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)] f.eks. Lær OCR-tjenesten at undgå fejl, næste gang lignende data behandles. |[Bruge OCR til at gøre PDF- og billedfiler til elektroniske dokumenter](across-how-use-ocr-pdf-images-files.md) |
| Forbinde eller fjerne indgående dokumentposter for ikke-bogførte salgs- eller købsdokumenter og med enhver debitor-, kreditor- eller finanspost fra dokumentet eller posten. |[Oprette indgående dokumentposter direkte fra dokumenter og poster](across-how-connect-disconnect-income-document-records.md) |
| Fra vinduerne **Kontoplan** og **Finansposter** skal du bruge en søgefunktionen til at finde finansposter for bogførte dokumenter, som ikke har indgående dokument poster og derefter knytte centralt til eksisterende poster eller oprette nye med vedhæftede dokument filer. |[Finde bogførte dokumenter uden indgående dokumentposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få et større overblik ved at indstille indgående dokumentposter til Behandlet for at fjerne dem fra standardvisningen. |[Administrere mange indgående dokumentposter](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Se også
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
