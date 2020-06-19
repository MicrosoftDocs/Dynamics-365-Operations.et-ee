---
title: Maksesageduste häälestamine
description: Microsoft Dynamics 365 Human Resources kasutab maksesagedust aastase soodustuse palga arvutamiseks, töövõtja iga makseprioodil makstava soodustuse preemia summa määramiseks ja pakkujatele tehtavate maksete sageduse määramiseks.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5d562b64a161891bf34b0dfa94fbf68325e21b5
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429953"
---
# <a name="set-up-payment-frequencies"></a>Maksesageduste häälestamine

Microsoft Dynamics 365 Human Resources kasutab maksesagedust aastase soodustuse palga arvutamiseks, töövõtja iga makseprioodil makstava soodustuse preemia summa määramiseks ja pakkujatele tehtavate maksete sageduse määramiseks.

Soodustuse maksmise sagedused kasutavad teisendustegureid, et teisendada soodustuse makseperioode kuude, poolaasta, kahe nädala ja nädala ning igapäevase maksesageduse vahel. See võimaldab ettevõtetel määrata soodustuse plaanis maksesageduste vahelise sõltuvuse.

Teisendamistegurite väljad määravad teisendustegurid maksesagedustest tavapärase makseperioodini ja võimaldavad süsteemil maksesageduste vahel teha arvutusi. Teisendusteguri summa määratleb ka soodustuse preemia summa, mille töövõtja peaks igal maksesagedusel tasuma.

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Maksesagedused**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Maksesagedus** | Kordumatu maksesageduse nimi. |
   | **Kirjeldus** | Maksesageduse kirjeldus. |
   | **Periood** | Sobiv periood, mis ühtib kõige paremini soodustuse pakkuja ja töövõtja maksesagedusega. Perioodi loend koosneb tavapärastest makseperioodidest. |
   | **Makseperioodide arv** | Makseperioodide arv, mis näitab, kui tihti soodustuse pakkujale või töövõtjatele makstakse. Seda summat kasutatakse töövõtja aastase soodustuse palga summa arvutamiseks. |
   | **Aastane tuletustegur** | Maksesageduse aastane teisendustegur. Näiteks igakuise maksesageduse aastane teisendustegur on: </br></br>(12 igakuist makset / 1 aasta) = 12 |
   | **Pooleaastane tuletustegur** | Maksesageduse pooleaastane teisendustegur. Näiteks igakuise maksesageduse pooleaastane teisendustegur on: </br></br>(12 igakuist makset / 2 korda aastas) = 6 |
   | **Kord kvartalis tuletustegur** | Maksesageduse kvartaalne teisendustegur. Näiteks igakuise maksesageduse kvartaalne teisendustegur on: </br></br>(12 igakuist makset / 4 kvartalit) = 3 |
   | **Igakuine tuletustegur** | Maksesageduse igakuine teisendustegur. Näiteks igakuise maksesageduse igakuine teisendustegur on: </br></br>(12 igakuist makset / 12 kuud) = 1 |
   | **Maksesageduse kaks korda kuus tuletustegur** | Maksesageduse kaks korda kuus teisendustegur. Näiteks igakuise maksesageduse kaks korda kuus teisendustegur on: </br></br>(12 igakuist makset / 24 (2 korda kuus)) = 0,5 | 
   | **Kahenädalane tuletustegur** | Maksesageduse aastane teisendustegur. Näiteks igakuise maksesageduse aastane teisendustegur on: </br></br>(12 igakuist makset / 26 nädalat) = 0,461538 |
   | **Nädalane tuletustegur** | Maksesageduse aastane teisendustegur. Näiteks igakuise maksesageduse aastane teisendustegur on: </br></br>(12 igakuist makset / 52 nädalat) = 0,230769 |
   | **Igapäevane tuletustegur** | Maksesageduse aastane teisendustegur. Näiteks igakuise maksesageduse aastane teisendustegur on: </br></br>(12 igakuist makset / 365 päeva) = 0,032877 |
   | **Tunnine tuletustegur** | Maksesageduse aastane teisendustegur. Näiteks igakuise maksesageduse aastane teisendustegur on: </br></br>(12 igakuist makset / 2080 tundi) = 0,005769

4. Valige käsk **Salvesta**. 
