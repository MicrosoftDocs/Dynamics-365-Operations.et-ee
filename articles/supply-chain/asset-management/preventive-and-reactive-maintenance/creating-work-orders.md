---
title: Töökäskude loomine
description: Selles teemas tutvustatakse, kuidas luua töökäske varahalduses.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 876aef9f3f470490bb385e1861c837dcfa82db69
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131789"
---
# <a name="creating-work-orders"></a><span data-ttu-id="af0c2-103">Töökäskude loomine</span><span class="sxs-lookup"><span data-stu-id="af0c2-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af0c2-104">Pärast ennetavate hooldustööde plaanimist on järgmine etapp luua nende jaoks töökäsud.</span><span class="sxs-lookup"><span data-stu-id="af0c2-104">After you've scheduled preventive maintenance jobs, the next step is to create work orders for them.</span></span> <span data-ttu-id="af0c2-105">Saate seda teha, kasutades ühte hooldusgraafikutest.</span><span class="sxs-lookup"><span data-stu-id="af0c2-105">You can complete this step by using one of the maintenance schedules.</span></span> <span data-ttu-id="af0c2-106">Plaanitud töödel võib hooldusgraafikus olla erinevad viitetüübid, nagu järgmises tabelis on kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="af0c2-106">The scheduled jobs in a maintenance schedule can have different reference types, as described in the following table.</span></span>

| <span data-ttu-id="af0c2-107">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="af0c2-107">Reference type</span></span> | <span data-ttu-id="af0c2-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="af0c2-108">Description</span></span> |
|---|---|
| <span data-ttu-id="af0c2-109">Hoolduskavad</span><span class="sxs-lookup"><span data-stu-id="af0c2-109">Maintenance plans</span></span> | <span data-ttu-id="af0c2-110">Ennetavad hooldustööd, mis põhinevad hoolduskava tüübil *Aeg* või *Loendur*.</span><span class="sxs-lookup"><span data-stu-id="af0c2-110">Preventive maintenance jobs that are based on the *Time* or *Counter* maintenance plan type.</span></span> |
| <span data-ttu-id="af0c2-111">Hoolduskorrad</span><span class="sxs-lookup"><span data-stu-id="af0c2-111">Maintenance rounds</span></span> | <span data-ttu-id="af0c2-112">Ennetavad hooldustööd, mis sisaldavad mitut sarnast tüüpi hooldust nõudvat vara.</span><span class="sxs-lookup"><span data-stu-id="af0c2-112">Preventive maintenance jobs that contain several assets that require a similar type of maintenance.</span></span> |
| <span data-ttu-id="af0c2-113">Hooldusnõue</span><span class="sxs-lookup"><span data-stu-id="af0c2-113">Maintenance request</span></span> | <span data-ttu-id="af0c2-114">Käsitsi loodud vara hoolduse või paranduse taotlus.</span><span class="sxs-lookup"><span data-stu-id="af0c2-114">A manually created request for maintenance or repair of an asset.</span></span> <span data-ttu-id="af0c2-115">Selle taotluse saab teisendada töökäsuks.</span><span class="sxs-lookup"><span data-stu-id="af0c2-115">This request can be converted to a work order.</span></span> |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a><span data-ttu-id="af0c2-116">Töökäskude loomine teie hooldusgraafikute põhjal</span><span class="sxs-lookup"><span data-stu-id="af0c2-116">Create work orders based on your maintenance schedule</span></span>

<span data-ttu-id="af0c2-117">Hooldusgraafikul põhinevate töökäskude loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="af0c2-117">To create work orders that are based on your maintenance schedule, follow these steps.</span></span>

1. <span data-ttu-id="af0c2-118">Avage üks järgmistest lehekülgedest, olenevalt sellest, kuidas te soovite oma töökäsud oma ajakava üksuste jaoks valida.</span><span class="sxs-lookup"><span data-stu-id="af0c2-118">Open one of the following pages, depending on how you want to select schedule items for your work orders:</span></span>

    - <span data-ttu-id="af0c2-119">Kogu hooldusgraafik (**Varahaldus \> Haldusgraafik \> Kogu hooldusgraafik**)</span><span class="sxs-lookup"><span data-stu-id="af0c2-119">All maintenance schedule (**Asset management \> Management schedule \> All maintenance schedule**)</span></span>
    - <span data-ttu-id="af0c2-120">Hooldusgraafiku ridade avamine (**Varahaldus \> Haldusgraafik \> Ava hooldusgraafiku read**)</span><span class="sxs-lookup"><span data-stu-id="af0c2-120">Open maintenance schedule lines (**Asset management \> Management schedule \> Open maintenance schedule lines**)</span></span>
    - <span data-ttu-id="af0c2-121">Hooldusgraafiku kaustade avamine (**Varahaldus \> Haldusgraafik \> Ava hooldusgraafiku kaustad**)</span><span class="sxs-lookup"><span data-stu-id="af0c2-121">Open maintenance schedule pools (**Asset management \> Management schedule \> Open maintenance schedule pools**)</span></span>

1. <span data-ttu-id="af0c2-122">Märkige ruudustikus märkeruut iga planeeritud hooldustöö puhul, mille jaoks soovite töökäsu luua.</span><span class="sxs-lookup"><span data-stu-id="af0c2-122">In the grid, select the check box for every scheduled maintenance job that you want to create a work order for.</span></span> <span data-ttu-id="af0c2-123">Seejärel valige toimingupaanil suvand **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="af0c2-123">Then, on the Action Pane, select **Work order**.</span></span>

    <span data-ttu-id="af0c2-124">Kuvatakse dialoogiboks **Töökäskude loomine**.</span><span class="sxs-lookup"><span data-stu-id="af0c2-124">The **Create work orders** dialog box appears.</span></span> <span data-ttu-id="af0c2-125">Väli **Hooldusprognoosi tunnid** näitab valitud ridade prognoosi tundide koguarvu.</span><span class="sxs-lookup"><span data-stu-id="af0c2-125">The **Maintenance forecast hours** field shows the total number of forecast hours for the selected lines.</span></span>

    ![Töökäskude loomise dialoogiboks](media/18-preventive-maintenance.png)

1. <span data-ttu-id="af0c2-127">Määrake jaotises **Parameetrid** loodavate töökäskude arv.</span><span class="sxs-lookup"><span data-stu-id="af0c2-127">In the **Parameters** section, specify the number of work orders that should be created.</span></span> <span data-ttu-id="af0c2-128">Tehke üks järgmistest valikutest:</span><span class="sxs-lookup"><span data-stu-id="af0c2-128">Select one of the following options:</span></span>

    - <span data-ttu-id="af0c2-129">**Üks töökäsk rea kohta** – looge üks töötellimus iga hooldusgraafiku rea kohta.</span><span class="sxs-lookup"><span data-stu-id="af0c2-129">**One work order per line** – Create one work order per maintenance schedule line.</span></span>
    - <span data-ttu-id="af0c2-130">**Üks töökäsk** – looge töökäsud, mis on rühmitatud vastavalt teiste suvandite sätetele, mis muutuvad selle suvandi valimisel kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="af0c2-130">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="af0c2-131">Väljal **Töökäsu tüüp** valige töökäsu tüüp, mida kõigi loodavate töötellimuste puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="af0c2-131">In the **Work order type** field, select the work order type to use for all the work orders that you create.</span></span>
1. <span data-ttu-id="af0c2-132">Vastavalt oma seadistustele töökäskude loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="af0c2-132">Select **OK** to create the work orders according to your settings.</span></span>

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a><span data-ttu-id="af0c2-133">Hooldusplaani käitamise ajal automaatselt loodavate töökäsu ridade rühmitamine</span><span class="sxs-lookup"><span data-stu-id="af0c2-133">Group work order lines that are automatically created while a maintenance plan runs</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af0c2-134">Selles jaotises kirjeldatud funktsioon on saadaval eelväljaande osana.</span><span class="sxs-lookup"><span data-stu-id="af0c2-134">The functionality that is described in this section is available as part of a preview release.</span></span> <span data-ttu-id="af0c2-135">Sisu ja funktsioonid võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="af0c2-135">The content and the functionality are subject to change.</span></span> <span data-ttu-id="af0c2-136">Lisateavet eelväljaannete kohta vt teemast [Ühe versiooni teenuse värskenduste KKK](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span><span class="sxs-lookup"><span data-stu-id="af0c2-136">For more information about preview releases, see [One version service updates FAQ](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/one-version).</span></span>

<span data-ttu-id="af0c2-137">See funktsioon võimaldab teil määrata reeglid töökäsu ridade rühmitamiseks ühe töökäsu alla, kui süsteem on häälestatud koostama töökäske hooldusplaani põhjal automaatselt.</span><span class="sxs-lookup"><span data-stu-id="af0c2-137">This feature lets you define rules for grouping work order lines under a single work order when the system is set up to generate work orders automatically, based on a maintenance plan.</span></span> <span data-ttu-id="af0c2-138">Varem võisid automaatselt loodud töökäsud sisaldada ainult ühte rida.</span><span class="sxs-lookup"><span data-stu-id="af0c2-138">Previously, automatically generated work orders could contain only one line.</span></span> <span data-ttu-id="af0c2-139">Samas nüüd saate töökäske rühmitada näiteks vara, vara tüübi või töö asukoha alusel.</span><span class="sxs-lookup"><span data-stu-id="af0c2-139">However, you can now group work orders by, for example, asset, asset type, or functional location.</span></span> <span data-ttu-id="af0c2-140">(Käsitsi loodud töökäske sai sel viisil juba rühmitada, nagu selle teema eelmises jaotises on kirjeldatud.)</span><span class="sxs-lookup"><span data-stu-id="af0c2-140">(Manually generated work orders could already be grouped in this way, as described in the previous section of this topic.)</span></span>

### <a name="enable-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="af0c2-141">Automaatselt loodud töökäskude rühmitamise lubamine</span><span class="sxs-lookup"><span data-stu-id="af0c2-141">Enable grouping for automatically generated work orders</span></span>

<span data-ttu-id="af0c2-142">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="af0c2-142">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="af0c2-143">Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="af0c2-143">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="af0c2-144">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="af0c2-144">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="af0c2-145">**Moodul:** *varahaldus*</span><span class="sxs-lookup"><span data-stu-id="af0c2-145">**Module:** *Asset Management*</span></span>
- <span data-ttu-id="af0c2-146">**Funktsiooni nimi:** *(Eelversioon) Töökäskude rühmitamise reeglite rakendamine hooldusplaani käitades*</span><span class="sxs-lookup"><span data-stu-id="af0c2-146">**Feature name:** *(Preview) Apply rules for grouping work orders while running a maintenance plan*</span></span>

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a><span data-ttu-id="af0c2-147">Automaatselt loodud töökäskude rühmitamise häälestamine</span><span class="sxs-lookup"><span data-stu-id="af0c2-147">Set up grouping for automatically generated work orders</span></span>

<span data-ttu-id="af0c2-148">Automaatselt loodud töökäskude rühmitamise häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="af0c2-148">To set up grouping for automatically generated work orders, follow these steps.</span></span>

1. <span data-ttu-id="af0c2-149">Avage **Varahaldus \> Seadistus \> Ennetav hooldus \> Hooldusplaanid**.</span><span class="sxs-lookup"><span data-stu-id="af0c2-149">Go to **Asset management \> Setup \> Preventative maintenance \> Maintenance plans**.</span></span>
1. <span data-ttu-id="af0c2-150">Iga plaani jaoks, kus soovite rühmitatud töökäsud luua, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="af0c2-150">For each plan where you want to generate grouped work orders, follow these steps:</span></span>

    1. <span data-ttu-id="af0c2-151">Valige loendipaanil plaan.</span><span class="sxs-lookup"><span data-stu-id="af0c2-151">Select the plan in the list pane.</span></span>
    1. <span data-ttu-id="af0c2-152">Veenduge kiirkaardil **Read**, et märkeruut **Loo automaatselt** oleks igal real valitud.</span><span class="sxs-lookup"><span data-stu-id="af0c2-152">On the **Lines** FastTab, make sure that the **Auto create** check box is selected on every line.</span></span>

1. <span data-ttu-id="af0c2-153">Avage **Varahaldus \> Perioodiline \> Ennetav hooldus \> Hoolduskavade plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="af0c2-153">Go to **Asset management \> Periodic \> Preventive maintenance \> Schedule maintenance plans**.</span></span>
1. <span data-ttu-id="af0c2-154">Dialoogiboksis **Hoolduskavade plaanimine** jaotises **Perioodiline** määrake plaani ajahorisont (kui kaugele töö loomise jaoks plaanitud hooldustööde otsimisel ette vaadata).</span><span class="sxs-lookup"><span data-stu-id="af0c2-154">In the **Schedule maintenance plans** dialog box, in the **Period** section, specify the time horizon for the plan (how far to look ahead when finding scheduled maintenance jobs to generate work for).</span></span>
1. <span data-ttu-id="af0c2-155">Määrake suvand **Loo töökäsk graafikust automaatselt** valikule *Jah*.</span><span class="sxs-lookup"><span data-stu-id="af0c2-155">Set the **Automatically create work order from schedule** option to *Yes*.</span></span>
1. <span data-ttu-id="af0c2-156">Valige jaotisest **Töökäsk** üks järgmistest suvanditest.</span><span class="sxs-lookup"><span data-stu-id="af0c2-156">In the **Work order** section, select one of the following options:</span></span>

    - <span data-ttu-id="af0c2-157">**Üks töökäsk rea kohta** – looge üks töötellimus iga hooldusgraafiku rea kohta.</span><span class="sxs-lookup"><span data-stu-id="af0c2-157">**One work order per line** – Create one work order per maintenance schedule line.</span></span> <span data-ttu-id="af0c2-158">(See suvand pakub samu funktsioone, mis on saadaval, kui funktsioon *Töökäskude rühmitamise reeglite rakendamine hooldusplaani käitades* on välja lülitatud.)</span><span class="sxs-lookup"><span data-stu-id="af0c2-158">(This option provides the same functionality that is available when the *Apply rules for grouping work orders while running a maintenance plan* feature is turned off.)</span></span>
    - <span data-ttu-id="af0c2-159">**Üks töökäsk** – looge töökäsud, mis on rühmitatud vastavalt teiste suvandite sätetele, mis muutuvad selle suvandi valimisel kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="af0c2-159">**One work order per** – Create work orders that are grouped according to the settings of the other options that become available when you select this option.</span></span>

1. <span data-ttu-id="af0c2-160">Kui soovite valikuid rakendada siis, kui käivitate ainult mõned oma hoolduskavad, lisage kiirkaardil **Kaasatavad kirjed** vastavalt vajadusele filtrid, nagu võite teha Microsoft Dynamics 365 Supply Chain Managementi teiste pakett-tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="af0c2-160">If you want the options to apply when you run only some of your maintenance plans, on the **Records to include** FastTab, add filters as you require, just as you might do for other batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="af0c2-161">Häälestage kiirkaardil **Käivita taustal** vastavalt vajadusele partii ja plaanimise valikud, nagu võite teha teiste rakenduse Supply Chain Management pakett-töödes.</span><span class="sxs-lookup"><span data-stu-id="af0c2-161">On the **Run in the background** FastTab, set up batch and scheduling options as you require, just as you might do for other batch jobs in Supply Chain Management.</span></span>
1. <span data-ttu-id="af0c2-162">Valitud hoolduskavade käivitamiseks ja/või plaanimiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="af0c2-162">Select **OK** to run and/or schedule the selected maintenance plans.</span></span>
