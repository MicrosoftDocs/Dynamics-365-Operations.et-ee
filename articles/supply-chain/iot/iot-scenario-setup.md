---
title: IoT iseõppimisvõime stsenaariumi seadistamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida stsenaariumi Supply Chain Managementis IoT iseõppimisvõime jaoks.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5633741fcd9c04b68e5b174447d7ead3c521ccd7
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597164"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="e3b26-103">IoT iseõppimisvõime stsenaariumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="e3b26-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3b26-104">Selles teemas kirjeldatakse, kuidas konfigureerida stsenaariumi Supply Chain Managementis IoT iseõppimisvõime jaoks.</span><span class="sxs-lookup"><span data-stu-id="e3b26-104">This topic describes how to configure a scenario in Supply Chain Management for IoT Intelligence.</span></span> <span data-ttu-id="e3b26-105">Enne, kui saate seadistada stsenaariume, peate [seadistama LCS-i](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="e3b26-105">Before you can setup the scenarios, you must [setup LCS](iot-lcs-setup.md).</span></span>

<span data-ttu-id="e3b26-106">Selles teemas konfigureerite stsenaariumi **Seadmete seisakuaeg** teatise loomiseks Supply Chain Managementis masina tõrgete puhul.</span><span class="sxs-lookup"><span data-stu-id="e3b26-106">In this topic, you will configure the **Equipment downtime** scenario to generate a notification in Supply Chain Management when a machine goes down.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="e3b26-107">Stsenaariumi **Seadmete seisakuaeg** konfigureerimine Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="e3b26-107">Configure the **Equipment downtime** scenario in Supply Chain Management</span></span>

<span data-ttu-id="e3b26-108">Stsenaarium **Seadmete seisakuaeg** vastendab märguande osalisest väljas masina teatiste lävele.</span><span class="sxs-lookup"><span data-stu-id="e3b26-108">The **Equipment downtime** scenario maps a part out signal to a machine alert threshold.</span></span> <span data-ttu-id="e3b26-109">Masinat jälgitakse ainult juhul, kui see on selle stsenaariumi jaoks valitud ja on seatud käitama Supply Chain managementis.</span><span class="sxs-lookup"><span data-stu-id="e3b26-109">The machine is monitored only when the machine is selected for the scenario and is set to running in Supply Chain Management.</span></span> <span data-ttu-id="e3b26-110">Kui aeg, millal seade sai viimati märguande osaliselt väljas, on suurem kui teatise lävi, käivitatakse teatis **Masina seisak**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-110">If the time since the machine’s last received Part Out signal is greater than the alert threshold, then a **Machine down** notification is triggered.</span></span> <span data-ttu-id="e3b26-111">Kui masin töötab edasi kuni järgmise märguande **PartOut** saamiseni käivitatakse teatis **Masin töötab**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-111">If the machine is still running, when the next **PartOut** signal is received a **Machine up** notification is triggered.</span></span> <span data-ttu-id="e3b26-112">Kui masina seisak kestab 30 minutit, käivitatakse uus teatis **Masina seisak**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-112">If a machine stays down for 30 mins a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="e3b26-113">Stsenaariumil **Seadmete seisakuaeg** on järgmised sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="e3b26-113">The **Equipment downtime** scenario has these dependencies:</span></span>

+ <span data-ttu-id="e3b26-114">Teatise käivitamiseks tuleb käivitada tootmistellimus vastendatud masinal.</span><span class="sxs-lookup"><span data-stu-id="e3b26-114">A production order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="e3b26-115">Vastendatud masina signaali osaliselt väljas esindav märguanne tuleb saata kordumatu atribuudi nimega IoT-keskusesse.</span><span class="sxs-lookup"><span data-stu-id="e3b26-115">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="e3b26-116">IoT-keskuse sõnum peab sisaldama Unixi millisekundites ajatempli atribuuti.</span><span class="sxs-lookup"><span data-stu-id="e3b26-116">A Unix milliseconds timestamp property must be present in the IoT hub message.</span></span>

<span data-ttu-id="e3b26-117">Stsenaariumi konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e3b26-117">To configure the scenario, follow these steps:</span></span>

1. <span data-ttu-id="e3b26-118">Logige sisse Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="e3b26-118">Log into Supply Chain Management.</span></span>
2. <span data-ttu-id="e3b26-119">Lubage IoT iseõppimisvõime funktsiooni lipp.</span><span class="sxs-lookup"><span data-stu-id="e3b26-119">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="e3b26-120">Lisateavet vt [Funktsioonihalduse ülevaatest](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e3b26-120">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
3. <span data-ttu-id="e3b26-121">Konfigureerige mõõdikud.</span><span class="sxs-lookup"><span data-stu-id="e3b26-121">Configure the metrics.</span></span> <span data-ttu-id="e3b26-122">Vaadake lisateavet teemast [Kuidas konfigureerida mõõdikuid](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="e3b26-122">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="e3b26-123">Liikuge jaotisse **Tootmise juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-123">Navigate to **Production control**.</span></span>
5. <span data-ttu-id="e3b26-124">Liikuge jaotisse **Seadistus \> IoT iseõppimisvõime \> Stsenaariumide haldus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-124">Navigate to **Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="e3b26-125">Klõpsake paani **Seadmete seisakuaeg** nuppu **Konfigureeri**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-125">Click **Configure** on the **Equipment downtime** tile.</span></span> <span data-ttu-id="e3b26-126">Konfigureerimisviisard algab lehega **Seadmete anduri skeemi määratlus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-126">The configuration wizard starts with the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="e3b26-127">Selle eesmärk on seadistada skeem Supply Chain Managementis, et see vastaks IoT sõnumite JSON-vormingule.</span><span class="sxs-lookup"><span data-stu-id="e3b26-127">The goal here is to setup the schema in Supply Chain Management to match the JSON format of the IoT messages.</span></span> <span data-ttu-id="e3b26-128">Saate määratleda mitu sõnumiskeemi.</span><span class="sxs-lookup"><span data-stu-id="e3b26-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="e3b26-129">Vaadake lisateavet teemast [IoT-keskuse sõnumiskeemi vormingud](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="e3b26-129">For more information, see [Message schema formats for IoT Hub](iot-schema-format.md).</span></span> <span data-ttu-id="e3b26-130">Selles näites sisaldab sõnumi koormus järgmise vorminguga sõnumite partiid.</span><span class="sxs-lookup"><span data-stu-id="e3b26-130">In this example, the message payload contains a batch of messages with this format:</span></span>

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. <span data-ttu-id="e3b26-131">Lisage tabelisse rida.</span><span class="sxs-lookup"><span data-stu-id="e3b26-131">Add a row to the table.</span></span>

    1. <span data-ttu-id="e3b26-132">Määrake välja **Skeemi nimi** väärtuseks **ID**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-132">Set the **Schema name** to **ID**.</span></span>
    2. <span data-ttu-id="e3b26-133">Määrake välja **Skeemi tee** väärtuseks **/payload[\*]/id**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-133">Set the **Schema path** to **/payload[\*]/id**.</span></span>
    3. <span data-ttu-id="e3b26-134">Määrake välja **Kirjeldus** väärtuseks **Sõnumi ID**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-134">Set the **Description** to **Message ID**.</span></span>

8. <span data-ttu-id="e3b26-135">Lisage tabelisse rida.</span><span class="sxs-lookup"><span data-stu-id="e3b26-135">Add a row to the table.</span></span>

    1. <span data-ttu-id="e3b26-136">Määrake välja **Skeemi nimi** väärtuseks **Ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-136">Set the **Schema name** to **Timestamp**.</span></span>
    2. <span data-ttu-id="e3b26-137">Määrake välja **Skeemi tee** väärtuseks **/payload[\*]/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-137">Set the **Schema path** to **/payload[\*]/timestamp**.</span></span>
    3. <span data-ttu-id="e3b26-138">Määrake välja **Kirjeldus** väärtuseks **Sõnumi ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-138">Set the **Description** to **Message timestamp**.</span></span>

9. <span data-ttu-id="e3b26-139">Lisage tabelisse rida.</span><span class="sxs-lookup"><span data-stu-id="e3b26-139">Add a row to the table.</span></span>

    1. <span data-ttu-id="e3b26-140">Määrake välja **Skeemi nimi** väärtuseks **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-140">Set the **Schema name** to **Value**.</span></span>
    2. <span data-ttu-id="e3b26-141">Määrake välja **Skeemi tee** väärtuseks **/payload[\*]/value**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-141">Set the **Schema path** to **/payload[\*]/value**.</span></span>
    3. <span data-ttu-id="e3b26-142">Määrake välja **Kirjeldus** väärtuseks **Sõnumi väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-142">Set the **Description** to **Message value**.</span></span>

    <span data-ttu-id="e3b26-143">Teil pole vaja määratleda sõnumi kõiki atribuute, ainult neid, mida vajate.</span><span class="sxs-lookup"><span data-stu-id="e3b26-143">You don't need to define all the properties in the message, only the ones that you need.</span></span> <span data-ttu-id="e3b26-144">Selles näites ei loonud te rida üksusele **Juurajatempel**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-144">In this example, you did not create a row for **Root timestamp**.</span></span> <span data-ttu-id="e3b26-145">Üksuse **Juurajatempel** tee oleks **/timestamp**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-145">The path for **Root timestamp** would be **/timestamp**.</span></span>
  
10. <span data-ttu-id="e3b26-146">Klõpsake nuppu **Edasi**, et avada leht **Seadmete anduri skeemikaart**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-146">Click **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="e3b26-147">Määrake real **Seadmete ressursi ID** välja **Skeemi nimi** väärtuseks **ID**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-147">In the row for **Equipment resource ID** set the **Schema name** to **ID**.</span></span> <span data-ttu-id="e3b26-148">Kehtivad väärtused kuvatakse ripploendi tabelis.</span><span class="sxs-lookup"><span data-stu-id="e3b26-148">The valid values are displayed in a dropdown table.</span></span>
12. <span data-ttu-id="e3b26-149">Määrake rea **UTC-aeg** välja **Skeemi nimi** väärtuseks **Ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-149">In the row for **UTC time** set the **Schema name** to **Timestamp**.</span></span> <span data-ttu-id="e3b26-150">Kehtivad väärtused kuvatakse ripploendi tabelis.</span><span class="sxs-lookup"><span data-stu-id="e3b26-150">The valid values are displayed in a dropdown table.</span></span>
13. <span data-ttu-id="e3b26-151">Määrake real **Osaliselt toodetud märguanne** välja **Skeemi nimi** väärtuseks **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-151">In the row for **Part produced signal** set the **Schema name** to **Value**.</span></span> <span data-ttu-id="e3b26-152">Kehtivad väärtused kuvatakse ripploendi tabelis.</span><span class="sxs-lookup"><span data-stu-id="e3b26-152">The valid values are displayed in a dropdown table.</span></span>
14. <span data-ttu-id="e3b26-153">Klõpsake nuppu **Edasi** lehe **Seadmete ressursi ID konfiguratsioon** jaoks.</span><span class="sxs-lookup"><span data-stu-id="e3b26-153">Click **Next** for the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="e3b26-154">Selles etapis vastendate IoT-keskuse sõnumi väärtused Supply Chain Managementi ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="e3b26-154">In this step, you map the IoT Hub message values to the Supply Chain Management resources.</span></span>

    1. <span data-ttu-id="e3b26-155">Lisage tabelis **Märguande andmete väärtused** uus rida ja sisestage veergu **Väärtus** väärtus **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-155">In the **Signal Data Values** table, add a new row, and enter **IoTInt.Machine1225.PartOut** in the **Value** column.</span></span> <span data-ttu-id="e3b26-156">Väärtus **IoTInt.Machine1225.PartOut** tuletatakse IoT-keskuse sõnumi JSON-i atribuudist **id**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-156">The value **IoTInt.Machine1225.PartOut** comes from the JSON **id** property in the IoT hub message.</span></span>
    2. <span data-ttu-id="e3b26-157">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-157">Click **Save**.</span></span>
    3. <span data-ttu-id="e3b26-158">Klõpsake tabelis **Ärikirje vastendamine** valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-158">In the **Business Record Mapping** table, click **New**.</span></span> <span data-ttu-id="e3b26-159">Välja **Ärikirje tüüp** vaikeväärtus asustatakse automaatselt ja seda ei pea muutma.</span><span class="sxs-lookup"><span data-stu-id="e3b26-159">The default value for the **Business record type** is autopopulated, and you don't need to change it.</span></span>
    4. <span data-ttu-id="e3b26-160">Valige veerus **Ärikirje** Supply Chain Managementi masina ressurss, kust selle signaali väärtus saadetakse.</span><span class="sxs-lookup"><span data-stu-id="e3b26-160">In the **Business record** column, select the Supple Chain Management machine resource this signal value is being sent from.</span></span>
    5. <span data-ttu-id="e3b26-161">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-161">Click **Save**.</span></span>
    6. <span data-ttu-id="e3b26-162">Korrake neid etappe, lisades uue ärikirje vastendamise üksusele **Machine1226**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-162">Repeat these steps, adding a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="e3b26-163">Saate vastendada mitu signaali andmete väärtust ühele kirjele Supply Chain Managementis.</span><span class="sxs-lookup"><span data-stu-id="e3b26-163">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="e3b26-164">Kasutage veergu **Valitud**, et valida, milliseid masinaid soovite töödelda.</span><span class="sxs-lookup"><span data-stu-id="e3b26-164">Use the **Selected** column to choose which machines you want to process.</span></span> <span data-ttu-id="e3b26-165">Kõiki märguande väärtusi ei pea määratlema ja kõiki masinaid ei pea valima.</span><span class="sxs-lookup"><span data-stu-id="e3b26-165">You do not have to define all signal values and you do not have to select all machines.</span></span>
17. <span data-ttu-id="e3b26-166">Klõpsake nuppu **Edasi** lehe **Osaliselt toodetud märguande konfigureerimine** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e3b26-166">Click **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="e3b26-167">Lisage rida tabelisse **Märguande andmete väärtused** ja seadke suvandi **Väärtu** väärtuseks **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-167">In the **Signal Data Values** table, add a row, and set **Value** to **True**.</span></span> <span data-ttu-id="e3b26-168">Väärtus **Tõene** tuletatakse IoT-keskuse sõnumi JSON-i atribuudist **väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-168">The value **True** comes from the JSON **value** property in the IoT hub message.</span></span> <span data-ttu-id="e3b26-169">Saate lisada nii palju väärtusi, kui oma stsenaariumi jaoks vajate.</span><span class="sxs-lookup"><span data-stu-id="e3b26-169">You can add as many values as you need for your scenario.</span></span>
19. <span data-ttu-id="e3b26-170">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-170">Click **Save**.</span></span>
20. <span data-ttu-id="e3b26-171">Klõpsake nuppu **Edasi**, et avada leht **Seadmete seisakuaja lävi**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-171">Click **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="e3b26-172">Loetletud masinad on varasemalt märguande väärtustele vastendatud masinad.</span><span class="sxs-lookup"><span data-stu-id="e3b26-172">The machines listed are the machines previously mapped to signal values.</span></span> <span data-ttu-id="e3b26-173">Selles etapis määratlete masina seisaku tuvastamise läve.</span><span class="sxs-lookup"><span data-stu-id="e3b26-173">In this step, you define a threshold to determine if a machine is down.</span></span> <span data-ttu-id="e3b26-174">Näiteks kui seate läve väärtuseks 10, loob Supply Chain Management teatise, kui masinalt ei tule 10 minuti jooksul sõnumit osaliselt väljas.</span><span class="sxs-lookup"><span data-stu-id="e3b26-174">For example, if you set the threshold to 10, Supply Chain Management generates a notification if there is no part out message from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="e3b26-175">Lehele **Stsenaariumi lubamine** minemiseks klõpsake valikut **Järgmine**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-175">Click **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="e3b26-176">Liigutage liugurit stsenaariumi lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="e3b26-176">Toggle the slider to enable the scenario.</span></span>
22. <span data-ttu-id="e3b26-177">Klõpsake nuppu **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-177">Click **Finish**.</span></span>

<span data-ttu-id="e3b26-178">Stsenaariumi häälestus on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e3b26-178">The scenario setup is complete.</span></span> <span data-ttu-id="e3b26-179">IoT iseõppimisvõime alustab automaatselt IoT-keskuse sõnumite töötlemist.</span><span class="sxs-lookup"><span data-stu-id="e3b26-179">IoT Intelligence will automatically start processing the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="e3b26-180">Stsenaariumi **Toote kvaliteet** konfigureerimine Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="e3b26-180">Configure the **Product quality** scenario in Supply Chain Management</span></span>

<span data-ttu-id="e3b26-181">Stsenaarium **Toote kvaliteet** loob teatise, kui kauba atribuut jääb määratletud vahemikust väljapoole.</span><span class="sxs-lookup"><span data-stu-id="e3b26-181">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="e3b26-182">Näiteks võib sensor saata iga kauba kaalu IoT-keskusesse.</span><span class="sxs-lookup"><span data-stu-id="e3b26-182">For example, a sensor could send the weight of each item to IoT Hub.</span></span> <span data-ttu-id="e3b26-183">Supply Chain Managementis luuakse teatis, kui kaup on liiga raske või liiga kerge.</span><span class="sxs-lookup"><span data-stu-id="e3b26-183">In Supply Chain Management, a notification would be generated if the item was too heavy or too light.</span></span>

<span data-ttu-id="e3b26-184">Stsenaariumil on järgmised sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="e3b26-184">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="e3b26-185">Tootmistellimus peab töötama vastendatud masinal ja tootma vastendatud partii atribuudiga toodet teatise käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="e3b26-185">A Production Order must be running on a mapped machine and producing a product with a mapped batch attribute for an alert to be triggered.</span></span>
+ <span data-ttu-id="e3b26-186">Partii atribuuti esindav märguanne tuleb saata kordumatu atribuudi nimega IoT-keskusesse.</span><span class="sxs-lookup"><span data-stu-id="e3b26-186">A signal representing the batch attribute must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="e3b26-187">IoT-keskuse sõnum peab sisaldama Unixi millisekundites ajatempli atribuuti.</span><span class="sxs-lookup"><span data-stu-id="e3b26-187">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="e3b26-188">Stsenaariumi **Tootmise viivitused** konfigureerimine Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="e3b26-188">Configure the **Production delays** scenario in Supply Chain Management</span></span>

<span data-ttu-id="e3b26-189">Stsenaarium **Tootmise viivitused** loob teatise, kui tootmise läbilaskevõime langeb alla läve väärtuse.</span><span class="sxs-lookup"><span data-stu-id="e3b26-189">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="e3b26-190">Selle stsenaariumi puhul saadetakse IoT-keskusesse märguanne **PartOut** iga toodetud kauba kohta.</span><span class="sxs-lookup"><span data-stu-id="e3b26-190">In this scenario, a **PartOut** signal is sent to IoT Hub for each item produced.</span></span> <span data-ttu-id="e3b26-191">Supply Chain Managementis arvutatakse tellimuse viivitus vastavalt sellele, kui pikalt on tootmistellimuse käitamine plaanitud, mitu kaupa tuleks toota, kui kaua tööd on käitatud ja mitu märguannet **PartOut** vastu võetakse.</span><span class="sxs-lookup"><span data-stu-id="e3b26-191">In Supply Chain Management, the order delay is calculated based on how long the production order is scheduled to run, how many items should be produced, how long the job has been running, and how many **PartOut** signals are received.</span></span> <span data-ttu-id="e3b26-192">Viivituse teatis luuakse siis, kui selle töö märguannete **PartOut** arv jääb eeldatava väärtuse läve väärtusest allapoole.</span><span class="sxs-lookup"><span data-stu-id="e3b26-192">A delay notification would be generated if the number of the **PartOut** signals for the job falls below the threshold value of the expected value.</span></span>

<span data-ttu-id="e3b26-193">Stsenaariumil on järgmised sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="e3b26-193">The scenario has these dependencies:</span></span>

+ <span data-ttu-id="e3b26-194">Teatise käivitamiseks tuleb käivitada tootmistellimus vastendatud masinal.</span><span class="sxs-lookup"><span data-stu-id="e3b26-194">A Production Order must be running on a mapped machine for an alert to be triggered.</span></span>
+ <span data-ttu-id="e3b26-195">Vastendatud masina signaali osaliselt väljas esindav märguanne tuleb saata kordumatu atribuudi nimega IoT-keskusesse.</span><span class="sxs-lookup"><span data-stu-id="e3b26-195">A signal representing a mapped machine's part out signal must be sent to the IoT Hub with a unique property name.</span></span>
+ <span data-ttu-id="e3b26-196">IoT-keskuse sõnum peab sisaldama Unixi millisekundites ajatempli atribuuti.</span><span class="sxs-lookup"><span data-stu-id="e3b26-196">A Unix milliseconds timestamp property must be present in the IoT Hub message.</span></span>

## <a name="how-to-disable-a-scenario"></a><span data-ttu-id="e3b26-197">Stsenaariumi keelamine</span><span class="sxs-lookup"><span data-stu-id="e3b26-197">How to disable a scenario</span></span>

<span data-ttu-id="e3b26-198">Stsenaariumi keelamiseks järgige neid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="e3b26-198">To disable a scenario, follow these steps:</span></span>

1. <span data-ttu-id="e3b26-199">Liikuge Supply Chain Managementi jaotisse **Tootmise juhtimine \> Häälestamine \> IoT iseõppimisvõime \> Stsenaariumihaldus**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-199">In Supply Chain Management, navigate to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="e3b26-200">Klõpsake stsenaariumi suvandit **Konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-200">Click **Configure** on the scenario.</span></span>
3. <span data-ttu-id="e3b26-201">Klõpsake viisardi viimasele vahekaardile jõudmiseks nuppu **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="e3b26-201">Click **Next** to get to the last wizard tab.</span></span>
4. <span data-ttu-id="e3b26-202">Liigutage liugurit stsenaariumi keelamiseks.</span><span class="sxs-lookup"><span data-stu-id="e3b26-202">Toggle the slider to disable the scenario.</span></span>
