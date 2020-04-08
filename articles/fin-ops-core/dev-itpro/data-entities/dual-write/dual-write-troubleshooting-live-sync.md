---
title: Reaalajas sünkroonimise probleemide tõrkeotsing
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada reaalajas sünkroonimisega seotud probleeme.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 60839bbd1b3ae642cdd419c7df2388292776a461
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172733"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Reaalajas sünkroonimise probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see teavet, mis aitab lahendada reaalajas sünkroonimisega seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Reaalajas sünkroonimine põhjustab 403 keelatud tõrke, kui loote kirje Finance and Operationsi rakenduses

Kui proovite luua rakenduses Finance and Operations kirjet, võidakse kuvada järgmine tõrketeade.

*\[{\\„tõrge\\”:{\\„kood\\”:\\„0x80072560\\”,\\„sõnum\\”:\\„Kasutaja pole organisatsiooni liige.\\”}}\], Kaugserver tagastas tõrke: (403) keelatud.”}}”.*

Probleemi lahendamiseks järgige juhiseid teemas [Süsteemi nõuded ja eeltingimused](requirements-and-prerequisites.md). Nende sammude lõpule viimiseks peab rakenduses Common Data Service loodud topeltkirjutuse kasutajatel olema süsteemiadministraatori roll. Vaikeomanikust meeskonnal peab samuti olema süsteemiadministraatori roll.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Mis tahes üksuse reaalajas sünkroonimine põhjustab sarnase tõrke, kui loote kirje Finance and Operationsi rakenduses

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Teile võidakse kuvada järgnev tõrketeate iga kord, kui proovite üksuse andmeid Finance and Operationsi rakenduses salvestada.

*Andmebaasi muudatusi ei saa salvestada. Tööüksus ei saa kannet kinnitada. Üksuse uoms-i ei saa andmeid kirjutada. Üksusesse UnitOfMeasureEntity kirjutamine nurjus, kuna tõrketeade ei saa sünkroonida üksuse uoms-i.*

Probleemi lahendamiseks peate veenduma, et eeltingimuseks olevad viiteandmed on olemas nii Finance and Operationsi rakenduses kui ka Common Data Service'is. Näiteks kui olete klient rakeenduses Finance and Operations, mis kuulub kindlasse kliendigruppi, veenduge, et see kliendigrupp on olemas Common Data Service'is.

Kui andmed on olemas kummalgi poolel ja olete teinud kindlaks, et probleem ei ole seotud andmetega, toimige järgmiselt.

1. Peatage seostatud üksus.
2. Logige sisse rakendusse Finance and Operations ja veenduge, et nurjuva üksuse kirjed on olemas tabelites DualWriteProjectConfiguration ja DualWriteProjectFieldConfiguration. Näiteks selline näeb välja päring, kui üksus **Kliendid** nurjub.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Kui nurjunud üksusel on kirjeid ka pärast üksuse vastendamise peatamist, kustutage nurjunud üksusega seotud kirjed. Märkige tabelis DualWriteProjectConfiguration veerg **projectname** ja tooge tabelist DualWriteProjectFieldConfiguration kirje, kasutades kirje kustutamiseks projekti nime.
4. Käivitage üksuse vastendamine. Kontrollige, kas andmed sünkroonitakse tõrgeteta.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Lugemis- või kirjutusprivileegide tõrgete käsitlemine rakenduses Finance and Operations andmete loomisel

Võite saada tõrketeate „Vigane taotlus”, mis sarnaneb järgmise näitega rakenduses Finance and Operations andmete loomisel.

![Vigase taotluse tõrketeate näide](media/error_record_id_source.png)

Probleemi lahendamiseks peate määrama vastendatud Dynamics 365 Salesi või Dynamics 365 Customer Service'i äriüksusele õige turberolli puuduva privileegi lubamiseks.

1. Otsige rakendusest Finance and Operations üles andmeintegratsiooni ühendusekogumis vastendatud äriüksus.

    ![Organisatsiooni vastendamine](media/mapped_business_unit.png)

2. Logige Dynamics 365 mudeljuhitud rakenduse keskkonda sisse, liikuge jaotisesse **Säte \> Turve** ja otsige üles vastendatud äriüksuse meeskond.

    ![Vastendatud äriüksuse meeskond](media/setting_security_page.png)

3. Avage selle meeskonna leht redigeerimiseks ja seejärel valige **Rollide haldamine** dialoogiboksi **Meeskonna rollide haldamine** avamiseks.

    ![Nupp rollide haldamine](media/manage_team_roles.png)

4. Määrake roll, millel on asjaomaste üksuste lugemise/kirjutamise privileeg ja seejärel valige **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>Sünkroonimisprobleemide parandamine keskkonnas, millel on hiljuti muudetud Common Data Service'i keskkond

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui proovite luua rakenduses Finance and Operations andmeid, võidakse kuvada järgmine tõrketeade.

*{„entityName”:„CustCustomerV3Entity”,„executionStatus”:2,„fieldResponses”:\[\],„recordResponses”:\[{„errorMessage”:„**Lasti ei saanud luua üksusele CustCustomerV3Entity**”,„logDateTime”:„2019-08-27T18:51:52.5843124Z”,„verboseError”:„Lasti loomine nurjus tõrkega kehtetu URI: URI on tühi.”}\],„isErrorCountUpdated”:true}*

Dynamics 365 mudeljuhitud rakenduses näeb tõrge välja järgnev.

*ISV-koodist ilmnes ootamatu tõrge. (ErrorType = ClientError) Ootamatu erand lisandmoodulist (Käivita): Microsoft.Dynamics.Integraator.CrmPlugins.Plugin: System.Exception: üksuse konto töötlemine nurjus – (ühenduse loomise katse nurjus, kuna ühendatud osapool ei reageerinud pärast teatud ajavahemikku või loodud ühendus nurjus, kuna ühendatud host ei vastanud*

See tõrge ilmneb, kui Common Data Service'i keskkond on valesti lähtestatud sel ajal, kui proovite luua andmeid rakenduses Finance and Operations.

Probleemi lahendamiseks tehke järgmist.

1. Logige aiaaw Finance and Operationsi virtuaalarvutisse (VM), avage SQL Server Management Studio (SSMS) ja otsige kirjeid tabelist DUALWRITEPROJECTCONFIGURATIONENTITY, kus **internalentityname** võrdub üksusega **Klientide V3** ja **externalentityname** võrdub üksusega **kontod**. Päring näeb välja järgnev.

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

3. Veenduge, et veerul **externalenvironmentURL** oleks õige Common Data Service'i või rakenduse URL. Kustutage kõik duplikaatkirjed, mis osutavad valele Common Data Service'i URL-ile. Kustutage vastavad kirjed tabelitest DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION.
4. Peatage üksuse vastendamine ja taaskäivitage see
