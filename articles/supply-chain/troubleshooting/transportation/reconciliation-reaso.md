---
title: Põhikonto saab krediidikontona lisada ainult vastavussebviimise põhjustel
description: Transpordihalduses vastavussebviimise põhjuse häälestamisel saate kreeditkontoks lisada ainult põhikonto.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026425"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="50303-103">Põhikonto saab krediidikontona lisada ainult vastavussebviimise põhjustel</span><span class="sxs-lookup"><span data-stu-id="50303-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="50303-104">KB number: 4603538</span><span class="sxs-lookup"><span data-stu-id="50303-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="50303-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="50303-105">Symptoms</span></span>

<span data-ttu-id="50303-106">Transpordihalduses vastavussebviimise põhjuse häälestamisel saate kreeditkontoks lisada ainult põhikonto.</span><span class="sxs-lookup"><span data-stu-id="50303-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="50303-107">Te ei saa krediidikontona lisada kulukeskust ega muid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="50303-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="50303-108">Deebetkonto võimaldab teil siiski valida teisi dimensioone.</span><span class="sxs-lookup"><span data-stu-id="50303-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="50303-109">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="50303-109">Resolution</span></span>

<span data-ttu-id="50303-110">Kui vastavusseviimine ei ole hankijale maksmiseks, vaid kindla põhikonto krediteerimiseks, ei luba süsteem teil vastavusseviimise põhjuse häälestamisel valida kreeditkonto jaoks rahalist mõõdet.</span><span class="sxs-lookup"><span data-stu-id="50303-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="50303-111">Kui konto struktuur nõuab kreediti põhikonto jaoks kindlat finantsdimensiooni väärtust, ei saa tulemuseks saadud hankija töölehte automaatselt sisestada, kuna finantsdimensiooni väärtus puudub.</span><span class="sxs-lookup"><span data-stu-id="50303-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="50303-112">Seega peate esmalt käsitsi määrama kreeditkonto, kasutades **Arve tööleht** lehte.</span><span class="sxs-lookup"><span data-stu-id="50303-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="50303-113">Kuna kreeditkonto jaoks on vajalik dimensiooniväärtus, ei saa hankija arve töölehte automaatselt sisestada.</span><span class="sxs-lookup"><span data-stu-id="50303-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="50303-114">Pärast dimensiooniväärtuse käsitsi sisestamist peate selle krediidirea põhikontole lisama.</span><span class="sxs-lookup"><span data-stu-id="50303-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
