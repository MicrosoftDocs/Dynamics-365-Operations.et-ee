---
title: Viga aruande lõpetamise päevikuna postitamisel
description: Kui postitate aruande lõpetatud päevikuna, kuvatakse tõrketeade, mis ütleb, et tellitud tellitud kogust ei saa vähendada.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026428"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a><span data-ttu-id="b3350-103">Viga aruande lõpetamise päevikuna postitamisel</span><span class="sxs-lookup"><span data-stu-id="b3350-103">Error when the Report as finished journal is posted</span></span>

<span data-ttu-id="b3350-104">KB number: 4612891</span><span class="sxs-lookup"><span data-stu-id="b3350-104">KB number: 4612891</span></span>

## <a name="symptoms"></a><span data-ttu-id="b3350-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="b3350-105">Symptoms</span></span>

<span data-ttu-id="b3350-106">Töölehe **Lõpetatuna kinnitatud** sisestamisel ilmneb tõrge ja kuvatakse järgmine tõrketeade:</span><span class="sxs-lookup"><span data-stu-id="b3350-106">When you post the **Report as finished** journal, an error occurs, and you receive the following error message:</span></span>

> <span data-ttu-id="b3350-107">Tellitud kogust ei saa vähendada, kuna pole piisavalt avatud laokandeid, mille olek on Tellitud.</span><span class="sxs-lookup"><span data-stu-id="b3350-107">Quantity ordered cannot be reduced because there are not enough open inventory transactions with the ordered status.</span></span> <span data-ttu-id="b3350-108">Kaubad on ostetud, saadud või registreeritud.</span><span class="sxs-lookup"><span data-stu-id="b3350-108">The items are Purchased, Received or Registered.</span></span>

<span data-ttu-id="b3350-109">See tõrge ilmneb ainult siis, kui väli **Veakogus** on seadistatud esimesele **Lõpetatuna kinnitatud** reale ja **Hea kogus** väli on seadistatud viimasele reale.</span><span class="sxs-lookup"><span data-stu-id="b3350-109">This error occurs only when the **Error quantity** field is set on the first line of the **Report as finished** journal, and the **Good quantity** field is set on the last line.</span></span> <span data-ttu-id="b3350-110">Kui **Veakogus** väli on seadistatudviimasele reale, siis tõrkeid ei esine.</span><span class="sxs-lookup"><span data-stu-id="b3350-110">If the **Error quantity** field is set on the last line, no error occurs.</span></span>

## <a name="resolution"></a><span data-ttu-id="b3350-111">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="b3350-111">Resolution</span></span>

<span data-ttu-id="b3350-112">Tõrke vältimiseks avage **Tootmise juhtimise parameetrite** leht ja seejärel seadke seal **Üldine** vahekaardil suvandi **Kasvu püsikogus tõrkekogusega** väärtusele *Jah*.</span><span class="sxs-lookup"><span data-stu-id="b3350-112">To prevent this error, open the **Production control parameters** page, and then, on the **General** tab, set the **Increase remain qty with error qty** option to *Yes*.</span></span>
