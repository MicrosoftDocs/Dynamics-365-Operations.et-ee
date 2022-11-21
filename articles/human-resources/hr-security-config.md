---
title: Virtuaaltabelipõhiste integratsioonide turbekonfiguratsiooni mõisted
description: See artikkel selgitab ülesehitust Integratsiooni loomiseks Microsofti ja Dynamics 365 Human Resources muude süsteemide vahel.
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759726"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>Virtuaaltabelipõhiste integratsioonide turbekonfiguratsiooni mõisted

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab ülesehitust virtuaalsete [Microsoft Dataverse tabelite (üksuste)](/dev-itpro/power-platform/virtual-entities-overview) kasutamise jaoks, et luua integratsiooni Dynamics 365 Human Resources kolmanda osapoole süsteemi vahel. Artikli fookus on turvalisuse konfiguratsioonil ja autentimise ja autoriseerimise aspektidel, mis on vajalikud süsteemipiiri vahel, et luua funktsionaalne, turvaline süsteem.

## <a name="prerequisite-reference-articles"></a>Eeltingimuse viiteartiklid

Järgmistes artiklites antakse lisateavet selle artikli mõistete kohta.

- [Virtuaalsete üksuste ülevaade](/dev-itpro/power-platform/virtual-entities-overview)
- [Virtuaaltabelitega (üksustega) alustamine](/developer/data-platform/virtual-entities/get-started-ve)
- [Mitme rentniku serverilt serverile autentimise kasutamine (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Kasuta OAuthi autentimist (Microsoft Dataverse Dataverse)](/developer/data-platform/authenticate-oauth)
- [OAuth 2.0 kliendi mandaadid voogu Microsofti identiteedi platvormil](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [Autentimine ja autoriseerimine](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>Arhitektuur 

Järgmine alistika diagramm näitab põhimõisteid, mis on kaasatud virtuaaltabeleid (üksusi) kasutavatesse integratsiooniprojektidesse.

![Virtuaalne tabelipõhine integreerimine.](./media/Hosts.jpg)

Siin on mõne eelneva diagrammi elementide selgitus:

- **Microsoft** – Microsoft hostib ja käitab erinevaid Dynamics 365 tooteid klientide nimel.

    - **Azure Active Directory(Azure AD) Rentnik C** – Azure AD Microsofti omane rentnik. Rentnik, kus Dynamics 365 avaldused registreeritakse.

- **Partneri integreerimine**

    - **Süsteemi integreerimine** – Süsteem, mis integreeritakse Dynamics 365-ga. See võib olla palgasüsteem või mis tahes süsteem, mis põhineb Dynamics 365-is salvestatud andmetel.
    - **Adapter** – tarkvara või teenus, mis vastutab suhtlemise eest nii Dynamics 365-ga kui ka integreerimissüsteemiga.

        > [!NOTE]
        > Kui adapter on mõeldud kasutamiseks mitmel Dynamics 365 kliendil, siis eeldatakse, et see registreeritakse mitmekordse rakendusena Azure AD rakenduses.

    - **Azure AD rentnik A** – Azure AD rentnik, mis kuulub integreeriva partneri omaks. Rentnik, kus adapteri rakenduse ID on registreeritud.

- **Vastastikused** kliendid – klient, kes Dynamics 365 Human Resources rakendab ja integreerib partneri lahendust.

    - **Dynamics 365 Finantsid ja Inimressursid** – Kliendispetsiifiline Dynamics 365 Finantsid või Inimressursid eksemplar, mis sisaldab kliendiandmeid, mida integreerimissüsteem nõuab.
    - **Dataverse**– kliendipõhine keskkond Dataverse, mis on ühendatud kas finantside või inimressurssidega. Dataverse Rakendus <a0/& pakub Veebi API-d Dynamics 365 andmetega suhtlemiseks.
    - **Azure AD rentnik B** – kliendi rentnik Azure AD. See toimib identiteedipakkujana (autoriseerimisserver) ja väljastab lubasid, mis autoriseerivad kutsujaid kliendi eksemplari kutsumiseks Dataverse.

## <a name="basic-request-flow"></a>Põhiline nõudevoog

See jaotis kirjeldab tüüpiliste integratsiooni kaasatud nõude põhivoogu. See viitab selles artiklis varasemale aarhitektatuuri diagrammile.

Tüüpiline taotlus nõuab adapterilt Dynamics 365-lt andmete saatmist ning seejärel nende andmete salvestamist ja sünkroonimist integreerimissüsteemi.

1. Adapter palub veebi Dataverse API-l teha päringuid vastavate andmete kohta.

    > [!NOTE]
    > Autentimine on eeltingimus ning loa soetamine on protsessi oluline osa. Autentimist kirjeldatakse jaotises Autentimine [ja autoriseerimine süsteemipiiril](#authentication-and-authorization-at-system-boundaries).

    See kutse tehakse veebi API-le Dataverse päringuks rakenduse andmete kohta, mida esitatakse virtuaalse tabeli kaudu. (Vt "2. Esialgne sünkroonimine" ja "3. Deltasünkroonimine diagrammis.)

2. Dataverse rakendus <a0/& tegeleb taotlusega, päringutes virtuaalse tabeli virtuaalüksuse kaudu diagrammis ("Virtuaaltabeli puhver"). Taotlus Dataverse edastatakse finantside või inimressursside virtuaalüksuse teenusesse, et esitada päring andmete kohta, mis on füüsiliselt salvestatud Finantside või Inimressursside andmebaasi.
3. Finantside või inimressursside virtuaalüksuse teenus tõlgib virtuaalüksuse taotluse päringusse finantside või inimressursside üksuse kohta, mis varundab virtuaalse Dataverse üksuse. Andmed tuuakse andmebaasist, teisendatakse tagasi üksuse esitusse Dataverse ja tagastatakse kutsujale.
4. Adapter lõpetab kõik vajalikud vastendamised ja andmete tõlkimise ning helistab integreerimissüsteemi nii, et andmed püsiks integreerimissüsteemi andmebaasis. (Vt "4. Salvesta andmed"diagrammi.)

## <a name="authentication-and-authorization-at-system-boundaries"></a>Autentimine ja autoriseerimine süsteemipiiril

*Autentimine* kinnitab, et kasutaja või rakenduse identiteet on kindlaks tehtud, ja kinnitab, et kasutaja või rakendus on nende identimiseks. *Autoriseerimine* annab kasutajale või rakendusele juurdepääsuõiguse konkreetsetele rakendusetaseme õigustele. Lisateavet vt autentimise vs [. autoriseerimise kohta](/azure/active-directory/develop/authentication-vs-authorization).

Enamik ristsüsteemi kutseid aritmtuuri diagrammis, mis on selle artikli varasemas versioonis, hõlmavad adapterit. Adapter peab end autentima, et teha järgmised kõned:

- Kutse: Dataverse
- Integratsioonisüsteemi kutsumine

Vaadake diagrammis süsteemi piire. Kõik süsteemide vahelised veebitaotlused tuleb autentida ja rakendustaseme autoriseerimise kontrollid tuleb enne kutsujale andmete tagastamist läbida. Päringu jaoks Dynamics 365 virtuaaltabeli suhtes, mida varundavad finantsid või inimressursid, jõustatakse autentimise ja autoriseerimise kontrollid järgmistes süsteemipiirides:

- Adapteri ja veebi API Dataverse (OData) lõpp-punkti vaheline kõne
- Virtuaalüksuse Dataverse ja finantside või inimressursside virtuaalüksuse teenuse vaheline kõne

Mõlemal juhul tehakse autentimise kontrollid esimesena. Seejärel kontrollitakse rakendusetasandi autoriseerimist, et tagada autenditud kasutaja või rakenduse õiged rakendusetaseme privileegid taotletud andmete toomiseks.

Autentimist kõneks Dataverse käsitletakse läbi kandja loa, mis tuleb veebitaotluses kaasata HTTP-päisena Dataverse. Adapter peab saama rentniku B eksemplari loa Azure AD. (Vt "1. Hangi luba"diagrammis.) Azure AD toimib autentimisvoos identiteedipakkujana.

Adapter autendib, pakkudes rakenduse identiteeti (mittesaladust, Azure AD nagu on registreeritud rentnikus A) ja rakenduse saladust või serti, mis on ainult adapteri rakendusel.

Kui kasutaja või rakendus on saanud kutseid Dataverse teha, Dataverse kontrollitakse kasutajat või rakendust iga taotluse suhtes. Need kontrollid veenduge, et kutsujal (adapteri rakenduse identiteedil, mis on diagrammis määratletud "\<guid A\>" on vastavad) rakenduseõigused. Rakendustaseme autoriseerimist hallatakse Dataverse läbi rakenduse kasutaja, mis tähistab adapteri rakenduse ID-d. Rakendusetaseme õigusi hallatakse, andes juurdepääsu kindlatele määratletud Dataverse rakenduse rollidele. Need rollid pakuvad rakendusele granulaarsed privileegid.

Üksikasjalikumaid juhiseid vt mitme rentniku [serverist serverisse autentimise kasutamine](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication).

Kui Dataverse rakenduse õiguste kontrollid on läbitud, helistab virtuaalüksuse üksus virtuaalüksuse teenuse lõpp-punkti finantside või inimressursside keskkonnas. Selle kõne miseks kasutatakse serverilt serverile (S2S) autentimist. See kasutab finantside ja toimingute virtuaalandmeallika konfiguratsioonikirjes konfigureeritud identiteeti ja saladust.

![Finantside ja toimingute virtuaalandmeallika konfiguratsioonikirje sisendkausta keskkonnas.](./media/sandbox.jpg)

Lisateavet vt virtuaalüksuste [Dataverse konfigureerimine](/dev-itpro/power-platform/admin-reference).

Virtuaalüksuse Dataverse call to Finance’ile või Inimressurssidele hõlmab adapteri Dataverse algse adapteri kutse identiteeti (identiteeti, mis on arhitektuuri diagrammis tähistatud nimega "\<guid A\>). Kui virtuaalüksuse andmeallikas on õigesti konfigureeritud ja S2S-i autentimise kontrollid on läbitud, käivitab finantside või inimressursside virtuaalüksuse teenus päringu algse kutsuja kontekstis (adapter, \<guid A\>). Rakenduse õiguste kontrollid (autoriseerimine) finantside või inimressursside tasemel tehakse selleks, et tagada adapteri privileegid, mis on vajalikud päringu kaudu taotletud andmeüksustele juurdepääsemiseks.

Finantside ja inimressursside turvalisust hallatakse järgmistel viisidel:

1. Vastendades adapteri identiteedi (\<guid A\>) kindla finantside või inimressursside kasutajaga. Vastendamine toimub Azure **active Directory rakenduste lehel**. Lisateavet vt teemast Välise rakenduse [registreerimine](/dev-itpro/data-entities/services-home-page.md#register-your-external-application).
2. Andes finantside või inimressursside kasutajale sobivad rakenduse tasandi rollid, kohustused ja privileegid. Lisateavet vt Rollipõhisest [turvalisusest](/dev-itpro/sysadmin/role-based-security).

Kui adapteri rakendusele (\<guid A\>) antakse soovitud andmetele juurdepääsuks vajalikud privileegid, ilmnevad järgmised sündmused:

1. Päring on käivitunud.
2. Andmed tõlgitakse tagasi selle üksuse Dataverse lehele.
3. Andmed tagastatakse adapterile.

> [!IMPORTANT]
> Arenduse ajal saab adapterit käitada, kasutades finantside või inimressursside kasutajat, kes on administraatori rolliga. Tootmiskeskkonnas ei tohi adapterit siiski kunagi administraatori privileegidega käitada.

## <a name="key-takeaways"></a>Võtmete võtta

Siin on mõned virtuaalse tabeli või olemi ülesehituse olulised tulemid:

- Inimressursside abil varundatud virtuaaltabelite turvakonfiguratsiooni hallatakse Inimressurssides.
- Klient (käesolevas artiklis varasema aritmtuuridiagrammi "Vastastikusel kliendil") on täielik kontroll selle üle, millised privileegid on antud integreeriva adapteri identiteedile (diagrammis "\<guid A\>").
- Klient vastutab õige turvakonfiguratsiooni eest oma Inimressursside keskkonnas. Adapterit loov integreeriv partner peab andma juhiseid adapteri nõutavate privileegide kohta.
