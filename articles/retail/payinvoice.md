---
title: Arve tasumise stsenaariumide seadistamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida rakendust Dynamics 365 for Retail, et see toetaks arve maksetega seotud erinevaid stsenaariume.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 53c4b9a9c9dac1add7021d909b2c8900d11e5c0c
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="d250f-103">Arve tasumise stsenaariumide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d250f-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d250f-104">Arve maksmise funktsiooni rakenduses Dynamics 365 for Retail on laiendatud, et see toetaks järgmist.</span><span class="sxs-lookup"><span data-stu-id="d250f-104">The Pay invoice functionality in Dynamics 365 for Retail has been expanded to support:</span></span>
- <span data-ttu-id="d250f-105">Mitme müügitellimuse arve tasumine ühe kassakandega.</span><span class="sxs-lookup"><span data-stu-id="d250f-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="d250f-106">Mitme kliendiarve tüübi makse, sh vabas vormis arved, projektipõhised arved ja kreeditarved.</span><span class="sxs-lookup"><span data-stu-id="d250f-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="d250f-107">Nende stsenaariumide lubamiseks tuleb kaupluste funktsiooniprofiili konfigureerida allpool kirjeldatud viisil.</span><span class="sxs-lookup"><span data-stu-id="d250f-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>  

1. <span data-ttu-id="d250f-108">Valige suvandid **Jaemüük > Kanali seadistus > Kassa seadistus > Kassa profiilid > Funktsiooniprofiilid** ja valige profiil, mis on seotud kauplustega, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="d250f-108">Go to **Retail > Channel setup > POS setup > POS profiles > Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>

1. <span data-ttu-id="d250f-109">Konfigureerige vahekaardil **Funktsioonid** vajaduse järgi järgmisi parameetreid.</span><span class="sxs-lookup"><span data-stu-id="d250f-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="d250f-110">**Müügitellimuse arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu müügitellimisel põhinevat arvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="d250f-110">**Sales order invoice** - Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>

    - <span data-ttu-id="d250f-111">**Vabas vormis arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu vabas vormis arvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="d250f-111">**Free text invoice** - Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>

    - <span data-ttu-id="d250f-112">**Projektiarve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu projektiarvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="d250f-112">**Project invoice** - Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>

    - <span data-ttu-id="d250f-113">**Müügitellimuse kreeditarve** – valige väärtus **Jah**, et lasta kasutajatel tasakaalustada mitu müügitellimusel põhinevat kreeditarvet avatud arvete suhtes või töödelda tagasimakset kliendile avatud kreeditarve jaoks.</span><span class="sxs-lookup"><span data-stu-id="d250f-113">**Sales order credit note** - Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="d250f-114">Osaliste summade makset või tasakaalustamist veel ei toetata.</span><span class="sxs-lookup"><span data-stu-id="d250f-114">Payment or settlement of partial amounts is not yet supported.</span></span>

