---
title: Alampearaamatu ülekandmine pearaamatusse
description: Selles teemas kirjeldatakse rakendusega Microsoft Dynamics 365 Finance seotud võimalusi alampearaamatu ülekandmiseks pearaamatusse.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000443"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="1b1c1-103">Alampearaamatu ülekandmine pearaamatusse</span><span class="sxs-lookup"><span data-stu-id="1b1c1-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b1c1-104">Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 Finance võimalusi, mis on seotud alampearaamatu töölehtede kirjete pakettide edastamise reeglitega.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="1b1c1-105">Versioonis 8.1 tehti muudatusi, et lubada reeglite edastamine, mis võimaldas sünkroonsel valikul aeguda.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the Synchronous option.</span></span> <span data-ttu-id="1b1c1-106">Lisateavet vt teemast [Rakenduse Finance and Operations eemaldatud või aegunud funktsioonid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="1b1c1-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="1b1c1-107">Alampearaamatu partiide edastamiseks on saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="1b1c1-108">Asünkroonne – see valik ajastab kohe alampearaamatu raamatupidamiskirjete edastamise pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="1b1c1-109">Pearaamatu kanne salvestatakse kohe, kui ressursid on vabad seda taotlust serveris töötlema.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="1b1c1-110">Plaanitud partii – see valik lisab alampearaamatu raamatupidamiskirjed, mis edastatakse pearaamatu töötlemise järjekorda, kus kandeid töödeldakse saabumise järjekorras.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="1b1c1-111">Pearaamatu kanne salvestatakse planeeritud ajal, kui ressursid on vabad seda pakett-tööd serveris töötlema.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="1b1c1-112">Versiooni 10.0.8 tehti parandusi asünkroonse valiku jõudluse suurendamiseks.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchrounous option.</span></span> <span data-ttu-id="1b1c1-113">See funktsioon on lubatud selle funktsiooni nimega **Alampearaamatu edastamine pearaamatu jõudluse optimeerimiseks**.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="1b1c1-114">See funktsioon parandab andmeedastust alampearaamatust pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="1b1c1-115">See võimaldab protsessi tõhustada ja see rühmitab edastamiseks väiksemate kannete kogumid.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="1b1c1-116">See võimaldab pakktöötlusserveri tõhusamat kasutamist.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="1b1c1-117">Selle funktsiooni kasutamiseks peab pakktöötlusserver olema seadistatud, võrgus ja toimima, et asünkroonse edastamise valik töötaks.</span><span class="sxs-lookup"><span data-stu-id="1b1c1-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchrounous transfer option to work.</span></span> 