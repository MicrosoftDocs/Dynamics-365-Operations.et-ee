---
title: Pealevõtmismooduli sisseregistreerimine
description: See teema kirjeldab pealevõtmise registreerimise moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0baa922afc72778dd6e4836398a280cbe6abaec2
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270579"
---
# <a name="check-in-for-pickup-module"></a><span data-ttu-id="f48e6-103">Pealevõtmismooduli sisseregistreerimine</span><span class="sxs-lookup"><span data-stu-id="f48e6-103">Check-in for pickup module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f48e6-104">See teema kirjeldab pealevõtmise registreerimise moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="f48e6-104">This topic covers the check-in for pickup module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="f48e6-105">Pealeregistreerimise moodulis on kinnitusleht klientide jaoks, kes kasutavad kliendi sisseregistreerimise võimalusi kauplusesse Dynamics 365 Commerce saabumisest teavitada.</span><span class="sxs-lookup"><span data-stu-id="f48e6-105">The check-in for pickup module provides a confirmation page for customers who use the Dynamics 365 Commerce customer check-in capabilities to notify a store about their arrival.</span></span> <span data-ttu-id="f48e6-106">Pealeregistreerimise moodul võimaldab teil konfigureerida vormi, mis kogub klientidelt lisateavet, et tellimuse tarnet hõlbustada.</span><span class="sxs-lookup"><span data-stu-id="f48e6-106">The check-in for pickup module also lets you configure a form that collects additional information from customers to facilitate order delivery.</span></span> <span data-ttu-id="f48e6-107">See teave sisaldab kliendi parkimiskoha numbrit ning oma sõiduki tootjat ja mudelit.</span><span class="sxs-lookup"><span data-stu-id="f48e6-107">This information includes a customer's parking spot number, and the make and model of their vehicle.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="f48e6-108">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="f48e6-108">Module properties</span></span>

| <span data-ttu-id="f48e6-109">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="f48e6-109">Property name</span></span> | <span data-ttu-id="f48e6-110">Väärtused</span><span class="sxs-lookup"><span data-stu-id="f48e6-110">Values</span></span> | <span data-ttu-id="f48e6-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f48e6-111">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="f48e6-112">Kinnitustekst</span><span class="sxs-lookup"><span data-stu-id="f48e6-112">Confirmation text</span></span> | <span data-ttu-id="f48e6-113">Tekstistring</span><span class="sxs-lookup"><span data-stu-id="f48e6-113">Text string</span></span> | <span data-ttu-id="f48e6-114">Sisseregistreerimise kinnituse lehel kuvatava pealkirja sisu.</span><span class="sxs-lookup"><span data-stu-id="f48e6-114">Content for the heading that appears on the check-in confirmation page.</span></span> |
| <span data-ttu-id="f48e6-115">Kuva QR-koodi</span><span class="sxs-lookup"><span data-stu-id="f48e6-115">Show QR code</span></span> | <span data-ttu-id="f48e6-116">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="f48e6-116">**True** or **False**</span></span> | <span data-ttu-id="f48e6-117">Kui atribuudi väärtuseks on seatud **Tõene**, kuvatakse sisseregistreerimise kinnituslehel QR-kood, mis tähistab tellimuse kinnituse ID-d.</span><span class="sxs-lookup"><span data-stu-id="f48e6-117">When this property is set to **True**, the check-in confirmation page shows a QR code that represents the order confirmation ID.</span></span> |
| <span data-ttu-id="f48e6-118">Lisateabe pealkiri</span><span class="sxs-lookup"><span data-stu-id="f48e6-118">Additional information heading</span></span> | <span data-ttu-id="f48e6-119">Tekstistring</span><span class="sxs-lookup"><span data-stu-id="f48e6-119">Text string</span></span> | <span data-ttu-id="f48e6-120">Täiendavate teabeväljade konfigureerimisel kuvatava pealkirja sisu.</span><span class="sxs-lookup"><span data-stu-id="f48e6-120">Content for the heading that appears when additional information fields have been configured.</span></span> |
| <span data-ttu-id="f48e6-121">Lisateabe klahvid</span><span class="sxs-lookup"><span data-stu-id="f48e6-121">Additional information keys</span></span> | <span data-ttu-id="f48e6-122">Ressursi ID / ressursi väärtuse paar</span><span class="sxs-lookup"><span data-stu-id="f48e6-122">Resource ID/resource value pair</span></span> | <span data-ttu-id="f48e6-123">Iga võti loob vormi välja ja sellega seotud sildi, mida kasutatakse klientidelt lisateabe kogumiseks.</span><span class="sxs-lookup"><span data-stu-id="f48e6-123">Each key creates a form field and an associated label that are used to collect additional information from customers.</span></span> |
| <span data-ttu-id="f48e6-124">Täiendavate teabevõtmete \> ressursi ID</span><span class="sxs-lookup"><span data-stu-id="f48e6-124">Additional information keys \> Resource ID</span></span> | <span data-ttu-id="f48e6-125">Tekstistring</span><span class="sxs-lookup"><span data-stu-id="f48e6-125">Text string</span></span> | <span data-ttu-id="f48e6-126">Iga infovõti loob vormi välja ja sellega seotud sildi, mida kasutatakse klientidelt lisateabe kogumiseks.</span><span class="sxs-lookup"><span data-stu-id="f48e6-126">Each information key creates a form field and an associated label that are used to collect additional information from customers.</span></span> <span data-ttu-id="f48e6-127">See atribuut tuvastab lisateabe võtme.</span><span class="sxs-lookup"><span data-stu-id="f48e6-127">This property identifies the additional information key.</span></span> <span data-ttu-id="f48e6-128">Kassas (POS) loodud ülesandes kuvatakse selle atribuudi väärtus juhiste väljal sildina.</span><span class="sxs-lookup"><span data-stu-id="f48e6-128">In the task that is created in point of sale (POS), the value of this property is shown as the label in the instructions field.</span></span> |
| <span data-ttu-id="f48e6-129">Täiendavate teabevõtmete \> ressursi väärtus</span><span class="sxs-lookup"><span data-stu-id="f48e6-129">Additional information keys \> Resource value</span></span> | <span data-ttu-id="f48e6-130">Tekstistring</span><span class="sxs-lookup"><span data-stu-id="f48e6-130">Text string</span></span> | <span data-ttu-id="f48e6-131">Kassasoleva ülesande tekstivälja silt.</span><span class="sxs-lookup"><span data-stu-id="f48e6-131">The label for the text field in the task in POS.</span></span> |
| <span data-ttu-id="f48e6-132">Täiendavate teabevõtmete \> on nõutav</span><span class="sxs-lookup"><span data-stu-id="f48e6-132">Additional information keys \> Required</span></span> | <span data-ttu-id="f48e6-133">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="f48e6-133">**True** or **False**</span></span> | <span data-ttu-id="f48e6-134">See atribuut määrab, kas kliendid peavad vormi välja enne jätkamist täitma.</span><span class="sxs-lookup"><span data-stu-id="f48e6-134">This property specifies whether customers must fill in the form field before they can continue.</span></span> <span data-ttu-id="f48e6-135">Kui selle atribuudi väärtuseks on seatud **Tõene**, renderdatakse vormi sildi kõrvale tärn ja tehakse tühikontroll, et takistada klientide jätkamist, kui ühtegi väärtust ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="f48e6-135">When this property is set to **True**, an asterisk is rendered next to the form label, and a null check is done to prevent customers from continuing if no value is entered.</span></span> |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a><span data-ttu-id="f48e6-136">Lehele sisseregistreerimise mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="f48e6-136">Add the check-in for pickup module to a page</span></span>

<span data-ttu-id="f48e6-137">Sisseregistreerimise mooduli registreerimine tuleb lisada uuele lehele, mille loote sisseregistreerimise kinnituse jaoks.</span><span class="sxs-lookup"><span data-stu-id="f48e6-137">The check-in for pickup module should be added to the new page that you create for check-in confirmation.</span></span> <span data-ttu-id="f48e6-138">See lehekülg on sisseregistreerimise kinnituskogemus klientide jaoks, kes valivad lingi **Olen siin** või nupu oma meilis.</span><span class="sxs-lookup"><span data-stu-id="f48e6-138">That page will serve as the check-in confirmation experience for customers who select the **I am here** link or button in their email.</span></span> 

## <a name="configure-the-additional-information-form"></a><span data-ttu-id="f48e6-139">Lisateabe vormi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f48e6-139">Configure the additional information form</span></span>

<span data-ttu-id="f48e6-140">Vaikimisi, kui rohkem teabevõtmeid pole konfigureeritud, näitab moodul vaikimisi kliente sisseregistreerimise kinnituslehekülge.</span><span class="sxs-lookup"><span data-stu-id="f48e6-140">By default, if no additional information keys are configured, the module shows customers the check-in confirmation page.</span></span> <span data-ttu-id="f48e6-141">Kuna kuvatakse sisseregistreerimise kinnitust, luuakse müügikohas ülesanne kauplusele, kust tellimus peale võetakse.</span><span class="sxs-lookup"><span data-stu-id="f48e6-141">As the check-in confirmation is shown, a task is created in POS for the store where the order is being picked up.</span></span>

<span data-ttu-id="f48e6-142">Kui konfigureeritakse üks või mitu täiendavat teabevõtit, palutakse klientidel kõigepealt sisestada teave.</span><span class="sxs-lookup"><span data-stu-id="f48e6-142">When one or more additional information keys are configured, customers are first prompted to enter information.</span></span> <span data-ttu-id="f48e6-143">Kui valite **Edasta**, kuvatakse neile sisseregistreerimise kinnitus ja kassas luuakse ülesanne.</span><span class="sxs-lookup"><span data-stu-id="f48e6-143">When they select **Submit**, they are shown the check-in confirmation, and a task is created in POS.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="f48e6-144">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f48e6-144">Additional resources</span></span>

[<span data-ttu-id="f48e6-145">Luba kliendi sisseregistreerimise teatised kassas (POS)</span><span class="sxs-lookup"><span data-stu-id="f48e6-145">Enable customer check-in notifications in point of sale (POS)</span></span>](enable-customer-check-in.md)
