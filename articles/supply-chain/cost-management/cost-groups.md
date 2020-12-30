---
title: Kulugrupid
description: Kulugrupid annavad aluse toodetud kauba omahinna püsikulude, nt materjali, töö ja üldise püsikulude segmentimiseks ja analüüsimiseks. Kulugrupi segmentimisel on tootmiskeskkonnas mitu sünonüümi, nagu kulude jaotamine, kulu eraldamine või kulu klassifikatsioon.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dee8e40de43480cd010b5acc41a3d87611c2ab6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426401"
---
# <a name="cost-groups"></a>Kulugrupid

[!include [banner](../includes/banner.md)]

Kulugrupid annavad aluse toodetud kauba omahinna püsikulude, nt materjali, töö ja üldise püsikulude segmentimiseks ja analüüsimiseks. Kulugrupi segmentimisel on tootmiskeskkonnas mitu sünonüümi, nagu kulude jaotamine, kulu eraldamine või kulu klassifikatsioon. 

Kulugrupi segmentimisel on tootmiskeskkonnas mitu sünonüümi, nagu kulude jaotamine, kulu eraldamine või kulu klassifikatsioon. Kulugrupi segmentimine võib täita mitut eesmärki. Järgmisena on toodud mõned näited.

-   See võib segmentida erinevat tüüpi materjalide, nagu koostisained ja pakkematerjal konserveeritud kaupade jaoks, kulusid kaupadele määratud kulugruppide põhjal.
-   See võib segmentida erinevat tüüpi operatsiooniressursside, nagu erinevat tüüpi tööd või masinad, kulusid operatsiooniressursside ja marsruutimisoperatsioonidega seotud kulukategooriatele määratud kulugruppide põhjal.
-   See võib segmentida seadistusaja ja käitusaja kulusid marsruutimisoperatsioonides marsruutimisoperatsioonidega seotud kulukategooriatele määratud kulugruppide põhjal.
-   See võib segmentida erinevat tüüpi üldkulude, nagu töö ja masinatega seotud üldkulud, kulusid kuluarvutustabeli seadistuses kaudsetele kuludele määratud kulugruppide põhjal.
-   See võib toimida kuluarvutuse lehe seadistuses mitmesugust tüüpi tootmise üldkulude arvutamise alusena. See üldkulu võib sisaldada erinevaid operatsiooniressursside marsruutimisteabe või seadistus- ja käitusaja teabega seotud üldkulusid. Tootmise üldkulu võib olla seotud ka komponentmaterjali kuluosaga, mis kajastab lean manufacturingi põhimõtet, mis kõrvaldab vajaduse marsruutimisteabe järgi.

Kulugrupi segmentimine kehtib toodetud kauba arvutatud kulu kohta, olenemata sellest, kas see kulu põhines standardsetel kuludel või planeeritud kuludel. Lehel **Kokkuvõte** kuvatakse see segmentimine kulugruppide, taseme või nii kulugrupi kui ka taseme järgi. 

Võimet säilitada kulugrupi segmentimine tootmisstruktuuri mitme taseme lõikes nimetatakse *tükeldamiseks*. Tükeldamine rakendub ainult toodetud kaupadele, mis kasutavad standardse kulu laovarude mudelit. Kui tükeldamist ei kasutata, käsitletakse toodetud komponendi kulu materjali kuluosana. Varude parameeter kulude jaotamiseks alammoodulite kaupa näitab, et kulugrupi segmentimine säilitatakse standardse kulu arvutamisel üle mitme taseme. Kui aga poliitikal pole tasemeid, rakendub kulugrupi segmentimine ainult ühe taseme arvutamisele. Näiteks kuvatakse lehel **Kulude ümberarvestus kulugruppide kaupa** kulugrupi segmentimine standardsete kuluüksuste puhul mitme taseme lõikes. 

Kulugrupi segmentimist saab rakendada standardsete kuluüksuste hälvete puhul. Teine varude parameeter määratleb, kas hälbed määratakse kulugrupi alusel või lihtsalt summeeritakse. 

Kulugrupile saab määrata kulugrupi tüübi ja toimimise täiendavate segmentimise eesmärkide puhul.

-   **Kulugrupi tüüp** – igale kulugrupile tuleb määrata kulugrupi tüüp, mis näitab, et kulugrupp rakendub otse materjalile, otse tootmisele või otse välisteenustele, või määratleda selle kas kaudsena või määratlematuna. Otsese materjalina määratud kulugrupi saab määrata kaupadele. Otsese tootmise kulugrupi saab määrata kulukategooriatele. Otsese välisteenuste kulugrupi saab määrata teenuse tootetüübile, et saaksite liigitada teenuse ostmisega seotud kulusid allhanketegevustesse. Kaudse kulugrupi saab määrata lisatasude või määrade kaudsetele kuludele. Määratlemata kulugrupi saab määrata kaupadele, kulukategooriatele või kaudsetele kuludele. Kulugrupi tüübi määramisel on mitu eesmärki. Esiteks piirab see kulugrupi määramise võimalust ja kohalduvate kulugruppide loendi vaatamist. Teiseks võimaldab see lisasegmentimist aruandluse eesmärgil. Kolmandaks saab seda kasutada hälvete pearaamatukontode määramiseks.
-   **Käitumine** – igale kulugrupile saab valikuliselt määrata käitumise, mis näitab kulugrupi rakendumist fikseeritud kuludele või muutuvkuludele. Kulugruppi, mille käitumise väärtus on null, käsitletakse muutuva kuluna. Käitumine määratakse vaid aruandluse eesmärgil. Näiteks saab kulusid kuvada fikseeritud ja muutuvkulude segmentatsioonina kuluarvutustabelis ja lehel **Kulude ümberarvestus kulugruppide kaupa**. Igale kulugrupile kasumisätte protsentide määramisel pakub koosluse arvutamine soovituslikke müügihindu kulupõhise hinnalisandi alusel.




