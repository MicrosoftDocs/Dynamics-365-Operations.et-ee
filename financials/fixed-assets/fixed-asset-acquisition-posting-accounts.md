---
title: "Põhivara soetamise sisestuskontod"
description: Selles artiklis selgitatakse, kuidas seadistada pearaamatu sisestuskontosid varade omandamiseks.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 887616463856875e2382a00b1d56520391ead844
ms.contentlocale: et-ee
ms.lasthandoff: 06/29/2017


---

# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="38fbb-103">Põhivara soetamise sisestuskontod</span><span class="sxs-lookup"><span data-stu-id="38fbb-103">Fixed asset acquisition posting accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="38fbb-104">Selles artiklis selgitatakse, kuidas seadistada pearaamatu sisestuskontosid varade omandamiseks.</span><span class="sxs-lookup"><span data-stu-id="38fbb-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="38fbb-105">Põhivara soetamisel kasutatavad kontod võivad erineda, olenevalt vara soetamiseks kasutatavast meetodist.</span><span class="sxs-lookup"><span data-stu-id="38fbb-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="38fbb-106">Tehke lehel Põhivara sisestusreeglid vahekaardil Pearaamatukontod valikud Soetus ja Soetuse korrigeerimine pearaamatusse sisestatavate põhivarakontode seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="38fbb-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="38fbb-107">Tavaliselt on töölehtedel ja ostutellimustel uue põhivara soetamisväärtuse debiteerimisel pearaamatukontoks bilansikonto.</span><span class="sxs-lookup"><span data-stu-id="38fbb-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="38fbb-108">Seda kontot ei kuvata tavaliselt töölehtedel ning seda ei saa kannete sisestamisel asendada.</span><span class="sxs-lookup"><span data-stu-id="38fbb-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="38fbb-109">Vastaskonto on samuti bilansikonto.</span><span class="sxs-lookup"><span data-stu-id="38fbb-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="38fbb-110">Pearaamatu ja põhivara töölehtedel on selleks kontoks tavaliselt pangakonto, mida kasutatakse põhivara soetamisel.</span><span class="sxs-lookup"><span data-stu-id="38fbb-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="38fbb-111">Vastaskontoks on töölehtedel pakutav vaikekonto.</span><span class="sxs-lookup"><span data-stu-id="38fbb-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="38fbb-112">Seda saab vahetada töölehel ükskõik millise kontoplaanis oleva konto või hankija konto vastu, kui põhivara osteti hankijalt.</span><span class="sxs-lookup"><span data-stu-id="38fbb-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="38fbb-113">Kui põhivara soetamisel kasutatakse ostureskontro lehte Arve tööleht või Ostutellimused, asendatakse põhivarakande vastaskonto kande puhul valitud hankija kontoga.</span><span class="sxs-lookup"><span data-stu-id="38fbb-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="38fbb-114">Mooduli Pearaamat töölehe Põhivara varud kaudu sisestatud soetamiste puhul pole põhivara ostetud välistest allikatest, vaid on toodud üle ettevõtte laost.</span><span class="sxs-lookup"><span data-stu-id="38fbb-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="38fbb-115">Seepärast kasutatakse vastaskontona laokauba väljamineku kontot moodulis Laohaldus.</span><span class="sxs-lookup"><span data-stu-id="38fbb-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="38fbb-116">Lisateavet leiate jaotisest [Varade soetamine hankega](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="38fbb-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>




