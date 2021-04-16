---
title: Tunnistuse tüüp
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Sertifikaadi tüüp.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798388"
---
# <a name="certificate-type"></a><span data-ttu-id="cb36b-103">Tunnistuse tüüp</span><span class="sxs-lookup"><span data-stu-id="cb36b-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cb36b-104">Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Sertifikaadi tüüp.</span><span class="sxs-lookup"><span data-stu-id="cb36b-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cb36b-105">Füüsiline nimi: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="cb36b-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="cb36b-106">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cb36b-106">Description</span></span>

<span data-ttu-id="cb36b-107">See üksus määratleb Human Resourcesis seadistatud kutsetunnistuste tüüpide loendi.</span><span class="sxs-lookup"><span data-stu-id="cb36b-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="cb36b-108">Üksus pole juriidilisele isikule (ettevõttele) omane.</span><span class="sxs-lookup"><span data-stu-id="cb36b-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="cb36b-109">JSON-i esindus</span><span class="sxs-lookup"><span data-stu-id="cb36b-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="cb36b-110">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="cb36b-110">Properties</span></span>

| <span data-ttu-id="cb36b-111">Atribuut</span><span class="sxs-lookup"><span data-stu-id="cb36b-111">Property</span></span><br><span data-ttu-id="cb36b-112">**Füüsiline nimi**</span><span class="sxs-lookup"><span data-stu-id="cb36b-112">**Physical name**</span></span><br><span data-ttu-id="cb36b-113">**_Tüüp_**</span><span class="sxs-lookup"><span data-stu-id="cb36b-113">**_Type_**</span></span> | <span data-ttu-id="cb36b-114">Kasuta</span><span class="sxs-lookup"><span data-stu-id="cb36b-114">Use</span></span> | <span data-ttu-id="cb36b-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cb36b-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cb36b-116">**Serdi tüübi olemi ID**</span><span class="sxs-lookup"><span data-stu-id="cb36b-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="cb36b-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="cb36b-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="cb36b-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="cb36b-118">*GUID*</span></span> | <span data-ttu-id="cb36b-119">Kirjutuskaitstud</span><span class="sxs-lookup"><span data-stu-id="cb36b-119">Read-only</span></span><br><span data-ttu-id="cb36b-120">Nõutav</span><span class="sxs-lookup"><span data-stu-id="cb36b-120">Required</span></span> 
<span data-ttu-id="cb36b-121">Süsteemi loodud</span><span class="sxs-lookup"><span data-stu-id="cb36b-121">System-generated</span></span> | <span data-ttu-id="cb36b-122">Sertifikaadi tüübi kordumatu peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="cb36b-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="cb36b-123">**Sertifikaadi tüüp**</span><span class="sxs-lookup"><span data-stu-id="cb36b-123">**Certificate Type**</span></span><br><span data-ttu-id="cb36b-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="cb36b-124">mshr_certificatetype</span></span><br><span data-ttu-id="cb36b-125">*String*</span><span class="sxs-lookup"><span data-stu-id="cb36b-125">*String*</span></span> | <span data-ttu-id="cb36b-126">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="cb36b-126">Read/write</span></span><br><span data-ttu-id="cb36b-127">Nõutav</span><span class="sxs-lookup"><span data-stu-id="cb36b-127">Required</span></span> | <span data-ttu-id="cb36b-128">Sertifikaadi tüübi kordumatu kasutaja loetav identifikaator.</span><span class="sxs-lookup"><span data-stu-id="cb36b-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="cb36b-129">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="cb36b-129">**Description**</span></span><br><span data-ttu-id="cb36b-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="cb36b-130">mshr_description</span></span><br><span data-ttu-id="cb36b-131">*String*</span><span class="sxs-lookup"><span data-stu-id="cb36b-131">*String*</span></span> | <span data-ttu-id="cb36b-132">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="cb36b-132">Read/write</span></span><br><span data-ttu-id="cb36b-133">Nõutav</span><span class="sxs-lookup"><span data-stu-id="cb36b-133">Required</span></span> | <span data-ttu-id="cb36b-134">Serfifikaadi tüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="cb36b-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="cb36b-135">**Nõuab uuendamist**</span><span class="sxs-lookup"><span data-stu-id="cb36b-135">**Require Renewal**</span></span><br><span data-ttu-id="cb36b-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="cb36b-136">mshr_requirerenewal</span></span><br><span data-ttu-id="cb36b-137">*suvandikomplekt mshr_noyes*</span><span class="sxs-lookup"><span data-stu-id="cb36b-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="cb36b-138">Loe/kirjuta</span><span class="sxs-lookup"><span data-stu-id="cb36b-138">Read/write</span></span><br><span data-ttu-id="cb36b-139">Valikuline</span><span class="sxs-lookup"><span data-stu-id="cb36b-139">Optional</span></span> | <span data-ttu-id="cb36b-140">Näitab, kas serdi uuendamine on nõutav.</span><span class="sxs-lookup"><span data-stu-id="cb36b-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cb36b-141">Vt ka</span><span class="sxs-lookup"><span data-stu-id="cb36b-141">See also</span></span>

[<span data-ttu-id="cb36b-142">Kandidaadi jälgimissüsteemi integreerimise API tutvustus</span><span class="sxs-lookup"><span data-stu-id="cb36b-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="cb36b-143">Palgatava kandidaadi päringu näidis</span><span class="sxs-lookup"><span data-stu-id="cb36b-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]