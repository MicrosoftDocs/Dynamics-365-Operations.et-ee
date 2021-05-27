---
title: TDS-i registreerimisnumbrite häälestamine juriidiliste isikute jaoks
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
ms.openlocfilehash: 3550b2b7b305702ffc337ba0a9bb79f60a9de120
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023175"
---
# <a name="set-up-tds-registration-numbers-for-legal-entities"></a><span data-ttu-id="c5c3b-103">TDS-i registreerimisnumbrite häälestamine juriidiliste isikute jaoks</span><span class="sxs-lookup"><span data-stu-id="c5c3b-103">Set up TDS registration numbers for legal entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5c3b-104">See teema kirjeldab, kuidas seadistada maksegraafikuid allika (TDS) eraldamisel mahaarvatud maksuga.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-104">This topic explains how to set up Tax Deducted at Source (TDS) registration numbers for legal entities.</span></span>

1. <span data-ttu-id="c5c3b-105">Avage **Organisatsiooni haldus \> Organisatsioonid \> Juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-105">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

    <span data-ttu-id="c5c3b-106">[![Vahekaart juriidilised olemid](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span><span class="sxs-lookup"><span data-stu-id="c5c3b-106">[![Legal entities page](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span></span>

2. <span data-ttu-id="c5c3b-107">Kiirkaardi **Maksuteave** väljale **Püsikonto number** sisestage juriidilise isiku püsikonto number (PAN).</span><span class="sxs-lookup"><span data-stu-id="c5c3b-107">On the **Tax information** FastTab, in the **Permanent account number** field, enter the permanent account number (PAN) of the legal entity.</span></span>
3. <span data-ttu-id="c5c3b-108">Sisestage **Ringinumber** väljale TDS-i asutuse ringinumber.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-108">In the **Circle number** field, enter the circle number of the TDS authority.</span></span>
4. <span data-ttu-id="c5c3b-109">Sisestage **Sihtnumber** väljale TDS-i asutuse sihtnumber.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-109">In the **Ward number** field, enter the ward number of the TDS authority.</span></span>
5. <span data-ttu-id="c5c3b-110">Väljale **Hindav ametnik** sisestage TDS-i asutuse hindava ametniku üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-110">In the **Assessing officer** field, enter the details of the assessing officer for the TDS authority.</span></span>
6. <span data-ttu-id="c5c3b-111">Valige **Mahaarvaja tüüp** väljal juriidilise isiku mahaarvaja tüübi kategooria.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-111">In the **Type of deductor** field, select the deductor type category for the legal entity.</span></span>
7. <span data-ttu-id="c5c3b-112">Toimingupaanil valige **Registreerimise ID** et avada **Halda aadressi** leht.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-112">On the Action Pane, select **Registration IDs** to open the **Manage addresses** page.</span></span>
8. <span data-ttu-id="c5c3b-113">**Maksuteabe** kiirkaardil valige **Lisa** või **Redigeeri** et avada **Maksuteabe haldamine** leht, kus saate maksu registreerimiskirjet hallata.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-113">On the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>

    <span data-ttu-id="c5c3b-114">[![Aadresside lehe haldamine](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span><span class="sxs-lookup"><span data-stu-id="c5c3b-114">[![Manage addresses page](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span></span>

9. <span data-ttu-id="c5c3b-115">Sisestage **Kinnipeetava maksu** kiirkaardi väljale **Maksukonto number (TAN)** väljale registreerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-115">On the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the registration number.</span></span> <span data-ttu-id="c5c3b-116">TAN peab koosnema viiest tähestikumärgist, seejärel neljast numbrimärgist ja seejärel ühest tähestikumärgist.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-116">This number must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="c5c3b-117">Siin on näide: **AXDF87645F**.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-117">Here is an example: **AXDF87645F**.</span></span>
10. <span data-ttu-id="c5c3b-118">Sisestage **Nimi või kirjeldus** kinnipeetava maksu registreerimisnumbri kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-118">In the **Name or description** field, enter a description of the withholding tax registration number.</span></span>

    <span data-ttu-id="c5c3b-119">[![Maksuteabe lehe haldamine](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span><span class="sxs-lookup"><span data-stu-id="c5c3b-119">[![Manage tax information page](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span></span>

11. <span data-ttu-id="c5c3b-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c5c3b-120">Close the page.</span></span>
