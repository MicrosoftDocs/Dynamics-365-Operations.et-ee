---
title: Mobiilse seadme menüüelemendi seadistamine komplekteerimisrea ülevaate kuvamiseks
description: Selles teemas selgitatakse, kuidas määratleda, millal kuvatakse mobiilses seadmes laotööd töötlevatele laotöötajatele kõigi tööridade loend. See võimalus võib olla kasulik laotöötajatele, kes vajavad sageli ülevaadet töökäsu komplekteerimisridadest, et nad saaksid komplekteerimisjärjekorda optimeerida.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: a52a789044ca66c6771224a6cf0be8749bc99e5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/23/2020
ms.locfileid: "3837308"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="2ffca-104">Mobiilse seadme menüüelemendi seadistamine komplekteerimisrea ülevaate kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="2ffca-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2ffca-105">Selles teemas selgitatakse, kuidas konfigureerida suvandeid, mis on seotud komplekteerimisrea ülevaatega mobiilse seadme menüüelementide jaoks, mida kasutatakse komplekteerimistöö töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="2ffca-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="2ffca-106">Komplekteerimisrea ülevaade laseb laotöötajatel vaadata nende kõikide praeguse ülesandega seotud tööridade loendit ja seal valikuid teha.</span><span class="sxs-lookup"><span data-stu-id="2ffca-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="2ffca-107">See võimalus aitab töötajatel oma komplekteerimisjärjekorda optimeerida.</span><span class="sxs-lookup"><span data-stu-id="2ffca-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="2ffca-108">Funktsioon pakub suvandeid, mis asendavad standardse nupu **Jäta vahele**, mis võimaldab töötajatel read ükshaaval kindlas järjekorras läbi käia.</span><span class="sxs-lookup"><span data-stu-id="2ffca-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="2ffca-109">(Selle nupu kasutamise suvand on siiski alles.)</span><span class="sxs-lookup"><span data-stu-id="2ffca-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="2ffca-110">Administraatorid saavad iga menüüelementi ükshaaval konfigureerida, et kontrollida, kuidas, millal ja kus laorakenduses komplekteerimisrea ülevaade kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="2ffca-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="2ffca-111">Töö komplekteerimisrea ülevaate funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="2ffca-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="2ffca-112">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="2ffca-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="2ffca-113">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="2ffca-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="2ffca-114">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="2ffca-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="2ffca-115">**Moodul:** _laohaldus_</span><span class="sxs-lookup"><span data-stu-id="2ffca-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="2ffca-116">**Funktsiooni nimi:** _töö komplekteerimisrea ülevaade_</span><span class="sxs-lookup"><span data-stu-id="2ffca-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="2ffca-117">Menüüelementide konfigureerimine kõiki tööridade loendi kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="2ffca-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="2ffca-118">Mobiilse seadme menüüelemendi seadistamiseks komplekteerimisrea ülevaate kuvamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="2ffca-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="2ffca-119">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="2ffca-120">Valige või looge menüüelement, mis on seotud komplekteerimistööga, ja määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="2ffca-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="2ffca-121">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="2ffca-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="2ffca-122">**Kasuta olemasolevat tööd:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="2ffca-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="2ffca-123">**Juhtija:** *kasutaja juhitud* või *süsteemi juhitud*</span><span class="sxs-lookup"><span data-stu-id="2ffca-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="2ffca-124">Lisateavet selle kohta, kuidas luua menüüelemente ja kasutada mitmesuguseid sätteid, mis on saadaval lehel **Mobiilse seadme menüüelemendid**, leiate teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="2ffca-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="2ffca-125">Konfigureerige funktsioon kiirkaardil **Üldine**, seades välja **Kuva tööridade loend** väärtuseks üks järgmistest.</span><span class="sxs-lookup"><span data-stu-id="2ffca-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="2ffca-126">**Kuva ainult taotlemisel** – töötajad saavad kuvada komplekteerimisloendi, valides laorakenduses nupu **Hüppa selle juurde**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="2ffca-127">**Kuva iga komplekteerimise alguses** – töötajatele kuvatakse loend iga kord, kui nad alustavad või viivad komplekteerimisrea lõpule.</span><span class="sxs-lookup"><span data-stu-id="2ffca-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="2ffca-128">Samuti saavad nad loendit uuesti vaadata, valides laorakenduses nupu **Hüppa selle juurde**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="2ffca-129">**Kuva ainult esimese komplekteerimise alguses** – töötajatele kuvatakse loend iga uue komplekteerimistöö alustamisel, kuid mitte iga rea järel.</span><span class="sxs-lookup"><span data-stu-id="2ffca-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="2ffca-130">Samuti saavad nad loendit uuesti vaadata, valides laorakenduses nupu **Hüppa selle juurde**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="2ffca-131">**Ära kuva kunagi** – laorakenduses kuvatakse standardne nupp **Jäta vahele** ning tööridade loendi kuvamine lülitatakse välja.</span><span class="sxs-lookup"><span data-stu-id="2ffca-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="2ffca-132">Nupp **Jäta vahele** võimaldab töötajatel read ükshaaval kindlas järjekorras läbi käia.</span><span class="sxs-lookup"><span data-stu-id="2ffca-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="2ffca-133">Nad võivad loendi läbi käia nii mitu korda kui vaja, kuni kõik read on töödeldud.</span><span class="sxs-lookup"><span data-stu-id="2ffca-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="2ffca-134">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="2ffca-135">Kui seate välja **Kuva tööridade loend** väärtuseks mõne muu väärtuse peale *Ära kuva kunagi*, muutub kättesaadavaks toimingupaanil olev nupp **Väljaloend**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="2ffca-136">Valige toimingupaanil **Väljaloend**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="2ffca-137">Konfigureerige lehel **Väljaloend** teave, mis kuvatakse laorakenduses iga loendis oleva rea puhul.</span><span class="sxs-lookup"><span data-stu-id="2ffca-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="2ffca-138">Välja **Esmane juhtelement** väärtuseks on alati seatud *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="2ffca-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="2ffca-139">Seetõttu algab loendi iga rida reanumbriga.</span><span class="sxs-lookup"><span data-stu-id="2ffca-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="2ffca-140">Kasutage ülejäänud välju **Kuvaväli**, et lisada vajaduse järgi kuni seitse täiendavat kuvavälja.</span><span class="sxs-lookup"><span data-stu-id="2ffca-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="2ffca-141">Valige igal väljal **Kuvaväli** töörea välja nimi.</span><span class="sxs-lookup"><span data-stu-id="2ffca-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="2ffca-142">Igal real kuvatakse seejärel selle välja väärtus.</span><span class="sxs-lookup"><span data-stu-id="2ffca-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="2ffca-143">Väärtused kuvatakse siin valitud järjekorras.</span><span class="sxs-lookup"><span data-stu-id="2ffca-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="2ffca-144">Võite jätta mõned väljad **Kuvaväli** tühjaks, kui teil pole kõiki seitset väärtust vaja.</span><span class="sxs-lookup"><span data-stu-id="2ffca-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="2ffca-145">Valige toimingupaanil **Salvesta** ja sulgege siis leht **Väljaloend**.</span><span class="sxs-lookup"><span data-stu-id="2ffca-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>
