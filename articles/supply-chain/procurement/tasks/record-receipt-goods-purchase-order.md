---
title: Kaupade vastuvõtu registreerimine ostutellimusel
description: See artikkel selgitab, kuidas kirjendada kaupade sissetulekut otse ostutellimusele.
author: GalynaFedorova
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22baf6d0f6db04b3c6ce3c09ee8cb286e9a1e590
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882456"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Kaupade vastuvõtu registreerimine ostutellimusel

[!include [banner](../../includes/banner.md)]

See artikkel selgitab, kuidas kirjendada kaupade sissetulekut otse ostutellimusele. Võimalik on registreerida toote sissetulek ka laos ja siis hiljem kirjendada ostutellimusel. Selle toimingu teeb tavaliselt ostuagent või ostureskontro koordinaator. Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul. Näites on toimingud lihtsa ostutellimuse koostamiseks, et saaksite esitada protseduuri tegevusjuhisena. Kui kasutaksite protseduuri oma andmetega, tuleks alustada alamülesandest **Kaupade vastuvõtu registreerimine**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Uue ostutellimuse koostamine kaupade vastuvõtmiseks
1. Minge **navigeerimispaanile > Moodulid > Hange ja hankimine > Ostutellimused > Kõik ostutellimused**.
2. Valige suvand **Uus**.
3. Väljale **Tarnija konto** sisestage `US-101`.
4. Valige nupp **OK**.
5. Väljale **Kauba kood** sisestage `M0001`.
6. Väljale **Kogus** sisestage `5`.
7. Valige toimingupaanil **Ostmine**.
8. Valige **Kinnita**.

## <a name="record-receipt-of-goods"></a>Kaupade vastuvõtu salvestamine
1. Valige toimingupaanil **Vastuvõtmine**.
2. **Valige toote** sissetulek. **Koguse** väli võimaldab teha erinevaid valikuid koguse kohta, mida soovite vastu võtta. Näiteks kui kogus on eelnevalt laos registreeritud, võite teha valiku **Registreeritud kogus**. Selle näite puhul kasutage väärtust **Tellitud kogus**.
3. Laiendage jaotist **Ülevaade**.
4. **Sisestage suvaline väärtus väljale Toote sissetulek.** Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.  
5. Laiendage jaotist **Read**.
6. Määrake **Koguse** väärtuseks 4. Siin saate määrata käsitsi koguse, mida iga tellimuse rea puhul vastu võetakse.  
7. Valige nupp **OK**. Kaup on nüüd ostutellimusel vastuvõetuks registreeritud ja seda kajastava dokumendina on loodud toote sissetuleku tööleht. Saate kasutada toimingut Toote sissetulek ostutellimuse juurde loodud töölehtede ülevaatamiseks, et näha, mis millal vastu võeti.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]