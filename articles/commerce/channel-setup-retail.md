---
title: Jaemüügikanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.
author: samjarawan
ms.date: 04/23/2021
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
ms.openlocfilehash: 3f1f5dc2c8402d9b6b68a049f804932812eb74c0
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937530"
---
# <a name="set-up-a-retail-channel"></a>Jaemüügikanali häälestus

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus jaemüügikanal.

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

Et kanalit saaks leida Tegevuspaanil jaotise **Seadistus** alt, tuleb seadistada täiendavad elemendid.

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

Konfigureeritud tarneviise saate näha, valides **Tarneviisid** vahekaardilt **Seadistus** tegevuspaani alt.  

Tarneviisi muutmiseks või lisamiseks toimige järgmiselt.

1. Avage navigeerimispaanil **Moodulid \> Varude haldus \> Tarneviisid**.
1. Valige tegevuspaanilt suvand **Uus**, et luua uus tarneviis, või valige olemasolev režiim.
1. Kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**. Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.

Järgmine pilt näitab tarneviisi näidet.

![Tarneviiside häälestamine](media/channel-setup-retail-7.png)

### <a name="set-up-incomeexpense-account"></a>Tulu/kulu konto seadistamine

Tulu/kulu konto seadistamiseks läbige need etapid.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel suvand **Tulu/kulu konto**.
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

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Täitmisgrupi määramine**.
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
1. Valige tegevuspaanil nupp **Salvesta**

Järgmine pilt näitab täitmisgrupi määramise seadistuse näidet.

![Täitmisgrupi määramiste seadistamine](media/channel-setup-retail-9.png)

### <a name="set-up-safes"></a>Seifide seadistamine

Seifide seadistamiseks läbige need etapid.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel klõpsake suvandile **Seifid**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage seifi nimi.
1. Valige toimingupaanil nupp **Salvesta**.

### <a name="ensure-unique-transaction-ids"></a>Kordumatute kande-ID-de tagamine

Äriversiooni 10.0.18 kohaselt on kassa (POS) jaoks loodud kannete ID-d järjestikused ja sisaldavad järgmisi osi.

- Fikseeritud osa, mis on ühendatud kaupluse ID ja terminali ID-ga. 
- Seeriaosa, mis on numbrite jada. 

Täpsemalt on vorming *{store}{terminal} -{numbersequence}*. 

Kuna kande ID-sid saab luua ühenduseta ja võrguühenduseta režiimides, on olemas duplikaatkande ID-de genereerimise eksemplarid. Kande ID duplikaatide eemaldamiseks on vaja andmed käsitsi parandada. 

Rakenduse kommertsversiooniga 10.0.19 värskendati kande ID vormingut, et eemaldada seeriaosa ja selle asemel kasutatakse 13-numbrit, mis on loodud arvutades aja millisekundites alates 1970. Selle muudatusega on uus kande ID vorming *{store} - {terminal} - {millisecondsSince1970}*. See värskendus muudab kande ID mittejärjestatuks ja tagab, et kande ID-d on alati kordumatud. 

> [!NOTE]
> Kannete ID-d on mõeldud ainult sisesüsteemi jaoks, nii et need ei pea olema järjestikused. Paljud riigid nõuavad siiski, et sissetuleku ID-d oleks järjestikused.

Uue kande ID vormingu funktsiooni saab lubada **funktsioonihalduse** tööruumis. 

Uute kande-ID-de kasutamise lubamiseks järgige järgmiseid samme.

1. Avage Commerce'i peakorteris **Süsteemihaldus \> Tööruumid \> Funktsioonihaldus**.
1. "Jaemüügi ja äri" mooduli filter.
1. Otsige **"luba uut kande ID-d, et vältida topeltkande ID-de tekkimist"** funktsiooni nime.
1. Valige funktsioon, mida soovite sisse lülitada, ja seejärel valige paremal paanil nupp **Luba kohe**.  
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
1. Käitage **1070 kanali konfiguratsiooni** ja **1170 POS Task Recorderi** tööd, et sünkroonida lubatud funktsioon kauplustesse.
1. Pärast muudatuste saatmist kauplustesse tuleb kassaterminalid sulgeda ja uuesti avada, et kasutada uut kande ID vormingut. 

> [!NOTE]
> Pärast uue kande ID vormingu funktsiooni lubamist ei saa te seda funktsiooni keelata. Kui see tuleb keelata, pöörduge commerce Supporti poole.

## <a name="additional-resources"></a>Lisaressursid

[Kanalite ülevaade](channels-overview.md)

[Kanali häälestuse eeltingimused](channels-prerequisites.md)

[Veebikanali häälestamine](channel-setup-online.md)

[Kõnekeskuse kanali seadistamine](channel-setup-callcenter.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
