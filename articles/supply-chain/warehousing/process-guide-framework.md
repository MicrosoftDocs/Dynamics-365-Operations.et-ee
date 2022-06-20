---
title: Protsessijuhendi raamistik
description: See artikkel annab teavet protsessijuhendi raamistiku kohta arendajatele, kes laiendavad meie lao mobiilseid protsesse X++is.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e88f32e0347a808d03615cf85e50b1592d691670
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860431"
---
# <a name="process-guide-framework"></a>Protsessijuhendi raamistik

[!include [banner](../includes/banner.md)]

See artikkel annab teavet protsessijuhendi raamistiku kohta arendajatele, kes laiendavad lao mobiilseid protsesse X++-s. Lao mobiilsed protsessid on laiendatavad, kuna protsessid on jaotatud väikesteks sammudeks. Iga sammu äriloogika ja kasutajaliidese ehitus on eraldatud üksikuteks klassideks, mis võimaldab laiendada.

## <a name="overview-of-the-existing-design"></a>Ülevaade olemasolevast kujunduses

Lao mobiilsed täitmise vood avaldatakse ühe kohandatud teenuse lõpp-punkti kaudu. Mobiilirakendusest saabub päring XML-stringina, mis sisaldab mobiiliäpis esitatava kasutajaliidese metaandmeid ning kasutaja poolt sisestatud väärtusi.

Kui päring on vastu võetud, on esimene samm selle XML-i deserialiseerimine. Klass **WHSMobileAppServiceXMLTranslator** teisendab XML-i konteineriks, mis sisaldab nii juht- kui ka seansi teavet.

Pärast seda kasutatakse konteineris olevat teavet, et järeldada, millise laoprotsessi kallal kasutaja töötab või hakkab kohe algama (mida kujutab **WHSWorkExecuteMode** numbriline loend) ja vastavalt sellele luuakse tuletatud klass **WHSWorkExecuteDisplay**. Käivitatakse meetod **displayform()**, mis seejärel teeb järgmist.

-   Töötleb kasutaja andmeid (delegeeritud **WHSRFControlData** klassi, kuid mõned protsessid rakendavad spetsiifilist loogikat, kirjutades üle meetodi **processControl()**).

-   Käivitab äriloogika.

-   Suurendab sammu.

-   Ehitab uut kasutajaliidest esindava konteineri (tavaliselt **ehitan…()** meetodil).

Seejärel tagastatakse konteiner tõlkijale, mis seejärel XML-i jada ja saadab selle vastusena mobiilseadmesse.

Järgmine jadaskeem näitab täitmisvoo ülevaadet. Pange tähele, et diagramm on pigem skemaatiline ülevaade ega kujuta endast tegelikku koodi 1:1.

![Protsessi skemaatiline ülevaade.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Disaini muutmise põhjus

Ülaltoodud disain pakub väga lihtsat raamistikku mobiilsetes voogudes kasutatavate protsesside ehitamiseks. Siiski, nagu ülalpool on näha, võtavad **displayform()** meetodid üle mitmed kohustused. See delegeerib need teistele meetoditele ja klassidele, kuid konkreetsete klassikohustuste puudumisel tehakse seda klasside lõikes ebajärjekindlalt. Kuna toetatud stsenaariumide arv kasvab orgaaniliselt, võivad mõned neist klassidest muutuda üsna keerukaks. Asja huvitavamaks muutmiseks tühistatakse mõned neist klassidest/meetoditest ja neid kasutatakse mitmes režiimis uuesti. Tulemuseks on ülipikad ja kõrge tsüklomaatilise keerukusega meetodid. Need on varem tekitanud hooldusprobleeme. Vigade parandamine nendes meetodites on olnud riskantne ja altis regressioonile.
Näiteks meetod **processWorkLine()** klassis **WhsWorkExecuteDisplay** on viidatud mitmest protsessist (põhimõtteliselt kõikjal, kus töö teostatakse).

Nende laiendatavaks muutmiseks oleks üks võimalus jagada **displayForm** meetodid väiksemateks meetoditeks ja lisada laiendatavuse punktid. Stsenaariumimaatriksi tõttu oleks aga partneritel keeruline laiendusi kirjutada ja regressioonide vastu valideerida. Vähe sellest, ülalmainitud struktureeritud vastutuse jaotuse puudumise tõttu kasvab kood aja jooksul ettearvamatult, tekitades probleeme kvaliteetsete laienduste ehitamisel.

Selle tulemusena on ümberkujundamine jätkusuutlik valik, mille eesmärk on selgelt määratletud klassid, millel on iseseisvad kohustused. Klassil peaks olema üks vastutus, üks põhjus muutuda ja üks põhjus, miks end pikendada.

## <a name="design-overview"></a>Kujunduse ülevaade

Uuendatud raamistikus keerleb põhistrateegia kahe põhimõtte ümber: jagage täitmisvoog üksikuteks komponentideks, millel on täpselt määratletud vastutus, ja omage igas komponendis täpselt määratletud laienduspunkte.

Uue raamistiku nimi on “ProcessGuide”. Selle põhjuseks on asjaolu, et nende klasside eesmärk on juhtida kasutajat läbi äriprotsessi (erinevalt teisest kliendist, millel on vormipõhine kogemus, kus kasutajal on suurem paindlikkus andmetega suhtlemise või toimimise järjekorras ülesanded).

> [!NOTE]
> Üks tähelepanuväärne detail on "WHS" eesliite tahtlik väljajätmine. Kui algselt võeti mobiilsed protsessid kasutusele laonduse jaoks, siis hiljem on need ületanud piire, toetades erinevaid tootmis- ja laohaldusprotsesse. Selle tulemusena jäeti raamistiku nimest välja lao viide.

Komponentide tuvastamiseks tuleb kõigepealt vaadata tootmise alustamise protsessi (**WhsWorkExecuteDisplayProdStart** klass). Siin on protsessi skeem.

![Skemaatilise protsessi pilt.](media/production-start-process-schematic.png)

Juhtimisvoogu arvestades on vaja järgmisi komponente:

-   Kontroller kogu äriprotsessi läbimiseks.
-   Samm, mis vastutab protsessi sammu täitmise eest.
-   Andmetöötleja andmete astmeliseks töötlemiseks.
-   Lehe koostaja, kes vastutab ühe etapi kasutajaliidese loomise eest.
-   Astmevahetuse eest vastutav navigatsiooniagent.
-   Äriprotsessi läbiviimise eest vastutav klass.

Kui alustate ülaltoodud protsessi vooskeemil 1. toimingust ja alustate eelmise etapi andmete töötlemist ning seejärel kasutajaliidese loomisega, jätkatakse andmete töötlemist järgmises etapis. See loob tiheda seose järjestikuste sammude vahel, mille tulemusena näeks meie uus kõrgetasemeline skeem välja järgmine:

![Skemaatilise kõrgtasemelise protsessi pilt.](media/high-level-schematic.png)

Järgmised on ümberkujundatud protsessi põhikomponendid:

-   **ProcessGuideController** - see klass korraldab äriprotsessi üldist täitmist. See määratleb tehased, mis instantseerivad sammu ja navigeerimisagendi, mis seejärel moodustavad protsessi täitmise, samuti protsessi tühistamise või väljumise puhastusloogika.

-   **ProcessGuideStep** - see klass esindab ühte sammu äriprotsessis. See klass sisaldab nende tehaste määratlust, mis loovad lehe koostaja, toimingud ja andmetöötlejad ning vastutavad nende õiges järjestuses käivitamise eest.

-   **ProcessGuideNavigationAgent** - see klass vastutab sammude vahel navigeerimise eest. Kui samm on lõpule viidud, vastutab navigatsiooniagent järgmise sammu määratlemise eest ja edastab kõik parameetrid, mida eelmine samm võib järgmisele edastada.

-   **ProcessGuidePageBuilder** - see klass vastutab kasutajaliidese käivitamise eest.

-   **ProcessGuideAction** - see klass tähistab toimingut, mida kuvatakse kasutajale nupuna.

-   **ProcessGuideDataProcessor** - see klass vastutab kasutaja sisestatud andmete töötlemise eest väljale.

## <a name="execution-flow"></a>Käivitamisvoog

Täitmisvoo alguspunkt jääb muutumatuks. Seega saabub taotlus ikkagi samade lõpp-punktide kaudu, millele järgneb XML-i deserialiseerimine konteinerisse. Konteiner siis suunatakse meetodisse **getNextFormState()**.

Tähelepanu väärivad kolm olulist klassi:

-  **ProcessGuideSessionState** - see sisaldab seansi olekuteavet – režiim, pääse, kontroller, sooritatav samm jne.

-  **ProcessGuidePage** - see sisaldab kasutajaliidese metaandmete tugevalt trükitud esitust.

-  **ProcessGuideRequest** - see sisaldab kahte ülalnimetatud liikmetena ja on mobiilseadmelt saadud päringu tugevalt tüpiseeritud esitus.

Need klassid luuakse konteineriteabe (nii oleku kui ka kasutaja sisestatud kontrollandmete) abil. See pakub tüübikindlat viisi väärtustele juurde pääsemiseks ja nendega manipuleerimiseks. Võrreldes konteineri korduva juurdepääsuga protsessi ajal, annab see kasu nii loetavuse kui ka jõudluse osas.

Seansi olekuteavet kasutatakse õige **ProcessGuideController** klassi jooksutamiseks. Pärast loomist käivitatakse klassis **ProcessGuideController** meetod **createResponse()**. See meetod on protsessijuhise loogika sisenemispunkt ja pärast täitmist naaseb vastusega (esindatud klassis **ProcessGuideResponse**). Seejärel teisendatakse vastus tagasi konteinerisse ja antakse tagasi pärandloogikale, mis seejärel järjestab selle XML-i ja saadab vastuse tagasi mobiilseadmesse.

Järgmisena peab kontroller leidma täitmiseks järgmise sammu. Kui see on uue protsessi algus, kutsub kontroller protsessi esimese sammu saamiseks välja meetodi **initialStep()**. Pärast seda kutsuks see **ProcessGuideStepis** meetodit **execute()**. See meetod loob seejärel klassi **ProcessGuidePageBuilder** ja kutsub esile **buildPage()**, mis tagastaks objektiga **ProcessGuidePage**, mis on kasutajale esitatava kasutajaliidese virtuaalne esitus. See samm saadaks tulemuse tagasi kontrollerile, mis seejärel salvestab praeguse seansi oleku ja tagastab tulemuse tagasi **getNextFormState()** klassi **ProcessGuideResponse** kujul. Seejärel teisendatakse vastus tagasi konteinerisse, seejärel jadatakse XML-vormingusse ja saadab vastuse mobiilseadmesse tagasi.

Järgmine jadaskeem selgitab seda juhtimisvoogu. Pange tähele, et see on kõige levinum juhtimisvoog, mis on disaini selgitamiseks lihtsustatud.

![Lihtsustatud juhtelemendi voog.](media/control-flow.png)

Kui kasutaja teeb mobiilseadmes toimingu, klõpsates nuppu (või skannib väärtust – mis tavaliselt käivitab vaiketoimingu), jõuab päring klassi **ProcessGuideController** meetodile **createResponse()** sama marsruut. Seekord aga teab kontroller seansi oleku info põhjal, millises etapis kasutaja on. Vastavalt sellele loob see sobiva **ProcessGuideStep** klassi ja käivitab täitmismeetodi. **ProcessGuideStep** omakorda loeb kasutaja poolt välja kutsutud toimingu nime ja loob seejärel sobiva **ProcessGuideAction** klassi ja kutsub esile **execute()**.

Klass **ProcessGuideAction** vastutab konkreetse toimingu täitmise eest, kuid on kaks märkimisväärset erandit.

Esimene on **ProcessGuideOKAction** klass. See toiming tähendab, et kasutaja soovib kinnitada ja protsessiga edasi liikuda. Vastavalt sellele – see meetod teeb tegelikult meetodijärgse klassi ProcessGuideStep, mis tähendab, et samm kutsub **ProcessGuideDataProcessor** klassis välja meetodi **processData()**. See töötleb kasutaja sisestatud andmeid, värskendab seejärel sammu olekut ja saadab tulemuse kontrollerile tagasi. Sõltuvalt protsessori tulemusest kutsub samm välja lehe koostaja sobiva kasutajaliidese loomiseks või määrab etapi oleku lõpetatuks. See kajastub alloleva järjestusdiagrammi ülemises pooles.

Teine erand on tühistamistoiming, mida rakendatakse klassides **ProcessGuideCancelResetProcessAction** ja **ProcessGuideCancelExitProcessAction**. Need toimingud kujutavad endast kavatsust protsess katkestada ja minna tagasi protsessi algusesse või protsessist täielikult väljuda. Sarnaselt toiminguga **OK** kutsuvad need toimingud tagasi ka sammule, mis annab kavatsusest märku **ProcessGuideControllerile**. Seejärel teostab kontroller vajaliku olekumuutujate puhastamise ja kas viib juhtimise protsessi algsesse etappi või lõpetab protsessi üldse.

Kui sammu olekuks on määratud **Lõpetatud**, instantseerib kontroller pärast toimingu lõpetamist **ProcessGuideNavigationAgent**, mis tagastab järgmise sammu nime. Seejärel käivitab kontroller selle sammu, kutsub välja meetodi **execute()** – ja tsükkel jätkub. Kõige sagedamini kutsub uus samm välja vastava **ProcessGuidePageBuilderi**, et luua kasutajaliides järgmise kasutajale esitatava ekraani jaoks, mis seejärel tagasi saadetakse. Seda voolu on kujutatud alloleva järjestusdiagrammi alumises pooles.

![järjestuse diagramm.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Uue protsessi loomine raamistiku ProcessGuide abil

Parim viis juhtimisvoo selgitamiseks on kasutada rakenduses olemasolevat näidet – tootmise alustamise protsessi.

## <a name="overview-of-the-production-start-process"></a>Ülevaade tootmise alustamise protsessist

Alustame protsessi voolu mõistmisest. Esimeses etapis küsitakse kasutajalt tootmistellimuse ID-d.

![Tootmis-ID teabeaken.](media/production-id-prompt.png)

Kui kasutaja sisestab tootmistellimuse ID, kinnitatakse tellimuse number. Mõned käitatavad kontrollimised põhinevad sellel, kas tellimus on samas laos, kuhu kasutaja on sisse logitud, ja tellimuse olekul. Kui valideerimine ebaõnnestub, kuvatakse kasutajale veateade. Kui valideerimine õnnestub, kuvatakse kasutajale tootmistellimuse ja kauba üksikasjad.

Kasutaja saab protsessi algusesse naasmiseks tühistada või kinnitamiseks klõpsata **OK**. Viimasel juhul seatakse tootmistellimus olekusse **Alustatud**, vastavad ajakirjad konteeritakse, juhtelement liigub tagasi esimese sammu juurde ja kasutajale kuvatakse teade “Töö lõpetatud”.


## <a name="creating-the-controller"></a>Kontrolleri loomine

Esimene samm äriprotsessi ülesehitamisel on kontrolleriklassi loomine, mis laiendatakse  **ProcessGuideController** abstraktsest klassist, mis kirjeldab kontrolleri vaikekäitumist. Klassi uus nimi on **ProdProcessGuideProductionStartController** ja seda kaunistab **WHSWorkExecuteMode** väärtus **StartProdOrder**. Kasutatakse sama **SysExtension**-põhist initsialiseerimist, mida kasutati klassides **WHSWorkExecuteDisplay**, mis aitab kontrollerit luua, kui kasutaja käivitab selle režiimi menüü-üksuse.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Klassi **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>kontrolleri** nimetamismuster. See on muster, mida kasutatakse kontrolleriklasside jaoks ja teiste klasside laiendamiseks.


## <a name="building-the-first-step"></a>Esimese sammu ehitamine

Järgmisena loote esimese sammu määratlemiseks klassi **ProdProcessGuidePromptProductionIdStep**, mis on laiendatud klassist **ProcessGuideStep**.

Klassi instantseerimise ülesanne on delegeeritud astmetehasele, mille kutsub välja **ProcessGuideController** põhiklass. Tehase vaikerakendus loob sammu nime alusel. Seetõttu peate kontrolleri esimese sammuna **ProdProcessGuidePromptProductionIdStep** loomiseks tegema kahte asja.

-   Täiustage klassi **ProcessGuidePromptProductionIdStep** atribuudiga **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   Rakendage kontrolleriklassis sammu nime tagastamiseks abstraktset meetodit **initialStepName()**.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Atribuudi **ProcessGuideStepName** väärtus ei pea täpselt vastama klassi nimele, nagu ülal näidatud. Selle rakendamine võimaldab aga klassi kasutamisel ristviidete ümber ühtlust ja tüübiohutust. Soovitatav on kasutada seda nimetamisviisi.
>
> Etapi **ProcessGuideStepName**-põhine teostus on rakendatud klassis **ProcessGuideStepDefaultFactory**. Harvadel juhtudel, kui soovite sammu käivitamiseks teistsugust strateegiat, peate tegema järgmist.
> -   Looge uus tehaseklass, mis pärineb klassist **ProcessGuidStepAbstractFactory**.
> -   Soovi korral looge uus parameetriklass, mis rakendab liidest **ProcessGuideIStepCreationParameters** ja sisaldab parameetreid, mida tehas vajab.
> -   Ülaltoodud tehase ja parameetrite tagastamiseks kirjutage üle oma kontrolleriklassis meetodid **stepFactory()** ja **stepCreationParameters()**.

Järgmine samm on klassi **ProdProcessGuidePromptProductionIdStep** funktsionaalsuse juurutamine. Peate rakendama kasutajaliidese koostamise, kasutaja sisestatud andmete töötlemise ja sammu lõppemise kindlaksmääramise loogika.

### <a name="building-the-user-interface-for-the-first-step"></a>Esimeseks sammuks kasutajaliidese loomine

Kasutajaliides on koostatud kasutades klassi, mis pärineb **ProcessGuidePageBuilder** abstraktsest klassist. Selle sammu jaoks määrake klassile nimi, mis esindab selle tegevust – **ProdProcessGuidePromptProductionIdPageBuilder**.

Klassi instantseerimismehhanism on sarnane sellega, kuidas samm kontrollerist instantseeriti. 

-   Täiustage klassi **ProdProcessGuidePromptProductionIdPageBuilder** atribuudiga **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   Rakendage klassis **ProdProcessGuidePromptProductionIdStep** selle nime tagastamiseks abstraktset meetodit **pageBuilderName()**.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Sarnaselt astmevabrikule on lehtede koostaja tehase jaoks rakendatud ka abstraktne tehasemuster. Nii et harvadel juhtudel, kui soovite lehe koostaja loomiseks teistsugust strateegiat, saate teha järgmist.
> - Looge uus tehaseklass, mis pärineb klassist **ProcessGuidePageBuilderAbstractFactory**.
> - Soovi korral looge uus parameetriklass, mis rakendab liidest **ProcessGuideIPageBuilderCreationParameters** ja sisaldab parameetreid, mida tehas vajab.
> - Ülaltoodud tehase ja parameetrite tagastamiseks kirjutage üle oma sammu klassis meetodid **pageBuilderFactory()** ja **pageBuilderCreationParameters()**.

Kasutajaliidese juurutamiseks vajate lehte, millel on üks tekstikast tootmistellimuse ID sisestamiseks, lisaks nupp **OK** ja nupp **Tühista**. Nupp **Tühista** peaks võimaldama väljuda protsessist.

Selle rakendamiseks peate klassis **ProdProcessGuidePromptProductionIdPageBuilder** üle kirjutama kaks meetodit:

-   Kasutage tekstikasti lisamiseks meetodit **addDataControls()**.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Nuppude **OK** ja **Cancel** lisamiseks kasutage meetodit **addActionControls()**.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

See lisab andmete juhtelemendid ja seejärel nupud. Kui aga soovite luua ekraani vahelduvate andmete juhtelementide ja nuppudega, saate paindlikkuse huvides selle asemel ülekirjutada meetodi **addControls()**.

Täiendav stsenaarium, mida kaaluda, on see, kuidas leht uuesti üles ehitada valideerimistõrgete korral, näiteks kui kasutaja sisestab vale tootmistellimuse ID. Põhiklass **ProcessGuidePageBuilder** rakendab vaikekäitumist, mis taastab kasutajaliidese, tühjendab skannitud väärtuse ja lisab veateate juurde veakontrolli. Kuna see on vaikekäitumine, mida soovite kasutada, ei pea te vigade käsitlemiseks koodi lisama.

> [!TIP]
> Kui soovite tõrkeolukordades rakendada kohandatud kasutajaliidese käitumist, saate üle kirjutada ühe või mitu **rebuildFromRequestPage()**, **isErrorState()** ja **reuseRequestPageOnError()** meetodit.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Kasutaja sisestatud andmete töötlemine esimeses etapis

Andmete töötlemine toimub **ProcessGuideDataProcessorDefault** klassis, mis omakorda käivitab pärandklassi **WhsRfControlData**. Seda vaikekäitumist pole vaja muuta ja **WhsRfControlData**-l on juba välja **ProdId** kinnitamise loogika, seega ei pea te selle käsitlemiseks loogikat kirjutama. Kui valideerimisloogika jaoks on vaja laiendusi, kaaluge **WhsControl**-põhise laiendusmehhanismi kasutamist.

### <a name="determine-if-the-first-step-is-complete"></a>Tehke kindlaks, kas esimene samm on lõpetatud

Kui valideerimine on edukas, on aeg märkida samm lõpetatuks. Seda tehakse põhiklassis, kuid sammu lõpetamise määramiseks peate tingimuse rakendama. Seda teeb järgmine ülekirjutatud meetod.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>2. samm: vaadake tellimuse üksikasju ja kinnitage

Protsessi teises etapis kuvatakse kasutajale ekraan tellimuse üksikasjadega. Kasutaja saab tootmistellimuse alguse kinnitamiseks klõpsata nupul **OK** või protsessi algusesse naasmiseks **Tühista**. Selle näite puhul nimetage sammuks **ProdProcessGuideConfirmProductionOrderStep** ja lehe koostaja klassiks **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Klass ProdProcessGuideConfirmProductionOrderStep näeb välja järgmine.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Kuna kasutaja ei sisesta siia väärtusi, ei pea te meetodit **isComplete()** üle kirjutama. Toiming on lõppenud, kui kasutaja klõpsab **OK**.

Lehe koostaja klass kirjutab üle kolme sildi lisamiseks meetodi **addDataControls()**. Esimene silt näitab tootmistellimuse ID-d, teine ​​sisaldab kauba teavet (nt kauba ID, mõõtmed või kirjeldus) ja kolmas sisaldab kogust ja mõõtühikut.

Seejärel tühistatakse **addActionControls()**, et lisada 2 nuppu – nupp **OK** ja nupp **Cancel**, et protsess tühistada ja selle algusesse tagasi minna.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> Selles artiklis on X++ meetodite jaoks sama lähtekood rakenduse sirvija abil. Filtreerige klassi nimi, paremklõpsake klassi nimel ja valige **Kuva kood**.

### <a name="step-3-start-the-production-order"></a>3. samm: tootmistellimuse alustamine

Kolmas samm on tootmistellimuse käivitamise äriloogika elluviimine. See samm erineb mõnevõrra eelmistest sammudest, kuna sellel sammul pole kasutajaliidest. See samm täidetakse vaikselt, kui kasutaja klõpsab eelmises etapis **OK**.

Abstraktne klass **ProcessGuideStepWithoutPrompt** rakendab selliste sammude jaoks vaikekäitumist. Seetõttu peaks praegune samm laiendama klassi **ProcessGuideStepWithoutPrompt** ja kirjutama üle meetodi **doExecute()**.

Järgmine koodinäide näitab klassi ja meetodi **doExecute()** rakendamist. Meetod lihtsalt hangib seansi olekust tellimuse ID ja kasutaja ID ning kutsub esile meetodi selle tootmistellimuse käivitamiseks.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Erandi korral tagab raamistiku erandi käsitlemise loogika protsessi tagasipööramise eelmisele etapile.

> [!NOTE]
> **addProcessCompletionMessage()** käivitamine lisab navigeerimisparameetritele teate „Töö lõpetatud”. Järgmine samm (eeldusel, et sellel on kasutajaliides) kuvab selle teate. Selle loogikaga tegelevad põhiklassid ja selle käitumise saavutamiseks ei pea protsessiklassidele konkreetset koodi lisama.


### <a name="building-the-navigation-through-the-steps"></a>Navigeerimise loomine läbi sammude

**ProcessGuideController** baasklass loob klassi **ProcessGuideNavigationAgentDefault**, mis tugineb eelnevalt määratletud navigatsioonimarsruudile, mis on lihtne lähte- ja sihtkoha etappide kaart. Tootmise alustamise stsenaariumi jaoks piisaks sellest teostusest, kuna tingimuslikku hargnemist pole. Seetõttu peate navigeerimismarsruudi määratlemiseks üle kirjutama ainult meetodi **initializeNavigationRoute()**.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

On protsesse, kus toimub tingimuslik hargnemine (kasutaja toimingute või muude tingimuste alusel). Sellised protsessid peavad tegema järgmist:

-   Rakendage klassist **ProcessGuideNavigationAgent** päritud konkreetsed navigeerimisagendid.

-   Rakendage klassist **ProcessGuideNavigationAgentAbstractFactory** päritud spetsiifiline navigeerimisagendi tehas, mis sisaldab loogikat õige navigeerimisagendi loomiseks praeguse sammu, seansi oleku, kasutaja toimingu või muu loogika põhjal.

-   Soovi korral kirjutage üle sobivate parameetrite edastamiseks kontrolleriklassis meetod **navigationAgentCreationParameters()**.

-   Eespool loodud navigatsiooniagendi tehase käivitamiseks kirjutage kontrolleris üle meetod **navigationAgentFactory()**.

### <a name="action-classes"></a>Tegevusklassid

Toiminguklassid esindavad kasutaja toiminguid, nii et selles näites kasutatakse toimingute loomise viisi näitamiseks toimingut **OK**.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Klass peab rakendama 2 abstraktset meetodit:

-   **label()**, mis tagastab sildi, mis kuvatakse selle toiminguga seotud nupujuhtelemendis.

-   **doExecute()**, mis sooritab toimingu. Nagu varem mainitud, kutsub nupp **OK** lihtsalt esile toimingujärgse käsu. Kuid teistel toimingutel võib siin olla keerulisem loogika.

Toimingud luuakse **SysExtension** raamistiku abil, mis põhineb atribuudil **ProcessGuideActionName**. Sarnaselt leheehitajate instantseerimisega rakendab astmeklass vaiketoimingute tehast ja seda on võimalik üle kirjutada. Lehe koostaja lisab sellise nupujuhtimise.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Seda tehes palub see sammul luua edasiantud nimele toiminguklass ja seob selle toimingu nupuga.

### <a name="summary"></a>Kokkuvõte

Et summeerida kõik selles artiklis kirjeldatud, on siin protsessi jaoks vajaliku koodi täielik kokkuvõte:

1.  **ProdProcessGuideProductionStartController**

    1.  Kirjuta üle **initialStepName()**, et anda esimesele sammule nimi.
    2.  Navigeerimiskaardi koostamiseks kirjuta üle meetod **initializeNavigationRoute()**.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Kirjuta üle **isComplete()**, et määrata, millal etapp loetakse lõpetatuks.
    2.  Kasutatava lehe koostaja määramiseks kirjuta üle **pageBuilderName()**.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Tekstikasti **Prod ID** lisamiseks meetodit **addDataControls()**.
    2.  Nuppude **OK** ja **Cancel** lisamiseks kirjutage üle meetod **addActionControls()**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Kasutatava lehe koostaja määramiseks kirjuta üle **pageBuilderName()**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Tellimuse, kauba ja koguse teabe siltide lisamiseks kirjutage üle meetod **addDataControls()**.

    2.  Nuppude **OK** ja **Cancel** lisamiseks kirjutage üle meetod **addActionControls()**.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Meetod **generateItemInfoForProdId(),** mida kasutatakse kauba teabesiltide loomiseks, jäetakse sellest artiklist välja. See meetod teeb päringu mõnest tabelist, et saada üksuse ID, kirjeldus ja mõõtmed. Kui soovite funktsiooni **generateItemInfoForProdId()** paremini mõista, vaadake lähtekoodi.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Kirjutage üle **doExecute()**, et käivitada tootmisprotsess ja lisada protsessi lõpetamise teade.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Pange tähele, et paljud levinumad mustrid (kasutajaliidese taastamine vea korral, protsessi lõpuleviimise teade, **OK** ja **Tühista** käitumine) on viidud raamistikku, säästes nii rakenduse arendajat standardkoodi kirjutamisest, mis suurendab nii vigate teket kui ka sellel on oht protsesside vahel ebajärjekindlaks käitumiseks. Kui stsenaarium peab siiski tavapärasest teest kõrvale kalduma, antakse rakenduse arendajale võimalus sobivate meetodite üle kirjutamiseks – kuid siis on see tahtlik kõrvalekalle, mis on nii selgesõnaline kui ka jälgitav.


### <a name="extending-a-business-process"></a>Äriprotsessi laiendamine

Seni on see artikkel välja tõstetud, kuidas processGuide'i raamistikku kasutades **uut protsessi** luua. Sellest viimasest jaotisest leiate mõned näited selle äriprotsessi laiendamise kohta.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Voo sammu lisamine (kasutades ProcessGuideNavigationAgentDefault klassi)

Kuhu laiendada:

-   Protsessi **ProcessGuideController** klassi alamosa.

Kuidas laiendada:

-   Laiendage kontrolleriklassis meetodit **initializeNavigationRoute()** ja kutsuge klassis **ProcessGuideNavigationRoute** välja meetod **addFollowingStep()**.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Voo etapi lisamine (kasutades kohandatud navigeerimisagenti)

Kuhu laiendada:

-   **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent** alamosa.

Kuidas laiendada:

-   Looge **ProcessGuideNavigationAgent** uus alamklass, mis tagastab soovitud sammu nime.

-   Looge **ProcessGuideNavigationAgentFactoryst** tulenev uus klass, mis tagastab tingimuslikult ülal loodud navigeerimisagendi.

-   Laiendage kontrolleriklassis meetodit **navigationAgentFactory()**, et tagastada ülal loodud tehas.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Lisage olemasoleva sammu kasutajaliidesesse uus juhtelement 

Kuhu laiendada:

-   Sammu **ProdProcessGuidePageBuilder** alamosa.

Kuidas laiendada:

-   Laiendage meetodit **addDataControls()** ja lisage täiendav juhtelement.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Kasutajaliidese täielik uuendamine olemasolevas etapis

Kuhu laiendada:

-   **ProdProcessGuideStep** alamosa.

Kuidas laiendada:

-   Looge klassist **ProdProcessGuidePageBuilder** uus alamklass ja rakendage soovitud kasutajaliides.

-   Laiendage sammuklassis meetodit **pageBuildeName()**, et tagastada ülal loodud klassi atribuut **ProcessGuidePageBuilderName**.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Muutke loogikat, kui etapp loetakse lõpetatuks

Kuhu laiendada:

-   **ProdProcessGuideStep** alamosa.

Kuidas laiendada:

-   Täiendava loogika loomiseks laiendage meetodit **isComplete()**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]