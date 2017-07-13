---
title: "Dynamics AX 2012 versioonitäiendus versiooniks Dynamics 365 for Finance and Operations, Enterprise edition"
description: "Selles teemas kirjeldatakse protsessi, mida kliendid, kellel praegu töötab Microsoft Dynamics AX 2012, saavad kasutada oma andmete ja koodi üleviimiseks rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: et-ee
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Microsoft Dynamics AX 2012 versioonitäiendus versiooniks Microsoft Dynamics 365 for Finance and Operations, Enterprise edition

[!include[banner](../includes/banner.md)]

Platvormivärskenduses 8 annab Microsoft Dynamics 365 for Finance and Operations, Enterprise edition versioonitäienduse tee, mida kliendid, kellel praegu töötab Microsoft Dynamics AX 2012, saavad kasutada oma andmete ja koodi üleviimiseks versiooni Finance and Operations. Versioonitäiendus on rajatud järgmistele elementidele.

- Tööriistad, mis aitavad olemasoleva kohandatud rakendusekoodi AX 2012-st üle tuua.
- Andmete täiendusprotsess, mida võite kasutada oma andmebaasi ületoomiseks. Seetõttu on võimalik täiendada kogu kandeajalugu.

## <a name="overview"></a>Ülevaade

Üldist täiendusprotsessi saab visualiseerida kolme üldfaasina: analüüsimine, käivitamine ja valideerimine.

Järgmisel skeemil on näidatud kogu versioonitäienduse protsess ja tegevused, mida käsitleme iga faasi osana. 

![Täiendusprotsess](./media/upgrade-process.png)

## <a name="analyze"></a>Analüüsi

Analüüsimise faasi tegevused aitavad hinnata versioonitäienduse jaoks vajalikku panust. Need aitavad teil ka projektiplaani koostada. Need toimingud saab teha enne Finance and Operationsi ostmist. Need aitavad teil teha teadliku ostuotsuse, pakkudes andmepunkti panuse ja ressursside kohta, mida teil vaja läheb.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>LCS-is avaliku eelvaate jaoks registreerumine

Analüüsimistegevuste tegemiseks enne Finance and Operationsi ostmist võite registreeruda avaliku eelvaate saamiseks. Avalik eelvaade võimaldab teil juurutada oma Finance and Operationsi keskkondi. See annab teile ka juurdepääsu teenuse Microsoft Dynamics Lifecycle Services (LCS) tööriistadele, mida kasutatakse teie AX 2012 keskkonna ja olemasoleva kohandatud koodi hindamiseks.

Kui teil on AX 2012 jaoks olemasolev LCS-i projekt, peate Finance and Operationsi hindamiseks siiski registreeruma uues projektis.

Lisateavet selle kohta, kuidas saada klientide jaoks avalikku eelvaadet, leiate lehelt https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Lisateavet selle kohta, kuidas saada partnerite jaoks avalikku eelvaadet, leiate lehelt https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Arvestage, et see avalik eelvaade erineb [30-päevasest prooviversioonist](https://aka.ms/D365OperationTrials). Kolmekümnepäevased prooviversioonid annavad Finance and Operationsi juurutatud versiooni, mida saate kasutada rakenduse uurimiseks ja hindamiseks. Kuid analüüsitegevused nõuavad terviklikku LCS-i kogemust ja tööriistu.

### <a name="select-the-upgrade-methodology"></a>Valige versioonitäienduse metoodika
Määrake oma uues LCS-i projektis projekti metoodikaks **Versiooni AX 2012 täiendamine versiooniks Dynamics 365 for Operations**. See metoodika on koostatud spetsiaalselt versiooni täiendavatele AX 2012 klientidele. Selles kirjeldatakse üksikasjalikult kolme faasi ja antakse lingid kõigisse protsessi tugidokumentidesse.

![Versioonitäienduse metoodika(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Käivitage versioonitäienduse analüüsija
Versioonitäienduse analüüsimistööriist töötab AX 2012 keskkonna suhtes ja tuvastab ülesanded, mis tuleb täita AX 2012 keskkonna ettevalmistamiseks, et muuta versiooni täiendamise kogemus sujuvamaks ja odavamaks.

- **Andmete puhastamine** – see protsess aitab tuvastada andmed, mille võite funktsioone kaotamata eemaldada. See tööriist tuvastab mitmesugust tüüpi andmed, mida saate puhastamisprotsessiga vähendada. Iga andmetüübi puhul antakse selgitus puhastamise mõju kohta. Saate seejärel valida, kas käivitada puhastamisprotsess. Osa teie Finance and Operationsi tellimuse kulust põhineb andmebaasi suurusel. Seega vähendate suurust vähendades selle tellimusekomponendi maksumust ja aitate vähendada ka versioonitäienduse kasutuselevõtmisele kuluvat aega. Väiksem andmebaas aitab tagada kiirema versioonitäienduse.
- **SQL-i konfiguratsioon** – see protsess vaatab üle SQL-i konfiguratsiooni ja soovitab optimeerimisi. Veendudes, et SQL töötab optimaalselt, aitab see protsess vähendada versioonitäienduse kasutuselevõtmiseks vajalikku aega.
- **Kasutuselt kõrvaldatud funktsioonid** – see protsess tuvastab funktsioonid, mida praegu kasutate, kuid mis ei ole rakenduses Finance and Operations saadaval. Seega aitab protsess teil funktsioonide lünki aegsasti avastada. Samuti soovitab see alternatiive.

Lisaks peate selles etapis installima AX 2012 keskkonda kiirparanduse KBXXXXXXX. See kiirparandus annab täiendamiseelse kontroll-loendi. AX 2012 keskkonnas saate kasutada seda kontroll-loendit versioonitäienduse protseduuri jaoks vajalike andmete sisestamiseks. Näiteks saate ühes täiendamiseelse kontroll-loendi toimingus anda Microsoft Azure Active Directory (Azure AD) sisselogimisteabe iga praeguse AX 2012 kasutaja kohta, et iga kasutaja saaks Finance and Operationsisse sisse logida.

Selle etapi väljundist saab AX 2012 süsteemiadministraatorite jaoks versioonitäienduse projektiplaani töövoog.

Lisateavet leiate jaotisest [Analüüs: versioonitäienduse analüüsija kasutamine migreerimistöö plaanimiseks](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>Kooditäienduse hindamistööriistade käitamine
See toiming võtab AX 2012-st teie koodi, teisendab selle uude vormingusse ja annab tagasisidet konfliktide kohta, mille arendaja peab hiljem lahendama. Sellel toimingul põhineb teie kooditäienduse kulukalkulatsioon.

Selle toimingu tegemiseks tuleb eksportida kood AX 2012-st mudelilao ekspordina ja laadida see üles LCS-i kooditäienduse tööriista. Kooditäienduse tööriist koostab teie koodist täiendatud versiooni ja aruande järelejäänud konfliktide kohta, mis tuleb lahendada. Teie arendaja saab siis vaadata üle nii täiendatud koodi kui ka aruande, et määrata panus, mis on teie koodibaasi täiendamiseks vajalik.

Selle etapi väljund on teie Microsoft Dynamics AX-i arendajate jaoks versioonitäienduse projektiplaani töövoog.

Lisateavet leiate teemast [Analüüs: koodi täiendamise panuse hindamine](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Demokeskkonna juurutamine
Demokeskkonnad on vaikekeskkonnad, mis sisaldavad demoandmeid (mitte teie enda andmeid) ja standardkoodi (ilma kohandusteta). Soovitame demokeskkonna juurutamist uute funktsioonide hindamiseks ja AX 2012-s kasutatavate (kuid Finance and Operationsis võib-olla muutunud) standardprotsesside üldise sobivuse erinevuste analüüsi tegemiseks. Võite juurutada need demokeskkonnad Azure’is või laadida need alla teie oma riistvaral töötava virtuaalse seadmena (VM). Kui juurutate need Azure’is, peate esitama oma Azure’i tellimuse, kuna kasutate ikka veel avalikku eelvaateprojekti ega ole veel Finance and Operationsi tellimust ostnud.

Selle etapi väljund on teie funktsionaalsete kasutajate või ärikasutajate jaoks versioonitäienduse projektiplaani töövoog.

Lisateavet leiate jaotisest [Analüüs: liivakastikeskkonna juurutamine](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Projektiplaani loomine
Versioonitäienduse metoodikas antakse projektiplaani mall. Selles etapis kasutatakse eelmiste toimingute analüüsi faasi väljundit täiendusprojekti projektiplaani täitmiseks. Projektiplaani sisaldab ka kõiki testimise üksikasju: andmetäienduse testimine, ülemineku testimine, funktsionaalse testi läbimise kordused ja mitmesugused ressursimääramised nende toimingute jaoks.

Selles etapis annab projektiplaan andmepunkti, mis võib aidata teil mõista aega ja kulu, mis on Finance and Operationsile üleminekuga seotud.

## <a name="execute"></a>Täida
Käivitamisfaasis täidate ülesanded, mida analüüsimise faasis plaanisite. Käivitamise faasi liikumiseks tuleb osta Finance and Operations ja teil peavad olema olemas ressursid, kes saavad versioonitäiendusega töötada.

### <a name="switch-to-the-lcs-implementation-project"></a>LCS-i juurutusprojektile üleminek
Avaliku eelvaate projekt, mida analüüsi faasis kasutasite, on oma eesmärgi täitnud. Võite sellest nüüd loobuda. Ülejäänud etappides on vaja ainult projektiplaani, mille analüüsimise faasi viimases sammus koostasite.

Kui ostate Finance and Operationsi tellimuse, siis saate üksikasjad selle kohta, kuidas uue LCS-i projekti jaoks registreeruda. Seda projekti nimetatakse juurutusprojektiks ja see on teie tellimuse uus püsiv LCS-i projekt, kuni teil tellimus on. See projekt erineb avalikust eelvaateprojektist selle poolest, et seda haldab Microsoft. Seetõttu on sellel projektil järgmised omadused.

- Kõiki projekti keskkondi majutatakse Azure’is.
- Projektiga seotud Azure’i tellimust haldab Microsoft. Seetõttu ei esitata Azure’i kulude eest eraldi arveid. Need kulud katab teie Finance and Operationsi tellimus.
- Projekti tootmiskeskkonda haldab Microsoft. Seega teeb koodijuurutusi, versioonitäiendusi ja infrastruktuuri hooldust otse Microsoft, mitte teie töötajad. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>AX 2012 ettevalmistamistoimingute tegemine
Tehke toimingud, mille versioonitäienduse analüüsimistööriist avastas ja mis on teie täienduse projektiplaanis dokumenteeritud. Need toimingud peavad tegema teie Microsoft Dynamics AX-i süsteemiadministraator ja andmebaasi administraator (DBA).

[Andmetäiendus AX 2012-st Dynamics 365 for Operationsiks – täiendamiseelne kontroll-loend AX 2012-s](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>Kooditäienduse tegemine
Tehke toimingud, mis plaaniti analüüsimisfaasi kooditäienduse hindamise etapis. Teie arendajad peavad need toimingud käivitama.

Sellest punktist edasi tuleb koodimuutused AX 2012-s külmutada. AX 2012-s peaks koodi muutmine olema lubatud ainult hädaolukorras. Kui muudatus on tehtud, tuleb see käsitsi uude koodibaasi edastada.

### <a name="develop-new-code"></a>Uue koodi väljatöötamine
Tehke toimingud sobivuse erinevuste analüüsist, mis tehti analüüsimise faasi etapis Demokeskkonna juurutamine. Need ülesanded on tõenäoliselt segu funktsionaalsetest toimingutest, mis määratlevad konfiguratsiooni ja arendustegevused kohanduste jaoks, mis on seotud uute funktsioonidega, mis kasutusele võetakse.

### <a name="data-upgrade-development-environment"></a>Andmetäiendus (arenduskeskkond)
Pärast kooditäienduse toimingute tegemist võite täiendada AX 2012 andmebaasi esimest korda Finance and Operationsiks. Esimene versioonitäiendus toimub arenduskeskkonnas, et saaksite hõlpsamini parandada või siluda probleeme, mis selles etapis ilmnevad. Arenduskeskkonnas saab probleemi kohe siluda, koodi saab kohandada ja versioonitäienduse minutitega uuesti käivitada. Suuremad liivakastikeskkonnad sellist paindlikkust ei võimalda ja probleemide silumiseks ning parandamiseks, koodi uuendamiseks, uuendatud koodi juurutamiseks ja uuesti käitamiseks on vaja vähemalt mõnda tundi.

Järgmine illustratsioon näitab seda protsessi. Varundage lihtsalt AX 2012 andmebaas, laadige see Azure’i üles, taastage see Finance and Operationsi keskkonda ja käivitage siis andmetäiendus.

![Andmetäiendus arenduskeskkonnas](./media/data-upgrade-dev.png)
 
Andmetäiendus tehakse spetsiaalset tüüpi juurutatava paketi kaudu. Sama mehhanismi saab kasutada uue Finance and Operationsi koodi juurutamiseks ühest keskkonnast teise.

Alusraamistik, mida kasutatakse andmete teisendamiseks andmebaasis selle protsessi käigus on suures osas sama, mis täiendamisraamistik AX 2012-s, mis põhineb klasse **ReleaseUpdatexxx** käitavatel X++ pakett-töödel.

Üksikasjad leiate jaotisest [Andmetäiendus AX 2012-st Dynamics 365 for Operationsiks arenduskeskkonnas](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Andmetäiendus (liivakastikeskkonnad)
Kui andmetäiendus arenduskeskkonnas on lõpule viidud, saab sama protsessi käivitada liivakastikeskkonnas. Liivakastikeskkond on keskkond, kus ärikasutajad ja funktsionaalse töörühma liikmed saavad äriprotsesse testida, kasutades täiendatud AX 2012 andmeid ja koodi.

Järgmisel illustratsioonil on näidatud liivakastikeskkonnas andmetäienduse käitamise protsess. Erinevus seisneb selles, et tavapärase SQL-i varundamise asemel kasutatakse Bacpaci tööriista. See tööriist on vajalik Microsoft SQL Serveri ja Azure SQL-i andmebaasi vaheliseks teisendamiseks. See on standardne SQL-i tööriist ning ei ole Finance and Operationsi põhine.

![Andmete versioonitäiendus liivakastikeskkonnas](./media/data-upgrade-sandbox.png)

Üksikasjad leiate jaotisest [Andmetäiendus AX 2012-st Dynamics 365 for Operationsiks liivakastikeskkonnas](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Kontrolli
Kui sisenete valideerimisfaasi, on teil keskkonnad, mis sisaldavad teie täiendatud kohandatud koodi ja täiendatud andmeid. See faas kirjeldab valideerimise ja testimise protsessi, kas täiendatud keskkond toimib soovitud viisil. Samuti kirjeldab see kasutuselevõtuks valmistumise protsessi.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Tehke ülemineku testimine ja koostage üleminekuplaan
Mõistet _üleminek_ kasutatakse siin uue süsteemi kasutuselevõtu lõpliku protsessi kirjeldamiseks. See protsess koosneb ülesannetest, mis toimuvad pärast AX 2012 väljalülitamist ja enne Finance and Operationsi sisselülitamist. 

Testimise eesmärk on üleminekuprotsessi harjutamine. Sel viisil saate tagada, et kõik, kes on tegeliku üleminekuga seotud, saaksid sujuva kogemuse.

On kaks peamist töövoogu.

- **Tehniline töövoog** – see töövoog on andmetäienduse käivitamisprotsess. Teie ettevõte rakendab lubatud seisuaja hulgale piirmäära. Selle seisuaja jooksul ei ole AX 2012 ega Finance and Operations saadaval. Tehnilisel töövool võib olla vaja ettevõtte seisuaja piiride järgimiseks andmete versioonitäienduse protseduuri jõudlust häälestada. 
- **Funktsionaalne töövoog** – pärast andmetäiendust on Finance and Operationsi keskkonnas vaja teha mitu konfigureerimistoimingut. Kõik need toimingud tuleb dokumenteerida ja kvantifitseerida ning neile tuleb määrata ressurss, kuna need peavad sobima kokku tehniliste ülesannetega ettevõtte seisuaja piirides.

Üksikasjade kohta vt teemat 
- [Valideerimine: ülemineku testimine](upgrade-cutover-testing.md)
- [Valideerimine: rakenduse valideerimisprotsess](app-validation-process.md)

### <a name="functional-test-pass"></a>Funktsionaalse testi läbimine
Läbige kõigi äriprotsesside puhul täielik funktsionaalne testimine. See testi läbimine on kõigi Finance and Operationsit puudutavate äriprotsesside ulatuslik uuesti testimine. Need äriprotsessid hõlmavad nii vanu protsesse, mis toodi üle AX 2012-st, kui ka uusi protsesse, mis hõlmavad Finance and Operationsis esmakordselt kasutusele võetud uusi funktsioone. 

Olenevalt koodi kvaliteedist võib probleemi kõrvaldamine ja uuesti testimine nõuda mitut funktsionaalse testi läbimise kordust. Kui probleem on lahendatud, testige kindlasti uuesti kõiki seonduvaid protsesse, garanteerimaks, et muudatus ei mõjuta eelnevat või järgnevat protsessi.

Üksikasjad leiate jaotisest [Valideerimine: funktsonaalne testimine](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Kasutuselevõtueelne kontroll-loend
Kasutuselevõtueelne kontroll-loend on soovituslik protseduur, mis võib aidata vähendada vigade esinemise võimalust lõpliku üleviimise käigus kasutuselevõtmiseks. Üks nädal enne kasutuselevõtu tähtaega peatage AX 2012-s konfiguratsioonimuudatused (st \<moodulis\>\Seadistus). See konfiguratsioonimuudatuste piirang on üksnes protseduuriline. Microsoft Dynamics AX-i süsteemiadministraatorid nõustuvad lihtsalt selles punktis seda tüüpi muudatused ootele panema.

Soovitame teil ka Finance and Operationsi koodibaasis koodide muutmise külmutada. Edasist muutmist ei tohiks lubada, v.a juhul, kui neid on hinnatud ja on teada, et need ei takistaks kasutuselevõtmist.  

Pärast konfigureerimispiirangu seadmist ja koodi külmutamist tuleb andmetäiendus enne kasutuselevõttu viimast korda käivitada. Sel viisil saate tagada, et kõik töötab endiselt oodatud viisil. 

Üksikasjad leiate teemast [Valideerimine: ettevalmistamine süsteemi kasutuselevõtuks](upgrade-go-live-prep.md).



### <a name="supported-upgrade-paths"></a>Toetatud täiendusteed
Alates 2017. aasta juunist toetatakse Microsoft Dynamics AX 2012 R3-s täiendamist Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni versiooniks 0617. Toetatakse kõiki AX 2012 R3 kumulatiivseid värskendusi.

Microsoft Dynamics AX 2012 R2 ja Microsoft Dynamics AX 2012 RTM-i praegu ei toetata. Tugi lisatakse 2017. aasta jooksul.

Toetatakse ainult täiendamist Finance and Operationsi pilves juurutatud versiooniks. Täiendamist asutusesiseseks versiooniks ei toetata. Asutusesiseseks versiooniks täiendamise tugi lisatakse 2017. aasta jooksul.

