---
title: Feltkobling, når du importerer SEPA CAMT-filer | Microsoft Docs
description: Du kan indlæse bankkontoudtogsfiler i de regionale SEPA-standarder (Single Euro Payments Area) på europæiske markeder.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: db90358fcca87bc7217d48efa7577e8d4a835c58
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2022
ms.locfileid: "8521354"
---
# <a name="field-mapping-when-importing-sepa-camt-files" /><a name="field-mapping-when-importing-sepa-camt-files"></a>Feltkobling, når du importerer SEPA-CAMT-filer
[!INCLUDE[prod_short](includes/prod_short.md)] understøtter de regionale SEPA-standarder for import af SEPA-kontoudtog fra banken (CAMT-format). Du kan finde flere oplysninger i [Brug AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md).  

 SEPA CAM-standarden har selv lokale variationer. Derfor er du muligvis nødt til at ændre udvekslingsopsætningen for generiske data (repræsenteret af koden **SEPA CAMT** på siden **Bogføringsudvekslingsdefinitioner**) for at tilpasse den til en lokal variant af standarden. Følgende tabeller viser tilknytningen af element til felt for tabel 81, 273 og 274 i implementeringen af SEPA CAMT i [!INCLUDE[prod_short](includes/prod_short.md)].  

 Du kan finde oplysninger om oprettelse eller justering af en dataudvekslingsdefinition i [Konfigurere dataudvekslingsdefinitioner](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="camt-data-mapping-to-fields-in-the-general-journal-table-81" /><a name="camt-data-mapping-to-fields-in-the-general-journal-table-81"></a>CAMT-datatilknytning til felter i tabellen Finanskladde (81)

|Sti til element|Meddelelseselement|Datatype|Beskrivelse|Identifikator for minustegn|Feltnr.|Feltnavn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Beløb|Decimal|Pengebeløbet i kontantposten.||13|Beløb|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Tekst|Angiver, om posten er en kreditnota eller en debitering|DBIT|13|Beløb|  
|Stmt/Ntry/BookgDt/Dt|Dato|Dato|Dato, når der bogføres en post til en konto på kontoservicens bøger||5|Bogføringsdato|  
|Stmt/Ntry/BookgDt/DtTm|Dato og klokkeslæt|Dato og klokkeslæt|Dato og klokkeslæt, når der bogføres en post til en konto på kontoservicens bøger||5|Bogføringsdato|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Navn|Tekst|Navnet på den part, som skylder et pengebeløb til slutkreditor||1221|Oplysninger om indbetaler|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ustrukturerede|Tekst|Oplysninger, der gives for at aktivere matchning/afstemning af en post med de varer, som betalingen er beregnet til at udligne, f.eks fakturaer i et debitorsystem, på en ustruktureret måde||8|Beskrivelse|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Tekst|Yderligere oplysninger om posten||1222|Oplysninger om transaktion|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273" /><a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-table-273"></a>CAMT-datatilknytning til felter i tabellen Bankkontoafstemning (273)

|Sti til element|Meddelelseselement|Datatype|Beskrivelse|Identifikator for minustegn|Feltnr.|Feltnavn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/CreDtTm|CreationDateTime|Dato|Den dato og det klokkeslæt, hvor meddelelsen blev oprettet||3|Kontoudtogsdato|  
|Stmt/Bal/Amt|Beløb|Decimal|Det beløb, der er resultatet af nettobeløbene for alle debet- og kreditposter||4|Kontoudtogs slutsaldo|  

## <a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274" /><a name="camt-data-mapping-to-fields-in-the-bank-acc-reconciliation-line-table-274"></a>CAMT-datatilknytning til felter i tabellen Bankkto.afstemningslinje (274)

|Sti til element|Meddelelseselement|Datatype|Beskrivelse|Identifikator for minustegn|Feltnr.|Feltnavn|  
|------------------|---------------------|---------------|-----------------|-------------------------------|---------------|----------------|  
|Stmt/Ntry/Amt|Beløb|Decimal|Pengebeløbet i kontantposten.||7|Kontoudtogsbeløb|  
|Stmt/Ntry/CdtDbtInd|CreditDebitIndicator|Tekst|Angiver, om posten er en kreditnota eller en debitering|DBIT|7|Kontoudtogsbeløb|  
|Stmt/Ntry/BookgDt/Dt|Dato|Dato|Dato, når der bogføres en post til en konto på kontoservicens bøger||5|Transaktionsdato|  
|Stmt/Ntry/BookgDt/DtTm|Dato og klokkeslæt|Dato og klokkeslæt|Dato og klokkeslæt, når der bogføres en post til en konto på kontoservicens bøger||5|Transaktionsdato|  
|Stmt/Ntry/ValDt/Dt|Dato|Dato|Dato, når aktiver bliver tilgængelige for ejeren af kontoen i forbindelse med en kreditpost eller ophører med at være tilgængelig for ejeren af kontoen i tilfælde af en debetpost||12|Valørdato|  
|Stmt/Ntry/ValDt/DtTm|Dato og klokkeslæt|Dato og klokkeslæt|Dato og klokkeslæt, når aktiver bliver tilgængelige for ejeren af kontoen i forbindelse med en kreditpost eller ophører med at være tilgængelig for ejeren af kontoen i tilfælde af en debetpost||12|Valørdato|  
|Stmt/Ntry/NtryDtls/TxDtls/RltdPties/Dbtr/Nm|Navn|Tekst|Navnet på den part, som skylder et pengebeløb til slutkreditor||15|Oplysninger om indbetaler|  
|Stmt/Ntry/NtryDtls/TxDtls/RmtInf/Ustrd|Ustrukturerede|Tekst|Oplysninger, der gives for at aktivere matchning/afstemning af en post med de varer, som betalingen er beregnet til at udligne, f.eks fakturaer i et debitorsystem, på en ustruktureret måde||6|Beskrivelse|  
|Stmt/Ntry/AddtlNtryInf|AdditionalEntryInformation|Tekst|Yderligere oplysninger om posten||16|Oplysninger om transaktion|  

 Elementer i noden **Ntry**, der importeres i [!INCLUDE[prod_short](includes/prod_short.md)], men som ikke knyttes til nogen felter, gemmes i tabellen **Kolonnedef for bogf.udveksling**. Brugere kan få vist disse elementer på siderne **Betalingsudligningskladde**, **Betalingsudligning**, og **Bankkontoafstemning** ved at vælge handlingen **Oplysninger om bankkontoudtogslinje**. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

> [!IMPORTANT]
> Når du importerer CAMT-bankkontoudtog, forventer [!INCLUDE[prod_short](includes/prod_short.md)], at hver transaktion er entydig, hvilket vil sige, at feltet **Transaktions-id**, som stammer fra *Stmt/Ntry/NtryDtls/TxDtls/REFS/EndToEndId* i CAMT-filen, skal være entydig inden for den åbne bankkontoafstemning. Hvis oplysningerne ikke er til stede, [!INCLUDE[prod_short](includes/prod_short.md)] ignoreres betalingen. Hvis en tidligere bankafstemning på den samme bankkonto er bogført med samme transaktions-ID som ved den aktuelle import, vil den aktuelle transaktion ikke automatisk blive afstemt, men kan stadig indlæses.

## <a name="see-also" /><a name="see-also"></a>Se også
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Udveksle data elektronisk](across-data-exchange.md)  
[Brug AMC Banking 365 Fundamentals-udvidelsen](ui-extensions-amc-banking.md)   
[Brug XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
