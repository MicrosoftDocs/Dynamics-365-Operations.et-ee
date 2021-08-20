---
title: Tulu tuvastamise ümberjaotamine
description: Selles teemas kirjeldatakse ümberjaotamist, mis võimaldab organisatsioonidel müügilepingute tingimuste muutumisel tulu hindu ümber arvutada. See sisaldab linke teistele teemadele, milles kirjeldatakse tulu tuvastamist erinevates stsenaariumites.
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
ms.openlocfilehash: 50ae395c370947e348714ce5685123328849966f3a67903e9ddf8c27dee42f5f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745033"
---
# <a name="revenue-recognition-reallocation"></a>Tulu tuvastamise ümberjaotamine

[!include [banner](../includes/banner.md)]

Ümberjaotamine võimaldab organisatsioonidel müügilepingute tingimuste muutumisel tulu hindu ümber arvutada. Tulu tuvastamise eesmärgil loetakse müügitellimuse dokumente lepinguks.

Teie organisatsioon peab ise otsustama, kas ümberjaotamine on vajalik. Uue rea lisamine müügitellimusele või uue müügitellimuse lisamine kliendile ei pruugi tähendada lepingu muudatust. Järgnevate stsenaariumite korral võib ümberjaotamine olla vajalik.

- Klient lisas müügitellimusele kaupu või eemaldas müügitellimusest kaupu pärast seda, kui tellimus oli täielikult või osaliselt arveldatud.
- Samale sõlmitud lepingule sisestati mitu müügitellimust kas kinnitatud olekus või arveldatud olekus.
- Klient tagastas või sai kauba eest krediiti pärast algse müügitellimuse täielikku või osalist arveldamist.

Ümberjaotamise protsessil on mõned olulised piirangud.

- Protsessi saab käitada ainult üks kord. Seetõttu on oluline käivitada see alles pärast seda, kui kõik muudatused on tehtud.
- Protsessi ei saa käivitada projekti müügitellimustel.
- Kui tegemist on mitme müügitellimusega, peavad need kuuluma samale kliendikontole.
- Kõik ümberjaotatavad müügitellimused peavad olema samas kandevaluutas.
- Pärast käitamist ei saa protsessi tühistada ega tagasi võtta.

## <a name="set-up-reallocation"></a>Ümberjaotamise häälestamine

Ümberjaotamise protsessi mõjutab üks parameeter.

Kuna ümberjaotamist saab teha müügitellimusel, mis on osaliselt või täielikult arveldatud, tuleb kõik arve varasemad raamatupidamiskirjed korrigeerida uute, ümberjaotatud tulu hindade alusel. Selliseks korrigeerimiseks tühistatakse algse arve raamatupidamiskirje ja sisestatakse uus, ümberjaotatud tulu hindadel põhinev raamatupidamiskirje.

Iga organisatsioon peab ise otsustama, kas korrigeerimisega uuendatakse ainult pearaamatut või ka müügireskontrot. Langetatav otsus määrab, milline on lehe **Pearaamatu parameetrid** vahekaardi **Tulu tuvastamine** suvandi **Arvete korrigeerimiste sisestamine müügireskontrole ümberjaotamisel** kohane säte (**Tulu tuvastamine \> Häälestamine \> Pearaamatu parameetrid**). Kohane säte sõltub konkreetsest stsenaariumist. Lisateavet võimalike stsenaariumite kohta leiate käesolevas teemas allpool jaotises [Ümberjaotamise stsenaariumid](#scenarios-for-reallocation) olevate linkide kaudu.

[![Tulu tuvastamise vahekaart pearaamatu parameetrite lehel.](./media/01_RevRecScenarios.png)](./media/01_RevRecScenarios.png)

Kui suvand **Arvete korrigeerimiste sisestamine müügireskontrole** on määratud olekusse **Jah**, on ümberjaotamise protsessil järgmised tulemused.

- Müügireskontros luuakse kreeditdokument, et tühistada korrigeerimist vajav arve.

    - Kreeditdokument kasutab algset arvenumbrit uuesti, kuid sellele lisatakse number „-1“.
    - Kreeditdokument tasakaalustatakse automaatselt algse arvega. Kui originaalarve oli juba tasakaalustatud teise kreeditdokumendi või maksega, siis see tasakaalustus tühistatakse automaatselt.
    - Kreeditdokument sisestatakse pearaamatusse, et tühistada algsele arvele sisestatud raamatupidamiskirje. Kuid varude ja tuletusreegli (COGS) kande kirjeid ei tühistata.

- Müügireskontros luuakse uus arve, mis põhineb uutel, ümberjaotatud hinna summatel.

    - Uus arve kasutab algset arvenumbrit uuesti, kuid sellele lisatakse number „-2“.
    - Uus arve tasakaalustatakse automaatselt kõigi kreeditdokumentide või maksetega, mis olid varem algse arvega tasakaalustatud.
    - Uus arve sisestatakse pearaamatusse, kasutades uusi, ümberjaotatud tulu hinna summasid. Seda ei sisestata uuesti varude ja COGS-kontodele, kuna need kirjed säilitatakse algse arve raamatupidamiskirjel.

Kui suvand **Arvete korrigeerimiste sisestamine müügireskontrole** on määratud olekusse **Ei**, on ümberjaotamise protsessil järgmised tulemused.

- Tühistatud raamatupidamiskirje sisestatakse ainult pearaamatusse. Tühistatakse kogu algse arve arvestus, v.a varude ja COGS-i konto kirjed.
- Uutel, ümberjaotatud tulu hindadel põhinev uus raamatupidamiskirje sisestatakse ainult pearaamatusse. Seda ei sisestata uuesti varude ja COGS-kontodele, kuna need kirjed säilitatakse algse arve raamatupidamiskirjel.
- Lehel **Kliendi kanded** olevat arvet ei mõjutata ega muudeta, vaid see kajastab endiselt algset raamatupidamiskirjet. Puudub viide tühistamisele või uutele raamatupidamiskirjetele.

Nagu eelnevalt mainitud, saate kas uuendada ainult pearaamatut või uuendada nii pearaamatut kui müügireskontrot. Mõlemal teguviisil on oma plussid ja miinused. Enne valiku langetamist soovitame teil hinnata oma organisatsiooni vajadusi. Kui uuendate nii pearaamatut kui müügireskontrot, näidatakse õigeid raamatupidamiskirjeid uuel arvel ja neid saab vaadata dokumendis lehel **Kliendi kanded**. Lisaks kasutatakse tasakaalustusprotsessis uuendatud raamatupidamiskirjeid skontode ja kasumi või kahjumi sisestamiseks. Teisest küljest näidatakse kreeditdokumenti ja uut arvet kliendi väljavõtetel ja ajalise jaotuse aruannetel sarnaselt muudele kreeditdokumentidele ja kliendi arvetele. Nende dokumentide kirjelduses näidatakse, et need loodi raamatupidamise korrektsiooni kaudu.

## <a name="run-the-reallocation-process"></a>Ümberjaotamise protsessi käitamine

Ümberjaotamise protsessi alustamiseks valige **Hinna ümberjaotamine uute tellimuse ridadega** mis tahes müügitellimuses, mis on tarvis ümber jaotada. Teise variandina võite avada **Tulu tuvastamine \> Perioodilised ülesanded \> Hinna ümberjaotamine uute tellimuse ridadega** ja sisestada kohased filtrid, näiteks kliendi konto.

[![Leht Hinna ümberjaotamine uute tellimuse ridadega.](./media/02_RevRecScenarios.png)](./media/02_RevRecScenarios.png)

Lehe **Hinna ümberjaotamine uute tellimuse ridadega** ülemise ruudustiku nimi on **Müük**. Selles loetletakse kliendi müügitellimused. Valige müügitellimused, mis tuleb ümber jaotada. Projekti müügitellimusi ei saa valida, kuna projekti müügitellimusi ei saa ümber jaotada. Samuti ei saa te valida müügitellimusi, millel juba on ümberjaotamise ID, kuna projektiväliseid müügitellimusi saab ümber jaotada ainult üks kord. Kui müügitellimusel on ümberjaotamise ID, on teine kasutaja selle juba ümberjaotamisele märkinud.

Lehe alumise ruudustiku nimi on **Read**. Pärast ühe või mitme müügitellimuse valimist ruudustikul **Müük** kuvatakse ruudustikul **Read** müügitellimuse read. Valige müügitellimuse read, mis tuleb ümber jaotada. Kui valisite ainult ühe müügitellimuse, tuleb sama müügitellimuse read ümber jaotada. Selline olukord võib tekkida, kui üks müügitellimuse ridadest oli eelnevalt arveldatud ja seejärel lisati uus rida või olemasolev rida eemaldati või tühistati. Kui rida eemaldati, siis seda ruudustikus ei kuvata. Seetõttu ei saa seda valida. Kuid ümberjaotamise protsessi käivitamisel võetakse see siiski arvesse.

Kui olete vajalike müügitellimuse ridade valimise lõpetanud, kasutage toimingupaani nuppe järgmiselt.

- **Uuenda ümberjaotamist** – valitud müügitellimuse ridadele uute tulu hinna summade arvutamine. Kui rida eemaldati või tühistati, tehakse ümberjaotamine ainult teie valitud olemasolevatele ridadele. Järgmisel joonisel on toodud näide müügitellimuse ridadest enne ümberjaotamise uuendamist.

    [![Müügitellimuse read enne ümberjaotamise uuendamist.](./media/03_RevRecScenarios.png)](./media/03_RevRecScenarios.png)

    Uued tulu hinna summad kuvatakse ruudustiku **Read** veerus **Ümberjaotud summa**. Selles etapis on ümberjaotamine töödeldud, kuid see on veel arvutamata. Järgmisel joonisel on toodud näide müügitellimuse ridadest pärast ümberjaotamise uuendamist.

    [![Müügitellimuse read pärast ümberjaotamise uuendamist.](./media/04_RevRecScenarios.png)](./media/04_RevRecScenarios.png)

- **Töötle** – ümberjaotatud tulu hindade töötlemine või sisestamine. Pärast selle nupu klõpsamist ei saa ümberjaotamist enam mingil viisil tagasi võtta. Kui te ei valinud enne nupu **Töötle** klõpsamist **Uuenda ümberjaotamist**, käivitatakse ümberjaotamine automaatselt.

    - Kui ühtegi müügitellimuse rida ei ole arveldatud, uuendatakse tulu hinna summad kõigil müügitellimustel, mis valiti ümberjaotamiseks.
    - Kui üks või mitu müügitellimuse rida on arveldatud, sisestatakse korrigeerivad raamatupidamiskirjed ja korrigeeritakse kõik arveldatud müügitellimuse rea jaoks loodud tulugraafiku üksikasjad.

- **Eeldatav kanne** – kõigi arveldatud müügitellimuse ridade jaoks loodud raamatupidamiskirjete eelversiooni kuvamine. Kui ühtegi rida pole arveldatud, ei kuvata midagi. Kui te ei valinud enne nupu **Eeldatav kanne** klõpsamist **Uuenda ümberjaotamist**, käivitatakse ümberjaotamine automaatselt.
- **Tulu ümberjaotamine** – kõigi valitud ridade tulu hinna eraldamist näitava lehe avamine. Lehel olevat teavet ei saa muuta. See näitab ümberjaotamiseks kasutatud rea summasid.

    [![Ümberjaotamiseks kasutatud rea summad.](./media/05_RevRecScenarios.png)](./media/05_RevRecScenarios.png)

- **Lähtesta valitud kliendi andmed** – kui ümberjaotamise protsess käivitati, kuid seda ei viidud lõpule, kustutage ainult valitud kliendi ümberjaotamise tabelis olevad andmed. Näiteks kui märgite ümberjaotamiseks mitu müügitellimuse rida, jätate lehekülje avatuks ilma nupul **Töötle** klõpsamata ja seejärel lehekülg aegub. Sellisel juhul jäävad müügitellimuse read märgituks ja pole teisele kasutajale ümberjaotamise protsessi lõpule viimiseks kättesaadavad. Avamisel võib leht isegi tühi olla. Sellises olukorras saab nupuga **Lähtesta valitud kliendi andmed** töötlemata müügitellimused kustutada, et teine kasutaja saaks ümberjaotamise protsessi lõpule viia.

## <a name="scenarios-for-reallocation"></a>Ümberjaotamise stsenaariumid

Järgmistes teemades kirjeldatakse tulu tuvastamise erinevaid stsenaariume.

- [Tulu tuvastamise ümberjaotamine – 1. stsenaarium](rev-rec-reallocation-scenario-1.md) – sisestatakse kaks müügitellimust, kuid need ainult kinnitatakse. Sama stsenaarium annab sarnased tulemused, kui kinnitatud olekus on rohkem kui kaks müügitellimust.
- [Tulu tuvastamise ümberjaotamine – 2. stsenaarium](rev-rec-reallocation-scenario-2.md) – sisestatakse kaks müügitellimust ja seejärel lisab klient pärast esimese müügitellimuse arveldamist lepingule kauba.
- [Tulu tuvastamise ümberjaotamine – 3. stsenaarium](rev-rec-reallocation-scenario-3.md) – olemasolevale arveldatud müügitellimusele lisatakse uus rida.
- [Tulu tuvastamise ümberjaotamine – 4. stsenaarium](rev-rec-reallocation-scenario-4.md) – olemasolevalt osaliselt arveldatud müügitellimuselt eemaldatakse rida.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]