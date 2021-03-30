---
title: Sisestatud rendikannete tühistamine
description: See teema selgitab, kuidas sisestatud rendikannet muuta. Kõiki vara rentimise kaudu loodud kandeid saab tühistada.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 22d8eee22221efaf5e7a715c8b95dff261bee62f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249721"
---
# <a name="reverse-posted-lease-transactions"></a><span data-ttu-id="860b9-104">Sisestatud rendikannete tühistamine</span><span class="sxs-lookup"><span data-stu-id="860b9-104">Reverse posted lease transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="860b9-105">Kõiki vara rentimise kaudu loodud kandeid saab tühistada.</span><span class="sxs-lookup"><span data-stu-id="860b9-105">Any transaction that is created through Asset leasing can be reversed.</span></span> <span data-ttu-id="860b9-106">Kanded, mis on tühistatud vara rentimise jaotuse kaudu värskendavad teie rendilepingu andmeid.</span><span class="sxs-lookup"><span data-stu-id="860b9-106">Transactions that are reversed through Asset leasing update your lease data.</span></span> <span data-ttu-id="860b9-107">Seetõttu värskendavad nad ka rendikohustise ja kasutamisõiguse esemeks oleva vara bilansilist väärtust.</span><span class="sxs-lookup"><span data-stu-id="860b9-107">Therefore, they also update the carrying values of the lease liability and right-of-use (ROU) asset.</span></span>

<span data-ttu-id="860b9-108">Rendi tühistamise kande loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="860b9-108">To create a reversing transaction for a lease, follow these steps.</span></span>

1. <span data-ttu-id="860b9-109">Valige kas lehel **Vara kanded** või **Kohustuste kanded** kanne ja seejärel valige käsk **Tühista kanne**.</span><span class="sxs-lookup"><span data-stu-id="860b9-109">On either the **Asset transactions** page or the **Liability transactions** page, select the transaction, and then select **Reverse transaction**.</span></span>
2. <span data-ttu-id="860b9-110">Kuvatavas dialoogiboksis saate redigeerida kuupäeva, millal tühistamise kanne sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="860b9-110">In the dialog box that appears, you can edit the date when the reversing entry will be posted.</span></span> <span data-ttu-id="860b9-111">Vaikimisi on väli **Kuupäev** seadistatud valitud kande sisestamise kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="860b9-111">By default, the **Date** field is set to the transaction posting date of the transaction that you selected.</span></span> <span data-ttu-id="860b9-112">Tühistamise kirjet ei saa sisestada enne valitud kande algset sisestamiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="860b9-112">The reversing entry can't be posted earlier than the original posting date of the selected transaction.</span></span>
3. <span data-ttu-id="860b9-113">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="860b9-113">Select **OK**.</span></span> <span data-ttu-id="860b9-114">Sisestatakse töölehe kirje, mis tühistab valitud kirje.</span><span class="sxs-lookup"><span data-stu-id="860b9-114">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="860b9-115">Tühistamine kuvatakse kas lehel **Vara kanded** või **Kohustuste kanded** ja lehel kuvatav praeguse saldo netosumma värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="860b9-115">The reversal is shown on the **Asset transactions** or **Liability transactions** page, and the net total of the current balance that is shown on the page is updated.</span></span>

<span data-ttu-id="860b9-116">Kui valite käsu **Tühista jälitus**, kuvatakse dialoogiboks, kus kuvatakse nii algsed kui ka tühistatud kanded, koos lingitud numbriga, mida nimetatakse *jälgimisnumbriks*.</span><span class="sxs-lookup"><span data-stu-id="860b9-116">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked number that is known as a *trace number*.</span></span> <span data-ttu-id="860b9-117">Tühistamise lihtsustamiseks ja nähtavuse parandamiseks saate tühistamisi jälgida ka rendigraafikute abil.</span><span class="sxs-lookup"><span data-stu-id="860b9-117">To make the reversals easier to understand and to improve visibility, you can also track reversals by using the lease schedules.</span></span>

<span data-ttu-id="860b9-118">Väli **Viimase töölehe number** lehel **Graafik** näitab kannete töölehe numbreid.</span><span class="sxs-lookup"><span data-stu-id="860b9-118">The **Latest journal number** field on the **Schedule** page shows the journal numbers of transactions.</span></span> <span data-ttu-id="860b9-119">Kande tühistamisel värskendatakse see väli tühistamistehingu töölehe numbriga.</span><span class="sxs-lookup"><span data-stu-id="860b9-119">When a transaction is reversed, this field is updated with the journal number of a reversing transaction.</span></span> <span data-ttu-id="860b9-120">Lisaks valitakse märkeruut **Tühistatud**, mis näitab, et kanne on tühistatud ja valitakse väli **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="860b9-120">Additionally, the **Reversed** check box is selected to indicate that the transaction is reversed, and the **Posted** field is selected.</span></span>

## <a name="revoke-a-reversed-transaction"></a><span data-ttu-id="860b9-121">Tühistatud tehingu taastamine</span><span class="sxs-lookup"><span data-stu-id="860b9-121">Revoke a reversed transaction</span></span>

<span data-ttu-id="860b9-122">Tühistatud tehingu taastamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="860b9-122">To revoke a reversed transaction, follow these steps.</span></span>

1. <span data-ttu-id="860b9-123">Valige algne kanne kas lehel **Graafik** või **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="860b9-123">On either the **Schedule** page or the **Transactions** page, select the original transaction.</span></span>
2. <span data-ttu-id="860b9-124">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="860b9-124">Follow one of these steps:</span></span>

    - <span data-ttu-id="860b9-125">Kui valisite kande lehel **Graafik**, järgige töölehe loomise etappe jaotises [Igakuiste töölehe kannete loomine partiis](create-monthly-journals-batch.md).</span><span class="sxs-lookup"><span data-stu-id="860b9-125">If you selected the transaction on the **Schedule** page, follow the steps for creating a journal in [Create monthly journal entries in a batch](create-monthly-journals-batch.md).</span></span> <span data-ttu-id="860b9-126">Peate töölehe käsitsi sisestama.</span><span class="sxs-lookup"><span data-stu-id="860b9-126">You must manually post the journal.</span></span>
    - <span data-ttu-id="860b9-127">Kui valisite kande lehel **Kanded**, valige **Tühista kanne**.</span><span class="sxs-lookup"><span data-stu-id="860b9-127">If you selected the transaction on the **Transactions** page, select **Reverse transaction**.</span></span> <span data-ttu-id="860b9-128">Kuvatakse teade, mis teatab, et see tühistamine on varasema tühistamise tagasi võtmine ja saate redigeerida selle tühistamise sisestamiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="860b9-128">You receive a message that states that this revocation is a revocation of an earlier reversal, and that you can edit the posting date for this revocation.</span></span> <span data-ttu-id="860b9-129">Kuid valideerimised mõjutavad kuupäevi, mida saab väljale **Kuupäev** sisestada.</span><span class="sxs-lookup"><span data-stu-id="860b9-129">However, general business validations affect the dates that can be entered in the **Date** field.</span></span> 

3. <span data-ttu-id="860b9-130">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="860b9-130">Select **OK**.</span></span> <span data-ttu-id="860b9-131">Sisestatakse töölehe kirje, mis tühistab valitud kirje.</span><span class="sxs-lookup"><span data-stu-id="860b9-131">A journal entry is posted that reverses the entry that you selected.</span></span> <span data-ttu-id="860b9-132">Tühistamine kuvatakse lehel **Kanded** ja taastatakse kogu praegune saldo selleks, mis see oli enne esimest tühistamist.</span><span class="sxs-lookup"><span data-stu-id="860b9-132">The reversal is shown on the **Transactions** page, and the net total current balance is restored to what it was before the first reversal.</span></span> <span data-ttu-id="860b9-133">Seetõttu muutub tühistamise mõju saldole olematuks.</span><span class="sxs-lookup"><span data-stu-id="860b9-133">Therefore, the impact that the reversal had on the balances is negated.</span></span>

<span data-ttu-id="860b9-134">Kui valite käsu **Tühista jälitus**, kuvatakse dialoogiboks, kus kuvatakse nii algsed kui ka tühistatud kanded, koos lingitud jälgimisnumbriga.</span><span class="sxs-lookup"><span data-stu-id="860b9-134">When you select **Reverse tracing**, a dialog box appears that shows both the original transactions and the reversed transactions, together with a linked trace number.</span></span>

<span data-ttu-id="860b9-135">Saate tühistusi ka vastaval lehel **Graafikud** jälgida.</span><span class="sxs-lookup"><span data-stu-id="860b9-135">You can also track revocations by using the appropriate **Schedules** page.</span></span> <span data-ttu-id="860b9-136">Kustutatakse väli **Tühistatud**, samas kui valitakse väli **Töölehele sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="860b9-136">The **Reverse** field is cleared, whereas the **Journal posted** field is selected.</span></span> <span data-ttu-id="860b9-137">Lisaks värskendatakse väli **Viimane töölehe number** tühistamise kande töölehe numbriga ja väli **Töölehe number** värskendatakse tühistamise töölehe numbriga.</span><span class="sxs-lookup"><span data-stu-id="860b9-137">Additionally, the **Latest journal number** field is updated with the journal number of the revocation transaction, and the **Journal number** field is updated with the reversal journal number.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]