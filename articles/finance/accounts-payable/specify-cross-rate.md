---
title: Ristkursi määramine
description: See teema annab üldteavet ristkursside kohta rakenduses Microsoft Dynamics 365 Finance.
author: abruer
manager: AnnBe
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a1463b9676e6b26543fd88607ca13b0ceb12be5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231562"
---
# <a name="specify-the-cross-rate"></a><span data-ttu-id="85448-103">Ristkursi määramine</span><span class="sxs-lookup"><span data-stu-id="85448-103">Specify the cross rate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85448-104">See teema selgitab ristkursi eesmärki ja ristkursi määramist makse tasakaalustamisel arvega.</span><span class="sxs-lookup"><span data-stu-id="85448-104">This topic explains the purpose of a cross rate, and how to specify the cross rate when you settle a payment with an invoice.</span></span> <span data-ttu-id="85448-105">Kasutage ristkurssi, kui kehtivad kõik järgmised kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="85448-105">Use a cross rate when all of the following criteria apply:</span></span> 
-   <span data-ttu-id="85448-106">Tasakaalustate makse arvega.</span><span class="sxs-lookup"><span data-stu-id="85448-106">You are settling a payment with an invoice.</span></span> 
-   <span data-ttu-id="85448-107">Makse rida ja arve rida kasutavad erinevaid valuutasid.</span><span class="sxs-lookup"><span data-stu-id="85448-107">The payment line and the invoice line use different currencies.</span></span> 
-   <span data-ttu-id="85448-108">Kumbki valuuta pole arvestusvaluuta.</span><span class="sxs-lookup"><span data-stu-id="85448-108">Neither currency is the accounting currency.</span></span> 

<span data-ttu-id="85448-109">Ristkurssi ei kasutata, et arvutada maksekande valuuta ümberarvestus makse arvestusvaluutaks.</span><span class="sxs-lookup"><span data-stu-id="85448-109">The cross rate is not used to calculate the payment transaction currency translation to the payment accounting currency.</span></span> <span data-ttu-id="85448-110">Selle asemel tuuakse vahetuskursside tabelitest vahetuskursid, et arvutada maksekande valuuta summa ja makse arvestusvaluuta summa väärtus.</span><span class="sxs-lookup"><span data-stu-id="85448-110">Instead, the exchange rates from the exchange rate tables are retrieved to calculate the value of the payment transaction currency amount and the payment accounting currency amount.</span></span> 

<span data-ttu-id="85448-111">Näiteks arvestusvaluuta on USD, arve valuuta on CAD ja makse valuuta on EUR.</span><span class="sxs-lookup"><span data-stu-id="85448-111">For example, the accounting currency is USD, the invoice currency is CAD, and the payment currency is EUR.</span></span> <span data-ttu-id="85448-112">Ristkurss võimaldab sisestada vahetuskursi otse CAD ja EURi vaheliseks teisendamiseks, nii et USD-d pole vaja kasutada.</span><span class="sxs-lookup"><span data-stu-id="85448-112">The cross rate lets you enter an exchange rate to translate directly between CAD and EUR, and not have to translate through USD.</span></span> <span data-ttu-id="85448-113">Kui valite arve ja esmase makse, saate arve rea jaoks sisestada ristkursi.</span><span class="sxs-lookup"><span data-stu-id="85448-113">When you select an invoice and a primary payment, you can enter a cross rate for the invoice line.</span></span> <span data-ttu-id="85448-114">Ristkurss on nende kannete valuutade vaheline vahetuskurss tasakaalustamise kuupäeva seisuga.</span><span class="sxs-lookup"><span data-stu-id="85448-114">The cross rate is the exchange rate between the currencies for those transactions, as of the settlement date.</span></span>

1.  <span data-ttu-id="85448-115">Minge ühele järgmistest lehtedest:</span><span class="sxs-lookup"><span data-stu-id="85448-115">Go to one of the following pages:</span></span>
- <span data-ttu-id="85448-116">**Müügireskontro > Üldine > Kliendid > Kõik kliendid**</span><span class="sxs-lookup"><span data-stu-id="85448-116">**Accounts receivable > Common > Customers > All customers**</span></span> 
- <span data-ttu-id="85448-117">**Ostureskontrod > Üldine > Hankijad > Kõik hankijad**</span><span class="sxs-lookup"><span data-stu-id="85448-117">**Accounts payable > Common > Vendors > All vendors**</span></span> 
- <span data-ttu-id="85448-118">**Hanked > Üldine > Hankijad > Kõik hankijad**</span><span class="sxs-lookup"><span data-stu-id="85448-118">**Procurement and sourcing > Common > Vendors > All vendors**</span></span>
2.  <span data-ttu-id="85448-119">Valige klient või tarnija, kelle avatud kandeid te tasakaalustate.</span><span class="sxs-lookup"><span data-stu-id="85448-119">Select the customer or vendor whose open transactions you are settling.</span></span> 
3.  <span data-ttu-id="85448-120">Kliendi korral tehke loendilehel **Kõik kliendid** valik **Kogumine > Avatud kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="85448-120">For a customer, on the **All customers** list page, go to **Collect > Settle open transactions**.</span></span> <span data-ttu-id="85448-121">Hankija korral tehke loendilehel **Kõik hankijad** valik **Arve > Avatud kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="85448-121">For a vendor, on the **All vendors** list page, go to **Invoice > Settle open transactions**.</span></span> 
4.  <span data-ttu-id="85448-122">Valige kanne, mis on esmane makse ja klõpsake nuppu **Märgi makse**.</span><span class="sxs-lookup"><span data-stu-id="85448-122">Select the transaction that is the primary payment, and then click **Mark payment**.</span></span> <span data-ttu-id="85448-123">Veerus **Märgi** valitakse märkeruut ja veerus **Esmane makse** kuvatakse ikoon teabega.</span><span class="sxs-lookup"><span data-stu-id="85448-123">The check box in the **Mark** column is selected, and an information icon is shown in the **Primary payment** column.</span></span> 
5.  <span data-ttu-id="85448-124">Väljale **Ristkurss** sisestage arve valuuta ja makse valuuta vaheline vahetuskurss tasakaalustamise kuupäeva seisuga.</span><span class="sxs-lookup"><span data-stu-id="85448-124">In the **Cross rate** field, enter the exchange rate between the invoice currency and the payment currency, as of the settlement date.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]