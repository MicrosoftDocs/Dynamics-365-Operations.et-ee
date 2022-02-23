---
title: Jaemüügikanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.
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
ms.openlocfilehash: a9291dddf7d4dc080b6eb1ec60702de32a761f45
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411636"
---
# <a name="set-up-a-retail-channel"></a>Jaemüügikanali seadistamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce toetab mitut jaemüügikanalit. Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks). Igal kaupluse kanalil võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal. Enne jaekaupluse kanali loomist tuleb seadistada kõik need elemendid. 

Enne jaemüügikanali loomist veenduge, et järgite [kanali eeltingimusi](channels-prerequisites.md).

## <a name="create-and-configure-a-new-retail-channel"></a>Uue jaemüügikanali loomine ja konfigureerimine

1. Avage navigatsioonipaneelil **Moodulid \> Kanalid \> Kauplused \> Kõik kauplused**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Nimi** uue kanali nimi.
1. Sisestage väljale **Kaupluse number** kordumatu kaupluse number. See number võib olla tähtnumbriline ja kuni 10 tähemärgi pikkune.
1. Sisestage ripploendisse **Juriidiline isik** sobiv juriidiline isik.
1. Sisestage ripploendisse **Ladu** sobiv ladu.
1. Valige sobiv ajavöönd väljal **Kaupluse ajavöönd**.
1. Valige ripploendist **Käibemaksugrupp** kauplusele sobiv käibemaksugrupp.
1. Valige väljal **Valuuta** sobiv valuuta.
1. Sisestage väljale **Kliendi aadressiraamat** kehtiv aadressiraamat.
1. Sisestage väljale **Vaikeklient** kehtiv vaikeklient.
1. Valige väljal **Funktsiooniprofiil** funktsiooniprofiil, kui see on kohaldatav.
1. Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab uue jaemüügikanali loomist.

![Uus jaemüügikanal](media/channel-setup-retail-1.png)

Järgmine pilt näitab jaemüügikanali näidet.

![Jaemüügikanali näide](media/channel-setup-retail-2.png)

## <a name="other-settings"></a>Muud sätted

On mitmeid muid valikulisi sätteid, mida saab jaotistes **Väljavõte/sulgemine** ja **Mitmesugust** vastavalt jaemüügikaupluse vajadustele seadistada.

Lisaks vt jaotist [Kassa ekraanipaigutused](pos-screen-layouts.md), et saada lisainfot vaikimisi ekraanipaigutuse seadistamise kohta jaotises **Ekraani paigutus** ja jaotist [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md), et saada seadistamise infot **Riistvarajaamade** jaotise kohta.

Järgmine pilt näitab jaemüügikanali seadistuse konfiguratsiooni näidet.

![Jaemüügikanali konfiguratsiooni näide](media/channel-setup-retail-3.png)

## <a name="additional-channel-set-up"></a>Täiendava kanali seadistamine

Et kanalit saaks leida **Tegevuspaanil** jaotise **Seadistus** alt, tuleb seadistada täiendavad elemendid.

Veebikanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside, sularaha deklaratsiooni, tarneviiside, tulu/kulu konto, jaotiste, täitmisgrupi määramise ja seifide seadistamist.

Järgmine pilt näitab erinevaid täiendavaid jaemüügikanali seadistamise suvandeid vahekaardil **Seadistamine**.

![Kanali seadistamine](media/channel-setup-retail-4.png)

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

### <a name="set-up-cash-declaration"></a>Sularaha deklaratsiooni seadistamine

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Sularaha deklaratsioon**.
1. Valige tegevuspaanil **Uus** ja seejärel looge kõik kohaldatavad **Mündi** ja **Paberraha** nominaalväärtused.

Järgmine pilt näitab sularaha deklaratsiooni näidet.

![Sularaha deklaratsioonide seadistamine](media/channel-setup-retail-6.png)

### <a name="set-up-modes-of-delivery"></a>Tarneviiside häälestamine

Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.  

Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.
1. Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.
1. Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**. Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.

Järgmine pilt näitab tarneviisi näidet.

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Tulu/kulu konto seadistamine

Tulu/kulu konto seadistamiseks läbige need etapid.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Tulu/kulu konto**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage nimi väljale **Nimi**.
1. Sisestage otsingunimi väljale **Otsingunimi**.
1. Sisestage kontotüüp väljale **Kontotüüp**.
1. Vajadusel sisestage tekst väljadele **Teate rida 1**, **Teate rida 2**, **Saatelehe tekst 1** ja **Saatelehe tekst 2**.
1. Sisestage jaotisse **Sisestamine** sisestamise andmed.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab tulu/kulu konto näidet.

![Tulu/kulu kontode seadistamine](media/channel-setup-retail-8.png)

### <a name="set-up-sections"></a>Jaotiste seadistamine

Jaotiste seadistamiseks läbige need etapid.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsa **Jaotised**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Jaotise number** jaotise number.
1. Sisestage kirjeldus väljale **Kirjeldus**.
1. Sisestage väljale **Jaotise suurus** jaotise suurus.
1. Vajadusel konfigureerige jaotiste **Üldine** ja **Müügistatistika** sätteid.
1. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-a-fulfillment-group-assignment"></a>Täitmisgrupi määramise seadistamine

Täitmisgrupi määramise seadistamiseks tehke järgmist.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige täitmisgrupp ripploendist **Täitmisgrupp**.
1. Sisestage kirjeldus ripploendisse **Kirjeldus**.
1. Valige toimingupaanil nupp **Salvesta**

Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Seifide seadistamine

Seifide seadistamiseks läbige need etapid.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsa **Seifid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage seifi nimi.
1. Valige toimingupaanil nupp **Salvesta**.

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Veebikanali häälestamine](channel-setup-online.md)

[Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)

