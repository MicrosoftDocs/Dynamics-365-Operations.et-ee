---
title: Kohustuste jagamise seadistamine
description: Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 712cc90bef4f3ad56291e99edd9f963ae88add48
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143508"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="c7c63-103">Kohustuste jagamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="c7c63-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c7c63-104">Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="c7c63-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="c7c63-105">Seda põhimõtet nimetatakse kohustuste jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7c63-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="c7c63-106">Näiteks ei soovi te võib-olla, et sama isik kinnitab kaupade kättesaamise ja töötleb hankijale tehtavat makset.</span><span class="sxs-lookup"><span data-stu-id="c7c63-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="c7c63-107">Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi.</span><span class="sxs-lookup"><span data-stu-id="c7c63-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="c7c63-108">Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="c7c63-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="c7c63-109">Reegli loomiseks järgige järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="c7c63-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="c7c63-110">Protseduuri lõpuleviimiseks peate olema süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="c7c63-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="c7c63-111">Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid.</span><span class="sxs-lookup"><span data-stu-id="c7c63-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="c7c63-112">Avage **Navigeerimispaan > Moodulid > Süsteemiadministratsioon > Turvalisus > Kohustuste jagamine > Kohustuste reeglite jagamine**.</span><span class="sxs-lookup"><span data-stu-id="c7c63-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="c7c63-113">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c7c63-113">Click **New**.</span></span>
3. <span data-ttu-id="c7c63-114">Tippige reegli väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c7c63-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="c7c63-115">Väljal **Esimene kohustus**, klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c7c63-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c7c63-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c7c63-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="c7c63-117">Valige esimene kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="c7c63-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="c7c63-118">Väljal **Teine kohustus**, klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c7c63-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="c7c63-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c7c63-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="c7c63-120">Valige teine kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="c7c63-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="c7c63-121">Valige suvand väljal **Olulisusaste**.</span><span class="sxs-lookup"><span data-stu-id="c7c63-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="c7c63-122">Valige riski, mis tekib, kui sama kasutaja või roll täidab mõlemat kohustust, olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="c7c63-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="c7c63-123">Sisestage väärtus väljale **Turberisk**.</span><span class="sxs-lookup"><span data-stu-id="c7c63-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="c7c63-124">Sisestage turberiski kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c7c63-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="c7c63-125">Sisestage väärtus väljale **Turberiski vähendamine**.</span><span class="sxs-lookup"><span data-stu-id="c7c63-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="c7c63-126">Sisestage turberiski vähendamiseks kasutatavate tegevuste kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c7c63-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="c7c63-127">Näiteks saate riski vähendamiseks teha protsessi kohta üksikasjalikumaid ülevaateid, teha igakuise juhtiva ülevaatuse või jagada ressursse teiste osakondadega.</span><span class="sxs-lookup"><span data-stu-id="c7c63-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="c7c63-128">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c7c63-128">Click **Save**.</span></span>

