---
title: Kohustuste jagamise seadistamine
description: Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745737"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="b5d7e-103">Kohustuste jagamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="b5d7e-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b5d7e-104">Saate seadistada reeglid nende ülesannete eraldamiseks, mille peavad täitma erinevad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="b5d7e-105">Seda põhimõtet nimetatakse kohustuste jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="b5d7e-106">Näiteks ei soovi te võib-olla, et sama isik kinnitaks kaupade kättesaamise ja töötleks hankijale tehtavat makset.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="b5d7e-107">Kohustuste jagamine aitab vähendada pettuseriski ja tuvastada vigu või ebaregulaarsusi.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="b5d7e-108">Samuti saate kohustuste jagamise abil jõustada sisekontrollipoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="b5d7e-109">Reegli loomiseks järgige järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="b5d7e-110">Protseduuri lõpuleviimiseks peate olema süsteemiadministraator.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="b5d7e-111">Avage **Süsteemihaldus** > **Turve** > **Kohustuste jagamine** > **Kohustuste jagamise reeglid**.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="b5d7e-112">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-112">Click **New**.</span></span>
3. <span data-ttu-id="b5d7e-113">Tippige reegli väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="b5d7e-114">Väljal **Esimene kohustus**, klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b5d7e-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="b5d7e-116">Valige esimene kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="b5d7e-117">Väljal **Teine kohustus**, klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="b5d7e-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="b5d7e-119">Valige teine kohustus, mida juhitakse reegliga.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="b5d7e-120">Valige suvand väljal **Olulisusaste**.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="b5d7e-121">Valige riski, mis tekib, kui sama kasutaja või roll täidab mõlemat kohustust, olulisusaste.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="b5d7e-122">Sisestage väärtus väljale **Turberisk**.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="b5d7e-123">Sisestage turberiski kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="b5d7e-124">Sisestage väärtus väljale **Turberiski vähendamine**.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="b5d7e-125">Sisestage turberiski vähendamiseks kasutatavate tegevuste kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="b5d7e-126">Näiteks saate riski vähendamiseks teha protsessi kohta üksikasjalikumaid ülevaateid, teha igakuise juhtiva ülevaatuse või jagada ressursse teiste osakondadega.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="b5d7e-127">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="b5d7e-128">Kohustuste jagamise reeglite järgimist ei kontrollita, kui loote reegli.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="b5d7e-129">Saate luua reegli, mis loob olemasolevatele rollidele vastuolu.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="b5d7e-130">Olemasolevad kasutajarolli määramised võivad olla vastuolus ka uue reegliga.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="b5d7e-131">Vastavust peate kontrollima pärast reegli loomist või muutmist.</span><span class="sxs-lookup"><span data-stu-id="b5d7e-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="b5d7e-132">Lisateavet vt [Kohustuste jagamise konfliktide tuvastamine ja lahendamine](identify-resolve-conflicts-segregation-duties.md)</span><span class="sxs-lookup"><span data-stu-id="b5d7e-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]