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
ms.openlocfilehash: 17ed1dcae97f6cd28175c483be5ca3ce96d59e05
ms.sourcegitcommit: 053f4cda6862fbcd9e3aa6e9cb009e7de833beac
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/28/2021
ms.locfileid: "5075734"
---
# <a name="global-withholding-tax"></a><span data-ttu-id="7672d-104">Globaalne kinnipeetav maks</span><span class="sxs-lookup"><span data-stu-id="7672d-104">Global withholding tax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7672d-105">Selles teemas antakse teavet globaalsete kinnipeetava maksu funktsionaalsuse kohta ja selgitatakse selle seadistamist.</span><span class="sxs-lookup"><span data-stu-id="7672d-105">This topic provides information about global withholding tax functionality and explains how to set it up.</span></span> <span data-ttu-id="7672d-106">Uus funktsionaalsus on saadaval versioonis 10.0.17 ja uuemates.</span><span class="sxs-lookup"><span data-stu-id="7672d-106">The new functionality is available in version 10.0.17 and later.</span></span>

<span data-ttu-id="7672d-107">Globaalse kinnipeetava maksu funktsionaalsus on võimendatud hankija ja kliendi tehingute jaoks, nii et kinnipeetav maks arvutatakse kauba tasemel.</span><span class="sxs-lookup"><span data-stu-id="7672d-107">Global withholding tax functionality is enhanced for vendor and customer transactions, so that withholding tax is calculated at the item level.</span></span> <span data-ttu-id="7672d-108">Ostutehingutest kinnipeetava maksu konto saldot saab tasakaalustada, käitades kinnipeetava maksu töö kinnipeetava maksu tasakaalustuskonto vastu.</span><span class="sxs-lookup"><span data-stu-id="7672d-108">The balance in the withholding tax account from purchase transactions can be settled by running the withholding tax payment job against the withholding tax settlement account.</span></span>

> [!NOTE]
> <span data-ttu-id="7672d-109">Globaalne kinnipeetav maks ei toeta ostutellimuse, hankija arve ja müügitellimuse lehtede funktsiooni **Tasude haldamine**.</span><span class="sxs-lookup"><span data-stu-id="7672d-109">Global withholding tax doesn't support the **Maintain charges** function on the purchase order, vendor invoice, and sales order pages.</span></span>

## <a name="turn-on-global-withholding-tax"></a><span data-ttu-id="7672d-110">Globaalse kinnipeetava maksu sisse lülitamine</span><span class="sxs-lookup"><span data-stu-id="7672d-110">Turn on global withholding tax</span></span>

1. <span data-ttu-id="7672d-111">Valige tööruumis **Funktsioonihaldus** suvand **Globaalne kinnipeetav maks** ja seejärel valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="7672d-111">In the **Feature management** workspace, select **Global withholding tax**, and then select **Enable now**.</span></span>
2. <span data-ttu-id="7672d-112">Avage **Maks \> Seadistus \> Parameetrid \> Pearaamatu parameetrid** ja seejärel seadistage vahekaardil **Kinnipeetav maks** suvand **Luba globaalne kinnipeetav maks** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7672d-112">Go to **Tax \> Setup \> Parameters \> General ledger parameters**, and then, on the **Withholding tax** tab, set the **Enable global withholding tax** option to **Yes**.</span></span>
3. <span data-ttu-id="7672d-113">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7672d-113">Select **Save**.</span></span>
4. <span data-ttu-id="7672d-114">Värskendage lehekülg oma veebibrauseris.</span><span class="sxs-lookup"><span data-stu-id="7672d-114">Refresh the page in your web browser.</span></span>

> [!NOTE]
> <span data-ttu-id="7672d-115">Globaalset kinnipeetava maksu funktsiooni ei saa sisse lülitada riikide/regioonide puhul, kus on lokaliseeritud kinnipeetava maksu lahendused juba olemas.</span><span class="sxs-lookup"><span data-stu-id="7672d-115">Global withholding tax functionality can’t be turned on for countries/regions where localized withholding tax solutions already exist.</span></span> <span data-ttu-id="7672d-116">Need alad on järgmised (kuid mitte ainult) - India, Brasiilia, Tai, Saudi Araabia, Iirimaa, Suurbritannia ja Ameerika Ühendriikidega.</span><span class="sxs-lookup"><span data-stu-id="7672d-116">These areas include but are not restricted to India, Brazil, Thailand, Saudi Arabia, Ireland, Great Britain and the United States.</span></span>
