---
title: Hooldustellimuste loomine automaatselt
description: "Hooldustellimusi saate luua nii ühe kui ka mitme hooldusleppe jaoks."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c39e5b5eb79859b0a76c357edfee953ca90c0c4a
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-automatically"></a>Hooldustellimuste loomine automaatselt    

[!include [banner](../includes/banner.md)]


Hooldustellimusi saate luua nii ühe kui ka mitme hooldusleppe jaoks. Loodud hooldustellimusi saate vaadata vormil **Hooldustellimused**.

Hooldustellimusi luuakse ainult hooldusleppe kehtivusperioodi ajaks. Kui osa vormil **Hooldustellimuste loomine** määratud intervallist on hooldusleppe alguskuupäevast varasem või lõppkuupäevast hilisem, luuakse hooldustellimused ainult hooldusleppe kuupäevadesse jääva intervalliosa jaoks.

Kui loote hooldustellimused hooldusleppe realt käsitsi või automaatselt, peab hoolduslepe jääma rea algus- ja lõppkuupäevade ajaintervalli piiresse, kui te ei määratle real lõppkuupäeva.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Teenustellimuste automaatne loomine ühe teenusleppe jaoks

1.  Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.

2.  Valige soovitud teenusleping.

3.  Klõpsake vahekaarti **Tarnimine** ja seejärel valikut **Planeeritud hooldustellimused**.

4.  Hooldusperioodi määratlemiseks sisestage soovitud kuupäevad väljadele **Kuupäevast** ja **Kuupäevani**.

5.  Loodud hooldustellimuste loendi kuvamiseks märkige ruut **Näita teabelogi**.

6.  Valige kandetüübid väljagrupis **Kaasa kandetüübid**. Kandetüübid tähistavad teenusleppes loodavaid ridu ning iga valitud kandetüübi puhul luuakse mitu teenustellimust, sõltuvalt teenusleppe real määratud teenusintervallist.

7.  Puuduvate hooldustellimuste loomiseks pidevast hooldustellimuste sarjast märkige ruut **Pidev**.

8.  Klõpsake nupul **OK**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Teenustellimuste automaatne loomine mitme teenusleppe jaoks

1.  Klõpsake valikuid **Teeninduse haldus** \> **Perioodiline** \> **Hooldustellimused** \> **Hooldustellimuste loomine**.

2.  Hooldustellimuste loomisel kasutatavate kriteeriumite lisamiseks või kustutamiseks saate valikuid teha, klõpsates käsku **Vali**.

3.  Klõpsake nupul **OK**.

## <a name="see-also"></a>Vt ka

[Teenusetellimused](service-orders.md)

[Hooldustellimuste loomine automaatselt](auto-create-service-orders.md)

  


