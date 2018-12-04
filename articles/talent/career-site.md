---
title: "Karjäärisaidi funktsionaalsus Attractis"
description: "Selles artiklis antakse ülevaade kandidaatide leidmise karjäärisaidi funktsionaalsusest rakenduses Microsoft Dynamics 365 for Talent - Attract. See selgitab ka seda, kuidas seda funktsionaalsust seadistada."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: et-ee
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a>Karjäärisaidi funktsionaalsus Attractis

[!include [banner](includes/banner.md)]

Selles artiklis antakse ülevaade kandidaatide leidmise karjäärisaidi funktsionaalsusest rakenduses Microsoft Dynamics 365 for Talent: Attract. See selgitab ka seda, kuidas seda funktsionaalsust seadistada.

## <a name="overview"></a>Ülevaade

Attract annab rentniku igale keskkonnale ühe karjäärisaidi. Näiteks kui organisatsioonil on arenduskeskkond ja katsekeskkond, eraldatakse üks karjäärisait arenduskeskkonnale ja teine karjäärisait eraldatakse katsekeskkonnale. Iga karjäärisait on **täiesti isoleeritud** ja omab eraldi autentimise mehhanismi. Töid ja kandidaatide profiile karjäärisaitide vahel ei jagata.

Vaikimisi on karjäärisait avalik. Seega saavad kandidaadid näha kõiki väliseks märgitud töid ilma sisse logimata. Siiski, kõik muud toimingud nõuavad kandidaadilt sisselogimist.

## <a name="career-site-management"></a>Karjäärisaidi haldus

Järgmisi karjäärisaidi elemente juhitakse sätete abil.

- **Organisatsiooni nimi:** organisatsiooni nimi kuvatakse karjäärisaidi ülaosas navigeerimisribal. Valides organisatsiooni nime, lähevad kandidaadid lehele, kus on loetletud kõik avatud tööd.
- **Organisatsiooni logo:** karjäärisaidi ülemises vasakus servas kuvatakse organisatsiooni logo kujutist. Valides logo kujutise, lähevad kandidaadid lehele, kus on loetletud kõik avatud tööd.

Organisatsiooni nime ja logo väärtuste seadistamiseks logige administraatorina Attracti sisse, valige menüü **Sätted** (hammasratta sümbol) alt **Halduskeskus** ja seejärel valige vahekaart **Ettevõtte andmed**.

> [!NOTE]
> Karjäärisaidil näidatava logo kujutise fikseeritud kõrgus on 20 pikslit (px). Halduskeskusest lisatud pildi suurus muudetakse sobivaks. Seetõttu võib laius sõltuvalt pildist muutuda.

## <a name="career-site-url"></a>Karjäärisaidi URL

Kui te esmakordselt [sisestate välise töö](./Creating-jobs-Attract.md#postings), võite **Rakenda** lingi Attracti rakendusest kopeerida. Selle lingi URL on järgmises vormingus: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`

Karjäärisaidi URL on URL-i **Rakenda** alamstring. See sisaldab kõike, kuni ettevõtte nimeni. Seepärast on eelnevale **Rakenda** URL-ile karjäärisaidi URL `https://jobs.talent.dynamics.com/jobs/<company_name>/`.

## <a name="authentication-options"></a>Autentimise valikud

Kandidaatidel on Attracti karjäärisaidile sisselogimiseks järgmised võimalused.

- Isiklik konto:

    - LinkedIn
    - Microsoft – WHS
    - Google
    - Facebook

- Töö- või koolikonto:

    - Windows Azure Active Directory (Azure AD)

Azure AD sisselogimine on mõeldud ainult sisemistele kandidaatidele. Seetõttu toimib see ainult sisemistele kandidaatidele, kes kasutavad oma ettevõtte Azure AD mandaate. Näiteks kandidaat, kes on hetkel Contoso Ltd töötaja, soovib kandideerida kõrvalise ettevõtte, Alpine Ski House, tööle. Sellisel juhul sisselogimine ebaõnnestub, kui töötaja proovige kasutada oma Contoso Ltd. Azure AD mandaate.

## <a name="create-and-maintain-a-profile"></a>Profiili loomine ja haldamine

Pärast kandidaatide karjäärisaidile sisselogimist saavad nad lehe ülaosast navigeerimisribalt valida **Minu profiil**, et omale profiil luua ja seda hallata. Profiil sisaldab isikuandmeid, töökogemuse andmeid, hariduse üksikasju, dokumente, linke ja andmeid oskuste kohta. Pärast profiili loomist saab seda kasutada kandidaadile huvi pakkuvatele töödele kandideerimiseks. Profiilid aitavad ka Attractil kandidaatidele õigeid töid soovitada.

## <a name="find-the-right-job"></a>Õige töö leidmine

Tööde loendi lehel saavad kandidaadid konkreetset tööd otsida sisestades otsingusõnu. Otsingu funktsionaalsus otsib otsingusõnu töö pealkirjadest ja töö kirjeldustest ning näitab tulemusena vastavaid töid. Kandidaadid saavad tulemusi igal ajal vastavalt töö asukohale või töö funktsioonile filtreerida.

Kandidaadid saavad karjäärisaidil vaadata ka soovitatud töid. Kandidaatidele soovitatud tööd põhinevad kandidaadi varasematel kandideerimistel, profiilil ja elulookirjeldusel.

> [!NOTE]
> Töö soovitused kuvatakse ainult siis, kui karjäärisaidile on postitatud vähemalt 10 tööd ja kui kandidaat on täitnud oma profiili.

## <a name="apply-for-jobs"></a>Töökohtadele kandideerimine

Kui kandidaadid leiavad õige töö, saavad nad kandideerida, kasutades töö üksikasjade lehel olevat nuppu **Esita avaldus**. Sellel hetkel saavad kandidaadid luua kas täiesti uue profiili või vaadata üle oma olemasoleva profiili andmed. Kui see on nõutud, saavad kandidaadid üles laadida oma elulookirjelduse ja seejärel tööavalduse esitada.

## <a name="check-application-status"></a>Avalduse oleku kontrollimine

Kui kandidaadid kandideerivad ühele või enamale tööle, saavad nad oma avatud ja suletud kandideerimiste vaatamiseks valida lehe ülaservas olevalt navigeerimisribalt **Avaldused**. Kui kandidaadid ühe oma avaldustest avavad, näevad nad hetkeseisu ja mistahes ootel olevat tegevust, mille nad peavad teostama. Näiteks, kui kandidaat peab välja pakkuma võimalikud kuupäevad silmast silma vestluseks, kuvatakse lehel tema valikuid.

## <a name="internal-jobs"></a>Sisemised tööd

Hetkel ei kuvata sisemiseks märgitud ja Attracti karjäärisaidile sisestatud töid karjäärisaidil. Need on juurdepääsetavad ainult läbi otsese URL-i **Esita avaldus**, mille saab kopeerida Attracti rakendusest.

