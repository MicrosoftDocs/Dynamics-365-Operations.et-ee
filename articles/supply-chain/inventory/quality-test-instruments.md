---
title: Kvaliteedijuhtimise testvahendid
description: See teema kirjeldab, kuidas luua testvahendeid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestInstrument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc09021f89a9064a3140a726fca74e3eceab13da
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956625"
---
# <a name="quality-management-test-instruments"></a><span data-ttu-id="13eed-103">Kvaliteedijuhtimise testvahendid</span><span class="sxs-lookup"><span data-stu-id="13eed-103">Quality management test instruments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="13eed-104">See teema kirjeldab, kuidas luua testvahendeid, mida saab kasutada kvaliteettellimuste testidel Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="13eed-104">This topic describes how to create test instruments that can be used for tests on quality orders in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="13eed-105">Kasutate **Testvahendite** lehte, et määrata ja vaadata üksikasju seadmete kohta, mida kasutatakse kvaliteettellimustel testide sooritamiseks.</span><span class="sxs-lookup"><span data-stu-id="13eed-105">You use the **Test instruments** page to define and view details about the devices that are used to perform tests on quality orders.</span></span> <span data-ttu-id="13eed-106">Testvahendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="13eed-106">Test instruments are optional.</span></span> <span data-ttu-id="13eed-107">Kuid need võivad aidata kvaliteeditöötajatel teada, millist seadet või tööriista nad peaksid konkreetse testi tegemiseks kasutama.</span><span class="sxs-lookup"><span data-stu-id="13eed-107">However, they can help quality workers know which device or tool they should use to perform a specific test.</span></span>

## <a name="test-instrument-example"></a><span data-ttu-id="13eed-108">Testvahendi näide</span><span class="sxs-lookup"><span data-stu-id="13eed-108">Test instrument example</span></span>

<span data-ttu-id="13eed-109">Teete mitmesuguseid elektrikomponentide teste.</span><span class="sxs-lookup"><span data-stu-id="13eed-109">You're performing various tests on electrical components.</span></span> <span data-ttu-id="13eed-110">Mõned testid on mõeldud komponentide väljundpingele, üks test nende temperatuurile ja üks test nende kaalu jaoks.</span><span class="sxs-lookup"><span data-stu-id="13eed-110">Some tests are for the voltage output of the components, one test is for their temperature, and one test is for their weight.</span></span> <span data-ttu-id="13eed-111">Iga testi tegemiseks kasutatakse erinevaid tööriistu, seadmeid või varustust.</span><span class="sxs-lookup"><span data-stu-id="13eed-111">Different tools, devices, or equipment is used to perform each test.</span></span> <span data-ttu-id="13eed-112">Näiteks kasutatakse pinge mõõtmiseks pingemõõturit, temperatuuri mõõtmiseks termomeetrit ja kaalu mõõtmiseks kaalu.</span><span class="sxs-lookup"><span data-stu-id="13eed-112">For example, a voltage meter is used to measure voltage, a thermometer is used to measure temperature, and a scale is used to measure weight.</span></span> <span data-ttu-id="13eed-113">Kõiki neid seadmeid saate seadistada testimisinstrumentidena ja märkida mõõtühik, milles testitulemused tuleks salvestada.</span><span class="sxs-lookup"><span data-stu-id="13eed-113">You can configure each of these devices as a test instrument and indicate the unit of measure that the test results should be recorded in.</span></span> <span data-ttu-id="13eed-114">Näiteks registreeritakse pingemõõturi tulemused voltides, termomeetri tulemused registreeritakse Fahrenheiti või Celsiuse skaalal kraadides ning kaalumise tulemused registreeritakse naela või kilogrammina.</span><span class="sxs-lookup"><span data-stu-id="13eed-114">For example, results from the voltage meter are recorded in volts, results from the thermometer are recorded in degrees Fahrenheit or degrees Celsius, and results from the scale are recorded in pounds or kilograms.</span></span>

## <a name="create-a-test-instrument"></a><span data-ttu-id="13eed-115">Testvahendi loomine</span><span class="sxs-lookup"><span data-stu-id="13eed-115">Create a test instrument</span></span>

1. <span data-ttu-id="13eed-116">Avage **Varude haldus \> Seaded \> Kvaliteedijuhtimine \> Testvahendid**.</span><span class="sxs-lookup"><span data-stu-id="13eed-116">Go to **Inventory management \> Setup \> Quality control \> Test instruments**.</span></span>
1. <span data-ttu-id="13eed-117">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="13eed-117">On the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="13eed-118">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="13eed-118">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="13eed-119">**Testvahendid** – Sisestage testvahendi kordumatu ID või nimi.</span><span class="sxs-lookup"><span data-stu-id="13eed-119">**Test instrument** – Enter a unique ID or name for the test instrument.</span></span>
    - <span data-ttu-id="13eed-120">**Kirjeldus** – Sisestage testvahendi detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="13eed-120">**Description** – Enter a detailed description of the test instrument.</span></span>
    - <span data-ttu-id="13eed-121">**Ühik** – Valige mõõtühik, milles seade tulemuse annab.</span><span class="sxs-lookup"><span data-stu-id="13eed-121">**Unit** – Select the unit that the instrument measures results in.</span></span> <span data-ttu-id="13eed-122">**Täpsus** väli seatakse automaatselt valitud ühiku põhjal.</span><span class="sxs-lookup"><span data-stu-id="13eed-122">The **Precision** field is automatically set, based on the unit that you select.</span></span>

1. <span data-ttu-id="13eed-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="13eed-123">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13eed-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="13eed-124">Additional resources</span></span>

- [<span data-ttu-id="13eed-125">Kvaliteedijuhtimise test</span><span class="sxs-lookup"><span data-stu-id="13eed-125">Quality management test</span></span>](quality-tests.md)
- [<span data-ttu-id="13eed-126">Kvaliteedijuhtimise testgrupid</span><span class="sxs-lookup"><span data-stu-id="13eed-126">Quality management test groups</span></span>](quality-test-groups.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
