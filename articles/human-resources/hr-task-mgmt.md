---
title: Ülesandehaldus
description: Selles teemas selgitatakse Microsoftis saadaolevat ülesannete haldamise funktsiooni Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 727e1eb75f807d84f088cf3dd139eb094aa76618
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087213"
---
# <a name="task-management"></a>Ülesandehaldus

[!INCLUDE [PEAP](../includes/peap-1.md)]

Ülesannete haldamine võimaldab teil luua ülesandeid, mis tuleb täita töötajate palkamiseks (pardal), lõpetamiseks (offboard) ja üleviimise (ülemineku) töötajateks. Ülesannete haldamisel kasutatakse kontroll-loendite mõistet. Kontroll-loend on sisse- ja väljamineku- või üleminekuülesannete loendist. Ülesandehaldus kasutab kontroll-loendeid ülesannete rühmitamiseks ja üksikisikutele või rühmadele määramiseks. Sisse- ja väljalülitamise, pardalemineku ja üleminekute kontroll-loendi funktsioon on sarnane.

## <a name="checklist-overview"></a>Kontroll-loendi ülevaade

Kontroll-loend on ülesannete rühm. Kontroll-loendid annavad teile paindliku viisi ülesannete rühmitamiseks ja neid saab uuesti kasutada (näiteks kui palkate täiendavaid töötajaid). Saate luua nii palju kontroll-loendeid kui vaja ja määrata samad ülesanded mitmele kontroll-loendile.

### <a name="examples"></a>Näited

Järgmised näited näitavad, kuidas kontrollnimekirju saab sisseelamisprotsessis kasutada. Kuna aga registreerimisnimekirja funktsioon pardalemineku, pardalemineku ja üleminekute jaoks on sarnane, kehtib teave ka pardalemineku ja ülemineku protsesside kohta.

Osana pardalemineku protsessist saavad inimressursside (HR) spetsialistid luua ülesandeid, mis jälgivad sissetulevate ja hiljuti palgatud töötajate pardalemineku edenemist. Kuna sisseelamisprotsess võib sõltuvalt töötaja asukohast või geograafilisest asukohast erineda, saate luua mitu sissesõidu kontroll-loendit, et mahutada erinevaid värbamisolukordi.

**Näide 1**

Iga Töötaja, kes on palgatud Ameerika Ühendriikides, peab täitma selliseid ülesandeid nagu maksude kinnipidamise vormide täitmine. Kuid sellised ülesanded nagu ettevõtte auto määramine võivad olla kohaldatavad ainult täitevtasandi töötajatele. Sellisel juhul saab luua kaks pardalemineku kontrollnimekirja: **ainult USA-s asuvad töötajad** ja **juhid**. Seejärel, kui Ameerika Ühendriikides palgatakse keskastme juht, **valitakse USA-s asuv töötajate** kontrollnimekiri. Kui aga Ameerika Ühendriikides palgatakse juhtivtöötaja, valitakse mõlemad kontrollnimekirjad, et tagada kõigi nõutavate pardalemineku ülesannete täitmine.

**Näide 2**

Ettevõttel on nii hooajatöötajad kui ka regulaarsed täistööajaga töötajad. Kuigi mõned ülesanded (näiteks uue töötaja saabumisaja kontrollimine) kehtivad mõlemat tüüpi töötajatele, kehtivad mõned lisaülesanded ainult tavalistele täistööajaga töötajatele. Sellisel juhul saate luua kaks kontroll-loendit. Mõlemad kontrollnimekirjad sisaldavad ülesandeid, mis kehtivad nii hooajalistele kui ka tavalistele täistööajaga töötajatele, kuid ainult üks kontrollnimekiri sisaldab neid ülesandeid, mis on spetsiifilised tavalistele täistööajaga töötajatele.

## <a name="task-management-workspace"></a>Ülesandehalduse tööruum

Tööruumis **Ülesandehaldus** loetletakse kõik toimingud, mis on määratud üksikisikutele sisse- ja väljalülitamise ja ülemineku protsessides. Protsessi ülesannete vaatamiseks valige vasakus ülanurgas sobiv vahekaart: **Sisse- ja** väljaminek **, Offboarding** või **Transitions**. Vaikimisi pääsevad ülesandehalduse **tööruumile juurde** ainult personalispetsialistid.

Vahekaart **Onboarding** sisaldab loendit **Alusta varsti**, mis näitab sissetulevaid töötajaid, ja hiljuti palgatud **loendit**, mis näitab hiljuti palgatud töötajaid. Mõlemas loendis saate valida ainult ühe töötaja. Töötaja valimisel kuvatakse lehe paremal küljel kõik selle töötaja pardaleminekuga seotud ülesanded. Vahekaart **Onboarding** sisaldab ka loendit **Kõik tööülesanded**, mis näitavad kõiki sissetulevate või hiljuti palgatud töötajate ülesandeid. Lõpuks sisaldab see tähtaja ületanud ülesannete loendit ja praegusele kasutajale määratud ülesannete loendit.

Vahekaart **Offboarding** sisaldab ettevõttest lahkuvate töötajate loendit ja ettevõttest juba väljunud töötajate loendit. Mõlemas loendis saate valida ainult ühe töötaja. Töötaja valimisel kuvatakse kõik selle töötaja offboardingiga seotud ülesanded. Vahekaart **Offboarding** sisaldab ka loendit **Kõik tööülesanded**, mis näitavad kõiki väljunud või väljunud töötajate ülesandeid. Lõpuks sisaldab see tähtaja ületanud ülesannete loendit ja praegusele kasutajale määratud ülesannete loendit.

Vahekaart **Üleminekud sisaldab loendit** Kõik **tööülesanded**, mis kuvab kõik ülesanded kõigi töötajate jaoks, kes vahetavad positsioone või kes on hiljuti positsioone muutnud. Samuti on olemas tähtaja ületanud ülesannete loend ja praegusele kasutajale määratud ülesannete loend.

Kõigil kolmel vahekaardil saavad personaliassistendid ja haldurid teha järgmised tegevused.

- Rakenda töötajale kontroll-loend.
- Värskendage tööülesande olekut.
- Ülesande ümbermääramine.
- Värskendage ülesande tähtaega.

> [!NOTE]
> Vaikimisi kuvatakse vahekaardil Onboarding **töötajad,** kes on viimase seitsme päeva jooksul palgatud. Selle sätte muutmiseks **sisestage lehe** Inimressursside parameetrid **vahekaardi Üldine** väljale **Viimatised palgad** ajaraami. Loendis Viimatised **palgad** olevat teavet saab kuvada kindla päevade, kuude või aastate kohta. Näiteks viimase 14 päeva jooksul palgatud töötajate loendi vaatamiseks seadke **välja** Periood **14** ja **välja Ühikuks** **Päevad**.
>
> **Lehel Inimressursside parameetrid** saate värskendada ka väljunud ja väljunud töötajate loendite kuupäevavahemikku, mis kuvatakse vahekaardil **Offboarding**.
>
> Need sätted kehtivad ka personalihalduse **tööruumi kohta**.

## <a name="setting-up-tasks"></a>Ülesannete häälestamine

Saate luua ülesandeid individuaalselt ja seejärel neid mitmes kontroll-loendis uuesti kasutada. Tööülesande **loomiseks valige lehel Pardalemineku häälestus** vahekaardil **Tööülesanded** suvand **Uus**.

Teise võimalusena saate ülesandeid lisada otse kontroll-loendisse. Ülesande lisamiseks kontroll-loendisse klõpsake **Sisselülitamise seadistamine** lehel **Kontrollnimekiri** looge ülesande lisamiseks uus kontroll-loend või lisage ülesanne olemasolevasse kontroll-loendisse.

> [!NOTE]
> Kui lisate ülesande otse kontroll-loendisse, ei saa te seda teistes kontroll-loendites uuesti kasutada.

Järgmises tabelis kirjeldatakse välju, mis on saadaval, kui loote ülesande kummagi meetodiga.

| Field           | Kirjeldus |
|-----------------|-------------|
| Ülesanne            | Sisestage ülesande nimi. |
| Kirjeldus     | Sisestage ülesande kirjeldus. |
| Valikuline        | Määrake, kas ülesanne on valikuline ja ainult informatiivne. |
| Ülesande link       | Sisestage välise veebilehe URL või rakenduses konkreetne leht, kus kasutaja peaks ülesande täitma. Lisateabe saamiseks vaadake [Ülesande lingid](#task-links) osa. |
| Määramise tüüp | Ülesandeid saab määrata konkreetsele töötajale, ametikohale või ametikohtade rühmale, mõjutatud töötaja juhile (st töötajale, kes osaleb sisse-, välja- või üleminekuprotsessis) või mõjutatud töötajale. Valige ülesande tüüp. Lisateabe saamiseks vaadake [Ülesande tüübid](#assignment-types) osa. |
| Määratud töötajale     | Valige konkreetne töötaja, ametikoht või ametikohtade rühm, millele ülesanne määrata. |
| Kontaktisik  | Täpsustage isik, kelle poole tuleks pöörduda, kui ülesande kohta on küsimusi. |
| Tähtaja nihe | Määrake päevade arv enne või pärast ülesande täitmise tähtaega liitumis-, lõpetamis- või üleminekukuupäeva. Lisateabe saamiseks vaadake [Ülesande tähtpäevad ja väli Tähtaja nihe](#task-due-dates-and-the-due-date-offset-field) osa. |
| Juhised    | Sisestage juhised ülesande täitmiseks. Lisateabe saamiseks vaadake [Juhised](#instructions) osa. |

### <a name="task-links"></a>Ülesande lingid

Ülesande link pakub linki välisele veebilehele või Dynamics 365 rakenduse lehele. Saate määrata ülesande lingi, kui ülesandele määratud isik peaks selle ülesande täitmiseks minema Dynamics 365 rakenduses konkreetsele veebilehele või konkreetsele lehele. Ülesande lingi loomisel saate valida ühe järgmistest valikutest.

- **Menüüelement** – Kui valite selle suvandi, kuvatakse kõigi Dynamics 365 rakenduse lehtede loend. Valige loendist leht.
- **URL** – Kui valite selle suvandi, sisestage selle veebilehe URL, kuhu soovite ülesandega määratud isikul liikuda. Määratud leht võib olla leht, mis ei ole Dynamics 365 rakenduse osa.
- **Töötaja andmed** – Kui valite selle suvandi, valige üks järgmistest valikutest.

    - **Töötaja iseteenindustegevused** – See suvand näitab saadaolevate lehtede loendit **Töötaja iseteenindus**. Kasutage seda, kui kaasatud töötajale määratud ülesanne tuleb täita **Töötaja iseteenindus**. Näiteks kui soovite, et töötaja sisestaks oma isiklikud kontaktandmed, valige **Töötaja iseteenindustegevused** ja seejärel valige **Isiklikud detailid&gt; Isiklik informatsioon**.
    - **Töötajate juhtimise toimingud** – See suvand kuvab lehtede loendi, mis on seotud töötaja kirjega, kuid mis pole töötajale juurdepääsetavad. Näiteks kui soovite, et ülesande omanik sisestaks konkreetse töötaja kohta käiva teabe, näiteks hüvitisteabe, valige **Töötajate juhtimise toimingud** ja seejärel valige **Hüvitis&gt; Fikseeritud hüvitis**.

### <a name="assignment-types"></a>Ülesande tüübid

Kui töötaja võetakse tööle, lõpetatakse või üle viiakse, saab valida ühe või mitu kontrollnimekirja. Pärast kontrollnimekirja valimist ja töölevõtmise, lõpetamise või üleviimise protsessi lõppu luuakse ülesanded ja määratakse kasutajatele edenemise jälgimiseks.

Kui ülesanne on loodud, määratakse see konkreetsele kasutajale. Kasutaja, kellele ülesanne määratakse, sõltub selle ülesande jaoks valitud ülesande tüübist. Järgmised väärtused on saadaval **Ülesande tüüp** väli:

- **Tööline** – Määrake ülesanne konkreetsele töötajale. Pärast selle väärtuse valimist valige jaotisest töötaja **Määratud** valdkonnas.
- **positsioon** – Määrake ülesanne konkreetsele ametikohale. Pärast selle väärtuse valimist valige positsioonis **Määratud** valdkonnas.

    Näiteks IT-insener vastutab alati uue töötaja sülearvuti ettevalmistamise eest. Sel juhul valige sülearvuti konfiguratsiooniülesande loomisel **positsioon** ülesande tüübina ja seejärel valige **IT insener** kui positsioon. Seejärel, kui töötaja on palgatud ja kontrollnimekiri on määratud, määratakse sülearvuti konfiguratsiooniülesanne sellele töötajale, kes on IT-inseneri ametikohal palkamistoimingu sisestamise ajal.

- **Grupp** – Määrake ülesanne ametikohtade rühmale (ülesannete grupp). Pärast selle väärtuse valimist valige loendis rühm **Määratud** valdkonnas. Lisateabe saamiseks vaadake [Ülesanderühmade seadistamine (valikuline)](#setting-up-assignment-groups-optional) osa.
- **Juht** – Määrake ülesanne töölevõetava, töö lõpetamise või üleviimise töötaja juhile.

    > [!IMPORTANT]
    > Kontrollnimekirja rakendamisel, kui palgatud, lõpetatud või üleviidud töötajale pole praegu määratud ühtegi ametikohta, ei saa juhti määrata. Sel juhul määratakse ülesanne kontrollnimekirja omanikule. Lisateabe saamiseks vaadake [Kontrollnimekirjade koostamine](#setting-up-checklists) osa.

- **Töötaja** – Määrake tööle võetav, lõpetatav või üleviidav töötaja.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Ülesande tähtpäevad ja väli Tähtaja nihe

Tööülesannete tähtpäevad põhinevad töösuhte alguskuupäeval, lõpetamise kuupäeval või üleminekukuupäeval. Mõned ülesanded tuleb lõpetada enne töötaja alguskuupäeva, samas kui teised ülesanded saab lõpetada pärast seda. Ülesande määratlemisel määrate **Tähtaja nihe** väljale tähtpäeva määramiseks, mis on seotud alguskuupäeva, lõpetamise kuupäeva või üleminekukuupäevaga. Näiteks IT-insener peab uuele töötajale sülearvuti ette valmistama kaks päeva enne selle töötaja alguskuupäeva. Sel juhul määrake sülearvuti konfiguratsiooniülesande loomisel **Tähtaja nihe** väljale **-2**. Siis, kui töötaja töö alguskuupäev on 5. mai, siis ülesande täitmise tähtaeg on 3. mai.

> [!NOTE]
> Tähtaegu saab muuta pärast ülesande loomist.

Tähtajad arvutatakse kontrollnimekirjaga seotud kalendri alusel. Lisateabe saamiseks vaadake [Kontrollnimekirjade koostamine](#setting-up-checklists) osa.

### <a name="instructions"></a>Juhised

Komplekssed ülesanded võivad nõuda mitut sammu või ülesande täitja peab andma lisateavet. Aastal **Juhised** väljale saate sisestada juhiseid või lisateavet, et aidata isikul, kellele ülesanne on määratud, seda täita.

## <a name="setting-up-checklists"></a>Kontrollnimekirjade koostamine

Kontroll-loend on ülesannete rühm. Saate luua nii palju kontroll-loendeid kui vaja ja määrata samad ülesanded mitmele kontroll-loendile. Kontrollnimekirja loomisel määrate omaniku ja kalendri.

Kui **Ülesande tüüp** ülesande väli on seatud **positsioon**, **·**, või **Grupp**, kuid ülesande tüübist ei saa tuletada ühtegi konkreetset isikut, määratakse ülesanne kontrollnimekirja omanikule. Siin on mõned näited olukordadest, kus kontrollnimekirja omanikule määratakse ülesanded.

- Tööle võetavale või koondatavale töötajale ametikohta ei määrata. Kuna töötajal ei ole ametikoha määramist, ei saa tema juhti määrata.
- The **Ülesande tüüp** väli on seatud **positsioon**, kuid ülesande loomise ajal pole sellele ametikohale määratud ühtegi töötajat. Näiteks **Sülearvuti seadistamine** ülesanne on määratud positsioonile 000876 (**Tehnilise toe spetsialist**). Töötaja töölevõtmise ajal ei määrata ühtegi töötajat ametikohale 000876. Seetõttu luuakse kontrollnimekirja omanikule ülesanne.
- The **Ülesande tüüp** väli on seatud **Grupp**, kuid ülesande loomise ajal pole rühma ametikohtadele määratud ühtegi töötajat.

Kontrollnimekirja jaoks määratud kalendrit kasutatakse sellesse kontrollnimekirja kuuluvate ülesannete tähtpäevade arvutamiseks. Töö- ja puhkepäevad määratakse kalendri seadistuses. Tööülesannete täitmise tähtpäeva arvestamisel arvestatakse tööpäevad ja välja jäetakse vabad päevad. Töövabade päevade hulka kuuluvad nädalavahetused ja pühad. 

Pärast kalendri seadistamist seostatakse see kontrollnimekirja malliga. Nii arvutatakse iga kontrollnimekirjas oleva ülesande tähtaeg samal viisil. Saate seadistada mitu kalendrit, kuid iga kontrollnimekirjaga saab seostada ainult ühe kalendri.

## <a name="setting-up-assignment-groups-optional"></a>Ülesanderühmade seadistamine (valikuline)

Mõnikord vastutab ülesande eest rühm inimesi. Näiteks võib IT-töötajate rühm vastutada sülearvutite ettevalmistamise eest uute töötajate jaoks.

Ülesanderühma seadistamiseks järgige neid samme.

1. peal **Grupiülesanne** leht, valige **Uus**.
1. Sisestage nimi (näiteks **IT sülearvuti**) ja rühma kirjeldus.
1. Valige käsk **Salvesta**.
1. peal **liikmed** FastTab, valige **Lisama**.
1. Aastal **Positsioonid** väljal valige kõik ametikohad, mis ülesande eest vastutavad.

Pärast ülesannete rühma loomist on see ülesande loomisel valimiseks saadaval. Ülesande jaoks konkreetse rühma valimiseks peate valima **Grupp** aastal **Ülesande tüüp**. Teie loodud grupp on seejärel valikus saadaval **Määratud** valdkonnas.

> [!IMPORTANT]
> Kui ülesanne on määratud rühmale, märgitakse ülesanne kui **Lõpetatud** kui üks inimene rühmas selle lõpetab. Ülesanded luuakse töölevõtmise, lõpetamise või ülemineku ajal. Need luuakse kasutajatele, kes on määratud rühma kaasatud ametikohtadele.

## <a name="setting-up-task-groups-optional"></a>Töörühmade seadistamine (valikuline)

Sisse-, välja- või üleminekuprotsess võib hõlmata paljusid ülesandeid. Kõigi nõutavate ülesannete kontroll-loendisse määramise hõlbustamiseks saate seotud ülesannete kategoriseerimiseks luua valikulisi tegumirühmi. Näiteks personali-, IT- ja palgaarvestusosakond peavad uue töötaja palkamiseks täitma konkreetseid ülesandeid. Seetõttu loote järgmised töörühmad: **HR**, **·**, ja **Palgaarvestus**. Seejärel saate ülesande loomisel ühe neist töörühmadest sellega seostada.

Kui soovite lisada ülesande kontroll-loendisse, saate ülesannete loendit filtreerida selle töörühma järgi, millele soovitud ülesanne on määratud. Näiteks kontrollnimekirja malli loomisel saate loendit filtreerida nii, et ainult need IT-ülesanded, mis on määratud **IT** töörühmad on näitusel. Seetõttu saate tagada, et valitud on ainult asjakohased IT-ülesanded.

## <a name="using-checklists"></a>Kontrollnimekirjade kasutamine

Kui töötaja võetakse tööle, lõpetatakse või üle viiakse, saab valida ühe või mitu kontrollnimekirja. Tööülesannete tähtpäevad ja töötajate ülesanded luuakse pärast palkamise, lõpetamise või üleminekuprotsessi lõppu. Näiteks kui valite **Laenutus** või **Rentige ja lisage üksikasju** nuppu, luuakse ülesanded üksikisikutele, lähtudes ülesande tüübist.

Igale ülesandele määratakse tähtaeg, lisades või lahutades töötaja alguskuupäevast tähtpäeva nihe. Lisateabe saamiseks vaadake [Ülesande tähtpäevad ja väli Tähtaja nihe](#task-due-dates-and-the-due-date-offset-field) osa.

Kui kasutate personalitoiminguid, luuakse ülesanded, kui **Täielik** nupp on valitud või toiming kinnitatakse.

Aastal **Ülesannete haldamine** tööruumis saate rakendada töötajale kontrollnimekirja, valides töötaja lihtsal loendi lehel või üksikasjade lehel ja seejärel valides **Rakenda kontrollnimekiri**. Väärtus **Sihtkuupäev** välja kasutatakse ülesannete tähtpäeva arvutamiseks. Tavaliselt peaks sihtkuupäev ühtima töötaja töölevõtmise, lõpetamise või ülemineku kuupäevaga.

Samuti saate töötajale kontrollnimekirja rakendada, avades tema **Tööline** leht ja valimine **Kontrollnimekirjad** menüüs.

## <a name="completing-tasks"></a>Ülesannete täitmine

peal **Töötaja iseteenindus** lehel saab töötaja vaadata kõiki talle määratud ülesandeid. Iga määratud ülesande puhul **Ülesanne**, **·**, **·**, ja **Kontaktisik** väärtused on näidatud. Lisaks saab töötaja iga ülesande jaoks avada seotud välise veebilehe või seotud lehe rakenduses Dynamics 365.

Ülesandeid saab märkida kui **Pooleli**, **·**, või **Lõpetatud**. Kui ülesanne määrati rühmale, märgitakse see kui **Lõpetatud** kui üks inimene rühmas selle lõpetab.

Ülesandeid saab ka ümber määrata.
