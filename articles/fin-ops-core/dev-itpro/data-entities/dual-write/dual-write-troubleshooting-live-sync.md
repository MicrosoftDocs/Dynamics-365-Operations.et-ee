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
ms.openlocfilehash: 1c0dfebb3ef442f67d8489d7aed00305c02cf410
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748893"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="3bda2-103">Reaalajas sünkroonimise probleemide tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="3bda2-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="3bda2-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="3bda2-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="3bda2-105">Eelkõige annab see teavet, mis aitab lahendada reaalajas sünkroonimisega seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="3bda2-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3bda2-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="3bda2-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3bda2-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="3bda2-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="3bda2-108">Reaalajas sünkroonimine põhjustab 403 keelatud tõrke, kui loote rea Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="3bda2-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="3bda2-109">Kui proovite luua rakenduses Finance and Operations rida, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="3bda2-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="3bda2-110">*\[{\\„tõrge\\”:{\\„kood\\”:\\„0x80072560\\”,\\„sõnum\\”:\\„Kasutaja pole organisatsiooni liige.\\”}}\], Kaugserver tagastas tõrke: (403) keelatud.”}}”.*</span><span class="sxs-lookup"><span data-stu-id="3bda2-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="3bda2-111">Probleemi lahendamiseks järgige juhiseid teemas [Süsteemi nõuded ja eeltingimused](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="3bda2-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="3bda2-112">Nende sammude lõpule viimiseks peab rakenduses Dataverse loodud topeltkirjutuse kasutajatel olema süsteemiadministraatori roll.</span><span class="sxs-lookup"><span data-stu-id="3bda2-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="3bda2-113">Vaikeomanikust meeskonnal peab samuti olema süsteemiadministraatori roll.</span><span class="sxs-lookup"><span data-stu-id="3bda2-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="3bda2-114">Mis tahes tabeli reaalajas sünkroonimine põhjustab sarnase tõrke, kui loote rea rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3bda2-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="3bda2-115">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="3bda2-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="3bda2-116">Teile võidakse kuvada järgnev tõrketeade iga kord, kui proovite tabeli andmeid rakenduses Finance and Operations salvestada.</span><span class="sxs-lookup"><span data-stu-id="3bda2-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="3bda2-117">*Andmebaasi muudatusi ei saa salvestada. Tööüksus ei saa kannet kinnitada. Üksuse uoms-i ei saa andmeid kirjutada. Üksusesse UnitOfMeasureEntity kirjutamine nurjus, kuna tõrketeade ei saa sünkroonida üksuse uoms-i.*</span><span class="sxs-lookup"><span data-stu-id="3bda2-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="3bda2-118">Probleemi lahendamiseks peate veenduma, et eeltingimuseks olevad viiteandmed on olemas nii Finance and Operationsi rakenduses kui ka Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="3bda2-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="3bda2-119">Näiteks kui olete klient rakeenduses Finance and Operations, mis kuulub kindlasse kliendigruppi, veenduge, et see kliendigrupp on olemas Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="3bda2-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="3bda2-120">Kui andmed on olemas kummalgi poolel ja olete teinud kindlaks, et probleem ei ole seotud andmetega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3bda2-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="3bda2-121">Peatage seotud tabel.</span><span class="sxs-lookup"><span data-stu-id="3bda2-121">Stop the related table.</span></span>
2. <span data-ttu-id="3bda2-122">Logige sisse rakendusse Finance and Operations ja veenduge, et nurjuva tabeli read oleks olemas tabelites DualWriteProjectConfiguration ja DualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3bda2-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="3bda2-123">Näiteks selline näeb välja päring, kui tabel **Kliendid** nurjub.</span><span class="sxs-lookup"><span data-stu-id="3bda2-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="3bda2-124">Kui nurjunud tabelil on ridu ka pärast tabeli vastendamise peatamist, kustutage nurjunud tabeliga seotud read.</span><span class="sxs-lookup"><span data-stu-id="3bda2-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="3bda2-125">Märkige tabelis DualWriteProjectConfiguration veerg **projectname** ja tooge tabelist DualWriteProjectFieldConfiguration rida, kasutades rea kustutamiseks projekti nime.</span><span class="sxs-lookup"><span data-stu-id="3bda2-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="3bda2-126">Käivitage tabeli vastendamine.</span><span class="sxs-lookup"><span data-stu-id="3bda2-126">Start the table mapping.</span></span> <span data-ttu-id="3bda2-127">Kontrollige, kas andmed sünkroonitakse tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="3bda2-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="3bda2-128">Lugemis- või kirjutusprivileegide tõrgete käsitlemine rakenduses Finance and Operations andmete loomisel</span><span class="sxs-lookup"><span data-stu-id="3bda2-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="3bda2-129">Võite saada tõrketeate „Vigane taotlus”, mis sarnaneb järgmise näitega rakenduses Finance and Operations andmete loomisel.</span><span class="sxs-lookup"><span data-stu-id="3bda2-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Vigase taotluse tõrketeate näide](media/error_record_id_source.png)

<span data-ttu-id="3bda2-131">Probleemi lahendamiseks peate määrama vastendatud Dynamics 365 Salesi või Dynamics 365 Customer Service'i äriüksusele õige turberolli puuduva privileegi lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="3bda2-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="3bda2-132">Otsige rakendusest Finance and Operations üles andmeintegratsiooni ühendusekogumis vastendatud äriüksus.</span><span class="sxs-lookup"><span data-stu-id="3bda2-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisatsiooni vastendamine](media/mapped_business_unit.png)

2. <span data-ttu-id="3bda2-134">Logige Dynamics 365 mudeljuhitud rakenduse keskkonda sisse, liikuge jaotisesse **Säte \> Turve** ja otsige üles vastendatud äriüksuse meeskond.</span><span class="sxs-lookup"><span data-stu-id="3bda2-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Vastendatud äriüksuse meeskond](media/setting_security_page.png)

3. <span data-ttu-id="3bda2-136">Avage selle meeskonna leht redigeerimiseks ja seejärel valige **Rollide haldamine** dialoogiboksi **Meeskonna rollide haldamine** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="3bda2-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Nupp rollide haldamine](media/manage_team_roles.png)

4. <span data-ttu-id="3bda2-138">Määrake roll, millel on asjaomaste tabelite lugemise/kirjutamise privileeg ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="3bda2-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="3bda2-139">Sünkroonimisprobleemide parandamine keskkonnas, millel on hiljuti muudetud Dataverse'i keskkond</span><span class="sxs-lookup"><span data-stu-id="3bda2-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="3bda2-140">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="3bda2-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="3bda2-141">Kui proovite luua rakenduses Finance and Operations andmeid, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="3bda2-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="3bda2-142">*{„entityName”:„CustCustomerV3Entity”,„executionStatus”:2,„fieldResponses”:\[\],„recordResponses”:\[{„errorMessage”:„**Lasti ei saanud luua üksusele CustCustomerV3Entity**”,„logDateTime”:„2019-08-27T18:51:52.5843124Z”,„verboseError”:„Lasti loomine nurjus tõrkega kehtetu URI: URI on tühi.”}\],„isErrorCountUpdated”:true}*</span><span class="sxs-lookup"><span data-stu-id="3bda2-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="3bda2-143">Dynamics 365 mudeljuhitud rakenduses näeb tõrge välja järgnev.</span><span class="sxs-lookup"><span data-stu-id="3bda2-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="3bda2-144">*ISV-koodist ilmnes ootamatu tõrge. (ErrorType = ClientError) Ootamatu erand lisandmoodulist (Käivita): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: üksuse konto töötlemine nurjus – (ühenduse loomise katse nurjus, kuna ühendatud osapool ei reageerinud pärast teatavat ajavahemikku või loodud ühendus nurjus, kuna ühendatud host ei vastanud*</span><span class="sxs-lookup"><span data-stu-id="3bda2-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="3bda2-145">See tõrge ilmneb, kui Dataverse'i keskkond on valesti lähtestatud sel ajal, kui proovite luua andmeid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3bda2-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="3bda2-146">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3bda2-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="3bda2-147">Logige sisse Finance and Operationsi virtuaalarvutisse (VM), avage SQL Server Management Studio (SSMS) ja otsige ridu tabelist DUALWRITEPROJECTCONFIGURATIONENTITY, kus **internalentityname** võrdub üksusega **Klientide V3** ja **externalentityname** võrdub üksusega **kontod**.</span><span class="sxs-lookup"><span data-stu-id="3bda2-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="3bda2-148">Päring näeb välja järgnev.</span><span class="sxs-lookup"><span data-stu-id="3bda2-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="3bda2-149">Kasutage järgmise päringu käivitamiseks eelmise päringu tulemuste projekti nime.</span><span class="sxs-lookup"><span data-stu-id="3bda2-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="3bda2-150">Veenduge, et veerul **externalenvironmentURL** oleks õige Dataverse'i või rakenduse URL.</span><span class="sxs-lookup"><span data-stu-id="3bda2-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="3bda2-151">Kustutage kõik duplikaatread, mis osutavad valele Dataverse'i URL-ile.</span><span class="sxs-lookup"><span data-stu-id="3bda2-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="3bda2-152">Kustutage vastavad read tabelitest DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="3bda2-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="3bda2-153">Peatage tabeli vastendamine ja taaskäivitage see</span><span class="sxs-lookup"><span data-stu-id="3bda2-153">Stop the table mapping, and then restart it</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]