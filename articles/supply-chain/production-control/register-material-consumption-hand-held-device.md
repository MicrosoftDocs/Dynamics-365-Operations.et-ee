---
title: Materjalitarbe registreerimine mobiilse seadmega
description: Selles teemas kirjeldatakse töövoogu, mis võimaldab registreerida tootmises toormaterjali pihuseadme abil.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5b9c73cf9b23eb8ad9ed872b76b92b395609e9a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "336125"
---
# <a name="register-material-consumption-using-a-mobile-device"></a>Materjalitarbe registreerimine mobiilse seadmega

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse töövoogu, mis võimaldab registreerida tootmises toormaterjali pihuseadme abil.

<a name="introduction"></a>Sissejuhatus
------------

See töövoog on vajalik juhul, kui materjali jälgitavus on rangelt nõutav. Sellistel juhtudel tuleb materjalide jälgitavuse tagamiseks registreerida tarbimisel täpne kellaaeg ja kogus. Seda protsessi võib vaadelda vastandina eelnevalt või järgnevale mahaarvamise toimingule, kus registreerimise aja ja tegeliku tarbimise aja vahel on nihe. See selgitab, miks mõne jälgitavuse nõudega materjali puhul ei saa kasutada automaatse tarbimise strateegiat. Vaatame lihtsat stsenaariumi, mis selgitab, kuidas seadistada töövoogu tooraine registreerimise võimaldamiseks tootmises pihuseadme abil. [![töövoo seadistamine tooraine registreerimise võimaldamiseks tootmises pihuseadme abil](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a>Stsenaariumi üksikasjad

Pidev tootmisprotsess (5) tarbib partii kaudu juhitud toormaterjali RM-100. Materjali vaba varu on asukohas Bulk-001 (1) litsentsiplaadil PL-1 kahe partiina B1 ja B2, mõlema kogus 100 naela. RM-100 puhul väljastatakse ja töödeldakse laotöö (2) ja materjal komplekteeritakse asukohast Bulk-001 ning viiakse sisendasukohta PIL-01 (3), mis on määratletud mitte litsentsiplaadiga juhitavana. Masina operaator kaalub tootmise sisendasukohast (3) pärineva materjali ja registreerib kaalu ning partiinumbri tarbituks (4). Tootmise sisendasukohast lisatakse materjali osa kindlate ajavahemike järel käsitsi tootmisprotsessi. Kui masina operaator materjali lisab, siis see kaalutakse ja partiinumber registreeritakse.

## <a name="set-up-theworkflow-to-register-consumption-using-a-handheld-device"></a>Töövoo seadistamine tarbimise registreerimiseks pihuseadme abil
Looge valmiskauba toode FG-100, mille materjalikoosluses on partii kaudu juhitav toormaterjal RM-100. Lisage kaks partiid RM-100 (B1 ja B2) koguses 100 asukohta Bulk-001 litsentsiplaadil PL-1. RM-100 koosluse rea automaatse tarbimise põhimõtteks määratakse **Käsitsi**. Määrake toodangu sisendasukohaks PIL-01. Seda saab teha, valides selle asukoha laos 51 toodangu vaike-sisendasukohaks.

1.  Uue mobiilse seadme menüüelemendi loomine. 

-    **Menüüelemendi nimi** – materjali tarbimise registreerimine. 
-    **Pealkiri** – materjali tarbimise registreerimine. 
-    **Režiim** – kaudne. 
-    **Tegevuse kood** – materjali tarbimise registreerimine.

2.  Lisage menüüelement seadme menüüsse **Mobiilne tootmine**.
3.  Looge valmis tootele tootmistellimus. 

-    **Kaubakood** – FG-100 
-    **Laoala** – 5 
-    **Ladu** – 51 
-    **Kogus** – 150

Tootmistellimus **hinnatakse** ja **väljastatakse** ning luuakse laotöö.

4.  Tehke töö, kasutades pihuseadme toormaterjali komplekteerimise töövoogu.

See toob materjali hulgiasukohast tootmise sisendasukohta PIL-01. Kui töö on lõpetatud, on materjali olek **Komplekteeritud toodangu sisendasukohas**. Pärast töö töötlemist võib olek olla **Komplekteeritud** või **Füüsiliselt reserveeritud**. See konfigureeritakse parameetriga **Väljastamisolek pärast paigutamist laovormil**.

5.  Alustage tootmistellimust kliendist või pihuseadmelt, kasutades menüüelementi **Tootmise algus**.

Pärast tootmistellimuse alustamist võite registreerida materjali tarbimise pihuseadme töövoo abil. Alustame 25 naela partii B1 tarbimise registreerimisega.

6.  Valige pihuseadme menüüst menüüelement **Registreeri materjali** **tarbimine**, sisestage järgmised andmed. 

-    Toote tellimisnumber. 
-    Asukoht, kust materjali tarbitakse, praegusel juhul PIL-01. 
-    Kaubakood RM-100. 
-    Partii number B1. 
-    Kogus 25.

7.  Valige **OK**.

Pange tähele, et ekraanil kuvatakse teade „Töölehe rida on loodud”. Tootmistellimusel on avatud tööleht tüübiga **Tootmise komplekteerimisloend** kaubale koodiga RM-100 ja partiinumbriga B1. 

Nüüd saate otsustada registreerimist jätkata, nt partiinumbril B2, ja iga kord, kui valite **OK**, lisatakse avatud töölehele uus töölehe rida. 

Kui olete registreerimise lõpetanud, siis valige **Valmis** töölehe sisestamiseks ja töövoo lõpetamiseks.

### <a name="additional-comments"></a>Lisakommentaarid 

-   Kui kasutaja tühistab töövoo pärast töölehe rea loomist, siis on tööleht sisestamata olekus, ent kui kasutaja kasutab hiljem töövoogu sama tootmistellimuse jaoks, siis lisatakse read avatud töölehele, mitte uuele töölehele.
-   Uus töövoog toetab ka seerianumbrite registreerimist.
-   Registreerida on võimalik ainult kooslusel või valitud tootmistellimuses või partiitellimuses määratletud kaubakoodi.
-   Materjali saab üle tarbida. Näiteks kui eeldatav materjalitarbimise kogus on 100 naela, siis võib selle tarbida üle näiteks kogusega 105 naela.


