---
title: "Nõudluse prognoosimise ülevaade"
description: "Nõudluse prognoosimist kasutatakse müügitellimuste sõltumatu nõudluse ja klienditellimuste mistahes lahtisidestuspunktist sõltuva nõudluse ennustamiseks. Täiustatud nõudluse prognoos vähendamise eeskirjades on ideaalne lahendus mass kohandamine."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72004
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9152616b81e7873426f296376b5e57c94439379d
ms.lasthandoff: 03/31/2017


---

# <a name="demand-forecasting-overview"></a>Nõudluse prognoosimise ülevaade

Nõudluse prognoosimist kasutatakse müügitellimuste sõltumatu nõudluse ja klienditellimuste mistahes lahtisidestuspunktist sõltuva nõudluse ennustamiseks. Täiustatud nõudluse prognoos vähendamise eeskirjades on ideaalne lahendus mass kohandamine.

Alusprognoosi loomiseks edastatakse kannete ajaloo kokkuvõte Azure'is hostitud Microsoft Azure'i masinõppe teenusele. Teenust ei jagata kasutajate vahel, mistõttu saab seda hõlpsalt tööstuspõhistele nõuetele kohandada. Dynamics 365 operatsioonide abil visualiseerida prognoos, prognoos kohandada ja vaadata tulemuslikkuse võtmenäitajate (KPI) prognoosi täpsuse kohta.

## <a name="key-features-of-demand-forecasting"></a>Nõudluse prognoosimise võtmefunktsioonid
Järgnevalt on toodud mõned nõudluse prognoosimise peamised funktsioonid:

-   ajaloolistel andmetel põhineva statistilise alusprognoosi loomine;
-   dünaamilise prognoosi dimensioonide kogu kasutamine;
-   nõudluse trendide, usaldusvahemike ja prognoosi korrigeerimiste visualiseerimine;
-   korrigeeritud prognoosi planeerimisprotsessides kasutamise autoriseerimine;
-   võõrväärtuste eemaldamine;
-   prognoosi täpsuse mõõdikute loomine.

## <a name="major-themes-in-demand-forecasting"></a>Nõudluse prognoosimise põhiteemad
Nõudluse prognoosimisse on rakendatud kolm põhiteemat.

-   **Modulaarsus** – nõudluse prognoos on modulaarne ja hõlpsalt konfigureeritav. Saab lülitada funktsioone sisse ja välja, muutes konfiguratsioonivõti kell **kaubanduse**&gt;**varude eelarve**&gt;**nõudluse prognoosimise**.
-   **Korduvkasutamise Microsoft pinu** – Microsoft käivitas masinõpet platvormi veebruaris 2015. Kohapeal õpet, mis on nüüd osa Microsoft Cortana Analytics komplekti, saate kiiresti ja lihtsalt luua ennustav analüüs katseid, näiteks nõudluse hindamise katsete, algoritmid R või Python Programmeerimine keeles ja lihtne drag-and-drop liides.
    -   Saate alla laadida Dynamics 365 toimingute nõudluse prognoosimise eksperimente, nende vastavad äritegevuse nõuetele, avaldada Azure on veebipõhine teenus ja nõudluse loomiseks kasutada. Katseid on allalaadimiseks saadaval, kui olete ostnud Dynamics 365 toimingute liitumisleping tootmise planeerija, nagu enterprise tase kasutaja.
    -   Mistahes saadaolevaid nõudluse ennustuse katseid saate alla laadida [Cortana analüüsigaleriist](https://gallery.cortanaanalytics.com/). Dynamics 365 toimingute nõudluse prognoosimise eksperimendid on automaatselt integreeritud Dynamics 365 operatsioonide, klientide ja partnerite peab töötlema integratsiooni eksperimente, mis nad alla laadida ning [Cortana Analytics Galerii](https://gallery.cortanaanalytics.com/). Seega katsed selle [Cortana Analytics Galerii](https://gallery.cortanaanalytics.com/) ei ole nii lihtne kasutada Dynamics 365 toimingute nõudluse prognoosimise eksperimente. Katseid koodi peate muutma nii, et nad kasutavad Dynamics 365 toimingute rakendusliides (API).
    -   Looge oma katsed Microsoft Azure Machine Learning Studios, avaldage need Azure'is teenustena ning kasutage neid nõudluse prognooside loomisel.
    -   Kui te ei vaja suurt jõudlust või suure hulga andmete töötlust, saate kasutada masinõppe tasuta kihti. Soovitame alati sellest kihist alustada, eriti juurutamise ja testimise faasis. Kui vajate suuremat jõudlust ja täiendavat salvestusruumi, saate kasutada masinõppe standardset kihti. See kiht nõuab Azure'i tellimust ja sellega kaasnevad lisakulud. Masinõppe hindade kohta vt lisateavet aadressil <http://aka.ms/machine-learning-price-info>.
-   **Ilmaennustus vähendamise seose kordagi** – nõudluse prognoosimise Dynamics 365 toimingute ehitab selle funktsiooni, mis võimaldab prognoos nii sõltuv ja sõltumatu nõudluse seose kordagi.

## <a name="basic-flow-in-demand-forecasting"></a>Nõudluse planeerimise põhivoog
Järgmine diagramm näitab nõudluse prognoosimise põhivoogu. 

[![nõudluse prognoosimise Sissejuhatus diagramm](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Nõudluse prognoos põlvkonna algab Dynamics 365 toiminguteks. Selgituseks Dynamics 365 tegevuse selgituseks andmebaasi andmed on kogutud ja asustab vahekausta tabelis. See lavastus tabel söödetakse hiljem masinõpet teenust. Minimaalne kohandamine viies võin pistik vahekausta tabeli andmete allikatest. Andmete allikad võivad sisaldada Microsoft Exceli faile, komaga eraldatud väärtuste (CSV) faili ja andmeid Microsoft Dynamics AX-i 2009 ja Microsoft Dynamics AX 2012. Seetõttu võib tekitada nõudluse ennustab, et kaaluda ajaloolisi andmeid, mis on levinud mitme süsteemid. Siiski peavad koondandmed, nagu nimed ja mõõtühikud, mitmesugustes andmeallikas samad olema.

Kui kasutate Dynamics 365 toimingute nõudluse prognoosimise masinõpet eksperimente, nad otsivad kõige sobivam viis aegridade prognoosimise meetodeid baseline Ilmaennustus seas. Need eelhindamiseks parameetrid hallatakse Dynamics 365 toiminguteks. 

Prognoosid, ajaloolisi andmeid ja muudatusi, nõudluse prognoosid eelmise iteratsiooni tehtud on siis saadaval Dynamics 365 toiminguteks. 

Kasutage Dynamics 365 operatsioonide visualiseerida ja muuta ravi prognoos. Enne prognooside planeerimises kasutamist tuleb käsitsi tehtud korrigeerimised autoriseerida.

## <a name="limitations"></a>Kitsendused
Nõudluse prognoosimise Dynamics 365 toiminguteks on vahend, mis aitab klientidel Exemption luua prognoosimise protsessid. See pakub põhifunktsioone nõudluse prognoosimise lahenduse ja on projekteeritud nii, et seda saab hõlpsasti pikendada. Nõudluse prognoos ei pruugi olla parim sobiv klientidele nagu jaemüük, hulgimüük, ladustamine, transport, või muud kutseorganisatsioonid.

<a name="see-also"></a>Vt ka
--------

[Demand forecasting setup](demand-forecasting-setup.md)

[Generating a statistical baseline forecast](generate-statistical-baseline-forecast.md)

[Making manual adjustments to the baseline forecast](manual-adjustments-baseline-forecast.md)

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


