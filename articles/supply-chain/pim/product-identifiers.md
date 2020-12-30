---
title: Toote identifikaatorid
description: Selles teemas kirjeldatakse erinevaid toote identifikaatoreid ja kirjeldatakse, kuidas lisada toote identifikaatoreid toote andmetesse.
author: cvocph
manager: tfehr
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: c16818f1dc52c9e21130539213e7e8d1053fef1d
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529182"
---
# <a name="product-identifiers"></a>Toote identifikaatorid

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse erinevaid toote identifikaatoreid ja kirjeldatakse, kuidas lisada toote identifikaatoreid toote andmetesse.

Kui töötate rakenduses Microsoft Dynamics ERP või Microsoft Dynamics CRM kaupluses või laos olevate toodetega, peab teil nende toodete ja tootevariantide tuvastamiseks olema hea strateegia.

## <a name="unique-product-numberproduct-id"></a>Kordumatu tootenumber / toote ID

Rakenduses Dynamics 365 Supply Chain Management on toote peamine identifikaator tootenumber (ehk toote kordumatu ID). Selle numbri saab lasta numbriseerial automaatselt luua või tootega käsitsi siduda. Tootevariantide jaoks saab numbrid määratleda tootenomenklatuuri malli kaudu.

Paljudel juhtudel pole tootenumber algselt loodud rakenduses Dynamics 365 Supply Chain Management. Selle asemel on see seotud tootega toote elutsükli halduse (PLM) süsteemis või toote teabehalduse (PDM) süsteemis. Sel juhul saate toodete ja tootevariantide importimiseks kasutada andmeüksuseid. Tarneahela haldus kasutab seejärel kõigi operatsioonide numbreid.

Kui juurutate rakendust Tarneahela haldus, peaksite pöörama erilist tähelepanu oma tootenumbrite strateegiale. Hea nummerdamissüsteem parandab logistikavoogusid ja aitab vältida vigu. Hea toote identifikaator sisaldab kuni 15 tähemärki. Ideaaljuhul sisaldab see vähem kui 10 tähemärki ja kuni viis liigitavat tähemärki. Samuti saate kiirotsingute lubamiseks kasutada otsingunimesid. Otsingunimi on täiendav nimi, mis tähistab toote klassifikatsioone.

Kui kasutate Common Data Service, siis on ka toote number Tarneahela halduses ka toote number Common Data Service-is. Tootevariandid sünkroonitakse Common Data Service-iga eristatavate toodetena.

## <a name="item-number-and-product-dimensions"></a>Kaubakood ja tootedimensioonid

Kaubakood on toote identifikaator, mida kasutab kindel juriidiline isik. Ideaalis peaks kaubakood olema sama, mis tootenumber. Kui nomenklatuur erineb juriidilise isiku kohta, muutub toote jälgimine tarneahelas keeruliseks ja kaasnevad koormavad ümbermärgistamise ja viitamise protsessid. Ühilduvuse tagamiseks vanemate versioonidega (st rakendustega Microsoft Dynamics AX 2009 ja varasematega) säilitasime selle mudeli. Kuid soovitame siiski alati eemaldada identifikaatorid, mis on seotud juriidiliste isikutega, ja kasutada selle asemel peamise identifikaatorina kordumatut tootenumbrit.

Peale selle ei saa tootevarianti kaubakoodi järgi kordumatult tuvastada. See nõuab alati kaubakoodi ja kõiki tooteetalonis määratletud tootedimensioonide kombinatsiooni. See nõue võib muutuda kohmakaks ja aeglustada tuvastamise protsessi. Soovitame ka seepärast võimaluse korral alati kaubakoodi asemel kasutada kordumatut tootenumbrit.

Paljudel lehtedel on endiselt peamiste identifikaatoritena märgitud tootekood ja tootedimensioonid. Kuid tootenumbreid saab kasutada otsinguteks. Jaotises **Müük ja turundus** &gt; **Häälestus** &gt; **Otsing** &gt; **Otsinguparameetrid** saate muuta otsingut nii, et see kasutaks peamise otsingustrateegiana kaubakoodide asemel tootenumbreid. Kui seate suvandi **Tooteotsingu lubamine** väärtuseks **Jah**, kuvab otsing lisaks tooteetalonidele ka tootevariandid. Lisateavet vt teemast [Toodete ja tootevariantide otsimine tellimuse sisestamise käigus](search-products-product-variants.md).

Peale selle saate otsida ja filtreerida tootenumbrit, toote nime ja kirjeldust ning tootevariandi tootedimensiooni ID-sid. Kui valite variandi, valitakse ka seotud tootekood ja kõik tootedimensiooni ID-d. Nii on õige variandi leidmine ja valimine lihtsam. Selle sätte kasutamine on soovitatav, kui kasutate toodete peamiste identifikaatoritena tootevariante ja kordumatuid tootenumbreid. Ainsaks erandiks võib olla moetööstus, kus äriprotsesside korral on tihti vaja, et peate esmalt valima etaloni ja siis variandi. Enne nummerdamissüsteemi juurutamist hinnake hoolikalt seda suvandit.

> [!NOTE]
> Selle toote kaubakoodi ei saa muuta, kui selle toote puhul on olemas üks või rohkem kandeid.

## <a name="product-name-and-description"></a>Toote nimi ja kirjeldus

Toote nimi ja kirjeldus on toote identifikaatorid, mida näevad inimesed ja mida saab esitada mitmes keeles. Vaikimisi kuvab rakenduse Tarneahela haldus klient kogu tooteteabe ettevõtte vaikekeeles, mitte kasutaja keeles. Kuid suhtluses klientide ja hankijatega kasutatakse tõlgitud tootenimesid ja kirjeldusi. Tõlked põhinevad kliendi ja hankija kontode keelekoodil.

Tootevariantide jaoks saab tootenimesid luua tootenomenklatuuri malli kaudu. Kuna tootenimed ei pea olema kordumatud, võite leida mitu sama nimega toodet.

## <a name="product-and-item-search-names"></a>Toote ja kauba otsingunimed

Tarneahela haldus pakub toodete ja kaupade (väljastatud tooted) jaoks teisest otsingunime. See otsingunimi ei pea olema kordumatu ja seda saab pärast toote või tootevariandi loomist muuta. Soovitame kasutada otsingunime toodete otsimiseks kategooriate kaupa. Otsingunimed võimaldavad kasutada kiirotsinguid, eriti müügi ja ostu protsessides.

Otsingunimi võib sisaldada ka kliendi või hankija toote ID-d või mõnda muud välist toote ID-d, kui see väline ID on toote peamine otsingukriteerium.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Välised tooteidentifikaatorid (kliendi ja hankija identifikaatorid)

Väljastatud toodete jaoks saate hallata kaubakoode, kauba nimesid ja kauba kirjeldusi, mida klient või hankija kasutab. Viited kuvatakse välistel dokumentidel, nagu müügitellimused, ostutellimused, saatelehed ja arved. Rakenduse Tarneahela haldus praeguses versioonis ei kuvata väliseid viiteid põhitoimingute lehtedel. Ainsaks erandiks on hankija kaubakood. See number kuvatakse dialoogiboksis **Tooteteave**, kui väljastatud toote jaoks on määratud vaikehankija.

Saate hallata väliseid toote identifikaatoreid väljastatud toote, väljastatud tootevariandi, kliendi või kliendigrupi või hankija või hankijagrupi kaupa.

Lehel **Väljastatud tooted** tehke üht järgmistest.

- Klientide jaoks valige vahekaardil **Müük** grupis **Seostuv teave** suvand **Väline kaubakirjeldus**.
- Hankijate jaoks valige vahekaardil **Ost** grupis **Seostuv teave** suvand **Väline kaubakirjeldus**.

Lehel **Välised kaubakirjeldused** saate seostada kliendi või hankija kaubakoodi väljastatud tootega. See seos tuleb luua iga juriidilise isiku jaoks. Järgmist teavet saab salvestada. Kahjuks on sildid rakenduse Tarneahela haldus praeguses versioonis veidi eksitavad. Kuid neid silte võidakse tulevases versioonis muuta.

| Väli | Vastav klienditeave | Vastav hankijateave |
|-------|------------------------------------|----------------------------------|
| Väline kaubakood | Kliendi kaubakood | Hankija kaubakood |
| Kirjeldus | Nimi, mille klient seostab kaubaga | Nimi, mille hankija seostab kaubaga |
| Väline kaubatekst | Kliendi kauba kirjeldus | Hankija kauba kirjeldus |

Kui paljud kliendid või hankijad kasutavad samu kaubakoode (näiteks ostuseose või kaubandusgrupi korral), saate luua kliendi- või hankijagruppe, et lihtsustada välise tooteteabe haldamist.

- Kliendigruppide jaoks avage **Müük** &gt; **Häälestus** &gt; **Kaubad** &gt; **Väline kaubakirjeldus**, et luua ja hallata gruppe ning seotud kaubakoode. Klientide seostamiseks grupiga avage **Müügireskontro** &gt; **Kliendid** &gt; **Kõik kliendid** ja seejärel määrake väärtus kiirkaardi **Müügitellimuse vaikeandmed** väljal **Kaup – kliendigrupp**.
- Hankijagruppide jaoks avage **Hanked** &gt; **Häälestus** &gt; **Väline kaubakirjelduse grupp**, et luua ja hallata gruppe ning seotud kaubakoode. Hankijate seostamiseks grupiga avage **Ostureskontro** &gt; **Hankijad** &gt; **Kõik hankijad** ja seejärel määrake väärtus kiirkaardi **Ostutellimuse vaikeandmed** väljal **Kaup – hankijagrupp**.
 
## <a name="bar-codes"></a>Vöötkoodid

Kui soovite toodete tuvastamiseks kasutada vöötkoodiskannerit, peab toote identifikaator vastama kasutatava vöötkoodistandardi nõuetele. Seetõttu ei sisalda vöötkoodid tavaliselt mitte toote algnumbrit, vaid numbrit, mis luuakse spetsiaalselt valitud vöötkooditehnoloogia jaoks. Saate mitut vöötkoodi hallata vöötkoodi tüübi järgi. Saate isegi seostada sama vöötkoodi mitme tootega ja seejärel vöötkoodi skannimisel valida tegeliku aktiivse seose.

Enne vöötkoodide määratlemist saate määratleda ühe või mitu vöötkoodi häälestust. Vöötkoodi häälestused aitavad kinnitada, et vöötkoodid järgivad nõutud juhised ja et seetõttu saab neid tõhusalt printida ja skannida. Saate hallata ka erilisi vöötkoode konkreetsete tootekoguste jaoks.

Soovitame kasutada vöötkoodi häälestust kaubanduses kasutatavate kaubakoodide (GTIN) või rahvusvaheliste tootekoodide (EAN) haldamiseks.

Vöötkoodide haldamiseks valige lehel **Väljastatud tooted** vahekaardil **Halda varusid** grupis **Ladu** suvand **Vöötkoodid**.

## <a name="gtin-codes"></a>GTIN-koodid

e-Commerce’is on oluline, et kõik osapooled räägiksid ühist keelt ja viitaksid toodetele ühist identifikaatorite kogumit kasutades. Seetõttu tuginevad mõned tööstusharud süsteemile [GTIN](https://www.gs1.org/id-keys/gtin), mis on globaalne kaubakoodide süsteem, mida pakub GS1.

Soovitame GTIN säilitada kui vöötkood. Kuid saate seda hallata ka lehel **Kaup – GTIN**. Selle lehe avamiseks valige lehel **Väljastatud tooted** vahekaardil **Halda varusid** grupis **Ladu** suvand **GTIN-koodid**. Pange tähele, et GTIN-i ei hallata globaalse numbrina. Selle asemel haldab seda juriidiline isik.

Rakenduses Tarneahela haldus saate laotoimingutes määratleda pakendamisvariandid, määrates kindlad mõõtühikud. Näiteks võib kaup olla ladustatud tükkidena, kuueste komplektidena, 18 kaupa sisaldavate alustena või täis kaubaalustena. Iga pakendamisvariandi jaoks määratletakse kindel mõõtühik. Kuna GTIN on tavaliselt seotud toote pakendamisüksusega, saate lehel **Kaup – GTIN** hallata erinevaid GTIN-koode toote ja mõõtühiku kohta. Siiski ei saa te sama GTIN-koodi kasutada juriidilise isiku erinevate kaupade või tootevariantide jaoks rohkem kui üks kord.

**GTIN-koodide** haldamiseks valige lehel **Väljastatud tooted** vahekaardil **Halda varusid** grupis **Ladu** suvand **GTIN**.

## <a name="external-codes"></a>Välised koodid

Mitmele üksusele saab määrata väliskoode. Näiteks saate määratleda väliseid koode toodete ja väljastatud toodete tuvastamiseks. Neid väliseid koode saab kasutada statistiliste koodide või maksukoodide seostamiseks väljastatud toodete ja väljastatud tootevariantidega. Väliseid koode määratletakse juriidilise isiku ja koodi tüübi järgi. Neil peab olema kordumatu juriidiline isik, koodi tüüp ja tabeli viide.

Kahjuks pole standardfunktsiooni, mis võimaldaks tooteid otsida väliste koodide järgi.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Tooteidentifikaatorite importimiseks ja eksportimiseks kasutatavad andmeüksused

| Üksuse nimi | Identifikaatorite importimine | Identifikaatorite eksportimine | Kommentaarid |
|-------------|--------------------|--------------------|----------|
| Tooted V2 | Tootenumber, toote otsingunimi, toote nimi, toote kirjeldus | Tootenumber, toote otsingunimi, toote nimi, toote kirjeldus | Olenevalt üksuse sätetest ja tootenumbri numbriseeriast saab tootenumbri luua automaatselt importimise ajal. |
| Tootevariandid | Tootenumber, toote otsingunimi, toote nimi, toote kirjeldus | Tootenumber, toote otsingunimi, toote nimi, toote kirjeldus | Olenevalt tootenomenklatuuri mallist saab toote numbri luua automaatselt importimise ajal. Kuid saate importida mis tahes kordumatu tootenumbri ja see tootenumber ei pea järgima tootenomenklatuuri mallide struktuuri. |
| Toote tõlked | Toote nimi, toote kirjeldus | Toote nimi, toote kirjeldus | See üksus alistab iga keele. Pange tähele, et kui juriidilise isiku esmase keele nimi või kirjeldus alistatakse, muutub toote nimi ja kirjeldus. |
| Väljastatud toote loomine V2 | Kaubakood, tootenumber, kauba otsingunimi| Kaubakood, tootenumber, kauba otsingunimi, toote otsingunimi, toote nimi | See üksus võib olla väljakutse, kui uute väljastatud toodete loomise ajal kasutatakse numbriseeriaid. Seda mõjutavad nii **kaubakoodi** numbriseeria kui ka **tootenumbri** numbriseeria. Kuid **kaubakoodi** numbriseeria kehtib juriidilise isiku kohta, samal ajal kui **tootenumbri** numbriseeria on globaalne. Seetõttu pole soovitatav uute väljastatud toodete juurutamisel kasutada **kaubakoodi** numbriseeriat. Kui üksust kasutatakse olemasoleva toote väljastamiseks, tuleb üksuses esitada tootenumber. Lisateavet vaadake selle teema jaotisest „Toote ja kauba numbriseeriad”. |
| Väljastatud tootevariandid | Kaubakood, tootedimensioonid, tootenumber | Tootenumber, toote otsingunimi, toote nimi, toote kirjeldus, tootedimensioonid | Sarnaselt **tootevariantide** üksusele saab ka seda üksust kasutada uute toodete loomiseks, mis järgivad variandi jaoks tootenomenklatuuri malli või kasutavad enda tootenumbreid. |
| Klientide väline kaubakirjeldus | Kliendi kaubakood, kliendi kauba nimi, kliendi kirjeldus, kliendi konto | Kliendi kaubakood, kliendi kauba nimi, kliendi kirjeldus, kliendi konto | Klientide gruppi (näiteks ostjaseos) saab koondada ühte gruppi, kasutades üksust **Välise kaubakirjelduse kliendigrupid**. |
| Hankijate väline kaubakirjeldus | Hankija kaubakood, hankija kauba nimi, hankija kirjeldus, hankija konto | Hankija kaubakood, hankija kauba nimi, hankija kirjeldus, hankija konto | Hankijate gruppi (näiteks müügiseos või tööstusorganisatsioon) saab koondada ühte gruppi, kasutades üksust **Välise kaubakirjelduse hankijagrupid**. |
| Kauba vöötkood | Vöötkood | Vöötkood | Pange tähele, et importimise ajal peate viitama vöötkoodi häälestusele, mis on määratletud sihtsüsteemis. Imporditud vöötkoodiviiteid kontrollitakse selle vöötkoodi häälestuse suhtes ja need lükatakse tagasi, kui vöötkoodid ei vasta selles vöötkoodi häälestuses määratletud nõuetele. |
| Väljastatud toodete väliskoodid | Väline kood | Väline kood, väliskoodi klassid, kaubakood | Välised koodid on esitatud juriidilise isiku alusel. Importimiseks peate viitama määratletud koodiklassile. Importige koodiklassid, kasutades üksust **Väljastatud toodete väliskoodi klassid**. |
| Väljastatud toodevariantide väliskoodid | Väline kood | Väline kood, väliskoodi klassid, kaubakood, tootedimensioonid | Välised koodid on esitatud juriidilise isiku alusel. Importimiseks peate viitama määratletud koodiklassile. Importige koodiklassid, kasutades üksust **Väljastatud toodete väliskoodi klassid**. See üksus viitab tootevariantidele kaubakoodi ja tootedimensioonide alusel. |
| Väljastatud tootevariantide välised koodid tootenumbri identifikaatori järgi | Väline kood | Väline kood, väliskoodi klassid, tootenumber | Välised koodid on esitatud juriidilise isiku alusel. Importimiseks peate viitama määratletud koodiklassile. Importige koodiklassid, kasutades üksust **Väljastatud toodete väliskoodi klassid**. See üksus viitab tootevariantidele variandi tootenumbri järgi. (Alates järgmisest peamisest väljalaskest) |
| GTIN | Pole kohaldatav | Pole kohaldatav | Praegu pole ühtegi kindlat üksust, mida kasutatakse GTIN-koodide importimiseks ja eksportimiseks. Soovitame kasutada üksust **Kauba vöötkood**. |
| Tooteüksuse common data service’i identifikaatori üksus | Pole kohaldatav | Kaubakood, kauba otsingunimi, toote otsingunimi, hankija kaubakood, kliendi kaubakood, välised koodid, GTIN-koodid, vöötkoodid | See üksus konsolideerib kõik identifikaatorid ühte andmemudelisse, et kõigi identifikaatorite ja nende seotud tüüpide eksportimiseks saaks kasutada ühte liidest. Kasutage üksust **Tooteüksuse identifitseerimiskood**, et eksportida identifitseerimiskoodid ja kirjeldused. Kasutage üksust **Tooteüksuse identifikaatori ulatus**, et eksportida identifikaatorisse täiendavat ulatuse teavet, nagu osapool, juriidiline isik, kogus või ühik. |

### <a name="product-and-item-number-sequences"></a>Toote ja kauba numbriseeriad

Saate määratleda kaks erinevat numbriseeriat:

- Numbriseeria **Tootenumber** globaalse tootenumbri jaoks.
- Numbriseeria **Kaubakood** juriidilise isiku kohta kehtiva kaubakoodi jaoks.

> [!NOTE]
> Kasutage kaubakoodi eraldi identifikaatorina ainult siis, kui migreerite erinevaid juriidilisi isikuid erinevatest allikatest, millel olid erinevad nummerdamissüsteemid. Proovige alati kasutada toote identifikaatorit, mis on kõigis juriidilistes isikutes kordumatu. Seetõttu peaksite numbriseeria **Kaubakood** jaoks suvandi **Käsitsi** väärtuseks määrama **Jah**. Sel viisil järgib kaubakood loomisel tootenumbrit. Kui Supply Chain Management ei ole uute tootenumbrite jaoks juhtiv süsteem, peaksite suvandi **Käsitsi** väärtuseks määrama **Jah** nii numbriseeria **Kaubakood** kui ka **Tootenumber** korral.

Kui kasutate toodete loomiseks üksust **Väljastatud toote loomine V2**, võivad mitu sätet mõjutada seda, kuidas numbriseeriaid kasutatakse tootenumbri ja kaubakoodi loomiseks:

- numbriseeria **Tootenumber** sätted;
- numbriseeria **Kaubakood** sätted;
- kaubakoodi vastendamine; 
- tootenumbri vastendamine.

Järgmine tabel annab ülevaate importimise ja käsitsi loomise tulemustest, kui kasutatakse numbriseeria ja välja vastendamise sätete kindlat kombinatsiooni.

| Tootenumbri numbriseeria | Kaubakoodi numbriseeria | Kaubakoodi vastendamine | Tootenumbri vastendamine | Üksuse importimise tulemus | Käsitsi loomise tulemus | Lõppsõna |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Käsitsi = ei | Käsitsi = ei | Vastendamist pole. | Vastendamist pole. | Tootenumbrid kasutavad numbriseeriat **Tootenumber**. Kaubakoodid kasutavad numbriseeriat **Kaubakood**. | Tootenumbrid kasutavad numbriseeriat **Tootenumber**. Kaubakoodid kasutavad numbriseeriat **Kaubakood**. | Selle konfiguratsiooniga järgivad tootenumbrid tootenumbri seeriat ja kaubakoodid järgivad kaubakoodi seeriat. Kuid see konfiguratsioon ei tööta siis, kui imporditakse rohkem kui üks üksus (rida). |
| Käsitsi = ei | Käsitsi = jah | Automaatne loomine | Vastendamist pole. | Nii tootenumbrid kui ka kaubakoodid kasutavad numbriseeriat **Kaubakood**. | Nii tootenumbrid kui ka kaubakoodid kasutavad numbriseeriat **Tootenumber**. | Nii tootenumbrid kui ka kaubakoodid järgivad tootenumbri seeriat. See on soovitatav viis hulgitoodete importimiseks väljastatud toote loomise V2 andmeüksusega. |
| Käsitsi = ei | Käsitsi = jah | Vastendamist pole. | Vastendamist pole. | Nii tootenumbrid kui ka kaubakoodid kasutavad numbriseeriat **Tootenumber**. | Nii tootenumbrid kui ka kaubakoodid kasutavad numbriseeriat **Tootenumber**. | Nii tootenumbrid kui ka kaubakoodid kasutavad tootenumbri seeriat. Kuid see konfiguratsioon ei tööta siis, kui imporditakse rohkem kui üks üksus (rida). |
| Käsitsi = jah | Pole kohaldatav | Pole kohaldatav | Automaatne loomine | Saate järgmise tõrketeate: „Numbriseeriat ei saa tuvastada.” | Numbriseeria **Kaubakood** kohaselt | Seda sätet ei saa importida. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Tooteüksuse identifikaator (kõigi tooteidentifikaatorite eksportimine)

Tooteüksuse identifikaatori mudel loodi selleks, et lubada CDS-i versiooni 1.0 ettevalmistamist kõigi identifikaatoritega, mida kasutatakse tootele viitamiseks. Ülesande lihtsustamiseks koondatakse kõik identifikaatorid ühte globaalsesse identifikaatorite tabelisse, et neid saaks eksportida ühe mudelina. Pange tähele, et CDS-i see versioon ei kasutada tooteidentifikaatorite mudelit. Seetõttu on üksuse **Tooteüksuse common data service’i identifikaatori üksus** ja selle protsessi praktilisus piiratud ja see võib tulevikus muutuda.

Tooteidentifikaatorite tabel on globaalne tabel, kuhu lisatakse korduva pakett-töö kaudu andmeid kõigist peamise juriidilise isiku viitetabelitest. Peate globaalse tooteetaloni ulatuse määratlusena valima juriidilise isiku ja tootekategooria hierarhia. Globaalse tooteidentifikaatorite tabeli loomine on piiratud toodetega, mis on väljastatud valitud juriidilisse isikusse, ja toodetega, mis on tootekategooria hierarhias oleva rolli **common data service'i** jaoks valitud tootehierarhia liikmed.

See protsess eeldab, et toote koondandmeid hallatakse peamiselt ühes keskses juriidilises isikus. (Kuid see juriidiline isik võib olla virtuaalne juriidiline isik, mida kasutatakse ainult globaalsete koondandmete haldamiseks.)

Keskkonna konfigureerimiseks tehke järgmist.

1. Valige CDS-i jaoks kategooriahierarhia. Kui lehel **Kategooriahierarhia rolli seosed** pole rolliga **common data service** seostatud ühtegi hierarhiat, peate looma uue seose. Valige roll **common data service** ja seejärel seostage kategooriahierarhia, mis esindab tooteportfooliot, mis tuleb CDS-iga sünkroonida.
2. Valige globaalsete toote koondandmete jaoks juriidiline isik. Lehel **Tooteteabe halduse parameetrid** vahekaardil **Toote atribuudid** valige peaettevõte, kus toote ja kauba identifikaatoreid peamiselt hallatakse.
3. Määratlege identifitseerimiskoodide tüübid ja koodid, mis tuleb eksportida. Avage **Tooteteabe haldus** &gt; **Häälestus** &gt; **Toote identifitseerimiskoodid**. Identifitseerimiskoodide tüüpide loomiseks valige **Loo koodid**. Koodi tüübi kirje luuakse iga identifikaatoritüübi jaoks, mis leitakse valitud juriidilisest isikust.

    Pange tähele, et vöötkoodide korral luuakse koodi tüüp iga vöötkoodi häälestuse jaoks. Väliste koodide korral luuakse koodi tüüp iga väliskoodi klassi jaoks.

    Nüüd saate hallata kooditüüpide loendit. Saate muuta koodi, nime ja kirjeldust. Saate ka kooditüüpe kustutada. Kustutatud kooditüüpe ei kasutata globaalse tooteüksuste identifikaatorite tabelite täitmiseks.

4. Kui olete lõpetanud tooteidentifikaatori kooditüüpide määratlemise, saate luua identifikaatoreid globaalses tabelis, käivitades lehel **Tooteüksuse identifitseerimiskoodid** töö **Tooteüksuse identifikaatorite loomine**. See töö tuleks käivitada pakett-tööna. See töö tuleks seadistada perioodilise pakett-tööna, et tabelit täidetaks uute kirjete kohaselt.

Nüüd saate kasutada andmeüksuseid **Tooteüksuse common data service’i identifikaatori üksus**, **Tooteüksuse identifitseerimiskood** ja **Tooteüksuse identifikaatori ulatus**, et eksportida identifikaatoreid mis tahes sihtsüsteemi jaoks.

## <a name="related-topic"></a>Seotud teema

[Toodete ja tootevariantide otsimine tellimuse sisestamise käigus](search-products-product-variants.md)
