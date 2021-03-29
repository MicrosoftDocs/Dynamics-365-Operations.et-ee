---
title: Tulu tuvastamise ümberjaotamine – 1. stsenaarium
description: Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus sisestatakse kaks müügitellimust, kuid need ainult kinnitatakse. Sama stsenaarium annab sarnased tulemused, kui kinnitatud olekus on rohkem kui kaks müügitellimust.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 25fb32ce72555e573cd37a0ab092b51b99bb4372
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260873"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Tulu tuvastamise ümberjaotamine – 1. stsenaarium

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus sisestatakse kaks müügitellimust, kuid need ainult kinnitatakse. Sama stsenaarium annab sarnased tulemused, kui kinnitatud olekus on rohkem kui kaks müügitellimust.

Selles stsenaariumis määratakse lehe **Pearaamatu parameetrid** vahekaardi **Tulu tuvastamine** suvand **Arvete korrigeerimiste sisestamine müügireskontrole** olekusse **Ei** (**Tulu tuvastamine \> Häälestamine \> Pearaamatu parameetrid**).

[![Suvand arvete korrigeerimiste sisestamine müügireskontrole määratud olekusse Ei](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Müügitellimus luuakse kliendile US\_SI\_0003. Klient ostab sülearvuti (kaubakood S0012) ja sellele tugilepingu (kaubakood S0008, „Püsiv projekteerimisteenus“). Sülearvuti tulu tuvastatakse kohe (tulu tuvastamise graafik puudub). Tugilepingu tulu lükatakse edasi ja tuvastatakse 12 kuu jooksul, nagu määratleb lepingu kuupäevavahemik.

[![Sülearvuti ja tugilepingu müügitellimuse read](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Müügitellimus kinnitatakse. Kuna mõlemad kaubad on häälestatud tulu hinna eraldamiseks, arvutatakse tulu hind müügitellimuse kinnitamisel. Tuvastatavat tulu saate vaadata lehel **Tulu hinna eraldamine** (lehel **Müügitellimus**, toimingupaanil, vahekaardil **Haldamine**, grupis **Tulu tuvastamine** valige **Tulu hinna eraldamine**). Sülearvuti tulu sisestatakse tulu kontole summas 1008.01 $. Tugilepingu tulu sisestatakse edasilükkunud tulu kontole summas 190.99 $. Tulu hindade summa peab võrduma tulu hinna eraldamise hõivamiseks häälestatud ridade summaga (1199.00 $).

[![Tulu hinna eraldamise leht](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Müügitehingu sõlmimisel otsustas klient mitte osta installimisteenuseid (kaubakood S0001), kuid muutis hiljem meelt. Seetõttu sisestatakse samale kliendile teine müügitellimus.

[![Installimisteenuste müügitellimuse rida](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Kinnitatakse teine müügitellimus. Kuna see müügitellimus sisaldab ainult üht rida, siis müügitellimuse kinnitamisel tulu hinna eraldamist ei tehta. Tulu hinna eraldamine toimub ainult siis, kui on kaks või enam kordumatut kaupa ja kui need kaubad on häälestatud tulu hinna eraldamiseks.

Kui see uus müügitellimus on ainus muudatus kliendi lepingus, saab ümberjaotamise protsessi nüüd käivitada. Valige ühes kahest müügitellimusest **Hinna ümberjaotamine uute tellimuse ridadega**, et avada leht **Hinna ümberjaotamine uute tellimuse ridadega**. Teise variandina võite avada **Tulu tuvastamine \> Perioodilised ülesanded \> Hinna ümberjaotamine uute tellimuse ridadega**. Valige kaks müügitellimust ja vastavad müügitellimuse read ning seejärel valige **Uuenda ümberjaotamist**. Veerus **Ümberjaotud summa** näidatakse iga müügitellimuse rea uus tulu hind.

[![Uued tulu hinnad lehel Hinna ümberjaotamine uute tellimuse ridadega](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Kui valite **Eeldatav kanne**, siis ei näidata midagi, sest ühtegi arvet pole sisestatud.

Ümberjaotamise lõpule viimiseks valige **Töötle**. Teilt küsitakse sisestamise kuupäeva, isegi kui midagi ei sisestata. Kui ümberjaotamine on lõpule viidud, näidatakse iga müügitellimuse lehel **Tulu hinna eraldamine** mõlema müügitellimuse kõigi kaupade hinna eraldamist. Teisisõnu, iga müügitellimuse leht **Tulu hinna eraldamine** sisaldab kaupa, mida selles müügitellimuses ei ole, kuna see kaup on osa samast lepingust, kuid erinevast müügitellimusest.

> [!TIP]
> Nende lisakaupade näitamisele konteksti andmiseks saate ruudustikku lisada täiendavaid veerge, näiteks **Ümberjaotamise ID** ja **Müügitellimus**.
> 
> [![Täiendavad veerud tulu hinna eraldamiste lehel](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]