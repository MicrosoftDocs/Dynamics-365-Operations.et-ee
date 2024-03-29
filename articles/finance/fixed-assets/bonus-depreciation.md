---
title: Lisakulum
description: Selles artiklis antakse ülevaade lisakulumi funktsioonist.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: kfend
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 801747f06d16e70cd04b727787f0bfa6b6baefc0
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711141"
---
# <a name="bonus-depreciation"></a>Lisakulum

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade lisakulumi funktsioonist.

Lisakulumi rakendamine võimaldab teil põhivarale selle esimesel kasulikul töö- ja amortisatsiooniaastal lisakulumit arvestada. Lisakulum tuleb võtta enne mis tahes kulumiarvutusi. Seetõttu on kõige parem kasutada lisakulumit raamatutega, kus funktsioon Pearaamatusse sisestamine on keelatud. Saate kasutada suvandit **Pearaamatusse sisestamata kannete kustutamine**, et kustutada selliste raamatute kannete ajalugu, mis ei sisestada pearaamatusse. Seejärel saate mahutada lisakulumi hiljem vara elutsüklisse, kustutades eelnevalt sisestatud kulumikanded. 

Lisakulumit saate arvutada soovitusprotsessi abil või luua lisakulumikanded käsitsi. Lisakulumikandeid ei ole võimalik luua, kui selles põhivara kulumiraamatus on kulumikandeid või kulumi korrigeerimiskandeid.

Kui kasutate lisakulumi arvutamisel soovitusprotsessi, kaasatakse aluse arvutamisse kõik olemasolevad lisakulumikanded. Arvutus hõlmab ka mis tahes varasemaid lisakulumeid, mille sisestasite vara jaoks käsitsi. 

Kui põhivarale määratakse rohkem kui üks lisakulum, tuleb teil määrata prioriteedid. Iga lisakulum vähendab põhivara järgmise lisakulumi alust. Jääkväärtust põhivara lisakulumi aluse arvutustesse ei kaasata ning kulumi arvestusreeglid lisakulumile ei kehti. 

Praegu on Ameerika Ühendriikides määratletud teatud vara sektsiooni 179 varana. Sektsiooni 179 mahaarvamise abil saate taastada kogu või osa mõne vara maksumusest teatud piirini. Saate taastada kulu, arvates selle maha vara kasutuselevõtmise aastal.

## <a name="example"></a>Näide
Järgmised lisakulumid on seostatud vararaamatuga.

-   **Sektsioon 179:** 1000,00, prioriteet 1
-   **Tsooniprivileeg:** 30 protsenti, prioriteet 2

Vara soetusmaksumus on 5000,00. Lisakulumi arvutamisel saadakse sektsiooni 179 esimeseks lisakulumisummaks 1000,00 dollarit. 

Järgmine lisakulumi summa, tsooniprivileegi kulumi puhul, arvutatakse järgmiselt. 

Soetuskulu – 1000 (sektsiooni 179 kulum) x 30 protsenti = 1200 

Kui lisakulumi summa on rohkem kui ülejäänud soetusmaksumus, on lisakulumi summa lisakulumi arvutuse tulemus või ülejäänud soetusmaksumus, misiganes summa on väiksem. 

Kui soetusmaksumuse jääk on 0 (null) või sellest väiksem, siis lisakulumi kandeid ei looda. 

Lisakulumi arvutamisel soovitusprotsessi abil luuakse lisakulumikanne kõigi rakendatavate põhivara kulumiraamatuga seotud lisakulumikirjete kohta. 

Loodavate lisakulumikirjete arv on piiramatu. Pärast nende kirjete põhivaragrupi raamatule rakendatakse need sellele kulumiraamatusse. 

Lisakulum sisestatakse protsendina või kindla summana. Kui sisestate kulumisoovitusi, sisestatakse lisakulumikanded raamatusse kulumikannetest eraldi kannetena.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
