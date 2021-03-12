---
title: Potentsiaalne klient sularahaks
description: Selles teemas antakse ülevaade lahendusest Prospect to cash rakenduste Dynamics 365 Supply Chain Management ja Dynamics 365 Sales vahel.
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: b2f2f7d95d3f0e6bd774c43024836aac1f729abd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977634"
---
# <a name="prospect-to-cash"></a>Potentsiaalne klient sularahaks

[!include [banner](../includes/banner.md)]

Lahendus Prospect to cash võimaldab otsest sünkroonimist rakenduste Dynamics 365 Supply Chain Management ja Dynamics 365 Sales vahel. Andmete integratsiooniga saadaolevad lahenduse Prospect to cash mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist. Andmete edastamise ajal saate teha Salesis müügi- ja turundustegevusi ning täita Supply Chain Managementis varude halduse abil tellimusi. 

Lisateabe saamiseks lahenduse Potentsiaalne klient sularahaks kohta vaadake YouTube’i lühivideot: [Lahenduse Potentsiaalne klient sularahaks integreerimine](https://www.youtube.com/watch?v=AVV9x5x-XCg).

Lahenduse Potentsiaalne klient sularahaks praegune versioon pakub vahetu sünkroonimise järgmisi tüüpe.

- [Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega](accounts-template-mapping-direct.md)
- [Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega](products-template-mapping-direct.md)
- [Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega](contacts-template-mapping-direct.md)
- [Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales](sales-quotation-template-mapping-sales-fin.md)
- [Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel](sales-order-template-mapping-direct-two-ways.md)
- [Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Süsteemi nõuded rakendusele Supply Chain Management
Lahendust Potentsiaalne klient sularahaks toetatakse järgmistel versioonidel.

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (detsember 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (detsember 2017) – rakenduse järk 7.3.11971.56116 platvormivärskendusega 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017) – platvormivärskendusega 8 (rakenduse järk 7.2.11792.56024 platvormijärguga 7.0.4565.16212).
- Nõutavad on järgmised kiirparandused.

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Sales rakendusse Supply Chain Management andmete integratsiooni funktsiooni kaudu. See pakub ka mitmesuguseid muid täiustusi.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Supply Chain Management rakendusse Sales andmete integratsiooni funktsiooni kaudu.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Supply Chain Management rakendusse Sales andmete integratsiooni funktsiooni kaudu.

    > [!NOTE]
    > KB4045570 tuleb installida ainult sellepärast, et installifail sisaldab muudatusi muudest kiirparandustest. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016)

- Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016) platvormivärskendusega 8 või uuem

- Nõutavad on järgmised kiirparandused.

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – müügitellimuse sünkroonimine andmete integraatori abil rakendusest Supply Chain Management rakendusse Sales. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – müügitellimuse sünkroonimine andmete integraatori abil rakendusest Supply Chain Management rakendusse Sales.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – vajalik on tugi lahenduse Potentsiaalne klient sularahaks integreerimiseks andmeüksuste kaudu.
    
    > [!NOTE]
    > Pärast kiirparanduste installimist peate vormilt **SalesPopulateProspectToCash** käivitama järgmise pakett-töö. See vorm on peidetud, kuna teil on seda vaja ainult üks kord. Vormile juurdepääsu saamiseks logige keskkonda sisse ja lisage oma brauseri aadressile järgmine URL: *&mi=action:SalesPopulateProspectToCash*, näiteks `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Vormi avanemisel klõpsake OK. See täidab tabelites **SalesLine**, **SalesQuotationLine** ja **CustInvoiceTrans** uue välja **LineCreationSequnceNumber** kordumatute väärtustega ja värskendab tooteloendit. See on vajalik lahenduse Potentsiaalne klient sularahaks integratsiooni toimimiseks.


## <a name="system-requirements-for-sales"></a>Rakenduse Sales süsteeminõuded

Lahenduse Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmised komponendid.

- Rakenduse Dynamics 365 Sales versiooni 1612 (8.2.1.207) (DB 8.2.1.207) veebiversioon või hilisem versioon
- Lahendus Prospect to cash (P2C) rakendusele Dynamics 365, versioon 1.15.0.0 või hilisem versioon. Lahendus on allalaadimiseks saadaval AppSource’is. [Lahenduse Dynamics 365, Potentsiaalne klient sularahaks allalaadimine](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
