---
title: Ühe kande KKK
description: Teemas on toodud vastused korduma kippuvatele küsimustele ühe kande funktsionaalsuse kohta. Ühe kandega finantstöölehtede jaoks (üldine tööleht, põhivara tööleht, hankija maksete tööleht jne) saate sisestada mitu alampearaamatu kannet ühes kandes.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 916f0172a2d7f9fad9dcd70b31f8ecf65e47b2c8
ms.sourcegitcommit: bd4763cc6088e114818e80bb1c27c6521b039743
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5107745"
---
# <a name="one-voucher-faq"></a><span data-ttu-id="52117-104">Ühe kande KKK</span><span class="sxs-lookup"><span data-stu-id="52117-104">One voucher FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52117-105">Teemas on toodud vastused korduma kippuvatele küsimustele ühe kande funktsionaalsuse kohta.</span><span class="sxs-lookup"><span data-stu-id="52117-105">This topic answers frequently asked questions about the One voucher functionality.</span></span> <span data-ttu-id="52117-106">Üks finantstöölehtede kanne võimaldab teil ühe kande kontekstis sisestada mitu alammooduli kannet.</span><span class="sxs-lookup"><span data-stu-id="52117-106">One voucher for financial journals lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="52117-107">Töölehed, mida saate kandesse kaasata, võivad muuhulgas olla pearaamatud, põhivara töölehed ja hankija makse töölehed.</span><span class="sxs-lookup"><span data-stu-id="52117-107">The journals that you can include in that voucher can be general journals, fixed asset journals, and vendor payment journals, among others.</span></span>

## <a name="when-will-the-one-voucher-functionality-be-deprecated"></a><span data-ttu-id="52117-108">Millal ühe kande funktsioon iganeb?</span><span class="sxs-lookup"><span data-stu-id="52117-108">When will the One voucher functionality be deprecated?</span></span>

<span data-ttu-id="52117-109">Kuigi Microsoft ei saa esitada täpset hinnangut selle kohta, millal ühe kande funktsioon iganeb, läheb igenemiseni tõenäoliselt veel vähemalt kaks aastat.</span><span class="sxs-lookup"><span data-stu-id="52117-109">Although Microsoft can't provide an accurate estimate about when the One voucher functionality will be deprecated, it will likely be at least two years before the deprecation occurs.</span></span>

<span data-ttu-id="52117-110">Nagu on märgitud ühes kande dokumentatsioonis, saab täita mitmeid ärinõudeid ainult ühe kande abil.</span><span class="sxs-lookup"><span data-stu-id="52117-110">As is noted in the One voucher documentation, numerous business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="52117-111">Microsoft peab tagama, et kõiki tuvastatud ärinõudeid saab süsteemis siiski täita pärast seda, kui funktsioon on iganenud.</span><span class="sxs-lookup"><span data-stu-id="52117-111">Microsoft must ensure that all the identified business requirements can still be met in the system after the functionality is deprecated.</span></span> <span data-ttu-id="52117-112">Seetõttu tuleb funktsioonivahede täitmiseks tõenäoliselt lisada uued funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="52117-112">Therefore, new features will probably have to be added to fill functional gaps.</span></span>

<span data-ttu-id="52117-113">Kui kõik funktsioonivahed on täidetud, teatab Microsoft, et funktsioon iganeb.</span><span class="sxs-lookup"><span data-stu-id="52117-113">After all functional gaps are filled, Microsoft will communicate that the feature will be deprecated.</span></span> <span data-ttu-id="52117-114">Kuid iganemine ei ole kehtiv vähemalt aasta jooksul pärast sellest teavitamist.</span><span class="sxs-lookup"><span data-stu-id="52117-114">However, the deprecation won't be effective for least one year after that communication.</span></span>

<span data-ttu-id="52117-115">Lisateavet leiate jaotisest [Ühe kande dokumentatsioon](one-voucher.md).</span><span class="sxs-lookup"><span data-stu-id="52117-115">For more information, see the [One voucher documentation](one-voucher.md).</span></span>

## <a name="what-will-the-solution-that-replaces-one-voucher-look-like"></a><span data-ttu-id="52117-116">Milline näeb välja lahendus, mis asendab ühe kande?</span><span class="sxs-lookup"><span data-stu-id="52117-116">What will the solution that replaces One voucher look like?</span></span>

<span data-ttu-id="52117-117">Microsoft ei saa pakkuda konkreetset lahendust, kuna iga funktsioonivahe on erinev ja seda tuleb hinnata ärinõuete alusel.</span><span class="sxs-lookup"><span data-stu-id="52117-117">Microsoft can't provide a specific solution, because each feature gap is different and must be evaluated based on the business requirements.</span></span> <span data-ttu-id="52117-118">Mõned funktsioonivahed asendatakse tõenäoliselt kindlatele ärinõuetele vastavate funktsioonidega.</span><span class="sxs-lookup"><span data-stu-id="52117-118">Some functional gaps will likely be replaced with features that help meet specific business requirements.</span></span> <span data-ttu-id="52117-119">Ülejäänud vahed võidakse siiski täita, jätkates töölehele sisestamise lubamist, nagu siis, kui kasutatakse üht kannet, kuid täiendades süsteemi, et jälgida üksikasju vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="52117-119">However, other gaps might be filled by continuing to allow for entry in a journal, as when One voucher is used, but enhancing the system to track more detail as required.</span></span>

## <a name="where-can-i-track-the-progress-of-the-feature-gaps-being-filled"></a><span data-ttu-id="52117-120">Kus saab jälgida täidetava funktsioonivahe edenemist?</span><span class="sxs-lookup"><span data-stu-id="52117-120">Where can I track the progress of the feature gaps being filled?</span></span>

<span data-ttu-id="52117-121">Nagu iga uue funktsiooni puhul, peavad kliendid vaatama väljalaske plaani ja "Mis on uut või muutunud" dokumentatsiooni.</span><span class="sxs-lookup"><span data-stu-id="52117-121">As for every new feature, customers must watch the Release plan and "What's new or changed" documentation.</span></span> <span data-ttu-id="52117-122">Iga funktsioon lisatakse nendele dokumentidele ja märkus näitab, et see funktsioon on vajalik selliste ärinõuete täitmiseks, mis nõudsid eelnevalt ühe kande funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="52117-122">Each feature will be added to these documents, and a note will indicate that the feature is required to meet a business requirement that previously required the One voucher functionality.</span></span>

## <a name="when-the-deprecation-date-is-identified-where-will-it-be-communicated"></a><span data-ttu-id="52117-123">Kui iganemiskuupäev on kindlaks määratud, kus sellest teavitatakse?</span><span class="sxs-lookup"><span data-stu-id="52117-123">When the deprecation date is identified, where will it be communicated?</span></span>

<span data-ttu-id="52117-124">Ühe kande iganemine on oluline muudatus, millest teavitatakse laialdaselt.</span><span class="sxs-lookup"><span data-stu-id="52117-124">The deprecation of One voucher is a significant change that will be widely communicated.</span></span> <span data-ttu-id="52117-125">Sellest teavitatakse tootedokumentatsioonis, blogipostituste ja teadete kaudu vastavatel Microsofti konverentsidel palju enne tegelikku iganemise kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="52117-125">It will be communicated through the product documentation, a blog post, and announcements at applicable Microsoft conferences, well in advance of the date when the deprecation takes effect.</span></span>
