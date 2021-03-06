---
title: Veebipõhise funktsiooniprofiili loomine
description: See teema kirjeldab, kuidas luua rakenduses Microsoft Dynamics 365 Commerce veebipõhine funktsiooniprofiil.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: be78b92858979b8bb009a4699eff96379ef7cef3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791098"
---
# <a name="create-an-online-functionality-profile"></a>Funktsiooniprofiili loomine võrgus

[!include [banner](includes/banner.md)]

Selles teemas antakse ülevaade rakenduse Microsoft Dynamics 365 Commerce veebipõhise funktsiooniprofiili seadistamisest.

Veebipõhine funktsiooniprofiil võimaldab erinevaid võrgukanalites kasutatavaid seadistusi. Iga võrgukanal peab määrama veebipõhise funktsiooniprofiili.

## <a name="create-an-online-functionality-profile"></a>Veebipõhise funktsiooniprofiili loomine

Järgmine protseduur selgitab, kuidas luua rakenduses Commerce Headquarters veebipõhine funktsiooniprofiil.

1. Avage navigeerimispaanil **Moodulid \> Kanali seadistus \> Võrgupoe häälestus \> Funktsiooniprofiilid**.
1. Valige toimingupaanil nupp **Uus**.
1. Väljale **Profiil** sisestage profiili ID.
1. Sisestage väljale **Kirjeldus** väärtus (alumisel pildil oleval näitel „Adventure Worksi profiil”).
1. Jaotises **Funktsioonid** muutke vastavalt vajadusele sätteid **OSTUKORV**, **RETAILI KLIENDID** või **VÄLJAREGISTREERIMINE**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmisel pildil on näidatud veebipõhise funktsiooniprofiili näide.
  
![Veebipõhise funktsiooniprofiili näide](media/online-functionality-profile.png)

## <a name="functions"></a>Funktsioonid

- **Ühenda tooted**: kui see on lubatud, võimaldab see funktsioon ostukorvil värskendada kogust, kui sama üksus lisatakse mitu korda.
- **Luba väljaregistreerimine ilma maksmiseta**: kui see on lubatud, käsitleb see funktsioon stsenaariumi, kui ostukorvi lisatud kaupadel on hind 0,00 dollarit.
- **Loo klient asünkroonses režiimis**: see on pärandseadistus, mis on kohaldatav kolmanda poole e-Commerce’i kanalitele ja ei rakendata Dynamics 365 e-Commerce’i saidile.

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Veebikanali häälestamine](channel-setup-online.md)

[Jaemüügikanali seadistamine](channel-setup-retail.md)

[Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
