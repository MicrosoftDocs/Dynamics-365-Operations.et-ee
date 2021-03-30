---
title: Arveldusallika uurija
description: Selles artiklis antakse teavet arveldusallika uurija kohta, mida saate kasutada pearaamatu raamatupidamiskannete taga oleva allikateabe üksikasjalikuks analüüsiks.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: roschlom
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f92781a8e1400206f91f91c46c319b928e0010c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250718"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="98736-103">Arveldusallika uurija</span><span class="sxs-lookup"><span data-stu-id="98736-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98736-104">Selles artiklis antakse teavet arveldusallika uurija kohta, mida saate kasutada pearaamatu raamatupidamiskannete taga oleva allikateabe üksikasjalikuks analüüsiks.</span><span class="sxs-lookup"><span data-stu-id="98736-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="98736-105">Arvestusallika uurija on uus leht, millel kuvatakse allika teave.</span><span class="sxs-lookup"><span data-stu-id="98736-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="98736-106">Arvestusallika uurijat saab kasutada eraldiseisva tööriistana või pearaamatu arvestuskirjete taga olevate üksikasjade analüüsimiseks.</span><span class="sxs-lookup"><span data-stu-id="98736-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="98736-107">Näiteks võite kasutada arvestusallika uurijat selleks, et saada kõige üksikasjalikumat allika teavet saldo kohta jaotises Jälje saldo või tehingukande puhul.</span><span class="sxs-lookup"><span data-stu-id="98736-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="98736-108">Seejärel võite kasutada funktsiooni Ekspordi MS Excelisse teabe edasiseks tükeldamiseks ja jagamiseks Microsoft Excelis (nt liigendtabelis või liigendtabeli aruandes).</span><span class="sxs-lookup"><span data-stu-id="98736-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="98736-109">Arvestusallika uurija kuvab alati sama koondsumma pearaamatukonto kohta, mida näitab pearaamat (nt proovibilansis).</span><span class="sxs-lookup"><span data-stu-id="98736-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="98736-110">Sarnaselt proovibilansile saate kuvada segmendid eraldi veergudes.</span><span class="sxs-lookup"><span data-stu-id="98736-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="98736-111">Valige lihtsalt sobiv finantsdimensioonide kogum.</span><span class="sxs-lookup"><span data-stu-id="98736-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="98736-112">Parameetrite abil saate määratleda analüüsi kuupäevavahemiku.</span><span class="sxs-lookup"><span data-stu-id="98736-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="98736-113">See funktsioon sarnaneb samuti proovibilansi funktsioonile.</span><span class="sxs-lookup"><span data-stu-id="98736-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="98736-114">Kõigi dokumentide puhul, mis kasutavad lähtedokumendi raamistikku, näitab arvestusallika uurija lisateavet arvestuse jaotuste ja kohaldatavusel ka projekti arvestuse jaotuste alusel.</span><span class="sxs-lookup"><span data-stu-id="98736-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="98736-115">See teave hõlmab rahasumma tüüpi, projekti, tegevust, kategooriat ja rea atribuute.</span><span class="sxs-lookup"><span data-stu-id="98736-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="98736-116">Siin on mõned näited analüüsimise kohta, mida saab teha.</span><span class="sxs-lookup"><span data-stu-id="98736-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="98736-117">Ostutellimuste ja hankija arvete vahelised erinevused, kuna iga erinevus kajastatakse rahasumma tüübiga (nt hinnavahe).</span><span class="sxs-lookup"><span data-stu-id="98736-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="98736-118">Arveldatavad tunnid võrreldes arveldamatute tundide ja kuludega projekti, äriüksuse ja põhikonto kohta.</span><span class="sxs-lookup"><span data-stu-id="98736-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="98736-119">Lähtedokumentide puhul, mis kasutavad lähtedokumendi viite ID-de kontseptsiooni, kuvab arvestusallika uurija veelgi rohkem üksikasju, nt kliendi, hankija, töötaja, toote, koguse, ühiku teksti ja kirjeldused.</span><span class="sxs-lookup"><span data-stu-id="98736-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="98736-120">Siin on mõned näited analüüsimise kohta, mida saab teha.</span><span class="sxs-lookup"><span data-stu-id="98736-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="98736-121">Hotellikulud äriüksuse ja hotelli kaubamärgi kohta rahandusperioodil, tuginedes kuluaruannetele</span><span class="sxs-lookup"><span data-stu-id="98736-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="98736-122">Allahindlused hankija, toote, osakonna kohta</span><span class="sxs-lookup"><span data-stu-id="98736-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="98736-123">Nende dokumentide puhul saate minna arvestusallika uurijast ka tegeliku lähtedokumendi juurde.</span><span class="sxs-lookup"><span data-stu-id="98736-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]