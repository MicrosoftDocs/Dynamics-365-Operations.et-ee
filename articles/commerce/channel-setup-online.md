---
title: Võrgukanali häälestamine
description: See artikkel kirjeldab, kuidas luua uus võrgukanal Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 02/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: be9fafe8ece771ad6577db1cdb70af6f48e054cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272876"
---
# <a name="set-up-an-online-channel"></a>Võrgukanali häälestamine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas luua uus võrgukanal Microsoft Dynamics 365 Commerce.

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

![Uus võrgukanal.](media/channel-setup-online-1.png)

Järgmine pilt näitab võrgukanali näidet.

![Võrgukanali näide.](media/channel-setup-online-2.png)

## <a name="assign-the-channel-to-a-commerce-scale-unit"></a>Kanali määramine Commerce Scale Uniti jaoks

Teie uus kanal peab olema määratud Commerce Scale Uniti. Juhiseid vt kanalite [konfigureerimine Commerce Scale Uniti kasutamiseks](../fin-ops-core/dev-itpro/deployment/initialize-retail-channels.md#configure-channels-to-use-commerce-scale-unit).

## <a name="set-up-languages"></a>Keelte seadistamine

Kui teie e-äri sait toetab mitut keelt, laiendage **jaotist Keeled** ja lisage vajaduse korral lisakeeli.

## <a name="set-up-payment-account"></a>Maksekonto seadistamine

Jaotisest **Maksekonto** saate lisada kolmanda osapoole maksepakkuja. Lisateavet Adyeni maksekonnektori seadistamise kohta vt teemast [Dynamics 365 maksekonnektor Adyeni jaoks](./dev-itpro/adyen-connector.md).

## <a name="additional-channel-setup"></a>Täiendava kanali seadistamine

Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, tarneviiside ja täitmisgrupi määramist.

Järgmine pilt näitab seadistuste **Tarneviisid**, **Makseviisid** ja **Täitmisgurpi määramine** suvandeid vahekaardil **Seadistus**.

![Täiendavad võrgukanali seadistamise toimingud.](media/channel-setup-online-3.png)

### <a name="set-up-payment-methods"></a>Seadistada maksemeetodid

Kõigi selles kanalis toetatud maksetüübi makseviiside seadistamiseks toimige järgmiselt.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige navigeerimispaanil soovitud makseviis.
1. Sisestage jaotises **Üldine** **Toimingu nimi** ja konfigureerige muud soovitud sätted.
1. Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab sularaha makseviisi näidet.

![Makseviiside näited.](media/channel-setup-retail-5.png)

### <a name="set-up-modes-of-delivery"></a>Tarneviiside häälestamine

Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.  

Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.
1. Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.
1. Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**. Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.

Järgmine pilt näitab tarneviisi näidet.

![Tarneviiside häälestamine.](media/channel-setup-retail-7.png)

### <a name="set-up-a-fulfillment-group-assignment"></a>Täitmisgrupi määramise seadistamine

Täitmisgrupi määramise seadistamiseks tehke järgmist.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige täitmisgrupp ripploendist **Täitmisgrupp**.
1. Sisestage kirjeldus ripploendisse **Kirjeldus**.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.

![Täitmisgrupi määramiste seadistamine.](media/channel-setup-retail-9.png)

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Kanali häälestuse eeltingimused](channels-prerequisites.md)

[Jaemüügikanali seadistamine](channel-setup-retail.md)

[Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](./dev-itpro/adyen-connector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
