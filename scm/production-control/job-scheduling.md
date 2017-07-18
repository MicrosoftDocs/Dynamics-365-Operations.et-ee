---
title: "Tööde planeerimine"
description: "Selles artiklis antakse teavet tööde plaanimise kohta, mis on operatsioonide plaanimisest üksikasjalikum plaanimise vorm. Saate kasutada töö planeerimist selleks, et planeerida üksikuid töid või töökoja tellimusi, ja et juhtida tootmiskeskkonda."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19431
ms.assetid: aef37341-91d8-4263-80eb-35d9584be156
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 3c7224390ce336439c2e43188c19b4b93cf793b8
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017

---

# <a name="job-scheduling"></a>Tööde planeerimine

[!include[banner](../includes/banner.md)]


Selles artiklis antakse teavet tööde plaanimise kohta, mis on operatsioonide plaanimisest üksikasjalikum plaanimise vorm. Saate kasutada töö planeerimist selleks, et planeerida üksikuid töid või töökoja tellimusi, ja et juhtida tootmiskeskkonda.

Saate kasutada töö planeerimist selleks, et planeerida üksikuid töid või töökoja tellimusi, ja et juhtida tootmiskeskkonda. Töö planeerimine jaotab iga toimingu üksikuteks ülesanneteks või töödeks. Need tööd määratakse siis operatsiooniressurssidele, kes need ära teevad. Töö planeerimine võimaldab ka sünkroonida kõik tööd, millele valitud töö viitab. Saate määrata töö alguskuupäeva ja kellaaja või lõppkuupäeva ning kellaaja ja siis plaani käitada. Määratud aeg võib olenevalt planeerimissuunast olla algus- või lõppaeg. See funktsioon on kasulik näiteks siis, kui tööd saab korraga käitada ainult ühes masinas või kui soovite optimeerida tööd, mis käivitatakse iga ressursi puhul.

## <a name="tasks-in-the-job-scheduling-process"></a>Ülesanded tööde planeerimise protsessis
Tööde planeerimise protsess hõlmab järgmisi ülesandeid.

-   Jaotage operatsioonid töödeks.
-   Planeerige tööd seotud operatsioonile määratud ressursside kuupäevade ja aegade alusel.
-   Arvutage iga töö algus- ja lõppkellaajad. Saate kasutada piiratud võimsust veendumaks, et ajad ei kattu.
-   Määrake, millistel ressursigrupi ressursidel tööd käitada. Selle ülesande puhul on nõutav, et operatsioonile on määratud ressursigrupp. Töö planeerimine valib ressursid või ressursigrupid lühima täitmisaja alusel ja kaalub ka ressursside varasemaid reserveeringuid.
-   Tükeldage operatsioonid töödeks, kui käitate tööde planeerimist. Tööd planeeritakse kuupäeva ja kellaaja alusel, vastavalt tootmisprotsessi määratud tellimusele. Operatsiooni häälestus määrab tööd, mis planeerimisprotsessis tükeldatakse. Operatsioonile määratud protsessigrupp kontrollib, kas tööd luuakse. Töö on loodud üksnes juhul, kui sel on kindel kestus. Nt transpordi ajatöö on loodud, kui valitud operatsiooni transpordiaeg on määratud.

## <a name="scheduling-direction"></a>Planeerimise suund
Töid saab planeerida edasi või tagasi.

-   **Edasi** – kasutage edasisuunas planeerimist tootmise alustamiseks võimalikult vara. Seda teatakse ka tõukemeetodi nime all, kuna tootmine tõugatakse tootmisprotsessist läbi. Tootmine on ajastatud algama ja lõppema kõige varasematel võimalikel kuupäevadel.
-   **Tagasi** – kasutage tagasisuunas planeerimist tootmise alustamiseks võimalikult hilja. Seda teatakse ka tõmbemeetodi nime all, kuna see põhineb kuupäeval, millal tootmine peab olema lõpule viidud. Tagasisuunaline planeerimist arvutatakse tagasi hiliseima võimaliku kuupäevani, millal tootmist tuleks alustada, et see ei ületaks lõpptähtaega.

## <a name="finite-capacity"></a>Piiratud võimsus
Saate töid planeerida, kasutades piiratud võimsust. Kui kasutate piiratud võimsust, ei saa planeeritud võimsus olla suurem kui ressursile saadaolev võimsus. Kasutatav aeg on määratud vahemikuna, millal ressurss on saadaval ja võimsust ei ole millekski muuks reserveeritud. Piiratud võimsusel põhinev planeerimine tagab, et konkreetsel kuupäeval toimuva operatsiooni algus- ja lõppkellaajad ei kattu. Arvestatakse ressursivõimsust, mis on juba reserveeritud, ning arvestatakse ka kattuvaid algus- ja lõpuaegu. Piiratud võimsus määrab võimsuse koguse, mis peab olema ressursi jaoks saadaval, et saavutada selle ressursi optimaalne kasutamine. See määratlemine tasakaalustatakse operatsioonide lühima võimaliku täitmisaja arvutusega.

## <a name="finite-materials"></a>Piiratud materjalid
Piiratud materjalidel põhinev töö planeerimine tagab, et nõutavad materjalid on toimingu alguseks saadaval. Kaupade laovarude reeglid määratlevad need piirangud. Planeerimine kasutab vajaduste tükeldamist, et määrata, millal kaubakomponendid on saadaval. Kui planeerite piiratud materjale seadistamata, siis järeldab süsteem, et kõik kaubad on nõudmisel saadaval.

## <a name="finite-properties"></a>Piiratud atribuudid
Spetsiaalsetel atribuutidel põhinev töö planeerimine nõuab atribuutide täpsustamist tootmisprotsessi toimingute kohta. Need atribuudid peavad võimsuse reserveerimiseks olema täidetud.

## <a name="references"></a>Viited
Töö planeerimise käigus planeeritakse kõik praeguse tootmise viidatud tootmised. Kui tootmisel on üks või rohkem alltootmist, siis tuleb need planeerida samal ajal põhitootmisega, kuna põhitootmist ei saa alustada, kuni seonduvad alltootmised on lõpetatud.

## <a name="schedule-resources"></a>Ressursside plaanimine
Planeerimismootor uurib ressursside kombinatsioone, et tuvastada kombinatsioonid, mis nõuded täidavad. Saate määrata valikukriteeriumi, valides lehe **Parameetrite planeerimine** väljal **Esmase ressursi valik** ühe järgmistest väärtustest.

-   **Kestus** – planeerimismootor valib ressursi, millel on lühim täitmisaeg. **Märkus.** Kestuse alusel planeerimine võib põhjustada jõudluse langust, kui sama ressursigrupp sisaldab palju ressursse ja kasutatakse teiseseid operatsioone. Saate planeerida maksimaalselt 32 ressurssi operatsiooni kohta. Kui ületate selle koguse, kuvatakse teabelogiteade ja töö planeerimine ei otsi parimat alternatiivset ressurssi.
-   **Prioriteet** – planeerimismootor valib ressursi, millel on kõrgeim prioriteet, kui kahel või enamal ressursil on samased võimalused ja tasemed. Ressurssil, millel on sellel väljal madalaim arvväärtus, on kõrgeim prioriteet.

Töö planeerimise käivitamisel plaanib süsteem ressursse piirangute alusel, mis on määratletud ressursi parameetrites. Saate ressursside võimsust kontrollida, kasutades kalendrisätteid. Süsteem arvutab planeerimisprotsessi ajal ressursside koormused. **Märkus.** Tootmiste puhul, mis kasutavad operatsioonide planeerimise funktsiooni, saate käivitada töö planeerimise pärast operatsioonide planeerimist. Kui te operatsioonide planeerimist ei kasuta, saate käivitada üksnes tööde planeerimise.

## <a name="maximum-capacities-for-resources-per-job-order"></a>Ressursside maksimaalsed võimsused tööde järjekorra kohta
Ressursid määratakse töödele töö planeerimise kaudu. Saate kehtestada ressurssidele maksimaalsed võimsused tööde järjekorra kohta. Näiteks saate seadistada süsteemile piirangu, et ühele tootmistellimusele ei tohi kuluda rohkem kui 50 protsenti koguvõimsusest. See häälestus annab teile suurema kontrolli ressursside planeerimise üle töö planeerimise tasemel. Seega võib selle abil probleeme ennetada, kui samaaegseks tootmiseks ei ole piisavalt võimsust.

## <a name="resource-efficiency"></a>Ressursside efektiivsus
Töö planeerimine võtab arvesse ressurssidele määratud efektiivsusprotsente. Efektiivsusprotsendid vähendavad või suurendavad ressursi jaoks reserveeritud aja hulka. Seetõttu suureneb või väheneb ka täitmisaeg. Arvutamiseks kasutatakse järgmist valemit: planeerimisaeg = aeg × 100 ÷ efektiivsusprotsent. Selles valemis hõlmab *Aeg* nii käitamisaega kui ka häälestusaega.




