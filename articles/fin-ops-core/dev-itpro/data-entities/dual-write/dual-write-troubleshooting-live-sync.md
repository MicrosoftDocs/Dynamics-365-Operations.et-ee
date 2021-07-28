---
title: Reaalajas sünkroonimise probleemide tõrkeotsing
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada reaalajas sünkroonimisega seotud probleeme.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2694f48b295ba727870f068e7062f7cdcababdbe
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6350784"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Reaalajas sünkroonimise probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see teavet, mis aitab lahendada reaalajas sünkroonimisega seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Reaalajas sünkroonimine põhjustab 403 keelatud tõrke, kui loote rea Finance and Operationsi rakenduses

Kui proovite luua rakenduses Finance and Operations rida, võidakse kuvada järgmine tõrketeade.

*\[{\\„tõrge\\”:{\\„kood\\”:\\„0x80072560\\”,\\„sõnum\\”:\\„Kasutaja pole organisatsiooni liige.\\”}}\], Kaugserver tagastas tõrke: (403) keelatud.”}}”.*

Probleemi lahendamiseks järgige juhiseid teemas [Süsteemi nõuded ja eeltingimused](requirements-and-prerequisites.md). Nende sammude lõpule viimiseks peab rakenduses Dataverse loodud topeltkirjutuse kasutajatel olema süsteemiadministraatori roll. Vaikeomanikust meeskonnal peab samuti olema süsteemiadministraatori roll.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Mis tahes tabeli reaalajas sünkroonimine põhjustab sarnase tõrke, kui loote rea rakenduses Finance and Operations

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Teile võidakse kuvada järgnev tõrketeade iga kord, kui proovite tabeli andmeid rakenduses Finance and Operations salvestada.

*Andmebaasi muudatusi ei saa salvestada. Tööüksus ei saa kannet kinnitada. Üksuse uoms-i ei saa andmeid kirjutada. Üksusesse UnitOfMeasureEntity kirjutamine nurjus, kuna tõrketeade ei saa sünkroonida üksuse uoms-i.*

Probleemi lahendamiseks peate veenduma, et eeltingimuseks olevad viiteandmed on olemas nii Finance and Operationsi rakenduses kui ka Dataverse'is. Näiteks kui olete klient rakeenduses Finance and Operations, mis kuulub kindlasse kliendigruppi, veenduge, et see kliendigrupp on olemas Dataverse'is.

Kui andmed on olemas kummalgi poolel ja olete teinud kindlaks, et probleem ei ole seotud andmetega, toimige järgmiselt.

1. Peatage seotud tabel.
2. Logige sisse rakendusse Finance and Operations ja veenduge, et nurjuva tabeli read oleks olemas tabelites DualWriteProjectConfiguration ja DualWriteProjectFieldConfiguration. Näiteks selline näeb välja päring, kui tabel **Kliendid** nurjub.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Kui nurjunud tabelil on ridu ka pärast tabeli vastendamise peatamist, kustutage nurjunud tabeliga seotud read. Märkige tabelis DualWriteProjectConfiguration veerg **projectname** ja tooge tabelist DualWriteProjectFieldConfiguration rida, kasutades rea kustutamiseks projekti nime.
4. Käivitage tabeli vastendamine. Kontrollige, kas andmed sünkroonitakse tõrgeteta.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Lugemis- või kirjutusprivileegide tõrgete käsitlemine rakenduses Finance and Operations andmete loomisel

Võite saada tõrketeate „Vigane taotlus”, mis sarnaneb järgmise näitega rakenduses Finance and Operations andmete loomisel.

![Vigase taotluse tõrketeate näide.](media/error_record_id_source.png)

Probleemi lahendamiseks peate määrama vastendatud Dynamics 365 Salesi või Dynamics 365 Customer Service'i äriüksusele õige turberolli puuduva privileegi lubamiseks.

1. Otsige rakendusest Finance and Operations üles andmeintegratsiooni ühendusekogumis vastendatud äriüksus.

    ![Organisatsiooni vastendamine.](media/mapped_business_unit.png)

2. Logige Dynamics 365 mudeljuhitud rakenduse keskkonda sisse, liikuge jaotisesse **Säte \> Turve** ja otsige üles vastendatud äriüksuse meeskond.

    ![Vastendatud äriüksuse meeskond.](media/setting_security_page.png)

3. Avage selle meeskonna leht redigeerimiseks ja seejärel valige **Rollide haldamine** dialoogiboksi **Meeskonna rollide haldamine** avamiseks.

    ![Rollide haldamise nupp.](media/manage_team_roles.png)

4. Määrake roll, millel on asjaomaste tabelite lugemise/kirjutamise privileeg ja seejärel valige **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Sünkroonimisprobleemide parandamine keskkonnas, millel on hiljuti muudetud Dataverse'i keskkond

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui proovite luua rakenduses Finance and Operations andmeid, võidakse kuvada järgmine tõrketeade.

*{„entityName”:„CustCustomerV3Entity”,„executionStatus”:2,„fieldResponses”:\[\],„recordResponses”:\[{„errorMessage”:„**Lasti ei saanud luua üksusele CustCustomerV3Entity**”,„logDateTime”:„2019-08-27T18:51:52.5843124Z”,„verboseError”:„Lasti loomine nurjus tõrkega kehtetu URI: URI on tühi.”}\],„isErrorCountUpdated”:true}*

Dynamics 365 mudeljuhitud rakenduses näeb tõrge välja järgnev.

*ISV-koodist ilmnes ootamatu tõrge. (ErrorType = ClientError) Ootamatu erand lisandmoodulist (Käivita): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: üksuse konto töötlemine nurjus – (ühenduse loomise katse nurjus, kuna ühendatud osapool ei reageerinud pärast teatavat ajavahemikku või loodud ühendus nurjus, kuna ühendatud host ei vastanud*

See tõrge ilmneb, kui Dataverse'i keskkond on valesti lähtestatud sel ajal, kui proovite luua andmeid rakenduses Finance and Operations.

Probleemi lahendamiseks tehke järgmist.

1. Logige sisse Finance and Operationsi virtuaalarvutisse (VM), avage SQL Server Management Studio (SSMS) ja otsige ridu tabelist DUALWRITEPROJECTCONFIGURATIONENTITY, kus **internalentityname** võrdub üksusega **Klientide V3** ja **externalentityname** võrdub üksusega **kontod**. Päring näeb välja järgnev.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Kasutage järgmise päringu käivitamiseks eelmise päringu tulemuste projekti nime.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Veenduge, et veerul **externalenvironmentURL** oleks õige Dataverse'i või rakenduse URL. Kustutage kõik duplikaatread, mis osutavad valele Dataverse'i URL-ile. Kustutage vastavad read tabelitest DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION.
4. Peatage tabeli vastendamine ja taaskäivitage see


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]