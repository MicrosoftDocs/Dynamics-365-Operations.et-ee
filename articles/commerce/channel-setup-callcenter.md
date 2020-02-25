---
title: Kõnekeskuse kanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6ec42ab920868f541eeac54556f4f24cb1efaa3a
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002446"
---
# <a name="set-up-a-call-center-channel"></a>Kõnekeskuse kanali seadistamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.

## <a name="overview"></a>Ülevaade

Rakenduse Dynamics 365 Commerce kõnekeskus on sellist tüüpi kanal, mille saab määratleda rakenduses. Kõnekeskuse üksustele kanali määratlemine võimaldab süsteemil siduda konkreetsed andmed ja tellimuse töötlemise vaikesätted müügitellimustega. Ettevõte saab määratleda Commerce'is mitu kõnekeskuse kanalit. 

Enne uue kõnekeskuse kanali loomist veenduge, et olete lõpuni viinud [Kanali eeltingimuste häälestamise](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Uue kõnekeskuse kanali loomine ja konfigureerimine

Uue kõnekeskuse kanali loomiseks ja konfigureerimiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Kanalid \> Kõnekeskused \> Kõik kõnekeskused**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Nimi** uue kanali nimi.
1. Valige ripploendist sobiv **Juriidiline isik**.
1. Valige ripploendist sobiv **Lao** asukoht.
1. Sisestage väljale **Vaikeklient** kehtiv vaikeklient.
1. Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.
1. Esitage **Hinnaerandi** teabekood. Pidage meeles, et peate selleks teabekoodi looma.
1. Sisestage **Ootelepaneku koodi** teabekood. Pidage meeles, et peate selleks teabekoodi looma.
1. Sisestage **Krediidi** teabekood. Pidage meeles, et peate selleks teabekoodi looma.
1. Valige käsk **Salvesta**.

Järgmine pilt näitab uue kõnekeskuse kanali loomist.

![Uus kõnekeskuse kanal](media/channel-setup-callcenter-1.png)

Järgmine pilt näitab kõnekeskuse kanali näidet.

![Kõnekeskuse kanali näide](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Täiendava kanali seadistamine

Kõnekeskuse kanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside ja tarneviiside seadistamist.

Järgmine pilt näitab seadistuste **Tarneviisid** ja **Makseviisid** suvandeid vahekaardil **Seadistus**.

![Täiendavad kõnekeskuse kanali seadistamise toimingud](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Seadistada maksemeetodid

Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige navigeerimispaanil soovitud makseviis.
1. Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.
1. Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab sularaha makseviisi näidet.

![Makseviiside näited](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Tarneviiside häälestamine

Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.  

Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.
1. Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.
1. Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**. Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.

Järgmine pilt näitab tarneviisi näidet.

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

## <a name="additional-resources"></a>Lisaressursid

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Kõnekeskuse müügifunktsioonid](call-center-functionality.md)

[Kõnekeskuse tellimuse töötlemise suvandite seadistamine](set-up-order-processing-options.md)

[Kõnekeskuse kataloogid](call-center-catalogs.md)

[Pettuseteatiste seadistamine ja nendega töötamine](set-up-fraud-alerts.md)

[Kõnekeskuste järjepidevusprogrammide seadistamine](set-up-continuity-program.md)
