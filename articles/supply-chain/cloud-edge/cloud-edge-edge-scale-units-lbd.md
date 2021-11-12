---
title: Perimeeterskaalaüksuste juurutamine kohandatud riistvara jaoks LBD abil (eelvaade)
description: See teema selgitab, kuidas kasutada ettevõtte andmetel (LBD) põhinevat kohandatud riistvara ja juurutamist, kasutades valdustelimuse skaala üksuseid.
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678977"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Perimeeterskaalaüksuste juurutamine kohandatud riistvara jaoks LBD abil (eelvaade)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Servaskaala ühikud on hankeahela halduse jaotatud topoloogias olulise rolliga. Selles topoloogias saate jaotada töökoormusi Supply Chain Management pilve keskuse ja täiendavate kaaluühikute vahel pilves või servas.

Servaskaala ühikuid saab juurutada, luues kohalikke äriandmeid (LBD) [ettevõttekeskkonnas](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) ja konfigureerides need siis nii, et see töötaks supply chain management jaotatud topoloogias kaaluühikuna. Selle saavutamiseks seostatakse ettevõttesisene LBD keskkond Supply Chain Management pilve keskkonnaga, mis on konfigureeritud funktsioneerima keskusena.  

Servaskaala üksused on praegu eelvaates. Seetõttu saate seda tüüpi keskkonda kasutada ainult vastavalt [eelvaate tingimustele](https://aka.ms/scmcnepreviewterms).

See teema kirjeldab, kuidas seadistada ettevõttesisene LBD-keskkond servaskaala üksusena ja seejärel seostada see keskusega.

## <a name="deployment-overview"></a>Juurutamise ülevaade

Siin on juurutamise protsessi ülevaade.

1. **Lubage LBD-pesa oma LBD-projektis Microsoft Dynamics Lifecycle Services (LCS).**

    Eelvaate ajal sihivad LBD-servaskaala üksused olemasolevaid LBD-kliente. Täiendav 60-päevase piiratud LBD boksi pesa antakse ainult konkreetsetes kliendiolukordades.

1. **Seadistage ja juurutage LBD keskkond *tühja* andmebaasiga.**

    Kasutage LCS-i, et juurutada LBD-keskkond uusima topoloogia ja tühja andmebaasiga. Lisateavet vt [Häälestusest tühja andmebaasiga LBD keskkonna juurutamiseks](#set-up-deploy) selles teemas hiljem. Peate kasutama Supply Chain Management versiooni 10.0.19 platvormi värskendusega 43 või uuemaga üle kogu keskuse ja kaalu ühiku keskkondades.

1. **Laadige sihtpaketid LBD-projekti varadesse LCS-s.**

    Valmistage ette rakenduse, platvormi ja kohandamise paketid, mida kasutate kogu keskuses ja servaskaala üksuses. Lisateavet vt [Sihtpakettide üleslaadimine LBD-projekti varadesse LCS-i](#upload-packages) selle teema jaotisest.

1. **LBD-keskkonna hooldus sihtpakettide abil.**

    See samm tagab, et keskusele ja sihtkohale juurutatakse samad järgud ja kohandused. Lisateavet vt jaotisest [Teenuse LBD-keskkond koos sihtpakettide](#service-target-packages) sektsiooniga selles teemas.

1. **Viige lõpule kaaluühiku konfigureerimine ja töökoormuse määramine.**

    Lisateavet vt teemast [Oma LBD servaskaala üksuse määramine keskusesse](#assign-edge-to-hub) jaotisesse hiljem siin teemas.

Selle teema ülejäänud osades on lisateave iga protsessi etapi kohta, kuidas neid samme lõpetada.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Seadistage ja juurutage LBD keskkond tühja andmebaasiga

See samm loob funktsionaalse LBD keskkonna. Keskkonnal ei pea siiski olema samu rakenduse ja platvormi versioone kui keskuse keskkonnas. Lisaks puudub see ikkagi kohandustest ja sellel ei ole veel lubatud töötada kaaluühikuna.

1. Järgige juhiseid [apealsete keskkondade häälestamine ja juurutamine (platvormivärskendus 41 ja uuemad)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Peate kasutama Supply Chain Management versiooni 10.0.19 platvormi värskendusega 43 või uuemaga üle kogu keskuse ja kaalu ühiku keskkondades

    > [!IMPORTANT]
    > **Enne** selle teema lõpule viimist lugege ülejäänud osa.

1. Enne konfiguratsiooni kirjeldamist infrastruktuuri\\ConfigTemplate.xml failis käivitage järgmine skript:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > See skript eemaldab mis tahes konfiguratsiooni, mis ei ole vajalik servaskaala ühikute juurutamiseks.

1. Seadistage andmebaas, mis sisaldab tühje andmeid, nagu kirjeldatud [konfigureerimise andmebaasides](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Kasutage selle sammu jaoks tühja faili data.bak.
1. Seadistage eeljuurutuse skript. Vaata lisainformatsiooni [Kohaliku esindaja eeljuurutuse ja järeljuurutuse skriptid](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopeerige sisu **ScaleUnit** kaustast **infrastruktuuri skriptid** kaustast **skriptid** kausta agendi faili talletusossa, mis häälestati keskkonnas. Tavaline tee on \\\\lbdiscsi01\\agendi\\skriptid.
    2. Looge **PreDeployment.ps1** mis käivitab skriptid nõutud parameetreid kasutades. Eeljuurutuse skript tuleb panna **Skriptid** talletusosa skriptide kausta. Vastasel juhul ei saa seda käivitada. Tavaline tee on \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Skripti PreDeployment.ps1 sisu sarnaneb järgmise näitega.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
        ```

        > [!NOTE]
        > Parameeter InstanceId peaks koosnema ainult kahest märgist. Esimene märk on @ ja teine võib olla mis tahes suurtäht inglise tähestikust.
        >
        > - Kehtivad väärtused:
        >   - @D
        >   - @X
        > - Mittekehtivad väärtused:
        >   - @a
        >   - @4
        >   - @#

1. Juurutage keskkond viimase saadaoleva alus topoloogia abil.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Laadige sihtpaketid LBD-projekti varadesse LCS-i

See samm valmistab ette rakenduse versiooni, platvormi versiooni ja kohandused, mis läheb üle LBD-kaalu ühiku keskkonda.

1. Laadige üles sama kombineeritud rakenduse/platvormi pakett, mida rakendati keskuse keskkonnas, LCS-i valdusse projekti varateeki.
1. Hankige jaoturi keskkonnas kombineeritud rakenduse/platvormi pakett, mida rakendati keskuse keskkonnas, LCS-i valdusse projekti varateeki.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Teenindage LBD keskkonda sihtpakettidega

See etapp joondab rakenduse versiooni, platvormi versiooni ja kohandused, mis läheb üle LBD-kaalu ühiku keskkonda.

1. Teenus LBD keskkonnas koos eelmises sammus üleslaaditud kombineeritud rakendus-/platvormipaketiga.
1. Teenus LBD keskkonnas koos eelmises sammus üleslaaditud kombineeritud rakendus-/platvormipaketiga.

    ![Valides hoolduse > Rakenda LCS-s värskendused.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Valides hoolduse > Rakenda LCS-s värskendused")

    ![Kohandatud paketi valimine.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Kohandatud paketi valimine")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Määrake oma LBD servaskaala üksus keskusesse

Kui servaskaala ühikud on veel eelvaates, peate kasutama [saadaolevaid kaaluühiku juurutuse ja konfiguratsiooni tööriistu](https://github.com/microsoft/SCMScaleUnitDevTools) et määrata GitHub-is oma LBD servaskaala üksus keskusele. Protsess võimaldab LBD konfiguratsioonil toimida servaskaala üksusena ja seostab selle keskusega. Protsess sarnaneb ühe boksi arenduskeskkonna konfigureerimisega.

1. Laadige alla viimane väljalase [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) ja laadige faili sisu lahti.
1. Saate luua faili koopia `UserConfig.sample.xml` ja sellele nime anda `UserConfig.xml`.
1. Looge Microsoft Azure Active Directory (Azure AD) rakendus teie Azure AD rentnikus nagu mainitud [Kaaluühiku ja töökoormuse Juurutusjuhendis](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Kui see on loodud, navigeerige Azure AD avalduste vormi (SysAADClientTable) oma keskusesse.
    1. Looge uus kirje ja seadistage **Kliendi ID** loodud rakenduse ID-le. Määrake **nimeks** *ScaleUnits* ja **kasutaja ID** *Adminiks*.

1. Looge Active Directory Federation Service (AD FS) rakendus, nagu on nimetatud [Kaaluühiku ja töökoormuste juurutusjuhendis](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Kui see on loodud, navigeerige Azure AD avalduste vormi (SysAADClientTable) oma kaaluühiku keskusesse.
    1. Looge uus kirje ja seadistage **Kliendi ID** loodud rakenduse ID-le. Määrake **Kasutaja ID** väärtuseks *Admin*.

1. Muuda `UserConfig.xml` faili.
    1. Sisestage `InterAOSAADConfiguration` jaotisesse teave eelnevalt loodud Azure AD rakendusest.
        - Sisestage `AppId` elemendis Azure'i rakenduse ID.
        - Sisestage `AppSecret` elemendis Azure'i rakenduse saladus.
        - `Authority` element peab sisaldama URL-i, mis määrab teie rentniku turvaasutuse.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Jaotises `ScaleUnitConfiguration` muutke esimese `ScaleUnitInstance` jaoks `AuthConfiguration` jaotist.
        - Sisestage `AppId` elemendis Azure'i rakenduse ID.
        - Sisestage `AppSecret` elemendis Azure'i rakenduse saladus.
        - `Authority` element peab sisaldama URL-i, mis määrab teie rentniku turvaasutuse.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Lisaks määrake selle sama `ScaleUnitInstance` jaoks järgmised väärtused:
        - `Domain` elemendis määrake oma keskuse URL. Näiteks: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Kontrollige `EnvironmentType` elemendis, et see oleks väärtusele `LCSHosted` seatud.

    1. Jaotises `ScaleUnitConfiguration` muutke teise `ScaleUnitInstance` jaoks `AuthConfiguration` jaotist.
        - Sisestage `AppId` elemendis AD FS-i rakenduse ID.
        - Sisestage `AppSecret` elemendis ADFS rakenduse saladus.
        - Element `Authority` peab sisaldama teie AD FS-i eksemplari URL-i.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Lisaks määrake selle sama `ScaleUnitInstance` jaoks järgmised väärtused:
        - `Domain` elemendis määrake oma kaaluühiku keskuse URL. Näiteks: https://ax.contoso.com/
        - Kontrollige `EnvironmentType` elemendis, et see oleks seatud väärtusele LBD.
        - Sisestage `ScaleUnitId` elemendis sama väärtus, mille määrate `InstanceId` eeljuurutusskripti `Configure-CloudandEdge.ps1` konfigureerimisel.

        > [!NOTE]
        > Kui te ei kasuta vaike-ID-d (@A), veenduge, et värskendate ScaleUnitId iga ConfiguredWorkload jaoks töökoormuste jaotises.

1. Avage PowerShell ja navigeerige `UserConfig.xml` fail sisaldavasse kausta.

1. Käivitage tööriista selle käsuga.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Pärast iga tegevust peate tööriista uuesti käivitama.

1. Valige tööriistas **2. Valmistage keskkondi ette töökoormuse installiks**. Seejärel käitage järgmised etapid:
    1. Valige **1. Valmistage keskus ette**.
    1. Valige **2. Valmistage ette kaaluühik**.

    > [!NOTE]
    > Kui te ei käivita seda käsku puhtast installist ja see nurjub, tehke järgmist:
    >
    > - Eemaldaga kaustast kõik `aos-storage` kaustad (v.a `GACAssemblies`).
    > - Käivitage järgmine SQL-i käsk oma äriandmebaasis (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Käivitage järgmised SQL-i käsud oma äriandmebaasis (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Kontrollige, kas muudatuste jälitamine on teie äriandmebaasis (AXDB) lubatud
    1. Käivitage SQL Server Management Studio (SSMS).
    1. Paremklõpsake oma äriandmebaasil (AXDB) ja valige atribuudid.
    1. Avanevas aknas valige **Muudatuste jälitamine** ja muutke järgmisi sätteid:

        - **Muudatuste jälitamine:** *tõene*
        - **Kinnipidamise periood:** *7*
        - **Kinnipidamise ühikud:** *päevi*
        - **Automaatne puhastamine:** *tõene*

1. Valige tööriistas **3. Töökoormuste installimine**. Seejärel käitage järgmised etapid:
    1. Valige **1. Installi keskusesse**.
    1. Valige **2. Installige keskusesse**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
