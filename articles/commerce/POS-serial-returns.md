---
title: Tagasta seerianumbriga kontrollitud tooted kassas
description: See teema kirjeldab võimalusi järjestatud kaupade valideerimiseks osana müügikoha rakenduse Microsoft Dynamics 365 Commerce tagastusprotsessist.
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 7a067994828f3df577c0dc4146d26ac81990d4ac
ms.sourcegitcommit: 927574c77f4883d906e5c7bddf0af9b717e492bf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129803"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a><span data-ttu-id="61bce-103">Tagasta seerianumbriga kontrollitud tooted kassas</span><span class="sxs-lookup"><span data-stu-id="61bce-103">Return serial number–controlled products in POS</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="61bce-104">See teema kirjeldab võimalusi järjestatud kaupade valideerimiseks osana müügikoha rakenduse Microsoft Dynamics 365 Commerce tagastusprotsessist.</span><span class="sxs-lookup"><span data-stu-id="61bce-104">This topic describes the capabilities for validating serialized items as part of the return process in the Microsoft Dynamics 365 Commerce point of sale (POS) application.</span></span>

> [!NOTE]
> <span data-ttu-id="61bce-105">Commerce version 10.0.20 väljalaskes ja hilisemas versioonis on saadaval uus funktsioon nimega **Ühtne tagastuse töötlemise kogemus kassas**.</span><span class="sxs-lookup"><span data-stu-id="61bce-105">In the Commerce version 10.0.20 release and later, a new feature that is named **Unified return processing experience in POS** is available.</span></span> <span data-ttu-id="61bce-106">Seerianumbrite valideerimiseks tagastustellimuse töötlemise ajal kassas peate selle funktsiooni sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="61bce-106">To use serial number validation during return order processing in POS, you must turn on this feature.</span></span> <span data-ttu-id="61bce-107">Teavet teiste võimaluste kohta, mida see funktsioon pakub, kui see on sisse lülitatud, vt [loo tagastused müügikohas](POS-returns.md).</span><span class="sxs-lookup"><span data-stu-id="61bce-107">For information about others capabilities that this feature provides when it's turned on, see [Create returns in POS)](POS-returns.md).</span></span>
>
> <span data-ttu-id="61bce-108">Kui funktsioon on sisse lülitatud, ei saa seda välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="61bce-108">After the feature is turned on, it can't be turned off.</span></span>

## <a name="options-for-validating-serialized-returns"></a><span data-ttu-id="61bce-109">Järjestatud tagastuste kinnitamise suvandid</span><span class="sxs-lookup"><span data-stu-id="61bce-109">Options for validating serialized returns</span></span>

<span data-ttu-id="61bce-110">Kui kassa funktsioon **ühtne tagastustöötluse kogemus** on sisse lülitatud, saavad organisatsioonid kassa kaudu kontrollida seerianumbriga kaupade tagastusi.</span><span class="sxs-lookup"><span data-stu-id="61bce-110">When the **Unified return processing experience in POS** feature is turned on, organizations can perform a validation on returns of serial number–controlled items through POS.</span></span> <span data-ttu-id="61bce-111">See võimalus võib hoiatada kasutajaid, kui tagastatav seerianumber erineb algsest müüdud seerianumbrist.</span><span class="sxs-lookup"><span data-stu-id="61bce-111">This capability can warn users if the serial number that is being returned differs from the original serial number that was sold.</span></span> <span data-ttu-id="61bce-112">Commerce version 10.0.20 väljalaskes ja hilisemas versioonis on teade, mille kasutajad saavad, ainult hoiatusteade.</span><span class="sxs-lookup"><span data-stu-id="61bce-112">In the Commerce version 10.0.20 release and later, the message that users receive is only a warning message.</span></span> <span data-ttu-id="61bce-113">Kasutajad saavad tagastust jätkata seerianumbri suhtes, mis erineb algselt müüdud seerianumbrist.</span><span class="sxs-lookup"><span data-stu-id="61bce-113">Users can continue to process a return against a serial number that differs from the serial number that was originally sold.</span></span>

<span data-ttu-id="61bce-114">Organisatsiooni seerianumbri kinnitamise konfigureerimiseks pärast seda, kui kassa funktsiooni **Ühtne tagastustöötluse kogemus** on sisse lülitatud, minge **Jaemüük ja Äri \> Headquarters häälestus \> Parameetrid \> Commerce parameetrid** rakenduses Commerce headquarters.</span><span class="sxs-lookup"><span data-stu-id="61bce-114">To configure serial number validation for an organization after the **Unified return processing experience in POS** feature is turned on, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters** in Commerce headquarters.</span></span> <span data-ttu-id="61bce-115">Seadke vahekaardil **Varud** kiirkaardil **Kaupluse lao toimingud** suvandile **Luba müügikohas seerianumbrite valideerimine** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="61bce-115">On the **Inventory** tab, on the **Store inventory operations** FastTab, set the **Enable validation of serial numbers on POS returns** option to **Yes**.</span></span>

## <a name="process-returns-for-serialized-items-in-pos"></a><span data-ttu-id="61bce-116">Kassas järjestatud kaupade tagastuste protsess</span><span class="sxs-lookup"><span data-stu-id="61bce-116">Process returns for serialized items in POS</span></span>

<span data-ttu-id="61bce-117">Kui valik **Luba müügikoha tagastuste seerianumbrite valideerimine** on seatud väärtusele **Jah**, kui seerianumbri juhitav kaup tagastatakse müügikoha kaudu, saab kasutaja sisestada tagastusrea seerianumbri lehekülje üksikasjade **tagastatavate toodete** paanile.</span><span class="sxs-lookup"><span data-stu-id="61bce-117">If the **Enable validation of serial numbers on POS returns** option has been set to **Yes**, when a serial number–controlled item is returned through POS, the user can enter the serial number for the return line in the details pane on the **Returnable products** page.</span></span> <span data-ttu-id="61bce-118">Kui sisestatud seerianumber ei vasta algsele müügikande seerianumbrile, saab kasutaja hoiatusteate.</span><span class="sxs-lookup"><span data-stu-id="61bce-118">If the serial number that is entered doesn't match the original serial number that was sold for the sales transaction, the user receives a warning message.</span></span> <span data-ttu-id="61bce-119">Rakendus ei takista siiski kasutajal tagastuse sisestamist jätkata.</span><span class="sxs-lookup"><span data-stu-id="61bce-119">However, the application doesn't prevent the user from continuing to post the return.</span></span>

> [!NOTE]
> <span data-ttu-id="61bce-120">Praegu toetab müügikoht seerianumbrite kinnitamist ainult tagastusridadel, kus algne tellitud kogus ei ole suurem kui üks.</span><span class="sxs-lookup"><span data-stu-id="61bce-120">Currently, POS supports validation of serial numbers only on return lines where the original ordered quantity is no more than one.</span></span> <span data-ttu-id="61bce-121">Kui algne müügitellimuse rida loodi mittekassakanalis ja kui tellitud kogus antud müügireal on rohkem kui üks, ei saa kaupa kassa kaudu õigesti tagastada.</span><span class="sxs-lookup"><span data-stu-id="61bce-121">If the original sales order line was created in a non-POS channel, and if the quantity that was ordered for the serialized item on a given sales line is more than one, the item can't be correctly returned through POS.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61bce-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="61bce-122">Additional resources</span></span>

[<span data-ttu-id="61bce-123">Tagastuste loomine müügikohas</span><span class="sxs-lookup"><span data-stu-id="61bce-123">Create returns in POS</span></span>](POS-returns.md)
