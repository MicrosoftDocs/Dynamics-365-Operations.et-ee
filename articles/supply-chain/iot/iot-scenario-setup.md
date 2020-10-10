---
title: IoT iseõppimisvõime stsenaariumi seadistamine
description: Selles teemas selgitatakse, kuidas konfigureerida stsenaariume IoT iseõppimisvõime jaoks rakenduses Microsoft Dynamics 365 Supply Chain Management.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d1deaa2130b63272da39a42315c6a1bc4b7ccb8a
ms.sourcegitcommit: 8adc65e26d78e229271eb427659a87ee5f371319
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/15/2020
ms.locfileid: "3814055"
---
# <a name="scenario-setup-for-iot-intelligence"></a><span data-ttu-id="f0e28-103">IoT iseõppimisvõime stsenaariumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="f0e28-103">Scenario setup for IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f0e28-104">Selles teemas selgitatakse, kuidas konfigureerida stsenaariume IoT iseõppimisvõime jaoks rakenduses Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0e28-104">This topic explains how to configure scenarios for IoT Intelligence in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f0e28-105">Enne stsenaariumide seadistamist tuleb teil [seadistada teenused Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span><span class="sxs-lookup"><span data-stu-id="f0e28-105">Before you can set up the scenarios, you must [set up Microsoft Dynamics Lifecycle Services (LCS)](iot-lcs-setup.md).</span></span>

<span data-ttu-id="f0e28-106">Selles teemas konfigureerite stsenaariumi **Seadmete seisakuaeg**, et masina tõrgete puhul luuaks rakenduses Supply Chain Management teatis.</span><span class="sxs-lookup"><span data-stu-id="f0e28-106">In this topic, you will configure the **Equipment downtime** scenario so that a notification is generated in Supply Chain Management when a machine goes down.</span></span> <span data-ttu-id="f0e28-107">Selles teemas näidatakse ka, kuidas konfigureerida stsenaariumi **Tootekvaliteet**, et kauba atribuudi jäämisel väljapoole määratud vahemikku luuaks teatis, ja kuidas konfigureerida stsenaariumi **Tootmisviivitused**, et olukorras, kus tootmise läbilaskevõime jääb allapoole läviväärtust, luuaks teatis.</span><span class="sxs-lookup"><span data-stu-id="f0e28-107">The topic also shows how to configure the **Product quality** scenario so that a notification is generated if an attribute of an item is outside a specified range, and how to configure the **Production delays** scenario so that a notification is generated if the production throughput falls below a threshold value.</span></span>

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a><span data-ttu-id="f0e28-108">Stsenaariumi Seadmete seisakuaeg konfigureerimine Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="f0e28-108">Configure the Equipment downtime scenario in Supply Chain Management</span></span>

<span data-ttu-id="f0e28-109">Stsenaarium **Seadmete seisakuaeg** vastendab märguande **PartOut** masina teatiste lävega.</span><span class="sxs-lookup"><span data-stu-id="f0e28-109">The **Equipment downtime** scenario maps a **PartOut** signal to a machine alert threshold.</span></span> <span data-ttu-id="f0e28-110">Masinat jälgitakse ainult juhul, kui see on selle stsenaariumi jaoks valitud ja kui selle olekuks on rakenduses Supply Chain Management seatud **Töötab**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-110">The machine is monitored only when it's selected for the scenario and when is set to **Running** in Supply Chain Management.</span></span> <span data-ttu-id="f0e28-111">Kui aeg, millal masinast saadi viimati märguanne **PartOut**, on suurem kui teatiste lävi, käivitatakse teatis **Masina seisak**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-111">If the time since a **PartOut** signal was last received from the machine exceeds the alert threshold, a **Machine down** notification is triggered.</span></span> <span data-ttu-id="f0e28-112">Kui masin töötab edasi, käivitatakse järgmise märguande **PartOut** saamisel teatis **Masin töötab**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-112">If the machine is still running, a **Machine up** notification is triggered when the next **PartOut** signal is received.</span></span> <span data-ttu-id="f0e28-113">Kui masina seisak kestab 30 minutit, käivitatakse uus teatis **Masina seisak**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-113">If a machine stays down for 30 minutes, a new **Machine down** notification is triggered.</span></span>

<span data-ttu-id="f0e28-114">Stsenaariumil **Seadmete seisakuaeg** on järgmised sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="f0e28-114">The **Equipment downtime** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="f0e28-115">Teatist saab käivitada ainult juhul, kui tootmistellimus töötab vastendatud masinal.</span><span class="sxs-lookup"><span data-stu-id="f0e28-115">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="f0e28-116">Märguanne, mis esindab vastendatud masina märguannet **PartOut**, tuleb saata IoT keskusesse koos kordumatu atribuudinimega.</span><span class="sxs-lookup"><span data-stu-id="f0e28-116">A signal that represents a mapped machine's **PartOut** signal must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="f0e28-117">Azure'i IoT keskuse teade peab sisaldama UNIX-i atribuuti **ajatempel**, mille väärtust väljendatakse millisekundites (ms).</span><span class="sxs-lookup"><span data-stu-id="f0e28-117">A UNIX **timestamp** property, where the value is expressed in milliseconds (ms), must be present in the Azure IoT Hub message.</span></span>

<span data-ttu-id="f0e28-118">Stsenaariumi konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="f0e28-118">To configure the scenario, follow these steps.</span></span>

1. <span data-ttu-id="f0e28-119">Logige sisse rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f0e28-119">Sign in to Supply Chain Management.</span></span>
2. <span data-ttu-id="f0e28-120">Lubage IoT iseõppimisvõime funktsiooni lipp.</span><span class="sxs-lookup"><span data-stu-id="f0e28-120">Enable the IoT Intelligence feature flag.</span></span> <span data-ttu-id="f0e28-121">Lisateavet vt [Funktsioonihalduse ülevaatest](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="f0e28-121">For more information, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
3. <span data-ttu-id="f0e28-122">Konfigureerige mõõdikud.</span><span class="sxs-lookup"><span data-stu-id="f0e28-122">Configure the metrics.</span></span> <span data-ttu-id="f0e28-123">Vaadake lisateavet teemast [Kuidas konfigureerida mõõdikuid](iot-metrics-setup.md#configure-metrics).</span><span class="sxs-lookup"><span data-stu-id="f0e28-123">For more information, see [How to configure metrics](iot-metrics-setup.md#configure-metrics).</span></span>
4. <span data-ttu-id="f0e28-124">Avage **Tootmise juhtimine \> Seadistus \> IoT iseõppimisvõime \> Stsenaariumihaldus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-124">Go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
6. <span data-ttu-id="f0e28-125">Valige paanil **Seadmete seisakuaeg** suvand **Konfigureeri**, et avada viisard.</span><span class="sxs-lookup"><span data-stu-id="f0e28-125">On the **Equipment downtime** tile, select **Configure** to open the configuration wizard.</span></span>

   <span data-ttu-id="f0e28-126">Viisardi esimene leht on **Seadmete anduri skeemi määratlus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-126">The first page in the wizard is the **Equipment sensor schema definition** page.</span></span> <span data-ttu-id="f0e28-127">Sellel lehel on teie eesmärk seadistada rakenduses Supply Chain Management skeem nii, et see ühtiks IoT keskuse teadete vorminguga JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="f0e28-127">On this page, your goal is to set up the schema in Supply Chain Management so that it matches the JavaScript Object Notation (JSON) format of the IoT Hub messages.</span></span> <span data-ttu-id="f0e28-128">Saate määratleda mitu teateskeemi.</span><span class="sxs-lookup"><span data-stu-id="f0e28-128">Multiple message schemas can be defined.</span></span> <span data-ttu-id="f0e28-129">Vaadake lisateavet teemast [IoT keskuse teadete skeemivormingud](iot-schema-format.md).</span><span class="sxs-lookup"><span data-stu-id="f0e28-129">For more information, see [Schema formats for IoT Hub messages](iot-schema-format.md).</span></span> <span data-ttu-id="f0e28-130">Selles näites sisaldab teate last järgmises vormingus teadete partiid.</span><span class="sxs-lookup"><span data-stu-id="f0e28-130">In this example, the message payload contains a batch of messages that has the following format.</span></span>

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

7. <span data-ttu-id="f0e28-131">Lisage tabelisse rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f0e28-131">Add a row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="f0e28-132">Seadke välja **Skeemi nimi** väärtuseks **ID**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-132">Set the **Schema name** field to **ID**.</span></span>
    2. <span data-ttu-id="f0e28-133">Seadke välja **Skeemi tee** väärtuseks **/payload\[\*\]/id**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-133">Set the **Schema path** field to **/payload\[\*\]/id**.</span></span>
    3. <span data-ttu-id="f0e28-134">Seadke välja **Kirjeldus** väärtuseks **Teate ID**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-134">Set the **Description** field to **Message ID**.</span></span>

8. <span data-ttu-id="f0e28-135">Lisage tabelisse veel üks rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f0e28-135">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="f0e28-136">Seadke välja **Skeemi nimi** väärtuseks **Ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-136">Set the **Schema name** field to **Timestamp**.</span></span>
    2. <span data-ttu-id="f0e28-137">Seadke välja **Skeemi tee** väärtuseks **/last\[\*\]/ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-137">Set the **Schema path** field to **/payload\[\*\]/timestamp**.</span></span>
    3. <span data-ttu-id="f0e28-138">Seadke välja **Kirjeldus** väärtuseks **Teate ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-138">Set the **Description** field to **Message timestamp**.</span></span>

9. <span data-ttu-id="f0e28-139">Lisage tabelisse veel üks rida ja seadke järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f0e28-139">Add another row to the table, and set the following values:</span></span>

    1. <span data-ttu-id="f0e28-140">Seadke välja **Skeemi nimi** väärtuseks **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-140">Set the **Schema name** field to **Value**.</span></span>
    2. <span data-ttu-id="f0e28-141">Seadke välja **Skeemi tee** väärtuseks **/last\[\*\]/väärtus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-141">Set the **Schema path** field to **/payload\[\*\]/value**.</span></span>
    3. <span data-ttu-id="f0e28-142">Seadke välja **Kirjeldus** väärtuseks **Teate väärtus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-142">Set the **Description** field to **Message value**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0e28-143">Te ei pea kõiki teate atribuute määratlema.</span><span class="sxs-lookup"><span data-stu-id="f0e28-143">You don't have to define all the properties in the message.</span></span> <span data-ttu-id="f0e28-144">Määratlege ainult vajalikud atribuudid.</span><span class="sxs-lookup"><span data-stu-id="f0e28-144">Define only the properties that you require.</span></span> <span data-ttu-id="f0e28-145">Eelmiste sammude käigus ei loonud te rida **juurajatempli** jaoks.</span><span class="sxs-lookup"><span data-stu-id="f0e28-145">In the preceding steps, you didn't create a row for **Root timestamp**.</span></span> <span data-ttu-id="f0e28-146">Üksuse **Juurajatempel** tee oleks **/ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-146">The path of **Root timestamp** would be **/timestamp**.</span></span>

10. <span data-ttu-id="f0e28-147">Valige **Edasi**, et avada leht **Seadmete anduri skeemikaart**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-147">Select **Next** to go to the **Equipment sensor schema map** page.</span></span>
11. <span data-ttu-id="f0e28-148">Määrake **Seadmete ressursi ID** real välja **Skeemi nimi** väärtuseks **ID**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-148">In the row for **Equipment resource ID**, in the **Schema name** field, select **ID**.</span></span>
12. <span data-ttu-id="f0e28-149">Määrake rea **UTC-aeg** välja **Skeemi nimi** väärtuseks **Ajatempel**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-149">In the row for **UTC time**, in the **Schema name** field, select **Timestamp**.</span></span>
13. <span data-ttu-id="f0e28-150">Määrake real **Osaliselt toodetud märguanne** välja **Skeemi nimi** väärtuseks **Väärtus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-150">In the row for **Part produced signal**, in the **Schema name** field, select **Value**.</span></span>
14. <span data-ttu-id="f0e28-151">Valige **Edasi**, et minna lehele **Seadmete ressursi ID konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-151">Select **Next** to go to the **Equipment resource ID configuration** page.</span></span>
15. <span data-ttu-id="f0e28-152">Järgige neid juhiseid, et vastendada IoT keskuse teatiste väärtused rakenduse Supply Chain Management ressurssidega.</span><span class="sxs-lookup"><span data-stu-id="f0e28-152">Follow these steps to map the values in the IoT Hub message to the Supply Chain Management resources:</span></span>

    1. <span data-ttu-id="f0e28-153">Lisage tabelile **Märguande andmete väärtused** uus rida.</span><span class="sxs-lookup"><span data-stu-id="f0e28-153">In the **Signal Data Values** table, add a new row.</span></span> <span data-ttu-id="f0e28-154">Sisestage väljale **Väärtus** tekst **IoTInt.Machine1225.PartOut**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-154">In the **Value** field, enter **IoTInt.Machine1225.PartOut**.</span></span> <span data-ttu-id="f0e28-155">See väärtus on pärit IoT keskuse teate JSON-i atribuudist **id**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-155">This value  comes from the JSON **id** property in the IoT Hub message.</span></span>
    2. <span data-ttu-id="f0e28-156">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-156">Select **Save**.</span></span>
    3. <span data-ttu-id="f0e28-157">Valige tabelis **Ärikirje vastendamine** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-157">In the **Business Record Mapping** table, select **New**.</span></span> <span data-ttu-id="f0e28-158">Välja **Ärikirje tüüp** vaikeväärtus täidetakse automaatselt ja seda ei pea muutma.</span><span class="sxs-lookup"><span data-stu-id="f0e28-158">A default value for the **Business record type** field is automatically filled in, and you don't have to change it.</span></span>
    4. <span data-ttu-id="f0e28-159">Valige väljal **Ärikirje** rakenduse Supply Chain Management masina ressurss, kust selle märguande väärtus saadetakse.</span><span class="sxs-lookup"><span data-stu-id="f0e28-159">In the **Business record** field, select the Supply Chain Management machine resource that the signal value is being sent from.</span></span>
    5. <span data-ttu-id="f0e28-160">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-160">Select **Save**.</span></span>
    6. <span data-ttu-id="f0e28-161">Korrake neid samme, et lisada üksusele **Machine1226** uus ärikirje vastendus.</span><span class="sxs-lookup"><span data-stu-id="f0e28-161">Repeat these steps to add a new business record mapping for **Machine1226**.</span></span> <span data-ttu-id="f0e28-162">Ühe kirjega saate rakenduses Supply Chain Management vastendada mitu märguande andmete väärtust.</span><span class="sxs-lookup"><span data-stu-id="f0e28-162">You can map multiple signal data values to a single record in Supply Chain Management.</span></span>

16. <span data-ttu-id="f0e28-163">Kasutage veergu **Valitud**, et valida masinad, mida soovite töödelda.</span><span class="sxs-lookup"><span data-stu-id="f0e28-163">Use the **Selected** column to select the machines that you want to process.</span></span> <span data-ttu-id="f0e28-164">Kõiki märguande väärtusi ei pea määratlema ja kõiki masinaid ei pea valima.</span><span class="sxs-lookup"><span data-stu-id="f0e28-164">You don't have to define all signal values, and you don't have to select all machines.</span></span>
17. <span data-ttu-id="f0e28-165">Valige **Edasi**, et avada **Osaliselt toodetud märguande konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-165">Select **Next** to go to the **Part produced signal configuration** page.</span></span>
18. <span data-ttu-id="f0e28-166">Lisage rida tabelisse **Märguande andmete väärtused** ja seadke välja **Väärtus** väärtuseks **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-166">In the **Signal Data Values** table, add a row, and set the **Value** field to **True**.</span></span> <span data-ttu-id="f0e28-167">See väärtus on pärit IoT keskuse teate JSON-i atribuudist **väärtus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-167">This value comes from the JSON **value** property in the IoT Hub message.</span></span> <span data-ttu-id="f0e28-168">Saate lisada nii palju väärtusi, kui oma stsenaariumi jaoks vajate.</span><span class="sxs-lookup"><span data-stu-id="f0e28-168">You can add as many values as you require for your scenario.</span></span>
19. <span data-ttu-id="f0e28-169">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-169">Select **Save**.</span></span>
20. <span data-ttu-id="f0e28-170">Valige **Edasi**, et avada leht **Seadmete seisakuaja lävi**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-170">Select **Next** to go to the **Equipment downtime threshold** page.</span></span> <span data-ttu-id="f0e28-171">Loetletud masinad on varem märguande väärtustega vastendatud masinad.</span><span class="sxs-lookup"><span data-stu-id="f0e28-171">The machines that are listed are the machines that were previously mapped to signal values.</span></span> <span data-ttu-id="f0e28-172">Sellel lehel määratlete läve masina seisaku tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0e28-172">On this page, you will define a threshold to determine whether a machine is down.</span></span> <span data-ttu-id="f0e28-173">Näiteks kui seate läve väärtuseks **10**, loob rakendus Supply Chain Management teatise, kui masinalt ei tule 10 minuti jooksul märguannet **PartOut**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-173">For example, if you set the threshold to **10**, Supply Chain Management will generate a notification if no **PartOut** signal is received from a machine for 10 minutes.</span></span>
21. <span data-ttu-id="f0e28-174">Lehele **Stsenaariumi lubamine** minemiseks valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-174">Select **Next** to go to the **Enable scenario** page.</span></span> <span data-ttu-id="f0e28-175">Seadistage suvand stsenaariumi lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0e28-175">Set the option to enable the scenario.</span></span>
22. <span data-ttu-id="f0e28-176">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-176">Select **Finish**.</span></span>

<span data-ttu-id="f0e28-177">Stsenaariumi seadistus on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="f0e28-177">The scenario setup is now completed.</span></span> <span data-ttu-id="f0e28-178">IoT iseõppimisvõime alustab automaatselt IoT keskuse teatiste töötlemist.</span><span class="sxs-lookup"><span data-stu-id="f0e28-178">IoT Intelligence will automatically start to process the IoT Hub messages.</span></span>

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a><span data-ttu-id="f0e28-179">Stsenaariumi Toote kvaliteet konfigureerimine Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="f0e28-179">Configure the Product quality scenario in Supply Chain Management</span></span>

<span data-ttu-id="f0e28-180">Stsenaarium **Toote kvaliteet** loob teatise, kui kauba atribuut jääb määratletud vahemikust väljapoole.</span><span class="sxs-lookup"><span data-stu-id="f0e28-180">The **Product quality** scenario generates a notification if an attribute of an item is outside a specified range.</span></span> <span data-ttu-id="f0e28-181">Näiteks saadab sensor iga kauba kaalu IoT keskusesse.</span><span class="sxs-lookup"><span data-stu-id="f0e28-181">For example, a sensor sends the weight of each item to IoT Hub.</span></span> <span data-ttu-id="f0e28-182">Kui kaup on liiga raske või liiga kerge, luuakse rakenduses Supply Chain Management teatis.</span><span class="sxs-lookup"><span data-stu-id="f0e28-182">If an item is too heavy or too light, a notification is generated in Supply Chain Management.</span></span>

<span data-ttu-id="f0e28-183">Stsenaariumil **Tootekvaliteet** on järgmised sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="f0e28-183">The **Product quality** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="f0e28-184">Teatis käivitatakse ainult siis, kui tootmistellimus töötab vastendatud masinal ja toodab vastendatud partiiatribuuti omavat toodet.</span><span class="sxs-lookup"><span data-stu-id="f0e28-184">An alert can be triggered only if a production order is running on a mapped machine and producing a product that has a mapped batch attribute.</span></span>
+ <span data-ttu-id="f0e28-185">Partiiatribuuti esindav märguanne tuleb saata IoT keskusesse koos kordumatu atribuudinimega.</span><span class="sxs-lookup"><span data-stu-id="f0e28-185">A signal that represents the batch attribute must be sent to the IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="f0e28-186">IoT keskuse teade peab sisaldama UNIX-i atribuuti **ajatempel**, mille väärtust väljendatakse millisekundites.</span><span class="sxs-lookup"><span data-stu-id="f0e28-186">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a><span data-ttu-id="f0e28-187">Stsenaariumi Tootmise viivitused konfigureerimine Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="f0e28-187">Configure the Production delays scenario in Supply Chain Management</span></span>

<span data-ttu-id="f0e28-188">Stsenaarium **Tootmise viivitused** loob teatise, kui tootmise läbilaskevõime langeb alla läve väärtuse.</span><span class="sxs-lookup"><span data-stu-id="f0e28-188">The **Production delays** scenario generates a notification if the production throughput falls below a threshold value.</span></span> <span data-ttu-id="f0e28-189">Selle stsenaariumi puhul saadetakse IoT keskusesse märguanne **PartOut** iga toodetava kauba kohta.</span><span class="sxs-lookup"><span data-stu-id="f0e28-189">In this scenario, a **PartOut** signal is sent to IoT Hub for each item that is produced.</span></span> <span data-ttu-id="f0e28-190">Rakenduses Supply Chain Management arvutatakse tellimuse viivitus selle põhjal, kui pikalt on tootmistellimuse käitamine plaanitud, mitu kaupa tuleks toota, kui kaua tööd on käitatud ja mitu märguannet **PartOut** vastu võetakse.</span><span class="sxs-lookup"><span data-stu-id="f0e28-190">In Supply Chain Management, the order delay is calculated based on the amount of time that the production order is scheduled to run, the number of items that should be produced, the amount of time that the job has been running, and the number of **PartOut** signals that are received.</span></span> <span data-ttu-id="f0e28-191">Viivituse teatis luuakse siis, kui töö märguannete **PartOut** arv jääb läviväärtusest allapoole.</span><span class="sxs-lookup"><span data-stu-id="f0e28-191">A delay notification is generated if the number of **PartOut** signals for the job falls below the threshold value.</span></span>

<span data-ttu-id="f0e28-192">Stsenaariumil **Tootmise viivitused** on järgmised sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="f0e28-192">The **Production delays** scenario has the following dependencies:</span></span>

+ <span data-ttu-id="f0e28-193">Teatist saab käivitada ainult juhul, kui tootmistellimus töötab vastendatud masinal.</span><span class="sxs-lookup"><span data-stu-id="f0e28-193">An alert can be triggered only if a production order is running on a mapped machine.</span></span>
+ <span data-ttu-id="f0e28-194">Märguanne, mis esindab vastendatud masina märguannet **PartOut**, tuleb saata Azure'i IoT keskusesse koos kordumatu atribuudinimega.</span><span class="sxs-lookup"><span data-stu-id="f0e28-194">A signal that represents a mapped machine's **PartOut** signal must be sent to the Azure IoT hub, and a unique property name must be included.</span></span>
+ <span data-ttu-id="f0e28-195">IoT keskuse teade peab sisaldama UNIX-i atribuuti **ajatempel**, mille väärtust väljendatakse millisekundites.</span><span class="sxs-lookup"><span data-stu-id="f0e28-195">A UNIX **timestamp** property, where the value is expressed in ms, must be present in the IoT Hub message.</span></span>

## <a name="disable-a-scenario"></a><span data-ttu-id="f0e28-196">Stsenaariumi keelamine</span><span class="sxs-lookup"><span data-stu-id="f0e28-196">Disable a scenario</span></span>

<span data-ttu-id="f0e28-197">Stsenaariumi keelamiseks järgige neid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="f0e28-197">To disable a scenario, follow these steps.</span></span>

1. <span data-ttu-id="f0e28-198">Avage rakenduses Supply Chain Management suvand **Tootmise juhtimine \> Seadistus \> IoT iseõppimisvõime \> Stsenaariumihaldus**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-198">In Supply Chain Management, go to **Production control \> Setup \> IoT Intelligence \> Scenario management**.</span></span>
2. <span data-ttu-id="f0e28-199">Stsenaariumi paanil valige **Konfigureeri**.</span><span class="sxs-lookup"><span data-stu-id="f0e28-199">On the tile for the scenario, select **Configure**.</span></span>
3. <span data-ttu-id="f0e28-200">Valige **Edasi**, et minna viimasele viisardilehele.</span><span class="sxs-lookup"><span data-stu-id="f0e28-200">Select **Next** to go to the last wizard page.</span></span>
4. <span data-ttu-id="f0e28-201">Seadistage suvand stsenaariumi keelamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0e28-201">Set the option to disable the scenario.</span></span>
