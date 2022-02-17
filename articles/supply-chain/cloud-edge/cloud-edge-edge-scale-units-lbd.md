---
title: Perimeeterskaalaüksuste juurutamine kohandatud riistvara jaoks LBD abil
description: See teema selgitab, kuidas kasutada ettevõtte andmetel (LBD) põhinevat kohandatud riistvara ja juurutamist, kasutades valdustelimuse skaala üksuseid.
author: cabeln
ms.date: 01/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1204b65e76c107c29a94a61c321064a87c7571fb
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024538"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Perimeeterskaalaüksuste juurutamine kohandatud riistvara jaoks LBD abil

[!include [banner](../includes/banner.md)]

Servaskaala ühikud on hankeahela halduse jaotatud topoloogias olulise rolliga. Selles topoloogias saate jaotada töökoormusi Supply Chain Management pilve keskuse ja täiendavate kaaluühikute vahel pilves või servas.

Servaskaala ühikuid saab juurutada, luues kohalikke äriandmeid (LBD) [ettevõttekeskkonnas](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) ja konfigureerides need siis nii, et see töötaks supply chain management jaotatud topoloogias kaaluühikuna. Selle saavutamiseks seostatakse ettevõttesisene LBD keskkond Supply Chain Management pilve keskkonnaga, mis on konfigureeritud funktsioneerima keskusena.  

See teema kirjeldab, kuidas seadistada ettevõttesisene LBD-keskkond servaskaala üksusena ja seejärel seostada see keskusega.

## <a name="infrastructure-considerations"></a>Infrastruktuuri kaalutlused

Edge-skaala üksused töötavad kohapealsetes keskkondades, nii et infrastruktuuri nõuded on üsna sarnased. Siiski tuleb märkida teatud erinevusi:

- Edge-skaala üksused ei kasuta finantsaruandlust, seega ei vaja nad finantsaruandluse sõlme.
- Tootmis- ja ladustamiskoormused ei ole arvutusmahukad, seega kaaluge vastavalt oma arvutusvõimsuse arvutamist AOS-sõlmede jaoks.

## <a name="deployment-overview"></a>Juurutamise ülevaade

Siin on juurutamise protsessi ülevaade.

1. **Lubage LBD-pesa oma LBD-projektis Microsoft Dynamics Lifecycle Services (LCS).**

1. **Seadistage ja juurutage LBD keskkond *tühja* andmebaasiga.**

    Kasutage LCS-i, et juurutada LBD-keskkond uusima topoloogia ja tühja andmebaasiga. Lisateavet vt [Häälestusest tühja andmebaasiga LBD keskkonna juurutamiseks](#set-up-deploy) selles teemas hiljem. Peate kasutama tarneahela halduse versiooni 10.0.21 või uuemat jaoturi- ja skaalaüksuse keskkondades.

1. **Laadige sihtpaketid LBD-projekti varadesse LCS-s.**

    Valmistage ette rakenduse, platvormi ja kohandamise paketid, mida kasutate kogu keskuses ja servaskaala üksuses. Lisateavet vt [Sihtpakettide üleslaadimine LBD-projekti varadesse LCS-i](#upload-packages) selle teema jaotisest.

1. **LBD-keskkonna hooldus sihtpakettide abil.**

    See samm tagab, et keskusele ja sihtkohale juurutatakse samad järgud ja kohandused. Lisateavet vt jaotisest [Teenuse LBD-keskkond koos sihtpakettide](#service-target-packages) sektsiooniga selles teemas.

1. **Viige lõpule kaaluühiku konfigureerimine ja töökoormuse määramine.**

    Lisateavet vt teemast [Oma LBD servaskaala üksuse määramine keskusesse](#assign-edge-to-hub) jaotisesse hiljem siin teemas.

Selle teema ülejäänud osades on lisateave iga protsessi etapi kohta, kuidas neid samme lõpetada.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Seadistage ja juurutage LBD keskkond tühja andmebaasiga

See samm loob funktsionaalse LBD keskkonna. Keskkonnal ei pea siiski olema samu rakenduse ja platvormi versioone kui keskuse keskkonnas. Lisaks puudub see ikkagi kohandustest ja sellel ei ole veel lubatud töötada kaaluühikuna.

1. Järgige juhiseid [apealsete keskkondade häälestamine ja juurutamine (platvormivärskendus 41 ja uuemad)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Peate kasutama tarneahela halduse versiooni 10.0.21 või uuemat jaoturi- ja skaalaüksuse keskkondades. Lisaks peate kasutama infrastruktuuri skriptide versiooni 2.12.0 või uuemat versiooni. 

    > [!IMPORTANT]
    > **Enne** selle teema lõpule viimist lugege ülejäänud osa.

1. Enne konfiguratsiooni kirjeldamist infrastruktuuri\\ConfigTemplate.xml failis käivitage järgmine skript:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > See skript eemaldab mis tahes konfiguratsiooni, mis ei ole vajalik servaskaala ühikute juurutamiseks.

1. Seadistage andmebaas, mis sisaldab tühje andmeid, nagu kirjeldatud [konfigureerimise andmebaasides](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Kasutage selle sammu jaoks tühja faili data.bak.
1. Kui olete [lõpetanud sammu Andmebaaside](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) konfigureerimine, käivitage andmebaasi Scale Unit Alm Orchestrator konfigureerimiseks järgmine skript.

    > [!NOTE]
    > Ärge konfigureerige finantsaruandluse andmebaasi andmebaasi konfigureerimise [etapis Konfigureerige andmebaase](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Scriptize-Database.ps1 teeb järgmisi toiminguid.

    1. Looge tühi andmebaas, mille nimi **on ScaleUnitAlmDb**.
    2. Kasutajate vastendus andmebaasirollidega järgmise tabeli põhjal.

        | Kasutaja            | Tüüp | Andmebaasi roll |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | dbowner\_     |

1. Jätkake kohapealsete [keskkondade häälestamise ja juurutamise juhiseid (platvormi värskendus 41 ja uuem)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Kui olete AD FS-i [konfigureerimise juhised lõpule viinud](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb), tehke järgmist.

    1. Looge uus Active Directory Federation Services (AD FS) rakendus, mis võimaldab Alm Orchestration teenusel suhelda teie rakendusobjekti serveriga (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Looge uus Azure Active Directory (Azure AD) rakendus, mis võimaldab Alm Orchestration teenusel suhelda scale unit management teenusega.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Jätkake kohapealsete [keskkondade häälestamise ja juurutamise juhiseid (platvormi värskendus 41 ja uuem)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Kui peate sisestama kohaliku agendi konfiguratsiooni, veenduge, et lubate Edge Scale Uniti funktsioonid ja esitate kõik vajalikud parameetrid.

    ![Servaskaala ühiku funktsioonide lubamine.](media/EnableEdgeScaleUnitFeatures.png "Servaskaala ühiku funktsioonide lubamine.")

1. Enne keskkonna juurutamist LCS-is seadistage juurutuseelne skript. Vaata lisainformatsiooni [Kohaliku esindaja eeljuurutuse ja järeljuurutuse skriptid](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopeerige skript Configure-CloudAndEdge.ps1 infrastructure **scripts** **kaustast** ScaleUnit **keskkonnas seadistatud agendifailide salvestusruumi kausta Skriptid.** Tavaline tee on \\\\lbdiscsi01\\agendi\\skriptid.
    2. Looge **PreDeployment.ps1** mis käivitab skriptid nõutud parameetreid kasutades. Eeljuurutuse skript tuleb panna **Skriptid** talletusosa skriptide kausta. Vastasel juhul ei saa seda käivitada. Tavaline tee on \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Skripti PreDeployment.ps1 sisu sarnaneb järgmise näitega.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
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
1. Pärast keskkonna juurutamist tehke järgmist.

    1. Käivitage oma ettevõtte andmebaasis (AXDB) järgmised SQL-käsud.

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Suurendage samaaegset maksimaalset partiiseanssi väärtuseni, mis on suurem kui 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Veenduge, et muudatuste jälgimine on teie ettevõtte andmebaasis (AXDB) lubatud.

        1. Avage SQL Serveri haldusstuudio (SSMS).
        1. Valige ja hoidke (või paremklõpsake) oma ettevõtte andmebaasi (AXDB) ja seejärel valige **Atribuudid**.
        1. Valige kuvatavas aknas suvand **Muuda jälgimist** ja seejärel seadke järgmised väärtused.

            - **Muudatuste jälitamine:** *tõene*
            - **Kinnipidamise periood:** *7*
            - **Kinnipidamise ühikud:** *päevi*
            - **Automaatne puhastamine:** *tõene*

    1. Lisage varem loodud AD FS-rakenduse ID (kasutades skripti Create-ADFSServerApplicationForEdgeScaleUnits.ps1) oma skaalaüksuse rakenduste tabelisse Azure AD. Selle toimingu saate käsitsi kasutajaliidese (UI) kaudu lõpule viia. Teise võimalusena saate selle andmebaasi kaudu lõpule viia järgmise skripti abil.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a> Azure'i võtmehoidla ja rakenduse häälestamine Azure AD skaalaüksuste vahelise suhtluse lubamiseks

1. Pärast keskkonna juurutamist looge lisarakendus Azure AD, mis võimaldab usaldusväärset suhtlust jaoturi ja skaalaüksuse vahel.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Pärast rakenduse loomist peate looma kliendisaladuse ja salvestama teabe Azure'i võtmehoidlasse. Lisaks peate andma juurdepääsu loodud rakendusele Azure AD, et see saaks võtmehoidlasse salvestatud saladused tuua. Teie mugavuse huvides teeb järgmine skript automaatselt kõik vajalikud toimingud.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Kui pole ühtegi võtmevõlvi, millel on määratud **KeyVaultName** väärtus, loob skript selle automaatselt.

1. Azure AD Lisage äsja loodud rakenduse ID (skripti Create-SpokeToHubAADApplication.ps1 kasutamisel) oma jaoturi rakenduste tabelisse Azure AD. Selle toimingu saate kasutajaliidese kaudu käsitsi lõpule viia.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Laadige sihtpaketid LBD-projekti varadesse LCS-i

See samm valmistab ette rakenduse versiooni, platvormi versiooni ja kohandused, mis läheb üle LBD-kaalu ühiku keskkonda.

1. Laadige üles sama kombineeritud rakenduse/platvormi pakett, mida rakendati keskuse keskkonnas, LCS-i valdusse projekti varateeki.
1. Hankige jaoturi keskkonnas kombineeritud rakenduse/platvormi pakett, mida rakendati keskuse keskkonnas, LCS-i valdusse projekti varateeki.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Teenindage LBD keskkonda sihtpakettidega

See etapp joondab rakenduse versiooni, platvormi versiooni ja kohandused, mis läheb üle LBD-kaalu ühiku keskkonda.

1. Teenus LBD keskkonnas koos eelmises sammus üleslaaditud kombineeritud rakendus-/platvormipaketiga.
1. Teenus LBD keskkonnas koos eelmises sammus üleslaaditud kombineeritud rakendus-/platvormipaketiga.

    ![Värskenduste rakendamine LCS-is.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Värskenduste rakendamine LCS-is")

    ![Kohandatud paketi valimine.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Kohandatud paketi valimine")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Määrake oma LBD servaskaala üksus keskusesse

Servaskaala üksuse konfigureerite ja haldate skaala ühikuhaldusportaali kaudu. Lisateavet leiate teemast [Skaalaühikute ja töökoormuse haldamine portaali](./cloud-edge-landing-page.md#scale-unit-manager-portal) Scale Unit Manager abil.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
