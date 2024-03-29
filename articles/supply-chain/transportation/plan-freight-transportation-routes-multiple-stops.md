---
title: Mitme peatusega veose transpordimarsruutide plaanimine
description: Selles artiklis kirjeldatakse mitmesuguseid elemente, mida kasutatakse transpordiprotsesside plaanimisel Dynamics 365 Supply Chain Managementis.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate, TMSRouteSchedule, TMSRouteRateDetail
audience: Application User
ms.reviewer: kamaybac
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3d316b5bed67e84fdd5cec8b518069c053436d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671587"
---
# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Mitme peatusega veose transpordimarsruutide plaanimine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse mitmesuguseid elemente, mida kasutatakse transpordiprotsesside plaanimisel Dynamics 365 Supply Chain Managementis.

Keerukate transpordimarsruutide puhul, mis sisaldavad mitut peatust, saate kasutada marsruudiplaane ja marsruudi juhendeid. Kui sama marsruuti kasutatakse regulaarselt, saate seadistada plaanitud marsruudi.

## <a name="route-plans"></a>Protsessi plaanid
Marsruudiplaan sisaldab marsruudisegmente, mis annavad teavet peatuste kohta, mida marsruudil külastatakse, ja vedajate kohta, keda iga segmendi puhul kasutatakse. Marsruudi peatused tuleb määratleda keskustena. Keskus võib olla hankija, ladu, klient või lihtsalt ümberlaadimiskoht, kus vedajat vahetate. Iga segmendi puhul saate määratleda mitmesuguste tasude jaoks hinnad. Järgmisena on toodud mõned näited.

-   Tasud antud segmentidesse sõidu eest
-   Kauba pealevõtmise tasud
-   Kaupade kohaletoimetamise tasud

Iga marsruudiplaan peab olema seotud marsruudi juhendiga.

## <a name="route-guides"></a>Protsessi juhendid
Marsruudi juhend määratleb kriteeriumid koorma vastendamiseks konkreetse marsruudiplaaniga. Näiteks saab määratleda lähte- ja sihtkoha keskuse, konteineri mahu või kaalu piirangud ja vedaja, teenuse või grupi. Marsruudi juhendid on saadaval lehel **Marsruudi määra töölaud**, kus koormad saab vastendada marsruutidega kas käsitsi või automaatselt. Kui marsruudi juhend on plaanitud marsruudi kohta, on see saadaval ka lehel **Koorma koostamise töölaud**.

## <a name="scheduled-routes"></a>Plaanitud protsessid
Plaanitud marsruut on eelmääratud marsruudiplaan, millel on tarnekuupäevade graafik. Plaanitud marsruudid ja plaanimata marsruudid erinevad selle poolest, kuidas neile koormad määratakse. Kui määrate plaanimata marsruudi, kasutades marsruudi määra töölauda, kinnitatakse ainult koorem ja marsruudi juhend. Kui määrate plaanitud marsruudi, arvestatakse ka tellimuste ja keskuste kuupäevi ja aadresse ning marsruudiplaanil olevat kuupäeva. Marsruudi määra töölaua lehte pole vaja kasutada plaanitud marsruudile käsitsi koormate määramiseks. Selle asemel võite kasutada koorma koostamise töölauda, et soovitada koormate koostamist antud plaanitud marsruudi müügitellimuste kliendiaadresside ja tarnekuupäevade põhjal. Plaanitud marsruutide puhul on marsruudiplaanil fikseeritud lähte- ja sihtkeskused. Tavaliselt on vedaja ja teenus kõigi segmentide puhul sama, kuid need võivad erineda. Sihtkeskused luuakse marsruudil külastatavate klientide sihtnumbrite järgi. Ühe marsruudiplaani kohta võib määratleda mitu marsruudiplaani. Marsruudiplaan peab olema seotud marsruudi juhendiga. Kuid plaanitud marsruutide puhul saab plaani seostada ainult ühe marsruudi juhendiga. Marsruudi ajakava kasutatakse ainult tegelike marsruutide loomiseks lehel **Marsruudi ajakava**. Koorma koostamise töölaua koormate soovitamisel võite kasutada koorma vaikemalli.

## <a name="load-building-workbench"></a>Koorma koostamise töölaud
Koorma koostamise töölaud kasutab koorma soovitamiseks müügitellimuste ja plaanitud marsruutide kliendiaadresse ja tarnekuupäevi. Vaikimisi sisestatakse marsruudi väärtused töölauale. Kuid võite valida alguskuupäeva, mis on marsruudi alguskuupäevast varasem. Koorma soovitamisel kontrollitakse kõigi avatud müügitellimuste tarneaadressi ja tarnekuupäeva. Kui tarneaadressi sihtnumber vastab marsruudiplaani keskuse sihtnumbrile ja kui tarnekuupäev on kriteeriumides valitud vahemikus, soovitatakse koormale müügitellimust. Arvestatakse ka koormamalli mahtu. Korraga pakutakse ainult ühte koormat. Kui teil on müügitellimus, mida ei arvestata, võib olla vaja kasutada teist koormamalli (nt suurema veoki või konteineri koormamalli) või plaanida täiendav tarne.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]