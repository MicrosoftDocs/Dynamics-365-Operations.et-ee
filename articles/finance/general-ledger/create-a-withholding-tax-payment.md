---
title: Kinnipeetava maksu makse loomine
description: Kinnipeetava maksu makse tööprotseduur tasakaalustab kinnipeetava maksu saldod kinnipeetava maksu kontode ostureskontrost ja tasakaalustab need kinnipeetava maksu tasakaalustuskontoga kindla perioodi jooksul. Selles teemas loetletakse kinnipeetava maksu makse seadistamise etapid.
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
ms.openlocfilehash: eae914ccafad12426cadd91c0950bada23548005
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212273"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="edc01-104">Kinnipeetava maksu makse loomine</span><span class="sxs-lookup"><span data-stu-id="edc01-104">Create a withholding tax payment</span></span>

<span data-ttu-id="edc01-105">Kinnipeetava maksu makse tööprotseduur tasakaalustab kinnipeetava maksu saldod kinnipeetava maksu kontode ostureskontrost ja tasakaalustab need kinnipeetava maksu tasakaalustuskontoga kindla perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="edc01-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="edc01-106">Selles teemas loetletakse kinnipeetava maksu makse seadistamise etapid.</span><span class="sxs-lookup"><span data-stu-id="edc01-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="edc01-107">Kinnipeetava maksu vastaskontot (müügireskontrost) ei võeta kinnipeetava maksu makse arvutamisel arvesse.</span><span class="sxs-lookup"><span data-stu-id="edc01-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="edc01-108">Avage **Navigeerimispaan > Moodulid > Maks > Deklaratsioonid > Kinnipeetav maks > Kinnipeetava maksu makse**.</span><span class="sxs-lookup"><span data-stu-id="edc01-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="edc01-109">Klõpsake väljal **Tasakaalustusperiood** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="edc01-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="edc01-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="edc01-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="edc01-111">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="edc01-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="edc01-112">Sisestage kuupäev väljale **Kande kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="edc01-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="edc01-113">Kinnipeetava maksu makse kande sisestamiseks kinnipeetava maksu tasakaalustuskontole valige käsk **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="edc01-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="edc01-114">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="edc01-114">Click **OK**.</span></span>

![Kinnipeetava maksu makse parameetrid](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]