---
title: Sünkroonige leppe arved rakenduses Field Service vabas vormis arveteks rakenduses Supply Chain Management
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse lepinguarvete sünkroonimiseks rakendusest Dynamics 365 Field Service vabas vormis arveteks rakenduses Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 0942ce83060c186212d7f425f8dbd0a4ca2c09e7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252770"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="e8233-103">Sünkroonige leppe arved rakenduses Field Service vabas vormis arveteks rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8233-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e8233-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse lepinguarvete sünkroonimiseks rakendusest Dynamics 365 Field Service vabas vormis arvetega rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8233-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e8233-105">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="e8233-105">Templates and tasks</span></span>

<span data-ttu-id="e8233-106">Rakenduse Field Service lepingu arvete sünkroonimiseks vabas vormis arvetega rakenduses Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="e8233-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="e8233-107">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="e8233-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="e8233-108">Leppe arved (rakendus Field Service rakendusele Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="e8233-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="e8233-109">**Ülesannete nimed andmete integratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="e8233-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="e8233-110">Arve päised</span><span class="sxs-lookup"><span data-stu-id="e8233-110">Invoice headers</span></span>
- <span data-ttu-id="e8233-111">Arve read</span><span class="sxs-lookup"><span data-stu-id="e8233-111">Invoice lines</span></span>

<span data-ttu-id="e8233-112">Enne lepingu arvete sünkroonimist on nõutav järgmine sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="e8233-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="e8233-113">Kontod (Salesist Supply Chain Managementi) – otsene</span><span class="sxs-lookup"><span data-stu-id="e8233-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="e8233-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="e8233-114">Entity set</span></span>

| <span data-ttu-id="e8233-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="e8233-115">Field Service</span></span>  | <span data-ttu-id="e8233-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8233-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="e8233-117">arved</span><span class="sxs-lookup"><span data-stu-id="e8233-117">invoices</span></span>       | <span data-ttu-id="e8233-118">Dataverse’i kliendi vabas vormis arve päised</span><span class="sxs-lookup"><span data-stu-id="e8233-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="e8233-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="e8233-119">invoicedetails</span></span> | <span data-ttu-id="e8233-120">Dataverse’i kliendi vabas vormis arve read</span><span class="sxs-lookup"><span data-stu-id="e8233-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="e8233-121">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="e8233-121">Entity flow</span></span>

<span data-ttu-id="e8233-122">Field Service’i leppe arveid saab teenuse Microsoft Dataverse andmeintegratsiooni projekti kaudu sünkroonida rakendusega Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8233-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="e8233-123">Nende arvete värskendused sünkroonitakse rakenduses Supply Chain Management vabas vormis arvetega, kui vabas vormis arvete raamatupidamisolek on **Pooleli**.</span><span class="sxs-lookup"><span data-stu-id="e8233-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="e8233-124">Pärast vabas vormis arvete sisestamist rakenduses Supply Chain Management värskendatakse raamatupidamisolekuks **Lõpetatud**, mis tähendab, et enam ei saa sünkroonida värskendusi rakendusest Field Service.</span><span class="sxs-lookup"><span data-stu-id="e8233-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="e8233-125">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="e8233-125">Field Service CRM solution</span></span>

<span data-ttu-id="e8233-126">Tabelile **Arve** on lisatud veerg **Lepingust pärinevate ridadega**.</span><span class="sxs-lookup"><span data-stu-id="e8233-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="e8233-127">See veerg aitab tagada, et sünkroonitakse ainult lepingu arved.</span><span class="sxs-lookup"><span data-stu-id="e8233-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="e8233-128">Väärtus on **tõene**, kui arve sisaldab vähemalt ühte lepingust pärinevat arverida.</span><span class="sxs-lookup"><span data-stu-id="e8233-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="e8233-129">Tabelile **Arverida** on lisatud veerg **Lepingust pärinev**.</span><span class="sxs-lookup"><span data-stu-id="e8233-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="e8233-130">See veerg aitab tagada, et sünkroonitakse ainult lepingust loodud arveread.</span><span class="sxs-lookup"><span data-stu-id="e8233-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="e8233-131">Väärtus on **tõene**, kui arve rida pärineb lepingust.</span><span class="sxs-lookup"><span data-stu-id="e8233-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="e8233-132">**Arve kuupäev** on kohustuslik väli rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e8233-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="e8233-133">Seetõttu peab veerul rakenduses Field Service enne sünkroonimist olema väärtus.</span><span class="sxs-lookup"><span data-stu-id="e8233-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="e8233-134">Selle nõudega kooskõlla viimiseks lisatakse järgmine loogika.</span><span class="sxs-lookup"><span data-stu-id="e8233-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="e8233-135">Kui veerg **Arve kuupäev** on tabelis **Arve** tühi (st kui sel puudub väärtus), seatakse selleks tänane kuupäev, kui lisatakse lepingust pärinev arve rida.</span><span class="sxs-lookup"><span data-stu-id="e8233-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="e8233-136">Kasutaja saab veergu **Arve kuupäev** muuta.</span><span class="sxs-lookup"><span data-stu-id="e8233-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="e8233-137">Ent kui kasutaja üritab lepingu arvet salvestada, saab ta äriprotsessi tõrke, kui arvel on veerg **Arve kuupäev** tühi.</span><span class="sxs-lookup"><span data-stu-id="e8233-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="e8233-138">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="e8233-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="e8233-139">Rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e8233-139">In Supply Chain Management</span></span>

<span data-ttu-id="e8233-140">Integreerimiseks tuleb seadistada arve päritolu, et eristada vabas vormis arveid rakenduses Supply Chain Management, mis on loodud lepingu arvetest rakenduses Field Service.</span><span class="sxs-lookup"><span data-stu-id="e8233-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="e8233-141">Kui arve päritolutüüp on **Lepingu arve integratsioon**, kuvatakse **müügiarve** päises väli **Välise arve number** .</span><span class="sxs-lookup"><span data-stu-id="e8233-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="e8233-142">Lisaks arve päises kuvamisele, saab **Välise arve numbri** teavet kasutada, aitamaks tagada, et rakenduse Field Service lepingu arvete põhjal loodud arved filtreeritakse rakenduse Supply Chain Management sünkroonimisel rakendusega Field Service välja.</span><span class="sxs-lookup"><span data-stu-id="e8233-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="e8233-143">Avage **Müügireskontro** \> **Seadistus** \> **Arve päritolukoodid**.</span><span class="sxs-lookup"><span data-stu-id="e8233-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="e8233-144">Uue arve päritolu loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e8233-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="e8233-145">Sisestage väljal **Arve päritolu** arve päritolu nimi, näiteks **FS**.</span><span class="sxs-lookup"><span data-stu-id="e8233-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="e8233-146">Sisestage väljale **Kirjeldus** kirjeldus, näiteks **Field Service’i lepingu arve**.</span><span class="sxs-lookup"><span data-stu-id="e8233-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="e8233-147">Valige märkeruut **Päritolu tüübi määramine**.</span><span class="sxs-lookup"><span data-stu-id="e8233-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="e8233-148">Seadke välja **Arve päritolu tüüp** väärtuseks **Lepingu arve integratsioon**.</span><span class="sxs-lookup"><span data-stu-id="e8233-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="e8233-149">Valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e8233-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="e8233-150">Andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="e8233-150">In the Data Integration project</span></span>

<span data-ttu-id="e8233-151">Ülesanne: **Arve read**</span><span class="sxs-lookup"><span data-stu-id="e8233-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="e8233-152">Veenduge, et välja **Põhikonto kuvatav väärtus** vaikeväärtus rakenduses Supply Chain Management värskendatakse soovitud väärtusega sobivaks.</span><span class="sxs-lookup"><span data-stu-id="e8233-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="e8233-153">Malli vaikeväärtus on **401100**.</span><span class="sxs-lookup"><span data-stu-id="e8233-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e8233-154">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="e8233-154">Template mapping in Data integration</span></span>

<span data-ttu-id="e8233-155">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="e8233-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="e8233-156">Leppe arved (rakendus Field Service rakendusele Supply Chain Management): arve päised</span><span class="sxs-lookup"><span data-stu-id="e8233-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="e8233-157">[![Malli vastendamine andmete integratsioonis](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="e8233-157">[![Template mapping in Data integration](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="e8233-158">Leppe arved (rakendus Field Service rakendusele Supply Chain Management): arve read</span><span class="sxs-lookup"><span data-stu-id="e8233-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="e8233-159">[![Malli vastendamine andmete integratsioonis](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="e8233-159">[![Template mapping in Data integration](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]