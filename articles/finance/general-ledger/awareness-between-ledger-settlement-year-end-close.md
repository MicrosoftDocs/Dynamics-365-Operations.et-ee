---
title: Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel
description: See artikkel annab teavet täiustuste kohta, mis mõjutavad pearaamatu tasakaalustusi ja Pearaamatu aasta lõpu sulgemist.
author: kweekley
ms.date: 04/06/2022
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
ms.openlocfilehash: 30d3cc0bbd97cd006f12d06cda64ee63cb42252e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902512"
---
# <a name="awareness-between-ledger-settlement-and-year-end-close"></a>Teadlikkus pearaamatu tasakaalustamise ja aastalõpu sulgemise vahel

[!include [banner](../includes/banner.md)]


Finantside Microsoft Dynamics versioonis 10.0.25 **on** pearaamatu tasakaalustuse ja aasta lõpu sulgemise funktsiooni vaheline teave saadaval funktsioonihalduse **tööruumis**. See funktsioon lisab kaks peamist täiustust, mis mõjutavad pearaamatu tasakaalustust ja pearaamatu aasta lõpu sulgemist.

Pearaamatu aasta sulgemise jooksul ei kaasata tasakaalustatud pearaamatukandeid enam järgmise rahandusaasta algsaldosse. See täiustus tagab, et algsaldosse kaasatakse ainult tasakaalustamata pearaamatukanded. On oluline pearaamatu välisvaluuta ümberarvutamise käivitamisel. Välisvaluuta ümberarvutamine käivitatakse ainult pearaamatu kannete puhul, mille olek on **Tasakaalustata**. Kuid enne pearaamatu **tasakaalustamise ja aasta lõpu sulgemise funktsiooni vahelist teadmist summeeriti algsaldo nii kandes,** **·** **mille olek on Tasakaalustatud kui ka need, mille olek on Tasakaalustamata ja** summeeritud summa olekuks seadistati Tasakaalustamata.**·**

Teine täiustus võimaldab teil pearaamatu aasta lõpu sulgemise ajal sisestada üksikasjalikud algsaldo kanded. Kui aasta **lõpu sulgemisel üksikasjade säilitamine** suvandi **väärtuseks** on seatud Jah, luuakse iga tasakaalustamata pearaamatukande jaoks eraldi algsaldo. See säte määratletakse pearaamatu tasakaalustuse seadistuses igale põhikontole. Säilitades algsaldo üksikasjalikke kandeid, parandate oluliselt tasakaalustamata pearaamatukannete tasakaalustamisvõimet järgmisel rahandusaastal.

Uute täienduste toetamiseks tehti pearaamatu tasakaalustusse ja aasta lõpu sulgemisse muudatusi.

### <a name="changes-to-ledger-settlement"></a>Pearaamatu tasakaalustamise muudatused

- Pearaamatu tasakaalustamine peab olema rahandusaasta sees.
- Pearaamatu tasakaalustamine peab olema tehtud ühe põhikonto kannete puhul. Põhikonto on nüüd pearaamatu tasakaalustuse lehel nõutav **filter**.
- Pearaamatu tasakaalustamist ja pearaamatu tasakaalustuse tagasipööramist ei saa teha kannete puhul, mis sisestatakse suletud rahandusaastasse (teisisõnu on aasta lõpu sulgemine käitatud).

### <a name="changes-to-year-end-close"></a>Aasta lõpu sulgemise muudatused

- Aasta lõpu sulgemist ei saa tagasi pöörata, kui järgmises rahandusaastas on tasakaalustatud mis tahes algsaldo kandeid. See muudatus kehtib aasta lõpu sulgemise tühistamisel **või** **aasta** lõpu sulgemise uuestikäivitusel ja olemasolevate aasta lõpu kirjete kustutamisel aasta sulgemisel on aasta sulgemisel seatud suvandile Jah pearaamatu parameetrites.
- Kui aasta **lõpu sulgemisel üksikasjade säilitamine** **valik** on pearaamatu tasakaalustuses mis tahes bilansikonto puhul seatud väärtusele Jah, luuakse sellele põhikontole üksikasjalikumad algsaldo kanded.

## <a name="before-you-enable-the-feature"></a>Enne funktsiooni lubamist

Funktsiooni ja andmemudeli muudatuste tõttu on oluline arvestada enne funktsiooni lubamist järgmisi punkte:

- Kuna algsaldosse tuuakse edasi ainult tasakaalustatud kanded, peate tühistama praeguse rahandusaasta kanded, mis tasakaalustatakse eelmise rahandusaasta kannetega. Kanded tuleb lähtestada praeguse rahandusaasta kannete suhtes. Seda saab teha korrigeeriva kirje kaudu jooksvas rahandusaastas. Korrektsioon tühistab summeeritud algsaldod ja vastaskontod üksikasjaliku kandega, mis on vajalik pearaamatu kannete tasakaalustamiseks praegusel aastal. 

  > [!IMPORTANT]
  > Kui seda ei tehtud, kuvatakse jooksva **rahandusaasta** aasta sulgemisel tasakaalustatusest väljas tõrge. Kui pearaamatukandeid ei saa tasakaalustada ja lähtestada sama finantsaastaga, siis ärge seda funktsiooni enne aasta lõpu sulgemist lubage. Lubage funktsioon kohe pärast aasta lõpu sulgemist ja enne uute pearaamatukannete tasakaalustamist järgmises rahandusaastas. 
  
- Kui funktsioon on lubatud, tühjendatakse automaatselt kõik tasakaalustamiseks märgitud, kuid tasakaalustamata kanded. Töö kaotsimineku vältimiseks tasakaalustage kõik märgitud kanded enne funktsiooni lubamist.
- Mõned organisatsioonid käitavad aasta lõpu sulgemist mitu korda samale rahandusaastale. Ärge lubage funktsiooni, kui aasta lõpu sulgemine on juba kord käitatud ja see käivitatakse uuesti sama rahandusaasta kohta. See funktsioon peab olema lubatud enne esimese aasta lõpu sulgemise või pärast finantsaasta eelmise aasta lõpu sulgemise protsessi.

  Kui soovite funktsiooni lubada, kuid aasta lõpu sulgemist on juba korra käitatud, peate enne funktsiooni lubamist aasta lõpu sulgemise tühistama.

- Kuna tasakaalustamine põhikontode vahel pole enam lubatud, korrigeerige vastavalt vajadusele oma kontoplaani või protsesse, et tagada pearaamatu tasakaalustamine sama põhikontoga.
- Seda funktsiooni ei saa lubada, kui kasutatakse avaliku sektori aasta lõpetamise protsessi.

## <a name="set-up-ledger-settlement"></a>Seadista pearaamatu tasakaalustamine

Pärast funktsiooni lubamist ja enne järgmise aasta lõpu sulgemise käivitamist peab iga organisatsioon otsustama, kas kande üksikasjad aasta lõpus suletakse. Valik ei mõjuta algsaldo sisestamisi eelmistest aasta lõpu sulgemisprotsessidest.

Aasta **lõpu sulgemisel üksikasjade alles seadmine** on seadistatud igale pearaamatu tasakaalustuse häälestuse lehel olevale **põhikontole**.

1.  Minge pearaamatu **pearaamatu seadistuse** > **pearaamatu** > **parameetritele**.
2.  Valige vahekaardil **Pearaamatu tasakaalustused** suvand Pearaamatu **tasakaalustuskontod**.

- või -

1.  Minge pearaamatu perioodiliste **toimingute** > **pearaamatu** > **tasakaalustustele**.
2.  Saate valida **pearaamatu tasakaalustuskontod**.

Pearaamatu tasakaalustuste lehele on lisatud **kaks veergu**:
    
- **Põhikonto** tüüp – see veerg on ainult teabelise eesmärgiga. See näitab põhikontole määratud tüüpi.
- **Säilita üksikasjad aasta lõpus sulgemisel** – vaikimisi on suvandi väärtuseks **Ei**. Väärtuseks saab seada **Jah** ainult juhul, kui põhikonto **tüübi veerus on** **väärtus Bilanss**, **Vara** või **Kohustus**. Kui valiku väärtuseks on määratud **Ei**, sisestatakse algsaldod kokkuvõttena, nagu seda tüüpiline aasta lõpu sulgemisel. Kui see on seatud väärtusele **Jah**, luuakse üksikasjalikult algsaldod iga pearaamatukande kohta, mis pole põhikonto puhul tasakaalustatud.

## <a name="year-end-close"></a>Aastalõpu sulgemine

Kui käivitate aasta lõpu **sulgemise** > **·** > **pearaamatu** perioodi sulgemise aasta sulgemisega, loob protsess pearaamatu tasakaalustamiseks määratletud põhikontode algsaldod. Algsaldod luuakse kas kokkuvõttena või üksikasjadena, sõltuvalt pearaamatu tasakaalustuse seadistusest. Protsess ei hõlma tasakaalustatud pearaamatukandeid, sõltumata sellest, kas sisestate iga põhikonto algsaldo kokkuvõttena või üksikasjalikult.

Näiteks sisestatakse mitu tehingut põhikontole 130100 2021.

| Töölehe number | Vautšer  | Kuupäev       | Tüüp      | Pearaamatukonto | Konto nimi        | Kirjeldus       | Valuuta | Summa kandevaluutas | Summa  | Summa aruandlusvaluutas |
|----------------|----------|------------|-----------|----------------|---------------------|-------------------|----------|--------------------------------|---------|------------------------------|
| 20853          | FTV-3000 | 12/3/2021  | Kasutusel | 130100-001-    | Müügireskontro | Teenustasu       | USA dollar      | 100                            | 100     | 100                          |
| 20855          | FTV-3004 | 12/5/2021  | Kasutusel | 130100-002-    | Müügireskontro | Utilities         | USA dollar      | 175                            | 175     | 175                          |
| 20854          | CMV-4000 | 12/16/2021 | Kasutusel | 130100-001-    | Müügireskontro | Tagasimakse            | USA dollar      | -100                           | -100    | -100                         |
| 20851          | ARP‑8000 | 12/20/2021 | Kasutusel | 130100-002-    | Müügireskontro |                   | USA dollar      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Kasutusel | 130100-002-    | Müügireskontro |                   | EUR      | -127.11                        | -174.12 | -174.12                      |
| 20856          | CMV-4010 | 12/21/2021 | Kasutusel | 130100-002-    | Müügireskontro | Krediit kontol | USA dollar      | -175                           | -175    | -175                         |
| 20857          | FTV-3011 | 12/28/2021 | Kasutusel | 130100-001-    | Müügireskontro | Utilities         | USA dollar      | 400                            | 400     | 400                          |
| 20910          | FTV-3020 | 12/29/2021 | Kasutusel | 130100-002-    | Müügireskontro | Teenindus           | USA dollar      | 300                            | 300     | 300                          |

Nendest kannetest tasakaalustatakse pearaamatu tasakaalustamisel kolm.

On olemas arve 175 USD-le (175 USD- d). See arve tasuti maksega eurodes (EUR) ja skonto võeti.

| Töölehe number | Vautšer  | Kuupäev       | Tüüp      | Pearaamatukonto | Konto nimi        | Kirjeldus | Valuuta | Summa kandevaluutas | Summa  | Summa aruandlusvaluutas |
|----------------|----------|------------|-----------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20855          | FTV-3004 | 12/5/2021  | Kasutusel | 130100-002-    | Müügireskontro | Utilities   | USA dollar      | 175                            | 175     | 175                          |
| 20851          | ARP‑8000 | 12/20/2021 | Kasutusel | 130100-002-    | Müügireskontro |             | USA dollar      | -0.88                          | -0.88   | -0.88                        |
| 20853          | ARPM0004 | 12/20/2021 | Kasutusel | 130100-002-    | Müügireskontro |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Põhikonto funktsiooni tulemused 130100 sellest, kas funktsioon on lubatud enne aasta lõpu sulgemise käivitamist. Kui see funktsioon on lubatud, sõltub tulemus ka aasta lõpu sulgemisel üksikasjade säilita üksikasjade sättest.

### <a name="the-feature-isnt-enabled"></a>Funktsioon pole lubatud
Aasta lõpu sulgemine loob 2022. aastal põhikonto jaoks 130100 algsaldo kande. Kannete summa arvestusvaluutas on USD 525.

| Töölehe number | Vautšer  | Kuupäev     | Tüüp    | Pearaamatukonto | Konto nimi        | Kirjeldus | Valuuta | Summa kandevaluutas | Summa  | Summa aruandlusvaluutas |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|---------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro |             | USA dollar      | 299.12                         | 299.12  | 299.12                       |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro |             | USA dollar      | 400                            | 400     | 400                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro |             | EUR      | -127.11                        | -174.12 | -174.12                      |

Isegi kui makse kanne -127,11 eurot-11-ks tasakaalustati, jääb kanne algsaldoks edasi.

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--no"></a>Funktsioon on lubatud ja säilita üksikasjad aasta lõpus sulgemisel = Ei

Aasta lõpu sulgemine loob 2022. aastal põhikonto jaoks 130100 algsaldo kande. Kannete summa arvestusvaluutas on endiselt USD 525, kuid pearaamatuga tasakaalustatud kanded jäetakse algsaldost välja. Konto kogusumma on 130100-002- USD 125 asemel USD 299.12 ja 127,11 EUROT 174,12 eurot kanne on täielikult välja jäetud.

| Töölehe number | Vautšer  | Kuupäev     | Tüüp    | Pearaamatukonto | Konto nimi        | Kirjeldus | Valuuta | Summa kandevaluutas | Summa | Summa aruandlusvaluutas |
|----------------|----------|----------|---------|----------------|---------------------|-------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro |             | USA dollar      | 125                            | 125    | 125                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro |             | USA dollar      | 400                            | 400    | 400                          |

### <a name="feature-is-enabled-and-keep-detail-during-year-end-close--yes"></a>Funktsioon on lubatud ja säilita üksikasjad aasta lõpus sulgemisel = Jah

Aasta lõpu sulgemine loob 2022. aastal põhikonto jaoks 130100 algsaldo kande. Viie tasakaalustamata kande jaoks luuakse eraldi algsaldo kanne. Arvestusvaluutas kannete summa pole veel USD 525.

| Töölehe number | Vautšer  | Kuupäev     | Tüüp    | Pearaamatukonto | Konto nimi        | Kirjeldus       | Valuuta | Summa kandevaluutas | Summa | Summa aruandlusvaluutas |
|----------------|----------|----------|---------|----------------|---------------------|-------------------|----------|--------------------------------|--------|------------------------------|
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro | Teenustasu       | USA dollar      | 100                            | 100    | 100                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro | Tagasimakse            | USA dollar      | -100                           | -100   | -100                         |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro | Krediit kontol | USA dollar      | -175                           | -175   | -175                         |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-001-    | Müügireskontro | Utilities         | USA dollar      | 400                            | 400    | 400                          |
| 20910          | YEC_2021 | 1.1.2022 | Algsaldo | 130100-002-    | Müügireskontro | Teenindus           | USA dollar      | 300                            | 300    | 300                          |

Kui kande üksikasjad säilitatakse, siis algseid üksikasjalikke kandeid ei mõjutata. Need jäävad suletuks finantsaastal sisestatud ja tasakaalustamata. Nende kannete koopia luuakse algsaldo jaoks. Järgmised väärtused originaalkannetest kopeeritakse algsaldo kannetesse.

- Pearaamatukonto (põhikonto ja kõik finantsdimensioonid)
- Summad kandes, raamatupidamises ja aruandlusvaluutades
- Kirjeldus
- Sisestamiskiht
- Sisestamistüüp

   > [!NOTE]
   > Ühelegi muule algsaldo kandele pole sisestustüüpi määratud. Seetõttu saab sisestamistüüpi kasutada üksikasjades edasi suunatud eristamiseks avamiskannetest.

Mõned algsete kannete väljad peavad algsaldo üksikasjalikes kannetes muutma. Algsaldo kannete kuupäev on alati järgmise rahandusaasta esimene päev. Töölehe kood peab olema muutunud ja kande number muutub aasta lõpu sulgemise dialoogiboksis sisestatud väärtuseks.

Teavet algsete kannete kohta leiate pearaamatu tasakaalustuste **lehelt**. Iga üksikasjalik algsaldo kanne näitab **ruudustikus algse** kande kuupäeva veergu. See veerg aitab vastendada kandeid uuel rahandusaastal. Saate valida vaate **originaalkande, et** minna tagasi algse kande juurde.

## <a name="settle-transactions"></a><a name="settle-transactions"></a>Kannete tasakaalustamine
Pearaamatu kannete tasakaalustamiseks toimige järgmiselt.

1. Minge pearaamatu perioodiliste **toimingute** > **pearaamatu** > **tasakaalustustele**.
2.  Seadke lehekülje ülaosas filtrid.

    1. Kuupäevavahemiku valimine. Teise võimalusena valige kuupäevavahemiku kood, et kuupäevavahemik automaatselt täita.

       - Kuupäevavahemik ei saa finantsaastaid ületada. Kui kuupäevavahemik ületab rahandusaastad, siis kuva kannete kuvamisel kandeid ei **kuvata**.
       - Kui kuupäevavahemik on avatud rahandusaastas, saab kandeid tasakaalustada ja tasakaalustuse saab tühistada. Kui kuupäevavahemik on suletud rahandusaastas või kui aasta lõpu sulgemine on lõpetatud, siis kuvatakse kanded, kuid neid ei saa tasakaalustada ega tasakaalustamata. Kannete märke saate eemaldada ainult suletud rahandusaastal. Kui kuupäevavahemik on suletud rahandusaastas, **ei** ole nupud Märgi valitud, **·** **Tasakaalusta märgitud kanded ja Tühistatud** märgitud kanded saadaval.

    2. Valige põhikonto, mille kandeid kuvada. See väli on kohustuslik. Otsing näitab ainult põhikontosid, mis on **valitud pearaamatu tasakaalustuse** lehel ettevõtte kontoplaani jaoks.
    3. Valige sisestamiskiht. Te ei saa tasakaalustada kandeid, mis on erinevates sisestamiskihtides.
    4. Põhikonto ja dimensioonide näitamiseks eraldi veergudes valige finantsdimensioonide kogum.

3.  Valige **kuvamiskanded**, et näidata kõiki seadistatud filtritele vastavad kanded. Filtrite või dimensioonikogumite muutmisel peate uuesti valima **Kuva kanded**.
4.  Valige tasakaalustuse read. Lehekülje ülaosas oleva **valitud summa** välja väärtus suureneb või väheneb, et kajastada valitud ridade kogusummat.
5.  Kui olete kannete valimise lõpetanud, valige suvand **Märgi valituna**. Iga valitud kande puhul kuvatakse märge veerus **Märgitud**. Lisaks suureneb või väheneb **märgitud summa** välja väärtus ruudustiku kohal, et kajastada märgitud ridade kogusummat.
6.  Kui väärtus väljal Märgitud summa **on** **0** (null), valige suvand Tasakaalusta **märgitud kanded.**

    - Osaline tasakaalustus pole lubatud. Näiteks ei saa te tasakaalustada $100 tehingukandeid $90 kreeditkandega. Järelejääv $10 kreeditkanne tuleb märkida ka tasakaalustusse kaasamiseks.
    - Sisestage tasakaalustuse kuupäev. Kuupäev peab olema tasakaalustuse jaoks märgitud kannete hiimaks või pärast seda.

Märgistatud kannete olek uuendatakse olekule **Tasakaalustatud**.

> [!IMPORTANT]
> Tasakaalustatakse kõik kanded, mille olete märkinud tasakaalustamiseks aktiivse juriidilise isiku puhul ja valitud põhikonto. Kanded ei pea lehel ilmuma. Need tasakaalustatakse isegi siis, kui nad on filtri tõttu peidetud.

Mõned protsessid, nt kande tühistamine, tasakaalustavad automaatselt pearaamatukanded. Näiteks makse ja arve tasakaalustatakse Müügireskontros ja tasakaalustus loob realiseeritud kasumi/kahjumi. Makse ja arve tasakaalustus ei tasakaalusta ühtegi pearaamatu kannet, nt pearaamatu müügireskontro kanded. Kui aga makse ja arve müügireskontros tasakaalustamata on, põhjustab müügireskontro tasakaalustuse tagasipööratud raamatupidamiskirje algse ja tühistava raamatupidamiskirje pearaamatus tasakaalustamise. Kui pearaamatu **tasakaalustuse** ja aasta lõpu sulgemise vahelised teadmised on lubatud, siis ei ilmu tagasipööramise pearaamatu tasakaalustamine automaatselt, kui tagasipööramise kuupäev on teises finantsaastas.

## <a name="use-excel-for-ledger-settlement"></a>Kasuta pearaamatu tasakaalustamiseks Excelit

Pearaamatu tasakaalustuse lehel kuvatavaid **kandeid** saab eksportida Excelisse. Excelis saate kandeid veelgi filtreerida, et määrata, millised kanded tasakaalustuse jaoks märkida.
Mõlemad pearaamatu tasakaalustusüksused ekspordivad pearaamatukandeid ainult põhikonto jaoks, mis on valitud pearaamatu **tasakaalustuse** lehel. Kuigi suletud rahandusaastate kandeid saab Exceli abil siiski märkida või eemaldada, ei saa neid tasakaalustada. Lisaks ei saa tasakaalustatud kandeid sel rahandusaastal tühistada.

## <a name="make-transactions-easier-to-find"></a>Muudke kannete leidmine lihtsamaks

Pearaamatu **tasakaalustuste** leht sisaldab võimalusi, mis lihtsustavad tasakaalustuse jaoks vajaminev kannete vaatamist.

• Kasutage märgitud **filtrit**, et filtreerida kandeid selle **põhjal**, kas nende puhul on märgitud ruut märgitud.
• Kasutage olekufiltrit **kannete** filtreerimiseks nende oleku alusel.
• Valige kogusumma **järgi sortimine** kogusumma järgi, et sortida summad absoluutväärtuse alusel. Sel viisil saate grupeerida deebeteid ja kreediteid, mis on ühesuguse summaga.

## <a name="reverse-a-settlement"></a>Tasakaalustuse tühistamine

Saate tühistada ekslikult tehtud tasakaalustuse.

1.  Järgige jaotises Kannete tasakaalustamine samme 1 kuni [3](#settle-transactions), et näidata kandeid, mille suhtes olete huvitatud.
2.  Valige **Oleku** filtris valik **Tasakaalustatud**.
3.  Valige read, mida tagasipööramiseks valida.
4.  Valige Märgitud **kannete tagasipööramine**. Kõigi sama tasakaalustuse ID-ga kannete olek uuendatakse olekuks **Tasakaalusta pole.**

> [!IMPORTANT]
> Kõik sama tasakaalustuse ID-ga kanded tühistatakse, isegi kui neid pole märgitud. Näiteks märgitakse ja tasakaalustati neli rida. Kõigil neljal real on sama tasakaalustuse ID. Kui märgite neljast reast ühe ja valite siis **märgitud kannete ümberpööramise**, tühistatakse kõik neli rida.






