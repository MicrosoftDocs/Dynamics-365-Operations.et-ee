---
title: "Positiivse makse ülevaade"
description: "See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5b88b940e7a590ff99b6ab8a99ce45d32dfe0505
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="positive-pay-overview"></a><span data-ttu-id="ad3bf-103">Positiivse makse ülevaade</span><span class="sxs-lookup"><span data-stu-id="ad3bf-103">Positive pay overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ad3bf-104">See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="ad3bf-105">Positiivset makset kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="ad3bf-106">Positiivsete maksete failid aitavad pankadel tšekipettusi vältida.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="ad3bf-107">Saate seadistada positiivse makse elektroonilise tšekkide loendi koostamiseks iga kord, kui tšekke prinditakse.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="ad3bf-108">Tšeki esitamisel pangale võrdleb pank seda siis eelnevalt esitatud tšekkide loendiga.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="ad3bf-109">Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="ad3bf-110">Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="ad3bf-111">Positiivse makse teine nimetus on SafePay.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="ad3bf-112">Positiivse makse failides võib olla tundliku loomuga teavet maksesaajate ja tšekisummade kohta.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="ad3bf-113">Seetõttu kasutage kindlasti vajalikke turvameetmeid alates failide loomise hetkest kuni nende panka saabumiseni.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="ad3bf-114">Positiivsete maksete failid laaditakse alla veebibrauseri allalaadimisjuhiste kohaselt.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="ad3bf-115">Positiivse makse failid luuakse andmeüksuste abil.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="ad3bf-116">Enne positiivsete maksete faili koostamist tuleb seadistada XML-i jaoks teisendusvormingud, mis teisendavad andmed pangale sobivasse vormingusse.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="ad3bf-117">Iga pangakonto puhul, millele soovite positiivset makseteavet luua, tuleb määrata positiivse makse vorming.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="ad3bf-118">Pärast maksete loomist saate luua positiivse maksefaili üksikule juriidilisele isikule ja üksikule pangakontole.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="ad3bf-119">Teine võimalus on positiivsete maksete failide loomine juriidiliste isikute ja pangakontode jaoks üheaegselt.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="ad3bf-120">Kui positiivses maksefailis loetletud tšekid on tasutud, saate pangast kinnituskoodi.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="ad3bf-121">Seejärel saate positiivse makse faili Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis kinnitada.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-121">You can then confirm the positive pay file in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="ad3bf-122">Kui peate positiivse makse faili muutma, saate selle tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="ad3bf-123">Siis lähtestatakse igas positiivse makse failis oleva tšeki puhul väli, mis näitab, kas see tšekk on olnud positiivse makse faili lisatud.</span><span class="sxs-lookup"><span data-stu-id="ad3bf-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="ad3bf-124">Lisateavet vt jaotisest [Positiivse makse failide seadistamine ja loomine](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="ad3bf-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>




