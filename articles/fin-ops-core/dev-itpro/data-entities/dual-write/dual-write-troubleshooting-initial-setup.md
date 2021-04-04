---
title: Tõrkeotsingu probleemid algse häälestuse ajal
description: See teema annab teavet, mis võib aidata lahendada probleeme, mis ilmnevad topeltkirjutuse esialgse häälestamise käigus.
author: RamaKrishnamoorthy
manager: AnnBe
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
ms.openlocfilehash: f6ff9a304de8a94b86e6866d6d2cb65fbfdfb02f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561174"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="c8c47-103">Tõrkeotsingu probleemid algse häälestuse ajal</span><span class="sxs-lookup"><span data-stu-id="c8c47-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="c8c47-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="c8c47-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="c8c47-105">Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda topeltkirjutuse esialgse häälestamise käigus.</span><span class="sxs-lookup"><span data-stu-id="c8c47-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c8c47-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="c8c47-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c8c47-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="c8c47-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a><span data-ttu-id="c8c47-108">Finance and Operationsi rakendust ei saa linkida Dataverse'iga</span><span class="sxs-lookup"><span data-stu-id="c8c47-108">You can't link a Finance and Operations app to Dataverse</span></span>

<span data-ttu-id="c8c47-109">**Topeltkirjutuse seadistamiseks nõutav roll:** Finance and Operationsi rakenduste ja Dataverse'i süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="c8c47-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="c8c47-110">Tõrkeid lehel **Dataverse'i häälestuse link** põhjustab tavaliselt puudulik häälestus või lubade probleemid.</span><span class="sxs-lookup"><span data-stu-id="c8c47-110">Errors on the **Setup link to Dataverse** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="c8c47-111">Veenduge, et kogu seisundikontroll läbitakse lehel **Dataverse'i häälestuse link**, nagu näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="c8c47-111">Make sure that the whole health check passes on the **Setup link to Dataverse** page, as shown in the following illustration.</span></span> <span data-ttu-id="c8c47-112">Topeltkirjutust ei saa linkida, kui tervet seisundikontrolli pole läbitud.</span><span class="sxs-lookup"><span data-stu-id="c8c47-112">You can't link dual-write unless the whole health check passes.</span></span>

![Edukas seisundikontroll](media/health_check.png)

<span data-ttu-id="c8c47-114">Keskkondade Finance and Operations ja Dataverse linkimiseks peab teil olema Azure AD rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="c8c47-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Dataverse environments.</span></span> <span data-ttu-id="c8c47-115">Pärast keskkondade linkimist saavad kasutajad sisse logida oma konto mandaadiga ja värskendada olemasoleva tabeli vastenduse.</span><span class="sxs-lookup"><span data-stu-id="c8c47-115">After you link the environments, users can sign in by using their account credentials and update an existing table map.</span></span>

## <a name="error-when-you-open-the-link-to-dataverse-page"></a><span data-ttu-id="c8c47-116">Tõrge Dataverse'i lehe lingi avamisel</span><span class="sxs-lookup"><span data-stu-id="c8c47-116">Error when you open the Link to Dataverse page</span></span>

<span data-ttu-id="c8c47-117">**Probleemi lahendamiseks nõutav mandaat:** Azure AD rentniku admin</span><span class="sxs-lookup"><span data-stu-id="c8c47-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="c8c47-118">Kui proovite avada rakenduses Finance and Operations lehte **Dataverse'i link**, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="c8c47-118">You might receive the following error message when you open the **Link to Dataverse** page in a Finance and Operations app:</span></span>

<span data-ttu-id="c8c47-119">*Vastuse oleku kood ei näita edu: 404 (ei leitud).*</span><span class="sxs-lookup"><span data-stu-id="c8c47-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="c8c47-120">See tõrge ilmneb, kui nõusoleku etappi pole lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c8c47-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="c8c47-121">Selleks, et kontrollida, kas nõusoleku etapp on lõpule viidud, logige sisse lehele portal.Azure.com Azure AD rentniku administraatori kontoga ja kontrollige, kas kolmanda osapoole rakendus, mille ID on **33976c19-1db5-4c02-810e-c243db79efde**, kuvatakse Azure AD **Ettevõtte rakenduste** loendis.</span><span class="sxs-lookup"><span data-stu-id="c8c47-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="c8c47-122">Kui seda pole, peate andma rakenduse nõusoleku.</span><span class="sxs-lookup"><span data-stu-id="c8c47-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="c8c47-123">Rakenduse nõusoleku andmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c8c47-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="c8c47-124">Avage järgmine URL administraatori mandaadiga.</span><span class="sxs-lookup"><span data-stu-id="c8c47-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="c8c47-125">Teilt küsitakse nõusolekut.</span><span class="sxs-lookup"><span data-stu-id="c8c47-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="c8c47-126">Valige **Nõustu**, et kinnitada oma nõusolekut rakenduse installimiseks, millel on teie rentniku ID **33976c19-1db5-4c02-810e-c243db79efde**.</span><span class="sxs-lookup"><span data-stu-id="c8c47-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="c8c47-127">See rakendus on nõutav rakendusre Dataverse ja Finance and Operations linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="c8c47-127">This app is required to link Dataverse and Finance and Operations apps.</span></span> <span data-ttu-id="c8c47-128">Kui teil on selle etapiga probleeme, avage brauser inkognito-režiimis (Google Chrome'is) või InPrivate-režiimis (rakenduses Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="c8c47-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="c8c47-129">Veenduge, et ettevõtte andmed ja topeltkirjutuse meeskonnad on linkimisel õigesti häälestatud</span><span class="sxs-lookup"><span data-stu-id="c8c47-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="c8c47-130">Tagamaks, et topeltkirjutus töötaks õigesti, luuakse konfiguratsiooni ajal valitud ettevõtted Dataverse'i keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="c8c47-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Dataverse environment.</span></span> <span data-ttu-id="c8c47-131">Vaikimisi on need ettevõtted kirjutuskaitstud ja atribuudi **IsDualWriteEnable** väärtuseks on seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="c8c47-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="c8c47-132">Lisaks luuakse vaikimisi omanikust äriüksuse omanik ja meeskond ning kaasatakse ettevõtte nimi.</span><span class="sxs-lookup"><span data-stu-id="c8c47-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="c8c47-133">Enne vastenduste lubamist kontrollige, kas meeskonna vaikeomanik on määratud.</span><span class="sxs-lookup"><span data-stu-id="c8c47-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="c8c47-134">Tabeli **Ettevõtted (CDM\_Company)** leidmiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c8c47-134">To find the **Companies (CDM\_Company)** table, follow these steps.</span></span>

1. <span data-ttu-id="c8c47-135">Valige filter Dynamics 365 mudeljuhitud rakenduse paremas ülanurgas.</span><span class="sxs-lookup"><span data-stu-id="c8c47-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="c8c47-136">Valige ripploendist **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="c8c47-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="c8c47-137">Tulemuste nägemiseks valige **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="c8c47-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="c8c47-138">Valige ettevõte, mis oli topeltkirjutuse konfigureerimisel lingitud.</span><span class="sxs-lookup"><span data-stu-id="c8c47-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="c8c47-139">Veenduge, et veerus **Vaikeomanikust meeskond** oleks väärtus.</span><span class="sxs-lookup"><span data-stu-id="c8c47-139">Verify that the **Default owning team** column has a value.</span></span> <span data-ttu-id="c8c47-140">Järgmisel joonisel on veeru **Vaikeomanikust meeskond** väärtuseks seatud **USMF topeltkirjutus**.</span><span class="sxs-lookup"><span data-stu-id="c8c47-140">In the following illustration, the **Default owning team** column is set to **USMF Dual Write**.</span></span>

    ![Vaikeomanikust meeskonna kontrollimine](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="c8c47-142">Leidke juriidiliste tabelite või ettevõtete arvu piirang, mida saab siduda topeltkirjutusega</span><span class="sxs-lookup"><span data-stu-id="c8c47-142">Find the limit on the number of legal tables or companies that can be linked for dual-write</span></span>

<span data-ttu-id="c8c47-143">Kui proovite lubada vastendusi, võidakse kuvada järgmine tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="c8c47-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="c8c47-144">*Topeltkirjutuse tõrge – lisandmooduli registreerimine nurjus: \[(Osavastendust ei saanud tuua projektile DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Tõrge ületab maksimaalse lubatud psade arvu vastendusele DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Ilmnes üks või mitu tõrget.*</span><span class="sxs-lookup"><span data-stu-id="c8c47-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="c8c47-145">Praegune piirang keskkondade linkimiseks on umbes 40 juriidilist tabelit.</span><span class="sxs-lookup"><span data-stu-id="c8c47-145">The current limit when you link the environments is approximately 40 legal tables.</span></span> <span data-ttu-id="c8c47-146">See tõrge ilmneb, kui proovite lubada vastendusi ja rohkem kui 40 juriidilist tabelit on lingitud keskkondade vahel.</span><span class="sxs-lookup"><span data-stu-id="c8c47-146">This error occurs if you try to enable maps, and more than 40 legal tables are linked between the environments.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]