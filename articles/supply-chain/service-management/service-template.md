---
title: Teenusmallid
description: Saate hooldusleppe määrata malliks ja hiljem malli read teise hoolduleppesse või hooldustellimusse kopeerida.
author: ShylaThompson
manager: tfehr
ms.date: 02/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8a92d67afe5fd427d1bc272c59e459cb1547d22
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983226"
---
# <a name="service-templates"></a><span data-ttu-id="87abe-103">Teenusmallid</span><span class="sxs-lookup"><span data-stu-id="87abe-103">Service templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87abe-104">Saate hooldusleppe määrata malliks ja hiljem malli read teise hoolduleppesse või hooldustellimusse kopeerida.</span><span class="sxs-lookup"><span data-stu-id="87abe-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="87abe-105">Näide</span><span class="sxs-lookup"><span data-stu-id="87abe-105">Example</span></span>

<span data-ttu-id="87abe-106">Kliendil, kellele osutate teenusteenust, on ühesugused teenindusliftid viies erinevas asukohas.</span><span class="sxs-lookup"><span data-stu-id="87abe-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="87abe-107">Soovite kliendile seadistada kuni viis teenuslepingut, üks iga paiga kohta.</span><span class="sxs-lookup"><span data-stu-id="87abe-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="87abe-108">Seadistustöö kordamise piiramiseks ja tagamaks, et teenuslepingute seadistusteave on ühesugune, loote teenuslepingu ja määrate selle liftide teenustöö malliks.</span><span class="sxs-lookup"><span data-stu-id="87abe-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="87abe-109">Nüüd saate malli ridu kopeerida viide uude hooldusleppesse nii, et iga hoolduslepe on täidetud mallist pärit ridadega.</span><span class="sxs-lookup"><span data-stu-id="87abe-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="87abe-110">Loo mall</span><span class="sxs-lookup"><span data-stu-id="87abe-110">Create a template</span></span>

<span data-ttu-id="87abe-111">Kui loote hooldusmalli, loote esmalt hooldusleppe, loote selles vajalikud read ja seote seejärel hooldusleppe hooldusmalli grupiga.</span><span class="sxs-lookup"><span data-stu-id="87abe-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="87abe-112">Hoolduslepet saab malliks määrata ainult siis, kui sellega ei ole seotud ühtegi hooldustellimust.</span><span class="sxs-lookup"><span data-stu-id="87abe-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="87abe-113">Samuti ei saa malliks määratud hoolduslepingu alusel koostada ühtegi hooldustellimust.</span><span class="sxs-lookup"><span data-stu-id="87abe-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="87abe-114">Kopeeri malliread</span><span class="sxs-lookup"><span data-stu-id="87abe-114">Copy template lines</span></span>

<span data-ttu-id="87abe-115">Saate teenusmallist kopeerida malli ridu teise teenuslepingusse või teenustellimusse.</span><span class="sxs-lookup"><span data-stu-id="87abe-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="87abe-116">Kui kopeerite malli ridu hooldustellimustesse või hoolduslepetesse, kuvatakse teie malligrupid puuvaatena, kus iga gruppi saab laiendada.</span><span class="sxs-lookup"><span data-stu-id="87abe-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="87abe-117">Selline kuva laseb teil vaadata iga malli ja malli rida.</span><span class="sxs-lookup"><span data-stu-id="87abe-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="87abe-118">On lihtsam otsustada, millist hooldusmalli rida soovite kopeerida, kui olete grupeerinud mallid kasutusele osutavate nimede alla.</span><span class="sxs-lookup"><span data-stu-id="87abe-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87abe-119">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="87abe-119">Related topics</span></span>

[<span data-ttu-id="87abe-120">Teenusemallide kopeerimine</span><span class="sxs-lookup"><span data-stu-id="87abe-120">Copy service templates lines</span></span>](copy-service-template-lines.md)
