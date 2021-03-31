---
title: Vabas vormis arve parandamine
description: Selles artiklis selgitatakse, kuidas parandada sisestatud vabas vormis arvet ja väljastada see uuesti parandatud arvena.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71b94e6fa4faafdc5fbe68e89635ec79616164bb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217526"
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
> See funktsioon on saadaval ainult juhul, kui on valitud konfiguratsioonivõti **Vabas vormis arve parandamine**. Konfiguratsioonivõtmete lubamise kohta lisateabe saamiseks vaadake jaotist Luba (või keela) konfiguratsioonivõtmed teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]