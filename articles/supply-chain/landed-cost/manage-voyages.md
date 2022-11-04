---
title: Teekondade haldamine
description: See artikkel kirjeldab, kuidas töötada reisidega. Teekond tähistab harilikult laeva. Kuid olenevalt teie tavadest ja protseduuridest võib see tähistada ka hankijat, ostutellimust või mõnda muud teie organisatsiooni jaoks sobivat üksust.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMTableListPage, ITMTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 4499eeb9cdd4efd9c4b630106c6e052378191f2a
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725465"
---
# <a name="manage-voyages"></a>Teekondade haldamine

[!include [banner](../../includes/banner.md)]

Teekond tähistab harilikult laeva. Kuid olenevalt teie tavadest ja protseduuridest võib see tähistada ka hankijat, ostutellimust või mõnda muud teie organisatsiooni jaoks sobivat üksust.

Lehel **Kõik teekonnad** kuvatakse teekonna üksikasjad, tarne- ja kuluarvestuse teave ning teave kaupade, ostutellimuste ja üleviimistellimuste kohta. Lehe **Kõik teekonnad** avamiseks valige **Väljalaadimiskulu \> Teekonnad \> Kõik teekonnad**. Sellel lehel kuvatakse kõikide praeguste teekondade loend. Toimingupaani nuppude abil saate teekondi luua, kustutada ja nendega töötada. Valige leondist teekond, et vaadata selle üksikasju.

> [!NOTE]
> Teekonnaga on seotud saatmiskonteinerid ja fooliod. Saatmiskonteineriga on seotud osturead. Lisaks jaotatakse siin sisestatud kulud kõigile manustatud osturidadele.
> Projekti ostutellimust ei toetata väljaminev kulus.

## <a name="action-pane"></a>Toimingupaan

Lehe **Teekonnad** toimingupaanil on nupud, mille abil saate valitud teekonnaga töötada. Iga nupp teeb ühe toimingu. Toimingupaanil on ka vahekaardid, millest omakorda igaühel on seotud nuppude komplekt. Välja arvatud juhtudel, kui on märgitud teisiti, on kõik nupud ja vahekaardid saadaval nii lehe **Kõik teekonnad** loendivaates kui ka ühe valitud teekonna üksikasjade vaates.

### <a name="buttons-that-appear-directly-on-the-action-pane"></a>Otse toimingupaanil kuvatud nupud

Järgmises tabelis kirjeldatakse otse toimingupaanil saadaolevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| New | Teekonna loomine. <!-- KFM: Link to scenario --> |
| Kustutamine | Praeguse teekonna kustutamine. Kustutada saab ainult neid teekondi, mille teekonnaolek on *Kinnitatud*. Kui teekond väljub sadamast ja töötleb transiidis olevaid kaupu, ei saa seda enam kustutada. |
| Reisi redaktor | Avage leht **Teekonna redaktor**, kus saate teekonnale osturidu lisada või neid eemaldada, luua uusi konteinereid ja muuta teekonna enda üksikasju. |
| Reisikulud | Avage leht **Teekonna kulud**, kus saate kõigi teekonna kaupade teekonnakulusid vaadata ja lisada. Kui teekonnakulud lisatakse teekonnale käsitsi, lisatakse need automaatselt lehele **Kulude päring** ja jaotatakse kõigile kaupadele vastavalt lehel **Teekonnakulud** määratletud meetodile. |

### <a name="buttons-on-the-voyage-tab"></a>Nupud vahekaardil Teekond

Järgmises tabelis kirjeldatakse toimingupaani vahekaardil **Teekond** olevaid nuppe. See vahekaart on saadaval ainult siis, kui töötate lehe **Kõik teekonnad** loendivaates.

| Nupp | Kirjeldus |
|---|---|
| Saatmiskonteiner | Avage leht, millel kuvatakse kõik valitud teekonnaga seostatud saatmiskonteinerid. Konteinereid võib olla üks või mitu. |
| Foolio | Avage leht, millel kuvatakse kõik valitud teekonnaga seostatud fooliod. Foolioid võib olla üks või mitu. |

### <a name="buttons-on-the-manage-tab"></a>Nupud vahekaardil Halda

Järgmises tabelis kirjeldatakse toimingupaani vahekaardil **Haldamine** olevaid toiminguid.

| Nupp | Kirjeldus |
|---|---|
| Dokumendid on vastu võetud | Teekonna värskendamine nii, et suvandi **Dokumendid on vastu võetud** väärtuseks oleks *Jah*. Selle nupu abil saate lukustada kauba ja/või osturea nii, et seda ei saa rohkem värskendada. |
| Transiidis | Seadke väljale **Teekonna olek** transiidis oleku olek, mis on määratud lehel **[Väljalaadimiskulu parameetrid](landed-cost-parameters.md)**. Sellel protsessil puudub täiendav loogika. Teekonna saab transiidis oleku olekusse värskendada ka automaatselt, jaotise [Jälgimise juhtimiskeskus](delivery-information-setup.md) sätete alusel.
| Kuluarvutuse jaoks valmis | Seadke väljale **Teekonna olek** kuluarvestuseks valmisoleku olek, mis on määratud lehel **[Väljalaadimiskulu parameetrid](landed-cost-parameters.md)**. Teekonna kuluarvutuse saab teha siis, kui kõik arved on töödeldud (nii laovaru arved kui teekonnakulu arved) ja kaubad on vastu võetud. Kui teekonnaga seotud eeldatavad kulud pole arvutatud, ilmneb tõrge, kui püüate teekonna kuluarvutust töödelda. |
| Arvutatud kulu | Kõigi kuluarvutuse ebakorrapärasuste puhastamine pärast seda, kui kõigi ostutellimuste ja teekonnakulude kohta on arve olemas. Selle nupu valimisel kuvatakse dialoogiaken **Teekonna värskendamine - arvutatud kulu**. Seal saate valida, kas sisestada standardsel finantskuupäeval või määrata sisestuskuupäev, ja seejärel käivitada tegevuse. Saate tegevuse uuesti käivitada nii palju kordi kui soovite. Dialoogiaknas **Teekonna värskendamine - arvutatud kulu** saate ka määrata graafiku tegevuse käivitamiseks perioodilise ülesandena (pakett-töö). Soovitame tegevust regulaarselt käitada, seadistades selle pakett-tööna. |
| Kviitungite loendi sisestamine | Sisestage sissetulekute loend teekonna kõigi ostutellimuse ridade jaoks.  |
| Sisesta toote sissetulek | Sisestage toote sissetulek teekonna kõigi ostutellimuse ridade jaoks. Teekonnaga seostatud ostutellimuse ridade toote sissetuleku protsessi kasutatakse ainult siis, kui kaubad **ei** läbi transiidis olevate kaupade töötlust. Kui kaubad läbivad transiidis olevate kaupade töötluse, kuvatakse tõrketeade, kui püüate ostutellimuse rea jaoks sisestada toote sissetulekut.  |
| Sisesta arve | Sisestage arve teekonna kõigi ostutellimuse ridade jaoks. Kui teekonna kaubad läbivad transiidis olevate kaupade töötluse, arveldatakse ostutellimuse read enne vastuvõtuprotsessi läbimist. Kui algne ostutellimus on arveldatud, luuakse algsete ostutellimuse ridadega seostatud transiidis olevate kaupade tellimused. Seejärel saab ladu tellimused vastu võtta.  |
| Lähetuse üleviimistellimus | Sisestage üleviimistellimuse teekond teekonna kõigi üleviimistellimuse ridade jaoks. Selle nupu valimisel on värskendamiseks saadaval ainult üleviimistellimused. |
| Võta üleviimistellimus vastu | Sisestage üleviimistellimuse sissetulek teekonna kõigi üleviimistellimuse ridade jaoks. |
| Võta transiidis olevad kaubad vastu | Võtke vastu kõik teekonna transiidis olevad tellimuseread. See nupp on üks kolmest valikust, mis on saadaval teekonna transiidis olevate kaupade vastu võtmiseks. (Ülejäänud kaks valikut on nupp **Loo saabumistööleht**, mida kirjeldatakse selles tabelis hiljem, ja mobiilirakendus Warehouse Management.) See suvand on lihtsaim suvand ja töötleb transiidis olevad kaubad transiidis olevate kaupade laost välja ja lõppsihtlattu sisse. Kui soovite protsessi täpsemini juhtida, kasutage kaupade sissetuleku töötlemiseks saabumise töölehte või mobiilset seadet. |
| Otsi automaatseid kulusid | Asjakohaste teekonnakulude otsimine. Kui need kulud on juba leitud või värskendatud, saate järgmise teate: „Leidub arveldamata kuluridasid. Kas soovite need üle kirjutada?“ Otsitakse kõiki kulusid, mida loomise hetkel teekonnaga ei seostatud. Teekonnakulusid, mis on teekonnale manustatud ja mis on arveldatud, ei kirjutata üle. |
| Loo saabumise tööleht | <p>Avage dialoogiaken **Saabumistöölehe loomine**, kus saate luua saabumise töölehe, mis määratleb asukoha. Dialoogiaknas on järgmised suvandid.</p><ul><li>**Loo transiidis olevatest kaupadest** või **Loo üleviimistellimusest** – selle suvandi silt muutub sõltuvalt sellest, kas kasutate transiidis olevate kaupade protsessi. Määrake selle väärtuseks *Jah*, et avada saabumise töölehe leht, mis võimaldab töödelda teekonnaga seotud transiidis olevate kaupade standardset saabumise töölehte. Kui kaup on juba lõppsihtlaos vastu võetud, siis seda ei lisata saabumise töölehe ridadele.</li><li>**Lähtesta kogus** – määrake selle suvandi väärtuseks *Jah*, et lähtestada vastu võetav kogus, põhinedes teekonna real määratletud kaupade kogusel. Kui teekonna rida on osaliselt vastu võetud, on see kogus järelejäänud kogus. Soovitame määrata selle suvandi väärtuseks *Jah*.</li><li>**Loo tellimuse ridadelt** – määrake selle suvandi väärtuseks *Jah*, et võtta väärtus tellimuse ridadelt.</li></ul><p>See nupp on üks kolmest valikust, mis on saadaval teekonna kaupade vastu võtmiseks. (Muud valikud on selles tabelis varem kirjeldatud nupp **Võta transiidis olevad kaubad vastu** ja mobiilirakendus Warehouse Management.)</p> |
| Kulude laekumine | Saate koguda kulusid seal, kus kulutüübil on deebeti jaoks määratud pearaamatukonto. Seda nuppu kasutatakse tavaliselt siis, kui varud on transiidis või kui kaubad on kätte saadud ja arveldatud. |
| Koonda kulud | Kulude teisaldamine saatmiskonteineri tasemelt teekonna tasemele. Võite seda nuppu kasutada jagatud teenuste/saatmise stsenaariumis, kus mitu olemit jagavad saatmiskonteineri või paki mahtu. Näiteks on teekonnal 40-jalane saatmiskonteiner ja 20-jalane saatmiskonteiner ning jaotamine tehakse mahu järgi. Sel juhul võidakse 20-jalast konteinerit jagavaid või selle mahtu kasutavaid kaupu/üksuseid penaltiseerida. Kulude õiglaseks jaotamiseks võivad mõned organisatsioonid soovida kanda kulud üle teekonnale ja jaotada need teekonnataseme jaotamismeetodi alusel. |
| Muuda teekonna malli | Avatakse dialoogiaken, kus saate muuta teekonna malli. Pärast malli muutmist teekonnakulud kustutatakse. Seetõttu peate võib-olla valima **Otsi automaatsed kulud** (vt kirjeldust selles tabelis eespool) või lisama kulud uuesti käsitsi. |

### <a name="buttons-on-the-general-tab"></a>Nupud vahekaardil Üldine

Järgmises tabelis kirjeldatakse toimingupaani vahekaardil **Üldine** olevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| Saabunud kaupade loend | Avatakse toote sissetulekute loend teekonna kõigi ostutellimuse ridade jaoks.  Kui ühtegi toote sissetuleku loendit pole töödeldud, ei ole see nupp saadaval. |
| Toote sissetulek | Avatakse toote sissetuleku kirje nende ostutellimuse ridade jaoks, mis on teekonnaga seotud, kui seda kirjet kasutatakse. Kui ühtegi toote sissetulekut pole sisestatud, ei ole see nupp saadaval. Kui kasutate transiidis olevate kaupade töötlemist, ei kasutata toote sissetuleku protsessi. |
| Kauba saabumine | Avatakse kauba saabumise tööleht, kui seda kasutatakse. |
| Jälitamine | Avatakse leht **Sissetulevate jälgimine**, kus saate värskendada saatmiskonteineris ja teekonnal olevate kaupade eeldatavat tarnekuupäeva ning värskendada ostutellimuse ridade eeldatavaid tarnekuupäevi. |
| Kulude päring | <p>Avatakse leht **Kulude päring**, kus kuvatakse teekonna kõik kulud.</p><p>Valige toimingupaanil **Kuva**, et reguleerida kuva. Saate vaadata kõiki tasemeid ning kauba ja kulutüübi koodi.</p><p>Lehel **Kulude päring** kuvatakse ainult otseselt varude kannetega seotud kulutüübi koodid. Kulutüübi koodide eemaldamisega saate lehte reguleerida, grupeerides kulud kokku. See võimalus võib olla kasulik, kui kasutate suurusi ja värve.</p><p>Lehel **Kulude päring** kuvatakse ainult kulutüübi koodid, millel on välja **Deebet** äärtuseks määratud *Kaup*.</p> |
| Transiidis olevad kaubad: tellimused | Avatakse leht **Transiidis olevate kaupade tellimused**, kus kuvatakse ainult valitud teekonna transiidis olevate kaupade kirjed. |

## <a name="lines-view"></a>Ridade vaade

Vaate **Read** avamiseks avage teekond ja seejärel valige teekonna päises ülal paremal vahekaart **Read**.

### <a name="information-on-the-voyage-header-fasttab"></a>Teave teekonna päise kiirkaardil

Teekonna vaate **Read** kiirkaart **Teekonna päis** sisaldab teekonda kirjeldavat põhiteavet. Paljud kiirkaardil kuvatavad väljad ilmuvad samuti **päisevaates**, nagu kirjeldatud selles artiklis.

### <a name="information-on-the-voyage-lines-fasttab"></a>Teave teekonna ridade kiirkaardil

Teekonna vaate **Read** kiirkaart **Teekonna read** on seotud teekonna üksikasjadega ja kuluarvutuse teabega, mis kehtivad teekonna tasemel. Siin saate üle vaadata teekonnaga seostatud saatmiskonteinereid, foolioid ja kaupu. Kuvatakse ka teekonnal olevate kaupade hind ja kogus. Saate vaadata kõiki loetletud saatmiskonteinereid või foolioid, valides vastava lingi.

### <a name="information-on-the-line-details-fasttab"></a>Teave rea üksikasjade kiirkaardil

Teekonna vaate **Read** kiirkaart **Rea üksikasjad** annab lisateavet kiirkaardil **Teekonna read** praegu valitud rea kohta. Arvestage, et see kiirkaart sisaldab üksikasju positsiooni kohta, mis igal real konteineris on, ja selle deklareeritud koguse kohta.

## <a name="header-view"></a>Päisevaade

Vaate **Päis** avamiseks avage teekond ja seejärel valige teekonna päises ülal paremal vahekaart **Päis**.

### <a name="settings-on-the-general-fasttab"></a>Kiirkaardi Üldine sätted

Järgmises tabelis kirjeldatakse teekonna vaate **Päis** kiirkaardil **Üldine** saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Reis | Sisestage teekonna või lennu number. |
| Reserveerimise viide | Kui teie saatja või saatmiskeskus annab viitenumbri teekonna tuvastamiseks (st saatja või saatmiskeskuse siseviite), sisestage see siia. |
| Laev | Sisestage või valige laev. Kui laev väärtusena loetelus puudub, saate sisestada laeva ID vaba tekstina. Sel juhul põhitabelit ei värskendata, nii et laeva ID saab sellel väljal hiljem valida. |
| Välise reisi ID | Saate sisestada avalikult kättesaadava teekonna ID (nt lennu numbri). |
| Koondlennuveokiri/veokiri | Saate sisestada põhivedaja lennu saatelehe või veokirja numbri. Selle väärtuse saate määrata lennukiga saatmisel. |
| Maja lennu veokiri / veokiri | Saate sisestada saatmiskonteineri edasisaatja lennu saatelehe või veokirja numbri. |
| Rent | Märkige see ruut, kui konteiner on rendikonteiner, mis tuleb tagastada. |
| Kirjeldus | Saate sisestada teekonna kirjeldus, et seda oleks lihtsam ära tunda. |
| Reisi olek | Teekonna olek. Väärtused on *Loodud*, *Transiidis*, *Dokumendid on vastu võetud* ja *Arvutatud kulu*. Selle välja arvutus ei põhine loogikal. Seda värskendatakse ainult sisestamistegevuse kaudu. Väärtus *Arvutatud kulu* näitab, et laovaru ja kõigi teekonnakulude arve on vastu võetud. Kui arve ei ole vastu võetud, ei saa teekonna olek olla *Arvutatud kulu*. |
| Ostutellimuse olek | Kõrgeim olek, mis on saavutatud kõikide teekonnaga seotud ostutellimuste lõikes. |
| Dokumendid on vastu võetud | Väärtus, mis näitab, kas teie ettevõte on vastu võtnud kõik teekonnaga seotud dokumendid. Väärtuse muutmiseks valige toimingupaanil vahekaardil **Haldamine** grupis **Teekonna värskendamine** suvand **Dokumendid on vastu võetud**. |
| Saatmisettevõte | Valige selle teekonna jaoks saatmisettevõte. Selle välja abil saab määratleda automaatsed kulud. |
| Nimi | Väljal **Saatmisettevõte** valitud ettevõtte nimi. |
| Mõõtmine | See väli võimaldab määratleda automaatse kulu mõõtmise. Mõõtmisi kasutavad tihti organisatsioonid, kes ei tea kaupade individuaalset mahtu või kaalu, kuid vajavad täpsemat jaotust kui võimaldavad summa ja koguse suvandid. Ekspediitor esitab kaalu või kuupmõõdu ja teie saate selle seada kas kauba või ostutellimuse tasemele. Seda saab parameetri valimisel automaatselt värskendada või käsitsi sisestada. |
| Mõõtühik | Mõõtühik, mida rakendatakse väljal **Mõõtmine** olevale numbrile. |
| Kaubaaluste arv | Saate määratleda teekonnarea kaubaaluste arvu. Seda välja värskendatakse automaatselt, kui lehe **Väljalaadimiskulu parameetrid** vahekaardil **Üldine** on suvandi **Kastide arvu automaatne värskendamine** väärtuseks määratud *Jah*. |

### <a name="settings-on-the-delivery-fasttab"></a>Kiirkaardi Tarne sätted

Järgmises tabelis kirjeldatakse teekonna vaate **Päis** kiirkaardil **Tarne** saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Loodud kuupäev ja kellaaeg | Teekonna loomise kuupäev ja kellaaeg. |
| Tehasest otse hankimise kuupäev | See väli valib teekonnaga seotud ostutellimuste hulgast varaseima tehasest väljumise kuupäeva. Tehasest väljumise kuupäev on saadaval ostutellimuse päises ja seda värskendatakse jälgimiskontrolli funktsiooni abil. |
| Lähetuskuupäev | Lennuki või laeva päritolukohast lahkumise eeldatav kuupäev. |
| Väljumiskuupäev | Väljumiskuupäev on tavaliselt kuupäev, mil lennuk või laev tegelikult ülemeresadamast lahkub. Lähetuskuupäev ja väljumiskuupäev ei pea kattuma. Välja **Väljumiskuupäev** eesmärk on üksnes teavitav. Seda ei kasutata eeldatava tarnekuupäeva prognoosimiseks. Jälgimiskontrolli funktsiooni kasutatakse eeldatava tarnekuupäeva prognoosimiseks ja selle välja saab seadistada nii, et jälgimiskontrolli funktsioon täidab selle automaatselt. |
| Kauplusse liikumise kuupäev | See väli valib varaseima kuupäeva, mil kaubad teekonnaga seotud ostutellimustest on müügiks saadaval. |
| Eeldatav tarnekuupäev | Eeldatav tarnekuupäev on tavaliselt kaupade lattu saabumise kuupäev. Sellel väljal on ainult informatiivne eesmärk. Seda ei kasutata kaupade koondplaneerimiseks. Ostutellimuse rea eeldatavat tarnekuupäeva kasutatakse teekonna kaupade koondplaneerimiseks ja seda värskendatakse jälgimiskontrolli funktsiooni abil. Selle välja saab seadistada nii, et selle täidab jälgimiskontrolli funktsioon. |
| Tegelik tarnekuupäev | Varaseim tarnekuupäev teekonnaga ühendatud kaupade alusel. |
| Arvatav saabumisaeg sadamas | Saate sisestada teekonna lähtesadamasse saabumise prognoositava kuupäeva saatmisagendi esitatud teabe alusel. |
| Algdokumendid on vastu võetud | Saate sisestada algdokumentide vastuvõtmise kuupäeva. |
| Maakleri soovitus | Saate sisestada maakleri teavitamise kuupäeva. |
| Saadetud algne veokiri | Siaate ssestada algse veokirja saatmise kuupäeva. |
| Kaubad on vabastatud | Saate sisestada kaupade tollist väljastamise kuupäeva. |
| Kliendiga kohtumine | Saate sisestada kliendiga kohtumise kuupäeva, mis on prognoositav kuupäev, mil klient saab kaupade omanikuks. |
| Lattu tarnitud | Saate sisestada kuupäeva, mil kaubad lattu tarniti. |
| Kinnitamise kuupäev | Saate sisestada kinnitamise kuupäeva. |
| Tarnejuhised | Saate sisestada tarnejuhiste vastuvõtmise kuupäeva. |
| Tarneviis | See väli annab teavet teekonna tarnimiseks kasutatud meetodi kohta ja selle tarnemeetodiga seotud automaatsete kulude kuluvaliku kohta. |
| Lähtesadam | Lähtesadam, millest teekond väljub. |
| Sihtsadam | Saatmissadam, kuhu teekond saabub. Saatmiskonteineritel võivad olla erinevad sadamad, sest laev võib peatuda mitmes sadamas. Kinnitades sihtsadama saatmiskonteineri tasemel, esitate täpsed sadama üksikasjad teekonna iga saatmiskonteineri kohta. Veosega seostatud automaatne kulu määratletakse saatmiskonteineri tüübi, sihtsadama ja lähtesadama kombinatsiooni alusel. |
| Kohalik ekspediitor | Sellel väljal on ainult informatiivne eesmärk. Kohalik ekspediitor peaks olema valitav hankija tabelist. |
| Kohaliku transpordi kuupäev | Kuupäev, milleks kohalik transport on broneeritud. See väli aitab ladu planeerimisel. |
| Kohaliku transpordi kellaaeg | Ajavahemik, milleks kohalik transport on broneeritud. See väli aitab ladu planeerimisel. |
| Teekonna mall | Teekonna jaoks määratletud teekonna marsruudi mall. Teekonna marsruudi malli kasutatakse saatmiskonteineri ja teekonna sihtsadama ja lähtesadama sisestamiseks. Need väärtused aitavad omakorda tuvastada teekonnaga seotud automaatseid kulusid. |

### <a name="settings-on-the-other-fasttab"></a>Kiirkaardi Muud sätted

Järgmises tabelis kirjeldatakse teekonna vaate **Päis** kiirkaardil **Muud** saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Märkused | Saate sisestada teekonnaga seotud lisateavet. |
| Hindamise kuupäev | Saate valida teekonnaga seotud ostutellimuste jaoks varaseima tehasest väljumise kuupäeva. |
| Ootel reis | Selle abil saate määrata, kas saadetis või teekond on juba väljunud. Sellel on ainult teavitav eesmärk.  |
| Saatmiskonteinerite ümbernimetamine | Rohkem kui ühe konteineriga teekondade korral veel vastu võtmata konteinerite arv. |

## <a name="voyage-update-periodic-tasks"></a>Teekonna värskendamise perioodilised ülesanded

Moodul **Väljalaadimiskulu** hõlmab mitut teekonnaga seotud perioodilist ülesannet, mis võivad hulgivärskendada teekonna mitmeid aspekte. Nende perioodiliste ülesannete käitamiseks või plaanimiseks avage **Väljalaadimiskulu \> Perioodilised ülesanded \> Teekonna värskendused** ja seejärel valige üks järgmistest ülesandetüüpidest.

- **Dokumendid on vastu võetud** – selle ülesandega saate määrata suvandi **Dokumendid on vastu võetud** väärtuseks *Jah* korraga mitmele teekonnale. Värskendatavate teekondade määratlemiseks kasutage sätteid **Filter**.
- **Transiidis olevad** – see ülesanne võimaldab korraga mitme teekonna jaoks määrata välja **Teekonna olek** transiidis olevasse olekusse, mis on kehtestatud lehel **[Väljalaadimiskulu parameetrid](landed-cost-parameters.md)**. Värskendatavate teekondade määratlemiseks kasutage sätteid **Filter**.
- **Kuluarvestuseks valmis** – see ülesanne võimaldab korraga mitme teekonna jaoks määrata välja **Teekonna olek** kuluarvestuseks valmis olekusse, mis on kehtestatud lehel **[Väljalaadimiskulu parameetrid](landed-cost-parameters.md)**. Tavaliselt seadistatakse see ülesanne käivituma regulaarse graafikuga.
- **Arvestatud kulu** – see ülesanne võimaldab korraga mitme teekonna jaoks määrata välja **Teekonna olek** arvestatud kulu olekusse, mis on kehtestatud lehel **[Väljalaadimiskulu parameetrid](landed-cost-parameters.md)** eeldusel, et kulu on arvutatud, kuid pole veel teekonnal värskendatud. Tavaliselt seadistatakse see ülesanne käivituma regulaarse graafikuga.
