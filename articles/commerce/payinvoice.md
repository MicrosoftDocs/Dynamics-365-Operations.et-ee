---
title: Arve tasumise stsenaariumide seadistamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida rakendust Dynamics 365 Commerce, et see toetaks arve maksetega seotud erinevaid stsenaariume.
author: josaw1
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 08d3cf48c0bea6f0e13dda49e53b314a6037860d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804549"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="559e2-103">Arve tasumise stsenaariumide seadistamine</span><span class="sxs-lookup"><span data-stu-id="559e2-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="559e2-104">Arve maksmise funktsiooni rakenduses Dynamics 365 Commerce on laiendatud, et see toetaks järgmist.</span><span class="sxs-lookup"><span data-stu-id="559e2-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="559e2-105">Mitme müügitellimuse arve tasumine ühe kassakandega.</span><span class="sxs-lookup"><span data-stu-id="559e2-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="559e2-106">Mitme kliendiarve tüübi makse, sh vabas vormis arved, projektipõhised arved ja kreeditarved.</span><span class="sxs-lookup"><span data-stu-id="559e2-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="559e2-107">Nende stsenaariumide lubamiseks tuleb kaupluste funktsiooniprofiili konfigureerida allpool kirjeldatud viisil.</span><span class="sxs-lookup"><span data-stu-id="559e2-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="559e2-108">Valige suvandid **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid** ja valige profiil, mis on seotud kauplustega, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="559e2-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="559e2-109">Konfigureerige vahekaardil **Funktsioonid** vajaduse järgi järgmisi parameetreid.</span><span class="sxs-lookup"><span data-stu-id="559e2-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="559e2-110">**Müügitellimuse arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu müügitellimisel põhinevat arvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="559e2-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="559e2-111">**Vabas vormis arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu vabas vormis arvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="559e2-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="559e2-112">**Projektiarve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu projektiarvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="559e2-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="559e2-113">**Müügitellimuse kreeditarve** – valige väärtus **Jah**, et lasta kasutajatel tasakaalustada mitu müügitellimusel põhinevat kreeditarvet avatud arvete suhtes või töödelda tagasimakset kliendile avatud kreeditarve jaoks.</span><span class="sxs-lookup"><span data-stu-id="559e2-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="559e2-114">Osaliste summade makset või tasakaalustamist veel ei toetata.</span><span class="sxs-lookup"><span data-stu-id="559e2-114">Payment or settlement of partial amounts is not yet supported.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]