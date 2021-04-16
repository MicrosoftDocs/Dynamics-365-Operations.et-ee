---
title: Power Portali kasutamine osapoole andmemudeliga
description: See teema kirjeldab muudatusi Power Portali veebirollides osapoole andmemudeli topeltkirjutuse tõttu.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833086"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="0ace1-103">Power Portali kasutamine osapoole andmemudeliga</span><span class="sxs-lookup"><span data-stu-id="0ace1-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0ace1-104">Topeltkirjutusega rakenduse orkestratsioonilahenduse versioon 2.0.999.0 ja uuem sisaldab andmemudeli muudatusi osapoole ja globaalse aadressiraamatu konto- ja kontaktitabelite kohta.</span><span class="sxs-lookup"><span data-stu-id="0ace1-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="0ace1-105">Muudatused võimaldavad mitu-mitmele-seoseid, mis toetavad laiendatud äristsenaariume.</span><span class="sxs-lookup"><span data-stu-id="0ace1-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="0ace1-106">Neid muudatusi ei toeta portaali veebirollid, sealhulgas kliendiportaal, mis on tarnitud valmislahendustena või mis oli teie keskkonnas olemas enne topeltkirjutuse installimist.</span><span class="sxs-lookup"><span data-stu-id="0ace1-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="0ace1-107">Selleks, et veebirollid töötaks nii nagu oodatud, peate looma uued veebirollid, kasutades uut andmemudelit.</span><span class="sxs-lookup"><span data-stu-id="0ace1-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="0ace1-108">Kokkuvõttes on tabelite omavaheline suhtlus muutunud, kuid tabeliõigused kliendiportaalis pole muutunud.</span><span class="sxs-lookup"><span data-stu-id="0ace1-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="0ace1-109">See teema kirjeldab, kuidas luua uusi veebirolle, mis töötavad uue täiustatud andmemudeliga.</span><span class="sxs-lookup"><span data-stu-id="0ace1-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="0ace1-110">Diagramm näitab tabeliseost **ilma** osapooleta ja globaalse aadressiraamatu andmemudelita.</span><span class="sxs-lookup"><span data-stu-id="0ace1-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![osapoolemudelita](media/without-party-model.PNG)

<span data-ttu-id="0ace1-112">Diagramm näitab tabeliseost **koos** osapoole ja globaalse aadressiraamatu andmemudeliga.</span><span class="sxs-lookup"><span data-stu-id="0ace1-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![osapoolemudeliga](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="0ace1-114">Loo uue tabeli luba</span><span class="sxs-lookup"><span data-stu-id="0ace1-114">Create a new table permission</span></span>

<span data-ttu-id="0ace1-115">Nende uute tabeli lubade loomiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="0ace1-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="0ace1-116">Logige sisse [Power Apps](https://make.powerapps.com) ja minge oma rakendustesse.</span><span class="sxs-lookup"><span data-stu-id="0ace1-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="0ace1-117">Valige oma portaalihalduse rakendus.</span><span class="sxs-lookup"><span data-stu-id="0ace1-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="0ace1-118">Valige külgribal **Turvalisuse > Tabeliõigused**.</span><span class="sxs-lookup"><span data-stu-id="0ace1-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="0ace1-119">Peate looma kolm uut luba.</span><span class="sxs-lookup"><span data-stu-id="0ace1-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="0ace1-120">Ühenduse loomine Osapoolega</span><span class="sxs-lookup"><span data-stu-id="0ace1-120">Contact to Party connection</span></span>
    + <span data-ttu-id="0ace1-121">Ühenduse loomine Osapoole ja Konto vahel</span><span class="sxs-lookup"><span data-stu-id="0ace1-121">Party to Account connection</span></span>
    + <span data-ttu-id="0ace1-122">Ühenduse loomine Konto ja Tellimuse vahel</span><span class="sxs-lookup"><span data-stu-id="0ace1-122">Account to Order connection</span></span>

4. <span data-ttu-id="0ace1-123">Looge ja salvestage luba Kontakti ja Osapoole vahel ühenduse loomiseks, häälestades need parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0ace1-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="0ace1-124">**Nimi**: ühenduse loomine Osapoole ja Konto vahel (või teie valik)</span><span class="sxs-lookup"><span data-stu-id="0ace1-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="0ace1-125">**Tabeli nimi**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="0ace1-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="0ace1-126">**Veebisait**: kliendiportaal</span><span class="sxs-lookup"><span data-stu-id="0ace1-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="0ace1-127">**Ulatus**: Kontakt</span><span class="sxs-lookup"><span data-stu-id="0ace1-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="0ace1-128">**Privileegid**: vali kõik</span><span class="sxs-lookup"><span data-stu-id="0ace1-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="0ace1-129">**Veebirollid**: autenditud kasutajad, kliendi esindaja (või teie valik)</span><span class="sxs-lookup"><span data-stu-id="0ace1-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="0ace1-130">Looge ja salvestage luba Osapoole ja Konto vahel ühenduse loomiseks, häälestades need parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0ace1-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="0ace1-131">**Nimi**: ühenduse loomine Osapoole ja Konto vahel (või teie valik)</span><span class="sxs-lookup"><span data-stu-id="0ace1-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="0ace1-132">**Tabeli nimi**: konto</span><span class="sxs-lookup"><span data-stu-id="0ace1-132">**Table Name**: account</span></span>
    + <span data-ttu-id="0ace1-133">**Veebisait**: kliendiportaal</span><span class="sxs-lookup"><span data-stu-id="0ace1-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="0ace1-134">**Ulatus**: vanem</span><span class="sxs-lookup"><span data-stu-id="0ace1-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="0ace1-135">**Privileegid**: vali kõik</span><span class="sxs-lookup"><span data-stu-id="0ace1-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="0ace1-136">**Ematabeli luba**: ühendus Konto ja Osapoole vahel</span><span class="sxs-lookup"><span data-stu-id="0ace1-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="0ace1-137">Looge ja salvestage luba Konto ja Tellimuse vahel ühenduse loomiseks, häälestades need parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0ace1-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="0ace1-138">**Nimi**: ühenduse loomine Konto ja Tellimuse vahel (või teie valik)</span><span class="sxs-lookup"><span data-stu-id="0ace1-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="0ace1-139">**Tabeli nimi**: müügitellimus</span><span class="sxs-lookup"><span data-stu-id="0ace1-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="0ace1-140">**Veebisait**: kliendiportaal</span><span class="sxs-lookup"><span data-stu-id="0ace1-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="0ace1-141">**Ulatus**: vanem</span><span class="sxs-lookup"><span data-stu-id="0ace1-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="0ace1-142">**Privileegid**: vali kõik</span><span class="sxs-lookup"><span data-stu-id="0ace1-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="0ace1-143">**Ematabeli luba**: ühendus Osapoole ja Konto vahel</span><span class="sxs-lookup"><span data-stu-id="0ace1-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
