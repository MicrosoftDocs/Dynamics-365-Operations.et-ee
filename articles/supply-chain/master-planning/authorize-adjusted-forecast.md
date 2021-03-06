---
title: Korrigeeritud prognoosi autoriseerimine
description: Kõiki prognoosi andmeid ei pea kohe autoriseerima. Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud. Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanImportForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72734
ms.assetid: cb8fd809-605a-4a8b-a390-636edfec21f9
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 42137b9eb24e14518244d87e72e9ea1295be4485
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188954"
---
# <a name="authorize-an-adjusted-forecast"></a>Korrigeeritud prognoosi autoriseerimine

[!include [banner](../includes/banner.md)]

Kõiki prognoosi andmeid ei pea kohe autoriseerima. Selles artiklis selgitatakse, kuidas määrata perioodi, milleks prognoos on autoriseeritud. Samuti selgitatakse, kuidas autoriseerida prognoosiks kindlaid ettevõtteid ja prognoosimudeleid.

Kõiki prognoosi andmeid ei pea kohe autoriseerima. Prognoosi autoriseerimisele saate määrata algus- ja lõppkuupäevad. See funktsioon lubab kindlad vahemikud külmutada. 

Määratud algus- ja lõppkuupäevad peavad vastama loodud prognoosi vahemiku algus‑ ja lõppkuupäevadele. Süsteem rakendab seda piirangut ja korrigeerib automaatselt kuupäevi, kui see peaks vajalik olema. 

Viimati loodud prognoosi üksikasju saate vaadata lehekülje **Autoriseerimine** vahekaardilt **Üksikasjad**. 

Saate valida ettevõtted ja prognoosimudelid, mida prognoosi kasutama autoriseerida. Ruudustik hõlmab vaikimisi kõiki ettevõtteid, millele prognoositud nõudlus on loodud. Igale ettevõttele on eeltäidetud prognoosimudel, mis vastab praegusele koondplaneerimise parameetrites seadistatud prognoosiplaanile. Selle prognoosimudeli saate siiski vahetada ettevõttele kuuluva mistahes prognoosimudeli vastu. Kui valitud ettevõtte jaoks ei loodud prognoositud nõudluse andmeid, kuvatakse importimise ajal hoiatusteade. 

Oluline on mõista, kuidas töötab ruut **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised**. Kui olete statistilist alusprognoosi käsitsi korrigeerinud, lubatakse korrigeeritud väärtusi kasutada isegi juhul, kui see ruut on tühi. Pärast autoriseerimist muudatusi siiski eiratakse. Seepärast on järgmisel korral loodud prognoos ainult statistiline prognoos ega sisalda ühtki käsitsi tehtud korrigeerimist, isegi kui ruut **Kanna käsitsi tehtud korrigeerimised üle nõudluse prognoosi** on valitud. Seetõttu võite võtta ruutu **Salvesta nõudluse alusprognoosis käsitsi tehtud korrigeerimised** kui mehhanismi, mis laseb teil säilitada või hüljata kõik käsitsi tehtud muudatused.

## <a name="additional-resources"></a>Lisaressursid

[Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)

[Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]