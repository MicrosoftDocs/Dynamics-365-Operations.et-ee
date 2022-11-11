---
title: Ostutaotlused
description: See artikkel kirjeldab ostutaotlusi.
author: t-benebo
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: d9d55186307b18f4c3be78ae0828b08d3c987aad
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740680"
---
# <a name="purchase-requisitions"></a>Ostutaotlused

[!include [banner](../../includes/banner.md)]

Koondplaneerimine saab kinnitatud ostutaotlusi täiendada. Seega ei pea kasutajad kasutama ostutaotluste katteks ostutellimuste loomise töövoogu. Selle asemel saab ostutaotlusi katta koondplaneerimisega. Selle funktsiooni tõttu saab ostutaotlus luua ostutellimuse, üleviimistellimuse või tootmistellimuse, sõltuvalt seotud tootele määratud väärtusest **Plaanitud tellimuse tüüp**.

## <a name="enable-master-plans-to-include-requisitions"></a>Koondplaanide seadistamine taotluste lubamine

Koondplaani laovarude arvutamiseks taotluse kaasamiseks tehke järgmist.

1. Avage **Koondplaneerimine** \> **Seadistus** \> **Plaanid** \> **Koondplaanid**.
1. Looge või valige koondplaan.
1. Määrake FastTab-il **Üldine** suvandil **Kaasa taotlused** valikut *Jah*.
1. Korrake samme 2 ja 3 iga täiendava koondplaani puhul, kuhu soovite tellimused lisada.

## <a name="approved-requisitions-time-fence"></a>Kinnitatud taotluste ajapiir

*Kinnitatud ostutellimuste ajapiir* määrab, kui palju (päevi) tagasi koondplaan kinnitatud täiendamistaotluste nõuet kaasab. Saate määrata kinnitatud taotluse ajapiiri nii laovarude grupi tasemel kui ka koondplaani tasemel.

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a>Laovarude grupi kinnitatud taotluse ajapiiri määramine

1. Avage **Koondplaneerimine** \> **Seadistus** \> **Laovarud** \> **Laovarude grupid**.
1. Looge või valige laogrupp.
1. Määrake kiirkaardil **Muu** väli **Kinnitatud ostutaotluste ajapiir (päevades)** päevade arvule, mis ajapiiri kaasata.
1. Korrake samme 2 ja 3 iga täiendava laovarude grupi jaoks, millele soovite kinnitatud ostutellimuste ajapiiri seadistada.

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a>Individuaalsetele koondplaanidele kinnitatud taotluse ajapiiri määramine

Individuaalsele koondplaanile kinnitatud taotluse ajapiiri määramisel alistab säte kõigi rakendatavate laovarude grupi ajapiiri sätte.

1. Avage **Koondplaneerimine** \> **Seadistus** \> **Plaanid** \> **Koondplaanid**.
1. Looge või valige koondplaan.
1. Määrake kiirkaardil **Ajapiirid päevades** väli **Kinnitatud ostutaotluste ajapiir (päevades)** päevade arvule, mis ajapiiri kaasata.
1. Korrake samme 2 ja 3 iga täiendava koondplaani jaoks, millele soovite kinnitatud ostutellimuste ajapiiri seadistada.

> [!IMPORTANT]
> Kinnitatud taotluse ajapiire ei toetata optimeerimise planeerimisel. Kuni neid toetatakse, ignoreeritakse kõiki väärtusi, mille sisestate väljale **Kinnitatud ostutaotluste ajapiir (päevades)**.

## <a name="independent-supply-regardless-of-coverage-code"></a>Sõltumatu tarne, sõltumata laovarude koodist

Ostutaotlused on alati kaetud sõltumatute plaanitud tellimustega, olenemata laovarude koodist. Selline käitumine tagab ostutaotluste ja täiendustellimuste vahelise selge jälgimise ja töövoo.

### <a name="example-1"></a>Näide 1

Toode on häälestatud nii, et sellel oleks **katvuse koodi** väärtus *Min/max*. Sellel on järgmised varude ja ostutellimuse olekud:

- Vaba kaubavaru kogus = 10.
- Minimaalne laokogus = 15.
- Maksimaalne laokogus = 20.
- Olemas on ühe tüki ostutaotlus. Selle taotlemise kuupäev on täna.

Kui koondplaneerimine töötab, luuakse kaks plaanitud tellimust: üks 10 ühiku jaoks, et täiendada varud maksimaalse koguseni, ja üks tüki kohta, et ostutaotlust täiendada.

### <a name="example-2"></a>Näide 2

Toode on häälestatud nii, et sellel oleks **katvuse koodi** väärtus *Min/max*. Sellel on järgmised varude ja ostutellimuse olekud:

- Vaba kaubavaru kogus = 17.
- Minimaalne laokogus = 15.
- Maksimaalne laokogus = 20.
- Olemas on ühe tüki ostutaotlus. Selle taotlemise kuupäev on täna.

Kui koondplaneerimine töötab, luuakse ostutaotluse täiendamiseks üks plaanitud tellimus ühe tüki kohta.

### <a name="example-3"></a>Näide 3

Toode on seadistatud nii, et sellel on väärtus **Laovarude kood** väärtusega *Periood* ja perioodi pikkus on 7 päeva. Sellel on järgmised varude, müügitellimuste ja ostutellimuste olekud:

- Vaba kaubavaru kogus = 0.
- Olemas on müügitellimus viiele eksemplarile. Selle on eeldatav lähetuskuupäev täna, millele on lisatud üks päev.
- Olemas on kolme tüki ostutaotlus. Selle taotlemise kuupäev on täna pluss kolm päeva.

Kui koondplaneerimine töötab, luuakse kaks plaanitud tellimust: üks kolme ühiku jaoks, et täiendada ostutaotlust ja üks viie ühiku jaoks, et müügitellimuse nõue taastada.

> [!NOTE]
> Pärast ostutaotlusega seotud plaanitud tellimuse kinnitamist edastab planeerimismootor sidumise ostutaotlusele. Kui hiljem leitakse, et kinnitatud tellimusel puudub mõni ostutaotluse täitmiseks vajalik kogus, loob süsteem erinevuse jaoks uue plaanitud tellimuse.

Täpsemat teavet ostutaotluste kohta vt teemast [Ostutaotluste ülevaade](../../procurement/purchase-requisitions-overview.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]