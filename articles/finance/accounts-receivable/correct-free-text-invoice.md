---
title: Vabas vormis arve parandamine
description: Selles artiklis selgitatakse, kuidas parandada sisestatud vabas vormis arvet ja väljastada see uuesti parandatud arvena.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9fccd6dbb33efd1556c56a6d92ad191ecfd317fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878185"
---
# <a name="correct-a-free-text-invoice"></a>Vabas vormis arve parandamine

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas parandada sisestatud vabas vormis arvet ja väljastada see uuesti parandatud arvena.

Juba sisestatud vabas vormis arve parandamiseks avage sisestatud vabas vormis arve. Valige lehel **Arve** suvand **Tühista** ja seejärel **Arve parandamine**. Valige põhjuse kood, lisage kommentaarid ja valige uue parandatud arve kuupäev. Saate parandatud arvet muuta ja selle sisestada. 

Parandatud arve sisestamisel koostatakse tühistamisarve krediidisummale, mis võrdub algse arve summaga. Seetõttu on algse arve ja arve tühistamise kombineeritud saldo 0 (null). Tühistamisarve tasakaalustatakse algse arve suhtes. 

Pärast parandatud arve sisestamist, on teil kolm arvet.

-   **Algne arve** – arve, mis sisaldab parandatavat teavet.
-   **Tühistamisarve** – süsteemi loodud kreeditarve, mis loodi viimati parandatud arve tühistamiseks.
-   **Parandatud arve** – arve, mis sisaldab parandatud arve teavet.

Tühistamis- ja parandamisarveid saab tuvastada kahel moel.

-   Lehel **Kõik vabas vormis arved** on veerg **Parandus**, kus näete, millised arved on tühistamis- ja parandusarved.
-   Vabas vormis arve päises on näha olek **Tühistusarve \[arve number\]** või **Parandusarve \[arve number\]**.

> [!NOTE]
> See funktsioon on saadaval ainult juhul, kui on valitud konfiguratsioonivõti **Vabas vormis arve parandamine**. Lisateavet selle kohta, kuidas lubada konfiguratsioonivõtmeid, leiate hooldusrežiimi artikli jaotisest Luba (või keela) konfiguratsioonivõtmed [...](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
