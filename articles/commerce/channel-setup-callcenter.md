---
title: Kõnekeskuse kanali seadistamine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.
author: samjarawan
ms.date: 03/13/2020
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
ms.openlocfilehash: 34fa845c72f23485a2573d6bb4cf38b66c7adb7c
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6351196"
---
# <a name="set-up-a-call-center-channel"></a>Kõnekeskuse kanali häälestus


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus kõnekeskus.

## <a name="overview"></a>Ülevaade


Rakenduse Dynamics 365 Commerce kõnekeskus on sellist tüüpi Commerce'i kanal, mille saab määratleda rakenduses. Kõnekeskuse üksustele kanali määratlemine võimaldab süsteemil siduda konkreetsed andmed ja tellimuse töötlemise vaikesätted müügitellimustega. Kui ettevõttel on võimalik määratleda mitu kõnekeskuse kanalit Commerce'is, on oluline märkida, et üks kasutaja võib olla seotud ainult ühe kõnekeskuse kanaliga. 

Enne uue kõnekeskuse kanali loomist veenduge, et olete lõpetanud [Kanali eeltingimuste seadistuse](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Uue kõnekeskuse kanali loomine ja konfigureerimine

Uue kõnekeskuse kanali loomiseks ja konfigureerimiseks toimige järgmiselt.

1. Minge navigatsioonipaanil jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kõnekeskused \> Kõik kõnekeskused**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage väljale **Nimi** uue kanali nimi.
1. Valige ripploendist sobiv **Juriidiline isik**.
1. Valige ripploendist sobiv **Lao** asukoht. Seda asukohta kasutatakse vaikimisi selle kõnekeskuse kanali jaoks loodud müügitellimuste puhul, kui kliendi või kauba tasemel pole määratud muid vaikesätteid.
1. Sisestage väljale **Vaikeklient** kehtiv vaikeklient. Neid andmeid kasutatakse uute kliendikirjete loomisel automaatseks asustamiseks vaikimisi. Kõnekeskuse tellimuste loomisel ei soovitata vaikekliendi jaoks tellimusi luua.
1. Sisestage väljale **Meiliteavituse profiil** kehtiv meiliteavituse profiil. Kui kõnekeskuse tellimused on loodud ja töödeldud, kasutatakse e-posti teatise profiili, et vallandada automatiseeritud e-posti teatised klientidele teabega nende tellimuse oleku kohta.
1. Esitage **Hinnaerandi** teabekood. Peate selleks esmalt looma teabekoodi. See teabekood moodustab põhjusetähiste hulga, millest kasutajal viibatakse valida, kui ta kasutab hinna tühistamise funktsionaalsust kõnekeskuse tellimusel.
1. Sisestage **Ootelepaneku koodi** teabekood. Peate selleks esmalt looma teabekoodi. See teabekood moodustab valikulise põhjusetähiste hulga, millest kasutajal viibatakse valida, kui ta seab tellimuse ootele.
1. Sisestage **Krediidi** teabekood. Peate selleks esmalt looma teabekoodi. See teabekood moodustab põhjusekoodide hulga, mille hulgast kasutaja saab valida, kui kasutab kõnekeskuse tellimuse kreeditfunktsiooni, et anda kliendile klienditeeninduse lisatagastusi.
1. Valikuline: finantsdimensioonide seadistus kiirvahekaardil **Finantsdimensioonid** . Siin sisestatud dimensioonid muutuvad vaikimisi säteteks selles kõnekeskuse kanalis loodud mistahes müügitellimusel.
1. Klõpsake valikut **Salvesta**.

Järgmine pilt näitab uue kõnekeskuse kanali loomist.

![Uus kõnekeskuse kanal.](media/channel-setup-callcenter-1.png)

Järgmine pilt näitab kõnekeskuse kanali näidet.

![Kõnekeskuse kanali näide.](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Täiendava kanali seadistamine

Kõnekeskuse kanali häälestamiseks nõutavad täiendavad toimingud hõlmavad makseviiside ja tarneviiside seadistamist.

Järgmine pilt näitab seadistuste **Tarneviisid** ja **Makseviisid** suvandeid vahekaardil **Seadistus**.

![Täiendavad kõnekeskuse kanali seadistamise toimingud.](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Seadistada maksemeetodid

Kõigi selles kanalis toetatud maksetüüpide makseviiside seadistamiseks toimige järgmiselt. Kasutajad peavad valima eelnevalt määratletud makseviiside hulgast, et linkida need kõnekeskuse kanaliga. Enne kõnekeskuse makseviiside seadistamist seadistage esmalt oma põhimakseviisid rakenduses **Jaemüük ja kaubandus \> Kanali seadistus \> Makseviisid \> Makseviisid**.

1. Valige tegevuspaanil vahekaart **Seadista** ja seejärel **Makseviisid**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige navigeerimispaanil makseviis, mis on saadaval saadaolevate eelnevalt määratletud maksete hulgast.
1. Konfigureerige kõik maksetüübi jaoks vajalikud lisasätted. Krediitkaartide, kinkekaartide või kliendikaardi korral on vajalik täiendav häälestus funktsiooni **Kaardi seaded** valimisega. 
1. Konfigureerige jaotises **Sisestus** maksetüübi õiged sisestuskontod.
1. Klõpsake toimingupaanil valikut **Salvesta**.

Järgmine pilt näitab sularaha makseviisi näidet.

![Makseviiside näited.](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Tarneviiside häälestamine

Konfigureeritud tarneviise saate näha valides **Tarneviisid** vahekaardilt **Seadistus** **Tegevuspaani** alt.  

Selleks, et muuta või lisada tarneviis, mis on seotud kõnekeskuse kanaliga, toimige järgmiselt.

1. Valige tarnevormi kõnekeskuserežiimidest **Tarneviiside haldamine**
1. Valige tegevuspaanilt **Uus**, et luua uus tarneviis, või valige olemasolev režiim.
1. Kõnekeskuse kanali lisamiseks valige jaotisest **Jaemüügikanalid** käsk **Lisa rida**. Kanalite lisamine kasutades organisatsiooni sõlmpunkte, mitte iga kanalit ükshaaval lisades, täiustab kanalite lisamist veelgi.
1. Veenduge, et tarneviis on konfigureeritud andmetega kiirvahekaardil **Tooted** ja kiirvahekaardil **Aadressid**. Kui tarneviisi puhul ei kehti ükski toode või tarneaadress, siis selle valimine tellimuse sisestamise ajal põhjustab tõrkeid.
1. Pärast seda, kui on tehtud muudatused kõnekeskuse tarneviisi konfiguratsioonides, tuleb käivitada ülesanne **Protsessi tarneviisid** , et aktiveerida muutuste maatriks. Selle ülesande leiate, kui navigeerite **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Protsessi tarneviisid**.

Järgmine pilt näitab tarneviisi näidet.

![Tarneviiside häälestamine.](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Kanali kasutajate seadistamine

Kui soovite luua müügitellimuse, mis on lingitud kõnekeskuse kanaliga Kaubanduse peakorterist, peab müügitellimuse loonud kasutaja olema lingitud kõnekeskuse kanaliga. Kasutaja ei saa kaubanduse peakorteris loodud müügitellimust kõnekeskuse kanaliga käsitsi linkida. Link on süstemaatiline ja põhineb kasutajal ja kasutaja suhtel kõnekeskuse kanaliga. Kasutaja võib olla seotud ainult ühe kõnekeskuse kanaliga.

1. Valige toimingupaanil vahekaart **Kanal** ja seejärel **Kanalikasutajad**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige ripploendi valikuloendist olemasolev **Kasutaja ID**, et linkida see kasutaja kõnekeskuse kanaliga

Pärast kanali kasutaja seadistust ja pärast kasutaja poolt uue müügitellimuse loomist kaubanduse peakorteris, lingitakse müügitellimus nendega seostatud kõnekeskuse kanaliga. Selle kanali mis tahes konfiguratsioonid rakendatakse süstemaatiliselt müügitellimusele. Kasutaja saab kinnitada, millise kõnekeskuse kanaliga on müügitellimus lingitud, vaadates kanali nime viidet müügitellimuse päises.


### <a name="set-up-price-groups"></a>Hinnagruppide häälestamine

Hinnarühmad on valikulised, kuid kui neid kasutatakse, saab kontrollida, milliseid müügihindu pakutakse klientidele, kes seavad tellimusi kõnekeskuse kanalis. Kui hinnarühm pole kliendile konfigureeritud või kui kataloogi hinnarühmi ei rakendata müügitellimusele (kasutades kõnekeskuse tellimuse päise välja **Lähtekoodi ID** ), kasutatakse kauba otsimisel kanali hinnarühma. Kui kõnekeskuse kanalis hinnarühma ei leita, kasutatakse vaikimisi kauba põhihindu. 

Hinnarühma seadistamiseks tehke järgmist.

1. Valige toimingupaanil vahekaart **Kanal** ja seejärel **Hinnarühmad**.
1. Klõpsake toimingupaanil valikut **Uus**.
1. Valige rippvalikuloendist **Jaemüügi hinnarühm** .

## <a name="additional-resources"></a>Lisaressursid

[Kanali seadistamise eeltingimused](channels-prerequisites.md)

[Kõnekeskuse müügifunktsioonid](call-center-functionality.md)

[Kõnekeskuse tellimuse töötlemise suvandite seadistamine](set-up-order-processing-options.md)

[Kõnekeskuse kataloogid](call-center-catalogs.md)

[Pettuseteatiste seadistamine ja nendega töötamine](set-up-fraud-alerts.md)

[Kõnekeskuste järjepidevusprogrammide seadistamine](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]