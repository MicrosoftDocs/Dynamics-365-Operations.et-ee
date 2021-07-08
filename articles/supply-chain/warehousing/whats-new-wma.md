---
title: Mis on uut või muudetud Warehouse Management laohalduse mobiilirakenduses
description: Selles teemas loetletakse Microsoft Dynamics 365 Supply Chain Management iga Warehouse Management mobiilirakenduse väljastatud versiooni uued ja muudetud funktsioonid.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261772"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="6f0bf-103">Mis on uut või muudetud Warehouse Management laohalduse mobiilirakenduses</span><span class="sxs-lookup"><span data-stu-id="6f0bf-103">What's new or changed in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f0bf-104">Selles teemas loetletakse Microsoft Dynamics 365 Supply Chain Management iga Warehouse Management mobiilirakenduse väljastatud versiooni uued funktsioonid, parandused, täiustused ja teadaolevad vead.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-104">This topic lists new features, fixes, improvements, and known issues for each released version of the Warehouse Management mobile app for Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="version-2060"></a><span data-ttu-id="6f0bf-105">Versioon 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="6f0bf-105">Version 2.0.6.0</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2060"></a><span data-ttu-id="6f0bf-106">Uued funktsioonid, parandused ja täiustused versioonis 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="6f0bf-106">New features, fixes, and improvements in version 2.0.6.0</span></span>

<span data-ttu-id="6f0bf-107">See versioon tutvustab järgmisi uusi funktsioone, parandusi ja täiustusi:</span><span class="sxs-lookup"><span data-stu-id="6f0bf-107">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="6f0bf-108">Demorežiim kuvab nüüd kõik sildid seadme keeles.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-108">Demo mode now shows all labels in the device language.</span></span>
- <span data-ttu-id="6f0bf-109">Vähem tõenäoline, et saate järgmise tõrketeate: "Määratud suuruse jaoks ei leia sobivat vaadet."</span><span class="sxs-lookup"><span data-stu-id="6f0bf-109">You're less likely to receive the following error message: "Cannot find a suitable view for the specified size."</span></span>
- <span data-ttu-id="6f0bf-110">Töökaartide minimaalne kõrgus on suurenenud (juhul, kui tööloendis on konfigureeritud kolm või vähem välju).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-110">The minimum height for work cards has been increased (for cases where three or fewer fields are configured to appear in the work list).</span></span>
- <span data-ttu-id="6f0bf-111">Üksikasjade kaartide allosas on veerised (fade out) parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-111">Margins (fade out) at the bottom of details cards have been improved.</span></span>
- <span data-ttu-id="6f0bf-112">Serveriga vahetatud XML-failide kehtetuid sümboleid käsitsetakse nüüd graatsiliselt.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-112">Invalid symbols in XML files that are exchanged with the server are now handled gracefully.</span></span> <span data-ttu-id="6f0bf-113">(Näiteks mitteprinditavaid tähemärke käsitsetakse nüüd graafiliselt ega põhjusta enam rakenduse hangumist.)</span><span class="sxs-lookup"><span data-stu-id="6f0bf-113">(For example, non-printable characters are now handled gracefully and no longer cause the app to stop responding.)</span></span>
- <span data-ttu-id="6f0bf-114">HTTP-tõrkeid (nt "tõrge 503") serveri nõude esitamise korral käsitsetakse nüüd graatsiliselt.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-114">HTTP errors (such as "error 503") when a server request is submitted are now handled gracefully.</span></span>
- <span data-ttu-id="6f0bf-115">Tõrke kuvamisel ei kuvata valikute loendit enam liitboksi juhtelementide puhul automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-115">While an error is being shown, the options list is no longer automatically shown for combo box controls.</span></span>
- <span data-ttu-id="6f0bf-116">Rakendus ei lõpeta enam vastamist kasutaja sätetes valitud kuvapaigutuse tõttu.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-116">The app no longer stops responding because of the display orientation that is selected in user settings.</span></span>
- <span data-ttu-id="6f0bf-117">Tootepilti näidatakse nüüd iseteeninduskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-117">Product images are now shown in self-service environments.</span></span> <span data-ttu-id="6f0bf-118">(See muudatus rakendub ainult madala resolutsiooniga versioonidele.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-118">(This change applies to low-resolution versions only.</span></span> <span data-ttu-id="6f0bf-119">Failihalduse teenus ei toeta täissuurusega pilte iseteeninduskeskkonnas.)</span><span class="sxs-lookup"><span data-stu-id="6f0bf-119">The file management service doesn't support full-sized images in self-service environments.)</span></span>
- <span data-ttu-id="6f0bf-120">Probleem, mis hõlmas nullkoguse lühikesi valikuid on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-120">An issue that involved zero-quantity short picks has been fixed.</span></span>
- <span data-ttu-id="6f0bf-121">Rakendus ei hangu enam, kui üksikasjakaart näitab mitut identset välja.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-121">The app no longer stops responding when a details card shows multiple identical fields.</span></span>

### <a name="known-issues-in-version-2060"></a><span data-ttu-id="6f0bf-122">Teadaolevad probleemid versioonis 2.0.6.0</span><span class="sxs-lookup"><span data-stu-id="6f0bf-122">Known issues in version 2.0.6.0</span></span>

<span data-ttu-id="6f0bf-123">Selles versioonis on järgmised teadaolevad probleemid.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-123">The following known issues exist in this version:</span></span>

- <span data-ttu-id="6f0bf-124">Rakendus (eriti tööloend) muutub aja jooksul aeglasemaks.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-124">The app (especially the work list) becomes slower over time.</span></span>
- <span data-ttu-id="6f0bf-125">**Windowsi versioon:** kui USB-vidinat kasutatakse Windowsi skannimiseks, põhjustavad ebaühtlased tulemused skannitud sümbolite sassimineku.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-125">**Windows version:** When a USB gun is used for scanning on Windows, inconsistent results cause scanned symbols to be mixed up.</span></span>

## <a name="version-2050"></a><span data-ttu-id="6f0bf-126">Versioon 2.0.5.0</span><span class="sxs-lookup"><span data-stu-id="6f0bf-126">Version 2.0.5.0</span></span>

<span data-ttu-id="6f0bf-127">See versioon tutvustab järgmisi uusi funktsioone, parandusi ja täiustusi:</span><span class="sxs-lookup"><span data-stu-id="6f0bf-127">This version introduces the following new features, fixes, and improvements:</span></span>

- <span data-ttu-id="6f0bf-128">Kliendi saladus ei ole enam ühenduse sätete häälestamises peidetud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-128">The client secret is no longer hidden in the connection settings setup.</span></span>
- <span data-ttu-id="6f0bf-129">Selle täielikuks nägemiseks võite nüüd teksti pikalt vajutada.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-129">You can now long-press on any text to see it fully.</span></span>
- <span data-ttu-id="6f0bf-130">Veateade, kui ladustamiõigused puuduvad, on täiustatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-130">The error message when storage permissions are missing has been improved.</span></span>
- <span data-ttu-id="6f0bf-131">Teatud voogude jaoks on lisatud uued kontrolliseeriad.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-131">New control sequences have been added for some flows.</span></span>
- <span data-ttu-id="6f0bf-132">Edastamisnupp ei muutu enam akna suuruse tõttu kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-132">The submit button no longer incorrectly becomes available because of the window size.</span></span>
- <span data-ttu-id="6f0bf-133">Suuremate nuppude kasutamisel saavad liugurid väiksematele ekraanidele edasi minna.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-133">Sliders can now proceed on smaller screens when larger button sizes are used.</span></span>
- <span data-ttu-id="6f0bf-134">Nelja nupuga ülekatet ei katkestata enam.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-134">The four-button overlay is no longer cut off.</span></span>
- <span data-ttu-id="6f0bf-135">Klaviatuur toetab nüüd kustutusnuppu.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-135">The keyboard now supports the delete button.</span></span>
- <span data-ttu-id="6f0bf-136">Ereduse probleem, mis võib tekkida klaviatuuri klahvi vajutamisel, on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-136">A brightness issue that could occur when the keyboard is pressed has been fixed.</span></span>
- <span data-ttu-id="6f0bf-137">Mitmed demoandmete probleemid on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-137">Various demo data issues have been fixed.</span></span>
- <span data-ttu-id="6f0bf-138">Probleem, mis mõjutas numbrivälju üksikasjade lehel, on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-138">An issue that affected numeric fields on the details page has been fixed.</span></span>
- <span data-ttu-id="6f0bf-139">Ekraani klaviatuur aeg-ajalt mõnes seadmes enam ei kao.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-139">The screen keyboard no longer occasionally disappears on some devices.</span></span>
- <span data-ttu-id="6f0bf-140">Erinevad kasutajaliidese (UI) vead on fikseeritud, nt vead, mis mõjutasid taustavärvi ja paigutamist.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-140">Various user interface (UI) bugs have been fixed, such as bugs that affected the background color and positioning.</span></span>
- <span data-ttu-id="6f0bf-141">Venekeelne kasutajaliides on täiustatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-141">The Russian-language UI has been improved.</span></span>
- <span data-ttu-id="6f0bf-142">Mitmed probleemid, mis põhjustasid süsteemi hangumise, on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-142">Various issues that caused the system to stop responding have been fixed.</span></span>
- <span data-ttu-id="6f0bf-143">Kalkulaatori taasavamisega seotud probleem on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-143">An issue that was related to reopening the calculator has been fixed.</span></span>
- <span data-ttu-id="6f0bf-144">**Android versioon:** probleem, mis põhjustas Android 4.4 hangumise, on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-144">**Android version:** An issue that caused Android 4.4 to stop responding on startup has been fixed.</span></span>
- <span data-ttu-id="6f0bf-145">**Android versioon:** minimaalset skaleerimist on vähendatud 50 protsendini.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-145">**Android version:** Minimum scaling has been reduced to 50 percent.</span></span>

## <a name="version-2040"></a><span data-ttu-id="6f0bf-146">Versioon 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="6f0bf-146">Version 2.0.4.0</span></span>

<span data-ttu-id="6f0bf-147">Versiooni 2.0.4.0 oli Warehouse Management laohalduse mobiilirakenduse esimene üldiselt saadaolev väljaanne.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-147">Version 2.0.4.0 was the first generally available release of the Warehouse Management mobile app.</span></span>

### <a name="new-features-fixes-and-improvements-in-version-2040"></a><span data-ttu-id="6f0bf-148">Uued funktsioonid, parandused ja täiustused versioonis 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="6f0bf-148">New features, fixes, and improvements in version 2.0.4.0</span></span>

<span data-ttu-id="6f0bf-149">See versioon sisaldab järgmisi uusi funktsioone, parandusi ja täiustusi, mis polnud eelvaate versioonis saadaval.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-149">This version introduces the following new features, fixes, and improvements that weren't available in the preview version:</span></span>

- <span data-ttu-id="6f0bf-150">Kui üksikasjade kaart sisaldab kahte sama andmesildiga silti, on üks siltidest peidetud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-150">If a details card includes two labels that have identical data, one of the labels is hidden.</span></span>
- <span data-ttu-id="6f0bf-151">Erimärgid on nüüd vaikimisi kuvatud ja nende peitmise suvand on kasutaja sätetest eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-151">Special characters are now shown by default, and the option to hide them has been removed from user settings.</span></span>
- <span data-ttu-id="6f0bf-152">Keelatud esitamisnupud kuvatakse nüüd kompaktses käeshoitavas vaates kättesaamatuna.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-152">Disabled submit buttons are now shown as unavailable in compact arm-held view.</span></span>
- <span data-ttu-id="6f0bf-153">Juhtimisseadmete järjestuse loogika muutmine tagab sujuvama skaleerimise seadmete vahel.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-153">A change to the sequencing logic for controls ensures smoother scaling across devices.</span></span> <span data-ttu-id="6f0bf-154">Seega on vaja fontide või nuppude taastmist vähem korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-154">Therefore, there is less need to adjust the scaling of fonts or buttons.</span></span>
- <span data-ttu-id="6f0bf-155">Värvi vaikekujundus on muudetud *Tumedaks*.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-155">The default color theme has been changed to *Dark*.</span></span>
- <span data-ttu-id="6f0bf-156">Lindivaatesse on lisatud keelatud edastamisnupu puuduv ikoon.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-156">The missing icon for the disabled submit button has been added in ribbon view.</span></span>
- <span data-ttu-id="6f0bf-157">Aegunud erandid viivad teid nüüd ühenduse lehele, selle asemel et kuvada viga real.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-157">Time-out exceptions now take you to the connection page instead of showing an in-line error.</span></span>
- <span data-ttu-id="6f0bf-158">Kui ühtegi edastamistegevust pole saadaval (nt **OK**, **Jah**, **Aktsepteeri**, **Valmis** või **Lõpetatud**), siis edastamise nupp on keelatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-158">If no submit action is available (such as **OK**, **Yes**, **Accept**, **Done**, or **Finished**), the submit button will be disabled.</span></span>
- <span data-ttu-id="6f0bf-159">Rakenduse stabiilsust on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-159">App stability has been improved.</span></span>
- <span data-ttu-id="6f0bf-160">Turvalisuse ületuskontrolli [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-160">There is a fix for security vulnerability [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).</span></span>
- <span data-ttu-id="6f0bf-161">**Windowsi versioon:** Windowsi probleem, kus menüüd ei reageerinud pärast akna suuruse muutust, on parandatud.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-161">**Windows version:** An issue on Windows, where menus were unresponsive after the window was resized, has been fixed.</span></span>

### <a name="known-issue-in-version-2040"></a><span data-ttu-id="6f0bf-162">Teadaolev probleem versioonis 2.0.4.0</span><span class="sxs-lookup"><span data-stu-id="6f0bf-162">Known issue in version 2.0.4.0</span></span>

<span data-ttu-id="6f0bf-163">Selles versioonis on järgmine teadaolev probleem:</span><span class="sxs-lookup"><span data-stu-id="6f0bf-163">The following known issue exists in this version:</span></span>

- <span data-ttu-id="6f0bf-164">Sellel versioonil on probleem seadmetega, mis kasutavad Androidi versiooni 4.4.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-164">This version has an issue with devices that use Android 4.4.</span></span> <span data-ttu-id="6f0bf-165">Rakenduse kasutamisel võib sellel Androidi versioonil tekkida probleeme.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-165">You might experience issues when you use the app on this Android version.</span></span>
