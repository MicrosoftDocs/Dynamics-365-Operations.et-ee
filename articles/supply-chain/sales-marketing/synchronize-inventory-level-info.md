---
title: Varude taseme teabe sünkroonimine rakendusest Supply Chain Management rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude tasemel teabe sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ce5ddf863988475550584384f4cf26f1302768aa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355897"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Varude taseme teabe sünkroonimine rakendusest Supply Chain Management rakendusse Field Service 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude tasemel teabe sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.

[![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel.](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Olemasolevate varude taseme sünkroonimiseks rakendusest Supply Chain Management rakendusse Field Service kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

**Mall andmeintegratsioonis**
- Tootevarud (rakendusest Supply Chain Management rakendusse Field Service)
  
**Ülesanne andmeintegratsiooni projektis**
- Tootevarud

Enne kaubavarude taseme sünkroonimist on nõutavad järgmised sünkroonimisülesanded.
- Laod (rakendusest Supply Chain Management rakendusse Field Service) 
- Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük) 

## <a name="entity-set"></a>Üksuste komplekt

| Field Service                      | Supply Chain Management                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Dataverse’i vabad varud lao järgi     |

## <a name="entity-flow"></a>Üksuse voog
Valitud toodete varude tasemel teave saadetakse rakendusest Finance and Operations rakendusse Field Service. Varude tasemel teave hõlmab järgmist. 
- Vaba kaubavaru (praegune laos asuv registreeritud füüsiline kogus)
- Tellimusel kogus (kogu registreeritud tellimisel kogus, nagu müügitellimused)
- Tellitud kogus (kogu registreeritud tellitud kogus, nagu ostutellimused)

See teave hõivatakse iga lao iga väljastatud toote kohta ja sünkroonitakse muutuse jälgimise põhjal, kui kaubavaru tase muutub.

Rakenduses Field Service loob integratsioonilahendus deltale varude töölehed, et rakenduse Field Service tasemed vastaksid rakenduse Supply Chain Management tasemetele.

Rakendus Supply Chain Management toimib kaubavarude tasemete koondina. Seega on oluline seadistada töökäskude, üleviimiste ja korrigeerimiste integreerimine rakendusest Field Service rakendusse Supply Chain Management kui seda funktsiooni kasutatakse rakenduses Field Service koos varude tasemete sünkroonimisega rakendusest Supply Chain Management.

Tooteid ja ladusid, kus varude tase koondatakse rakendusest Supply Chain Management, saab juhtida jaotisest Täpsem päring ja filtreerimine (Power Query).

> [!NOTE]
> Rakenduses Field Service on võimalik luua mitmeid ladusid (seadistusega **On väliselt hallatav = Ei**) ja seejärel vastendada need ühe laoga rakenduses Supply Chain Management koos täpsema päringu ja filtreerimise funktsiooniga. Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku varude taseme ja saadab ainult värskendused rakendusse Supply Chain Management. Sellisel juhul ei saa Field Service varude taseme värskendusi rakendusest Supply Chain Management. Lisateavet vt teemadest [Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Töökäskude sünkroonimine rakenduses Field Service rakenduses Supply Chain Management projektiga seotud müügitellimustega](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
**Välised tootevarud** on uus üksus, mida kasutatakse ainult integratsiooni tagaserveris. See üksus saab kaubavarude taseme väärtused rakendusest Supply Chain Management integratsioonis ja seejärel muudab need väärtused käsitsi varude töölehtedeks, mis seejärel muudab varude tooteid laos.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="data-integration"></a>Andmete integratsioon
Et projekt töötaks peate tagama, et uuendatakse integreerimisvõtit msdynce_externalproductinventories jaoks.
1.  Avage **Andmete integreerimine > Ühenduskomplektid**.
2.  Valige kasutatav ühenduskomplekt.
3.  Vahekaardil **Integreerimisvõti** veenduge, et lisatakse järgmised võtmed toodetele msdynce_externalproductinventories
      - msdynce_productnumber (tootenumber)
      - msdynce_warehouseid (lao ID)
      
### <a name="data-integration-project"></a>Andmeintegratsiooni projekt
Saate rakendada filtreid täpsema päringu ja filtreerimise abil, nii et ainult teatud tooted ja laod saadavad varude tasemel teavet rakendusest Supply Chain Management rakendusse Field Service.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Tootevarud (rakendusest Supply Chain Management rakendusse Field Service): tootevarud

[![Malli vastendamine andmete integratsioonis.](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]