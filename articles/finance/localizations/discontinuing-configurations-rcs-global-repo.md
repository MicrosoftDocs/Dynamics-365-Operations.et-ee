---
title: Katkesta konfiguratsioonid RCS-i globaalses hoidlas
description: See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018729"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="d0c2a-103">Katkesta konfiguratsioonid RCS-i globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="d0c2a-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0c2a-104">See teema kirjeldab, kuidas lõpetada konfiguratsioonid RCS-i globaalses hoidlas.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="d0c2a-105">Varem oli võimalik kustutada ainult need konfiguratsioonid, mida enam ei vajata.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="d0c2a-106">Nüüd saate väljastatud konfiguratsiooni RCS-i globaalses hoidlas märkida kui **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="d0c2a-107">Saate sellega ka hallata järgmisi funktsioone:</span><span class="sxs-lookup"><span data-stu-id="d0c2a-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="d0c2a-108">Esitage eelnevalt teatised, kui konfiguratsiooni konfigureerimine on kavandatud lõpetama.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="d0c2a-109">Kaasab asenduskonfiguratsioonile rakendatavad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="d0c2a-110">Seadistage **Toetatud kuni** konfiguratsiooni jaoks lõppkuupäev, et kasutajat teavitada selle lõpetamisest.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="d0c2a-111">Kui lõpetate konfiguratsiooniversiooni, saate määrata järgmise valikulise teabe:</span><span class="sxs-lookup"><span data-stu-id="d0c2a-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="d0c2a-112">**Asenduskonfiguratsioon**</span><span class="sxs-lookup"><span data-stu-id="d0c2a-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="d0c2a-113">**Asenduskonfiguratsiooni versioon**</span><span class="sxs-lookup"><span data-stu-id="d0c2a-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="d0c2a-114">**Vabas vormis märkus**: kasutage seda välja dokumentatsiooni linkide või viidete esitamiseks</span><span class="sxs-lookup"><span data-stu-id="d0c2a-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="d0c2a-115">**Toetatud kuni**: sellel väljal kuvatakse pakutav kuupäev, milleni praegust konfiguratsiooni/versiooni toetatakse.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="d0c2a-116">Seda kuupäeva tuleb käsitsi uuendada.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="d0c2a-117">Konfiguratsiooni katkestamiseks viige lõpule järgmised sammud.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="d0c2a-118">Valige, kas soovite ühe versiooni või kõigi sama sättega versioonide ühe operatsiooniga lõpetada, seades **Kõigi versioonide** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="d0c2a-119">Seadke **Katkestamise** parameetri väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="d0c2a-120">Konfiguratsioonide katkestamiseks valige **Ok**.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="d0c2a-121">Muudatuste salvestamisel täidetakse väli **Lõpetatud kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Katkesta konfiguratsiooniteave](media/Discontinue-details-2.png)
  
<span data-ttu-id="d0c2a-123">Saate konfiguratsiooni tagasi valida **Ühiskasutuses** või korrigeerida igal ajal oma teabe sisestamist.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="d0c2a-124">Kui jagate konfiguratsiooni, määrake kuupäev, **Toetatud kuni**, mis näitab kogu muu lepinguga seotud teavet ja teie tulevasi plaane.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="d0c2a-125">Kui soovite plaanitud katkestuse kohta teavet jagada, siis enne konfiguratsiooni tegeliku katkestamist saab kasutaja eeltäita kõik asendamisega seotud väljad, kuid jätta parameetri **Katkestamine** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="d0c2a-126">Lõpetamine ei piira konfiguratsioonidega toiminguid.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="d0c2a-127">Saate jätkata konfiguratsioonide importimist, käivitamist või tuletamist, kuid need väljad on informatiivsed.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="d0c2a-128">Finantsid toetavad selle teabe kuvamist alates versioonist 10.0.14</span><span class="sxs-lookup"><span data-stu-id="d0c2a-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="d0c2a-129">Alates versioonist 10.0.14 toetab Dynamics 365 Finance lõpetamisteabe kuvamist.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="d0c2a-130">Lehel **Globaalne hoidla** saate vaadata ajateavet, mis on seotud hiljutise teabega.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="d0c2a-131">Vaikimisi filtreeritakse välja enamjaolt konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="d0c2a-132">Lehel **Imporditud konfiguratsioonid** (ERSolutionTable) kuvatakse konfiguratsioonid, mis on impordi ajal juba lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="d0c2a-133">Nende konfiguratsioonide puhul, mis pärast importimist enam ei tööta, saab teabe sünkroonida, käivitades töö **Impordi konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d0c2a-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


