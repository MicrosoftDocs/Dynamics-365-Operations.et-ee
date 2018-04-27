---
title: "Rakenduse Field Service lepingu arvete sünkroonimine vabas vormis arvetega rakenduses Finance and Operations"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse rakenduse Microsoft Dynamics 365 for Field Service lepingu arvete sünkroonimiseks vabas vormis arvetega rakenduses Microsoft Dynamics 365 for Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: et-ee
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="75a52-103">Rakenduse Field Service lepingu arvete sünkroonimine vabas vormis arvetega rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75a52-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="75a52-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse rakenduse Microsoft Dynamics 365 for Field Service lepingu arvete sünkroonimiseks vabas vormis arvetega rakenduses Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75a52-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="75a52-105">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="75a52-105">Templates and tasks</span></span>

<span data-ttu-id="75a52-106">Rakenduse Field Service lepingu arvete sünkroonimiseks vabas vormis arvetega rakenduses Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="75a52-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="75a52-107">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="75a52-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="75a52-108">Lepingu arved (Field Service’ist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="75a52-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="75a52-109">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="75a52-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="75a52-110">Arve päised</span><span class="sxs-lookup"><span data-stu-id="75a52-110">Invoice headers</span></span>
- <span data-ttu-id="75a52-111">Arve read</span><span class="sxs-lookup"><span data-stu-id="75a52-111">Invoice lines</span></span>

<span data-ttu-id="75a52-112">Enne lepingu arvete sünkroonimist on nõutav järgmine sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="75a52-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="75a52-113">Kontod (Salesist Fin and Opsi) – otse</span><span class="sxs-lookup"><span data-stu-id="75a52-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="75a52-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="75a52-114">Entity set</span></span>

| <span data-ttu-id="75a52-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="75a52-115">Field Service</span></span>  | <span data-ttu-id="75a52-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75a52-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="75a52-117">arved</span><span class="sxs-lookup"><span data-stu-id="75a52-117">invoices</span></span>       | <span data-ttu-id="75a52-118">CDS-i kliendi vabas vormis arve päised</span><span class="sxs-lookup"><span data-stu-id="75a52-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="75a52-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="75a52-119">invoicedetails</span></span> | <span data-ttu-id="75a52-120">CDS-i kliendi vabas vormis arve read</span><span class="sxs-lookup"><span data-stu-id="75a52-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="75a52-121">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="75a52-121">Entity flow</span></span>

<span data-ttu-id="75a52-122">Rakenduse Field Service lepingu arveid saab Common Data Service’i (CDS) andmeintegratsiooni projekti kaudu sünkroonida rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75a52-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="75a52-123">Nende arvete värskendused sünkroonitakse rakenduses Finance and Operations vabas vormis arvetega, kui vabas vormis arvete raamatupidamisolek on **Pooleli**.</span><span class="sxs-lookup"><span data-stu-id="75a52-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="75a52-124">Pärast vabas vormis arvete sisestamist rakenduses Finance and Operations värskendatakse raamatupidamisolekuks **Lõpetatud**, mis tähendab, et enam ei saa sünkroonida värskendusi rakendusest Field Service.</span><span class="sxs-lookup"><span data-stu-id="75a52-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="75a52-125">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="75a52-125">Field Service CRM solution</span></span>

<span data-ttu-id="75a52-126">Olemile **Arve** on lisatud väli **Lepingust pärinevate ridadega**.</span><span class="sxs-lookup"><span data-stu-id="75a52-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="75a52-127">See väli aitab tagada, et sünkroonitakse ainult lepingu arved.</span><span class="sxs-lookup"><span data-stu-id="75a52-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="75a52-128">Väärtus on **tõene**, kui arve sisaldab vähemalt ühte lepingust pärinevat arverida.</span><span class="sxs-lookup"><span data-stu-id="75a52-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="75a52-129">Olemile **Arve rida** on lisatud väli **Lepingust pärinevate ridadega**.</span><span class="sxs-lookup"><span data-stu-id="75a52-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="75a52-130">See väli aitab tagada, et sünkroonitakse ainult lepingust loodud arve read.</span><span class="sxs-lookup"><span data-stu-id="75a52-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="75a52-131">Väärtus on **tõene**, kui arve rida pärineb lepingust.</span><span class="sxs-lookup"><span data-stu-id="75a52-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="75a52-132">**Arve kuupäev** on kohustuslik väli rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="75a52-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="75a52-133">Seetõttu peab väljal rakenduses Field Service enne sünkroonimist olema väärtus.</span><span class="sxs-lookup"><span data-stu-id="75a52-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="75a52-134">Selle nõudega kooskõlla viimiseks lisatakse järgmine loogika.</span><span class="sxs-lookup"><span data-stu-id="75a52-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="75a52-135">Kui väli **Arve kuupäev** on olemil **Arve** tühi (st kui sel puudub väärtus), seatakse selleks tänane kuupäev, kui lisatakse lepingust pärinev arve rida.</span><span class="sxs-lookup"><span data-stu-id="75a52-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="75a52-136">Kasutaja saab välja **Arve kuupäev** muuta.</span><span class="sxs-lookup"><span data-stu-id="75a52-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="75a52-137">Ent kui kasutaja üritab lepingu arvet salvestada, saab ta äriprotsessi tõrke, kui arvel on väli **Arve kuupäev** tühi.</span><span class="sxs-lookup"><span data-stu-id="75a52-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="75a52-138">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="75a52-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="75a52-139">Rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="75a52-139">In Finance and Operations</span></span>

<span data-ttu-id="75a52-140">Integreerimiseks tuleb seadistada arve päritolu, et eristada vabas vormis arveid rakenduses Finance and Operations, mis on loodud lepingu arvetest rakenduses Field Service.</span><span class="sxs-lookup"><span data-stu-id="75a52-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="75a52-141">Kui arve päritolutüüp on **Lepingu arve integratsioon**, kuvatakse **müügiarve** päises väli **Välise arve number** .</span><span class="sxs-lookup"><span data-stu-id="75a52-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="75a52-142">Lisaks arve päises kuvamisele, saab **välise arve numbri** teavet kasutada, aitamaks tagada, et rakenduse Field Service lepingu arvete põhjal loodud arved filtreeritakse rakenduse Finance and Operations sünkroonimisel rakendusega Field Service välja.</span><span class="sxs-lookup"><span data-stu-id="75a52-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="75a52-143">Avage **Müügireskontro** \> **Seadistus** \> **Arve päritolukoodid**.</span><span class="sxs-lookup"><span data-stu-id="75a52-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="75a52-144">Uue arve päritolu loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="75a52-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="75a52-145">Sisestage väljal **Arve päritolu** arve päritolu nimi, näiteks **FS**.</span><span class="sxs-lookup"><span data-stu-id="75a52-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="75a52-146">Sisestage väljale **Kirjeldus** kirjeldus, näiteks **Field Service’i lepingu arve**.</span><span class="sxs-lookup"><span data-stu-id="75a52-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="75a52-147">Valige märkeruut **Päritolu tüübi määramine**.</span><span class="sxs-lookup"><span data-stu-id="75a52-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="75a52-148">Seadke välja **Arve päritolu tüüp** väärtuseks **Lepingu arve integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="75a52-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="75a52-149">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="75a52-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="75a52-150">Andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="75a52-150">In the Data Integration project</span></span>

<span data-ttu-id="75a52-151">Ülesanne: **Arve read**</span><span class="sxs-lookup"><span data-stu-id="75a52-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="75a52-152">Veenduge, et välja **Põhikonto kuvatav väärtus** vaikeväärtus rakenduses Finance and Operations värskendatakse soovitud väärtusega sobivaks.</span><span class="sxs-lookup"><span data-stu-id="75a52-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="75a52-153">Malli vaikeväärtus on **401100**.</span><span class="sxs-lookup"><span data-stu-id="75a52-153">The default template value is **401100**.</span></span>

