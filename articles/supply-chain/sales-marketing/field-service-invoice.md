---
title: Rakenduse Field Service lepingu arvete sünkroonimine vabas vormis arvetega rakenduses Finance and Operations
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse lepinguarvete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service vabas vormis arvetega rakenduses Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55301ba39dd28fbae5b6c21b1da3c3d9cf6afd8a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560159"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a>Rakenduse Field Service lepinguarvete sünkroonimine rakenduse Finance and Operations vabas vormis arvetega

[!include[banner](../includes/banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse lepinguarvete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service vabas vormis arvetega rakenduses Microsoft Dynamics 365 for Finance and Operations.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Rakenduse Field Service lepingu arvete sünkroonimiseks vabas vormis arvetega rakenduses Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

**Malli nimi andmete integratsioonis:**

- Lepingu arved (Field Service’ist Fin and Opsi)

**Ülesannete nimed andmete integratsiooni projektis.**

- Arve päised
- Arve read

Enne lepingu arvete sünkroonimist on nõutav järgmine sünkroonimine.

- Kontod (Salesist Fin and Opsi) – otse

## <a name="entity-set"></a>Üksuste komplekt

| Field Service  | Finance and Operations                 |
|----------------|----------------------------------------|
| arved       | CDS-i kliendi vabas vormis arve päised |
| invoicedetails | CDS-i kliendi vabas vormis arve read   |

## <a name="entity-flow"></a>Üksuse voog

Field Service’i lepingu arveid saab teenuse Common Data Service (CDS) andmeintegratsiooni projekti kaudu sünkroonida rakendusega Finance and Operations. Nende arvete värskendused sünkroonitakse rakenduses Finance and Operations vabas vormis arvetega, kui vabas vormis arvete raamatupidamisolek on **Pooleli**. Pärast vabas vormis arvete sisestamist rakenduses Finance and Operations värskendatakse raamatupidamisolekuks **Lõpetatud**, mis tähendab, et enam ei saa sünkroonida värskendusi rakendusest Field Service.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus

Olemile **Arve** on lisatud väli **Lepingust pärinevate ridadega**. See väli aitab tagada, et sünkroonitakse ainult lepingu arved. Väärtus on **tõene**, kui arve sisaldab vähemalt ühte lepingust pärinevat arverida.

Olemile **Arve rida** on lisatud väli **Lepingust pärinevate ridadega**. See väli aitab tagada, et sünkroonitakse ainult lepingust loodud arve read. Väärtus on **tõene**, kui arve rida pärineb lepingust.

**Arve kuupäev** on kohustuslik väli rakenduses Finance and Operations. Seetõttu peab väljal rakenduses Field Service enne sünkroonimist olema väärtus. Selle nõudega kooskõlla viimiseks lisatakse järgmine loogika.

- Kui väli **Arve kuupäev** on olemil **Arve** tühi (st kui sel puudub väärtus), seatakse selleks tänane kuupäev, kui lisatakse lepingust pärinev arve rida.
- Kasutaja saab välja **Arve kuupäev** muuta. Ent kui kasutaja üritab lepingu arvet salvestada, saab ta äriprotsessi tõrke, kui arvel on väli **Arve kuupäev** tühi.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="in-finance-and-operations"></a>Rakenduses Finance and Operations

Integreerimiseks tuleb seadistada arve päritolu, et eristada vabas vormis arveid rakenduses Finance and Operations, mis on loodud lepingu arvetest rakenduses Field Service. Kui arve päritolutüüp on **Lepingu arve integratsioon**, kuvatakse **müügiarve** päises väli **Välise arve number** .

Lisaks arve päises kuvamisele, saab **välise arve numbri** teavet kasutada, aitamaks tagada, et rakenduse Field Service lepingu arvete põhjal loodud arved filtreeritakse rakenduse Finance and Operations sünkroonimisel rakendusega Field Service välja.

1. Avage **Müügireskontro** \> **Seadistus** \> **Arve päritolukoodid**.
2. Uue arve päritolu loomiseks valige **Uus**.
3. Sisestage väljal **Arve päritolu** arve päritolu nimi, näiteks **FS**.
4. Sisestage väljale **Kirjeldus** kirjeldus, näiteks **Field Service’i lepingu arve**.
5. Valige märkeruut **Päritolu tüübi määramine**.
6. Seadke välja **Arve päritolu tüüp** väärtuseks **Lepingu arve integratsioon**.
7. Valige **Salvesta**.

### <a name="in-the-data-integration-project"></a>Andmeintegratsiooni projektis

Ülesanne: **Arve read**  

Veenduge, et välja **Põhikonto kuvatav väärtus** vaikeväärtus rakenduses Finance and Operations värskendatakse soovitud väärtusega sobivaks.

Malli vaikeväärtus on **401100**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-headers"></a>Lepingu arved (Field Service’ist Fin and Opsi): arve päised

[![Malli vastendamine andmete integratsioonis](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-fin-and-ops-invoice-lines"></a>Lepingu arved (Field Service’ist Fin and Opsi): arve read

[![Malli vastendamine andmete integratsioonis](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)
