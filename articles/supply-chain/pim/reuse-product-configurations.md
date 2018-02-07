---
title: Tootekonfiguratsioonide taaskasutamine
description: "Soovi korral saate määrata toote olemasoleva konfiguratsiooni automaatse taaskasutamise. Seejärel, kui kasutaja on konfiguratsiooniseansi lõpule viinud, kontrollib süsteem, kas kasutaja valikule vastav konfiguratsioon on juba olemas. Vastava konfiguratsiooni leidmisel kasutatakse konfiguratsiooni ID-d, vastavat kooslust ja protsessi uuesti."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: c447440c33c1f80c6056974086b90d3b43e8499e
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="reuse-product-configurations"></a><span data-ttu-id="068e6-105">Tootekonfiguratsioonide taaskasutamine</span><span class="sxs-lookup"><span data-stu-id="068e6-105">Reuse product configurations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="068e6-106">Soovi korral saate määrata toote olemasoleva konfiguratsiooni automaatse taaskasutamise.</span><span class="sxs-lookup"><span data-stu-id="068e6-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="068e6-107">Seejärel, kui kasutaja on konfiguratsiooniseansi lõpule viinud, kontrollib süsteem, kas kasutaja valikule vastav konfiguratsioon on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="068e6-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="068e6-108">Vastava konfiguratsiooni leidmisel kasutatakse konfiguratsiooni ID-d, vastavat kooslust ja protsessi uuesti.</span><span class="sxs-lookup"><span data-stu-id="068e6-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="068e6-109">Konfiguratsioonide taaskasutuse nõuded</span><span class="sxs-lookup"><span data-stu-id="068e6-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="068e6-110">Konfiguratsioonide taaskasutamise lubamiseks peate määrama lehel **Tootekonfiguratsiooni mudeli üksikasjad**komponentidele ja atribuutidele järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="068e6-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="068e6-111">**Komponendid ja alamkomponendid** – valige kiirkaardi **Üldine** väljal **Taaskasuta konfiguratsioone** suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="068e6-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="068e6-112">**Atribuudid** – valige kiirkaardil **Atribuudid** suvand **Lisa taaskasutusse**.</span><span class="sxs-lookup"><span data-stu-id="068e6-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="068e6-113">See suvand kuvatakse ainult siis, kui seotud komponendi taaskasutamine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="068e6-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="068e6-114">Kui te ei vali taaskasutamiseks ühtki atribuuti, kasutatakse konfiguratsiooni alati uuesti, olenemata kasutaja valikutest konfigureerimisseansi ajal.</span><span class="sxs-lookup"><span data-stu-id="068e6-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="068e6-115">Olemasoleva konfiguratsiooni atribuutide väärtused peavad ühtima kasutaja valikutega.</span><span class="sxs-lookup"><span data-stu-id="068e6-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="068e6-116">Näiteks kui kasutaja valib konfiguratsiooniseansi ajal värviks **Sinine**, kontrollib süsteem, kas komponendi olemasolevas konfiguratsioonis on värv sinine.</span><span class="sxs-lookup"><span data-stu-id="068e6-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="068e6-117">Konfiguratsiooni taaskasutuse lähestamine</span><span class="sxs-lookup"><span data-stu-id="068e6-117">Resetting configuration reuse</span></span>
<span data-ttu-id="068e6-118">Konfiguratsiooni taaskasutuse lähtestamisel ei võeta varem loodud konfiguratsioone arvesse.</span><span class="sxs-lookup"><span data-stu-id="068e6-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="068e6-119">Soovi korral saate konfiguratsiooni taaskasutuse lähtestada, kui kooslust või protsessi on muudetud, kuid seotud atribuute mitte.</span><span class="sxs-lookup"><span data-stu-id="068e6-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="068e6-120">Saate lähtestada konfiguratsiooni taaskasutuse komponendi kiirkaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="068e6-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>




