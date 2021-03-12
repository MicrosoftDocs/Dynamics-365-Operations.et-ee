---
title: Viitvõlaskeemide loomine
description: Selles teemas selgitatakse, kuidas luua viitvõlaskeeme.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAccrualTable
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457be741dfd3b44cb963db37857d6a7bceecc14e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994661"
---
# <a name="create-accrual-schemes"></a><span data-ttu-id="3810d-103">Viitvõlaskeemide loomine</span><span class="sxs-lookup"><span data-stu-id="3810d-103">Create accrual schemes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3810d-104">Selles teemas selgitatakse, kuidas luua viitvõlaskeeme.</span><span class="sxs-lookup"><span data-stu-id="3810d-104">This topic explains how to create an accrual scheme.</span></span> <span data-ttu-id="3810d-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="3810d-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="3810d-106">Avage **Navigeerimispaan > Moodulid > Pearaamat > Töölehe seadistus > Viitvõlaskeemid**.</span><span class="sxs-lookup"><span data-stu-id="3810d-106">Go to **Navigation pane > Modules > General ledger > Journal setup > Accrual schemes**.</span></span>
2. <span data-ttu-id="3810d-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="3810d-107">Select **New**.</span></span>
3. <span data-ttu-id="3810d-108">Väljale **Viitvõla ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="3810d-108">In the **Accrual identification** field, type a value.</span></span>
4. <span data-ttu-id="3810d-109">Väljale **Viitvõlaskeemi kirjeldus** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="3810d-109">In the **Description of accrual scheme** field, type a value.</span></span>
5. <span data-ttu-id="3810d-110">Väljal **Deebet** täpsustage soovitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="3810d-110">In the **Debit** field, specify the desired values.</span></span> <span data-ttu-id="3810d-111">Määratletud põhikonto asendab deebeti põhikonto töölehe kandereal ja seda kasutatakse ka viitvõla tühistamiseks pearaamatu tekkepõhiste kannete põhjal.</span><span class="sxs-lookup"><span data-stu-id="3810d-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="3810d-112">Väljal **Kreedit** täpsustage soovitud väärtust.</span><span class="sxs-lookup"><span data-stu-id="3810d-112">In the **Credit** field, specify the desired values.</span></span> <span data-ttu-id="3810d-113">Määratletud põhikonto asendab kreediti põhikonto töölehe kandereal ja seda kasutatakse ka viitvõla tühistamiseks pearaamatu tekkepõhiste kannete põhjal.</span><span class="sxs-lookup"><span data-stu-id="3810d-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="3810d-114">Väljal **Sooduskood** valige kuidas soovite, et sooduskood tuvastatakse kui kanded on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="3810d-114">In the **Voucher** field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="3810d-115">Väljale **Kirjeldus** sisestage väärtus, mis kirjeldab sisestatud kandeid.</span><span class="sxs-lookup"><span data-stu-id="3810d-115">In the **Description** field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="3810d-116">Väljal **Perioodi sagedus** valige, kui sageli soovite, et kanded esineks.</span><span class="sxs-lookup"><span data-stu-id="3810d-116">In the **Period frequency** field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="3810d-117">Väljale **Juhtumite arv perioodide kaupa** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="3810d-117">In the **Number of occurrences by period** field, enter a number.</span></span>
11. <span data-ttu-id="3810d-118">Väljal **Sisesta kanded** valige, millal kandeid peaks postitama, näiteks **Iga kuu**.</span><span class="sxs-lookup"><span data-stu-id="3810d-118">In the **Post transactions** field, select when the transactions should be posted, such as **Monthly**.</span></span>

