---
title: Kaubavajaduse loomine teenustellimusest
description: Kui teil on vaja teenusetellimuse jaoks konkreetseid kaupu reserveerida, saate selle jaoks luua laokauba vajadused.
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
ms.openlocfilehash: e76b0c636470a89ba2091363efe2f34eb3d58f88
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="create-item-requirements-for-service-orders"></a>Kaubavajaduse loomine teenustellimusest 

[!include [banner](../includes/banner.md)]


Saate luua hooldustellimuse klientidele osutatavate teenuste jälgimiseks ja haldamiseks. Kui teil on vaja teenusetellimuse jaoks konkreetseid kaupu reserveerida, saate selle jaoks luua laokauba vajadused. Kaubavajadust saab laost kohe tarbida või see võib algatada kauba tootmistellimuse.

Kasutades kaubakannete asemel kaubavajadusi, saate planeerida tarne just selleks ajaks, mil kaupa tegelikult kasutatakse, luua ostutellimuse, kaasata kauba kaubandusleppe raamistikku ja kaasata kaubavajaduse tootmisplaanidesse.

Teenusetellimuste kaubavajadusi töödeldakse projekti kaudu. Teenusetellimusele kaubavajaduse loomiseks peab olema projektile määratud teenusetellimus. Pärast hooldustellimusele kaubavajaduse loomist saate valitud projekti kaubavajadust vormil **Projektid** vaadata.

## <a name="create-an-item-requirement-for-a-service-order"></a>Teenustellimusele kaubavajaduse loomine

1.  Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.

2.  Valige teenusetellimus, millele soovite kaubavajaduse luua.

3.  Klõpsake **toimingupaani** vahekaardil **Lähetus** valikut **Kaubavajadus**.

4.  Sisestage vormil **Kaubavajadused** nõutava kauba teave. Konkreetsete väljade kohta lisateabe saamiseks vt jaotist [Kaubavajadused (vorm)](https://technet.microsoft.com/en-us/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Teenusleppele kaubavajaduse loomine

1.  Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.

2.  Avage teenuselepe, millele soovite kaubavajaduse luua.

3.  Uue rea loomiseks klõpsake kiirkaardi **Read** valikut **Lisa**.

4.  Valige **Kaup** väljal **Kande tüüp**.

5.  Valige **Kaubavajadus** väljal **Kauba seadistus**.

6.  Valige väljal **Kaubakood** kaup, mis on hooldusleppe jaoks vajalik.

7.  Valige kiirkaardi **Rea üksikasjad** vahekaardi **Toote dimensioonid** väljal **Laoala** kauba laoala.

8.  Lepperealt hooldustellimuse loomiseks kiirkaardil **Read** klõpsake valikut **Hooldustellimuste loomine** ja sisestage seejärel asjakohane teave vormi **Hooldustellimuste loomine**. 


## <a name="see-also"></a>Vt ka

[Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)

  


