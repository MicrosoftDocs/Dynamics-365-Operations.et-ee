---
title: Kombineeritud litsentsiplaadi vastuvõtmine
description: Selles teemas kirjeldatakse, kuidas kasutada kombineeritud litsentsiplaadi vastuvõtmist töö registreerimiseks ja loomiseks mitmele kaubale mobiilse seadmega.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a44165bc59d65a9dfdf8e591152f427b97930b34
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "365887"
---
# <a name="mixed-license-plate-receiving"></a><span data-ttu-id="98a3d-103">Kombineeritud litsentsiplaadi vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="98a3d-103">Mixed license plate receiving</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98a3d-104">Kombineeritud litsentsiplaadi vastuvõtmine võimaldab koostada mitmest kaubast koosneva litsentsiplaadi enne registreerimist ja paigutamistöö loomist.</span><span class="sxs-lookup"><span data-stu-id="98a3d-104">Mixed license plate receiving allows you to build a license plate consisting of multiple items before you register and create put-away work.</span></span> 

<span data-ttu-id="98a3d-105">Mitmest kaubast koosnevat litsentsiplaati pole vaja iga kauba registreerimiseks vastuvõtudokis jagada.</span><span class="sxs-lookup"><span data-stu-id="98a3d-105">A license plate that consists of multiple items does not have to be split at the receiving dock for you to register each item.</span></span> 

<span data-ttu-id="98a3d-106">Kaubaga seotud voo kasutamisel lähtedokumendi ridade tuvastamiseks võite skannida kauba juhtelemendil vöötkoodid.</span><span class="sxs-lookup"><span data-stu-id="98a3d-106">When using an item-related flow to identify the source document lines, you can scan bar codes on the item control.</span></span> <span data-ttu-id="98a3d-107">Kui vöötkoodile on konfigureeritud kogus ja mõõtühik, siis lisatakse kaup ja kogus automaatselt kombineeritud litsentsiplaadile ja teid suunatakse teise kauba skannimiseks ekraanile tagasi.</span><span class="sxs-lookup"><span data-stu-id="98a3d-107">If the bar code has a quantity and a unit of measure (UOM) configured on it, the item and quantity will automatically be added to the mixed license plate, and you will be returned to the screen to scan another item.</span></span> <span data-ttu-id="98a3d-108">See võimaldab skannida kiiresti kõiki kaupu, ilma et oleks vaja iga etapi puhul kinnitada.</span><span class="sxs-lookup"><span data-stu-id="98a3d-108">This allows you to quickly scan all the items without having to make a confirmation at each step.</span></span> 

<span data-ttu-id="98a3d-109">Kombineeritud litsentsiplaadi vastuvõtuvoos võite kuvada juba litsentsiplaadile skannitud kaupade loendi ja siit saab kauba kogust muuta või parandada.</span><span class="sxs-lookup"><span data-stu-id="98a3d-109">In the flow for mixed license plate receiving, you can display the list of items that are already scanned to the license plate and from here you can modify or correct the quantity of an item.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="98a3d-110">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="98a3d-110">Where it applies</span></span>

<span data-ttu-id="98a3d-111">Kombineeritud litsentsiplaadi vastuvõtmine on mobiilse seadme vastuvõtuvoog töö registreerimiseks ja loomiseks korraga mitmele reale/kaubale.</span><span class="sxs-lookup"><span data-stu-id="98a3d-111">Mixed license plate receiving is a mobile device receiving flow to register and create work for multiple lines/items at the same time.</span></span> <span data-ttu-id="98a3d-112">Sellest on abi, kui võtate vastu mitme kaubaga sissetulevaid litsentsiplaate.</span><span class="sxs-lookup"><span data-stu-id="98a3d-112">This is useful if you receive inbound license plates with multiple items.</span></span> 

## <a name="how-to-set-up-mixed-license-plate-receiving"></a><span data-ttu-id="98a3d-113">Kombineeritud litsentsiplaadi vastuvõtu seadistamine</span><span class="sxs-lookup"><span data-stu-id="98a3d-113">How to set up mixed license plate receiving</span></span>
<span data-ttu-id="98a3d-114">Kombineeritud litsentsiplaadi vastuvõtmine on seadistatud mobiilse seadme menüüelemendina.</span><span class="sxs-lookup"><span data-stu-id="98a3d-114">Mixed license plate receiving is set up as a mobile device menu item.</span></span>

<span data-ttu-id="98a3d-115">Peate looma uue menüüelemendi sellise töörežiimiga, mis ei kasuta olemasolevat tööd, ja kasutama ühte järgmistest meetoditest.</span><span class="sxs-lookup"><span data-stu-id="98a3d-115">You need to create a new menu item with mode work that does not use existing work and use one of the following methods:</span></span>

- <span data-ttu-id="98a3d-116">Kombineeritud litsentsiplaadi vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="98a3d-116">Mixed license plate receiving</span></span>
- <span data-ttu-id="98a3d-117">Kombineeritud litsentsiplaadi vastuvõtt ja kõrvaleseadmine</span><span class="sxs-lookup"><span data-stu-id="98a3d-117">Mixed license plate receiving and put away</span></span>

<span data-ttu-id="98a3d-118">Valikud lähtedokumendi ridade tuvastamiseks on ostutellimuse kaup, ostutellimuse rida, tagastustellimus, üleviimistellimuse kaup ja üleviimistellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="98a3d-118">The options to identify the source document lines are purchase order item, purchase order line, return order, transfer order item, and transfer order line.</span></span> <span data-ttu-id="98a3d-119">Nende valikutega saab vastuvõetavat tellimust ühel litsentsiplaadil muuta.</span><span class="sxs-lookup"><span data-stu-id="98a3d-119">These options can change the receiving order on a single license plate.</span></span> <span data-ttu-id="98a3d-120">Viimane valik on koormakauba järgi.</span><span class="sxs-lookup"><span data-stu-id="98a3d-120">The last option is by load item.</span></span> <span data-ttu-id="98a3d-121">Litsentsiplaadile saab lisada mitu kaupa, kuid mitme koorma vahel ei saa liikuda.</span><span class="sxs-lookup"><span data-stu-id="98a3d-121">You can add multiple items to a license plate, but you cannot switch between multiple loads.</span></span>
