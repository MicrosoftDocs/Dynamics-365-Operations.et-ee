---
title: Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui makseviisi jaotist ei laadita ja kuvatakse tõrketeade.
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
ms.openlocfilehash: f0751fc76e6eb4320f766886b4c1efcb1042e996
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585280"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="fc175-103">Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge</span><span class="sxs-lookup"><span data-stu-id="fc175-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc175-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui **makseviisi jaotist** ei laadita ja kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="fc175-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="fc175-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fc175-105">Description</span></span>

<span data-ttu-id="fc175-106">Kui avate e-poe väljaregistreerimise lehekülje, ei laadita **makseviisi jaotist** ja kuvatakse järgmine tõrketeade: "Midagi läks valesti.</span><span class="sxs-lookup"><span data-stu-id="fc175-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="fc175-107">Proovige hiljem uuesti.”</span><span class="sxs-lookup"><span data-stu-id="fc175-107">Please try again later."</span></span>

![Maksemooduli tõrge](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="fc175-109">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="fc175-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="fc175-110">Oodake, kuni Commerce Scale Unit vahemälu aegub</span><span class="sxs-lookup"><span data-stu-id="fc175-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="fc175-111">E-poe väljaregistreerimise lehel olevad makseteenuse sätted salvestatakse vahemällu Commerce Scale Unit ja selle kuvamiseks e-kaubanduse saidil võib aega võtta kuni 15 minutit.</span><span class="sxs-lookup"><span data-stu-id="fc175-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="fc175-112">Need makseteenuse sätted hõlmavad kaupmehe konto ID, pilve API võtme ja erinevate makseviisiga seotud konfiguratsioonisätete muudatusi.</span><span class="sxs-lookup"><span data-stu-id="fc175-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc175-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fc175-113">Additional resources</span></span>

[<span data-ttu-id="fc175-114">Võrgukanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="fc175-114">Set up an online channel</span></span>](../channel-setup-online.md)
