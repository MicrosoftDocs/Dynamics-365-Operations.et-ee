---
title: Registreerimise sobivuse töötlemine
description: Selles teemas selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8997cf24bf24097e46a05acffef8b3839056c57
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067625"
---
# <a name="process-enrollment-eligibility"></a>Registreerimise sobivuse töötlemine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.

1. Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Registreerimise sobivuse töötlemine**.

2. Dialoogiaknas **Soodustuse registreerimise sobivuse protsessi käitamine** määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Registreerimisperiood** | Registreerimisperiood, mille jaoks registreerimise sobilikkust töödelda. |
   | **Juriidiline isik** | Juriidiline isik, mille jaoks registreerimise sobilikkust töödelda. |
   | **Töötaja** | Töötaja, kelle jaoks registreerimise sobilikkust töödelda. Kui jätate selle välja tühjaks, töödeldakse registreerimise sobilikkust kõigi töötajate puhul. |
   | **Soodustusplaan** | Soodustuse plaan, mille jaoks registreerimise sobilikkust töödelda.

3. Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.

   1. Sisestage teavet protsessi kohta.

   2. Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.

   3. Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.

   4. Valige nupp **OK**. Protsess töötab teie määratud parameetritega.

4. Valige nupp **OK**.

## <a name="view-process-results"></a>Protsessi tulemuste kuvamine

Selles teemas selgitatakse, kuidas kuvada sobivuse töötlemise tulemusi.

1.  Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Protsessi tulemused**.

2.  Lehel **Protsessi tulemused** on määratud järgmised väljad.

   | Field | Kirjeldus |
   | --- | --- |
   | **Protsessi ID** | Töötaja, juriidilise isiku ja protsessi käituse kombinatsiooni ainuidentifikaator. |
   | **Protsessi tüüp** | See tuvastab käivitatud protsessi. Näide: registreerimine. |
   | **Ajatempel** | Sobivuse töötlemise kellaaeg. |
   | **Juriidiline isik** | Registreerimise käigus määratud juriidiline isik. |
   | **Töötaja** | Töödeldav töötaja. |
   | **Plaan | See soodustusplaan, mille jaoks registreeriti. |
   | **Sobivusreegel** | Töödeldud sobivusreegel. Kui enne sobivuse töötlemist ilmnes tõrge, on see tühi. Näiteks: kui töötaja jaoks pole kompensatsiooni määratud, siis sobivuse töötlemist ei käivitata ja see väli jäetakse tühjaks. |
   | **Tulemi olek** | See on Sobilik või Sobimatu. Tulemuse olek on Sobimatu, kui töötaja ei vastanud sobivusreegli kriteeriumidele, kui töötaja kohta puudub nõutav teave (nt maksesagedus või põhipalk) või kui puudub teave soodustusplaani kohta, mis takistab töötajate registreerimist. |
   | **Tulemusteade** | Näitab, miks töötaja on soodustusplaani jaoks sobimatu või kui sobivusreegel on edastatud. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
