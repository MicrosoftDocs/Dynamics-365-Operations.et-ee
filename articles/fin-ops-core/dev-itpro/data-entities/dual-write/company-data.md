---
title: Ettevõtte mõiste teenuses Dataverse
description: Selles teemas kirjeldatakse ettevõtte andmete integreerimist rakenduse Finance and Operations ja teenuse Dataverse vahel.
author: RamaKrishnamoorthy
ms.date: 08/04/2020
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
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6a858135d377b30d6e8885ae18b2dc50da11813b
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941025"
---
# <a name="company-concept-in-dataverse"></a><span data-ttu-id="275e9-103">Ettevõtte mõiste teenuses Dataverse</span><span class="sxs-lookup"><span data-stu-id="275e9-103">Company concept in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


<span data-ttu-id="275e9-104">Rakenduses Finance and Operations on mõiste *ettevõte* nii juriidiline kui ka ka ärikonstruktsioon.</span><span class="sxs-lookup"><span data-stu-id="275e9-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="275e9-105">See on ka andmete turvalisuse ja nähtavuse piir.</span><span class="sxs-lookup"><span data-stu-id="275e9-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="275e9-106">Kasutajad töötavad alati ühe ettevõtte kontekstis ning ettevõte segmendib enamiku andmetest.</span><span class="sxs-lookup"><span data-stu-id="275e9-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="275e9-107">Teenuses Dataverse pole ei ole samaväärset mõistet.</span><span class="sxs-lookup"><span data-stu-id="275e9-107">Dataverse doesn't have an equivalent concept.</span></span> <span data-ttu-id="275e9-108">Lähim mõiste on *äriüksus*, mis on peamiselt kasutajaandmete turvalisuse ja nähtavuse piir.</span><span class="sxs-lookup"><span data-stu-id="275e9-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="275e9-109">Sellel mõistel pole sama juriidilist ega ärimõju nagu ettevõtte mõistel.</span><span class="sxs-lookup"><span data-stu-id="275e9-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="275e9-110">Kuna äriüksus ja ettevõte ei ole samaväärsed mõisted, ei ole võimalik jõustada üks-ühele (1:1) vastendust nende vahel teenuse Dataverse integratsiooni eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="275e9-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Dataverse integration.</span></span> <span data-ttu-id="275e9-111">Kuid kuna kasutajad peavad vaikimisi nägema samu ridu rakenduses ja teenuses Dataverse, on Microsoft võtnud teenuses Dataverse kasutusele uue tabeli nimega CDM\_Company.</span><span class="sxs-lookup"><span data-stu-id="275e9-111">However, because users must, by default, be able to see the same rows in the application and Dataverse, Microsoft has introduced a new table in Dataverse that is named cdm\_Company.</span></span> <span data-ttu-id="275e9-112">See tabel on samaväärne rakenduse tabeliga Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="275e9-112">This table is equivalent to the Company table in the application.</span></span> <span data-ttu-id="275e9-113">Selleks, et ridade nähtavus oleks valmislahendusena rakenduse ja teenuse Dataverse vahel samaväärne, soovitame teenuse Dataverse andmete järgmist seadistust.</span><span class="sxs-lookup"><span data-stu-id="275e9-113">To help guarantee that visibility of rows is equivalent between the application and Dataverse out of the box, we recommend the following setup for data in Dataverse:</span></span>

+ <span data-ttu-id="275e9-114">Igale Finance and Operationsi ettevõtte reale, millele on topeltkirjutus lubatud, luuakse seotud rida cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="275e9-114">For each Finance and Operations Company row that is enabled for dual-write, an associated cdm\_Company row is created.</span></span>
+ <span data-ttu-id="275e9-115">Kui rida CDM\_Company on loodud ja lubatud kahesuguse kirjutuse jaoks, luuakse samanimeline vaikeäriüksus.</span><span class="sxs-lookup"><span data-stu-id="275e9-115">When a cdm\_Company row is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="275e9-116">Kuigi selle äriüksuse jaoks luuakse automaatselt vaiketöörühm, ei kasutata äriüksust.</span><span class="sxs-lookup"><span data-stu-id="275e9-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="275e9-117">Luuakse eraldi omaniku töörühm, millel on sama nimi.</span><span class="sxs-lookup"><span data-stu-id="275e9-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="275e9-118">See on samuti äriüksusega seostatud.</span><span class="sxs-lookup"><span data-stu-id="275e9-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="275e9-119">Mistahes rea omanik, mis on loodud ja kahesuguselt kirjutatud teenusesse Dataverse, on vaikimisi määratud väärtuseks „DW omanikust töörühm, mis on lingitud seostatud äriüksusega.</span><span class="sxs-lookup"><span data-stu-id="275e9-119">By default, the owner of any row that is created and dual-written to Dataverse is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="275e9-120">Järgmisel joonisel on näide seda tüüpi andmete seadistamise kohta teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="275e9-120">The following illustration shows an example of this data setup in Dataverse.</span></span>

![Andmete seadistus teenuses Dataverse](media/dual-write-company-1.png)

<span data-ttu-id="275e9-122">Selle konfiguratsiooni tõttu kuulub kõigi USMF-i ettevõttega seotud rea töörühmale, mis on seotud USMF-i äriüksusega teenuses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="275e9-122">Because of this configuration, any row that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Dataverse.</span></span> <span data-ttu-id="275e9-123">Seetõttu saab iga kasutaja, kellel on juurdepääs sellele äriüksusele turberolli kaudu, mis on määratud äriüksuse tasemel nähtavusele, nüüd näha neid ridu.</span><span class="sxs-lookup"><span data-stu-id="275e9-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those rows.</span></span> <span data-ttu-id="275e9-124">Järgnev näide näitab, kuidas töörühmi saab kasutada neile ridadele õige juurdepääsu pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="275e9-124">The following example shows how teams can be used to provide the correct access to those rows.</span></span>

+ <span data-ttu-id="275e9-125">Roll "Müügihaldur" on määratud "USMF müük" töörühma liikmetele.</span><span class="sxs-lookup"><span data-stu-id="275e9-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="275e9-126">Kasutajad, kellel on roll „Müügihaldur", pääsevad juurde mistahes kontoridadele, mis on sama äriüksuse liikmed.</span><span class="sxs-lookup"><span data-stu-id="275e9-126">Users who have the "Sales Manager" role can access any account rows that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="275e9-127">Töörühm "USMF müük" on seotud varem mainitud USMF-i äriüksusega.</span><span class="sxs-lookup"><span data-stu-id="275e9-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="275e9-128">Seetõttu saavad töörühma „USMF Sales” liikmed vaadata mistahes kontot, mis kuulub „USMF DW” kasutajale, mis oleks tulnud USMF ettevõtte tabelist rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="275e9-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company table in Finance and Operations.</span></span>

![Töörühmade kasutamine](media/dual-write-company-2.png)

<span data-ttu-id="275e9-130">Vastavalt eespool toodud joonisele, on see 1:1 vastendamine äriüksuse, ettevõtte ja töörühma vahel vaid alguspunkt.</span><span class="sxs-lookup"><span data-stu-id="275e9-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="275e9-131">Selles näites luuakse teenuses Dataverse uus "Euroopa" äriüksus käsitsi ülataseme üksusena nii DEMF-i kui ka ESMF-i jaoks.</span><span class="sxs-lookup"><span data-stu-id="275e9-131">In this example, a new "Europe" business unit is manually created in Dataverse as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="275e9-132">See uus juuräriüksus pole kahesuguse kirjutamisega seotud.</span><span class="sxs-lookup"><span data-stu-id="275e9-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="275e9-133">Siiski saab seda kasutada "EUR Sales" töörühmale juurdepääsu andmiseks kontoandmetele nii DEMF-is kui ka ESMF-is, määrates seostatud turberollis andmete nähtavuseks **Ülataseme/alataseme äriüksus**.</span><span class="sxs-lookup"><span data-stu-id="275e9-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="275e9-134">Viimaseks aruteluteemaks on, kuidas kahesugune kirjutamine määrab, millisele omanikust töörühmale tuleks read määrata.</span><span class="sxs-lookup"><span data-stu-id="275e9-134">A final topic to discuss is how dual-write determines which owner team it should assign rows to.</span></span> <span data-ttu-id="275e9-135">Seda käitumist juhib veerg **Omanikust vaiketöörühm** real CDM\_Company.</span><span class="sxs-lookup"><span data-stu-id="275e9-135">This behavior is controlled by the **Default owning team** column on the cdm\_Company row.</span></span> <span data-ttu-id="275e9-136">Kui rida cdm\_Company on kahesuguseks kirjutamiseks lubatud, loob lisandmoodul automaatselt seostatud äriüksuse ja omaniktöörühma (kui seda veel pole) ja seadistab veeru **Omanikust vaiketöörühm**.</span><span class="sxs-lookup"><span data-stu-id="275e9-136">When a cdm\_Company row is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** column.</span></span> <span data-ttu-id="275e9-137">Administraator saab selle veeru muuta muuks väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="275e9-137">The admin can change this column to a different value.</span></span> <span data-ttu-id="275e9-138">Kuid administraator ei saa tühjendada veergu seni, kuni tabel on lubatud kahesuguseks kirjutamiseks.</span><span class="sxs-lookup"><span data-stu-id="275e9-138">However, the admin can't clear the column as long as the table is enabled for dual-write.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="275e9-139">![Omanikust vaiketöörühma veerg](media/dual-write-default-owning-team.jpg)</span><span class="sxs-lookup"><span data-stu-id="275e9-139">![Default owning team column](media/dual-write-default-owning-team.jpg)</span></span>

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="275e9-140">Ettevõtte segmentimine ja eellaadimine</span><span class="sxs-lookup"><span data-stu-id="275e9-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="275e9-141">Teenuse Dataverse integreerimine toob kaasa ettevõtte paarsuse, kasutades ettevõtte identifikaatorit andmete segmentimiseks.</span><span class="sxs-lookup"><span data-stu-id="275e9-141">Dataverse integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="275e9-142">Järgmine illustratsioon näitab, et kõik ettevõttekohased tabelid laiendatakse nii, et neil onleks mitu-ühele (N : 1) seos tabeliga CDM\_Company.</span><span class="sxs-lookup"><span data-stu-id="275e9-142">As the following illustration shows, all company-specific tables are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company table.</span></span>

> [!div class="mx-imgBorder"]
<span data-ttu-id="275e9-143">![Seos N : 1 ettevõttekohase tabeli ja tabeli cdm_Company vahel](media/dual-write-bootstrapping.png)</span><span class="sxs-lookup"><span data-stu-id="275e9-143">![N:1 relationship between a company-specific table and the cdm_Company table](media/dual-write-bootstrapping.png)</span></span>

+ <span data-ttu-id="275e9-144">Ridade puhul muutub väärtus pärast ettevõtte lisamist ja salvestamist kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="275e9-144">For rows, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="275e9-145">Seetõttu peaksid kasutajad veenduma, et nad valivad õige ettevõtte.</span><span class="sxs-lookup"><span data-stu-id="275e9-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="275e9-146">Ainult read, millel on ettevõtte andmed on kahesuguse kirjutamise õigused rakenduse ja teenuse Dataverse vahel.</span><span class="sxs-lookup"><span data-stu-id="275e9-146">Only rows that have company data are eligible for dual-write between the application and Dataverse.</span></span>
+ <span data-ttu-id="275e9-147">Teenuse Dataverse olemasolevate andmete puhul on peagi saadaval administraatori juhitav eellaadimine.</span><span class="sxs-lookup"><span data-stu-id="275e9-147">For existing Dataverse data, an admin-led bootstrapping experience will soon be available.</span></span>


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a><span data-ttu-id="275e9-148">Ettevõtte nime automaatne asustamine klientide kaasamise rakendustes</span><span class="sxs-lookup"><span data-stu-id="275e9-148">Autopopulate company name in customer engagement apps</span></span>

<span data-ttu-id="275e9-149">Ettevõtte nime automaatseks asustamiseks klientide kaasamise rakendustes on mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="275e9-149">There are several ways to auto-populate the company name in customer engagement apps.</span></span>

+ <span data-ttu-id="275e9-150">Kui olete süsteemiadministraator, saate määrata vaikeettevõtte , kui valite **Täpsemad sätted > Süsteem > Turve > Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="275e9-150">If you are a system administrator, you can set the default company by navigating to **Advanced Settings > System > Security > Users**.</span></span> <span data-ttu-id="275e9-151">Avage vorm **Kasutaja** ja määrake jaotises **Organisatsiooni andmed** väärtus **Ettevõtte vaikesätteks vormidel**.</span><span class="sxs-lookup"><span data-stu-id="275e9-151">Open the **User** form, and in the **Organization Information** section, set the **Company to default on Forms** value.</span></span>

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Vaikeettevõtte seadmine organisatsiooni andmete jaotises.":::

+ <span data-ttu-id="275e9-153">Kui teil on tasemel **Äriüksus** **Kirjutuspääs** tabelile **Süsteemikasutaja**, saate vaikeettevõtet muuta mistahes vormil, kui valite ettevõtte rippmenüüst **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="275e9-153">If you have **Write** access to the **SystemUser** table for the **Business Unit** level, then you can change the default company on any form by selecting a company from the **Company** drop-down menu.</span></span>

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Ettevõtte nime muutmine uuel kontol.":::

+ <span data-ttu-id="275e9-155">Kui teil on **Kirjutuspääs** rohkem kui ühe ettevõtte andmetele, saate vaikeettevõtet muuta, kui valite rea, mis kuulub muule ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="275e9-155">If you have **Write** access to data in more than one company, then you can change the default company by choosing a row that belongs to different company.</span></span>

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Rea valimine muudab vaikeettevõtet.":::

+ <span data-ttu-id="275e9-157">Kui olete süsteemikonfigureerija või -administraator, ja soovite kohandatud vormil automaatselt ettevõtte andmeid asustada, saate kasutada [vormisündmusi](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span><span class="sxs-lookup"><span data-stu-id="275e9-157">If you are a system configurator or administrator, and you want to auto-populate company data on a custom form, then you can use [form events](/powerapps/developer/model-driven-apps/clientapi/events-forms-grids).</span></span> <span data-ttu-id="275e9-158">Lisage JavaScripti viide failile **msdyn_/DefaultCompany.js** ja kasutage järgmisi sündmusi.</span><span class="sxs-lookup"><span data-stu-id="275e9-158">Add a JavaScript reference to **msdyn_/DefaultCompany.js** and use the following events.</span></span> <span data-ttu-id="275e9-159">Saate kasutada valmisvormi, näiteks vormi **Konto**.</span><span class="sxs-lookup"><span data-stu-id="275e9-159">You can use any out-of-the-box form, for example, the **Account** form.</span></span>

    + <span data-ttu-id="275e9-160">Vormi sündmus **OnLoad**: määrake veerg **defaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="275e9-160">**OnLoad** event for the form: Set the **defaultCompany** column.</span></span>
    + <span data-ttu-id="275e9-161">Veeru **Ettevõte** sündmus **OnChange**: määrake veerg **updateDefaultCompany**.</span><span class="sxs-lookup"><span data-stu-id="275e9-161">**OnChange** event for the **Company** column: Set the **updateDefaultCompany** column.</span></span>

## <a name="apply-filtering-based-on-the-company-context"></a><span data-ttu-id="275e9-162">Filtreerimise rakendamine ettevõtte konteksti põhjal</span><span class="sxs-lookup"><span data-stu-id="275e9-162">Apply filtering based on the company context</span></span>

<span data-ttu-id="275e9-163">Filtreerimise rakendamiseks ettevõtte konteksti põhjal kohandatud vormidele või standardvormidele lisatud otsinguveergudele avage vorm ja kasutage ettevõtte filtri rakendamiseks jaotist **Seotud kirjete filtreerimine**.</span><span class="sxs-lookup"><span data-stu-id="275e9-163">To apply filtering based on the company context on your custom forms or on custom lookup columns added to the standard forms, open the form and use the **Related Records Filtering** section to apply the company filter.</span></span> <span data-ttu-id="275e9-164">Selle peate määrama igale otsinguveerule, mis antud real nõuab filtreerimist aluseksoleva ettevõtte põhjal.</span><span class="sxs-lookup"><span data-stu-id="275e9-164">You must set this for each lookup column that requires filtering based on the underlying company on a given row.</span></span> <span data-ttu-id="275e9-165">Säte kuvatakse järgmisel joonisel suvandi **Konto** jaoks.</span><span class="sxs-lookup"><span data-stu-id="275e9-165">The setting is shown for **Account** in the following illustration.</span></span>

:::image type="content" source="media/apply-company-context.png" alt-text="Ettevõtte konteksti rakendamine":::



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]