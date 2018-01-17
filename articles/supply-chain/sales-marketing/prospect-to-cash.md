---
title: Potentsiaalne klient sularahaks
description: "See teema annab ülevaate lahendusest Potentsiaalne klient sularahaks rakenduste Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, ja Microsoft Dynamics 365 for Sales vahel."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f169b0ee20a7ca0c8d05c8bdcf2c04d411722f01
ms.openlocfilehash: ff166f89d13acbc3aefcbdb39f485881c81cb42c
ms.contentlocale: et-ee
ms.lasthandoff: 12/21/2017

---

# <a name="prospect-to-cash"></a>Potentsiaalne klient sularahaks

[!include[banner](../includes/banner.md)]

Lahendus Potentsiaalne klient sularahaks võimaldab vahetut sünkroonimist rakenduste Dynamics 365 for Finance and Operations, Enterprise Edition, ja Dynamics 365 for Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales vahel. Andmete edastamise ajal rakenduste Finance and Operations ja Sales vahel saate teha Salesis müügi- ja turundustegevusi ning täita Finance and Operationsis varude halduse abil tellimusi.

Lahenduse Potentsiaalne klient sularahaks praegune versioon pakub vahetu sünkroonimise järgmisi tüüpe.

- [Kontode haldamine rakenduses Sales ja nende sünkroonimine rakendusest Sales rakendusega Finance and Operations.](accounts-template-mapping-direct.md)
- [Toodete haldamine rakenduses Finance and Operations ja nende vahetu sünkroonimine rakendusega Sales](products-template-mapping-direct.md)
- [Kontaktide haldamine rakenduses Sales ja nende vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega](contacts-template-mapping-direct.md)
- [Rakenduse Sales müügipakkumise vahetu sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Müügitellimuste vahetu sünkroonimine rakendusest Finance and Operations rakendusega Sales](sales-order-template-mapping-direct.md)
- [Müügitellimuste vahetu sünkroonimine rakenduse Finance and Operations ja rakenduse Sales vahel](sales-order-template-mapping-direct-two-ways.md)
- [Rakenduse Finance and Operations müügiarvete vahetu sünkroonimine rakendusega Sales](sales-invoice-template-mapping-direct.md)

Lahenduse Potentsiaalne klient sularahaks varasemad versioonid pakuvad mittevahetu sünkroonimise järgmisi tüüpe.

- [Kontode haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations.](accounts-template-mapping.md)
- [Klientide haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations](contacts-template-mapping.md)
- [Toodete haldamine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales](products-template-mapping.md)
- [Müügipakkumiste loomine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations](sales-quotation-template-mapping.md)
- [Müügitellimuste loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales](sales-order-template-mapping.md)
- [Müügiarvete loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Rakenduse Finance and Operations süsteeminõuded

Lahenduse Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmised komponendid.

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017) platvormivärskendusega 8 (rakenduse järk 7.2.11792.56024 platvormi järguga 7.0.4565.16212)
- Nõutavad on järgmised kiirparandused.

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Sales rakendusse Finance and Operations andmete integratsiooni funktsiooni kaudu. See pakub ka mitmesuguseid muid täiustusi.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse rea sünkroonimist rakendusest Finance and Operations rakendusse Sales andmete integratsiooni funktsiooni kaudu.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Finance and Operations rakendusse Sales andmete integratsiooni funktsiooni kaudu.

    > [!NOTE]
    > KB4045570 tuleb installida ainult sellepärast, et installifail sisaldab muudatusi muudest kiirparandustest. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016) 

- Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016) platvormivärskendusega 8 või uuemaga

- Nõutavad on järgmised kiirparandused.

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – müügitellimuse sünkroonimine andmete integraatori abil rakendusest Finance and Operations rakendusse Sales. 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – müügitellimuse päise ja ridade sünkroonimine andmete integraatori abil rakendusest Finance and Operations rakendusse Sales.
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – vajalik on tugi lahenduse Potentsiaalne klient sularahaks integreerimiseks andmeüksuste kaudu.
    
    > [!NOTE]
    > Pärast kiirparanduste installimist peate vormilt **SalesPopulateProspectToCash** käivitama järgmise pakett-töö. See vorm on peidetud, kuna teil on seda vaja ainult üks kord. Vormile juurdepääsuks logige keskkonda sisse ja lisage oma brauseri aadressiribale järgmine URL: &mi=action:SalesPopulateProspectToCash, näiteks https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash. Vormi avanemisel klõpsake OK. See täidab tabelites **SalesLine**, **SalesQuotationLine** ja **CustInvoiceTrans** uue välja **LineCreationSequnceNumber** kordumatute väärtustega ja värskendab tooteloendit. See on vajalik lahenduse Potentsiaalne klient sularahaks integratsiooni toimimiseks.


## <a name="system-requirements-for-sales"></a>Rakenduse Sales süsteeminõuded

Lahenduse Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmised komponendid.

- Rakenduse Dynamics 365 for Sales versiooni 1612 (8.2.1.207) (DB 8.2.1.207) veebiversioon
- Lahendus Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Lahenduses Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.14.1.0, toetatakse malle versiooniga 1.0.0.0 ja 1.0.0.1
   >
   > Lahenduses Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.15.0.0, toetatakse malle versiooniga 2.0.0.0 ja 2.1.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>Installige lahendus Potentsiaalne klient sularahaks rakendusele Sales

1. Laadige alla [lahenduse Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales paketi ZIP-fail](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSource’ist.
2. Veenduge, et ZIP-fail oleks blokeerimata. Vastasel juhul, kui proovite lahendusepaketti installida, võidakse kuvada järgmine tõrketeade: „Impordipakette ei leitud.” ZIP-faili blokeeringu tühistamiseks paremklõpsake sellel ja valige **Atribuudid**. Valige **Tühista blokeerimine**.
3. Pakkige lahti **PackageDeployer.exe** ja käivitage see.
4. Installige lahendus Potentsiaalne klient sularahaks oma rakenduse Sales eksemplari.

    1. Valige juurutuse tüübiks **Office 365**.
    2. Valige **Kuva täpsem**.
    3. Kiirinstallimiseks valige regioon. Kui valite **Ei tea**, otsib süsteem kõiki regioone ja installimine võtab kauem aega.
    4. Sisestage installimise õigustega administraatorist kasutaja kasutajanimi ja parool.

