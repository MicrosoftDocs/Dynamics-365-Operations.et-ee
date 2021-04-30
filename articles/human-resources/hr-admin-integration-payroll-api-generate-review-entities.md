---
title: Palgaarvestuse üksuste loomine ja ülevaatus
description: Selles teemas kirjeldatakse palgaolemite genereerimist ja ülevaatamist.
author: andreabichsel
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c6e043498d4e36e38575a16c6475a5edfef51fc6
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881967"
---
# <a name="generate-payroll-entities"></a><span data-ttu-id="869c8-103">Palgaarvestuse üksuste loomine</span><span class="sxs-lookup"><span data-stu-id="869c8-103">Generate payroll entities</span></span>

<span data-ttu-id="869c8-104">Selle funktsiooni OData abil saate luua palgaarvestuse integreerimiseks vajalikud olemid.</span><span class="sxs-lookup"><span data-stu-id="869c8-104">Use this OData function to generate the entities needed for payroll integration.</span></span> <span data-ttu-id="869c8-105">Kui neid olemeid muudetakse personaliosakonnas (nt kohandatud väljade lisamine), saab seda funktsiooni uuesti kutsuda iga olemi metaandmete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="869c8-105">If any changes are made to these entities in Human Resources, such as adding custom fields, this function can be called again to refresh the metadata of each entity.</span></span> <span data-ttu-id="869c8-106">Vastus sisaldab toimingu ID-d, mida saate jälgida, et teaksite, kui genereerimisprotsess on lõppenud.</span><span class="sxs-lookup"><span data-stu-id="869c8-106">The response contains an operation ID that you can monitor so you know when the generation process has completed.</span></span>

<span data-ttu-id="869c8-107">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="869c8-107">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/RefreshHumanResourcesVirtualEntities
```

<span data-ttu-id="869c8-108">**keha**</span><span class="sxs-lookup"><span data-stu-id="869c8-108">**body**</span></span>

```json
{
    "PhysicalNames" : ["PayrollEmployeeEntity", "HcmWorkerBaseEntity", "PayrollPositionEntity", "PayrollPositionJobEntity", "PayrollWorkerAddressEntity", "HcmJobDetailEntity", "HcmCompFixedPlanTableEntity", "PayrollFixedCompensationPlanEntity", "HcmEmploymentDetailEntity"]
}
```

<span data-ttu-id="869c8-109">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="869c8-109">**Response**</span></span>

```json
{
    "AsyncOperationId": "8b98d338-f939-4c86-9a91-80b76b6ab2ea"
}
```

## <a name="review-payroll-entities"></a><span data-ttu-id="869c8-110">Palgaarvestuse olemite ülevaade</span><span class="sxs-lookup"><span data-stu-id="869c8-110">Review payroll entities</span></span>

<span data-ttu-id="869c8-111">Selle API abil saate tuua nende olemite loendi, mis on edukalt loodud ja kasutusvalmis.</span><span class="sxs-lookup"><span data-stu-id="869c8-111">Use this API to retrieve a list of the entities that have been successfully generated and are ready for use.</span></span>

<span data-ttu-id="869c8-112">**Taotlus**</span><span class="sxs-lookup"><span data-stu-id="869c8-112">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hrvirtualentitycatalogs?$filter=mshr_hasbeengenerated eq true
```

<span data-ttu-id="869c8-113">**Vastus**</span><span class="sxs-lookup"><span data-stu-id="869c8-113">**Response**</span></span>

```json
{
      "value": [
        {
            "mshr_physicalname": "PayrollWorkerAddressEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-1c00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmJobDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6400-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmCompFixedPlanTableEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6b00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollEmployeeEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-6d00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmEmploymentDetailEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-7e00-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollFixedCompensationPlanEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-9300-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "HcmWorkerBaseEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-c000-005001000000",
            "mshr_refresh": null
        },
        {
            "mshr_physicalname": "PayrollPositionJobEntity",
            "mshr_hasbeengenerated": true,
            "mshr_hrvirtualentitycatalogid": "00000603-0000-0000-e700-005001000000",
            "mshr_refresh": null
        }
    ]
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]