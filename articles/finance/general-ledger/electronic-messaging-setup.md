---
title: Elektroonilise sõnumi häälestamine
description: See artikkel annab teavet selle kohta, kuidas seadistada elektrooniliste teadete (EM) funktsioone.
author: liza-golub
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 6ac6e4fbc37165a3126de3b1f937a43c980410b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874547"
---
# <a name="set-up-electronic-messages"></a>Elektroonilise sõnumi häälestamine

[!include [banner](../includes/banner.md)]

**Elektroonilise sõnumside** (EM) abil saate hallata erinevaid elektroonilise aruandluse protsesse erinevate dokumenditüüpide jaoks. Mõnes keerukamas stsenaariumis, mis toetab [riigipõhist arunde lisandmoodulit](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality) seadistatakse elektrooniline sõnumside mitme sõnumi olekute, sõnumiüksuste olekute, tegevuste, lisaväljade ja täidetavate klasside kombinatsioonina. Nende stsenaariumide jaoks on importimiseks saadaval andmeüksuste paketid. Kui te kasutate neid andmeüksuse pakette, peate need importima juriidilisse isikusse, kasutades andmehalduse tööriista. Lisateavet andmehalduse tööriista kasutamise kohta vt jaotisest [Andmehaldus](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

Kui te ei impordi andmeüksuse paketti, saate elektronsõnumite funktsiooni seadistada käsitsi. Sel juhul peate seadistama järgmised elemendid:

- [Numbriseeriad](#sequences)
- [Sõnumiüksuste tüübid](#types)
- [Sõnumiüksuste olekud](#item)
- [Sõnumite olekud](#statuses)
- [Lisaväljad](#additional)
- [Täidetava klassi sätted](#executable)
- [Kirjete asustamise tegevused](#populate)
- [Saate asustada mitme ettevõtte kirjed.](#multiple-companies-populate)
- [Veebirakendused](#applications)
- [Veebiteenuse sätted](#settings)
- [Sõnumi töötlemise tegevused](#actions)
- [Elektronsõnumi töötlemine](#processing)

Järgmised jaotised annavad iga elemendi kohta lisateavet.

## <a name="number-sequences"></a><a id="sequences"></a>Numbriseeriad

Saate seadistada numbriseeriad nii sõnumite kui ka sõnumiüksuste jaoks. Numbriseeriaid kasutatakse sõnumite ja sõnumiüksuste automaatseks nummerdamiseks. Määratud numbreid kasutatakse süsteemis sõnumite ja sõnumiüksuste kordumatute identifikaatoritena. Saate elektroonilise sõnumside jaoks numbriseeriad seadistada lehel **Pearaamatu parameetrid** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**.

## <a name="message-item-types"></a><a id="types"></a>Sõnumiüksuste tüübid

Sõnumiüksuste tüübid tuvastavad kirjete tüübid, mida kasutatakse elektronsõnumites. Saate sõnumiüksuste tüübid seadistada lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste tüübid**.

## <a name="message-item-statuses"></a><a id="item"></a>Sõnumiüksuste olekud

Sõnumiüksuste tüübid tuvastavad olekud, mis rakenduvad sõnumiüksustele teie seadistataval töötlemisel. Saate sõnumiüksuste olekud seadistada lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste olekud**.

Sõnumiüksuse oleku parameeter **Luba kustutamine** määrab selle, kas saate lehel **Elektronsõnumid** või **Elektronsõnumi üksused** selle olekuga sõnumiüksuseid kustutada.

## <a name="message-statuses"></a><a id="statuses"></a>Sõnumite olekud

Saate seadistada sõnumite olekud, mis peaksid sõnumite töötlemisel kättesaadavad olema. Saate sõnumiüksuste olekud seadistada lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumi olekud**.

Järgmises tabelis kirjeldatakse lehe **Sõnumite olekud** välju.

| Välja nimi          | Kirjeldus |
|---------------------|-------------|
| Teate olek      | Saate sisestada sõnumi olekule kordumatu nime. Sõnumiolekuid kasutatakse elektronsõnumi oleku iseloomustamiseks igal ajahetkel. Sisestatud nimi kuvatakse lehel **Elektronsõnumid** ja elektronsõnumitega seotud logis. |
| Kirjeldus         | Saate sisestada sõnumi oleku kirjelduse. |
| Vastuse tüüp       | Saate valida sõnumi olekuks vastuse tüübi. Töötluse mõned tegevused võivad anda enam kui üht tüüpi vastuseid. Näiteks tegevused tüübiga **Veebiteenus** võib olenevalt selle täitmise tulemusest anda vastuseks tüübi **Edukalt täidetud** või **Tehniline tõrge**. Sel juhul peab määrama sõnumi oleku mõlema vastusetüübi korral. Lisateavet tegevusetüüpide ja nendega seotud vastuste [tüüpide](#action-types) kohta vt selle artikli jaotisest Teate töötlemise tegevusetüübid. |
| Sõnumiüksuse olek | Mõnikord peab elektronsõnumi olek mõjutama seotud sõnumiüksuste olekut. Valige sellel väljal sõnumiüksuse olek, mille soovite sõnumi olekuga seostada. |
| Luba kustutamine        | Märkige see ruut, kui kasutajatel peab olema võimalik kustutada elektronsõnumeid, millel on lehel **Elektronsõnumid** see olek. |

## <a name="additional-fields"></a><a id="additional"></a>Lisaväljad

EM-funktsioon võimaldab teil koguda kirjeid Microsoft Dynamics 365 finantside kandetabelist teate kaupadena. Sel viisil saate kirjed aruandluseks ette valmistada ja seejärel need esitada. Mõnikord pole aga kandetabelites piisavalt teavet, et täita kirjeid aruandluse nõuetele vastaval viisil. Kogu teabe täitmiseks, mis tuleb kirje kohta esitada, saate seadistada lisaväljad. Lisaväljad saab seostada nii sõnumite kui ka sõnumiüksustega. Saate sõnumiüksuste olekud seadistada lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Lisaväljad**.

Järgmises tabelis kirjeldatakse lehe **Lisaväljad** üldisi välju.

| Field       | Kirjeldus |
|-------------|-------------|
| Välja nimi  | Saate sisestada protsessiga seotud elektrooniliste sõnumite üksuste täiendava välja nime. See nimi kuvatakse kasutajaliideses, kui töötate protsessiga. Nime saab kasutada ka elektroonilise aruandlusega (ER) konfiguratsioonides, mis on protsessiga seotud. |
| Kirjeldus | Saate sisestada lisavälja kirjelduse. |
| Kasutaja redigeerimine   | Valige selle suvandi sätteks **Jah**, kui kasutajatel peab olema võimalik lisavälja väärtust kasutajaliideses muuta. |
| Loendur     | Valige selle suvandi sätteks **Jah**, kui lisaväli peab sisaldama elektronsõnumis numbriseeriat. Lisaväljale sisestatakse väärtused automaatselt tegevuse **Elektroonilise aruandluse eksport** tüübi käitamise ajal. |
| Peidetud      | Seadke see valik väärtusle **jah** kui lisaväli peaks olema peidetud kasutajaliideses **elektrooniliste teadete** lehel või **elektroonilise teate üksuste** lehel. |

Kiirkaardil **Väärtused** saate eelmääratleda väärtused, mis lisaväljal võivad olla. Seejärel on need väärtused kasutajatele valimiseks saadaval. Seetõttu ei pea neid töötlemise ajal käsitsi sisestama. Järgmises tabelis kirjeldatakse välju.

| Field                | Kirjeldus |
|----------------------|-------------|
| Välja väärtus          | Saate sisestada aruandluse ajal sõnumi või sõnumiüksusega kasutatava väljaväärtuse. |
| Kirjeldus          | Saate sisestada välja väärtuse kirjelduse. |
| Konto tüüp         | Mõni välja väärtus võib olla piiratud kindla kontotüübiga. Valige üks järgmistest väärtustest: **Kõik**, **Klient** või **Hankija**. |
| Konto kood         | Kui valisite väljal **Konto tüüp** suvandi **Klient** või **Hankija**, saate täiendavalt piirata välja väärtuse kasutamist kindla grupi või tabeliga. |
| Konto/grupi number | Kui valisite väljal **Konto tüüp** väärtuse **Klient** või **Hankija** ja sisestasite väljale **Konto kood** grupi või tabeli, saate sellele väljale sisestada kindla grupi või vastaspoole. |
| Jõustunud            | Saate määrata kuupäeva, mil väärtust tuleks arvestama hakata. |
| Aegumine           | Saate määrata kuupäeva, mil väärtuse arvestamine tuleks lõpetada. |

Vaikimisi ei mõjuta väljadega **Konto/grupi number**, **Konto kood**, **Jõustunud** ja **Aegumine** määratletud kriteeriumide kombinatsioonid lisaväljade väärtuste valikut. Siiski saab neid kombinatsioone kasutada täidetavas klassis, et rakendada kindlat loogikat, mis arvutab lisaväljade väärtused.

## <a name="executable-class-settings"></a><a id="executable"></a>Täidetava klassi sätted

Täidetav klass on X++ meetod või klass, mida elektronsõnumite töötlemine saab seoses tegevusega kutsuda, kui protsessi jaoks on vajalik hindamine.

Saate käsitsi seadistada täitmisklassi, mis tuleb kutsuda töötlemise ajal, määrates **Maksu** \> **Seadistamise** \> **Elektrooniliste teadete** \> **täitmisklassi sätted**. Looge **täitmisklassi sätete** lehel rida ja seadke järgmised väljad.

| Field                 | Kirjeldus |
|-----------------------|-------------|
| Täidetav klass      | Saate sisestada nime, mida kasutatakse, kui seadistatakse sõnumi töötlemise tegevust, millega seoses seda klassi kutsutakse. |
| Kirjeldus           | Saate sisestada täidetava klassi kirjelduse. |
| Täidetava klassi nimi | Saate valida X++ täidetava klassi. |
| Käivitamise tase       | See väli määratakse automaatselt, sest väärtus peab valitud täidetava klassi jaoks olema eelmääratletud. See väli piirab taset, millel seotud hindamine käivitatakse. |
| Klassi kirjeldus     | See väli määratakse automaatselt, sest väärtus peab valitud täidetava klassi jaoks olema eelmääratletud. |
| Tegevuse tüüp           | See väli on saadaval, kui **\[EM\] täitmisklassi tegevuse tüübi** funktsioon on **funktsioonihalduse** tööruumis sisse lülitatud. Sellel väljal saate määrata täitmisklassi tegevusetüübi. See väli võimaldab täpsemat kontrolli järgmise tegevuse üle, mis on **elektroonilise teate** lehel saadaval. |

Mõnel täidetaval klassil võivad olla kohustuslikud parameetrid, mille peab määrama enne täidetava klassi esmakordset käivitamist. Nende parameetrite määratlemiseks valige tegevuspaanil **parameetrid**. Sisestage ilmuvasse dialoogiaknasse kommentaar ja seejärel valige **OK**. Kindlasti tuleb valida **OK**. Muidu ei salvestata parameetreid andmebaasis ja täidetavat klassi ei kutsuta õigesti.

## <a name="populate-records-actions"></a><a id="populate"></a>Kirjete asustamise tegevused

Saate kasutada kirjete asustamise tegevusi, et seadistada tegevusi, mis lisavad kirjed sõnumiüksuste tabelisse, et neid saaks lisada elektronsõnumile. Näiteks kui teie elektronsõnum peab teatama kliendiarveid, peate seadistama kirjete asustamise tegevuse, mis on lingitud tabeli Kliendiarve tööleht väljaga **Andmeallikas**.

Saate seadistada kirjete asustamise tegevused lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Kirjete asustamise tegevused**. Looge uus kirje iga tegevuse jaoks, mis peaks lisama kirjeid tabelisse, ja määrake järgmised väljad.

| Väli       | Kirjeldus |
|-------------|-------------|
| Nimi        | Saate sisestada nime tegevusele, mis täidab teie protsessis kirjed. |
| Kirjeldus | Saate sisestada kirjete asustamise tegevuse kirjelduse. |

Kiirkaardil **Andmeallikate seadistus** lisage rida iga andmeallika jaoks, mida protsessis kasutatakse, ja määrake järgmised väljad.

| Väli                  | Kirjeldus |
|------------------------|-------------|
| Nimi                   | Saate andmeallikale sisestada nime. |
| Sõnumiüksuse tüüp      | Saate valida sõnumiüksuse tüübi, mida tuleb kasutada, kui andmeallika jaoks luuakse kirjeid. |
| Konto tüüp           | Saate valida konto tüübi, mis tuleb seostada andmeallika kirjetega. |
| Peatabeli nimi      | Saate valida tabeli, mis peab olema andmeallikas. |
| Dokumendi numbriväli  | Saate valida välja, millelt tuleks valitud peatabelis võtta dokumendi number. Selle välja väärtust kasutatakse teateüksuse **Dokumendinumber** välja väärtusena. |
| Dokumendi kuupäevaväli    | Saate valida välja, millelt tuleks valitud peatabelis võtta dokumendi number. Selle välja väärtust kasutatakse teateüksuse **Sõnumiüksuse kuupäev** välja väärtusena. |
| Dokumendi kontoväli | Saate valida välja, millelt tuleks valitud peatabelis võtta dokumendi number. Selle välja väärtust kasutatakse teateüksuse **Kontonumber** välja väärtusena. |
| Ettevõte                | See väli on saadaval, kui **kirjete tegevuste funktsiooni ettevõtteülesed päringud** on **funktsioonihalduse** tööruumis sisse lülitatud. Kasutage seda funktsiooni ettevõtteüleste andmeallikate häälestamiseks asustatud kirjete tegevuste jaoks. Andmeid saab tuua mitmest ettevõttest. |
| Kasutaja päring             | <p>Kui valite päringu loomiseks ruudustiku kohal suvandi **Redigeeri päringut** ja määrate kriteeriumid, mida tuleb rakendada valitud koondtabelile, mille andmed täidetakse, valitakse see märkeruut automaatselt. Muul juhul täidetakse kõik kirjed valitud põhitabeli allikast.</p><p>Kui **asustatud kirjete tegevuste funktsiooni kontserniülesed** päringud on sisse lülitatud ja kirjed tuleb koguda mitmelt ettevõttelt, lisage rida iga täiendava juriidilise isiku jaoks, kes tuleb aruandlusesse **funktsioonihalduse** töötuumis kaasata. Iga uue rea jaoks valige käsk **Redigeeri päringut** ja määrake rea väljal **Ettevõte** määratud juriidilisele isikules eostuv kriteerium. Kui olete lõpetanud, sisaldab **andmeallikate häälestuse** ruudustik kõigi juriidiliste isikute ridu, mis tuleb aruandesse kaasata.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a> Saate asustada mitme ettevõtte kirjed.

Kui teie ettevõte peab esitama aruande mitmest sama finantsandmebaasi juriidilisest isikust, [seadistage](#populate) asusta kirjete tegevused kõigile juriidilistele isikutele, kelle andmed tuleb aruandesse kaasata.

Selle võimaluse lubamiseks finantskeskkonnas järgige neid samme. 

1. Avage tööruumide **funktsioonihaldus** \> **·**.
2. Otsige ja valige **loendi asusta kirjete tegevuste funktsiooni jaoks ettevõtetevahelised** päringud.
3. Valige **Luba kohe**. 

Et seadistada mitme [ettevõtte asustamiskirjete](#populate) tegevused, millest tuleb andmed aruandlusesse kaasata, järgige neid samme.

1. Minge maksu seadistamise **elektrooniliste** \> **teadete** \> **asustamiskirjete** \> **tegevustele.**

    Kui ettevõtteülesed päringud asustamiskirjete **tegevuste funktsiooni kohta on lubatud,** sisaldab **andmeallikate** häälestusruudustik **tegevuslehel Asusta kirjed ettevõtte** **välja.** See väli näitab praeguse juriidilise isiku ID-d [olemasolevate](#populate) kirjete puhul, mis loodi asustamiskirjete tegevuste üldise seadistuse ajal.

2. Andmeallikate **häälestusruudustikus** lisage rida igale all juriidilisele isikule, kes tuleb aruandlusesse kaasata ja seadke järgmised väljad.

    | Välja nimi             | Väärtus |
    |------------------------|-------|
    | Nimi                   | Sisestage tekstiväärtus, mis aitab teil mõista, kust see kirje pärineb. Näiteks sisestage **andmeallika nimi - allettevõte 1**. |
    | Sõnumiüksuse tüüp      | Valige teate kauba tüüp, mis on vajalik EM-i töötlemiseks. |
    | Konto tüüp           | Määrake konto tüüp, mis on vajalik EM-i töötlemiseks. Kui teie EM-töötlusel pole kindlaid kontotüüpe, valige **väärtus Kõik**. |
    | Peatabeli nimi      | Määrake kindlaks EM-i töötlemiseks vajaliku koondtabeli nimi. |
    | Dokumendi numbriväli  | Määrake väli, mis sisaldab dokumendi numbrit teie EM-i töötlemise kirjetes. |
    | Dokumendi kuupäevaväli    | Määrake väli, mis sisaldab dokumendi kuupäeva teie EM-i töötlemise kirjetes. |
    | Dokumendi kontoväli | Määrake väli, mis sisaldab dokumendi kontot teie EM-i töötlemise kirjetes. |
    | Ettevõte                | Valige allüksuse juriidilise isiku ID. |
    | Kasutaja päring             | See ruut valitakse kriteeriumide määratlemisel automaatselt, valides käsu Redigeeri **päringut**. |

3. Iga uue rea jaoks valige **käsk Redigeeri päringut** **ja määrake rea väljal Ettevõte määratud juriidilise isikuga** seotud kriteeriumid.

## <a name="web-applications"></a><a id="applications"></a>Veebirakendused

Veebirakenduse sätetega saate seadistada veebirakenduse nii, et see toetab Open Authorization (OAuth) 2.0. OAuth on avatud standard, mis võimaldab kasutajatel anda rakendusele enda nimel turvalise delegeeritud juurdepääsu identimisteavet jagamata. Samuti saate läbi teha autoriseerimisprotsessi, hankides autoriseerimiskoodi ja pääsutõendi. Veebirakenduse sätteid saate määrata lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Veebirakendused**.

Alljärgnevas tabelis kirjeldatakse lehe **Veebirakendused** välju.

| Väli                        | Kirjeldus |
|------------------------------|-------------|
| Rakenduse nimi             | Saate sisestada veebirakenduse nime. |
| Kirjeldus                  | Saate sisestada veebirakenduse kirjelduse. |
| Baas-URL                     | Saate sisestada veebirakenduse Interneti-baasaadressi. |
| Autoriseerimise URL-i tee       | Saate määrata tee, mida kasutatakse autoriseerimiseks vajaliku URL-i koostamiseks. |
| Loa URL-i tee               | Saate määrata tee, mida kasutatakse tõendi jaoks vajaliku URL-i koostamiseks. |
| Ümbersuunamis-URL                 | Saate sisestada ümbersuunamis-URL-i. |
| Kliendi ID                    | Saate sisestada veebirakenduse kliendi ID. |
| Kliendi saladus                | Saate sisestada veebirakenduse kliendi saladuse. |
| Serveri luba                 | Saate sisestada veebirakenduse serveritõendi. |
| Autoriseerimise vormingu vastendamine | Saate valida elektroonilise aruandluse vormingu, mida kasutatakse autoriseerimistaotluse loomiseks. |
| Impordi loa mudelivastendus   | Saate valida elektroonilise aruandluse importimismudeli vastenduse, mida kasutatakse pääsutõendi salvestamiseks. |
| Antud ulatus                | Rakendusetaotluste jaoks antud ulatus. Seda välja värskendatakse automaatselt. |
| Juurdepääsuloa aegumiseni on jäänud  | Pääsutõendi aegumiseni jäänud aeg. Seda välja värskendatakse automaatselt. | 
| Aktsepteerimine                       | Saate määrata veebitaotluse atribuudi **Aktsepteeri**. Näiteks sisestage **application/vnd.hmrc.1.0+json**. |
| Sisutüüp                 | Saate määrata sisu tüübi. Näiteks sisestage **application/json**. |

Peale selle on lehe **Veebirakendused** toimingupaanil saadaval järgmised nupud autoriseerimisprotsessi toetamiseks.

- **Hangi autoriseerimiskood** – veebirakenduse autoriseerimise käivitamiseks. See funktsioon kasutab autoriseerimistaotluse loomiseks **autoriseerimisvormingu vastenduse** väljal määratud ER-vormingut.
- **Hangi pääsutõend** – pääsutõendi hankimise protsessi käivitamiseks.
- **Värskenda pääsutõendit** – pääsutõendi värskendamiseks. See funktsioon kasutab ER-vormingut, mis on määratud väljal **Impordi loa mudeli vastendamine** juurdepääsu loa teabe importimiseks.

Kui süsteemi andmebaasi salvestatud veebirakenduse pääsutõend on krüptitud kujul, saab seda kasutada veebiteenusele tehtavate taotluste jaoks. Turvalisuse tagamiseks peab juurdepääs pääsutõendile olema piiratud turberollidega, mis peavad saama nende taotlustega tegeleda. Kui taotlusega püüavad tegeleda turbegruppi mittekuuluvad kasutajad, saavad nad tõrketeate, et neil pole lubatud valitud veebirakenduse kaudu tegutseda. Selleks et seadistada turberollid, millel peab olema juurdepääs pääsutõendile, kasutage kiirkaarti **Turberollid** lehel **Veebirakendused**. Kui turberolle pole veebirakenduse jaoks määratletud, saab ainult süsteemiadministraator selle veebirakenduse kaudu tegutseda.

Iga valitud veebirakendusega tegevuse puhul salvestab **tegevuslogi** kiirkaart teabe kasutaja kohta ning kuupäeva ja kellaaja.

Mõned veebiteenused võivad nõuda erinevate päiste kaasamist taotlustesse. Süsteemiadministraator saab seadistada lisapäised ja nende väärtused kiirkaardil **Lisapäised** ning kasutada neid seejärel taotluse loomise ajal.

## <a name="web-service-settings"></a><a id="settings"></a>Veebiteenuse sätted

Saate veebiteenuse sätteid kasutada otsese andmeedastuse seadistamiseks veebiteenusele. Veebirakenduse sätteid saate määrata lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Veebirakendused**.

Järgmises tabelis kirjeldatakse lehe **Veebiteenuse sätted** välju.

| Väli                          | Kirjeldus |
|--------------------------------|-------------|
| Veebiteenus                    | Saate sisestada veebiteenuse nime. |
| Kirjeldus                    | Saate sisestada veebiteenuse kirjelduse. |
| Interneti-aadress               | <p>Saate sisestada veebiteenuse Interneti-aadressi. Kui veebiteenusele on määratud veebirakendus ja veebiteenuse internetiaadress peaks olema sama, mis valitud veebirakenduse puhul määratletud aadress, valige suvand **Kopeeri baas-URL**, et kopeerida veebirakendusest pärinev baas-URL sellele väljale. Veebirakenduse baas-URL kopeeritakse seejärel sellele väljale.</p><p>**Hoiatus:** Kolmanda osapoole teenused või muud siin konfigureeritavad teenused ei vaja sertifikaati ja need ei pruugi vastata Microsofti privaatsusstandarditele. Peaksite vaatama üle iga teenuse privaatsusdokumentatsiooni ja töötama koos iga teenuse pakkujaga, et saada lisateavet teenuse pakutava vastavuse taseme kohta. Teie vastutate selle eest, et need teenused vastaksid teie turvalisusele, privaatsusele ja juriidilistele standarditele. Teenuse kasutamisega seotud risk langeb teile. Microsoft ei anna mingeid kiirgarantiisid, garantiisid ega tingimusi. Soovitame tungivalt kasutada ainult turvaliseid ja autoriseeritud ühendusi nagu näiteks HTTPS teenuseid.</p> |
| Sert                    | Saate valida eelnevalt seadistatud Azure Key Vault serdi. |
| Veebirakendus                | Saate valida eelnevalt seadistatud veebirakenduse. |
| Vastuse tüüp – XML        | Määrake selle suvandi väärtuseks **Jah**, kui vastuse tüüp on XML. |
| Päringu meetod                 | Saate määrata päringu meetodi. HTTP määrab päringu meetodite komplekti, mis näitavad toimingut, mis tuleb antud ressursiga teha. Taotlusmeetod võib olla **HANGI**, **POSTITA** või muu HTTP-meetod. |
| Päringu päised                | Saate määrata päringu päised. Taotluse päis on HTTP-päis, mida saab HTTP-päringus kasutada. See ei ole seotud teate sisuga. |
| Aktsepteerimine                         | Saate määrata veebitaotluse aktsepteerimise atribuudid. |
| Aktsepteeri kodeering                | Saate määrata aktsepteerimise kodeeringu väärtuse. Taotluse Aktsepteeri kodeering HTTP-päis reklaamib sisu kodeeringut, millest klient saab aru. See sisu kodeering on tavaliselt tihendamise algoritm. |
| Sisutüüp                   | Saate määrata sisu tüübi. Sisutüübi üksuse HTTP-päis tähistab ressursi meediumitüüpi. |
| Edukas vastuse kood       | Saate määrata HTTP olekukoodi, mis näitab, et taotlus õnnestus. |
| Taotluse päiste vorminguvastendus | Saate valida elektroonilise aruandluse vormingu, mida kasutatakse veebitaotluse päiste loomiseks. |

## <a name="message-processing-actions"></a><a id="actions"></a>Sõnumi töötlemise tegevused

Saate kasutada sõnumi töötlemise tegevusi, et luua oma protsesside jaoks tegevusi ja seadistada nende parameetreid. Saate seadistada sõnumi töötlemise tegevused lehel **Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumitöötlemise tegevused**.

Järgmistes tabelites kirjeldatakse lehel **Sõnumi töötlemise tegevused** olevaid väljasid.

### <a name="general-fasttab"></a>Kiirkaart Üldine

| Väli                                     | Kirjeldus |
|-------------------------------------------|-------------|
| Tegevuse tüüp                               | Saate valida tegevuse tüübi. Lisateavet saadaval valikute kohta vt selle artikli [jaotisest](#action-types) Teate töötlemise tegevusetüübid. |
| Vormingu vastendamine                            | Saate valida ER-i vormingu, mis tuleb tegevuse jaoks kutsuda. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimine**, **Elektroonilise aruandluse importimine** ja **Elektroonilise aruandluse eksportimissõnum**. |
| Vorminguvastendus URL-i tee jaoks               | Saate valida ER-i vormingu, mis tuleb tegevuse jaoks kutsuda. Seda vormi kasutatakse URL-aadressi tee koostamiseks, mis lisatakse valitud veebiserveri jaoks määratavale interneti baasaadressile. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus**. |
| Sõnumiüksuse tüüp                         | Saate valida kirjete tüübid, mille saamiseks tegevust tuleb hinnata. See väli on saadaval tegevuste jaoks, mille tüüp on **Sõnumiüksuse täitmise tase**, **Elektroonilise aruandluse eksportimine**, **Elektroonilise aruandluse importimine** ja **Veebiteenus** ning teised tüübid. Kui jätate selle välja tühjaks, hinnatakse kõiki sõnumiüksuse tüüpe, mis on sõnumi töötlemiseks määratletud. |
| Täidetav klass                          | Valige olemasolev täitmisklassi säte. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Sõnumi täitmise tase** ja **Sõnumiüksuse täitmise tase**. |
| Kirjete asustamise tegevus                   | Valige olemasolev asusta kirjete tegevus. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Kirjete asustamine**. |
| Veebiteenus                               | Valige olemasolev veebiteenus. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus**. |
| Saadetava faili nimi                         | Sisestage selle toiminguga saadetavale elektroonilisele teatele manuse nimi. Kui mitu manust on sama algse failinimega, saadetakse uusim manuse nimi. Kui ei leita manust, mille failil oleks määratud algne nimi, saadetakse taotlus ilma sisuta. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus**. |
| Faili nimi                                 | Saate määrata tegevuse tulemfaili nime. See fail võib olla vastus veebiserverilt või loodud aruanne. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus** ja **Elektroonilise aruandluse eksportimissõnum**. |
| Failide manustamine lähtedokumentidele          | Märkige see ruut loodud failide lisamiseks EM-üksuste viidatud koondtabeli kirjetele. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimissõnum** ja **Veebiteenus**. |
| Manusta failid väljundarhiivist üksustele | Valige see märkeruut, et ekstraktida eraldi XML-failid väljundi arhiivifailist ja lisada need vastavatele elektroonilistele teateüksustele. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksport**. |
| Sõnumiüksuste arv ekspordi kohta        | Määrake sõnumiüksuste arvu limiit, mis tuleb kaasata ühte faili (teade). See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksport**. |
| ER allika kasutamine                             | Märkige see ruut ER-i lähteparameetrite kasutamiseks importimiseks. Muul juhul kasutatakse elektroonilise teate manust. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse import**. |
| Kuva dialoog                               | Valige selle suvandi sätteks **Jah**, kui enne aruande loomist tuleb kasutajale kuvada dialoogiboks. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimissõnum**. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Sõnumi töötlemise tegevuse tüübid

Väljal **Tegevuse tüüp** on saadaval järgmised suvandid.

- **Sõnumi loomine** – kasutage seda tegevusetüüpi, et kasutajad saaksid lehel **Elektronsõnum** käsitsi sõnumeid koostada. Seda tüüpi tegevuse jaoks ei saa esialgset olekut seadistada.
- **Asusta kirjed** – see tegevuse tüüp peab juba olema häälestatud. Seostage see kirjete asustamistegevusega, mis lubab tegevuse, mis on kaasatud töötlemisse. Eeldatakse, et seda tegevusetüüpi kasutatakse kas sõnumitöötluse esimese tegevuse puhul (kui varem loodud elektronsõnumeid pole) või tegevuse puhul, millega lisatakse sõnumiüksuseid varem loodud sõnumile tegevusega, mille tegevustüüp on **Sõnumi loomine**. Seetõttu saab seda tüüpi tegevuse jaoks seadistada ainult sõnumiüksuste tulemuse oleku.Seetõttu saab seda tüüpi tegevuste puhul määrata tulemoleku ainult sõnumiüksuste puhul. Esialgse oleku saab seadistada ainult sõnumite puhul.
- **Sõnumi täitmise tase** – kasutage seda tegevusetüüpi, et seadistada täidetav klass, mida tuleb hinnata sõnumi tasemel.
- **Sõnumiüksuse täitmise tase** – kasutage seda tegevuse, et seadistada täidetav klass, mida tuleb hinnata sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimine** – kasutage seda tegevustüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval ER-i konfiguratsioonil sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimissõnum** – kasutage seda tegevusetüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval elektroonilise aruandluse konfiguratsioonil sõnumi tasemel (näiteks kui sõnumil pole sõnumiüksusi).
- **Elektroonilise aruandluse importimine** – kasutage seda tegevuse tüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb imporditaval elektroonilise aruandluse konfiguratsioonil.
- **Kasutaja töötlemine sõnumi tasemel** – kasutage seda tegevusetüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab tegema mõne käsitsi tegevuse sõnumi tasemel. Näiteks võib kasutaja uuendada sõnumite olekut.
- **Kasutaja töötlemine** – kasutage seda tegevusetüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab tegema mõne käsitsi tegevuse sõnumiüksuse tasemel. Näiteks võib kasutaja uuendada sõnumiüksuste olekut.
- **Veebiteenus** – kasutage seda tegevusetüüpi tegevuste jaoks, mis peavad loodud aruande edastama veebiteenusele. Seda tegevuse tüüpi ei kasutata itaalia ostu- ja müügiarvete suhtluse aruandluse jaoks. Selle tegevustüübi puhul **Sõnumi töötlemise tegevuse** leht sisaldab **Mitmesugused üksikasjad** kiirkaarti, kus saate määrata kinnitusteksti. See kinnitustekst kuvatakse kasutajatele enne valitud veebiteenusele tehtud taotlusega tegelemist.
- **Kinnituse taotlemine** – kasutage seda tegevusetüüpi kinnituse taotlemiseks serverist.

### <a name="initial-statuses-fasttab"></a>Kiirkaart Algolekud

> [!NOTE]
> Kiirkaart **Algolekud** pole saadaval tegevuste jaoks, mille esialgne tegevusetüüp on **Sõnumi loomine**.

| Väli               | Kirjeldus |
|---------------------|-------------|
| Sõnumiüksuse olek | Saate valida sõnumiüksuse oleku, mille saamiseks valitud sõnumi töötlemise tegevust tuleb hinnata. |
| Kirjeldus         | Valitud sõnumiüksuse oleku kirjeldus. |

### <a name="result-statuses-fasttab"></a>Kiirkaart Tulemi olekud

| Väli               | Kirjeldus |
|---------------------|-------------|
| Teate olek      | Saate valida sõnumite olekud, mille saamiseks valitud sõnumi töötlemise tegevust tuleb hinnata. See väli on saadaval ainult sõnumi töötlemise tegevuse jaoks, mida hinnatakse sõnumi tasemel. Näiteks on see saadaval tegevustele tüübiga **Elektroonilise aruandluse eksportimine** ja **Elektroonilise aruandluse importimine**, kuid see pole saadaval tegevustele tüübiga **Kasutaja töötlemine** ja **Sõnumiüksuse täitmistase**. |
| Kirjeldus         | Valitud sõnumi oleku kirjeldus. |
| Vastuse tüüp       | Valitud sõnumi oleku vastuse tüüp. |
| Sõnumiüksuse olek | Saate valida tulemuseks saavad olekud, mis peaksid olema saadaval pärast seda, kui valitud sõnumi töötlemise tegevus on hinnatud. See väli on saadaval ainult sõnumi töötlemise tegevuse jaoks, mida hinnatakse sõnumiüksuse tasemel. Näiteks on see saadaval tegevuste jaoks, mille tüüp on **Kasutaja töötlemine** ja **Sõnumiüksuse käivitamise tase**. Sõnumi töötlemise tegevuste jaoks, mida hinnatakse sõnumi tasemel, kuvab see väli sõnumiüksuse oleku, mis seadistati valitud sõnumi oleku jaoks. |

Järgmises tabelis on näidatud tulemolekud, mis tuleb seadistada eri tegevusetüüpidele ja vastusetüüpidele.

| Elektronsõnumi tegevusetüüp / vastusetüüp | Täitmine õnnestus | Äritõrge | Tehniline tõrge | Kasutaja määratud | Loobu |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Loo sõnum                               | X                     |                |                 |              |        |
| Elektroonilise aruandluse eksportimine                  | X                     |                |                 |              |        |
| Elektroonilise aruandluse importimine                  |                       |                |                 |              |        |
| Veebiteenus                                  | X                     |                | X               |              |        |
| Kasutaja töötlemine                              |                       |                |                 |              |        |
| Sõnumi käivitamise tase                      |                       |                |                 |              |        |
| Asustamiskirjed                             |                       |                |                 |              |        |
| Sõnumiüksuse käivitamise tase                 |                       |                |                 |              |        |
| Päringu kinnitamine                         | X                     | X              | X               |              |        |
| Elektroonilise aruandluse eksportimissõnum          | X                     |                |                 |              |        |
| Kasutaja töötlemine sõnumi tasemel                |                       |                |                 |              |        |

## <a name="electronic-message-processing"></a><a id="processing"></a>Elektronsõnumi töötlemine

Elektronsõnumi töötlemine on elektronsõnumite funktsiooni põhikontseptsioon. See koondab tegevused, mida tuleb elektronsõnumi saamiseks hinnata. Tegevusi saab siduda esialgse oleku ja tulemuse oleku kaudu. Teise võimalusena saab tüübiga **Kasutaja töötlemine** tegevusi alustada sõltumatult. Elektrooniliste sõnumite töötlemise seadistamiseks minge **Maks** \> **Seadistamine** \> **Elektroonilised teated** \> **Elektrooniliste teadete töötlus**.

Kiirkaart **Tegevus** võimaldab teil töötlemisele lisada eelmääratletud tegevusi. Saate määrata, kas tegevus peab käivitama eraldi või kas selle saab käivitada töötlemisega. Selleks et määrata, et töötlemisel saab tegevuse käivitada ainult kasutaja, valige selle tegevuse puhul välja **Käivita eraldi** sätteks **Jah**. Kui tegevus tuleb käivitada, töödeldes sõnumeid või sõnumiüksusi, mis on tegevuse algse olekuna määratletud olekus, valige välja **Käivita eraldi** sätteks **Ei**. Tegevused tüübiga **Kasutaja tegevus** tuleb alati eraldi käivitada.

Mõnikord tuleb mitu tegevust koondada järjekorda, isegi kui esimene tegevus on seadistatud nii, et see käivitub eraldi. Näiteks peab kasutaja käivitama aruande loomise. Siiski peab kasutaja käivitama aruande loomise, kuid kohe pärast aruande loomist tuleb see saata veebiteenusele ja süsteemis tuleb kajastada veebiteenusest saadud vastust. Sel juhul saate luua eraldamatu jada tegevustele, mis tuleb käivitada alati koos. Valige kiirkaardil **Tegevus** ruudustiku kohal suvand **Eraldamatud jadad** ja looge jada. Seejärel valige kõigi tegevuste jaoks, mis tuleb koos käivitada, jada väljal **Eraldamatu jada**. Sellisel juhul saab jada esimese tegevuse puhul valida välja **Käivita eraldi** sätteks **Jah**, kuid kõigi teiste tegevuste puhul **Ei**.

**Elektroonilise aruandluse ekspordi** ja **elektroonilise aruandluse ekspordi sõnumite** tüüpide tegevused käitavad sisendparameetreid omava ER-vormingu. Kui teie elektrooniline sõnumitöötlus sisaldab ükskõik kumma tüübi tegevusi, peate enne aruande genereerimist määratlema sisendparameetrite väärtused. Sel viisil saab süsteem kasutada aruande loomiseks pakktöötlust. Saate valida ruudustikust ülalpool **parameetrid**, et seadistada parameetrid valitud tegevusetüübile (**elektroonilise aruandluse eksport** või **elektroonilise aruandluse eksporditeate**). Märkige **Kasuta parameetreid** ruut tegevuse puhul, mida tuleb pakett-töö käitamisel kasutada määratud parameetritega.

Kasuta **Sõnumiüksuse lisaväljad** kiirkaarti, mis võimaldab teil lisada eelmääratletud lisavälju, mis on seotud sõnumiüksustega. Peata lisama lisaväljad iga sõnumiüksuse tüübi jaoks, millega väljad on seotud. Saate määrata vaikeväärtuse, mis määratakse töötlemise ajal lisaväljale.

Kasutage **Sõnumi lisaväljad** kiirkaarti mis võimaldab teil lisada eelmääratletud lisavälju, mis on seotud sõnumitega. Saate määrata vaikeväärtuse, mis määratakse töötlemise ajal lisaväljale.

Kasutage **Turberollid** kiirkaarti mis võimaldab teil seadistada turberolle, mis on süsteemis eelmääratletud spetsiifilise töötlemise jaoks. Kasutajad, kellel on kindel roll, näevad ainult töötlemist, mis on määratletud selle rolli jaoks.

Kiirkaart **Partii** võimaldab teil seadistada töötlemist partiirežiimis. Soovitatav on seadistada pakktöötlus otse **elektrooniliste teadete** või **elektrooniliste teadete üksuste** lehel töötlemiseks, kui valite **Käivita töötlemine** toimingupaanil et alustada töötlemist.
