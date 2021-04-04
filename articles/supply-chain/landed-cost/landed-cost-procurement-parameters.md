---
title: Tarnehinna hankeparameetrid
description: See teema kirjeldab, kuidas seadistada asjakohaseid hankeparameetreid, kui kasutate Tarnehinna moodulit.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500738"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="d0c9f-103">Tarnehinna hankeparameetrid</span><span class="sxs-lookup"><span data-stu-id="d0c9f-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d0c9f-104">**Hankeparameetrite** lehel on mõned sätted, mis on eriti asjakohased, kui kasutate **Tarnehinna** moodulit.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="d0c9f-105">Kasutage **Tellimuseridade värskendamine** dialoogiboksi, mis on avatud **Hankeparameetrite** lehel, et määrata, kas ostutellimuse päises tehtud muudatuste korral tuleks ostutellimuse read automaatselt uuendada.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="d0c9f-106">Selle seadistamise lõpetamiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="d0c9f-107">Minge **Hanked \> Seadistus \> Hangete parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="d0c9f-108">Vahekaardil **Üldine**, valige link **Uuenda tellimuse ridu**.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="d0c9f-109">Dialoogiaknas **Tellimuse ridade värskendamine** loetletakse tellimuse päise väljad, mida saab rakendada ka tellimuseridade seotud väljade automaatseks värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="d0c9f-110">Seadistage iga loendi väli ühele järgmistest väärtustest:</span><span class="sxs-lookup"><span data-stu-id="d0c9f-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="d0c9f-111">**Alati** - Tellimuse read uuendatakse tellimuse päise uuendamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="d0c9f-112">**Mitte kunagi** - Tellimuse ridu ei uuendata kunagi tellimuse päise uuendamisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="d0c9f-113">**Küsi** - Kasutajalt küsitakse, kas tellimuse ridu tuleks uuendada.</span><span class="sxs-lookup"><span data-stu-id="d0c9f-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
