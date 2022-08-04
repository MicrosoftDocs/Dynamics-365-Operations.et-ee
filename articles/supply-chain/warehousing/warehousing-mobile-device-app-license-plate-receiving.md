---
title: Identifitseerimisnumbri vastuvõtmine mobiilirakenduse Warehouse Management kaudu
description: See artikkel selgitab, kuidas laohalduse mobiilirakendust seadistada, et toetada litsentsiplaadi vastuvõtuprotsessi füüsiliste varude saamiseks.
author: perlynne
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters, WHSRFMenuItem, WHSLicensePlate, WHSPackingStructure
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 657c29ec6ddfb2be918424e06eaf219f51a30a02
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069058"
---
# <a name="license-plate-receiving-via-the-warehouse-management-mobile-app"></a>Identifitseerimisnumbri vastuvõtmine mobiilirakenduse Warehouse Management kaudu

[!include [banner](../includes/banner.md)]

See artikkel selgitab laohalduse mobiilirakenduse seadistamist nii, et see toetab füüsiliste varude vastuvõtuprotsessi litsentsiplaadiga vastuvõtuprotsessi kasutamist.

Selle funktsiooni abil saate kiiresti kirjendada sissetulevate varude vastuvõtmist, mis on seotud saadetise eelteatisega (ASN). Süsteem loob ASN-i automaatselt, kui laohaldusprotsesse (WMS) kasutatakse üleviimistellimuse lähetamiseks. Ostutellimuse protsessi puhul saab ASN-i käsitsi kirjendada või automaatselt importida sissetuleva ASN-i andmeüksuse protsessi abil.

ASN-i andmed on seotud koormate ja saadetistega *pakkestruktuuride* kaudu, kus kaubaalused (peamised identifitseerimisnumbrid) võivad sisaldada kaste (pesastatud identifitseerimisnumbrid).

> [!NOTE]
> Selleks, et vähendada laokannete arvu, kui kasutatakse pesastatud identifitseerimisnumbreid, siis registreerib süsteem füüsilise vaba kaubavaru peamisele identifitseermisnumbrile. Füüsiline vaba kaubavaru liikumise käivitamiseks pesastatud identifitseerimisnumbrilt peamisele identifitseerimisnumbrile pakkestruktuuri andmete põhjal, peab mobiilses seadmes olema menüü üksus, mis põhineb töö loomise protsessil *Pakena pesastatud identifitseerimisnumbritele*.

## <a name="warehousing-mobile-device-app-processing"></a>Ladustamise mobiilse seadme rakenduse töötlemine

Kui töötaja skannib sissetuleva litsentsiplaadi ID, siis käivitab süsteem litsentsiplaadi vastuvõtuprotsessi. Selle teabe alusel registreeritakse litsentsiplaadi sisu (ASNist tulevad andmed) füüsiliselt saabumisala asukohas. Järgnevas voost sõltuvad teie äriprotsessiga seotud vajadused.

## <a name="work-policies"></a>Tööpoliitikad

(Näiteks) mobiilse seadme menüükäsu *Teata lõpetamisest* protsessi puhul toetab protsessi vastuvõttev litsentsiplaat määratletud seadistuse alusel mitmeid töövooge.

### <a name="work-policies-with-work-creation"></a>Tööloomega tööpoliitikad

Kui registreerite sissetulevad kaubad töid loova tööpoliitika abil, siis loob ja salvestab süsteem iga registreeringu kohta kõrvaleseatavad töökirjed. Kui kasutate tööprotsessi *Litsentsiplaadi vastuvõtt ja kõrvaleseadmine*, siis käsitletakse registreeringut ja kõrvaleseadmist ühe toiminguna, kasutades ühte mobiilse seadme menüükäsku. Protsessi *Vastuvõttev litsentsiplaat* kasutamisel käsitletakse vastuvõtu ja kõrvalseadmise protsesse kahe erineva ladustamistoiminguna, millest kumbagi kohta käib eraldi mobiilse seadme menüükäsk.

### <a name="work-policies-without-work-creation"></a>Tööloometa tööpoliitikad

Te saate kasutada litsentsiplaadi vastuvõtuprotsessi tööd loomata. Kui määratlete tööpoliitikad, millel on töökäsu tüüp *Üleviimistarne* ja/või *Ostutellimused* ning kasutate protsessi *Litsentsiplaadi vastuvõtmiseks (ja kõrvaleseadmiseks)*, siis ei loo järgmised kaks ladustamise mobiilirakenduse protsessi uut tööd. Selle asemel registreeritakse litsentsiplaadil vastuvõtualal sissetulevad füüsilised varud.

- *Vastuvõttev litsentsiplaat*
- *Litsentsiplaadi vastuvõtt ja kõrvaleseadmine*

> [!NOTE]
> - Peate määratlema jaotises **Varude asukohad** vähemalt ühe asukoha tööpoliitika jaoks. Sama asukohta ei saa määrata mitme tööpoliitika jaoks.
> - Ladustamise mobiilse seadme menüükäskude suvand **Prindi silt** ei prindi tööd loomata litsentsiplaadi silti.

Funktsiooni oma süsteemis kättesaadavaks muutmiseks peate lülitama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse funktsiooni *Ladustamisrakenduse täiustusi vastu võttev litsentsiplaat*.

### <a name="receive-inventory-on-a-location-that-doesnt-track-license-plates"></a>Litsentsiplaate mittejälgivas asukohas varude vastuvõtmine

Asukoha profiilile määratud lao asukohta saab kasutada ka siis, kui funktsioon **Kasuta litsentsiplaadi jälgimist** ei ole sisse lülitatud. Seega saate varude vastuvõtmisel registreerida vabad varud otse asukohas, loomata selleks tööd.

## <a name="add-mobile-device-menu-items-for-each-receiving-location-in-a-warehouse"></a>Mobiilse seadme menüükäskude lisamine iga vastuvõtva asukoha jaoks laos

Funktsioon *Ladustamisrakenduse täiustusi vastu võttev litsentsiplaat* võimaldab teil teostada vastuvõtte mis tahes asukohas laos, lisades ladustamise mobiilirakendusele vastuvõtva (ja kõrvaleseadva) asukohapõhise litsentsiplaadi menüükäsud. Varem toetas süsteem vastuvõtmist ainult iga lao jaoks eraldi seatud vaikimisi asukohas. Nüüd aga pakuvad antud funktsiooni sisse lülitamisel mobiilse seadme vastuvõtva (ja kõrvaleseadva) litsentsiplaadi menüükäsud võimalust **Kasuta vaikeandmeid**, mis võimaldab teil valida iga menüükäsu jaoks kohandatud „kuhu“ asukoha. (See suvand oli teatud menüükäsu tüüpide jaoks juba saadaval.)

Funktsiooni oma süsteemis kättesaadavaks muutmiseks peate lülitama [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse funktsiooni *Ladustamisrakenduse täiustusi vastu võttev litsentsiplaat*.

## <a name="show-or-skip-the-receiving-summary-page"></a>Kuva või jäta vastuvõtmise kokkuvõte leht

Saate kasutada funktsiooni *Kokkuvõtte lehe vastuvõtmise juhtimine mobiilses seadmes*, et kasutada täiendava üksikasjaliku lao mobiilirakenduse Warehouse Management voogu identifitseerimisnumbri vastuvõtmisprotsessi osana.

Kui see funktsioon on sisse lülitatud, annavad identifitseerimisnumbri vastuvõtmise või identifitseerimisnumbri vastuvõtmise ja ladustamise menüü üksused mobiilses seadmes sätte **Kuva vastuvõttev kokkuvõtte leht**. Sellel sättel on järgmised suvandid.

- **Kuva üksikasjalik kokkuvõte** – identifitseerimisnumbri vastuvõtmise ajal kuvatakse töötajatele täiendav leht, mis sisaldab täielikku ASN-i teavet.
- **Jäta kokkuvõte vahele** – töötajatele ei kuvata täielikku ASN-i teavet. Lao töötajad ei saa määrata ka likvideerimiskoodi või lisada erandeid vastuvõtu protsessi ajal.

Selle funktsiooni kasutamiseks peab juhtelement, *kas kuvada mobiilse seadme funktsiooni vastuvõtu kokkuvõtete* lehekülg, olema süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.21 puhul on see funktsioon vaikimisi sisse lülitatud. Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides Juhtelementi, kas kuvada vastuvõtu kokkuvõtteleht mobiilsete seadmete funktsioonis Funktsioonihalduse tööruumis.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a>Takista üleviimistellimuse – saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu

Identifitseerimisnumbri vastuvõtmisprotsessi ei saa kasutada, kui ASN sisaldab juba olemasolevat identifitseerimisnumbri ID-d ja sellel on füüsiline vaba kaubavaru muus lao asukohas, kus identifitseerimisnumbri registreerimine toimub.

Üleviimistellimuste olukorras, kus transiitlaos ei jälgita identifitseerimisnumbreid (ja seega ei jälgita ka füüsilist vaba kaubavaru identifitseerimisnumbri kohta), saate kasutada funktsiooni *Takista üleviimistellimuse – saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu*, et vältida transiidis olevate identifitseerimisnumbrite füüsilise vaba kaubavaru värskendamist. Et see funktsioon oleks saadaval, *peab teie süsteemi jaoks olema sisse lülitatud funktsioon Takista üleviimistellimuse* saadetud litsentsiplaate kasutamast muudes ladudes kui sihtlao funktsioon. Tarneahela halduse 10.0.25 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on vanem kui 10.0.25, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides seda Funktsioonihalduse [tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Selle funktsiooni haldamiseks, kui see on saadaval, toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Määrake vahekaardi **Üldine** kiirkaardil **Identifitseerimisnumbrid** väljale **Transiitlao identifitseerimisnumbri poliitika** üks järgmistest väärtustest.

    - **Luba mittejälitatud identifitseerimisnumbri taaskasutamine** – süsteem töötab samamoodi nagu siis, kui funktsioon *Takista üleviimistellimuse saadetud identifitseerimisnumbrite kasutamist muudes ladudes, mis ei ole sihtkoha ladu* pole saadaval. See väärtus on vaikesäte funktsiooni esmakordsel aktiveerimisel.
    - **Takista mittejälitatud identifitseerimisnumbri korduvkasutamist** – sihtkoha laos on lubatud ainult need vaba kauvabaru värskendused, mis on seotud saadetud identifitseerimisnumbriga, kuni üleviimistellimus on vastu võetud.

## <a name="more-information"></a>Lisateave

Lisateavet mobiilse seadme menüü üksuste kohta vt teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).

Lisateavet tootestsenaariumi *Teata lõpetamisest* kohta vt teemast [Lao tööpoliitikate ülevaade](warehouse-work-policies.md).

Lisateavet sissetuleva koormuse halduse kohta vt teemast [Ostutellimuste sissetulevate koormate laohaldus](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]