---
title: Tulu tuvastamise ümberjaotamine – 2. stsenaarium
description: Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus sisestatakse kaks müügitellimust ja seejärel lisab klient pärast esimese müügitellimuse arveldamist lepingule kauba. Kui lepingule lisatakse uus kaup, siis saab selle lisada kas uuele müügitellimusele või olemasolevale müügitellimusele.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 31a0b26fbf2383c90caaa8c1ea0e56ab5f377609
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814196"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Tulu tuvastamise ümberjaotamine – 2. stsenaarium

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus sisestatakse kaks müügitellimust ja seejärel lisab klient pärast esimese müügitellimuse arveldamist lepingule kauba. Kui lepingule lisatakse uus kaup, siis saab selle lisada kas uuele müügitellimusele või olemasolevale müügitellimusele.

Selles stsenaariumis määratakse lehe **Pearaamatu parameetrid** vahekaardi **Tulu tuvastamine** suvand **Arvete korrigeerimiste sisestamine müügireskontrole** olekusse **Ei** (**Tulu tuvastamine \> Häälestamine \> Pearaamatu parameetrid**).

[![Suvand arvete korrigeerimiste sisestamine müügireskontrole määratud olekusse Ei](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Müügitellimus luuakse kliendile US\_SI\_0003. Klient ostab sülearvutile installimisteenused (kaubakood S0001) ja tugilepingu (kaubakood S0008), kuid ei ole veel sülearvutit välja valinud. Installimisteenuste tulu lükatakse edasi kuni sülearvuti ostmise kuupäevani. Tugilepingu tulu lükatakse edasi ja tuvastatakse 12 kuu jooksul, nagu määratleb lepingu kuupäevavahemik.

[![Installimisteenuste ja tugilepingu müügitellimuse read](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Müügitellimus kinnitatakse. Kuna mõlemad kaubad on häälestatud tulu hinna eraldamiseks, arvutatakse tulu hind müügitellimuse kinnitamisel. Tuvastatavat tulu saate vaadata lehel **Tulu hinna eraldamine** (lehel **Müügitellimus**, toimingupaanil, vahekaardil **Haldamine**, grupis **Tulu tuvastamine** valige **Tulu hinna eraldamine**). Installimisteenuste tulu sisestatakse edasilükkunud tulu kontole summas 250.00 $. Tugilepingu tulu sisestatakse samuti edasilükkunud tulu kontole summas 150.00 $. Tulu hindade summa peab võrduma tulu hinna eraldamise hõivamiseks häälestatud ridade summaga (400.00 $).

[![Tulu hinna eraldamise leht](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Müügitellimus arveldatakse täielikult. Järgmine joonis kujutab arve jaoks sisestatud raamatupidamise kirjet.

[![Täielikult arveldatud müügitellimuse raamatupidamiskirje](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Luuakse ka tulu tuvastamise graafik, kuid ühtegi tulu veel ei tuvastata.

[![Tulu tuvastamise graafiku leht](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Mõni päev hiljem valib klient sülearvuti. Kliendile sisestatakse teine müügitellimus.

[![Sülearvuti müügitellimuse rida](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Kinnitatakse teine müügitellimus. Kuna see müügitellimus sisaldab ainult üht rida, siis müügitellimuse kinnitamisel tulu hinna eraldamist ei tehta. Tulu hinna eraldamine toimub ainult siis, kui on kaks või enam kordumatut kaupa ja kui need kaubad on häälestatud tulu hinna eraldamiseks.

Kui see uus müügitellimus on ainus muudatus kliendi lepingus, saab ümberjaotamise protsessi nüüd käivitada. Valige ühes kahest müügitellimusest **Hinna ümberjaotamine uute tellimuse ridadega**, et avada leht **Hinna ümberjaotamine uute tellimuse ridadega**. Teise variandina võite avada **Tulu tuvastamine \> Perioodilised ülesanded \> Hinna ümberjaotamine uute tellimuse ridadega**. Valige kaks müügitellimust ja vastavad müügitellimuse read ning seejärel valige **Uuenda ümberjaotamist**. Veerus **Ümberjaotud summa** näidatakse iga müügitellimuse rea uus tulu hind.

[![Uued tulu hinnad lehel Hinna ümberjaotamine uute tellimuse ridadega](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Seejärel valige **Eeldatav kanne**, et vaadata ainult pearaamatusse sisestatavaid raamatupidamiskirjeid. Kuna suvand **Arvete korrigeerimiste sisestamine müügireskontrole** on lehel **Pearaamatu parameetrid** määratud olekusse **Ei**, ei muutu ümberjaotamise töötlemisel müügireskontros midagi.

[![Raamatupidamiskirjed lehel Eeldatav kanne](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

Lehel **Eeldatav kanne** tühistavad kolm viimast rida sisestatud arve algse raamatupidamise kirje. Esimesed neli rida moodustavad arve jaoks sisestatud uue raamatupidamise kirje. Oluline on mõista, et kliendile pole uut arvet esitatud. Pärast ümberjaotamist on kliendi võlgnevus endiselt 426.00 $ ja see summa tuleb sisestada uues raamatupidamise kirjes müügireskontrosse. Poolelioleva maksu ja edasilükkunud tulu summaks on 188.69 $ + 314.48 $ + 26.00 $ = 529.17 $. Edasilükkunud tulu summa on ümberjaotamise tõttu muutunud. Erinevus 103.17 $ sisestatakse osalise arve tulu kliiringu kontole. See saldo tühjendatakse, kui sisestatakse ümberjaotamisse kaasatud teise müügitellimuse arve.

Ümberjaotamise lõpule viimiseks valige **Töötle**. Teilt küsitakse sisestamise kuupäeva, isegi kui midagi ei sisestata. Kui ümberjaotamine on lõpule viidud, näidatakse iga müügitellimuse lehel **Tulu hinna eraldamine** mõlema müügitellimuse kõigi kaupade hinna eraldamist. Teisisõnu, iga müügitellimuse leht **Tulu hinna eraldamine** sisaldab kaupa, mida selles müügitellimuses ei ole, kuna see kaup on osa samast lepingust, kuid erinevast müügitellimusest.

> [!TIP]
> Nende lisakaupade näitamisele konteksti andmiseks saate ruudustikku lisada täiendavaid veerge, näiteks **Ümberjaotamise ID** ja **Müügitellimus**.
> 
> [![Täiendavad veerud tulu hinna eraldamiste lehel](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

Müügitellimuses 00036 uuendati ka tulu tuvastamise graafikut uue tulu ümberjaotamise hinna alusel. Selles müügitellimuses avage leht **Tulu tuvastamise graafik**. Varem oli kauba S0008 jaoks 13 rida (sellele kaubale oli määratud 12 kuu pikkune graafik). Nüüd on ridu 39: algse graafiku 13 rida, tagasivõtugraafiku 13 rida ja uuel tulu hinnal põhinevad 13 rida.

[![Uuendatud tulu tuvastamise graafiku leht 39 reaga kauba S0008 jaoks](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Sarnaselt oli kauba S0001 jaoks varem kaks rida, kuid nüüd on neid kuus.

[![Uuendatud tulu tuvastamise graafiku leht kuue reaga kauba S0001 jaoks](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Kui valite müügitellimuses 000036 **Kanne**, näidatakse arve töölehel algset raamatupidamise kirjet. Müügitellimuse tühistatud kirje ja uue raamatupidamise kirje vaatamiseks valige toimingupaanil **Tulu korrigeerimised** ja seejärel **Kanne**.

[![Müügitellimus 000036](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Järgmiseks avage leht **Kõik kliendid** (**Müügireskontro \> Kliendid \> Kõik kliendid**), valige klient **US\_SI\_0003** ja seejärel valige **Kanded**. Näidatakse müügitellimuse 000036 avatud arvet. Kui valite kande, näete algset raamatupidamise kirjet, mitte ümberjaotamise uut raamatupidamise kirjet. Tühistatud kirjet ja uut raamatupidamise kirjet ei saa müügireskontros vaadata.

Nüüd arveldatakse teine müügitellimus. Kliendile esitatav koguarve on 1099.00 $ + maks 71.44 $ = 1170.44 $. Järgmine joonis kujutab sisestatud raamatupidamise kirjet.

[![Kande kannete leht sisestatud raamatupidamise kirjega](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Kuna tulu ja müügi summa on suurem kui 1170.44 $, sisestatakse erinevus -130.17 $. See summa tühjendab osalise arve tulu kliiringu konto saldo. Pärast ümberjaotamist sisestatakse see saldo uude raamatupidamise kirjesse.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]