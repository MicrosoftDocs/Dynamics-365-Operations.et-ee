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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 82bdcc71196c22689cc65601f98187aaa9e5e9d6
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997298"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="a782d-103">Reaalajas sünkroonimise probleemide tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="a782d-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="a782d-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="a782d-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="a782d-105">Eelkõige annab see teavet, mis aitab lahendada reaalajas sünkroonimisega seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="a782d-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a782d-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="a782d-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="a782d-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="a782d-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="a782d-108">Reaalajas sünkroonimine põhjustab 403 keelatud tõrke, kui loote kirje Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="a782d-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="a782d-109">Kui proovite luua rakenduses Finance and Operations kirjet, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="a782d-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="a782d-110">*\[{\\„tõrge\\”:{\\„kood\\”:\\„0x80072560\\”,\\„sõnum\\”:\\„Kasutaja pole organisatsiooni liige.\\”}}\], Kaugserver tagastas tõrke: (403) keelatud.”}}”.*</span><span class="sxs-lookup"><span data-stu-id="a782d-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="a782d-111">Probleemi lahendamiseks järgige juhiseid teemas [Süsteemi nõuded ja eeltingimused](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="a782d-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="a782d-112">Nende sammude lõpule viimiseks peab rakenduses Common Data Service loodud topeltkirjutuse kasutajatel olema süsteemiadministraatori roll.</span><span class="sxs-lookup"><span data-stu-id="a782d-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="a782d-113">Vaikeomanikust meeskonnal peab samuti olema süsteemiadministraatori roll.</span><span class="sxs-lookup"><span data-stu-id="a782d-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="a782d-114">Mis tahes üksuse reaalajas sünkroonimine põhjustab sarnase tõrke, kui loote kirje Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="a782d-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="a782d-115">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="a782d-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="a782d-116">Teile võidakse kuvada järgnev tõrketeate iga kord, kui proovite üksuse andmeid Finance and Operationsi rakenduses salvestada.</span><span class="sxs-lookup"><span data-stu-id="a782d-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="a782d-117">*Andmebaasi muudatusi ei saa salvestada. Tööüksus ei saa kannet kinnitada. Üksuse uoms-i ei saa andmeid kirjutada. Üksusesse UnitOfMeasureEntity kirjutamine nurjus, kuna tõrketeade ei saa sünkroonida üksuse uoms-i.*</span><span class="sxs-lookup"><span data-stu-id="a782d-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="a782d-118">Probleemi lahendamiseks peate veenduma, et eeltingimuseks olevad viiteandmed on olemas nii Finance and Operationsi rakenduses kui ka Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="a782d-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="a782d-119">Näiteks kui olete klient rakeenduses Finance and Operations, mis kuulub kindlasse kliendigruppi, veenduge, et see kliendigrupp on olemas Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="a782d-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="a782d-120">Kui andmed on olemas kummalgi poolel ja olete teinud kindlaks, et probleem ei ole seotud andmetega, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a782d-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="a782d-121">Peatage seostatud üksus.</span><span class="sxs-lookup"><span data-stu-id="a782d-121">Stop the related entity.</span></span>
2. <span data-ttu-id="a782d-122">Logige sisse rakendusse Finance and Operations ja veenduge, et nurjuva üksuse kirjed on olemas tabelites DualWriteProjectConfiguration ja DualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a782d-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="a782d-123">Näiteks selline näeb välja päring, kui üksus **Kliendid** nurjub.</span><span class="sxs-lookup"><span data-stu-id="a782d-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="a782d-124">Kui nurjunud üksusel on kirjeid ka pärast üksuse vastendamise peatamist, kustutage nurjunud üksusega seotud kirjed.</span><span class="sxs-lookup"><span data-stu-id="a782d-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="a782d-125">Märkige tabelis DualWriteProjectConfiguration veerg **projectname** ja tooge tabelist DualWriteProjectFieldConfiguration kirje, kasutades kirje kustutamiseks projekti nime.</span><span class="sxs-lookup"><span data-stu-id="a782d-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="a782d-126">Käivitage üksuse vastendamine.</span><span class="sxs-lookup"><span data-stu-id="a782d-126">Start the entity mapping.</span></span> <span data-ttu-id="a782d-127">Kontrollige, kas andmed sünkroonitakse tõrgeteta.</span><span class="sxs-lookup"><span data-stu-id="a782d-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="a782d-128">Lugemis- või kirjutusprivileegide tõrgete käsitlemine rakenduses Finance and Operations andmete loomisel</span><span class="sxs-lookup"><span data-stu-id="a782d-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="a782d-129">Võite saada tõrketeate „Vigane taotlus”, mis sarnaneb järgmise näitega rakenduses Finance and Operations andmete loomisel.</span><span class="sxs-lookup"><span data-stu-id="a782d-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Vigase taotluse tõrketeate näide](media/error_record_id_source.png)

<span data-ttu-id="a782d-131">Probleemi lahendamiseks peate määrama vastendatud Dynamics 365 Salesi või Dynamics 365 Customer Service'i äriüksusele õige turberolli puuduva privileegi lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="a782d-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="a782d-132">Otsige rakendusest Finance and Operations üles andmeintegratsiooni ühendusekogumis vastendatud äriüksus.</span><span class="sxs-lookup"><span data-stu-id="a782d-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisatsiooni vastendamine](media/mapped_business_unit.png)

2. <span data-ttu-id="a782d-134">Logige Dynamics 365 mudeljuhitud rakenduse keskkonda sisse, liikuge jaotisesse **Säte \> Turve** ja otsige üles vastendatud äriüksuse meeskond.</span><span class="sxs-lookup"><span data-stu-id="a782d-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security** , and find the team of the mapped business unit.</span></span>

    ![Vastendatud äriüksuse meeskond](media/setting_security_page.png)

3. <span data-ttu-id="a782d-136">Avage selle meeskonna leht redigeerimiseks ja seejärel valige **Rollide haldamine** dialoogiboksi **Meeskonna rollide haldamine** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="a782d-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Nupp rollide haldamine](media/manage_team_roles.png)

4. <span data-ttu-id="a782d-138">Määrake roll, millel on asjaomaste üksuste lugemise/kirjutamise privileeg ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a782d-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="a782d-139">Sünkroonimisprobleemide parandamine keskkonnas, millel on hiljuti muudetud Common Data Service'i keskkond</span><span class="sxs-lookup"><span data-stu-id="a782d-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="a782d-140">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="a782d-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="a782d-141">Kui proovite luua rakenduses Finance and Operations andmeid, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="a782d-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="a782d-142">*{„entityName”:„CustCustomerV3Entity”,„executionStatus”:2,„fieldResponses”:\[\],„recordResponses”:\[{„errorMessage”:„ **Lasti ei saanud luua üksusele CustCustomerV3Entity** ”,„logDateTime”:„2019-08-27T18:51:52.5843124Z”,„verboseError”:„Lasti loomine nurjus tõrkega kehtetu URI: URI on tühi.”}\],„isErrorCountUpdated”:true}*</span><span class="sxs-lookup"><span data-stu-id="a782d-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Unable to generate payload for entity CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="a782d-143">Dynamics 365 mudeljuhitud rakenduses näeb tõrge välja järgnev.</span><span class="sxs-lookup"><span data-stu-id="a782d-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="a782d-144">*ISV-koodist ilmnes ootamatu tõrge. (ErrorType = ClientError) Ootamatu erand lisandmoodulist (Käivita): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: üksuse konto töötlemine nurjus – (ühenduse loomise katse nurjus, kuna ühendatud osapool ei reageerinud pärast teatavat ajavahemikku või loodud ühendus nurjus, kuna ühendatud host ei vastanud*</span><span class="sxs-lookup"><span data-stu-id="a782d-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="a782d-145">See tõrge ilmneb, kui Common Data Service'i keskkond on valesti lähtestatud sel ajal, kui proovite luua andmeid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a782d-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="a782d-146">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a782d-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="a782d-147">Logige aiaaw Finance and Operationsi virtuaalarvutisse (VM), avage SQL Server Management Studio (SSMS) ja otsige kirjeid tabelist DUALWRITEPROJECTCONFIGURATIONENTITY, kus **internalentityname** võrdub üksusega **Klientide V3** ja **externalentityname** võrdub üksusega **kontod**.</span><span class="sxs-lookup"><span data-stu-id="a782d-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="a782d-148">Päring näeb välja järgnev.</span><span class="sxs-lookup"><span data-stu-id="a782d-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="a782d-149">Kasutage järgmise päringu käivitamiseks eelmise päringu tulemuste projekti nime.</span><span class="sxs-lookup"><span data-stu-id="a782d-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="a782d-150">Veenduge, et veerul **externalenvironmentURL** oleks õige Common Data Service'i või rakenduse URL.</span><span class="sxs-lookup"><span data-stu-id="a782d-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="a782d-151">Kustutage kõik duplikaatkirjed, mis osutavad valele Common Data Service'i URL-ile.</span><span class="sxs-lookup"><span data-stu-id="a782d-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="a782d-152">Kustutage vastavad kirjed tabelitest DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="a782d-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="a782d-153">Peatage üksuse vastendamine ja taaskäivitage see</span><span class="sxs-lookup"><span data-stu-id="a782d-153">Stop the entity mapping, and then restart it</span></span>
