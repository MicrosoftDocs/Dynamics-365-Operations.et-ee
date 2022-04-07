---
title: Kindlate toote töötsükli olekutega toodete välistamine
description: Selles teemas selgitatakse, kuidas välistada optimeerimise planeerimise funktsiooni kasutamisel töötsükli olekul põhinevaid tooteid.
author: t-benebo
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-11-13
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: cdc1d47a4d12515e82e5feb55c5d473476e36873
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469194"
---
# <a name="exclude-products-that-have-specific-product-lifecycle-states"></a>Kindlate toote töötsükli olekutega toodete välistamine

[!include [banner](../../includes/banner.md)]

Väljastatud toodetel ja väljastatud tooteversioonidel on väli **Toote töötsükli olek**. See väli võimaldab teil muu hulgas kontrollida, millised tooted on koondplaneerimise käigus kaasatud. Te saate lisada, eemaldada ja redigeerida töötsükli olekuid vastavalt vajadusele, tehes valiku **Tooteteabe haldus \> Häälestus \> Toote töötsükli olek**. Määrake iga toote elutsükli oleku jaoks suvandi **On planeerimiseks aktiivne** väärtuseks *Jah*, kui selle olekuga tooted tuleks koondplaneerimise käigus kaasata. Kui suvandi väärtuseks on määratud *Ei*, välistatakse seotud tooted ja variandid kõigi koondandmete ja kõigi koosluse tasemel arvutustest.

Väljastatud tooteid ja variante, mille puhul jäetakse väli **Toote töötsükli olek** tühjaks, käsitletakse nii, nagu oleks neil toote töötsükli olek, kus suvandi **On planeerimiseks aktiivne** väärtuseks on määratud *Jah*. Teisisõnu kaasatakse need koondplaneerimise käigus.

> [!NOTE]
> Et vältida tarbetuid tarnesoovitusi, soovitame teil seostada kõik iganenud väljastatud tooted ja variandid toote töötsükli olekuga, kus suvandi **On planeerimiseks aktiivne** väärtuseks on määratud *Ei*. See lähenemine on eriti oluline, kui töötate toote konfiguratsiooni variantidega, mis ei ole korduvkasutatavad, kuna see aitab ennetada jäätmete teket.

## <a name="related-resources"></a>Seotud ressursid

Lisateavet toote töötsükli olekute kohta leiate teemast [Toote töötsüklite ülevaade](../../pim/product-lifecycle.md).

Täpsema teabe saamiseks selle kohta, kuidas kasutada toote töötsükli olekut toodete välistamiseks koondplaneerimisest ja koosluse taseme arvutustest, lugege teemat [Toote töötsükli oleku loomine toote välistamiseks koondplaneerimisest](../../pim/tasks/exclude-products-master-planning.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]