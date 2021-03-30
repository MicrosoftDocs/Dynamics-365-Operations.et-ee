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
ms.openlocfilehash: d1abd942da608bc221a7a66e03b5269fa30e2c20
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212026"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="ee0b6-103">Ostutellimuse loomine ühekordse tarnija jaoks</span><span class="sxs-lookup"><span data-stu-id="ee0b6-103">Create a purchase order for a one-time supplier</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee0b6-104">Selles protseduuris selgitatakse, kuidas luua ostutellimus ühekordsele hankijale.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-104">This procedure shows you how to create a purchase order for a one-time supplier.</span></span> <span data-ttu-id="ee0b6-105">Hankija luuakse automaatselt koos ostutellimusega, hankija kontot pole vaja käsitsi luua.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-105">The supplier is created automatically with the purchase order, rather than having to create the vendor account manually.</span></span> <span data-ttu-id="ee0b6-106">Ostutellimused loob tavaliselt ostuagent.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-106">Purchase orders are typically created by a purchasing agent.</span></span> <span data-ttu-id="ee0b6-107">Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="ee0b6-108">Eeltingimuseks on, et ühekordse hankija konto on seadistatud lehel Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-108">It is a prerequisite that a one-time vendor account has been set up in the Account payable parameters page.</span></span>


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a><span data-ttu-id="ee0b6-109">Ostutellimuse loomine ühekordse tarnija jaoks</span><span class="sxs-lookup"><span data-stu-id="ee0b6-109">Create a purchase order for a one-time supplier</span></span>
1. <span data-ttu-id="ee0b6-110">Avage Hanked > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-110">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="ee0b6-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-111">Click New.</span></span>
3. <span data-ttu-id="ee0b6-112">Tehke väljal Ühekordne hankija valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-112">Select Yes in the One-time supplier field.</span></span>
    * <span data-ttu-id="ee0b6-113">Hankija konto luuakse automaatselt ja määratakse ostutellimusele.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-113">A vendor account is automatically created and assigned to the purchase order.</span></span> <span data-ttu-id="ee0b6-114">Hankija konto luuakse lehe Ostureskontro parameetrid vahekaardil Üldine määratud malli põhjal.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-114">The vendor account is created based on the template that is specified on the General tab in the Accounts payable parameters page.</span></span>  
4. <span data-ttu-id="ee0b6-115">Sisestage väljale Nimi hankija nimi.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-115">In the Name field, type a name for the supplier.</span></span>
5. <span data-ttu-id="ee0b6-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-116">Click OK.</span></span>
    * <span data-ttu-id="ee0b6-117">Ostutellimuse saab nüüd lõpetada ja seda saab töödelda, nagu iga teist tellimust.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-117">The purchase order can now be completed and processed like any other order.</span></span> <span data-ttu-id="ee0b6-118">Selle tegemiseks pole mingeid erijuhiseid.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-118">There are no special characteristics related to how this is done.</span></span> <span data-ttu-id="ee0b6-119">Arvel kajastub tellimusega koos loodud hankija kontol toimuv kanne ja seejärel töödeldakse makse.</span><span class="sxs-lookup"><span data-stu-id="ee0b6-119">The invoice will account a due transaction on the vendor account that was created with the order, and payment will then be processed.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]