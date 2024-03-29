---
title: Tuletatud raamatud
description: Selles artiklis antakse ülevaade tuletatud raamatu funktsioonist.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: kfend
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81abb1b16069adb3cdcc73bdf6b963463cc88938
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714085"
---
# <a name="derived-books"></a>Tuletatud raamatud

[!include [banner](../includes/banner.md)]

Selles artiklis antakse ülevaade tuletatud raamatu funktsioonist.

Tuletatud raamatuid kasutatakse kindla intervalliga plaanitud põhivara raamatu kannete sisestamise lihtsustamiseks.  Saate valida ühe raamatu esmaseks raamatuks. Tavaliselt on see raamat, mida kasutatakse kulumi arvutamiseks. Seejärel saate sellega siduda muud raamatud, mis on seadistatud esmase raamatuga sama intervalliga kandeid sisestama. Maksukulumi raamatud seadistatakse sageli tuletatud raamatutena. 

Kõige tavalisemad tuletatud raamatutesse sisestamiseks seadistatud kanded on soetamised, soetuse korrigeerimised ja likvideerimised. 

## <a name="example"></a>Näide

Raamatud B ja C on seadistatud raamatu A tuletatud raamatutena soetuskande tüübi puhul. Sisestate raamatusse A vara 123 soetuskande summas 1500.00. 

Kande sisestamisel luuakse soetuskanne ning sisestatakse varasse 123 raamatu B puhul ja varasse 123 raamatu C puhul väärtusega 1500,00. Kui valmistate ette esmase raamatu kandeid põhivara töölehele sisestamiseks, saate vaadata ja muuta ka tuletatud raamatute kandeid. Tuletatud väärtusega kandeid ei kuvata esmase raamatu kannete ettevalmistamisel mõnel muul töölehel. Esmase raamatu kannete sisestamisel sisestatakse need siiski määratud kontodele ja sisestuskihtidele.

> [!NOTE]                                                                                                                               
> Raamatud, mis on seadistatud kannete sisestamiseks esmaste raamatute intervallidest erinevate intervallidega, tuleb põhivaraga siduda eraldi, mitte tuletatud raamatutena.  

Lisateavet leiate teemast [Postitage tuletatud raamatutega](post-derived-value-models.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
