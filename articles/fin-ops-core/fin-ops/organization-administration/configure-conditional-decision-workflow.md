---
title: Töövoos tingimuslike otsuste konfigureerimine
description: Kasutage järgmist protseduuri, et konfigureerida tingimusliku otsuse atribuudid.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a953d4e781db42834f0bc8daf80040c39ea5b5c
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698116"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a>Töövoos tingimuslike otsuste konfigureerimine

[!include [banner](../includes/banner.md)]

Kasutage järgmist protseduuri, et konfigureerida tingimusliku otsuse atribuudid.

Tingimuslik otsus on punkt, milles töövoog jaguneb kaheks haruks. Töövoo redaktoris tingimusliku otsuse loomiseks paremklõpsake tingimuslikku otsust ja seejärel klõpsake valikut **Atribuudid**, et avada vorm **Atribuudid**.

## <a name="name-a-decision"></a>Otsusele nime andmine

Tingimuslikule otsusele nime sisestamiseks tehke järgmist.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Väljal **Nimi** sisestage tingimuslikule otsusele kordumatu nimi.

## <a name="set-conditions"></a> Tingimuste määramine

Süsteem määrab, haru kasutada, hinnates edastatud dokumenti ja otsustades, kas see vastab kindlatele tingimustele.

1. Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2. Klõpsake valikut **Lisa tingimus**.
3. Sisestage tingimus.
4. Sisestage lisatingimused, kui need on nõutavad.
5. Kontrollimaks, kas teie sisestatud tingimused on õigesti konfigureeritud, tehke järgmist.

    1. Klõpsake valikut **Katseta**, et avada leht **Katseta töövoo tingimust**.
    2. Valige vormi alal kirje **Kontrolli tingimust**.
    3. Klõpsake nuppu **Test**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.
    4. Klõpsake valikut **OK** või **Tühista**, et naasta vormile **Atribuudid**.
