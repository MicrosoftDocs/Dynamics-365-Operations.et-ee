---
title: Sisu tarne võrgu rakendamise suvandid
description: See teema annab ülevaate erinevatest võimalustest sisu tarnevõrgu (CDN) rakendamise kohta, mida saab kasutada Microsoft Dynamics 365 Commerce keskkondades. Need valikud on rakenduse Azure Front Door rakenduse Commerce antud eksemplarid ja Azure Front Door kliendi-eksemplarid.
author: BrianShook
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 73da1fff8f79b4fcde38f9da643b8a3479247959f763976d782279e4e2af7a33
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729910"
---
# <a name="content-delivery-network-implementation-options"></a>Sisu tarne võrgu rakendamise suvandid

[!include [banner](includes/banner.md)]

See teema annab ülevaate erinevatest võimalustest sisu tarnevõrgu (CDN) rakendamise kohta, mida saab kasutada Microsoft Dynamics 365 Commerce keskkondades. Need valikud on rakenduse Azure Front Door rakenduse Commerce antud eksemplarid ja Azure Front Door kliendi-eksemplarid.

Äriklientidel on mitu valikut, kui nad kaaluvad, millist CDN-teenust oma Ärikeskkonnas kasutada. Commerce on vabastatud põhilise Azure Front Door toega, mis katab baashostimis- ja kohandatud domeeninõudeid. Ettevõtete puhul, kes soovivad rohkem kontrolli ja spetsiifilisesid turvavõimeid, nagu veebirakenduse tulemüür (WAF), on parim valik kasutada kas Azure Front Doori kliendiomast eksemplari või välist CDN-teenust.

Commerce'i keskkondades saab kasutada kolme CDN-i rakendusvalikut:

- Saate kasutada Commerce'i pakutavat Azure Front Door eksemplari
- Kliendi omanduses olev Azure Front Door eksemplar (suurema kontrolli ja täiendavate turvafunktsioonide jaoks)
- Väline CDN-teenus

Kõik kolm CDN-i rakendusvalikut annavad kohandatud domeenidest ainult dünaamilise HTML-sisu. Commerce halddab Microsofti hallatud CDN-ide kaudu automaatselt kõigi JavaScript, kaskaadstiililehti (CSS), pilte, videosid ja muud staatilist sisu. Teie valitud suvand määrab saadaolevad tegevusvõimalused, juhtimisvõimalused ja täiendavad turvavõimalused.

Järgmisel joonisel on näidatud ülevaade pakkumiskutse protsessist.

![Ülevaade Commerce ülesehitusest.](media/Commerce_CDN-Option_ComparisonModels.png)

Lisateavet Rakenduse Azure Front Door eksemplari häälestamise kohta ärisaidi jaoks vt [Lisa CDN-tugi](add-cdn-support.md).

## <a name="use-the-commerce-provided-azure-front-door-instance"></a>Saate kasutada Commerce'i pakutavat Azure Front Door eksemplari

Järgmises tabelis loetletakse rakenduse Azure Front Door Commerce-antud eksemplari kasutamise plusse ja miinuseid sisu lõpp-punktide haldamiseks.

| Plusse | Miinuseid |
|------|------|
| <ul><li>Eksemplar kaasatakse ärikulusse.</li><li>Kuna ärimeeskond haldab eksemplari, on vajalik väiksem hooldus ja häälestusetappideks on ühiskasutusega etapid.</li><li>Azure'i majutatud infrastruktuur on skaleeritav, turvaline ja usaldusväärne.</li><li>Secure Sockets Layeri (SSL) sert nõuab kellaaja seadistust ja seda uuendatakse automaatselt.</li><li>Ärimeeskond jälgib eksemplari vigade ja hälbide suhtes.</li></ul> | <ul><li>Kooslust ei toetata.</li><li>Konkreetseid kohandusi ega seadistuse korrigeerimisi pole.</li><li>Eksemplar sõltub ärimeeskonnast uuenduste või muudatuste puhul.</li><li>Domeenide ja laiendusdomeenide integreerimiseks Azure'i DNS-iga on vaja eraldi Azure Front Door eksemplari.</li><li>Puudub telemeetria vastuste kohta sekundis (RPS) või kliendile pakutakse veamäära.</li></ul> |

Järgmine näide näitab Commerce-toetatud Azure Front Door`i eksemplari arhitektuuri.

![Saate kasutada Commerce pakutavat Azure Front Door eksemplari.](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a>Kasuta kliendi-põhist Azure Front Door eksemplari

Järgmises tabelis loetletakse rakenduse Azure Front Door Commerce-antud eksemplari kasutamise plusse ja miinuseid sisu lõpp-punktide haldamiseks.

| Plusse | Miinuseid |
|------|------|
| <ul><li>Seadistus on turvaline ja seda on lihtne hallata.</li><li>Azure'i majutatud infrastruktuur on skaleeritav, turvaline ja usaldusväärne.</li><li>Eksemplar võimaldab WAF-i integreerimist ja granulaarreegli juhtimist trahvija astme turvalisusele, mis on häälestatud konkreetselt teie saidile.</li><li>Eksemplar võimaldab SSL-sertifikaatide (nii kliendi omad kui ka Azure Front Door-hallatud) ja domeeni seostamist trahvija kontrolli.</li><li>Eksemplar pakub apex domeenilahendust, kui see on ühendatud otse Azure DNS-iga.</li><li>Antakse telemeetria ja teatis.</li><li>Secure Sockets Layeri (SSL) sert nõuab kellaaja seadistust ja seda uuendatakse automaatselt.</li></ul> | <ul><li>Eksemplar on ise hallatav.</li><li>Nõutakse algset teadmiste kogust.</li></ul> |

Järgmine näide näitab äri infrastruktuuri, mis sisaldab kliendi-omast Azure Front Door`i eksemplari.

![Järgmine näide näitab Commerce infrastruktuuri, mis sisaldab kliendi-omast Azure Front Door eksemplari.](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a>Väline CDN-teenus

Järgmises tabelis loetletakse välise CDN-teenuse kasutamise plussid ja miinused sisu lõpp-punktide haldamiseks.

| Plusse | Miinuseid |
|------|------|
| <ul><li>See valik on kasulik, kui olemasolev domeen on juba majutatud välisele CDN-ile.</li><li>WAF: sõltub välisest pakkujast.</li></ul> | <ul><li>Eraldi leping ja täiendav kuluarvestus on nõutavad.</li><li>SSL võib vajada lisakulusid.</li><li>Kuna teenus on eraldi Azure'i pilvestruktuurist, tuleb hallata lisa infrastruktuuri.</li><li>Teenus võib nõuda pikemaid ajainvesteeringuid lõpp-punkti ja turvalisuse seadistusse.</li><li>Teenus on ise hallatav.</li><li>Teenus on ise jälgitav.</li></ul> |

Järgmine näide näitab Äri infrastruktuuri, mis sisaldab välist CDN-teenust.

![Commerce infrastruktuur, mis sisaldab välist CDN-teenust.](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a>Lisaressursid

[Sisu edastamise võrgu (CDN) toe lisamine](add-cdn-support.md)
