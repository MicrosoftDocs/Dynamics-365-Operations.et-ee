---
title: Kontsernisisese tellimuse sisestusparameetrite seadistamine
description: See artikkel selgitab kontsernisiseste tellimuste parameetrite seadistamist
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 24389d8ed3768089d59dc87e5948e9ea7fa1ecfc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679243"
---
# <a name="set-up-parameters-to-post-an-intercompany-order"></a>Kontsernisisese tellimuse sisestusparameetrite seadistamine

[!include [banner](../../includes/banner.md)]

Kontsernisisese kliendi arve sisestamisel saate seadistada nii kontsernisisese ostutellimuse kui ka algse kliendi arve automaatse sisestamise.

> [!NOTE]
> Enne selle protseduuri sooritamist seadistage ettevõtte prindihaldus nii, et see osutaks õigele arveprinterile. See tagab, et algse müügitellimuse arve prinditakse õigele printerile.

Peate seadistama järgmised parameetrid:

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**. Valige müügitellimus, millega soovite töötada.
1. Valige müügitellimusel tegevuspaanil **Päisevaade** ja seejärel valige kiirkaart **Kontsernisisesed sätted** ja avage see.
1. Minge tegumiriba vahekaardile **Müügitellimus** ja valige **Redigeeri**.
1. Minge tagasi **Kontsernisiseste sätete** kiirkaardile ja valige **Otsetarne**, et lubada otsetarne kogu kontserniahelas (kõik tellimused).
1. Müügitellimuse salvestamiseks uue sättega valige käsk **Salvesta**. Seejärel valige **Sulge** müügitellimuse sulgemiseks.
1. Avage **Hanked \> Hankijad \> Kõik hankijad**. Valige vahekaardil **Üldine** suvand **Kontsernisisene**.
1. Lehel **Kontsernisisene** valige **Ostutellimuse poliitika** link. Väljagrupil **Kontsernisisene ostutellimus (otsetarne)** valige käsk **Sisesta arve automaatselt** ja eemaldage märge väljalt **Prindi arve automaatselt**.
1. Väljagrupil **Algne müügitellimus (otsetarne)** valige väli **Sisesta arve automaatselt** ja eemaldage märge väljalt **Prindi arve automaatselt**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
