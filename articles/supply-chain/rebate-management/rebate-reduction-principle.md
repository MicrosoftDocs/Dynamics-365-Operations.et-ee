---
title: Tagasimakse vähendamise põhimõtted
description: Selles teemas kirjeldatakse, kuidas vähendamise põhimõtteid seadistada. Vähendamise põhimõtted kontrollivad käitumist, kui samale kaubale või kandele rakenduvad mitu tagasimakset.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 5a8bbfaff05b665cb85e9166cfc76363c4aedb64
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919839"
---
# <a name="rebate-reduction-principles"></a>Tagasimakse vähendamise põhimõtted

[!include [banner](../includes/banner.md)]

Saate grupeerida Tagasimaksehalduse tehinguid *vähendamispõhimõtetesse*, et vähendada muid kaubaga seotud sätteid ja/või vähendada tagasimakse arvutuste tulemuseks tulenevaid väärtusi. Pärast tagasimakse vähendamise põhimõtete kehtestamist saate need soovi korral omistada oma tagasimakse haldamise tehingute ridadele.

Tagasimakse vähendamise reeglid kehtivad ainult siis, kui tagasimaksete tehingud kattuvad. Seetõttu võivad nad anda mitu tagasimakset olukorras, kus mitu tagasimakset pole võlgu.

## <a name="manage-rebate-reduction-principles"></a>Tagasimakse vähendamise põhimõtete haldamine

Tagasimakse vähendamise põhimõtetega töötamiseks minge asukohta **Tagasimaksehaldus \> Seadistamine \> Tagasimakse vähendamise põhimõtted**. Seejärel toimingupaani nuppude abil saate vähendamise põhimõtteid lisada ja eemaldada vastavalt vajadusele. Seadke igal põhimõtte väljad nii, nagu kirjeldatud järgmises tabelis.

| Field | Kirjeldus |
|---|---|
| Tagasimakse vähendamise põhimõte | Sisestage tagasimakse vähendamise põhimõtte kordumatu nimi. |
| Kirjeldus | Sisestage tagasimakse vähendamise põhimõtte kirjeldus. |
| Vähendamise rakendamine | Valige see märkeruut, et kohaldada vähendamise alust tagasimaksetele, mis kuuluvad selle tagasimakse vähendamise põhimõttele. |
| Vähendamise alus | Kui valisite märkeruudu **Vähenda**, valige vähendamise alus (*Eraldis*, *Tagasimaksed* või *Mõlemad*). Kui valite *mõlemad* ja nii eraldis kui ka tagasimakse on sisestatud eelmise tehingu jaoks, rakendatakse ainult tagasimakse. |
| Välista vähendamisest | Kui see ruut on märgitud, jäetakse sellele tagasimakse vähendamise põhimõttele kuuluvad sätted ja tagasimaksed järgmistest vähendamistest välja. Välja **Vähendamine alus** säte ei kehti sellele sättele. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Tagasimakse vähendamise põhimõtte seadistuste näited

Järgmises tabelis on toodud mõned tüüpilised näited tagasimakse vähendamise põhimõtte seadistustest. Iga tagasimakse vähendamise põhimõtte puhul kirjeldab välja **Kirjeldus** väärtus tagasimakse vähendamise põhimõtte eesmärki.

| Tagasimakse vähendamise põhimõte | Kirjeldus | Vähendamise rakendamine | Vähendamise alus | Välista vähendamisest |
|---|---|---|---|---|
| Edasi lükatud | Vähenda tagasimakset | Jah | Mõlemad | Ei |
| V.a | Välista tagasimakse | Jah | Tagasimakse | Jah |
| Mitu | Mitu tagasimakset | Jah | Mõlemad | Jah |
| None | Ainult eraldis ja tagasimakse | Ei | Mõlemad | Jah |
| Ettevalmistus | Ainult ettevalmistus | Jah | Ettevalmistus | Ei |
| Tagasimakse | Ainult tagasimakse | Jah | Tagasimakse | Jah |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Tagasimakse vähendamise põhimõtte kalkulatsioonide näited

Teil on müügitellimus, millel on üks müügitellimuse rida. Selle rea väärtus on $1000. Tellimusele rakenduvad järgmised tehingud.

- **Tehing 1:** 10 protsenti $1000-st
- **Tehing 2:** 15 protsenti $1,000-st
- **Tehing 3:** 20 protsenti $1,000-st
- **Tehing 4:** 25 protsenti $1,000-st

Töötlemisjärjestus on väga oluline. Tellimuse töötlus põhineb viisil, kuidas töötate, nagu on kirjeldatud teemaks [Tagasimaksete töötlemine, ülevaatamine ja sisestamine](process-review-post.md).

Näiteks järgmine tabel võtab tulemuse kokku, kui kasutate tellimust *1, 2, 3, 4* ja kui töötlete ainult eraldisi.

| Pakkumised | Kirjeldus ja sätted | Eraldise tulemus |
|---|---|---|
| 1 | <p>Klassifikatsioon ei kontrolli muid vähendamisi. Kontroll tehakse nii sätete kui ka tagasimaksete puhul.</p><ul><li>**Rakenda vähendus:** *Ei*</li><li>**Vähendamise alus:** *Mõlemad*</li><li>**Välista vähendamisest:** *Ei*</li></ul> | $1000 × 10% = $100 |
| 2 | <p>Klassifikatsioon kontrollib muid vähendamisi, kuid on märgitud nii, et seda ennast eiratakse. Kontroll tehakse ainult tagasimaksete puhul.</p><ul><li>**Rakenda vähendus:** *Jah*</li><li>**Vähendamise alus:** *Tagasimakse*</li><li>**Välista vähendamisest:** *Jah*</li></ul> | $1,000 × 15% = $150 |
| 3 | <p>Klassifikatsioon kontrollib muid tehingute vähendamisi. Kontroll tehakse nii sätete kui ka tagasimaksete puhul.</p><ul><li>**Rakenda vähendus:** *Jah*</li><li>**Vähendamise alus:** *Mõlemad*</li><li>**Välista vähendamisest:** *Ei*</li></ul> | ($1000 – tehing 1) × 20% = $180 |
| 4 | <p>Klassifikatsioon kontrollib muid tehingute vähendamisi. Kontroll tehakse nii sätete kui ka tagasimaksete puhul.</p><ul><li>**Rakenda vähendus:** *Jah*</li><li>**Vähendamise alus:** *Mõlemad*</li><li>**Välista vähendamisest:** *Ei*</li></ul> | (1000 $ – tehing 1 – tehing 3) × 25% = $180 |

Järgnev tabel näitab mõningaid näiteid, kus eraldist töödeldakse erinevates tellimustes ja kus seetõttu saavutati erinevad kogusummad. Sätete hälve sõltub tellimusest, mille alusel süsteem tehinguid töötleb. On oluline mõista, kuidas töötlemistellimus mõjutab lõplikku tagasimakse summat.

| Jada | Kalkulatsioon |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Tehing 1:** $1000 × 10% = $100</li><li>**Tehing 2:** $1,000 × 15% = $150</li><li>**Tehing 3:** ($1000 – tehing 1) × 20% = $180</li><li>**Tehing 4:** (1000 $: tehing 1 – tehing 2) × 25% = $180</li><li>**Kogu eraldis:** $610</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Tehing 4:** $1000 x 25% = $250</li><li>**Tehing 3:** ($1,000 – tehing 4) × 20% = $150</li><li>**Tehing 2:** $1,000 x 15% = $150</li><li>**Tehing 1:** $1,000 x 10% = $100</li><li>**Kogu eraldis:** $650</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Tehing 3:** $1,000 x 20% = $200</li><li>**Tehing 2:** $1,000 x 15% = $150</li><li>**Tehing 1:** $1,000 x 10% = $100</li><li>**Tehing 4:** (1,000 $: tehing 3 – tehing 1) × 25% = $175</li><li>**Kogu eraldis:** $625</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Tehing 2:** $1,000 × 15% = $150</li><li>**Tehing 4:** $1,000 × 25% = $250</li><li>**Tehing 1:** $1000 × 10% = $100</li><li>**Tehing 3:** (1,000 $: tehing 4 – tehing 1) × 20% = $130</li><li>**Kogu eraldis:** $630</li></ul> |
