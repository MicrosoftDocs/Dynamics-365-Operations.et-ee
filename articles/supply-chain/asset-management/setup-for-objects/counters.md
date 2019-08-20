---
title: Varamõõdikud
description: Teemas selgitatakse varamõõdikute tüüpe rakenduses Asset Management.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783217"
---
# <a name="asset-measures"></a><span data-ttu-id="5309b-103">Varamõõdikud</span><span class="sxs-lookup"><span data-stu-id="5309b-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="5309b-104">Teemas selgitatakse varamõõdikute tüüpe rakenduses Asset Management.</span><span class="sxs-lookup"><span data-stu-id="5309b-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="5309b-105">Varamõõdikute tüüpe kautatakse varade mõõdikute registreerimiseks (nt tootmistundide arv, varas toodetud kogus).</span><span class="sxs-lookup"><span data-stu-id="5309b-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="5309b-106">Varatüübid on seotud varamõõdikute tüüpidega.</span><span class="sxs-lookup"><span data-stu-id="5309b-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="5309b-107">See tähendab, et varamõõdikut saab kasutada vara puhul, kui varamõõdik on seaditatud varas kasutatud varatüübile.</span><span class="sxs-lookup"><span data-stu-id="5309b-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="5309b-108">Enne varamõõdikute registreerimist peate smalt looma kasutatavad varamõõdikute tüübid üksuses **Loendur**.</span><span class="sxs-lookup"><span data-stu-id="5309b-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="5309b-109">Järgmisena saate luua varade mõõdikute registreerimised üksuses **Varamõõdikud**.</span><span class="sxs-lookup"><span data-stu-id="5309b-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="5309b-110">Varamõõdikuid saab kasutada hoolduskavades.</span><span class="sxs-lookup"><span data-stu-id="5309b-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="5309b-111">Hoolduskava rea tüüp võib olla näiteks „Loendur”, mis on seotud tootmistundide arvu või toodetud kogusega.</span><span class="sxs-lookup"><span data-stu-id="5309b-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="5309b-112">Varamõõdkute registreerimist saab mõõtmise registreerimist saab uuendada käsitsi või automaatselt vastavalt tootmistundidele või toodetud kogusele.</span><span class="sxs-lookup"><span data-stu-id="5309b-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="5309b-113">Varamõõdikut saab seadistada kasutama ühte kolmest uuendusmeetodist (valitud üksuse **Loendurid** väljal **Uuendamine**):</span><span class="sxs-lookup"><span data-stu-id="5309b-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="5309b-114">Käsitsi – peate varamõõdikute väärtused käsitsi registreerima.</span><span class="sxs-lookup"><span data-stu-id="5309b-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="5309b-115">Tootmistunnid – loendur uuendatakse automaatselt tootmistundide arvu põhjal.</span><span class="sxs-lookup"><span data-stu-id="5309b-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="5309b-116">Tootmiskogus – loendur uuendatakse automaatselt toodetud koguse põhjal.</span><span class="sxs-lookup"><span data-stu-id="5309b-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="5309b-117">Toodetud koguse kasutamisel kaasatakse *kõik* registreeritud kaubad mõõdikute registreeringusse – nii õiged kui ka vealised kogused.</span><span class="sxs-lookup"><span data-stu-id="5309b-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="5309b-118">Vajadusel on alati võimalik teha varamõõdikute käsitsi registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="5309b-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="5309b-119">Loenduritüüpie loomine varaloenduri registreeringuteks</span><span class="sxs-lookup"><span data-stu-id="5309b-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="5309b-120">Valige **Varahaldu** > **Seadistus** > **Vara tüübid** > **Loendurid**.</span><span class="sxs-lookup"><span data-stu-id="5309b-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="5309b-121">Valige uue varamõõdiku tüübi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5309b-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="5309b-122">Sisestage ID väljale **Loendur** ja loenduri nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="5309b-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="5309b-123">Valige kiirkaardil **Üldine** mõõtühik väljal **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="5309b-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="5309b-124">Valige väljal **Uuuendmine** varamõõdiku jaoks kasutatv uuendusmeetod.</span><span class="sxs-lookup"><span data-stu-id="5309b-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="5309b-125">Valige „Jah” tumblernupul **Päri loenduri väärtused**, kui varastruktuuris olevad alamvarad peaksid automaatselt pärima emaettevõtte varades tehtud mõõdikute registreeringud.</span><span class="sxs-lookup"><span data-stu-id="5309b-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="5309b-126">Valige väljal **Kogusumma** summeerimismeetod seda varamõõdiku tüüpi kasutava varamõõdiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="5309b-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="5309b-127">„Summa” on sandardne valik, mida kasutatakse registreeritud väärtuste pidevalks lisamiseks koguväärtusele.</span><span class="sxs-lookup"><span data-stu-id="5309b-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="5309b-128">Väärtust „Keskmine” võib kasutada, kui varamõõdik on seadistatud jälgima läve (nt vara temperatuur, vibratsioon või kulumine).</span><span class="sxs-lookup"><span data-stu-id="5309b-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="5309b-129">Väljale **Hälve üle** sisestage ülemine tase protsentides, et valideerida, kas varamõõdiku käsitsi registreerimine on eeldatud vahemikus.</span><span class="sxs-lookup"><span data-stu-id="5309b-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="5309b-130">Valideerimine põhineb olemasolevate varamõõdikute registreeringute lineaarsel suurenemisel.</span><span class="sxs-lookup"><span data-stu-id="5309b-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="5309b-131">Väljale **Hälve allpool** sisestage alumine tase protsentides, et valideerida, kas varamõõdiku käsitsi registreerimine on eeldatud vahemikus.</span><span class="sxs-lookup"><span data-stu-id="5309b-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="5309b-132">Valideerimine põhineb olemasolevate varamõõdikute registreeringute lineaarsel vähenemisel.</span><span class="sxs-lookup"><span data-stu-id="5309b-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="5309b-133">Väljal **Tüüp** valige teate tüüp (teave, hoiatus, tõrge), mis kuvatakse, kui ilmnevad hälbed väljaspool määratletud vahemikku, kui registreerite varamõõdikut käsitsi.</span><span class="sxs-lookup"><span data-stu-id="5309b-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="5309b-134">Lisage kiirkaardil **Varade tüübid** varade tüübid, mis peaksid olema võimelised kasutama varamõõdikut.</span><span class="sxs-lookup"><span data-stu-id="5309b-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="5309b-135">Lisage kiirkaardil **Seotud varamõõdikud** need varamõõdikud, mida soovite selle varamõõdiku uuendamisel automaatselt uuendada.</span><span class="sxs-lookup"><span data-stu-id="5309b-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="5309b-136">Seotud varamõõdik uuendatakse automaatselt ainult juhul, kui seotud varamõõdikul on vara tüüp, millega see on seotud varamõõdiku seadistamisel.</span><span class="sxs-lookup"><span data-stu-id="5309b-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="5309b-137">Näiteks: seadistate varamõõdiku „tootmistundidele” ja lisate varatüübi „Veoauto mootor”.</span><span class="sxs-lookup"><span data-stu-id="5309b-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="5309b-138">Kui seda varamõõdikut uuendatakse, uuendatakse ka seotud loendur „Õli" sama varamõõdiku väärtustega.</span><span class="sxs-lookup"><span data-stu-id="5309b-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="5309b-139">Välja **Loenurid** seaditus sisaldab välja „Tunnid” seadistust.</span><span class="sxs-lookup"><span data-stu-id="5309b-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="5309b-140">Varamõõdiku seose tagamisekes tuleb ka varamõõdikus „Õli” lisada varatüüp „Veoauto mootor” kiirkaardile **Varade tüübid**.</span><span class="sxs-lookup"><span data-stu-id="5309b-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="5309b-141">Vaadake allolevatelt kuvatõmmistelt näidet tundide ja õli varamõõdiku seadistamise kohta.</span><span class="sxs-lookup"><span data-stu-id="5309b-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="5309b-142">Kui väljale **Loendurid** on varade tüübid lisatud varamõõdiku tüübile, siis lisatakse see varamõõdik automaatselt varade tüüpidele kiirkaardil **Loendurid** üksuses [Varade tüübid](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="5309b-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Joonis 1](media/071-setup-for-objects.png)


