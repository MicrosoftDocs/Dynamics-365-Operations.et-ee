---
title: Potentsiaalne klient sularahaks
description: "See teema annab ülevaate lahendusest Potentsiaalne klient sularahaks rakenduste Dynamics 365 for Finance and Operations, Enterprise edition, ja Dynamics 365 for Sales vahel."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a>Potentsiaalne klient sularahaks  

[!include[banner](../includes/banner.md)]

Lahendus Potentsiaalne klient sularahaks kasutab [andmete integratsiooni](/common-data-service/entity-reference/dynamics-365-integration), et sünkroonida andmeid rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, ja Dynamics 365 for Sales eksemplarides teenuse Common Data Service (CDS) kaudu. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Dynamics 365 for Finance ja Operations and Dynamics 365 for Sales vahel. Andmete edastamise ajal rakenduste Finance and Operations ja Sales vahel saate teha Salesis müügi- ja turundustegevusi ning täita Finance and Operationsis varude halduse abil tellimusi. 

See lahendus võimaldab integratsiooni järgmistes valdkondades. 

-   [Kontode haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations.](accounts-template-mapping.md)
-   [Kontaktide haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations.](contacts-template-mapping.md)
-   [Toodete haldamine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales.](products-template-mapping.md)
-   [Müügipakkumiste loomine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping.md)
-   [Müügitellimuste loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales](sales-order-template-mapping.md)
-   [Müügiarvete loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Dynamics 365 for Finance and Operations, Enterprise Editioni süsteeminõuded

Lahenduse Lahendus Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmine.

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juuli 2017) platvormivärskendusega 8 (rakendus 7.2.11792.56024 platvormiga 7.0.4565.16212)

- Kaks kiirparandust rakendusele Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017).

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – see kiirparandus võimaldab müügitellimuse rea sünkroonimist andmete integratsiooni funktsiooniga rakendusest Finance and Operations rakendusse Sales.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – see kiirparandus võimaldab müügitellimuse sünkroonimist andmete integratsiooni funktsiooniga rakendusest Finance and Operations rakendusse Sales.
    
**Märkus**. KB4036524 tuleb installida ainult sellepärast, et installifail sisaldab muudatusi versioonist KB4036461.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Rakenduse Dynamics 365 for Sales süsteeminõuded

Lahenduse Lahendus Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmine.

- Rakenduse Dynamics 365 for Sales versiooni 1612 (8.2.1.207) (DB 8.2.1.207) veebiversioon või hilisem.
- Lahendus Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.14.0.0 (v14) või hilisem.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installige lahendus Potentsiaalne klient sularahaks rakendusele Sales

- Laadige alla [lahenduse Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales paketi ZIP-fail](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSource’ist.

- Veenduge, et ZIP-fail poleks blokeeritud, et te ei saaks lahendusepaketi installimisel tõrketeadet „Impordipakette ei leitud”. Faili blokeeringu tühistamiseks tehke järgmist.

    -  Paremklõpsake ZIP-faili.
    -  Valige **Atribuudid** ja seejärel valige **Tühista blokeering**. 

- Pakkige lahti PackageDeployer.exe ja käivitage see.

- Installige lahendus Potentsiaalne klient sularahaks oma rakenduse Sales eksemplari.

    - Valige juurutuse tüüp **Office 365**.
    - Valige **Kuva täpsem**.
    - Kiirinstallimiseks valige **Regioon**. Kui valite **Ei tea**, otsib süsteem kõiki regioone ja installimine võtab kauem aega.
    - Sisestage installimise kasutajaõigustega administraatorist kasutaja **Kasutajanimi** ja **Parool**.

