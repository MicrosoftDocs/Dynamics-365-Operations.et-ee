---
title: Tulu tuvastamise ümberjaotamine – 4. stsenaarium
description: Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus olemasolevast, osaliselt arveldatud müügitellimusest eemaldatakse rida. See stsenaarium annab ühesuguse tulemuse olenemata sellest, kas rida eemaldatakse müügitellimusest või määratakse tühistatud olekusse.
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
ms.openlocfilehash: 50a2d0d2ca28d9b62713502700f2c4bd2e42751e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238300"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Tulu tuvastamise ümberjaotamine – 4. stsenaarium

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus olemasolevast, osaliselt arveldatud müügitellimusest eemaldatakse rida. See stsenaarium annab ühesuguse tulemuse olenemata sellest, kas rida eemaldatakse müügitellimusest või määratakse tühistatud olekusse.

Selles stsenaariumis määratakse lehe **Pearaamatu parameetrid** vahekaardi **Tulu tuvastamine** suvand **Arvete korrigeerimiste sisestamine müügireskontrole** olekusse **Ei** (**Tulu tuvastamine \> Häälestamine \> Pearaamatu parameetrid**).

[![Suvand arvete korrigeerimiste sisestamine müügireskontrole määratud olekusse Ei](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Müügitellimus luuakse kliendile US\_SI\_0003. Klient ostab sülearvuti (kaubakood S0012), installimisteenused (kaubakood S0001) ja tugilepingu (kaubakood S0008, „Püsiv projekteerimisteenus“). Sülearvuti ja installimisteenuste tulu tuvastatakse kohe. Tugilepingu tulu lükatakse edasi ja tuvastatakse 12 kuu jooksul, nagu määratleb lepingu kuupäevavahemik.

[![Sülearvuti, installimisteenuste ja tugilepingu müügitellimuse read](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Müügitellimus kinnitatakse. Kuna kõik kolm kaupa on häälestatud tulu hinna eraldamiseks, arvutatakse tulu hind müügitellimuse kinnitamisel. Tuvastatavat tulu saate vaadata lehel **Tulu hinna eraldamine** (lehel **Müügitellimus**, toimingupaanil, vahekaardil **Haldamine**, grupis **Tulu tuvastamine** valige **Tulu hinna eraldamine**). Sülearvuti tulu sisestatakse tulu kontole summas 995.84 $. Installimisteenuste tulu sisestatakse samuti tulu kontole summas 314.47 $. Tugilepingu tulu sisestatakse edasilükkunud tulu kontole summas 188.69 $. Tulu hindade summa peab võrduma tulu hinna eraldamise hõivamiseks häälestatud ridade summaga (1499.00 $).

[![Tulu hinna eraldamise leht](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Kliendiga arveldatakse sülearvuti ja tugileping, kuid mitte installimisteenuseid. Järgmine joonis kujutab arve jaoks sisestatud raamatupidamise kirjet.

[![Arveldatud müügitellimuse raamatupidamise kirje](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Raamatupidamise kirje sisestab 1276.94 $ müügireskontrole. Ent kuna see arve on osaline arve, ei võrdu tulu või edasilükatud tulu ja maks kokku müügireskontro summaga. Erinevus -14.47 $ sisestatakse osalise arve tulu kliiringu kontole.

Luuakse ka tulu tuvastamise graafik.

[![Osalise arve leht Tulu tuvastamise graafik](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Hiljem otsustab klient installimisteenuseid mitte osta. Seetõttu eemaldatakse see rida müügitellimusest. Arvestage, et müügitellimust ei saa uuesti kinnitada, kuna müügitellimusele jäävad ainult arveldatud read.

[![Müügitellimus pärast installimisteenuste rea eemaldamist](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Müügitellimust ei saa küll kinnitada, kuid selle saab ümber jaotada. Valige müügitellimuses **Hinna ümberjaotamine uute tellimuse ridadega**, et avada leht **Hinna ümberjaotamine uute tellimuse ridadega**. Valige kaks allesjäänud müügitellimuse rida ning seejärel valige **Uuenda ümberjaotamist**. Veerus **Ümberjaotud summa** näidatakse müügitellimuse iga allesjäänud rea uus tulu hind.

[![Uued tulu hinnad lehel Hinna ümberjaotamine uute tellimuse ridadega](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Järgmiseks valige **Eeldatav kanne**, et vaadata raamatupidamise kirjeid.

[![Raamatupidamiskirjed lehel Eeldatav kanne](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

Lehel **Eeldatav kanne** tühistavad viis viimast rida sisestatud arve algse raamatupidamise kirje. Esimesed neli rida on arve jaoks sisestatud uued raamatupidamise kirjed. Oluline on mõista, et kliendile pole uut arvet esitatud. Pärast ümberjaotamist on kliendi võlgnevus endiselt 1276.94 $ ja see summa tuleb sisestada uues raamatupidamise kirjes müügireskontrosse. Uus tulu või edasilükatud tulu pluss maks on kokku 1276.94 $. Seetõttu ei pea te sisestama osalise arve tulu kliiringu kontole.

Ümberjaotamise lõpule viimiseks valige **Töötle**. Sisestatakse sisestamiskuupäev. Pärast ümberjaotamise lõpule viimist näidatakse lehel **Tulu hinna eraldamine** kahe allesjäänud kauba hinna ümberjaotust.

[![Allesjäänud kaupade hinna ümberjaotus tulu hinna eraldamise lehel](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Uuendati ka tulu tuvastamise graafikut uue tulu ümberjaotamise hinna alusel. Müügitellimuses avage leht **Tulu tuvastamise graafik**. Varem oli kauba S0008 jaoks 13 rida (sellele kaubale oli määratud 12 kuu pikkune graafik). Nüüd on ridu 39: algse graafiku 13 rida, tagasivõtugraafiku 13 rida ja uuel tulu hinnal põhinevad 13 rida.

[![Uuendatud tulu tuvastamise graafiku leht 39 reaga kauba S0008 jaoks](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Kui valite **Kanne**, näidatakse arve töölehel algset raamatupidamise kirjet. Müügitellimuse tühistatud kirje ja uue raamatupidamise kirje vaatamiseks valige toimingupaanil **Tulu korrigeerimised** ja seejärel **Kanne**.

Järgmiseks avage leht **Kõik kliendid** (**Müügireskontro \> Kliendid \> Kõik kliendid**), valige klient **US\_SI\_0003** ja seejärel valige **Kanded**. Lehel **Kliendi kanded** näidatakse ainult algne arve (000008) koos algse raamatupidamise kirjega. Kuna lehel **Pearaamatu parameetrid** on suvand **Arvete korrigeerimiste sisestamine müügireskontrole** määratud olekusse **Ei**, uuendatakse ainult pearaamatut. Seetõttu ei näidata tühistatud ja uuendatud raamatupidamise kirjeid. Arvestage, et näidatakse [3. stsenaariumis](rev-rec-reallocation-scenario-3.md) loodud tulu korrigeerimise kandeid.

[![Algne raamatupidamise kirje lehel Kliendi kanded](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]