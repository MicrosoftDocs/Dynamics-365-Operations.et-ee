---
title: "Varude taseme teabe sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude taseme andmete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Varude taseme teabe sünkroonimine rakendusest Finance and Operations rakendusse Field Service 

[!include[banner](../includes/banner.md)]

See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude taseme andmete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Mallid ja ülesanded
Järgmist malli ja aluseks olevaid ülesandeid kasutatakse vabade varude taseme sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.

**Malli nimi andmete integratsioonis:**
- Tootevarud (rakendusest Finance and Operations rakendusse Field Service)
  
**Ülesannete nimed andmete integratsiooni projektis.**
- Tootevarud

Enne kaubavarude taseme sünkroonimist on nõutavad järgmised sünkroonimisülesanded.
- Laod (rakendusest Finance and Operations rakendusse Field Service) 
- Field Service'i tooted laoühikuga (rakendusest Finance and Operations rakendusse Müük) 

## <a name="entity-set"></a>Üksuste komplekt

| Field Service                      | Finance and Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Vabad CDS-i varud lao järgi     |

## <a name="entity-flow"></a>Üksuse voog
Valitud toodete varude taseme teave rakendusest Finance and Operations saadetakse rakendusse Field Service. Kaubavarude taseme info sisaldab järgmist. 
- Laos olev kogus (praegune laos asuv registreeritud füüsiline kogus)
- Tellimusel kogus (kogu registreeritud tellimisel kogus - st müügitellimuste kogusumma)
- Tellitud kogus (kogu registreeritud tellitud kogus - st ostutellimuste kogusumma)

See teave hõivatakse iga lao iga väljastatud toote kohta ja sünkroonitakse muutuse jälgimise põhjal, kui kaubavaru tase muutub.

Rakenduses Field Service loob integreeritud lahendus deltale laotöölehti, et saada rakenduse Field Service tasemed vastama rakenduse Finance and Operations tasemetele.

Rakendus Finance and Operations toimib kaubavarude tasemete koondina. Seega on oluline seadistada töökäskude, üleviimiste ja korrigeerimiste integreerimine rakendusest Field Service rakendusse Finance and Operations, kui funktsionaalsust kasutatakse rakenduses Field Service koos kaubavarude taseme sünkroonimisega rakendusest Finance and Operations.

Tooteid ja ladusid, kus varude tase koondatakse rakendusest Finance and Operations, saab juhtida jaotisest Täpsem päring ja filtreerimine (Power Query).

Märkus: Rakenduses Field Services on võimalik luua mitmeid ladusid (seadistusega On väliselt hallatav = ei) ja seejärel vastendada need ühe laoga rakenduses Finance and Operations, koos täpsema pärinug- ja filtreerimise funktsionaalsusega. Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku kaubavaru taseme ja lihtsalt saadab värskendused rakendusse Finance and Operations. Sllisel juhul ei saa rakendus Field Service kaubavarude taseme värskendusi rakendusest Finance and Operations. Vaadake lisainfot varude korrigeerimise rakendusest Field Service rakendusse Finance and Operations sünkroonimise alt ja sünkroonige töökäsud rakendusest Field Service projektiga seotud töökäskudesse rakenduses Finance and Operations.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus
Väliste tootevarude üksus on uus üksus, mida kasutatakse ainult integratsiooni tagaserveris. See saab kaubavarude taseme väärtused rakendusest Finance and Operations integratsioonist ja seejärel muudab need väärtused käsitsi laotöölehtedekks, mis seejärel muudetakse lao tootevarudeks. 

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="in-the-data-integration-project"></a>Andmeintegratsiooni projektis
Rakendage filtrid suvandi Täpsem päring ja filtreerimine abil juhtimaks, et ainult soovitud tooted ja laod saadavad kaubavarude taseme andmeid rakendusest Finance and Operations rakendusse Field Service.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Tootevarud (rakendusest Finance and Operations rakendusse Field Service): varude üleviimine

[![Malli vastendamine andmete integratsioonis](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

