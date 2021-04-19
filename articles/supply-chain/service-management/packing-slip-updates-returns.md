---
title: Saatelehtede värskendamine tagastamisteks
description: Enne kui tagastatud kaubad saab lattu vastu võtta tuleb vastava tellimuse saateleht uuendada.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9b5c7e5726c36aa963e5750c63df20c1e2e6c35
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810698"
---
# <a name="packing-slip-updates-for-returns"></a><span data-ttu-id="f9854-103">Saatelehtede värskendamine tagastamisteks</span><span class="sxs-lookup"><span data-stu-id="f9854-103">Packing slip updates for returns</span></span>  

[!include [banner](../includes/banner.md)]


<span data-ttu-id="f9854-104">Enne kui tagastatud kaubad saab lattu vastu võtta tuleb vastava tellimuse saateleht uuendada.</span><span class="sxs-lookup"><span data-stu-id="f9854-104">Before returned items can be received into inventory, the packing slip for the order to which they belong must be updated.</span></span> <span data-ttu-id="f9854-105">Nii nagu arve värskendamise protsess on finantskande värskendamine, on saatelehe värskendamise protsess laokirje füüsiline värskendamine, st see teeb muudatused laovarudes.</span><span class="sxs-lookup"><span data-stu-id="f9854-105">Just as the invoice update process is the update to the financial transaction, the packing slip update process is the physical update of the inventory record, which means that it commits the changes to inventory.</span></span> <span data-ttu-id="f9854-106">Tagastuste korral rakendatakse likvideerimistegevuseks määratud etapid saatelehe värskendamise käigus.</span><span class="sxs-lookup"><span data-stu-id="f9854-106">In the case of returns, the steps that are assigned to the disposition action are implemented during the packing slip update.</span></span>

<span data-ttu-id="f9854-107">Saatelehe uuendamist saab töödelda kas saabuva kauba töölehel või tagastustellimusel.</span><span class="sxs-lookup"><span data-stu-id="f9854-107">The packing slip update can be processed in either the item arrival journal or the return order.</span></span>

<span data-ttu-id="f9854-108">Osana saatelehtede sisestamise protsessist saab kliendi saatedokumentidel oleva saatelehe viitenumbri siduda tellimusridadega.</span><span class="sxs-lookup"><span data-stu-id="f9854-108">As part of the process for posting packing slips, the packing slip reference number from the customer’s shipping documents can be associated with the order lines.</span></span> <span data-ttu-id="f9854-109">See seos on valikuline ja ainult viitamiseks.</span><span class="sxs-lookup"><span data-stu-id="f9854-109">This association is optional and for reference only.</span></span> <span data-ttu-id="f9854-110">See ei loo ühtki kandevärskendust.</span><span class="sxs-lookup"><span data-stu-id="f9854-110">It does not create any transactional updates.</span></span>

<span data-ttu-id="f9854-111">Kui kõik oodatud tagastuskaubad pole saabunud, peaksite kaasama ainult koguse, mis on vastu võetud saatelehe värskendusega.</span><span class="sxs-lookup"><span data-stu-id="f9854-111">If not all of the expected return items have arrived, you should include only the quantity that has been received in the packing slip update.</span></span> <span data-ttu-id="f9854-112">Jätke saabumata kaubad tellimusele tagastussaadetise saabumiseni.</span><span class="sxs-lookup"><span data-stu-id="f9854-112">Leave the remaining items on the order until the rest of the return shipment has arrived.</span></span>

<span data-ttu-id="f9854-113">Kui kaup on saadetud vahelaost tagasi lähetamise ja vastuvõtmise osakonda, nt juhul kui vahelao kontrollija ei tea, millisesse lattu kaup ladustada, tuleb vastav saateleht värskendada, et vahelaos määratud likvideerimiskood õigesti registreerida ja seda õigesti käsitleda.</span><span class="sxs-lookup"><span data-stu-id="f9854-113">If an item is sent back from quarantine to the Shipping and Receiving department, such as when the quarantine inspector does not know where to store the item in inventory, the corresponding packing slip must be updated to correctly register and act on the disposition code that is specified as a result of the quarantine.</span></span>

<span data-ttu-id="f9854-114">Kui värskendate müügilepingust pärineva tagastatud kauba saatelehte, värskendatakse automaatselt selle kauba müügilepingu kohustust, et peegeldada koguse või summa muutust.</span><span class="sxs-lookup"><span data-stu-id="f9854-114">When you update a packing slip for a returned item that is from a sales agreement, the sales agreement commitment for that item is automatically updated to reflect the change in the quantity or the amount.</span></span> 

## <a name="see-also"></a><span data-ttu-id="f9854-115">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f9854-115">See also</span></span>

[<span data-ttu-id="f9854-116">Tagastuste arvete värskendamine</span><span class="sxs-lookup"><span data-stu-id="f9854-116">Perform invoice updates for returns</span></span>](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]