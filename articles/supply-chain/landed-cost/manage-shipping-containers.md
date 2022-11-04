---
title: Saatmiskonteinerite haldamine
description: See artikkel kirjeldab, kuidas töötada konteinerite saatmisega. Saatmiskonteinereid kasutatakse füüsiliselt kokkurühmitatud kaupade rühmitamiseks. Neid kasutatakse ka juhul, kui kulud tuleb jagada ainult nende kaupade vahel, tavaliselt seetõttu, et need on füüsiliselt koos.
author: Weijiesa
ms.date: 12/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: b409017407ce1c027184bdc2292197840c61e04a
ms.sourcegitcommit: eb9a53d5cf10f1ada68757536d6a94b2cb00929d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/27/2022
ms.locfileid: "9725437"
---
# <a name="manage-shipping-containers"></a>Saatmiskonteinerite haldamine

[!include [banner](../../includes/banner.md)]

Saatmiskonteinereid kasutatakse füüsiliselt kokkurühmitatud kaupade rühmitamiseks. Neid kasutatakse ka juhul, kui kulud tuleb jagada ainult nende kaupade vahel, tavaliselt seetõttu, et need on füüsiliselt koos.

Kaupade vaatamiseks ja töötlemiseks saatmiskonteineri lehel avage **Väljalaadimiskulu \> Saatmiskonteinerid \> Kõik saatmiskonteinerid**. Lehel **Kõik saatmiskonteinerid** on kuvatud kõigi saadaolevate saatmiskonteinerite loend. Toimingupaani nuppude abil saate saatmiskonteinereid luua, kustutada ja nendega töötada. Valige loendist mõni saatmiskonteiner, et vaadata selle üksikasju lehel **Saatmiskonteinerid**.

Saatmiskonteineri üksikasjade lehe ülaosas on kuvatud saatmiskonteineri ja kuluarvutuse teave. Jaotises **Read** on kuvatud konteineriga seostatud fooliod, kaubad ja ostutellimused või üleviimistellimused.

## <a name="action-pane"></a>Toimingupaan

Lehe **Kõik saatmiskonteinerid** ja **Saatmiskonteinerid** toimingupaanil on nupud, mille abil saate valitud saatmiskonteineriga töötada. Iga nupp teeb ühe toimingu. Toimingupaanil on ka vahekaardid, millest omakorda igaühel on seotud nuppude komplekt. Välja arvatud juhul, kui on märgitud teisiti, on kõik järgmistes alamjaotistes kirjeldatud nupud ja vahekaardid saadaval nii loendivaates (st lehel **Kõik saatmiskonteinerid**) kui ka üksikasjalikus vaates (st lehel **Saatmiskonteinerid**).

### <a name="buttons-on-the-manage-tab"></a>Nupud vahekaardil Halda

Järgmises tabelis kirjeldatakse toimingupaani vahekaardil **Halda** olevaid nuppe.

| Nupp | Kirjeldused |
|---|---|
| Kviitungite loendi sisestamine | Sisestage sissetulekute loend või vaadake toote sissetulekute loendeid kõigi saatmiskonteineri ostutellimuse ridade kohta.  |
| Sisesta toote sissetulek | Sisestage toote sissetulek saatmiskonteineri kõigi ostutellimuse ridade jaoks. |
| Sisesta arve | Sisestage arve saatmiskonteineri kõigi ostutellimuse ridade jaoks.  |
| Lähetuse üleviimistellimus | Sisestage üleviimistellimuse saadetis saatmiskonteineri kõigi üleviimistellimuse ridade jaoks. Dialoogiboksis kuvatakse ainult need saatmiskonteineri read, mis on üleviimistellimuse tüüpi. |
| Võta üleviimistellimus vastu | Sisestage üleviimistellimuse sissetulek saatmiskonteineri kõigi üleviimistellimuse ridade jaoks. Vastuvõtmise dialoogiboks on kõige lihtsam viis kajastada saatmiskonteineri või teekonna sissetulnud kaupu ja on üks kolmest saadaolevast suvandist. Saate vastu võtta ka saabumisttöölehtede või mobiilses seadmes töötlemise kaudu. |
| Loo saabumise tööleht | Saate täpsemaid laofunktsioone kasutades luua organisatsioonidele saabumiste töölehe. Suvandid on _Lähtesta kogus_ (soovitatav) ja kas _Loo transiidis olevatest kaupadest_ või _Loo ostutellimustest_. Viimased kaks suvandit sõltuvad sellest, kas kasutatakse transiidis olevate kaupade töötlemist. |
| Nimeta ümber | Avage dialoogiboks, kus saate valitud saatmiskonteineri ümber nimetada. |
| Muuda teekonna malli | Vahetage teekonnamalli. Kuna pärast teekonnamalli vahetamist kustutatakse saadetise kulud, tuleb võib-olla teha valik **Otsi automaatsed kulud** või sisestada kulud käsitsi uuesti. |
| Teisenda renditavaks | Teisendage valitud saatmiskonteiner üüritud saatmiskonteineriks. |

### <a name="buttons-on-the-general-tab"></a>Nupud vahekaardil Üldine

Järgmises tabelis kirjeldatakse toimingupaani vahekaardil **Üldine** olevaid nuppe.

| Nupp | Kirjeldused |
|---|---|
| Saabunud kaupade loend | Sisestage sissetulekute loend saatmiskonteineri kõigi ostutellimuse ridade jaoks.  |
| Toote sissetulek | Vaadake toote sissetulekukirjet, kui seda kasutatakse. Toote sissetulekute töötlust kasutatakse ainult siis, kui kaubad ei kasuta transiidis oleva kauba funktsioone. |
| Kauba saabumine | Vaadake saatmiskonteineri kauba saabumistöölehte, kui seda töölehte kasutatakse. |
| Etapid | Etappide abil tuvastatakse teekonna marsruudi eri osasid. Täitmisajad saab saadetise jälgimise hõlbustamiseks seostada iga etapiga. Lisateavet vt teemast [Mitmeetapilise teekonna seadistamine](multi-leg-journey-setup.md). |
| Jälitamine | Vaadake või värskendage saadetise jälgimist. |
| Transiidis olevad kaubad: tellimused | Lehe **Transiidis olevad kaubad** saate avada otse konteinerist. Sellel lehel on kuvatud ainult valitud saatmiskonteineri transiidis olevate kaupade kirjed. |

## <a name="header-view"></a>Päisevaade

Vaate **Päis** avamiseks avage saatmiskonteiner ja seejärel valige saatmiskonteineri päises ülal paremal vahekaart **Päis**.

### <a name="settings-on-the-general-fasttab"></a>Kiirkaardi Üldine sätted

Järgmises tabelis kirjeldatakse saatmiskonteineri vaate **Päis** kiirkaardil **Üldine** saadaolevaid sätteid.

| Field | Kirjeldus |
|---|---|
| Saatmiskonteiner | Saatmiskonteineri nimi. |
| Reis | Saatmiskonteineriga seostatud teekond. |
| Saatmiskonteineri tüüp | Sisestage saatmiskonteineri tüüp. See väli peab olema seatud. Selle abil saate määrata näiteks veose kulu, valides saatmiskonteineri tüübiga seostatud automaatse kulu. |
| Laev | Sisestage või valige laev. Kui laev väärtusena loetelus puudub, saate sisestada laeva ID vaba tekstina. Sel juhul põhitabelit ei värskendata, nii et laeva ID saab sellel väljal hiljem valida. Lisateavet vt teemast [Laevad](shipping-information-setup.md#vessels). |
| Ühiku tüüp | Ühikutüüpe kasutatakse saatmiskonteinerite rühmitamise ja tuvastamise lisavõimalusena. Need kuvatakse ja valitakse saatmiskonteineri lehel. Lisateavet vt teemast [Ühikutüüpide seadistamine](shipping-container-setup.md#unit-types). |
| Külmutuse tüüp | Külmutuse tüüpe kasutatakse saatmiskonteinerite rühmitamise ja tuvastamise lisavõimalusena, tavaliselt külmkonteinerite korral. Need kuvatakse ja valitakse saatmiskonteineri lehel. Lisateavet vt teemast [Külmutuse tüüpide seadistamine](shipping-container-setup.md#refrigeration-types). |
| Mõõtmine | See väli võimaldab mõõdu määrata moodulis **Väljalaadimiskulu**. Mõõtmisi kasutavad tihti organisatsioonid, kes ei tea kaupade individuaalset mahtu või kaalu, kuid vajavad täpsemat jaotust, kui võimaldavad summa või koguse suvandid. Ekspediitor esitab kaalu kilogrammides või kuupmõõdu ja teie saate selle seada kas kauba või ostutellimuse tasemele. Seda saab parameetri valimisel automaatselt värskendada või käsitsi sisestada. |
| Mõõtühik | Mõõtühik, mida rakendatakse väljal **Mõõtmine** olevale numbrile. |
| Tegelik kaal | Saate jäädvustada paki või konteineri tegeliku kaalu. Seda väärtust saab kasutada võrdluskontrolliks saatmiskonteineri seadistuses lubatud maksimumkaalu suhtes. |
| Pakkide arv | Selle parameetri valimise korral värskendatakse automaatselt pakkide arv. |
| Kauba kirjeldus | Kaupade kirjelduse saab valida saatmiskonteineri või foolio päises. Seda kasutatakse kaupade teekonna, saatmiskonteineri või foolio tuvastamiseks. Lisateabe saamiseks lugege teemat [Kaupade kirjeldus](shipping-information-setup.md#description-of-goods). |
| Maja lennu veokiri / veokiri | Saate määrata saatmiskonteineri edasisaatja lennu saatelehe või veokirja. |
| Märkused | Saatmiskonteineriga seotud lisateave. |
| Tagastatav | Väärtus, mis näitab, kas saatmiskonteineri saab pärast teekonda tagastada. |
| Reisi olek | Saatmiskonteineriga seostatud teekonna olek. |
| Ostutellimuse olek | Saatmiskonteineriga seostatud ostutellimuse olek. |

### <a name="settings-on-the-delivery-fasttab"></a>Kiirkaardi Tarne sätted

Järgmises tabelis kirjeldatakse saatmiskonteineri vaate **Päis** kiirkaardil **Tarne** saadaolevaid sätteid.

| Field | Kirjeldus |
|---|---|
| Loodud kuupäev ja kellaaeg | Konteineri loomise kuupäev ja kellaaeg. |
| Tehasest otse hankimise kuupäev | See kuupäev esitatakse tavaliselt tehasele/hankijale näitamaks, millal te eeldate, et kaubad lahkuvad selle valdusest. Kui töötate Aasias asuva tehasega, on see kuupäev sageli nõutav selle kuupäeva asemel, milleks soovite kauba kätte saada. (Vastupidiselt sellele on kohaliku tarne korral nõutav kuupäev, milleks soovite kauba kätte saada.) Selle välja saab täita ainult saatmiskonteinerite loendi ostutellimuse ridadel. Samuti saate selle siin käsitsi sisestada. |
| Lähetuskuupäev | Selle kuupäeva saab printida ostutellimuse dokumendile. Tavaliselt teavitab see tehast/hankijat kuupäevast, milleks tuleb kaubad sadamasse tarnida. Sellel väljal on ainult informatiivne eesmärk. Seda ei kasutata saatmiskonteineris kaupade eeldatava tarnekuupäeva prognoosimiseks. Selle välja saab seada nii, et see värskendatakse automaatselt jälgimiskontrolli lehe värskendamise korral. |
| Kauplusse liikumise kuupäev | Varaseim kuupäev, mil kaubad teekonnaga seotud ostutellimustest on müügiks saadaval.|
| Eeldatav tarnekuupäev | Tavaliselt kuupäev, mil kaubad peaksid lattu saabuma. Sellel väljal on ainult informatiivne eesmärk. Seda ei kasutata saatmiskonteineri ostutellimuse ridade koondplaneerimise arvutamiseks. Ostutellimuse ridade eeldatav tarnekuupäev värskendatakse jälgimiskontrolli kaudu. Selle välja saab seadistada nii, et see värskendatakse automaatselt jälgimiskontrolli lehe värskendamise korral. |
| Väljumiskuupäev | Tavaliselt kuupäev, mil lennuk või laev tegelikult ülemeresadamast lahkub. |
| Arvatav saabumisaeg sadamas | Sihtkohta („sihtkoha“ sadamasse) prognoositud saabumiskuupäev. |
| Algdokumendid on vastu võetud | Valikuline: värskendage algdokumentide vastuvõtmise kuupäeva. |
| Maakleri soovitus | Valikuline: värskendage maakleri teavitamise kuupäeva. |
| Saadetud algne veokiri | Valikuline: värskendage algse veokirja saatmise kuupäeva. |
| Kaubad on vabastatud | Valikuline: värskendage kaupade väljastamise kuupäeva. |
| Kliendiga kohtumine | Valikuline: värskendage kliendikohtumise kuupäeva. |
| Lattu tarnitud | Valikuline: värskendage kuupäeva, mil kaubad lattu tarniti. |
| Kinnitamise kuupäev | Valikuline: värskendage kinnitamise kuupäeva. |
| Tarnejuhised | Valikuline: värskendage tarnejuhiste kuupäeva. |
| Lähtesadam | Sadam, kust kaubad teele saadetakse. |
| Sihtsadam | Sadam, kuhu kaubad saadetakse. |
| Kohalik ekspediitor | Sellel väljal on ainult informatiivne eesmärk. Kohalik ekspediitor peaks olema valitav hankija tabelist. |
| Kohaliku transpordi kuupäev | Sisestage kuupäev, milleks kohalik transport on broneeritud. See väli aitab ladu planeerimisel. |
| Kohaliku transpordi kellaaeg | Sisestage ajavahemik. See väli aitab ladu planeerimisel. |
| Teekonna mall | Teekonna jaoks määratletud teekonna marsruudi mall. Teekonna mall sisaldab üksikasju „sihtsadama“ ja „lähtesadama“ kohta ning täitmisaegu, mis on seostatud saatmiskonteineri jälgimiskontrolliga. |

### <a name="settings-on-the-other-fasttab"></a>Kiirkaardi Muud sätted

Järgmises tabelis kirjeldatakse saatmiskonteineri vaate **Päis** kiirkaardil **Muu** saadaolevaid sätteid.

| Field | Kirjeldus |
|---|---|
| Rent | Väärtus, mis näitab, kas saatmiskonteiner on üüritud saatmiskonteiner. Üürikonteineritega võivad olla seostatud üürikulud. |
| Teisendatud renditavaks | Väärtus, mis näitab, kas saatmiskonteiner on teisendatud üüritud saatmiskonteineriks. Üürikonteineritega võivad olla seostatud üürikulud. |
| Algne reis | Algne teekond, kui saatmiskonteiner on teisaldatud uude teekonda. |
| Kasutatud | Kasutage seda kirjet üüritud saatmiskonteineri kasutamise korral. Sellel on ainult teavitav eesmärk. |
| Eeldatav laadimiskuupäev | Kuupäev, mil eeldatakse saatmiskonteinerisse kaupade laadimist. |
| Meie seerianumber | Sisestage seerianumber, mida kasutatakse ettevõttesiseselt saatmiskonteineri jaoks. |
| Saatmisettevõtte seerianumber | Sisestage seerianumber, mille on saatmiskonteineri jaoks esitanud saatmisettevõte või agent. |
| Ülevaatuse sertifikaadi rakendamise kuupäev | Kuupäev, mil on taotletud saatmiskonteineri ülevaatust. |
| Ülevaatuse sertifikaadi kättesaamise kuupäev | Kuupäev, mil on saadud ülevaatuse sertifikaat. |
| Ülevaatuse sertifikaadi aegumise kuupäev | Kuupäev, mil ülevaatuse sertifikaat aegub. |
| Ülevaatuse sertifikaadi number | Pärast ülevaatust väljastatud sertifikaadi number. |

## <a name="lines-view"></a>Ridade vaade

Vaate **Read** avamiseks avage saatmiskonteiner ja seejärel valige saatmiskonteineri päises ülal paremal vahekaart **Read**.

### <a name="information-on-the-shipping-container-fasttab"></a>Teave kiirkaardil Saatmiskonteiner

Vaate **Read** kiirkaardil **Saatmiskonteiner** on kuvatud teave foolio kohta. Suurem osa sellest teabest ilmub ka päise **vaates**, nagu on kirjeldatud selles artiklis.

### <a name="information-and-buttons-on-the-lines-fasttab"></a>Teave ja nupud kiirkaardil Read

Vaate **Read** kiirkaardil **Read** on kuvatud üksikasjad iga täieliku või osalise ostutellimuse rea kohta, mis on kaasatud praegusesse saatmiskonteinerisse.

Järgmises tabelis kirjeldatakse vaate **Read** kiirkaardil **Read** saadaolevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| Eemaldamine | Eemaldage valitud ostutellimuse rida teekonnast. |
| Varud \> Kanded | Vaadake valitud ostutellimuse rea laokandeid. Pange tähele, et kui kasutate transiidis kaupade funktsiooni, kuvatakse ka algne tellimus ja transiidis olevate kaupade tellimused. |
| Varud \> Kuva dimensioonid | Avage dialoogiboks, kus saate valida varude dimensioonid, mis kuvatakse teie vaadatavate kannete kohta. |
| Värskendamine | Värskendage teavet, mis on seotud valitud ostutellimuserea reasumma, kaalu või mahuga. |

### <a name="information-on-the-lines-details-fasttab"></a>Teave kiirkaardil Ridade üksikasjad

Vaate **Read** kiirkaart **Ridade üksikasjad** kuvab üksikasjad kiirkaardil **Read** parasjagu valitud ostutellimuse rea kohta.
