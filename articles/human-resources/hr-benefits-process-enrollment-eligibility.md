---
title: Registreerimise sobivuse töötlemine
description: Selles artiklis selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 69ea23e4051a6975a5892cd027777c5a88472509
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112253"
---
# <a name="process-enrollment-eligibility"></a>Registreerimise sobivuse töötlemine

Selles artiklis selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.

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

Selles artiklis selgitatakse, kuidas kuvada sobivuse töötlemise tulemusi.

1.  Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Protsessi tulemused**.

2.  Vormil **Protsessi tulemused** on määratud järgmised väljad.

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