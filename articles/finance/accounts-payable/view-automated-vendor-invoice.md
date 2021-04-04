---
title: Hankija arve automatiseerimise tulemuste kuvamine (eelversioon)
description: Selles teemas selgitatakse, kuidas vaadata hankija arvete olekut, mis on kaasatud töövoole edastamise automatiseeritud protsessi.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b87af4c64f8021a1b23cca5d8f38ac21c8efbd4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248084"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="64338-103">Hankija arve automatiseerimise tulemuste kuvamine</span><span class="sxs-lookup"><span data-stu-id="64338-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64338-104">Selles teemas selgitatakse, kuidas vaadata hankija arvete olekut, mis on kaasatud töövoole edastamise automatiseeritud protsessi.</span><span class="sxs-lookup"><span data-stu-id="64338-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="64338-105">Automatiseerimisajaloo üksikasjad säilitatakse iga imporditud hankija arve kohta.</span><span class="sxs-lookup"><span data-stu-id="64338-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="64338-106">Sõltuvalt teie automatiseeritud äriprotsessidest kuvatakse lehel **Ootel hankija arved** väärtused **Automatiseeritud sissetuleku vastavusseviimise olek** ja **Automatiseeritud töövoole edastamise olek**.</span><span class="sxs-lookup"><span data-stu-id="64338-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="64338-107">Saate vaadata üksikasju ja teha plaani, et keskenduda arvetele, mis automatiseerimise käigus nurjusid.</span><span class="sxs-lookup"><span data-stu-id="64338-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="64338-108">Seejärel saate pärast probleemi parandamist jätkata imporditud arve automatiseeritud protsessi.</span><span class="sxs-lookup"><span data-stu-id="64338-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="64338-109">Enne edastatud arve redigeerimist peate automatiseeritud töötluse peatama.</span><span class="sxs-lookup"><span data-stu-id="64338-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="64338-110">Kui automaatses töövoole edastamise protsessis tuleb arve peatada, seadke välja **Kaasa automatiseeritud töötlusse** väärtuseks **Ei** lehel **Hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="64338-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="64338-111">Automatiseerimine ei käivitu enne, kui suvandi **Kaasa automatiseeritud töötlusse** väärtuseks seatakse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="64338-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="64338-112">Arve saab jääta välja täiendavast automatiseerimisest, kui see ei ole veel töövoosüsteemis ja seda ei kasutata automatiseeritud protsessis.</span><span class="sxs-lookup"><span data-stu-id="64338-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="64338-113">Kui imporditud arve puhul rakendatakse töövoole edastamise protsessi, saate vaadata selle suvandi **Automatiseerimise olek** väärtust lehel **Hankija arved**.</span><span class="sxs-lookup"><span data-stu-id="64338-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="64338-114">Jälgitakse järgmisi olekuid.</span><span class="sxs-lookup"><span data-stu-id="64338-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="64338-115">**Kaasatud** – automatiseeritud protsessid, mis on määratud lehel **Ostureskontro parameetrid**, töötavad õigesti, kuid pole veel lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="64338-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="64338-116">**Peatatud** – automatiseeritud protsessid, mis on määratud lehel **Ostureskontro parameetrid**, on käivitatud, kuid vähemalt üks etapp protsessis nurjus.</span><span class="sxs-lookup"><span data-stu-id="64338-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="64338-117">Olekut **Peatatud** rakendatakse ka juhul, kui välja **Kaasa automatiseeritud töötlemisse** väärtuseks on seatud **Ei**.</span><span class="sxs-lookup"><span data-stu-id="64338-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="64338-118">Nurjumisi saate kuvada, kui valite **Kuva kõige viimased tulemused**.</span><span class="sxs-lookup"><span data-stu-id="64338-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="64338-119">**Töövoos** – imporditud arve on edastatud töövoosüsteemi kas automatiseeritud töövoole edastamise protsessi kaudu või käsitsi.</span><span class="sxs-lookup"><span data-stu-id="64338-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="64338-120">**Töövoog lõpetatud** – töövooprotsess on imporditud arve jaoks lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="64338-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]