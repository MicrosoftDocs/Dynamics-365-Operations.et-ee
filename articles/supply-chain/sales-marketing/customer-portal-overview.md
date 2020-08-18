---
title: Kliendiportaal Dynamics 365 Supply Chain Managementi ülevaate jaoks
description: Selles teemas tutvustatakse kliendiportaali ja selgitatakse, kes peaks seda kasutama ning kuidas see töötab.
author: dasani-madipalli
manager: tfehr
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 709ba18be9e2edd5d0a7f143aaed5ef94f365b91
ms.sourcegitcommit: 9a2e9f7dfec47c42178bb67a3e099e610515baf3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456922"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a>Kliendiportaal Dynamics 365 Supply Chain Managementi ülevaate jaoks

## <a name="what-is-the-customer-portal"></a>Mis on kliendiportaal?

Tänapäevased tarneahelasüsteemid sõltuvad integratsioonist. Neil on vaja, et varud, kliendinõudlus ja müügiosakond oleksid integreeritud, mitte ei asetseks eri kohtades. Kliendiportaal aitab organisatsioonidel, mis kasutavad Microsoft Dynamics 365 Supply Chain Managementi, seda integratsiooni täiustada ja tõhusamalt oma kliente kursis hoida.

Kliendiportaal on [Power Appsi portaalide](https://docs.microsoft.com/powerapps/maker/portals/overview) mall, mis laseb ettevõtetel luua väljapoole suunatud ettevõtetele mõeldud (B2B) veebisaidi olukordade puhuks, mis on seotud müügitellimuse töötlemisega. Mall kasutab [topeltkirjutust](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Managementi ja Power Appsi portaale, et võimaldada välistel ettevõtetest klientidel vaadata ja luua andmeid ettevõtte Dynamics 365 keskkonnas.

Kliendiportaali mallil on kõik kohandusvõimalused, mida pakub Power Appsi portaalide funktsioon. Malli saab lihtsasti muuta, et see esindaks ettevõtte brändi, lisada saab täiendavaid funktsioone ja muuta kasutajakogemust. Kõiki malli pakutavaid valmiskujul funktsioone saab muuda vastavalt soovile.

> [!IMPORTANT]
> Ei eeldata, et mall on iseseisvalt täiesti töökorras. See kujutab endast vaid tööriista, mis on mõeldud klientidele, kes soovivad luua väljapoole suunatud veebisaidi, et kliendid saaksid töötada teenusest Supply Chain Management hangitud andmetega.

> [!NOTE]
> Kliendiportaali dokumentatsioon on suunatud administraatoritele, kohandajatele ja süsteemiintegraatoritele, kes seadistavad kliendiportaali Supply Chain Managementi paigaldamiseks. Supply Chain Managementi käitava organisatsiooni lõpp-portaali kasutavate klientide kirjeldamiseks kasutatakse termineid _klient_ ja _kasutaja_.

## <a name="video"></a>Video

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

Video [Kliendiportaali malli ülevaade Dynamics 365 Supply Chain Managementis](https://youtu.be/nPrqoLuHfV8) (ülaltoodud) on leitav [Finance and Operationsi esitusloendist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadaval YouTube'is.

## <a name="who-should-use-it"></a>Kes peaks seda kasutama?

Kliendiportaal on loodud ettevõtetele, kes kasutavad Supply Chain Managementi teenust ja kellel on järgmised omadused.

- Nad soovivad ehitada väljapoole suunatud veebisaidi, mis annab tellimuse töötlemisega seotud teavet (näiteks tellimuse olek või konto teave) Supply Chain Managementi süsteemist edasi otse ettevõtte klientidele.
- Nad on üle minemas teenuselt Dynamics AX 2012 teenusele Supply Chain Management ning kasutasid varem [AX 2012 kliendi iseteeninduse portaali](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).

Järgmist tüüpi organisatsioonid **ei** ole head kandidaadid kliendiportaali kasutamiseks.

- Ettevõtted, kes soovivad ehitada veebisaidi klientidele, kes ei ole ettevõttest kliendid. Sellised ettevõtted peaksid mõtlema [Dynamics 365 Commerce'i e-kaubanduse veebisaidi](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site) loomisele.
- Ettevõtted, kes juba kasutavad Power Appsi portaalide veebisaiti sarnasel otstarbel. Need ettevõtted ei saa kliendiportaalist täiendavat kasu. Kliendiportaal esitatakse mallina, mis toimib juhendina ja lähtepunktina klientidele, kes soovivad ühendada omavahel topeltkirjutuse, Supply Chain Managementi ja Power Appsi portaalid. Kui olete juba sellist otstarvet täitva veebisaidi seadistanud, siis ei pruugi kliendiportaali malli kasutamisest selle veebisaidi ümberkavandamiseks erilist kasu olla.

## <a name="how-does-it-work"></a>Kuidas see käib?

Kliendiportaali pakutakse Power Appsi portaalide mallina. See sõltub Power Appsi portaalidest ja topeltkirjutusest.

[Power Appsi portaalid](https://docs.microsoft.com/powerapps/maker/portals/overview) kujutavad endast funktsiooni, mis võimaldab kasutajatel luua väljapoole suunatud veebisaidi, millesse saavad sisse logida organisatsioonivälised inimesed. Portaalide tegemiseks pole enamasti vaja koodi kirjutada. Kliendiportaal on üks paljudest Microsofti pakutavatest kättesaadavatest [Dynamics 365 portaalimallidest](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365).

[Topeltkirjutus](https://docs.microsoft.com/powerapps/maker/portals/overview) on valmiskujul taristutoode, mis pakub reaalaja lähedast suhtlust Dynamics 365 mudelipõhiste rakenduste ja Finance and Operationsi rakenduste vahel. Topeltkirjutus pakub kahesuunalist integratsiooni Finance and Operationsi rakenduste ja teenuse Common Data Service vahel. Seega pakub see rakenduste vahel integreeritud kasutuskogemust. Kliendiportaal sõltub topeltkirjutusega sünkroonitud üksustest. Enne Supply Chain Managementist pärinevate andmete esitamist kliendiportaalis peab olema topeltkirjutuse funktsioon kõikide asjakohaste üksuste jaoks lubatud.

![Kliendiportaali sõltuvused](media/customer-portal-elements.png "Kliendiportaali sõltuvused")

Kliendiportaal toimib lähtepunktina organisatsioonide jaoks, mis soovivad kasutada Power Appsi portaale, et ehitada väljapoole suunatud veebisait, mis kasutab nende Supply Chain Managementist pärinevaid andmeid. See aitab organisatsioonidel ühendada topeltkirjutuse, Supply Chain Managementi ja Power Appsi portaalid.