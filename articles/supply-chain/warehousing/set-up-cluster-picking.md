---
title: Kogumi komplekteerimise seadistamine
description: Selles teemas kirjeldatakse, kuidas seadistada klastri komplekteerimist ja kuidas rakendada klastri komplekteerimisega kauba kinnitamist.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2ec0890963b2b01407acac8003453faf370894b4
ms.openlocfilehash: 1c23421ddfda8c5f6fa27a31831a00ead6094db9
ms.contentlocale: et-ee
ms.lasthandoff: 04/11/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a>Kogumi komplekteerimise seadistamine

Selles teemas kirjeldatakse, kuidas võimaldada töötajatel kasutada oma mobiilseid seameid komplekteerimistöö grupeerimiseks kogumitesse, et nad saaksid mitme töötellimuse puhul komplekteerida kaupu samal ajal ühest kohast. Seda nimetatakse *kogumi komplekteerimiseks*.

## <a name="about-cluster-picking"></a>Teave kogumi komplekteerimise kohta

Kui töötellimused on lattu vabastatud, saab töötaja määrata tellimused mobiilse seadme abil kogumisse. Kogum korraldab töötaja jaoks komplekteerimistöö. Kui töötellimus on määratud kogumisse, peab töötaja tellimuse komplekteerimistöö tegemiseks kasutama kogumi komplekteerimist. Töötaja ei saa kasutada muid komplekteerimisviise. Kui töötellimus on kogumisse ekslikult määratud, peab töötaja kogumi lõhkuma ja selle uuesti looma.

Vajaduse korral saab töötaja edastada kogumi edasi teisele töötajale. Sel juhul muutub kogumi olekuks Edastatud. Kui töötaja kasutab komplekteerimis- ja mahapanekutöö lõpuleviimise näitamiseks mobiilset seadet, tuleb saadetis või koorem kinnitada rakenduse Dynamics 365 for Finance and Operations kliendis.

## <a name="set-up-cluster-picking"></a>Kogumi komplekteerimise seadistamine

Kogumi komplekteerimise lubamiseks peate tegema järgmised seadistused.

-   **Kogumiprofiilid** – saate määrata kogumi ID automaatse loomise, kasutatavate positsioonide arvu, kogumite lõhkumise ning komplekteerimistöö järjestamise ja kinnitamise viisi.

-   **Töömallid** – saate määrata, kuidas luua komplekteerimistöö kogumi komplekteerimiseks.

-   **Asukoha korraldus** – saate määrata, kust kaubad komplekteerida ja kuhu need maha panna.

-   **Mobiilse seadme menüü-üksused** – saate konfigureerida mobiilse seadme menüü-üksuse kasutama olemasolevat tööd, mida juhitakse kogumi komplekteerimisega. Seejärel peate menüü-üksuse lisama mobiilse seadme menüüsse, et see kuvataks mobiilses seadmes.

-   **Laohalduse parameetrid**– saate määrata numbriseeria, mida kasutatakse, kui soovite kogumitele identifikaatorid luua.

## <a name="set-up-a-cluster-profile"></a>Kogumi profiili seadistamine

Kogumi profiili seadistamiseks toimige järgmiselt.

1.  Valige **Laohaldus** \> **Seadistamine** \> **Mobiilne seade** \> **Kogumiprofiilid**.

2.  Klõpsake uue profiili loomiseks suvandit **Uus**.

3.  Klõpsake suvandit **Kogumi loomine** ja valikus **Kogumi sortimine** klõpsake suvandit **Uus** kogumi sortimiskriteeriumide seadistamiseks. Sortimiskriteeriumid määravad järjestuse, milles töötaja teeb komplekteerimistööd. Saate lisada nii palju kriteeriume kui vaja.

4.  Sisestage väljale **Järjekorranumber** number, mis määratleb järjestuse, milles sortimiskriteeriume töödeldakse.

5.  Valige väljal **Välja nimi** väli, mis määratleb sortimise. Näiteks kui valite välja **WMSLocationId**, sorditakse töö asukoha järgi.

6.  Väljal **Sortimine** tehke üks järgmistest valikutest.

| **Suvand**     | **Kirjeldus**                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kasvavas järjestuses**  | Komplekteerimistööd järjestatakse sortimiskriteeriumite alusel kasvavalt. Näiteks kui kasutate sortimiskriteeriumina välja **WMSLocationId** ja teie asukoha ID-d on 1, 2, 3 ja 4, saate esmalt komplekteerida asukohast 4. |
| **Kahanevas järjestuses** | Komplekteerimistööd järjestatakse sortimiskriteeriumite alusel kahanevalt. Näiteks kui kasutate sortimiskriteeriumina välja **WMSLocationId** ja teie asukoha ID-d on 1, 2, 3 ja 4, saate esmalt komplekteerida asukohast 1. |

## <a name="item-confirmation"></a>Kauba kinnitamine

Kogumi komplekteerimise rakendamiseks on kinnitamine väga oluline, et kontrollida kogumitesse lisatud kaupu. Kogumi komplekteerimisprotsessi ajal saab kaupu kogumi komplekteerimisel kontrollida. Seadistus põhineb toote vöötkoodi seadistusel.

### <a name="set-up-item-verification-with-cluster-picking"></a>Kauba kontrollimise seadistamine kogumi komplekteerimisega

1.  Avage mobiilse seadme menüüelemendis seadistusvorm töö kinnitamiseks: **Laohaldus** \> **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüüelemendid**.

2.  Avage mobiilse seadme menüüelemendist jaotis **Töö kinnituse häälestus**. Suvand **Toote kinnitus** võimaldab iga varude üksust mobiilsel seadmel skannides kontrollida.

