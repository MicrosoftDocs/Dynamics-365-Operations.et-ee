---
title: Rendigrupi loomine
description: See artikkel selgitab, kuidas seadistada rendigruppe. Rendigrupid vajalikud uute rendikirjete loomiseks.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd1a6f61346233bf205657917c65fccd82167f7f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895018"
---
# <a name="create-a-lease-group"></a>Rendigrupi loomine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada rendigruppe. Rendigrupid vajalikud uute rendikirjete loomiseks. Rendi raamatud on seostatud iga rendigrupiga. Rendi raamatud määravad vaikimisi raamatud, mis tuleb iga rendikirje jaoks luua. Saate määrata rendigrupile konkreetsed kontod lehel **Rendikirje sisestamise parameetrid**.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Rendi raamatu loomine ja rendigrupi lisamine

1. Avage **Vara rentimine \> Seadistus \> Rendigrupid**.
2. Rendigrupi lisamiseks valige toimingupaanilt suvand **Uus**. Ruudustikku lisatakse rida.
3. Sisestage välja **Rendigrupp** uuele reale väärtus.
4. Sisestage väärtus väljal **Kirjeldus**.

Teie sisestatud teave lisatakse väljale **Rendigrupp** lehel **Rendikirje lisamine**.

## <a name="associate-a-book-with-a-lease-group"></a>Raamatu seostamine rendigrupiga

Pärast rendigruppide loomist saate määrata igale grupile raamatu. Rendikirje loomisel ja selle rendigrupile määramisel loob süsteem iga raamatu jaoks graafikute kogumi, mis seostatakse selle rendigrupiga.

> [!NOTE]
> Enne rendigrupile määramist tuleb raamatud häälestada.

1. Avage **Vara rentimine \> Seadistus \> Rendigrupp**.
2. Valige rendigrupp ja valige seejärel **Raamatud**.
3. Valige **Uus** ja valige seejärel väljal **Raamatu tüüp** rendigrupile määramiseks raamat. Kui renti tuleb arvestada mitmel erineval viisil, saate määrata rendigrupile mitu raamatut.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
