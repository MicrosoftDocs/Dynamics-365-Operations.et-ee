---
title: Mitmeetapilise teekonna marsruudi seadistamine
description: Selles teemas kirjeldatakse mitmeetapiliste teekonna marsruutide seadistamist Väljalaadimiskulu mooduli jaoks.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 45e32c59c79389bcab15dd07d1bbd33d7ff34340
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021560"
---
# <a name="multi-leg-journey-setup"></a>Mitmeetapilise teekonna marsruudi seadistamine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse mitmeetapiliste teekonna marsruutide seadistamist **Väljalaadimiskulu** mooduli jaoks.

## <a name="legs"></a>Etapid

Etappide abil tuvastatakse teekonna marsruudi eri osasid. Iga etapi koostamisel valitakse siht- ja lähtesadamad ning transpordimeetod, mida selles etapis kasutatakse. Iga etapiga saab seostada täitmisajad. Täitmisajad aitavad saadetist jälgida ja nende abil saab arvutada teekonna kaupade prognoositava tarnekuupäeva. Kui teekonna marsruudi üks etapp lõpetatakse, saab teekonna olekut, saatmiskonteinerit ja seotud ostutellimuse ridu jälgimiskontrolli seadistuse kaudu värskendada. Etappe saab kasutada üks teekonna marsruudi mall või korduvkasutada mitu teekonna marsruudi malli. Konteineri laadimine, tolli ja kohalik transport on tavaliselt seadistatud etappidena ja nende jaoks kasutatakse mittespetsiifilist saatmissadamat.

Etappidega töötamiseks avage **Väljalaadimiskulu \> Mitmeetapilise teekonna marsruudi seadistamine \> Etapid**. Seal saate etappide kirjeid vaadata, avada, luua ja kustutada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Etapp | Sisestage teekonna marsruudi etapi kordumatu ID nimi/number. |
| Kirjeldus | Sisestage teekonna marsruudi etapi kirjeldus. Tavaliselt tuuakse kirjelduses ära siht- ja lähtesadamad või teekonna marsruudi etapp. |
| Lähtesadam | Sisestage etapi kaupade päritolukoht. |
| Sihtsadam | Sisestage etapi kaupade sihtkoht. |
| Tarneviis | Sisestage etapi transpordimeetod. |

## <a name="journey-templates"></a>Teekonna mallid

Teekonna marsruudi mall määratleb mitmeetapilise teekonna marsruudi kahe sadama vahel, mida kaubad teekonna jooksul läbivad. Teekonna marsruudi etapid liidetakse, et määratleda aeg, mis on vajalik kaupade liikumiseks hankija päritolukohast lõppsihtlattu. Kui etapid seatakse teekonna marsruudi malli teatud järjestuses, määratlevad täitmisajad iga etapi kuupäevad ning teekonna, konteineri ja teekonna osturidade oleku. [Jälgimise juhtimiskeskuses](delivery-information-setup.md) seadistatakse teekonna marsruudi malli moodustavate etappidega seotud täitmisajad. Teekonna marsruudi malli kasutatakse ka teekonna automaatsete kulude seadistamisel. Kui teekonna marsruut on määratletud, saab automaatsete kulude lehel määratleda kaupade transpordiga seotud kulu.

Teekonna marsruudi mallidega töötamiseks avage **Väljalaadimiskulu \> Mitmeetapilise teekonna marsruudi seadistamine \> Teekonna marsruudi mallid**. Seal saate teekonna marsruudi malle vaadata, avada, luua ja kustutada.

Määrake iga teekonna marsruudi malli jaoks päises järgmised väljad.

| Field | Kirjeldus |
|---|---|
| Teekonna mall | Sisestage teekonna marsruudi malli kordumatu ID nimi/number. Teekonna marsruudi mall kirjeldab tavaliselt teekonna marsruudi lähtekohta ja sihtkohta. |
| Kirjeldus | Sisestage teekonna marsruudi malli kirjeldus. Tavaliselt tuuakse kirjelduses ära siht- ja lähtesadamad ja liikumisviis. |

Jaotises **Read** lisage rida teekonna marsruudi iga etapi jaoks ja seadke read järjekorda. Ridade järjekorra muutmiseks kasutage tööriistariba **ülesnoolt** ja **allanoolt**. Järgmises tabelis kirjeldatakse iga rea jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Etapp | Valige teekonna marsruudile lisatav etapp. |
| Kirjeldus | Etapi kirjeldus. |
| Lähtesadam | Etapi kaupade päritolukohaks olev sadam. See sadam on sihtsadam, mida kasutatakse teekonna automaatsete kulude määratlemiseks. |
| Sihtsadam | Etapi kaupade lõppsihtkoht. |
| Tarneviis | Etapis kasutatav tarnemeetod. |
| Teekonna lähtesadam | Kui etapi jaoks määratletud sadamat kasutatakse automaatsete kulude määratlemiseks, märkige see ruut, et määrata see teekonna marsruudi lähtesadamaks. See sadam kuvatakse teekonna päises. |
| Teekonna sihtsadam | Kui etapi jaoks määratletud sadamat kasutatakse automaatsete kulude määratlemiseks, märkige see ruut, et määrata see teekonna marsruudi sihtsadamaks. See sadam kuvatakse teekonna päises. |
| Saatmisettevõte | Valige etapis kasutatav saatmisettevõte. |

## <a name="activities"></a>Tegevused

Lehel **Tegevused** olevad sätted määravad tegevusetüübid, mis võivad etapi sihtsadamas toimuda. Kasutajad, kes töötavad lehel **Kõik saatmiskonteinerid**, saavad teha valiku nende väärtuste hulgast, kui nad prognoosivad iga tegevuse kestust ja märgivad võrdluse eesmärgil üles tegeliku kestuse.

Tegevuste seadistamiseks avage **Väljalaadimiskulu \> Mitmeetapilise teekonna marsruudi seadistamine \> Tegevused**. Seal saate toimingupaani nuppude abil tegevusi lisada, eemaldada ja redigeerida.

Järgmises tabelis kirjeldatakse ruudustiku iga tegevuse jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Tegevus | Tegevuse nimi. |
| Kirjeldus | Tegevuse kirjeldus. |
| Saatmisettevõte | Tegevusega seostatud saatmisettevõtte hankija konto. |
