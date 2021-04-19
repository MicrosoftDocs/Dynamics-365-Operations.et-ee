---
title: Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui makseviisi jaotist ei laadita ja kuvatakse tõrketeade.
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
ms.openlocfilehash: d2c5f01d17df79c9b23fd513aaeb5c0605d657e9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801767"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a><span data-ttu-id="93632-103">Krediitkaardi sisestamise lehel kuvatakse väljaregistreerimisel tõrge</span><span class="sxs-lookup"><span data-stu-id="93632-103">Credit card entry page shows an error at checkout</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93632-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui **makseviisi jaotist** ei laadita ja kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="93632-104">This topic provides troubleshooting guidance that can help when the **Payment method** section isn't loaded and shows an error message.</span></span>

## <a name="description"></a><span data-ttu-id="93632-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="93632-105">Description</span></span>

<span data-ttu-id="93632-106">Kui avate e-poe väljaregistreerimise lehekülje, ei laadita **makseviisi jaotist** ja kuvatakse järgmine tõrketeade: "Midagi läks valesti.</span><span class="sxs-lookup"><span data-stu-id="93632-106">When you open the checkout page of an online store, the **Payment method** section isn't loaded, and the following error message is shown: "Something went wrong.</span></span> <span data-ttu-id="93632-107">Proovige hiljem uuesti.”</span><span class="sxs-lookup"><span data-stu-id="93632-107">Please try again later."</span></span>

![Maksemooduli tõrge](media/payment-module-error.jpg)

## <a name="resolution"></a><span data-ttu-id="93632-109">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="93632-109">Resolution</span></span>

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a><span data-ttu-id="93632-110">Oodake, kuni Commerce Scale Unit vahemälu aegub</span><span class="sxs-lookup"><span data-stu-id="93632-110">Wait for the Commerce Scale Unit cache to expire</span></span>

<span data-ttu-id="93632-111">E-poe väljaregistreerimise lehel olevad makseteenuse sätted salvestatakse vahemällu Commerce Scale Unit ja selle kuvamiseks e-kaubanduse saidil võib aega võtta kuni 15 minutit.</span><span class="sxs-lookup"><span data-stu-id="93632-111">The payment service settings on the online store's checkout page are cached on the Commerce Scale Unit and can take up to 15 minutes to appear on the e-commerce site.</span></span> <span data-ttu-id="93632-112">Need makseteenuse sätted hõlmavad kaupmehe konto ID, pilve API võtme ja erinevate makseviisiga seotud konfiguratsioonisätete muudatusi.</span><span class="sxs-lookup"><span data-stu-id="93632-112">These payment service settings include changes to the merchant account ID, cloud API key, and various configuration settings that are related to the payment method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93632-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="93632-113">Additional resources</span></span>

[<span data-ttu-id="93632-114">Võrgukanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="93632-114">Set up an online channel</span></span>](../channel-setup-online.md)
