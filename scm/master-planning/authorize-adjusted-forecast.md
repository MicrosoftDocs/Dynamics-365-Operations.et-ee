---
title: Lubada kohandatud ilm
description: "Kõiki prognoosi andmeid ei pea kohe autoriseerima. Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud. Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f151f4b4290df0b2bf1b5d1159654bd248a439b1
ms.lasthandoff: 03/31/2017


---

# <a name="authorize-an-adjusted-forecast"></a>Lubada kohandatud ilm

Kõiki prognoosi andmeid ei pea kohe autoriseerima. Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud. Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid.

Kõiki prognoosi andmeid ei pea kohe autoriseerima. Prognoosi autoriseerimisele saate määrata algus- ja lõppkuupäevad. See funktsioon lubab kindlad vahemikud külmutada. 

Algus- ja lõppkuupäevad, teie määratud peab vastama selle algus- ja lõppkuupäevad ämber, loodud prognoos. Süsteemi jõustab see piirang ja automaatselt kuupäevad, kui korrigeerimine ei ole vajalik. 

Viimati loodud prognoosi üksikasju saate vaadata lehekülje **Autoriseerimine** vahekaardilt **Üksikasjad**. 

Saate valida ettevõtted ja prognoosimudelid, mida prognoosi kasutama autoriseerida. Ruudustik hõlmab vaikimisi kõiki ettevõtteid, millele prognoositud nõudlus on loodud. Igale ettevõttele on eeltäidetud prognoosimudel, mis vastab praegusele koondplaneerimise parameetrites seadistatud prognoosiplaanile. Selle prognoosimudeli saate siiski vahetada ettevõttele kuuluva mistahes prognoosimudeli vastu. Kui valitud ettevõtte jaoks ei loodud prognoositud nõudluse andmeid, kuvatakse importimise ajal hoiatusteade. 

Oluline on mõista, kuidas töötab ruut **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised**. Kui olete teinud käsitsi muudatusi statistiliste lähtealuse Ilmaennustus, korrigeeritud väärtust kasutamine on lubatud, isegi kui see märkeruut on tühjendatud. Pärast autoriseerimist muudatusi siiski eiratakse. Seepärast on järgmisel korral loodud prognoos ainult statistiline prognoos ega sisalda ühtki käsitsi tehtud korrigeerimist, isegi kui ruut **Kanna käsitsi tehtud korrigeerimised üle nõudluse prognoosi** on valitud. Seetõttu võite võtta ruutu **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised** kui mehhanismi, mis laseb teil säilitada või hüljata kõik käsitsi tehtud muudatused.

<a name="see-also"></a>Vt ka
--------

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


