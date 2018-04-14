--- 
title: Kohustuste jagamise seadistamine
description: "Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad."
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ea94570ca23761195ed93bbab6c51f5df02c28bb
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="18498-103">Kohustuste jagamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="18498-103">Set up segregation of duties</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18498-104">Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="18498-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="18498-105">Seda põhimõtet nimetatakse kohustuste jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="18498-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="18498-106">Näiteks ei soovi te võib-olla, et sama isik kinnitab kaupade kättesaamise ja töötleb hankijale tehtavat makset.</span><span class="sxs-lookup"><span data-stu-id="18498-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="18498-107">Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi.</span><span class="sxs-lookup"><span data-stu-id="18498-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="18498-108">Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="18498-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="18498-109">Reegli loomiseks järgige järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="18498-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="18498-110">Protseduuri lõpuleviimiseks peate olema süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="18498-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="18498-111">Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid.</span><span class="sxs-lookup"><span data-stu-id="18498-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="18498-112">Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kohustuste jagamise reeglid.</span><span class="sxs-lookup"><span data-stu-id="18498-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="18498-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="18498-113">Click New.</span></span>
3. <span data-ttu-id="18498-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="18498-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="18498-115">Sisestage reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="18498-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="18498-116">Klõpsake väljal Esimene kohustus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="18498-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="18498-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="18498-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18498-118">Valige esimene kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="18498-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="18498-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="18498-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="18498-120">Klõpsake väljal Teine kohustus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="18498-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="18498-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="18498-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18498-122">Valige teine kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="18498-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="18498-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="18498-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="18498-124">Valige suvand väljal Olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="18498-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="18498-125">Valige riski, mis tekib, kui sama kasutaja või roll täidab mõlemat kohustust, olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="18498-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="18498-126">Sisestage väärtus väljale Turberisk.</span><span class="sxs-lookup"><span data-stu-id="18498-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="18498-127">Sisestage turberiski kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="18498-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="18498-128">Sisestage väärtus väljale Turbe vähendamine.</span><span class="sxs-lookup"><span data-stu-id="18498-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="18498-129">Sisestage turberiski vähendamiseks kasutatavate tegevuste kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="18498-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="18498-130">Näiteks saate riski vähendamiseks teha protsessi kohta üksikasjalikumaid ülevaateid, teha igakuise juhtiva ülevaatuse või jagada ressursse teiste osakondadega.</span><span class="sxs-lookup"><span data-stu-id="18498-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="18498-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="18498-131">Click Save.</span></span>


