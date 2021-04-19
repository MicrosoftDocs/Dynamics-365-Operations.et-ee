---
title: Hooldusobjektigrupid
description: Objektigrupid on kasulikud objektide kohta käivate andmete sortimiseks ja filtreerimiseks aruannetes ja statistikas kasutamiseks.
author: ShylaThompson
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a559bdc8f7851e38274d9d23070f969502942ad8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835866"
---
# <a name="service-object-groups"></a><span data-ttu-id="db695-103">Hooldusobjekti grupid</span><span class="sxs-lookup"><span data-stu-id="db695-103">Service object groups</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db695-104">Objektigrupid on kasulikud objektide kohta käivate andmete sortimiseks ja filtreerimiseks aruannetes ja statistikas kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="db695-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="db695-105">Näiteks saate grupeerida objekte geograafilise asukoha või tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="db695-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="db695-106">Grupeeri geograafilise asukoha järgi</span><span class="sxs-lookup"><span data-stu-id="db695-106">Group by geographical location</span></span>

<span data-ttu-id="db695-107">Saate kasutada seda grupeerimismeetodit, et näidata, kus asuvad erinevad objektid, mida teie ettevõte teenindab.</span><span class="sxs-lookup"><span data-stu-id="db695-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="db695-108">Objektide grupeerimine geograafilise asukoha järgi võib olla kasulik ka siis, kui peate näiteks tuvastama objektid, millele juba selles konkreetses riigis/regioonis hooldust osutate.</span><span class="sxs-lookup"><span data-stu-id="db695-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="db695-109">Näide</span><span class="sxs-lookup"><span data-stu-id="db695-109">Example</span></span>

<span data-ttu-id="db695-110">Klient Belgiast helistab teie teeninduskeskusesse ja soovib luua hooldusleppe objektile ABC.</span><span class="sxs-lookup"><span data-stu-id="db695-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="db695-111">Olete lisanud geograafilise asukoha objektigrupi, Belgia, kõigile Belgias teenindavatele objektidele.</span><span class="sxs-lookup"><span data-stu-id="db695-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="db695-112">Kasutades seda gruppi filtrina, saate kiiresti otsida, et näha, kas ABC on kirjena teie rakenduses juba olemas või peate seadistama uue objekti.</span><span class="sxs-lookup"><span data-stu-id="db695-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="db695-113">Grupeeri tüübi järgi</span><span class="sxs-lookup"><span data-stu-id="db695-113">Group by type</span></span>

<span data-ttu-id="db695-114">Saate kasutada seda grupeerimismeetodit, et näidata, millist tüüpi objektidele teie ettevõtte hooldust osutab.</span><span class="sxs-lookup"><span data-stu-id="db695-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="db695-115">Objektide grupeerimine tüübi järgi võib olla kasulik ka siis, kui soovite näiteks luua uue objekti, mis põhineb sarnastel, programmis olemasolevatel objektidel.</span><span class="sxs-lookup"><span data-stu-id="db695-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="db695-116">Näide</span><span class="sxs-lookup"><span data-stu-id="db695-116">Example</span></span>

<span data-ttu-id="db695-117">Klient helistab ja soovib sõlmida hooldusleppe õhukonditsioneeri, HIJ, kohta.</span><span class="sxs-lookup"><span data-stu-id="db695-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="db695-118">Teil ei ole selle masina kohta veel kirjet.</span><span class="sxs-lookup"><span data-stu-id="db695-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="db695-119">Küll aga olete seadistanud objektigrupi nimega Õhukonditsioneerid ja olete lisanud selle grupi kõigile õhukonditsioneer-objektidele.</span><span class="sxs-lookup"><span data-stu-id="db695-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="db695-120">Seega saate kiiresti otsida ja tuvastada kõik muud õhukonditsioneer-masinad ja kasutada nende objektide malliteavet, et HIJ-ile hooldusleppe ridasid luua.</span><span class="sxs-lookup"><span data-stu-id="db695-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="db695-121">Kasutades objektigruppe sel viisil saate kiiresti uusi objekte seadistada ja määrata, milliseid hooldustöid nende puhul teostada.</span><span class="sxs-lookup"><span data-stu-id="db695-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 

## <a name="create-service-object-groups"></a><span data-ttu-id="db695-122">Hooldusobjektide gruppide loomine</span><span class="sxs-lookup"><span data-stu-id="db695-122">Create service object groups</span></span>

<span data-ttu-id="db695-123">Looge gruppe, millele saate määrata teenuseobjekte.</span><span class="sxs-lookup"><span data-stu-id="db695-123">Create groups that you can assign service objects to.</span></span> <span data-ttu-id="db695-124">Teenuseobjektid on laokaup ja muud tooted, mille jaoks teenuseid tehakse.</span><span class="sxs-lookup"><span data-stu-id="db695-124">Service objects are inventory items and other products for which services are performed.</span></span> <span data-ttu-id="db695-125">Teenuseobjekte rühmitades saate luua aruandeid sarnaste ja seotud teenuseobjektide jaoks.</span><span class="sxs-lookup"><span data-stu-id="db695-125">By grouping service objects, you can create reports for similar and related service objects.</span></span> <span data-ttu-id="db695-126">Näiteks võib teenuseobjekti grupp koosneda kahest teenuseobjektist: üks teenuseobjekt on komplekt ja teine on teenus komplekti installimiseks.</span><span class="sxs-lookup"><span data-stu-id="db695-126">For example, a service object group might consist of two service objects: One service object is a kit, and the second service object is the service to install the kit.</span></span>

<span data-ttu-id="db695-127">Teenuseobjekti gruppide loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="db695-127">To create service object groups, follow these steps:</span></span>

1. <span data-ttu-id="db695-128">Klõpsake valikuid **Hooldushaldus > Häälestus > Hooldusobjektid > Teenuseobjekti grupid**.</span><span class="sxs-lookup"><span data-stu-id="db695-128">Click **Service management > Setup > Service objects > Service object groups**.</span></span>

2. <span data-ttu-id="db695-129">Uue teenuseobjekti grupi loomiseks klõpsake käsku **Uus**.</span><span class="sxs-lookup"><span data-stu-id="db695-129">Click **New** to create a new service object group.</span></span>

3. <span data-ttu-id="db695-130">Sisestage teenusobjekti grupi kordumatu nimi ja soovi korral kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="db695-130">Enter a unique name for the service object group and, optionally, a description.</span></span>

<span data-ttu-id="db695-131">Saate määrata teenusegruppi objekte, kasutades vormi **Teenuseobjektid**.</span><span class="sxs-lookup"><span data-stu-id="db695-131">You can assign service objects to the group by using the **Service objects** form.</span></span> 

## <a name="see-also"></a><span data-ttu-id="db695-132">Vt ka</span><span class="sxs-lookup"><span data-stu-id="db695-132">See also</span></span>

[<span data-ttu-id="db695-133">Teenuseobjektide loomine</span><span class="sxs-lookup"><span data-stu-id="db695-133">Create service objects</span></span>](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]