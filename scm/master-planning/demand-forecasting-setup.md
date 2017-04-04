---
title: "Nõudluse prognoosi seadistus"
description: "Selles teemas kirjeldatakse seadistustoiminguid, mida tuleb nõudluse prognoosimiseks valmistumiseks teha."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanDefaultAlgorithmParameters, ReqDemPlanForecastParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72653
ms.assetid: c5fa4b09-512d-4349-ac51-cc13da69a160
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f629329f4f50bd7c8edcfd70641bace01a1c53aa
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-setup"></a>Nõudluse prognoosi seadistus

Selles teemas kirjeldatakse seadistustoiminguid, mida tuleb nõudluse prognoosimiseks valmistumiseks teha.  

Seadistustoimingud hõlmavad järgmiste andmete ja parameetrite seadistamist.

## <a name="item-allocation-key"></a>Kauba eraldamisvõti
Nõudluse prognoosi arvutatakse kaubale ja selle dimensioonidele ainult siis, kui kaup on osa kauba eraldamisvõtmest. Selle reegli aruandlusandmete rühma suure hulga üksusi, et nõudlus saab luua kiiremini. Kauba eraldise protsent peamisi ignoreeritakse, kui nõudlus on loodud. Prognoose luuakse ainult ajalooliste andmete põhjal. 

Kui prognoosi loomisel kasutatakse kauba eraldamisvõtit, peab kaup ja selle dimensioonid kuuluma ainult ühe kauba eraldamisvõtme juurde. 

Kauba eraldusvõtme varude arvestusühik (SKU) lisamiseks minge **kapten planeerimine**&gt;**install**&gt;**nõudluse prognoosimise**&gt;**kauba eraldamisvõtmed**. Kaubale kauba eraldamisvõtme määramiseks kasutage lehekülge **Kaupade määramine**.

## <a name="intercompany-planning-groups"></a>Kontsernisisesed plaanimisgrupid
Nõudluse prognoos loob ettevõteteülesed prognoosid. Microsoft Dynamics 365 operatsioonide planeeritud kokku ettevõtted on jaotatud ühe IC rühma planeerimine. Määrata ettevõtte, mis kauba eraldamisvõtmeid käsitlust nõudluse prognoosimiseks kohta siduda kauba eraldusvõtme planeerimine grupiliikme minnes kontsernisisese **kapten planeerimine**&gt;**Setup**&gt;**planeerimise rühmade kontsernisisese**. 

Vaikimisi, kui kauba eraldamisvõtmeid pole määratud kontserni planeerimise grupi liikmed, nõudluse prognoos arvutatakse kõik üksused, kõik kauba eraldamisvõtmeid määratud kõik Dynamics 365 toimingute ettevõtetele. Ettevõtte ja kauba eraldamisvõtmete täiendavad filtreerimissuvandid on saadaval leheküljel **Statistilise alusprognoosi loomine**. 

Vaadake üle prognoositavate kaupade arv. Mittevajalike kaupadega võivad Microsoft Azure'i masinõppe kasutamisel suurenenud kulud kaasneda.

## <a name="demand-forecasting-parameters"></a>Nõudluse prognoosimise parameetrid
Nõudluse prognoosimise parameetrite seadistamiseks avage **kapten planeerimine**&gt;**install**&gt;**nõudluse prognoosimise parameetrid**. Seadistus on globaalne, kuna nõudluse prognoosimine toimub ettevõteteüleselt. Teisisõnu rakendatakse seadistust kõigis ettevõtetes. 

Nõudluse prognoosimine loob koguselise prognoosi. Seetõttu peab väljal **Nõudluse prognoosi ühik** olema määratud mõõtühik, milles kogus peaks olema väljendatud. Kogumi ja protsentide jaotuse loogilisuse tagamiseks peaks mõõtühik olema kordumatu. Kogumi ja protsentide jaotuse kohta vt lisateavet artiklist [Alusprognoosi käsitsi korrigeerimine](manual-adjustments-baseline-forecast.md). Veenduge, et igal nõudluse prognoosimisse kaasatud SKU-na kasutataval mõõtühikul oleks mõõtühiku teisendusreegel ja üldise prognoosimise mõõtühik. Prognoosi loomise käitamisel logitakse kõik mõõtühikuta kaubad, nii et saate hõlpsalt seadistust korrigeerida. 

Nõudluse prognoosimist saab kasutada nii sõltuva kui ka sõltumatu nõudluse prognoosimiseks. Näiteks kui on valitud ainult ruut **Müügitellimus** ja kui kõik kaubad, mida arvestatakse nõudluse prognoosimisel, on müüdud, arvutab süsteem sõltumatu nõudluse. Kauba eraldamisvõtmetele ja nõudluse prognoosimisse saab siiski lisada olulisi alamkomponente. Kui ruut **Tootmisrida** on märgitud, arvutatakse sel juhul sõltuv prognoos. 

On kaks meetodid luua Dynamics 365 operatsioonide prognoos baseline. Saate prognoosimise mudeleid ajalooliste andmete peal kasutada või ajaloolised andmed prognoosi kopeerida. Nende kahe meetodi vahel saate valida väljal **Prognoosi koostamise strateegia**. Prognoosimudelite kasutamiseks valige **Azure'i masinõpe**. 

Kui klõpsate valikut **Prognoosi dimensioonid** lehekülje **Nõudluse prognoosimise parameetrid** vasakul paanil, saate valida ka nõudluse prognoosi loomisel kasutatavad prognoosi dimensioonid. Prognoosi dimensioon näitab prognoosile määratletud üksikasjade taset. Ettevõte, koht ja kauba eraldamisvõti on prognoosi kohustuslikud dimensioonid, kuid saate kasutada ka ladu, varude olekut, kliendigruppi, kliendikontot, riiki/regiooni, maakonda ja kaupa ning kõiki kauba dimensiooni tasemeid. 

Nõudluse prognoosimiseks kasutatavasse dimensioonide loendisse saate igal ajal prognoosi dimensioone juurde lisada. Samuti saate prognoosi dimensioone loendist eemaldada. Prognoosi dimensiooni lisamisel või eemaldamisel kaovad siiski käsitsi tehtud korrigeerimised. 

Kõik kaubad ei käitu nõudluse prognoosimise perspektiivist samal viisil. Sarnased kaubad saab koondada ühe kauba eraldamisvõtme alla ning seada kauba eraldamisvõtmeti parameetreid, nagu kande tüübid ja prognoosi meetodi seadistus. Klõpsake lehekülje **Nõudluse prognoosimise parameetrid** vasakul paanil valikut **Kauba eraldamisvõtmed**. 

Eelarve loomiseks Dynamics 365 operatsioonide kasutab masinõpet veebiteenust. Ühendust teenusega, peate sisestama Dynamics 365 toimingute järgmist kui logite Microsoft Azure masin õppe Studio:

-   veebiteenuse rakenduse programmeerimisliidese (API) võti;
-   veebiteenuse lõpp-punkti URL;
-   Azure'i salvestuskonto nimi;
-   Azure'i salvestuskonto võti.

**Märkus.** Azure'i salvestuskonto nime ja võtit on vaja ainult juhul, kui kasutate kohandatud salvestuskontot. Kui juurutate asutusesisese versiooni, peab olema tollilao konto Azure, et masinõpet teenust kasutada ajaloolisi andmeid. 

Nõudluse prognoosid loomiseks saate juurutada oma teenuseid kohapeal õppe Studio või Dynamics 365 toimingute nõudluse prognoosimise eksperimentide abil. Juurutamisstsenaariumid Dynamics 365 toimingute nõudluse prognoosimise eksperimendid on veebipõhine teenus on saadaval Dynamics 365 toiminguteks. Klõpsake lehel **Nõudluse prognoosimise parameetrid** vahekaarti **Azure'i masinõpe**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Seaded Dynamics 365 operatsioonide nõudluse prognoosimise õppe hooldus
Parameetreid, mida saab konfigureerida Dynamics 365 jaoks tegevuse nõudluse prognoosimise teenuse vaatamiseks minge **koondplaneerimise**&gt;**install**&gt;**nõudluse prognoosimise**&gt;**prognoosimise algoritmi parameetrid**. Selle **prognoosimise algoritmi parameetrid** lehel kuvatakse parameetrite vaikeväärtused. Neid parameetreid saab üle selle **nõudluse prognoosimise parameetrid** lehel. Parameetrite globaalseks ülekirjutamiseks kasutage vahekaarti **Üldine**, kauba eraldamisvõtmeti ülekirjutamiseks kasutage vahekaarti **Kauba eraldamisvõtmed**. Kauba eraldamisvõtme parameetrite ülekirjutamine mõjutab ainult selle kauba eraldamisvõtmega seostatud kaupade prognoosi.

<a name="see-also"></a>Vt ka
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)


