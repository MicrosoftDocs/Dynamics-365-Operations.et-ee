---
title: Äridokumentide halduse ülevaade
description: Siin teemas on ER-raamistiku äridokumendi halduri kasutamisõpetus.
author: NickSelin
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5a57b96387ca5746a30b2e438d6b5f0ce3040f54
ms.sourcegitcommit: 728cd7f723ee821337eee315a27977e99a44d9d3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/11/2020
ms.locfileid: "3258553"
---
# <a name="business-document-management-overview"></a>Äridokumentide halduse ülevaade

[!include [banner](../includes/banner.md)]

Äriüksuse kasutajad kasutavad raamistikku [Elektrooniline aruandlus (ER)](general-electronic-reporting.md), et konfigureerida väljuvate dokumentide vorminguid erinevate riikide/regioonide õigusnõuete järgi. Kasutajad saavad määratleda ka andmevoo, et täpsustada, mis avalduse andmeid loodud dokumendid sisaldavad. ER raamistik loob eelmääratletud mallide abil väljuvaid dokumente Microsoft Office’i vormingutes (Exceli töövihikud või Wordi dokumendid). Mallid täidetakse nõutud dokumentide loomise ajal kohustuslike andmetega vastavalt seadistatud andmevoole. Kindlate väljuvate dokumentide loomiseks saab kõiki vorminguid avaldada ER-lahenduse osana. Seda tähistab ER-vormingu seadistus, mis sisaldab erinevate väljuvate dokumentide loomiseks kasutatavaid malle. Äriüksuse kasutajad saavad selle raamistikuga hallata vajalikke äridokumente.

**Äridokumendi haldus** on ehitatud ER-raamistiku peale ja võimaldab äriüksuse kasutajatel muuta äridokumendi malle Microsoft Office 365 teenuse või vastava Microsoft Office töölauarakendusega. Dokumentide muutmisel võib vahetada äridokumendi välimust ja lisada kohatäitjaid ilma lähtekoodi muutmata ja uute juurutusteta. Äridokumentide mallide värskendamine ei vaja teadmisi ER-raamistikust.

> [!NOTE]
> Arvestage, et äridokumendi haldus võimaldab muuta malle, mida kasutatakse äridokumentide, nt tellimuste, arvete jne koostamiseks. Kui malli on muudetud ja uus versioon on avaldatud, kasutatakse seda versiooni nõutavate äridokumentide loomiseks. Äridokumendi haldust ei saa kasutada juba loodud äridokumentide muutmiseks.

## <a name="supported-deployments"></a>Toetatud juurutused

Praegu kasutatakse äridokumendi halduse funktsiooni vaid pilve juurutamiseks. Kui see funktsioon on teie asutusesisese juurutuse puhul väga tähtis, andke meile sellest teada, andes tagasisidet [ideede](https://experience.dynamics.com/ideas/) lehele.

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused

Äridokumentide haldusega Exceli või Wordi vormingutes mallide muutmiseks Microsoft Office’i töölauarakendustega, peab teil olema paigaldatud Microsoft Office 2010 või uuem versioon. Seda toetatakse pilveteenuses ja asutusesiseses juurutuses.

## <a name="business-document-availability"></a>Äridokumendi saadavus

Järgmised Exceli-põhiste mallidega aruanded on saadaval avaliku eelvaate avaldamisega:

**Müügireskontro** (august 2019)

- Müügi ettemaksuarve
- Müügitellimuse saateleht

**Ostureskontro** (august 2019)

- Varasem ostuarve
- Ostutellimus
- Ostutellimuse saateleht

Avaldatakse veel rohkem aruandeid. Lisaaruannete eriteatised saadetakse eraldi. 

Kõigi 2019. aasta oktoobri väljalaske jaoks kavandatud aruannete põhjaliku loendi leiate teemast [Seadistatavate äridokumentide aruandlus Wordis ja Excelis](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details). Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide.

## <a name="configure-er-parameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

Kuna äridokumendi haldus põhineb ER-raamistikul, peate sellega töötamiseks seadistama ER-näitajad. Selleks peate seadistama elektrilise aruandluse parameetrid, nagu on kirjeldatud teemas [Elektrilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md). Peate lisama ka uue konfiguratsiooni pakkuja vastavalt teemale [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-tööruum](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Impordi ER-lahendused

Selle protseduuri näites on kasutatud elektroonilise aruandluse näidiskonfiguratsioone. Peate importima oma praegusesse Dynamics 365 Finance’i eksemplari elektroonilise aruandluse konfiguratsioonid, mis sisaldavad äridokumentide malle, mida saab äridokumentide haldust kasutades redigeerida. Selle protseduuri lõpule viimiseks laadige järgmised failid alla ja salvestage need seejärel seadmesse.

**ER-näidiskliendi arveldamislahendus**

| **Fail**                                  | **Sisu**                                |
|-------------------------------------------|--------------------------------------------|
| Kliendiarvete loomine model.version.2.xml    | [ER-i andmemudeli konfiguratsioon](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Customer FTI report (GER).version.2.3.xml | [Vabas vormis arve ER-vormingu seadistus](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**ER-näidismakse tšekkide lahendus**

| **Fail**                                  | **Sisu**                                |
|-------------------------------------------|--------------------------------------------|
| Model for cheques.version.10.xml          | [ER-i andmemudeli konfiguratsioon](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Cheques printing format.version.10.9.xml  | [Maksetšeki ER-vormingu seadistus](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

**ER-väliskaubanduse näidislahendus**

| **Fail**                                  | **Sisu**                                |
|-------------------------------------------|--------------------------------------------|
| Intrastat model.version.1.xml             | [ER-i andmemudeli konfiguratsioon](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Intrastat report.version.1.9.xml          | [Intrastati kontrollaruande ER-vormingu seadistus](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Kasutage iga faili importimiseks järgmist protseduuri. Enne vastava ER-*vormingu* seadistuse importimist importige allolevates tabelites olevate kõikide ER-lahenduste ER-*andmemudeli* seadistus.

1. Avage jaotis **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \>  leht **Konfiguratsioonid**.
2. Valige lehe ülaosas **Vaheta**.
3. Valige **Laadi XML-failist**.
4. Vajaliku XML-faili laadimiseks valige **Sirvi**.
5. Seadistuse impordi kinnitamiseks valige **OK**.

![ER-seadete leht](./media/BDM-Overview-ERSolutions.png)


Teise võimalusena saate importida ametlikult avaldatud ER-vormingu konfiguratsioonid platvormilt Microsoft Dynamics Lifecycle Service (LCS). Näiteks selle protseduuri lõpetamiseks saate importida ER-vormingu konfiguratsiooni **Vabas vormis arve (Excel)** uusima versiooni. Vastav ER-i andmemudel ja ER-i mudelivastenduse konfiguratsioonid imporditakse automaatselt.

![LCS-i ühiste vahendite teegi sisu leht](./media/BDM-Overview-SharedAssetLibrary.png)

Rohkem teavet ER-seadistuste importimise kohta vt [ER-seadistuse töötsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md).


## <a name="enable-business-document-management"></a>Lubage äridokumentide haldus

Äridokumendi halduse käivitamiseks peate avama tööruumi **Funktsioonihaldus** ja lubama funktsiooni **Äridokumendi haldamine**.

Kõikide juriidiliste isikute äridokumentide haldamise lubamiseks toimige järgmiselt.

1. Avage tööruum **Funktsioonihaldus**.
2. Valige vahekaardi **Uus** loendist funktsioon **Äridokumendi haldus**.
3. Valitud funktsiooni lubamiseks valige **Luba kohe**.
4. Uue funktsiooni kasutamiseks värskenda lehte.

>[!NOTE]
> Lisateavet uue dokumendi kasutajaliidese kasutamise kohta äridokumentide halduses vt teemast [Uus dokumendi kasutajaliides äridokumentide halduses](er-business-document-management-new-template-ui.md).

![Funktsioonihalduse tööruum](./media/BDM-Overview-FMEnabling.png)

Lisateavet uute funktsioonide lubamise kohta vt [Funktsioonihalduse ülevaade](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Seadistage parameetrid

Järgmiste jaotiste teabega saate seadistada äridokumentide halduse põhinäitajaid.

### <a name="prerequisites-for-parameter-setup"></a>Näitaja seadistuse eeltingimused
Enne äridokumendi halduse seadistamist peate seadistama dokumendi halduse raamistiku nõutava dokumendi tüübi. Seda dokumendi tüüpi kasutatakse dokumentide ajutiseks talletamiseks Office'i vormingutes (Excel ja Word), mida kasutatakse mallidena ER-aruannetes. Ajutise talletamise malli saab muuta Office'i töölauarakenduste abil.

Selle dokumenditüübi puhul peavad olema valitud järgmised atribuudi väärtused.

| **Atribuudi nimi**  | **Atribuudi väärtus**   |
|---------------------|-----------------------|
| Klass               | Lisa fail           |
| Grupeeri               | Fail                  |
| Koht            | SharePoint            |

Lisateavet nõutavate dokumendihalduse näitajate ja dokumenditüüpide seadistamise kohta vt [Dokumendihalduse seadistamine](../../fin-ops/organization-administration/configure-document-management.md).

![Seadistage dokumendihalduse dokumendi tüüp](./media/BDM-Overview-DMSetting.png)

### <a name=""></a><a name="SetupBdmParameters">Seadistage näitajad</a>

Põhilisi äridokumendi halduse näitajaid saate seadistada lehel **Äridokumendi näitajad**. Lehele pääsevad ligi vaid kindlad kasutajad. See hõlmab:

- **Süsteemiadministraatori** rolli määratud kasutajad.
- Kasutajad, kes on määratud mis tahes kohustust täitvasse rolli. **Säilita äridokumentide halduse näitajad** (AOT-nimi **ERBDMaintainParameters**).

Kõigi juriidiliste isikute põhinäitajate seadistamiseks toimige järgnevalt.

1. Logige sisse kasutajana, kes pääseb ligi lehele **Äridokumendi näitajad**.
2. Minge **Organisatsioon haldus** \> **Digiaruandlus** \> **Äridokumendi haldus** \> **Äridokumendi näitajad**.
3.    Lehe **Äridokumendi näitajad** vahekaardi **Manused** väljal **SharePointi dokumendi tüüp** määratlege dokumendi tüüp, millega võidaks ajutiselt talletada malle Office’i vormingutes, kui neid muudetakse Office’i töölauarakendustega. 

> [!NOTE]
> Selle näitaja puhul on saadaval vaid SharePointi asukohaga seadistatud dokumendi tüübid.

![Äridokumendi halduse näitajate seadistamine](./media/BDM-Overview-BDMSetting.png)

Valitud dokumendi tüüp on ettevõttepõhine ja seda kasutatakse siis, kui kasutaja töötab äridokumendi haldamisega ettevõttes, mille jaoks valitud dokumendi tüüp on seadistatud. Muus ettevõttes äridokumendi haldamisega tegeleva kasutaja puhul kasutatakse sama valitud dokumendi tüüpi, kui ta pole seadistatud selle ettevõtte jaoks. Kui dokumendi tüüp on seadistatud, kasutatakse seda **SharePoint dokumendi tüübi** väljas valitu asemel.

> [!NOTE]
> **SharePointi dokumenditüübi** parameeter määratleb SharePointi kausta, kus talletatakse ajutuselt malle, mis on redigeeritavad kas Microsoft Exceli või Wordi abil. Peate seadistama selle parameetri, kui kavatsete kasutada neid Office'i töölaua rakendusi mallide redigeerimiseks. Lisateavet leiate teemast [Malli redigeerimine Office'i töölauarakenduses](#EditInOfficeDesktopApp). Kui plaanite malli muuta ainult Office 365 abi, võite selle parameetri jätta tühjaks. Lisateabe saamiseks vt jaotist [Malli redigeerimine teenuses Office 365](#EditInOffice365).

## <a name="configure-access-permissions"></a>Seadista juurdepääsuõigused

Kui äridokumentide halduse lubadele on juurdepääs keelatud, siis tavaliselt näeb äridokumentide halduse tööruumile juurdepääsu omav iga kasutaja kõiki ER-lahenduse malle. Äridokumentide halduse tööruum näitab vaid ER-vormingu seadete ja sildiga **Äridokumendi tüüp** märgitud malle.

![ER-seadete leht](./media/BDM-Overview-ERFormatTags.png)

Äridokumentide halduse tööruumi mallide loendit saab piirata juurdepääsu lubade seadistamisel. See võib olla oluline, kui eri mallidega luuakse äridokumente eri äriteenuse domeenidele (funktsionaalsed valdkonnad) ja tahate äridokumentide halduse tööruumis lubada kindlatel kasutajatel ligi pääseda eri mallidele ning neil lasta neid muuta.

Äridokumentide halduse tööruumi juurdepääsu lube saab määrata valikus **Juurdepääsu lubade seadistus**. Lehele pääsevad ligi vaid järgmised kasutajad:

- rolli **Süsteemiadministraator** määratud kasutajad.
- Kasutajad, kes on määratud mistahes teise rolli, mis on seadistatud täitma seda kohustust, **Seadista lube, et pääseda ligi muudetavatele äridokumentide mallidele** (AOT nimi **ERBDTemplatesSecurity**).

Kõikide juriidiliste isikute äridokumentide lubade ligipääsu seadistamiseks tehke järgmist.

1. Logige sisse kui lehe **Juurdepääsu lubade seadistus** ligipääsu omav kasutaja.
2. Minge **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Äridokumentide haldus** \> **Hallake juurdepääsu õigusi**.

    Pöörake tähelepanu teatele, mis teavitab teid sellest, et äridokumentide halduse juurdepääsu õiguste kasutamine pole hetkel lubatud.

    ![Äridokumentide halduse tööruumi juurdepääsu õiguste seadistaja leht](./media/BDM-Overview-TemplatesAccess1.png)

    Selle seadega saab iga kasutaja, kes on määratud mistahes turberolli, mille ülesandeks on teha kohustust **Hallake äridokumentide malle** (AOT nimi **ERBDManageTemplates**), avada äridokumentide halduse tööruumi ja muuta mistahes saadaval malli.

    Järgmine joonis kujutab, mis on saadaval äridokumentide halduse tööruumi kasutajatele, kellele on määratud roll **Müügireskontro ametnik**. Kasutaja saab praeguse juurdepääsu õigust seadega muuta eri valdkondade, sealhulgas arveldamise, seadusandliku aruandlus ja maksete äridokumentide malle.

    ![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-TemplatesForAlice1.png)

3. Lehel **Juurdepääsu lubade seadistus** valige **Juurdepääsu lubade seade**.
4. Dialoogikastis **Mallide muutmiseks vajalike juurdepääsu õiguste seaded** lubage valik **Rakendage seadistatud juurdepääsu õigused**.
5. Äridokumentide halduse juurdepääsemise õiguste lubamise kinnitamiseks valige **OK**.

    ![Äridokumentide halduse tööruumi juurdepääsu õiguste seadistamise leht](./media/BDM-Overview-TemplatesAccess2.png)

6. Valige **Lisa**, et sisestada uus äriroll õiguste jaoks eesmärgiga pääseda juurde seadistatavatele äridokumentide halduse mallidele.
7. Valige dialoogiboksis **Turberollid** roll **Müügireskontro ametnik** ja klõpsake siis nuppu **OK**.
8. Vahekaardil **Juurdepääsu õigused seadistuste siltide kohta** valige **Uus**.
9. Väljas **Sildi tüüp** valige **Funktsionaalsed valdkonnad** ja väljas **ID** valige **Arve esitamine**.
10. Valitud rolli seadistatud juurdepääsu õiguste salvestamiseks valige **Salvesta**.

    Praegune seade tähendab, et iga kasutaja jaoks, kellele on määratud **Arvete arvelduse töövõtja** roll ja kes täidab kohustust, **Hallake äridokumentide malle** (AOT nimi **ERBDManageTemplates**), ER-vormingu konfiguratsioon Äridokumendihalduse tööruumis saab redigeerida malle, millel on **Arve**  väärtusega **Funktsionaalne ala**.

11. Minge praeguse lehe paremas servas asuvasse paani **Seotud teave**. **Seotud teave** paan näitab, kuidas rakendatakse seadistatud juurdepääsu õigusi, sealhulgas mis ER-seadistuse mallid on saadaval kasutajatele, kes on määratud rolli **Müügireskontro ametnik**.

    ![Äridokumentide halduse tööruumi juurdepääsu õiguste seadistamise leht](./media/BDM-Overview-TemplatesAccess3.png)

12. Vahekaardil **Juurdepääsu õigused seadistuste kohta** valige **Lisa**.
13. Dialoogikastis **Vali seadistus** märkige ER-vormingu seadistus **Intrastat-aruanne**.
14. Valitud seadete sisestamise kinnitamiseks valige **OK** ja seejärel valitud rolli seadistatud juurdepääsu õiguste salvestamiseks valige **Salvesta**.

Praegune seade tähendab seda, et iga kasutaja, kes on määratud rolli **Müügireskontro ametnik** ja täidab ülesannet **Halda äridokumentide malle** (AOT nimi **ERBDManageTemplates**), saab muuta äridokumentide halduse tööruumis järgmisi malle:

- mallid, mille sildi **Funktsionaalsed valdkonnad** väärtus on **Arve esitamine**;
- vahekaardil **Juurdepääsu õigused seadistuste kohta** loetletud ER-vormingu seadistuste mallid (antud näites domeeni **Seaduslik aruandlus** vormingu seadistuse **Intrastat-aruanne** mallid).

![Äridokumentide halduse tööruumi juurdepääsu õiguste seadistamise leht](./media/BDM-Overview-TemplatesAccess4.png)

Järgmine joonis kujutab, mida äridokumentide halduse tööruum pakub kasutajale, kellele on määratud roll **Müügireskontro ametnik**. Kasutaja saab praeguse äridokumentide halduse juurdepääsu õiguste seadega muuta domeeni **Arve esitamine** ja ER-vormingu seadistuse **Intrastat-aruanne** äridokumentide malle. Domeeni **Maksed** mallid pole saadaval rollile **Müügireskontro ametnik**.

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-TemplatesForAlice2.png)

> [!NOTE]
> **Juurdepääsu õigused seadistuste kohta** reeglid salvestatakse ER-vormingu seadistuse ainulaadse tuvastamise ID abil. See tähendab seda, et neid reegleid ei kustutata, kui neile viitav ER-seadistus kustutatakse. Kui impordite kustutatud seaded tagasi sellesse eksemplari, viitavad need reeglid taas neile. Reegleid pole vaja uuesti seadistada pärast kustutatud seadete taasimportimist.

## <a name="use-business-document-management-to-edit-templates"></a>Mallide muutmiseks kasutage äridokumentide haldust

Ärikasutajad saavad muuta äridokumentide malle äridokumentide halduse tööruumis. Vaid järgmised kasutajad saavad pääseda äridokumentide halduse tööruumi:

- rolli **Süsteemiadministraator** määratud kasutajad;
- kasutajad, kes on määratud mistahes rolli, mis on seadistatud täitma seda kohustust, **Halda äridokumentide malle** (AOT nimi **ERBDManageTemplates**).

Vabas tekstis arve mallide muutmiseks äridokumentide halduse tööruumis toimige järgmiselt. Enne selle toimingu lõpetamist pead lõpetama selle teema kõik eelnevad toimingud.

1. Logige sisse kasutajana, kellel on juurdepääs Äridokumendi halduse tööruumile.
2. Avage äridokumentide halduse tööruum.

Kui tööruumis **Funktsioonihaldus** on funktsioon **Äridokumentide halduse Office’ile sarnanev kasutajaliides** välja lülitatud, kuvatakse tööruumi **Äridokumentide haldus** pearuudustikus järgmised mallid.

- Mallid, mille omanik on teie ER-i konfiguratsiooni pakkuja (st pakkuja, kes on praegu tööruumis **Elektrooniline aruandlus** aktiivseks märgitud). Kui olete mõne neist mallidest valinud, saate selle käivitamiseks või redigeerimise jätkamiseks teha valiku **Muuda malli**.
- Mallid, mis kuuluvad teistele ER-i konfiguratsiooni pakkujatele. Kui olete valinud ühe neist mallidest, saate teha valiku **Uus dokument**, et luua koopia sellest mallist, mis kuulub teie ER-i konfiguratsiooni pakkujale, ja seejärel alustada koopia muutmist.

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingTemplate1.png)

Vahekaart **Mall** esitleb valitud malli sisu. Valitud malli andmete ja selles olevate ER-vormingu seadistuse andmete üle vaatamiseks valige vahekaart **Üksikasjad**. Pange tähele, et, kõikide mallide olek on **Avaldatud** ja veerus **Redaktsioon** pole üldse andmeid. See tähendab seda, et neid malle hetkel ei muudeta.

Kui tööruumis **Funktsioonihaldus** on funktsioon **Äridokumentide halduse Office’ile sarnanev kasutajaliides** sisse lülitatud, kuvatakse tööruumi **Äridokumentide haldus** pearuudustikus mallid, mis kuuluvad teie ER-i konfiguratsiooni pakkujale (st pakkujale, kes on praegu tööruumis **Elektrooniline aruandlus** aktiivseks märgitud). Kui olete mõne neist mallidest valinud, saate selle käivitamiseks või redigeerimise jätkamiseks teha valiku **Muuda malli**.

Teiste ER-i konfiguratsiooni pakkujate omanduses olevate mallidega töötamiseks tehke valik **Uus dokument**, et luua koopia mallist, mis kuulub teie ER-i pakkujale. Seejärel saate hakata muutma koopiat. Lisateavet leiate teemast [Uue dokumendi kasutajaliides äridokumendi halduses](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Alustage seadistuse pakkuja mallide muutmist

1. Valige äridokumentide halduse tööruumi loendist mall **Tšekkide printimisvorming**.
2. Valige **Üksikasjad** vahekaart.

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingTemplate2.png)

Valitud mallile on saadaval valik **Muuda malli**. See valik on alati saadaval aktiivsele ER-seadistuse pakkujale (näiteks **Litware, Inc.**) kuuluva ER-vormingu seadistusega mallil. Valides **Muuda malli**, saab muuta asjakohase ER-vormingu seadistuse mustandi olemasolevat malli.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Alustage teist pakkujate mallide muutmist

1. Valige äridokumendi halduse tööruumis dokument, mida soovite mallina kasutada.

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingTemplate3.png)

3. Valige **Uus dokument** ja väljal **Pealkiri** muutke vajadusel redigeeritava malli pealkirja. Tekstiga nimetatakse ise tekkivat ER-vormingu seadistust. Pange tähele, et selle muudetavat malli sisaldava seadistuse (**Kliendi FTI aruande (GER) koopia**) mustand märgitakse automaatselt, et kasutada seda ER-vormingut praeguse kasutaja puhul. Samal ajal kasutatakse ER-vormingu põhiseadistuse muutmata algset malli selle ER-vormingu käivitamiseks kõikide kasutajate puhul.
4. Muutke väljas **Nimi** ise tekkiva muudetava malli esimese redaktsiooni nime.
5. Muutke väljal **Kommentaar** redigeeritava malli isetekkiva redaktsiooni märkust.
6. Muutmisprotsessi alustamise kinnitamiseks valige **OK**

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingTemplate4.png)

Suvand **Uus dokument** on alati saadaval praeguse ja teise pakkuja (selles näites Microsofti) ER-vormingu seadistusega mallil, millel pole redaktsiooni. Muudetud malli saab seejärel muuta uues ise loodavas ER-vormingus seadistusega.

### <a name="start-editing-a-template"></a>Alustage malli muutmisest

1. Valige valitud mallis **Dokumendi redigeerimine**.
2. Muutke väljas **Nimi** ise tekkiva muudetava malli esimese redaktsiooni nime.
3. Muutke väljas **Kommentaar** ise tekkiva muudetava malli redaktsiooni märkust.

    ![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingTemplate5.png)

5. Muutmis alustamise kinnitamiseks valige **OK**.

Avaneb leht **BDM malli muutja**. Valitud malli saab muuta internetis Office 365-ga.

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingLayout1.png)

### <a name=""></a><a name="EditInOffice365">Malli muutmine teenuses Office 365</a>

Te ei saa Office 365 abil malli muuta. Näiteks muuda veebilehitsejast kasutatavas Office’is malli päise välja küsimuste font **Tavaline** fondiks **Paks**. Need muudatused salvestatakse automaatselt malli peamises salvestusruumis (tavaliselt Azure bloobi salvestusruum) hoitava muudetava malli jaoks. See on konfigureeritud ER raamistiku jaoks.

![Äridokumentide halduse malli muutmisleht](./media/BDM-Overview-EditingLayout2.png)

### <a name=""></a><a name="EditInOfficeDesktopApp">Muuda malli Office’i töölauarakenduses</a>

> [!NOTE]
> See funktsioon on saadaval ainult siis, kui **SharePointi dokumenditüübi** parameeter on õigesti konfigureeritud. Lisateavet vt teemast [Parameetrite konfigureerimine](#SetupBdmParameters).

1. Malli muutmiseks Office’i töölauarakenduse funktsioonidega (selles näites Exceliga) valige **Ava töölauarakenduses**. Muudetav mall kopeeritakse alalisest salvestusruumist ajutisse salvestusruumi, mis on äridokumentide halduse näitajatega määratletud kui SharePoint kaust.
2. Kinnitage, et tahate avada malli Office’i töölaua Exceli rakendusega ajutisest faili salvestusruumist.

    ![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingLayout3.png)

3. Muutke malli. Näiteks muutke malli päise väljade küsimuste fondi värv **Must** värviks **Sinine**.

    ![Äridokumentide halduse malli muutmisleht](./media/BDM-Overview-EditingLayout4.png)

4. Malli muudatuste salvestamiseks ajutisse salvestusruumi valige Exceli töölaua rakenduses **Salvesta**.

    ![Äridokumentide halduse malli muutmisleht](./media/BDM-Overview-EditingLayout5.png)

5. Sulgege Exceli töölaua rakendus.
6. Ajutise malli salvestusruumi ajakohastamiseks alalise malli salvestusruumiga valige **Ajakohasta salvestatud koopia**.

> [!NOTE]
> Ajutises faili salvestusruumis oleva muudetava malli koopiat hoitakse alles vaid malli muutmise praeguse seansi ajaks. Kui lõpetate selle seansi lehe **BDM malli muutja** sulgemisega, see koopia kustutatakse. Kui muutsite ajutises faili salvestusruumis olevat malli ja ei valinud **Ajakohasta salvestatud koopia**, kui üritasite sulgeda lehte **BDM malli muutja**, küsitakse, kas tahate salvestada tehtud muudatused. Muudatuste salvestamiseks alalises faili asukohas asuvasse malli valige **Jah**.

### <a name="validate-a-template"></a>Valideeri mall

1. Lehel **BDM malli muutja** valige **Probleemide kontroll**, et valideerida muudetud mall asjakohase ER-vormingu seadistuse suhtes. Järgige soovitusi (kui olemas), et mall vastaks ER-vormingu põhiseadistuse vormingu ülesehitusele.
2. Valige **Näita vormingut**, et näha ER-vormingu põhiseadistuse vormingu praegust ülesehitust, mis peab vastama muudetavale mallile. 
3. Paani sulgemiseks valige **Peida vorming**.

    ![BDM BDM malli muutmise leht](./media/BDM-Overview-EditingTemplate6.png)

4. Sulgege leht **BDM malli muutja**.

Värskendatud malli näidatakse vahekaardil **Mall**. Pange tähele, et muudetud malli olek on nüüd **Mustand** ja praegune redaktsioon pole enam tühi. See tähendab seda, et seda malli on hakatud muutma.

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Katsetage muudetud malli 

1. Vahetage rakenduses ettevõtte **USMF**-i vastu.
2. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
3. Valige arve **FTI-00000002** ja seejärel valige **Prindihaldus**.
4. Valige **Moodul – müügireskontro** \> **Dokumendid** \> **Vabas tekstis arve** \> **Algne dokument** tase, et määratleda töötlemiseks arvete ulatus.
5. Väljas **Aruandevorming** valige dokumendi taseme ER-vorming **Kliendi FTI aruande (GER) koopia**.

    ![Prindihalduse seadete leht](./media/BDM-Overview-TestRun1.png)

6. Praeguse lehe sulgemiseks vajutage **Paoklahv**.
7. Valige **Prindi** ja seejärel klõpsake **Valitud**.
8. Laadige dokument alla ja avage see Exceli töölaua rakendusega.

![Vabas tekstis arvete leht](./media/BDM-Overview-TestRun2.png)

Muudetud malliga luuakse valitud üksuse vabas tekstis arve aruanne. Selleks, et analüüsida, kuidas malli muudatused mõjutavad seda aruannet, saate selle aruande käivitada ühes rakenduse seansis kohe pärast malli muutmist teises rakenduse seansis.

### <a name="create-an-alternative-template-revision"></a>Looge malli asendusredaktsioon

1. Avage leht **BDM malli muutja** ja valige mall **Kliendi FTI aruande (GER) koopia**.
2. Valige vahekaardil **Redaktsioonid** **Uus**.
3. Vajadusel muutke väljas **Nimi** teise redaktsiooni nime vastavalt praegu aktiivsele esimesele redaktsioonile.
4. Vajadusel muutke väljas **Kommentaar** ise tekkiva muudetava malli redaktsiooni märkust.

    ![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-AddRevision.png)

    Koostasite malli uue redaktsiooni püsivasse malli salvestusruumi. Nüüd saate jätkata praegu aktiivseks märgitud teise redaktsiooni malli muutmisega.

5. Valige esimene redaktsioon ja seejärel valige **Määra aktiivseks**. Saate määrata muu redaktsiooni aktiivseks, kui peaksite tahtma mistahes hetkel naasta malli sellele redaktsioonile.
6. Valige teine redaktsioon ja seejärel valige **Kustuta**.
7. Valitud redaktsiooni kustutamise kinnitamiseks valige **OK**. Kui ühtegi keelatud redaktsioone ei lähe enam vaja, saab need kustutada.

### <a name="delete-a-modified-template"></a>Kustutage muudetud mall

1. Valige lehel **BDM malli muutja** vahekaart **Mall**.
2. Valige **Kustuta**.
3. Kui valite kustutamise kinnitamiseks **OK**, kustutatakse muudetud malliga ER-vorming **Kliendi FTI aruande (GER) koopia**. Muude valikute avastamiseks valige **Tühista**.

### <a name="revoke-changes-of-template"></a>Võtke tagasi malli muudatused

Kui muudate praegu aktiivse pakkuja ER-vormingu malli, pakutakse võimalust tühistada mallile tehtud muudatused.

![Äridokumentide halduse tööruumi leht](./media/BDM-Overview-RevokeChanges.png)

1. Valige lehel **BDM malli muutja** vahekaart **Mall**.
2. Valige käsk **Võta tagasi**.
3. Kui valite malli muudatuste tühistamiseks **OK**, asendatakse muudetud mall algse malliga ja kõik muudatused eemaldatakse. Kui tühistate malli muudatused, saate kustutada malli. Muude valikute avastamiseks valige **Tühista**.

### <a name="publish-a-modified-template"></a>Avaldage muudetud mall
1. Valige lehe **BDM malli muutja** vahekaardil **Mall** valik **Avalda**.
2. Kui valite avaldamise kinnitamiseks **OK**, märgitakse lõpetatuks muudetud malliga ER-vormingu **Kliendi FTI aruande (GER) koopia** saadud mustand. Muudetud mall muutub teistele kasutajatele saadavaks. Selle ER-vormingu lõplikud versioonid säilitavad vaid malli viimase aktiivse redaktsiooni. Muud redaktsioonid kustutatakse. Muude valikute avastamiseks valige **Tühista**.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

#### <a name="i-selected-edit-document-but-instead-of-opening-the-bdm-template-editor-page-in-finance-and-operations-i-have-been-sent-to-the-office-365-web-page"></a>Valisin **Dokumendi redigeerimine**, kuid lehel **BDM malliredaktor** avamise asemel Finance and Operations-is suunati mind Office 365 veebilehele.
See on Office 365 ümbersuunamisega teadaolev probleem. See juhtub, kui logite sisse Office 365-te esimest korda. Selle probleemi lahendamiseks peate naasma veebilehitseja nupuga **Tagasi**.

#### <a name="i-understand-how-to-edit-a-template-by-using-office-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-adjusting-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-do-this-using-the-office-desktop-application"></a>Mõistan, kuidas muuta malli Office 365-ga esimesel rakenduse seansil ja, kuidas kasutada malli teises rakenduse seansis, kus tuleb muuta malli selleks, et näha, kuidas minu muudatused mõjutavad loodud äridokumenti. Kas saan seda teha Office’i töölauarakendusega?
Jah, saate. Esimeses rakenduse seansis valige **Avage töölauarakenduses**. Mall salvestatakse ajutisse faili salvestusruumi ja avatakse Office’i töölaua rakendusega. Järgmisena täitke järgmised etapid, et näha eelvaadet loodud äridokumendi malli muudatustest:

1. Muutke malli Office’i töölauarakendusega.
2. Valige Office’i töölauarakenduses **Salvesta**.
3. Valige esimese rakenduse seansi lehel **BDM malli muutja** valik **Ajakohasta salvestatud koopia**.
4. Käivitage see malli ER-vorming teises rakenduse seansis.

#### <a name="i-get-the-error-value-cannot-be-null-parameter-name-externalid-when-i-select-open-in-desktop-app-how-do-i-work-around-this"></a>Saan veateate „Väärtus ei saa olla null“. Näitaja nimi on „externalId“, kui valin **Ava töölauarakenduses**. Kuidas selle lahendan? 
Tõenäoliselt logisite sisse Azure AD domeeni praegusesse rakenduse eksemplari, mis erineb Azure AD domeenist, mida kasutati selle eksemplari kasutamisel. Kuna SharePointi teenus, mida kasutatakse mallide salvestamiseks ja Office’i töölauarakendusega muutmisvõimeliseks tegemiseks, kuulub samasse domeeni, seega meil pole õigust juurde pääseda SharePointi teenusele. Selle probleemi lahendamiseks logige sisse praegusesse seansi õige Azure AD domeeni kasutava kasutaja sisselogimisandmetega.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Elektroonilise aruandluse konfiguratsioonide kujundamine Wordi vormingus aruannete loomiseks](tasks/er-design-configuration-word-2016-11.md)

[Manustatud pildid ja kujutised ER-iga loodud dokumentides](electronic-reporting-embed-images-shapes.md)

[Elektroonilise aruandluse (ER) konfigureerimine andmete tõmbamiseks Power BI-sse](general-electronic-reporting-report-configuration-get-data-powerbi.md)

