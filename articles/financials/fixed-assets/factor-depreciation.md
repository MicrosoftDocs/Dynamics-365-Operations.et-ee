---
title: Kulumiarvestus kordaja alusel
description: "Selles artiklis antakse ülevaade teguripõhisest kulumiarvestusmeetodist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4b87d96e80b343a2b57db59b5d4c19e70d0a94ea
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="factor-depreciation"></a>Kulumiarvestus kordaja alusel

[!include[banner](../includes/banner.md)]


Selles artiklis antakse ülevaade teguripõhisest kulumiarvestusmeetodist.

Tegurid on põhivarade kulumiarvestuses kasutatavad protsendimäärad. Kui valite põhivara kulumireegli seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **Tegur**, saate seadistada progresseeruva, degressiivse või lineaarse kulumi.

-   Progresseeruva kulumi puhul suureneb kulumi summa igal kulumiperioodil.
-   Degressiivse kulumi puhul väheneb perioodide kulumisumma aja jooksul.
-   Lineaarse kulumi puhul on kulum igal perioodil ühesuurune.

Järgmiste reeglite ja näidete varal näete, kuidas saate seadistada iga kulumiliigi tegureid. 

> [!NOTE] 
> Märkus. Kui valite väljal **Meetod** väärtuse **Tegur**, kuvatakse väljad **Tegur** ja **Intervall**.

## <a name="progressive-depreciation"></a>Progresseeruv kulum
Välja **Tegur** väärtus on suurem kui **50**.

### <a name="example"></a>Näide

Soetusmaksumus on 100 000, tegur on 70, tööiga on 10 aastat ning kulumiarvestuse algus on 1. jaanuar. Kulumisummad ja raamatupidamisliku jääkväärtuse summad kuvatakse ainult kasuliku eluea kuue esimese aasta kohta.

| Aasta | Periood      | Kulumisumma | Raamatupidamisliku jääkväärtuse summa |
|------|-------------|---------------------|-----------------------|
| 1    | 31. detsember | 307.69              | 99 692.31             |
| 2    | 31. detsember | 1447.21            | 98,245.10             |
| 3    | 31. detsember | 3104.50            | 95,140.60             |
| 4    | 31. detsember | 5150.21            | 89,990.39             |
| 5    | 31. detsember | 7522.95            | 82,467.44             |
| 6    | 31. detsember | 10 184.06           | 72,283.38             |

## <a name="digressive-depreciation"></a>Degressiivne kulum
Välja **Tegur** väärtus on väiksem kui **50**.

### <a name="example"></a>Näide

Soetusmaksumus on 100 000, tegur on 20, tööiga on 10 aastat ning kulumiarvestuse algus on 1. jaanuar. Kulumisummad ja raamatupidamisliku jääkväärtuse summad kuvatakse ainult kasuliku eluea kuue esimese aasta kohta.

| Aasta | Periood      | Kulumisumma | Raamatupidamisliku jääkväärtuse summa |
|------|-------------|---------------------|-----------------------|
| 1    | 31. detsember | 56 080.43           | 43,919.57             |
| 2    | 31. detsember | 10 665.70           | 33,253.87             |
| 3    | 31. detsember | 7156.22            | 26,097.65             |
| 4    | 31. detsember | 5538.06            | 20,559.59             |
| 5    | 31. detsember | 4579.89            | 15,979.70             |
| 6    | 31. detsember | 3937.36            | 12,042.34             |

## <a name="straight-line-depreciation"></a>Lineaarne kulum
Välja **Tegur** väärtus võrdub **50**. Sellisel juhul on kulum igal perioodil sama ja teil tuleks kaaluda oma teistel väljadel määratud väärtuste mõju. Lugege selle kohta teemat [Lineaarne tööea kulumiarvestus](straight-line-service-life-depreciation.md).




