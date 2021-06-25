---
title: Kasutushalduse armatuurlaud
description: Käesolev teema kirjeldab, kuidas kasutada kasutushalduse armatuurlauda elektroonilise arveldamise teenuse kasutamise jälgimiseks ja ühildumiseks jäämiseks.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130502"
---
# <a name="usage-management-dashboard"></a><span data-ttu-id="6f1a5-103">Kasutushalduse armatuurlaud</span><span class="sxs-lookup"><span data-stu-id="6f1a5-103">Usage management dashboard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f1a5-104">**Kasutushalduse** armatuurlaud aitab jälgida elektroonilise arveldamise teenuse kasutamist ning seega aitab teie organisatsioonil püsida ühilduvigakuiste kasutustingimustega.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-104">The **Usage management** dashboard helps you monitor usage of the Electronic Invoicing service, and therefore helps your organization remain compliant in terms of its monthly usage.</span></span> <span data-ttu-id="6f1a5-105">Vastavuse määratleb esitamise mahu arvutamine ja võrreldakse seda esitamise soetatud mahuga, et tuvastada mis tahes kõrvalekaldeid soetatud mahu ja kasutatud mahu vahel.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-105">Compliance is determined by calculating the submission volume and comparing it with the acquired volume of submissions to identify any deviations between the acquired volume and the used volume.</span></span>

<span data-ttu-id="6f1a5-106">Armatuurlaud sisaldab järgmisi näidikuid:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-106">The dashboard includes the following indicators:</span></span>

- <span data-ttu-id="6f1a5-107">Üks kulumõõdik, mida saate kasutada tarbimise jälgimiseks litsentsimise vastavuse eesmärkidel:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-107">One cost indicator that you can use to monitor consumption for licensing compliance purposes:</span></span>

    - <span data-ttu-id="6f1a5-108">Kasutamine kuus (eksport)</span><span class="sxs-lookup"><span data-stu-id="6f1a5-108">Usage per month (export)</span></span>

- <span data-ttu-id="6f1a5-109">Kolm töönäitajat, mida saate kasutada elektroonilise arveldamise teenuse kasutamise jälgimiseks halduseesmärkidel:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-109">Three operational indicators that you can use to track usage of the Electronic Invoicing service for management purposes:</span></span>

    - <span data-ttu-id="6f1a5-110">Kasutus funktsiooni järgi</span><span class="sxs-lookup"><span data-stu-id="6f1a5-110">Usage by feature</span></span>
    - <span data-ttu-id="6f1a5-111">Kasutus keskkonna järgi</span><span class="sxs-lookup"><span data-stu-id="6f1a5-111">Usage by environment</span></span>
    - <span data-ttu-id="6f1a5-112">Kasutus kuus (import)</span><span class="sxs-lookup"><span data-stu-id="6f1a5-112">Usage per month (import)</span></span>

## <a name="measurement-scope"></a><span data-ttu-id="6f1a5-113">Mõõtmise ulatus</span><span class="sxs-lookup"><span data-stu-id="6f1a5-113">Measurement scope</span></span>

- <span data-ttu-id="6f1a5-114">Mõõtmise ühik:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-114">Unit of measure:</span></span> 

    <span data-ttu-id="6f1a5-115">**Kasutushalduse** armatuurlaud loendab äridokumentide ja imporditud elektrooniliste arvete esitamist.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-115">The **Usage management** dashboard counts the submission of business documents and imported electronic invoices.</span></span>

- <span data-ttu-id="6f1a5-116">Organisatsioon:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-116">Organization:</span></span> 

    <span data-ttu-id="6f1a5-117">Inventuuri summeerib teie organisatsiooni rentniku ID, olenemata Microsoft Dynamics 365 Finance või Dynamics 365 Supply Chain Management eksemplaride arvust või juriidiliste isikute arvust, kus elektroonilise arveldamiseteenus on lubatud.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-117">Counting is summarized by the tenant ID of your organization, regardless of the number of instances of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management, or the number of legal entities where the Electronic Invoicing service is enabled.</span></span>


## <a name="indicator-usage-per-month-export"></a><span data-ttu-id="6f1a5-118">Näitaja: kasutus kuus (eksport)</span><span class="sxs-lookup"><span data-stu-id="6f1a5-118">Indicator: Usage per month (export)</span></span>

<span data-ttu-id="6f1a5-119">See indikaator annab üksikasju elektrooniliste arvete kohta, mida teie organisatsioon määratletud perioodi jooksul väljastab.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-119">This indicator provides details about the electronic invoices that your organization issues during a defined period.</span></span>

### <a name="scope"></a><span data-ttu-id="6f1a5-120">Ulatus</span><span class="sxs-lookup"><span data-stu-id="6f1a5-120">Scope</span></span>
- <span data-ttu-id="6f1a5-121">Äridokumentide arv, mis on esitatud Finance and Supply Chain Management elektroonilise arveldamise teenusele, sõltumata ridade arvust, mida need äridokumendid sisaldavad.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-121">The number of business documents that are submitted from Finance and Supply Chain Management to the Electronic Invoicing service, regardless of number of lines that those business documents contain.</span></span>
- <span data-ttu-id="6f1a5-122">Edastatud äridokumentide arv, mida elektroonilise arveldamise teenus edukalt töötleb.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-122">The number of submitted business documents that are successfully processed by the Electronic Invoicing service.</span></span> <span data-ttu-id="6f1a5-123">Kui funktsiooniseadistuses määratletud tegevuste voog on lõpule viidud, loetakse dokument edukalt töödelduks.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-123">A document is considered successfully processed when the flow of actions that are defined in the feature setup is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="6f1a5-124">Kui elektrooniline arve esitatakse välisele veebiteenusele, ei sõltu inventuur veebiteenuse töötlemise tulemustest (aktsepteeritud, tagasi lükatud või skeemi kinnitamistõrge).</span><span class="sxs-lookup"><span data-stu-id="6f1a5-124">When an electronic invoice is submitted to an external web service, counting is independent of the results of web service processing (accepted, rejected, or schema validation error).</span></span> <span data-ttu-id="6f1a5-125">Kui veebiteenus sai ja vastas elektroonilise arveldamise teenuse taotlusele, loetakse esitamine kehtivaks inventuuriks.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-125">If the web service received and responded to the request from the Electronic Invoicing service, the submission is considered a valid counting.</span></span>

- <span data-ttu-id="6f1a5-126">**Erand:** äridokumente ei arvestata, kui need on uuesti Finance and Supply Chain Management elektroonilise arveldamise teenusesse esitatud, nt stsenaariumides, kus elektroonilise arve oleku muutmiseks on vajalik sama äridokumendi uuesti esitada.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-126">**Exception:** Business documents aren't counted if they are resubmitted from Finance and Supply Chain Management to the Electronic Invoicing service, such as in the scenarios where a resubmission of the same business document is required to change the status of the electronic invoice.</span></span> <span data-ttu-id="6f1a5-127">Näiteks Brasiilia elektroonilise arve väljastamist (fiskaaldokument) loetakse kehtivaks, kuid selle tühistamistaotlust ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-127">For example, issuance of a Brazilian electronic invoice (fiscal document) is counted as valid, but the cancellation request for it isn't counted.</span></span>


### <a name="calculation"></a><span data-ttu-id="6f1a5-128">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="6f1a5-128">Calculation</span></span>

<span data-ttu-id="6f1a5-129">Saldo arvutatakse järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-129">The calculation of the balance is calculated as follows:</span></span>

<span data-ttu-id="6f1a5-130">Saldo = Vaba + Ostetud – Kasutatud</span><span class="sxs-lookup"><span data-stu-id="6f1a5-130">Balance = Free + Purchased – Used</span></span>

<span data-ttu-id="6f1a5-131">Kus</span><span class="sxs-lookup"><span data-stu-id="6f1a5-131">Where:</span></span>

- <span data-ttu-id="6f1a5-132">Vaba:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-132">Free:</span></span>
  
    <span data-ttu-id="6f1a5-133">Äridokumentide vaba maht, mille klient saab kuu kohta esitada.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-133">A free volume of business documents the customer can submit per month.</span></span> <span data-ttu-id="6f1a5-134">See sisaldab 100 äridokumendi paketti, mida saab elektroonilise arvelduse teenusele esitada.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-134">It includes a package of 100 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="6f1a5-135">Vaba maht pole kumulatiivne ja ülejäänud saldot ei pöörata üle järgmisele perioodile.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-135">Free volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="6f1a5-136">Ostetud:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-136">Purchased:</span></span>
  
    <span data-ttu-id="6f1a5-137">See sisaldab 1000 äridokumendi paketti, mida saab elektroonilise arvelduse teenusele esitada.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-137">A package of 1,000 business documents that can be submitted to the Electronic Invoicing service.</span></span> <span data-ttu-id="6f1a5-138">See pakett tuleb soetuda teie organisatsioonile kord kuus.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-138">This package must be acquired for your organization on a monthly basis.</span></span> <span data-ttu-id="6f1a5-139">Vaba maht pole kumulatiivne ja ülejäänud saldot ei pöörata üle järgmisele perioodile.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-139">Purchased volume isn't cumulative, and any remaining balance isn't rolled over to the next period.</span></span>
  
- <span data-ttu-id="6f1a5-140">Kasutatud:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-140">Used:</span></span> 

    <span data-ttu-id="6f1a5-141">Äridokumendiedastuste arv elektroonilise arvelduse teenusele vastavalt määratletud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-141">The count of business document submissions to the Electronic Invoicing service according to defined criteria.</span></span>
   
> [!IMPORTANT]
> <span data-ttu-id="6f1a5-142">Kui teie organisatsioon plaanib ületada igakuist mahtu 100 vabaedastuse korral, ostke tippmaht, et tagada teie vastavus Microsofti elektroonilise arveldamise teenuse litsentsipoliitikaga.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-142">If your organization plans to exceed the monthly volume of 100 free submissions, purchase the peak volume to ensure that you remain compliant with the Microsoft licensing policy for the Electronic Invoicing service.</span></span>
>
> <span data-ttu-id="6f1a5-143">Praegu tuleb ostetud maht vastavalt soetuskuupäevale sisestada käsitsi mitme 1000 esitamisega pakendina.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-143">Currently, purchased volume must be manually entered, according to the date of acquisition, as multiple packages of 1,000 submissions.</span></span>

## <a name="indicator-usage-by-feature"></a><span data-ttu-id="6f1a5-144">Indikaator: kasutus funktsiooni järgi</span><span class="sxs-lookup"><span data-stu-id="6f1a5-144">Indicator: Usage by feature</span></span>

<span data-ttu-id="6f1a5-145">See näidik näitab elektroonilise arveldamise funktsioonide kasutamist elektrooniliste arvete väljastamiseks määratletud perioodil.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-145">This indicator shows the usage of electronic invoicing features for issuance of electronic invoices during a defined period.</span></span>

- <span data-ttu-id="6f1a5-146">Kalkulatsioon:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-146">Calculation:</span></span>
  
    <span data-ttu-id="6f1a5-147">Kasutatud = loendamine, mitu korda iga elektroonilise arvelduse funktsiooni kasutati äridokumentide edastamisel elektroonilise arveldamise teenusele.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-147">Used = The count of how many times each electronic invoicing feature was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-by-environment"></a><span data-ttu-id="6f1a5-148">Indikaator: kasutus keskkonna järgi</span><span class="sxs-lookup"><span data-stu-id="6f1a5-148">Indicator: Usage by environment</span></span>

<span data-ttu-id="6f1a5-149">See näidik näitab elektroonilise arveldamise teenuse keskkondade kasutamist määratletud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-149">This indicator shows the usage of electronic invoicing service environments during a defined period.</span></span>

- <span data-ttu-id="6f1a5-150">Kalkulatsioon:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-150">Calculation:</span></span>
    
    <span data-ttu-id="6f1a5-151">Kasutatud = loendamine, mitu korda iga elektroonilise arvelduse teenuse keskkonda kasutati äridokumentide edastamisel elektroonilise arveldamise teenusele.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-151">Used = The count of how many times each electronic invoicing service environment was used during the submission of business documents to the Electronic Invoicing service.</span></span>

## <a name="indicator-usage-per-month-import"></a><span data-ttu-id="6f1a5-152">Näitaja: kasutus kuus (import)</span><span class="sxs-lookup"><span data-stu-id="6f1a5-152">Indicator: Usage per month (import)</span></span>

<span data-ttu-id="6f1a5-153">See näidik näitab elektrooniliste arvete mahtu elektroonilise arveldamist Finance and Supply Chain Management kaudu määratletud perioodil.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-153">This indicator shows the volume of importation of electronic invoices by Electronic Invoicing service into Finance and Supply Chain Management during a defined period.</span></span>

- <span data-ttu-id="6f1a5-154">Ulatus:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-154">Scope:</span></span>

    <span data-ttu-id="6f1a5-155">Finance and Supply Chain Management imporditud elektroonilised arved, sõltumata ridade arvust, mida need elektroonilised arved sisaldavad.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-155">Electronic invoices that are imported into Finance and Supply Chain Management, regardless of the number of lines that those electronic invoices contain.</span></span>

- <span data-ttu-id="6f1a5-156">Kalkulatsioon:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-156">Calculation:</span></span>

    <span data-ttu-id="6f1a5-157">Saadud = Finance and Supply Chain Management\`ìst imporditud elektrooniliste arvete arv.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-157">Received = The count of imported electronic invoices into Finance and Supply Chain Management.</span></span>

## <a name="functions"></a><span data-ttu-id="6f1a5-158">Funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6f1a5-158">Functions</span></span>
### <a name="purchase"></a><span data-ttu-id="6f1a5-159">Ost</span><span class="sxs-lookup"><span data-stu-id="6f1a5-159">Purchase</span></span>

<span data-ttu-id="6f1a5-160">Valige **Kasutus kuus (eksport)** vahekaardil **Ost**, et soetatud edastuste summa käsitsi registreerida.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-160">On the **Usage per month (export)** tab, select **Purchase** to manually register the amount of acquired submissions.</span></span>

<span data-ttu-id="6f1a5-161">Antud kuupäeval tehke valik **Uus** ja sisestage sel kuupäeval soetatud **pakendite arv**.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-161">For a given date, select **New** and enter the number of **Packages** acquired for on that date.</span></span>

<span data-ttu-id="6f1a5-162">**Kogus** arvutatakse järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="6f1a5-162">The **Quantity** is calculated as:</span></span>

<span data-ttu-id="6f1a5-163">Kogus = Pakendid \* 1000</span><span class="sxs-lookup"><span data-stu-id="6f1a5-163">Quantity = Packages \* 1.000</span></span>

<span data-ttu-id="6f1a5-164">Arvutatud **kogus** peegeldab välja **Ostetud** indikaatorilt **Kasutus kuus (eksport)**.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-164">The calculated **Quantity** reflects in the **Purchased** from the indicator **Usage per month (export)**.</span></span>

### <a name="update"></a><span data-ttu-id="6f1a5-165">Värskendus</span><span class="sxs-lookup"><span data-stu-id="6f1a5-165">Update</span></span>

<span data-ttu-id="6f1a5-166">Tegevuspaanil valige **uuendamine**, et värskendada arvutust ja värskendada leheküljel ja diagrammil kuvatavaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-166">On the Action Pane, select **Update** to refresh the calculation and update the data shown on the page and in the chart.</span></span>

### <a name="reset-history-data"></a><span data-ttu-id="6f1a5-167">Lähtesta ajaloo andmed</span><span class="sxs-lookup"><span data-stu-id="6f1a5-167">Reset history data</span></span>

<span data-ttu-id="6f1a5-168">Tegevuspaanil valige suvand **Lähtesta ajaloo andmed**, et värskendada andmebaasi näidikute arvutamise asukohast.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-168">On the Action Pane, select **Reset history data** to refresh the database from where the indicators are calculated.</span></span>




> [!NOTE]
> <span data-ttu-id="6f1a5-169">**Kasutushalduse** armatuurlaud ei näita rahasummasid.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-169">The **Usage management** dashboard doesn't show monetary amounts.</span></span> <span data-ttu-id="6f1a5-170">Selle asemel näitab see ainult loendatud ja imporditud dokumentide mahtu.</span><span class="sxs-lookup"><span data-stu-id="6f1a5-170">Instead, it shows only the volume of counted submissions and imported documents.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
