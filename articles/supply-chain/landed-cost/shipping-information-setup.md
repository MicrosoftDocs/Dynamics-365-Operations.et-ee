---
title: Saatmisteabe häälestamine
description: See artikkel kirjeldab, kuidas seadistada lähetusteavet väljaminev kulumoodulile.
author: Weijiesa
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 62277f66a36817e83b4c0bf101aa7b6cc14ecccb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882630"
---
# <a name="shipping-information-setup"></a>Saatmisteabe häälestamine

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada lähetusteavet väljaminev **kulumoodulile**.

## <a name="description-of-goods"></a><a name="description-of-goods"></a>Kauba kirjeldus

Kaubakirjeldused aitavad tuvastada kaupade teekonna, saatmiskonteineri või foolio ning selles sisalduvad kaubad. Kaupade kirjelduse saate valida saatmiskonteineri päises või foolio päises.

Kaubakirjeldustega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Kaupade kirjeldus**. Seal saate vaadata, avada, luua ja kustutada kaubakirjelduste kirjeid. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Kauba kirjeldus | Sisestage seda kirjeldust kasutavate kaubatüübi ainu-ID nimi/number. |
| Kirjeldus | Sisestage selle kategooria kaubatüübi kirjeldus. |

## <a name="vessels"></a><a name="vessels"></a>Laevad

Laev on saatmisettevõtte või agentuuri kasutatava laeva või aluse kordumatu nimi. Teekonna loomisel peate selle jaoks alati valima või sisestama laeva. Kui kasutate sageli samu laevu, saate uue teekonna loomise kiirendamiseks ja hõlbustamiseks luua iga laeva jaoks laevakirje, mis võimaldab kasutajatel valida laeva loendist selle asemel, et sisestada selle nimi või number iga kord käsitsi.

Laevadega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Laevad**. Seal saate laevade kirjeid vaadata, avada, luua ja kustutada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Laev | Sisestage teekonnal kaupade transportimiseks kasutatava laeva ainu-ID nimi/number. |
| Kirjeldus | Sisestage laeva kirjeldus. Tavaliselt sisaldab kirjeldus laeva nime ja saatmisettevõtet/agenti. |
| Tarneviis | Valige aluse kasutatav tarneviis (nt _Õhk_, _Ookean_ või _Rong_). |

## <a name="exporters"></a>Eksportijad

Iga eksportijakirje tuvastab hankija või eksportija, kelle saab määrata teekonna hankijaks. Eksportijat saab seostada teekonnaga ja kasutada aruandluseks.

Eksportijatega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Eksportijad**. Seal saate eksportijate kirjeid vaadata, avada, luua ja kustutada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Eksportija | Sisestage teekonnal transporditavate kaupade eksportija ainu-ID nimi/number. |
| Kirjeldus | Sisestage eksportija kirjeldus. Tavaliselt sisaldab kirjeldus saatmisettevõtte/agendi täisnime. |

## <a name="commodity-codes"></a>Kaubaartiklite koodid

Kaubaartiklite koode kasutatakse aitamaks tolliasutusel tuvastada teekonna kaupasid ja arvutada nende tollimaksumäärasid. Kaubaartiklite koodid saate valida lehel **Väljastatud tooted**.

Kaubaartiklite koodidega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Kaubaartiklite koodid**. Seal saate kaubaartiklite koodide kirjeid vaadata, avada, luua ja kustutada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Kaubaartikkel | Sisestage seda tüüpi kaubaartikli kordumatu kood. |
| Kirjeldus | Sisestage kaubaartiklitüübi kirjeldus. |

## <a name="customs-description"></a>Tolli kirjeldus

Tolli kirjeldused aitavad kaupu tuvastada tolliga seotud eesmärkidel. Tolli kirjelduse saate valida lehel **Väljastatud tooted** või ostutellimuse ridadel.

Tolli kirjeldustega töötamiseks avage **Väljalaadimiskulu \> Saatmisteabe seadistamine \> Tolli kirjeldus**. Seal saate vaadata, avada, luua ja kustutada tolli kirjelduste kirjeid. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Tolli kirjeldus | Sisestage seda tüüpi tolliklassifikatsiooni kordumatu kood. Sageli on see kood ametlik kirjeldus, mille tolliasutus on esitanud kaupade kirjelduse ja kvalitatiivse väärtuse jaoks. |
| Kirjeldus | Sisestage tolliklassifikatsiooni kirjeldus. |
