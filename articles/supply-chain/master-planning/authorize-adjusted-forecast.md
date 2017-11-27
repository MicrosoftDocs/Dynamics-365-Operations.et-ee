---
title: Korrigeeritud prognoosi autoriseerimine
description: "Kõiki prognoosi andmeid ei pea kohe autoriseerima. Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud. Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5ce38e94ae4c7b28b4e182018add7c046f685e46
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="authorize-an-adjusted-forecast"></a>Korrigeeritud prognoosi autoriseerimine

[!include[banner](../includes/banner.md)]


Kõiki prognoosi andmeid ei pea kohe autoriseerima. Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud. Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid.

Kõiki prognoosi andmeid ei pea kohe autoriseerima. Prognoosi autoriseerimisele saate määrata algus- ja lõppkuupäevad. See funktsioon lubab kindlad vahemikud külmutada. 

Määratud algus- ja lõppkuupäevad peavad vastama loodud prognoosi vahemiku algus‑ ja lõppkuupäevadele. Süsteem rakendab seda piirangut ja korrigeerib automaatselt kuupäevi, kui see peaks vajalik olema. 

Viimati loodud prognoosi üksikasju saate vaadata lehekülje **Autoriseerimine** vahekaardilt **Üksikasjad**. 

Saate valida ettevõtted ja prognoosimudelid, mida prognoosi kasutama autoriseerida. Ruudustik hõlmab vaikimisi kõiki ettevõtteid, millele prognoositud nõudlus on loodud. Igale ettevõttele on eeltäidetud prognoosimudel, mis vastab praegusele koondplaneerimise parameetrites seadistatud prognoosiplaanile. Selle prognoosimudeli saate siiski vahetada ettevõttele kuuluva mistahes prognoosimudeli vastu. Kui valitud ettevõtte jaoks ei loodud prognoositud nõudluse andmeid, kuvatakse importimise ajal hoiatusteade. 

Oluline on mõista, kuidas töötab ruut **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised**. Kui olete statistilist alusprognoosi käsitsi korrigeerinud, lubatakse korrigeeritud väärtusi kasutada isegi juhul, kui see ruut on tühi. Pärast autoriseerimist muudatusi siiski eiratakse. Seepärast on järgmisel korral loodud prognoos ainult statistiline prognoos ega sisalda ühtki käsitsi tehtud korrigeerimist, isegi kui ruut **Kanna käsitsi tehtud korrigeerimised üle nõudluse prognoosi** on valitud. Seetõttu võite võtta ruutu **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised** kui mehhanismi, mis laseb teil säilitada või hüljata kõik käsitsi tehtud muudatused.

<a name="see-also"></a>Vt ka
--------

[Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)

[Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md)




