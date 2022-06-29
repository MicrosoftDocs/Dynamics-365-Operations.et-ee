---
title: Kogumi komplekteerimise häälestamine
description: See artikkel kirjeldab, kuidas seadistada kogumi komplekteerimist ja rakendada kauba kinnitust kogumi komplekteerimisega.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ec3de073def2ff63af3c04b5696cbcec4f09948
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014716"
---
# <a name="set-up-cluster-picking"></a>Kogumi komplekteerimise häälestamine

[!include[banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas lubada töötajatel kasutada oma mobiilseid seadmeid komplekteerimistöö grupeerimiseks klastriteks, nii et nad saavad komplekteeritud kaupu mitmest asukohast korraga mitme töötellimuse jaoks. Seda nimetatakse *kogumi komplekteerimiseks*.

## <a name="about-cluster-picking"></a>Teave kogumi komplekteerimise kohta

Kui töötellimused on lattu vabastatud, saab töötaja määrata tellimused mobiilse seadme abil kogumisse. Kogum korraldab töötaja jaoks komplekteerimistöö. Kui töötellimus on määratud kogumisse, peab töötaja tellimuse komplekteerimistöö tegemiseks kasutama kogumi komplekteerimist. Töötaja ei saa kasutada muid komplekteerimisviise. Kui töötellimus on kogumisse ekslikult määratud, peab töötaja kogumi lõhkuma ja selle uuesti looma.

Vajaduse korral saab töötaja edastada kogumi edasi teisele töötajale. Sel juhul muutub kogumi olekuks Edastatud. Kui töötaja kasutab komplekteerimis- ja mahapanekutöö lõpuleviimise näitamiseks mobiilset seadet, tuleb saadetis või koorem kinnitada kliendis.

## <a name="enable-cluster-picking"></a>Kogumi komplekteerimise lubamine

Kogumi komplekteerimise lubamiseks peate tegema järgmised seadistused.

- **Kogumiprofiilid** – saate määrata kogumi ID automaatse loomise, kasutatavate positsioonide arvu, kogumite lõhkumise ning komplekteerimistöö järjestamise ja kinnitamise viisi.

- **Töömallid** – saate määrata, kuidas luua komplekteerimistöö kogumi komplekteerimiseks.

- **Asukoha korraldus** – saate määrata, kust kaubad komplekteerida ja kuhu need maha panna.

- **Mobiilse seadme menüü-üksused** – saate konfigureerida mobiilse seadme menüü-üksuse kasutama olemasolevat tööd, mida juhitakse kogumi komplekteerimisega. Seejärel peate menüü-üksuse lisama mobiilse seadme menüüsse, et see kuvataks mobiilses seadmes.

- **Laohalduse parameetrid**– saate määrata numbriseeria, mida kasutatakse, kui soovite kogumitele identifikaatorid luua.

## <a name="set-up-a-cluster-profile"></a>Kogumi profiili seadistamine

Kogumi profiili seadistamiseks toimige järgmiselt.

1. Valige **Laohaldus** \> **Seadistamine** \> **Mobiilne seade** \> **Kogumiprofiilid**.

1. Klõpsake uue profiili loomiseks suvandit **Uus**.

1. Klõpsake suvandit **Kogumi loomine** ja valikus **Kogumi sortimine** klõpsake suvandit **Uus** kogumi sortimiskriteeriumide seadistamiseks. Sortimiskriteeriumid määravad järjestuse, milles töötaja teeb komplekteerimistööd. Saate lisada nii palju kriteeriume kui vaja.

1. Sisestage väljale **Järjekorranumber** number, mis määratleb järjestuse, milles sortimiskriteeriume töödeldakse.

1. Valige väljal **Välja nimi** väli, mis määratleb sortimise. Näiteks kui valite välja **WMSLocationId**, sorditakse töö asukoha järgi.

1. Väljal **Sortimine** tehke üks järgmistest valikutest.

| **Suvand**     | **Kirjeldus**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasvavas järjestuses**  | Komplekteerimistööd järjestatakse sortimiskriteeriumite alusel kasvavalt. Näiteks kui kasutate sortimiskriteeriumina välja **WMSLocationId** ja teie asukoha ID-d on 1, 2, 3 ja 4, saate esmalt komplekteerida asukohast 4. |
| **Kahanevas järjestuses** | Komplekteerimistööd järjestatakse sortimiskriteeriumite alusel kahanevalt. Näiteks kui kasutate sortimiskriteeriumina välja **WMSLocationId** ja teie asukoha ID-d on 1, 2, 3 ja 4, saate esmalt komplekteerida asukohast 1. |

## <a name="item-confirmation"></a>Kauba kinnitamine

Kogumi komplekteerimise rakendamiseks on kinnitamine väga oluline, et kontrollida kogumitesse lisatud kaupu. Kogumi komplekteerimisprotsessi ajal saab kaupu kogumi komplekteerimisel kontrollida. Seadistus põhineb toote vöötkoodi seadistusel.

### <a name="set-up-item-verification-with-cluster-picking"></a>Kauba kontrollimise seadistamine kogumi komplekteerimisega

1. Minge laohalduse **häälestuse** > **mobiilse** > **seadme** > **mobiilseadme menüü-üksustesse**.
1. Valige loendipaanil menüükäsk, mida soovite seadistada.
1. Tegevuspaanil valige töö **kinnituse häälestus**.
1. Tehke üks järgmistest toiming:
    - Kui seadistatav töötüübi kohta **on rida** juba olemas, valige see ja klõpsake siis tegevuspaanil **nuppu** Redigeeri.
    - Kui sobivat rida pole, valige tegevuspaanil **väärtus** Uus ja määrake tüübiks **Töö**.
1. Märkige uue **või** valitud rea puhul ruut Toote kinnitus. See võimaldab töötajatel mobiilse seadme abil kõiki laovarusid kontrollida.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]