---
title: Klassid "Vähem kui koormatäis" (LTL)
description: See teema kirjeldab, mis on "vähem kui koormatäis" (LTL) klassid ja kirjeldab, kuidas neid Microsoftis Dynamics 365 Supply Chain Management seadistada.
author: Henrikan
ms.date: 04/05/2021
ms.topic: article
ms.search.form: WHSLTLClass
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 295006cac0a67cd577809a1b62566de043ea55fb
ms.sourcegitcommit: 636c1bf096a8666a551b67e898da1f48feb9a187
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5941806"
---
# <a name="less-than-truckload-ltl-classes"></a>Klassid "Vähem kui koormatäis" (LTL)

[!include [banner](../includes/banner.md)]

Alla "Vähem kui koormatäis" (LTL) klass on veose lähetusklass, mida kasutatakse saadetavate kaupade klassifitseerimiseks. Üldiselt on igal toote või kauba tüübil riikliku autoveose klassifikatsiooni (NMFC) kood, mis vastab LTL-saadetiste konkreetsele veoklassi numbrile. LTL-veoseklassid esindavad kaupade kategooriaid, samas kui NMFC-koodid on seotud kindlate kaupadega igasühes 18 veose klassist.

See funktsioon võimaldab teil oma süsteemi kasutada, et teha järgmisi toiminguid.

- Määratlege LTL-veoklassid, mida kasutatakse teie ettevõttes.
- Määrake igale NMFC-koodile **NMFC-koodide** lehel LTL-klass. Lisateavet vt [riikliku autoveose klassifikatsiooni (NMFC) koodidest](nmfc-codes.md).
- Määrake NMFC-kood (ja seega ka LTL-kood) igale tootele lehel **Tooted**.
- Hinnake täpselt iga toote LTL-klassi, millele NMFC-kood on määratud.
- Määratlege iga LTL-klassi pakkimisnõuded, kontrollides rahvusvahelisi LTL-standardeid. Sel viisil tagate, et teie tooted on hästi kaitstud ja turvaliselt saadetud.
- Saate täpsed saadetise hinnangud, mis põhinevad iga toote LTL-veoklassil.

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Supply Chain Management LTL-klasse.

## <a name="create-an-ltl-class"></a>LTL-klassi loomine

LTL-klassi loomiseks tehke järgmist.

1. Järgige üht neist sammudest.

    - Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> LTL-klassid**.
    - Avage **Transpordihaldus \> Seadistused \> Transpordistandardid \> LTL-klassid**.

2. LTL-klassi loomiseks valige toimingupaanilt suvand **Uus**. Seejärel määrake järgmised väljad.

    - **LTL-klass** – sisestage oma ettevõtte sisemine LTL-klassi kood (ID) artiklitüübi puhul. Enamik ettevõtteid kasutab seda rahvusvahelist standardit. Sellisel juhul vastab selle välja väärtus välja **Klass** väärtusele. Kui teie ettevõte kasutab siiski oma standardit, sisestage sellele standardile vastav kood.
    - **Nimi** – sisestage kirjeldav nimi, mis aitab teil ja teistel kasutajatel valida iga NMFC-koodi jaoks õige LTL-klassi.
    - **Klass** – sisestage kaubatüübi rahvusvaheline standardne LTL-klassi ID-kood. Siia sisestav kood peab vastama ametlikule standardile.

## <a name="example-set-up-ltl-classes"></a>Näide: LTL-klasside häälestamine

Järgmine näide näitab, kuidas seadistada kahte erinevat LTL-klassi, mida saate kasutada erinevat tüüpi toodetega.

1. Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> LTL-klassid**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **LTL klass:** *92.5*
    - **Nimi:** *arvutid, monitorid, külmikud*
    - **Klass:** *92.5*

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **LTL klass:** *125*
    - **Nimi:** *väikesed kodumajapidamisseadmed*
    - **Klass:** *125*

1. Valige toimingupaanil nupp **Salvesta**.

## <a name="additional-resources"></a>Lisaressursid

- [Riikliku autoveose klassifikatsiooni (NMFC) koodid](nmfc-codes.md)
- [Veokirja loomine](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
