---
title: Tootmise sisestamine
description: "Selles artiklis antakse teavet eri tüüpi sisestuste kohta tootmisprotsessis."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemGroup, ProjCategory, WrkCtrResourceGroup, WrkCtrTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54591
ms.assetid: 0917fe64-f643-46ae-98ff-5013b266a067
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 78c30ba046441ab5e7fbf21bab81407acc59646f
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="production-posting"></a>Tootmise sisestamine

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet eri tüüpi sisestuste kohta tootmisprotsessis.

Tootmise sisestamistegevused järgivad tootmisprotsesse, mida kirjeldatakse allolevates jaotistes.

## <a name="material-consumption"></a>Materjali tarbimine
Materjalid registreeritakse tootmisel tarbituteks, kui sisestatakse tootmise komplekteerimise tööleht. See protsess loob väljaminekukanded, mis arvavad maha vaba kaubavaru. Tootmise parameetrites saate määrata, kas töös olevate (lõpetamata toodang \[WIP\]) toormaterjalide väärtus tuleb pearaamatusse sisestada. Lõpetamata (WIP) toormaterjalide väärtus sisestatakse siis sihtotstarbelisele komplekteerimislehe kontole ja sihtotstarbelisele komplekteerimislehe vastaskontole.

## <a name="time-consumption"></a>ajatarbimine.
Aega, mille töötajad tootmistöödele kulutavad, salvestatakse protsessikaardi töölehel või töökaardi töölehel. Kui need töölehed sisestatakse, töödeldakse pearaamatut, mis sisestab lõpetamata (WIP) ressursside sihtotatarbelisele kontole. See sisestus näitab tootmistellimusele kulutatud aja väärtust. Kui tootmistellimus on registreeritud lõpetatuks, tasakaalustatakse WIP-kontod.

## <a name="reporting-finished-goods-and-error-quantities"></a>Lõpetatud kaupade ja vigaste koguste aruandlus
Kui tootmistellimus on lõpetatuks tunnistatud, värskendatakse lõpule viidud lõpetatud kaupade kogust varude halduses töölehe Teata lõpetamisest kaudu. Kui kasutate WIP-kontosid, mille saab seadistada tootmise parameetrites, tehakse pearaamatu tööleht vähendamaks WIP-kontosid ja suurendamaks lõpetatud kaupade varusid. Tööleht kasutab standardhinda, mis on tootele määratud.

## <a name="ending-the-production-order"></a>Tootmistellimuse lõpetamine
Enne tootmistellimuse lõpetamist arvutatakse toodetud koguse tegelikud kulud. Kõik hinnangulised materjali- töö ja üldkulud tühistatakse ja asendatakse tegeliku kuluga. Lõpetatud kauba üleüldine kulu debiteeritakse lao kontolt Sissetulekud ja krediteeritakse kontole Väljaminekud. Kui märgite kuluarvutuse käivitamisel ruudu **Lõpeta töö**, muudetakse tootmistellimuse olek sättele **Lõpetatud**. See olek takistab lisakulude tahtmatut sisestamist lõpetatud tootmistellimusele. Saate täpsustada, et lõpule viidud kogustest aru andmise ajal teavitatud vigaste koguste väärtus tuleb eraldada lõpule viidud koguste puhul õigetest kogustest. Teise võimalusena saate määrata, et vigaste koguste väärtus tuleb sisestada sihtotstarbelisele praagikontole.

## <a name="controlling-the-level-of-ledger-posting"></a>Pearaamatusse sisestamise taseme juhtimine
Jaotises **Tootmise juhtimise parameetrid** saate kasutada välja **Pearaamatusse sisestamine**, et määrata pearaamatusse sisestamise taseme tootmisprotsesside puhul. Saadaval on järgmised väärtused:

-   **Kaup ja ressursid** – kasutage pearaamatuontosid, mis on seadistatud toormaterjalide ja lõpetatud kaupade kaubagruppides. Ajakulu WIP võetakse protsessi operatsioonide ressursist või ressursigrupist.
-   **Kaup ja kategooria** – kasutage pearaamatuontosid, mis on seadistatud toormaterjalide ja lõpetatud kaupade kaubagruppides. Ajakulu WIP võetakse kulukategooriatest, mis on seostatud protsessi operatsioonidega.
-   **Tootmisgrupid** – kasutage pearaamatukontosid, mis on seadistatud nii materjali- kui ka ajakulu tootmisgruppides. Tootmisgrupid on seostatud välastatud toodetega ja kopeeritud tootmistellimustele nende tellimuste loomisel. Tootmistellimuste sisestamine järgib tootmisgruppe, mis on seostatud tootmistellimusega.

**Märkus.** Kui lõpetatud kauba kulu arvutamisel kasutati standardset meetodit, siis kajastavad seda lõppkanded. Kui tegelike kulude ja standardse arvutusmeetodi tulemused erinevad, siis sisestatakse see erinevus tulu või kulu kontole.




