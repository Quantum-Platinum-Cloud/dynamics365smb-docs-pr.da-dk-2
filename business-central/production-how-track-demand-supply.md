---
title: Spore relationer mellem behov og forsyning
description: 'I dette emne forklares forskellige metoder til at spore relationer mellem behov og levering, f. eks. sporing af sammenkædede varer og håndtering af ikke-sporede planlægningselementer.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5830, 9101, 99000822, 99000855'
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="track-relations-between-demand-and-supply" />Spore relationer mellem behov og forsyning

Fra ethvert forsynings- eller behovsdokument i det såkaldte ordrenetværk, kan du spore ordrebehov (sporet antal), forecast, rammesalgsordre eller planlægningsparameter (ikkesporet antal), der er årsag til den pågældende planlægningslinje.

Planlægningskladderne indeholder også yderligere planlægningsoplysninger om ikke-ordreenheder for at hjælpe planlæggeren med at opnå den optimale forsyningsplan. Du kan finde flere oplysninger i [Ikke-sporede planlægningselementer](production-how-track-demand-supply.md#untracked-planning-elements).

## <a name="to-track-linked-items" />Sådan spores tilknyttede varer
Ordresporing viser, hvordan salgsordrer, produktionsordrer og købsordrer er relaterede til produktionsordrer via planlægnings- og reservationssystemerne.

Nedenstående beskrives, hvordan tilknyttede varer spores på en fastlagt produktionsordre. Trinene er de samme for alle andre typer og i forbindelse med planlægningskladdelinjer.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Fastlagt produktionsordre**, og vælg derefter det relaterede link.
2. Åbn den relevante fastlagte produktionsordre på listen.
3. I oversigtspanelet **Linjer** skal du vælge handlingen **Funktioner** og derefter vælge handlingen **Ordresporing**.

På linjerne i vinduet **Ordresporing** vises de bilag, der har relation til den aktuelle produktionsordrelinje.

## <a name="untracked-planning-elements" />Ikke-sporede planlægningselementer
Siden **Ikke-sporede planlægningselementer** åbnes, når du klikker på feltet **Ikke-sporet antal** på siden **Ordreplanlægning**. Det tjener to formål:

1. Indeholde oplysninger om ikke-sporet antal, der vises, når brugeren slår op fra siden Ordresporing for at få vist ikke-sporede antal.
2. Det skal indeholde advarselsmeddelelser, der vises, når brugeren vælge ikonet **Advarsel** på siden **Planlægningskladde**.

Siden indeholder poster for ikke-sporet overskud i ordresporingsnetværket. Disse poster genereres i forbindelse med planlægningskørslen og forklarer, hvor det ikke-sporede overskud på ordresporingslinjerne stammer fra. Det ikke-sporede overskud kan stamme fra:

- Produktionsforecast
- Rammeordrer
- Sikkerhedslager
- Genbestillingspunkt
- Maks. lagerbeholdning
- Ordrekvantum
- Maks. ordrestørrelse
- Min. ordrestørrelse
- Oprundingsfaktor
- Aktionsgrænse (% af lotstr.)

## <a name="see-also" />Se også
[Planlægning](production-planning.md)   
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Reservation, sporing og aktionsmeddelelser](design-details-reservation-order-tracking-and-action-messaging.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejd med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
