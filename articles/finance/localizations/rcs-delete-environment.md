---
title: Regulatory Configuration Service (RCS) – RCS-keskkonna kustutamine
description: See teema kirjeldab, kuidas Regulatory Configuration Service (RCS) teenuse süsteemi administraator saab kustutada RCS-keskkonda ja seotud andmeid.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295814"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="2e5f0-103">Regulatory Configuration Service (RCS) – RCS-keskkonna kustutamine</span><span class="sxs-lookup"><span data-stu-id="2e5f0-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e5f0-104">See teema kirjeldab, kuidas Regulatory Configuration Service (RCS) teenuse süsteemi administraator saab kustutada RCS-keskkonda ja seotud andmeid.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="2e5f0-105">Enne selles teemas kirjeldatud protseduuri lõpetamist peavad täidetud olema järgmised eeltingimused:</span><span class="sxs-lookup"><span data-stu-id="2e5f0-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="2e5f0-106">Teile peab RCS-keskkonnas olema määratud **Süsteemiadministraatori** roll.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="2e5f0-107">**Süsteemiadministraatori** rollile peab olema määratud **RCSDeleteEnvironmentDuty** roll.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="2e5f0-108">RCS keskkonna kustutamine</span><span class="sxs-lookup"><span data-stu-id="2e5f0-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="2e5f0-109">Avage RCS ja valige **Elektroonilise aruandluse** tööruumi paan.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="2e5f0-110">Jaotises **Seotud lingid** valige suvand **Kustuta RCS-keskkond**.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![Kustutage RCS-i keskkonna link jaotisest Seotud lingid](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="2e5f0-112">Kuvatavas dialoogiboksis vaadake üle sõnumid keskkonna kustutamise ulatuse kohta.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Teated dialoogiaknas RCS keskkonna kustutamine](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="2e5f0-114">RCS-keskkonna kustutamist ei saa tühistada.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="2e5f0-115">Toiming kustutab valitud RCS-keskkonna ja kõik seostuvad andmed, sh globaalsesse hoidlasse talletatud funktsioonid ja konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="2e5f0-116">Muude organisatsioonidega ühiskasutuses kasutatavad funktsioonid ja konfiguratsioonid sõltuvuste puudumusel lõpetatakse ja kustutatakse.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="2e5f0-117">Sõltuvusi omavad funktsioonid ja konfiguratsioonid märgitakse kui katkestatud.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="2e5f0-118">Sisestage esitatud väljale RCS-keskkonna globaalselt kordumatu identifikaator (GUID) kinnitamaks soovi kustutada.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="2e5f0-119">Keskkonna GUID on kustutamise teates.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="2e5f0-120">Valige nupp **Kustuta keskkond**.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="2e5f0-121">Teie RCS-keskkond ja kõik seotud andmed on nüüd kustutatud.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e5f0-122">Pärast RCS-keskkonna kustutamist pole võimalik andmeid taastada.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="2e5f0-123">Uue RCS-keskkonna saab luua mis tahes saadaolevas RCS-regioonis.</span><span class="sxs-lookup"><span data-stu-id="2e5f0-123">A new RCS environment can be created in any available RCS region.</span></span>
