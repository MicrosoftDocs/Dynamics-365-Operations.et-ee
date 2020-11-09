---
title: Veebikanali häälestamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus veebikanal.
author: samjarawan
manager: annbe
ms.date: 07/02/2020
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
ms.openlocfilehash: 07225d97af76ea665fa28362cc205c6e8dc4fdf4
ms.sourcegitcommit: 776758a0ff95c3c7398986095104d1d2b9814514
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/24/2020
ms.locfileid: "4107226"
---
# <a name="set-up-an-online-channel"></a>Veebikanali häälestamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus veebikanal.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce toetab mitut jaemüügikanalit. Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks). Võrgupoed annavad kliendile võimaluse osta tooteid lisaks oma jaekauplustele ka jaemüüja veebipoest.

Commerce'is veebipoe loomiseks peate esmalt looma võrgukanali. Enne uue võrgukanali loomist veenduge, et olete lõpuni viinud [Kanali eeltingimuste häälestamise](channels-prerequisites.md).

Enne uue saidi loomist peab olema rakenduses Commerce loodud vähemalt üks veebipood. Lisateavet leiate teemast [E-kaubanduse saidi loomine](create-ecommerce-site.md).

## <a name="create-and-configure-a-new-online-channel"></a>Uue võrgukanali loomine ja konfigureerimine

Uue võrgukanali loomiseks ja konfigureerimiseks toimige järgmiselt.

1. Avage navigatsioonipaneelil **Moodulid \> Kanalid \> Veebipoed**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Nimi** uue kanali nimi.
1. Sisestage ripploendisse **Juriidiline isik** sobiv juriidiline isik.
1. Sisestage ripploendisse **Ladu** sobiv ladu.
1. Valige sobiv ajavöönd väljal **Kaupluse ajavöönd**.
1. Valige väljal **Valuuta** sobiv valuuta.
1. Sisestage väljale **Vaikeklient** kehtiv vaikeklient.
1. Sisestage väljale **Kliendi aadressiraamat** kehtiv aadressiraamat.
1. Valige väljal **Funktsiooniprofiil** funktsiooniprofiil, kui see on kohaldatav.
1. Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab uue võrgukanali loomist.

![Uus võrgukanal](media/channel-setup-online-1.png)

Järgmine pilt näitab võrgukanali näidet.

![Võrgukanali näide](media/channel-setup-online-2.png)

## <a name="set-up-languages"></a>Keelte seadistamine

Kui teie e-kaubanduse sait toetab mitut keelt, laiendage jaotist **Keeled** ja lisage vajadusel täiendavaid keeli.

## <a name="set-up-payment-account"></a>Maksekonto seadistamine

Jaotisest **Maksekonto** saate lisada kolmanda osapoole maksepakkuja. Lisateavet Adyeni maksekonnektori seadistamise kohta vt teemast [Dynamics 365 maksekonnektor Adyeni jaoks](../retail/dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Täiendava kanali seadistamine

Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, tarneviiside ja täitmisgrupi määramist.

Järgmine pilt näitab seadistuste **Tarneviisid** , **Makseviisid** ja **Täitmisgurpi määramine** suvandeid vahekaardil **Seadistus**.

![Täiendavad võrgukanali seadistamise toimingud](media/channel-setup-online-3.png)

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
1. Valige tegevuspaanilt **Uus** , et luua uus tarneviis, või valige olemasolev režiim.
1. Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**. Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.

Järgmine pilt näitab tarneviisi näidet.

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Täitmisgrupi määramise seadistamine

Täitmisgrupi määramise seadistamiseks tehke järgmist.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige täitmisgrupp ripploendist **Täitmisgrupp**.
1. Sisestage kirjeldus ripploendisse **Kirjeldus**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Jaemüügikanali seadistamine](channel-setup-retail.md)

[Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](../retail/dev-itpro/adyen-connector.md)
