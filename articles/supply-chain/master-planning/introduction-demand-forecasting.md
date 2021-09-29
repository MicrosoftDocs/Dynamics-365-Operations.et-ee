---
title: Nõudluse prognoosimise ülevaade
description: Nõudluse prognoosimist kasutatakse müügitellimuste sõltumatu nõudluse ja klienditellimuste mistahes lahtisidestuspunktist sõltuva nõudluse ennustamiseks. Täiustatud nõudluse prognoosi vähendamise reeglid pakuvad ideaalset lahendusust masskohandamisele.
author: roxanadiaconu
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "72004"
- intro-internal
ms.assetid: 916707c9-1333-460f-a0fa-4e95f6fda2ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 984669d5e4bde4bd967bf0a181d1b45df16ee569
ms.sourcegitcommit: 24e20b3b96834b23311f1bf5dbab28baf3323728
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2021
ms.locfileid: "7484045"
---
# <a name="demand-forecasting-overview"></a>Nõudluse prognoosimise ülevaade

[!include [banner](../includes/banner.md)]

Nõudluse prognoosimist kasutatakse müügitellimuste sõltumatu nõudluse ja klienditellimuste mistahes lahtisidestuspunktist sõltuva nõudluse ennustamiseks. Täiustatud nõudluse prognoosi vähendamise reeglid pakuvad ideaalset lahendusust masskohandamisele.

Alusprognoosi loomiseks edastatakse kannete ajaloo kokkuvõte Azure’is hostitud Microsoft Azure’i masinõppe teenusele. Teenust ei jagata kasutajate vahel, mistõttu saab seda hõlpsalt tööstuspõhistele nõuetele kohandada. Supply Chain Managementi abil saate prognoosi visualiseerida, korrigeerida ning vaadata prognoosi täpsuse jõudlusnäidikuid.

> [!NOTE]
> Microsoft Azure Machine Learning Studio (klassikaline) on nõutav masinõppega prognoosi loomiseks. Alates 1. detsembrist 2021 ei saa te uusi Masinõppestuudio (klassikalisi) ressursse luua. Siiski saate oma olemasoleva Masinõppestuudio (klassikaliste) ressursside kasutamist jätkata kuni 31. augustini 2024. Värskendatud teabe saamiseks vaadake [Azure Masinõppestuudio](/azure/machine-learning/overview-what-is-machine-learning-studio#ml-studio-classic-vs-azure-machine-learning-studio).
> 
> Dynamics 365 Supply Chain Management versioon 10.0.23 ja uuemad toetavad uut Azure Masinõppestuudiot.

## <a name="key-features-of-demand-forecasting"></a>Nõudluse prognoosimise võtmefunktsioonid

Järgnevalt on toodud mõned nõudluse prognoosimise peamised funktsioonid:

- ajaloolistel andmetel põhineva statistilise alusprognoosi loomine;
- dünaamilise prognoosi dimensioonide kogu kasutamine;
- nõudluse trendide, usaldusvahemike ja prognoosi korrigeerimiste visualiseerimine;
- korrigeeritud prognoosi planeerimisprotsessides kasutamise autoriseerimine;
- võõrväärtuste eemaldamine;
- prognoosi täpsuse mõõdikute loomine.

## <a name="major-themes-in-demand-forecasting"></a>Nõudluse prognoosimise põhiteemad

Nõudluse prognoosimisse on rakendatud kolm põhiteemat.

- **Modulaarsus** – nõudluse prognoos on modulaarne ja hõlpsalt konfigureeritav. Konfiguratsioonivõtit muutes saate funktsiooni sisse ja välja lülitada, valides **Kaubandus** &gt; **Varude prognoos** &gt; **Nõudluse prognoos**.
- **Microsoft Stacki korduvkasutamine** – Microsoft Cortana Analytics Suite’i kuuluva masinõppe abil saate kiiresti ja hõlpsalt luua ennetavaid analüüsikatseid, nagu nõudluse hinnangu katsed, kasutades programmeerimiskeelte R või Python algoritme ja lihtsat lohistamisega liidest.
  - Nõudluse prognoosimise katsed saate alla laadida, muuta neid vastavalt oma äritegevusele ning avaldada need Azure'is veebiteenusena, et kasutada neid nõudluse prognooside loomisel. Katsed on allalaadimiseks saadaval, kui olete ostnud Supply Chain Managementi ettevõtte tasemel kasutaja tootmisplaneerija tellimuse.
  - Mistahes saadaolevaid nõudluse ennustuse katseid saate alla laadida [Cortana analüüsigaleriist](https://gallery.cortanaanalytics.com/). Kui nõudluse prognoosimise katsed integreeritakse Supply Chain Managementis automaatselt, siis [Cortana analüüsigaleriist](https://gallery.cortanaanalytics.com/) allalaaditud katseid tuleb klientidel ja partneritel iga integreerimiseks töödelda. Seetõttu pole [Cortana analüüsigaleriist](https://gallery.cortanaanalytics.com/) allalaaditud katseid nii lihtne kasutada kui rakenduse Finance and Operations nõudluse prognoosimise katseid. Katsete koodi tuleb muuta nii, et nende puhul kasutataks Finance and Operationsi rakenduse programmeerimisliidest (API).
  - Looge oma katsed Microsoft Azure Machine Learning Studios (klassikalne), avaldage need Azure’is teenustena ja kasutage neid nõudluse prognooside loomisel.
  - Kui te ei vaja suurt jõudlust või suure hulga andmete töötlust, saate kasutada masinõppe tasuta kihti. Soovitame alati sellest kihist alustada, eriti juurutamise ja testimise faasis. Kui vajate suuremat jõudlust ja täiendavat salvestusruumi, saate kasutada masinõppe standardset kihti. See kiht nõuab Azure'i tellimust ja sellega kaasnevad lisakulud. Masinõppe hindade kohta vt lisateavet aadressil [Machine Learning Studio hinnad](https://aka.ms/machine-learning-price-info).
- **Prognoosi vähendamine mistahes lahtisidestuspunktis** – nõudluse prognoosimine Dynamics AX-is tugineb sellel funktsioonil, mis võimaldab prognoosida nii sõltuvat kui ka sõltumatut nõudlust mistahes lahtisidestuspunktis.

## <a name="basic-flow-in-demand-forecasting"></a>Nõudluse planeerimise põhivoog

Järgmine diagramm näitab nõudluse prognoosimise põhivoogu.

[![nõudluse prognoosimise sissejuhatav diagramm.](./media/demand-forecasting-introduction.png)](./media/demand-forecasting-introduction.png)

Nõudluse prognoosi loomine algab Supply Chain Managementist. Supply Chain Managementi kannete andmebaasist kogutakse ajaloolisi kandeandmeid ja täidetakse koondamistabelit. Hiljem söödetakse koondamistabel masinõppe teenusesse. Minimaalse kohandamisega saate koondamistabelisse ühendada mitmed andmeallikad. Andmeallikad võivad sisalda Microsoft Exceli faile, komaeraldusega (CSV) faile ning andmeid rakendustest Microsoft Dynamics AX 2009 ja Microsoft Dynamics AX 2012. Seega saate luua nõudluse prognoose, mis arvestavad mitmesuguste süsteemide vahel pillutatud ajaloolisi andmeid. Siiski peavad koondandmed, nagu nimed ja mõõtühikud, mitmesugustes andmeallikas samad olema.

Nõudluse prognoosimise masinõppe katsete kasutamisel otsitakse alusprognoosi arvutamiseks kõige paremini sobivat viie ajaseeria prognoosimise meetodit. Nende prognoosimismeetodite parameetreid saate hallata Supply Chain Managementis.

Eelmistes iteratsioonides nõudluse prognoosides tehtud prognoosid, ajaloolised andmed ja mistahes muudatused on seejärel saadaval Supply Chain Managementis.

Supply Chain Managementi abil saate alusprognoose visualiseerida ja muuta. Enne prognooside planeerimises kasutamist tuleb käsitsi tehtud korrigeerimised autoriseerida.

## <a name="limitations"></a>Kitsendused

Nõudluse prognoosimine on tööriist, mis aitab tööstusvaldkonna klientidel prognoosimise protsesse luua. See pakub nõudluse prognoosimise põhifunktsioone ning on disainitud hõlpsalt laiendatavaks. Nõudluse prognoosimine ei pruugi olla parim lahendus sellistes valdkondades, nagu kaubandus, hulgimüük, ladustamine, transport või muud professionaalsed teenused, tegutsevate klientide jaoks.

### <a name="demand-forecast-variant-conversion-limitation"></a>Nõudluse prognoosi variandi teisenduse piirang

Mõõtühik variandi teisenduse kohta pole nõudluse prognoosi loomisel täielikult toetatud, kui varude mõõtühik erinev nõudluse prognoosi mõõtühikust.

Prognoosi loomine (**Varude mõõtühik > Nõudluse prognoosi mõõtühik**) kasutab toote mõõtühiku teisendust. Ajalooliste andmete laadimisel nõudluse prognoosi loomiseks, kasutatakse alati toote taseme mõõtühiku teisendust varude mõõtühiku teisendamisel nõudluse prognoosi mõõtühikuks, isegi kui variandi tasemel on määratletud teisendused.

Prognoosi autoriseerimise esimene osa (**Nõudluse prognoosi mõõtühik > Varude mõõtühik**) kasutab toote mõõtühiku teisendust. Prognoosi autoriseerimise teine osa (**Varude mõõtühik > Müügi mõõtühik**) kasutab variandi mõõtühiku teisendust. Kui loodud nõudluse prognoos on autoriseeritud, tehakse varude mõõtühiku teisendamine nõudluse prognoosi mõõtühikuks toote taseme mõõtühiku teisenduse abil. Samal ajal arvestatakse varude ühiku ja müügi mõõtühiku vahelisel teisendamisel variantide tasemel määratletud teisendusi.

Pange tähele, et nõudluse prognoosi mõõtühikul ei pea olema mingit kindlat tähendust. Seda võib määratleda kui „Nõudluse prognoosi ühik”. Iga toote puhul saate määratleda teisenduse suhteks 1:1 varude mõõtühikuga.

## <a name="additional-resources"></a>Lisaressursid

[Nõudluse prognoosi häälestus](demand-forecasting-setup.md)

[Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)

[Alusprognoosis käsitsi korrigeerimiste tegemine](manual-adjustments-baseline-forecast.md)

[Korrigeeritud prognoosi autoriseerimine](authorize-adjusted-forecast.md)

[Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md)

[Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost](remove-historical-outliers-calculating-demand-forecast.md)

[Nõudluse prognoosi funktsiooni pikendamine](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
