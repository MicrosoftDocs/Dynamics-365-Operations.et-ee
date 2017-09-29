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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="3d668-103">Kohustuste jagamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="3d668-103">Set up segregation of duties</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d668-104">Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="3d668-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="3d668-105">Seda põhimõtet nimetatakse kohustuste jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="3d668-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="3d668-106">Näiteks ei soovi te võib-olla, et sama isik kinnitab kaupade kättesaamise ja töötleb hankijale tehtavat makset.</span><span class="sxs-lookup"><span data-stu-id="3d668-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="3d668-107">Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi.</span><span class="sxs-lookup"><span data-stu-id="3d668-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="3d668-108">Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="3d668-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="3d668-109">Reegli loomiseks järgige järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="3d668-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="3d668-110">Protseduuri lõpuleviimiseks peate olema süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="3d668-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="3d668-111">Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid.</span><span class="sxs-lookup"><span data-stu-id="3d668-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="3d668-112">Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kohustuste jagamise reeglid.</span><span class="sxs-lookup"><span data-stu-id="3d668-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="3d668-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3d668-113">Click New.</span></span>
3. <span data-ttu-id="3d668-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="3d668-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="3d668-115">Sisestage reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="3d668-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="3d668-116">Klõpsake väljal Esimene kohustus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3d668-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3d668-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="3d668-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3d668-118">Valige esimene kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="3d668-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="3d668-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3d668-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="3d668-120">Klõpsake väljal Teine kohustus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3d668-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3d668-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="3d668-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3d668-122">Valige teine kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="3d668-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="3d668-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3d668-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="3d668-124">Valige suvand väljal Olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="3d668-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="3d668-125">Valige riski, mis tekib, kui sama kasutaja või roll täidab mõlemat kohustust, olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="3d668-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="3d668-126">Sisestage väärtus väljale Turberisk.</span><span class="sxs-lookup"><span data-stu-id="3d668-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="3d668-127">Sisestage turberiski kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3d668-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="3d668-128">Sisestage väärtus väljale Turbe vähendamine.</span><span class="sxs-lookup"><span data-stu-id="3d668-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="3d668-129">Sisestage turberiski vähendamiseks kasutatavate tegevuste kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3d668-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="3d668-130">Näiteks saate riski vähendamiseks teha protsessi kohta üksikasjalikumaid ülevaateid, teha igakuise juhtiva ülevaatuse või jagada ressursse teiste osakondadega.</span><span class="sxs-lookup"><span data-stu-id="3d668-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="3d668-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3d668-131">Click Save.</span></span>


