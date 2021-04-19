---
title: Salvestamine järgmise makse suvandi jaoks ei ilmu
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui märkeruut Salvesta minu järgmisele maksele ei ilmu maksemeetodi all e-äri saidi väljaregistreerimise lehel.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7e3156d1aa9a05dc5d159b6f9b33ae341de640bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801695"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a><span data-ttu-id="4c3f8-103">"Salvestamine järgmise makse suvandi jaoks ei ilmu</span><span class="sxs-lookup"><span data-stu-id="4c3f8-103">"Save for my next payment" option doesn't appear</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4c3f8-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui märkeruut **Salvesta minu järgmisele maksele** ei ilmu maksemeetodi all e-äri saidil **Makseviis** väljaregistreerimise lehel.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-104">This topic provides troubleshooting guidance that can help when the **Save for my next payment** check box doesn't appear under **Payment method** on an e-commerce site's checkout page.</span></span>

## <a name="description"></a><span data-ttu-id="4c3f8-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4c3f8-105">Description</span></span>

<span data-ttu-id="4c3f8-106">Märkeruut **Salvesta minu järgmise makse** jaoks ei ilmu maksemeetodi jaotises **Makseviis** e-kaubanduse saidi väljaregistreerimise lehel.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-106">The **Save for my next payment** check box doesn't appear in the **Payment method** section on an e-commerce site's checkout page.</span></span>

<span data-ttu-id="4c3f8-107">Järgmine näide näitab väljaregistreerimise lehe näidet, mis sisaldab märkeruutu **Salvesta minu järgmise makse** jaoks.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-107">The following illustration shows an example of a checkout page that includes the **Save for my next payment** check box.</span></span>

![Salvesta minu järgmise makse märkeruudu jaoks maksemoodulis](media/payment-module-save-payment.jpg)

## <a name="resolution"></a><span data-ttu-id="4c3f8-109">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="4c3f8-109">Resolution</span></span>

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a><span data-ttu-id="4c3f8-110">Veenduge, et Dynamics 365 Payment Connector Puhvri jaoks on Commerce Headquartersis õigesti konfigureeritud</span><span class="sxs-lookup"><span data-stu-id="4c3f8-110">Verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters</span></span>

<span data-ttu-id="4c3f8-111">Veenduge, et Dynamics 365 Payment Connector Puhvri jaoks on Commerce Headquartersis õigesti konfigureeritud, järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-111">To verify that the Dynamics 365 Payment Connector for Adyen is correctly configured in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4c3f8-112">Avage **Jaemüük ja kaubandus \> Kanalid \> Veebipoed**.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-112">Go to **Retail and Commerce \> Channels \> Online Stores**.</span></span>
1. <span data-ttu-id="4c3f8-113">Valige veebikauplus.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-113">Select the online store.</span></span>
1. <span data-ttu-id="4c3f8-114">Kiirkaardil **Maksekontod** veenduge, et välja **Luba makseteabe salvestamine e-äris** väärtuseks on seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="4c3f8-114">On the **Payment accounts** FastTab, make sure that the **Allow saving payment information in e-commerce** field is set to **True**.</span></span>

![Luba commerce headquartersi e-commerce'i väljale makseteabe salvestamine](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a><span data-ttu-id="4c3f8-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4c3f8-116">Additional resources</span></span>

[<span data-ttu-id="4c3f8-117">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="4c3f8-117">Payment module</span></span>](../payment-module.md)

[<span data-ttu-id="4c3f8-118">Veebimaksevahendite salvestamine Adyeni konnektori abil</span><span class="sxs-lookup"><span data-stu-id="4c3f8-118">Saving online payment instruments with the Adyen connector</span></span>](../dev-itpro/adyen-connector-listPI.md)
