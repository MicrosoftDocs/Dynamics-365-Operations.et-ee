---
title: "Töövoos tingimusliku otsuse konfigureerimine"
description: "Kasutage järgmist protseduuri, et konfigureerida tingimusliku otsuse atribuudid."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="3ec4b-103">Töövoos tingimusliku otsuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3ec4b-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3ec4b-104">Kasutage järgmist protseduuri, et konfigureerida tingimusliku otsuse atribuudid.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="3ec4b-105">Tingimuslik otsus on punkt, milles töövoog jaguneb kaheks haruks.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="3ec4b-106">Töövoo redaktoris tingimusliku otsuse loomiseks paremklõpsake tingimuslikku otsust ja seejärel klõpsake valikut **Atribuudid**, et avada vorm **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="3ec4b-107">Otsusele nime andmine</span><span class="sxs-lookup"><span data-stu-id="3ec4b-107">Name a decision</span></span>
<span data-ttu-id="3ec4b-108">Tingimuslikule otsusele nime sisestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="3ec4b-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="3ec4b-110">Väljal **Nimi** sisestage tingimuslikule otsusele kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="3ec4b-111"> Tingimuste määramine</span><span class="sxs-lookup"><span data-stu-id="3ec4b-111">Set conditions</span></span>
<span data-ttu-id="3ec4b-112">Süsteem määrab, haru kasutada, hinnates edastatud dokumenti ja otsustades, kas see vastab kindlatele tingimustele.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="3ec4b-113">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="3ec4b-114">Klõpsake valikut **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="3ec4b-115">Sisestage tingimus.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-115">Enter a condition.</span></span>
4.  <span data-ttu-id="3ec4b-116">Sisestage lisatingimused, kui need on nõutavad.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="3ec4b-117">Kontrollimaks, kas teie sisestatud tingimused on õigesti konfigureeritud, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="3ec4b-118">Klõpsake valikut **Katseta**, et avada leht **Katseta töövoo tingimust**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="3ec4b-119">Valige vormi alal kirje **Kontrolli tingimust**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="3ec4b-120">Klõpsake nuppu **Test**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-120">Click **Test**.</span></span> <span data-ttu-id="3ec4b-121">Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="3ec4b-122">Klõpsake valikut **OK** või **Tühista**, et naasta vormile **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="3ec4b-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






