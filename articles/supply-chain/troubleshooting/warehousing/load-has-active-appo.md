---
title: Saadetist ei saa kinnitada kalendri probleemi tõttu
description: Saadetist ei saa kinnitada kalendri probleemi tõttu
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938457"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a><span data-ttu-id="62b94-103">Saadetist ei saa kinnitada kalendri probleemi tõttu</span><span class="sxs-lookup"><span data-stu-id="62b94-103">You can't confirm a shipment because of an issue with the calendar</span></span>

<span data-ttu-id="62b94-104">Tõrkekood: TRX2716</span><span class="sxs-lookup"><span data-stu-id="62b94-104">Error code: TRX2716</span></span>

## <a name="symptoms"></a><span data-ttu-id="62b94-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="62b94-105">Symptoms</span></span>

<span data-ttu-id="62b94-106">Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="62b94-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="62b94-107">Kalendri tüübi %1 puhul tuleb kohtumine %2 sisse ja välja registreerida.</span><span class="sxs-lookup"><span data-stu-id="62b94-107">The calendar type %1 requires the appointment %2 to be checked in and out.</span></span>

<span data-ttu-id="62b94-108">Seega ei saa te koorma saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="62b94-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="62b94-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="62b94-109">Cause</span></span>

<span data-ttu-id="62b94-110">Koorma jaoks on aktiivsed kohtumised.</span><span class="sxs-lookup"><span data-stu-id="62b94-110">Active appointments for the load exist.</span></span> <span data-ttu-id="62b94-111">Näiteks on olemas reegel, mis nõuab juhi sisseregistreerimist.</span><span class="sxs-lookup"><span data-stu-id="62b94-111">For example, there is a rule that requires driver check-in.</span></span> <span data-ttu-id="62b94-112">Seetõttu on koorem praegu olekus, kus saadetise kinnitamine nurjub.</span><span class="sxs-lookup"><span data-stu-id="62b94-112">Therefore, the load is currently in a state where shipment confirmation fails.</span></span>

## <a name="resolution"></a><span data-ttu-id="62b94-113">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="62b94-113">Resolution</span></span>

<span data-ttu-id="62b94-114">Peate uurida ja lahendama kõik koormaga seotud aktiivsete kohtumistega seotud probleemid.</span><span class="sxs-lookup"><span data-stu-id="62b94-114">You must investigate and fix any issues with the active appointments that are linked to the load.</span></span>

1. <span data-ttu-id="62b94-115">Avage **Laohaldus \> Koormad \> Kõik koormad**.</span><span class="sxs-lookup"><span data-stu-id="62b94-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="62b94-116">Valige koorem, mille jaoks ei saa saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="62b94-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="62b94-117">Valige tegevuspaanil vahekaardil **Transport** grupis **Kohtumised** suvand **Kohtumise määramine**.</span><span class="sxs-lookup"><span data-stu-id="62b94-117">On the Action Pane, on the **Transportation** tab, in the **Appointments** group, select **Appointment scheduling**.</span></span>
1. <span data-ttu-id="62b94-118">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="62b94-118">Follow one of these steps:</span></span>

    - <span data-ttu-id="62b94-119">Veenduge, et juhi sisse- ja väljaregistreerimine oleks kohtumise jaoks lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="62b94-119">Make sure that driver check-in/check-out is completed for the appointment.</span></span>
    - <span data-ttu-id="62b94-120">Lõpetage või tühistage kohtumine.</span><span class="sxs-lookup"><span data-stu-id="62b94-120">Complete or cancel the appointment.</span></span>
    - <span data-ttu-id="62b94-121">Keelake seotud kohtumise reegli jaoks suvand **juhi sisseregistreerimine nõutav**.</span><span class="sxs-lookup"><span data-stu-id="62b94-121">Disable the **Driver check-in required** option for the related appointment rule.</span></span>
