---
title: "Töövoos tingimusliku otsuse konfigureerimine"
description: "Kasutage järgmist protseduuri, et konfigureerida tingimusliku otsuse atribuudid."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Töövoos tingimusliku otsuse konfigureerimine

[!include [banner](../includes/banner.md)]

Kasutage järgmist protseduuri, et konfigureerida tingimusliku otsuse atribuudid.

Tingimuslik otsus on punkt, milles töövoog jaguneb kaheks haruks. Töövoo redaktoris tingimusliku otsuse loomiseks paremklõpsake tingimuslikku otsust ja seejärel klõpsake valikut **Atribuudid**, et avada vorm **Atribuudid**.

## <a name="name-a-decision"></a>Otsusele nime andmine
Tingimuslikule otsusele nime sisestamiseks tehke järgmist.
1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Väljal **Nimi** sisestage tingimuslikule otsusele kordumatu nimi.

## <a name="set-conditions"></a> Tingimuste määramine
Süsteem määrab, haru kasutada, hinnates edastatud dokumenti ja otsustades, kas see vastab kindlatele tingimustele.
1.  Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.
2.  Klõpsake valikut **Lisa tingimus**.
3.  Sisestage tingimus.
4.  Sisestage lisatingimused, kui need on nõutavad.
5.  Kontrollimaks, kas teie sisestatud tingimused on õigesti konfigureeritud, tehke järgmist.
    1.  Klõpsake valikut **Katseta**, et avada leht **Katseta töövoo tingimust**.
    2.  Valige vormi alal kirje **Kontrolli tingimust**.
    3.  Klõpsake nuppu **Test**. Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.
    4.  Klõpsake valikut **OK** või **Tühista**, et naasta vormile **Atribuudid**.






