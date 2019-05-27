---
title: Varude taseme teabe sünkroonimine rakendusest Finance and Operations rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude tasemel teabe sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c7dce4427810b93e0ee4f1a27881c2b1b04fb125
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1535694"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Varude taseme teabe sünkroonimine rakendusest Finance and Operations rakendusse Field Service 

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude tasemel teabe sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Vaba kaubavaru sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

**Mall andmeintegratsioonis**
- Tootevarud (rakendusest Fin and Ops rakendusse Field Service)
  
**Ülesanne andmeintegratsiooni projektis**
- Tootevarud

Enne kaubavarude taseme sünkroonimist on nõutavad järgmised sünkroonimisülesanded.
- Laod (rakendusest Fin and Ops rakendusse Field Service) 
- Field Service’i tooted laoühikuga (rakendusest Fin and Ops rakendusse Sales) 

## <a name="entity-set"></a>Üksuste komplekt

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Vabad CDS-i varud lao järgi     |

## <a name="entity-flow"></a>Üksuse voog
Valitud toodete varude tasemel teave saadetakse rakendusest Finance and Operations rakendusse Field Service. Varude tasemel teave hõlmab järgmist. 
- Vaba kaubavaru (praegune laos asuv registreeritud füüsiline kogus)
- Tellimusel kogus (kogu registreeritud tellimisel kogus, nagu müügitellimused)
- Tellitud kogus (kogu registreeritud tellitud kogus, nagu ostutellimused)

See teave hõivatakse iga lao iga väljastatud toote kohta ja sünkroonitakse muutuse jälgimise põhjal, kui kaubavaru tase muutub.

Rakenduses Field Service loob integratsioonilahendus deltale varude töölehed, et rakenduse Field Service tasemed vastaksid rakenduse Finance and Operations tasemetele.

Rakendus Finance and Operations toimib kaubavarude tasemete koondina. Seega on oluline seadistada töökäskude, üleviimiste ja korrigeerimiste integreerimine rakendusest Field Service rakendusse Finance and Operations, kui seda funktsiooni kasutatakse rakenduses Field Service koos varude tasemete sünkroonimisega rakendusest Finance and Operations.

Tooteid ja ladusid, kus varude tase koondatakse rakendusest Finance and Operations, saab juhtida jaotisest Täpsem päring ja filtreerimine (Power Query).

> [!NOTE]
> Rakenduses Field Service on võimalik luua mitmeid ladusid (seadistusega **On väliselt hallatav = Ei**) ja seejärel vastendada need ühe laoga rakenduses Finance and Operations koos täpsema päringu ja filtreerimise funktsiooniga. Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku varude taseme ja saadab ainult värskendused rakendusse Finance and Operations. Sellisel juhul ei saa Field Service varude taseme värskendusi rakendusest Finance and Operations. Lisateavet vt teemadest [Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Töökäskude sünkroonimine rakenduses Field Service rakenduses Finance and Operations projektiga seotud müügitellimustega](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
**Välised tootevarud** on uus üksus, mida kasutatakse ainult integratsiooni tagaserveris. See üksus saab kaubavarude taseme väärtused rakendusest Finance and Operations integratsioonis ja seejärel muudab need väärtused käsitsi varude töölehtedeks, mis seejärel muudab varude tooteid laos.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="data-integration"></a>Andmete integratsioon
Et projekt töötaks peate tagama, et uuendatakse integreerimisvõtit msdynce_externalproductinventories jaoks.
1.  Avage **Andmete integreerimine > Ühenduskomplektid**.
2.  Valige kasutatav ühenduskomplekt.
3.  Vahekaardil **Integreerimisvõti** veenduge, et lisatakse järgmised võtmed toodetele msdynce_externalproductinventories
      - msdynce_productnumber (tootenumber)
      - msdynce_warehouseid (lao ID)
      
### <a name="data-integration-project"></a>Andmeintegratsiooni projekt
Saate rakendada filtreid täpsema päringu ja filtreerimise abil, nii et ainult teatud tooted ja laod saadavad varude tasemel teavet rakendusest Finance and Operations rakendusse Field Service.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

### <a name="product-inventory-fin-and-ops-to-field-service-product-inventory"></a>Tootevarud (rakendusest Fin and Ops rakendusse Field Service): tootevarud

[![Malli vastendamine andmete integratsioonis](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
