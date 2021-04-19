---
title: Ohtlike materjalide ülevaade
description: Selles teemas antakse ülevaade funktsioonidest, mis on seotud ohtlike materjalide käitlemise ja dokumenteerimisega tooteteabe ja laohalduse ajal.
author: dasani-madipalli
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 15edf61cba03a57b9b4d2c939228fd064b797942
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829374"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="50ed2-103">Ohtlike materjalide ülevaade</span><span class="sxs-lookup"><span data-stu-id="50ed2-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50ed2-104">Tarne-ja transpordimääruste nõuetele vastavuse säilitamiseks peavad organisatsioonid, kes tarnivad materjale, mis liigitatakse ohtlikuks kaubaks, lisama saadetistele täiendavaid pabereid.</span><span class="sxs-lookup"><span data-stu-id="50ed2-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="50ed2-105">Ohtlike materjalide funktsioon võimaldab klientidel talletada teavet, mis on seotud väljastatud kaupadega.</span><span class="sxs-lookup"><span data-stu-id="50ed2-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="50ed2-106">Seda teavet saab kasutada saatmisdokumentide ettevalmistamise hõlbustamiseks.</span><span class="sxs-lookup"><span data-stu-id="50ed2-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="50ed2-107">Organisatsioonil, kes tarnib ohtlikke kaupu, peavad saatmisprotsessi haldamiseks olema oma protsessid ja protseduurid.</span><span class="sxs-lookup"><span data-stu-id="50ed2-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="50ed2-108">Microsoft Dynamics 365 Supply Chain Management on tööriist, mis aitab genereerida nõutavaid dokumente.</span><span class="sxs-lookup"><span data-stu-id="50ed2-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="50ed2-109">Järgmisel joonisel on kuvatud ohtlike materjalide funktsiooni häälestamise ja kasutamise toimingud.</span><span class="sxs-lookup"><span data-stu-id="50ed2-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="50ed2-110">![Ohtlike materjalide funktsiooni häälestamine ja kasutamine](media/hazmat-overview.png "Ohtlike materjalide funktsiooni häälestamine ja kasutamine")</span><span class="sxs-lookup"><span data-stu-id="50ed2-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="50ed2-111">Ohtlike materjalide funktsioon häälestatakse tooteteabe halduses ja see pakub dokumente, mida saab printida laohalduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="50ed2-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="50ed2-112">Seetõttu on need alad laias laastus kaks peamist valdkonda, kus saate üle vaadata, häälestada ja kasutada seda funktsiooni funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="50ed2-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="50ed2-113">**Toote teabehaldus** – saate häälestada väljastatud toodetele rakendatavaid koode.</span><span class="sxs-lookup"><span data-stu-id="50ed2-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="50ed2-114">**Laohaldus** – töö täiendavate saatedokumentidega, mis prinditakse saadetiste jaoks.</span><span class="sxs-lookup"><span data-stu-id="50ed2-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="50ed2-115">Supply Chain Managementi ohtlike materjalide funktsioonid pakuvad kasulike tooteteabe väljade ja nendega seotud funktsioonide kogumit, mis aitab salvestada ohtlike toodetega seotud teavet ja viidata sellele.</span><span class="sxs-lookup"><span data-stu-id="50ed2-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="50ed2-116">Need funktsioonid aitavad ka luua ja printida saadetise dokumente, mis sisaldavad sama teavet mistahes ohtlike materjalide kohta, mida te lähetate.</span><span class="sxs-lookup"><span data-stu-id="50ed2-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="50ed2-117">Siiski ei muuda süsteem teie kaupa automaatselt nõuetele vastavaks teie riigis või piirkonnas kohalduvatele määrustele.</span><span class="sxs-lookup"><span data-stu-id="50ed2-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="50ed2-118">Kuigi need tööriistad on ette nähtud selleks, et aidata teil järgida ühiseid määrusi, ei ole need iseenesest piisavad ega nende piisavus pole garanteeritud.</span><span class="sxs-lookup"><span data-stu-id="50ed2-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="50ed2-119">Teie organisatsioon vastutab kõigi kohaldatavate määruste ja nende täitmiseks vajalike sammude eest.</span><span class="sxs-lookup"><span data-stu-id="50ed2-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="50ed2-120">Tooteteabe haldus</span><span class="sxs-lookup"><span data-stu-id="50ed2-120">Product information management</span></span>

<span data-ttu-id="50ed2-121">Toote teabehaldus pakub valikut häälestustabeleid, kuhu saate sisestada viiteteabe ohtlike kaupade loenditesse maantee-, õhu- ja meretranspordi jaoks.</span><span class="sxs-lookup"><span data-stu-id="50ed2-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="50ed2-122">Selle funktsiooni väljatöötamisel viidati järgmistele ühistele määrustele.</span><span class="sxs-lookup"><span data-stu-id="50ed2-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="50ed2-123">**ADR** – määrused, mis on seotud ohtlike kaupade rahvusvahelise autoveoga</span><span class="sxs-lookup"><span data-stu-id="50ed2-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="50ed2-124">**CFR 49** – Ameerika Ühendriikide määrused ohtlike kaupade veo kohta</span><span class="sxs-lookup"><span data-stu-id="50ed2-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="50ed2-125">**IMDG** – rahvusvaheline ohtlike kaupade (IMDG) kood</span><span class="sxs-lookup"><span data-stu-id="50ed2-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="50ed2-126">**IATA** – Rahvusvahelise Lennutranspordi Assotsiatsiooni (IATA) ohtlike kaupade määrused</span><span class="sxs-lookup"><span data-stu-id="50ed2-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="50ed2-127">Igas määruses on sätestatud ohtlike kaupade ja viitekoodide standardiseeritud loendid.</span><span class="sxs-lookup"><span data-stu-id="50ed2-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="50ed2-128">Seetõttu pakub Supply Chain Management nende ühiste koodide loendite viitetabeli.</span><span class="sxs-lookup"><span data-stu-id="50ed2-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="50ed2-129">Igal loendil on ka mõned unikaalsed koodid, mida saate määratleda.</span><span class="sxs-lookup"><span data-stu-id="50ed2-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="50ed2-130">Lisateabe saamiseks ohtlike materjalide määruste ja väärtuste häälestamise ja asjakohastele toodetele väärtuste määramise kohta lugege järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="50ed2-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="50ed2-131">Ohtlike materjalide häälestamine</span><span class="sxs-lookup"><span data-stu-id="50ed2-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="50ed2-132">Ohtlikud materjalid toodetes, tellimustes, saadetistes ja koormates</span><span class="sxs-lookup"><span data-stu-id="50ed2-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="50ed2-133">Laohaldus</span><span class="sxs-lookup"><span data-stu-id="50ed2-133">Warehouse management</span></span>

<span data-ttu-id="50ed2-134">Kui valmistate saadetist ette laohalduses, saate printida mitu uut aruannet, mis kasutavad tooteteabe halduses häälestatud teavet.</span><span class="sxs-lookup"><span data-stu-id="50ed2-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="50ed2-135">Lisateavet saadaolevate aruannete ja nende kasutamise kohta leiate teemast [Ohtlike materjalide päringud ja aruanded](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="50ed2-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]