---
title: Laotöö tühistamine erandi käsitlemiseks
description: Selles teemas kirjeldatakse funktsiooni Töö tühistamine, mis võimaldab laoinspektoritel blokeeritud tööd käsitleda.
author: omulvad
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 552c83be411ed0be83b15d2541493ff0213fbe58
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831406"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a><span data-ttu-id="75fef-103">Laotöö tühistamine erandi käsitlemiseks</span><span class="sxs-lookup"><span data-stu-id="75fef-103">Cancel warehouse work for exception handling</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75fef-104">Tarkvara Microsoft Dynamics 365 Supply Chain Management funktsioon Töö tühistamine võimaldab administraatorist kasutajal tühistada konkreetse laotöö, mis on küll praegu käimas, ent samas süsteemi poolt blokeeritud või seda ei saa erandlike asjaolude tõttu lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="75fef-104">The Cancel work functionality in Microsoft Dynamics 365 Supply Chain Management lets the admin user cancel specific warehouse work that is currently in progress, but that is blocked by the system or can't be completed because of exceptional circumstances.</span></span> <span data-ttu-id="75fef-105">See funktsioon on atraktiivne ja turvaline alternatiiv SQL-i parandusskriptidele, mis parandavad ebajärjekindlaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="75fef-105">This functionality is an attractive and secure alternative to SQL corrective scripts that fix inconsistent data.</span></span> <span data-ttu-id="75fef-106">Siiski, arvestades, et neid skripte taotletakse tavaliselt IT-spetsialistidelt, saavad funktsiooni Töö tühistamine kasutada ettevõttes administraatori õigustega kasutajad.</span><span class="sxs-lookup"><span data-stu-id="75fef-106">However, whereas these scripts are typically requested from IT professionals, the Cancel work functionality can be used by users in the company who have admin rights.</span></span>

<span data-ttu-id="75fef-107">Funktsioonile Töö tühistamine juurdepääsemiseks avage **Laohaldus** \> **Perioodilised ülesanded** \> **Puhastamine \> Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="75fef-107">You can access the Cancel work functionality at **Warehouse management** \> **Periodic tasks** \> **Clean up \> Cancel work**.</span></span> <span data-ttu-id="75fef-108">Määrake dialoogiboksis **Töö tühistamine** tühistatava töö ID ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="75fef-108">In the **Cancel work** dialog box, specify the work ID of the work to cancel, and then select **OK**.</span></span>

## <a name="warehouse-work-that-can-be-canceled"></a><span data-ttu-id="75fef-109">Tühistatav laotöö</span><span class="sxs-lookup"><span data-stu-id="75fef-109">Warehouse work that can be canceled</span></span>

<span data-ttu-id="75fef-110">Lao komplekteerimistoimingute ajal võib töötajatel esineda olukordi, kus nad on kogused registreerinud kui ladustamiskohast kasutuskohta komplekteeritud kogused, kuid seejärel ei saa nad paigutustoimingut registreerida.</span><span class="sxs-lookup"><span data-stu-id="75fef-110">During warehouse picking operations, a worker might encounter situations where they have registered quantities as picked from a storage location to their user location, but then they can't register the put operation.</span></span> <span data-ttu-id="75fef-111">Ebajärjekindlad laoandmed on sageli, kuid mitte alati, töö blokeerimise põhjus.</span><span class="sxs-lookup"><span data-stu-id="75fef-111">Inconsistent warehouse data is often, but not always, the reason why work is blocked.</span></span>

<span data-ttu-id="75fef-112">Erinevalt tavalisest tühistamis funktsioonist, millele pääseb juurde töö päise nupu **Tühista** abil, ei nõua funktsioon Töö tühistamine, et viimasele lõpetatud tööreale oleks määratud tüüp **paigutamine**.</span><span class="sxs-lookup"><span data-stu-id="75fef-112">Unlike the regular Cancel functionality that can be accessed by using the **Cancel** button on the work header, the Cancel work functionality doesn't require that the last completed work line be a work line of the **put** type.</span></span> <span data-ttu-id="75fef-113">Teisisõnu võib funktsiooni Töö tühistamine tühistamisloogika käitada ka siis, kui tööreal oleva kauba kogus on kasutaja asukohas.</span><span class="sxs-lookup"><span data-stu-id="75fef-113">In other words, for the Cancel work functionality, cancellation logic can be run even if the item quantity on a work line is in a user location.</span></span>

> [!NOTE]
> <span data-ttu-id="75fef-114">Töö jaoks, mis tuleb tööpõhjuste tõttu tühistada, peavad lao kasutajad jätkama töölehel asuva tavapärase tühistamisfunktsiooni kasutamist.</span><span class="sxs-lookup"><span data-stu-id="75fef-114">For work that must be canceled for operational reasons, warehouse users must continue to use the regular Cancel functionality on the work page.</span></span>

<span data-ttu-id="75fef-115">Funktsiooni Töö tühistamine abil saab tühistada ainult tööd, mille tüüp on **Müük**, **Edastuse väljaminek**, **Toormaterjalide komplekteerimine** või **Täiendamine**.</span><span class="sxs-lookup"><span data-stu-id="75fef-115">Only work of the **Sales**, **Transfer issue**, **Raw material picking**, or **Replenishment** type can be canceled by using the Cancel work functionality.</span></span> <span data-ttu-id="75fef-116">Tühistamisloogikat ei käivitata külmutatud toormaterjalide komplekteerimise töö või töö puhul, mida saab tühistada tavapärase tühistamisfunktsiooni abil (vt eelmist märkust).</span><span class="sxs-lookup"><span data-stu-id="75fef-116">Cancellation logic won't be run for frozen raw material picking work or work that can be canceled by using the regular Cancel functionality (see the preceding note).</span></span>

<span data-ttu-id="75fef-117">Töö blokeeringu tühistamiseks tühistab süsteem kõik allesjäänud tööread ja fikseerib laoandmed, mis on seotud kasutaja määratud töö ID-ga.</span><span class="sxs-lookup"><span data-stu-id="75fef-117">To unblock the work, the system cancels any remaining work lines and fixes the warehouse data that is associated with the work ID that the user specified.</span></span> <span data-ttu-id="75fef-118">Kõik tavapärased lao käitlustoimingud, mis hõlmavad mõjutatud kauba kogust, saavad seejärel jätkuda.</span><span class="sxs-lookup"><span data-stu-id="75fef-118">Any regular warehouse-handling operations that involve the affected item quantity can then resume.</span></span>

<span data-ttu-id="75fef-119">Et panna mõjutatud kaup kindlasse asukohta pärast töö tühistamist, peab kasutaja kasutama mobiilses seadmes varude liikumise või koguse korrigeerimise toimingut.</span><span class="sxs-lookup"><span data-stu-id="75fef-119">To put the affected item in a specific location after the work is canceled, the user must use an inventory movement or quantity adjustment operation on a mobile device.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]