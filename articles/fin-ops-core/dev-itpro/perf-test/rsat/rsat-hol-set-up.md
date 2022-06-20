---
title: Tööriista Regression Suite Automation Tool seadistamise ja installimise õppetükk
description: See artikkel on õppetükk, mis näitab, kuidas regressionkomplekti automatiseerimistööriista (RSAT) seadistada ja installida.
author: tonyafehr
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: ec4ae765aaac038e6c7eff11403fb21ebd27fc2c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858586"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Tööriista Regression Suite Automation Tool seadistamise ja installimise õppetükk

See artikkel on õppetükk, mis aitab teil saada seadistust ja alustada RSAT-iga ning RSAT-iga seostatud tööriistadega.

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> Kasutage Interneti-brauseri tööriistu selle lehe allalaadimiseks ja salvestamiseks PDF-vormingus.

## <a name="key-concepts"></a>Põhimõisted

- Mõistate installimise ja eeltingimuste seadistus, mis on vajalik mitmesuguste rakenduste jaoks, mis toetavad tööriista Regression suite automation tool (RSAT).
- Mõistate, kuidas saate tegevuse salvestaja funktsiooniga koos teenustega Microsoft Dynamics Lifecycle Services (LCS) ja Microsoft Azure DevOps luua, konfigureerida, käitada ja uurida testjuhtumeid ning nende kohta aruandeid esitada.
- Volitage funktsiooni kasutajaid kirjendama äriülesandeid, kasutades tegevuse salvestajat, ja seejärel teisendage ülesande salvestised automaatsete katsete komplekti, ilma et peaksite kirjutama lähtekoodi.

## <a name="before-you-begin"></a>Enne alustamist

### <a name="prerequisites"></a>Eeltingimused

- Selle õppetüki jaoks on vaja keskkonda, kus töötab Microsoft Dynamics 365 for Finance and Operationsi versioon 10.0 (aprill 2019) või uuem versioon. Klientide jaoks, kes kasutavad Microsoft Dynamics 365 for Finance and Operationsi, Enterprise edition 7.3, toetatakse ka platvormivärskendust 20 (PU20) või uuemat versiooni.
- Kasutajal peavad olema selle keskkonna administraatoriõigused.
- Teil peab olema juurdepääs kliendi rentniku LCS-ile ja Azure DevOpsile (varem Microsoft Visual Studio Team Services \[VSTS\]).
- Kasutajal, kes loob ja haldab testkomplekte, peab olema Azure DevOpsi katseplaanide või katsehalduri litsents. Katseplaanidele annavad juurdepääsu ka järgmised litsentsid.
    - Visual Studio ettevõtte litsents
    - Visual Studio Test Professionali litsents
    - MSDN-i platvormide tellija litsents
- RSAT-l peab olema juurdepääs katsekeskkonnale veebibrauseri kaudu.
- Katseparameetrite loomiseks ja redigeerimiseks peab olema installitud Microsoft Excel.

## <a name="configure-azure-devops"></a>Teenuse Azure DevOps konfigureerimine

### <a name="user-eligibility"></a>Kasutaja sobivus

Veenduge, et kasutaja oleks loodud Azure DevOpsis ja tal oleks tellimustase, mis annab juurdepääsu Azure’i katseplaanidele. Azure DevOpsi katseplaanide litsentsi on vaja vaid siis, kui kasutaja loob ja haldab katsejuhtumeid (ehk kõikidel RSAT kasutajatel seda litsentsi vaja pole). Teavet litsentsi nõudmiste kohta vt teemast [Litsentsi nõudmised](/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Uue Azure DevOpsi projekti loomine

RSAT kasutab Azure DevOpsi testjuhtumi ja testkomplekti halduseks, aruandluseks ja testkäivituse tulemuste uurimiseks.

> [!NOTE]
> Võite kasutada olemasolevat Azure DevOpsi projekti. Kuid kui olemasolev Azure DevOpsi projekt on seadistatud nii, et sellel on kohandatud mall, saate tõrke „VSTS-i sünkroonimistõrge”, kui sünkroonite testjuhtumeid äriprotsesside modelleerijast (BPM) Azure DevOpsi (vt jaotist [BPM-st Azure DevOpsi sünkroonimise testimine](#test-the-synchronization-from-bpm-to-azure-devops)). Kui kohandatud malli korral on järgitud järgmisi parimaid tavasid, saate sünkroonida testjuhtumid Azure DevOpsi. (Parimad tavad on loendatud tõrketeates.)

- Ärge kustutage ühtegi tööüksuse tüüpi või valmiskujul välja.
- Ärge kustutage ühtegi tööüksuse tüübi olekut.
- Ärge lisage tööüksuse tüübile ühtegi kohustuslikku välja.

![Tõrketeade parimate tavade loendiga.](./media/setup_rsa_tool_02.png)

Muidu soovitame selle õppetüki jaoks luua uue Azure DevOpsi projekti. Lisateavet vt teemast [Probleemid BPM-i sünkroonimisel kohandatud Azure DevOpsi (VSTS) protsessimalliga](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Avage Azure DevOpsi URL (`https://dev.azure.com/<Azure DevOps Name>`).
2. Valige suvand **Projekti loomine** Azure DevOpsi lehelt ülevalt paremalt nurgast.

    ![Projekti loomise nupp.](./media/setup_rsa_tool_03.png)

3. Täitke järgmise väljad ja valige käsk **Loo**.

    - **Projekti nimi**
    - **Versiooni kontroll** – valige suvand **Team Foundationi versioonikontroll**. Pange tähele, et vaikesuvandit **Git** ei toetata.
    - **Tööüksuse protsess**

    ![Uue projekti loomise dialoogiaken.](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Isikliku pääsutõendi loomine

Selles õppetükis kasutate LCS-i äriprotsessi modelleerijat (BPM) testjuhtumi teegi loomiseks ja testjuhtumite loomiseks Azure DevOpsiga. Vajate isiklikku pääsutõendit BPM-i sünkroonimiseks Azure DevOpsiga.

1. Valige profiili ikoon Azure DevOpsi projekti lehe ülevalt paremalt nurgast ja seejärel valige suvand **Turve**.

    ![Turbe käsk.](./media/setup_rsa_tool_05.png)

2. Vasakul paanil jaotisest **Turve** valige suvand **Isiklikud pääsutõendid**. Seejärel valige suvand **Uus tõend**.

    ![Nupp Uus tõend isiklike pääsutõendite vahekaardil kasutajasätetes.](./media/setup_rsa_tool_06.png)

3. Täitke järgmise väljad ja valige käsk **Loo**.

    - **Nimi**
    - **Aegumine (UTC)** – valige suvand **Määratletud kohandatud** ja seejärel kasutage kuupäevavalijat viimase saadavuskuupäeva valimiseks.
    - **Ulatused** – valige suvand **Täielik juurdepääs**.

    ![Isiklik pääsutõendi loomise dialoogiaken.](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Märkige loodud isiklik pääsutõend üles. Seda läheb vaja hiljem, kui seadistate RSAT konfiguratsiooni.

    ![Isiklik pääsutõend.](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>LCS-i projekti konfigureerimine

Testide ülemteegi jaoks on vaja teenuse Lifecycle Services (LCS) projekti. LCS äriprotsesside modelleerijat (BPM) kasutatakse testjuhtumite ülemteegina. BPM-i kasutatakse testteekide haldamiseks ja jaotamiseks LCS-i projektides. Näiteks testteeke loov Microsofti partner või sõltumatu tarkvarahankija (ISV) väljastab testteegid BPM-i teekidena. BPM-is on testjuhtumid korraldatud äriprotsessi järgi. BPM ei määratle testi läbimise täitmisjärjestust või -sagedust. Neid üksikasju hallatakse Azure DevOps selles artiklis allpool kirjeldatud viisil.  

LCS-i projekti jaoks saate kasutada olemasolevat kliendi juurutus- või partneriprojekti.

### <a name="update-the-lcs-language"></a>LCS-i keele värskendamine

> [!NOTE]
> Selleks et kasutajaliides (UI) kuvaks äriprotsesse õigesti, peab LCS-i eelistatud keel olema määratud valikule **Inglise (USA)**.

1. Minge LCS-i juurutusprojekti.
2. Valige paremast ülanurgast nupp **Sätted** (hammasrattasümbol) ja seejärel valige **Keele-eelistus**.

    ![Keele-eelistuse värskendamine.](./media/setup_rsa_tool_09.png)

3. Valige väljast **Eelistatud keel** suvand **Inglise (USA)** ja seejärel valige nupp **Salvesta**.

    ![Keele-eelistuse vahekaart kasutajasätetes.](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>LCS-i konfigureerimine ühenduse loomiseks Azure DevOpsi projektiga

Kui lõite varem uue Azure DevOpsi projekti, konfigureerige LCS-i projekt sellega ühendumiseks. Kui LCS-i projekt on juba Azure DevOpsi projekti ühendatud, võite minna edasi järgmisse jaotisesse.

1. Minge LCS-i juurutusprojekti.
2. Valige nupp **Menüü** ja seejärel suvand **Projekti sätted**.

    ![Projekti sätete käsk.](./media/setup_rsa_tool_11.png)

3. Valige vasakult paanilt **Visual Studio Team Services** ja seejärel suvand **Teenuse Visual Studio Team Services seadistamine**.

    ![Teenuse Visual Studio Team Services vahekaart projekti sätetes.](./media/setup_rsa_tool_12.png)

4. Välja **Azure DevOpsi saidi URL** sisestage Azure DevOpsi saidi URL. Välja **Isiklik pääsutõend** sisestage varem loodud isiklik pääsutõend.

    > [!NOTE]
    > Kuigi VSTS kannab nüüd nime Azure DevOps, kasutage LCS-i ühendamiseks Azure DevOpsi projektiga vana URL-i. Näiteks selles õppetükis kasutatud Azure DevOpsi URL on `https://dev.azure.com/D365FOFastTrack/`. Kuid järgmisel joonisel on see sisestatud kujul `https://D365FOFastTrack.visualstudio.com/`.

    ![Teenuse Visual Studio Team Services seadistamise 1. etapp.](./media/setup_rsa_tool_13.png)

5. Valige nupp **Jätka**.
6. Väljas **Teenuse Visual Studio Team Services projekt** valige valitud saidi VSTS-i projekt, mille soovite siduda LCS projektiga. Väli **Protsessimall** seatakse vaikimisi väärtusele **Kiire**. Kohandatud malli jaoks vaadake üle heade tavade juhised jaotises [Uue Azure DevOpsi projekti loomine](#create-a-new-azure-devops-project). Seejärel valige nupp **Jätka**.

    ![Teenuse Visual Studio Team Services seadistamise 2. etapp.](./media/setup_rsa_tool_14.png)

7. Vaadake sätted üle ja valige nupp **Salvesta**.

    ![Teenuse Visual Studio Team Services seadistamise 3. etapp.](./media/setup_rsa_tool_15.png)

8. Valige nupp **Autoriseerimine**, et anda LCS-ile volitus juurdepääsuks konfigureeritud Azure DevOpsi saidile teie nimel ja VSTS-iga integreeritavate funktsioonide sisse lülitamiseks.

    ![Nupp Autoriseerimine.](./media/setup_rsa_tool_16.png)

9. Kuvatakse teateaken tekstiga „Teid suunatakse ümber välisele saidile, et lubaksite LCS-il teie nimel teenusega Visual Studio Team Services ühenduse luua. Kas soovite jätkata?” Valige **Jah**.

    ![Teateaken.](./media/setup_rsa_tool_17.png)

10. Valige **Aktsepteerimine**.

    ![Juurdepääsu autoriseerimine.](./media/setup_rsa_tool_18.png)

11. Kui olete autoriseeritud kasutajana, peaks kasutajaliides viima teid tagasi LCS-i projekti sätete lehele.

    ![Autoriseeritud kasutaja.](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Uue BPM-i teegi loomine

1. Minge LCS-i juurutusprojekti.
2. Valige nupp **Menüü** ja seejärel suvand **Äriprotsesside modelleerija**.

    ![Äriprotsesside modelleerija käsk.](./media/setup_rsa_tool_20.png)

3. Valige suvand **Uus teek**.

    ![Uue teegi nupp.](./media/setup_rsa_tool_21.png)

4. Välja **Teegi nimi** sisestage nimi ja seejärel valige nupp **Loo**. Selle õppetüki käigus pange BPM-i teegi nimeks **RSAT**.

    ![Uue teegi loomise dialoogiaken.](./media/setup_rsa_tool_22.png)

5. Avage uus **RSAT** BPM-i teek.
6. Valige protsess **Peamise äriprotsessi näidis** ja seejärel valige paremalt suvand **Redigeerimisrežiim**.

    ![Redigeerimisrežiimi nupp.](./media/setup_rsa_tool_23.png)

7. Muutke väljade **Nimi** ja **Kirjeldus** väärtus valikule **Toote loomine**. Seejärel valige nupp **Salvesta**.

    ![Väljad Nimi ja Kirjeldus.](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Keskkond

### <a name="version-requirement"></a>Nõudmised versioonile

Vajalik on katse- või liivakastikeskkond versiooniga 10. Klienride jaoks, kes kasutavad versiooni 7.3, toetatakse ka platvormivärskendust 20 või uuemat versiooni.

> [!NOTE]
> RSAT-il peab olema juurdepääs teie katsekeskkonnale veebibrauseri kaudu.

### <a name="user-criteria"></a>Kasutaja kriteeriumid

Kasutajal peavad olema selle keskkonna administraatoriõigused.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Spikri sätete seadistamine ühenduse loomiseks LCS-iga

See etapp on vajalik ühenduse loomiseks LCS-iga, et tegevuse salvestisi saaks salvestada vastavasse BPM-i teeki LCS-is kliendi kaudu.

1. Avage klient.
2. Minge jaotisse **Süsteemihaldus \> Seadistus \> Süsteemi parameetrid**.
3. Vahekaardil **Spikker** väljas **Teenuse Lifecycle Services spikri konfiguratsioon** valige vastav LCS-i projekt (selles õppetükis **RSAT**).

    ![Teenuse Lifecycle Services spikri konfiguratsiooni väli vahekaardil Spikker.](./media/setup_rsa_tool_25.png)

    BPM-i teegid täidetakse vastavas LCS-i projektis.

4. Valige käsk **Salvesta**.
5. Spikri uuendatud sisu nägemiseks peate võib-olla brauserit värskendama.

    ![Teatis brauseri värskendamise kohta.](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Tegevuse salvestised

> [!NOTE]
> Veenduge, et kõik tegevuse salvestised algaksid peamiselt armatuurlaualt. Hoidke üksikud salvestised lühikesed ja keskenduge ühele äriülesandele, näiteks müügitellimuse loomisele.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Tegevuse salvestise loomine ja salvestamine BPM-i teeki

Looge vastav tegevuse salvestis, mida saate manustada uues BPM-i teegis loodud lihtsa äriprotsessi juurde.

1. Avage klient.
2. Valige peamiselt armatuurlaualt nupp **Sätted** (hammasratta sümbol) ja seejärel valige suvand **Tegevuse salvestaja**.

    ![Valige menüüs Sätted suvand Tegevuse salvestaja.](./media/setup_rsa_tool_27.png)

3. Valige nupp **Salvestise loomine**.

    ![Salvestise loomise nupp.](./media/setup_rsa_tool_28.png)

4. Täitke väljad **Salvestise nimi** ja **Salvestise kirjeldus** ja seejärel valige nupp **Alusta**.

    ![Salvestise nime ja salvestise kirjelduse väljad.](./media/setup_rsa_tool_29.png)

5. Salvestage toote loomise etapid. Kui olete lõpetanud, valige nupp **Peata** salvestamise lõpetamiseks.

    ![Toote loomise etapid.](./media/setup_rsa_tool_30.png)

6. Valige suvand **Salvesta teenustesse Lifecycle Services**.

    ![Tegevuse salvestise salvestamine teenusesse Lifecycle Services.](./media/setup_rsa_tool_31.png)

    Teegi teave laaditakse LCS-ist.

    ![Teegi teabe laadimine.](./media/setup_rsa_tool_32.png)

7. Valige tegevuse salvestisega seostamiseks BPM-i teek. Selles õppetükis valige varem loodud BPM-i teek **RSAT** ja selle all äriprotsess **Toote loomine**. Seejärel valige **OK**.

    ![Tegevuse salvestise seostamine BPM-i teegi ja äriprotsessiga.](./media/setup_rsa_tool_33.png)

    Ilmub teade „Salvestamine teenusesse Lifecycle Services õnnestus”.

    ![Teade õnnestunud salvestamisest LCS-i.](./media/setup_rsa_tool_34.png)

8. Kui soovite salvestada tegevuse salvestise lokaalselt ja seejärel laadida selle üles BPM-i LCS-i, järgige alltoodud etappe.

    1. Kui salvestamine on lõpule viidud, valige suvand **Salvesta sellesse arvutisse**.

        ![Salvesta sellesse arvutisse.](./media/setup_rsa_tool_35.png)

    2. Brauseri teavitusribalt valige nupp **Salvesta** või **Salvesta nimega**, et salvestada fail kohalikku arvutisse.

        ![Teavitusriba.](./media/setup_rsa_tool_36.png)

    3. Valige BPM-i teek **RSAT** ja seejärel äriprotsess tegevuse salvestise salvestamiseks.
    4. Vahekaardil **Ülevaade** valige nupp **Laadi üles**.

        ![Nupp Laadi üles.](./media/setup_rsa_tool_37.png)

    5. Valige nupp **Sirvi** ja seejärel valige varem salvestatud fail .axtr. Seejärel valige nupp **Laadi üles**.

        ![Üleslaadimiseks faili .axtr valimine.](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>BPM-ist Azure DevOpsi sünkroonimise testimine

Kui tegevuse salvestis on äriprotsessi juurde manustatud, peate kinnitama, et äriprotsessi ja seotud tegevuse salvestist saab sünkroonida Azure DevOpsi funktsioonina ja testjuhtumina (vastavalt), kasutades LCS-is VSTS-i sünkroonimise funktsiooni.

> [!NOTE]
> Vastav tööüksuse tüüp, mis Azure DevOpsis luuakse, on erinev, olenevalt protsessimallist, mille valisite LCS-i projekti konfigureerimisel Azure DevOpsiga, nagu on kirjeldatud jaotises [Uue Azure DevOpsi projekti loomine](#create-a-new-azure-devops-project).

1. Minge BPM-i teeki ja avage varem loodud **RSAT** teek.
2. Valige kolmikpunkti nupp (**...**) ja seejärel suvand **VSTS-i sünkroonimine**.

    ![VSTS-i sünkroonimise käsk kolmikpunkti menüüs.](./media/setup_rsa_tool_39.png)

    Kui VSTS-i sünkroonimine on lõpule viidud, ilmub vasakule vahekaart **Nõuded**, mis sisaldab vastavat Azure DevOpsi tööüksust.

    > [!NOTE]
    > Azure DevOpsis loodud tööüksusel on pealkirja eesliiteks BPM-i teegi nimi.

    ![Vahekaart Nõuded.](./media/setup_rsa_tool_40.png)

3. Värskendage lehte.
4. Valige kolmikpunkti nupp (**...**). Näete lisasuvandit, **Testjuhtumite sünkroonimine**. Valige see suvand.

    ![Testjuhtumite sünkroonimise käsk kolmikpunkti menüüs.](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Kui suvand **Testjuhtumite sünkroonimine** ei ole pärast lehe värskendamist saadaval, minge BPM-i pealehele ja valige suvand **Testjuhtumite sünkroonimine** kogu teegile. Seda saate tõhusalt sundkäivitada kogu teegi sünkroonimise.
    >
    > ![Suvandi Testjuhtumite sünkroonimine kogu teegi jaoks.](./media/setup_rsa_tool_42.png)

    Kui testjuhtumite sünkroonimine on lõpule viidud, luuakse vahekaardil **Nõuded** uus testjuhtum.

    ![Uus testjuhtum vahekaardil Nõuded.](./media/setup_rsa_tool_43.png)

5. Avage Azure DevOpsi projekt ja valige suvandid **Tahvlid \> Tööüksused**.

    ![Tööüksuste käsk jaotises Tahvlid.](./media/setup_rsa_tool_44.png)

6. Kinnitage, et BPM-i sünkroonimise kaudu loodud tööüksus ja testjuhtum on olemas.

    ![Tööüksus ja testjuhtum.](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>RSAT installimine ja konfigureerimine

RSAT-d saab installida igasse arvutisse, kus töötab Windows 10 ja mille saab ühendada veebibrauseri kaudu (Internet Explorer või Google Chrome) keskkonnaga.

> [!NOTE]
> Enne tööriista uue versiooni installimist soovitame varasema versiooni desinstallida.

### <a name="install-an-authentication-certificate"></a>Autentimisserdi installimine

Autentimise lubamiseks peate looma ja installima serdi samasse arvutisse, kus töötab RSAT.

#### <a name="generate-a-certificate"></a>Serdi loomine

1. Serdifaili loomiseks avage administraatorina Microsoft Windows PowerShelli aken ja käivitage järgmine käsk.

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Avage serdihaldus, sisestades käsu **certlm.msc** dialoogiaknasse **Käivita**, ja kinnitage, et sert **D365 automaattestimise sert** luuakse jaotisesse **Isiklik \> Serdid**.

    > [!NOTE]
    > Sisestage kindlasti **certlm.msc**, mitte **certmgr.msc**, sest serte salvestatakse kohalikus arvutis.

    ![D365 automaattestimise sert.](./media/setup_rsa_tool_46.png)

3. Tehke serdil paremklõps ja valige käsk **Kopeeri**.
4. Valige suvandid **Usaldusväärsed juurserdi haldurid \> Serdid**.

    ![Sertide kaust kaustas Trusted Root Certification Authorities.](./media/setup_rsa_tool_47.png)

5. Valige menüüst **Tegevus** käsk **Kleebi**, et kopeerida sert asukohta **Usaldusväärsed juurserdi haldurid**.

    ![Kleepimise käsk menüüs Tegevus.](./media/setup_rsa_tool_48.png)

6. Installitud serdi sõrmejälje saamiseks (ilma tühikute ja erimärkideta) avage administraatorina Windows PowerShelli aken ja käivitage järgmised käsud.

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Salvestage sõrmejälg, kuna vajate seda hiljem wif-failide värskendamisel rakendusobjekti serveri (AOS) jaoks ja RSAT konfiguratsiooni seadistamiseks.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>AOS-i arvuti konfigureerimine ühenduse usaldamiseks

> [!NOTE]
> Kui keskkond on järgu 2+ keskkond, tuleb serdi sõrmejälge värskendada failis wif.config keskkonna **kõikide** AOS-i arvutite jaoks.

1. Looge AOS-i arvutiga Remote Desktop Protocoli (RDP) ühendus. Sisselogimise üksikasjad on saadaval LCS-is keskkonna üksikasjade lehel.
2. Avage teenus Microsoft Internet Information Services (IIS) ja otsige saitide loendist üles **AOSService**.

    ![AOSService saitide loendis.](./media/setup_rsa_tool_49.png)

3. Tehke paremklõps valikul **Uuri**, et avada kaust **\<Drive\>: \\AosService\\WebRoot**. Otsige üles fail **wif.config**.

    ![File wif.config kaustas WebRoot.](./media/setup_rsa_tool_50.png)

4. Värskendage faili **wif.config**, lisades serdile ja ameti nimele uus asutuse kirje, nagu on näidatud järgmises näites.

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Kui mitu kasutajat kasutab sama rakendust, peab iga kasutaja looma eraldi sõrmejäljed, mis tuleb kõik lisada jaotisesse **\<keys\>**.

5. Kui AOS-i arvuteid on rohkem kui üks, korrake etappe 3 kuni 4 iga lisaarvuti jaoks.

    > [!NOTE]
    > Erineval vanematest järgu 2 keskkondadest juurutatakse uued järgu 2 keskkonnad kahe AOS-i juhtumiga.

6. Käivitage **iisreset** kõikides AOS-i arvutites.

    > [!NOTE]
    > Kui teil pole administraatoriõigusi käsu **iisreset** käivitamiseks järgu 1 arvutis, valige LCS-is keskkonna üksikasjade lehelt suvandid Hooldamine > Teenuste taaskäivitamine.

#### <a name="tier-2-environment"></a>Järgu 2+ keskkond

Kui kasutatakse järgu 2+ (standardse vastuvõtutesti liivakast või uuem versioon) keskkonda, siis kontrollige järgmist registri sätet või seadistage see arvutis, kuhu on installitud RSAT. See etapp on vajalik, kuna see aitab vältida autentimise või RSAT ühenduse tõrkeid.

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>RSAT installimine

1. Minge lehele <https://www.microsoft.com/download/details.aspx?id=57357> ja valige käsk **Laadi alla**.
2. Valige kõik failid ja seejärel valige nupp **Edasi**.

    ![Kõikide failide valimine.](./media/setup_rsa_tool_51.png)

3. Tehke topeltklõps .msi paketil installeri käivitamiseks. Kui installimine on lõpule viidud, valige nupp **Lõpeta**.

    ![RSAT installeri fail.](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Selenium ja brauseri draiverite installimine

RSAT vanemates versioonides pidite installima Seleniumi ja brauseri draiverid. Nüüd pole neid draivereid enam vaja installida, kuna need installitakse automaatselt.

1. Esimene kord, kui RSAT avate, palutakse teil Selenium automaatselt alla laadida ja installida. Lisateavet vt jaotisest [RSAT konfigureerimine](#configure-rsat).
2. Enne kui saate testjuhtumi käivitada, palutakse teil automaatselt alla laadida ja installida brauseri draiver, mis vastab vaikebrauserile, mis valitakse RSAT konfiguratsioonis. Lisateavet vt jaotisest [Testjuhtumite laadimine ja käivitamine](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>RSAT kasutamise alustamine

### <a name="create-a-test-plan-and-test-suites"></a>Katseplaani ja testkomplektide loomine

1. Avage Azure DevOpsi projekt ja valige suvand **Katseplaanid**.

    ![Katseplaanide käsk.](./media/setup_rsa_tool_53.png)

2. Valige suvand **Uus katseplaan**.

    ![Uue katseplaani nupp.](./media/setup_rsa_tool_54.png)

3. Täitke väli **Nimi** ja seejärel valige käsk **Loo**. Selles õppetükis pange katseplaani nimeks **RSAT katseplaan**.

    ![Uue katseplaani dialoogiaken.](./media/setup_rsa_tool_55.png)

4. Valige plussmärk (**+**) ja seejärel valige suvand **Staatiline komplekt**, et luua uue katseplaani alla staatiline komplekt. Pange uue testkomplekti nimeks **T01 – valmistamine lattu**.

    > [!NOTE]
    > Võite ka luua päringul põhineva komplekti, kui soovite, et uued testjuhtumid automaatselt BPM-ist RSAT testkomplekti tõmmataks.

    ![Staatilise komplekti loomine.](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Testjuhtumite manustamine testkomplektide juurde

1. Olemasolevate testjuhtumite lisamiseks testkomplekti valige paremalt käsk **Lisa olemasolev**.

    ![Nupp Lisa olemasolev.](./media/setup_rsa_tool_57.png)

2. Valige lehel **Testjuhtumite lisamine komplekti** käsk **Käivita päring** ja seejärel valige testjuhtum testkomplekti lisamiseks. Selles õppetükis valige testjuhtum **Uue toote loomine**. Seejärel valige lehel alt paremast nurgast suvand **Testjuhtumite lisamine** (seda nuppu pole järgmisel joonisel).

    ![Nupp Käivita päring.](./media/setup_rsa_tool_58.png)

    Testjuhtum lisatakse testkomplekti **T01 – valmistamine lattu**.

    ![Testkomplekti lisatud testjuhtum.](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>RSAT konfigureerimine

1. Avage RSAT.

    ![RSAT ikoon.](./media/setup_rsa_tool_60.png)

2. Saate hoiatusteate tekstiga „Tööriista Regression Suite Automation Tool jaoks on vaja aSeleniumi, kas soovite selle kohe automaatselt alla laadida ja installida?” Valige **Jah**.

    ![Hoiatusteade, et Regression Suite Automation Tool nõuab Selenium`i.](./media/setup_rsa_tool_61.png)

3. Valige nupp **Sätted** (hammasratta sümbol) ja seejärel täitke ilmuvas dialoogiaknas järgmised väljad.

    - **Azure DevOpsi URL** – sisestage Azure DevOpsi projekti URL, näiteks `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Pääsutõend** – sisestage pääsutõend, millega saab tööriist luua ühenduse Azure DevOpsiga. Kasutage isiklikku pääsutõendit, mille lõite varem selles õppetükis. Lisateavet vt teemast [Juurdepääsu autentimine isiklike pääsutõenditega](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Projekti nimi** – valige oma Azure DevOpsi projekti nimi.
    - **Katseplaan** – valige Azure DevOpsi katseplaan, mis sisaldab teie testjuhtumeid. Lisateavet vt teemast [Katseplaanide ja testkomplektide loomine](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Pärast katseplaani valimist valige suvand **Ühenduse test**, et kontrollida ühendust Azure DevOpsiga.
    - **Hosti nimi** – sisestage katsekeskkonna hosti nimi, näiteks **\<myaos\>.cloudax.dynamics.com**. Ärge lisage eesliidet **https://** või **http://**.
    - **SOAP-i hosti nimi** – sisestage katsekeskkonna SOAP-i hosti nimi. Tavaliselt on SOAP-i hosti nimi sama kui hosti nimi, aga sellel on järelliide **soap**. Siin on näide: **\<myaos\>soap.cloudax.dynamics.com**. Ärge lisage eesliidet **https://** või **http://**.

        > [!NOTE]
        > Hosti nime ja SOAP-i hosti nime leidmiseks avage IIS-i haldur, tehke paremklõps suvanditel **Saidid \> AOSService** ja seejärel valige suvand **Sidumiste redigeerimine**. Väärtused veerus **Hosti nimi** annavad hosti nime ja SOAP-i hosti nime (SOAP-i hosti nimel on URL-ist järelliide **soap**).

        ![Hosti nimi ja SOAP-i hosti nimi hosti nime veerus.](./media/setup_rsa_tool_63.png)

    - **Administraatori kasutajanimi** – sisestage katsekeskkonda administraatori meiliaadress.
    - **Sõrmejälg** – sisestage autentimisserdi sõrmejälg, nagu on kirjeldatud selles õppetükis eespool.
    - **Töökaust** – määrake kausta asukoht, kuhu salvestatakse automatiseerimise testfailid, nt Exceli andmete testfailid. Näiteks sisestage või valige **C:\\Temp\\RegressionTool**.

        > [!NOTE]
        > Kui kausta nimes on tühikud, siis käivitamine nurjub, sest kausta ei leita. See on teadaolev probleem ja see peaks olema tööriista uusimas versioonis lahendatud.

    - **Vaikebrauser** – valige kas **Internet Explorer** või **Google Chrome**. Veenduge, et installitud oleks sobivad brauseri draiverid.
    - **Testkäivituse ajalõpp** – määrake testkäivituste ajalõpu periood minutites. Kui ajalõpu periood möödub, siis kõik aktiivsed aknad suletakse ja ootel olevad testjuhtumid nurjuvad.
    - **Testtegevuse ajalõpp** – see väli reguleerib Finance and Operationsi keskkonna serveri päringute ajalõpu perioodi minutites. Tavaliselt piisab vaikeväärtusest (2 minutit). Kuid aeglasemate keskkondade korral võite seda pikendada, kui tekivad ajalõppudega seotud tõrked.
    - **Ettevõtte nimi** – sisestage ettevõtte nimi, mida kasutatakse Exceli parameetri faili loomisel vaikimisi ettevõttena. Saate ettevõtet hiljem muuta, redigeerides Exceli parameetrifaili.

    ![Sätete dialoogiaken.](./media/setup_rsa_tool_62.png)

4. Sätete rakendamiseks ja salvestamiseks valige käsk **Rakenda**.

    Praeguste sätete salvestamiseks arvutisse konfiguratsioonifaili valige käsk **Salvesta nimega**. Sätete taastamiseks arvutis olevast konfiguratsioonifailist valige käsk **Ava**.

5. Valige dialoogiboksi sulgemiseks suvand **Sule**.

### <a name="load-and-run-test-cases"></a>Testjuhtumite laadimine ja käivitamine

1. Valige nupp **Laadi**, et laadida katseplaan **RSAT katseplaan** Azure DevOpsi projektist.

    ![Nupp Laadi.](./media/setup_rsa_tool_64.png)

2. Valige testkomplektist testjuhtum **Uue toote loomine** ja seejärel valige suvandid **Uus \> Testikäivitus- ja parameetrifailide loomine**.

    ![Käsk Testkäivitus- ja parameetrifailide loomine menüüs Uus.](./media/setup_rsa_tool_65.png)

    Exceli parameetrifail luuakse kohalikku kausta, mille määratlesite RSAT konfiguratsioonis (nt **C:\\Temp\\RegressionTool**).

    ![Loodud Exceli parameetrifail.](./media/setup_rsa_tool_66.png)

3. Kui soovite parameetrifailid salvestada, valige nupp **Laadi üles**. Kõikide valitud testjuhtumite automatiseerimise testfailid laaditakse hiljem kasutamiseks üles Azure DevOpsi. (Need failid hõlmavad Exceli testparameetrifaile.)

    Nii saate valida nupu **Laadi** parameetrifailide (ja automatiseerimise failide) laadimiseks testjuhtumist otse Azure DevOpsist. Parameetrifaile pole vaja uuesti luua. See lähenemine muutub oluliseks hiljem, kui soovite säilitada muudatusi parameetrifailis ega taha, et need üle kirjutataks.

4. Veendumaks, et automatiseerimise ja parameetrifailid salvestatakse Azure DevOpsi, avage Azure DevOpsi projekt, valige suvandid **Tahvlid \> Tööüksused** ja valige testjuhtum **Uue toote loomine**. Vahekaardil **Manused** peaksite nägema nelja faili.

    - **.cs** – C\# automatiseerimise fail
    - **.dll** – kompileeritud automatiseerimise fail komplektina
    - **.xlsx** – Exceli parameetrifail
    - **.xml** – salvestusfail

    ![Failid vahekaardil Manused.](./media/setup_rsa_tool_67.png)

5. Valige käivitamiseks testjuhtum ja seejärel käsk **Käivita**.

    > [!NOTE]
    > Kui kasutate brauserina Internet Explorerit, siis veenduge enne testjuhtumi käivitamist, et teie töölaua eraldusvõime oleks seatud väärtusele **100%** suvandites **Windowsi kuvasätted \> Mõõtkava ja paigutus**. Kui te seda sätet virtuaalarvutis muuta ei saa, muutke seda kliendis (sülearvutis), mille kaudu üritate virtuaalarvutile ligi pääseda. Eraldusvõime sätted rakenduvad virtuaalarvuti kuvasätetele.

    ![Töölaua eraldusvõime on seatud väärtusele 100%.](./media/setup_rsa_tool_68.png)

6. Kui brauseri draivereid pole süsteemi installitud, kuvatakse hoiatusteade „Selleks toiminguks on vaja brauseri \<browser name\> draiverit. Kas soovite selle kohe automaatselt alla laadida ja installida?” Valige **Jah**.

    ![Internet Explorer`i hoiatusteade.](./media/setup_rsa_tool_69.png)

    ![Chrome’i hoiatusteade.](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Kui kasutate brauserina Chrome’i ja saate tõrketeate, et seanssi ei loodud, kuna Chrome’i versioon pole õige, siis laadige alla uusim Chrome’i draiver lehelt <http://chromedriver.chromium.org/downloads> kausta **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.

    ![Chrome’i tõrketeade.](./media/setup_rsa_tool_71.png)

    Käivitatakse testjuhtum ja värskendatakse välja **Tulemus**.

    ![Uuendatud tulemiväli.](./media/setup_rsa_tool_72.png)

    Kui olete õppetükki järginud nii, nagu see on kirjutatud, siis testjuhtum **Uue toote loomine** nurjub, kuna toote loomise tegevuse salvestamine salvestas toote nime püsiprogrammeeritud väärtusena. Kui sama testjuhtumi uuesti käivitate, saate tõrketeate, kuna toode on juba olemas.

    ![Nurjunuks määratud väli Tulemus.](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Testi tulemuste kuvamine

1. Tehke topeltklõps nurjunud testjuhtumil.

    Kuvatakse tõrketeade.

    ![Tõrketeade.](./media/setup_rsa_tool_73.png)

2. Kogu tõrketeate nägemiseks valige nupp **Üksikasjad**.

    ![Kogu tõrketeade.](./media/setup_rsa_tool_74.png)

3. Tõrketeate üksikasjaliku versiooni vaatamiseks Azure DevOpsis valige käsk **Ava Azure DevOpsis**. Azure DevOpsis saate vaadata testjuhtumi olekut ja üksikasjalikku tõrketeadet.

    ![Üksikasjalik tõrketeade Azure DevOps`is.](./media/setup_rsa_tool_75.png)

4. Testi tulemuste vaatamiseks otse Azure DevOpsi projektis valige suvandid **Katseplaanid \> Katseplaanid \> Käivitused**. Tehke topeltklõps testkäivitusel, mille üksikasju soovite näha.

    ![Testkäivituste loend Azure DevOps`is.](./media/setup_rsa_tool_76.png)

5. Vahekaart **Käivituse kokkuvõte** näitab, et testjuhtum nurjus, aga tegelikku tõrketeadet ei esitata. Üksikasjaliku tõrketeate vaatamiseks valige vahekaart **Testi tulemused**.

    ![Vahekaart Käivituse kokkuvõte.](./media/setup_rsa_tool_77.png)

    Vahekaardil **Testi tulemused** leiate testjuhtumi teabe koos tulemuse ja tõrketeatega.

    ![Vahekaart testi tulemused.](./media/setup_rsa_tool_78.png)

6. Üksikasjaliku tõrketeate nägemiseks tehke topeltklõps vastaval kirjel.

    ![Üksikasjalik tõrketeade.](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Kõik tõrketeated on saadaval ka lokaalselt failis **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. Saate eksportida testkäivituse tulemused katseplaani tasemest, valides nupu **Ekspordi**.

    ![Katseplaani eksportimine.](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Exceli parameetrifaili muutmine

1. Avage RSAT.
2. Valige testjuhtum ja seejärel nupp **Redigeeri** Exceli parameetrifaili avamiseks.

    Lehel **EcoResProductCreate** pange tähele, et väli **Tootenumber** on püsiprogrammeeritud. Peate värskendama selle välja uuele tootenumbrile, enne kui testjuhtumi uuesti käivitate.

3. Iga käivituse jaoks kordumatu tootenumbri loomiseks Exceli parameetrifaili uuesti avamata ja tootenumbrit iga kord käsitsi värskendamata kasutage järgmist Exceli valemit.

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Lisaks vahekaardile **Üldine** sisaldab Exceli parameetrifail andmete vahekaarti iga vormi lehe kohta, mida testjuhtum külastab.

    ![Tootenumbri väli.](./media/setup_rsa_tool_81.png)

4. Valige **Salvesta** ja sulgege seejärel Exceli tööraamat.
5. Valige nupp **Laadi üles** Exceli parameetrifaili salvestamiseks Azure DevOpsi.

    ![Teade üleslaadimise õnnestumise kohta.](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Testjuhtumite käivitamiseks konkreetses kasutaja kontekstist sisestage kasutaja meiliaadressi ID välja **Testkasutaja** Exceli parameetrifaili vahekaardil **Üldine**. RSAT uusimas versioonis on Exceli parameetrifaili väljade paigutust värskendatud, aga põhimõte on sama.
    >
    > ![Väli Testkasutaja.](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Tulemuste kinnitamine

- Testjuhtumi uuesti käivitamiseks valige nupp **Käivita** ja veenduge, et testjuhtum on läbitud. Testi tulemusi saate vaadata, nagu on kirjeldatud jaotises [Testi tulemuste vaatamine](#view-the-test-results).

    ![Läbituks määratud väli Tulemus.](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Testjuhtumite aheltöötlus

Üks RSAT põhifunktsioone on testjuhtumite aheltöötlus (test suudab edastada väärtusi teistele testidele). Testjuhtumid käivitatakse Azure DevOpsi katseplaanis määratud järjekorra järgi. (Seda järjekorda saab värskendada ka testtööriistas.) Seega kui soovite edastada muutujaid ühest testjuhtumist teise, on väga oluline, et testid oleksid õiges järjekorras.

Selles jaotises loote salvestatud muutuja esimeses testjuhtumis, loote teise testjuhtumi ja edastate salvestatud muutuja esimesest testjuhtumist teise testjuhtumisse. Seejärel käivitate testjuhtumid RSAT-s testjuhtumi ahelana.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Olemasoleva tegevuse salvestise muutmine salvestatud muutuja loomiseks

1. Avage klient.
2. Valige nupp **Sätted** (hammasratta sümbol) ja seejärel valige suvand **Tegevuse salvestaja**.
3. Valige nupp **Salvestise redigeerimine**.

    ![Salvestise redigeerimise nupp.](./media/setup_rsa_tool_85.png)

4. Valige nupp **Ava teenusest Lifecycle Services**.

    ![Nupp Ava teenusest Lifecycle Services.](./media/setup_rsa_tool_86.png)

5. Valige nupp **Vali teenuse Lifecycle Services teek**.

    ![Nupp Vali teenuse Lifecycle Services teek.](./media/setup_rsa_tool_87.png)

    BPM-i teegid laaditakse LCS-ist.

    ![BPM-i teekide laadimine.](./media/setup_rsa_tool_88.png)

6. Pärast BPM-i teekide laadimist LCS-ist valige BPM-i teek **RSAT** ja äriprotsess **Uue toote loomine**, millega tegevuse salvestis on seotud. Seejärel valige **OK**.

    ![BPM-i teegi ja äpriprotsessi valimine.](./media/setup_rsa_tool_89.png)

7. Vastava tegevuse salvestise nimi sisestatakse välja **Salvestise nimi**. Valige nupp **Alusta**.

    ![Tegevuse salvestise nimi väljal Salvestise nimi.](./media/setup_rsa_tool_90.png)

8. Valige suvandid **Tooteteabe haldus \> Tooted** ja valige nupp **Uus**, et avada leht, kus salvestati algne tegevuse salvestis, **Toote loomine**.
9. Valige nupp **Sisesta etapp**.

    > [!NOTE]
    > Uus etapp sisestatakse **pärast** paanilt valitud etappi.

    ![Nupp Sisesta etapp.](./media/setup_rsa_tool_91.png)

10. Tehke paremklõps väljal **Tootenumber** ja seejärel valige suvandid **Tegevuse salvestaja \> Kopeeri**.

    ![Käsk Kopeeri.](./media/setup_rsa_tool_92.png)

11. Paanile lisatakse uus etapp. Märkige välja **Tootenumber** väärtus üles, seda läheb hiljem vaja.

    ![Lisatud uus etapp.](./media/setup_rsa_tool_93.png)

12. Valige nupp **Muutmine on lõpetatud**.
13. Valige nupp **Salvesta teenusesse Lifecycle Services** ja seostage uus tegevuse salvestis sama BPM-i teegi ja äriprotsessiga, millega oli seotud algne tegevuse salvestis. Lisateavet vt jaotisest [Tegevuse salvestise loomine ja salvestamine BPM-i teeki](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Minge BPM-i teeki ja valige suvand **Testjuhtumite sünkroonimine**, et kirjutada üle tegevuse salvestis, mis on seotud testjuhtumiga Azure DevOpsis, nagu on kirjeldatud jaotises [BPM-ist Azure DevOpsi sünkroonimise testimine](#test-the-synchronization-from-bpm-to-azure-devops).
15. Avage RSAT ja valige nupp **Laadi**, et laadida uuesti kõik testjuhtumid testkomplektis. Peate looma uuesti automatiseerimise ja parameetrifaili vastava testjuhtumi jaoks, valides testjuhtumi ja seejärel suvandid **Uus \> Testkäivitus- ja parameetrifailide loomine**, nagu on kirjeldatud jaotises [Testjuhtumite laadimine ja käivitamine](#load-and-run-test-cases).

    > [!NOTE]
    > Kui Exceli parameetrifail jäeti lahti, siis uuesti loomine nurjub. Seetõttu olge kindel, et testjuhtumi Exceli parameetrifail suletakse enne uue Exceli parameetrifaili loomist.

16. Valige nupp **Redigeeri**, et avada uus Exceli parameetrifail. Näete uut kannet **Salvestatud muutuja** real 9. See muutuja, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, salvestatakse tegevuse salvestise XML-faili ja seda saab kasutada edaspidistes testides.

    ![Salvestatud muutuja kanne.](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Uue testjuhtumi loomine

1. Minge BPM-i teeki **RSAT**.
2. Valige protsess **Tugiäriprotsessi näidis** ja seejärel valige paremalt suvand **Redigeerimisrežiim**.
3. Muutke väljade **Nimi** ja **Kirjeldus** väärtus valikule **Toote väljastamine**. Seejärel valige nupp **Salvesta**.

    ![Väärtusele Toote väljastamine muudetud nimi ja kirjeldus.](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Uue kinnitamise funktsiooniga tegevuse salvestise loomine

- Looge tegevuse salvestis, et väljastada varem loodud toode USRT juriidilisse isikusse. Lisateavet vt jaotisest [Tegevuse salvestise loomine ja salvestamine BPM-i teeki](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Testjuhtumite ahela jaoks soovite alati otsida või filtreerida vajalikku kirjet, *sisestades välja väärtuse käsitsi*. Nii saab tööriist määrata kirje, mille suhtes järgmises testjuhtumis tuleb tegevus teha.

    ![Uus kinnitamise funktsiooniga tegevuse salvestis.](./media/setup_rsa_tool_96.png)

    Nagu eelmisel joonisel näha, siis pärast toote leidmist kiirfiltriga, aga enne nupu **Väljasta tooted** valimist kinnitate välja **Tootenumber** väärtuse veendumaks, et toote ID on varem loodud toote ID. Väärtuse kinnitamiseks tehke paremklõps väljal **Tootenumber** ja seejärel valige suvandid **Tegevuse salvestaja \> Kinnita \> Praegune väärtus**.

    ![Praeguse väärtuse kinnitamine.](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Tegevuse salvestise salvestamine BPM-i

1. Kui tegevuse salvestamine on lõpule viidud, valige suvand **Salvesta teenusesse Lifecycle Services**.

    ![Lõpetatud tegevuse salvestise salvestamine teenusesse Lifecycle Services.](./media/setup_rsa_tool_98.png)

2. Teegi teave laaditakse LCS-ist.

    ![Teegi teabe laadimine LCS-ist.](./media/setup_rsa_tool_99.png)

3. Valige tegevuse salvestisega seostamiseks BPM-i teek. Selles õppetükis valige varem loodud BPM-i teek **RSAT** ja selle all äriprotsess **Toote väljastamine**. Seejärel valige **OK**.

#### <a name="sync-bpm-to-azure-devops"></a>BPM-i sünkroonimine Azure DevOpsiga

1. Minge BPM-i teeki ja avage teek **RSAT**.
2. Valige suvand **VSTS-i sünkroonimine** ja seejärel suvand **Testjuhtumite sünkroonimine**. Lisateavet vt jaotisest [BPM-ist Azure DevOpsi sünkroonimise testimine](#test-the-synchronization-from-bpm-to-azure-devops).

    Kui sünkroonimine on lõpule viidud, kuvatakse äriprotsessi **Toote väljastamine** uus tööüksus ja vastav testjuhtum Azure DevOpsis jaotises **Tahvlid \> Tööüksused**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Uue testjuhtumi lisamine olemasolevasse testkomplekti

1. Valige suvandid **Katseplaanid \> Katseplaanid** ja valige plaan **RSAT katseplaan**.
2. Valige nupp **Lisa olemasolev**.
3. Lehel **Testjuhtumite lisamine komplekti** valige käsk **Käivita päring**.
4. Valige uus testjuhtum, mis loodi suvandi **Toote väljastamine** jaoks, ja seejärel valige lehel alt paremalt nurgast nupp **Testjuhtumite lisamine** (seda nuppu pole järgmisel joonisel).

    ![Leht Testjuhtumite lisamine komplekti.](./media/setup_rsa_tool_100.png)

    Testkomplektil on nüüd kaks testjuhtumit.

    ![Kaks testjuhtumit testkomplektis.](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Testjuhtumite laadimine RSAT-sse

1. Avage RSAT ja valige nupp **Laadi**.
2. Testjuhtumid laaditakse ja kuvatakse hoiatus tekstiga „See tegevus kirjutab üle Exceli testandmefailid, kohalikud muudatused lähevad kaduma. Kas soovite jätkata?” Valige nupp **Jah** Exceli parameetrifailide värskendamiseks kohalikus süsteemis, aga mitte Azure DevOpsi üles laaditud Exceli parameetrifailide värskendamiseks.

    ![See toiming kirjutab Exceli testandmefailid üle.](./media/setup_rsa_tool_102.png)

    Mõlemad testjuhtumid on laaditud koos Exceli parameetrifailiga esimese testjuhtumi jaoks. Kuna valisite viimasel käitusel nupu **Laadi**, tõmmatakse parameetrifailid Azure DevOpsist.

    ![Laaditud testjuhtumid.](./media/setup_rsa_tool_103.png)

3. Valige ainult teine testjuhtum ja seejärel suvandid **Uus \> Testkäivitus- ja parameetrifailide loomine**.

#### <a name="edit-the-excel-parameter-file"></a>Exceli parameetrifaili redigeerimine

1. Valige ainult teine testjuhtum ja seejärel valige nupp **Redigeeri** vastava Exceli parameetrifaili avamiseks.
2. Kopeerige salvestatud muutuja **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (vt jaotist [Olemasoleva tegevuse salvestise muutmine salvestatud muutuja loomiseks](#modify-an-existing-task-recording-to-create-a-saved-variable)) esimesest testjuhtumist kõikidesse väljadesse, kus kasutatakse tootenumbrit. Kopeerige selles juhtumis muutuja väljadesse **Tootenumber** ja **Tootenumbri kinnitus** lehel **EcoResProductListPage**.

    ![Tootenumbri ja tootenumbri kinnituse väljad.](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Muutujaid saab edastada testide vahel ainult sama testkäivituse ajal. Muutujate nimed peavad täpselt kattuma.

3. Valige **Salvesta** ja sulgege seejärel Exceli tööraamat.
4. Valige suvand **Laadi üles**, et salvestada Exceli parameetrifailis tehtud muudatused.

#### <a name="run-the-chained-test-cases"></a>Testjuhtumite ahela käivitamine

1. Valige mõlemad testjuhtumid ja seejärel käsk **Käivita**.
2. Kontrollige, kas mõlemad testjuhtumid on läbitud.

    ![Väli Tulemus, mis on seatud väärtusele Läbitud mõlema testjuhtumi korral.](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]