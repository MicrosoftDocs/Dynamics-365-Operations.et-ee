---
title: Tootmisüksuse loomine
description: Tootmisüksus on organisatsioon, mida kasutatakse äri majandusressursside ja tööprotsesside juhtimise jagamiseks.
author: sericks007
manager: AnnBe
ms.date: 08/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMOperatingUnit, OMInternalOrganizationSelector
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38db4a5f93f4b755cfd6fee43eaef27672551077
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143830"
---
# <a name="create-an-operating-unit"></a><span data-ttu-id="a4dc7-103">Tootmisüksuse loomine</span><span class="sxs-lookup"><span data-stu-id="a4dc7-103">Create an operating unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a4dc7-104">Tootmisüksus on organisatsioon, mida kasutatakse äri majandusressursside ja tööprotsesside juhtimise jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-104">An operating unit is an organization that is used to divide the control of economic resources and operational processes in a business.</span></span> <span data-ttu-id="a4dc7-105">Inimestel tootmisüksuses on kohustus maksimeerida nappide ressursside kasutamist, täiustada protsesse ja vastutada nende toimivuse eest.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-105">People in an operating unit have a duty to maximize the use of scarce resources, improve processes, and account for their performance.</span></span> <span data-ttu-id="a4dc7-106">Tootmisüksuste tüübid on kulukeskused, äriüksused, osakonnad ja väärtusevood.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-106">The types of operating units include cost centers, business units, departments, and value streams.</span></span> <span data-ttu-id="a4dc7-107">Kasutage tootmisüksuse loomiseks järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-107">Use the following procedure to create an operating unit.</span></span> <span data-ttu-id="a4dc7-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="a4dc7-109">Avage **Navigeerimispaan > Moodulid > Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-109">Go to **Navigation pane > Modules > Organization administration > Organizations > Operating units.**</span></span>
2. <span data-ttu-id="a4dc7-110">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-110">Click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="a4dc7-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="a4dc7-112">Saate valida loodava tootmisüksuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-112">Select the type of operating unit you want to create.</span></span>  
4. <span data-ttu-id="a4dc7-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-113">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a4dc7-114">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-114">In the **Name** field, type a value.</span></span>
    + <span data-ttu-id="a4dc7-115">Vajaduse korral laiendage jaotist **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-115">Expand the **General** section, if necessary.</span></span>  
    + <span data-ttu-id="a4dc7-116">Sisestage tootmisüksuse kohta üldine teave, nagu ID-kood, DUNS-number ja haldur.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-116">Provide general information about the operating unit, such as an identification number, DUNS number, and manager.</span></span>    
    + <span data-ttu-id="a4dc7-117">Vajaduse korral laiendage jaotist **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-117">Expand the **Addresses** section, if necessary.</span></span>  
    + <span data-ttu-id="a4dc7-118">Sisestage aadressiteave, nt tänavanimi, majanumber, sihtnumber ja linn.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-118">Enter address information, such as the street name and number, postal code, and city.</span></span> <span data-ttu-id="a4dc7-119">Klõpsake suvandit **Lisa**, et sisestada uus aadressikirje, või suvandit Redigeeri, et muuta olemasolevat aadressikirjet.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-119">Click **Add** to enter a new address record, or click Edit to modify an existing address record.</span></span>   
    + <span data-ttu-id="a4dc7-120">Vajaduse korral laiendage jaotist **Kontaktteave**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-120">Expand the **Contact information** section, if necessary.</span></span>  
    + <span data-ttu-id="a4dc7-121">Sisestage teave selliste sidepidamisviiside kohta nagu meiliaadressid, URL-id ja telefoninumbrid.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-121">Enter information about methods of communication, such as email addresses, URLs, and telephone numbers.</span></span> <span data-ttu-id="a4dc7-122">Uue sidekirje sisestamiseks klõpsake suvandit Uus.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-122">To enter a new communication record, click New.</span></span> <span data-ttu-id="a4dc7-123">Olemasoleva sidekirje muutmiseks klõpsake suvandeid **Rohkem suvandeid > Täpsem**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-123">To modify an existing communication record, click **More options > Advanced**.</span></span>   
6. <span data-ttu-id="a4dc7-124">Muutke valikut **Tootmisüksuse number** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-124">Optionally, change the **Operating unit number** as needed.</span></span> <span data-ttu-id="a4dc7-125">Pange tähele, et see number on ainuidentifikaator, mis vastab kirjele **Osapool** ja see ei saa olla sama ühegi teise tootmisüksusega.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-125">Note that this number is a unique idenitifier for the correspondng **Party** record and cannot be the same as any other operating unit.</span></span>
7. <span data-ttu-id="a4dc7-126">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-126">Select **Save**.</span></span>
