---
title: Ostmisega seotud cXML-i täiustused
description: Ostmisega seotud cXML-i täiustuste funktsioon põhineb olemasoleval väliskataloogi funktsioonil „Väljaregistreerimine”, mida kasutatakse ostutaotluste puhul.
author: GalynaFedorova
ms.date: 08/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatCXMLParameters, CatCXMLPurchRequest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2020-08-03
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 319079ca82ea91a4ab963a1dfa34ed256a3ddb21
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674277"
---
# <a name="purchasing-cxml-enhancements"></a>Ostmisega seotud cXML-i täiustused

[!include [banner](../includes/banner.md)]

Funktsioon _Ostmisega seotud cXML-i täiustused_ põhineb [olemasoleval väliskataloogi funktsioonil](set-up-external-catalog-for-punchout.md), mida kasutatakse ostutaotluste puhul. Selle olemasoleva funktsiooni nimi on _Väljaregistreerimine_. Kuigi ostutellimus ei pea pärinema ostutaotlusest, peab ostutellimusel oleva hankija ja ostutellimuse dokumendi saatmiseks kasutatavate parameetrite vahel olema seos.

## <a name="turn-on-the-purchasing-cxml-enhancements-feature"></a>Ostmisega seotud cXML-i täiustuste funktsiooni sisselülitamine

Funktsiooni sisselülitamiseks avage leht **[Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** ja otsige üles funktsioon, mille nimi on *Ostmisega seotud cXML-i täiustused*. Valige funktsioon ja seejärel valige selle sisselülitamiseks **Luba kohe**. (Tarneahela halduse versiooni 10.0.21 kohaselt on see funktsioon vaikimisi sisse lülitatud.)

Pärast funktsiooni sisselülitamist peate konfigureerima järgmise kolme valdkonna sätted.

- **[cXML-i parameetrid](#cxml-parameters)** – kasutage neid sätteid, et seadistada ostutellimuste saatmise funktsiooni globaalsed parameetrid.
- **[Hankija seadistus](#vendor-setup)** – kui laiendatavat kommertsmärgistuskeelt (cXML) tuleb vaikimisi kasutada kõigi uute ostutellimuste jaoks, mis mõne hankija jaoks luuakse, seadke selle hankija jaoks suvandi **Saada ostutellimus cXML-i kaudu** väärtuseks _Jah_.
- **[Väliskataloogid](#external-catalog-setup)** – kasutage uusi **Tellimuse atribuutide** sätteid, et määratleda ostutellimuse dokumendi vorming ja selle saatmisviis.

Järgmisel illustratsioonil on selle konfiguratsiooni kokkuvõte.

![cXML-i funktsioonide seadistamise alad.](media/cxml-settings-areas.png "cXML-i funktsioonide seadistamise alad")

Lisaks peate seadistama [Ostutellimustaotluse pakett-töö](#po-batch). Seda pakett-tööd kasutatakse kinnitatud ostutellimuste saatmiseks.

## <a name="set-up-global-cxml-parameters"></a><a name="cxml-parameters"></a>Globaalsete cXML-i parameetrite seadistamine

Kasutage lehte **cXML-i parameetrid**, et luua globaalsed sätted, mis kehtivad ostutellimuste saatmise korral.

![cXML-i parameetrite leht.](media/cxml-parameters.png "cXML-i parameetrite leht")

Avage **Hanked \> Seadistus \> cXML-i haldus \> cXML-i parameetrid** ning seadke järgmised parameetrid.

- **cXML-i testrežiim** – see globaalne parameeter mõjutab seda, kuidas ostutellimused pakett-tööst füüsiliselt saadetakse. Valige üks järgmistest väärtustest.

    - **Test** – selles režiimis käivitatakse pakett-töö ja luuakse teate jaoks XML-dokument, kuid seda ei saadeta. Selle asemel salvestatakse see läbivaatamiseks ostutellimustaotluses. See režiim on kasulik, kui juurutamine on just alanud ja soovite näha, kuidas andmeid cXML-i teatesse sisestatakse. Soovi korral võite luua ka näidisteateid, mida saate saata hankijatele esmaseks kinnitamiseks.
    - **Reaalajas** – selles režiimis kasutab funktsioon [väliskataloogi sätteid](#external-catalog-setup), et edastada iga dokument füüsiliselt hankijale.

- **Saada ostunõude värskendusi** – seadke selle suvandi väärtuseks *Jah*, et saata ostutellimuste kohta värskendusteateid. Seadke väärtuseks *Ei*, et takistada teate saatmist. Enamik hankijaid eelistab värskendusteateid mitte saada. Selle asemel soovivad nad, et kliendid võtaks nendega ühendust telefoni või e-posti teel, kui ostutellimust on vaja muuta. See parameeter on globaalne parameeter ja väliskataloogis ei saa hankijate jaoks ühtegi alistamist määratleda. Ostutellimus märgitakse värskendatuks, kui sisestate ostutellimusele teise kinnituse, kuid esimene kinnitus on juba hankijale saadetud ja ta on selle vastu võtnud. Kui teine kinnitus on olemas, kuid esimest kinnitust ei ole saadetud, käsitletakse teist kinnitust uue dokumendina. Ostutellimust saate kinnitada nii mitu korda, kui soovite, kuni saadetakse üks kinnitus. Seejärel käsitletakse järgmist kinnitust värskendusteatena.
- **Saada ostunõude kustutusteade** – seadke selle suvandi väärtuseks *Jah*, et saata ostutellimuste kohta kustutusteateid. Seadke väärtuseks *Ei*, et takistada teate saatmist. Enamik hankijaid eelistab kustutusteateid mitte saada. Selle asemel soovivad nad, et kliendid võtaks nendega ühendust telefoni või e-posti teel, kui ostutellimus saadeti kogemata. See parameeter on globaalne parameeter ja väliskataloogis ei saa hankijate jaoks ühtegi alistamist määratleda. Ostutellimus märgitakse kustutatuks, kui tühistate selle rakenduses Supply Chain Management.
- **Arhiivifail** – määratlege failitee, kuhu soovite eksportida ja salvestada arhiveeritud cXML-dokumente. Teed kasutatakse siis, kui käivitate lehel **Ostutellimustaotlus** likvideerimisfunktsiooni.
- **Tänava rea maksimaalne tähemärkide arv** – sisestage suurim märkide arv, mida saab cXML-dokumendis tänava väljal aadresside jaoks kasutada. Kui väliskataloogi atribuutides pole määratletud alistust, mõjutab see globaalne parameeter kõiki hankijaid.

## <a name="set-up-vendor-purchase-orders-to-use-cxml"></a><a name="vendor-setup"></a>Hankija ostutellimuste seadistamine cXML-i kasutamiseks

Iga kord, kui kinnitate ostutellimuse, mille suvandi **Saada ostutellimus cXML-i kaudu** väärtuseks on seatud _Jah_, loob süsteem automaatselt cXML-i teate ja saadab selle ostutellimusega seotud hankijale. Selle suvandi kontrollimiseks ostutellimuste puhul on kaks võimalust.

- Hankija seadistamiseks nii, et see kasutaks kõigi uute ostutaotlusest loodavate ostutellimuste puhul automaatselt cXML-i, avage **Hanked \> Hankijad \> Kõik hankijad** ning valige või looge hankija, et avada selle üksikasjade leht. Seejärel seadke kiirkaardil **Ostutellimuse vaikesätted** suvandi **Saada ostutellimus cXML-i kaudu** väärtuseks _Jah_. Kui cXML-i tuleb kasutada automaatselt ka uute ostutellimuste puhul, mida **ei** looda ostutaotluse põhjal, peate seadma seotud väliskataloogi puhul tellimuse atribuudi **ENABLEMANUALPO** väärtuseks _Tõene_, nagu on kirjeldatud selle teema tulevases jaotises [Tellimuse atribuutide seadmine](#set-order-properties).
- Üksikute ostutellimuste puhul avage **Hanked \> Ostutellimused \> Kõik ostutellimused** ja valige või looge ostutellimus, et avada selle üksikasjade leht. Aktiveerige vaade **Päis** ja seejärel seadistage kiirkaardil **Seadistus** suvand **Saada ostutellimus cXML-i kaudu** nii, nagu vaja.

![Hankija ostutellimuste vaikesätted.](media/cxml-order-defaults.png "Hankija ostutellimuste vaikesätted")

## <a name="set-up-an-external-catalog-to-use-cxml"></a><a name="external-catalog-setup"></a>Väliskataloogi seadistamine cXML-i kasutama

Lehel **Väliskataloogid** saate iga kataloogi puhul seadistada väljaregistreerimise ja ostutellimuste saatmise funktsioonid. Asjakohaste sätete leidmiseks avage **Hanked \> Kataloogid \> Väliskataloogid**. Alustage [iga kataloogi seadistamisest, nagu tavaliselt](set-up-external-catalog-for-punchout.md). See protsess hõlmab hankija määramist, kategooriate valimist, milles hankijal on lubatud tarnida, ja kataloogi aktiveerimist. Seejärel konfigureerige lisasätted, mida kirjeldatakse selles jaotises.

> [!NOTE]
> Kui kinnitate ostutellimuse, mida saab saata cXML-i kaudu, otsib süsteem üles selle ostutellimusega seotud hankija ja seejärel hankijaga seotud esimese aktiivse väliskataloogi. Süsteem kasutab seejärel ostutellimuse saatmiseks selle väliskataloogi sätteid. Kui seadistatud on mitu väliskataloogi, kasutab süsteem ainult esimest leitud väliskataloogi, lähtudes ostutellimuses märgitud hankijast. Seetõttu soovitame luua igale hankijale ainult üks väliskataloog.

![Väliskataloogi sätted.](media/cxml-supplier-catalog.png "Väliskataloogi sätted")

### <a name="set-the-punchout-protocol-type"></a>Väljaregistreerimisprotokolli tüübi määramine

Seadke lehel **Väliskataloogid** asuval kiirkaardil **Üldine** välja **Väljaregistreerimisprotokolli tüüp** väärtuseks _cXML_. See suvand on ainukesena saadaval, kui partner pole funktsiooni laiendanud ega paku laienduses lisasuvandit.

Kui kasutate kataloogi ka väljaregistreerimiseks, peate [seadistama ka teatevormingu](set-up-external-catalog-for-punchout.md). Teatevormingut kasutatakse taotlusest alguse saanud väljaregistreerimiskandes hankijaga ühenduse loomiseks. Ostutellimuse saatmisel kasutatakse tellimuse atribuute hankijaga ühenduse loomiseks.

### <a name="set-the-order-properties"></a><a name="set-order-properties"></a>Tellimuse atribuutide määramine

Funktsioon _Ostmisega seotud cXML-i täiustused_ lisab väliskataloogidele uute kiirkaardi **Tellimuse atribuudid**. Kiirkaart hõlmab võrgustikku, kus saate määratleda tellimuse atribuudid. Samuti on sellel tööriistariba. See tööriistariba hõlmab kolme järgmist nuppu, mida saate kasutada tellimuse atribuutide haldamiseks.

- **Vaikeatribuudid** – uue kataloogi seadistamisel valige see nupp, et lisada võrgustikku eelmääratletud sagedasti kasutatavad atribuudid.
- **Uus** – lisage ruudustikku uus atribuut.
- **Kustuta** – kustutage praegu valitud atribuut ruudustikust. Kui kustutate vaikeatribuudi kogemata, valige **Vaikeatribuudid**, et taastada kõik puuduvad atribuudid.

Iga kord, kui lisate ruudustikku ühe või mitu atribuuti, kasutage nende väärtuste määratlemiseks parempoolset veergu.

Kasutage vaikeatribuute järgmisel viisil.

- **BUYER\_COOKIE** – seda jälgimisvälja saab kasutada ettevõtte kohta kindla teabe määramiseks. Kui te pole hankijaga kokku leppinud, kuidas seda atribuuti kasutada, pole see ostutellimuse saatmisel kuigi oluline. Seetõttu peaksite selle puhul kasutama lihtsat väärtust.
- **DELIVERTO** – kui ostutellimusest pärit dokumenti sisestatakse tarneaadress, kasutatakse välja **Tähtis teave**, et määrata XML-teatises väli **DeliverTo**. Kui teil on vaja, et see väärtus oleks nõude esitaja, ja te määrate nõude esitaja välja ostutellimuse päises, sisestage selle atribuudi väärtuseks _REQUESTER_, et nõude esitaja nimi sisestataks XML-is väljale **DeliverTo**. Sel juhul on kasutatavad peamine meiliaadress ja telefoninumber pärit nõude esitajalt, mitte tellijalt.
- **DEPLOYMENTMODE** – määrake see atribuut hankija soovitud viisil. Väärtused on tavaliselt _PRODUCTION_ või _TEST_. Seadke väärtus hankijaga suhtlemise põhjal. Tavaliselt peab see ühtima väärtuse **ORDERCHECKURL** kaudu määratud süsteemiga, mille hankija määrab test- või tootmissüsteemina.
- **FIXEDBILLADDRESSID** – välja **addressID** määramisel XML-teatises võtab see enda väärtuseks aadressis määratletud asukoha. Kui hankijale edastatud ID väärtus erineb mingil põhjusel aadressi asukoha väärtusest, saate asukoha alistada, määratledes väärtuse selle suvandi kaudu. Eeldatakse, et te kasutate hankija puhul ainult üht aadressi ja aadress seadistatakse hankija süsteemis. Arveaadress on esmane arve saaja aadress, mis on määratletud juriidilise isiku jaoks rakenduses Supply Chain Management.
- **FIXEDSHIPADDRESSID** – välja **addressID** määramisel XML-teatises võtab see enda väärtuseks aadressis määratletud asukoha. Kui hankijale edastatud ID väärtus erineb mingil põhjusel aadressi asukoha väärtusest, saate asukoha alistada, määratledes väärtuse selle suvandi kaudu. Eeldatakse, et te kasutate hankija puhul ainult üht aadressi ja aadress seadistatakse hankija süsteemis. Tarneaadress on ostutellimuse päises määratletud aadress. Enamikule hankijatest sobib ainult päise aadressid, mitte rea aadressid. Kuigi XML sisaldab välju rea aadresside jaoks, seatakse need päise aadressiks.
- **FROM\_DOMAIN** – sisestage ostutellimuse dokumentide saatmiseks kasutatav väärtus. Selle väärtuse annab teie hankija.
- **FROM\_IDENTITY** – sisestage ostutellimuse dokumentide saatmiseks kasutatav väärtus. Selle väärtuse annab teie hankija.
- **ORDERCHECKURL** – sisestage URL, kuhu edastada ostutellimuse dokumendid. URL algab tähemärkidega `https://` ja selle annab teie hankija.
- **PAYLOAD\_ID** – sisestage lasti ID eesliite väärtus nii, nagu on vaja praeguse hankija puhul kehtivate äriprotsesside puhul.
- **SENDER\_DOMAIN** – sisestage ostutellimuse dokumentide saatmiseks kasutatav väärtus. Selle väärtuse annab teie hankija.
- **SENDER\_IDENTITY** – sisestage ostutellimuse dokumentide saatmiseks kasutatav väärtus. Selle väärtuse annab teie hankija.
- **SHARED\_SECRET** – sisestage ostutellimuse dokumentide saatmiseks kasutatav väärtus. Selle väärtuse annab teie hankija.
- **STREETLENGTH** – sisestage number, mis tähistab maksimaalset tähemärkide arvu, mis hankijale tänava nime puhul sobib. Kui siia sisestatakse väärtus, alistab see väärtuse, mis on määratletud lehel **cXML-i parameetrid**. Süsteem eemaldab reapiirid ja tühikud, et üritada jätta rakenduses Supply Chain Management määratud standardne aadress siin määratletud tähemärkide arvu piiridesse. Kõik lisatähemärgid kärbitakse.
- **TO\_DOMAIN** – sisestage ostutellimuse dokumentide saatmiseks kasutatav väärtus. Selle väärtuse annab teie hankija.
- **TO\_IDENTITY** – sisestage ostutellimuse dokumentide saatmiseks kasutatav väärtus. Selle väärtuse annab teie hankija.
- **USERAGENT** – sisestage väärtus süsteemi tuvastamiseks, mida te kasutate. Sisestage näiteks _Dynamics 365 Supply Chain Management_.
- **VERSION** – sisestage cXML-i versiooni number, kui hankija seda teavet nõuab. Vaikeversioon on *1.2.008*. See versioon on stabiilne ja sobib enamikule hankijatele.
- **RESPONSETEXT** – sisestage kohandatud tekst, mida soovite, et hankija tagastaks cXML-i vastuseteates pärast tellimuse saatmist. Sel viisil saab süsteem märkida teate _kinnitatuks_. Kui vastus ei ühti standardse tekstiga või siia sisestatud kliendi tekstiga, märgitakse taotlus _tõrkeks_.
- **RESPONSETEXTSUB** – määrake selle atribuudi väärtuseks _TRUE_, kui soovite otsida hankija vastuse tekstist väärtusi, mis on määratletud väljal **RESPONSETEXT**. Näiteks võib hankija tagastada vastuses pika stringi, mis sisaldab teksti „OK”. Sel juhul saate sisestada väljale **RESPONSETEXT** väärtuse _OK_ ja seada suvandi **RESPONSETESTSUB** väärtuseks _TRUE_, et otsida vastusest teksti „OK”. Seejärel saab tellimuse märkida _kinnitatuks_.
- **CONTENTTYPE** – tüüpilise kataloogiseadistuse puhul ei pea te seda atribuuti määrama. Kui saate ostutellimuse saatmisel hankija süsteemist tõrke „Server 500”, on teil võimalik probleemi testida, määrates selle atribuudi väärtuseks _FALSE_. See väärtus muudab veebipäringus üht sätet ja on võimalik, et mõne platvormi puhul on teadet võimalik saata.
- **ENABLEHEADERS** – seadke selle atribuudi väärtuseks _TRUE_, et saata päised koos ostutellimusega. Määrake see atribuut ainult juhul, kui hankija seda nõuab. Kui seate selle atribuudi väärtuseks _TRUE_, lisage täiendavad kohandatud atribuudid, mis põhinevad hankija antud nimedel, ja lisage nende eesliiteks _H\__. Tüüpilised näited on **H\_USERID**, **H\_PASSWORD**, **H\_RECEIVERID** ja **H\_ACTIONREQUEST**. Vaikeatribuudid hõlmavad järgmisi kohandatud atribuute.

    - **H\_USERID** – kui äripartner nõuab, et saadaksite ostutellimuse esitamisel URL-i osana kasutaja ID, sisestage see väärtus siia.
    - **H\_PASSWORD** – kui äripartner nõuab, et saadaksite ostutellimuse esitamisel URL-i osana parooli, sisestage see väärtus siia.

- **ENABLEMANUALPO** – kui selle atribuudi väärtuseks on seatud _TRUE_, siis pärivad kasutajate käsitsi loodud ostutellimused (st kui neid ei luua ostutaotluse põhjal) hankijalt suvandi **Saada ostutellimus cXML-i kaudu**. Kui seda atribuuti pole määratud või kui selle väärtuseks on seatud _FALSE_, ei määrata käsitsi loodud ostutellimuste puhul ostutellimuse päises suvandit **Saada ostutellimus cXML-i kaudu**. Ostutaotluse põhjal loodud ostutellimuste puhul päritakse suvand **Saada ostutellimus cXML-i kaudu** alati hankijalt, hoolimata selle atribuudi sättest. Lisateavet leiate selle teema varasemast jaotisest [Hankija ostutellimuste seadistamine cXML-i kasutamiseks](#vendor-setup).
- **PUNCHOUTPOONLY** – kui selle atribuudi väärtuseks on seatud _TRUE_, määravad ostutellimuse päises suvandi **Saada ostutellimus cXML-i kaudu** ainult väljaregistreerimisprotsessi kaudu loodud ostutaotluse read. Lisaks peab ostutellimuse kõigi ridade ostutaotluse rea tüüp olema _Väliskataloogi kaup_. Vastasel juhul ei saa cXML-i ostutellimust luua.
- **PUNCHOUTSHIPTO** – kui selle atribuudi väärtuseks on seatud _TRUE_, lisatakse juriidilise isiku vaike-aadress väljaregistreerimise seadistustaotluse teatele, kui kasutaja avab väliskataloogi. See aadress lisatakse aadressina **ShipTo**. Hankijad kasutavad aadressi **ShipTo**, et näidata ettevõtte asukoha põhjal hinnakirja.
- **TRACEPUNCHOUT** – seadke selle atribuudi väärtuseks _TRUE_, kui te saate ostutaotlusest väliskataloogi minna üritades tõrketeate. Seejärel lisatakse jälitusteave teadetesse **PunchOutSetupRequest** ja **PunchOutResponse**, mis saadetakse rakenduse Supply Chain Management ja hankija saidi vahel. Seda teavet saate vaadata lehel **CXML-i ostukorvi teatelogi**, mille saate avada probleemse hankija kataloogi lehel **Väliskataloogi seadistus**. Peaksite määrama selle atribuudi väärtuseks _TRUE_ ainult tõrkeotsinguks, kuna see vähendab iga väljaregistreerimise puhul suuresti andmebaasi jõudlust. Lisateavet leiate selle teema hilisemast jaotisest [cXML-i ostukorvi teatelogi kuvamine väliskataloogi väljaregistreerimisel](#message-log).
- **REPLACENEWLINE** – seadke selle atribuudi väärtuseks _TRUE_, kui teil tekib probleem selle tõttu, et hankija süsteem saadab teate **PunchOutResponse**, mis sisaldab reavahetuse märke (\\n). See probleem võib ilmneda juhul, kui hankija teateid sõelutakse vahetarkvara või hankekeskuse kaudu. Kui teil tekib probleem uue hankija seadistuse tõttu, seadke atribuudi **TRACEPUNCHOUT** väärtuseks _TRUE_, et vaadata teadet **PunchOutResponse** ja teha kindlaks, kas XML-sildid on reavahetuse märkide tõttu katkenud.
- **POCOMMENTS** – seadke selle atribuudi väärtuseks _TRUE_, kui soovite, et cXML-dokument sisaldaks märkusi, mis on rakenduses Supply Chain Management ostutellimusele lisatud. Manuse tekst lisatakse ostutellimuse teates päise kommentaaridesse. Lisateavet selle kohta, kuidas süsteem neid manuseid valib ja töötleb, leiate selle teema hilisemast jaotisest [Ostutellimusele märkuste lisamine](#attach-po-notes).
- **VENDCOMMENTS** – seadke selle atribuudi väärtuseks _TRUE_, kui soovite, et cXML-dokument sisaldaks märkusi, mis on rakenduses Supply Chain Management ostutellimusele lisatud. Manuse tekst lisatakse ostutellimuse teates päise kommentaaridesse. Lisateavet selle kohta, kuidas süsteem neid manuseid valib ja töötleb, leiate jaotisest [Ostutellimusele märkuste lisamine](#attach-po-notes).
- **CLEANAMP** – seadke selle atribuudi väärtuseks _TRUE_, kui te saate hankija puhul väljaregistreerides tõrketeate ja hankija tagastus-URL sisaldab valesti kodeeritud ampersande (\&).
- **PUNCHOUTTZ** – seadke selle atribuudi väärtuseks _TRUE_, kui hankija, kellega töötate, kasutab rahvusvahelise standardiorganisatsiooni (ISO) 8601 standardit, et kontrollida väljaregistreerimise taotluse teate kuupäeva/kellaaega kindlal viisil. Supply Chain Management kasutab teates **PunchOutSetupRequest** koordineeritud maailmaaega (UTC). Kui seate selle atribuudi väärtuseks _TRUE_, lisatakse seega kuupäeva/kellaaja vormingule *+00:00*.
- **WMSADDRESSID** – seadke selle atribuudi väärtuseks _TRUE_, et kasutada ostutellimuse päise laonumbrit hankijale saadetava ostutellimustaotluse jaoks väärtusena **addressID** aadressis **ShipTo**. Kui määrate atribuudile **FIXEDSHIPADDRESSID** väärtuse, siis arvestatakse selle väärtuse asemel toda väärtust. Seetõttu peaksite kasutama üht või teist atribuuti, et seada dokumendi aadressis **ShipTo** väärtus **addressID**.
- **PUNCHOUTSHIPTOUSER** – see atribuut töötab koos atribuudiga **PUNCHOUTSHIPTO**. Kui atribuudi **PUNCHOUTSHIPTO** väärtuseks on seatud _TRUE_, kasutatakse juriidilise isiku aadressi. Kui atribuudi **PUNCHOUTSHIPTOUSER** väärtuseks on seatud _TRUE_, kasutatakse juriidilise isiku aadressi asemel väljaregistreerimise kasutaja esmast aadressi.

### <a name="activate-the-external-catalog"></a>Väliskataloogi aktiveerimine

Kui olete väliskataloogi kõigi atribuutide seadistamise ja muude sätete konfigureerimise lõpetanud, minge tagasi vahekaardile **Üldine**, mis asub lehel **Väliskataloogid**, ja seadke suvandi **Aktiivne** väärtuseks *Jah*.

### <a name="attach-notes-to-a-purchase-order"></a><a name="attach-po-notes"></a>Ostutellimusele märkuste lisamine

Nagu mainiti jaotises [Tellimuse atribuutide määramine](#set-order-properties), saate seada väliskataloogi seadistuses atribuudi **POCOMMENTS** ja/või **VENDCOMMENTS** väärtuseks _TRUE_, kui soovite, et saadetav cXML sisaldaks teksti, mis on pärit ostutellimusele ja/või hankijakirjetele lisatud märkustest. Selles jaotises antakse üksikasjalikumat teavet selle kohta, kuidas süsteem neid manuseid kasutamise korral valib ja töötleb.

Märkuste tüüpide seadistamiseks, mida süsteem hakkab otsima, **minge hankevormi häälestuse \> vormi \> seadistusse \>**. Seejärel seadke vahekaardil **Ostutellimus** välja **Kaasa seda tüüpi dokumendid** väärtuseks märkuse tüüp, mida soovite kaasata. Kaasatakse ainult teksti kujul märkmed, mitte dokumendi kujul manused.

![Vormi seadistuse leht.](media/cxml-form-setup.png "Vormi seadistuse leht")

Manused kaasatakse ostutellimusse ainult juhul, kui nende välja **Tüüp** väärtuseks on seatud väärtus, mille valisite väljal **Kaasa seda tüüpi dokumendid**, ja kui nende välja **Piirang** väärtus on _Väline_. Ostutellimuse manuste loomiseks, vaatamiseks või redigeerimiseks avage **Hanked \> Kõik ostutellimused**, valige või looge ostutellimus ja seejärel valige ülevalt parempoolsest nurgast nupp **Manused** (kirjaklambrisümbol).

![Manustatud märge, mis on seadistatud hankijale saatmiseks.](media/cxml-note-to-vendor.png "Manustatud märge, mis on seadistatud hankijale saatmiseks")

## <a name="view-the-cxml-cart-message-log-for-external-catalog-punchout"></a><a name="message-log"></a>cXML-i ostukorvi teatelogi kuvamine väliskataloogi väljaregistreerimisel

Kui seate väliskataloogi puhul välja **Väljaregistreerimisprotokolli tüüp** väärtuseks _cXML_, jäädvustab süsteem hankijalt tagasi tulevate ostukorvide teatelogi. Seda logi saab kasutada tõrkeotsinguks ja muudeks andmetoiminguteks.

Väliskataloogi logi valimiseks valige asjaomane kataloog ja seejärel toimingupaanilt suvand **cXML-i ostukorvi teatelogi**. Lehel **cXML-i ostukorvi teatelogi** on näha tagastatud ostukorvide loend, ostukorvidega seotud XML ja seotud ostutaotluses loodud read.

![cXML-i ostukorvi teatelogi leht.](media/cxml-cart-message-log.png "cXML-i ostukorvi teatelogi leht")

## <a name="set-the-extrinsic-elements-for-external-catalog-punchout"></a>Väliste elementide määramine väliskataloogi väljaregistreerimiseks

Kui te seate väliskataloogi puhul välja **Väljaregistreerimisprotokolli tüüp** väärtuseks *cXML*, saate lisada kohandatud väliseid elemente, mis lisatakse taotluse XML-i teates õigesse kohta.

Väliste elementide lisamiseks väliskataloogi toimige järgmiselt.

1. Avage **Hanked \> Kataloogid \> Väliskataloogid**.
1. Valige asjaomane kataloog.
1. Valige jaotises **Välised** kiirkaardil **Teate vorming** suvand **Lisa**, et lisada ruudustikku rida iga välise elemendi jaoks, mida soovite kaasata. Määrake igas reas järgmised väljad.

    - **Nimi** – sisestage elemendi nimi. See väärtus muutub iga rea loodava XML-elemendi **Väline** atribuudi **nimi** väärtuseks. Tavaliselt lepitakse iga välise elemendi nimi hankijaga kokku.
    - **Väärtus** – valige elemendi väärtus. See väärtus muutub iga rea loodava XML-elemendi väärtuseks. Saadaval on järgmised väärtused:

        - **Kasutaja nimi** – kasutage väljaregistreerimistegevust tegeva kasutaja nime. See nimi on rakenduse Supply Chain Management sisselogimisnimi.
        - **Kasutaja meil** – kasutage väljaregistreerimistegevust tegeva kasutaja meiliaadressi. Tegemist on aadressiga, mille kasutaja on seadistanud lehe **Kasutaja suvandid** vahekaardil **Konto**.
        - **Juhuslik väärtus** – kasutage kordumatut juhuslikku väärtust.
        - **Kasutaja täisnimi** – kasutage väliskataloogi kasutava kasutajaga seotud kontaktisiku täisnime.
        - **Eesnimi** – kasutage väliskataloogi kasutava kasutajaga seotud kontaktisiku eesnime.
        - **Perekonnanimi** – kasutage väliskataloogi kasutava kasutajaga seotud kontaktisiku perekonnanime.
        - **Telefoninumber** – kasutage väliskataloogi kasutava kasutajaga seotud kontaktisiku esmast telefoninumbrit.

![Välise elemendi sätted.](media/cxml-extrinsics.png "Välise elemendi sätted")

Kasutaja või administraator ei näe väliseid elemente, kuna neid ei lisata enne, kui kasutaja teeb väljaregistreerimistegevust. Need lisatakse cXML-i seadistustaotluse teates automaatselt elementide **BuyerCookie** ja **BrowserFromPost** vahele. Seetõttu ei pea te väliskataloogi seadistades neid käsitsi XML-is seadistama.

![XML-i lisatud välised elemendid.](media/cxml-extrinsics-xml.png "XML-i lisatud välised elemendid")

## <a name="create-and-process-a-purchase-order"></a><a name="create-po"></a>Ostutellimuse loomine ja töötlemine

Kui loote hankijale ostutellimuse, pärib see samalt hankijalt suvandi **Saada ostutellimus cXML-i kaudu** seadistuse. Säte on siiski saadaval ostutellimuse vaate **Päis** kiirkaardil **Seadistus**, et saaksite seda hiljem vajadusel muuta.

![cXML-i kasutamiseks seadistatud ostutellimus.](media/cxml-purchase-order.png "cXML-i kasutamiseks seadistatud ostutellimus")

Kui loote ostutellimuse ostutaotlusest, mis on pärit väljaregistreerimise voost, täidetakse kõik vajalike ridade üksikasjad. Seejärel saate ostutellimuse read käsitsi lisada või kopeerida need muudest ostutellimustest. Seadke kindlasti kõik kohustuslikud väljad. Need kohustuslikud väljad sisaldavad välisviitenumbrit, mis on cXML-i teates kasutatav hankija number.

![Välisviitenumbri näide.](media/cxml-line-details.png "Välisviitenumbri näide")

Kui olete ostutellimuses kõigi üksikasjade täitmise lõpetanud, kinnitage see kindlasti. Teadet ei saadeta, kui ostutellimus pole kinnitatud. Ostutellimuse kinnitamiseks valige toimingupaani vahekaardi **Ostmine** grupis **Tegevused** suvand **Kinnita**. 

Pärast ostutellimuse kinnitamist saate vaadata kinnituse olekut töölehtede **Ostutellimuse kinnitused** kaudu. Valige toimingupaani vahekaardi **Ostmine** grupis **Töölehed** suvand **Ostutellimuse kinnitused**.

Igal ostutellimusel võib olla palju kinnitusi. Iga kinnitus on märgitud suureneva numbriga. Järgmises näites on ostutellimus *00000275* ja kinnitus *00000275-1*. See nummerdamine kajastab rakenduse Supply Chain Management standardset funktsiooni, mille puhul tuvastatakse kinnituse põhjal ostutellimuse muudatused ja seetõttu ka hankijale saadetava cXML-i teate tüüp. Nagu illustratsioonilt näha, hõlmab leht **Ostutellimuse kinnitused** ka välju **Tellimuse saatmise olek** ja **Tellimustaotluse hankija olek**. Lisateavet eri olekuväärtuste kohta, mida sellel lehel näha võite, leiate selle teema hilisemast jaotisest [Ostutellimustaotluste jälgimine](#monitor-po-requests).

![Ostutellimuse kinnituste leht.](media/cxml-po-confirmations.png "Ostutellimuse kinnituste leht")

Dokumendi kohta lisateabe vaatamiseks valige ruudustiku kohalt **Ostutellimustaotlus**.

Leht **Ostutellimustaotlus** hõlmab kaht ruudustikku. Lehe ülemises osas olevas ruudustikus on üks kirje iga saatmiseks märgitud ostutellimuse jaoks. Lehe alumises osas oleva vahekaardi **Ostutellimustaotluse ajalugu** ruudustikus võib olla valitud ostutellimuse kohta mitu kirjet, et näidata iga kinnituse olekut. Järgmisel illustratsioonil on näha ülemises ruudustikus olev ostutellimus 00000275 ja vahekaardi **Ostutellimustaotluse ajalugu** võrgustikus olev dokument 00000275-1.

![Ostutellimustaotluse leht.](media/cxml-po-request.png "Ostutellimustaotluse leht")

Dokument saadetakse, kui pakett-töö on seadistatud ja käivitatud. Oleku muutumist saate vaadata pärast dokumendi saatmist. Järgmisel illustratsioonil on välja **Tellimuse saatmise olek** väärtuseks seatud _Saadetud_. Välja **Tellimustaotluse hankija olek** väärtus on _Kinnitatud_, et näidata, et hankija sai dokumendi kätte ning suutis seda oma süsteemis lugeda ja talletada. Vahekaardil **Ostutellimustaotluse ajalugu** olevas ruudustikus on näha dokumendi saatmise aeg. Lisateavet eri olekuväärtuste kohta, mida sellel lehel näha võite, leiate jaotisest [Ostutellimustaotluste jälgimine](#monitor-po-requests).

![Olekuteated ostutellimustaotluse lehel.](media/cxml-po-request-2.png "Olekuteated ostutellimustaotluse lehel")

## <a name="schedule-the-purchase-order-request-batch-job"></a><a name="po-batch"></a>Ostutellimustaotluse pakett-töö ajastamine

Pakett-töö aktiveerimiseks ostutellimustaotluste saatmiseks avage **Hanked \> Seadistus \> cXML-i haldus \> Ostutellimustaotlus** ning seejärel valige toimingupaanil vahekaardi **Ostutellimustaotlus** grupis **Partii** suvand **Edasta töö**, et avada dialoogiboks **Ostunõude ettevalmistamine ja saatmine**. Seda dialoogiboksi saate kasutada kordumise seadistamiseks, nagu te teete seda pakett-tööde puhul rakenduses Supply Chain Management. Valige oma tellimuse mahul põhinev intervall. Kuigi saate pakett-töö käivitada iga minut, on parem saata partiisid kogu tööpäeva jooksul, võttes arvesse hankijate graafikutega ühtivaid tellimuse sissetuleku ajavahemikke.

Näiteks on teie hankijal poliitika, mille põhjal lähetatakse kõik enne kella 13.00 vastu võetud tellimused samal päeval. Sel juhul saate käivitada partii ainult paar korda hommikul, et edastada olemasolevad tellimused. Ülejäänud tellimused saadetakse seejärel järgmisel päeval. Selle otsuse puhul on tegemist äriotsusega. Saate selle üle vaadata ja seadistada parameetrid sellest lähtudes.

Protsessi käigus otsitakse ostutellimustaotluse dokumente, mille olek on *Ootel*. Kui teil on tellimus, mille peate hankijale kohe saatma, saate valida **Edasta töö** ja seada suvandi **Pakktöötlus** väärtuseks *Ei*.

## <a name="monitor-purchase-order-requests"></a><a name="monitor-po-requests"></a>Ostutellimustaotluste jälgimine

### <a name="view-the-status-of-a-purchase-order"></a>Ostutellimuse oleku vaatamine

Tellimuste, mida saab saata cXML-i kaudu, kinnitamise puhul määratakse nende olekuks _Ootel_. Nagu kirjeldati jaotises [Ostutellimuse loomine ja töötlemine](#create-po), saate vaadata ostutellimuse olekut lehel **Ostutellimustaotlus**. Igal ostutellimustaotlusel võib olla üks mitmest olekust sõltuvalt selle parameetritest ja andmetest. Selles jaotises kirjeldatakse eri olekutüüpe ja väärtusi, mis neil olla võivad. See teave aitab teil hallata probleeme ja mõista oma ostutellimuste olekut.

![Ostutellimuse olek ostutellimustaotluse lehel.](media/cxml-monitor-po-request.png "Ostutellimuse olek ostutellimustaotluse lehel")

Lehe **Ostutellimustaotlus** üleval olevas ruudustikus võivad olla järgmised olekuväärtused.

- **Tellimuse saatmise olek** – sellel väljal võib olla üks järgmistest väärtustest.

    - **Ootel** – dokument on saatmise ootel.
    - **Saadetud** – dokument on saadetud.
    - **Peatatud** – dokument märgiti enne saatmist _peatatuks_. (Dokumendi märkimiseks _peatatuks_ valige lehe **Ostunõue** toimingupaanil suvand **Peata**.)
    - **Arhiiv** – dokument on likvideeritud. (Dokumendi likvideerimiseks valige lehe **Ostunõue** toimingupaanil suvand **Likvideeri**.)

- **Tellimustaotluse hankija olek** – sellel väljal võib olla üks järgmistest väärtustest.

    - **Ootel** – dokument on saatmise ootel.
    - **Kinnitatud** – hankija on kinnitanud, et ta on dokumendi vastu võtnud. Saate hankija tagastatud XML-i teate üksikasju vaadata, kui valite lehe alumisest osast vahekaardi **Vastuse XML**.
    - **Tõrge** – dokument saadeti hankijale, kuid ilmnes tõrge. Saate tõrketeate üle vaadata, kui valite lehe alumisest osast vahekaardi **Vastuse XML**.

Lehe **Ostutellimustaotlus** alumises osas oleva vahekaardi **Ostutellimustaotluse ajalugu** ruudustikus võivad olla järgmised väärtused.

- **Tellimustaotluse tüüp** – sellel väljal võib olla üks järgmistest väärtustest.

    - **Uus** – rida märgitakse uueks kohe pärast ostutellimuse kinnitamist.
    - **Värskendus** – kui üks kinnitus on juba saadetud ja hankija on selle vastu võtnud, märgitakse järgmine kinnitus _värskenduseks_. Värskendusi saadetakse ainult juhul, kui suvandi **Saada ostunõude värskendusi** väärtuseks on [globaalsetes cXML-i parameetrites](#cxml-parameters) seatud *Jah*.
    - **Kustutamiseks** – kui kinnitus on saadetud ja hankija on selle vastu võtnud, kuid ostutellimus tühistatakse, märgitakse ootel kinnituse olekuks _Kustutamiseks_. Kustutusteateid saadetakse ainult juhul, kui suvandi **Saada ostunõude kustutusteade** väärtuseks on [globaalsetes cXML-i parameetrites](#cxml-parameters) seatud *Jah*.

- **Taotluse aeg** – tellimuse kinnituse loomise aeg. Saate võrrelda taotluse aega tellimuse oleku ajaga, et teha kindlaks kinnituse ja hankija vastuse vaheline aeg.
- **Tellimuse saatmise olek** – see väli on sama mis lehe ülemises osas olev väli **Tellimuse saatmise olek**. Seda korratakse siin, et lihtsustada oleku vaatamist kinnituse tasemel. Kui välja **Tellimustaotluse tüüp** väärtuseks on seatud *Uus* ja ostutellimus kinnitatakse uuesti enne kinnituse saatmist, seatakse välja **Tellimuse saatmise olek** väärtuseks *Arhiiv*.
- **Tellimuse oleku aeg** – aeg, mil ostutellimustaotluse ajaloo kirjet viimati värskendati. (Värskendused hõlmavad olekumuudatusi.)
- **Tellimustaotluse hankija olek** – see väli on sama mis lehe ülemises osas olev väli **Tellimustaotluse hankija olek**. Seda korratakse siin, et lihtsustada oleku vaatamist kinnituse tasemel.
- **Taasedastamise aeg** – kirje uuesti edastamise aeg.
- **Taasedastuste arv** – kirje taasedastuste arv. Kõrge arv tähendab mitut tõrget ja võib seega tähendada, et teie või hankija andmete seadistuses leidub probleem.

### <a name="view-the-xml-for-a-purchase-order-request-message"></a>Ostutellimustaotluse teate XML-i vaatamine

Ostutellimustaotluse teate XML-i vaatamiseks valige lehe **Ostutellimustaotlus** alumisest osast vahekaart **Vastuse XML-i tekst**. Sellel vahekaardil olev teave võib tulla kasuks testimisel või tõrgete korral. Teabe lugemise hõlbustamiseks saate seda vaadata vormindatud teatena. Kopeerige vahekaardi sisu tekstifaili ja vaadake seda XML-redaktoris.

![Taotluse XML-i teksti vahekaart.](media/cxml-request-xml-text.png "Taotluse XML-i teksti vahekaart")

### <a name="view-the-details-of-the-vendor-response"></a>Hankija vastuse üksikasjade vaatamine

Hankija kinnituse või tõrkevastuse sisu vaatamiseks valige lehe **Ostutellimustaotlus** alumisest osast suvand **Vastuse XML**.

![Vastuse XML-i vahekaart.](media/cxml-response-xml.png "Vastuse XML-i vahekaart")

## <a name="additional-resources"></a>Lisaressursid

- [Väliskataloogi seadistamine e-hanke väljaregistreerimiseks](set-up-external-catalog-for-punchout.md)
- [Väliskataloogide kasutamine e-hanke väljaregistreerimiseks](use-external-catalogs-for-punchout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
