---
title: Teams, ofte stillede spørgsmål
description: Få svar på nogle typiske spørgsmål om arbejde med Teams og Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, faq, errors
ms.date: 05/19/2021
ms.author: jswymer
ms.openlocfilehash: 325783df3cacd37250c1efa75320386ef9c4cb19
ms.sourcegitcommit: eeaf9651c26e49974254e29b7e2d16200c818dad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6341504"
---
# <a name="teams-faq"></a>Teams, ofte stillede spørgsmål

[!INCLUDE [online_only](includes/online_only.md)]

I denne artikel besvares nogle af de spørgsmål, du kan have om at arbejde med Teams og [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Generelt](#tab/general)

### <a name="how-do-i-sign-in-to-the-prod_shortmd-app-in-teams"></a>Hvordan logger jeg på [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Når du har installeret appen, bliver du bedt om at logge på, første gang du bruger appen, indsætte et link til [!INCLUDE [prod_short.md](includes/prod_short.md)] i Teams-chatten eller vælge handlingen **Detaljer** på et kort i Teams. Afhængigt af Teams-klienten skal du muligvis angive dine legitimationsoplysninger, som du bruger til at få adgang til [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-sign-out-of-the-prod_shortmd-app-in-teams"></a>Hvordan logger jeg ud fra [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Hvis du vil aflogge den nuværende brugeridentitet i Teams, som bruges til at oprette forbindelse til [!INCLUDE [prod_short.md](includes/prod_short.md)], skal du gå til en vilkårlig chatboks og vælge ikonet for [!INCLUDE [prod_short.md](includes/prod_short.md)] nedenfor og vælge **Indstillinger**. Når vinduet vises, skal du kontrollere den identitet, der er logget på i øjeblikket, og derefter vælge **Log af**.

### <a name="does-the-app-for-teams-connect-to-prod_shortmd-on-premises"></a>Er appen for Teams tilsluttet [!INCLUDE [prod_short.md](includes/prod_short.md)] på stedet? 

Nummer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams fungerer kun sammen med [!INCLUDE [prod_short.md](includes/prod_short.md)] online. Der er ingen planer om at understøtte [!INCLUDE [prod_short.md](includes/prod_short.md)]-installationstyper&mdash;f.eks. i det lokale miljø, hybrid-sky eller privat sky&mdash;som Microsoft hverken er vært for eller administrerer direkte.

### <a name="does-the-app-work-with-multiple-companies-and-environments"></a>Fungerer appen med flere virksomheder og miljøer? 

Ja. Hvis du vil søge efter kontakter i et andet regnskab, skal du gå til [Indstillinger](across-teams-settings.md). Når [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen udvider et link til et kort, skal tilknytningen indeholde miljø- og firmanavnene for appen for at matche posten i den rigtige virksomhed. Du kan indsætte links til virksomheder og miljøer, som du har adgang til i virksomheden og fra den [!INCLUDE [prod_short.md](includes/prod_short.md)]-konto, du har brugt til at logge på. Deltagerne i chatten vil se kortet. Men de kan ikke se kortdetaljerne, medmindre de har tilladelse til det firma eller -miljø, hvor denne post er gemt.

### <a name="in-which-countries-or-regions-is-the-prod_shortmd-app-available"></a>I hvilke lande eller områder er [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen tilgængelig? 

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams er ikke begrænset af land eller område. Appen er tilgængelig på alle markeder, der aktuelt understøttes af markedspladsen Teams. 

### <a name="does-the-prod_shortmd-app-work-with-any-localization-of-prod_shortmd"></a>Kan [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen fungere med enhver lokalisering af [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Ja. Appen er beregnet til at fungere sammen med enhver lokalisering af [!INCLUDE [prod_short.md](includes/prod_short.md)], om denne lokalisering tilbydes direkte fra Microsoft eller fra en partner. Du kan finde flere oplysninger i [Tilgængelighed i land/område og understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json).

### <a name="which-languages-does-the-prod_shortmd-app-support"></a><a name="language"></a>Hvilke sprog [!INCLUDE [prod_short.md](includes/prod_short.md)] understøtter app'en?

To ting bestemmer det sprog, der bruges til kort- og kort detaljer i Teams:

1. Dit sprog i Teams, som du kan se fra kontoindstillingerne i Teams. 
2. Dit sprog i [!INCLUDE [prod_short.md](includes/prod_short.md)], som du kan se [!INCLUDE [prod_short.md](includes/prod_short.md)]-webklienten med (Se [Skift af grundlæggende indstilling - sprog](ui-change-basic-settings.md#language)).

I følgende tabel forklares det, hvordan oplevelsen adskiller sig fra meddelelses forfattere og-modtagere, afhængigt af sprogindstillingerne og tilgængeligheden af sprog.

|Hvem|Kort|Kortdetaljer |
|-|----|--------------| 
|Meddelelsesforfatter |Vises på det sprog, der er angivet for dig i Teams. Hvis [!INCLUDE [prod_short.md](includes/prod_short.md)] ikke tilbyder det samme sprog, vises kortet på engelsk. |Vises på det sprog, der er angivet for dig i [!INCLUDE [prod_short.md](includes/prod_short.md)].  som kan indeholde sprog fra sprog-apps, der stammer fra partnere. |
|Meddelelsesmodtager |Vises på sproget for meddelelsens forfatter. |Vises på det sprog, der er angivet for dig i [!INCLUDE [prod_short.md](includes/prod_short.md)]. |

Du kan finde en liste over understøttede sprog til [!INCLUDE [prod_short.md](includes/prod_short.md)] i [Understøttede sprog](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations?toc=/dynamics365/business-central/toc.json#supported-languages).

### <a name="does-the-prod_shortmd-app-work-with-industry-solutions"></a>Samarbejder appen [!INCLUDE [prod_short.md](includes/prod_short.md)] med andre brancheløsninger?

Ja. Det er imidlertid kun nogle funktioner i appen, der fungerer med [Integrer apps](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview):

- Appen fungerer sammen med links, der er baseret på mønsteret for **\*.bc.dynamics.com**, som typisk bruges sammen med Integrer apps.
- Kontaktsøgning er ikke tilgængelig for Integrer apps, som erstatter basisprogrammet fra Microsoft.

### <a name="where-can-i-find-teams-integration-inside-the-prod_shortmd-web-client"></a>Hvor kan jeg finde Teams-integrationen i [!INCLUDE [prod_short.md](includes/prod_short.md)]-webklienten? 

I øjeblikket er der ingen integrering af Teams-kontrolenheder eller tilstedeværelse af Teams-funktioner i [!INCLUDE [prod_short.md](includes/prod_short.md)]-webklienten eller andre klienter.

### <a name="does-prod_shortmd-work-with-the-teams-mobile-app"></a>Arbejder [!INCLUDE [prod_short.md](includes/prod_short.md)] med Teams mobilapp?

Ja. Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] kan installeres fra den Teams desktopappen eller browseren - eller af en administrator for alle brugere. Når [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen er installeret, er den automatisk tilgængelig i Teams til iOS og Android. På mobilenheder kan du kun få vist kort, der er sendt af andre, få adgang til oplysninger, eller du kan få vist kortet i sin helhed i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Du kan dog ikke indsætte links, som kan udvides til kort, når du opretter meddelelser eller søger efter kontakter. Du kan se minimumskrav til mobil under [Minimumskrav til brug af Business Central](product-requirements.md).

### <a name="is-the-prod_shortmd-app-for-teams-the-same-as-the-prod_shortmd-app-for-ios-and-android"></a>Er [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams den samme som [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til iOS og Android?

Nummer Appen til Teams er et tilføjelsesprogram til Microsoft Teams og er udelukkende beregnet til samarbejdsoplevelser i Teams. På den anden side giver [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen en omfattende oplevelse, så du kan arbejde med [!INCLUDE [prod_short.md](includes/prod_short.md)]-data på dine mobilenheder.

Mobilbrugere opfordres til at installere både mobilappen og appen til Teams for at få mest muligt ud af [!INCLUDE [prod_short.md](includes/prod_short.md)]. Når begge er installeret, kan du vælge **Pop op**-handlingen på et kort i Teams for at åbne kortdetaljerne i [!INCLUDE [prod_short.md](includes/prod_short.md)]-mobilappen. Du kan finde oplysninger om installation af [!INCLUDE [prod_short.md](includes/prod_short.md)] og Teams mobilapps på:

- [Hent Business Central til din mobilenhed](install-mobile-app.md)
- [Hent Teams mobilappen](https://support.microsoft.com/office/download-the-mobile-app-for-teams-5940ebdc-0082-4fb1-83c4-751edc23dcb5) på Microsoft Support

### <a name="does-the-prod_shortmd-app-work-in-all-teams-clients"></a>Fungerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i alle Teams-klienter?

Nummer Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams understøttes ikke, når den installeres som en pakke til macOS eller Linux. På disse platforme kan du få adgang til Teams ved hjælp af en understøttet webbrowser i stedet.

Du kan se minimumskrav til [!INCLUDE [prod_short.md](includes/prod_short.md)] i [Minimumskrav til brug af Business Central](product-requirements.md#teams).

Der er flere oplysninger om, hvordan du vælger Teams-klienter, og hvordan du installerer dem, i [Hent klienter til Microsoft Teams](/microsoftteams/get-clients)-dokumentationen til Teams.

### <a name="which-teams-client-is-best-for-prod_shortmd"></a>Hvilke Teams-klienter er bedst til [!INCLUDE [prod_short.md](includes/prod_short.md)]?

Der er kun mindre forskelle og begrænsninger mellem Teams-klienter, som kan påvirke din oplevelse med [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams. Når du vælger en Teams-klient, skal du overveje:

- Du kan ikke få adgang til kameraet og lokationen i oplysningsvinduet i computerappen for Teams.
- Telefonnumre kan ikke aktiveres fra oplysningsvinduet i Teams til iOS, Team til Android eller Teams i browseren.
- Bruger du Microsoft Edge sammen med Teams i browseren, kan du nemt arbejde på tværs af flere identiteter og konti ved at logge på Teams fra forskellige profiler. Du kan lære mere om brugen af profiler i Microsoft Edge under [Log på og opret flere profiler i Microsoft Edge](https://support.microsoft.com/office/sign-in-and-create-multiple-profiles-in-microsoft-edge-df94e622-2061-49ae-ad1d-6f0e43ce6435) i Microsoft Support.

### <a name="what-is-the-best-way-for-me-to-demonstrate-prod_shortmd-and-microsoft-teams-to-prospective-customers"></a>Hvordan kan jeg bedst demonstrere [!INCLUDE [prod_short.md](includes/prod_short.md)] og Microsoft Teams til mulige kunder?

Hvis du er en forhandlingspartner, kan det være en god idé at have et miljø, som du kan vise som del af salgsdemonstrationer. Hvis du vil undgå at påvirke Microsoft Teams i din organisation, kan du få en Microsoft 365-demokonto på [https://aka.ms/CDX](https://aka.ms/CDX). Denne konto giver dig fuld kontrol over en uafhængig Azure-organisation, der omfatter Microsoft Teams og [!INCLUDE [prod_short.md](includes/prod_short.md)]. Du kan finde flere oplysninger i [Forberede demonstrationsmiljøer i Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment).

### <a name="does-the-prod_shortmd-app-for-teams-cater-for-my-customization-and-personalization"></a>Passer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams til min opsætning og brugertilpasning?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams kan vise kort for links til kundesider og tabeller i [!INCLUDE [prod_short.md](includes/prod_short.md)], f.eks. de sider og tabeller, der stammer fra dine egne brugerdefinerede udvidelser eller fra AppSource.

De felter, der vises på et kort i Teams, kan også være påvirket af de [!INCLUDE [prod_short.md](includes/prod_short.md)]-tilpasninger, der er installeret i organisationen. Kort overvejer ikke rollespecifikke tilpasninger eller brugertilpasninger. I vinduet kortoplysninger vises dog postoplysninger, som du kan se dem i [!INCLUDE [prod_short.md](includes/prod_short.md)], herunder alle udvidelser, rolle tilpasninger og brugertilpasninger.

Når du søger efter kontakter, påvirkes de felter, der er tilknyttet i tabellen **Kontakter**, og de felter, der vises i søgeresultaterne, påvirkes ikke af tilpasninger eller personlige indstillinger.

### <a name="how-do-the-permissions-required-by-the-app-affect-my-privacy"></a>Hvordan påvirker de tilladelser, der kræves af app'en, mine personlige oplysninger?

Før du installerer [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Team, kan du gennemse de tilladelser, der som minimum kræves, for at appen kan fungere. Når du installerer app'en, accepterer du, at appen har tilladelse til at modtage meddelelser og data, som du angiver, og Teams har tilladelse til at gemme og behandle disse meddelelser.

Nogle [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner kræver også åbning af eksterne hyperlinks eller adgang til kameraet eller geografisk placering. Antag f.eks., at du vil tage et billede af en købsfaktura for at blive behandlet. Denne [!INCLUDE [prod_short.md](includes/prod_short.md)]-app bruger ikke disse muligheder uden din tilladelse, og de bruges kun af bestemte funktioner i vinduet **Detaljer**. Når du bruger en af disse funktioner første gang, vises der en dialogboks, hvor du bliver spurgt, om du vil give adgang til de nødvendige enhedsegenskaber.

- På skrivebordet for grupper gennemgås og tilpasses App-tilladelser fra vinduet **Indstillinger**. Vælg et profilbillede øverst i app'en, vælg **indstillinger** > **Tilladelser**, og vælg derefter [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen.

- For Teams i browseren og Teams til iOS eller Android kan du gennemse eller ændre tilladelser fra browseren eller enhedens indstillinger.

> [!NOTE]
> Nøjagtigt, hvilke [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner der beder dig om tilladelser, afhænger af de tilføjelsesprogrammer og tilpasninger [!INCLUDE [prod_short.md](includes/prod_short.md)], som du opretter forbindelse til.

### <a name="where-can-i-learn-about-my-privacy"></a>Hvor kan jeg se mere om mine personlige oplysninger? 

Du kan få mere at vide om, hvordan Microsoft håndterer dine data i [Microsofts erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?linkid=2030602). 

Kontakt administratoren for at få mere at vide om, hvordan virksomheden håndterer beskyttelsen af dine data.

### <a name="how-do-i-uninstall-the-prod_shortmd-app-for-teams"></a>Hvordan afinstallerer jeg [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen i Teams?

Hvis du vil fjerne den app, du har installeret til dig selv, skal du gå til en vilkårlig chatboks, finde ikonet for [!INCLUDE [prod_short.md](includes/prod_short.md)] nedenfor, højreklikke på ikonet og vælge **Fjern**.  

### <a name="will-microsoft-continue-to-improve-the-prod_shortmd-app-for-teams"></a>Fortsætter Microsoft med at forbedre [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen for Teams?

Hos Microsoft lytter vi hele tiden til feedback fra vores forskellige grupper af brugere og handler på de mest interessante forslag. Du kan finde flere oplysninger om kommende nyheder for appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams, i [Dynamics 365-udgivelsesplaner](/dynamics365-release-plan/2021wave1/).

Hvis du vil deltage i forbedringen af appen til Teams eller har en god ide til at forenkle dit arbejde eller dine samarbejdsoplevelser i Teams, kan du tilføje en idé eller tilslutte dig eksisterende ideer på [https://aka.ms/BusinessCentralIdeas](https://aka.ms/BusinessCentralIdeas).

## <a name="searching-for-contacts"></a>[Søgning efter kontakter](#tab/contacts)

### <a name="which-tables-does-the-app-search-in"></a>Hvilke tabeller søger appen i?

Når du søger efter kontakter fra appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams, bliver dine søgeord sammenlignet med poster i tabellen **Kontakter** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. 

### <a name="which-fields-in-the-contacts-table-can-i-search"></a>Hvilke felter i tabellen over kontakter kan jeg søge i?

Når du skriver dine søgeord i søgefeltet, sammenlignes udtrykkene med de fleste felter i tabellen **Kontakter**. Disse felter omfatter f.eks. **Nummer**, **Navn**, **Adresse**, **Telefonnr.** eller **Mobilnr.** og **Mail**. 

Søgeord matches ikke med brugerdefinerede felter, der er føjet til tabellen **Kontaktpersoner** af apps og udvidelser.

### <a name="do-search-results-include-companies-and-persons"></a>Omfatter søgeresultater virksomheder og personer?

Ja. I [!INCLUDE [prod_short.md](includes/prod_short.md)] kan kontakter være af typen **Virksomhed** eller **Person**, hvor en eller flere personer kan være knyttet til en virksomhed. I søgeresultaterne kan virksomheder og personer have forskellige ikoner.

### <a name="do-contacts-of-any-business-relationship-appear-in-the-results"></a>Vises kontakterne for en forretningsrelation i resultaterne?

Ja. Nogle kontakter kan repræsentere debitorer eller kreditorer eller begge dele. Andre kontakter uden defineret forretningsforbindelse repræsenterer typisk potentielle kunder. Kontakter med andre forretningsforbindelser, herunder de brugerdefinerede relationer, du har konfigureret i [!INCLUDE [prod_short.md](includes/prod_short.md)], vises også i søgeresultaterne.

### <a name="can-i-look-up-contact-details-during-meetings"></a>Kan jeg søge efter kontaktoplysninger under møder?

Ja. Du kan søge efter kontaktoplysninger, interaktionshistorik og relaterede dokumenter for debitoren eller kreditoren i løbet af et Teams-møde eller et opkald, mens mødet afholdes, uden at forlade Teams.

Du kan faktisk søge efter kontaktoplysninger fra ethvert sted i Teams ved hjælp af kommandoboksen. Du kan f.eks. søge efter kontaktoplysninger fra kalenderen i Teams, så du lettere kan arrangere møder.

### <a name="how-do-i-view-my-last-interactions-with-a-contact"></a>Hvordan får jeg vist mine sidste interaktioner med en kontakt?

Detaljevinduet for en kontakt viser interaktionslogposter. Interaktionslogposter giver en oversigt over de interaktioner, som organisationen har haft med den specifikke kontakt. Interaktionerne kan omfatte mails, som du har udvekslet, opkald, du har modtaget, eller dokumenter, du har sendt.

For de interaktioner, der skal vises, skal [!INCLUDE [prod_short.md](includes/prod_short.md)] være konfigureret til at spore interaktioner. Du kan lære mere om logføring af interaktioner i [Registrere interaktioner med kontakter](marketing-interactions.md).

### <a name="how-do-i-register-a-teams-call-or-meeting-as-an-interaction"></a>Hvordan kan jeg registrere et Teams-opkald eller -møde som en interaktion?

Find handlingen **Opret interaktion** i detaljevinduet for en kontakt, og vælg mellem indgående og udgående opkald som interaktionsskabeloner. Du kan også oprette dine egne brugerdefinerede interaktionsskabeloner, som er specielt beregnet til brug sammen med Teams-samtaler.

### <a name="can-i-call-a-contact-from-the-prod_shortmd-app-for-teams"></a>Kan jeg ringe til en kontakt fra appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams?

Integrationen af [!INCLUDE [prod_short.md](includes/prod_short.md)] med opkaldsfunktionerne i Teams er begrænsede. Det er ikke muligt at starte et VOIP-opkald direkte fra vinduet for kontaktkort eller kontaktoplysninger. Når du får vist kontaktoplysninger i appen Teams til pc, kan du imidlertid vælge feltet for telefonnummer for at ringe nummeret op, hvis Teams er konfigureret som standardopkaldsapp på din enhed. Hvis du vil ringe til fastnet- eller mobiltelefonnumre ved hjælp af PSTN, det traditionelle telefonsystem, kræver det, at du har appen Microsoft 365 Business Voice. Du kan få mere at vide i [Hvad er Microsoft 365 Business Voice?](/MicrosoftTeams/business-voice/whats-business-voice).

### <a name="how-do-i-view-recent-documents-for-a-customer-or-vendor"></a>Hvordan kan jeg få vist de seneste dokumenter for en debitor eller kreditor?

[!INCLUDE [prod_short.md](includes/prod_short.md)] knytter typisk en kontakt til en debitor- eller kreditorpost, som igen er tilknyttet poster for forretningstransaktioner som f.eks. salgstilbud eller købsfakturaer. Hvis du vil have vist de tilknyttede dokumenter for en kontakt, skal du gå til detaljevinduet for kontakten, vælge værdien i feltet **Forretningsrelation** eller bruge handlingerne til at navigere til den tilknyttede debitor eller kreditor. På siden for debitoren eller kreditoren skal du udvide faktaboksruden for at få vist statistik for forskellige dokumenter, som du kan dykke ned i. Din oplevelse kan variere afhængigt af dine tilpasninger og personlige indstillinger.

### <a name="how-do-i-search-for-contacts-using-special-characters"></a>Hvordan søger jeg efter kontakter ved hjælp af specialtegn?

Du kan indtaste søgekriterier med stort set alle Unicode-tegn. [!INCLUDE [prod_short.md](includes/prod_short.md)] har imidlertid reserveret følgende tegn til andre formål: **=**, **.**, **\**_ og _*@**. Hvis du bruger disse tegn i søgeordene, returneres de forventede resultater muligvis ikke. Hvis du ikke kan se de forventede resultater, skal du sætte apostroffer omkring tegnene i søgeordene, f.eks. **Contoso'= '2**.

### <a name="how-can-i-search-contacts-stored-in-a-different-company"></a>Hvordan kan jeg søge efter kontakter, der findes i et andet regnskab?

Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams kan søge efter debitorer, kreditorer og andre kontakter i ét regnskab ad gangen.  
Hvis du vil søge efter kontakter, der findes i et andet [!INCLUDE [prod_short.md](includes/prod_short.md)]-regnskab, skal du åbne [Indstillinger](across-teams-settings.md)og derefter skifte miljøet og regnskabet derfra.

### <a name="are-prod_shortmd-contacts-different-than-the-ones-in-the-teams-contacts-screen"></a>Er kontakterne i [!INCLUDE [prod_short.md](includes/prod_short.md)] forskellige fra dem i skærmbilledet for kontakter i Teams?

Ja. Kontakter i [!INCLUDE [prod_short.md](includes/prod_short.md)] repræsenterer de forretningskontakter, der er tilgængelige for din organisation. Disse kontakter har en etableret og veldefineret forretningsrelation, eller er kontakter, der repræsenterer potentielle kunder. Disse kontakter er typisk eksterne kontakter. Til sammenligning er kontakterne på kontaktlisten for Teams-opkald dine egne kontakter. Disse kontaktpersoner deles ikke nødvendigvis med andre i din organisation, og de repræsenterer typisk kontakter, der er interne i organisationen.

### <a name="does-prod_shortmd-synchronize-contacts-with-teams"></a>Synkroniserer [!INCLUDE [prod_short.md](includes/prod_short.md)] kontakter med Teams?

Nummer Kontaktpersoner i [!INCLUDE [prod_short.md](includes/prod_short.md)] forbliver adskilte fra kontakter, der er gemt i Teams.
Der er i øjeblikket ingen planer om at synkronisere de to lister.

### <a name="what-is-the-minimum-version-of-prod_shortmd-for-contact-search"></a>Hvad er minimumversionen af [!INCLUDE [prod_short.md](includes/prod_short.md)] med henblik på søgning efter kontakter?

Søgning efter kontakter kræver, at du har installeret appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams version 1.0.4 eller nyere, og at du har oprettet forbindelse til [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljøer i version 18 eller nyere.

### <a name="can-i-search-from-my-mobile-device"></a>Kan jeg søge fra min mobilenhed?

På dette tidspunkt er søgning efter kontakter fra Teams til iOS og Teams til Android ikke tilgængelig.

### <a name="which-permissions-do-i-need-for-contact-search"></a>Hvilke tilladelser skal jeg bruge til søgning efter kontakter?

Hvis du vil søge efter kontakter, skal du have tilladelse på det relevante objektniveau til tabellen **Kontakter** i det [!INCLUDE [prod_short.md](includes/prod_short.md)]-regnskab, du søger i. Hvis du vil have vist detaljevinduet for en kontakt, skal du som minimum have læsetilladelse til siden **Kontakt** i [!INCLUDE [prod_short.md](includes/prod_short.md)]-regnskabet og alle andre relaterede objekter.

### <a name="can-i-use-contact-search-if-im-a-delegated-admin"></a>Kan jeg søge efter kontakter, hvis jeg er en delegeret administrator?

Ja. Du kan også søge efter kontakter og kontaktoplysninger, hvis du har rollen som delegeret administrator i en organisation.

### <a name="is-contact-search-affected-by-api-limits"></a>Er søgning efter kontakter omfattet af API-begrænsninger?

Ja. Søgning efter kontakter fra Teams er baseret på [!INCLUDE [prod_short.md](includes/prod_short.md)] v 2.0-API'er og underlagt eventuelle API-grænser for brugen. Du kan få mere at vide om grænserne for de [Aktuelle API-grænser](/dynamics-nav/api-reference/v2.0/dynamics-current-limits).

### <a name="why-does-it-sometimes-ask-me-to-set-up-the-app"></a>Hvorfor bliver jeg nogle gange bedt mig om at konfigurere appen?

Når du logger på appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams første gang, vil appen forsøge at fastlægge dit foretrukne regnskab i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Hvis appen ikke kan bestemme det foretrukne regnskab, kan det være nødvendigt at gå til **Indstillinger** og vælge det regnskab, du vil søge i. Dette sker f.eks., hvis du har adgang til flere regnskaber på tværs af miljøerne i din organisation. I så fald skal du vælge et regnskab, før du kan begynde at søge.  

Appen beder dig muligvis også om at kontrollere **Indstillinger**, hvis du tilsyneladende ikke har et [!INCLUDE [prod_short.md](includes/prod_short.md)]-abonnement, et [!INCLUDE [prod_short.md](includes/prod_short.md)]-miljø eller en [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens for din konto.

### <a name="id-like-to-search-for-items-or-records-from-other-tables-can-i-do-this-from-teams"></a>Jeg vil søge efter varer eller poster fra andre tabeller. Kan jeg gøre det fra Teams?

Det er ikke muligt at søge i andre tabeller på nuværende tidspunkt. Appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams søger kun i kontaktlisten for [!INCLUDE [prod_short.md](includes/prod_short.md)], som kan omfatte kreditorer, debitorer og andre kontakter.

Hvis du ønsker, at søgefunktionerne kan inkludere andre tabeller, opfordrer vi brugere af vores forum tilføje en idé eller tilslutte sig eksisterende ideer på https://aka.ms/BusinessCentralIdeas.

## <a name="working-with-cards"></a>[Arbejde med kort](#tab/cards)

### <a name="which-types-of-links-does-the-app-support"></a>Hvilke typer links understøtter appen?

[!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams reagerer på de fleste [!INCLUDE [prod_short.md](includes/prod_short.md)]-webklientlinks. Når hyperlinket henviser til en enkelt post på en side, vises der felter for den pågældende post på kortet. De understøttede sidetyper omfatter: 

- Kortsider, f.eks. varekortet
- Dokumentsider, f.eks. salgsordredokumentet
- ListPlus-sider, der repræsenterer en enkelt post, der består af andre poster, f.eks. en bankkontoafstemningskonto
- Simple listesider, hvor en post ikke giver mulighed for at rulle ned på en separat side med oplysninger, f.eks. listen over postnumre

Når du indsætter et hyperlink til URL-adressen til webklienten for rodwebstedet, f.eks. https://businesscentral.dynamics.com, viser kortet i stedet oplysninger, der kan hjælpe nye brugere med at få adgang til [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="how-do-i-delete-a-card-i-sent-to-a-chat"></a>Hvordan sletter jeg et kort, jeg har sendt til en chat?

Du kan ikke slette et kort, som du allerede har sendt til chat. Men du kan slette hele den meddelelse, som kortet er en del af.

Som meddelelsesforfatter kan du slette alle de meddelelser, du har sendt til chat med en person, gruppe eller kanal&mdash;medmindre administratoren har angivet politikker, der forhindrer sletning af meddelelser. Hvis du tilpasser en kanal som kanalejer, kan administratoren også have givet dig tilladelse til at slette alle meddelelser i kanalen, herunder de meddelelser, som andre brugere har sendt.

Hvis du sletter en meddelelse, der indeholder et kort, slettes eller påvirkes data ikke [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="do-cards-always-show-up-to-date-information"></a>Viser kort altid opdaterede oplysninger?

Nummer Feltværdierne på et kort i Teams, herunder alle billeder, er baseret på de data, der er tilgængelige, da kortet blev sendt til chatten. [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort opdateres ikke automatisk i Teams. 

### <a name="will-others-see-my-card-if-they-dont-have-the-prod_shortmd-app-for-teams"></a>Vil andre se mit kort, hvis de ikke har [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til Teams? 

Når du skriver og sender en meddelelse til chatten, som indeholder et kort, vil alle brugere kunne se kortet&mdash;selvom de ikke har installeret appen [!INCLUDE [prod_short.md](includes/prod_short.md)] til Teams.

### <a name="how-do-i-find-out-which-company-a-card-in-teams-belongs-to"></a>Hvordan finder jeg ud af, hvilket firma et kort i Teams tilhører?

Hvis du arbejder på tværs af [!INCLUDE [prod_short.md](includes/prod_short.md)]-firmaer, skal du kontakte administratoren for at få aktiveret et virksomhedskort for hvert regnskab. Når dette tip er aktiveret, vises dette iøjnefaldende i alle oplysnings vinduer i Teams, og det firma og miljø, som posten tilhører, vises. Hvis du vil lære, hvordan du konfigurerer virksomhedskort, skal du se [Sådan får du vist et firmalogo, så du hurtigt kan få adgang til firmaoplysninger](ui-change-basic-settings.md#badge).

## <a name="working-with-card-details"></a>[Arbejde med kortdetaljer](#tab/carddetails)

### <a name="where-is-the-save-button-in-the-details-window-in-teams"></a>Hvor er knappen til gem i vinduet detaljer i Teams?

[!INCLUDE [prod_short.md](includes/prod_short.md)] gemmer automatisk de ændringer, du foretager i et felt, så snart du forlader feltet. Hvis du vil bevare et felt, skal du klikke eller trykke et vilkårligt sted uden for feltet eller bruge tabulatortasten til at flytte til næste felt. Når der vises data i en dialogboks i detaljevinduet, skal du muligvis klikke på knappen **OK** for at [!INCLUDE [prod_short.md](includes/prod_short.md)] gemme ændringerne.

### <a name="if-i-choose-to-view-details-for-a-card-will-other-users-see-my-details-window"></a>Hvis jeg vælger at få vist detaljer om et kort, får andre brugere vist vinduet mine oplysninger?

Nummer Mens alle i chatten eller mødet kan se selve kortet, vises vinduet med oplysninger kun for dig på din enhed, når du vælger **Detaljer**. Andre brugere skal vælge **Detaljer**, hvis de vil have vist detaljevinduet på deres enhed.

### <a name="can-i-start-a-teams-call-from-the-details-window-in-teams"></a>Kan jeg starte et Teams-opkald fra vinduet detaljer i Teams?

Ja. Hvis du bruger appen Teams til pc, skal du starte et opkald ved at vælge det tilknyttede nummer i feltet for telefonnummer, f.eks. **Mobilnr.** felt på kortet **Konktakt**. Teams skal være din angivne opkalds-app.

Hvis du vil ringe til lokale eller internationale fastnetnumre og mobiltelefoner, kræver Teams, at du har en Business Voice-licens til virksomhedsopkald. Du skal også konfigurere Teams som opkaldsløsning. Du kan finde flere oplysninger i [Planlægning af stemmeløsning i Teams](/microsoftteams/cloud-voice-landing-page) i dokumentationen til Teams.

### <a name="can-i-print-documents-from-the-details-window-in-teams"></a>Kan jeg udskrive dokumenter fra vinduet med detaljer i Teams?

Ja. Du udskriver rapporter og andre dokumenter med standardudskrivningsfunktioner for [!INCLUDE [prod_short.md](includes/prod_short.md)] og enhver skybaseret printer, der er konfigureret på siden **Printerstyring** i [!INCLUDE [prod_short.md](includes/prod_short.md)]. Du kan ikke udskrive fra Teams til lokale printere, der kender din klientenhed, f.eks. printere, som du typisk udskriver fra browseren. Du kan derfor ikke udskrive fra vinduet Vis rapport, men kun fra hovedrapportens anmodningsside, direkte til dine Cloud-printere.

Du kan finde flere oplysninger om oprettelse af Cloud-printere i [Konfiguration af printere](ui-specify-printer-selection-reports.md).

### <a name="can-i-access-the-camera-from-the-details-window-in-teams"></a>Kan jeg få adgang til kameraet fra detalje vinduet i Teams?

Ja. Alle [!INCLUDE [prod_short.md](includes/prod_short.md)]-funktioner i vinduet detaljer, som bruger kameraet, er tilgængelige på alle Teams-klienter.

### <a name="can-i-access-my-location-from-the-details-window-in-teams"></a><a name="location"></a>Kan jeg få adgang til min lokation fra detaljevinduet i Teams?

Hvis du bruger funktioner i [!INCLUDE [prod_short.md](includes/prod_short.md)], der får adgang til dine aktuelle placeringskoordinater, f.eks. med Maps, skal du bruge Teams i browseren eller Teams mobil-app. Placeringen er ikke tilgængelig, når appen Teams desktop bruges. 

## <a name="collaborating-with-guests"></a>[Samarbejde med gæster](#tab/collaborating)

### <a name="can-i-share-cards-with-users-outside-my-organization"></a>Kan jeg dele kort med brugere uden for organisationen?

Ja. Når du skriver og sender en meddelelse, der indeholder et kort, vil alle modtagere i chatten kunne se kortet&mdash;selvom de er gæster eller eksterne i forhold til organisationen. Gæster kan også åbne vinduet detaljer, hvis de har tilladelse til at få adgang til de pågældende data i [!INCLUDE [prod_short.md](includes/prod_short.md)].

### <a name="is-the-experience-any-different-for-users-that-are-guests"></a>Er der en anden oplevelse hos brugere, som er gæster?

Ja. Hvis du inviterer gæstebrugere fra uden for organisationen til at deltage i chat eller en kanal, får de tilsvarende, men ikke identiske, sammenlignet med brugere inden for organisationen. Når en gæst modtager en meddelelse, der indeholder et kort, kan de se det. Gæster kan også åbne vinduet detaljer, hvis de har tilladelse til at få adgang til de pågældende data i [!INCLUDE [prod_short.md](includes/prod_short.md)] og har fået tildelt en [!INCLUDE [prod_short.md](includes/prod_short.md)]-licens inden for organisationen. Når en gæst skriver en meddelelse, vil links til gæstens eller din [!INCLUDE [prod_short.md](includes/prod_short.md)] ikke blive udvidet til kort.

Hvis du vil have oplysninger om andre lighedspunkter og forskelle mellem gæster og teammedlemmer, skal du se [Gæsteerfaringer i Teams](/MicrosoftTeams/guest-experience) i dokumentationen til Teams.

### <a name="how-does-a-guest-user-install-the-prod_shortmd-app"></a>Hvordan installeres en gæstebruger [!INCLUDE [prod_short.md](includes/prod_short.md)]? 

Gæster har ikke adgang til app-markedspladsen for at installere apps selv. Appen kan imidlertid installeres automatisk på basis af virksomhedens politikker. En anden måde, en gæstebruger kan installere [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen på er, når de modtager en chatmeddelelse, der indeholder et [!INCLUDE [prod_short.md](includes/prod_short.md)]-kort. I dette tilfælde vælger brugeren knappen **Detaljer** eller menuen på kortet og installerer derefter [!INCLUDE [prod_short.md](includes/prod_short.md)]-appen til brug sammen med organisationen. Når appen er installeret, modtager brugeren ikke automatisk tilladelse til at få adgang til data fra din [!INCLUDE [prod_short.md](includes/prod_short.md)].

---

## <a name="see-also"></a>Se også

[[!INCLUDE [prod_short](includes/prod_short.md)] og Microsoft Teams Oversigt over integration](across-teams-overview.md)  
[Installere appen [!INCLUDE [prod_short](includes/prod_short.md)] til Microsoft Teams](across-install-app-for-teams.md)  
[Søgning efter debitorer, kreditorer og andre kontakter fra Microsoft Teams](across-search-contacts-teams.md)  
[Dele poster i Microsoft Teams](across-working-with-teams.md)  
[Fejlfinding i Teams](admin-teams-troubleshooting.md)  
[Ændring af virksomhed og andre indstillinger i Teams](across-teams-settings.md)  
[Udvikling af Teams-integration](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]