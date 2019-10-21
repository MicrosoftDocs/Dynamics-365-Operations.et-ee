---
title: Tuletatud raamatud
description: Selles artiklis antakse ülevaade tuletatud raamatu funktsioonist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a649fdbc355b3382bc6c80be03f8b37a06d5226
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177332"
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

Lisateavet vt teemast [Sisestamine tuletatud raamatute kaudu](post-derived-value-models.md).



