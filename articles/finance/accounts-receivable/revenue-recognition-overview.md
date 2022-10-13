---
title: Tulu tuvastamise ülevaade (sisaldab videot)
description: See artikkel annab teavet tulu tuvastamise funktsiooni kohta. See funktsioon pakub paindlikku raamistikku, mis võimaldab teil määratleda ettevõtte erireeglid nii tuluhinna kui ka tulugraafiku kajastamiseks mitme elemendiga tellimuste puhul.
author: bking
ms.date: 03/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5bf07356b5613f438034f8dabac7db197e69a6c8
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644026"
---
# <a name="revenue-recognition-overview"></a>Tulu tuvastamise ülevaade

[!include [banner](../includes/banner.md)]

>[!NOTE]
>See funktsioon on taunitud oktoober 2023, uued kasutajad peaksid kasutama kordustellimuse arveldust.

Mitut elementi müüvad ettevõtted (nt tooted, teenused, kordustellimused jne) peavad olema võimelised tagama mitme elemendiga tellimusi, et saaks tulu tuvastada kindlate ettevõtte- ja valdkonnaspetsiifiliste juhiste alusel.

Tulu tuvastamise, sh kogumifunktsiooni kasutamist ei toetata Commerce'i kanalites (e-kaubandus, kassa, kõnekeskus). Tulu tuvastamisega konfigureeritud kaupu ei tuleks Commerce'i kanalites loodud tellimustele või kannetele lisada.

Üldiselt saab tulu tuvastamise protsessi kasutada järgmiste ülesannete täitmiseks.

* Tulude jaotamine aitab tagada, et vastav tulu hind tuvastatakse mitme elemendiga tellimuste komponentide väärtuse alusel.
* Lükake edasi tulu, põhinedes tulugraafikul, mis kajastab lepingujärgset ajavahemikku ja tulu tuvastamise protsente aja jooksul.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Tulu [tuvastamise viis Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) videos (vt ülalpool) [sisaldub finantsis ja operatsioonides,](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) mis on saadaval YouTube.

Tulu tuvastamise funktsioon pakub paindlikku raamistikku, mis võimaldab teil määratleda ettevõtte erireeglid nii tuluhinna kui ka tulugraafiku kajastamiseks.

Väljastatud tooteid kasutatakse müügitellimuse dokumentide tulu tuvastamiseks. Välja saadetud tooted sisaldavad seadistust, mis on vajalik tuluhinna ja tulugraafiku määramiseks. Müügitellimus võib pärineda aja- ja materjalikulu projektist.

Ettevõtted saavad kasutada tulugraafiku funktsiooni tuluhinna funktsiooni kasutamata. Seetõttu kasutatakse hindu müügitellimuse ridadel kas tulu või edasilükkunud tuluna. Kui müügitellimuse real on olemas tulugraafik, lükatakse müügitellimuse rea hind edasi. Kui müügitellimuse real pole tulugraafikut, sisestatakse müügitellimuse rea hind tulukonto arvele.

Tuluhind arvutatakse kas müügitellimuse kinnitamisel või arve sisestamisel. Enne arve sisestamist tuluhinna eelvaate nägemiseks peate müügitellimuse kinnitama.

Kui müügitellimus on kinnitatud, luuakse ka eeldatav tulugraafik, kui mõnel müügitellimuse real on tulugraafik. Müügitellimuse arveldamisel kustutatakse eeldatav tulugraafik ja see asendatakse tegeliku tulu kajastamise graafikuga.

Tulu kajastamise graafiku üksikasjad kinnitatakse iga müügitellimuse rea kohta. Tänu sellele saab tulu tuvastamise haldur vaadata üksikasju ja saab vabastada read tulule, kui lepinguline kohustus on lõpule viidud. Iga perioodi lõpus saab tulu tuvastamise haldur luua tulutöölehe, et vabastada kõik graafikuread, mille tähtaeg on määratud kuupäevaga samal päeval või sellest varem. Seda tulutöölehte ei sisestata kohe. Seetõttu on tulu tuvastamise halduri kaudu võimalik kinnitada, et õiged summad vabastatakse edasilükkunud tulult tegelikule tulule.

Kui lepingumuudatus põhjustab uue müügitellimuse rea lisamise kas olemasolevale müügitellimusele või uuele müügitellimusele, saab tuluhinna kõigi müügitellimuste ridade korrigeerimiseks ümberjaotamise protsessi käitada.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

