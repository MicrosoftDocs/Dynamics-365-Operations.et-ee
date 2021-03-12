---
title: Kirjemallide ülevaade
description: Selles artiklis tutvustatakse kirjemallide mõistet ja selgitatakse, kuidas neid saab kasutada teavet jagavate kirjete loomiseks.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca9ddaed0c4aad6aeb3877384778d33f83e6e4aa
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796846"
---
# <a name="record-templates-overview"></a><span data-ttu-id="07e00-103">Kirjemallide ülevaade</span><span class="sxs-lookup"><span data-stu-id="07e00-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07e00-104">Selles artiklis tutvustatakse kirjemallide mõistet ja selgitatakse, kuidas neid saab kasutada teavet jagavate kirjete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="07e00-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="07e00-105">Kirje mallid aitavad teil kirjeid kiiremini luua, kuid mõnede kirje tüüpide jaoks saate luua ainult kirje malle.</span><span class="sxs-lookup"><span data-stu-id="07e00-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="07e00-106">Näiteks kujutage ette, et sisestate renditeavet autorendiettevõtte puhul, mis asub San Franciscos.</span><span class="sxs-lookup"><span data-stu-id="07e00-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="07e00-107">Kuna enamik kliente on tõenäoliselt pärit San Francisco piirkonnast, oleks tore, kui saaksite rendivormil automaatselt täita väljade **Osariik**, **Maakond** ja **Linn** väärtused.</span><span class="sxs-lookup"><span data-stu-id="07e00-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="07e00-108">Saate malle rakendada ainult nendes tarkvara osades, millele teil juurdepääs on.</span><span class="sxs-lookup"><span data-stu-id="07e00-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="07e00-109">Siiski on kõik mallipealkirjad teile uue kirje loomisel nähtavad, ja ka teistele kasutajatele, kui loote mallid, mis on saadaval kõigile kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="07e00-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="07e00-110">Võtke seda mallide nimetamisel arvesse.</span><span class="sxs-lookup"><span data-stu-id="07e00-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="07e00-111">Vältige näiteks nimesid, mis sisaldavad selliseid sõnu, nagu „komisjonitasu”, kui see on konfidentsiaalne teave, et osa ettevõtte töötajatest saab komisjonitasul põhinevat palka.</span><span class="sxs-lookup"><span data-stu-id="07e00-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="07e00-112">Kui teil on juurdepääs ühele või mitmele mallile, mis on loodud konkreetse vormi jaoks, ja proovite luua sellesse vormi uut kirjet, kuvatakse leht **Malli valimine üksusele**.</span><span class="sxs-lookup"><span data-stu-id="07e00-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="07e00-113">Kui valite malli loendist, luuakse uus kirje, mis sisaldab valitud mallil põhinevat vaiketeavet.</span><span class="sxs-lookup"><span data-stu-id="07e00-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="07e00-114">Kui te ei soovi uute kirjete loomisel malle kasutada, märkige ruut **Ära edaspidi küsi** lehel **Malli valimine üksusele**.</span><span class="sxs-lookup"><span data-stu-id="07e00-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="07e00-115">Mallivaliku uuesti kuvamiseks paremklõpsake suvalisel kirjel, klõpsake valikut **Kirje teave** ning seejärel klõpsake valikut **Näita mallivalikut**.</span><span class="sxs-lookup"><span data-stu-id="07e00-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
