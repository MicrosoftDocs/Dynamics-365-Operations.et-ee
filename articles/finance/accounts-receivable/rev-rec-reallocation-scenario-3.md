---
title: Tulu tuvastamise ümberjaotamine – 3. stsenaarium
description: Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus olemasolevale arveldatud müügitellimusele lisatakse uus rida. Kui lepingule lisatakse uus kaup, siis saab selle lisada kas uuele müügitellimusele või olemasolevale müügitellimusele.
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
ms.openlocfilehash: e4e0d89c094bd8dba9ff4560502035fa36ec453454a4e31596db8cfd3517c8e5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726154"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Tulu tuvastamise ümberjaotamine – 3. stsenaarium

[!include [banner](../includes/banner.md)]

Selles teemas tutvustatakse ümberjaotamise stsenaariumi, kus olemasolevale arveldatud müügitellimusele lisatakse uus rida. Kui lepingule lisatakse uus kaup, siis saab selle lisada kas uuele müügitellimusele või olemasolevale müügitellimusele. See stsenaarium selgitab ka seda, mis toimub müügireskontro uuendamisel ümberjaotamise tõttu.

Selles stsenaariumis määratakse lehe **Pearaamatu parameetrid** vahekaardil **Tulu tuvastamine** suvand **Arvete korrigeerimiste sisestamine müügireskontrole** olekusse **Jah** (**Tulu tuvastamine \> Häälestamine \> Pearaamatu parameetrid**).

[![Suvand arvete korrigeerimiste sisestamine müügireskontrole määratud olekusse Jah.](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Müügitellimus luuakse kliendile US\_SI\_0003. Klient ostab sülearvuti (kaubakood S0012) ja sellele tugilepingu (kaubakood S0008, „Püsiv projekteerimisteenus“). Sülearvuti tulu tuvastatakse kohe. Tugilepingu tulu lükatakse edasi ja tuvastatakse 12 kuu jooksul, nagu määratleb lepingu kuupäevavahemik.

[![Sülearvuti ja tugilepingu müügitellimuse read.](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Müügitellimus kinnitatakse. Kuna mõlemad kaubad on häälestatud tulu hinna eraldamiseks, arvutatakse tulu hind müügitellimuse kinnitamisel. Tuvastatavat tulu saate vaadata lehel **Tulu hinna eraldamine** (lehel **Müügitellimus**, toimingupaanil, vahekaardil **Haldamine**, grupis **Tulu tuvastamine** valige **Tulu hinna eraldamine**). Sülearvuti tulu sisestatakse tulu kontole summas 1008.01 $. Tugilepingu tulu sisestatakse edasilükkunud tulu kontole summas 190.99 $. Tulu hindade summa peab võrduma tulu hinna eraldamise hõivamiseks häälestatud ridade summaga (1199.00 $).

[![Tulu hinna eraldamise leht.](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Müügitellimus arveldatakse täielikult. Järgmine joonis kujutab arve jaoks sisestatud raamatupidamise kirjet.

[![Täielikult arveldatud müügitellimuse raamatupidamiskirje.](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Luuakse ka tulu tuvastamise graafik. Pärast mõne aja möödumist on kahe kuu kohta olemas tuvastatud tugilepingu tulu.

[![Tulu tuvastamise graafiku leht pärast kahe kuu möödumist.](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Siis otsustab siis lisada installimisteenuseid (kaubakood S0001). See kaup lisatakse olemasolevale müügitellimusele. Kliendil palutakse kinnitada, et ta soovib muuta täielikult arveldatud müügitellimust, ja ta valib **Jah**.

[![Müügitellimus pärast installimisteenuste rea lisamist.](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Kui see uus kaup on ainus muudatus kliendi lepingus, saab ümberjaotamise protsessi nüüd käivitada. Valige müügitellimuses **Hinna ümberjaotamine uute tellimuse ridadega**, et avada leht **Hinna ümberjaotamine uute tellimuse ridadega**. Valige selle müügitellimuse kõik müügitellimuse read ning seejärel valige **Uuenda ümberjaotamist**. Veerus **Ümberjaotud summa** näidatakse iga müügitellimuse rea uus tulu hind.

[![Uued tulu hinnad lehel Hinna ümberjaotamine uute tellimuse ridadega.](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Järgmiseks valige **Eeldatav kanne**, et vaadata raamatupidamise kirjeid. Kuna lehel **Pearaamatu parameetrid** on suvand **Arvete korrigeerimiste sisestamine müügireskontrole** määratud olekusse **Jah**, sisestatakse need raamatupidamiskirjed pearaamatusse kreeditdokumendi kaudu ja müügireskontros luuakse uus arve.

[![Raamatupidamiskirjed lehel Eeldatav kanne.](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

Lehel **Eeldatav kanne** tühistavad neli viimast rida sisestatud arve algse raamatupidamise kirje. Esimesed viis rida on arve jaoks sisestatud uued raamatupidamise kirjed. Oluline on mõista, et kliendile pole uut arvet esitatud. Pärast ümberjaotamist on kliendi võlgnevus endiselt 1276.94 $ ja see summa tuleb sisestada uues raamatupidamise kirjes müügireskontrosse. Poolelioleva maksu ja tulu või edasilükkunud tulu summaks on 995.83 $ + 188.69 $ + 77.94 $ = 1262.46 $. Edasilükkunud tulu summa tulu on ümberjaotamise tõttu muutunud. Erinevus -14.48 $ sisestatakse osalise arve tulu kliiringu kontole. See saldo tühjendatakse, kui sisestatakse müügitellimusele lisatud uue kauba arve.

Ümberjaotamise lõpule viimiseks valige **Töötle**. Sisestatakse sisestamiskuupäev. Pärast ümberjaotamise lõpule viimist näidatakse lehel **Tulu hinna eraldamine** kõigi kolme kauba hinna ümberjaotust.

[![Kõigi kolme kauba hinna ümberjaotus tulu hinna eraldamise lehel.](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Uuendati ka tulu tuvastamise graafikut uue tulu ümberjaotamise hinna alusel. Müügitellimuses avage leht **Tulu tuvastamise graafik**. Varem oli kauba S0008 jaoks 13 rida (sellele kaubale oli määratud 12 kuu pikkune graafik). Nüüd on ridu 39: algse graafiku 13 rida, tagasivõtugraafiku 13 rida ja uuel tulu hinnal põhinevad 13 rida.

[![Uuendatud tulu tuvastamise graafiku leht 39 reaga kauba S0008 jaoks.](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Kui valite **Kanne**, näidatakse arve töölehel algset raamatupidamise kirjet. Müügitellimuse tühistatud kirje ja uue raamatupidamise kirje vaatamiseks valige toimingupaanil **Tulu korrigeerimised** ja seejärel **Kanne**.

Järgmiseks avage leht **Kõik kliendid** (**Müügireskontro \> Kliendid \> Kõik kliendid**), valige klient **US\_SI\_0003** ja seejärel valige **Kanded**. Lehel **Kliendi kanded** näidatakse algset arvet (000006), stornodokumenti (000006-1) ja uut arvet (000006-2). Algne arve ja stornodokument tasakaalustatakse üksteise suhtes ning nende saldo on 0 (null). Pearaamatu mõjude vaatamiseks vaadake iga dokumendi kannet.

[![Algne arve, stornodokument ja uus arve lehel Kliendi kanded.](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Müügitellimus arveldatakse uuesti lisatud kauba kohta. Kliendile esitatav koguarve on 300.00 $ + maks 19.50 $ = 319.50 $. Järgmine joonis kujutab sisestatud raamatupidamise kirjet.

[![Kande kannete leht sisestatud raamatupidamise kirjega.](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Kuna tulu ja müügi summa on suurem kui 319.50 $, sisestatakse erinevus 14.48 $. See summa tühjendab osalise arve tulu kliiringu konto saldo. See saldo uuendati uues raamatupidamise kirjes, mis sisestati pärast ümberjaotamist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]