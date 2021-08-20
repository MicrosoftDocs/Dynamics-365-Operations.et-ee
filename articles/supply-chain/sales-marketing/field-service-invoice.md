---
title: Sünkroonige leppe arved rakenduses Field Service vabas vormis arveteks rakenduses Supply Chain Management
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse lepinguarvete sünkroonimiseks rakendusest Dynamics 365 Field Service vabas vormis arveteks rakenduses Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 04/10/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 8fffa2bfc0bd7a1fa479c63f0f4d20b5c3ae37c93317a18a67202968b6acf405
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753911"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a>Sünkroonige leppe arved rakenduses Field Service vabas vormis arveteks rakenduses Supply Chain Management

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse lepinguarvete sünkroonimiseks rakendusest Dynamics 365 Field Service vabas vormis arvetega rakenduses Dynamics 365 Supply Chain Management.

## <a name="templates-and-tasks"></a>Mallid ja ülesanded

Rakenduse Field Service lepingu arvete sünkroonimiseks vabas vormis arvetega rakenduses Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.

**Malli nimi andmete integratsioonis:**

- Leppe arved (rakendus Field Service rakendusele Supply Chain Management)

**Ülesannete nimed andmete integratsiooni projektis**

- Arve päised
- Arve read

Enne lepingu arvete sünkroonimist on nõutav järgmine sünkroonimine.

- Kontod (Salesist Supply Chain Managementi) – otsene

## <a name="entity-set"></a>Üksuste komplekt

| Field Service  | Supply Chain Management                 |
|----------------|----------------------------------------|
| arved       | Dataverse’i kliendi vabas vormis arve päised |
| invoicedetails | Dataverse’i kliendi vabas vormis arve read   |

## <a name="entity-flow"></a>Üksuse voog

Field Service’i leppe arveid saab teenuse Microsoft Dataverse andmeintegratsiooni projekti kaudu sünkroonida rakendusega Supply Chain Management. Nende arvete värskendused sünkroonitakse rakenduses Supply Chain Management vabas vormis arvetega, kui vabas vormis arvete raamatupidamisolek on **Pooleli**. Pärast vabas vormis arvete sisestamist rakenduses Supply Chain Management värskendatakse raamatupidamisolekuks **Lõpetatud**, mis tähendab, et enam ei saa sünkroonida värskendusi rakendusest Field Service.

## <a name="field-service-crm-solution"></a>Rakenduse Field Service CRM lahendus

Tabelile **Arve** on lisatud veerg **Lepingust pärinevate ridadega**. See veerg aitab tagada, et sünkroonitakse ainult lepingu arved. Väärtus on **tõene**, kui arve sisaldab vähemalt ühte lepingust pärinevat arverida.

Tabelile **Arverida** on lisatud veerg **Lepingust pärinev**. See veerg aitab tagada, et sünkroonitakse ainult lepingust loodud arveread. Väärtus on **tõene**, kui arve rida pärineb lepingust.

**Arve kuupäev** on kohustuslik väli rakenduses Supply Chain Management. Seetõttu peab veerul rakenduses Field Service enne sünkroonimist olema väärtus. Selle nõudega kooskõlla viimiseks lisatakse järgmine loogika.

- Kui veerg **Arve kuupäev** on tabelis **Arve** tühi (st kui sel puudub väärtus), seatakse selleks tänane kuupäev, kui lisatakse lepingust pärinev arve rida.
- Kasutaja saab veergu **Arve kuupäev** muuta. Ent kui kasutaja üritab lepingu arvet salvestada, saab ta äriprotsessi tõrke, kui arvel on veerg **Arve kuupäev** tühi.

## <a name="prerequisites-and-mapping-setup"></a>Eeltingimused ja vastendamise seadistamine

### <a name="in-supply-chain-management"></a>Rakenduses Supply Chain Management

Integreerimiseks tuleb seadistada arve päritolu, et eristada vabas vormis arveid rakenduses Supply Chain Management, mis on loodud lepingu arvetest rakenduses Field Service. Kui arve päritolutüüp on **Lepingu arve integratsioon**, kuvatakse **müügiarve** päises väli **Välise arve number** .

Lisaks arve päises kuvamisele, saab **Välise arve numbri** teavet kasutada, aitamaks tagada, et rakenduse Field Service lepingu arvete põhjal loodud arved filtreeritakse rakenduse Supply Chain Management sünkroonimisel rakendusega Field Service välja.

1. Avage **Müügireskontro** \> **Seadistus** \> **Arve päritolukoodid**.
2. Uue arve päritolu loomiseks valige **Uus**.
3. Sisestage väljal **Arve päritolu** arve päritolu nimi, näiteks **FS**.
4. Sisestage väljale **Kirjeldus** kirjeldus, näiteks **Field Service’i lepingu arve**.
5. Valige märkeruut **Päritolu tüübi määramine**.
6. Seadke välja **Arve päritolu tüüp** väärtuseks **Lepingu arve integratsioon**.
7. Valige **Salvesta**.

### <a name="in-the-data-integration-project"></a>Andmeintegratsiooni projektis

Ülesanne: **Arve read**  

Veenduge, et välja **Põhikonto kuvatav väärtus** vaikeväärtus rakenduses Supply Chain Management värskendatakse soovitud väärtusega sobivaks.

Malli vaikeväärtus on **401100**.

## <a name="template-mapping-in-data-integration"></a>Malli vastendamine andmete integratsioonis

Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a>Leppe arved (rakendus Field Service rakendusele Supply Chain Management): arve päised

[![Malli vastendamine arvepäiste andmete integreerimisel.](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a>Leppe arved (rakendus Field Service rakendusele Supply Chain Management): arve read

[![Malli vastendamine arve ridade andmete integreerimisel.](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]