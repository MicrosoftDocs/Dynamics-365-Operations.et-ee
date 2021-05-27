---
title: Kinnipeetava maksu haldurite häälestamine TDS-i maksutüübi jaoks
description: See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.
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
ms.openlocfilehash: 5375363a9b1383a83e80fc3c4b841780adab4172
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023170"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a><span data-ttu-id="9a599-103">Kinnipeetava maksu haldurite häälestamine TDS-i maksutüübi jaoks</span><span class="sxs-lookup"><span data-stu-id="9a599-103">Set up withholding tax authorities for the TDS tax type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a599-104">See teema kirjeldab, kuidas tasakaalustada allikas (TDS) mahaarvatud perioodilist maksu.</span><span class="sxs-lookup"><span data-stu-id="9a599-104">This topic explains how to set up Tax Deducted at Source (TDS) authorities.</span></span>

1. <span data-ttu-id="9a599-105">Avage **Maks \> Kaudsed maksud \> Kinnipeetav maks**.</span><span class="sxs-lookup"><span data-stu-id="9a599-105">Go to **Tax \> Indirect taxes \> Withholding tax authorities**.</span></span>

    <span data-ttu-id="9a599-106">[![Kinnipeetava maksu komponentide leht](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span><span class="sxs-lookup"><span data-stu-id="9a599-106">[![Withholding tax authorities page](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)</span></span>

2. <span data-ttu-id="9a599-107">**Maksu tüübi** väljal valige **TDS** kinnipeetava maksu komponentide häälestamiseks.</span><span class="sxs-lookup"><span data-stu-id="9a599-107">In the **Tax type** field, select **TDS** to set up withholding tax authorities for the TDS tax type.</span></span>
3. <span data-ttu-id="9a599-108">Rea loomiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a599-108">On the Action Pane, select **New** to create a line.</span></span>
4. <span data-ttu-id="9a599-109">Sisestage **Kinnipeetava maksu komponendi** väljale TDS-i komponendi nimi.</span><span class="sxs-lookup"><span data-stu-id="9a599-109">In the **Withholding tax authority** field, enter a name for the TDS authority.</span></span>
5. <span data-ttu-id="9a599-110">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9a599-110">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="9a599-111">Vahekaardil **Üldine** valige **Hankija konto** väljal hankija konto TDS komponentide jaoks.</span><span class="sxs-lookup"><span data-stu-id="9a599-111">On the **General** FastTab, in the **Vendor account** field, select the vendor account for the TDS authority.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9a599-112">Peate määrama panga nime, kuhu deponeeritakse TDS-i asutuse hankijale võlgnetavad vahendid.</span><span class="sxs-lookup"><span data-stu-id="9a599-112">You must define the name of the bank where funds that are owed to the TDS authority vendor will be deposited.</span></span> <span data-ttu-id="9a599-113">Panga nimi määratletakse **Pangakontode** lehel (**Maksekonto \> Kõik hankijad \> Hankija \> Häälestatud \>Pangakontod**).</span><span class="sxs-lookup"><span data-stu-id="9a599-113">The bank's name is defined on the **Bank accounts** page (**Accounts payable \> All vendors \> Vendor \> Set up \> Bank accounts**).</span></span>

7. <span data-ttu-id="9a599-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a599-114">Close the page.</span></span>
