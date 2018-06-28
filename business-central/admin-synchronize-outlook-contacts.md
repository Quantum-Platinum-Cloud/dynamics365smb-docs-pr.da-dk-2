---
title: Dele kontaktpersoner mellem Business Central og Outlook | Microsoft Docs
description: "Denne tjeneste er tæt integration med Office 365, så du kan dele kontaktpersoner mellem Outlook og Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: contacts, Office 365
ms.date: 04/09/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: fa6779ee8fb2bbb453014e32cb7f3cf8dcfa18da
ms.openlocfilehash: b535255be4b751744ae8c459bdc3d87cd1271dee
ms.contentlocale: da-dk
ms.lasthandoff: 04/11/2018

---
# <a name="synchronize-contacts-in-business-central-with-contacts-in-microsoft-outlook"></a>Synkronisere kontaktpersoner i Business Central med kontaktpersoner i Microsoft Outlook
Du kan se de samme kontaktpersoner i [!INCLUDE[d365fin](includes/d365fin_md.md)] som i Outlook, hvis du har oprettet synkronisering af kontaktpersoner. Hvis du er sælger, udfører du måske noget af dit arbejde i Outlook og noget af dit arbejde i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis kontakterne er identiske begge steder, gør det dit arbejde mere enkelt.  

En dedikeret mappe i Outlook gør det nemt at finde kontaktpersoner, og du kan indstille et filter til at synkronisere de kontakter fra [!INCLUDE[d365fin](includes/d365fin_md.md)], som du vil have vist i Outlook. Når kontaktsynkroniseringen er oprettet, kan du starte synkroniseringen manuelt eller oprette en automatisk synkronisering, der regelmæssigt kan sørge for, at kontakterne bliver synkroniseret.  

## <a name="set-up-synchronization"></a>Konfigurere synkronisering
Du angiver, hvordan du vil synkronisere kontaktpersoner med Outlook i vinduet **Opsætning af Exchange-synkronisering** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Som en forudsætning skal din Office 365-mailkonto være angivet i din brugerprofil i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan kontrollere dette i sektionen **Office 365-godkendelse** i din brugerprofil på listen **Brugere**.  

I vinduet **Opsætning af Exchange-synkronisering** kan du kontrollere, at forbindelsen til Exchange fungerer, og derefter konfigurere synkroniseringen. Åbn vinduet **Opsætning af Exchange-synkronisering**, og start synkroniseringen. Du kan også angive et filter for, hvilke kontakter der skal synkroniseres mellem [!INCLUDE[d365fin](includes/d365fin_md.md)] og Outlook. For eksempel kan du angive et filter for navn, type, virksomhed eller lignende. Du kan også ændre standardnavnet på den mappe, som kontakterne skal synkronisere i Outlook. Standardnavnet er *Business Central*.  

Når synkroniseringen er blevet oprettet, synkroniseres ændringer, som du foretager af kontakten i enten Outlook eller i [!INCLUDE[d365fin](includes/d365fin_md.md)], med den anden kontaktperson.  

Hver af dine kolleger kan også oprette deres egen Exchange-synkronisering og angive deres eget filter for, hvilke kontakter der skal synkroniseres.  

## <a name="synchronize-contacts"></a>Synkronisere kontakter
Hvis du plejer at arbejde med kontaktpersoner i [!INCLUDE[d365fin](includes/d365fin_md.md)], vil du finde det let at starte synkroniseringen manuelt, når det passer dig, fra oversigten **Kontakter**. Vælg handlingen **Synkroniser med Office 365**, og afgør, om du vil ændre det filter, du har oprettet. Når du klikker på knappen OK, starter synkroniseringen med det samme, og de seneste ændringer anvendes på dine kontakter i Outlook.  

I oversigten **Kontakter** kan du synkronisere kontakter på to måder:

* **Synkroniser med Office 365**

  Denne handling synkroniserer alle ændringer fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til Office 365 siden den forrige synkronisering baseret på den seneste ændringsdato. Eventuelle nye kontakter fra Office 365 synkroniseres tilbage til [!INCLUDE[d365fin](includes/d365fin_md.md)] også. Dette er typisk hurtigere end at foretage en fuld synkronisering.  

* **Komplet synkronisering med Office 365**

  Denne handling synkroniserer alle kontakter i begge retninger, uanset datoen for sidste synkronisering og datoen for seneste ændring.  

I begge tilfælde synkroniseres kontakter kun fra Outlook, hvis de nødvendige felter er udfyldt. De obligatoriske felter for synkronisering til Office 365 er **Navn**, **Mailadresse**, og de skal være af typen Person. [!INCLUDE[d365fin](includes/d365fin_md.md)] er overordnet med hensyn til kontaktoplysninger, så kontaktoplysninger fra [!INCLUDE[d365fin](includes/d365fin_md.md)] gemmes i tilfælde af dubletter.  

I Outlook vises kontakter fra [!INCLUDE[d365fin](includes/d365fin_md.md)] i en mappe under **Andre kontakter** i visningen **Personer**. Hvis du ikke kender visningen Personer i Outlook, kan du gå til den fra indstillingerne for navigation i nederste venstre hjørne af Outlook.  

## <a name="see-also"></a>Se også
[Introduktion](product-get-started.md)  
[Finans](finance.md)  
[Salg](sales-manage-sales.md)  
[Køb](purchasing-manage-purchasing.md)  
[Bruge kontaktpersoner (Personer) i Outlook på internettet](https://support.office.com/en-us/article/Using-contacts-People-in-Outlook-on-the-web-1e3438c7-26b2-420c-87de-3cea9d31b5cb?appver=OWB150)  
