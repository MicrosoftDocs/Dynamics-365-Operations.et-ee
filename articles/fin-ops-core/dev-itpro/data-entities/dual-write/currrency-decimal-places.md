---
title: Valuuta andmetüübi migreerimine topeltkirjutamise jaoks
description: Selles teemas kirjeldatakse, kuidas muuta kümnendkohtade arvu, mida topeltkirjutamine valuuta puhul toetab.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 78820ff49958fc3b474038c0fcd126bcf6886d0d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560819"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="49ab2-103">Valuuta andmetüübi migreerimine topeltkirjutamise jaoks</span><span class="sxs-lookup"><span data-stu-id="49ab2-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="49ab2-104">Saate suurendada valuutaväärtuste puhul toetatavate kümnendkohtade arvu kuni kümneni.</span><span class="sxs-lookup"><span data-stu-id="49ab2-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="49ab2-105">Vaikepiirang on neli kümnendkohta.</span><span class="sxs-lookup"><span data-stu-id="49ab2-105">The default limit is four decimal places.</span></span> <span data-ttu-id="49ab2-106">Kümnendkohtade arvu suurendades aitate vältida andmekadu siis, kui kasutate andmete sünkroonimiseks topeltkirjutamist.</span><span class="sxs-lookup"><span data-stu-id="49ab2-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="49ab2-107">Kümnendkohtade arvu suurendamine on valikuline muudatus.</span><span class="sxs-lookup"><span data-stu-id="49ab2-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="49ab2-108">Selle rakendamiseks peate paluma Microsoftilt abi.</span><span class="sxs-lookup"><span data-stu-id="49ab2-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="49ab2-109">Kümnendkohtade arvu muutmise protsessil on kaks sammu.</span><span class="sxs-lookup"><span data-stu-id="49ab2-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="49ab2-110">Taotlege Microsoftilt migreerimist.</span><span class="sxs-lookup"><span data-stu-id="49ab2-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="49ab2-111">Muutke kümnendkohtade arv teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="49ab2-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="49ab2-112">Rakendus Finance and Operations ja teenus Dataverse peavad toetama valuutaväärtuste puhul sama kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="49ab2-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="49ab2-113">Vastasel juhul võib esineda andmekadu, kui seda teavet sünkroonitakse rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="49ab2-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="49ab2-114">Migreerimisprotsess muudab viisi, kuidas valuuta- ja vahetuskursiväärtuseid talletatakse, kuid mitte andmeid.</span><span class="sxs-lookup"><span data-stu-id="49ab2-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="49ab2-115">Pärast migreerimise lõpule viimist saab valuutakoodide ja hinnakujunduse kümnendkohtade arvu suurendada ning andmed, mida kasutajad sisestavad ja vaatavad, võivad hõlmata täpsemaid kümnendkohti.</span><span class="sxs-lookup"><span data-stu-id="49ab2-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="49ab2-116">Migreerimine on valikuline.</span><span class="sxs-lookup"><span data-stu-id="49ab2-116">Migration is optional.</span></span> <span data-ttu-id="49ab2-117">Kui rohkemate kümnendkohtade tugi võib teile kasuks tulla, soovitame teil migreerimist kaaluda.</span><span class="sxs-lookup"><span data-stu-id="49ab2-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="49ab2-118">Organisatsioonid, millel pole vaja rohkem kui nelja kümnendkohaga väärtuseid, ei pea migreerima.</span><span class="sxs-lookup"><span data-stu-id="49ab2-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="49ab2-119">Microsoftilt migreerimise taotlemine</span><span class="sxs-lookup"><span data-stu-id="49ab2-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="49ab2-120">Olemasolevate valuutaveergude talletamise puhul teenuses Dataverse ei toetata rohkem kui nelja kümnendkohta.</span><span class="sxs-lookup"><span data-stu-id="49ab2-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="49ab2-121">Seetõttu kopeeritakse valuutaväärtused migreerimise käigus andmebaasi uutele sisemistele veergudele.</span><span class="sxs-lookup"><span data-stu-id="49ab2-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="49ab2-122">See protsess jätkub, kuni kõik andmed on migreeritud.</span><span class="sxs-lookup"><span data-stu-id="49ab2-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="49ab2-123">Migreerimise lõpus asendatakse vanad talletustüübid sisemiselt uute talletustüüpidega, kuid andmeväärtused ei muutu.</span><span class="sxs-lookup"><span data-stu-id="49ab2-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="49ab2-124">Valuutaveerud toetavad seejärel kuni kümmet kümnendkohta.</span><span class="sxs-lookup"><span data-stu-id="49ab2-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="49ab2-125">Migreerimise käigus saab jätkata teenuse Dataverse kasutamist häirimatult.</span><span class="sxs-lookup"><span data-stu-id="49ab2-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="49ab2-126">Samal ajal muudetakse vahetuskursse nii, et need toetaks kuni 12 kümnendkohta praeguse kümnese piirangu asemel.</span><span class="sxs-lookup"><span data-stu-id="49ab2-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="49ab2-127">See muudatus on vajalik selleks, et kümnendkohtade arv oleks sama nii rakenduses Finance and Operations kui ka teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="49ab2-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="49ab2-128">Migreerimine ei muuda andmeid.</span><span class="sxs-lookup"><span data-stu-id="49ab2-128">Migration doesn't change any data.</span></span> <span data-ttu-id="49ab2-129">Pärast valuuta- ja vahetuskursivveergude teisendamist saavad administraatorid seadistada süsteemi kasutama valuutaveergude puhul kuni kümmet kümnendkohta, määrates kümnendkohtade arvu iga kande valuuta ning hinnakujunduse jaoks.</span><span class="sxs-lookup"><span data-stu-id="49ab2-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="49ab2-130">Migreerimise taotlemine</span><span class="sxs-lookup"><span data-stu-id="49ab2-130">Request a migration</span></span>

<span data-ttu-id="49ab2-131">Selle funktsiooni kättesaadavaks tegemiseks saatke e-kiri aadressile **CDSExpandDecimal@microsoft.com** ja lisage sellele järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="49ab2-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="49ab2-132">**Teema:** taotlus laiendatud kümnendkohtade toe lubamiseks organisatsiooni \<organizationID\> puhul</span><span class="sxs-lookup"><span data-stu-id="49ab2-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="49ab2-133">**Sisu:** soovin, et minu organisatsiooni \<organizationID\> puhul lubataks laiendatud kümnendkohtade tugi.</span><span class="sxs-lookup"><span data-stu-id="49ab2-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="49ab2-134">Microsofti esindaja võtab teiega järgmisteks sammudeks ühendust kahe kuni kolme tööpäeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="49ab2-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="49ab2-135">Kui taotlete migreerimist, peaksite teadma järgmiseid üksikasju ja neid arvesse võtma.</span><span class="sxs-lookup"><span data-stu-id="49ab2-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="49ab2-136">Andmete migreerimiseks kuluv aeg sõltub süsteemis olevate andmete hulgast.</span><span class="sxs-lookup"><span data-stu-id="49ab2-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="49ab2-137">Suurte andmebaaside migreerimine võib kesta mitu päeva.</span><span class="sxs-lookup"><span data-stu-id="49ab2-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="49ab2-138">Andmebaasi maht suureneb migreerimise ajal ajutiselt, kuna indeksite jaoks on vaja täiendavat ruumi.</span><span class="sxs-lookup"><span data-stu-id="49ab2-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="49ab2-139">Pärast migreerimise lõpule viimist vabaneb suurem osa täiendavast ruumist.</span><span class="sxs-lookup"><span data-stu-id="49ab2-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="49ab2-140">Kui migreerimise käigus ilmnevad tõrked, mis takistavad migreerimise lõpule viimist, saadab süsteem Microsofti tugiteenusele teate, et tugiteenuse töötajad saaksid sekkuda.</span><span class="sxs-lookup"><span data-stu-id="49ab2-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="49ab2-141">Isegi kui migreerimise ajal ilmnevad tõrked, on teenus Dataverse täielikult tavapäraseks kasutamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="49ab2-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="49ab2-142">Migreerimisprotsess on pöördumatu.</span><span class="sxs-lookup"><span data-stu-id="49ab2-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="49ab2-143">Kümnendkohtade arvu muutmine</span><span class="sxs-lookup"><span data-stu-id="49ab2-143">Changing the number of decimal places</span></span>

<span data-ttu-id="49ab2-144">Kui migreerimine on lõpule viidud, saab teenus Dataverse talletada numbreid, millel on rohkem kümnendkohti.</span><span class="sxs-lookup"><span data-stu-id="49ab2-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="49ab2-145">Administraatorid saavad valida mitut kümnendkohta kasutatakse kindlate valuutakoodide ja hinnakujunduse puhul.</span><span class="sxs-lookup"><span data-stu-id="49ab2-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="49ab2-146">Microsoft Power Appsi, Power BI ja Power Automate'i kasutajad saavad seejärel vaadata ja kasutada numbreid, millel on rohkem kümnendkohti.</span><span class="sxs-lookup"><span data-stu-id="49ab2-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="49ab2-147">Selle muudatuse tegemiseks peate värskendama Power Appsis järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="49ab2-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="49ab2-148">**Süsteemisätted: valuuta täpsus hinnakujunduse puhul** – veerg **Määra valuuta täpsus, mida kasutatakse hinnakujunduse jaoks terves süsteemis** määratleb, kuidas valuuta organisatsiooni puhul käitub, kui valitud on **Hinnakujunduse täpsus**.</span><span class="sxs-lookup"><span data-stu-id="49ab2-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="49ab2-149">**Ärihaldus: valuutad** – veerg **Valuuta täpsus** võimaldab teil määrata kindla valuuta jaoks kohandatud kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="49ab2-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="49ab2-150">Tervet organisatsiooni hõlmav säte pole ideaalne.</span><span class="sxs-lookup"><span data-stu-id="49ab2-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="49ab2-151">Sellel on mõned piirangud.</span><span class="sxs-lookup"><span data-stu-id="49ab2-151">There are some limitations:</span></span>

+ <span data-ttu-id="49ab2-152">Te ei saa tabelis valuutaveergu konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="49ab2-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="49ab2-153">Saate määrata rohkem kui neli kümnendkohta ainult **Hinnakujunduse** ja **Kande valuuta** tasemetes.</span><span class="sxs-lookup"><span data-stu-id="49ab2-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="49ab2-154">Süsteemisätted: valuuta täpsus hinnakujunduse puhul</span><span class="sxs-lookup"><span data-stu-id="49ab2-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="49ab2-155">Pärast migreerimise lõpule viimist saavad administraatorid määrata valuuta täpsuse.</span><span class="sxs-lookup"><span data-stu-id="49ab2-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="49ab2-156">Avage **Sätted \> Haldus** ja valige **Süsteemisätted**.</span><span class="sxs-lookup"><span data-stu-id="49ab2-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="49ab2-157">Seejärel muutke vahekaardil **Üldine** veergu **Määra valuuta täpsus, mida kasutatakse hinnakujunduse jaoks terves süsteemis** väärtust, nagu on näidatud järgmisel illustratsioonil.</span><span class="sxs-lookup"><span data-stu-id="49ab2-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![Valuuta süsteemisätted](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="49ab2-159">Ärihaldus: valuutad</span><span class="sxs-lookup"><span data-stu-id="49ab2-159">Business Management: Currencies</span></span>

<span data-ttu-id="49ab2-160">Kui teil on vaja, et konkreetse valuuta täpsus erineks hinnakujunduses kasutatavast valuuta täpsusest, saate seda muuta.</span><span class="sxs-lookup"><span data-stu-id="49ab2-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="49ab2-161">Avage **Sätted \> Ärihaldus**, valige **Valuutad** ja seejärel valuuta, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="49ab2-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="49ab2-162">Seejärel seadke veeru **Valuuta täpsus** väärtuseks soovitud kümnendkohtade arv, nagu on näidatud järgmisel illustratsioonil.</span><span class="sxs-lookup"><span data-stu-id="49ab2-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Konkreetse lokaadi valuutasätted](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="49ab2-164">tabelid: valuutaveerg</span><span class="sxs-lookup"><span data-stu-id="49ab2-164">tables: Currency column</span></span>

<span data-ttu-id="49ab2-165">Kindlate valuutaveergude jaoks konfigureeritav maksimaalne kümnendkohtade arv on neli.</span><span class="sxs-lookup"><span data-stu-id="49ab2-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]