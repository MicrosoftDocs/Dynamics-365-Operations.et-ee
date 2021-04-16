---
title: Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks
description: Selles teemas selgitatakse, kuidas saate käivitatud ER-vormingu andmeallikaid siluda, et mõista paremini konfigureeritud andmevoogu ja teisendust.
author: NickSelin
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: fe3e6a4223fc8b26e523a982a2e1752a34b370de
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753668"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="e3210-103">Käivitatud ER-vormingu andmeallikate silumine andmevoo ja teisenduse analüüsimiseks</span><span class="sxs-lookup"><span data-stu-id="e3210-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="e3210-104">Kui [konfigureerite](tasks/er-format-configuration-2016-11.md) elektroonilise aruandluse (ER) lahendust väljaminevate dokumentide loomise otstarbel, siis määratlete andmete rakendusest kätte saamiseks ja saadud väljundi sisestamiseks kasutatavad meetodid.</span><span class="sxs-lookup"><span data-stu-id="e3210-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="e3210-105">ER-lahenduse töötsükli toe tõhususe tagamiseks peaks teie lahendus sisaldama  [ER-andmemudelit](general-electronic-reporting.md#DataModelComponent) ja selle [vastendamise](general-electronic-reporting.md#ModelMappingComponent) komponente ning samuti [ER-vormingut](general-electronic-reporting.md#FormatComponentOutbound) ja selle vastendamise komponente, et tagada mudeli vastendamise rakenduspõhisus, samal ajal kui muud komponendid püsivad rakendusest sõltumatud.</span><span class="sxs-lookup"><span data-stu-id="e3210-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="e3210-106">Seetõttu võivad loodud väljundisse andmete sisestamise protsessi [mõjutada ](general-electronic-reporting.md#FormatComponentOutbound) mitmesugused ER-komponendid.</span><span class="sxs-lookup"><span data-stu-id="e3210-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="e3210-107">Vahel näevad loodud väljundi andmed välja teistsugused kui samad andmed rakenduse andmebaasis.</span><span class="sxs-lookup"><span data-stu-id="e3210-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="e3210-108">Sellisel juhul tuleks määratleda, milline ER-komponent vastutab andmeteisenduse eest.</span><span class="sxs-lookup"><span data-stu-id="e3210-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="e3210-109">ER-andmeallika silurifunktsioon vähendab märkimisväärselt selle uurimiseks kuluvat aega ja kulusid.</span><span class="sxs-lookup"><span data-stu-id="e3210-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="e3210-110">Saate katkestada ER-vormingu käitamise ja avada andmeallika siluri liidese.</span><span class="sxs-lookup"><span data-stu-id="e3210-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="e3210-111">Seal saate kuvada saadaolevaid andmeallikaid ja valida käitamiseks konkreetse andmeallika.</span><span class="sxs-lookup"><span data-stu-id="e3210-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="e3210-112">Käsitsi käitamine simuleerib andmeallika käitamist ER-vormingu tavapärase käitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="e3210-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="e3210-113">Tulemus esitatakse lehel, kus saate saadud andmeid analüüsida.</span><span class="sxs-lookup"><span data-stu-id="e3210-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="e3210-114">Andmeallika silumisfunktsiooni sisselülitamiseks seadke ER-i kasutajaparameetrite all suvandi **Luba vormingu käitamisel andmete silumine** sätteks **Jah** .</span><span class="sxs-lookup"><span data-stu-id="e3210-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="e3210-115">Seejärel saate alustada andmeallika silumist, kui käivitate ER-vormingu väljaminevate dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e3210-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="e3210-116">Lisaks saate kasutada suvandit **Alusta silumist**, et käivitada [ER-i toimingukoostajas](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document) konfigureeritud ER-vormingu andmeallika silumine.</span><span class="sxs-lookup"><span data-stu-id="e3210-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="e3210-117">Selles teemas antakse suunised täidetud ER-vormingute andmeallika silumise käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="e3210-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="e3210-118">See selgitab, kuidas mõista teabe abil andmevoogu ja andmete teisendusi.</span><span class="sxs-lookup"><span data-stu-id="e3210-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="e3210-119">Käesolevas teemas toodud näidetes kasutatakse hankija maksete töötlemise äriprotsessi.</span><span class="sxs-lookup"><span data-stu-id="e3210-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="e3210-120">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="e3210-120">Limitations</span></span>

<span data-ttu-id="e3210-121">Andmeallika silurit saab kasutada väljaminevate dokumentide loomiseks käitatavate ER-vormingutes kasutatud andmeallikatele ligi pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="e3210-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="e3210-122">Seda ei saa kasutada sissetulevate dokumentide sõelumiseks loodud ER-vormingute andmeallikate silumiseks.</span><span class="sxs-lookup"><span data-stu-id="e3210-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="e3210-123">Järgmised ER-vormingute sätted ei ole hetkel andmeallikate silumiseks kättesaadavad.</span><span class="sxs-lookup"><span data-stu-id="e3210-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="e3210-124">Vormiteisendused</span><span class="sxs-lookup"><span data-stu-id="e3210-124">Format transformations</span></span>
- <span data-ttu-id="e3210-125">Vormi ja vastendamise kinnitusreeglid</span><span class="sxs-lookup"><span data-stu-id="e3210-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="e3210-126">Avaldiste lubamine</span><span class="sxs-lookup"><span data-stu-id="e3210-126">Enabling expressions</span></span>
- <span data-ttu-id="e3210-127">Mälusisese andmekogumise üksikasjad</span><span class="sxs-lookup"><span data-stu-id="e3210-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e3210-128">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e3210-128">Prerequisites</span></span>

- <span data-ttu-id="e3210-129">Selles teemas toodud näidete läbimiseks peab teil olema juurdepääs ühele järgmistest [rollidest](../sysadmin/tasks/assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e3210-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="e3210-130">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="e3210-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="e3210-131">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="e3210-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e3210-132">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="e3210-132">System administrator</span></span>

- <span data-ttu-id="e3210-133">Ettevõtte sätteks peab olema seatud **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="e3210-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="e3210-134">Järgige käesoleva teema [1. lisas](#appendix1) toodud etappe, et laadida alla Microsofti ER-lahenduse komponendid, mis on vajalikud hankija maksete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="e3210-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="e3210-135">Järgige käesoleva teema [2. lisas](#appendix2) toodud etappe, et valmistada allalaaditavat ER-lahendust kasutades ostureskontro hankija maksete töötlemiseks ette.</span><span class="sxs-lookup"><span data-stu-id="e3210-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="e3210-136">Maksefaili saamiseks hankija makse töötlemine</span><span class="sxs-lookup"><span data-stu-id="e3210-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="e3210-137">Järgige käesoleva teema [3. lisas](#appendix3) toodud etappe, et töödelda hankija makseid.</span><span class="sxs-lookup"><span data-stu-id="e3210-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![Hankija maksete töötlemine on pooleli](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="e3210-139">Laadige alla ja salvestage zip-fail kohalikku arvutisse.</span><span class="sxs-lookup"><span data-stu-id="e3210-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="e3210-140">Ekstraktige zip-failist maksefail **ISO20022 Credit transfer.xml**.</span><span class="sxs-lookup"><span data-stu-id="e3210-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="e3210-141">Avage ekstraktitud maksefail XML-failide vaaturis.</span><span class="sxs-lookup"><span data-stu-id="e3210-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="e3210-142">Maksefailis puuduvad hankija pangakonto rahvusvahelises pangakontonumbris (IBAN) tühikud.</span><span class="sxs-lookup"><span data-stu-id="e3210-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="e3210-143">Seega erineb see lehel **Pangakontod** [sisestatud](#enteredIBANcode) väärtusest.</span><span class="sxs-lookup"><span data-stu-id="e3210-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![Tühikuteta IBAN-kood](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="e3210-145">Saate kasutada ER-i andmeallika silurit, et saada teada, millist ER-lahenduse komponenti kasutatakse IBAN-koodi tühikute kärpimiseks.</span><span class="sxs-lookup"><span data-stu-id="e3210-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="e3210-146">Andmeallika silumise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="e3210-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="e3210-147">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e3210-148">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="e3210-149">Määrake suvandi **Luba vormingu käitamisel andmete silumine** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e3210-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3210-150">See parameeter on kasutajakohane ja ettevõttekohane.</span><span class="sxs-lookup"><span data-stu-id="e3210-150">This parameter is user-specific and company-specific.</span></span>

    ![Kasutaja parameetrite dialoogiaken](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="e3210-152">Hankija makse töötlemine silumiseks</span><span class="sxs-lookup"><span data-stu-id="e3210-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="e3210-153">Järgige käesoleva teema [3. lisas](#appendix3) toodud etappe, et töödelda hankija makseid.</span><span class="sxs-lookup"><span data-stu-id="e3210-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="e3210-154">Valige teateaknas **Jah**, et kinnitada oma soov katkestada hankija makse töötlemine ja käivitada selle asemel lehel **Andmeallikate silumine** andmeallika silumine.</span><span class="sxs-lookup"><span data-stu-id="e3210-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![Kinnituse teateaken](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="e3210-156">Maksetöötluses kasutatavate andmeallikate silumine</span><span class="sxs-lookup"><span data-stu-id="e3210-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="e3210-157">Mudeli vastendamise silumine</span><span class="sxs-lookup"><span data-stu-id="e3210-157">Debug the model mapping</span></span>

1. <span data-ttu-id="e3210-158">ER-komponendi silumise käivitamiseks valige lehekülje **Andmeallikate silumine** toimingupaanil suvand **Mudelivastendus**.</span><span class="sxs-lookup"><span data-stu-id="e3210-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="e3210-159">Valige vasakpoolselt andmeallikate paanilt andmeallikas **\$notSentTransactions** ja seejärel **Loe kõiki kirjeid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="e3210-160">Saate valida **Loe 1 kirje**, **Loe 10 kirjet**, **Loe 100 kirjet** või **Loe kõiki kirjeid**, et valida sobiv kirjete arv, mida valitud andmeallikas loetakse.</span><span class="sxs-lookup"><span data-stu-id="e3210-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="e3210-161">Sel moel saate simuleerida andmetele juurdepääsu töötavast ER-vormingust.</span><span class="sxs-lookup"><span data-stu-id="e3210-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="e3210-162">Valige paremalt andmepaanilt suvand **Laienda kõik**.</span><span class="sxs-lookup"><span data-stu-id="e3210-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="e3210-163">Näete, et **Kirje loetelu** tüübi kohta valitud andmeallikas sisaldub üks kirje.</span><span class="sxs-lookup"><span data-stu-id="e3210-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="e3210-164">Laiendage andmeallikas **\$notSentTransactions** ja valige pesastatud meetod **vendBankAccountInTransactionCompany()**.</span><span class="sxs-lookup"><span data-stu-id="e3210-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="e3210-165">Laiendage meetod **vendBankAccountInTransactionCompany()** ja seejärel valige pesastatud väli **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="e3210-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="e3210-166">Valige **Too väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e3210-166">Select **Get value**.</span></span>

    <span data-ttu-id="e3210-167">Saate valida suvandi **Too väärtus**, et sundkäivitada valitud andmeallika valitud välja väärtuse lugemine.</span><span class="sxs-lookup"><span data-stu-id="e3210-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="e3210-168">Sel moel saate simuleerida antud väljale juurdepääsu töötavast ER-vormingust.</span><span class="sxs-lookup"><span data-stu-id="e3210-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="e3210-169">Valige **Laienda kõik**.</span><span class="sxs-lookup"><span data-stu-id="e3210-169">Select **Expand all**.</span></span>

    ![IBAN-välja väärtus mudeli vastendamisel](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="e3210-171">Nagu näete, ei vastuta mudelivastendus kärbitud tühikute eest, kuna tagastatav hankija pangakonto IBAN-kood sisaldab tühikuid.</span><span class="sxs-lookup"><span data-stu-id="e3210-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="e3210-172">Seega peate jätkama andmeallika silumist.</span><span class="sxs-lookup"><span data-stu-id="e3210-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="e3210-173">Vormingu vastendamise silumine</span><span class="sxs-lookup"><span data-stu-id="e3210-173">Debug the format mapping</span></span>

1. <span data-ttu-id="e3210-174">ER-komponendi silumise jätkamiseks valige lehekülje **Andmeallikate silumine** toimingupaanil suvand **Mudelivastendus**.</span><span class="sxs-lookup"><span data-stu-id="e3210-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="e3210-175">Valige **\$PaymentByDebtor** ja seejärel valige **Loe kõiki kirjeid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="e3210-176">Laiendage **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="e3210-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="e3210-177">Laiendage **\$PaymentByDebtor.Lines** ja seejärel valige **Loe kõiki kirjeid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="e3210-178">Laiendage **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="e3210-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="e3210-179">Laiendage **\$PaymentByDebtor.Lines.CreditorAccount.Identification** ja seejärel valige **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="e3210-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="e3210-180">Valige **Too väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e3210-180">Select **Get value**.</span></span>
8. <span data-ttu-id="e3210-181">Valige **Laienda kõik**.</span><span class="sxs-lookup"><span data-stu-id="e3210-181">Select **Expand all**.</span></span>

    ![IBAN-välja väärtus vormingu vastendamisel](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="e3210-183">Nagu näete, ei vastuta vorminguvastenduse andmeallikad kärbitud tühikute eest, kuna tagastatav hankija pangakonto IBAN-kood sisaldab tühikuid.</span><span class="sxs-lookup"><span data-stu-id="e3210-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="e3210-184">Seega peate jätkama andmeallika silumist.</span><span class="sxs-lookup"><span data-stu-id="e3210-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="e3210-185">Vormingu silumine</span><span class="sxs-lookup"><span data-stu-id="e3210-185">Debug the format</span></span>

1. <span data-ttu-id="e3210-186">ER-komponendi silumise jätkamiseks valige lehekülje **Andmeallikate silumine** toimingupaanil suvand **Vorming**.</span><span class="sxs-lookup"><span data-stu-id="e3210-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="e3210-187">Laiendage vormingu elemendid, et valida **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf**, ja seejärel valige **Loe kõiki kirjeid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="e3210-188">Laiendage vormingu elemendid, et valida **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, ja seejärel valige **Loe kõiki kirjeid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="e3210-189">Laiendage vormingu elemendid, et valida **ISO20022CTReports** \> **XMLHeader** \> **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, ja seejärel valige **Too väärtus**.</span><span class="sxs-lookup"><span data-stu-id="e3210-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="e3210-190">Valige **Laienda kõik**.</span><span class="sxs-lookup"><span data-stu-id="e3210-190">Select **Expand all**.</span></span>

    ![IBAN-välja väärtus vormingus](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="e3210-192">Nagu näete, ei vastuta vormingu sidumine kärbitud tühikute eest, kuna tagastatav hankija pangakonto IBAN-kood sisaldab tühikuid.</span><span class="sxs-lookup"><span data-stu-id="e3210-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="e3210-193">Seega on elementi **BankIBAN** konfigureeritud kasutama vorminguteisendust, mis kärbib tühikuid.</span><span class="sxs-lookup"><span data-stu-id="e3210-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="e3210-194">Sulgege andmeallika silur.</span><span class="sxs-lookup"><span data-stu-id="e3210-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="e3210-195">Vorminguteisenduste ülevaatus</span><span class="sxs-lookup"><span data-stu-id="e3210-195">Review the format transformations</span></span>

1. <span data-ttu-id="e3210-196">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e3210-197">Valige leheküljel **Konfiguratsioonid** suvand **Maksemudel** \> **ISO20022 kreeditülekanne**.</span><span class="sxs-lookup"><span data-stu-id="e3210-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="e3210-198">Valige **Kujundaja** ja seejärel laiendage elemendid, et valida **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="e3210-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![BankIBAN element vormingukujundaja lehel](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="e3210-200">Nagu näete, on elementi **BankIBAN** konfigureeritud kasutama teisendust **eemalda mittetähtnumbrimärgid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="e3210-201">Valige vahekaart **Teisendused**.</span><span class="sxs-lookup"><span data-stu-id="e3210-201">Select the **Transformations** tab.</span></span>

    ![BankIBAN elemendi teisenduste vahekaart](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="e3210-203">Nagu näete, siis on teisendus **eemalda mittetähtnumbrimärgid** konfigureeritud kasutama avaldist, mis kärbib esitatud tekstistringist tühikud.</span><span class="sxs-lookup"><span data-stu-id="e3210-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="e3210-204">Toimingukoostajas silumise käivitamine</span><span class="sxs-lookup"><span data-stu-id="e3210-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="e3210-205">Kui konfigureerite ER-vormingu mustandversiooni, mida saab käitada otse toimingukoostajas, siis pääsete ligi andmeallika silurile, valides toimingupaanilt **Alusta silumist**.</span><span class="sxs-lookup"><span data-stu-id="e3210-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Silumise alustamise nupp vormingu koostaja lehel](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="e3210-207">Redigeeritava ER-vormingu vorminguvastendus ja vormingu komponendid on silumiseks kättesaadavad.</span><span class="sxs-lookup"><span data-stu-id="e3210-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="e3210-208">Mudelivastenduse koostajas silumise käivitamine</span><span class="sxs-lookup"><span data-stu-id="e3210-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="e3210-209">Kui konfigureerite ER-vormingu mudelivastendust, mida saab käitada lehel **Mudelivastendus**, siis pääsete ligi andmeallika silurile, valides toimingupaanilt **Alusta silumist**.</span><span class="sxs-lookup"><span data-stu-id="e3210-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![Silumise alustamise nupp mudelivastenduse koostaja lehel](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="e3210-211">Redigeeritava ER-vastenduse mudelivastenduse komponent on silumiseks kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="e3210-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="e3210-212">1. lisa: ER-lahenduse hankimine</span><span class="sxs-lookup"><span data-stu-id="e3210-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="e3210-213">ER-lahenduse allalaadimine</span><span class="sxs-lookup"><span data-stu-id="e3210-213">Download an ER solution</span></span>

<span data-ttu-id="e3210-214">Kui soovite töödeldava hankija makse kohta loodava elektroonilise maksefaili loomiseks kasutada ER-lahendust, siis saate [laadida alla](download-electronic-reporting-configuration-lcs.md) ER-maksevormingu **ISO20022 kreeditülekanne**, mis on kättesaadav rakenduse Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegis või globaalses hoidlas.</span><span class="sxs-lookup"><span data-stu-id="e3210-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![ER-maksevormingu importimine konfiguratsiooni hoidla lehel](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="e3210-216">Lisaks valitud ER-vormingule tuleb ER-lahenduse **ISO20022 kreeditülekanne** raames automaatselt Microsoft Dynamics 365 Finance'i eksemplari importida ka järgmised [konfiguratsioonid](general-electronic-reporting.md#Configuration).</span><span class="sxs-lookup"><span data-stu-id="e3210-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="e3210-217">**Maksemudel** [ER-i andmemudeli konfiguratsioon](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="e3210-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="e3210-218">**ISO20022 kreeditülekanne** [ER-vormingu konfiguratsioon](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="e3210-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="e3210-219">**Maksemudeli vastendamine 1611** [ER-mudeli vastendamise konfiguratsioon](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="e3210-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="e3210-220">**Maksemudeli vastendamine sihtkohta ISO20022** ER-mudeli vastendamise konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="e3210-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="e3210-221">Need konfiguratsioonid leiate ER-raamistiku lehelt **Konfiguratsioonid** (**Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**).</span><span class="sxs-lookup"><span data-stu-id="e3210-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![Imporditud konfiguratsioonid lehel Konfiguratsioonid](./media/er-data-debugger-configurations.png)

<span data-ttu-id="e3210-223">Kui konfiguratsioonipuus puudub mõni varasemalt loetletud konfiguratsioon, siis peate need käsitsi LCS-i ühiste vahendite teegist alla laadima samal viisil, nagu laadisite alla ER-maksevormingu **ISO20022 kreeditülekanne**.</span><span class="sxs-lookup"><span data-stu-id="e3210-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="e3210-224">Allalaaditud ER-lahenduse analüüsimine</span><span class="sxs-lookup"><span data-stu-id="e3210-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="e3210-225">Mudeli vastendamise läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="e3210-225">Review the model mapping</span></span>

1. <span data-ttu-id="e3210-226">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e3210-227">Valige **Maksemudel** \> **Maksemudeli vastendus 1611**.</span><span class="sxs-lookup"><span data-stu-id="e3210-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="e3210-228">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e3210-228">Select **Designer**.</span></span>
4. <span data-ttu-id="e3210-229">Valige vastendamiskirje **Maksemudeli vastendus ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="e3210-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="e3210-230">Valige **Kujundaja** ja seejärel vaadake läbi avatud mudelivastendus.</span><span class="sxs-lookup"><span data-stu-id="e3210-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="e3210-231">Pange tähele, et andmemudeli väli **Maksed** on seotud andmeallikaga **\$notSentTransactions**, mis tagastab töödeldavate hankija maksete ridade loetelu.</span><span class="sxs-lookup"><span data-stu-id="e3210-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![Maksete väli mudelivastendamise kujundaja lehel](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="e3210-233">Vormingu vastendamise läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="e3210-233">Review the format mapping</span></span>

1. <span data-ttu-id="e3210-234">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e3210-235">Valige **Maksemudel** \> **ISO20022 kreeditülekanne**.</span><span class="sxs-lookup"><span data-stu-id="e3210-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="e3210-236">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e3210-236">Select **Designer**.</span></span>
4. <span data-ttu-id="e3210-237">Teostage lehel **Vastendamine** avatud vorminguvastenduse läbivaatus.</span><span class="sxs-lookup"><span data-stu-id="e3210-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="e3210-238">Pange tähele, et faili **ISO20022CTReports** \> **XMLHeader** element **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** on seotud andmeallikaga **\$PaymentByDebtor**, mis on andmemudeli väljal **Maksed** konfigureeritud grupi kirjetesse.</span><span class="sxs-lookup"><span data-stu-id="e3210-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![PmtInf element vormingukujundaja lehel](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="e3210-240">Vormingu läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="e3210-240">Review the format</span></span>

1. <span data-ttu-id="e3210-241">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e3210-242">Valige **Maksemudel** \> **ISO20022 kreeditülekanne**.</span><span class="sxs-lookup"><span data-stu-id="e3210-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="e3210-243">Valige **Kujundaja** ja seejärel vaadake läbi avatud vorming.</span><span class="sxs-lookup"><span data-stu-id="e3210-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="e3210-244">Pange tähele, et suvandi **Dokument** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** all toodud vormingu element on konfigureeritud hankija konto IBAN-koodi sisestamiseks maksefaili.</span><span class="sxs-lookup"><span data-stu-id="e3210-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![BankIBAN element vormingukujundaja lehel](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="e3210-246">2. lisa: ostureskontro konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e3210-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="e3210-247">Hankija atribuudi muutmine</span><span class="sxs-lookup"><span data-stu-id="e3210-247">Modify a vendor property</span></span>

1. <span data-ttu-id="e3210-248">Avage **Ostureskontro** \> **Hankijad** \> **Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="e3210-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="e3210-249">Valige hankija **DE-01002** ja seejärel valige toimingupaani vahekaardil **Hankija** grupis **Seadistamine** suvand **Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="e3210-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="e3210-250">Valige kiirkaardil **Identifitseerimine** väli **IBAN**, <a name="enteredIBANcode"></a>sisestage **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="e3210-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="e3210-251">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e3210-251">Select **Save**.</span></span>

![IBAN-i väli hankija pangakontode lehel](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="e3210-253">Makseviisi seadistamine</span><span class="sxs-lookup"><span data-stu-id="e3210-253">Set up a method of payment</span></span>

1. <span data-ttu-id="e3210-254">Avage **Ostureskontro** \> **Maksmise seadistamine** \> **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="e3210-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="e3210-255">Valige makseviis **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="e3210-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="e3210-256">Seadistage kiirkaardi **Failivormingud** jaotises **Failivormingud** suvandi **Üldine elektrooniline ekspordivorming** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e3210-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="e3210-257">Valige väljal **Ekspordivormingu konfiguratsioon** ER-vorming **ISO20022 kreeditülekanne**.</span><span class="sxs-lookup"><span data-stu-id="e3210-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="e3210-258">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e3210-258">Select **Save**.</span></span>

![Failivormingu sätted makseviiside lehel](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="e3210-260">Hankija makse lisamine</span><span class="sxs-lookup"><span data-stu-id="e3210-260">Add a vendor payment</span></span>

1. <span data-ttu-id="e3210-261">Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="e3210-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="e3210-262">Lisage uus makseleht.</span><span class="sxs-lookup"><span data-stu-id="e3210-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="e3210-263">Valige **Read** ja lisage uus makserida.</span><span class="sxs-lookup"><span data-stu-id="e3210-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="e3210-264">Valige väljal **Konto** hankija **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="e3210-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="e3210-265">Sisestage väljale **Deebet** väärtus.</span><span class="sxs-lookup"><span data-stu-id="e3210-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="e3210-266">Valige väljal **Makseviis** **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="e3210-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="e3210-267">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e3210-267">Select **Save**.</span></span>

![Lisatud hankija makse hankija maksete lehel](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="e3210-269">3. lisa: hankija makse töötlemine</span><span class="sxs-lookup"><span data-stu-id="e3210-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="e3210-270">Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="e3210-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="e3210-271">Valige lehel **Hankija maksete tööleht** varasemalt loodud maksete tööleht ja seejärel valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="e3210-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="e3210-272">Valige makserida ja seejärel valige **Makse olek** \> **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="e3210-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="e3210-273">Valige **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="e3210-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="e3210-274">Valige väljal **Makseviis** **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="e3210-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="e3210-275">Valige väljal **Pangakonto** suvand **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="e3210-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="e3210-276">Valige dialoogiaknas **Maksete loomine** suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3210-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="e3210-277">Valige dialoogiaknas **Elektroonilise aruandluse parameetrid** suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="e3210-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]