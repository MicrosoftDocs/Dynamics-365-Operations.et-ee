---
title: Jaemüügihinna aruanded
description: Selles teemas antakse ülevaade hinnaaruande funktsioonist, mida saab kasutada tootesortimendi puhul tulevaste hinnamuutuste kuvamiseks.
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: f317b22f2794dc71093068a51c8e9d4e6d7d55ac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231148"
---
# <a name="retail-price-reports"></a><span data-ttu-id="bb426-103">Jaemüügihinna aruanded</span><span class="sxs-lookup"><span data-stu-id="bb426-103">Retail price reports</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="bb426-104">Klientidele konkurentsivõimeliste hindade pakkumiseks muudavad jaemüüjad sageli toodete hinda.</span><span class="sxs-lookup"><span data-stu-id="bb426-104">In order to provide competitive prices to their customers, retailers often change prices of products.</span></span> <span data-ttu-id="bb426-105">Kauplusejuhatajad soovivad hõlpsat juurdepääsu hiljutistele või tulevastele hinnamuutustele, et saaksid plaanida poeriiulitel olevate hinnasiltide värskendamiseks vajalikke ressursse.</span><span class="sxs-lookup"><span data-stu-id="bb426-105">Store managers want the ability to easily access recent or upcoming price changes so that they can plan for the required resources to update the price labels displayed on the store shelves.</span></span> <span data-ttu-id="bb426-106">Rakenduse Retail versioonis 10.0 saab kaupluse juhataja avada aruande **Hind**, navigeerides jaotisse **Kõik kauplused \> Kauplus \> Hinnaaruanne** ja vaadates kauplusega seotud toodete värskendatud hindu.</span><span class="sxs-lookup"><span data-stu-id="bb426-106">With release 10.0 of Retail, a store manager can open the **Price** report by navigating to **All stores \> Store \> Price report** and viewing the updated prices for the products associated to the store.</span></span> 

<span data-ttu-id="bb426-107">Hinnaaruande lubamiseks peab parameeter **Luba kaupluse hinnaaruanne** olema sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="bb426-107">To enable the price report, the **Enable price report for store** parameter must be turned on.</span></span> <span data-ttu-id="bb426-108">See parameeter asub vahekaardil **Kaubanduse parameetrid \> Allahindlused \> Mitmesugust**. Lehe **Hinnaaruanne** avamisel kuvatakse dialoogiboks mitmesuguste konfiguratsioonidega.</span><span class="sxs-lookup"><span data-stu-id="bb426-108">This parameter is located on the **Commerce parameters \> Discounts \> Miscellaneous** tab. Opening the **Price report** page displays a dialog box with various configurations.</span></span> <span data-ttu-id="bb426-109">Allpool on loetletud saadaolevad konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="bb426-109">The available configurations are listed below.</span></span>

| <span data-ttu-id="bb426-110">Konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="bb426-110">Configuration</span></span> | <span data-ttu-id="bb426-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bb426-111">Description</span></span> |
|---|---|
| <span data-ttu-id="bb426-112">Alguskuupäev/lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="bb426-112">From date / To date</span></span>| <span data-ttu-id="bb426-113">Kuupäevavahemik, mille kohta tuleb hinnaaruanne luua.</span><span class="sxs-lookup"><span data-stu-id="bb426-113">The date range for which the price report should be generated.</span></span> <span data-ttu-id="bb426-114">Kestus on praegu kuni 7 päeva.</span><span class="sxs-lookup"><span data-stu-id="bb426-114">The duration is currently limited to 7 days.</span></span> |
| <span data-ttu-id="bb426-115">Kanal</span><span class="sxs-lookup"><span data-stu-id="bb426-115">Channel</span></span>| <span data-ttu-id="bb426-116">Kauplus, mille kohta tuleb hinnaaruanne luua.</span><span class="sxs-lookup"><span data-stu-id="bb426-116">The store for which the price report should be generated.</span></span> |
| <span data-ttu-id="bb426-117">Kuva tooted ja saadaolevad varud</span><span class="sxs-lookup"><span data-stu-id="bb426-117">Display products with available inventory</span></span>| <span data-ttu-id="bb426-118">Kui valite selle suvandi sätteks **Jah**, kuvatakse hinnad ainult nende toodete kohta, millel on kaupluses praegu füüsilised varud saadaval.</span><span class="sxs-lookup"><span data-stu-id="bb426-118">Setting this to **Yes** will show the prices for only those products which currently have physical inventory available in the store.</span></span> |
| <span data-ttu-id="bb426-119">Kuva tootevariantide hinnad</span><span class="sxs-lookup"><span data-stu-id="bb426-119">Display prices for variants</span></span> | <span data-ttu-id="bb426-120">Kui valite selle suvandi sätteks **Jah**, kuvatakse koos tooteetalonidega tootevariantide hinnad.</span><span class="sxs-lookup"><span data-stu-id="bb426-120">Setting this to **Yes** will display the prices of the variants along with the product masters.</span></span> <span data-ttu-id="bb426-121">See väli tuleks olekusse **Sees** lülitada ainult siis, kui teil on variandikohaseid hindu, kuna ridade arv muutub väga suureks.</span><span class="sxs-lookup"><span data-stu-id="bb426-121">This should only be turned **On** if you have variant-specific prices, because the number of rows grows very large.</span></span> <span data-ttu-id="bb426-122">Tulevastes väljaannetes lubame dimensioonipõhised hinnad, nii et kaupluse juhataja saab valida dimensioonid, mille kohta hinnad tuleb kuvada.</span><span class="sxs-lookup"><span data-stu-id="bb426-122">In future releases, we will enable the dimensions-based prices so that the store manager can choose the dimensions for which the prices should be displayed.</span></span> |
| <span data-ttu-id="bb426-123">Kuva hinnamuudatustega tooted</span><span class="sxs-lookup"><span data-stu-id="bb426-123">Display products with price changes</span></span> | <span data-ttu-id="bb426-124">Kui valite selle suvandi sätteks **Jah**, kuvatakse hinnad ainult nende kuupäevade kohta, millal hind on muutunud.</span><span class="sxs-lookup"><span data-stu-id="bb426-124">Setting this to **Yes** will display the prices for only those dates on which the price has been changed.</span></span> <span data-ttu-id="bb426-125">Hind *üks päev enne* valitud **alguskuupäeva** kuvatakse alati, nii et kaupluse juht saab hõlpsasti tuvastada tooted, mille hind pole kogu valitud ajaperioodi jooksul muutunud, ja kuvada ka praeguse hinna.</span><span class="sxs-lookup"><span data-stu-id="bb426-125">The price for *one day before* the selected **From date** will always be displayed, so that the store manager can easily identity the products which have not changed prices for the entire selected duration, and can also view the current price.</span></span> |

<span data-ttu-id="bb426-126">Kui aruanne on loodud, saab selle Exceli failina alla laadida, et kasutada täiendavaid filtreerimisvalikuid.</span><span class="sxs-lookup"><span data-stu-id="bb426-126">After the report is generated, the Excel file can be downloaded for any additional filtering needs.</span></span> <span data-ttu-id="bb426-127">Hinnaaruannet saab kasutada ka toodete varasemate hindade kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="bb426-127">The price report can also be used to check the historical prices of products for past dates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]