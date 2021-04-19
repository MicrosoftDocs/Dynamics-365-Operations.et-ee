---
title: Kulude automaatne häälestus
description: Selles teema kirjeldatakse, kuidas häälestada kulureeglid erinevatele sissetulevate teekondade tasemetele. Nende reeglite alusel arvutab süsteem kulud ja lisab need automaatselt. Seetõttu ei pea kasutajad kulusid käsitsi lisama.
author: sherry-zheng
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2e9135019323db74a4dca9343d315cbbf9683e32
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841955"
---
# <a name="auto-costs-setup"></a>Kulude automaatne häälestus

[!include [banner](../../includes/banner.md)]

Saate kasutada lehte **Automaatsed kulud**, et häälestada kulureeglid erinevatele kulualadele (nt teekonnad, saatmiskonteinerid, fooliod, ostutellimused, kaubad või üleviimistellimuse read). Süsteem arvutab kulud ja lisab need automaatselt reeglite ja kasutajate valitud väljade põhjal, kui nad loovad kirjeid ühe kuluala kohta. Seetõttu ei pea kasutajad kulusid käsitsi lisama.

Automaatsete kuludega töötamiseks valige **Väljalaadimiskulu \> Kuluarvutuse häälestamine \> Automaatsed kulud**. Seejärel häälestage oma automaatsete kulude reeglid nii, nagu on kirjeldatud selles teemas.

## <a name="work-with-cost-areas"></a>Kulualade kasutamine

Automaatsed kulud toimivad nagu kaubanduslepped või automaatsed lisakulud. Iga automaatse kulu kirje kuulub konkreetsele kulutasemele. Kasutage lehe **Automaatsed kulud** loendipaanil välja **Kuluala**, et valida kuluala, mida soovite kasutada. Loendipaanil kuvatakse ainult automaatsed kulud, mis kuuluvad praegu valitud kulualale. Kõik teie loodavad automaatsed kulud kuuluvad praegu valitud kulualale.

Kulualad võimaldavad süsteemil jaotada kulusid kuluala ostutellimuse ridade vahel. Näiteks ühe saatmiskonteineri kulu puhul jagatakse see väärtus kõigi selles saatmiskonteineris olevate toodete vahel. Kui konteinereid on kaks või enam, saab iga saatmiskonteineri puhul määrata sama kulutüübi. Seetõttu saab konteineri tüüpi kasutada õige automaatse kulu leidmiseks.

## <a name="buttons-on-the-action-pane"></a>Toimingupaani nupud

Järgmises tabelis kirjeldatakse lehe **Automaatsed kulud** toimingupaanil olevaid nuppe.

| Nupp | Kirjeldus |
|---|---|
| Redigeeri | Saate redigeerida olemasolevat automaatset kulu. |
| New | Saate luua automaatse kulu. |
| Kustutamine | Saate kustutada automaatse kulu. |
| Kopeerimise lähtekoht | Saate luua olemasoleva kirje põhjal uue automaatse kulu kirje. Seejärel saate uut kirjet vabalt redigeerida. See nupp aitab teil kiiresti luua uusi automaatseid kulusid. |
| Dimensioonide kuvamine | Avage dialoogiboks, kus saate valida varude dimensioonid, mis kuvatakse teie kuvatavate kulukannete kohta. Kui tühjendate märkeruudud, kuvatakse kulukannete kohta vähem varude dimensioone. Seetõttu kuvatakse kande kohta vähem üksikasju. Kui automaatsele kulule on määratud varude dimensioon, rakendatakse automaatne kulu ainult siis, kui määratud varude dimensiooni kasutatakse teekonnal oleva kauba puhul. |

## <a name="settings-on-the-header"></a>Päises olevad sätted

Päisejaotises olevate sätete kombinatsioon määrab, millal ja kuidas konkreetne automaatne kulu teekonnale lisatakse. Automaatne kulu rakendatakse teekonnale, saatmiskonteinerile või fooliole ainult siis, kui automaatse kulu üksikasjad ühtivad selle kuluala päise üksikasjadega. Kõigi vastendatud automaatsete kulude summa määrab teekonna hinnangulise väljamineva kulu. See kulu jaotatakse kõigi laeval või teekonnal olevate kaupade vahel.

Järgmises tabelis kirjeldatakse kõiki välju, mida võidakse päises kuvada. Saadaolevad konkreetsed väljad varieeruvad siiski sõltuvalt kulualast ja neis kuvatakse praegu valitud dimensioonid.

| Field | Kirjeldus |
|---|---|
| **Konto kood** | <p>Valige üks järgmistest väärtustest.</p><ul><li>**Tabel** – kulureegel rakendub ainult konkreetsele hankijale.</li><li>**Grupp** – kulureegel rakendub konkreetsele hankijate grupile. Süsteem otsib hankija kirjega seostatud [hankija kulutüübi gruppi](costing-parameters-setup.md).</li><li>**Kõik** – kulureegel rakendub kõigile hankijatele. |
| **Saatmisettevõte** | Valige hankija või hankijate grupp, millele kulureegel rakendub. See väli on saadaval ainult juhul, kui teete väljal **Konto kood** valiku *Tabel* või *Grupp*. |
| **Tollimaakler** | Valige hankija või hankijate grupp, millele kulureegel rakendub. See väli on saadaval ainult juhul, kui teete väljal **Konto kood** valiku *Tabel* või *Grupp*. |
| **Kauba kood** | <p>Valige üks järgmistest väärtustest.</p><ul><li>**Tabel** – kulureegel rakendub ainult konkreetsele kaubale.</li><li>**Grupp** – kulureegel rakendub konkreetsele kaubagrupile. Süsteem otsib kauba kirjega seostatud [kauba kulutüübi gruppi](costing-parameters-setup.md).</li><li>**Kõik** – kulureegel rakendub kõigile kaupadele.|
| **Kauba seos** | Valige kaup või kaubagrupp, millele kulureegel rakendub. See väli on saadaval ainult juhul, kui teete väljal **Kauba kood** valiku *Tabel* või *Grupp*. |
| **Tarneviis** | Valige tarneviis (nt õhu- või meretransport), millele kulureegel rakendub. |
| **Konteineri tüüp** | Saatmiskonteineri tüüp, milles kaubad saadetakse. Automaatset kulu saab teekonnale rakendada ainult juhul, kui konteineri tüüp, mille automaatse kulu häälestus vastab teekonna konteineritüübile. |
| **Sadamast** ja **Sadamani** | Teekonna lähte- („kust”) ja sihtsadam („kuhu”). (Mõnedel saatmiskonteineritel võivad olla erinevad „kuhu”-sadamad, sest teekond võib kulgeda läbi mitme sadama.) Automaatse kulu saab teekonnale rakendada ainult siis, kui automaatse kulu häälestuse „kust”- ja „kuhu”-sadamad vastavad teekonna „kust”- ja „kuhu”-sadamatele. |
| **Automaatse kulu number** | Automaatse kulu reegli kordumatu identifikaator. Selle välja väärtus luuakse automaatselt lehel **Väljamineva kulu parameetrid** häälestatud numbriseeria alusel. |
| **Varude dimensioonid** | Mõned kulualad lasevad teil päisesse kaasata ühe või mitu kaubadimensiooni (nt suurus, värv, ladu ja partii number). Valige toimingupaanil üksus **Kuva dimensioonid**, et valida kaasatavad dimensioonid. |

## <a name="settings-on-the-lines-fasttab"></a>Kiirkaardi Read sätted

Kiirkaardil **Read** lisage rida iga valuuta kohta, mida saab kasutada, kui kulu rakendatakse teekonnal ostutellimuse reale. 

Kaupade ja ostutellimuste puhul vastendab süsteem iga ostutellimuse rea valuutad kiirkaardil **Read** määratud valuutadega. See rakendub ainult vastavale reale või kaubale seatud kuluväärtusele. Kui rea või kauba valuuta jaoks pole ühtegi rida häälestatud, ei rakendata automaatset kulu sellele reale või kaubale.

Muude kulualade tüüpide puhul rakenduvad kõik kiirkaardil **Read** olevad read igale teekonnale, saatmiskonteinerile, fooliole või üleviimistellimuse reale, mis vastab päises määratud väärtustele.

Järgmises tabelis kirjeldatakse kõiki välju, mida võidakse igal real kuvada. Saadaolevad konkreetsed väljad varieeruvad siiski sõltuvalt praegu valitud kulualast.

| Field | Kirjeldus |
|---|---|
| **Currency** | Saate valida valuuta, millele rida rakendub. See valuuta on seotud ostutellimusega. Kui süsteem püüab leida automaatseid kulusid, mida tuleks rakendada teekonnale ja selle teekonnaridadele, valib see rea, mille valuuta on sama, mis ostutellimusel. See väli on saadaval ainult siis, kui välja **Kuluala** väärtuseks on seatud *Ostutellimus* või *Kaup*. |
| **Kulutüübi kood** | Kulu tüüp. |
| **Jaotamismeetod** | <p>Meetod, mida kasutatakse kulude jaotamiseks ridadele. Valikud on järgmised:</p><ul><li><p>**Protsent** – välja **Kuluväärtus** väärtus on protsent, mida rakendatakse kaupade koguväärtusele.</p><p>Näiteks kui välja **Kuluväärtus** väärtuseks on seatud *10* ja kaupade koguväärtus 800 $, on kuluväärtus 80 $ (= 800 $ × 10 protsenti).</p></li><li>**Kogus** – kulu jaotatakse kaupade koguse alusel.</li><li>**Summa** – kulu jaotatakse kaupade väärtuse alusel.</li><li>**Maht** – kulu jaotatakse kaupade mahu alusel. Maht on määratud kauba põhiandmetes.</li><li>**Kaal** – kulu jaotatakse kaupade kaalu alusel. Kaal on määratud kauba põhiandmetes.</li><li>**Mahuline** – kulu jaotatakse kaupade mahumõõdu alusel.</li><li><p>**Mõõt** – see valik võimaldab mõõdu määrata moodulis **Väljalaadimiskulu**. Seda kasutavad tihti organisatsioonid, kes ei tea kaupade individuaalset mahtu või kaalu, kuid nõuavad täpsemat jaotust, kui valikud **Summa** ja **Kogus** võimaldavad. Ekspediitor või agent pakub organisatsioonile kaalu või mahu (kuupmeetrites) mõõtmist kas kauba või ostutellimuse tasemel.</p><p>Näiteks meretransport on 900 $. Kauba A kaal on 800 kilogrammi (kg) ja maht 2 kuupmeetrit (m³). Kauba B kaal on 100 kg ja maht 1 m³. Siin on tulemused, kui kulud jaotatakse kaalu järgi:</p><ul><li>Kaup A = 800 $</li><li>Kaup B = 100 $</li></ul><p>Siin on tulemused, kui kulud jaotatakse mahu järgi:</p><ul><li>Kaup A = 600 $</li><li>Kaup B = 300 $</li></ul><p>**Märkus:** kui välja **Jaotusmeetod** väärtuseks on seatud *Mõõt*, kasutab süsteem mõõte, mis on sisestatud nii kuluala (saatmiskonteiner) kui ka ridade kohta. Nende mõõtude liitmine ei pea tingimata andma oodatud koguväärtust. Kui aga nende eeldatava koguväärtuse saavutamine on nõutav, saate kogumõõdu ülevaatamiseks teha statistika abil kontrolli. Mõõtmisviiba säte ja mõõdu automaatne uuendamine saadetise või konteineri tasemel häälestatakse teekonna päises.</p></li></ul> |
| **Alates kuupäevast** | Saate määrata kuluarvutuse kuupäevavahemiku alguse, kui kuupäevade vahemik on olemas. See on esimene kuupäev, mil automaatne kulu rakendub. |
| **Kuupäevani** | Saate määrata kuluarvutuse kuupäevavahemiku lõpu, kui kuupäevade vahemik on olemas. See on viimane kuupäev, mil automaatne kulu rakendub. |
| **Kategooria** | <p>Saate valida kulu arvutamiseks kasutatava meetodi. Valikud on järgmised:</p><ul><li>**Fikseeritud** – kulu jaotatakse jaotusmeetodi alusel.</li><li>**Tükid** – kulu eraldatakse tüki kohta. Seetõttu jaotusmeetodit ei asutata.</li><li>**Protsent** – lisatakse protsent kaupade väärtusest. Seetõttu jaotusmeetodit ei asutata.</li><li>**Määr** – valige see suvand, kui on olemas kogusejaotused. Rea väli **Jaotusmeetod** peab olema seatud väärtusele *Mõõt*.</li><ul> |
| **Koguse alusel jaotatud** | <p>Valige see märkeruut, et teha nupp **Kogusejaotused** kättesaadavaks kiirkaardil **Read**. Kogusejaotused võimaldavad kulude jaotamist ja erinevate kulude varieerumist sõltuvalt teekonna ostutellimuse rea kogusest. Seda funktsiooni kasutatakse sageli siis, kui tarneviis on õhutransport. Rea väli **Kategooria** peab olema seatud väärtusele *Määr*.</p><p>Kogus, mis on seotud väljal **Jaotusmeetod** tehtud valikuga. Kuluväärtus on kuni väljale **Kuluväärtus** sisestatud koguseni.<p>Näiteks annavad kogused 45–100 kg iga mõõdu (nt kg/m³) kohta tasu 6,00 $. Üle 100 kg kogused annavad iga mõõdu (nt kg/m³) kohta tasu 5,50 $.</p> |
| **Omahind** | Sisestage kulu väärtus. |
| **Kulu valuutakood** | Valige kulu valuuta. |
| **Kauba käibemaksugrupp** | Valige kulu maksukood. |
| **Minimaalne kulu** | <p>See väli kehtib ainult siis, kui valitud on märkeruut **Koguse järgi jaotatud**. Kui mõõt ei jõua selle väärtuseni, valitakse minimaalne väärtus, sõltumata lehel **Kogusejaotused** määratud kuludest.<p>Näiteks annavad kogused 0–45 kg iga mõõdu (kg/m³) kohta tasu 6 $. Kogused 46–100 kg annavad iga mõõdu (kg/m³) kohta tasu 5,50 $. Kui saadetakse 2 kg, loob kogusejaotus kuluväärtuse 12 $. Kui aga väli **Miinimumkulu** väärtuseks seatakse *100 $*, on lõppkulu 100 $.</p> |
| **Agregaat** | Märkige see ruut, et lubada kasutajatel teisaldada see kulu saatmiskonteineri tasemelt teekonna tasemele. Sel juhul saab kulusid automaatselt arvutada saatmiskonteineri tasemel. Kuid neid saab siiski kombineerida ja jaotada ka kõigi kaupade vahel teekonna kõigis konteinerites, selle asemel et jaotada seda kõigile konkreetses saatmiskonteineris olevatele kaupadele. |
| **Seostatud kulutüüp** | <p>Linkige praegune rida teise reaga samas automaatses kulukirjes, määrates väärtuse **Kulutüübi kood** sellele reale, millega soovite linkida. See funktsioon on saadaval ainult siis, kui praeguse rea välja **Kategooria** väärtuseks on seatud *Protsent*. Kui praegune rida on lingitud mõne teise reaga, põhineb praeguse rea kulu selle teise rea kulul.</p><p>Veokulud võivad olla näiteks 1000 $ ning te soovite, et kütuse lisatasu oleks 10 protsenti veokuludest. Sel juhul peab rea välja **Kategooria** väärtus olema *Protsent*, välja **Kuluväärtus** väärtus *10%* ja välja **Lingitud kulu tüüp** väärtus *Veos*.</p> |
| **Väärtuse korrigeerimine** ja **Korrigeerimissumma** | <p>Kasutage neid välju, et korrigeerida erinevate protsendiväärtuste väärtust ja summat. Need on saadaval ainult siis, kui välja **Kuluala** väärtuseks on seatud *Kaup*.</p><p>Kauba erinevate komponentide jaoks saab häälestada erineva kuluarvutuse. Ühel kaubakomponendil võib olla selle kauba muudest komponentidest erinev kuluprotsent. Mõnikord on selline lähenemine vajalik kauba teatud osa väärtuse leidmiseks erinevate määrade juures.</p><p>Näiteks kella tollimaksu arvutamiseks kasutatakse kahte määra: ühel komponendil on 10-protsendine tollimaksumäär ja teisel komponendil on 2-protsendiline tollimaksumäär. Sel juhul tükeldatakse kuluarvutus nende kahe komponendi vahel.</p><p>Kauba kulu arvutatakse välja, kuid kuluväärtust korrigeeritakse erineva kulukategooriaga komponentide väärtusega. Ülejäänud komponentide kulu saab seejärel arvutada summa abil, mille võrra eelmist arvutust korrigeeriti.</p><p>Näiteks on kella komponendi A kulu 9,50 $ ja tollimaks 10 protsenti ning komponendi B kulu 0,50 $ ja tollimaks 2 protsenti. Seetõttu on kogukulu 10,00 $. Esimene kirje on 10-protsendise rea kohta. Sellel kasutatakse järgmisi väärtusi:</p><ul><li>**Kategooria:** *Protsent*</li><li>**Kulu väärtus:** *10*</li><li>**Väärtuse korrigeerimine:** *Korrigeerimisalus*</li><li>**Korrigeeritud väärtus:** *-0,50*</li></ul><p>See häälestus määrab, et kauba kulu (10 $) tuleb vähendada 0,50 $ (komponendi B hind) võrra, enne kui 10-protsendiline tollimaks arvutatakse. Seetõttu rakendatakse 10-protsendiline maksumäär väärtusele 9,50 $.</p><p>Teine kirje on 2-protsendilise rea kohta (0,50 $, mille võrra eelmist kirjet korrigeeriti). Sellel kasutatakse järgmisi väärtusi:</p><ul><li>**Kategooria:** *Protsent*</li><li>**Kulu väärtus:** *2*</li><li>**Väärtuse korrigeerimine:** *Kasuta*</li><li>**Korrigeerimine:** *0,50*</li></ul><p>Selle häälestuse korral arvutatakse ülejäänud tollimaks, mis tuleb tasuda komponendi B kohta.</p> |
