---
title: Veose täiendustellimuse loomine
description: Selles teemas selgitatakse, kuidas luua veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse.
author: mkirknel
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f426dbf00eace23da2f26eb50dd9675fe22ed445
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914767"
---
# <a name="create-a-consignment-replenishment-order"></a>Veose täiendustellimuse loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas selgitatakse, kuidas luua veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse. Samuti näitab see, kuidas registreerida toodete sissetulekut, et veose varud oleksid registreeritud hankijale kuuluva vaba kaubavaruna. Selle protseduuri viib tavaliselt läbi hankespetsialist. Saate seda juhendit kasutada demoettevõtte USMF andmetega. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

## <a name="create-a-consignment-replenishment-order"></a>Veose täiendustellimuse loomine
1. Navigeerimispaanil avage **Moodulid > Hanked > Veos > Veose täiendustellimused**.
2. Valige suvand **Uus**.
3. Väljal **Hankija konto** valige hankija **US-104** (peate valima hankija, mis on lehel **varude omanikud** omanikuna registreeritud). 
4. Valige nupp **OK**.
5. Valige **Lisa rida**.
6. Väljale **Kaubakood** sisestage `M9211CI` (peate valima kauba, mis on seadistatud veose varude jaoks).
7. Sisestage arv väljale **Kogus**.
8. Väljale **Nõutud tarnekuupäev** sisestage kuupäev. MRP moodul kasutab nõutud ja kinnitatud kuupäevi kaupade eeldatava saabumise jaoks.  
9. Väljale **Kinnitatud tarnekuupäev** sisestage kuupäev.
10. Laiendage jaotist **Rea üksikasjad**.
11. Valige vahekaart **Varude dimensioonid**.
12. Värskendage lehte omaniku kuvamiseks väljal **Varude dimensioonide omanik**. Hankija US-104 on nüüd omanikuna registreeritud.  

## <a name="check-the-inventory-transaction-status"></a>Kontrollige kande kuupäeva olekut
1. Valige **Laoseis**.
2. Valige **Kanded**.
3. Pange tähele, et soovitud rea väli **Sissetulek** on seadistatud olekule **Tellitud**.  
4. Sulgege leht.

## <a name="receive-items"></a>Võta kaubad vastu
1. Valige **Toote sissetulek**.
2. Väljale **Väline toote sissetulek** sisestage väärtus.
3. Väljale **Kogus** sisestage arv, mis on väiksem kui arv, mida seal kuvatakse. 
4. Valige nupp **OK**.

## <a name="check-the-on-hand-inventory"></a>Kontrollige vaba kaubavaru
1. Valige **Laoseis**.
2. Valige **Varu**.
3. Valige **Ülevaade**. Kaubad, mis on saadud hankijale kuuluva veose kaubavaruna, on vaba varuna saadaval. Veose täiendustellimuse järelejäänud kogus kuvatakse väljal **Tellitud kokku**.  
4. Sulgege leht.

