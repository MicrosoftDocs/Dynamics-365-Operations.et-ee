---
title: Katkesta konfiguratsioonid RCS-i globaalses hoidlas
description: See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.
author: JaneA07
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
ms.openlocfilehash: 25ad0744e7c3320505c13c465d440b6a364da47c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840288"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="78056-103">Katkesta konfiguratsioonid RCS-i globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="78056-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78056-104">See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.</span><span class="sxs-lookup"><span data-stu-id="78056-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="78056-105">Varem oli võimalik kustutada ainult need konfiguratsioonid, mida enam ei vajata.</span><span class="sxs-lookup"><span data-stu-id="78056-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="78056-106">Nüüd saate väljastatud konfiguratsiooni RCS-i globaalses hoidlas märkida kui **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="78056-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="78056-107">Saate sellega ka hallata järgmisi funktsioone:</span><span class="sxs-lookup"><span data-stu-id="78056-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="78056-108">Esitage eelnevalt teatised, kui konfiguratsiooni konfigureerimine on kavandatud lõpetama.</span><span class="sxs-lookup"><span data-stu-id="78056-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="78056-109">Kaasab asenduskonfiguratsioonile rakendatavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="78056-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="78056-110">Seadistage **Toetatud kuni** konfiguratsiooni jaoks lõppkuupäev, et kasutajat teavitada selle lõpetamisest.</span><span class="sxs-lookup"><span data-stu-id="78056-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="78056-111">Kui lõpetate konfiguratsiooniversiooni, saate määrata järgmise valikulise teabe:</span><span class="sxs-lookup"><span data-stu-id="78056-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="78056-112">**Asenduskonfiguratsioon**</span><span class="sxs-lookup"><span data-stu-id="78056-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="78056-113">**Asenduskonfiguratsiooni versioon**</span><span class="sxs-lookup"><span data-stu-id="78056-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="78056-114">**Vabas vormis märkus**: kasutage seda välja dokumentatsiooni linkide või viidete esitamiseks</span><span class="sxs-lookup"><span data-stu-id="78056-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="78056-115">**Toetatud kuni**: sellel väljal kuvatakse pakutav kuupäev, milleni praegust konfiguratsiooni/versiooni toetatakse.</span><span class="sxs-lookup"><span data-stu-id="78056-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="78056-116">Seda kuupäeva tuleb käsitsi uuendada.</span><span class="sxs-lookup"><span data-stu-id="78056-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="78056-117">Konfiguratsiooni katkestamiseks viige lõpule järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="78056-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="78056-118">Valige, kas soovite ühe versiooni või kõigi sama sättega versioonide ühe operatsiooniga lõpetada, seades **Kõigi versioonide** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="78056-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="78056-119">Seadke **Katkestamise** parameetri väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="78056-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="78056-120">Konfiguratsioonide katkestamiseks valige **Ok**.</span><span class="sxs-lookup"><span data-stu-id="78056-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="78056-121">Muudatuste salvestamisel täidetakse väli **Lõpetatud kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="78056-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Katkesta konfiguratsiooniteave](media/Discontinue-details-2.png)
  
<span data-ttu-id="78056-123">Saate konfiguratsiooni tagasi valida **Ühiskasutuses** või korrigeerida igal ajal oma teabe sisestamist.</span><span class="sxs-lookup"><span data-stu-id="78056-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="78056-124">Kui jagate konfiguratsiooni, määrake kuupäev, **Toetatud kuni**, mis näitab kogu muu lepinguga seotud teavet ja teie tulevasi plaane.</span><span class="sxs-lookup"><span data-stu-id="78056-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="78056-125">Kui soovite plaanitud katkestuse kohta teavet jagada, siis enne konfiguratsiooni tegeliku katkestamist saab kasutaja eeltäita kõik asendamisega seotud väljad, kuid jätta parameetri **Katkestamine** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="78056-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="78056-126">Lõpetamine ei piira konfiguratsioonidega toiminguid.</span><span class="sxs-lookup"><span data-stu-id="78056-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="78056-127">Saate jätkata konfiguratsioonide importimist, käivitamist või tuletamist, kuid need väljad on informatiivsed.</span><span class="sxs-lookup"><span data-stu-id="78056-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="78056-128">Finantsid toetavad selle teabe kuvamist alates versioonist 10.0.14</span><span class="sxs-lookup"><span data-stu-id="78056-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="78056-129">Alates versioonist 10.0.14 toetab Dynamics 365 Finance lõpetamisteabe kuvamist.</span><span class="sxs-lookup"><span data-stu-id="78056-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="78056-130">Lehel **Globaalne hoidla** saate vaadata ajateavet, mis on seotud hiljutise teabega.</span><span class="sxs-lookup"><span data-stu-id="78056-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="78056-131">Vaikimisi filtreeritakse välja enamjaolt konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="78056-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="78056-132">Lehel **Imporditud konfiguratsioonid** (ERSolutionTable) kuvatakse konfiguratsioonid, mis on impordi ajal juba lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="78056-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="78056-133">Nende konfiguratsioonide puhul, mis pärast importimist enam ei tööta, saab teabe sünkroonida, käivitades töö **Impordi konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="78056-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


