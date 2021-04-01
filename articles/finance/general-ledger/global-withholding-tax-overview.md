---
title: Globaalne kinnipeetav maks
description: Selles teemas antakse teavet globaalsete kinnipeetava maksu funktsionaalsuse ja selle seadistamise kohta. Globaalse kinnipeetava maksu funktsionaalsus on võimendatud hankija ja kliendi tehingute jaoks, nii et kinnipeetav maks arvutatakse kauba tasemel.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 25fc503d6145872b8e9f28b8d9a4d7b9c1ba53a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249163"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="5f790-104">Globaalne kinnipeetav maks</span><span class="sxs-lookup"><span data-stu-id="5f790-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f790-105">Selles teemas antakse teavet globaalsete kinnipeetava maksu funktsionaalsuse kohta ja selgitatakse selle seadistamist.</span><span class="sxs-lookup"><span data-stu-id="5f790-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="5f790-106">Uus funktsionaalsus on saadaval versioonis 10.0.17 ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="5f790-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="5f790-107">Globaalse kinnipeetava maksu funktsionaalsus on võimendatud hankija ja kliendi tehingute jaoks, nii et kinnipeetav maks arvutatakse kauba tasemel.</span><span class="sxs-lookup"><span data-stu-id="5f790-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="5f790-108">Ostutehingutest kinnipeetava maksu konto saldot saab tasakaalustada, käitades kinnipeetava maksu töö kinnipeetava maksu tasakaalustuskonto vastu.</span><span class="sxs-lookup"><span data-stu-id="5f790-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="5f790-109">Globaalne kinnipeetav maks ei toeta ostutellimuse, hankija arve ja müügitellimuse lehtede funktsiooni **Tasude haldamine**.</span><span class="sxs-lookup"><span data-stu-id="5f790-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="5f790-110">Globaalse kinnipeetava maksu sisse lülitamine</span><span class="sxs-lookup"><span data-stu-id="5f790-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="5f790-111">Valige tööruumis **Funktsioonihaldus** suvand **Globaalne kinnipeetav maks** ja seejärel valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="5f790-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="5f790-112">Avage **Maks \> Seadistus \> Parameetrid \> Pearaamatu parameetrid** ja seejärel seadistage vahekaardil **Kinnipeetav maks** suvand **Luba globaalne kinnipeetav maks** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="5f790-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="5f790-113">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5f790-113">Select **Save**.</span></span>
4. <span data-ttu-id="5f790-114">Värskendage lehekülg oma veebibrauseris.</span><span class="sxs-lookup"><span data-stu-id="5f790-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="5f790-115">Globaalset kinnipeetava maksu funktsiooni ei saa sisse lülitada riikide/regioonide puhul, kus on lokaliseeritud kinnipeetava maksu lahendused juba olemas.</span><span class="sxs-lookup"><span data-stu-id="5f790-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="5f790-116">Need alad on järgmised (kuid mitte ainult) - India, Brasiilia, Tai, Saudi Araabia, Iirimaa, Suurbritannia ja Ameerika Ühendriikidega.</span><span class="sxs-lookup"><span data-stu-id="5f790-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]