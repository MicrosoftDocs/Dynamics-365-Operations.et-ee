---
title: Väljalaadimiskulu parameetrite seadistus
description: See teema kirjeldab, kuidas seadistada üldteavet ja konfiguratsioonisätteid, mida kasutatakse kogu moodulis Väljalaadimiskulu teabe sisestamise, olekuvärskenduste, numbriseeriate ja käitumise jaoks.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 489c0db50d52c1e58eab73ad19a73babf22b4de7
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500762"
---
# <a name="landed-cost-parameters-setup"></a>Väljalaadimiskulu parameetrite seadistus

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Te kasutate lehte **Väljalaadimiskulu parameetrid** selleks, et seadistada üldteavet ja konfiguratsioonisätteid, mida kasutatakse kogu moodulis **Väljalaadimiskulu** teabe sisestamise, olekuvärskenduste, numbriseeriate ja käitumise jaoks. Parameetrite seadistus on juriidiliste isikute jaoks ühine ja administraator saab seda muuta.

## <a name="open-the-landed-cost-parameters-page"></a>Lehe Väljalaadimiskulu parameetrid avamine

Parameetritega töötamiseks avage **Väljalaadimiskulu \> Seadistus \> Väljalaadimiskulu parameetrid** ja seejärel seadke väljad järgmistes jaotistes kirjeldatud viisil.

![Väljalaadimiskulu parameetrite leht](media/landed-cost-parameters.png "Väljalaadimiskulu parameetrite leht")

## <a name="general-tab"></a>Vahekaart Üldine

### <a name="general-fasttab"></a>Kiirkaart Üldine

Järgmine tabel kirjeldab väljasid, mis on saadaval lehe **Väljalaadimiskulu parameetrid** vahekaardi **Üldine** kiirkaardil **Üldine**.

| Sätted | Kirjeldus |
|---|---|
| Kasuta saatmiskurssi | Saatmiskurss seatakse määratud perioodiks ja seda kasutatakse mitut valuutat kasutatavate kaupade kulude prognoosimiseks. Saatmiskursi kasutamiseks määrake suvandi väärtuseks *Jah*. |
| Vahetuskursi tüüp | Vahetuskursside vaikekogum, mida kasutatakse reisi ja reisikulude mitme valuutaga arvutusteks. |
| Uuenda ostutellimuse kogust | Valige, mis juhtub, kui kasutaja muudab ostutellimuse real kogust.<ul><li>**Aktsepteeri** – reisi kogust korrigeeritakse automaatselt.</li><li>**Hoiatus** – kui rida on seotud reisiga, kuvatakse hoiatus, kuid reisi kogus värskendatakse.</li><li>**Tõrge** – kui rida on seotud reisiga, kuvatakse tõrketeade ja ostutellimust ei saa värskendada. Seetõttu tuleb tellimuse rida esmalt reisist eemaldada.</li></ul> |
| Uuenda pakkide arv automaatselt | Kui suvandi väärtuseks on seatud *Jah*, liidetakse kõik pakid kokku ning kuvatakse reisi- ja konteineritasemel. Kui väärtuseks on seatud *Ei*, seatakse pakkide arvuks algselt 0 (null) ja seda saab vajaduse korral käsitsi redigeerida. |

### <a name="costing-fasttab"></a>Kiirkaart Kuluarvutus

Järgmine tabel kirjeldab väljasid, mis on saadaval lehe **Väljalaadimiskulu parameetrid** vahekaardi **Üldine** kiirkaardil **Kuluarvutus**.

| Sätted | Kirjeldus |
|---|---|
| Sisestamistäpsustus | Valige pearaamatus väärtuse korrigeerimine.<ul><li>**Kokku** – pearaamatusse sisestatakse kogusumma.</li><li>**Kaubagrupp** – korrigeerimine määratakse kaubagrupi kohta.</li><li>**Kauba number** – korrigeerimine määratakse kauba kohta. See väärtus on kõige üksikasjalikum.</li></ul> |
| Luba nullkulud | Seadke suvandi väärtuseks *Ei*, et kuvada tõrge, kui kasutaja püüab sisestada reisiarve või ostutellimuse kuluhinnangu, mis ei sisalda eeldatava reisikulu väärtust. Tõrketeade teatab, et 0 (null) kulu ei saa eraldada ja et arve sisestamine nurjub. Sellisel juhul saab kasutaja hinnangut käsitsi uuendada (või automaatse kulu ümber konfigureerida) ja seejärel sisestada värskendatud väärtuse või kustutada kulu, kui see ei rakendu.<p>Seadke suvandi väärtuseks *Jah*, et lubada reisi kulu tühjaks jätta. Sellisel juhul eraldatakse hind 0 (null) vastavalt kulualale. Seejärel saab hankija kuluarvet reisi vastuvõtmisel töödelda nullhinnaga kulu suhtes.</p><p>Soovitame teil konfigureerida automaatsel kulukirje hinnangu, et vältida nullhinnaga kulu kuvamist. Kuigi see hinnang pole täiesti täpne, peaks see siiski olema täpsem kui eeldatav nullkulu.</p> |
| Korrigeerimise sisestuskuupäev | Ostureskontro reisikulu arve sisestamisel värskendatakse ka tasakaalustuste tabelit (varude korrigeerimised). Valige kuupäev, mis on seatakse lehel **Reisikulude valimine** vaikimisi, kui olete arve töölehel.<ul><li>**Kande kuupäev** – kasutage töölehe kuupäeva (sisestuskuupäev).</li><li>**Ostutellimuse arve kuupäev** – kasutage laoarve (ostutellimuse) finantsteabe sisestuskuupäeva.</li><li>**Valitud kuupäev** – kasutaja saab määrata sisestuskuupäeva. Ehkki kuupäeva saab tühjaks jätta, siis juhul, kui see on kuluarve sisestamisel endiselt tühi, kuvatakse kasutajale tõrge.</li></ul> |
| Kasuta ostuarve kannet | Kui seada selle suvandi väärtuseks *Jah*, kasutavad kulude tekkepõhised kanded sama kandenumbrit, mida kasutatakse ostuarve jaoks. Kui väärtuseks on seatud *Ei*, kasutab süsteem järgmist saadaolevat numbrit numbriseeriast **Kulude tekkepõhine kanne**, mis on seadistatud lehe **Väljalaadimiskulu parameetrid** vahekaardil **Numbriseeriad**.<p>Sellel suvandil on mõju ainult siis, kui suvandi **Sisesta pearaamatu kulude kontole** väärtuseks on seatud *Jah* vahekaardil **Arve**, mis asub lehel **Ostureskontro parameetrid**.</p> |
| Blokeeri käsitsi sisestamine kliiringukontole | Seadke suvandi väärtuseks *Jah*, et vältida kliiringukontodele sisestamist, kui kannet ei ole reisiga seostatud, valides hankijaarve töölehe toimingupaanil **Funktsioonid \> Vali reisikulud**. Soovitame seada selle suvandi väärtuseks *Jah*, et reisi ja kliiringukonto saaks õigesti tasakaalustada. |
| Kasuta kulutüübi tasu juurdekasvukontot | Kui selle suvandi väärtuseks on seatud *Jah*, konfigureeritakse kulude tekkepõhiseks arvestamiseks tasu juurdekasvukonto asjakohase kulutüübi koodi jaoks lehel **Kulutüübi koodid**.<p>Sellel suvandil on mõju ainult siis, kui suvandi **Sisesta pearaamatu kulude kontole** väärtuseks on seatud *Jah* vahekaardil **Arve**, mis asub lehel **Ostureskontro parameetrid**. |
| Sadama korrigeerimised hälbena | Kui selle suvandi väärtuseks on seatud *Jah*, alistab see standardfunktsiooni ja sunnib eeldatavate kulude ja tegelike kulude hälvetega seotud varude korrigeerimiskannete sisestamise häblekontole.<p>Kui selle suvandi väärtuseks on seatud *Ei*, töödeldakse hälvetega seotud varude korrigeerimiskandeid kularvutusumeetodi ja kulutüübi koodi konfiguratsiooni alusel. Standardkulu korral sisestatakse hälbed endiselt hälbekontole. Libiseva kaalutud keskmise (WMA) korral sisestatakse hälbed hälbekontole või varudesse.</p><p>Sellel suvandil on mõju ainult siis, kui suvandi **Sisesta pearaamatu kulude kontole** väärtuseks on seatud *Jah* vahekaardil **Arve**, mis asub lehel **Ostureskontro parameetrid**.</p> |

### <a name="validation-fasttab"></a>Kiirkaart Kinnitamine

Järgmine tabel kirjeldab väljasid, mis on saadaval lehe **Väljalaadimiskulu parameetrid** vahekaardi **Üldine** kiirkaardil **Kinnitamine**.

| Sätted | Kirjeldus |
|---|---|
| Mitu kuluarvet | Valige, mis juhtub, kui reisi, foolio või konteineri suhtes töödeldakse sama lisatasu jaoks üle ühe arve.<ul><li>**Aktsepteeri** – süsteemil tuleb mitu kuluarvet lubada.</li><li>**Hoiatus** – kuvatakse hoiatus.</li><li>**Tõrge** – näidatakse tõrketeadet.</li></ul> |
| Mitu hankijat foolio kohta | Valige, mis juhtub, kui fooliosse lisatakse üle ühe hankija ostutellimuse.<ul><li>**Aktsepteeri** – süsteemil tuleb tegevus lubada.</li><li>**Hoiatus** – kuvatakse hoiatus, kuid tegevust saab siiski teha.</li><li>**Tõrge** – kuvatakse tõrketeade ja tegevust takistatakse.</li></ul><p>Teie tollimaakler või kohalikud seadused võivad olla määranud selle välja jaoks kindla väärtuse.</p> |
| Mitme tarnemeetodi lubatud kõikumine | Valige, mis juhtub, kui reisile lisatakse kaubad ostutellimusest, mis kasutab reisi omast erinevat tarnemeetodit.<ul><li>**Aktsepteeri** – süsteemil tuleb tegevus lubada.</li><li>**Hoiatus** – kuvatakse hoiatus, kuid tegevust saab siiski teha.</li><li>**Tõrge** – kuvatakse tõrketeade ja tegevust takistatakse.</li></ul> |
| Mitme lao lubatud kõikumine | Valige, mis juhtub, kui reis sisaldab mitut tellimuserida, mis tuleb tarnida eri ladudesse. Need tellimuseread võivad olla jaotatud ühe või mitme ostutellimuse vahel.<ul><li>**Aktsepteeri** – süsteemil tuleb tegevus lubada.</li><li>**Hoiatus** – kuvatakse hoiatus.</li><li>**Tõrge** – näidatakse tõrketeadet.</li></ul> |
| Mahuteave on puudu | Valige, mis juhtub, kui kasutaja lisab reisile ilma mahuta kauba.<ul><li>**Aktsepteeri** – süsteemil tuleb kaup aktsepteerida.</li><li>**Hoiatus** – kuvatakse hoiatus.</li><li>**Tõrge** – näidatakse tõrketeadet.</li></ul><p>Kui mahte kasutatakse kulude arvutamiseks ja jaotamiseks, soovitame teha valiku *Hoiatus* või *Tõrge*.</p> |
| Teenuste pakkuja ilma reisikuluta | Valige, mis juhtub, kui kasutaja püüab töödelda reisiga seostamata teenusepakkuja arvet. <ul><li>**Aktsepteeri** – süsteemil tuleb tegevus lubada.</li><li>**Hoiatus** – kuvatakse hoiatus.</li><li>**Tõrge** – näidatakse tõrketeadet.</li></ul><p>Soovitame teha valiku *Hoiatus*.</p> |

### <a name="defaults-fasttab"></a>Kiirkaart Vaikesätted

Järgmine tabel kirjeldab väljasid, mis on saadaval lehe **Väljalaadimiskulu parameetrid** vahekaardi **Üldine** kiirkaardil **Vaikesätted**.

| Sätted | Kirjeldus |
|---|---|
| Töölehe nimi | Valige vaiketööleht, mida funktsioon *Loo saabumistööleht* peab kasutama. |
| Reisi olek | Valige olek, mis reisil peab olema enne, kui kasutajad saavad süsteemis selle jaoks üüritud saatmiskonteineri seadistada. See tegevus tehakse tavaliselt siis, kui kaubad on transiidis või dokis. |
| Teekonna mall | Valige vaiketeekonnamall, mida kasutada uute üüritud saatmiskonteinerite jaoks. Tavaliselt valite teekonnamalli, mis sisaldab üürikulusid. |
| Liikumine | Liikumise tööleht töödeldakse automaatselt, kui tarne üle-/alakogus jääb määratud kõikumise piiresse. Valige kasutamiseks vaikeliikumistööleht. Valitud liikumise töölehe nime väli **Vastaskonto** peab sisaldama väärtust. |
| Ülekanne | Alatarne töötlemisel kantakse vähendatud sissetulekukogus üle alatarnelattu. Valige kasutamiseks vaikeülekandmistööleht. |
| Keela ostutellimused, mis pole seotud reisiga | Lülitage reisiga seostamata ostutellimuste jaoks välja väljalaadimiskulu üle-/alatarne funktsioon. |
| Keela ostutellimused, mis pole transiidis olevate kaupade ostutellimused | Lülitage transiidis olevate kaupade funktsiooni mittekasutavate ostutellimuste jaoks välja väljalaadimiskulu üle-/alatarne funktsioon. |
| Transiidis olevad kaubad: liigse vastuvõtu ajapikenduse periood | Määrake päevade arv pärast saatmiskonteineri esimest sissetulekut, mille jooksul saab selle saatmiskonteineri jaoks veel täiendavaid ülesissetulekuid lõpule viia. |

## <a name="status-updates-tab"></a>Vahekaart Olekuvärskendused

Süsteem kasutab olekuväärtusi, et tähistada iga reisi olekut. Reisi olekuväärtusi saab reisidele automaatselt rakendada reisi jälgimise või perioodiliste pakett-tööde kaudu. Alternatiivina saate need käsitsi rakendada, kui avate reisi ja valite oleku toimingupaani vahekaardi **Halda** grupis **Reisi värskendamine**. 

Saate luua nii palju reisi olekuväärtusi, kui soovite. Kuid neli neist peavad olema lehe **Väljalaadimiskulu parameetrid** vahekaardil **Olekuvärskendused** määratud eriotstarbel kasutamiseks. Järgmises tabelis on kirjeldatud seal saadaolevaid välju.

| Sätted | Kirjeldus |
|---|---|
| Arvutatud kulu | Valige reisi olek, mis näitab, et reis on lõpule viidud. |
| Transiidis | Valige reisi olek, mis näitab, et reis on transiidis. |
| Kuluarvutuse jaoks valmis | Valige reisi olek, mis näitab, et reis on kuluarvutuseks valmis. Seda olekut kasutatakse siis, kui reisi jaoks on töödeldud kõik varude ostuarved ja reisi kuluarved, mille korral on välja **Krediteeri reisikulusse** väärtuseks seatud *Hankija*. Reisid, mille korral kuluarvutusprotsess nurjub, tähistatakse olekuga *Kuluarvutuseks jaoks valmis*.|
| Eelnevalt arvutatud kulu | Valige reisi olek, mis näitab, et reisi eelkuluarvutus on pooleli. Seda olekut kasutatakse siis, kui uus kulukanne lisatakse reisile pärast seda, kui selle jaoks on kuluarvutus juba tehtud. Uusi kulukandeid võidakse lisada olemasoleva kuluarvutusega reisile teise veoarve või ootamatu üleseisutrahvitasu vastuvõtmise korral. See olek rakendatakse automaatselt, kui kuluarvutusega reisile lisatakse uus reisikulu. |

## <a name="voyage-creator-tab"></a>Vahekaart Reisilooja

Järgmises tabelis kirjeldatakse lehe **Väljalaadimiskulu parameetrid** vahekaardi **Reisilooja** jaotisi.

| Lõik | Kirjeldus |
|---|---|
| Lubatud kõikumised | Väljad **Lubatud mahukõikumine** ja **Lubatud kaalukõikumine** määravad läved, mida ületavad kaubad loetakse ülemahulisteks ja ülekaalulisteks. Kui kasutaja lisab kaubad lehel **Reisilooja** ning maht või kaal ületab siin seatud väärtuse, kuvab süsteem hoiatuse. Iga välja väärtust väljendatakse vastava saatmiskonteineritüübi jaoks seatud maksimummahu või -kaalu protsendina. Soovitame väärtust, mis on vahemikus 5–10 protsenti maksimummahust või -kaalust. |
| Foolio loomise häälestamine | Süsteem saab reisi loomise käigus luua mitu fooliot. Määrake selles jaotises, millal tuleb luua uus foolio. Iga selle jaotise rea korral kontrollib süsteem määratud tabelit ja välja ning loob foolio iga kordumatu väljaväärtuse jaoks. |

## <a name="cost-estimates-tab"></a>Vahekaart Kuluhinnangud

Lehe **Väljalaadimiskulu parameetrid** vahekaart **Kuluhinnangud** sisaldab ainult ühte välja: **Kuluarvutuse vaikeversioon**. See väli rakendub ainult juhul, kui kuluarvutusmeetod on *Standardne kuluarvutus*. Valige kuluarvutuse vaikeversioon, mida kasutada perioodilises ülesanded *Kauba omahinna uuendus*. Võimalik, et peate seda sätet muutma iga kord, kui algab uus majandusaasta.

## <a name="inventory-dimensions-tab"></a>Vahekaart Varude dimensioonid

Kasutate vahekaarti **Varude dimensioonid** lehel **Väljalaadimiskulu parameetrid**, et kontrollida, milliseid saadaolevaid varude dimensioone tuleks vaikimisi kuvada igal mooduli Väljalaadimiskulu lehel, kus dimensioone kasutatakse.

Valige dimensioon ja seejärel määrake suvandi **Reisi read**, **Transiidis olevad kaubad** ja/või **Kuluhinnangud** väärtuseks *Jah* iga lehe korral, kus see dimensioon tuleks vaikimisi kuvada. Korrake seda toimingut vastavalt vajadusele teiste dimensioonide jaoks.

Selle vahekaardi sätted kehtestavad vaikedimensioonid igale määratud lehele kõigi juriidiliste isikute lõikes. Kuid kasutajad, kes töötavad määratud lehtedel, saavad vaikedimensioonid alistada, kui teevad toimingupaanil valiku **Varud \> Kuva dimensioonid**.

## <a name="number-sequences-tab"></a>Vahekaart Numbriseeriad

Lehe **Väljalaadimiskulu parameetrid** vahekaardil **Numbriseeriad** on loetletud kõik viitenumbriseeria tüübid, mida nõuab moodul Väljalaadimiskulu, kuid mis ei ole juriidiliste isikute jaoks ühised. Iga loendis oleva viite jaoks valige numbriseeria kood.

> [!NOTE]
> Mitme ettevõttega konfiguratsioonis tuleb igale ettevõttele (juriidilisele isikule) luua erinevad numbriseeriad.

## <a name="shared-number-sequences-tab"></a>Vahekaart Ühiskasutatud numbriseeriad

Lehe **Väljalaadimiskulu parameetrid** vahekaardil **Ühiskasutatud numbriseeriad** on loetletud kõik viitenumbriseeria tüübid, mis on moodulis Väljalaadimiskulu juriidiliste isikute jaoks ühised. Praegu on loendis ainult üks numbriseeria. Seda numbriseeriat kasutatakse reisi ID jaoks.

Lehel **Kõik reisid** saavad kasutajad vaadata kõiki reise kõigi juriidiliste isikute lõikes. Kuid reisi redigeerimiseks ja töötlemiseks peavad kasutajad olema valitud kirje juriidilises isikus.

## <a name="feature-visibility-tab"></a>Vahekaart Funktsioonide nähtavus

Väljalaadimiskulu lisab funktsioone (välju ja funktsioone) mitmele lahenduses Microsoft Dynamics 365 Supply Chain Management sageli kasutatavale lehele. Need lehed sisaldavad lehti, mis on seotud hankija koondandmetega, väljastatud toodetega, ostutellimustega, üleviimistellimustega ja laoseadistusega. Väljalaadimiskulu kasutamise korral peate need funktsioonid enne nende kasutamist kõigi jaoks nähtavaks tegema. Kui te ei kasuta Väljalaadimiskulu, saate soovi korral funktsioonid peita.

Väljalaadimiskulu saadaolevate funktsioonide nähtavaks tegemiseks seadke lehe **Väljalaadimiskulu parameetrid** vahekaardil **Funktsioonide nähtavus** suvandi **Aktiveeri** väärtuseks *Jah*. Seadke väärtuseks *Ei*, et peita funktsioonid tavalehtedel väljaspool Väljalaadimiskulu. Ent isegi siis, kui suvandi väärtuseks on seatud *Ei*, jääb moodul ise, sh leht **Väljalaadimiskulu parameetrid**, kättesaadavaks kasutajatele, kellel on sellele juurdepääsemiseks vajalikud load.
