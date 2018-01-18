---
title: "Kupongide loomine jaemüügi jaoks"
description: "Selles teemas antakse ülevaade jaemüügikupongidest ja selgitatakse, kuidas neid seadistada."
author: scott-tucker
manager: AnnBe
ms.date: 05/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailCoupon, RetailParameters, RetailSharedParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: scotttuc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 7e05361bf865e44ba6073198fba94d7102b1ed19
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="create-coupons-for-retail-sales"></a>Kupongide loomine jaemüügi jaoks

[!include[banner](includes/banner.md)]


## <a name="overview-of-coupons"></a>Kupongide ülevaade

Kupongid on koodid ja vöötkoodid, mida kasutatakse jaeallahindluste lisamiseks kannetele. Igal kupongil võib olla mitu koodi ja igal koodil võivad olla oma kehtivuskuupäevad. 

Iga kupong on seotud ühe jaeallahindlusega. Allahindlusega seotud hinnagrupid määratlevad kliendid, kes saavad kupongi kasutada, või kanalid, kus kupong kehtib. 

Põhimõtteliselt on kupongid jaeallahindlustele lisanduv kinnitus. Kupongil on vajalikud kupongi koodid ja vöötkoodid, millel on nende koodide kuupäevavahemikud. Kupongil on ka valikulised kasutuspiirid ja kliendile vajalikud atribuudid. Allahindlus annab toodete kogumi, millele kupong kehtib. Allahindluse hinnagrupid annavad klientide kogumi, kanalid või kataloogid, millele kupong kehtib.

Kupongi loomiseks tuleb luua allahindlus ja kupong eraldi. Seejärel tuleb need siduda, valides allahindluse Microsoft Dynamics 365 for Retailis kupongi lehel. 

> [!NOTE]
> Kui kupong on allahindlusega seotud, muutub mitu välja Microsoft Dynamics 365 for Retaili allahindluse lehel kirjutuskaitsuks, kuna neid hallatakse kupongi sätetega. Nende väljade hulka kuuluvad oleku ja standardsete kuupäevavahemike väljad.

### <a name="limited-use-coupons"></a>Piiratud kasutusega kupongid

Kupongid saab konfigureerida piiratud kasutusega kupongidena. Kasutuspiiri saab määratleda kliendi või kanali kaupa või üldise piirina. Seda piiri rakendatakse koodi või vöötkoodi sisestamisel või skannimisel kassas või müügitellimuse sisestamisel. Kupong registreeritakse kasutatuks, kui tellimus, millega kupong seotud on, on täidetud.

Kupongi piirmäär rakendatakse kupongi koodi kohta. Näiteks ühekordselt kasutatavat kupongi, millel on kaks kupongi koodi, saab kasutada kaks korda: üks kord kummagi kupongi koodi kohta. Kummagi kupongi koodi saab eraldi aktiivseks määrata.

## <a name="managing-coupons"></a>Kupongide haldamine

Allahindlus ja kupong tuleb luua eraldi. Seejärel tuleb need siduda, valides kupongi lehel allahindluse. Kui kupong on allahindlusega seotud, muutub mitu allahindluse välja kirjutuskaitstuks, kuna neid hallatakse kupongi sätetega. Nende väljade hulka kuuluvad oleku ja standardsete kuupäevavahemike väljad.  

Põhimõtteliselt on kupongid nüüd jaeallahindlustele lisanduv kinnitus. Kupongil on kupongi koodid ja vöötkoodid, millel on nende koodide kuupäevavahemikud, kasutuspiirid ja kliendile vajalik atribuut. Allahindlus annab toodete kogumi, millele kupong kehtib. Allahindluse hinnagrupid annavad klientide kogumi, kanalid või kataloogid, millele kupong kehtib.

## <a name="system-setup-for-coupons"></a>Süsteemi seadistus kupongide puhul 

Enne kupongi seadistamist tuleb seadistada kupongi vöötkood ja kaks kupongi numbriseeriat. 

1.  Looge lehel **Maski märgid** kupongi koodile uus maski märk. Valida saab mis tahes kasutamata märki.
2.  Looge lehel **Vöötkoodi maski häälestus** uus vöötkoodi mask. Määrake välja **Tüüp** väärtuseks **Kupong**.
3.  Looge lehel **Vöötkoodi seadistus** uus vöötkood, mis kasutab äsja loodud vöötkoodi maski.
4.  Looge lehel **Numbriseeriad** kaks uut numbriseeriat. Üks seeria on kupongi koodi ID jaoks ja teine seeria kupongi numbri jaoks. Kupongi koodi ID on kupongi iga koodi ainuidentifikaator. Kupongi number on kupongi ainuidentifikaator. Igal kupongil võib olla mitu koodi ja vöötkoodi, mis kupongi käivitavad.

    > [!NOTE]
    > Mõlema numbriseeria puhul tuleb määrata väljale **Ulatus** valik **Ettevõte**. Enamasti tuleks luua automaatselt mõlemad seerianumbrid.

5.  Valige lehel **Jaemüügi ühisparameetrid** vahekaardil **Vöötkoodid** varem loodud vöötkood.
6.  Valige lehel **Jaemüügi parameetrid** vahekaardil **Numbriseeriad** kupongi numbrile ja kupongi koodi ID-le loodud numbriseeriad.
7.  Nüüd võite lehe **Kupongid** avada ja uusi kuponge luua.

## <a name="the-effect-of-partial-updates-on-coupons"></a>Kupongide osalise uuendamise mõju

Kupongi funktsioon hõlmab Dynamics 365 for Retailis mitut eraldi funktsiooni. Microsoft Dynamics 365 for Retail Headquartersit (HQ) ja kanalit saab komponentide lõikes osaliselt uuendada. Seetõttu on oluline mõista, kuidas osalised uuendused kupongi funktsiooni tervikuna mõjutavad.

- **HQ-d uuendatakse osaliselt, kuid Retaili serverit ja kassat ei uuendata.** HQ uuendamisel uuendatakse kupongi ja allahindluse lehti ning jaemüügi hinnamootorit uuendatakse samuti. Kui uuendada ainult ühte neist kahest komponendist, ei vasta mõned Retaili lehed hinna arvutamise andmetele. Seetõttu võib allahindluse arvutamisel ilmneda ootamatuid allahindluse arvutusi või tõrkeid.
- **HQ-d uuendatakse, kuid Retaili serverit ja kassat ei uuendata (N-1).** Kuna kõiki jaekauplusi ei saa korraga uuendada, siis soovitame enne jaekaupluste uuendamist HQ-d uuendada. Stsenaariumi N-1 puhul ei ole kupongidega seotud uued funktsioonid saadaval kauplustes, mida pole veel uuendatud. Näiteks pakub kupongi funktsioon ridade „väljajätmist”. Kui kasutate allahindlusel ridade väljajätmist, siis ei rakendata neid varasemat versiooni kasutavas jaekaupluses.
- **HQ-d ei uuendata, kuid Retaili serverit ja kassat uuendatakse (N+1).** Kuna uuendatud hinnamootor Retaili serveris suudab tulla hindade arvutamisel toime pärand-allahindluskoodidega, ei tohiks uuendusel olla selles stsenaariumis funktsioonidele mingit mõju.

