---
title: Kohustuste jagamise seadistamine
description: Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68e1a4419eaa11a59e1b634deb8e76a2bb9b6fdf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "318783"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="5eb68-103">Kohustuste jagamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="5eb68-103">Set up segregation of duties</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5eb68-104">Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="5eb68-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="5eb68-105">Seda põhimõtet nimetatakse kohustuste jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="5eb68-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="5eb68-106">Näiteks ei soovi te võib-olla, et sama isik kinnitab kaupade kättesaamise ja töötleb hankijale tehtavat makset.</span><span class="sxs-lookup"><span data-stu-id="5eb68-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="5eb68-107">Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi.</span><span class="sxs-lookup"><span data-stu-id="5eb68-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="5eb68-108">Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="5eb68-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="5eb68-109">Reegli loomiseks järgige järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="5eb68-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="5eb68-110">Protseduuri lõpuleviimiseks peate olema süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="5eb68-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="5eb68-111">Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid.</span><span class="sxs-lookup"><span data-stu-id="5eb68-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="5eb68-112">Avage Süsteemihaldus > Turve > Kohustuste jagamine > Kohustuste jagamise reeglid.</span><span class="sxs-lookup"><span data-stu-id="5eb68-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="5eb68-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5eb68-113">Click New.</span></span>
3. <span data-ttu-id="5eb68-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="5eb68-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="5eb68-115">Sisestage reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="5eb68-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="5eb68-116">Klõpsake väljal Esimene kohustus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5eb68-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="5eb68-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5eb68-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5eb68-118">Valige esimene kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="5eb68-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="5eb68-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5eb68-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5eb68-120">Klõpsake väljal Teine kohustus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5eb68-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5eb68-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5eb68-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5eb68-122">Valige teine kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="5eb68-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="5eb68-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5eb68-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="5eb68-124">Valige suvand väljal Olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="5eb68-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="5eb68-125">Valige riski, mis tekib, kui sama kasutaja või roll täidab mõlemat kohustust, olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="5eb68-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="5eb68-126">Sisestage väärtus väljale Turberisk.</span><span class="sxs-lookup"><span data-stu-id="5eb68-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="5eb68-127">Sisestage turberiski kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="5eb68-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="5eb68-128">Sisestage väärtus väljale Turbe vähendamine.</span><span class="sxs-lookup"><span data-stu-id="5eb68-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="5eb68-129">Sisestage turberiski vähendamiseks kasutatavate tegevuste kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="5eb68-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="5eb68-130">Näiteks saate riski vähendamiseks teha protsessi kohta üksikasjalikumaid ülevaateid, teha igakuise juhtiva ülevaatuse või jagada ressursse teiste osakondadega.</span><span class="sxs-lookup"><span data-stu-id="5eb68-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="5eb68-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5eb68-131">Click Save.</span></span>

