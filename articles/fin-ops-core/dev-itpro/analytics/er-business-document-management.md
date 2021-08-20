---
title: Äridokumentide halduse ülevaade
description: Siin teemas on ER-raamistiku äridokumendi halduri kasutamisõpetus.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERSecurityAccessEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b59f535e01de2ae30e6bbeb6d5ab97a415df6043233694d4feb1c48140a110f6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753072"
---
# <a name="business-document-management-overview"></a>Äridokumentide halduse ülevaade

[!include [banner](../includes/banner.md)]

Äriüksuse kasutajad kasutavad raamistikku [Elektrooniline aruandlus (ER)](general-electronic-reporting.md), et konfigureerida väljuvate dokumentide vorminguid erinevate riikide/regioonide õigusnõuete järgi. Kasutajad saavad määratleda ka andmevoo, et täpsustada, mis avalduse andmeid loodud dokumendid sisaldavad. ER raamistik loob eelmääratletud mallide abil väljuvaid dokumente Microsoft Office’i vormingutes (Exceli töövihikud või Wordi dokumendid). Mallid täidetakse nõutud dokumentide loomise ajal kohustuslike andmetega vastavalt seadistatud andmevoole. Kindlate väljuvate dokumentide loomiseks saab kõiki vorminguid avaldada ER-lahenduse osana. Seda tähistab ER-vormingu seadistus, mis sisaldab erinevate väljuvate dokumentide loomiseks kasutatavaid malle. Äriüksuse kasutajad saavad selle raamistikuga hallata vajalikke äridokumente.

**Äridokumendi haldus** on ehitatud ER-i raamistiku põhjal ja võimaldab ärikasutajatel redigeerida äridokumendi malle Microsoft 365 teenuse või sobiva Microsoft Office'i töölauarakenduse kaudu. Dokumentide muutmisel võib vahetada äridokumendi välimust ja lisada kohatäitjaid ilma lähtekoodi muutmata ja uute juurutusteta. Äridokumentide mallide värskendamine ei vaja teadmisi ER-raamistikust.

> [!NOTE]
> Arvestage, et äridokumendi haldus võimaldab muuta malle, mida kasutatakse äridokumentide, nt tellimuste, arvete jne koostamiseks. Kui malli on muudetud ja uus versioon on avaldatud, kasutatakse seda versiooni nõutavate äridokumentide loomiseks. Äridokumendi haldust ei saa kasutada juba loodud äridokumentide muutmiseks.

## <a name="supported-deployments"></a>Toetatud juurutused

Praegu kasutatakse äridokumendi halduse funktsiooni vaid pilve juurutamiseks. Kui see funktsioon on teie asutusesisese juurutuse puhul väga tähtis, andke meile sellest teada, andes tagasisidet [ideede](https://experience.dynamics.com/ideas/) lehele.

## <a name="supported-microsoft-office-applications"></a>Toetatud Microsoft Office’i rakendused

Äridokumentide haldusega Exceli või Wordi vormingutes mallide muutmiseks Microsoft Office’i töölauarakendustega, peab teil olema paigaldatud Microsoft Office 2010 või uuem versioon. Seda toetatakse pilvepõhistes ja asutusesisestes juurutustes.

Äridokumentide haldusega Exceli või Wordi vormingutes mallide muutmiseks Microsoft 365 rakendustega, peab teil olema veebitellimuse Microsoft 365 Office. See on pilvepõhises juurutamises toetatud.

## <a name="business-document-availability"></a>Äridokumendi saadavus

Kõigi 2019. aasta oktoobri väljalaske jaoks kavandatud aruannete põhjalikku loendit vt [Seadistatavate äridokumentide aruandlus Wordis ja Excelis](/dynamics365-release-plan/2019wave2/dynamics365-finance-operations/configurable-business-documents-reporting-word-excel-pdf#feature-details).

Kõigi 2020. aasta oktoobri väljalaske jaoks kavandatud aruannete põhjalikku loendit vt [Seadistatavad äridokumendid – Wordi mallid](/dynamics365-release-plan/2020wave1/dynamics365-finance/configurable-business-documents-word-templates).

Tulevastes väljalasetes muutub veel aruandeid kättesaadavaks. Lisaaruannete eriteatised saadetakse eraldi. Teavet selle kohta, kuidas praegu saadaolevate aruannete loendit vaadata, vt allpool jaotises [Seadistatavate äridokumentide toetamiseks rakenduses Finance välja antud ER-i konfiguratsioonide loend](#list-of-configurations-cbd).

Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide.

## <a name="configure-er-parameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

Kuna äridokumendi haldus põhineb ER-raamistikul, peate sellega töötamiseks seadistama ER-näitajad. Selleks peate seadistama elektrilise aruandluse parameetrid, nagu on kirjeldatud teemas [Elektrilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md). Peate lisama ka uue konfiguratsiooni pakkuja vastavalt teemale [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

![ER-tööruum.](./media/BDM-Overview-ERSetting.png)

## <a name="import-er-solutions"></a>Impordi ER-lahendused

Selle protseduuri näites on kasutatud elektroonilise aruandluse näidiskonfiguratsioone. Peate importima oma praegusesse Dynamics 365 Finance’i eksemplari elektroonilise aruandluse konfiguratsioonid, mis sisaldavad äridokumentide malle, mida saab äridokumentide haldust kasutades redigeerida. Selle protseduuri lõpule viimiseks laadige järgmised failid alla ja salvestage need seejärel seadmesse.

**ER-näidiskliendi arveldamislahendus**

| Fail                                      | Sisu |
|-------------------------------------------|---------|
| Kliendiarvete loomine model.version.2.xml    | [ER-i andmemudeli konfiguratsioon](https://download.microsoft.com/download/b/f/a/bfa5cb52-e6e2-42bc-a4c0-77014a4c54e6/Customerinvoicingmodel.version.2.xml) |
| Customer FTI report (GER).version.2.3.xml | [Vabas vormis arve ER-vormingu seadistus](https://download.microsoft.com/download/3/c/2/3c2e58f2-6e56-43d9-85ea-4c97252a108d/CustomerFTIreportGER.version.2.3.xml) |

**ER-näidismakse tšekkide lahendus**

| Fail                                     | Sisu |
|------------------------------------------|---------|
| Model for cheques.version.10.xml         | [ER-i andmemudeli konfiguratsioon](https://download.microsoft.com/download/3/7/6/376cb0f6-181a-4895-a432-390ffca64162/Modelforcheques.version.10.xml) |
| Cheques printing format.version.10.9.xml | [Maksetšeki ER-vormingu seadistus](https://download.microsoft.com/download/6/d/6/6d61bfff-3d89-4377-9e34-2e3ee6d6df91/Chequesprintingformat.version.10.9.xml) |

**ER-väliskaubanduse näidislahendus**

| Fail                             | Sisu |
|----------------------------------|---------|
| Intrastat model.version.1.xml    | [ER-i andmemudeli konfiguratsioon](https://download.microsoft.com/download/2/0/0/200d6ed1-eff8-48ec-ab75-175a4acf9714/Intrastatmodel.version.1.xml) |
| Intrastat report.version.1.9.xml | [Intrastati kontrollaruande ER-vormingu seadistus](https://download.microsoft.com/download/7/a/2/7a2a27c3-a8a5-42a1-9d04-f0a8e1ec1707/Intrastatreport.version.1.9.xml) |

Kasutage iga faili importimiseks järgmist protseduuri. Enne vastava ER-*vormingu* seadistuse importimist importige allolevates tabelites olevate kõikide ER-lahenduste ER-*andmemudeli* seadistus.

1. Avage jaotis **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> leht **Konfiguratsioonid**.
2. Valige lehe ülaosas **Vaheta**.
3. Valige **Laadi XML-failist**.
4. Vajaliku XML-faili laadimiseks valige **Sirvi**.
5. Seadistuse impordi kinnitamiseks valige **OK**.

![Konfiguratsiooni importimist kinnitavate ER-konfiguratsioonide leht.](./media/BDM-Overview-ERSolutions.png)

Teise võimalusena saate importida ametlikult avaldatud ER-vormingu konfiguratsioonid platvormilt Microsoft Dynamics Lifecycle Service (LCS). Näiteks selle protseduuri lõpetamiseks saate importida ER-vormingu konfiguratsiooni **Vabas vormis arve (Excel)** uusima versiooni. Vastav ER-i andmemudel ja ER-i mudelivastenduse konfiguratsioonid imporditakse automaatselt.

![LCS-i ühiste vahendite teegi sisu leht.](./media/BDM-Overview-SharedAssetLibrary.png)

Rohkem teavet ER-seadistuste importimise kohta vt [ER-seadistuse töötsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md).

## <a name="enable-business-document-management"></a>Lubage äridokumentide haldus

Äridokumendi halduse käivitamiseks peate avama tööruumi **Funktsioonihaldus** ja lubama funktsiooni **Äridokumendi haldamine**.

Kõikide juriidiliste isikute äridokumentide haldamise lubamiseks toimige järgmiselt.

1. Avage tööruum **Funktsioonihaldus**.
2. Valige vahekaardi **Uus** loendist funktsioon **Äridokumendi haldus**.
3. Valitud funktsiooni lubamiseks valige **Luba kohe**.
4. Uue funktsiooni kasutamiseks värskenda lehte.

> [!NOTE]
> Lisateavet uue dokumendi kasutajaliidese kasutamise kohta äridokumentide halduses vt teemast [Uus dokumendi kasutajaliides äridokumentide halduses](er-business-document-management-new-template-ui.md).

![Funktsioonihalduse tööruum.](./media/BDM-Overview-FMEnabling.png)

Lisateavet uute funktsioonide lubamise kohta vt [Funktsioonihalduse ülevaade](../../fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="configure-parameters"></a>Seadistage parameetrid

Järgmiste jaotiste teabega saate seadistada äridokumentide halduse põhinäitajaid.

### <a name="prerequisites-for-parameter-setup"></a>Näitaja seadistuse eeltingimused

Enne äridokumendi halduse seadistamist peate seadistama dokumendi halduse raamistiku nõutava dokumendi tüübi. Seda dokumendi tüüpi kasutatakse dokumentide ajutiseks talletamiseks Office'i vormingutes (Excel ja Word), mida kasutatakse mallidena ER-aruannetes. Ajutise talletamise malli saab muuta Office'i töölauarakenduste abil.

Selle dokumenditüübi puhul peavad olema valitud järgmised atribuudi väärtused.

| Atribuudi nimi | Atribuudi väärtus |
|----------------|-----------------|
| Klass          | Lisa fail     |
| Grupeeri          | Fail            |
| Koht       | SharePoint      |

Lisateavet nõutavate dokumendihalduse näitajate ja dokumenditüüpide seadistamise kohta vt [Dokumendihalduse seadistamine](../../fin-ops/organization-administration/configure-document-management.md).

![Seadistage dokumendihalduse dokumendi tüüp.](./media/BDM-Overview-DMSetting.png)

### <a name="set-up-parameters"></a><a name="SetupBdmParameters"></a>Seadistage näitajad

Põhilisi äridokumendi halduse näitajaid saate seadistada lehel **Äridokumendi näitajad**. Lehele pääsevad ligi vaid kindlad kasutajad. See hõlmab:

- **Süsteemiadministraatori** rolli määratud kasutajad.
- Kasutajad, kes on määratud mis tahes kohustust täitvasse rolli. **Säilita äridokumentide halduse näitajad** (AOT-nimi **ERBDMaintainParameters**).

Kõigi juriidiliste isikute põhinäitajate seadistamiseks toimige järgnevalt.

1. Logige sisse kasutajana, kes pääseb ligi lehele **Äridokumendi näitajad**.
2. Minge **Organisatsioon haldus** \> **Digiaruandlus** \> **Äridokumendi haldus** \> **Äridokumendi näitajad**.
3. Lehe **Äridokumendi näitajad** vahekaardi **Manused** väljal **SharePointi dokumendi tüüp** määratlege dokumendi tüüp, millega võidaks ajutiselt talletada malle Office’i vormingutes, kui neid muudetakse Office’i töölauarakendustega. 

> [!NOTE]
> Selle näitaja puhul on saadaval vaid SharePointi asukohaga seadistatud dokumendi tüübid.

![Äridokumendi halduse näitajate seadistamine.](./media/BDM-Overview-BDMSetting.png)

Valitud dokumendi tüüp on ettevõttepõhine ja seda kasutatakse siis, kui kasutaja töötab äridokumendi haldamisega ettevõttes, mille jaoks valitud dokumendi tüüp on seadistatud. Muus ettevõttes äridokumendi haldamisega tegeleva kasutaja puhul kasutatakse sama valitud dokumendi tüüpi, kui ta pole seadistatud selle ettevõtte jaoks. Kui dokumendi tüüp on seadistatud, kasutatakse seda **SharePoint dokumendi tüübi** väljas valitu asemel.

> [!NOTE]
> **SharePointi dokumenditüübi** parameeter määratleb SharePointi kausta, kus talletatakse ajutuselt malle, mis on redigeeritavad kas Microsoft Exceli või Wordi abil. Peate seadistama selle parameetri, kui kavatsete kasutada neid Office'i töölaua rakendusi mallide redigeerimiseks. Lisateavet leiate teemast [Malli redigeerimine Office'i töölauarakenduses](#EditInOfficeDesktopApp). Kui plaanite malli muuta ainult Microsoft 365 funktsioonide abil, võite selle parameetri jätta tühjaks. Lisateabe saamiseks vt jaotist [Malli redigeerimine Microsoft 365-s](#EditInOffice365).

## <a name="configure-access-permissions"></a>Seadista juurdepääsuõigused

Kui äridokumentide halduse lubadele on juurdepääs keelatud, siis tavaliselt näeb äridokumentide halduse tööruumile juurdepääsu omav iga kasutaja kõiki ER-lahenduse malle. Äridokumentide halduse tööruum näitab vaid ER-vormingu seadete ja sildiga **Äridokumendi tüüp** märgitud malle.

![ER-i konfiguratsioonide leht äridokumendi tüübisildiga.](./media/BDM-Overview-ERFormatTags.png)

Äridokumentide halduse tööruumi mallide loendit saab piirata juurdepääsu lubade seadistamisel. See võib olla oluline, kui eri mallidega luuakse äridokumente eri äriteenuse domeenidele (funktsionaalsed valdkonnad) ja tahate äridokumentide halduse tööruumis lubada kindlatel kasutajatel ligi pääseda eri mallidele ning neil lasta neid muuta.

Äridokumentide halduse tööruumi juurdepääsu lube saab määrata valikus **Juurdepääsu lubade seadistus**. Lehele pääsevad ligi vaid järgmised kasutajad:

- rolli **Süsteemiadministraator** määratud kasutajad.
- Kasutajad, kes on määratud mistahes teise rolli, mis on seadistatud täitma seda kohustust, **Seadista lube, et pääseda ligi muudetavatele äridokumentide mallidele** (AOT nimi **ERBDTemplatesSecurity**).

Kõikide juriidiliste isikute äridokumentide lubade ligipääsu seadistamiseks tehke järgmist.

1. Logige sisse kui lehe **Juurdepääsu lubade seadistus** ligipääsu omav kasutaja.
2. Minge **Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Äridokumentide haldus** \> **Hallake juurdepääsu õigusi**.

    Pöörake tähelepanu teatele, mis teavitab teid sellest, et äridokumentide halduse juurdepääsu õiguste kasutamine pole hetkel lubatud.

    ![Äridokumentide halduse tööruumi juurdepääsu õiguste seadistaja leht.](./media/BDM-Overview-TemplatesAccess1.png)

    Selle seadega saab iga kasutaja, kes on määratud mistahes turberolli, mille ülesandeks on teha kohustust **Hallake äridokumentide malle** (AOT nimi **ERBDManageTemplates**), avada äridokumentide halduse tööruumi ja muuta mistahes saadaval malli.

    Järgmine joonis kujutab, mis on saadaval äridokumentide halduse tööruumi kasutajatele, kellele on määratud roll **Müügireskontro ametnik**. Kasutaja saab praeguse juurdepääsu õigust seadega muuta eri valdkondade, sealhulgas arveldamise, seadusandliku aruandlus ja maksete äridokumentide malle.

    ![Müügireskontro ametniku äridokumentide halduse tööruumi leht.](./media/BDM-Overview-TemplatesForAlice1.png)

3. Lehel **Juurdepääsu lubade seadistus** valige **Juurdepääsu lubade seade**.
4. Dialoogikastis **Mallide muutmiseks vajalike juurdepääsu õiguste seaded** lubage valik **Rakendage seadistatud juurdepääsu õigused**.
5. Äridokumentide halduse juurdepääsemise õiguste lubamise kinnitamiseks valige **OK**.

    ![Äridokumentide halduse tööruumi juurdepääsu õiguste kinnitamine.](./media/BDM-Overview-TemplatesAccess2.png)

6. Valige **Lisa**, et sisestada uus äriroll õiguste jaoks eesmärgiga pääseda juurde seadistatavatele äridokumentide halduse mallidele.
7. Valige dialoogiboksis **Turberollid** roll **Müügireskontro ametnik** ja klõpsake siis nuppu **OK**.
8. Vahekaardil **Juurdepääsu õigused seadistuste siltide kohta** valige **Uus**.
9. Väljas **Sildi tüüp** valige **Funktsionaalsed valdkonnad** ja väljas **ID** valige **Arve esitamine**.
10. Valitud rolli seadistatud juurdepääsu õiguste salvestamiseks valige **Salvesta**.

    Praegune seade tähendab, et iga kasutaja jaoks, kellele on määratud **Arvete arvelduse töövõtja** roll ja kes täidab kohustust, **Hallake äridokumentide malle** (AOT nimi **ERBDManageTemplates**), ER-vormingu konfiguratsioon Äridokumendihalduse tööruumis saab redigeerida malle, millel on **Arve** väärtusega **Funktsionaalne ala**.

11. Minge praeguse lehe paremas servas asuvasse paani **Seotud teave**. **Seotud teave** paan näitab, kuidas rakendatakse seadistatud juurdepääsu õigusi, sealhulgas mis ER-seadistuse mallid on saadaval kasutajatele, kes on määratud rolli **Müügireskontro ametnik**.

    ![Juurdepääsu lubade seadistuse lehe seotud teabe paan.](./media/BDM-Overview-TemplatesAccess3.png)

12. Vahekaardil **Juurdepääsu õigused seadistuste kohta** valige **Lisa**.
13. Dialoogikastis **Vali seadistus** märkige ER-vormingu seadistus **Intrastat-aruanne**.
14. Valitud seadete sisestamise kinnitamiseks valige **OK** ja seejärel valitud rolli seadistatud juurdepääsu õiguste salvestamiseks valige **Salvesta**.

Praegune seade tähendab seda, et iga kasutaja, kes on määratud rolli **Müügireskontro ametnik** ja täidab ülesannet **Halda äridokumentide malle** (AOT nimi **ERBDManageTemplates**), saab muuta äridokumentide halduse tööruumis järgmisi malle:

- mallid, mille sildi **Funktsionaalsed valdkonnad** väärtus on **Arve esitamine**;
- vahekaardil **Juurdepääsu õigused seadistuste kohta** loetletud ER-vormingu seadistuste mallid (antud näites domeeni **Seaduslik aruandlus** vormingu seadistuse **Intrastat-aruanne** mallid).

![Juurdepääsu lubade seadistuse lehe juurdepääsu lubade kiirkaardid.](./media/BDM-Overview-TemplatesAccess4.png)

Järgmine joonis kujutab, mida äridokumentide halduse tööruum pakub kasutajale, kellele on määratud roll **Müügireskontro ametnik**. Kasutaja saab praeguse äridokumentide halduse juurdepääsu õiguste seadega muuta domeeni **Arve esitamine** ja ER-vormingu seadistuse **Intrastat-aruanne** äridokumentide malle. Domeeni **Maksed** mallid pole saadaval rollile **Müügireskontro ametnik**.

![Äridokumendi mallide redigeerimine äridokumentide halduse tööruumi lehel.](./media/BDM-Overview-TemplatesForAlice2.png)

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

![Mallide loendid äridokumentide halduse tööruumi lehel.](./media/BDM-Overview-EditingTemplate1.png)

Vahekaart **Mall** esitleb valitud malli sisu. Valitud malli andmete ja selles olevate ER-vormingu seadistuse andmete üle vaatamiseks valige vahekaart **Üksikasjad**. Pange tähele, et, kõikide mallide olek on **Avaldatud** ja veerus **Redaktsioon** pole üldse andmeid. See tähendab seda, et neid malle hetkel ei muudeta.

Kui tööruumis **Funktsioonihaldus** on funktsioon **Äridokumentide halduse Office’ile sarnanev kasutajaliides** sisse lülitatud, kuvatakse tööruumi **Äridokumentide haldus** pearuudustikus mallid, mis kuuluvad teie ER-i konfiguratsiooni pakkujale (st pakkujale, kes on praegu tööruumis **Elektrooniline aruandlus** aktiivseks märgitud). Kui olete mõne neist mallidest valinud, saate selle käivitamiseks või redigeerimise jätkamiseks teha valiku **Muuda malli**.

Teiste ER-i konfiguratsiooni pakkujate omanduses olevate mallidega töötamiseks tehke valik **Uus dokument**, et luua koopia mallist, mis kuulub teie ER-i pakkujale. Seejärel saate hakata muutma koopiat. Lisateavet leiate teemast [Uue dokumendi kasutajaliides äridokumendi halduses](er-business-document-management-new-template-ui.md).

### <a name="initiate-editing-templates-owned-by-your-configuration-provider"></a>Alustage seadistuse pakkuja mallide muutmist

1. Valige äridokumentide halduse tööruumi loendist mall **Tšekkide printimisvorming**.
2. Valige **Üksikasjad** vahekaart.

![Äridokumentide halduse tööruumi leht, üksikasjade vahekaart.](./media/BDM-Overview-EditingTemplate2.png)

Valitud mallile on saadaval valik **Muuda malli**. See valik on alati saadaval aktiivsele ER-seadistuse pakkujale (näiteks **Litware, Inc.**) kuuluva ER-vormingu seadistusega mallil. Valides **Muuda malli**, saab muuta asjakohase ER-vormingu seadistuse mustandi olemasolevat malli.

### <a name="initiate-editing-templates-owned-by-other-providers"></a>Alustage teist pakkujate mallide muutmist

1. Valige äridokumendi halduse tööruumis dokument, mida soovite mallina kasutada.

    ![Dokumendi valimine äridokumentide halduse tööruumi lehel.](./media/BDM-Overview-EditingTemplate3.png)

2. Valige **Uus dokument** ja väljal **Pealkiri** muutke vajadusel redigeeritava malli pealkirja. Tekstiga nimetatakse ise tekkivat ER-vormingu seadistust. Pange tähele, et selle muudetavat malli sisaldava seadistuse (**Kliendi FTI aruande (GER) koopia**) mustand märgitakse automaatselt, et kasutada seda ER-vormingut praeguse kasutaja puhul. Samal ajal kasutatakse ER-vormingu põhiseadistuse muutmata algset malli selle ER-vormingu käivitamiseks kõikide kasutajate puhul.
3. Muutke väljas **Nimi** ise tekkiva muudetava malli esimese redaktsiooni nime.
4. Muutke väljal **Kommentaar** redigeeritava malli isetekkiva redaktsiooni märkust.
5. Muutmis alustamise kinnitamiseks valige **OK**.

![Uue malli loomiseks redigeerimisprotsessi alguse kinnitamine.](./media/BDM-Overview-EditingTemplate4.png)

Kui ühtegi teenusepakkujat pole, pakutakse selle loomist. Kui aktiivset teenusepakkujat ei ole, pakutakse talle võimalust valida see aktiveerimiseks.

Pakkuja loomiseks muutke väljal **Nimi** teenusepakkuja nime, värskendage uue pakkuja välja **Interneti-aadress** ja klõpsake kinnitamiseks nuppu **OK**.

   ![BDM-is uue pakkuja loomine.](./media/bdm_create_provider.png)

Olemasoleva pakkuja aktiveerimiseks valige väljal **Konfiguratsioonipakkuja** pakkuja pakkuja nimi ja valige **OK**, et seada pakkuja aktiivseks.

   ![Pakkuja aktiveerimine BDM-is.](./media/bdm_choose_provider.png)

> [!NOTE]
> Iga BDM-i mall viitab pakkujale kui konfiguratsiooni autorile. Seetõttu on malli jaoks vaja aktiivset pakkujat.


Suvand **Uus dokument** on alati saadaval praeguse ja teise pakkuja (selles näites Microsofti) ER-vormingu seadistusega mallil, millel pole redaktsiooni. Muudetud malli saab seejärel muuta uues ise loodavas ER-vormingus seadistusega.



### <a name="start-editing-a-template"></a>Alustage malli muutmisest

1. Valige valitud mallis **Dokumendi redigeerimine**.
2. Muutke väljas **Nimi** ise tekkiva muudetava malli esimese redaktsiooni nime.
3. Muutke väljas **Kommentaar** ise tekkiva muudetava malli redaktsiooni märkust.

    ![Malli redigeerimine äridokumentide halduse tööruumi lehel.](./media/BDM-Overview-EditingTemplate5.png)

4. Muutmis alustamise kinnitamiseks valige **OK**.

Avaneb leht **BDM malli muutja**. Valitud malli saab redigeerida internetis Microsoft 365 abil.

![Äridokumentide halduse malli muutmisleht.](./media/BDM-Overview-EditingLayout1.png)

### <a name="edit-a-template-in-microsoft-365"></a><a name="EditInOffice365"></a>Malli redigeerimine rakenduses Microsoft 365

Te saate malli muuta Microsoft 365 abil. Näiteks muuda veebilehitsejast kasutatavas Office’is malli päise välja küsimuste font **Tavaline** fondiks **Paks**. Need muudatused salvestatakse automaatselt malli peamises salvestusruumis (tavaliselt Azure bloobi salvestusruum) hoitava muudetava malli jaoks. See on konfigureeritud ER raamistiku jaoks.

![Fondi paksuks kirjaks muutmine malli päises äridokumendi halduse malli muutmislehel.](./media/BDM-Overview-EditingLayout2.png)

### <a name="edit-a-template-in-the-office-desktop-application"></a><a name="EditInOfficeDesktopApp"></a>Muuda malli Office’i töölauarakenduses

> [!NOTE]
> See funktsioon on saadaval ainult siis, kui **SharePointi dokumenditüübi** parameeter on õigesti konfigureeritud. Lisateavet vt teemast [Parameetrite konfigureerimine](#SetupBdmParameters).

1. Malli muutmiseks Office’i töölauarakenduse funktsioonidega (selles näites Exceliga) valige **Ava töölauarakenduses**. Muudetav mall kopeeritakse alalisest salvestusruumist ajutisse salvestusruumi, mis on äridokumentide halduse näitajatega määratletud kui SharePoint kaust.
2. Kinnitage, et tahate avada malli Office’i töölaua Exceli rakendusega ajutisest faili salvestusruumist.

    ![Exceli töölauaraenduses avatud mall.](./media/BDM-Overview-EditingLayout3.png)

3. Muutke malli. Näiteks muutke malli päise väljade küsimuste fondi värv **Must** värviks **Sinine**.

    ![Malli päises fondi värvi muutmine Exceli töölauarakendust kasutades.](./media/BDM-Overview-EditingLayout4.png)

4. Malli muudatuste salvestamiseks ajutisse salvestusruumi valige Exceli töölaua rakenduses **Salvesta**.

    ![Äridokumentide halduse malli muutmislehel muudatuste salvestamine kasutades Exceli töölauarakendust.](./media/BDM-Overview-EditingLayout5.png)

5. Sulgege Exceli töölaua rakendus.
6. Ajutise malli salvestusruumi ajakohastamiseks alalise malli salvestusruumiga valige **Ajakohasta salvestatud koopia**.

> [!NOTE]
> Ajutises faili salvestusruumis oleva muudetava malli koopiat hoitakse alles vaid malli muutmise praeguse seansi ajaks. Kui lõpetate selle seansi lehe **BDM malli muutja** sulgemisega, see koopia kustutatakse. Kui muutsite ajutises faili salvestusruumis olevat malli ja ei valinud **Ajakohasta salvestatud koopia**, kui üritasite sulgeda lehte **BDM malli muutja**, küsitakse, kas tahate salvestada tehtud muudatused. Muudatuste salvestamiseks alalises faili asukohas asuvasse malli valige **Jah**.

### <a name="validate-a-template"></a>Valideeri mall

1. Lehel **BDM malli muutja** valige **Probleemide kontroll**, et valideerida muudetud mall asjakohase ER-vormingu seadistuse suhtes. Järgige soovitusi (kui olemas), et mall vastaks ER-vormingu põhiseadistuse vormingu ülesehitusele.
2. Valige **Näita vormingut**, et näha ER-vormingu põhiseadistuse vormingu praegust ülesehitust, mis peab vastama muudetavale mallile. 
3. Paani sulgemiseks valige **Peida vorming**.

    ![BDM BDM malli muutmise leht.](./media/BDM-Overview-EditingTemplate6.png)

4. Sulgege leht **BDM malli muutja**.

Värskendatud malli näidatakse vahekaardil **Mall**. Pange tähele, et muudetud malli olek on nüüd **Mustand** ja praegune redaktsioon pole enam tühi. See tähendab seda, et seda malli on hakatud muutma.

![Värskendatud malli vaatamine äridokumentide halduse tööruumi lehel.](./media/BDM-Overview-EditingTemplate5.png)

### <a name="test-the-modified-template"></a>Katsetage muudetud malli 

1. Vahetage rakenduses ettevõtte **USMF**-i vastu.
2. Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.
3. Valige arve **FTI-00000002** ja seejärel valige **Prindihaldus**.
4. Valige **Moodul – müügireskontro** \> **Dokumendid** \> **Vabas tekstis arve** \> **Algne dokument** tase, et määratleda töötlemiseks arvete ulatus.
5. Väljas **Aruandevorming** valige dokumendi taseme ER-vorming **Kliendi FTI aruande (GER) koopia**.

    ![Prindihalduse seadete leht.](./media/BDM-Overview-TestRun1.png)

6. Praeguse lehe sulgemiseks vajutage **Paoklahv**.
7. Valige **Prindi** ja seejärel valige **Valitud**.
8. Laadige dokument alla ja avage see Exceli töölaua rakendusega.

![Vabas tekstis arvete leht.](./media/BDM-Overview-TestRun2.png)

Muudetud malliga luuakse valitud üksuse vabas tekstis arve aruanne. Selleks, et analüüsida, kuidas malli muudatused mõjutavad seda aruannet, saate selle aruande käivitada ühes rakenduse seansis kohe pärast malli muutmist teises rakenduse seansis.

### <a name="create-an-alternative-template-revision"></a>Looge malli asendusredaktsioon

1. Avage leht **BDM malli muutja** ja valige mall **Kliendi FTI aruande (GER) koopia**.
2. Valige vahekaardil **Redaktsioonid** **Uus**.
3. Vajadusel muutke väljas **Nimi** teise redaktsiooni nime vastavalt praegu aktiivsele esimesele redaktsioonile.
4. Vajadusel muutke väljas **Kommentaar** ise tekkiva muudetava malli redaktsiooni märkust.

    ![Malli redaktsioonide loomine äridokumentide halduse tööruumi lehel.](./media/BDM-Overview-AddRevision.png)

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

![Malli muudatustest loobumine äridokumentide halduse tööruumi lehel.](./media/BDM-Overview-RevokeChanges.png)

1. Valige lehel **BDM malli muutja** vahekaart **Mall**.
2. Valige käsk **Võta tagasi**.
3. Kui valite malli muudatuste tühistamiseks **OK**, asendatakse muudetud mall algse malliga ja kõik muudatused eemaldatakse. Kui tühistate malli muudatused, saate kustutada malli. Muude valikute avastamiseks valige **Tühista**.

### <a name="publish-a-modified-template"></a>Avaldage muudetud mall

1. Valige lehe **BDM malli muutja** vahekaardil **Mall** valik **Avalda**.
2. Kui valite avaldamise kinnitamiseks **OK**, märgitakse lõpetatuks muudetud malliga ER-vormingu **Kliendi FTI aruande (GER) koopia** saadud mustand. Muudetud mall muutub teistele kasutajatele saadavaks. Selle ER-vormingu lõplikud versioonid säilitavad vaid malli viimase aktiivse redaktsiooni. Muud redaktsioonid kustutatakse. Muude valikute avastamiseks valige **Tühista**.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="i-selected-edit-document-but-instead-of-going-to-the-bdm-template-editor-page-in-finance-i-was-sent-to-the-microsoft-365-webpage"></a>Valisin suvandi Redigeeri dokumenti, kuid lehele BDM malliredaktor minemise asemel rakenduses Finance suunati mind Microsoft 365 veebilehele.

See on teadaolev Microsoft 365 ümbersuunamisega seotud probleem. See esineb, kui logite sisse Microsoft 365-sse esimest korda. Selle probleemi lahendamiseks valige oma brauseris **Tagasi**, et naasta eelmisele lehele.

### <a name="i-understand-how-to-edit-a-template-by-using-microsoft-365-in-the-first-application-session-and-how-to-use-the-template-in-the-second-application-session-and-adjust-the-template-to-see-how-my-changes-affect-the-generated-business-document-can-i-use-the-office-desktop-application-in-the-same-way"></a>Mõistan, kuidas redigeerida malli Microsoft 365-ga esimeses rakenduse seansis ja kuidas kasutada malli teises rakenduse seansis ja kuidas malli muuta, et näha, kuidas minu muudatused mõjutavad loodud äridokumenti. Kas ma saan kasutada Office’i töölauarakendust samal viisil?

Jah, saate. Esimeses rakenduse seansis valige **Avage töölauarakenduses**. Mall salvestatakse ajutisse faili salvestusruumi ja avatakse Office’i töölaua rakendusega. Järgmisena täitke järgmised etapid, et näha eelvaadet loodud äridokumendi malli muudatustest:

1. Muutke malli Office’i töölauarakendusega.
2. Valige Office’i töölauarakenduses **Salvesta**.
3. Valige esimese rakenduse seansi lehel **BDM malli muutja** valik **Ajakohasta salvestatud koopia**.
4. Käivitage see malli ER-vorming teises rakenduse seansis.

### <a name="when-i-select-open-in-desktop-app-i-receive-the-following-error-message-value-cannot-be-null-parameter-name-externalid-how-do-i-work-around-this-issue"></a>Kui valin Ava töölauarakenduses, kuvatakse järgmine tõrketeade: „Väärtus ei saa olla null. Parameetri nimi: externalId.” Kuidas see probleem lahendada?

Tõenäoliselt logisite sisse Azure AD domeeni praegusesse rakenduse eksemplari, mis erineb Azure AD domeenist, mida kasutati selle eksemplari kasutamisel. Kuna SharePointi teenus, mida kasutatakse mallide salvestamiseks ja Office’i töölauarakendusega muutmisvõimeliseks tegemiseks, kuulub samasse domeeni, seega meil pole õigust juurde pääseda SharePointi teenusele. Selle probleemi lahendamiseks logige sisse praegusesse seansi õige Azure AD domeeni kasutava kasutaja sisselogimisandmetega.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektrooniline aruandlus. OPENXML-vormingus aruannete loomiseks konfiguratsiooni koostamine (november 2016)](tasks/er-design-reports-openxml-2016-11.md)

[Elektroonilise aruandluse konfiguratsioonide kujundamine Wordi vormingus aruannete loomiseks](tasks/er-design-configuration-word-2016-11.md)

[Manustatud pildid ja kujutised ER-iga loodud dokumentides](electronic-reporting-embed-images-shapes.md)

[Elektroonilise aruandluse (ER) konfigureerimine andmete tõmbamiseks Power BI-sse](general-electronic-reporting-report-configuration-get-data-powerbi.md)

## <a name="list-of-er-configurations-that-have-been-released-in-finance-to-support-configurable-business-documents"></a><a name="list-of-configurations-cbd"></a>Rakenduses Finance väljastatud ER-i konfiguratsioonide loend, et toetada konfigureeritavaid äridokumente

Rakenduse Finance ER-i konfiguratsioonide [loendit](general-electronic-reporting.md#list-of-configurations) värskendatakse pidevalt. Avage [Globaalne hoidla](er-download-configurations-global-repo.md), et vaadata praegu toetatud ER-i konfiguratsioonide loendit. Saate [filtreerida](../../../finance/localizations/enhanced-filtering-global-repo.md) globaalset hoidlat, et vaadata ER-i konfiguratsioonide loendit, mida kasutatakse konfigureeritavate äridokumentide toetamiseks.

![Globaalse hoidla sisu filtreerimine konfiguratsioonihoidla lehel.](./media/bdm-overview-filterglobalrepo.gif)

Järgmises tabelis on toodud ER-i konfiguratsioonide loend, mis toetavad konfigureeritavaid äridokumente ja mis on rakenduses Finance väljastatud kuni 2020. a detsembrini.

| Andmemudeli konfiguratsioon    | Vormingu konfiguratsioonid                           |
|-----------------------------|-------------------------------------------------|
| Veokirja mudel        | Veokiri (Excel)                          |
|                             | Veokiri (Word)                           |
| Päritolusertifikaadi mudel | Päritolusertifikaat (Excel)                   |
|                             | Päritolusertifikaat (Word)                    |
| Arve mudel               | Kliendi deebet- ja kreeditarve (Excel)          |
|                             | Kliendi deebet- ja kreeditarve (Word)           |
|                             | Vabas vormis arve (Excel)                       |
|                             | Vabas vormis arve (Excel) (BH)                  |
|                             | Vabas vormis arve (FR) (Excel)                  |
|                             | Vabas vormis arve (LT) (Excel)                  |
|                             | Vabas vormis arve (LV) (Excel)                  |
|                             | Vabas vormis arve (PL) (Excel)                  |
|                             | Vabas vormis arve (CZ) (Excel)                  |
|                             | Vabas vormis arve (EE) (Excel)                  |
|                             | Vabas vormis arve (HU) (Excel)                  |
|                             | Vabas vormis arve (TH) (Excel)                  |
|                             | Vabas vormis arve (Word)                        |
|                             | Projektilepingu reaüksused (Excel)             |
|                             | Projektilepingu reaüksused (CZ) (Excel)        |
|                             | Projektilepingu reaüksused (Excel) (BH)        |
|                             | Projektilepingu reaüksused (HU) (Excel)        |
|                             | Projektilepingu reaüksused (LT) (Excel)        |
|                             | Projektilepingu reaüksused (PL) (Excel)        |
|                             | Projektilepingu reaüksused (Word)              |
|                             | Projekti kliendi kinnipidamise vabastamine (Excel)      |
|                             | Projekti kliendi kinnipidamise vabastamine (CZ) (Excel) |
|                             | Projekti kliendi kinnipidamise vabastamine (HU) (Excel) |
|                             | Projekti kliendi kinnipidamise vabastamine (LT) (Excel) |
|                             | Projekti kliendi kinnipidamise vabastamine (PL) (Excel) |
|                             | Projekti kliendi kinnipidamise vabastamine (TH) (Excel) |
|                             | Projekti kliendi kinnipidamise vabastamine (Word)       |
|                             | Projekti arve (Excel)                         |
|                             | Projekti arve (Word)                          |
|                             | Projekti arve (AE) (Excel)                    |
|                             | Projekti arve (CZ) (Excel)                    |
|                             | Projekti arve (Excel) (BH)                    |
|                             | Projekti arve (HU) (Excel)                    |
|                             | Projekti arve (JP) (Excel)                    |
|                             | Projekti arve (LT) (Excel)                    |
|                             | Projekti arve (PL) (Excel)                    |
|                             | Projekti arve (TH) (Excel)                    |
|                             | Projekti täielik arve (MY) (Excel)               |
|                             | Projekti lihtne arve (MY) (Excel)             |
|                             | Projektihalduse arve (Excel)                  |
|                             | Projektihalduse arve (CZ) (Excel)             |
|                             | Projektihalduse arve (Excel) (BH)             |
|                             | Projektihalduse arve (HU) (Excel)             |
|                             | Projektihalduse arve (JP) (Excel)             |
|                             | Projektihalduse arve (LT) (Excel)             |
|                             | Projektihalduse arve (PL) (Excel)             |
|                             | Projektihalduse arve (Word)                   |
|                             | Varasem ostuarve (Excel)                |
|                             | Varasem ostuarve (Word)                 |
|                             | Müügi ettemaksuarve (Excel)                   |
|                             | Müügi ettemaksuarve (Word)                    |
|                             | Müügi ettemaksuarve (PL) (Excel)              |
|                             | Müügiarve (Excel)                           |
|                             | Müügiarve (Excel) (BH)                      |
|                             | Müügiarve (CZ) (Excel)                      |
|                             | Müügiarve (Excel) (EE)                      |
|                             | Müügiarve (Excel) (FR)                      |
|                             | Müügiarve (Excel) (HU)                      |
|                             | Müügiarve (Excel) (IN)                      |
|                             | Müügiarve (Excel) (LT)                      |
|                             | Müügiarve (Excel) (LV)                      |
|                             | Müügiarve (Excel) (PL)                      |
|                             | Müügiarve (Excel) (TH)                      |
|                             | Müügiarve (Word)                            |
|                             | TMS-i faktuurarve (Excel)                  |
|                             | TMS-i faktuurarve (Word)                   |
|                             | Hankijaarve dokument (Excel)                 |
|                             | Hankijaarve dokument (CZ) (Excel)            |
|                             | Hankijaarve dokument (HU) (Excel)            |
|                             | Hankijaarve dokument (IN) (Excel)            |
|                             | Hankijaarve dokument (LT) (Excel)            |
|                             | Hankijaarve dokument (LV) (Excel)            |
|                             | Hankijaarve dokument (MY) (Excel)            |
|                             | Hankijaarve dokument (Word)                  |
| Tellimuse mudel                 | Lepingu kinnitus (Excel)                  |
|                             | Lepingu kinnitus (Word)                   |
|                             | Ostulepingu kinnitus (Excel)         |
|                             | Ostulepingu kinnitus (Word)          |
|                             | Ostutellimus (Excel)                          |
|                             | Ostutellimus (CZ) (Excel)                     |
|                             | Ostutellimuse päring (CZ) (Excel)             |
|                             | Ostutellimus (HU) (Excel)                     |
|                             | Ostutellimuse päring (HU) (Excel)             |
|                             | Ostutellimus (Word)                           |
|                             | Ostutellimuse päring (Excel)                  |
|                             | Ostutellimuse päring (Word)                   |
|                             | Müügitellimuse kinnitus (Excel)                |
|                             | Müügitellimuse kinnitus (CZ) (Excel)           |
|                             | Müügitellimuse kinnitus (HU) (Excel)           |
|                             | Müügitellimuse kinnitus (Word)                 |
| Saatelehe mudel          | Konteineri sisu (Excel)                      |
|                             | Konteineri sisu (Word)                       |
|                             | Koormaloend (Excel)                               |
|                             | Koormaloend (Word)                                |
|                             | Komplekteerimisleht (Excel)                            |
|                             | Komplekteerimisleht (CZ) (Excel)                       |
|                             | Komplekteerimisleht (Word)                             |
|                             | Tootmise komplekteerimisloend (Excel)                    |
|                             | Tootmise komplekteerimisloend (Word)                     |
|                             | Koorma saatmise komplekteerimisloend (Excel)             |
|                             | Koorma saatmise komplekteerimisloend (Word)              |
|                             | Saadetise saatmise komplekteerimisloend (Excel)         |
|                             | Saadetise saatmise komplekteerimisloend (Word)          |
|                             | Voo saatmise komplekteerimisloend (Excel)             |
|                             | Voo saatmise komplekteerimisloend (Word)              |
| Maksemudel               | Kliendi maksesoovitus (Excel)                 |
|                             | Kliendi maksesoovitus (Word)                  |
|                             | Hankija maksesoovitus (Excel)                   |
|                             | Hankija maksesoovitus (Word)                    |
| Pakkumise mudel             | Projektipakkumine (Excel)                       |
|                             | Projektipakkumine (Word)                        |
|                             | Pakkumiskutse (Excel)                   |
|                             | Pakkumiskutse (Nõustu) (Excel)          |
|                             | Pakkumiskutse (Nõustu) (Word)           |
|                             | Pakkumiskutse (Keeldu) (Excel)          |
|                             | Pakkumiskutse (Keeldu) (Word)           |
|                             | Pakkumiskutse (Tagasta) (Excel)          |
|                             | Pakkumiskutse (Tagasta) (Word)           |
|                             | Pakkumiskutse (Word)                    |
|                             | Müügipakkumine (Excel)                         |
|                             | Müügipakkumine (CZ) (Excel)                    |
|                             | Müügipakkumine (HU) (Excel)                    |
|                             | Müügipakkumine (Word)                          |
|                             | Müügipakkumise kinnitus (Excel)            |
|                             | Müügipakkumise kinnitus (Word)             |
| Vastavusseviimise mudel        | Kliendi kontoväljavõte, Ext (Excel)             |
|                             | Kliendi kontoväljavõte, Ext (CN) (Excel)        |
|                             | Kliendi kontoväljavõte, Ext (Word)              |
|                             | Kliendi kontoväljavõte, Prantsusmaa (Excel)          |
| Meeldetuletuse mudel              | Märgukirja märkus (Excel)                  |
|                             | Märgukirja märkus (CN) (Excel)             |
|                             | Märgukirjamärkus (Word)                   |
|                             | Kliendi viivisearve (Excel)                  |
|                             | Kliendi viivisearve (Word)                   |
| Veokirja mudel               | Koorma maksevahend (Excel)                             |
|                             | Koorma maksevahend (Word)                              |
|                             | Ostutellimuse saateleht (Excel)             |
|                             | Ostutellimuse saateleht (CZ) (Excel)        |
|                             | Ostutellimuse saateleht (Word)              |
|                             | Marsruut (Excel)                                   |
|                             | Marsruut (Word)                                    |
|                             | Müügitellimuse saateleht (Excel)                |
|                             | Müügitellimuse saateleht (CZ) (Excel)           |
|                             | Müügitellimuse saateleht (LT) (Excel)           |
|                             | Müügitellimuse saateleht (PL) (Excel)           |
|                             | Müügitellimuse saateleht (Word)                 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
