---
title: Vabas vormis arve parandamine
description: "Selles artiklis selgitatakse, kuidas parandada sisestatud vabas vormis arvet ja väljastada see uuesti parandatud arvena."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


---

# <a name="correct-a-free-text-invoice"></a>Vabas vormis arve parandamine

[!include[banner](../includes/banner.md)]


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
> See funktsioon on saadaval ainult juhul, kui on valitud konfiguratsioonivõti **Vabas vormis arve parandamine**.




