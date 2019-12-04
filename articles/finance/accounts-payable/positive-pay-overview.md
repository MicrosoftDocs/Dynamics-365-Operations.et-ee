---
title: Positiivse makse ülevaade
description: See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49fe8369fce599d16134541b1c968727f38ebff9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189633"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="3f424-103">Positiivse makse ülevaade</span><span class="sxs-lookup"><span data-stu-id="3f424-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f424-104">See artikkel sisaldab teavet positiivse makse kohta, mida kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="3f424-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="3f424-105">Positiivset makset kasutatakse pangale edastatava elektroonilise tšekkide loendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="3f424-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="3f424-106">Positiivsete maksete failid aitavad pankadel tšekipettusi vältida.</span><span class="sxs-lookup"><span data-stu-id="3f424-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="3f424-107">Saate seadistada positiivse makse elektroonilise tšekkide loendi koostamiseks iga kord, kui tšekke prinditakse.</span><span class="sxs-lookup"><span data-stu-id="3f424-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="3f424-108">Tšeki esitamisel pangale võrdleb pank seda siis eelnevalt esitatud tšekkide loendiga.</span><span class="sxs-lookup"><span data-stu-id="3f424-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="3f424-109">Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja.</span><span class="sxs-lookup"><span data-stu-id="3f424-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="3f424-110">Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.</span><span class="sxs-lookup"><span data-stu-id="3f424-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="3f424-111">Positiivse makse teine nimetus on SafePay.</span><span class="sxs-lookup"><span data-stu-id="3f424-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="3f424-112">Positiivse makse failides võib olla tundliku loomuga teavet maksesaajate ja tšekisummade kohta.</span><span class="sxs-lookup"><span data-stu-id="3f424-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="3f424-113">Seetõttu kasutage kindlasti vajalikke turvameetmeid alates failide loomise hetkest kuni nende panka saabumiseni.</span><span class="sxs-lookup"><span data-stu-id="3f424-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="3f424-114">Positiivsete maksete failid laaditakse alla veebibrauseri allalaadimisjuhiste kohaselt.</span><span class="sxs-lookup"><span data-stu-id="3f424-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="3f424-115">Positiivse makse failid luuakse andmeüksuste abil.</span><span class="sxs-lookup"><span data-stu-id="3f424-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="3f424-116">Enne positiivsete maksete faili koostamist tuleb seadistada XML-i jaoks teisendusvormingud, mis teisendavad andmed pangale sobivasse vormingusse.</span><span class="sxs-lookup"><span data-stu-id="3f424-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="3f424-117">Iga pangakonto puhul, millele soovite positiivset makseteavet luua, tuleb määrata positiivse makse vorming.</span><span class="sxs-lookup"><span data-stu-id="3f424-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="3f424-118">Pärast maksete loomist saate luua positiivse maksefaili üksikule juriidilisele isikule ja üksikule pangakontole.</span><span class="sxs-lookup"><span data-stu-id="3f424-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="3f424-119">Teine võimalus on positiivsete maksete failide loomine juriidiliste isikute ja pangakontode jaoks üheaegselt.</span><span class="sxs-lookup"><span data-stu-id="3f424-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="3f424-120">Kui positiivses maksefailis loetletud tšekid on tasutud, saate pangast kinnituskoodi.</span><span class="sxs-lookup"><span data-stu-id="3f424-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="3f424-121">Seejärel saate süsteemis kinnitada positiivse maksefaili.</span><span class="sxs-lookup"><span data-stu-id="3f424-121">You can then confirm the positive pay file in the system.</span></span> 

<span data-ttu-id="3f424-122">Kui peate positiivse makse faili muutma, saate selle tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="3f424-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="3f424-123">Siis lähtestatakse igas positiivse makse failis oleva tšeki puhul väli, mis näitab, kas see tšekk on olnud positiivse makse faili lisatud.</span><span class="sxs-lookup"><span data-stu-id="3f424-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="3f424-124">Lisateavet vt jaotisest [Positiivse makse failide seadistamine ja loomine](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="3f424-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>


