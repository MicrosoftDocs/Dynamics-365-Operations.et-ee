---
title: Nõudlusepõhiste materjalinõuete planeerimise (DDMRP) ülevaade
description: See artikkel annab teavet nõudlusepõhiste materjalinõuete planeerimise (DDMRP) kohta, pakkumise ja nõudluse dekodeerimisel põhinev planeerimismetoodika.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: d894b83afe822e013c0c4375e5cfe5e7e8ac8d1d
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186573"
---
# <a name="demand-driven-material-requirements-planning-ddmrp-overview"></a>Nõudlusepõhiste materjalinõuete planeerimise (DDMRP) ülevaade

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Aastate jooksul on ettevõtted kasutanud materjalinõuete planeerimist (MRP) süsteemina toote tootmiseks vajalike materjalide ja komponentide arvutamiseks. Tarneahelaid on nüüd muudetud. Osadel on pikemad täitmisajad, kuna need on pärit ülemerest. Seetõttu on paljud ettevõtted teatanud, et seal esineb lao- või üleladusid, sest nad ei tea, kui palju laovarusid ladustada. Samuti on olemas rohkem turu kõikumisi (vahel valesti prognoositud) ning kliendid nõuavad tooteid lühikese täitmisajaga. Seetõttu on tarneahela puudujääke üle kogu maailma. Lisaks annavad MRP tööriistad sageli planeerijatele teha tuhandetel toiminguid. Seetõttu on raske teada, kuhu keskenduda. Sageli on paljude nende probleemide lahendus lülituda nõudlusepõhise materjali nõuete planeerimisele (DDMRP).

DDMRP on pakkumise ja nõudluse dekodeerimisel põhinev planeerimismetoodika. Dekodeerimise saavutamiseks seadistatakse dekodeerimispunkti kaubad. Nende kaupade puhul säilitatakse puhvrid, et tagada õige laovaru säilitatakse. Pakkumise ja nõudluse dekodeerimisega välditakse "whip-mõju", kuna hälbeid ei läbita ahelas. (Vastavalt *sellele*, kuidas väikesed nõudluse kõikumised jaemüügitasemel võivad põhjustada progresseeruvalt suuremaid nõudluse kõikumisi hulgimüügi, levitaja, tootja ja toormaterjali tarnija tasemel.) Iga puhver on mõeldud osa keskmise kasutamise katmiseks ning seda saab korrigeerida ka nõudluse nõudluse katmiseks.

DDMRP on tõestanud, et on väärtuseline planeerimismetoodika muutuvatele keskkondadele, kus kliendi kõikumise ajad on kumulatiivsetest täitmisaegadest lühem.

## <a name="the-five-components-of-ddmrp"></a>DDMRP viis komponenti

DDMRP-s on viis jadakomponenti (etappi). Esimesed kolm komponenti määravad põhiselt nõudlusepõhiste materjalinõuete plaanimismudeli algse jakomponentide konfiguratsiooni. Kaks viimast komponenti määravad metoodika päevase operatsiooni.

1. **[Strateegiline varude positsioon](ddmrp-inventory-positioning.md)** – tuvastage hankeahela võrgu dekodeerimise punktid. Punktide dekodeerimisel kasutatakse tarneahela kindlaid punkte, kus saate asetada laopuhvri, mida jälgite ja täiendate.
2. **[Puhverprofiilid ja](ddmrp-buffer-profile-and-levels.md)** tasemed – määratlege iga dekodeerimispunkti puhul puhvri suurused (miinimumkogus, maksimaalne kogus ja lisatellimuse punkt) ning lisatellimuse kogus.
3. **[Dünaamilised puhvri korrigeerimised](ddmrp-buffer-profile-and-levels.md#dynamic-adjustments)** – kohandage puhvritasemeid, mis põhinevad erinevatele tootmisparameetritele või planeeritud tuleviku sündmustele.
4. **[Nõudlusepõhine planeerimine](ddmrp-planning.md)** – looge tarnetellimused nii, nagu need on nõutud. Need tarnetellimused hõlmavad tootmistellimusi, ostutellimusi ja lao üleviimistellimusi.
5. **[Väga läbiviiv ja](ddmrp-visual-and-collaborative-execution.md)** nähtav käivitamine – käivitage tarnetellimused visualiseerimise abiga.

DDMRP-i kasutavad tavaliselt tootjad, omavad mitmetasemelist kooslust. Kuid seda saab rakendada ka jaotus- ja jaemüügivõrkudele.

## <a name="ddmrp-in-dynamics-365-supply-chain-management"></a>DDMRP aastal Dynamics 365 Supply Chain Management

DDMRP on kaasatud Microsofti ja Dynamics 365 Supply Chain Management ei nõua täiendavaid litsentsitasusid. Tarneahela halduses on DDMRP-funktsioon lisatud olemasolevasse koondplaneerimise **moodulisse**. Kuid selleks on vaja kasutada plaanimise optimeerimise lisandmoodulit. 

DDMRP on integreeritud olemasolevate plaanimisseadistustega Tarneahela halduses ja seda kasutatakse koos nende seadistustega, et jõuda teie ettevõtte jaoks õigesse planeerimiskonfiguratsiooni. Seda kontrollib uus laovarude kood, mis erineb täielikult perioodist, min/max, vajadusest jne. See pole uus moodul ja see ei asenda olemasolevaid plaanimisfunktsioone. Kuid see annab teile kasutamiseks rohkem funktsioone.
