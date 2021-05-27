---
title: Pearaamatu vaikekirjeldused
description: Vaikekirjeldusi saate kasutada kande sisestuste välja Kirjeldus uuendamiseks pearaamatusse.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021608"
---
# <a name="default-descriptions-for-the-general-ledger"></a><span data-ttu-id="8b505-103">Pearaamatu vaikekirjeldused</span><span class="sxs-lookup"><span data-stu-id="8b505-103">Default descriptions for the general ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b505-104">Vaikekirjeldusi saate kasutada kande sisestuste välja **Kirjeldus** uuendamiseks pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="8b505-104">Default descriptions can be used to update the **Description** field in voucher postings to the general ledger.</span></span> <span data-ttu-id="8b505-105">Seda funktsiooni on täiustatud väljalaadimiskuluga töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="8b505-105">This functionality has been enhanced to work with Landed cost.</span></span>

<span data-ttu-id="8b505-106">Pearaamatu sisestuste vaikekirjelduste häälestamiseks valige **Organisatsiooni haldus \> Häälestamine \> Vaikekirjeldused**.</span><span class="sxs-lookup"><span data-stu-id="8b505-106">To set up default descriptions for ledger postings, go to **Organizational administration \> Setup \> Default descriptions**.</span></span>

<span data-ttu-id="8b505-107">Järgmises tabelis loetletakse uued väärtused, mis on lisatud lehe **Vaikekirjeldused** väljale **Kirjeldus**, et toetada väljalaadimiskulu.</span><span class="sxs-lookup"><span data-stu-id="8b505-107">The following table lists the new values that have been added for the **Description** field on the **Default descriptions** page to support Landed cost.</span></span>

| <span data-ttu-id="8b505-108">Kirjelduse tüüp</span><span class="sxs-lookup"><span data-stu-id="8b505-108">Description type</span></span> | <span data-ttu-id="8b505-109">Märkmed</span><span class="sxs-lookup"><span data-stu-id="8b505-109">Notes</span></span> |
|---|---|
| <span data-ttu-id="8b505-110">Impordi kuluarvutus – kulu juurdekasv</span><span class="sxs-lookup"><span data-stu-id="8b505-110">Import costing – Cost accrual</span></span> | <span data-ttu-id="8b505-111">Ostutellimuse arve sisestamisel töödeldakse kulude juurdekavu teekonna hinnanguliste kulude osas.</span><span class="sxs-lookup"><span data-stu-id="8b505-111">When a purchase order invoice is posted, a cost accrual is processed for estimate voyage costs.</span></span> <span data-ttu-id="8b505-112">Saate määrata vaikekirjeldused, et lisada kirjeldusele teekonna numbri.</span><span class="sxs-lookup"><span data-stu-id="8b505-112">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="8b505-113">Kasutage *%4* saadetise numbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="8b505-113">Use *%4* for the shipment number.</span></span> |
| <span data-ttu-id="8b505-114">Impordi kuluarvutus – kaubad transiittellimuses</span><span class="sxs-lookup"><span data-stu-id="8b505-114">Import costing – Goods in transit order</span></span> | <span data-ttu-id="8b505-115">Kui kasutate transiidi töötlust, sisestatakse ostutellimuse arve ja kaubad sisestatakse transiidikonto kaupadele.</span><span class="sxs-lookup"><span data-stu-id="8b505-115">If you're using in-transit processing, the purchase order invoice is posted, and the goods are posted to a goods in transit account.</span></span> <span data-ttu-id="8b505-116">Saate määrata vaikekirjeldused, et lisada kirjeldusele transiittellimuse numbri.</span><span class="sxs-lookup"><span data-stu-id="8b505-116">Default descriptions can be specified to add the in-transit order number to the description.</span></span> <span data-ttu-id="8b505-117">Kasutage *%4* transiittellimuse numbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="8b505-117">Use *%4* for the in-transit order number.</span></span> |
| <span data-ttu-id="8b505-118">Ladu - sulgemine - korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="8b505-118">Inventory – close – adjustment</span></span> | <span data-ttu-id="8b505-119">Kui ostureskontro (AP) arvet töödeldakse teekonna kulu jaoks, töödeldakse varude korrigeerimist teekonna kulude prognoosimiseks.</span><span class="sxs-lookup"><span data-stu-id="8b505-119">When the accounts payable (AP) invoice is processed for a voyage cost, an inventory adjustment is processed to estimate voyage costs.</span></span> <span data-ttu-id="8b505-120">Saate määrata vaikekirjeldused, et lisada kirjeldusele teekonna numbri.</span><span class="sxs-lookup"><span data-stu-id="8b505-120">Default descriptions can be specified to add the voyage number to the description.</span></span> <span data-ttu-id="8b505-121">Kasutage *%4* saadetise numbri jaoks.</span><span class="sxs-lookup"><span data-stu-id="8b505-121">Use *%4* for the shipment number.</span></span> |

<span data-ttu-id="8b505-122">Lisateavet lehe **Vaikekirjeldused** kasutamise kohta vt teemat [Automaatse sisestamise vaikekirjelduste häälestamine](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span><span class="sxs-lookup"><span data-stu-id="8b505-122">For more information about how to work with the **Default descriptions** page, see [Set up default descriptions for automatic posting](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).</span></span>
