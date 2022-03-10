---
title: Tööta funktsiooniseadistustega
description: See teema kirjeldab, kuidas seadistada elektroonilise arveldamise funktsioone.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 41ffc9c7009291a55392e50c5e490d3288d122bc
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371866"
---
# <a name="work-with-feature-setups"></a>Tööta funktsiooniseadistustega

[!include [banner](../includes/banner.md)]

Elektrooniliste failide ja muude töötlusetappide loomise seadistamine (nt digitaalselt allkirjastatavate failide esitamine, nende esitamine valitsuse veebiteenusele ja vastuse saamine või nende talletamine) seadistage müügivõimaluste, kohaldatavusreeglite ja muutujate seadistamine elektroonilise arveldamise funktsioonide jaoks.

Seadistusteave kombineeritakse funktsiooni seadistuse *mõistes* ning seda saab luua, kustutada, korrigeerida. Lõpuleviidud elektrooniliste arveldusfunktsiooni versioonide puhul saab teavet vaadata ka.

Saate luua nii palju funktsiooni seadistusüksusi, kui vajate erinevate stsenaariumite määratlemiseks elektrooniliste failide loomiseks, töötlemiseks ja vastuvõtuks. Kuigi nende funktsiooni seadistamise üksustel on täitmiseks sõltumatud töötlemistoimingud ja -tingimused, luuakse need osana ühest elektroonilise arvelduse funktsioonist ja pärivad selle elutsükli ja juurutusprotsessi.

## <a name="add-a-feature-setup"></a>Funktsiooni häälestuse lisamine

1. Logige oma teenuse Regulatory Configuration Service (RCS) kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .
3. Elektroonilise arveldamise **funktsioonide lehel** valige elektroonilise arveldamise funktsiooni versioon, mille olek on **Mustand**.
4. Vahekaardil Seadistused **valige** lisa **·**.
5. **Valige väljagrupi Uus** funktsiooniseadistuse **ripploendist** üks järgmistest suvanditest:
 
    - **Kohandatud häälestus** : looge uus funktsiooniseadistus, kus on tühjad kanalid, tühi töötlusvõimaluste loend, kohaldatavusreeglite tühi jaotis ja vaikemuutujate kogum, sõltuvalt häälestuse tüübist.
    - **Funktsiooni seadistusest** – looge koopia teisest funktsiooniseadistusest praeguse elektroonilise arvelduse funktsiooni ulatuses.

6. Kui valisite **viimases** sammus valiku Kohandatud seadistus, **sisestage funktsiooni seadistuskauba nimi ja kirjeldus ning seejärel valige jaotises Seadistuse** tüüp üks järgmistest suvanditest:

    - **Müügivõimaluste töötlemine** – valige see suvand väljaminevate elektrooniliste dokumentide loomiseks ja töötlemiseks. Selle häälestustüübi puhul loob süsteem tühja töötlusvõimaluste loendi, kohaldatavusreeglite tühja jaotise ja vaikemuutujate komplekti. Te ei saa töötada sissetulevate elektrooniliste dokumentide kanalitega.
    - **Andmekanal** : valige see suvand, et seadistada sissetulevate elektrooniliste dokumentide vastuvõtmise protsess ühest määratud kanalist ja nende otse Microsoftile Dynamics 365 Finance Dynamics 365 Supply Chain Management või ilma lisatoiminguteta. Selle seadistustüübi puhul loob süsteem andmekanalite jaoks eelmääratletud parameetrite loendi, kohaldatavusreeglite tühja jaotise ja vaikemuutujate komplekti. Müügivõimaluste töötlemisega ei saa rohkem tegevusi lisada.
    - **Andmekanali ja konveieri** töötlemine – see seadistustüüp sarnaneb andmekanali **häälestuse** tüübiga. Kuid enne sissetuleva elektroonilise dokumendi saatmist finants- või tarneahela haldusse saate seadistada töötlemisliinis lisategevuse.

7. Kui valisite viimases **sammus** **suvandi Andmekanal või Andmekanal ja Müügivõimaluste töötlemine,** **peate valima väljal Andmekanali valimine kanali, et see integreerida.**
8. Valige **Loo**.

Pärast funktsiooniseadistuse loomist saate selle konfigureerimiseks **valida** suvandi Redigeeri.

## <a name="edit-a-feature-setup"></a>Funktsiooni häälestuse redigeerimine

Sõltuvalt funktsiooni häälestuse tüübist saate konfigureerida väljaminevate elektrooniliste failide loomise protsessi ja edastada need väliskanalitele, või sissetulevate dokumentide saamise ja nende edastamise oma finants- või tarneahela haldusrakendusele.

### <a name="data-channel"></a>Andmekanal

Andmekanal *võtab* elektroonilise faili ja töötleb või edastab selle otse finants- või tarneahela haldusse. Valik ei ole funktsiooni häälestustel saadaval, kui tüüp on **Müügivõimaluste** töötlemine.

Andmekanali häälestamiseks sisestage kanali nimi. Seejärel määrake parameetrid valitud kanali tüübi põhjal. Andmekanali identifikaator peab viitama muutujale, mis luuakse just andmekanali tuvastamiseks. Seda kasutatakse viitena finants- või tarneahelahalduses.

Vahekaardil Manuste **filter** peaksite määrama filtrite komplekti, et võtta konkreetseid faile kanalist. Võite luua mitu rida, kui eeldate, et failidel on erinevad failinime laiendid või kui faile tuleb töödelda faili nimest sõltuvalt teisiti. Siin on põhiparameetrid:

- **Nimi** : sisestage selle faili nimi, millele süsteem töötlemise ajal viitab. Finantside ja tarneahelate halduse rakendustes saate faile vaadata edastuslogist.
- **Filtreeri** – failide valimiseks määratlege filter.
- **Valikuline** – kui see ruut on tühi, on fail nõutav. Sel juhul näitab süsteem tõrketeadet, kui kanalid ei sisalda filtrile vastavates failides. See parameeter kehtib e-kirjade puhul.

Kui kanal on postkastiks ja sissetulev e-kiri sisaldab mitut manust, saate konfigureerida reeglid määramaks, kuidas teenus manuseid käsitseb. Teenus võib iga manust arvestada eraldi elektroonilise arvega või käsitleda üht manust põhiarvena ja kõiki teisi manuseid lisana.

### <a name="processing-pipeline"></a>Müügivõimaluse töötlemine

Konveiertöötlus *on* tegevuste *kogum*, mida käitatakse järjestikku seni, kuni need on edukalt lõpule viidud. Saate kasutada konveierit, et seadistada elektrooniliste failide loomise ja teiste sammude tegemise protsess (nt digitaalselt allkirjastavad failid, edastamine välistele veebiteenustele ning vastuse sõelumine ning sissetulevate dokumentide vastuvõtmine ja töötlemine).

Tegevuste loend on eelmääratletud. Saate kasutada nuppe **Uus** ja **Kustuta**, et määrata tegevuste kombinatsioon, mis loogiliselt määrab nõutava protsessi dokumentide edastamiseks või vastuvõtuks.

Tegevuste järjekord on oluline. Tellimust saate korrigeerida nuppude **Üles ja** **Alla abil**.

Igal tegevusel on parameetrite kogum, mida saate konfigureerida või korrigeerida. Kindel parameetrite kogum sõltub tegevuse tüübist.

- **Tegevus** : valige tegevuse tüüp.
- **Tegevuse** nimi – sisestage tegevuse nimi. See nimi kuvatakse edastuslogides ja finants- ja tarneahela haldusrakenduste teadetes.
- **Kirjeldus** – annab protsessi tegevuse eesmärgi kohta rohkem üksikasju.
- **Luba kordamine** – **·** **selle ruudu märkimisel saate valida tegevuse väljal Uuesti kordamine ja konfigureerida lisaparameetrid vahekaardil Uuestisatriksi** parameetrid.

    Kui kindlat tegevust ei saa käivitada, saate konfigureerida teenuse käitumist. Näiteks kui väline veebiteenus, millega püüate ühendust luua, ei vasta vasta, saate määrata, mitu korda süsteem ühenduse uuesti käivitab, millist intervalli ja millise intervalliga ja millise töötluse müügivõimaluste toiminguga.

- **Ekspordi tulemused** – selle ruudu saate valida ühe toimingu *jaoks* müügivõimaluste töötlemisel. Elektroonilist faili, mida tegevus finants- või tarneahela halduse rakenduses toodab, saab seejärel eksportida elektrooniliste dokumentide **esitamise logilehelt**.

### <a name="applicability-rules"></a>Rakendatavuse reeglid

*Kohaldatavusreeglid* on konfigureeritavad klauslid, mis pakuvad konteksti käitatavatele elektroonilise arveldamise funktsioonidele elektroonilise arveldamise võimaluse komplekti kaudu.
Äridokumendid, mis on edastatud finants- või hankeahela haldusest elektroonilisele arveldamiseks, ei saa kasutada selgesõnalist viidet, mis võimaldab elektroonilise arvelduse võimaluse seada kutsuma konkreetset elektroonilise arveldamise funktsiooniversiooni ja kindlat funktsiooniseadistuse üksust edastamise töötlemiseks. Kui äridokument on õigesti konfigureeritud, sisaldab see nõutavaid elemente, mis võimaldavad elektroonilise arveldamise, et määrata, milline elektroonilise arveldamise funktsiooni versioon ja müügivõimaluste töötlemine peab olema valitud ja käitatud.

Kohaldatavusreeglid võimaldavad elektroonilise arveldamise teenusel leida täpsed elektroonilise arveldamise funktsioonid, mida tuleb kasutada esitamise töötlemiseks. Õigete funktsioonide leidmiseks vastendatakse **edastatud** äridokumendi kontekstiväljad kohaldatavusreeglite klauslitega.

Kohaldatavusreeglitega saate töötada järgmistel viisidel:

- Valige **uus**, et lisada kohaldatavusreeglite komplekti uus tingimus.
- Tingimuse **kustutamiseks** klõpsake nuppu Kustuta.
- Valige mitu kirjet ja kasutage kaupade või **loogiliste** **lausete** kombinatsiooni loomiseks nuppu Grupp või Grupp. Näiteks valige grupeerida soovitud read ja seejärel grupi **tingimus**. Pärast klauslite rühmitamist lisatakse ruudustikku uus veerg. See veerg määrab grupeeritud tingimuse loogilise tehte. Toetatakse järgmisi tehtemärkide tüüpe:

    - Equal
    - Not equal
    - Suurem kui/väiksem kui
    - Suurem kui või võrdne / väiksem kui või võrdne
    - Contains
    - Algab viisil

    > [!NOTE]
    > Klausli rühmituse tühistamise korral alustage alati kõige sisemisest rühmitustasemest.

### <a name="variables"></a>Muutujad

*Muutujad* on paindlikumad, kui seadistate müügivõimaluste töötlemise ja tegevuste vahel andmevoo. Mõne tegevuseparameetri abil saate viidata muutujale andmete või elektrooniliste failide ajutiseks tallemiseks. Mõningaid muutujaid kasutatakse andmete edastamiseks finants- või tarneahela halduse rakenduste ja elektroonilise arvelduse teenuse vahel.

Süsteem loob vaikimisi mõned muutujad. Näiteks businessDocumentDataModel **muutuja sisaldab äriandmeid JavaScripti objekti notationi (JSON) struktuuris,** mis tuleb edastusprotsessi ajal ühendatud rakendusest.

Saadaval on järgmised muutujatüübid:

- **Konstant** – konteiner ajutiste andmete salvestamiseks, mida kasutatakse müügivõimaluste tegevuste töötlemisel.
- **Kliendist** – muutuja sisu soetakse Dynamics 365 kliendilt, kui edastusprotsess käivitatakse.
- **Kliendile** – muutuja sisu tehakse Dynamics 365 kliendi poolt importimiseks kättesaadavaks, kui edastusprotsess käivitatakse.
- **Andmetüüp** – valige muutujasse talletatava teabe andmetüüp.

### <a name="parameters"></a>Parameetrid

Suvand **Keela äriandmete vähendamine** kasutatakse äriandmete töökoormuse struktuuri optimeerimiseks, mis tuleb finantside või tarneahela halduse rakendusest elektroonilise dokumendiedastuse ajal. Optimeerimine aitab vähendada andmeid, mis lähevad elektroonilise arveldamise teenusesse edasiseks teisendamiseks nõutavasse elektroonilisse faili. Vaikeväärtus on **Ei**.

- **Jah** – finants- või tarneahela haldus saadab arvemudeli või **Fiskaalmudeli** **·**(Brasiilia) struktuuri JSON-faili, mis on määratletud elektroonilise **aruandluse moodulis.** Kõik mudeli elemendid täidetakse äriandmetega rakenduse poolel, olenemata lõplikust elektroonilisest failistruktuurist. Mudelid sisaldavad tavaliselt rohkem äriandmeid, kui sihtfaili struktuur nõuab ning nende andmete loomiseks rakenduses võib vaja olla rohkem aega. Selle suvandi puhul **on väärtus Jah** nõutud harvadel juhtudel, kui soovite luua erinevaid väljundfaile ühele elektroonilise arveldamise funktsioonile ja funktsiooni häälestusele. Väärtus Jah on **kasulik**, kui sooritate oma stsenaariumite tõrkeotsingut, elektrooniliste failide struktuuri ja äriandmete täielikkust.
- **Ei** – finants- või tarneahela haldus teeb teenusele esimese kõne ilma äriandmeteta. Selle kutse eesmärk on saada teavet elektroonilise aruandluse (ER) konfiguratsiooni kohta, mida kasutatakse elektroonilise faili teisendamiseks töötlusvõimalustes. See teave tagastatakse rakendusse, mis kasutab seda äriandmete alamkogumi määramiseks, mis tuleb kaasata arvemudeli või fiskaalmudeli (Brasiilia) struktuuri JSON-faili **·** **·**. Väärtus Ei selle **suvandi** jaoks aitab vähendada äriandmete mahtu, mida rakendus teenusele esitab, sest rakendus saab esitada ainult äriandmeid, mis on vajalikud elektroonilise faili edukaks loomiseks.

### <a name="validate-a-feature-setup"></a>Funktsiooni häälestuse valideerimine

Saate käivitada kinnitamise, et kontrollida kogu konfiguratsiooni ühtsust. Näiteks kui tegevuse kohustuslik parameeter on jäetud tühjaks, tuvastab kinnitamine selle vastuolu ja te saate hoiatusteate.

- **Funktsiooniversiooni häälestuslehe** tegevuspaanil valige **Kinnita**.

## <a name="delete-a-feature-setup"></a>Funktsiooniseadistuse kustutamine

1. Elektroonilise arveldamise **funktsioonide lehel** valige elektroonilise arveldamise funktsiooni versioon, mille olek on **Mustand**.
2. **Vahekaardil Seadistused** valige **kustuta**.
3. Kuvatavas teateaknas valige **Jah**, et kinnitada, et soovite funktsiooniseadistuse kustutada.
