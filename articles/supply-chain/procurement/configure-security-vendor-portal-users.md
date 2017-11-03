---
title: Hankija portaali kasutajate turvalisus
description: "See artikkel selgitab, kuidas seadistada hankija portaali kasutavate väliste hankijate turvet. See teave kehtib ainult Dynamics AX-i 2016. aasta veebruari ja 2016. aasta mai versioonide puhul."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f79f686720d615da6996f854a9e4cc18f840337f
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="e8540-104">Hankija portaali kasutajate turvalisus</span><span class="sxs-lookup"><span data-stu-id="e8540-104">Vendor portal user security</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e8540-105">See artikkel selgitab, kuidas seadistada hankija portaali kasutavate väliste hankijate turvet.</span><span class="sxs-lookup"><span data-stu-id="e8540-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="e8540-106">See teave kehtib ainult Dynamics AX-i 2016. aasta veebruari ja 2016. aasta mai versioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="e8540-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="e8540-107">Hankija portaali funktsionaalsus on Dynamics 365 for Operationsi versioonis 1611 asendatud hankija koostöö laiendatud funktsionaalsusega.</span><span class="sxs-lookup"><span data-stu-id="e8540-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="e8540-108">Lisateavet hankija koostöö turvalisuse seadistamise kohta vt teemast [Hankija koostöö seadistamine ja haldamine](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="e8540-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="e8540-109">Hankija portaal näitab välishankijatele piiratud koguses teavet ostutellimuste (OT-d) kohta.</span><span class="sxs-lookup"><span data-stu-id="e8540-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="e8540-110">On oluline, et seadistate õigesti Microsoft Dynamics AX-i hankija portaali kasutajaõigused, nii et hankijatel ei ole soovimatut juurdepääsu teie Dynamics AX-i installi lisateabele.</span><span class="sxs-lookup"><span data-stu-id="e8540-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="e8540-111">**Oluline.** Erinevalt teistest kasutajatest ei peaks välishankijatel olema rolli **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="e8540-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="e8540-112">Roll **SystemUser** annab juurdepääsu privileegide kogumile, mis ei ole väliskasutajatele sobivad.</span><span class="sxs-lookup"><span data-stu-id="e8540-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="e8540-113">Hankija portaali kasutaja seadistamine</span><span class="sxs-lookup"><span data-stu-id="e8540-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="e8540-114">Enne kui loote kasutajakonto kellelegi, kes kasutab hankija portaali, peate seadistama hankija, et lubada hankija portaali koostöö.</span><span class="sxs-lookup"><span data-stu-id="e8540-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="e8540-115">Kasutage välja **Ostutellimuse koostöö** lehe **Hankijad** vahekaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="e8540-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="e8540-116">Välishankijatel, kes kasutavad hankija portaali, peab olema järgmine seaditus.</span><span class="sxs-lookup"><span data-stu-id="e8540-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="e8540-117">Microsoft Azure Active Directory (AAD) rakenduse kasutajakonto peab olema hankijale registreeritud Dynamics AX-i lehel **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="e8540-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="e8540-118">Hankijal peab olema turberoll **(Välis)hankija**, mitte roll **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="e8540-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="e8540-119">**Märkus.** Roll **SystemUser** antakse automaatselt, kui loote Dynamics AX-is uue kasutajakonto.</span><span class="sxs-lookup"><span data-stu-id="e8540-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="e8540-120">Seega peate selle rolli eemaldama ja kinnitama hoiatusteate, mille saate.</span><span class="sxs-lookup"><span data-stu-id="e8540-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="e8540-121">Hankija-kasutajale ei tohiks anda luba lisada täiendavaid välju ostutellimuse tabelitest oma ostutellimuse vaatesse.</span><span class="sxs-lookup"><span data-stu-id="e8540-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="e8540-122">Määrake vahekaardil **Isikupärastamine**, vahekaardil **Kasutajad** kasutaja suvand **Üksikasjalik isikupärastamine on lubatud** olekusse **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e8540-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="e8540-123">Kasutajakonto peab olema seostatud registreeritud kontaktisikuga.</span><span class="sxs-lookup"><span data-stu-id="e8540-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="e8540-124">Valige kontaktisik lehe **Kasutajad** väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="e8540-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="e8540-125">Valitud isikul peab olema asjakohase hankija jaoks olema roll **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="e8540-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="e8540-126">Kui sama isik taotleb mitme hankijakonto juurdepääsu hankija portaalile (võib-olla erinevatele juriidilistele isikutele), tuleb selle isiku iga kasutajakonto seostada sama registreeritud kontaktisikuga.</span><span class="sxs-lookup"><span data-stu-id="e8540-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="e8540-127">Roll **(Välis)hankija** hõlmab kõiki põhilisi võimalusi, mis on nõutavad hankija portaalis saadaolevate funktsioonide kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="e8540-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="e8540-128">See seadistus aitab tagada, et kasutajaliides, mida väliskasutaja näeb, keskendub ainult ettenähtud stsenaariumile.</span><span class="sxs-lookup"><span data-stu-id="e8540-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="e8540-129">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e8540-129">See also</span></span>
--------

[<span data-ttu-id="e8540-130">Hankija koostöö</span><span class="sxs-lookup"><span data-stu-id="e8540-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




