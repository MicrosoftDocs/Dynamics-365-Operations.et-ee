---
title: TDS-i pearaamatukontode häälestamine
description: See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023177"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="18c72-103">TDS-i pearaamatukontode häälestamine</span><span class="sxs-lookup"><span data-stu-id="18c72-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18c72-104">See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.</span><span class="sxs-lookup"><span data-stu-id="18c72-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="18c72-105">Te kasutate **Kontoplaani** lehte, et seadistada TDS-ile pearaamatukontod.</span><span class="sxs-lookup"><span data-stu-id="18c72-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="18c72-106">Minge jaotisse **Pearaamat \> Kontoplaan \> Kontod \> Põhikontod**.</span><span class="sxs-lookup"><span data-stu-id="18c72-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="18c72-107">Vahekaardil **Ülevaade** valige **Alt+N** TDS-i pearaamatukonto loomiseks ja sisestage nõutavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="18c72-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="18c72-108">Valige **Seadistus** vahekaardi väljal **Sisestamistüüp** suvand **Kinnipeetav maks**.</span><span class="sxs-lookup"><span data-stu-id="18c72-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="18c72-109">Pearaamatukontosid, mille sisestamistüüp on **Kinnipeetav maks** saab määratleda ainult müügireskontrona, mida kasutatakse TDS-i maksukoodi jaoksTDS-i müügireskontro summa sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="18c72-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="18c72-110">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="18c72-110">Close the page.</span></span>
