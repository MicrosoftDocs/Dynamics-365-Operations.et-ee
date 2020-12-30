---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (15. november 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 11/15/2018
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
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1a7598db1dc4c11864cf5f5a73d00672ceb66e8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460918"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-november-15-2018"></a><span data-ttu-id="65118-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (15. november 2018)</span><span class="sxs-lookup"><span data-stu-id="65118-103">What's new or changed in Dynamics 365 Talent - Core HR (November 15, 2018)</span></span>

<span data-ttu-id="65118-104">**Järk 8.1.2045**</span><span class="sxs-lookup"><span data-stu-id="65118-104">**Build 8.1.2045**</span></span>

<span data-ttu-id="65118-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="65118-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="other-changesfixes"></a><span data-ttu-id="65118-106">Muud muudatused/parandused</span><span class="sxs-lookup"><span data-stu-id="65118-106">Other changes/fixes</span></span>

### <a name="unable-to-change-employees-current-position-to-a-future-open-position"></a><span data-ttu-id="65118-107">Töövõtja praegust ametikohta ei saa muuta tulevaseks vabaks ametikohaks</span><span class="sxs-lookup"><span data-stu-id="65118-107">Unable to change employee´s current position to a future open position</span></span>

<span data-ttu-id="65118-108">Tehti muudatus ametikoha üleviimise võimaldamiseks juhul, kui ametikoht on ainult tulevikus saadaval.</span><span class="sxs-lookup"><span data-stu-id="65118-108">A change has been made to enable position transfers when the position is only available in the future.</span></span> 

### <a name="position-does-not-display-when-creating-a-new-employee"></a><span data-ttu-id="65118-109">Töökohta ei kuvata uue töövõtja loomisel</span><span class="sxs-lookup"><span data-stu-id="65118-109">Position does not display when creating a new employee</span></span>

<span data-ttu-id="65118-110">Tehti muudatus kõigi vabade ametikohtade kuvamiseks, mis on Talentis uut töövõtjat värvates määramiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="65118-110">A change has been made to display all open positions that are available for assignment when hiring new employees in Talent.</span></span> <span data-ttu-id="65118-111">See hõlmab ajaloolisi positsioone või kui positsioonidel on tulevane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="65118-111">This includes historical positions or if the postitions have been future dated.</span></span> <span data-ttu-id="65118-112">Positsioonid ilmuvad nüüd õigesti töösuhte alguskuupäeva alusel.</span><span class="sxs-lookup"><span data-stu-id="65118-112">Positions will now appear correctly based on the employment start date.</span></span> 

### <a name="termination-date-is-displaying-based-on-user-settings"></a><span data-ttu-id="65118-113">Lõpetamise kuupäeva kuvatakse kasutajasätete alusel</span><span class="sxs-lookup"><span data-stu-id="65118-113">Termination date is displaying based on user settings</span></span>

<span data-ttu-id="65118-114">Tehti muudatus varasemate töövõtjate loendis töövõtja eelistatud ajavööndi korral ajavööndi nihete arvestamiseks töösuhte lõpetamise kuupäeva kuvamisel.</span><span class="sxs-lookup"><span data-stu-id="65118-114">A change has been made to the past employees list to account for any time zone offsets for the employees preferred time zone when viewing the termination date.</span></span>

### <a name="work-items-assigned-to-me-links-not-displaying-the-correct-information"></a><span data-ttu-id="65118-115">Mulle määratud tööüksused ei kuva õiget teavet</span><span class="sxs-lookup"><span data-stu-id="65118-115">Work items assigned to me links not displaying the correct information</span></span>

<span data-ttu-id="65118-116">Selle muudatusega saab kuvada valitud kauba jaoks õige teabe, kui navigeerida loendis üksikute tööüksuste üksikasjadele.</span><span class="sxs-lookup"><span data-stu-id="65118-116">With this change, navigation to the details of the individual work items in the list will display the correct information for the item selected.</span></span> <span data-ttu-id="65118-117">Probleem ilmnes ainult täpsemate turvasuvanditega.</span><span class="sxs-lookup"><span data-stu-id="65118-117">This issue only occurred with advanced security options.</span></span>


## <a name="known-issue"></a><span data-ttu-id="65118-118">Teadaolev probleem</span><span class="sxs-lookup"><span data-stu-id="65118-118">Known issue</span></span>

- <span data-ttu-id="65118-119">**Probleemi**: uuele töötajale seotuse lisamisel on nupud **Uus** ja **Redigeeri** hallid.</span><span class="sxs-lookup"><span data-stu-id="65118-119">**Issue**: When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out.</span></span> 
- <span data-ttu-id="65118-120">**Lahendus:** veenduge enne manuse lehe avamist, et **Töötaja** lehe kiirinfod oleksid suletud.</span><span class="sxs-lookup"><span data-stu-id="65118-120">**Workaround:** Before opening the attachment page, make sure that the FactBoxes on the **Worker** page are closed.</span></span> <span data-ttu-id="65118-121">Kui kiirinfod on lehe **Töötaja** laadimisel suletud, on manuste nupud lubatud.</span><span class="sxs-lookup"><span data-stu-id="65118-121">If the FactBoxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="65118-122">(See probleem lahendatakse järgmisel platvormivärskendusel.)</span><span class="sxs-lookup"><span data-stu-id="65118-122">(This issue will be fixed in the next platform update.)</span></span>
