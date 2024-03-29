---
title: Veose täiendustellimuse loomine
description: See artikkel selgitab, kuidas luua saadetise varude täiendamise tellimus, kus saate jälgida hankija eeldatavat tarnet veose varudesse.
author: yufeihuang
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a1d0a7d322b17d3d80dd9fade2b037dd148d9f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859369"
---
# <a name="create-a-consignment-replenishment-order"></a>Veose täiendustellimuse loomine

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas luua saadetise varude täiendamise tellimus, kus saate jälgida hankija eeldatavat tarnet veose varudesse. Samuti näitab see, kuidas registreerida toodete sissetulekut, et veose varud oleksid registreeritud hankijale kuuluva vaba kaubavaruna. Selle protseduuri viib tavaliselt läbi hankespetsialist. Saate seda juhendit kasutada demoettevõtte USMF andmetega. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]