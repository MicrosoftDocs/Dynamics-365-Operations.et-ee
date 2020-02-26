---
title: Tulu tuvastamise ülevaade
description: Sellest teemast leiate teavet tulu tuvastamise funktsiooni kohta. See funktsioon pakub paindlikku raamistikku, mis võimaldab teil määratleda ettevõtte erireeglid nii tuluhinna kui ka tulugraafiku kajastamiseks mitme elemendiga tellimuste puhul.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: c5a3a90b0065f8cd076117818df810cf10202d29
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/07/2020
ms.locfileid: "3030964"
---
# <a name="revenue-recognition-overview"></a>Tulu tuvastamise ülevaade

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Tulu tuvastamise funktsiooni ei saa funktsioonihalduse kaudu sisse lülitada. Praegu peate selle sisselülitamiseks kasutama konfiguratsioonivõtmeid.

Mitut elementi müüvad ettevõtted (nt tooted, teenused, kordustellimused jne) peavad olema võimelised tagama mitme elemendiga tellimusi, et saaks tulu tuvastada kindlate ettevõtte- ja valdkonnaspetsiifiliste juhiste alusel.

Üldiselt saab tulu tuvastamise protsessi kasutada järgmiste ülesannete täitmiseks.

* Tulude jaotamine aitab tagada, et vastav tulu hind tuvastatakse mitme elemendiga tellimuste komponentide väärtuse alusel.
* Lükake edasi tulu, põhinedes tulugraafikul, mis kajastab lepingujärgset ajavahemikku ja tulu tuvastamise protsente aja jooksul.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Video [Tulu tuvastamise kasutamine rakenduses Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (kuvatud eespool) on kaasatud [Finance and Operationsi esitusloendisse](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadaval YouTube'is.

Tulu tuvastamise funktsioon pakub paindlikku raamistikku, mis võimaldab teil määratleda ettevõtte erireeglid nii tuluhinna kui ka tulugraafiku kajastamiseks.

Väljastatud tooteid kasutatakse müügitellimuse dokumentide tulu tuvastamiseks. Välja saadetud tooted sisaldavad seadistust, mis on vajalik tuluhinna ja tulugraafiku määramiseks. Müügitellimus võib pärineda aja- ja materjalikulu projektist.

Ettevõtted saavad kasutada tulugraafiku funktsiooni tuluhinna funktsiooni kasutamata. Seetõttu kasutatakse hindu müügitellimuse ridadel kas tulu või edasilükkunud tuluna. Kui müügitellimuse real on olemas tulugraafik, lükatakse müügitellimuse rea hind edasi. Kui müügitellimuse real pole tulugraafikut, sisestatakse müügitellimuse rea hind tulukonto arvele.

Tuluhind arvutatakse kas müügitellimuse kinnitamisel või arve sisestamisel. Enne arve sisestamist tuluhinna eelvaate nägemiseks peate müügitellimuse kinnitama.

Kui müügitellimus on kinnitatud, luuakse ka eeldatav tulugraafik, kui mõnel müügitellimuse real on tulugraafik. Müügitellimuse arveldamisel kustutatakse eeldatav tulugraafik ja see asendatakse tegeliku tulu kajastamise graafikuga.

Tulu kajastamise graafiku üksikasjad kinnitatakse iga müügitellimuse rea kohta. Tänu sellele saab tulu tuvastamise haldur vaadata üksikasju ja saab vabastada read tulule, kui lepinguline kohustus on lõpule viidud. Iga perioodi lõpus saab tulu tuvastamise haldur luua tulutöölehe, et vabastada kõik graafikuread, mille tähtaeg on samal päeval või varasem tema määratud kuupäevast. Seda tulutöölehet ei sisestata kohe. Tänu sellele saab tulu tuvastamise haldur kinnitada, et õiged summad vabastatakse edasilükkunud tulult tegelikule tulule.

Kui lepingumuudatus põhjustab uue müügitellimuse rea lisamise kas olemasolevale müügitellimusele või uuele müügitellimusele, saab tuluhinna kõigi müügitellimuste ridade korrigeerimiseks ümberjaotamise protsessi käitada.
