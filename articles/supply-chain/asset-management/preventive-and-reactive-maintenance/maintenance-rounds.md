---
title: Hoolduskorrad
description: Selles teemas selgitatakse hoolduskordi varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97f1984b71ab60519f81bb1f6ab38278a0e5aa43
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206100"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="00ca3-103">Hoolduskorrad</span><span class="sxs-lookup"><span data-stu-id="00ca3-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="00ca3-104">**Varahalduses** saate luua hoolduskordi erinevatele varadele, mille juures on vaja teostada regulaarsete intervallidega sarnaseid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="00ca3-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="00ca3-105">Näiteks määrimistööd või ohutuskontrollid, mida tuleb teostada sama intervalliga mitmel masinal.</span><span class="sxs-lookup"><span data-stu-id="00ca3-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="00ca3-106">Esimene etapp on luua hoolduskord koos varadega, mis vajavad samas vormis hooldustööd.</span><span class="sxs-lookup"><span data-stu-id="00ca3-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="00ca3-107">Järgmisena ajastate hoolduskorrad.</span><span class="sxs-lookup"><span data-stu-id="00ca3-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="00ca3-108">Kui olete hoolduskordade ajastamise lõpetanud, näete kõiki hoolduskorraga seotud töö kirjeid jaotistes **Kõik hooldusgraafikud** ja **Avatud hooldusgraafiku read**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="00ca3-109">Hoolduskordi saab seadistada ka töö asukohtadele, kus need tuleb teostada töö asukohta hoolduskorrapõhise töökäsu loomise hetkel paigaldatud varadele.</span><span class="sxs-lookup"><span data-stu-id="00ca3-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="00ca3-110">Lisainfo saamiseks hooldusraundide seadistamiseks töö asukohtadele vt [Töö asukohtade loomine](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="00ca3-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="00ca3-111">Hoolduskorra seadistamine</span><span class="sxs-lookup"><span data-stu-id="00ca3-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="00ca3-112">Klõpsake suvandil **Varahaldus** > **Seadistus** > **Ennetav hooldus** > **Hoolduskorrad**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="00ca3-113">Uue hoolduskorra loomiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="00ca3-114">Sisestage ID väljale **Hoolduskord** ja hoolduskorra nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="00ca3-115">Valige hoolduskorra jaoks alguskuupäev väljal **Alguskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="00ca3-116">Väljadele **Päevi lõpetamiseks** ja **Tunde lõpetamiseks** võite sisestada oodatava lõppkuupäeva päevade ja tundidena.</span><span class="sxs-lookup"><span data-stu-id="00ca3-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="00ca3-117">Oodatav lõppkuupäev arvutatakse vastavalt alguskuupäevale, mis arvutatakse välja hoolduskava ridade loomisel.</span><span class="sxs-lookup"><span data-stu-id="00ca3-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="00ca3-118">Näiteks võite sisestada väljale **Päevi lõpetamiseks** numbri "7" näitamaks, et seotud töö tuleks lõpetada nädala jooksul alates alguskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="00ca3-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="00ca3-119">Valige tumblernupule **Automaatloomine** väärus "Jah", kui töökäsud tuleks sellest hoolduskorrast loodud hoolduskava ridadest automaatselt luua.</span><span class="sxs-lookup"><span data-stu-id="00ca3-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="00ca3-120">Valige väljal **Töökäsu tüüp** sellest hoolduskorrast loodud töökäskudele töökäsu tüüp.</span><span class="sxs-lookup"><span data-stu-id="00ca3-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="00ca3-121">Valige väljal **Teenindustase** sellest hoolduskorrast loodud töökäskudele töökäsu teenindustase.</span><span class="sxs-lookup"><span data-stu-id="00ca3-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="00ca3-122">Klõpsake kiirkaardi **Vara read** jaotisel **Lisa**, et lisada hoolduskorrale vara.</span><span class="sxs-lookup"><span data-stu-id="00ca3-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="00ca3-123">Reanumber sisestatakse väljale **Reanumber** automaatselt, et näidata hoolduskorra varade järjestust.</span><span class="sxs-lookup"><span data-stu-id="00ca3-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="00ca3-124">Valige vara väljal **Vara**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="00ca3-125">Valige väljal **Hooldustöö tüüp** varale hooldustöö tüüp.</span><span class="sxs-lookup"><span data-stu-id="00ca3-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="00ca3-126">Valige vajadusel hooldustöö tüübiga seotud **Hooldustöö  tüübi variant** ja **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="00ca3-127">Valige väljal **Perioodi tüüp** korduvus (päev, nädal, jne).</span><span class="sxs-lookup"><span data-stu-id="00ca3-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="00ca3-128">Väljale **Perioodi sagedus** sisestage hoolduskorra korduste arv.</span><span class="sxs-lookup"><span data-stu-id="00ca3-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="00ca3-129">Näide: Kui olete valinud väljale **Perioodi tüüp** valiku "Päev" ja sisestate sellele väljale arvu "7", luuakse ennetava hoolduse ajastamisel kord nädalas uued hoolduskorra read.</span><span class="sxs-lookup"><span data-stu-id="00ca3-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="00ca3-130">Valige väljal **Alguskuupäev** hoolduskorras sisalduvale varale alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="00ca3-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="00ca3-131">See kuupäev võib hoolduskorrale seadistatud alguskuupäevast erineda.</span><span class="sxs-lookup"><span data-stu-id="00ca3-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="00ca3-132">Kui soovite hoolduskorrale veel varasid lisada, korrake etappe 9-16.</span><span class="sxs-lookup"><span data-stu-id="00ca3-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="00ca3-133">Klõpsake kiirkaardil **Töö asukoha read** hoolduskorrale töö asukohta lisamiseks valikut **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="00ca3-134">Vaadake eespoolt seotud väljade kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="00ca3-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="00ca3-135">Saadaval on samad väljad, mis ka vara rea loomisel, aga saate vajadusel töö asukohale valida ka **Tootja** ja **Mudeli**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="00ca3-136">Kui valite reale ainult töö asukoha aga ei tee valikuid **Vara tüüp**, **Tootja**, **Mudel**, **Hooldustöö tüüp**, **Hooldustöö  tüübi variant** ja **Vahetus**, kaasatakse hoolduskorda kõik selle töö asukohaga hoolduse ajastamise hetkel seotud töö asukohad.</span><span class="sxs-lookup"><span data-stu-id="00ca3-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="00ca3-137">Klõpsake kiirkaardil **Kogumid** hoolduskorda kaasatava töökäsu kogumi valimiseks suvandit **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="00ca3-138">Ühe hoolduskorraga saab ühendada mitu töökäsu kogumit.</span><span class="sxs-lookup"><span data-stu-id="00ca3-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="00ca3-139">Salvestage oma seadistus.</span><span class="sxs-lookup"><span data-stu-id="00ca3-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="00ca3-140">Väljad **Varad** ja **Read**, mis asuvad rühmas **Üksikasjad** kiirkaardil **Päis** näitavad valitud hoolduskorraga seotud varade ja ridade koguarvu.</span><span class="sxs-lookup"><span data-stu-id="00ca3-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="00ca3-141">Alloleval joonisel on kujutatud kolme vara hõlmava hoolduskorra näide.</span><span class="sxs-lookup"><span data-stu-id="00ca3-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![Joonis 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="00ca3-143">Hoolduskordade plaanimine</span><span class="sxs-lookup"><span data-stu-id="00ca3-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="00ca3-144">Kui olete hoolduskorra seadistanud, käivitate ajastamise töö, et ajastada kõik hoolduskorraga seotud tööd.</span><span class="sxs-lookup"><span data-stu-id="00ca3-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="00ca3-145">Klõpsake **Varahaldus** > **Perioodiline** > **Ennetav hooldus** > **Hoolduskordade ajastamine** või **Varahaldus** > **Üldine** > **Hooldusgraafik** > **Kõik hooldusgraafikud** või **Ava hooldusgraafiku read** või **Ava hooldusgraafiku kogumid** > valige loendist hooldusgraafiku rida > nupp **Hoolduskorrad**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="00ca3-146">Valige väljal **Periood** ajastamise tööks kasutatav perioodi tüüp.</span><span class="sxs-lookup"><span data-stu-id="00ca3-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="00ca3-147">Väljale **Perioodi sagedus** sisestage ajastamise töös sisalduv perioodide arv.</span><span class="sxs-lookup"><span data-stu-id="00ca3-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="00ca3-148">Ajastamise alguseks on praegune kuupäev.</span><span class="sxs-lookup"><span data-stu-id="00ca3-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="00ca3-149">Valige tumblernupule **Automaatloomine** väärus "Jah", kui selle hoolduskorra põhjal tuleks automaatselt luua töökäsk.</span><span class="sxs-lookup"><span data-stu-id="00ca3-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="00ca3-150">Kui tumblernupp on seatud väärtusele "Jah" ja tumblernupp **Automaatloomine** on samuti vormi **Hoolduskorrad** hoolduskorral seatud väärtusele "Jah", luuakse töökäsud hoolduskorra ridade põhjal ja luuakse ka hooldusgraafiku read olekuga "Töökäsk loodud".</span><span class="sxs-lookup"><span data-stu-id="00ca3-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="00ca3-151">Kui ainult üks tumblernuppudest **Automaatloomine** on seadistatud väärtusele "Jah" kas selles ripploendis või jaotises **Hoolduskorrad**, luuakse hooldusgraafiku read ainult olekuga "Loodud".</span><span class="sxs-lookup"><span data-stu-id="00ca3-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="00ca3-152">Sellisel juhul töökäske ei looda.</span><span class="sxs-lookup"><span data-stu-id="00ca3-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="00ca3-153">Vajaduse korral saate ajastamise tööle valida konkreetsed hoolduskorrad või teise alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="00ca3-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="00ca3-154">Klõpsake suvandil **Filter** ja lisage hoolduskorrad.</span><span class="sxs-lookup"><span data-stu-id="00ca3-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="00ca3-155">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-155">Click **OK**.</span></span>

7. <span data-ttu-id="00ca3-156">Nüüd saate hoolduskordade töid näha jaotises **Varahaldus** > **Üldine** > **Hooldusgraafik** > **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="00ca3-157">Kui ajastatud hoolduskorrad on ühendatud töökäskude kogumiga, näete hooldusgraafiku ridu ka jaotises **Avatud hooldusgraafiku kogumid**.</span><span class="sxs-lookup"><span data-stu-id="00ca3-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="00ca3-158">Hoolduskorrast loodud hooldusgraafiku ridadel on viitetüüp "Hoolduskorrad".</span><span class="sxs-lookup"><span data-stu-id="00ca3-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="00ca3-159">Kahel alloleval joonisel on kujutatud ajastamise töö dialoogis **Hoolduskordade plaanimine** ja hooldusgraafiku read, mis on loodud jaotises **Kõik hooldusgraafikud** selle ajastamise töö põhjal.</span><span class="sxs-lookup"><span data-stu-id="00ca3-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![Joonis 2](media/14-preventive-maintenance.png)

![Joonis 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="00ca3-162">Kui tarnija garantii alla käivatele varadele tehakse töökäsud käsitsi, kuvatakse dialoogikasti, et teavitada kasutajat garantiist.</span><span class="sxs-lookup"><span data-stu-id="00ca3-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="00ca3-163">Siis saab töökäsu loomise tühistada.</span><span class="sxs-lookup"><span data-stu-id="00ca3-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="00ca3-164">Automaatselt loodud töökäskudel on garantii seose kontrollimine välja jäetud.</span><span class="sxs-lookup"><span data-stu-id="00ca3-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="00ca3-165">Kiirkaardil **Taustal käitamine** saate seadistada pakett-töö regulaarsete intervallidega hoolduskordade ajastamiseks.</span><span class="sxs-lookup"><span data-stu-id="00ca3-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="00ca3-166">Kui hoolduskord sisaldub mitmes töökäsu kogumis (vt [Töökäskude kogumid](../work-orders/work-order-pools.md)), kuvatakse ühte kirjet igas jaotise **Avatud hooldusgraafiku kogumid** kogumis.</span><span class="sxs-lookup"><span data-stu-id="00ca3-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="00ca3-167">Seda tehakse töökäsu kogumite filtreerimisvalikute optimeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="00ca3-167">This is done to optimize the filtering options for work order pools.</span></span>

