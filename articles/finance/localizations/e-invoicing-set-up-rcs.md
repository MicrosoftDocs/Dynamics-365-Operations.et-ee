---
title: Saate häälestada regulatiivset konfiguratsiooniteenust (RCS).
description: See artikkel selgitab, kuidas seadistada regulatiivset konfiguratsiooniteenust (RCS).
author: gionoder
ms.date: 10/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 32ced98925ee66e02f0b073b4acbd586666ac20c
ms.sourcegitcommit: 1ecfc1d8afb2201ab895ae6f93304ba2b120f14b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2022
ms.locfileid: "9710777"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Saate häälestada regulatiivset konfiguratsiooniteenust (RCS).

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas seadistada regulatiivset konfiguratsiooniteenust (RCS).

## <a name="turn-on-globalization-features"></a>Globaliseerimisfunktsioonid sisse lülitamine

1. Logige oma RCS-i kontole sisse.
2. Valige paan **Funktsioonihaldus**.
3. Valige tööruumis **Funktsioonihaldus** loendist suvand **Globaliseerimise funktsioonid** ja seejärel valige **Luba kohe**.

Globaliseerimisfunktsiooni tööruumi **paan** peaks nüüd ilmuma RCS-i põhipaanil.

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>Määrake parameetrid RCS integratsioonile koos Elekrtoonilise arveldusega

1. Tööruumi **Globaliseerimisfunktsioonid** jaotisest **Seotud sätted** valige **Elektroonilise aruandluse parameetrid**.
2. Parameetrite esmakordsel häälestamisel palutakse teil luua ühendus elutsükli teenustega (LCS). Valige **siin, et luua ühendus elutsükli teenustega** ja pärast ühenduse loomise käivitamist valige **OK**.

    > [!IMPORTANT]
    > Riikides ja regioonides, kus andmete elukoht on jõustatud ja kui teie RCS on ette vaadatud eri regioonis, kus LCS on ressursid, võite RCS-is saada järgmise ühenduse tõrketeate: "RCS-is ei leitud HTTP-ressurssi, mis vastaks URI-le". Valige nupp **OK**. Võite saada teise tõrketeate RCS-is: "Dynamicsi elutsükli teenuste kasutaja loa loomine nurjus kasutaja nimel (). Palun võtke ühendust oma süsteemiadministraatoriga."
    >  
    > See juhtub, kuna LCS on globaalne teenus ja seda kasutatakse USA regioonis. Elukohapoliitika tõttu ei saa teie praeguse regiooni RCS LCS-ga ühendust luua. Nende kahe võimaluse all on kaks võimalikku lahendust:
    > - Kustutage RCS oma praegusest regioonist ja looge see UUESTI USA regioonis.
    > - Ignoreerige tõrkeid ja jätkake elektroonilise arvelduse häälestusega. Need tõrked ei mõjuta elektroonilise arveldamise funktsioone.

3. Vahekaardil Elektroonilise **arveldamise teenuse** **lõpp-punkti URI** Microsoft Azure väljal sisestage oma geograafia jaoks sobiv teenuse lõpp-punkt, nagu näha järgmises tabelis.

    | Azure'i andmekeskuse geograafiline piirkond | Teenuse lõpp-punkti URI |
    |----------------------------|----------------------|
    | Ameerika Ühendriigid              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Euroopa                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Ühendkuningriik             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Aasia                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Jaapan                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Šveits                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Brasiilia                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Araabia Ühendemiraadid       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Austraalia                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Kanada                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Prantsusmaa                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | India                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Norra                     | <p>`https://gw.no-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | Lõuna-Aafrika Vabariik               | <p>`https://gw.za-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. Vaadake üle ja sisestage väljale **Rakenduse ID** fikseeritud väärtus **0cdb527f-a8d1-4bf8-9436-b352c68682b2**. Kontrollige, et sisestatud oleks ainult globaalselt kordumatu kood (GUID) ja et väärtus ei sisaldaks muid sümboleid, nt tühikuid, komasid, punkte või jutumärke.
4. Sisestage **LCS-i keskkonna ID väljale oma elutsükli** teenuste (LCS) keskkonna ID Microsoft Dynamics. See väärtus on viide finants- või tarneahela halduskeskkonnale, mida kasutate elektroonilise arveldamise teenusega. ID [saamiseks logige LCS-i](https://lcs.dynamics.com/) sisse, **avage projekt ja seejärel vaadake vahekaardi Keskkonna** **·** **haldamine jaotises Keskkonna üksikasjad välja Keskkonna ID.**

    > [!IMPORTANT]
    > Kui elektroonilise arveldamise lisandmoodul on installitud LCS-i mitmesse finants- või tarneahela halduskeskkonda, kasutage alati kõige viimasena installitud keskkonna ID-d. Kui otsustate lisandmooduli uude keskkonda installida pärast elektroonilise arveldamise funktsiooni seadistamist ja töötamist, **siis värskendage RCS-i LCS-i keskkonna ID** välja uusimale väärtusele.

5. Valige **Salvesta** ja sulgege seejärel leht.

## <a name="configuration-providers"></a>Konfiguratsiooni pakkujad

Saate kasutada konfiguratsioonipakkujaid, et eristada elektroonilise aruandluse (ER) konfiguratsioonide omanikku, mida kasutatakse elektroonilise arveldamise protsessides ja omanike globaliseerimisfunktsioonid. Kõigi Microsofti antud ja globaalses hoidlas avaldatud globaliseerimisfunktsioonid on konfiguratsioonipakkuja seatud **Microsoftile** (`http://microsoft.com`).

Saate korrigeerida ainult ER konfiguratsioone ja globaliseerimisfunktsioonid, mis kuuluvad aktiivse konfiguratsiooni pakkujale. Saate kasutada neid konfiguratsioone ja funktsioone mallidena, et luua konfiguratsioone ja funktsioone, mis kuuluvad aktiivse konfiguratsiooni pakkujale, nii et saate neid korrigeerida.

Kõigepealt looge konfiguratsiooni pakkujad. Seejärel seadistage üks neist aktiivseks. Microsofti konfiguratsioonipakkujat ei saa **aktiivseks** muuta.

### <a name="create-a-configuration-provider"></a>Konfiguratsioonipakkuja loomine

1. Valige tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** suvand **Konfiguratsioonipakkujad**.
2. Valige suvand **Uus**.
3. Sisestage **väljale** Nimi konfiguratsioonipakkuja kordumatu nimi.
4. Sisestage **väljale Interneti-aadress** konfiguratsioonipakkuja kordumatu URL.
5. Valige **Salvesta** ja sulgege seejärel leht.

### <a name="select-a-configuration-provider-as-active"></a>Valige aktiivsena konfiguratsioonipakkuja.

1. Valige konfiguratsiooni pakkujate loendist konfiguratsioonipakkuja, mida soovite seada aktiivseks.
2. Valige **Määra aktiivseks**.

## <a name="import-er-configurations-from-the-global-repository"></a>ER-konfiguratsioonide importimine globaalsest hoidlast

1. Valige tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** suvand **Konfiguratsioonipakkujad**.
2. Valige konfiguratsiooni pakkujate loendis Microsoft ja **seejärel** valige **Hoidlad**.
3. Valige **globaalne** ja seejärel tegevuspaanil käsk **Avatud**.
4. Importige järgmised ER-mudelid:

    - **Kliendiarve kontekstimudel**
    - **Arve mudel**
    - **Fiskaaldokumendid** (brasiilia stsenaariumite puhul, kui vaja)
    - **Vastusesõnumi mudel**

5. Kui **arve mudeli vastendamist** automaatselt ei imporditud, importige see.
6. Sulgege leht.
