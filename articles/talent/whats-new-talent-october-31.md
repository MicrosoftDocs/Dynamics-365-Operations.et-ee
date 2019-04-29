---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (31. oktoober 2018)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talent Core HR-i uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d6942f8e4dc86f18a081b347df0567b1358a87ab
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "858786"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-31-2018"></a><span data-ttu-id="adb10-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (31. oktoober 2018)</span><span class="sxs-lookup"><span data-stu-id="adb10-103">What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="adb10-104">**Järk 8.1.2031**</span><span class="sxs-lookup"><span data-stu-id="adb10-104">**Build 8.1.2031**</span></span>

<span data-ttu-id="adb10-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="adb10-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="create-links-from-talent-to-finance-and-operations"></a><span data-ttu-id="adb10-106">Linkide loomine Talentist Finance and Operationsini</span><span class="sxs-lookup"><span data-stu-id="adb10-106">Create links from Talent to Finance and Operations</span></span>
<span data-ttu-id="adb10-107">See uus navigeerimisfunktsioon võimaldab teil linkida Talentist Finance Operationsini, pakkudes teile otsest navigeerimist Finance and Operations lehtedel.</span><span class="sxs-lookup"><span data-stu-id="adb10-107">This new navigation functionality allows you to link from Talent to Finance and Operations, giving you direct navigation into Finance and Operations pages.</span></span> <span data-ttu-id="adb10-108">Kui lingid on konfigureeritud, saate määratleda lingi nime ja grupi, kus link peaks rakenduses Talent asuma ja sihtlehe, mis peaks Finance and Operationsiga avanema.</span><span class="sxs-lookup"><span data-stu-id="adb10-108">When links are configured, you can specify the name and group of the link, where the link should surface in Talent, and the target page to be opened within Finance and Operations.</span></span>

#### <a name="coming-soon"></a><span data-ttu-id="adb10-109">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="adb10-109">Coming soon</span></span>
<span data-ttu-id="adb10-110">Tulevikus lisatakse välja kontekst, et võimaldada otsest navigeerimist Finance and Operations vastavatele kirjetele.</span><span class="sxs-lookup"><span data-stu-id="adb10-110">Field context will be added in the future to allow for direct navigation to corresponding records in Finance and Operations.</span></span> <span data-ttu-id="adb10-111">Näiteks saate kasutada **Lingi väljale**, et pakkuda konteksti, navigeerimaks otse konkreetse töövõtja või asukoha juurde Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="adb10-111">For example, you can use **Link to field** to provide the context to navigate directly to a specific employee or position in Finance and Operations.</span></span>

### <a name="configure-target-systems"></a><span data-ttu-id="adb10-112">Sihtsüsteemide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="adb10-112">Configure target systems</span></span>

<span data-ttu-id="adb10-113">Rakenduse Talent süsteemiadministraatoris saate määratleda lingid, mis ilmnevad läbi Süsteemiadministraatori tööruumi.</span><span class="sxs-lookup"><span data-stu-id="adb10-113">In Talent, system administrators can define links that will be surfaced through the System Administration workspace.</span></span> <span data-ttu-id="adb10-114">Konfiguratsiooni osaks on Finance and Operationsi keskkonnad, kuhu soovite kui lingi "sihtkohta" navigeerida.</span><span class="sxs-lookup"><span data-stu-id="adb10-114">Part of the configuration is the Finance and Operations environments that you would like to navigate to as the "target" of the link.</span></span> <span data-ttu-id="adb10-115">Saate seda teha, andes sihtsüsteemile nime ja Finance and Operationsi keskkonna URL-i.</span><span class="sxs-lookup"><span data-stu-id="adb10-115">You do this by giving the target system a name and providing the URL of the Finance and Operations environment.</span></span> <span data-ttu-id="adb10-116">Siin on näide antavast Finance and Operationsi URL-ist: https://devax00124aos.cloud.test.dynamics.com/.</span><span class="sxs-lookup"><span data-stu-id="adb10-116">Here is an example of a Finance and Operations URL that you would provide: https://devax00124aos.cloud.test.dynamics.com/.</span></span> <span data-ttu-id="adb10-117">Pärast oma sihtsüsteemi konfigureerimist saate määratleda oma lingid.</span><span class="sxs-lookup"><span data-stu-id="adb10-117">After you have configured your target systems,  you can define your links.</span></span>

### <a name="configure-links"></a><span data-ttu-id="adb10-118">Konfigureeri lingid</span><span class="sxs-lookup"><span data-stu-id="adb10-118">Configure links</span></span>

<span data-ttu-id="adb10-119">Iga loodud lingi kohta määratletakse järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="adb10-119">Each link that is created will have the following information defined.</span></span>

- <span data-ttu-id="adb10-120">Link – lingi nimi, mida kasutatakse ainult tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="adb10-120">Link - Name of the link, used for identification only.</span></span>

- <span data-ttu-id="adb10-121">Lingi lubamine – seatud olekusse **Jah**, kui soovite linki Talenti kasutajatele kuvada.</span><span class="sxs-lookup"><span data-stu-id="adb10-121">Enable this Link - Set to **Yes** if you want to display the link to users of Talent.</span></span>

- <span data-ttu-id="adb10-122">Kuvatav nimi – määratlege nimi, mis ilmub lingina Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="adb10-122">Display name - Define the name that will appear as a link to Finance and Operations.</span></span> <span data-ttu-id="adb10-123">Need andmed ei ole praegu tõlgitud.</span><span class="sxs-lookup"><span data-stu-id="adb10-123">This data is currently is not translated.</span></span>

- <span data-ttu-id="adb10-124">Lingi ilmutamise vorm – valige, missugusel lehel soovite linki kuvada.</span><span class="sxs-lookup"><span data-stu-id="adb10-124">Surface link on form - Choose which page you would like to display the link on.</span></span>

- <span data-ttu-id="adb10-125">Grupp – grupid ei ole kohustuslikud, kuid kui soovite linke gruppide abil korraldada, valige olemasolev grupp või looge uus, kasutades **Grupi** välja.</span><span class="sxs-lookup"><span data-stu-id="adb10-125">Group - Groups are not required, but if you want to organize your links using groups, select an existing group or create a new one using the **Group** field.</span></span>

- <span data-ttu-id="adb10-126">Sihtsüsteem – valige sihtsüsteem, mis loodi, kasutades **Sihtsüsteemi konfigureerimise** suvandit.</span><span class="sxs-lookup"><span data-stu-id="adb10-126">Target system - Select the target system that was created using the **Configure target system** option.</span></span> <span data-ttu-id="adb10-127">See saab olema Finance and Operationsi keskkond, mida kasutatakse lingiga navigeerides.</span><span class="sxs-lookup"><span data-stu-id="adb10-127">This will be the Finance and Operations environment that will be used when navigating by using the link.</span></span>

- <span data-ttu-id="adb10-128">Kasuta kasutaja praegust ettevõtet – valige **Jah**, kui soovite Finance and Operationsi navigeerimiesl kasutada kasutaja praeguse ettevõtte konteksti.</span><span class="sxs-lookup"><span data-stu-id="adb10-128">Use user's current Company - Select **Yes** if you would like to use the User's current company context when navigating to Finance and Operations.</span></span> <span data-ttu-id="adb10-129">Kui valitakse **Ei**, saate valida ettevõtte, mida tuleks kasutada.</span><span class="sxs-lookup"><span data-stu-id="adb10-129">If **No** is selected, then you can select the company that should be used.</span></span>

- <span data-ttu-id="adb10-130">Sihtmenüü käsk – sisestage Finance and Operationsi menüükäsk, mida link peab navigeerimisel kasutama.</span><span class="sxs-lookup"><span data-stu-id="adb10-130">Target menu item - Enter the menu item from Finance and Operation that the link should use when navigating.</span></span> <span data-ttu-id="adb10-131">Otse navigeeritavad menüü-üksused ei ole saadaval.</span><span class="sxs-lookup"><span data-stu-id="adb10-131">Menu items that you can directly navigate to are available.</span></span> <span data-ttu-id="adb10-132">Nõutava menüü-üksuse leidmiseks avage Finance and Operations ja avage navigeerimise sihtlehekülg.</span><span class="sxs-lookup"><span data-stu-id="adb10-132">To find the menu item required, open Finance and Operations and open the page that is the target of the navigation.</span></span> <span data-ttu-id="adb10-133">Kopeerige menüü-üksus URL-ist.</span><span class="sxs-lookup"><span data-stu-id="adb10-133">Copy the menu item from the URL.</span></span> <span data-ttu-id="adb10-134">Kui soovite näiteks, et link viiks teid töövõtjate loendisse Finance ja Operationsis, sisestage väärtus, mis kuvatakse URL-is pärast "&mi"-d.</span><span class="sxs-lookup"><span data-stu-id="adb10-134">For example, if you want the link to take you to the employee list in Finance and Operations, enter the value that appears after the "&mi" in the URL.</span></span> <span data-ttu-id="adb10-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="adb10-135">https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees.</span></span> <span data-ttu-id="adb10-136">Töövõtja loendi lehele navigeerimise menüü-üksus on selles näites: HcmWorkerListPage_Employees.</span><span class="sxs-lookup"><span data-stu-id="adb10-136">The menu item to navigate to the employee list page in this example is: HcmWorkerListPage_Employees.</span></span>

- <span data-ttu-id="adb10-137">Andmeallika link – valige andmeallikas, millele link viitab.</span><span class="sxs-lookup"><span data-stu-id="adb10-137">Link to data source - Select the source of data that the link is referencing.</span></span> <span data-ttu-id="adb10-138">Saadaval on kõige tavalisemad allikad nagu **Töötaja** ja **Ametikoht**.</span><span class="sxs-lookup"><span data-stu-id="adb10-138">The most common sources like **Worker** and **Position** are available.</span></span>

- <span data-ttu-id="adb10-139">Link väljale (tuleb varsti) – see välja valik võimaldab otsest navigeerimist üksikult kirjelt rakenduses Talent, üksikule kirjele rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="adb10-139">Link to field - (Coming soon) This field selection will allow for direct navigation from a single record in Talent to a single record in Finance and Operations.</span></span>

### <a name="access-to-links"></a><span data-ttu-id="adb10-140">Juurdepääs linkidele</span><span class="sxs-lookup"><span data-stu-id="adb10-140">Access to links</span></span>

<span data-ttu-id="adb10-141">Süsteemiadministraatorid näevad vastloodud linke määratletud lehtedel isegi siis, kui **Lingi lubamise** suvandiks on määratud **Ei**.</span><span class="sxs-lookup"><span data-stu-id="adb10-141">System administrators will see the newly created links on the defined pages even if the **Enable this link** option is set to **No**.</span></span> <span data-ttu-id="adb10-142">Seda saab kasutada linkide kontrollimiseks enne nende ilmutamist teistele töövõtjatele.</span><span class="sxs-lookup"><span data-stu-id="adb10-142">This can be used for testing links prior to surfacing them to other employees.</span></span> <span data-ttu-id="adb10-143">Kõik teised rollid näevad vaid konfigureeritud linke pärast seda, kui valiku **Lingi lubamise** suvandiks on määratud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="adb10-143">All other roles will only see the configured links after the **Enable this link** option is set to **Yes**.</span></span> <span data-ttu-id="adb10-144">Töövõtjatel, kellel on juurdepääs lehekülgedele, kuhu lingid on ilmutatud, on juurdepääs ka linkidele.</span><span class="sxs-lookup"><span data-stu-id="adb10-144">Employees who have access to the pages in which the links are surfaced will have access to the links.</span></span>

<span data-ttu-id="adb10-145">Kasutajatele võib ka rakenduses Finance and Operations määratleda turvaõigused, et pääseda ligi lehekülgedele Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="adb10-145">Users can also have security rights within Finance and Operations defined to access the pages in Finance and Operations.</span></span> <span data-ttu-id="adb10-146">Kui õiguseid ei ole, kuvatakse lingi kasutamisel turva dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="adb10-146">If they don't, a security dialog box will be displayed when using the link.</span></span>


## <a name="other-changesfixes"></a><span data-ttu-id="adb10-147">Muud muudatused/parandused</span><span class="sxs-lookup"><span data-stu-id="adb10-147">Other changes/fixes</span></span>

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a><span data-ttu-id="adb10-148">Uuele töövõtjale ei saa määrata ametikohti, mille alguskuupäev on tulevikus</span><span class="sxs-lookup"><span data-stu-id="adb10-148">Positions with a future start date cannot be assigned to a new employee</span></span>

<span data-ttu-id="adb10-149">Nüüd on võimalik määrata töövõtja ametikohale, mille alguskuupäev on tulevikus.</span><span class="sxs-lookup"><span data-stu-id="adb10-149">Changes have been made to allow employee assignments to future-dated positions.</span></span> <span data-ttu-id="adb10-150">Valida saab ametikohti, mille alguskuupäevad on tulevikus ja töövõtja määramine viiakse lõpule salvestamisel või töövoo lõpetamisel (kui töövoog on lubatud).</span><span class="sxs-lookup"><span data-stu-id="adb10-150">Positions that have start dates in the future can be selected and the employee assignment will be made upon save or completion of the workflow (if the workflow is enabled).</span></span>

### <a name="new-employee-cannot-be-assigned-existing-position"></a><span data-ttu-id="adb10-151">Uut töötajad ei saa olemasolevale ametikohale määrata</span><span class="sxs-lookup"><span data-stu-id="adb10-151">New employee cannot be assigned existing position</span></span>

<span data-ttu-id="adb10-152">Nüüd saab uusi töötajaid määrata olemasolevatele ametikohtadele.</span><span class="sxs-lookup"><span data-stu-id="adb10-152">Changes have been made so new employee assignment can now be assigned to existing positions.</span></span>

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a><span data-ttu-id="adb10-153">Staaži kuupäev / kontori asukoht kaovad, kui töösuhte alguskuupäev on minevikus ja kirje salvestatakse</span><span class="sxs-lookup"><span data-stu-id="adb10-153">Seniority date/Office location disappears when the employment start date is in the past and the record is saved</span></span>

<span data-ttu-id="adb10-154">Parandatud on **Staaži kuupäeva** ja **Kontori asukoha** nähtavust endiste töötajate muudatuste salvestamisel.</span><span class="sxs-lookup"><span data-stu-id="adb10-154">Changes have been made to correct the visibilty of the **Senority date** and **Office location** when saving changes for past employees.</span></span>

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a><span data-ttu-id="adb10-155">Ei saa sisestada andmeid tulevikus olevate töösuhete jaoks töötaja lehel</span><span class="sxs-lookup"><span data-stu-id="adb10-155">Can't enter data for future-dated employments on the worker page</span></span>

<span data-ttu-id="adb10-156">Tööhõiveandmed on tulevikus olevate töösuhete jaoks põhilisel töötaja lehel keelatud.</span><span class="sxs-lookup"><span data-stu-id="adb10-156">Employment data for future-dated employments has been disabled on the main worker page.</span></span> <span data-ttu-id="adb10-157">Tööhõiveandmeid saab sisestada **Kuupäevahalduri** lehekülgedelt.</span><span class="sxs-lookup"><span data-stu-id="adb10-157">Employment data can be entered through the **Date Manager** pages.</span></span> <span data-ttu-id="adb10-158">Tulevastes väljaannetes tehakse lisamuudatusi, et võimaldada tööhõiveandmete sisestamine töövoo protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="adb10-158">Additional changes will be made in future releases to enable entering employment data directly during the workflow process.</span></span>

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a><span data-ttu-id="adb10-159">Lisage ValidFrom ja ValidTo HcmPersonalContactPersonEntity</span><span class="sxs-lookup"><span data-stu-id="adb10-159">Add ValidFrom and ValidTo to HcmPersonalContactPersonEntity</span></span>

<span data-ttu-id="adb10-160">Andmehalduse raamistiku (DMF) üksus HcmPersonalContactPersonEntity on uuendatud ning sisaldab "kehtiv alates" ja "kehtiv kuni" kuupäevasid, et võimaldada teatud intgratsioonistsenaariumite soodustusi.</span><span class="sxs-lookup"><span data-stu-id="adb10-160">The Data Management Framework (DMF) entity HcmPersonalContactPersonEntity has been updated to include "valid from" and "valid to" dates to enable certain benefit integration scenarios.</span></span> 

## <a name="known-issue"></a><span data-ttu-id="adb10-161">Teadaolev probleem</span><span class="sxs-lookup"><span data-stu-id="adb10-161">Known issue</span></span>
- <span data-ttu-id="adb10-162">**Probleemi**: uuele töötajale seotuse lisamisel on nupud **Uus** ja **Redigeeri** hallid.</span><span class="sxs-lookup"><span data-stu-id="adb10-162">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="adb10-163">**Lahendus:** veenduge enne manuse lehe avamist, et **Töötaja** lehe kiirinfod oleksid suletud.</span><span class="sxs-lookup"><span data-stu-id="adb10-163">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="adb10-164">Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud.</span><span class="sxs-lookup"><span data-stu-id="adb10-164">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="adb10-165">(See probleem lahendatakse järgmisel platvormivärskendusel.)</span><span class="sxs-lookup"><span data-stu-id="adb10-165">(This issue will be fixed in the next platform update.)</span></span>
