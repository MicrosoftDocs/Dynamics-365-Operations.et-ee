---
title: Kõnekeskuse pettuseteatiste seadistamine ja kasutamine
description: Selles teemas kirjeldatakse, kuidas seadistada reegleid, et tellimuste töötlemise käigus teavitada klienditeeninduse esindajaid potentsiaalsetest valeandmetest. Saate määratleda spetsiaalsed koodid, mida kasutatakse kahtlaste tellimust automaatselt või manuaalselt ootele panekuks.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b4ee6b128e473d0999885f1cb1b4dbb015026c4e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022277"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a><span data-ttu-id="04d07-104">Kõnekeskuse pettuseteatiste seadistamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="04d07-104">Set up and work with call center fraud alerts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="04d07-105">Selles teemas selgitatakse, kuidas seadistada kriteeriume ja reegleid, et panna potentsiaalselt petturlikud müügitellimused täiendavaks ülevaatamiseks ootele.</span><span class="sxs-lookup"><span data-stu-id="04d07-105">This topic explains how to set up criteria and rules to put potentially fraudulent sales orders on hold for further review.</span></span> <span data-ttu-id="04d07-106">Pettuse kontrolli funktsioon võimaldab kontrollida müügitellimuse teabe kehtivust.</span><span class="sxs-lookup"><span data-stu-id="04d07-106">The fraud check feature is used to determine the validity of the information in a sales order.</span></span> <span data-ttu-id="04d07-107">Kui müügitellimuse teave tundub organisatsiooni petturliku tegevuse kriteeriumite ja reeglite alusel kahtlane, võidakse tellimus täiendavaks ülevaatamiseks ootele panna.</span><span class="sxs-lookup"><span data-stu-id="04d07-107">If the information in the sales order appears to be questionable, based on an organization's fraud criteria and rules, the order can be put on hold for further review.</span></span> <span data-ttu-id="04d07-108">Sel juhul ei saa tellimust lattu täiendavaks töötlemiseks edastada enne, kui ootelolek on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="04d07-108">In this case, the order can't be released to the warehouse for further processing until the hold has been cleared.</span></span>

> [!NOTE]
> <span data-ttu-id="04d07-109">Seda funktsiooni saab kasutada ainult Commerce’i kõnekeskuse kanali müügitellimuse töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="04d07-109">This feature can be used only with sales order processing for the Commerce call center channel.</span></span>

## <a name="turning-on-the-fraud-check-feature"></a><span data-ttu-id="04d07-110">Pettuse kontrolli funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="04d07-110">Turning on the fraud check feature</span></span>

<span data-ttu-id="04d07-111">Pettuse kontrolli funktsiooni kasutamiseks peate määrama kanali suvandi **Tellimuse lõpetamise lubamine** olekuks **Jah**, kui kõnekeskuse kanal on [määratletud](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options).</span><span class="sxs-lookup"><span data-stu-id="04d07-111">To use the fraud check feature, you must set the **Enable order completion** option on the channel to **Yes** when the call center channel is [defined](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options).</span></span> <span data-ttu-id="04d07-112">Kui tellimuse lõpetamine on sisse lülitatud, peavad kõnekeskuse kasutajad kõigi loodud müügitellimuste jaoks müügitellimuse lehel valima suvandi **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="04d07-112">When order completion is turned on, call center users must select **Complete** on the sales order page for all sales orders that are created.</span></span> <span data-ttu-id="04d07-113">Tegevus Lõpule viidud toob kaasa lehe **Müügitellimuse kokkuvõte** avanemise.</span><span class="sxs-lookup"><span data-stu-id="04d07-113">The Complete action causes the **Sales order summary** page to open.</span></span> <span data-ttu-id="04d07-114">Kui kasutajad on lehel **Müügitellimuse kokkuvõte** sisestanud vajalikud makseandmed, peavad nad tellimuse lõpuleviimiseks klõpsama käsku **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="04d07-114">After users enter the required payment data on the **Sales order summary** page, they select **Submit** to finalize the order.</span></span> <span data-ttu-id="04d07-115">Tellimuse esitamisel käivitatakse pettuse kontrolli funktsioon ja süsteemis olevad aktiivsed reeglid kinnitatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="04d07-115">When the order is submitted, the fraud check feature is triggered, and any rules that are active in the system are automatically validated.</span></span>

<span data-ttu-id="04d07-116">Kõnekeskuse kasutajad saavad ka käsitsi müügitellimuse pettuse tõttu ülevaatamise jaoks ootele panna, enne kui nad klõpsavad käsku **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="04d07-116">Call center users can also manually put sales orders on hold for fraud review before they select **Submit**.</span></span> <span data-ttu-id="04d07-117">Müügitellimuse käsitsi ootele panemiseks valige lehel **Müügitellimuse kokkuvõte** suvand **Pane ootele** \> **Pettuse tõttu käsitsi ootele panemine**.</span><span class="sxs-lookup"><span data-stu-id="04d07-117">To manually put a sales order on hold, on the **Sales order summary** page, select **Hold** \> **Manual fraud hold**.</span></span> <span data-ttu-id="04d07-118">Seejärel palutakse teil sisestada kommentaar tellimuse ootelepaneku põhjuse selgitamiseks.</span><span class="sxs-lookup"><span data-stu-id="04d07-118">You're then prompted to enter a comment to explain your reason for putting the order on hold.</span></span> <span data-ttu-id="04d07-119">See kommentaar kuvatakse töölaual [ootel tellimused](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), et anda konteksti ootel olevaid tellimusi ülevaatavale kasutajale, et ta saaks otsustada, kas tellimus tuleks väljastada.</span><span class="sxs-lookup"><span data-stu-id="04d07-119">This comment will appear in the [order holds](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) workbench to provide context to the user who reviews orders that are on hold to determine whether the order should be released.</span></span>

<span data-ttu-id="04d07-120">Lisaks kanalil suvandi **Tellimuse lõpetamise lubamine** konfigureerimisele peate kõnekeskuse parameetrites konfigureerima ka pettuse kontrolli funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="04d07-120">In addition to configuring the **Enable order completion** option on the channel, you must configure the fraud check feature in the Call center parameters.</span></span> <span data-ttu-id="04d07-121">Avage **Jaemüük ja kaubandus** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Kõnekeskuse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="04d07-121">Go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Call center parameters**.</span></span> <span data-ttu-id="04d07-122">Lehel **Kõnekeskuse parameetrid** määrake vahekaardil **Ootel** suvandi **Pettuse kontroll** olekuks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="04d07-122">On the **Call center parameters** page, on the **Holds** tab, set the **Fraud check** option to **Yes**.</span></span>

<span data-ttu-id="04d07-123">Vahekaardil **Ootel** peaksite määratlema ka [ooteloleku koodid](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds), mis rakendatakse tellimusele, mis on kas käsitsi või automaatselt pettuse tõttu ülevaatamise jaoks ootele pandud.</span><span class="sxs-lookup"><span data-stu-id="04d07-123">On the **Holds** tab, you should also define the [hold codes](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) that will be applied to an order that is either manually or automatically put on hold for fraud review.</span></span> <span data-ttu-id="04d07-124">Määrake ooteloleku koodid väljadel **Pettusest tuleneva ooteloleku kood** ja **Pettusest tuleneva ooteloleku kood**.</span><span class="sxs-lookup"><span data-stu-id="04d07-124">Set the hold codes in the **Manual fraud hold code** and **Fraud hold code** fields.</span></span> <span data-ttu-id="04d07-125">Kasulik võib olla kahe kordumatu ooteloleku koodi loomine, nii et kasutajad, kes töötavad ooteloleku töölaual, saaksid hõlpsalt filtreerida ja eristada automaatseid ja käsitsi ootele pandud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="04d07-125">You might find it helpful to create two unique hold codes, so that users who work in the holds workbench can easily filter and distinguish automatic holds from manual holds.</span></span>

<span data-ttu-id="04d07-126">Et pettuse kontrolli funktsiooni töötaks tõhusalt, peate määrama ka välja **Miinimumskoor**.</span><span class="sxs-lookup"><span data-stu-id="04d07-126">For the fraud check feature to work effectively, you must also set the **Minimum score** field.</span></span> <span data-ttu-id="04d07-127">Igal pettuse kriteeriumil ja reeglil, mis on süsteemis määratletud, on skoor.</span><span class="sxs-lookup"><span data-stu-id="04d07-127">Every fraud criterion and rule that is defined in the system has a score.</span></span> <span data-ttu-id="04d07-128">Kui müügitellimust kontrollitakse pettuse vastete suhtes, siis ühe või mitme vaste leidmisel liidetakse skoorid kokku, et esitada pettuse koguskoor.</span><span class="sxs-lookup"><span data-stu-id="04d07-128">When a sales order is checked for fraud matches, if one or more matches are found, the scores are added together to give the order a total fraud score.</span></span> <span data-ttu-id="04d07-129">Kui pettuse koguskoor ületab välja **Miinimumskoor** väärtust, pannakse tellimus automaatselt ootele.</span><span class="sxs-lookup"><span data-stu-id="04d07-129">If the total fraud score for an order exceeds the value of the **Minimum score** field, the order is automatically put on hold.</span></span> <span data-ttu-id="04d07-130">Soovi korral saate vahekaardil **Ootel** kasutada teisi skooriga seotud välju, et määratleda meiliaadressi skoor, telefoninumbri skoor, sihtnumbri skoor ja laiendatud sihtnumbri skoor.</span><span class="sxs-lookup"><span data-stu-id="04d07-130">You can optionally use the other score-related fields on the **Holds** tab to define the email score, phone score, ZIP/postal code score, and extended ZIP/postal code score.</span></span> <span data-ttu-id="04d07-131">Kui te ei määra ühelegi staatilise pettuse kriteeriumile skoori, kui määratlete neid lehel **Staatilised pettuse andmed**, annab süsteem neile skoorid, kasutades vaikeskoore, mille määrate vahekaardil **Ootel** lehel **Kõnekeskuse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="04d07-131">If you don't specify a score for any of these static fraud criteria when you define them on the **Static fraud data** page, the system will score them by using the default scores that you specify on the **Holds** tab of the **Call center parameters** page.</span></span>

<span data-ttu-id="04d07-132">Lõpetuseks kasutage välja **Pettuse kommentaar**, et määrada dokumendi tüüp, mida tuleb kasutada, kui kasutaja sisestab kommentaarid, kui ta paneb tellimuse pettuse tõttu ülevaatamise jaoks käsitsi ootele.</span><span class="sxs-lookup"><span data-stu-id="04d07-132">Finally, use the **Fraud comment type** field to specify the document type that should be used when users enter comments when they manually put an order on hold for fraud review.</span></span> <span data-ttu-id="04d07-133">Enamasti on selle välja väärtuseks **Märkus**.</span><span class="sxs-lookup"><span data-stu-id="04d07-133">Most often, this field is set to **Note**.</span></span>

## <a name="defining-fraud-criteria-and-rules"></a><span data-ttu-id="04d07-134">Pettuse kriteeriumide ja reeglite määratlemine</span><span class="sxs-lookup"><span data-stu-id="04d07-134">Defining fraud criteria and rules</span></span>

<span data-ttu-id="04d07-135">Süsteem järgib kaht tüüpi pettuse kriteeriume, et määratleda, kas tellimus tuleks pettuse tõttu ülevaatamise ootele panna.</span><span class="sxs-lookup"><span data-stu-id="04d07-135">The system references two types of fraud criteria to determine whether an order should be put on hold for fraud review:</span></span>

- <span data-ttu-id="04d07-136">**Staatilised pettuse andmed** kasutab kindlat väärtust, nt telefoninumber, mis on pandud blokeeritud numbrite loendisse, või e-posti aadress, mis on märgitud lipuga, sest seda on teadaolevalt varem kasutatud petturlike kannete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="04d07-136">**Static fraud data** uses a specific value, such as a phone number that has been put on a list of blocked numbers or an email address that has been flagged because it's known to have been used for previous fraudulent transactions.</span></span> <span data-ttu-id="04d07-137">Staatiliste pettuseandmete seadistamiseks avage **Jaemüük ja kaubandus** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Pettus** \> **Staatilised pettuse andmed**.</span><span class="sxs-lookup"><span data-stu-id="04d07-137">To set up static fraud data, go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Fraud** \> **Static fraud data**.</span></span> <span data-ttu-id="04d07-138">Lehel **Staatilised pettuse andmed** saate lisada pettuse kriteeriume käsitsi või andmeimpordi kaudu.</span><span class="sxs-lookup"><span data-stu-id="04d07-138">On the **Static fraud data** page, you can add fraud criteria manually or through data import.</span></span> <span data-ttu-id="04d07-139">Petturlikule teabele lisatakse skoorid.</span><span class="sxs-lookup"><span data-stu-id="04d07-139">Scores are attached to the fraudulent information.</span></span> <span data-ttu-id="04d07-140">Kui pettuse kontrolli funktsioon on sisse lülitatud, võrreldakse iga sisestatud müügitellimust staatiliste andmetega.</span><span class="sxs-lookup"><span data-stu-id="04d07-140">If the fraud check feature is turned on, every sales order that is entered is compared to the static data.</span></span> <span data-ttu-id="04d07-141">Kui andmed leitakse kas kliendi arveldusaadressist või tarneaadressist, mis on seotud tellimuse päisega, või kui andmed leitakse tarneaadressidest, mis on seotud selle müügitellimuse ridadega, liidetakse kõigi kordumatute vastete skoorid kokku ja võrreldakse väärtusega **Miinimumskoor**, et määrata kindlaks, kas tellimus tuleks ootele panna.</span><span class="sxs-lookup"><span data-stu-id="04d07-141">If the data is found in either the customer's billing address or the delivery address that is linked to the order header, or if the data is found in the delivery addresses that are linked to any of the lines on that sales order, the scores of all unique matches are added together and compared to the **Minimum score** value to determine whether the order should be put on hold.</span></span>
- <span data-ttu-id="04d07-142">**Pettuse reeglid** koosnevad kasutaja määratletud muutujatest ja tingimustest, mis on nende muutujate jaoks määratletud.</span><span class="sxs-lookup"><span data-stu-id="04d07-142">**Fraud rules** consist of user-defined variables and the conditions that are defined for those variables.</span></span> <span data-ttu-id="04d07-143">Reeglite loomiseks avage **Jaemüük ja kaubandus** \> **Kanali häälestus** \> **Kõnekeskuse seadistamine** \> **Pettus** \> **Reeglid**.</span><span class="sxs-lookup"><span data-stu-id="04d07-143">To create rules, go to **Retail and Commerce** \> **Channel setup** \> **Call center setup** \> **Fraud** \> **Rules**.</span></span> <span data-ttu-id="04d07-144">Pettuse reeglid võimaldavad ettevõttel konfigureerida keerukama reeglikomplekti, mis sisaldab avaldisi **AND** või **OR** mitme tingimuse hindamiseks.</span><span class="sxs-lookup"><span data-stu-id="04d07-144">Fraud rules let a company configure a more complex rule set that can include **AND** or **OR** statements to evaluate multiple conditions.</span></span> <span data-ttu-id="04d07-145">Näiteks, kasutaja soovib pettuse tõttu ülevaatamiseks panna kõik tellimused, mis on seotud klientidega, kes kuuluvad kindlasse kliendigruppi ja kes tellisid kindla toote.</span><span class="sxs-lookup"><span data-stu-id="04d07-145">For example, a user wants all orders for customers who belong to a specific customer group and who ordered a specific product to be put on hold for fraud review.</span></span> <span data-ttu-id="04d07-146">Sel juhul määratakse tingimused kliendi ja toodete kontrollimiseks lehel **Reeglid** ja kasutatakse tingimust AND.</span><span class="sxs-lookup"><span data-stu-id="04d07-146">In this case, conditions to validate the customer and products are defined on the **Rules** page, and an AND condition is used.</span></span> <span data-ttu-id="04d07-147">Tellimus pannakse sellisel juhul ootele ainult siis, kui mõlemad tingimused on täidetud ja kui reeglile määratud skoori väärtus, pluss teiste reeglite skoori väärtus, millele tellimus vastab, tõstab tellimuse pettuse koguskoori üle väärtuse **Minimaalne skoor**, mis on määratletud lehel **Kõnekeskuse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="04d07-147">An order is then put on hold only if both conditions are true, and if the score value that is assigned to this rule, plus the score value of any other rules that the order matches, causes the order's total fraud score to exceed the **Minimum score** value that is defined on the **Call center parameters** page.</span></span>

> [!NOTE]
> <span data-ttu-id="04d07-148">Mitme reegli või liiga keerukate reeglite kasutamine mõjutab süsteemi jõudlust müügitellimuste edastamisel.</span><span class="sxs-lookup"><span data-stu-id="04d07-148">Multiple rules or overly complex rules will affect system performance when sales orders are submitted.</span></span> <span data-ttu-id="04d07-149">Pettuse kontrolli funktsioon ei ole optimeeritud käsitlema suurt hulka staatiliste pettuse andmete kirjeid ja paljusid aktiivseid reegleid.</span><span class="sxs-lookup"><span data-stu-id="04d07-149">The fraud check feature hasn't been optimized to handle a large volume of static fraud data entries and many active rules.</span></span> <span data-ttu-id="04d07-150">Pidage meeles, et iga reeglit hinnatakse, kui kõnekeskuse kasutaja klõpsab müügitellimuse sisestamise ajal käsku **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="04d07-150">Remember that every rule is evaluated when call center users select **Submit** during sales order entry.</span></span> <span data-ttu-id="04d07-151">Reegleid võrreldakse müügitellimuse päise ja tellimuse kõigi ridadega.</span><span class="sxs-lookup"><span data-stu-id="04d07-151">The rules are evaluated against the sales order header and all order lines.</span></span> <span data-ttu-id="04d07-152">Mida rohkem on reegleid ja mida keerukamad on nende avaldised, seda rohkem kulub töötlemiseks aega.</span><span class="sxs-lookup"><span data-stu-id="04d07-152">The more rules there are and the more complex the rule statements are, the more time will be required for processing.</span></span> <span data-ttu-id="04d07-153">Kui tellimuses on palju rea kaupu ning palju aktiivseid reegleid ja staatilisi andmekirjeid, võib kõikide andmete ülevaatamise ja kontrollimise ning pettuse skoori arvutamise automaatne protsess jõudlust märkimisväärselt mõjutada.</span><span class="sxs-lookup"><span data-stu-id="04d07-153">If there are many line items on an order, and many active rules and static data entries, the automatic process of reviewing and validating all the data and calculating a fraud score can have a severe impact on performance.</span></span> <span data-ttu-id="04d07-154">Seda funktsiooni kasutavad organisatsioonid peavad enne reeglimuudatuste või staatiliste pettuse kriteeriumite muudatuste tootmiskeskkonnas juurutamist alati testima ja kinnitama, et tellimuste edastamisel töötlemisele kuluv aeg oleks aktsepteeritav.</span><span class="sxs-lookup"><span data-stu-id="04d07-154">Organizations that use this feature should always test and confirm that the processing time for order submission is acceptable before they apply any changes to rules or static fraud criteria to the production environment.</span></span>

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a><span data-ttu-id="04d07-155">Pettuse tõttu ülevaatamisel olevate tellimuste tuvastamine</span><span class="sxs-lookup"><span data-stu-id="04d07-155">Identifying orders that are on hold for fraud review</span></span>

<span data-ttu-id="04d07-156">Kui kõnekeskuse kasutajad esitavad müügitellimuse, siis kui tellimus vastab pettuse kriteeriumidele või reeglitele, ja kui skoor ületab miinimumi, saab kasutaja hoiatusteate, mis ütleb, et tellimus on pandud ootele.</span><span class="sxs-lookup"><span data-stu-id="04d07-156">When call center users submit a sales order, if the order matches the fraud criteria or rules, and if the score exceeds the minimum, the users receive a warning message that states that the order has been put on hold.</span></span> <span data-ttu-id="04d07-157">Kasutaja saab selle teate sulgeda, sest see on mõeldud ainult teavitamiseks.</span><span class="sxs-lookup"><span data-stu-id="04d07-157">Users can close this message, because it's for informational purposes only.</span></span> <span data-ttu-id="04d07-158">Kasutajad saavad soovi korral selle teabe edastada kliendile.</span><span class="sxs-lookup"><span data-stu-id="04d07-158">Users can optionally communicate this information to the customer.</span></span> <span data-ttu-id="04d07-159">Ettevõtte peab määrama protokolli, mida kasutajad sellisel juhul järgivad.</span><span class="sxs-lookup"><span data-stu-id="04d07-159">The business should determine the protocol that users follow in this situation.</span></span>

<span data-ttu-id="04d07-160">Tellimus on salvestatud, kuid sellele on märgitud lipp **Ära töötle**.</span><span class="sxs-lookup"><span data-stu-id="04d07-160">The order is saved, but the **Do not process** flag is set on it.</span></span> <span data-ttu-id="04d07-161">See lipp aitab tagada, et tellimust ei saa lattu väljastada.</span><span class="sxs-lookup"><span data-stu-id="04d07-161">This flag helps guarantee that the order can't be released to the warehouse.</span></span> <span data-ttu-id="04d07-162">Kasutajad saavad iga müügitellimuse korral lipu **Ära töötle** sätet lehel **Üksikasjalik olek** igal hetkel vaadata.</span><span class="sxs-lookup"><span data-stu-id="04d07-162">At any time, users can view the setting of the **Do not process** flag for any sales order on the **Detailed status** page.</span></span> <span data-ttu-id="04d07-163">Selle lehe saab avada lehtedel **Kõik müügitellimused** ja **Klienditeenindus**.</span><span class="sxs-lookup"><span data-stu-id="04d07-163">This page can be opened from the **All sales order** and **Customer service** pages.</span></span> <span data-ttu-id="04d07-164">Süsteem uuendab ka tellimuse välja **Üksikasjalik olek** väärtuseks **Pettusest tulenev ootelolek**.</span><span class="sxs-lookup"><span data-stu-id="04d07-164">The system also updates the value of the **Detailed status** field for the order to **Fraud hold**.</span></span>

<span data-ttu-id="04d07-165">Pettuse tõttu ülevaatamisel olevate tellimuste vaatamiseks ja haldamiseks avage **Jaemüük ja kaubandus** \> **Kliendid** \> **Ootel olevad tellimused**.</span><span class="sxs-lookup"><span data-stu-id="04d07-165">To view and manage the orders that are on hold for fraud review, go to **Retail and Commerce** \> **Customers** \> **Order holds**.</span></span> <span data-ttu-id="04d07-166">Lehel **Ootelolevad tellimused** valige loendist kirje ja klõpsake nuppu **Ootelolev tellimus**, et näha üksikasjalikumat vaadet, mis sisaldab teavet ooteloleku põhjuse kohta.</span><span class="sxs-lookup"><span data-stu-id="04d07-166">On the **Order holds** page, select an entry in the list, and then click **Order hold** to see a more detailed view that includes information about the reason for the hold.</span></span> <span data-ttu-id="04d07-167">Kiirkaardil **Pettuse üksikasjad** saate vaadata süstemaatilisi pettuse kriteeriume, mis leiti olevat tellimuse vasted ja millele rakendati skoorid.</span><span class="sxs-lookup"><span data-stu-id="04d07-167">On the **Fraud details** FastTab, you can view the systematic fraud criteria that were found to be a match for the order and the scores that were applied.</span></span> <span data-ttu-id="04d07-168">Kui tellimus pandi käsitsi ootele, saate vaadata üle tellimuse ootele pannud kasutaja kommentaarid vaadates jaotist **Pettusemärkmed** kiirkaardil **Märkused**.</span><span class="sxs-lookup"><span data-stu-id="04d07-168">If the order was put on manual hold, you can review any comments that were entered by the user who put the order on hold by looking at the **Fraud notes** section on the **Notes** FastTab.</span></span>

<span data-ttu-id="04d07-169">Lisateavet selle kohta, kuidas töötada ootel olevate tellimustega, vt teemast [Ootelolevad tellimused](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).</span><span class="sxs-lookup"><span data-stu-id="04d07-169">For more information about how to work with hold orders, see [Order holds](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).</span></span>