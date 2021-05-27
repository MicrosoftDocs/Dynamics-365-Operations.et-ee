---
title: Aruande tühistamine lõpetatuna loob ootamatu avatud kande
description: Märgistusega lõppenud aruandluse tühistamine loob avatud tehingu, kus vastupidisel kogusel on samad varude mõõtmed kui vastupidisel tehingul.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026451"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="e0cbf-103">Aruande tühistamine lõpetatuna loob ootamatu avatud kande</span><span class="sxs-lookup"><span data-stu-id="e0cbf-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="e0cbf-104">KB number: 4612469</span><span class="sxs-lookup"><span data-stu-id="e0cbf-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="e0cbf-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="e0cbf-105">Symptoms</span></span>

<span data-ttu-id="e0cbf-106">Märgistusega lõppenud aruandluse tühistamine loob avatud tehingu, kus vastupidisel kogusel on samad varude mõõtmed kui tühistatud tehingul.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="e0cbf-107">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="e0cbf-107">Resolution</span></span>

<span data-ttu-id="e0cbf-108">Kui tühistate aruande kui lõpetatud toimingu, lähtestatakse tootmisdokumentatsioonist varude mõõde.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="e0cbf-109">Seetõttu lähtestatakse partiinumber.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="e0cbf-110">Märkimise tõttu pärivad müügitellimuse kanded partiinumbri.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="e0cbf-111">Dimensiooni saab lähtestada, kui sisestatakse lõpetatuna kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="e0cbf-111">The dimension can be reset when the reporting as finished is posted.</span></span>
