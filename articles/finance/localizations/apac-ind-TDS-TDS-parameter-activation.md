---
title: TDS-i parameetrite määramine
description: See teema kirjeldab, kuidas seadistada parameetreid määratud kannetes allika (TDS) funktsioonis mahaarvatud maksu aktiveerimiseks. See on vajalik samm allika TDS-is maha arvatud maksu kasutamiseks.
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
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023176"
---
# <a name="set-the-tds-parameters"></a><span data-ttu-id="67c2c-104">TDS-i parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="67c2c-104">Set the TDS parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67c2c-105">See teema kirjeldab, kuidas seadistada parameetreid määratud kannetes allika (TDS) funktsioonis mahaarvatud maksu aktiveerimiseks.</span><span class="sxs-lookup"><span data-stu-id="67c2c-105">This topic explains how to set parameters to activate Tax Deducted at Source (TDS) functionality in specified transactions.</span></span> <span data-ttu-id="67c2c-106">See on vajalik samm allika TDS-is maha arvatud maksu kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="67c2c-106">This is a necessary step to use the Tax Deducted at Source TDS feature.</span></span>

1. <span data-ttu-id="67c2c-107">Avage **Pearaamat \> Pearaamatu seadistamine \> Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="67c2c-107">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="67c2c-108">Jaotises **Otsesed maksud** vahekaardil **Allikast mahaarvatud** väljal seadke suvand **Aktiveeri TDS** suvandiks **Jah** et aktiveerida TDS-funktsioon ning kasutatavad lehed ja väljad.</span><span class="sxs-lookup"><span data-stu-id="67c2c-108">On the **Direct taxes** tab, in the **Tax Deducted at Source** section, set the **Activate TDS** option to **Yes** to activate the TDS functionality, and the pages and fields that are used for it.</span></span>
3. <span data-ttu-id="67c2c-109">Seadke **Arve** valikule **Jah** et aktiveerida väljad, mida kasutatakse TDS-i arvutamiseks ja mahaarvamiseks arve tasemel.</span><span class="sxs-lookup"><span data-stu-id="67c2c-109">Set the **Invoice** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the invoice level.</span></span>
4. <span data-ttu-id="67c2c-110">Seadke **Makse** valikule **Jah** et aktiveerida väljad, mida kasutatakse TDS-i arvutamiseks ja mahaarvamiseks arve tasemel.</span><span class="sxs-lookup"><span data-stu-id="67c2c-110">Set the **Payment** option to **Yes** to activate the fields that are used to calculate and deduct TDS at the payment level.</span></span>

    <span data-ttu-id="67c2c-111">[![Otsesed maksud vahekaart](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span><span class="sxs-lookup"><span data-stu-id="67c2c-111">[![Direct taxes tab](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)</span></span>

5. <span data-ttu-id="67c2c-112">Leidke **Numbriseeriate** vahekaardil rida, kus **Viitenumbri** väärtuseks on seatud **Kinnipeetava maksu makse**.</span><span class="sxs-lookup"><span data-stu-id="67c2c-112">On the **Number sequences** tab, find the row where the **Reference** field is set to **Withholding tax payment**.</span></span> <span data-ttu-id="67c2c-113">Sisestage **Numbriseeria kood** väljale rea jaoks numbriseeria kood väljale .</span><span class="sxs-lookup"><span data-stu-id="67c2c-113">In the **Number sequence code** field for the row, select the number sequence code.</span></span> <span data-ttu-id="67c2c-114">Numbriseeria koodi kasutatakse TDS-i perioodilise tasakaalustusprotsessi jaoks kandenumbrite loomiseks.</span><span class="sxs-lookup"><span data-stu-id="67c2c-114">The number sequence code is used to generate voucher numbers for the periodic TDS settlement process.</span></span>

    > [!NOTE]
    > <span data-ttu-id="67c2c-115">Perioodilise TDS-i tasakaalustusprotsessi käivitamiseks minge **Maks \> Deklaratsioon \> kinnipeetava maksu \> Kinnipeetava maksu makse**.</span><span class="sxs-lookup"><span data-stu-id="67c2c-115">To run the periodic TDS settlement process, go to **Tax \> Declarations \> Withholding tax \> Withholding tax payment**.</span></span>

    <span data-ttu-id="67c2c-116">[![Vahekaart Numbriseeriad](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span><span class="sxs-lookup"><span data-stu-id="67c2c-116">[![Number sequences tab](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)</span></span>

6. <span data-ttu-id="67c2c-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="67c2c-117">Close the page.</span></span>
