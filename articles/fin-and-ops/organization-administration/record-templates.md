---
title: Kirjemallid
description: "Selles artiklis tutvustatakse kirjemallide mõistet ja selgitatakse, kuidas neid saab kasutada teavet jagavate kirjete loomiseks."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 298f34871265dbf5c437dcdc6c05270b4e2a9a9d
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="record-templates"></a><span data-ttu-id="69fa0-103">Kirjemallid</span><span class="sxs-lookup"><span data-stu-id="69fa0-103">Record templates</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="69fa0-104">Selles artiklis tutvustatakse kirjemallide mõistet ja selgitatakse, kuidas neid saab kasutada teavet jagavate kirjete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="69fa0-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="69fa0-105">Kirjemallid aitavad teil kirjeid Microsoft Dynamics 365 for Finance and Operationsis kiiremini luua.</span><span class="sxs-lookup"><span data-stu-id="69fa0-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="69fa0-106">Microsoft Dynamics 365 for Finance and Operationsis saate kirjemalle luua ainult teatud kirje tüüpide puhul.</span><span class="sxs-lookup"><span data-stu-id="69fa0-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="69fa0-107">Näiteks kujutage ette, et sisestate renditeavet autorendiettevõtte puhul, mis asub San Franciscos.</span><span class="sxs-lookup"><span data-stu-id="69fa0-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="69fa0-108">Kuna enamik kliente on tõenäoliselt pärit San Francisco piirkonnast, oleks tore, kui saaksite rendivormil automaatselt täita väljade **Osariik**, **Maakond** ja **Linn** väärtused.</span><span class="sxs-lookup"><span data-stu-id="69fa0-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="69fa0-109">Saate malle rakendada ainult nendes Finance and Operationsi osades, millele teil juurdepääs on.</span><span class="sxs-lookup"><span data-stu-id="69fa0-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="69fa0-110">Siiski on kõik mallipealkirjad teile uue kirje loomisel nähtavad, ja ka teistele kasutajatele, kui loote mallid, mis on saadaval kõigile kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="69fa0-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="69fa0-111">Võtke seda mallide nimetamisel arvesse.</span><span class="sxs-lookup"><span data-stu-id="69fa0-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="69fa0-112">Vältige näiteks nimesid, mis sisaldavad selliseid sõnu, nagu „komisjonitasu”, kui see on konfidentsiaalne teave, et osa ettevõtte töötajatest saab komisjonitasul põhinevat palka.</span><span class="sxs-lookup"><span data-stu-id="69fa0-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="69fa0-113">Kui teil on juurdepääs ühele või mitmele mallile, mis on loodud konkreetse vormi jaoks, ja proovite luua sellesse vormi uut kirjet, kuvatakse leht **Malli valimine üksusele**.</span><span class="sxs-lookup"><span data-stu-id="69fa0-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="69fa0-114">Kui valite malli loendist, luuakse uus kirje, mis sisaldab valitud mallil põhinevat vaiketeavet.</span><span class="sxs-lookup"><span data-stu-id="69fa0-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="69fa0-115">Kui te ei soovi uute kirjete loomisel malle kasutada, märkige ruut **Ära edaspidi küsi** lehel **Malli valimine üksusele**.</span><span class="sxs-lookup"><span data-stu-id="69fa0-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="69fa0-116">Mallivaliku uuesti kuvamiseks paremklõpsake suvalisel kirjel, klõpsake valikut **Kirje teave** ning seejärel klõpsake valikut **Näita mallivalikut**.</span><span class="sxs-lookup"><span data-stu-id="69fa0-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




