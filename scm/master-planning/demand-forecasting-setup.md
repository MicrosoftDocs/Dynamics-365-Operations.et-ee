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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5074f3ded26f55c6244feba9fcf0199c81cad468
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="demand-forecasting-setup"></a>Nõudluse prognoosi seadistus

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse seadistustoiminguid, mida tuleb nõudluse prognoosimiseks valmistumiseks teha.  

Seadistustoimingud hõlmavad järgmiste andmete ja parameetrite seadistamist.

## <a name="item-allocation-key"></a>Kauba eraldamisvõti
Nõudluse prognoosi arvutatakse kaubale ja selle dimensioonidele ainult siis, kui kaup on osa kauba eraldamisvõtmest. Seda reeglit jõustatakse suurele hulgale kaupadele, et nõudluse prognoosi loomine oleks kiirem. Nõudluse prognooside loomisel eiratakse kauba eraldamisvõtme protsenti. Prognoose luuakse ainult ajalooliste andmete põhjal. 

Kui prognoosi loomisel kasutatakse kauba eraldamisvõtit, peab kaup ja selle dimensioonid kuuluma ainult ühe kauba eraldamisvõtme juurde. 

Kauba eraldamisvõtmele varude arvestusühiku (SKU) lisamiseks minge jaotisse **Koondplaneerimine** &gt; **Seadistus** &gt; **Nõudluse prognoos** &gt; **Kauba eraldamisvõtmed**. Kaubale kauba eraldamisvõtme määramiseks kasutage lehekülge **Kaupade määramine**.

## <a name="intercompany-planning-groups"></a>Kontsernisisesed plaanimisgrupid
Nõudluse prognoos loob ettevõteteülesed prognoosid. Microsoft Dynamics 365 for Operationsis grupeeritakse koos plaanitud ettevõtted ühte kontsernisisesesse plaanimisgruppi. Ettevõtteti nõudluse prognoosimisel arvestatavate kauba eraldamisvõtmete määratlemiseks tuleks kauba eraldamisvõti seostada kontsernisisese plaanimisgrupi liikmega, minnes jaotisse **Koondplaneerimine** &gt; **Seadistus** &gt; **Kontsernisisesed plaanimisgrupid**. 

Kui kontsernisisese plaanimisgrupi liikmetele ei ole määratud ühtki kauba eraldamisvõtit, arvutatakse nõudluse prognoos vaikimisi kõigile kaupadele, mis on määratud kõigile kauba eraldamisvõtmetele kõigis Dynamics 365 for Operationsi ettevõtetes. Ettevõtte ja kauba eraldamisvõtmete täiendavad filtreerimissuvandid on saadaval leheküljel **Statistilise alusprognoosi loomine**. 

Vaadake üle prognoositavate kaupade arv. Mittevajalike kaupadega võivad Microsoft Azure'i masinõppe kasutamisel suurenenud kulud kaasneda.

## <a name="demand-forecasting-parameters"></a>Nõudluse prognoosimise parameetrid
Nõudluse prognoosimise parameetrite seadistamiseks minge jaotisse **Koondplaneerimine** &gt; **Seadistus** &gt; **Nõudluse prognoosimise parameetrid**. Seadistus on globaalne, kuna nõudluse prognoosimine toimub ettevõteteüleselt. Teisisõnu rakendatakse seadistust kõigis ettevõtetes. 

Nõudluse prognoosimine loob koguselise prognoosi. Seetõttu peab väljal **Nõudluse prognoosi ühik** olema määratud mõõtühik, milles kogus peaks olema väljendatud. Kogumi ja protsentide jaotuse loogilisuse tagamiseks peaks mõõtühik olema kordumatu. Kogumi ja protsentide jaotuse kohta vt lisateavet artiklist [Alusprognoosi käsitsi korrigeerimine](manual-adjustments-baseline-forecast.md). Veenduge, et igal nõudluse prognoosimisse kaasatud SKU-na kasutataval mõõtühikul oleks mõõtühiku teisendusreegel ja üldise prognoosimise mõõtühik. Prognoosi loomise käitamisel logitakse kõik mõõtühikuta kaubad, nii et saate hõlpsalt seadistust korrigeerida. 

Nõudluse prognoosimist saab kasutada nii sõltuva kui ka sõltumatu nõudluse prognoosimiseks. Näiteks kui on valitud ainult ruut **Müügitellimus** ja kui kõik kaubad, mida arvestatakse nõudluse prognoosimisel, on müüdud, arvutab süsteem sõltumatu nõudluse. Kauba eraldamisvõtmetele ja nõudluse prognoosimisse saab siiski lisada olulisi alamkomponente. Kui ruut **Tootmisrida** on märgitud, arvutatakse sel juhul sõltuv prognoos. 

Alusprognoosi loomiseks on Dynamics 365 for Operationsis kaks võimalust. Saate prognoosimise mudeleid ajalooliste andmete peal kasutada või ajaloolised andmed prognoosi kopeerida. Nende kahe meetodi vahel saate valida väljal **Prognoosi koostamise strateegia**. Prognoosimudelite kasutamiseks valige **Azure'i masinõpe**. 

Kui klõpsate valikut **Prognoosi dimensioonid** lehekülje **Nõudluse prognoosimise parameetrid** vasakul paanil, saate valida ka nõudluse prognoosi loomisel kasutatavad prognoosi dimensioonid. Prognoosi dimensioon näitab prognoosile määratletud üksikasjade taset. Ettevõte, koht ja kauba eraldamisvõti on prognoosi kohustuslikud dimensioonid, kuid saate kasutada ka ladu, varude olekut, kliendigruppi, kliendikontot, riiki/regiooni, maakonda ja kaupa ning kõiki kauba dimensiooni tasemeid. 

Nõudluse prognoosimiseks kasutatavasse dimensioonide loendisse saate igal ajal prognoosi dimensioone juurde lisada. Samuti saate prognoosi dimensioone loendist eemaldada. Prognoosi dimensiooni lisamisel või eemaldamisel kaovad siiski käsitsi tehtud korrigeerimised. 

Kõik kaubad ei käitu nõudluse prognoosimise perspektiivist samal viisil. Sarnased kaubad saab koondada ühe kauba eraldamisvõtme alla ning seada kauba eraldamisvõtmeti parameetreid, nagu kande tüübid ja prognoosi meetodi seadistus. Klõpsake lehekülje **Nõudluse prognoosimise parameetrid** vasakul paanil valikut **Kauba eraldamisvõtmed**. 

Prognoosi loomiseks kasutab Dynamics 365 for Operations masinõppe veebiteenust. Teenusega ühenduse loomiseks peate Microsoft Azure'i Machine Learning Studiosse sisselogimiseks andma Dynamics 365 for Operationsile järgmist teavet:

-   veebiteenuse rakenduse programmeerimisliidese (API) võti;
-   veebiteenuse lõpp-punkti URL;
-   Azure'i salvestuskonto nimi;
-   Azure'i salvestuskonto võti.

**Märkus.** Azure'i salvestuskonto nime ja võtit on vaja ainult juhul, kui kasutate kohandatud salvestuskontot. Kui juurutate asutusesisest versiooni, peab teil olema Azure'is kohandatud salvestuskonto, et masinõppe teenus pääseks ajaloolistele andmetele juurde. 

Nõudluse prognooside loomiseks saate juurutada oma teenuse, kasutades masinõppe stuudio või Dynamics 365 for Operationsi nõudluse prognoosimise katseid. Dynamics 365 for Operationsi nõudluse prognoosimise katsete veebiteenusena juurutamise juhised on saadaval Dynamics 365 for Operationsis. Klõpsake lehel **Nõudluse prognoosimise parameetrid** vahekaarti **Azure'i masinõpe**.

## <a name="settings-for-the-dynamics-365-for-operations-demand-forecasting-machine-learning-service"></a>Dynamics 365 for Operationsi nõudluse prognoosimise masinõppe teenuse sätted
Dynamics 365 for Operationsi nõudluse prognoosimise teenuse jaoks konfigureeritavate parameetrite vaatamiseks minge jaotisse **Koondplaneerimine** &gt; **Seadistus** &gt; **Nõudluse prognoos** &gt; **Prognoosi algoritmi parameetrid**. Lehel **Prognoosi algoritmi parameetrid** kuvatakse parameetrite vaikeväärtused. Saate need parameetrid üle kirjutada lehel **Nõudluse prognoosimise parameetrid**. Parameetrite globaalseks ülekirjutamiseks kasutage vahekaarti **Üldine**, kauba eraldamisvõtmeti ülekirjutamiseks kasutage vahekaarti **Kauba eraldamisvõtmed**. Kauba eraldamisvõtme parameetrite ülekirjutamine mõjutab ainult selle kauba eraldamisvõtmega seostatud kaupade prognoosi.

<a name="see-also"></a>Vt ka
--------

[Sissejuhatus nõudluse prognoosimisse](introduction-demand-forecasting.md)

[Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)

[Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)




