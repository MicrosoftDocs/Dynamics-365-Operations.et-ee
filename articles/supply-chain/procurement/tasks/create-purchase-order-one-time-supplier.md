---
title: Ostutellimuse loomine ühekordse tarnija jaoks
description: Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c4885547cdf2f8496446761e27ce39e67e670f15
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016398"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="52f81-103">Ostutellimuse loomine ühekordse tarnija jaoks</span><span class="sxs-lookup"><span data-stu-id="52f81-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52f81-104">Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale.</span><span class="sxs-lookup"><span data-stu-id="52f81-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="52f81-105">Hankija luuakse automaatselt koos ostutellimusega, hankija kontot pole vaja käsitsi luua.</span><span class="sxs-lookup"><span data-stu-id="52f81-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="52f81-106">Ostutellimused loob tavaliselt ostuagent.</span><span class="sxs-lookup"><span data-stu-id="52f81-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="52f81-107">Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul.</span><span class="sxs-lookup"><span data-stu-id="52f81-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="52f81-108">Eeltingimuseks on, et ühekordse hankija konto on seadistatud lehel Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="52f81-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="52f81-109">Ostutellimuse loomine ühekordse tarnija jaoks</span><span class="sxs-lookup"><span data-stu-id="52f81-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="52f81-110">Avage Hanked > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="52f81-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="52f81-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="52f81-111">Click New.</span></span>
3. <span data-ttu-id="52f81-112">Tehke väljal Ühekordne hankija valik Jah.</span><span class="sxs-lookup"><span data-stu-id="52f81-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="52f81-113">Hankija konto luuakse automaatselt ja määratakse ostutellimusele.</span><span class="sxs-lookup"><span data-stu-id="52f81-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="52f81-114">Hankija konto luuakse lehe Ostureskontro parameetrid vahekaardil Üldine määratud malli põhjal.</span><span class="sxs-lookup"><span data-stu-id="52f81-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="52f81-115">Sisestage väljale Nimi hankija nimi.</span><span class="sxs-lookup"><span data-stu-id="52f81-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="52f81-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52f81-116">Click OK.</span></span>
    * <span data-ttu-id="52f81-117">Ostutellimuse saab nüüd lõpetada ja seda saab töödelda, nagu iga teist tellimust.</span><span class="sxs-lookup"><span data-stu-id="52f81-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="52f81-118">Selle tegemiseks pole mingeid erijuhiseid.</span><span class="sxs-lookup"><span data-stu-id="52f81-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="52f81-119">Arvel kajastub tellimusega koos loodud hankija kontol toimuv kanne ja seejärel töödeldakse makse.</span><span class="sxs-lookup"><span data-stu-id="52f81-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>

