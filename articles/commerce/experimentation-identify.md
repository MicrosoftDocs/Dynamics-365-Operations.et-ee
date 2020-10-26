---
title: Hüpoteesi tuvastamine ja eksperimendi mõõdikute määramine
description: Selles teemas kirjeldatakse, kuidas tuvastada hüpoteesi ja edumõõdikuid eksperimendi jaoks, mille te käivitate e-kaubanduse veebisaidil rakenduses Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 99642861d69b7545f03c6ed2c2650eadeb377534
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930178"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="c1746-103">Hüpoteesi tuvastamine ja eksperimendi edumõõdikute määramine</span><span class="sxs-lookup"><span data-stu-id="c1746-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="c1746-104">Eksperimenteerimise elutsükli esimene etapp hõlmab eksperimendi hüpoteesi ning jälgitavate mõõdikute määramist edukuse hindamiseks.</span><span class="sxs-lookup"><span data-stu-id="c1746-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="c1746-105">Järgmine diagramm näitab kõiki etappe, mis on seotud e-kaubanduse veebisaidi jaoks [eksperimendi seadistamise ja käivitamisega](experimentation-overview.md) rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c1746-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c1746-106">Täiendavad etapid on toodud eraldi teemades.</span><span class="sxs-lookup"><span data-stu-id="c1746-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="c1746-107">[ ![Eksperimendi kasutaja teekond – tuvastamine](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="c1746-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="c1746-108">Hüpotees on väide, millega te ennustate eksperimendi tulemust.</span><span class="sxs-lookup"><span data-stu-id="c1746-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="c1746-109">Hüpotees määratletakse mitme teguri põhjal, näiteks kasutajate käitumisega seotud andmed ja veebisaidi andmed, mille olete kogunud.</span><span class="sxs-lookup"><span data-stu-id="c1746-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="c1746-110">Hüpoteesiga määratlete oletuse või teooria, mida soovite oma eksperimendi abil kontrollida.</span><span class="sxs-lookup"><span data-stu-id="c1746-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="c1746-111">Eksperimendi hüpoteesi näide võib olla „*valge T-särgi pilt minu avalehel paneb inimesi suvekuudel rohkem klõpsama kui sinine kampsun, sest inimesed tahavad kanda suvel midagi kerget ja heledat*”.</span><span class="sxs-lookup"><span data-stu-id="c1746-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="c1746-112">Sellisel juhul loote variatsioonid, mis sisaldavad valget T-särki ja sinist kampsunit, ning avaldate mõlemad korraga.</span><span class="sxs-lookup"><span data-stu-id="c1746-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="c1746-113">Hüpoteesi kontrollimiseks peab eksperimendi edukus või nurjumine olema vahetult seotud kasutaja tegevusega; näiteks kui veebisaidi kasutaja klõpsab lingile või nupule.</span><span class="sxs-lookup"><span data-stu-id="c1746-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks a link or button.</span></span> <span data-ttu-id="c1746-114">Need toimingud peavad vastama sündmustele, mis edastatakse eksperimenti jälgivale kolmanda osapoole teenusele.</span><span class="sxs-lookup"><span data-stu-id="c1746-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="c1746-115">Aja jooksul muudetakse tegevust tegevate kasutajate protsent mõõdikuks, mida saate kasutada aruannete loomiseks ning analüüsimiseks.</span><span class="sxs-lookup"><span data-stu-id="c1746-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="c1746-116">Kõik saadaolevad sündmused ja atribuudid leiate teemast [Commerce'i komponentide sündmused diagnostika ja tõrkeotsingu jaoks](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="c1746-116">Refer to the [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md) topic to review all of the available events and attributes.</span></span>

## <a name="previous-step"></a><span data-ttu-id="c1746-117">Eelmine etapp</span><span class="sxs-lookup"><span data-stu-id="c1746-117">Previous step</span></span>
[<span data-ttu-id="c1746-118">Eksperimenteerimine rakenduses Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="c1746-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="c1746-119">Järgmine etapp</span><span class="sxs-lookup"><span data-stu-id="c1746-119">Next step</span></span>
[<span data-ttu-id="c1746-120">Eksperimendi seadistamine</span><span class="sxs-lookup"><span data-stu-id="c1746-120">Set up an experiment</span></span>](experimentation-setup.md)
