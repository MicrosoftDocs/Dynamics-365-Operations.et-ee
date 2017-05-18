---
title: "Töövoos tingimusliku otsuse konfigureerimine"
description: "Kasutage järgmist protseduuri, et konfigureerida tingimusliku otsuse atribuudid."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d3efb6106df7d66ebe9b1a061f9976b8978704b1
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-conditional-decision-in-a-workflow"></a>Töövoos tingimusliku otsuse konfigureerimine

[!include[banner](../includes/banner.md)]


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






