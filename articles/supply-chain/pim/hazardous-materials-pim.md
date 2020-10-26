---
title: Ohtlikud materjalid
description: See teema annab teavet teie keskkonda talletatud ohtlike materjalide dokumentide ja teabe kohta.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979036"
---
# <a name="hazardous-materials"></a><span data-ttu-id="8693c-103">Ohtlikud materjalid</span><span class="sxs-lookup"><span data-stu-id="8693c-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8693c-104">Teave ohtlike materjalide kohta on seadistatud toote teabehalduses.</span><span class="sxs-lookup"><span data-stu-id="8693c-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="8693c-105">Siit moodulist leiate ka laohalduse kaudu prinditavad dokumendid.</span><span class="sxs-lookup"><span data-stu-id="8693c-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="8693c-106">Kui saadate materjale, mis on liigitatud ohtlikeks kaupadeks, tuleb saadetistega kaasa panna täiendavat dokumentatsiooni.</span><span class="sxs-lookup"><span data-stu-id="8693c-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="8693c-107">Ohtlike materjalide funktsioon võimaldab klientidel talletada klassifikatsiooni teavet ja siduda seda lähetatavate kaupadega.</span><span class="sxs-lookup"><span data-stu-id="8693c-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="8693c-108">Seda teavet saab kasutada saatmisdokumentide ettevalmistamise hõlbustamiseks.</span><span class="sxs-lookup"><span data-stu-id="8693c-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8693c-109">Microsoft Dynamics 365 Supply Chain Managementi ohtlike materjalide funktsioonid pakuvad kasulike tooteteabe väljade ja nendega seotud funktsioonide kogumit, mis aitab salvestada ohtlike toodetega seotud teavet ja viidata sellele.</span><span class="sxs-lookup"><span data-stu-id="8693c-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="8693c-110">Need funktsioonid aitavad ka luua ja printida saadetise dokumente, mis sisaldavad sama teavet mistahes ohtlike materjalide kohta, mida te lähetate.</span><span class="sxs-lookup"><span data-stu-id="8693c-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="8693c-111">Siiski ei muuda süsteem teie kaupa automaatselt nõuetele vastavaks teie riigis või piirkonnas kohalduvatele määrustele.</span><span class="sxs-lookup"><span data-stu-id="8693c-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="8693c-112">Kuigi need tööriistad on ette nähtud selleks, et aidata teil järgida ühiseid määrusi, ei ole need iseenesest piisavad ega nende piisavus pole garanteeritud.</span><span class="sxs-lookup"><span data-stu-id="8693c-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="8693c-113">Teie organisatsioon vastutab kõigi kohaldatavate määruste ja nende täitmiseks vajalike sammude eest.</span><span class="sxs-lookup"><span data-stu-id="8693c-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="8693c-114">Enne kui saate seda funktsiooni kasutada, on vaja teha järgmised seadistused.</span><span class="sxs-lookup"><span data-stu-id="8693c-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="8693c-115">**Toote teabehaldus:** saate seadistada väljastatud toodetele rakendatavaid koode.</span><span class="sxs-lookup"><span data-stu-id="8693c-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="8693c-116">**Laohaldus:** saadetise teabe printimiseks saate kasutada täiendavaid tarnedokumente.</span><span class="sxs-lookup"><span data-stu-id="8693c-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="8693c-117">Tooteteabe haldus</span><span class="sxs-lookup"><span data-stu-id="8693c-117">Product information management</span></span>

<span data-ttu-id="8693c-118">Toote teabehalduses on olemas valik seadistustabeleid, kus saate lisada viiteteabe, mis on esitatud ohtlike kaupade loendites maantee-, õhu- ja meretranspordi jaoks.</span><span class="sxs-lookup"><span data-stu-id="8693c-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="8693c-119">Siin on mõned määrused, millele sageli viidatakse.</span><span class="sxs-lookup"><span data-stu-id="8693c-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="8693c-120">**ADR** – määrused, mis on seotud ohtlike kaupade rahvusvahelise autoveoga</span><span class="sxs-lookup"><span data-stu-id="8693c-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="8693c-121">**CFR 49** – Ameerika Ühendriikide määrused ohtlike kaupade veo kohta</span><span class="sxs-lookup"><span data-stu-id="8693c-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="8693c-122">**IMDG** – rahvusvaheline ohtlike kaupade (IMDG) kood</span><span class="sxs-lookup"><span data-stu-id="8693c-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="8693c-123">**IATA** – Rahvusvahelise Lennutranspordi Assotsiatsiooni (IATA) ohtlike kaupade määrused</span><span class="sxs-lookup"><span data-stu-id="8693c-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="8693c-124">Kõigis neis määrustes on viitekoode sisaldav ohtlike kaupade loend.</span><span class="sxs-lookup"><span data-stu-id="8693c-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="8693c-125">Iga transporditüübi loendid on kombineeritud rahvusvaheliste ühisklassifikaatoritega.</span><span class="sxs-lookup"><span data-stu-id="8693c-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="8693c-126">Supply Chain Management pakub nende loendite ühiskasutatavate koodide viitetabeli.</span><span class="sxs-lookup"><span data-stu-id="8693c-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="8693c-127">Igal loendil on ka mõned unikaalsed koodid, mida saab määratleda.</span><span class="sxs-lookup"><span data-stu-id="8693c-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="8693c-128">Selle teabe konfigureerimise alustamiseks looge määrus, mida saate kasutada algsete parameetrite konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8693c-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="8693c-129">Laohaldus</span><span class="sxs-lookup"><span data-stu-id="8693c-129">Warehouse management</span></span>

<span data-ttu-id="8693c-130">Kui saadetis on ette valmistatud, saab printida mitu uut aruannet.</span><span class="sxs-lookup"><span data-stu-id="8693c-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="8693c-131">Need aruanded kasutavad teavet, mida olete toote teabehalduses seadistanud.</span><span class="sxs-lookup"><span data-stu-id="8693c-131">These reports use the information that you set up in Product information management.</span></span>
