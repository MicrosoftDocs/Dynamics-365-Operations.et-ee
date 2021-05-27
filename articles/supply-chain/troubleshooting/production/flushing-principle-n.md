---
title: Koosluseridade automaatse tarbimise põhimõtte sätteid ei järgita
description: Koosluseridade automaatse tarbimise põhimõtte sätteid ei järgita.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026441"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="66e9d-103">Koosluseridade automaatse tarbimise põhimõtte sätteid ei järgita</span><span class="sxs-lookup"><span data-stu-id="66e9d-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="66e9d-104">KB number: 4612725</span><span class="sxs-lookup"><span data-stu-id="66e9d-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="66e9d-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="66e9d-105">Symptoms</span></span>

<span data-ttu-id="66e9d-106">See probleem ilmneb, kui **Automaatse koosluse tarbimise** väli **Automaatse värskendamise** vahekaardil **Tootmise juhtimise parameetrite** lehel on seadistatud kui *Juhtimispõhimõte*.</span><span class="sxs-lookup"><span data-stu-id="66e9d-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="66e9d-107">See säte näitab, et ostutellimuse saades tuleb automaatselt tarbida kõiki koosluseridu.</span><span class="sxs-lookup"><span data-stu-id="66e9d-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="66e9d-108">Kui koosluseridade **juhtmispõhimõtte** väli on eraldi seatud väärtusele *Käsitsi*, võite eeldada, et koosluseridu ei tarbita automaatselt.</span><span class="sxs-lookup"><span data-stu-id="66e9d-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="66e9d-109">Kui see probleem ilmneb, tarbitakse siiski automaatselt koosluseridu, kus **Juhtimispõhimõtte** väli väärtuseks on määratud *Käsitsi*.</span><span class="sxs-lookup"><span data-stu-id="66e9d-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="66e9d-110">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="66e9d-110">Resolution</span></span>

<span data-ttu-id="66e9d-111">Kui teil tekib selline probleem, võivad teie tootmise juhtimise parameetrid olla seadistatud alluma **Juhtmispõhimõtte** sätetele koosluse ridadel.</span><span class="sxs-lookup"><span data-stu-id="66e9d-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="66e9d-112">Kontrollige **Tootmise juhtimise parameetrid** lehel **Automaatse uuendamise** vahekaardil **Automaatne koosluse** tarbimine väärtust.</span><span class="sxs-lookup"><span data-stu-id="66e9d-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="66e9d-113">Kui sätteks *Alati* ignoreerib süsteem kõigi koosluseridade **Juhtmispõhimõtte** sätet ja tühjendab alati.</span><span class="sxs-lookup"><span data-stu-id="66e9d-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="66e9d-114">Süsteemi koosluseridade **Juhtmispõhimõttele** allutamiseks muutke välja **Automaatne koosluse** *Juhtmispõhimõtteks*.</span><span class="sxs-lookup"><span data-stu-id="66e9d-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>
