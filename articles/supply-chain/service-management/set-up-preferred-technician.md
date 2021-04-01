---
title: Eelistatud tehniku seadistamine
description: Saate teenusleppe või teenuse tellimuse jaoks eelistatud tehnikuna valida mis tahes töötaja.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87b2554197c1963cdd7ba0871edb532661d10945
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256059"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="39b2c-103">Eelistatud tehniku seadistamine</span><span class="sxs-lookup"><span data-stu-id="39b2c-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="39b2c-104">Saate teenusleppe või teenuse tellimuse jaoks eelistatud tehnikuna valida mis tahes töötaja.</span><span class="sxs-lookup"><span data-stu-id="39b2c-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="39b2c-105">Siiski on hea mõte lisada töötaja sobivasse lähetustöörühma nii, et töötaja oleks loendis **Lähetustahvel**.</span><span class="sxs-lookup"><span data-stu-id="39b2c-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="39b2c-106">Töötaja lähetusmeeskonda määramine</span><span class="sxs-lookup"><span data-stu-id="39b2c-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="39b2c-107">Klõpsake valikuid **Inimressursid** \> **Üldine** \> **Töötajad** \> **Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="39b2c-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="39b2c-108">Topeltklõpsake töötajat tema üksikasjade lehe avamiseks.</span><span class="sxs-lookup"><span data-stu-id="39b2c-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="39b2c-109">**Toimingupaanil** klõpsake valikuid **Seadistamine** \>**Lähetustöörühm**, et avada vorm **Töötajate lähetamine**.</span><span class="sxs-lookup"><span data-stu-id="39b2c-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="39b2c-110">Väljal **Lähetustöörühm** valige töörühm, millesse tuleb töötaja määrata.</span><span class="sxs-lookup"><span data-stu-id="39b2c-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="39b2c-111">Eelistatud tehniku teenuseleppega töösse määramine</span><span class="sxs-lookup"><span data-stu-id="39b2c-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="39b2c-112">Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.</span><span class="sxs-lookup"><span data-stu-id="39b2c-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="39b2c-113">Topeltklõpsake teenuslepet, et avada üksikasjade vorm.</span><span class="sxs-lookup"><span data-stu-id="39b2c-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="39b2c-114">Vahekaardil **Üldine** valige väli **Eelistatud tehnik** ja valige sobiva lähetustöörühma liige teenuseleppe eelistatud tehnikuks.</span><span class="sxs-lookup"><span data-stu-id="39b2c-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="39b2c-115">Eelistatud tehniku teenusetellimusega töösse määramine</span><span class="sxs-lookup"><span data-stu-id="39b2c-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="39b2c-116">Klõpsake valikuid **Teenuste halduse** \> **Perioodiline** \> **Lähetustahvel**.</span><span class="sxs-lookup"><span data-stu-id="39b2c-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="39b2c-117">Vormil <STRONG>Lähetustahvel</STRONG> täpsustage lähetustegevuste kuupäevavahemik, mida soovite vaadata.</span><span class="sxs-lookup"><span data-stu-id="39b2c-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="39b2c-118">Samuti täpsustage, kas kuvada suletud tegevused ja kas piirata lähetustegevuste loendit meeskondadele, millesse te kuulute või mida teil on õigus jälgida.</span><span class="sxs-lookup"><span data-stu-id="39b2c-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="39b2c-119">Klõpsake nuppu <STRONG>OK</STRONG> vormi <STRONG>Lähetustahvel</STRONG> avamiseks.</span><span class="sxs-lookup"><span data-stu-id="39b2c-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="39b2c-120">Valige teenusetegevuse rida, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="39b2c-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="39b2c-121">Vahekaardil **Seotud** kasutage loendit **Töötaja**, et määrata sobiva lähetustöörühma liige teenuse osutamiseks eelistatud tehnikuks.</span><span class="sxs-lookup"><span data-stu-id="39b2c-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="39b2c-122">Vt ka</span><span class="sxs-lookup"><span data-stu-id="39b2c-122">See also</span></span>

[<span data-ttu-id="39b2c-123">Hoolduslepete arendamise ja loomise ülevaade</span><span class="sxs-lookup"><span data-stu-id="39b2c-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="39b2c-124">Hooldustellimuste loomine käsitsi</span><span class="sxs-lookup"><span data-stu-id="39b2c-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="39b2c-125">[Teenuseleping (vorm)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="39b2c-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]