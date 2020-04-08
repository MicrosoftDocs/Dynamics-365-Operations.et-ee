---
title: Probleemide tõrkeotsing esmase häälestamise ajal
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada topeltkirjutuse esmasel häälestamisel ilmnevaid probleeme Finance and Operationsi rakenduste ja Common Data Service'i vahel.
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
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172664"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="d5f38-103">Probleemide tõrkeotsing esmase häälestamise ajal</span><span class="sxs-lookup"><span data-stu-id="d5f38-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="d5f38-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="d5f38-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="d5f38-105">Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda topeltkirjutuse esialgse häälestamise käigus.</span><span class="sxs-lookup"><span data-stu-id="d5f38-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d5f38-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="d5f38-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="d5f38-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="d5f38-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="d5f38-108">Finance and Operationsi rakendust ei saa linkida Common Data Service'iga</span><span class="sxs-lookup"><span data-stu-id="d5f38-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="d5f38-109">**Topeltkirjutuse seadistamiseks nõutav mandaat:** Azure AD rentniku administraator</span><span class="sxs-lookup"><span data-stu-id="d5f38-109">**Required credentials to set up dual-write:** Azure AD tenant admin</span></span>

<span data-ttu-id="d5f38-110">Tõrkeid lehel **Common Data Service'i häälestuse link** põhjustab tavaliselt puudulik häälestus või lubade probleemid.</span><span class="sxs-lookup"><span data-stu-id="d5f38-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="d5f38-111">Veenduge, et kogu seisundikontroll läbitakse lehel **Common Data Service'i häälestuse link**, nagu näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="d5f38-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="d5f38-112">Topeltkirjutust ei saa linkida, kui tervet seisundikontrolli pole läbitud.</span><span class="sxs-lookup"><span data-stu-id="d5f38-112">You can't link dual-write unless the whole health check passes.</span></span>

![Edukas seisundikontroll](media/health_check.png)

<span data-ttu-id="d5f38-114">Keskkondade Finance and Operations ja Common Data Service linkimiseks peab teil olema Azure AD rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="d5f38-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="d5f38-115">Pärast keskkondade linkimist saavad kasutajad sisse logida oma konto mandaadiga ja värskendada olemasoleva üksuse vastenduse.</span><span class="sxs-lookup"><span data-stu-id="d5f38-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="d5f38-116">Tõrge Common Data Service'i lehe lingi avamisel</span><span class="sxs-lookup"><span data-stu-id="d5f38-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="d5f38-117">**Probleemi lahendamiseks nõutav mandaat:** Azure AD rentniku admin</span><span class="sxs-lookup"><span data-stu-id="d5f38-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="d5f38-118">Kui proovite avada rakenduses Finance and Operations lehte **Common Data Service'i link**, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="d5f38-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="d5f38-119">*Vastuse oleku kood ei näita edu: 404 (ei leitud).*</span><span class="sxs-lookup"><span data-stu-id="d5f38-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="d5f38-120">See tõrge ilmneb, kui nõusoleku etappi pole lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="d5f38-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="d5f38-121">Selleks, et kontrollida, kas nõusoleku etapp on lõpule viidud, logige sisse lehele portal.Azure.com Azure AD rentniku administraatori kontoga ja kontrollige, kas kolmanda osapoole rakendus, mille ID on **33976c19-1db5-4c02-810e-c243db79efde**, kuvatakse Azure AD **Ettevõtte rakenduste** loendis.</span><span class="sxs-lookup"><span data-stu-id="d5f38-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="d5f38-122">Kui seda pole, peate andma rakenduse nõusoleku.</span><span class="sxs-lookup"><span data-stu-id="d5f38-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="d5f38-123">Rakenduse nõusoleku andmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d5f38-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="d5f38-124">Avage järgmine URL administraatori mandaadiga.</span><span class="sxs-lookup"><span data-stu-id="d5f38-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="d5f38-125">Teilt küsitakse nõusolekut.</span><span class="sxs-lookup"><span data-stu-id="d5f38-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="d5f38-126">Valige **Nõustu**, et kinnitada oma nõusolekut rakenduse installimiseks, millel on teie rentniku ID **33976c19-1db5-4c02-810e-c243db79efde**.</span><span class="sxs-lookup"><span data-stu-id="d5f38-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="d5f38-127">See rakendus on nõutav rakendusre Common Data Service ja Finance and Operations linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="d5f38-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="d5f38-128">Kui teil on selle etapiga probleeme, avage brauser inkognito-režiimis (Google Chrome'is) või InPrivate-režiimis (rakenduses Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="d5f38-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="d5f38-129">Veenduge, et ettevõtte andmed ja topeltkirjutuse meeskonnad on linkimisel õigesti häälestatud</span><span class="sxs-lookup"><span data-stu-id="d5f38-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="d5f38-130">Tagamaks, et topeltkirjutus töötaks õigesti, luuakse konfiguratsiooni ajal valitud ettevõtted Common Data Service'i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="d5f38-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="d5f38-131">Vaikimisi on need ettevõtted kirjutuskaitstud ja atribuudi **IsDualWriteEnable** väärtuseks on seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="d5f38-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="d5f38-132">Lisaks luuakse vaikimisi omanikust äriüksuse omanik ja meeskond ning kaasatakse ettevõtte nimi.</span><span class="sxs-lookup"><span data-stu-id="d5f38-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="d5f38-133">Enne vastenduste lubamist kontrollige, kas meeskonna vaikeomanik on määratud.</span><span class="sxs-lookup"><span data-stu-id="d5f38-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="d5f38-134">Üksuse **Ettevõtted (CDM\_Company)** leidmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d5f38-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="d5f38-135">Valige filter Dynamics 365 mudeljuhitud rakenduse paremas ülanurgas.</span><span class="sxs-lookup"><span data-stu-id="d5f38-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="d5f38-136">Valige ripploendist **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="d5f38-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="d5f38-137">Tulemuste nägemiseks valige **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="d5f38-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="d5f38-138">Valige ettevõte, mis oli topeltkirjutuse konfigureerimisel lingitud.</span><span class="sxs-lookup"><span data-stu-id="d5f38-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="d5f38-139">Veenduge, et väljal **Vaikeomanikust meeskond** oleks väärtus.</span><span class="sxs-lookup"><span data-stu-id="d5f38-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="d5f38-140">Järgmisel joonisel on välja **Vaikeomanikust meeskond** väärtuseks seatud **USMF topeltkirjutus**.</span><span class="sxs-lookup"><span data-stu-id="d5f38-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![Vaikeomanikust meeskonna kontrollimine](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="d5f38-142">Leidke juriidiliste isikute või ettevõtete arvu piirang, mida saab siduda topeltkirjutusega</span><span class="sxs-lookup"><span data-stu-id="d5f38-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="d5f38-143">Kui proovite lubada vastendusi, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="d5f38-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="d5f38-144">*Topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: \[(Osavastendust ei saanud tuua projektile DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Tõrge ületab maksimaalse lubatud psade arvu vastendusele DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Ilmnes üks või mitu tõrget.*</span><span class="sxs-lookup"><span data-stu-id="d5f38-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="d5f38-145">Praegune piirang keskkondade linkimiseks on umbes 40 juriidilist isikut.</span><span class="sxs-lookup"><span data-stu-id="d5f38-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="d5f38-146">See tõrge ilmneb, kui proovite lubada vastendusi ja rohkem kui 40 juriidilist isikut on lingitud keskkondade vahel.</span><span class="sxs-lookup"><span data-stu-id="d5f38-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>
