---
title: Sådan allokeres ressourcer | Microsoft Docs
description: 'Du kan ændre det årlige beløb på en servicekontrakt eller et kontrakttilbud til det korrekte beløb, der faktureres årligt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="allocate-resources" />Allokere ressourcer
Det vigtigste element i servicestyring er de mennesker, der leverer servicen. Du kan konfigurere [!INCLUDE[prod_short](includes/prod_short.md)] til at tildele de relevante personer til de relevante job. Opgaverne kan baseres på servicezoner, hvor personerne befinder sig, eller hvor servicen finder sted. Du kan desuden gruppere ressourcerne, når der reageres på serviceanmodninger. Du kan finde flere oplysninger i [Definere ressourceallokering](service-how-setup-resource-allocation.md).

Du kan allokere ressourcer, f.eks. teknikere, ved hjælp af **Ordreoversigt** eller fra en serviceordre. Du kan bruge ressourcedisponering til at allokere ressourcer, der skal udføre serviceopgaverne i ordrerne eller tilbuddene.

Du kan allokere den samme ressource, f.eks. en tekniker, eller ressourcegruppe til alle serviceartiklerne i en serviceordre. Der oprettes allokeringsposter for de andre serviceartikler i ordren med samme ressourcenummer og allokeringsdato som den linje, du har allokeret. De allokerede timer er de timer, du har allokeret, delt med antallet af serviceartikler i ordren. Feltet **Status** indstilles automatisk til **Aktiv** for alle poster, der er oprettet.

## <a name="to-see-an-overview-of-service-orders-and-service-quotes" />Sådan får du vist en oversigt over serviceordrer og -tilbud
Du kan ofte få brug for at se listen over serviceordrer eller servicetilbud, som opfylder bestemte krav, så du kan udføre bestemte handlinger på hver enkelt af dem. Du kan f.eks. få brug for at allokere ressourcer til serviceordrer, der hører til en bestemt kunde.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ordreoversigt**, og vælg derefter det relaterede link.  
2. Vælg den type dokumenter, du vil have vist, i feltet **Dokumentfilter**.
3. Hvis du vil se en liste over dokumenter, der indeholder serviceopgaver, som en bestemt ressource eller ressourcegruppe er allokeret til, skal du udfylde felterne **Ressourcefilter** og **Ressourcegruppefilter** og trykke på <kbd>Enter</kbd>.  
4. Hvis du vil have vist en liste over dokumenter, der har en eller flere bestemte svardatoer inden for en bestemt periode, skal du udfylde feltet **Svardatofilter** og trykke på <kbd>Enter</kbd>.  
5. Hvis du vil have vist en liste over dokumenter, der indeholder en bestemt allokeringsstatus eller dokumentstatus, skal du udfylde feltet **Allokeringsfilter/Statusfilter** og trykke på <kbd>Enter</kbd>.  
6. Hvis du vil have vist en liste over dokumenter, der tilhører en bestemt kontrakt, debitor eller zone, skal du udfylde feltet **Kontraktfilter/Debitorfilter/Zonefilter** og trykke på <kbd>Enter</kbd>.  
7. Vælg en linje, der svarer til en serviceordre eller et servicetilbud, og vælg derefter handlingen **Vis bilag**.  

    Siden **Serviceordre** eller **Servicetilbud** åbnes, og du kan arbejde med dokumentet. Hvis du vil tilbage til siden **Ordreoversigt**, skal du vælge **OK**.

## <a name="to-allocate-a-resource-using-resource-or-resource-group-availability" />Sådan allokeres ressourcer vha. ressourcedisponering eller ressourcegruppedisponering
1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ordreoversigt**, og vælg derefter det relaterede link.  
2. Vælg serviceordren, og vælg derefter handlingen **Ressourceallokeringer**.  
3. Vælg posten med den serviceopgave, du vil allokere en ressource til.  
4. Vælg enten handlingen **Ressourcedisponering** eller handlingen **Ressourcegruppedisponering**.  
5. På siden **Ressourcedisponering (Service)** skal du vælge **Vis matrix**.  
6. Vælg en ressource, du vil allokere. Du kan basere valget på, om ressourcen er klar til opgaven, om den er placeret i kundezonen, og/eller om ressourcen foretrækkes af kunden.  
7. Angiv en dato, hvor ressourcen har nok ledige timer til opgaven, og som er tæt på serviceordrens svardato.  
8. Angiv det antal timer, du vil allokere ressourcen til serviceopgaver, i feltet **Antal til fordeling**.  
9. Vælg handlingen **Alloker** for at allokere den valgte ressource på den valgte dag.  

     Feltet **Status** indstilles automatisk til **Aktiv**.  

 Gentag disse trin for hver dato, du vil allokere ressourcen til serviceopgaven.  

> [!NOTE]  
>  Der kan kun være **aktive** allokeringsposter med én ressource eller ressourcegruppe ad gangen.  

## <a name="to-allocate-a-resource-using-a-service-order" />Allokere ressourcer ved hjælp af en serviceordre
Når du har oprettet og udfyldt en serviceordre eller et servicetilbud, kan du allokere ressourcer, f.eks. teknikere, til udførelse af serviceopgaver, der er registreret som serviceartikellinjer i dokumentet.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Vælg serviceordren, og vælg derefter **Rediger**.  
3. Vælg den serviceartikellinje, der svarer til den serviceopgave, du vil allokere en ressource til.  
4. Vælg **Ressourceallokeringer**.
5. Vælg en ikke-aktiv allokeringspost på siden **Ressourceallokeringer** for den serviceopgave, du vil allokere ressourcen til. Hvis den allokeringsposten ikke findes, kan du oprette en ny ved at vælge **Ny**.  
7. Angiv serviceopgaven ved at udfylde feltet **Serviceartikelnr.** på samme linje.  
8. Vælg ressourcen i feltet **Ressourcenr.**. Hvis ressourcen er med i en ressourcegruppe, indsættes nummeret på ressourcegruppen automatisk i feltet **Ressourcegruppenr.**. .  
9. Udfyld felterne **Allokeringsdato** og **Allokerede timer**. Feltet **Status** er angivet til statussen **Aktiv**. Dette angiver, at ressourcen er allokeret til serviceopgaven.  
10. Du kan også vælge **Alloker til alle serviceartikler** for at tildele ressourcen til alle artikler.

> [!NOTE]  
>  En serviceartikel i en serviceordre kan kun indeholde aktive allokeringsposter med én ressource eller ressourcegruppe ad gangen.

## <a name="to-reallocate-resources-on-a-service-order" />Sådan genallokeres ressourcer på en serviceordre
Du kan genallokere ressourcer direkte fra den serviceordre eller det servicetilbud, som du arbejder med. Den oprindelige post findes stadigvæk, men dens status opdateres på følgende måde:  

* Hvis reparationen blev startet, da allokeringen var **Aktiv**, dvs. hvis reparationsstatus for serviceartiklen i posten blev ændret til **I arbejde**, ændres allokeringsstatus automatisk fra **Genallokering nødvendig** til **Udført**.  
* Hvis reparationen ikke blev påbegyndt, mens allokeringen var **Aktiv**, ændrer programmet allokeringsstatus fra **Genallokering nødvendig** til **Annulleret**.  
* Hvis du genallokerer en serviceordre, som du har konverteret fra et tilbud, ændres status altid automatisk for de allokeringsposter, der er registreret for tilbuddet, til **Udført**, når du genallokerer serviceartiklerne i serviceordren.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Åbn den relevante serviceordre.  
3. Vælg den serviceartikellinje, der svarer til den serviceopgave, du vil allokere en ressource til, og vælg derefter handlingen **Ressourceallokeringer**.  
4. Vælg en allokeringspost med den serviceopgave, som du vil genallokere ressourcen til, på siden **Ressourceallokeringer**. Vælg den relevante ressource i feltet **Ressourcenr.**. Dette overskriver det ressourcenummer, der i forvejen var i feltet.  
5. Vælg <kbd>Enter</kbd>. Der åbnes en dialogboks, hvor du bliver spurgt, om du vil genallokere posten. Udfyld eventuelt feltet **Årsagskode**, og vælg knappen **Ja** for at bekræfte genallokeringen.  
6. Udfyld felterne **Allokeringsdato** og **Allokerede timer**. Posten indeholder nu den nye ressource, og status for posten er **Aktiv**.

## <a name="to-reallocate-a-resource-using-the-dispatch-board" />Sådan genallokeres ressourcer ved hjælp af ordreoversigten
Hvis den ressource, der er allokeret til en serviceopgave, ikke kan udføre arbejdet, betyder det, at serviceopgaven skal genallokeres. Ressourcer genallokeres som regel til en serviceopgave ved hjælp af **Ordreoversigt**.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ordreoversigt**, og vælg derefter det relaterede link.  
2. Vælg **Genallokering nødvendig** i feltet **Allokeringsfilter**. På siden **Ordreoversigt** vises de serviceordrer, som indeholder serviceopgaver, der skal genallokeres.  
3. Vælg den relevante serviceordre, og vælg derefter handlingen **Ressourceallokeringer**. Siden **Ressourceallokeringer** åbnes.  
4. Marker allokeringsposten med den serviceopgave, du vil genallokere en ressource til.  
5. Vælg den relevante ressource i feltet **Ressourcenr.**. Dermed overskrives det ressourcenummer, der i forvejen var i feltet.  
6. Vælg <kbd>Enter</kbd>. Dialogboksen **Genallokering af poster** åbnes. Angiv, om du vil genallokere denne post. Udfyld eventuelt feltet **Årsagskode**, og vælg knappen **Ja** for at bekræfte genallokeringen.  
7.  Udfyld felterne **Allokeringsdato** og **Allokerede timer**. Posten indeholder nu den nye ressource, og status for posten er **Aktiv**.  

    > [!NOTE]  
    >  Den gamle post findes stadigvæk, men dens status opdateres automatisk på følgende måde:  
    >   
    >  * Hvis reparationen blev startet, da allokeringen var **Aktiv**, dvs. hvis reparationsstatus for serviceartiklen i posten blev ændret til **I arbejde**, ændres allokeringsstatus automatisk fra **Genallokering nødvendig** til **Udført**.  
    > * Hvis reparationen ikke blev påbegyndt, mens allokeringen var **Aktiv**, bliver allokeringsstatus ændret fra **Genallokering nødvendig** til **Annulleret**.  
    > * Hvis du genallokerer en serviceordre, som du har konverteret fra et tilbud, ændres status altid automatisk for de allokeringsposter, der er registreret for tilbuddet, til **Udført**, når du genallokerer serviceartiklerne i serviceordren.  

## <a name="to-register-resource-hours" />Sådan registreres ressourcetimer
Når du arbejder med serviceartikler i serviceordrer, har du brug for at registrere de ressourcetimer, der anvendes på serviceydelsen. Følgende fremgangsmåde viser, hvordan ressourcetimerne skal registreres på siden **Serviceartikelkladde**.  

Du kan bruge samme fremgangsmåde til at registrere timerne på siden **Servicelinjer**, som du kan åbne fra siden Serviceordre. Åbn det relevante servicekort, og vælg handlingen **Servicelinjer**.  

Hvis samme ressource arbejder på alle serviceartiklerne i serviceordren, kan du registrere de samlede ressourcetimer for kun én serviceartikel og derefter opdele ressourcelinjen for at tildele ressourcetimer til de andre serviceartikler.

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceopgaver** og vælg derefter det relaterede link.
2. Vælg den linje, der indeholder den relevante serviceartikel, og vælg derefter handlingen **Artikelkladde**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-a-resource-to-all-service-items-in-an-order" />Sådan tildeles en ressource til alle serviceartikler i en ordre
Hvis samme ressource (f.eks. en tekniker) arbejder på alle serviceartiklerne i serviceordren, kan du registrere de samlede ressourcetimer for kun én serviceartikel og derefter opdele ressourcelinjen for at opdele ressourcetimerne på ressourcelinjerne for de andre serviceartikler.  

Følgende fremgangsmåde viser, hvordan ressourcelinjerne på siden **Servicefakturalinjer** kan opdeles.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, angiv **Serviceordre** og vælg derefter det relaterede link.  
2. Åbn den relevante serviceordre.  
3. I oversigtspanelet **Linjer** skal du vælge handlingen **Servicelinjer**. Siden **Servicelinjer** åbnes.  
4. Vælg den ressourcelinje, du vil opdele. Oplysningerne i feltet **Antal** opdeles automatisk mellem alle serviceartiklerne i ordren.  
5. Vælg handlingen **Opdel ressourcelinje**. Vælg **Ja** for at bekræfte.  

    Der oprettes ressourcelinjer for de andre serviceartikler i ordren med samme ressourcenummer som den linje, du har opdelt. Antallet er det antal, der er angivet for den opdelte linje delt med antallet af serviceartikler i ordren.  

## <a name="to-cancel-an-allocation" />Sådan annulleres allokeringer
Du kan annullere ressourceallokeringer til serviceopgaver uden at genallokere opgaverne.  

1. Vælg ![Lightbulb, der åbner funktionen Fortæl mig.](media/ui-search/search_small.png "Fortæl mig, hvad du vil foretage dig") ikon, skriv **Ordreoversigt**, og vælg derefter det relaterede link.  
2. Vælg serviceordren, og vælg derefter handlingen **Ressourceallokeringer**.  
3. Vælg allokeringsposten med den serviceopgave, du vil annullere allokeringen for.  
4. Vælg handlingen **Annuller allokering**.  
5. Vælg den relevante årsagskode i feltet **Årsagskode**.  
6. Vælg **Ja** for at bekræfte annulleringen.  

    > [!NOTE]  
    > Indstillingen **Genallokering nødvendig** i feltet **Status** markeres automatisk. Hvis reparationsstatus for serviceartiklen i posten er **Oprettet**, ændres reparationsstatus automatisk til **Henvist**, dvs. at der ikke er påbegyndt nogen reparation. Hvis reparationsstatus er **I arbejde**, ændres den til **Delvist repareret**, dvs. at en del af reparationen er udført.

## <a name="see-also" />Se også
[Opsætte ressourceallokering](service-how-setup-resource-allocation.md)  
[Allokeringsstatus og reparationsstatus](service-allocation-status-and-repair-status.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
