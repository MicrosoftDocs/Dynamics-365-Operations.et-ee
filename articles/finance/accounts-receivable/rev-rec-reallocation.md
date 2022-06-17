---
title: Tulu tuvastamise ümberjaotamine
description: Selles artiklis kirjeldatakse ümberjaotamist, mis võimaldab organisatsioonidel müügilepingute tingimuste muutumisel tulu hindu ümber arvutada. See sisaldab linke teistele teemadele, milles kirjeldatakse tulu tuvastamist erinevates stsenaariumites.
author: kweekley
ms.date: 09/09/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a79288fd69a2e7780ff03952b05b99db2ed88e41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903416"
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

    - See piirang eemaldatakse väljalaskes 10.0.17 ja hilisemas väljalaskes.

- Protsessi ei saa käivitada projekti müügitellimustel.

    - See piirang eemaldatakse väljalaskes 10.0.17 ja hilisemas väljalaskes.

- Kui tegemist on mitme müügitellimusega, peavad need kuuluma samale kliendikontole.
- Kõik ümberjaotatavad müügitellimused peavad olema samas kandevaluutas.
- Pärast käitamist ei saa protsessi tühistada ega tagasi võtta.

    - See piirang eemaldatakse väljalaskes 10.0.17 ja hilisemas väljalaskes.

- Ümberjaotust saab teha ainult kas müügitellimustele või projekti müügitellimustele. Seda ei saa teha müügitellimuste ja projekti müügitellimuste kombinatsioonile.

    - See piirang eemaldatakse väljalaskes 10.0.17 ja hilisemas väljalaskes.

## <a name="set-up-reallocation"></a>Ümberjaotamise häälestamine

Ümberjaotamise protsessi mõjutab üks parameeter.

Kuna ümberjaotamist saab teha müügitellimusel, mis on osaliselt või täielikult arveldatud, tuleb kõik arve varasemad raamatupidamiskirjed korrigeerida uute, ümberjaotatud tulu hindade alusel. Selliseks korrigeerimiseks tühistatakse algse arve raamatupidamiskirje ja sisestatakse uus, ümberjaotatud tulu hindadel põhinev raamatupidamiskirje.

Iga organisatsioon peab ise otsustama, kas korrigeerimisega uuendatakse ainult pearaamatut või ka müügireskontrot. Langetatav otsus määrab, milline on lehe **Pearaamatu parameetrid** vahekaardi **Tulu tuvastamine** suvandi **Arvete korrigeerimiste sisestamine müügireskontrole ümberjaotamisel** kohane säte (**Tulu tuvastamine \> Häälestamine \> Pearaamatu parameetrid**). Kohane säte sõltub konkreetsest stsenaariumist. Lisateavet võimalike stsenaariumite kohta leiate käesolevas artiklis allpool jaotises [Ümberjaotamise stsenaariumid](#scenarios-for-reallocation) olevate linkide kaudu.

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

Lehe **Hinna ümberjaotamine uute tellimuse ridadega** ülemise ruudustiku nimi on **Müük**. Selles loetletakse kliendi müügitellimused. Valige müügitellimused, mis tuleb ümber jaotada. Kui müügitellimusel on ümberjaotamise ID, on teine kasutaja selle juba ümberjaotamisele märkinud. Kui üks või mitu müügitellimust on eelnevalt ümber jaotatud ja tuleb kaasata teise ümberjaotusse, tuleb nende müügitellimuste ümberjaotamine esmalt tagasi võtta. Seejärel saab selle kaasata uude ümberjaotamisse. Lisateavet lugege selle artikli jaotistest [Ümberjaotamise tagasivõtmine](#undo-a-reallocation) ja [Mitmekordne ümberjaotamine](#reallocate-multiple-times).

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

## <a name="undo-a-reallocation"></a>Ümberjaotamise tagasivõtmine

Ümberjaotamise saab tagasi võtta järgmise ümberjaotamise käitamisega. Ümberjaotamine toimub uuesti ja kasutaja valib teise ümberjaotamise protsessi kaasamiseks erinevad müügitellimusread.

Kui ümberjaotamine toimub kahe või enama eraldi müügitellimuse vahel, saab selle tagasi võtta, kui mis tahes ümberjaotusse kaasatud müügitellimusest valida **Hinna ümberjaotamine uute tellimuseridadega**. Ümberjaotamise tagasivõtmiseks ei saa valida **Tulu tuvastamine \> Perioodilised ülesanded \> Hinna ümberjaotamine uute tellimuseridadega**, kuna sel viisil avatud lehel kuvatakse ainult ümberjaotamise ID-ta müügitellimused. Ümberjaotamise ID määratakse pärast dokumendi ümberjaotamist.

Tühistage lehel **Hinna ümberjaotamine uute tellimuseridadega** nende müügitellimuste märked, mis tuleks lepingulisest kokkuleppest välistada. Ümberjaotamise töötlemiseks kasutage toimingupaani nuppe **Värskenda ümberjaotamist** ja **Töötle**. Kui kõik müügitellimused (v.a aktiivsed müügitellimused) on märkimata, eemaldatakse ümberjaotamise ID muudatuse töötlemisel.

Kui ümberjaotamine on tehtud uue rea lisamisega täielikult või osaliselt arveldatud müügitellimusele, saab ümberjaotamise tagasi võtta ainult siis, kui eemaldate selle rea müügitellimusest ja käivitate ümberjaotamise uuesti. Müügitellimuse rida tuleb eemaldada, kuna eeldatakse, et kõik müügitellimuse read on sama lepingu osa. Müügitellimuse rea märkimist ei saa tühistada, kui olete lehel **Hinna ümberjaotamine uute tellimuse ridadega**.

## <a name="reallocate-multiple-times"></a>Mitmekordne ümberjaotamine

Mitut ümberjaotamist saab teha samale müügitellimusele, kui lepingusse on tehtud mitu muudatust. Muudatuste grupeerimiseks käivitab ümberjaotamine ümberjaotamise ID määramise müügitellimusele või müügitellimuste grupile. Mitme ümberjaotamise tegemisel kasutab iga täiendav ümberjaotamine esimese ümberjaotamisega sama ümberjaotamise ID-d.

Näiteks sisestatakse müügitellimus 00045 ja sellel on mitu rida. Pärast müügitellimuse täielikku arveldamist lisatakse sellele uus müügitellimuse rida. Seejärel käivitatakse ümberjaotamine. Selleks avatakse leht **Hinna ümberjaotamine uute tellimuse ridadega** kas müügitellimusest 00045 või valitakse **Tulu tuvastamine \> Perioodilised ülesanded \> Hinna ümberjaotamine uute tellimuse ridadega**. Müügitellimusele määratakse ümberjaotamise ID **Reall000001**.

Samale lepingule luuakse teine müügitellimus 00052. Ümberjaotamise saab uuesti käivitada, avades lehe **Hinna ümberjaotamine uute tellimuse ridadega** müügitellimusest 00045, kuid mitte müügitellimusest 00052. Kui avate lehe **Hinna ümberjaotamine uute tellimuse ridadega** müügitellimusest 00052, ei kuvata müügitellimust 00045, kuna sellele on määratud ümberjaotamise ID. Lehel kuvatakse ainult müügitellimused, millel pole ümberjaotamise ID-d.

Teiseks ümberjaotamiseks on kaks viisi. Saate tagasi võtta müügitellimuse 00045 ümberjaotamise. Sel juhul eemaldatakse ümberjaotamise ID ning seejärel saate teha ümberjaotamise müügitellimusest 00045 või müügitellimusest 00052. Teise võimalusena saate lehe **Hinna ümberjaotamine uute tellimuse ridadega** avada müügitellimusest 00045 ja lisada teise müügitellimuse. Ümberjaotamise töötlemisel määratakse ümberjaotamise ID **Reall000001** nii müügitellimusele 00045 kui ka müügitellimusele 00052.

## <a name="scenarios-for-reallocation"></a>Ümberjaotamise stsenaariumid

Järgmistes teemades kirjeldatakse tulu tuvastamise erinevaid stsenaariume.

- [Tulu tuvastamise ümberjaotamine – 1. stsenaarium](rev-rec-reallocation-scenario-1.md) – sisestatakse kaks müügitellimust, kuid need ainult kinnitatakse. Sama stsenaarium annab sarnased tulemused, kui kinnitatud olekus on rohkem kui kaks müügitellimust.
- [Tulu tuvastamise ümberjaotamine – 2. stsenaarium](rev-rec-reallocation-scenario-2.md) – sisestatakse kaks müügitellimust ja seejärel lisab klient pärast esimese müügitellimuse arveldamist lepingule kauba.
- [Tulu tuvastamise ümberjaotamine – 3. stsenaarium](rev-rec-reallocation-scenario-3.md) – olemasolevale arveldatud müügitellimusele lisatakse uus rida.
- [Tulu tuvastamise ümberjaotamine – 4. stsenaarium](rev-rec-reallocation-scenario-4.md) – olemasolevalt osaliselt arveldatud müügitellimuselt eemaldatakse rida.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
