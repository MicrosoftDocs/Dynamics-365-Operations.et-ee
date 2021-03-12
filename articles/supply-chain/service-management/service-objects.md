---
title: Teeninduse objektide ülevaade
description: Hooldusobjektid on kliendi varad ja tooted, millega seoses saab hooldust osutada.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1e0a40d351150ce432164438cd9680cf80792e1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974306"
---
# <a name="service-objects-overview"></a><span data-ttu-id="3fc86-103">Teeninduse objektide ülevaade</span><span class="sxs-lookup"><span data-stu-id="3fc86-103">Service objects overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3fc86-104">Hooldusobjektid on kliendi varad ja tooted, millega seoses saab hooldust osutada.</span><span class="sxs-lookup"><span data-stu-id="3fc86-104">Service objects are a customer’s assets and products for which you can perform a service.</span></span> <span data-ttu-id="3fc86-105">Olenevalt teie poolt pakutavast teenuse tüübist võivad objektid olla materiaalsed või immateriaalsed.</span><span class="sxs-lookup"><span data-stu-id="3fc86-105">Depending on the type of service you provide, objects can be tangible or intangible:</span></span>

-  <span data-ttu-id="3fc86-106">Materiaalsed objektid on nt masin või hoone, mille hooldamine seisneb füüsilistes ülesannetes.</span><span class="sxs-lookup"><span data-stu-id="3fc86-106">Tangible objects are things, such as a machine or a building, on which you can perform a physical service task.</span></span>

    <span data-ttu-id="3fc86-107">Materiaalne hooldusobjekt võib olla ka laokaup, mille loote vormil Väljastatud toote üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="3fc86-107">A tangible service object can also be an inventory item that you create in the Released product details form.</span></span> <span data-ttu-id="3fc86-108">Olenevalt varude dimensioonigrupist, mille kaubaga seote, saate hooldusobjekti luua kauba seerianumbrit sisaldavate üksikasjade tasemele.</span><span class="sxs-lookup"><span data-stu-id="3fc86-108">Depending on the inventory dimension group that you attach to the item, you can create a service object to a level of detail that includes the item serial number.</span></span> <span data-ttu-id="3fc86-109">See on kasulik, kui peate jälgima konkreetset kaupa, mida hooldusobjekt kajastab.</span><span class="sxs-lookup"><span data-stu-id="3fc86-109">This is useful when you must keep track of the exact item that the service object represents.</span></span>

    <span data-ttu-id="3fc86-110">Materiaalne hooldusobjekt võib olla ka kaup, mis ei ole otseselt seotud ettevõtte otsese toote- või tarneahelaga.</span><span class="sxs-lookup"><span data-stu-id="3fc86-110">A tangible service object can also be an item that is not directly related to a company's direct production or supply chain.</span></span> <span data-ttu-id="3fc86-111">Näiteks võib tööriistakomplekt, mida kasutatakse hooldustellimuses remontimiseks, olla hooldusobjekt, mis ei sisaldu varudes.</span><span class="sxs-lookup"><span data-stu-id="3fc86-111">For example, a tool kit that is used for repairs in a service order can be a service object that is not included in inventory.</span></span> <span data-ttu-id="3fc86-112">Sel juhul ei registreerita seda laokaubana.</span><span class="sxs-lookup"><span data-stu-id="3fc86-112">In this case, you don’t register it as an inventory item.</span></span>

-  <span data-ttu-id="3fc86-113">Immateriaalsed objektid on mittefüüsilised asjad, nt kontokogumid või juriidiline dokument, millega saate hooldustoiminguid teha.</span><span class="sxs-lookup"><span data-stu-id="3fc86-113">Intangible objects are nonphysical things, such as a set of accounts or a legal document, on which you can perform a service task.</span></span>

## <a name="example-of-an-intangible-service-object"></a><span data-ttu-id="3fc86-114">Immateriaalse hooldusobjekti näide</span><span class="sxs-lookup"><span data-stu-id="3fc86-114">Example of an intangible service object</span></span>

<span data-ttu-id="3fc86-115">Ettevõte A haldab mitme väikeettevõtte finantsandmeid.</span><span class="sxs-lookup"><span data-stu-id="3fc86-115">Company A maintains the financial records for several small companies.</span></span> <span data-ttu-id="3fc86-116">Üks ettevõtte A klient on kohalik jalgpallimeeskond, millele ettevõte A osutab iganädalast raamatupidamise teenust ja viib kord aastas läbi klubi kontode auditi.</span><span class="sxs-lookup"><span data-stu-id="3fc86-116">One of Company A's clients is the local football team, for which Company A does the weekly bookkeeping and annual audit of the club's accounts.</span></span> <span data-ttu-id="3fc86-117">Klubi kontod on seadistatud vormil Hooldusobjektid ja määratletud hooldusleppe objektina.</span><span class="sxs-lookup"><span data-stu-id="3fc86-117">The club's accounts are set up in the Service objects form and specified as the object in the service agreement.</span></span> <span data-ttu-id="3fc86-118">Objektil on kaks hooldusleppe rida.</span><span class="sxs-lookup"><span data-stu-id="3fc86-118">There are two service agreement lines for the object.</span></span> <span data-ttu-id="3fc86-119">1. rida on nädalase intervalliga iganädalane raamatupidamine ja 2. rida on iga-aastane audit, millele on määratud aastane intervall.</span><span class="sxs-lookup"><span data-stu-id="3fc86-119">Line 1 is weekly bookkeeping with a weekly interval assigned to the line, and line 2 is the annual audit with a yearly interval assigned to it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fc86-120">Seotud teemad</span><span class="sxs-lookup"><span data-stu-id="3fc86-120">Related topics</span></span>

[<span data-ttu-id="3fc86-121">Hooldusobjektide loomine</span><span class="sxs-lookup"><span data-stu-id="3fc86-121">Create service objects</span></span>](create-service-objects.md)

