---
title: Pakkimiseks ja ladustamiseks erinevate dimensioonide määramine
description: See teema näitab, kuidas määrata, millise protsessi (pakkimine, ladustamine või pesastatud pakkimine) jaoks iga määratud dimensiooni kasutatakse.
author: mirzaab
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResPhysicalProductDimensions, WHSPhysDimUOM
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e8ce576f21f1f5ea5f3acb7d43bbe68826e6f39
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580068"
---
# <a name="set-different-dimensions-for-packing-and-storage"></a>Pakkimiseks ja ladustamiseks erinevate dimensioonide määramine

[!include [banner](../../includes/banner.md)]

Mõned kaubad on pakitud või ladustatud nii, et teil võib tekkida vajadus jälgida füüsilisi dimensioone iga erineva protsessi puhul teisiti. Funktsiooni *Pakendatava toote dimensioonid* abil saate igale tootele seadistada ühe või mitut tüüpi mõõtmeid. Iga dimensiooni tüüp tagab füüsiliste mõõtmiste kogumi (kaal, laius, sügavus ja kõrgus) ning määrab nende füüsiliste mõõtmise väärtuste rakendumise protsessi. Kui see funktsioon on lubatud, toetab süsteem järgmisi dimensiooni tüüpe.

- *Ladustamine* – laoala dimensioone kasutatakse koos asukoha mahuliste mõõtmetega, et määrata, kui palju iga kaupa saab erinevates lao asukohtades ladustada.
- *Pakkimine* – pakkimise dimensioone kasutatakse konteineritesse pakkimisel ja käsitsi pakkimise protsessi käigus, et määrata, kui palju iga kaupa erinevatesse konteineritüüpidesse mahub.
- *Pesastatud pakkimine* – pesastatud pakkimise dimensioone kasutatakse siis, kui pakkimisprotsess sisaldab mitut taset.

*Ladustamise* dimensioone toetatakse isegi juhul, kui funktsioon *Pakendatava toote dimensioonid* pole lubatud. Häälestate need rakenduse Supply Chain Management lehte **Füüsiline dimensioon** kasutades. Neid dimensioone kasutavad kõik protsessid, kus pakkimise ja pesastatud pakkimise dimensioonid on määramata.

*Pakkimise* ja *pesastatud pakkimise* dimensioonid häälestatakse, kasutades lehte **Toote füüsilised dimensioonid**, mis lisatakse, kui lubate funktsiooni *Pakendatava toote dimensioonid*.
See teema sisaldab stsenaariumit, mis kirjeldab selle funktsiooni kasutamist.

## <a name="turn-on-the-packaging-product-dimensions-feature"></a>Lülitage pakendatavate toodete dimensioonide funktsioon sisse.

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Pakendatavate toodete mõõtmed*

## <a name="example-scenario"></a>Näidisstsenaarium

### <a name="set-up-the-scenario"></a>Stsenaariumi seadistamine

Enne kui käivitate näidisstsenaariumi, peate oma süsteemi selles jaotises kirjeldatud viisil ette valmistama.

#### <a name="enable-demo-data"></a>Demoandmete lubamine

Selle stsenaariumi kasutamiseks siin määratud demokirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku *USMF*.

#### <a name="add-a-new-physical-dimension-to-a-product"></a>Tootele uue füüsilise dimensiooni lisamine

Lisage tootele uus füüsiline dimensioon, tehes järgmist:

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toote **kaubakoodiga** *A0001*.
1. Avage toimingupaani vahekaart **Varude haldamine** ja valige grupis **Ladu** suvand **Füüsilised toote dimensioonid**.
1. Avaneb leht **Füüsilised toote dimensioonid**. Valige tegevuspaanil suvand **Uus**, et lisada ruudustikku uus dimensioon koos järgmiste sätetega.
    - **Füüsilise dimensiooni tüüp** - *Pakkimine*
    - **Füüsiline ühik** - *tk*
    - **Kaal** - *4*
    - **Massiühik** - *kg*
    - **Sügavus** - *3*
    - **Kõrgus** - *4*
    - **Laius** - *3*
    - **Pikkus** - *cm*
    - **Mahuühik** - *cm3*

Väli **Maht** arvutatakse automaatselt teie sätete **Sügavus**, **Kõrgus** ja **Laius** põhjal.

#### <a name="create-a-new-container-type"></a>Uue konteineri tüübi loomine

Avage suvand **Laohaldus \> Seadistus \> Konteinerid \> Konteineri tüübid** ja looge uus kirje järgmiste sätetega.

- **Konteineri tüübi kood** - *lühike kast*
- **Kirjeldus** - *lühike kast*
- **Maksimaalne netokaal** - *50*
- **Maht** - *144*
- **Pikkus** - *6*
- **Laius** - *6*
- **Kõrgus** - *4*

#### <a name="create-a-container-group"></a>Konteinerigrupi loomine

Avage suvand **Laohaldus \> Seadistus \> Konteinerid \> Konteinerigrupid** ja looge uus kirje järgmiste sätetega.

- **Konteinerigrupi ID** - *lühike kast*
- **Kirjeldus** - *lühike kast*

Lisage uus rida jaotisse **Üksikasjad**. Määrake **konteineri tüübiks** *Lühike kast*.

#### <a name="set-up-a-container-build-template"></a>Konteineri koostemalli häälestamine

Avage **Laohaldus \> Seadistus \> Konteinerid \> Konteinerite loomise mallid** ja valige **Kastid**. Muutke **konteinerigrupi ID** valikule *lühike kast*.

### <a name="run-the-scenario"></a>Käivitage stsenaarium

Pärast oma süsteemi ettevalmistamist eelmises jaotises kirjeldatud viisil olete valmis käivitama stsenaariumi nii, nagu on kirjeldatud järgmises jaotises.

#### <a name="create-a-sales-order-and-create-a-shipment"></a>Müügitellimuse ja saadetise loomine

Selles protsessis loote saadetise kauba *pakendamise* dimensioonide põhjal, mille kõrgus on alla 3.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *63*

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *5*

1. Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.
1. Sulgege leht.
1. Avage tegevuspaani vahekaart **Ladu** ja valige **Lattu väljastamine**, et luua lao jaoks töö.
1. Kiirkaardil **Müügitellimuse** read valige **Ladu \> Saadetise üksikasjad**.
1. Avage toimingupaanilt vahekaart **Transport** ja valige **Kuva konteinerid**. Kinnitage, et kaup pakiti konteineritesse, mis olid kaks *lühikese kasti* konteinerit.

#### <a name="place-an-item-into-storage"></a>Kauba lattu panemine

1. Avage mobiilne seade, logige sisse lattu 63 ja avage **Varud \> Korrigeeri üksuses**.
1. Sisestage **Loc** = *SHORT-01*. Tehke uus registreerimismärk näitajatega **Kaup** = *A0001* ja **Kogus** = *1 tk*.
1. Valige nupp **OK**. Teile kuvatakse tõrge „Asukoha SHORT-01 valimine nurjus, sest kaup A0001 ei mahu asukoha määratud mõõtmesse.” Seda seetõttu, et toote tüübi *Ladu* dimensioonid on suuremad kui asukoha profiilis määratletud dimensioonid.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]