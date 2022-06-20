---
title: Üle-/alakanded
description: See artikkel annab teavet, mis aitab teil seadistada poliitikate üksikasju üle-/alakannete puhul, nii et süsteem saab määrata, kuidas hallata kaupade ületöötlust ja alatöötlust sissetuleku ajal.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMOverUnderTrans, ITMOverUnderToleranceTable, ITMOverUnderReasonTable, ITMOverUnderToleranceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 79ce18a462f9c2f93dceec82da7ee0209ab61f78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844993"
---
# <a name="overunder-transactions"></a>Üle-/alakanded

[!include [banner](../../includes/banner.md)]

Teekonna tellimuste töötlemisel eeldab süsteem, et lõppsihtlaos tarbimiseks vastu võetud kauba kogus ühtiks teekonnaga seotud ostutellimuse ridadel määratud kogusega. Kuna aga laos ei võeta alati vastu ostutellimuse ridadel olevat täpset kogust, määratleb moodul **Väljalaadimiskulu** reeglite komplekti, mida kasutatakse kaupade üle- ja alatarnete käitlemiseks. Need reeglid on eriti olulised, kuna algne ostutellimus on arveldatud ja seda ei saa enam muuta. Üle-/alakannete poliitikate üksikasjade seadistamisega võimaldate süsteemil määratleda, kuidas hallata kaupade üle- ja alatöötlust sissetuleku ajal. Üle- ja alavarusid saate ka käsitsi hallata, kasutades lehte **Üle-/alakanded**.

## <a name="overunder-tolerances"></a>Lubatud üle-/alakõikumised

Seadistate ületarne ja alatarne kõikumisvahemikud, et määrata üle- ja alakogused või -mahud, mida saab teekonnal töödelda ilma veaolekut põhjustamata. Kui teekonna rea sissetulek on väljaspool neid kõikumisvahemikke, tuleb seda enne teekonna rea edasiseks töötlemiseks sulgemist muuta ja viga lahendada.

Kõikumisvahemike konfigureerimiseks avage **Väljalaadimiskulu \> Üle-/alataseme seadistus \> Üle-/alataseme kõikumisvahemikud**. Seal saate kõikumisvahemike kirjeid vaadata, redigeerida, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Konto kood | <p>Määratlege hankijad, kellele kõikumisvahemik rakendub, valides ühe järgmistest väärtustest.</p><ul><li>**Tabel** – üle-/alataseme kõikumisvahemik rakendub ainult rea jaoks valitud hankijale.</li><li>**Grupp** – üle-/alataseme kõikumisvahemik rakendub rea jaoks valitud hankijate kõikumisvahemiku grupi kõikidele hankijatele.</li><li>**Kõik** – üle-/alataseme kõikumisvahemik rakendub kõikidele hankijatele.</li></ul> |
| Konto seos | Valige hankija või hankijagrupp, millele üle-/alataseme kõikumisvahemik rakendub, sõltuvalt väärtusest, mille valisite väljal **Kontokood**. |
| Kauba kood | <p>Määratlege kaubad, millele kõikumisvahemik rakendub, valides ühe järgmistest väärtustest.</p><ul><li>**Tabel** – üle-/alataseme kõikumisvahemik rakendub ainult rea jaoks valitud kaubale.</li><li>**Grupp** – üle-/alataseme kõikumisvahemik rakendub rea jaoks valitud kaupade kõikumisvahemiku grupi kõikidele kaupadele.</li><li>**Kõik** – üle-/alataseme kõikumisvahemik rakendub kõikidele kaupadele.</li></ul> |
| Kauba seos | Valige kaup või kaubagrupp, millele üle-/alataseme kõikumisvahemik rakendub, sõltuvalt väärtusest, mille valisite väljal **Kaubakood**. |
| Summa lubatud kõikumine | Sisestage summana kõikumisvahemik, mis tuleks rakendada kogu ostutellimusele. |
| Protsentuaalne lubatud kõikumine | Sisestage protsendina kõikumisvahemik, mis tuleks rakendada üksikule ostutellimuse reale. |

## <a name="overunder-reasons"></a>Ületamise/allajäämise põhjused

Kui üle- või alakogus on seotud saadud teekonnareaga, võib olla vaja tuvastada üle- või alakoguse põhjus. Sel juhul saate kaupade kättesaamisel valida vastuvõtureal üle- või alatarne põhjuse.

Üle- ja alatarne põhjuste seadistamiseks avage **Väljalaadimiskulu \> Üle-/alataseme seadistus \> Üle-/alataseme põhjused**. Seal saate olemasolevaid üle- ja alatarne põhjuseid vaadata, redigeerida, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga põhjuse jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Ületamise/allajäämise põhjus | Sisestage üle- või alatarne kande põhjuse kordumatu nimi. |
| Kirjeldus | Sisestage üle-/alataseme põhjuse kirjeldus. |
| Liikumine | Valige üle-/alataseme põhjusega seotud liikumise tööleht. Sellel väljal loetletakse kõik saadaolevad töölehed, millega on töölehe tüüp *Liikumine* lehel **Varude töölehe nimed** seostatud (**Varude halduse seadistamine \> Töölehe nimed \> Varud**). |

## <a name="item-overunder-tolerance-groups"></a>Kauba lubatud üle-/alakõikumise grupid

Sarnaste kõikumisvahemikega kaupu saab grupeerida. Sel viisil saate määrata korraga kõigi selle grupi kaupade üle-/alataseme kõikumisvahemikud.

Kauba üle-/alataseme kõikumisvahemike grupi seadistamiseks avage **Väljalaadimiskulu \> Üle-/alataseme seadistus \> Kaupade üle-/alataseme kõikumisvahemike rühmad**. Seal saate üle-/alataseme kõikumisvahemike gruppide kirjeid vaadata, redigeerida, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Lubatud üle-/alakõikumise grupp | Sisestage grupi kordumatu nimi. Valige kõikumisvahemikku kirjeldav nimi, nt *1% Var*. |
| Kirjeldus | Saate sisestada grupi kirjeldus. |

## <a name="vendor-overunder-tolerance-groups"></a>Hankija lubatud üle-/alakõikumise grupid

Saate grupeerida hankijaid, kes teevad regulaarselt üle- või alatarneid. Seejärel saate määrata gruppidele üle-/alataseme kõikumisvahemikud.

Hankija üle-/alataseme kõikumisvahemike grupi seadistamiseks avage **Väljalaadimiskulu \> Üle-/alataseme seadistus \> Hankijate üle-/alataseme kõikumisvahemike rühmad**. Seal saate üle-/alataseme kõikumisvahemike gruppide kirjeid vaadata, redigeerida, lisada ja eemaldada. Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Üle-/alataseme grupid | Sisestage grupi kordumatu nimi. Valige nimi, mis kirjeldab gruppi kuuluvate hankijate tüüpi. |
| Kirjeldus | Saate sisestada grupi kirjeldus. |

## <a name="view-and-process-overunder-transactions"></a>Üle-/alakannete kuvamine ja töötlemine

Kui ladustatavate kaupade kogus ei vasta lähtekogusele, luuakse kas üle- või alakanne. Saabuva kauba töölehel olevat kogust tuleks uuendada ainult ladustatava kauba kogusega.

Teekonnaridade sissetuleku töötlemisel, saab hankija jaoks määrata üle-/alataseme kõikumisvahemikud. Seejärel vaadatakse kaubad üle ja kinnitatakse. Kõikumisvahemiku saab määrata protsendina, kohaliku summana või mõlemana.

Kui vastuvõetud kaup on kõikumisvahemiku piires, loob süsteem liikumise töölehe. Selle töölehe saab määratleda teekonna parameetrite lehel. Lisaks luuakse üle-/alakanne. Näiteks: tellimuse väärtus on 100 $, sissetuleku väärtus on 99 $ ja need väärtused vastavad kõikumisvahemike reeglitele. Sel juhul luuakse alatasemega koguse jaoks negatiivse liikumise tööleht.

Kui vastuvõetud kaup on kõikumisvahemikust väljas, loob süsteem koguse erinevuse jaoks üle-/alakande.

Üle-/alakannete vaatamiseks ja töötlemiseks avage **Väljalaadimiskulu \> Päringud \> Üle-/alakanded**. Seal seostatakse üle-/alakanne teekonna kõigi üle- või alalaekunud kaupadega. Soovitame kasutada lehte **Üle-/alakanded**, et lahendada kõik teekondadega seotud üle-/alakanded. Ühtlasi soovitame **mitte** kasutada alatarnete laokannete käsitsi lahendamiseks liikumise või inventuuritöölehti. Selle asemel peaksite alatarnitud laokoguste haldamiseks kasutama lehte **Üle-/alakanded**.

### <a name="upper-overview-tab"></a>Ülemine vahekaart Ülevaade

Üle-/alakannete vaatamiseks valige lehe **Üle-/alakanded** ülaosas vahekaart **Ülevaade**. Järgmises tabelis kirjeldatakse ruudustikus saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Üle-/alakande number | Saabumise töölehe töötlemisel automaatselt loodud üle-/alakande kirje kordumatu nimi. |
| Reis | Teekond, millele osturida lisati. |
| Saatmiskonteiner | Konteiner, millesse osturida lisati. |
| Saabumise tööleht | Saabumise tööleht, millest üle-/alataseme rida loodi. |
| Viide | Viide kas ostutellimusele või üleviimistellimusele, mis on üle-/alakandega seostatud. |
| Arv | Üle-/alakandes viidatud ostutellimus. |
| Hankija konto | Hankija, kellega on üle- või alatase seotud. |
| Transiidis olevad kaubad: number | Transiidis olevate kaupade kood, kui see on olemas. |
| Kaubakood | Kauba kood, millega on üle- või alatase seotud. |
| Algne kogus | Ostutellimuse rea algne kogus, mis on saadetisega seotud. |
| Tarnitud kogus | Tegelikult vastu võetud kogus. |
| Erinevus | Saabuva kauba töölehe eeldatava summa ja saabuva kauba töölehele sisestatud summa vahe. Negatiivne väärtus näitab kaupade ületarnet. |
| Järelejääv kogus | Kogus, mis jääb saabuva kauba töölehe reale. |
| Üle-/alatarne | Väärtus, mis näitab, kas vastuvõetud kogus on üle- või alatasemega. |
| Olek | Üle-/alakande olek. Sõltuvalt lehe **[Väljalaadimiskulu parameerid](landed-cost-parameters.md)** sätetest võib ületarne automaatselt luua ületarne summa liikumise töölehe ja sisestada töölehe. Sel juhul on üle-/alakande olek *Lõpule viidud*. Kui kaupade alatarnete laost välja viimiseks on vaja teha tegevus, on kirje olek *Pooleli*. |
| Ületamise/allajäämise põhjus | Üle-/alakandega seostatud põhjus. |
| Muud varude dimensioonid | Vajaduse korral saate võrgustikus kuvada täiendavate dimensioonide veerge. Nende dimensioonide hulka kuuluvad partii number, varude olek ja ladu. Tegevuspaanil valige **Varud \> Kuva dimensioonid**, et avada dialoogiboks, kus saate valida kaasamiseks dimensioonid. |

### <a name="upper-general-tab"></a>Ülemine vahekaart Üldine

Ülemisel vahekaardil **Ülevaade** praegu valitud rea kohta lisateabe vaatamiseks valige lehe **Üle-/alakanded** ülaosas vahekaart **Üldine** . Sellel vahekaardil olev teave hõlmab kõigi saadaolevate dimensioonide väärtusi. See teave tuuakse pärinevalt ostutellimuselt.

### <a name="lower-overview-tab"></a>Alumine vahekaart Ülevaade

Ülemisel vahekaardil **Ülevaade** valitud rea dokumendi tüübi kohta lisateabe vaatamiseks valige lehe **Üle-/alakanded** allosas vahekaart **Ülevaade** . Järgmises tabelis on kirjeldatud saadaolevaid välju.

| Field | Kirjeldus |
|---|---|
| Uue dokumendi tüüp | Selle välja väärtuseks on seatud kas *Liikumise tööleht* või *Ostutellimus*, sõltuvalt tegevusest, mis kuvatakse valitud üle-/alakande real. |
| Arv | Viide ja link kas ostutellimusele või liikumise töölehele, mis on valitud üle-/alakande reaga seostatud. |
| Ületamise/allajäämise põhjus | Valitud üle-/alakande reaga seostatud põhjus. |
| Kogus | Kogus, mille valisite ostutellimusele või liikumise töölehele, mis on valitud üle-/alakande reaga seostatud. |

### <a name="lower-general-tab"></a>Alumine vahekaart Üldine

Valitud üle-/alakande reaga seostatud üle-/alakande numbri, saatepartii ID ja dimensiooninumbri vaatamiseks valige lehe **Üle-/alakanded** allosas vahekaart **Üldine**. 

### <a name="process-overunder-transactions"></a>Üle-/alakannete töötlemine

Lehel **Üle-/alakanded** asuv tegevuspaan pakub lehel valitud kannete töötlemiseks järgmisi käske. Iga käsk võimaldab teil valida, kuidas iga kannet töödelda.

- **Loo \> Liikumine** – saate luua ja sisestada liikumise töölehe valitud kande jaoks. Alakannete puhul luuakse ja sisestatakse liikumise tööleht eeldatava ja tegelikult vastu võetud koguse vahelise erinevuse jaoks automaatselt. Valige see käsk ülekannete jaoks, kui soovite, et hankija teaks kuluerinevust.
- **Loo \> Ostutellimus** – saate luua ostutellimuse valitud kande eeldatava ja tegelikult vastu võetud koguse vahelise erinevuse jaoks. Valige see käsk ülekannete jaoks, kui organisatsioon teab kuluerinevust.
- **Loo \> Üleviimine sihtkohta** – see käsk rakendub ainult üleviimistellimustele. Valige, kui soovite üle- või alakoguse sihtlattu üle viia.
- **Loo \> Üleviimine lähtekohta** – see käsk rakendub ainult üleviimistellimustele. Valige, kui soovite üle- või alakoguse lähtelattu üle viia.
