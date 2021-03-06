---
title: Kupongide seadistamine jaemüügi jaoks
description: Selles teemas antakse ülevaade kupongidest ja selgitatakse, kuidas neid seadistada.
author: scott-tucker
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a4de42c23bf96591d1ac99ed32438fe34a485998
ms.sourcegitcommit: 05868764acd3d77970724a30c49c5ae5ffb6ca5b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5906645"
---
# <a name="set-up-coupons-for-retail-sales"></a>Kupongide seadistamine jaemüügi jaoks

[!include [banner](includes/banner.md)]

## <a name="overview-of-coupons"></a>Kupongide ülevaade

Kupongid on koodid ja vöötkoodid, mida kasutatakse allahindluste lisamiseks kannetele. Igal kupongil võib olla mitu koodi ja igal koodil võivad olla oma kehtivuskuupäevad.

Iga kupong on seotud ühe allahindlusega. Allahindlusega seotud hinnagrupid määratlevad kliendid, kes saavad kupongi kasutada, või kanalid, kus kupong kehtib.

Põhimõtteliselt on kupongid allahindlustele lisanduv kinnitus. Kupongil on vajalikud kupongi koodid ja vöötkoodid, millel on nende koodide kuupäevavahemikud. Kupongil on ka valikulised kasutuspiirid ja kliendile vajalikud atribuudid. Allahindlus annab toodete kogumi, millele kupong kehtib. Allahindluse hinnagrupid annavad klientide kogumi, kanalid või kataloogid, millele kupong kehtib.

Kupongi loomiseks tuleb luua allahindlus ja kupong eraldi. Seejärel tuleb need siduda, valides rakenduses Commerce kupongi lehel allahindluse.

> [!NOTE]
> Kui kupong on allahindlusega lingitud, muutub rakenduses Commerce mitu allahindluse välja kirjutuskaitstuks, kuna neid hallatakse kupongi sätetega. Nende väljade hulka kuuluvad oleku ja standardsete kuupäevavahemike väljad.
> 
> Kõnekeskuse kanali kupongi kasutamisel peate valima nupu **Arvuta ümber** **(Müü vahekaart > Arvuta > Arvuta ümber)**, et kupongiga seotud allahindlust saaks rakendada. See täiendav samm eemaldatakse tulevases versioonis.

### <a name="limited-use-coupons"></a>Piiratud kasutusega kupongid

Kupongid saab konfigureerida piiratud kasutusega kupongidena. Kasutuspiiri saab määratleda kliendi või kanali kaupa või üldise piirina. Seda piiri rakendatakse koodi või vöötkoodi sisestamisel või skannimisel kassas või müügitellimuse sisestamisel.

Kupongi piirmäär rakendatakse kupongi koodi kohta. Näiteks ühekordselt kasutatavat kupongi, millel on kaks kupongi koodi, saab kasutada kaks korda: üks kord kummagi kupongi koodi kohta. Kummagi kupongi koodi saab eraldi aktiivseks määrata.

Kuponge saab kasutada mis tahes müügikanalis, kuid kõikide kõnekeskuse tellimuste puhul saab piiratud kasutusega kuponge kasutada vaid selliste kõnekeskuste tellimuste puhul, kus on lubatud kõnekeskuse osas säte **Tellimuse lõpule viimine**. Kui see pole lubatud, siis saab kõnekeskuse tellimuste puhul kasutada vaid piiramatu kasutusega tüüpi kuponge.

> [!NOTE]
> Kui kupongikood on jõudnud kasutuspiirini, *ei* muuda süsteem automaatselt kupongikoodi olekuks „Kasutatud”. Siiski on kupongikood saavutanud kasutuspiiri ja seda ei saa enam kasutada. Kui kupongikoodi olekuks seatakse käsitsi midagi muud peale valiku **Aktiivne**, ei saa seda kupongikoodi enam ühelgi kanalil kasutada.  

## <a name="managing-coupons"></a>Kupongide haldamine

Allahindlus ja kupong tuleb luua eraldi. Seejärel tuleb need siduda, valides kupongi lehel allahindluse. Kui kupong on allahindlusega seotud, muutub mitu allahindluse välja kirjutuskaitstuks, kuna neid hallatakse kupongi sätetega. Nende väljade hulka kuuluvad oleku ja standardsete kuupäevavahemike väljad.

Põhimõtteliselt on kupongid nüüd allahindlustele lisanduv kinnitus. Kupongil on kupongi koodid ja vöötkoodid, millel on nende koodide kuupäevavahemikud, kasutuspiirid ja kliendile vajalik atribuut. Allahindlus annab toodete kogumi, millele kupong kehtib. Allahindluse hinnagrupid annavad klientide kogumi, kanalid või kataloogid, millele kupong kehtib.

## <a name="system-setup-for-coupons"></a>Süsteemi seadistus kupongide puhul

Enne kupongi seadistamist tuleb seadistada kupongi vöötkood ja kaks kupongi numbriseeriat.

1. Looge lehel **Maski märgid** kupongi koodile uus maski märk. Valida saab mis tahes kasutamata märki.
2. Looge lehel **Vöötkoodi maski häälestus** uus vöötkoodi mask. Määrake välja **Tüüp** väärtuseks **Kupong**.
3. Looge lehel **Vöötkoodi seadistus** uus vöötkood, mis kasutab äsja loodud vöötkoodi maski.
4. Looge lehel **Numbriseeriad** kaks uut numbriseeriat. Üks seeria on kupongi koodi ID jaoks ja teine seeria kupongi numbri jaoks. Kupongi koodi ID on kupongi iga koodi ainuidentifikaator. Kupongi number on kupongi ainuidentifikaator. Igal kupongil võib olla mitu koodi ja vöötkoodi, mis kupongi käivitavad.

    > [!NOTE]
    > Mõlema numbriseeria puhul tuleb määrata väljale **Ulatus** valik **Ettevõte**. Enamasti tuleks luua automaatselt mõlemad seerianumbrid.

5. Valige lehel **Kaubanduse parameetrid** vahekaardil **Vöötkoodid** varem loodud vöötkood.
6. Valige lehel **Commerce’i ühisparameetrid** vahekaardil **Numbriseeriad** kupongi numbrile ja kupongi koodi ID-le loodud numbriseeriad.
7. Nüüd võite lehe **Kupongid** avada ja uusi kuponge luua.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Kupongide osalise uuendamise mõju

Kupongi funktsioon hõlmab mitut eraldi funktsiooni. Commerce’i komponenti Headquarters (HQ) ja kanalit saab komponentide lõikes osaliselt värskendada. Seetõttu on oluline mõista, kuidas osalised uuendused kupongi funktsiooni tervikuna mõjutavad.

- **HQ-d uuendatakse osaliselt, kuid Commerce’i skaala üksust ja kassat ei uuendata.** HQ uuendamisel uuendatakse kupongi ja allahindluse lehti ning kaubanduse hinnamootorit uuendatakse samuti. Kui uuendada ainult ühte neist kahest komponendist, ei vasta mõned Commerce’i lehed hinna arvutamise andmetele. Seetõttu võib allahindluse arvutamisel ilmneda ootamatuid allahindluse arvutusi või tõrkeid.
- **HQ-d uuendatakse, kuid Commerce’i skaala üksust ja kassat ei uuendata (N-1).** Kuna kõiki kauplusi ei saa korraga uuendada, siis soovitame enne kaupluste uuendamist HQ-d uuendada. Stsenaariumi N-1 puhul ei ole kupongidega seotud uued funktsioonid saadaval kauplustes, mida pole veel uuendatud. Näiteks pakub kupongi funktsioon ridade „väljajätmist”. Kui kasutate allahindlusel ridade väljajätmist, siis ei rakendata neid varasemat versiooni kasutavas kaupluses.
- **HQ-d ei uuendata, kuid Commerce’i skaala üksust ja kassat uuendatakse (N+1).** Kuna uuendatud hinnamootor Commerce’i skaala üksuses suudab tulla hindade arvutamisel toime pärand-allahindluskoodidega, ei tohiks uuendusel olla selles stsenaariumis funktsioonidele mingit mõju.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
