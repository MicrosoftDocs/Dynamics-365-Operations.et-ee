---
title: TDS-i parameetrite määramine ostureskontros ja müügireskontros
description: See teema kirjeldab, kuidas seadistada parameetreid Ostureskontros ja Müügireskontros, et toetada allika (TDS) mahaarvamistes mahaarvatud maksu.
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023178"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="26e5d-103">TDS-i parameetrite määramine ostureskontros ja müügireskontros</span><span class="sxs-lookup"><span data-stu-id="26e5d-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26e5d-104">See teema kirjeldab, kuidas seadistada parameetreid Ostureskontros ja Müügireskontros, et toetada allika (TDS) mahaarvamistes mahaarvatud maksu.</span><span class="sxs-lookup"><span data-stu-id="26e5d-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="26e5d-105">Minge **Maks \> Seadistus \> Parameetrid \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="26e5d-106">Vahekaardil **Uuendused** valige dialoogiboksi **Tellimuse ridade värskendamine** avamiseks suvand **Tellimuse ridade värskendamine** dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="26e5d-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="26e5d-107">Jaotise **TDS grupp** väljal **TDS-i grupi värskendamine** määrake meetod, mida kasutataks TDS-grupi värskendamiseks rea tasemel.</span><span class="sxs-lookup"><span data-stu-id="26e5d-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="26e5d-108">Seda sätet kasutatakse TDS-i grupi tellimuse päises uuendamisel.</span><span class="sxs-lookup"><span data-stu-id="26e5d-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="26e5d-109">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="26e5d-109">The following options are available:</span></span>

    - <span data-ttu-id="26e5d-110">**Mitte kunagi** – TDS-gruppi ei uuendata tellimuse ridadel, kui seda värskendatakse tellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="26e5d-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="26e5d-111">**Alati** – TDS-gruppi ei uuendata tellimuse ridadel, kui seda värskendatakse tellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="26e5d-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="26e5d-112">**Viip** – Kasutajad saavad sõnumi, mis palub neil uuendada TDS-i gruppi tellimuse ridadel.</span><span class="sxs-lookup"><span data-stu-id="26e5d-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="26e5d-113">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-113">Select **OK**.</span></span>

    <span data-ttu-id="26e5d-114">[![Tellimuseridade uuendamise dialoogiboks](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="26e5d-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="26e5d-115">Minge **Maks \> Seadistus \> Parameetrid \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="26e5d-116">Seadke **Üldine** vahekaardil **Tükelda tarneaadressi põhjal** **Toote sissetulek** väärtusele **Jah** et sisestada ja tükeldada toote sissetulek, kus on erinevad tarneaadressid ja maksukonto numbrid (TAN-id).</span><span class="sxs-lookup"><span data-stu-id="26e5d-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="26e5d-117">Kui see valik on seatud valikule **Ei** ei saa te sisestada ostu saatelehte, kus on erinevad tarneaadressid ja TAN-id.</span><span class="sxs-lookup"><span data-stu-id="26e5d-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="26e5d-118">TAN-idega ostuarve sisestamiseks ja tükeldamiseks määrake valiku **Arve** valiku väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="26e5d-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="26e5d-119">[![Tükelda tarneteabe kiirkaardi põhjal](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="26e5d-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="26e5d-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="26e5d-120">Close the page.</span></span>
