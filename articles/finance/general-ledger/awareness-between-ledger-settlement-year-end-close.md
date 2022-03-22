---
title: Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel
description: See teema annab teavet täiustuste kohta, mis mõjutavad pearaamatu tasakaalustusi ja pearaamatu aastalõpu sulgemist.
author: kweekley
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: acfbcf1467363262769884063efbc1a6d6e21eb1
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075730"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Microsofti Dynamics 365 Finance versioonis 10.0.25 **on pearaamatu tasakaalustuse ja aastalõpu sulgemisfunktsiooni** vaheline teadlikkus saadaval **funktsioonihalduse** tööruumis. See funktsioon lisab kaks peamist täiustust, mis mõjutavad pearaamatu tasakaalustuse ja pearaamatu aastalõpu sulgemist.

Pearaamatu aastalõpu sulgemisel ei kaasata tasakaalustatud pearaamatukandeid enam järgmise finantsaasta algsaldosse. See täiustus tagab, et algsaldosse kaasatakse ainult lahendamata pearaamatukanded. See on oluline pearaamatu välisvaluuta ümberhindamise käivitamisel. Välisvaluuta ümberhindamist käitatakse ainult pearaamatukannete puhul, mille olek **pole tasakaalustatud**. Kuid enne **pearaamatu tasakaalustuse ja aastalõpu sulgemisfunktsiooni** teadlikkuse avaldamist võttis algsaldo kokku nii tehingu, mille olek **on Arveldatud**, kui ka need, mille olek **pole tasakaalus**, kui ka summeeritud summa olekuks **Määrati Tasakaalustamata**.

Teine täiustus võimaldab teil pearaamatu aasta lõpus sulgeda üksikasjalikud algsaldo kanded. **Kui suvandi Säilita üksikasjad aastalõpu sulgemise** ajal väärtuseks **on seatud Jah**, luuakse iga tasakaalustamatud andmikukande jaoks eraldi algsaldo. See säte on määratletud iga pearaamatu tasakaalustuse häälestuse põhikonto jaoks. Hoides algsaldo üksikasjalikke kandeid, parandate oluliselt võimet tasakaalustada järgmisel finantsaastal lahendamata pearaamatukandeid.

Uute täiustuste toetamiseks tehti pearaamatu tasakaalustuses ja aastalõpu sulgemises muudatusi.

### <a name="changes-to-ledger-settlement"></a>Pearaamatu tasakaalustuse muudatused

- Pearaamatu tasakaalustus peab toimuma finantsaasta jooksul.
- Pearaamatu tasakaalustamine tuleb teha ühel põhikontol tehtavate kannete puhul. Põhikonto on nüüd nõutav filter **lehel Pearaamatu tasakaalustus**.
- Pearaamatu tasakaalustuse ja pearaamatu tasakaalustuse ümberpööramist ei saa teha suletud finantsaasta jooksul konteeritud kannete puhul (teisisõnu on aastalõpu sulgemine käivitatud).

### <a name="changes-to-year-end-close"></a>Muudatused aastalõpu sulgemises

- Aastalõpu sulgemist ei saa tagasi pöörata, kui järgmisel finantsaastal on tasakaalustatud avasaldo tehinguid. See muudatus rakendub siis, kui aastalõpu sulgemine on tühistatud või kui aastalõpu sulgemine kordub ja **suvand Kustuta olemasolevad aastalõpukanded aasta** sulgemisel on pearaamatu parameetrites seatud **jah**.
- Kui suvandi **Säilita üksikasjad aastalõpu sulgemise** ajal on pearaamatu tasakaalustuse mis tahes bilansikonto puhul seatud **Jah**, luuakse selle põhikonto jaoks üksikasjalikumad algsaldo kanded.

## <a name="before-you-enable-the-feature"></a>Enne funktsiooni lubamist

Funktsionaalsuse ja andmemudeli muutuste tõttu on oluline enne funktsiooni lubamist arvestada järgmiste punktidega.

- Kõik kanded, mis on märgitud tasakaalustamiseks, kuid pole tasakaalustatud, märgitakse funktsiooni lubamisel automaatselt märkimata. Töökaotuse vältimiseks tasakaalustage kõik märgitud kanded enne funktsiooni lubamist.
- Mõned organisatsioonid käivitavad sama finantsaasta aasta sulgemist mitu korda. Ärge lubage funktsiooni, kui aastalõpu sulgemine on juba üks kord käivitatud ja seda käitatakse uuesti samal finantsaastal. Funktsioon peab olema lubatud enne esimese aastalõpu sulgemist või pärast finantsaasta viimase aasta lõpu sulgemist.

  Kui soovite funktsiooni lubada, kuid aastalõpu sulgemine on juba üks kord käivitatud, peate enne funktsiooni lubamist aastalõpu sulgema.

- Kuna tasakaalustamine eelarveaastate lõikes pole enam lubatud, soovitame selle funktsiooni enne aastalõpu sulgemisprotsessi alustamist lubada. Selleks, et tagada, et eelmised finantsaastatevahelised arveldused ei mõjutaks järgmise majandusaasta algsaldosid, tuleks algsaldo kanne tasakaalustada lõpetatava finantsaasta jaoks.
- Kuna põhikontode tasakaalustamine pole enam lubatud, kohandage oma kontoplaani või protsesse vastavalt vajadusele, et pearaamatu tasakaalustamist saaks teha samal põhikontol.
- Funktsiooni ei saa lubada, kui kasutatakse avaliku sektori aastalõpu sulgemisprotsessi.

## <a name="set-up-ledger-settlement"></a>Pearaamatu tasakaalustuse häälestamine

Pärast funktsiooni lubamist ja enne järgmise aastalõpu sulgemist peab iga organisatsioon kindlaks tegema, kas ta hoiab tehingu üksikasjad aasta lõpus lähedal. Valik ei mõjuta eelmiste aastalõpu sulgemisprotsesside algsaldo postitusi.

Suvand **Säilita üksikasjad aastalõpu sulgemise** ajal on seatud igale põhikontole **lehel Pearaamatu tasakaalustuse häälestus**.

1.  **Avage pearaamatu** > **ledger setupGeneral** > **ledger parameters**.
2.  Valige vahekaardil **Pearaamatu tasakaalustused** suvand **Pearaamatu tasakaalustuskontod**.

- või -

1.  **Avage pearaamatPeriodsed** > **ülesandedLedgeri** > **tasakaalustused**.
2.  Valige **Pearaamatu tasakaalustuskontod**.

Lehele Pearaamatu tasakaalustused **on lisatud** kaks veergu.
    
- **Peamine konto tüüp** – see veerg on mõeldud ainult informatiivsetel eesmärkidel. See näitab põhikontole määratud tüüpi.
- **Hoidke aasta lõpus üksikasjad lähedal** – vaikimisi on suvandi väärtuseks **seatud Ei**. Seda saab seadistada **Jah** ainult siis, kui väärtus on **Põhikonto tüüp** veerg on **Eelarve**, **·**, või **Vastutus**. Kui suvand on seatud **Ei**, postitatakse algsaldod kokkuvõttes, nagu tavaliselt aastalõpu sulgemisel. Kui see on seatud **Jah**, luuakse algsaldod üksikasjalikult iga peakonto tehingu kohta, mida põhikontol ei arveldata.

## <a name="year-end-close"></a>Aastalõpu sulgemine

Kui jooksed aastalõpu lähedale minnes **Pearaamat** > **Periood sulgub** > **Aasta lõpp**, loob protsess põhikontode algsaldod, mis on määratletud pearaamatu arveldamiseks. Algsaldod luuakse kas kokkuvõtlikult või üksikasjalikult, olenevalt pearaamatu arvelduse seadistusest. Protsess välistab arveldatud pearaamatutehingud, olenemata sellest, kas konteerite iga põhikonto algsaldo kokkuvõtlikult või üksikasjalikult.

Näiteks 2021. eelarveaastal postitatakse mitu tehingut põhikontole 130100.

| Töölehe kood | Vautšer  | Kuupäev       | Tüüp      | Pearaamatukonto | Konto nimi        | Kirjeldus       | Valuuta | Summa kandevaluutas | Summa  | Summa aruandlusvaluutas |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 3.12.2021  | Kasutusel | 130100-001-    | Müügireskontro | Teenustasu       | USA dollar      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 5.12.2021  | Kasutusel | 130100-002-    | Müügireskontro | Kommunaalteenused         | USA dollar      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 16.12.2021 | Kasutusel | 130100-001-    | Müügireskontro | Tagasimakse            | USA dollar      | -100                           | -100    | -100                         |
| 20851          | ARP‑8000 | 20.12.2021 | Kasutusel | 130100-002-    | Müügireskontro |                   | USA dollar      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | Kasutusel | 130100-002-    | Müügireskontro |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 21.12.2021 | Kasutusel | 130100-002-    | Müügireskontro | Krediit arvel | USA dollar      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 28.12.2021 | Kasutusel | 130100-001-    | Müügireskontro | Kommunaalteenused         | USA dollar      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 29.12.2021 | Kasutusel | 130100-002-    | Müügireskontro | Teenindus           | USA dollar      | 300                            | 300     | 300                          |

Nendest tehingutest kolm arveldatakse pearaamatu arvelduse käigus.

Olemas arve 175 USA dollarit (175 USD). See arve tasuti eurodes (EUR) maksega ja võeti sularahasoodustus.

| Töölehe kood | Vautšer  | Kuupäev       | Tüüp      | Pearaamatukonto | Konto nimi        | Kirjeldus | Valuuta | Summa kandevaluutas | Summa  | Summa aruandlusvaluutas |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 5.12.2021  | Kasutusel | 130100-002-    | Müügireskontro | Kommunaalteenused   | USA dollar      | 175                            | 175     | 175                          |
| 20851          | ARP‑8000 | 20.12.2021 | Kasutusel | 130100-002-    | Müügireskontro |             | USA dollar      | -0,88                          | -0,88   | -0,88                        |
| 20853          | ARPM0004 | 20.12.2021 | Kasutusel | 130100-002-    | Müügireskontro |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Põhikonto 130100 tulemused sõltuvad sellest, kas funktsioon on lubatud enne aastalõpu sulgemist. Kui funktsioon on lubatud, sõltub tulemus ka suvandi Säilita detail aastalõpu sulgemise ajal sättest.

### <a name="the-feature-isnt-enabled"></a>Funktsioon pole lubatud
Aastalõpu sulgemine loob 2022. aastal põhikonto 130100 kolm algsaldo tehingut. Arvestusvaluutas tehtud tehingute summa on USD 525.

| Töölehe kood | Vautšer  | Kuupäev     | Tüüp    | Pearaamatukonto | Konto nimi        | Kirjeldus | Valuuta | Summa kandevaluutas | Summa  | Summa aruandlusvaluutas |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro |             | USA dollar      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro |             | USA dollar      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Kuigi maksetehing summas -127,11 eurot arveldati, tuleb tehing siiski algsaldo.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Funktsioon on lubatud ja Säilita üksikasju aastalõpu sulgemise ajal = Ei

Aastalõpu sulgemine loob 2022. aastal põhikonto 130100 kaks algsaldo tehingut. Arvestusvaluutas tehtud tehingute summa on endiselt USD 525, kuid pearaamatus arveldatud tehingud jäetakse algsaldost välja. Konto 130100-002- kogusumma on USD 299.12 asemel USD 125 ja tehing 127,11 EUR/174,12 USD on täielikult välistatud.

| Töölehe kood | Vautšer  | Kuupäev     | Tüüp    | Pearaamatukonto | Konto nimi        | Kirjeldus | Valuuta | Summa kandevaluutas | Summa | Summa aruandlusvaluutas |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro |             | USA dollar      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro |             | USA dollar      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Funktsioon on lubatud ja Säilita üksikasju aastalõpu sulgemise ajal = Jah

Aastalõpu sulgemine loob 2022. aastal põhikontole 130100 viis algsaldo tehingut. Iga viie arveldamata tehingu jaoks luuakse eraldi algsaldo tehing. Arvestusvaluutas tehtud tehingute summa on endiselt USD 525.

| Töölehe kood | Vautšer  | Kuupäev     | Tüüp    | Pearaamatukonto | Konto nimi        | Kirjeldus       | Valuuta | Summa kandevaluutas | Summa | Summa aruandlusvaluutas |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro | Teenustasu       | USA dollar      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro | Tagasimakse            | USA dollar      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro | Krediit arvel | USA dollar      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro | Kommunaalteenused         | USA dollar      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro | Teenindus           | USA dollar      | 300                            | 300    | 300                          |

Kui tehingu üksikasjad säilitatakse, ei mõjuta see esialgseid üksikasjalikke tehinguid. Need jäävad suletaval eelarveaastal postitatud ja lahendamata. Nende tehingute koopia luuakse algsaldo jaoks. Algsaldo tehingutesse kopeeritakse järgmised algsete tehingute väärtused.

- Pearaamatukonto (põhikonto ja kõik finantsdimensioonid)
- Summad tehingu-, raamatupidamis- ja aruandlusvaluutas
- Kirjeldus
- Sisestamiskiht
- Sisestamistüüp

   > [!NOTE]
   > Ühelegi teisele algsaldo tehingule ei ole määratud konteerimistüüpi. Seetõttu saab konteerimistüüpi kasutada üksikasjalikult esile toodud avamistehingute eristamiseks.

Algsaldo üksikasjalikes tehingutes peavad mõned algsete tehingute väljad muutuma. Algsaldo tehingute kuupäev on alati järgmise eelarveaasta esimene päev. Ajakirja number peab muutuma ja vautšeri number muutub aastalõpu sulgemise dialoogiboksi sisestatud väärtuseks.

Teavet algsete tehingute kohta leiate aadressilt **Pearaamatu arveldus** lehel. Iga üksikasjalik algsaldo tehing näitab **Algne tehingukuupäev** veerus ruudustikus. See veerg aitab teil uue eelarveaasta tehinguid sobitada. Saate valida **Vaata originaalvoucherit** naasmiseks täieliku originaalvautšeri juurde.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Kannete tasakaalustamine
Pearaamatu kannete tasakaalustamiseks toimige järgmiselt.

1. **Avage pearaamatPeriodsed** > **ülesandedLedgeri** > **tasakaalustused**.
2.  Määrake lehe ülaosas olevad filtrid.

    1. Kuupäevavahemiku valimine. Teise võimalusena valige kuupäevavahemiku automaatseks täitmiseks kuupäevavahemiku kood.

       - Kuupäevavahemik ei tohi ületada eelarveaastaid. Kui kuupäevavahemik ületab eelarveaastaid, siis valiku tegemisel tehinguid ei kuvata **Kuva tehingud**.
       - Kui kuupäevavahemik on avatud eelarveaastal, saab tehinguid arveldada ja arvelduse tühistada. Kui kuupäevavahemik on suletud eelarveaastal või kui aastalõpu sulgemine on lõppenud, näidatakse tehinguid, kuid neid ei saa arveldada ega arveldamata. Tehingute märgistuse saate tühistada ainult suletud eelarveaastal. Kui kuupäevavahemik on suletud eelarveaastasse, **Märgi valituks**, **märgitud tehingud**, ja **Pöördmärgistatud tehingud** nupud pole saadaval.

    2. Valige põhikonto, millega tehinguid näidata. See väli on kohustuslik. Otsing näitab ainult peamisi kontosid, mis on valitud **Pearaamatu arveldus** lehekülg ettevõtte kontoplaani jaoks.
    3. Valige postitamiskiht. Te ei saa arveldada tehinguid, mis on erinevates postitamiskihtides.
    4. Põhikonto ja dimensioonide kuvamiseks eraldi veergudes valige finantsdimensioonide komplekt.

3.  Valige **Kuva tehingud** et kuvada kõik tehingud, mis vastavad teie määratud filtritele. Filtrite või dimensioonikogumite muutmisel peate uuesti valima **Kuva kanded**.
4.  Valige arveldamiseks read. Väärtus **Valitud summa** lehe ülaosas olev väli suureneb või väheneb, et kajastada valitud ridade kogusummat.
5.  Kui olete tehingute valimise lõpetanud, valige **Märgi valituks**. Iga valitud tehingu kohta kuvatakse linnuke **Märgitud** veerg. Lisaks väärtus **Märgitud summa** ruudustiku kohal olev väli suureneb või väheneb, et kajastada märgitud joonte kogusummat.
6.  Kui väärtus on **Märgitud summa** väli on **0** (null), valige **Arveldage märgitud tehingud**.

    - Osaline arveldamine pole lubatud. Näiteks ei saa te arveldada $100 deebettehingut $90 krediiditehinguga. Arveldusse kaasamiseks tuleb märkida ka ülejäänud $10 krediiditehing.
    - Sisesta arvelduskuupäev. Kuupäev peab olema arveldamiseks märgitud tehingute viimasel kuupäeval või hilisem.

Märgistatud kannete olek uuendatakse olekule **Tasakaalustatud**.

> [!IMPORTANT]
> Kõik tehingud, mille olete aktiivse juriidilise isiku ja valitud põhikonto jaoks arveldamiseks märkinud, arveldatakse. Tehingud ei pea lehel ilmuma. Need lahendatakse isegi siis, kui need on filtri tõttu peidetud.

Mõned protsessid, näiteks tehingu tühistamine, arveldavad pearaamatu tehingud automaatselt. Näiteks arveldatakse makse ja arve jaotises Debitoorsed arved ning arveldamine tekitab realiseeritud kasumi/kahjumi. Makse ja arve arveldamisel ei arveldata ühtegi pearaamatu tehingut, nt debitoorsete arvete pearaamatu konto tehinguid. Kui aga Debitoorses arvelduses on makse ja arve arveldamata, siis debitoorse võlgnevuste arvelduse tühistamise käigus konteeritud pöördarvestuskanne põhjustab algsed ja pöördarvestuse kanded pearaamatus arveldamise. Kui **Teadlikkus pearaamatu arvelduse ja aastalõpu sulgemise vahel** Kui funktsioon on lubatud, ei toimu tühistamise pearaamatu arveldust automaatselt, kui tühistamise kuupäev on muul eelarveaastal.

## <a name="use-excel-for-ledger-settlement"></a>Kasutage pearaamatu arveldamiseks Excelit

Tehingud, mis on näidatud **Pearaamatu arveldus** lehe saab eksportida Excelisse. Excelis saate tehinguid täiendavalt filtreerida, et määrata, millised tehingud arveldamiseks märkida.
Mõlemad pearaamatu arveldusüksused ekspordivad pearaamatu tehinguid ainult sellel põhikontol, mis on valitud **Pearaamatu arveldus** lehel. Kuigi suletud eelarveaastate tehinguid saab Exceli abil endiselt märgistada või märgistamata jätta, ei saa neid arveldada. Lisaks ei saa arveldatud tehinguid sellel eelarveaastal tagasi võtta.

## <a name="make-transactions-easier-to-find"></a>Muudke kannete leidmine lihtsamaks

The **Pearaamatu arveldused** leht sisaldab võimalusi, mis hõlbustavad arveldamiseks vajalike tehingute vaatamist.

• Kasuta **Märgitud** filter tehingute filtreerimiseks selle alusel, kas **Märgitud** nende jaoks on märgitud märkeruut.
• Kasuta **Olek** filter tehingute filtreerimiseks nende oleku alusel.
• Valige **Sorteeri absoluutsumma järgi** sorteerida summad absoluutväärtuse järgi. Sel viisil saate rühmitada deebeteid ja krediite, millel on sama summa.

## <a name="reverse-a-settlement"></a>Tasakaalustuse tühistamine

Saate tühistada ekslikult tehtud tasakaalustuse.

1.  Järgige samme 1 kuni 3 jaotises [Arvelda tehingud](#settle-transactions) Teid huvitavate tehingute kuvamiseks.
2.  Valige **Oleku** filtris valik **Tasakaalustatud**.
3.  Valige ümberpööramiseks read.
4.  Valige **Pöördmärgistatud tehingud**. Kõigi sama arveldus-ID-ga tehingute olekut värskendatakse **Ei lahendatud**.

> [!IMPORTANT]
> Kõik sama arveldus-ID-ga tehingud tühistatakse, isegi kui need pole märgitud. Näiteks märgiti ja arveldati neli rida. Kõigil neljal real on sama asula ID. Kui märgite ühe neist neljast reast ja seejärel valige **Pöördmärgistatud tehingud**, pööratakse kõik neli rida ümber.






