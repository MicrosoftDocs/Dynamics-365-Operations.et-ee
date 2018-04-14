---
title: Hooldusobjektigrupid
description: "Objektigrupid on kasulikud objektide kohta käivate andmete sortimiseks ja filtreerimiseks aruannetes ja statistikas kasutamiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e539d92753bbbc4ac0ca88cec83c4d15135c388b
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="service-object-groups"></a><span data-ttu-id="ecb9c-103">Hooldusobjekti grupid</span><span class="sxs-lookup"><span data-stu-id="ecb9c-103">Service object groups</span></span> 

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ecb9c-104">Objektigrupid on kasulikud objektide kohta käivate andmete sortimiseks ja filtreerimiseks aruannetes ja statistikas kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-104">Object groups are useful for sorting and filtering the data about objects for reports and statistics.</span></span> <span data-ttu-id="ecb9c-105">Näiteks saate grupeerida objekte geograafilise asukoha või tüübi järgi.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-105">For example, you can group objects by geographical location or by type.</span></span>

## <a name="group-by-geographical-location"></a><span data-ttu-id="ecb9c-106">Grupeeri geograafilise asukoha järgi</span><span class="sxs-lookup"><span data-stu-id="ecb9c-106">Group by geographical location</span></span>

<span data-ttu-id="ecb9c-107">Saate kasutada seda grupeerimismeetodit, et näidata, kus asuvad erinevad objektid, mida teie ettevõte teenindab.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-107">You can use this grouping method to show where the various different objects that your company services are located.</span></span> <span data-ttu-id="ecb9c-108">Objektide grupeerimine geograafilise asukoha järgi võib olla kasulik ka siis, kui peate näiteks tuvastama objektid, millele juba selles konkreetses riigis/regioonis hooldust osutate.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-108">Grouping objects by geographical location can also be useful if, for example, you must identify the objects that your company already provides services for in a particular country/region.</span></span>

## <a name="example"></a><span data-ttu-id="ecb9c-109">Näide</span><span class="sxs-lookup"><span data-stu-id="ecb9c-109">Example</span></span>

<span data-ttu-id="ecb9c-110">Klient Belgiast helistab teie teeninduskeskusesse ja soovib luua hooldusleppe objektile ABC.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-110">A customer from Belgium calls your service center and wants to create a service agreement for an object, ABC.</span></span> <span data-ttu-id="ecb9c-111">Olete lisanud geograafilise asukoha objektigrupi, Belgia, kõigile Belgias teenindavatele objektidele.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-111">You have attached an object group for geographical location, Belgium, to all objects that are serviced in Belgium.</span></span> <span data-ttu-id="ecb9c-112">Kasutades seda gruppi filtrina, saate kiiresti otsida, et näha, kas ABC on kirjena teie rakenduses juba olemas või peate seadistama uue objekti.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-112">By using this group as a filter, you can quickly search to see whether you already have a record for ABC in the program, or whether you must set up a new object.</span></span> 

## <a name="group-by-type"></a><span data-ttu-id="ecb9c-113">Grupeeri tüübi järgi</span><span class="sxs-lookup"><span data-stu-id="ecb9c-113">Group by type</span></span>

<span data-ttu-id="ecb9c-114">Saate kasutada seda grupeerimismeetodit, et näidata, millist tüüpi objektidele teie ettevõtte hooldust osutab.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-114">You can use this grouping method to show the types of objects that your company services.</span></span> <span data-ttu-id="ecb9c-115">Objektide grupeerimine tüübi järgi võib olla kasulik ka siis, kui soovite näiteks luua uue objekti, mis põhineb sarnastel, programmis olemasolevatel objektidel.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-115">Grouping objects by type can also be useful if, for example, you want to create a new object based on similar objects that already exist in the program.</span></span>

## <a name="example"></a><span data-ttu-id="ecb9c-116">Näide</span><span class="sxs-lookup"><span data-stu-id="ecb9c-116">Example</span></span>

<span data-ttu-id="ecb9c-117">Klient helistab ja soovib sõlmida hooldusleppe õhukonditsioneeri, HIJ, kohta.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-117">A customer calls and wants to set up a service agreement for an air conditioning machine, HIJ.</span></span> <span data-ttu-id="ecb9c-118">Teil ei ole selle masina kohta veel kirjet.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-118">You do not already have a record for this machine.</span></span> <span data-ttu-id="ecb9c-119">Küll aga olete seadistanud objektigrupi nimega Õhukonditsioneerid ja olete lisanud selle grupi kõigile õhukonditsioneer-objektidele.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-119">However, you have set up an object group titled Air Conditioners, and you have attached this group to all air conditioning objects.</span></span> <span data-ttu-id="ecb9c-120">Seega saate kiiresti otsida ja tuvastada kõik muud õhukonditsioneer-masinad ja kasutada nende objektide malliteavet, et HIJ-ile hooldusleppe ridasid luua.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-120">Therefore, you can quickly search for and identify all other air conditioning machines and use the template information from these objects to create service agreement lines for HIJ.</span></span> <span data-ttu-id="ecb9c-121">Kasutades objektigruppe sel viisil saate kiiresti uusi objekte seadistada ja määrata, milliseid hooldustöid nende puhul teostada.</span><span class="sxs-lookup"><span data-stu-id="ecb9c-121">By using object groups in this manner, you can quickly set up new objects and determine the service tasks that must be performed on them.</span></span> 




