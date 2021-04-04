---
title: Maksed tasakaalustatakse automaatselt enne tellimuste arveldamist või saatmist
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585285"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a><span data-ttu-id="0be36-103">Maksed tasakaalustatakse automaatselt enne tellimuste arveldamist või saatmist</span><span class="sxs-lookup"><span data-stu-id="0be36-103">Payments are automatically settled before orders are invoiced or shipped</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0be36-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.</span><span class="sxs-lookup"><span data-stu-id="0be36-104">This topic provides troubleshooting guidance that can help when a payment is settled in the Adyen portal immediately after an order is placed, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="description"></a><span data-ttu-id="0be36-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0be36-105">Description</span></span>

<span data-ttu-id="0be36-106">See teema annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.</span><span class="sxs-lookup"><span data-stu-id="0be36-106">After an order is placed, the payment is immediately settled in the Adyen portal, even though the sales order hasn't been invoiced or shipped.</span></span>

## <a name="resolution"></a><span data-ttu-id="0be36-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="0be36-107">Resolution</span></span>

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a><span data-ttu-id="0be36-108">Konfigureerige e-kaubanduse maksete käsitsi hõivamine Aydeni portaalis</span><span class="sxs-lookup"><span data-stu-id="0be36-108">Configure manual capture for e-commerce payments in the Adyen portal</span></span>

<span data-ttu-id="0be36-109">Et konfigureerida e-kaubanduse maksete käsitsi hõivamine Adyeni portaalis, järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="0be36-109">To configure manual capture for e-commerce payments in the Adyen portal, follow these steps.</span></span>

1. <span data-ttu-id="0be36-110">Logige sisse Adyeni portaali.</span><span class="sxs-lookup"><span data-stu-id="0be36-110">Sign in to the Adyen portal.</span></span>
1. <span data-ttu-id="0be36-111">Valige ülemises parempoolses nurgas oma e-äri kanali kaupmehekonto.</span><span class="sxs-lookup"><span data-stu-id="0be36-111">In the upper-right corner, select your merchant account for the e-commerce channel.</span></span>
1. <span data-ttu-id="0be36-112">Ülemisel navigeerimisribal valige **Konto** ja seejärel valige **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="0be36-112">On the top navigation, select **Account**, and then select **Settings**.</span></span>
1. <span data-ttu-id="0be36-113">Väljal **Salvestamise viivitus** valige **käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="0be36-113">In the **Capture Delay** field, select **manual**.</span></span>

    ![Viivitussätte hõivamine Adyeni portaalis](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a><span data-ttu-id="0be36-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0be36-115">Additional resources</span></span>

[<span data-ttu-id="0be36-116">Adyeni maksekonnektor</span><span class="sxs-lookup"><span data-stu-id="0be36-116">Adyen payment capture</span></span>](https://docs.adyen.com/point-of-sale/capturing-payments)

[<span data-ttu-id="0be36-117">Dynamics 365 maksekonnektor Adyeni jaoks</span><span class="sxs-lookup"><span data-stu-id="0be36-117">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="0be36-118">Dynamics 365 maksekonnektor Adyeni jaoks</span><span class="sxs-lookup"><span data-stu-id="0be36-118">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
