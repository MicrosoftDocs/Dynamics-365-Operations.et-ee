---
title: Asukoha ja osapoole seosetüüpide lisamine
description: Selles teemas kirjeldatakse uue asukoha ja osapoole seosetüübi loomist.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-05-02
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8c359c5c33bed5b5abe7fc0c8e362c3399e9051a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177398"
---
# <a name="add-location-roles-and-party-relationship-types"></a><span data-ttu-id="51b63-103">Asukoharollide ja osapoole seosetüüpide lisamine</span><span class="sxs-lookup"><span data-stu-id="51b63-103">Add location roles and party relationship types</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="add-location-roles"></a><span data-ttu-id="51b63-104">Asukoharollide lisamine</span><span class="sxs-lookup"><span data-stu-id="51b63-104">Add location roles</span></span>

<span data-ttu-id="51b63-105">Aadressile ja kontaktteabele uute asukoharollide lisamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="51b63-105">There are two ways to add a new location roles for address and contact information:</span></span>

-  <span data-ttu-id="51b63-106">Lisamine lehelt **Aadressi ja kontaktteabe eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="51b63-106">Add it through the **Address and contact information purpose** page.</span></span> <span data-ttu-id="51b63-107">Uus roll salvestatakse tabelisse **LogisticsLocationRole** tüübiga 0, mis näitab, et roll pole loetelus **LogisticsLocationRoleType** määratletud süsteemiroll.</span><span class="sxs-lookup"><span data-stu-id="51b63-107">The new role will be saved to the **LogisticsLocationRole** table with type = 0, which indicates that the role is not a system role defined in the **LogisticsLocationRoleType** enum and its extensions.</span></span> <span data-ttu-id="51b63-108">Kasutaja saab seda rolli kasutada aadressi või kontaktteabe loomisel.</span><span class="sxs-lookup"><span data-stu-id="51b63-108">A user will be able to use this role when creating address or contact information.</span></span>

    ![Aadressi ja kontaktteabe eesmärk](media/Address-Contact.PNG)

-  <span data-ttu-id="51b63-110">Saate lisada selle loetelu **LogisticsLocationRoleType** laiendisse ja lasta selle asustada andmebaasi sünkroonimisprotsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="51b63-110">Add it to the **LogisticsLocationRoleType** enum extension, and let it populate through the database sync process.</span></span>

    1.  <span data-ttu-id="51b63-111">Looge loetelule **LogisticsLocationRoleType** laiend ja lisage laiendis uus roll.</span><span class="sxs-lookup"><span data-stu-id="51b63-111">Create an extension to the **LogisticsLocationRoleType** enum and add the new role in the extension.</span></span> 
  
        ![LogisticsLocationRoleType](media/Logistics.PNG)

    2. <span data-ttu-id="51b63-113">Saate luua uuele rollile uue ressursifaili ja seejärel määrata selle atribuutidele väärtuse.</span><span class="sxs-lookup"><span data-stu-id="51b63-113">Create a new resource file for the new role, and then assign a value for its properties.</span></span>
     
     ![Uus ressursifail](media/Resource.PNG)
        
    3.  <span data-ttu-id="51b63-115">Saate luua andmete asustamise klassi ja esitada ohjemeetodi uue rolli asustamiseks.</span><span class="sxs-lookup"><span data-stu-id="51b63-115">Create a data population class and provide a handler method to populate the new role.</span></span> 

        ![Andmete asustamine](media/Dirdata.PNG)

    4.  <span data-ttu-id="51b63-117">Uue asukoharolli katseasustamiseks saate luua käitatava klassi ja kutsuda atribuudi DirDataPopulation::insertLogisticsLocationRoles() asukohas Main().</span><span class="sxs-lookup"><span data-stu-id="51b63-117">To test populating the new location role, you can create a runnable class, and call DirDataPopulation::insertLogisticsLocationRoles() in Main().</span></span> <span data-ttu-id="51b63-118">Kui see protsess on lõpule jõudnud, peaksite nägema uut rolli tabelis **LogisticsLocationRole** tüübiga \> 0.</span><span class="sxs-lookup"><span data-stu-id="51b63-118">After this process is complete, you should see the new role populated in the **LogisticsLocationRole** table with type \> 0.</span></span> <span data-ttu-id="51b63-119">Uus roll kuvatakse lehel **Aadressi ja kontaktteabe eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="51b63-119">The new role will display on the **Address and contact information purpose** page.</span></span>

        ![Uue asukoha sisestamine](media/InsertNewLocation.PNG)

## <a name="add-party-relationship-types"></a><span data-ttu-id="51b63-121">Osapoole seosetüüpide lisamine</span><span class="sxs-lookup"><span data-stu-id="51b63-121">Add party relationship types</span></span> 

<span data-ttu-id="51b63-122">Uue seosetüübi lisamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="51b63-122">There are two ways to add a new relationship type:</span></span>

-   <span data-ttu-id="51b63-123">Lisamine lehe **Seosetüübid** kaudu.</span><span class="sxs-lookup"><span data-stu-id="51b63-123">Add it through the **Relationship types** page.</span></span> <span data-ttu-id="51b63-124">Uus seos salvestatakse tabelisse **DirRelationshipTypeTable**, systemtype = 0.</span><span class="sxs-lookup"><span data-stu-id="51b63-124">The new relationship will be saved to **DirRelationshipTypeTable** with systemtype = 0.</span></span>

    ![Seosetüübid](media/Relationship.PNG)

-  <span data-ttu-id="51b63-126">Saate lisada selle loetelu **DirSystemRelationshipType** laiendisse ja lasta selle asustada andmebaasi sünkroonimisprotsessi kaudu.</span><span class="sxs-lookup"><span data-stu-id="51b63-126">Add it to the extension of the **DirSystemRelationshipType** enum, and let it populate through database sync process.</span></span>

    1.  <span data-ttu-id="51b63-127">Looge loetelule **DirSystemRelationshipType** laiend ja lisage uus seosetüüp.</span><span class="sxs-lookup"><span data-stu-id="51b63-127">Create an extension to the **DirSystemRelationshipType** enum and add the new relationship type.</span></span>

    2. <span data-ttu-id="51b63-128">Looge uuele tüübile lähtestaja.</span><span class="sxs-lookup"><span data-stu-id="51b63-128">Create an initializer for this new type.</span></span> <span data-ttu-id="51b63-129">Mitu näidet leiate põhikoodist, üks neist on **DirRelationshipTypeChildInitialize**.</span><span class="sxs-lookup"><span data-stu-id="51b63-129">You can find several examples in the core code, one of them is  **DirRelationshipTypeChildInitialize**.</span></span> <span data-ttu-id="51b63-130">See on osapoole seosetüübi Tütar lähtestajaklass.</span><span class="sxs-lookup"><span data-stu-id="51b63-130">This is an initializer class for party relationship type “Child”.</span></span> <span data-ttu-id="51b63-131">Saate alustada oma lähtestajaga, kopeerides ja kleepides selle koodi ning seejärel värskendades esiletõstetud alasid.</span><span class="sxs-lookup"><span data-stu-id="51b63-131">You can start with your initializer by copying and pasting this code and then update the highlighted areas.</span></span>
    
    ![DirRelationshipChild](media/DirRelationship.PNG)

    3.  <span data-ttu-id="51b63-133">Uue seosetüübi katseasustamiseks saate luua käitatava klassi ja kutsuda atribuudi DirDataPopulation::insertDirRelationshipTypes() asukohas Main().</span><span class="sxs-lookup"><span data-stu-id="51b63-133">To test populating the new relationship type, you can create a runnable class, and call DirDataPopulation::insertDirRelationshipTypes() in Main().</span></span> <span data-ttu-id="51b63-134">Peaksite uut seosetüüpi nägema tabelis **DirRelationshipTypeTable** ja uus seosetüüp on saadaval lehel **Seosetüübid**.</span><span class="sxs-lookup"><span data-stu-id="51b63-134">You should see the new relationship type in the **DirRelationshipTypeTable**, and the new relationship type will be available on the **Relationship types** page.</span></span>

        ![Käitatav klass](media/Runnable.PNG)
