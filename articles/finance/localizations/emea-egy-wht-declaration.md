---
title: Kinnipeetava maksu deklaratsioon Egiptuse jaoks
description: Käesolev teema kirjeldab, kuidas konfigureerida ja luua Egiptuse kinnipeetava maksu deklaratsioone.
author: sndray
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 4e3d68ac003fabaa504ffe81b8bf2f7ff8d7538d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839788"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="1bca0-103">Kinnipeetava maksu deklaratsioon Egiptuse jaoks (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="1bca0-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="1bca0-104">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1bca0-104">Overview</span></span>
<span data-ttu-id="1bca0-105">See teema kirjeldab, kuidas seadistada ja luua kinnipeetava maksu deklaratsioone ning kinnipeetava maksu deklaratsiooni vorme 41 ja 11 Egiptuse juriidilistele isikutele</span><span class="sxs-lookup"><span data-stu-id="1bca0-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="1bca0-106">Kõik Egiptuse üksused peavad ette valmistama vormi 41, mis võtab kokku kõik maksud, mis on kinnipeetud kohalikelt hankijatelt ja tarnijatelt.</span><span class="sxs-lookup"><span data-stu-id="1bca0-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="1bca0-107">Lisaks vormile 41 tuleb luua vorm 11 kõigi välismaiselt pakkujatelt kinnipeetud maksu üksikasjade jaoks.</span><span class="sxs-lookup"><span data-stu-id="1bca0-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="1bca0-108">Kinnipeetava **Maksu deklaratsiooni** aruanne sisaldab järgmisi Dynamics 365 Finance aruandeid:</span><span class="sxs-lookup"><span data-stu-id="1bca0-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="1bca0-109">Deklaratsiooni vormi number.</span><span class="sxs-lookup"><span data-stu-id="1bca0-109">Declaration form No.</span></span> <span data-ttu-id="1bca0-110">41</span><span class="sxs-lookup"><span data-stu-id="1bca0-110">41</span></span>
- <span data-ttu-id="1bca0-111">Deklaratsiooni vormi number.</span><span class="sxs-lookup"><span data-stu-id="1bca0-111">Declaration form No.</span></span> <span data-ttu-id="1bca0-112">11</span><span class="sxs-lookup"><span data-stu-id="1bca0-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="1bca0-113">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="1bca0-113">Prerequisites</span></span>
<span data-ttu-id="1bca0-114">Juriidilise isiku peamine aadress peab olema Egiptuses.</span><span class="sxs-lookup"><span data-stu-id="1bca0-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="1bca0-115">Tööruumis **Funktsioonide haldus**, lülitage sisse järgmised funktsioonid:</span><span class="sxs-lookup"><span data-stu-id="1bca0-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="1bca0-116">**Globaalne kinnipeetav maks**</span><span class="sxs-lookup"><span data-stu-id="1bca0-116">**Global withholding tax**</span></span>

<span data-ttu-id="1bca0-117">Lisateavet funktsioonide lubamise kohta, vaata [Funktsioonihalduse ülevaade.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span><span class="sxs-lookup"><span data-stu-id="1bca0-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="1bca0-118">Avage **Maks** > **Seadistus** > **Parameetrid** > **Pearaamatu parameetrid** ja seejärel seadistage vahekaardil **Kinnipeetav maks** suvand **Luba globaalne kinnipeetav maks** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="1bca0-119">**Elektroonilise aruandluse** tööruumis importige hoidlast järgmised elektroonilise aruandluse vormingud:</span><span class="sxs-lookup"><span data-stu-id="1bca0-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="1bca0-120">WHT deklaratsioon Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="1bca0-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="1bca0-121">Ülaltoodud vorming põhineb **maksudeklaratsiooni mudelil** ja kasutab **maksudeklaratsiooni mudeli vastendamist**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="1bca0-122">See lisakonfiguratsioon imporditakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="1bca0-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="1bca0-123">Lisateavet selle kohta, kuidas importida elektroonilise aruandluse konfiguratsioone, vaata [Elektrooniliste aruannete konfiguratsioonide allalaadimine Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="1bca0-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="1bca0-124">Elektroonilise aruandluse konfiguratsioonide allalaadimine</span><span class="sxs-lookup"><span data-stu-id="1bca0-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="1bca0-125">Egiptuse deklaratsioonivormide rakendamine põhineb elektroonilise aruandluse (ER) konfiguratsioonil.</span><span class="sxs-lookup"><span data-stu-id="1bca0-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="1bca0-126">Lisateavet konfigureeritava aruandluse võimaluste ja mõistete kohta vaata [Eektroonilisest aruandlusest](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="1bca0-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="1bca0-127">Tootmise ja kasutaja aktsepteerimise testimiseks (UAT) keskkonnad järgige teema juhiseid, [Laadige alla elektroonilise aruandluse konfiguratsioonid Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="1bca0-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="1bca0-128">Kinnipeetavate deklaratsioonide loomiseks Egiptuse juriidilises isikus, peate üles laadima järgmised konfiguratsioonid:</span><span class="sxs-lookup"><span data-stu-id="1bca0-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="1bca0-129">Maksudeklaratsiooni model.version.82.xml või uuem versioon</span><span class="sxs-lookup"><span data-stu-id="1bca0-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="1bca0-130">Maksudeklaratsioon model.version.82.xml või uuem versioon</span><span class="sxs-lookup"><span data-stu-id="1bca0-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="1bca0-131">WHT deklaratsioon Excel (EG.version.82.21 või hilisem versioon)</span><span class="sxs-lookup"><span data-stu-id="1bca0-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="1bca0-132">Pärast ER-i konfiguratsioonide allalaadimist Lifecycle Services (LCS) või globaalsest hoidlast viige lõpule järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="1bca0-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="1bca0-133">Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="1bca0-134">Lehel **Konfiguratsioonid** valige tegevuspaanil **Vahetuskursi laadimine XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="1bca0-135">Laadige üles kõik failid eelmise täpi loendis toodud järjestuses.</span><span class="sxs-lookup"><span data-stu-id="1bca0-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="1bca0-136">Pärast kõigi konfiguratsioonide üles laadimist peaks konfiguratsioonipuu olema finantsis.</span><span class="sxs-lookup"><span data-stu-id="1bca0-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="1bca0-137">Seadistage rakenduspõhised parameetrid</span><span class="sxs-lookup"><span data-stu-id="1bca0-137">Set up application-specific parameters</span></span>

<span data-ttu-id="1bca0-138">Rakendusespetsiifiliste parameetrite valik võimaldab kasutajatel määrata kriteeriumid, kuidas maksukanded igal loodud aruande real klassifitseeritakse ja arvutatakse, sõltuvalt **kinnipeetava maksu kaubagrupi** konfiguratsioonist või muudest otsingu määratluse kriteeriumitest.</span><span class="sxs-lookup"><span data-stu-id="1bca0-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="1bca0-139">Kinnipeetava deklaratsiooni vorm 41 sisaldab konkreetset veergu, kus kinnipeetava maksu kanne tuleb klassifitseerida vastavalt maksuameti klassifikatsioonile nimega **Allahindluse koodi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="1bca0-140">Selle asemel, et lisada need uued klassifikatsioonid kannete sisestamisel uuteks sisestusandmeteks, määratakse klassifikatsioonid konfiguratsioonides tehtud erinevate otsingute alusel, mida on tutvustatud **Konfiguratsioonid** > **Seadistage rakendusomased parameetrid** > **Seaded** nii, et need vastaksid Egiptuse kinnipeetavate aruannet nõuetele.</span><span class="sxs-lookup"><span data-stu-id="1bca0-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="1bca0-141">Järgmist konfiguratsiooni kasutatakse kannete klassifitseerimiseks kinnipeetava deklaratsiooni vormis 41 aruandes:</span><span class="sxs-lookup"><span data-stu-id="1bca0-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="1bca0-142">**DiscountTaxTypeLookup** -> veerg nr 18</span><span class="sxs-lookup"><span data-stu-id="1bca0-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="1bca0-143">Viige lõpule järgmised sammud erinevate otsingute häälestamiseks, mida kasutatakse "Mis deklaratsioon ja seotud raamatute aruanded" loomiseks.</span><span class="sxs-lookup"><span data-stu-id="1bca0-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="1bca0-144">**Elektroonilise aruandluse** tööruumis valige **konfiguratsioonide** > **Häälestus**, et seadistada reeglid kannete klassifitseerimise tuvastamiseks Deklaratsiooni aruandes.</span><span class="sxs-lookup"><span data-stu-id="1bca0-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="1bca0-145">Valige praegune versioon ja valige **Otsingud** otsingunime kiirkaardil.</span><span class="sxs-lookup"><span data-stu-id="1bca0-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="1bca0-146">Näiteks **DiscountTaxTypeLookup**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="1bca0-147">See otsing tuvastab maksuhalduri nõutavate allahindlustüüpide loendi.</span><span class="sxs-lookup"><span data-stu-id="1bca0-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="1bca0-148">Suvandis **Tingimused** valige kiirkaardil klassifikatsiooni veerus **Lisa** ja uuel real **Otsingu tulemused** veerus valige klassifikatsiooniga **18** seotud rida.</span><span class="sxs-lookup"><span data-stu-id="1bca0-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="1bca0-149">Veerus **Kinnipeetava maksu kaubagrupp** valige seotud kood, mida kasutatakse klassifikatsiooni tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="1bca0-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="1bca0-150">Näiteks **Lubatud allahindlus**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="1bca0-151">Korrake samme 3 ja 4 kõigi saadaval otsingute puhul.</span><span class="sxs-lookup"><span data-stu-id="1bca0-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="1bca0-152">Lõppkirje rea kaasamiseks klõpsake uuesti nuppu **Lisa** ja valige **otsingutulemuse** veerus suvand **Pole rakendatav**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="1bca0-153">Ülejäänud veergudes valige **Mitte tühi**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="1bca0-154">Seadistage pearaamatu parameetrid</span><span class="sxs-lookup"><span data-stu-id="1bca0-154">Set up General ledger parameters</span></span>

<span data-ttu-id="1bca0-155">WHT deklaratsioonivormi aruannete loomiseks Microsoft Excel, määratlege ER formaat **pearaamatu parameetrite** lehel.</span><span class="sxs-lookup"><span data-stu-id="1bca0-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="1bca0-156">Minge **Maksu** > **Seadistamise** > **pearaamatu parameetritesse**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="1bca0-157">Vahekaardil **Kinnipeetav maks** väljal **WHT deklaratsiooni vormingu vastendamine** valige **WHT Deklaratsioon Excel (EG)**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="1bca0-158">Kui jätate selle välja tühjaks, luuakse standardne käibemaksuaruanne SSRS-vormingus.</span><span class="sxs-lookup"><span data-stu-id="1bca0-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![Deklaratsiooni vorm](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="1bca0-160">Kinnipeetava deklaratsiooni vormide loomine</span><span class="sxs-lookup"><span data-stu-id="1bca0-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="1bca0-161">Konkreetse perioodi kinnipeetava deklaratsiooni vormi ettevalmistamine ja esitamine põhineb kinnipeetava maksu kannetel, mis sisestati tasakaalustamise ja maksemaksu sisestamise ajal.</span><span class="sxs-lookup"><span data-stu-id="1bca0-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="1bca0-162">Lisateavet globaalse kinnipeetava maksu kohta vt [globaalsest kinnipeetavast maksust](../general-ledger/global-withholding-tax-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1bca0-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="1bca0-163">Maksudeklaratsiooni aruande loomiseks viige lõpule järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="1bca0-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="1bca0-164">Minge **Maksu** > **Deklaratsioonidesse** > **Kinnipeetav maks** > \**Kinnipeetava maksu makse*.</span><span class="sxs-lookup"><span data-stu-id="1bca0-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="1bca0-165">Valige tasakaalustusperiood ja seejärel valige aruande alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="1bca0-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="1bca0-166">Sisestage makse kuupäev ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="1bca0-167">Avanev dialoogiboksis valige üks või mitu vormitüüpi **Vorm No 41**, **Vorm Nr 11** või **Pole**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="1bca0-168">Kui valite **Pole**, luuakse standardaruanne.</span><span class="sxs-lookup"><span data-stu-id="1bca0-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="1bca0-169">Keele valimine.</span><span class="sxs-lookup"><span data-stu-id="1bca0-169">Select the language.</span></span> <span data-ttu-id="1bca0-170">Kõik aruanded tõlgitakse **en-us** ja **ar-eg**.</span><span class="sxs-lookup"><span data-stu-id="1bca0-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="1bca0-171">Sisestage selle panga haru ja nimi, kus maksumakse tasutakse.</span><span class="sxs-lookup"><span data-stu-id="1bca0-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="1bca0-172">Valige ettevõtte tüüp ning seejärel sisestage tšeki- ja dokumendinumbrid.</span><span class="sxs-lookup"><span data-stu-id="1bca0-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="1bca0-173">Vaadake üksuse tüüpi.</span><span class="sxs-lookup"><span data-stu-id="1bca0-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="1bca0-174">Sisestage vormi määramiseks registreeritud isiku nimi ja valige **OK** aruande loomise kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="1bca0-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
