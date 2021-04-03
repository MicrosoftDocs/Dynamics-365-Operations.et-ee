---
title: Katkesta konfiguratsioonid RCS-i globaalses hoidlas
description: See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.
author: JaneA07
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 35d0af91161d898b09557a83913019609c71e836
ms.sourcegitcommit: e9d19f25e64cf4d1c1d07c8031a7081454a6f79e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/18/2021
ms.locfileid: "5474244"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="27a7f-103">Katkesta konfiguratsioonid RCS-i globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="27a7f-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27a7f-104">See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.</span><span class="sxs-lookup"><span data-stu-id="27a7f-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="27a7f-105">Varem oli võimalik kustutada ainult need konfiguratsioonid, mida enam ei vajata.</span><span class="sxs-lookup"><span data-stu-id="27a7f-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="27a7f-106">Nüüd saate väljastatud konfiguratsiooni RCS-i globaalses hoidlas märkida kui **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="27a7f-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="27a7f-107">Saate sellega ka hallata järgmisi funktsioone:</span><span class="sxs-lookup"><span data-stu-id="27a7f-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="27a7f-108">Esitage eelnevalt teatised, kui konfiguratsiooni konfigureerimine on kavandatud lõpetama.</span><span class="sxs-lookup"><span data-stu-id="27a7f-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="27a7f-109">Kaasab asenduskonfiguratsioonile rakendatavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="27a7f-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="27a7f-110">Seadistage **Toetatud kuni** konfiguratsiooni jaoks lõppkuupäev, et kasutajat teavitada selle lõpetamisest.</span><span class="sxs-lookup"><span data-stu-id="27a7f-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="27a7f-111">Kui lõpetate konfiguratsiooniversiooni, saate määrata järgmise valikulise teabe:</span><span class="sxs-lookup"><span data-stu-id="27a7f-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="27a7f-112">**Asenduskonfiguratsioon**</span><span class="sxs-lookup"><span data-stu-id="27a7f-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="27a7f-113">**Asenduskonfiguratsiooni versioon**</span><span class="sxs-lookup"><span data-stu-id="27a7f-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="27a7f-114">**Vabas vormis märkus**: kasutage seda välja dokumentatsiooni linkide või viidete esitamiseks</span><span class="sxs-lookup"><span data-stu-id="27a7f-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="27a7f-115">**Toetatud kuni**: sellel väljal kuvatakse pakutav kuupäev, milleni praegust konfiguratsiooni/versiooni toetatakse.</span><span class="sxs-lookup"><span data-stu-id="27a7f-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="27a7f-116">Seda kuupäeva tuleb käsitsi uuendada.</span><span class="sxs-lookup"><span data-stu-id="27a7f-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="27a7f-117">Konfiguratsiooni katkestamiseks viige lõpule järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="27a7f-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="27a7f-118">Valige, kas soovite ühe versiooni või kõigi sama sättega versioonide ühe operatsiooniga lõpetada, seades **Kõigi versioonide** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="27a7f-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="27a7f-119">Seadke **Katkestamise** parameetri väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="27a7f-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="27a7f-120">Konfiguratsioonide katkestamiseks valige **Ok**.</span><span class="sxs-lookup"><span data-stu-id="27a7f-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="27a7f-121">Muudatuste salvestamisel täidetakse väli **Lõpetatud kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="27a7f-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Katkesta konfiguratsiooniteave](media/Discontinue-details-2.png)
  
<span data-ttu-id="27a7f-123">Saate konfiguratsiooni tagasi valida **Ühiskasutuses** või korrigeerida igal ajal oma teabe sisestamist.</span><span class="sxs-lookup"><span data-stu-id="27a7f-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="27a7f-124">Kui jagate konfiguratsiooni, määrake kuupäev, **Toetatud kuni**, mis näitab kogu muu lepinguga seotud teavet ja teie tulevasi plaane.</span><span class="sxs-lookup"><span data-stu-id="27a7f-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="27a7f-125">Kui soovite plaanitud katkestuse kohta teavet jagada, siis enne konfiguratsiooni tegeliku katkestamist saab kasutaja eeltäita kõik asendamisega seotud väljad, kuid jätta parameetri **Katkestamine** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="27a7f-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="27a7f-126">Lõpetamine ei piira konfiguratsioonidega toiminguid.</span><span class="sxs-lookup"><span data-stu-id="27a7f-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="27a7f-127">Saate jätkata konfiguratsioonide importimist, käivitamist või tuletamist, kuid need väljad on informatiivsed.</span><span class="sxs-lookup"><span data-stu-id="27a7f-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="27a7f-128">Finantsid toetavad selle teabe kuvamist alates versioonist 10.0.14</span><span class="sxs-lookup"><span data-stu-id="27a7f-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="27a7f-129">Alates versioonist 10.0.14 toetab Dynamics 365 Finance lõpetamisteabe kuvamist.</span><span class="sxs-lookup"><span data-stu-id="27a7f-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="27a7f-130">Lehel **Globaalne hoidla** saate vaadata ajateavet, mis on seotud hiljutise teabega.</span><span class="sxs-lookup"><span data-stu-id="27a7f-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="27a7f-131">Vaikimisi filtreeritakse välja enamjaolt konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="27a7f-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="27a7f-132">Lehel **Imporditud konfiguratsioonid** (ERSolutionTable) kuvatakse konfiguratsioonid, mis on impordi ajal juba lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="27a7f-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="27a7f-133">Nende konfiguratsioonide puhul, mis pärast importimist enam ei tööta, saab teabe sünkroonida, käivitades töö **Impordi konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="27a7f-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


