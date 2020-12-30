---
title: Loo veokiri
description: See teema kirjeldab, kuidas luua veokirja, kui kasutate laohalduse protsesse.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd014f5804681936920b47e999709f153def11bc
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426677"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="cf6b8-103">Loo veokiri</span><span class="sxs-lookup"><span data-stu-id="cf6b8-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf6b8-104">See teema kirjeldab, kuidas luua veokirja, kui kasutate laohalduse protsesse.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="cf6b8-105">Veokiri on juriidiline dokument kaupu tarniva ettevõtte ja vedaja vahel.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="cf6b8-106">Dokument on tarnitavate kaupadega kaasas ja see on saadetise kviitungiks, kui kaubad tarnitakse sihtkohta.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="cf6b8-107">Kui kasutate laohaldust, on veokirja loomiseks kaks viisi.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="cf6b8-108">Looge aruanne käsitsi, kasutades lehte **Veokiri**.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="cf6b8-109">Looge aruanne valikust **Koorma planeerimise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="cf6b8-110">Kui loote veokirja valikust **Koorma planeerimise töölaud**, siis peab koorma olek olema **Välja saadetud**</span><span class="sxs-lookup"><span data-stu-id="cf6b8-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="cf6b8-111">Kui koormas on rohkem kui üks saadetis, luuakse veokiri iga saadetise jaoks.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="cf6b8-112">Pärast veokirja loomist saate seda muuta lehel **Veokiri**.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="cf6b8-113">Põhiveokiri</span><span class="sxs-lookup"><span data-stu-id="cf6b8-113">Master bill of lading</span></span>
<span data-ttu-id="cf6b8-114">Kui koormas on rohkem kui üks saadetis, saate luua koondveokirja.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="cf6b8-115">Sellel on sama paigutus ja teave kui veokirjal, kuid sisaldab kokkuvõtlikku sisu kõikide saadetiste kohta.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="cf6b8-116">Kui valiku **Loo põhiveokiri, kui koormas on rohkem kui üks saadetis** sätteks on **Jah** lehel **Transpordihalduse parameetrid**, luuakse koondveokiri automaatselt, kui loote veokirja valikust **Koorma planeerimise töölaud** ja on rohkem kui üks saadetis.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="cf6b8-117">Saate ka loendi veokirjadest, klõpsates valikuid **Seotud teave** &gt; **Veokiri**.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="cf6b8-118">Kui loote veokirju käsitsi, saate koondveokirja luua lehel **Veokiri**.</span><span class="sxs-lookup"><span data-stu-id="cf6b8-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



