---
title: "Nõudluse prognoosimise ülevaade"
description: "Nõudluse prognoosimist kasutatakse müügitellimuste sõltumatu nõudluse ja klienditellimuste mistahes lahtisidestuspunktist sõltuva nõudluse ennustamiseks. Täiustatud nõudluse prognoosi vähendamise reeglid pakuvad ideaalset lahendusust masskohandamisele."
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

[!include[banner](../includes/banner.md)]


Nõudluse prognoosimist kasutatakse müügitellimuste sõltumatu nõudluse ja klienditellimuste mistahes lahtisidestuspunktist sõltuva nõudluse ennustamiseks. Täiustatud nõudluse prognoosi vähendamise reeglid pakuvad ideaalset lahendusust masskohandamisele.

Alusprognoosi loomiseks edastatakse kannete ajaloo kokkuvõte Azure'is hostitud Microsoft Azure'i masinõppe teenusele. Teenust ei jagata kasutajate vahel, mistõttu saab seda hõlpsalt tööstuspõhistele nõuetele kohandada. Dynamics 365 for Operationsi abil saate prognoosi visualiseerida, korrigeerida ning vaadata prognoosi täpsuse jõudlusnäidikuid.

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

-   **Modulaarsus** – nõudluse prognoos on modulaarne ja hõlpsalt konfigureeritav. Konfiguratsioonivõtit muutes saate funktsiooni sisse ja välja lülitada, valides **Kaubandus** &gt; **Varude prognoos** &gt; **Nõudluse prognoos**.
-   **Microsofti virna korduskasutus** – Microsoft käivitas masinõppe platvormi 2015. aasta veebruaris. Praeguseks Microsoft Cortana Analytics Suite’i kuuluva masinõppe abil saate kiiresti ja hõlpsalt luua ennetavaid analüüsikatseid, nagu nõudluse hinnangu katsed, kasutades programmeerimiskeelte R või Python algoritme ja lihtsat lohistamisega liidest.
    -   Dynamics 365 for Operationsi nõudluse prognoosimise katsed saate alla laadida, muuta neid vastavalt oma äritegevusele ning avaldada need Azure'is veebiteenusena, et kasutada neid nõudluse prognooside loomisel. Katsed on allalaadimiseks saadaval, kui olete ostnud Dynamics 365 for Operationsi ettevõtte tasemel kasutaja tootmisplaneerija tellimuse.
    -   Mistahes saadaolevaid nõudluse ennustuse katseid saate alla laadida [Cortana analüüsigaleriist](https://gallery.cortanaanalytics.com/). Kui Dynamics 365 for Operationsi nõudluse prognoosimise katsed integreeritakse Dynamics 365 for Operationsis automaatselt, siis [Cortana analüüsigaleriist](https://gallery.cortanaanalytics.com/) allalaaditud katseid tuleb klientidel ja partneritel Dynamics 365 for Operationsiga integreerimiseks töödelda. Seetõttu pole [Cortana analüüsigaleriist](https://gallery.cortanaanalytics.com/) allalaaditud katseid nii lihtne kasutada kui Dynamics 365 for Operationsi nõudluse prognoosimise katseid. Katsete koodi tuleb muuta nii, et nende puhul kasutataks Dynamics 365 for Operationsi rakenduse programmeerimisliidest (API).
    -   Looge oma katsed Microsoft Azure Machine Learning Studios, avaldage need Azure'is teenustena ning kasutage neid nõudluse prognooside loomisel.
    -   Kui te ei vaja suurt jõudlust või suure hulga andmete töötlust, saate kasutada masinõppe tasuta kihti. Soovitame alati sellest kihist alustada, eriti juurutamise ja testimise faasis. Kui vajate suuremat jõudlust ja täiendavat salvestusruumi, saate kasutada masinõppe standardset kihti. See kiht nõuab Azure'i tellimust ja sellega kaasnevad lisakulud. Masinõppe hindade kohta vt lisateavet aadressil <http://aka.ms/machine-learning-price-info>.
-   **Prognoosi vähendamine mistahes lahtisidestuspunktis** – nõudluse prognoosimine Dynamics 365 for Operationsis tugineb sellel funktsioonil, mis võimaldab prognoosida nii sõltuvat kui ka sõltumatut nõudlust mistahes lahtisidestuspunktis.

## <a name="basic-flow-in-demand-forecasting"></a>Nõudluse planeerimise põhivoog
Järgmine diagramm näitab nõudluse prognoosimise põhivoogu. 

[![nõudluse prognoosimise sissejuhatav diagramm](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Nõudluse prognoosi loomine algab Dynamics 365 for Operationsis. Dynamics 365 for Operationsi kannete andmebaasist kogutakse ajaloolisi kandeandmeid ja täidetakse koondamistabelit. Hiljem söödetakse koondamistabel masinõppe teenusesse. Minimaalse kohandamisega saate koondamistabelisse ühendada mitmed andmeallikad. Andmeallikad võivad sisaldada Microsoft Exceli faile, komaeraldusega (CSV) faile ning Microsoft Dynamics AX 2009 ja Microsoft Dynamics AX 2012 andmeid. Seega saate luua nõudluse prognoose, mis arvestavad mitmesuguste süsteemide vahel pillutatud ajaloolisi andmeid. Siiski peavad koondandmed, nagu nimed ja mõõtühikud, mitmesugustes andmeallikas samad olema.

Dynamics 365 for Operationsi nõudluse prognoosimise masinõppe katsete kasutamisel otsitakse alusprognoosi arvutamiseks kõige paremini sobivat viie ajaseeria prognoosimise meetodit. Nende prognoosimismeetodite parameetreid saate hallata Dynamics 365 for Operationsis. 

Eelmistes iteratsioonides nõudluse prognoosides tehtud prognoosid, ajaloolised andmed ja mistahes muudatused on seejärel saadaval Dynamics 365 for Operationsis. 

Dynamics 365 for Operationsi abil saate alusprognoose visualiseerida ja muuta. Enne prognooside planeerimises kasutamist tuleb käsitsi tehtud korrigeerimised autoriseerida.

## <a name="limitations"></a>Kitsendused
Nõudluse prognoosimine Dynamics 365 for Operationsis on tööriist, mis aitab tööstusvaldkonna klientidel prognoosimise protsesse luua. See pakub nõudluse prognoosimise põhifunktsioone ning on disainitud hõlpsalt laiendatavaks. Nõudluse prognoosimine ei pruugi olla parim lahendus sellistes valdkondades nagu jaemüük, hulgimüük, ladustamine, transport või muud professionaalsed teenused, tegutsevate klientide jaoks.

<a name="see-also"></a>Vt ka
--------

[Nõudluse prognoosi seadistus](demand-forecasting-setup.md)

[Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)

[Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)

[Korrigeeritud prognoosi autoriseerimine](authorize-adjusted-forecast.md)

[Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md)

[Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost](remove-historical-outliers-calculating-demand-forecast.md)



