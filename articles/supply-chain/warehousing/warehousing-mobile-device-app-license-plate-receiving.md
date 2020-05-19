---
title: Identifitseerimisnumbri vastuvõtmine ladustamisrakenduse kaudu
description: Selles teemas selgitatakse, kuidas häälestada ladustamisrakendust, et toetada identifitseerimisnumbri vastuvõtmisprotsessi füüsiliste varude vastuvõtmiseks.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346372"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a>Identifitseerimisnumbri vastuvõtmine ladustamisrakenduse kaudu

Selles teemas selgitatakse, kuidas häälestada ladustamisrakendust, et see toetaks identifitseerimisnumbri vastuvõtmisprotsessi füüsiliste varude vastuvõtmiseks.

Selle funktsiooni abil saate kiiresti kirjendada sissetulevate varude vastuvõtmist, mis on seotud saadetise eelteatisega (ASN). Süsteem loob automaatselt ASN-i, kui üleviimistellimuse saatmiseks kasutatakse laohaldusprotsesse. Ostutellimuse protsessi puhul saab ASN-i käsitsi kirjendada või automaatselt importida sissetuleva ASN-i andmeüksuse protsessi abil.

ASN-i andmed on seotud koormate ja saadetistega *pakkestruktuuride* kaudu, kus kaubaalused (peamised identifitseerimisnumbrid) võivad sisaldada kaste (pesastatud identifitseerimisnumbrid).

> [!NOTE]
> Selleks, et vähendada laokannete arvu, kui kasutatakse pesastatud identifitseerimisnumbreid, siis registreerib süsteem füüsilise vaba kaubavaru peamisele identifitseermisnumbrile. Füüsiline vaba kaubavaru liikumise käivitamiseks pesastatud identifitseerimisnumbrilt peamisele identifitseerimisnumbrile pakkestruktuuri andmete põhjal, peab mobiilses seadmes olema menüü üksus, mis põhineb töö loomise protsessil *Pakena pesastatud identifitseerimisnumbritele*.

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a>Kuva või jäta vastuvõtmise kokkuvõte leht

Saate kasutada funktsiooni *Kokkuvõtte lehe vastuvõtmise juhtimine mobiilses seadmes*, et kasutada täiendava üksikasjaliku ladustamisrakenduse voogu identifitseerimisnumbri vastuvõtmisprotsessi osana.

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse seda funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *kokkuvõtte lehe vastuvõtmise juhtimine mobiilses seadmes*

Kui see funktsioon on sisse lülitatud, annavad identifitseerimisnumbri vastuvõtmise või identifitseerimisnumbri vastuvõtmise ja ladustamise menüü üksused mobiilses seadmes sätte **Kuva vastuvõttev kokkuvõtte leht**. Sellel sättel on järgmised suvandid.

- **Kuva üksikasjalik kokkuvõte** – identifitseerimisnumbri vastuvõtmise ajal kuvatakse töötajatele täiendav leht, mis sisaldab täielikku ASN-i teavet.
- **Jäta kokkuvõte vahele** – töötajatele ei kuvata täielikku ASN-i teavet. Lao töötajad ei saa määrata ka likvideerimiskoodi või lisada erandeid vastuvõtu protsessi ajal.

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Takista üleviimistellimuse – saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu

Identifitseerimisnumbri vastuvõtmisprotsessi ei saa kasutada, kui ASN sisaldab juba olemasolevat identifitseerimisnumbri ID-d ja sellel on füüsiline vaba kaubavaru muus lao asukohas, kus identifitseerimisnumbri registreerimine toimub.

Üleviimistellimuste olukorras, kus transiitlaos ei jälgita identifitseerimisnumbreid (ja seega ei jälgita ka füüsilist vaba kaubavaru identifitseerimisnumbri kohta), saate kasutada funktsiooni *Takista üleviimistellimuse – saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu*, et vältida transiidis olevate identifitseerimisnumbrite füüsilise vaba kaubavaru värskendamist.

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse seda funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Takista üleviimistellimuse saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu*

Selle funktsiooni haldamiseks, kui see on saadaval, toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Määrake vahekaardi **Üldine** kiirkaardil **Identifitseerimisnumbrid** väljale **Transiitlao identifitseerimisnumbri poliitika** üks järgmistest väärtustest.

    - **Luba mittejälitatud identifitseerimisnumbri taaskasutamine** – süsteem töötab samamoodi nagu siis, kui funktsioon *Takista üleviimistellimuse saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu* pole saadaval. See väärtus on vaikesäte funktsiooni esmakordsel aktiveerimisel.
    - **Takista mittejälitatud identifitseerimisnumbri korduvkasutamist** – sihtkoha laos on lubatud ainult need vaba kauvabaru värskendused, mis on seotud saadetud identifitseerimisnumbriga, kuni üleviimistellimus on vastu võetud.

## <a name="more-information"></a>Lisateave

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

Lisateavet mobiilse seadme menüü üksuste kohta vt teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).
