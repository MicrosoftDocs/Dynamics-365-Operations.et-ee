---
title: Väliskataloogi häälestamine e-hanke väljaregistreerimiseks
description: Selles teemas kirjeldatakse välise kataloogi või väljaregistreeritava kataloogi kasutamist hankijalt hinnapakkumise teabe kogumiseks ja selle lisamiseks ostutaotlusele.
author: RichardLuan
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchVendorPortalRequests, CatExternalCatalogConfiguration, CatCXMLCartLogList
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f6e551f9d3d181674595e945bf1fb4c62a70ed5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016373"
---
# <a name="set-up-an-external-catalog-for-punchout-e-procurement"></a>Väliskataloogi häälestamine e-hanke väljaregistreerimiseks

[!include [banner](../includes/banner.md)]

Välist kataloogi kasutades saate tagada, et toote ja hinna teave, mida hiljem rakenduses Supply Chain Management töötlete, on täpne ning ajakohane. Seejärel saab ostutaotluse kinnitada ja teisendada ostutellimuseks ning hankijale saab tellimuse esitada.

Kui väline kataloog on seadistatud ja töötaja koostab ostutaotlust, on olemas võimalus ümbersuunamiseks välisele saidile, välisesse kataloogi ja naasta välisel saidil loodud ostukorvi. See suhtlus põhineb cXML-protokollil ja see tuleb seadistada ostu- ja müügiorganisatsiooni süsteemide vahel.

Suhtluse seadistamiseks peab teie hankija andma teabeühikud, mida saate kasutada sellise välise kataloogi konfiguratsioonis nagu identiteet, ostja ettevõtte domeen, nt DUNS ja DUNS-i number, identimisteave ja URL, mille kaudu hankija kataloogi minna.

## <a name="setting-up-an-external-catalog"></a>Välise kataloogi seadistamine

Väline kataloog peaks võimaldama suunata ostutaotlusse siseneva töötaja toodete valimiseks ümber välisele saidile. Tooted, mille töötaja välisest kataloogist valib, tagastatakse ajakohase hinnateabega ja sealt lisatakse need ostutaotlusele. Eesmärk on see, et kasutajad ei saaks väliselt saidilt tellimust esitada. Välise kataloogi seadistamisel peate veenduma, et välise kataloogi kaudu kasutatava saidi eesmärk oleks koguda hinnapakkumise andmeid ja mitte esitada tegelikku tellimust.

### <a name="to-set-up-an-external-vendor-catalog-complete-the-following-tasks"></a>Välise hankija kataloogi seadistamiseks täitke järgmised ülesanded.

1. Hankekategooria hierarhia seadistamine. Lisateavet leiate jaotisest [Hankekategooria hierarhiate poliitikate seadistamine](tasks/set-up-policies-procurement-category-hierarchies.md).
2. Registreerige tarnija rakenduses Supply Chain Management. Enne kui saate seadistada konfiguratsioone välisesse hankija kataloogi pääsemiseks, peate seadistama Microsoft Dynamics 365-s hankija ja hankija kontakti. Välise kataloogi hankija tuleb lisada ka valitud hankekategooriasse. Lisateavet hankijate registreerimise kohta vt teemast [Hankija koostöö kasutajate haldamine](manage-vendor-collaboration-users.md). Teavet hankijate määramise kohta hankekategooriasse leiate jaotisest [Konkreetsetele hankekategooriatele hankijate kinnitamine](tasks/approve-vendors-specific-procurement-categories.md).
3. Veenduge, et oleks seadistatud mõõtühikud ja valuuta, mida hankija kasutab. Teavet mõõtühiku loomise kohta vaadake jaotisest [Mõõtühiku haldamine](../pim/tasks/manage-unit-measure.md).
4. Konfigureerige väline hankija kataloog, kasutades oma hankija välise kataloogisaidi nõudeid. Lisateavet selle ülesande kohta vt teemast [Välise hankija kataloogi konfigureerimine](#configure-the-external-vendor-catalog).
5. Testige hankija välise kataloogi konfiguratsioone, et kontrollida, kas sätted kehtivad ja te pääsete hankija välisesse kataloogi. Kasutage toimingut **Sätete valideerimine** määratletud taotluse seadistusteatise valideerimiseks. See sõnum peab põhjustama hankija välise kataloogisaidi avamise brauseriaknas. Valideerimise ajal ei saa sellelt hankijalt kaupu ja teenuseid tellida. Kaupade ja teenuste tellimiseks peate minema ostutaotlusest hankija kataloogi.
6. Aktiveerige väline kataloog, kasutades nuppu **Aktiveeri kataloog** lehel **Välised kataloogid**. Väline kataloog tuleb aktiveerida, enne kui töövõtjad saavad seda kasutada. Välise kataloogi saab alati inaktiveerida.


## <a name="configure-the-external-vendor-catalog"></a>Välise hankija kataloogi konfigureerimine

Selles jaotises antakse lisateavet eelmise jaotise ülesande 4 kohta.

1. Sisestage hankija välise kataloogi nimi ja kirjeldus. Sisestatud nimi kuvatakse diagrammil, mis kajastab välist kataloogi, mis ostutaotlust koostavale töötajale kuvatakse. Töötajad võivad klõpsata ostukorvil, et avada kataloog hankija välisel kataloogisaidil.
2. Lisage pilt, kasutades tegevust **Välise kataloogi pilt**. Pilt kuvatakse diagrammil, mis kajastab välist kataloogi, mis ostutaotlust koostavatele töötajatele kuvatakse. Pange tähele, et pildi laius ja kõrgus peavad olema võrdsed. Muidu ei kuvata pilti õigesti.
3. Valige, kas hankija välise kataloogi veebisait peab ilmuma samasse brauseriaknasse, kus töövõtja on ostutaotluse koostanud, või tuleb see kuvada uues aknas.
4. Valige kataloogi jaoks hankija. Loendis **Juriidilised isikud** on rida iga juriidilise isiku jaoks, kus hankija on seadistatud. Selleks et võimaldada kasutajatel tellida tooteid otse hankija kataloogist mõne juriidilise isiku, kuid mitte teiste, puhul, võite kasutada nuppu **Takista juurdepääsu** või **Luba juurdepääs** iga juriidilise isiku puhul, kelle kataloogi soovite kättesaadavaks teha või mitte.
5. Sisestage väljale **Vaikimisi aegumine (päevades)** päevade arv, mille jooksul välisest kataloogist saadud pakkumine kehtib ja seda saab kasutada väliselt hankijalt ostmiseks. Kui pakkumine on loodud ja toodud hankija väliselt kataloogisaidilt, kehtib pakkumine praeguse süsteemikuupäeva seisuga ja jääb kehtivaks sellele väljale sisestatud päevade jooksul.
6. Klõpsake nuppu **Lisa** hankekategooriate vastendamise alustamiseks välise kataloogiga. Seejärel valige kategooria loendist Kategooria nimi. Kategooriate loend on hankekategooriate ülemhulk, millega hankija on kõigis hankijale seadistatud juriidilistes isikutes vastendatud.

    > [!NOTE]
    > Hankepoliitikaid kasutatakse ostva juriidilise isiku või vastuvõtva tootmisüksuse kategooriatele juurdepääsu lubamiseks või piiramiseks. Väljaregistreerimine välisesse kataloogi nõuab, et oleks lubatud juurdepääs vähemalt ühele kataloogiga vastendatud hankekategooriale.

7. Seadistage cXML-i seadistustaotluse sõnum, mis hankijale saadetakse. Automaatselt loodava sõnumi vorming on minimaalne mall, mis on seansi alustamiseks nõutav. Sisestage siltide väärtused.

Saate igal ajal süsteemi loodud sõnumimalli uuesti laadida, klõpsates nuppu **Taasta sõnumivorming**. Pange tähele, et sõnumivormingu taastamisel asendatakse praegune sõnum automaatselt loodud sõnumivorminguga, millel on tühjad sildid.

### <a name="cxml-setup-message"></a>cXML-i seadistussõnum
Allpool leiate mallis sisalduvate siltide kirjelduse.

| Väli | Kirjeldus | 
|---------|---------|
|< Header >< From >< Credential domain=”” >|Ostja ettevõtte domeen.|
|< Header >< From >< Credential>< Identity >< /Identity > | Ostja ettevõtte identiteet.|
|< Header >< To >< Credential domain=”” > | Hankija ettevõtte domeen.|
|< Header >< To >< Credential>< Identity >< /Identity> | Hankija ettevõtte identiteet.|
|< Header >< Sender >< Credential domain=”” > | Ostja ettevõtte domeen.|
|< Header >< Sender >< Credential >< Identity >< /Identity> | Ostja ettevõtte identiteet.|
|< Header >< Sender >< Credential >< SharedSecret >< /SharedSecret >|Ostja ettevõtte jagatud saladus.|
|< Request deploymentMode=”” >|Test või tootmise juurutus.|
|< Request >< PunchOutSetupRequest >< SupplierSetup >< URL >< /URL>|Hankija väljaregistreerimise lõpp-punkti URL.|

### <a name="extrinsic-elements"></a>Välised elemendid

Väline element on lisateave (nt kasutajanimi), mis põhineb väljaregistreerival kasutajal. Väline element määratakse väljaregistreerimise toimumisel ja selle saab saata taotluse seadistusteates.
Teie hankijal võib olla nõue välise elemendi vastuvõtmise kohta seadistustaotluses. Sel juhul tuleb lisada väline element väliste elementide loendisse lehe **Väline kataloog** jaotises **Sõnumivorming**.
Määrake välisele elemendile nimi, mille hankija ära tunneb, ja vastendage see väärtusega. Väärtuste valikud on: kasutaja nimi, kasutaja meil või juhuslik väärtus.
Lisateavet cXML-protokolli kohta leiate [veebisaidilt cXML.org](http://cxml.org/).

## <a name="post-back-message"></a>Tagasisisestamise teade
Tagasisisestamise teade on teade, mis saadakse hankijalt, kui kasutaja logib väliselt saidilt välja ja naaseb rakendusse Supply Chain Management. Tagasisisestamise teateid ei saa konfigureerida. Need teated põhinevad cXML-protokolli definitsioonil. Siin on teave, mis võib kuuluda ostutaotluse real saadud tagasisisestuse teatesse.

| Hankijalt saadud teade | Kopeeritud taotluse reale|
|------------------------------|----------------------------------------------------------|
|< ItemIn quantity=”” > |Kogus|
|< ItemIn>< ItemID >< SupplierPartID >< /SupplierPartID >|Välise kauba ID|
|< ItemDetail>< UnitPrice >< Money currency=”” >| Valuuta|
|< ItemDetail >< UnitPrice >< Money >< /Money >| Ühiku hind|
|< ItemDetail >< Description ShortName=”” >|Toote nimi|
|< ItemDetail >< Description >< /Description >|Sisaldub kauba kirjelduses; toote nimi, kui valikut ShortName pole määratud.|
|< ItemDetail >< UnitOfMeasure >< /UnitOfMeasure >|Üksus|
|< ItemDetail >< Classification >< /Classification >|Sisaldub kauba kirjelduses|
|< ItemDetail >< Classification domain=”” >|Sisaldub kauba kirjelduses|

## <a name="delete-an-external-catalog"></a>Välise kataloogi kustutamine
Kustutage väline kataloog lehel tegevusega Kustuta.

Kui välises hankija kataloogis olev toode on taotletud, siis ei saa välist hankija kataloogi kustutada. Selle asemel määratakse välise hankija kataloogi olek passiivseks. Kui soovite eemaldada juurdepääsu välise hankija kataloogi saidile, kuid mitte seda kustutada, siis muutke välise kataloogi olek passiivseks.

## <a name="additional-resources"></a>Lisaressursid

- [cXML-i täiustuste ostmine](purchasing-cxml-enhancements.md)
- [Väliskataloogide kasutamine e-hanke väljaregistreerimiseks](use-external-catalogs-for-punchout.md)