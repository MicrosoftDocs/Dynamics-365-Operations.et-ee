---
title: Isikupärastatud soovitustest loobumine
description: See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce isikupärastatud soovituste saamisest.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8e7b800218f68167901d86d61ae483680a04cfab
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025240"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="26d40-103">Isikupärastatud soovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="26d40-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="26d40-104">See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce isikupärastatud soovituste saamisest.</span><span class="sxs-lookup"><span data-stu-id="26d40-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="26d40-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="26d40-105">Overview</span></span>

<span data-ttu-id="26d40-106">Konto loomise ajal seadistatakse uued kliendid automaatselt saama isikupärastatud soovitusi.</span><span class="sxs-lookup"><span data-stu-id="26d40-106">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="26d40-107">Samas pakub rakendus Dynamics 365 Commerce jaemüüjatele erinevaid võimalusi nende soovituste saamisest loobumiseks ja oma isikuandmete töötlemise piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="26d40-107">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="26d40-108">Autenditud kasutajad, kes loobuvad isikupärastatud soovituste saamisest, lõpetavad kohe isikupärastatud loendite nägemise.</span><span class="sxs-lookup"><span data-stu-id="26d40-108">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="26d40-109">Lisaks eemaldatakse kõik isikupärastamiseks kogutavad isikuandmed isikupärastatud soovituste mudelitest.</span><span class="sxs-lookup"><span data-stu-id="26d40-109">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="26d40-110">Lisateavet isikupärastatud tootesoovituste kohta vt jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="26d40-110">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="26d40-111">Jaemüüjate loobumiskogemuse rakendamise viisid</span><span class="sxs-lookup"><span data-stu-id="26d40-111">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="26d40-112">Jaemüüjatel on loobumiskogemuse rakendamiseks kolm viisi.</span><span class="sxs-lookup"><span data-stu-id="26d40-112">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="26d40-113">Kasutajate nimel loobumine</span><span class="sxs-lookup"><span data-stu-id="26d40-113">Opting out on behalf of users</span></span>

<span data-ttu-id="26d40-114">Commerce’i kontori kontohalduses saavad jaemüüjad loobuda kasutajate nimel.</span><span class="sxs-lookup"><span data-stu-id="26d40-114">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="26d40-115">Otsige kontori avalehelt **kõiki kliente**.</span><span class="sxs-lookup"><span data-stu-id="26d40-115">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="26d40-116">Otsige ja valige klient ning seejärel valige kiirkaart **Jaemüük**.</span><span class="sxs-lookup"><span data-stu-id="26d40-116">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Jaemüügi kiirkaart](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="26d40-118">Jaotises **Privaatsus** seadke suvand **Keela isikupärastamine** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="26d40-118">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Privaatsussätted](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="26d40-120">Valige **Salvesta** ja sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="26d40-120">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="26d40-121">Moodulipõhine loobumise kogemus</span><span class="sxs-lookup"><span data-stu-id="26d40-121">Module-based opt-out experience</span></span>

<span data-ttu-id="26d40-122">Jaemüüjad võivad lubada autenditud kasutajatel ise isikupärastatud soovitustest loobuda.</span><span class="sxs-lookup"><span data-stu-id="26d40-122">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="26d40-123">Selle loobumiskogemuse pakkumiseks lisage kasutaja loobumise moodul konto profiili lehtedele.</span><span class="sxs-lookup"><span data-stu-id="26d40-123">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="26d40-124">Kohandatud laiendid</span><span class="sxs-lookup"><span data-stu-id="26d40-124">Custom extensions</span></span>

<span data-ttu-id="26d40-125">Jaemüüjad saavad luua oma laiendid, et hallata kasutajate loobumise kogemust.</span><span class="sxs-lookup"><span data-stu-id="26d40-125">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="26d40-126">Lisateavet vt [Jaemüügiserveri API-de kutsumine](e-commerce-extensibility/call-retail-server-apis.md) ja [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="26d40-126">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="26d40-127">Isikupärastatud soovituste andmete digitaalse koopia hankimine autenditud kasutaja nimel</span><span class="sxs-lookup"><span data-stu-id="26d40-127">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="26d40-128">Kliendid võivad soovida saada oma isikuandmete digitaalset koopiat ja vaadata nende soovituste tulemusi ka eksporditud vaates.</span><span class="sxs-lookup"><span data-stu-id="26d40-128">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="26d40-129">Kui klient seda teavet taotleb, peab jaemüüja looma kohandatud laienduse, mis kutsub jaemüügiserveri rakenduse programmeerimise liidest (API) ja päringuid teie loendist **Teile valitud**, mis põhineb kliendi ID-l.</span><span class="sxs-lookup"><span data-stu-id="26d40-129">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="26d40-130">Seejärel saab tulemusi eksportida komaeraldusega väärtuste (CSV) vormingus ja jagada kliendiga.</span><span class="sxs-lookup"><span data-stu-id="26d40-130">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="26d40-131">Järgmine näide näitab, kuidas jaemüüja saab seda ülesannet täita.</span><span class="sxs-lookup"><span data-stu-id="26d40-131">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="26d40-132">Jaemüüja loob kohandatud laienduse, et tõmmata kasutaja nimel isiklikke soovituste andmeid.</span><span class="sxs-lookup"><span data-stu-id="26d40-132">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="26d40-133">Lisateavet moodulite loomise, olemasolevate moodulite kloonimise, jaemüügiserveri API-de kutsumise ja andmetegevuste kutsumise kohta vt teemast [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="26d40-133">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="26d40-134">Kohandatud laiend teeb kutsungi tuumandmetegevusele **hangi-soovitused** ja edastab sellele nõutud teabe, mis põhineb loendi nõuetel.</span><span class="sxs-lookup"><span data-stu-id="26d40-134">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="26d40-135">Loendi **Teile valitud** korral peab laiend edastama andmetegevusele õige loendi nime ja kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="26d40-135">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="26d40-136">Üks kohandatud laiendi loomise viis on kloonida olemasolevaid toote kogumise mooduleid, mida kasutatakse soovituste tulemuste tagastamiseks.</span><span class="sxs-lookup"><span data-stu-id="26d40-136">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="26d40-137">Selle olemasoleva mooduli kloonimisega saab jaemüüja olemasolevat koodi muuta ja lisada uue nupu, mis ekspordib soovituste tulemused CSV-faili.</span><span class="sxs-lookup"><span data-stu-id="26d40-137">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="26d40-138">Lisateavet vt teemast [Alustuskomplekti mooduli kloonimine](e-commerce-extensibility/clone-starter-module.md) ja [Tootekogumi moodulid](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="26d40-138">For more information, see [Clone a starter kit module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="26d40-139">Jaemüügiserveri API teegi täieliku vaate leiate teemast [Jaemüügiserveri kliendi ja tarbija API-d](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="26d40-139">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="26d40-140">Pärast kohandatud laiendi loomist saab jaemüüja eksportida CSV-faili kõigi soovituste tulemustega autenditud kasutaja kordumatu kliendi ID alusel.</span><span class="sxs-lookup"><span data-stu-id="26d40-140">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="26d40-141">Jaemüüja saab anda eksporditud CSV-faili, mis sisaldab soovitatavate toodete täielikku isikupärastatud loendit, autenditud kasutajaga ühiskasutusse.</span><span class="sxs-lookup"><span data-stu-id="26d40-141">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26d40-142">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="26d40-142">Additional resources</span></span>

[<span data-ttu-id="26d40-143">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="26d40-143">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="26d40-144">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="26d40-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="26d40-145">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="26d40-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="26d40-146">Tootesoovituste loendite lisamine lehtedele</span><span class="sxs-lookup"><span data-stu-id="26d40-146">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="26d40-147">Kassaseadmetele soovituste paneeli lisamine</span><span class="sxs-lookup"><span data-stu-id="26d40-147">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="26d40-148">Tootekogumi mooduli ülevaade</span><span class="sxs-lookup"><span data-stu-id="26d40-148">Product collection module overview</span></span>](product-collection-module-overview.md)
