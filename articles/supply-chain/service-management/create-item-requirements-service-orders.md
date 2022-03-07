---
title: Kaubavajaduse loomine hooldustellimuste jaoks
description: Selles teemas kirjeldatakse kauba nõuete loomist teenuse tellimuste jaoks.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75a05147883f1592b3a09e02e238661f6c20cf27
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7575287"
---
# <a name="create-item-requirements-for-service-orders"></a>Kaubavajaduse loomine hooldustellimuste jaoks

[!include [banner](../includes/banner.md)]

Saate luua hooldustellimuse klientidele osutatavate teenuste jälgimiseks ja haldamiseks. Kui teil on vaja teenusetellimuse jaoks konkreetseid kaupu reserveerida, saate selle jaoks luua laokauba vajadused. Kaubavajadust saab laost kohe tarbida või see võib algatada kauba tootmistellimuse.

Kasutades kaubakannete asemel kaubavajadusi, saate planeerida tarne just selleks ajaks, mil kaupa tegelikult kasutatakse, luua ostutellimuse, kaasata kauba kaubandusleppe raamistikku ja kaasata kaubavajaduse tootmisplaanidesse.

Teenusetellimuste kaubavajadusi töödeldakse projekti kaudu. Teenusetellimusele kaubavajaduse loomiseks peab olema projektile määratud teenusetellimus. Pärast hooldustellimusele kaubavajaduse loomist saate valitud projekti kaubavajadust vormil **Projektid** vaadata.

## <a name="create-an-item-requirement-for-a-service-order"></a>Teenustellimusele kaubavajaduse loomine

1. **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.
1. Valige teenusetellimus, millele soovite kaubavajaduse luua.
1. Klõpsake **Toimingupaani** vahekaardil **Lähetus** valikut **Kaubavajadus**.
1. Sisestage vormil **Kaubavajadused** nõutava kauba teave. Konkreetsete väljade kohta lisateabe saamiseks vt jaotist [Kaubavajadused (vorm)](https://technet.microsoft.com/library/aa552021\(v=ax.60\)).

## <a name="create-an-item-requirement-for-a-service-agreement"></a>Teenusleppele kaubavajaduse loomine

1. Valige **Teenusehaldus** \> **Üldine** \> **Hoolduslepped** \> **Hoolduslepped**.
1. Avage teenuselepe, millele soovite kaubavajaduse luua.
1. Tehke uue rea loomiseks kiirkaardil **Read** valik **Lisa**.
1. Valige **Kaup** väljal **Kande tüüp**.
1. Valige **Kaubavajadus** väljal **Kauba seadistus**.
1. Valige väljal **Kaubakood** kaup, mis on hooldusleppe jaoks vajalik.
1. Valige kiirkaardi **Rea üksikasjad** vahekaardi **Toote dimensioonid** väljal **Laoala** kauba laoala.
1. Lepperealt hooldustellimuse loomiseks kiirkaardil **Read** klõpsake valikut **Teenuse tellimuste loomine** ja sisestage seejärel asjakohane teave vormi **teenuse tellimuste loomine**.

## <a name="see-also"></a>Vt ka

[Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
