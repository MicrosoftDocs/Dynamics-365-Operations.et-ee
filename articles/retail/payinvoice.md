---
title: Arve tasumise stsenaariumide seadistamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida rakendust Dynamics 365 Retail, et see toetaks arve maksetega seotud erinevaid stsenaariume.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4fb9101843396e489e4d7b63879e9df35e52fe64
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2018009"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="2cf97-103">Arve tasumise stsenaariumide seadistamine</span><span class="sxs-lookup"><span data-stu-id="2cf97-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2cf97-104">Arve maksmise funktsiooni rakenduses Dynamics 365 Retail on laiendatud, et see toetaks järgmist.</span><span class="sxs-lookup"><span data-stu-id="2cf97-104">The Pay invoice functionality in Dynamics 365 Retail has been expanded to support:</span></span>

- <span data-ttu-id="2cf97-105">Mitme müügitellimuse arve tasumine ühe kassakandega.</span><span class="sxs-lookup"><span data-stu-id="2cf97-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="2cf97-106">Mitme kliendiarve tüübi makse, sh vabas vormis arved, projektipõhised arved ja kreeditarved.</span><span class="sxs-lookup"><span data-stu-id="2cf97-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="2cf97-107">Nende stsenaariumide lubamiseks tuleb kaupluste funktsiooniprofiili konfigureerida allpool kirjeldatud viisil.</span><span class="sxs-lookup"><span data-stu-id="2cf97-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="2cf97-108">Valige suvandid **Jaemüük \> Kanali seadistus \> Kassa seadistus \> Kassa profiilid \> Funktsiooniprofiilid** ja valige profiil, mis on seotud kauplustega, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="2cf97-108">Go to **Retail \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="2cf97-109">Konfigureerige vahekaardil **Funktsioonid** vajaduse järgi järgmisi parameetreid.</span><span class="sxs-lookup"><span data-stu-id="2cf97-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="2cf97-110">**Müügitellimuse arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu müügitellimisel põhinevat arvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="2cf97-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="2cf97-111">**Vabas vormis arve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu vabas vormis arvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="2cf97-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="2cf97-112">**Projektiarve** – valige väärtus **Jah**, et lasta kasutajatel maksta üks või mitu projektiarvet ühes kassakandes.</span><span class="sxs-lookup"><span data-stu-id="2cf97-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="2cf97-113">**Müügitellimuse kreeditarve** – valige väärtus **Jah**, et lasta kasutajatel tasakaalustada mitu müügitellimusel põhinevat kreeditarvet avatud arvete suhtes või töödelda tagasimakset kliendile avatud kreeditarve jaoks.</span><span class="sxs-lookup"><span data-stu-id="2cf97-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="2cf97-114">Osaliste summade makset või tasakaalustamist veel ei toetata.</span><span class="sxs-lookup"><span data-stu-id="2cf97-114">Payment or settlement of partial amounts is not yet supported.</span></span>
