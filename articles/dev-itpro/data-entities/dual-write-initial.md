---
title: Finance and Operationsi ja teenuse Common Data Service algse sünkroonimise täitmise järjestus
description: See teema määrab sünkroonimise järjestuse, mida peate esialgsete andmete loomiseks järgima.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797294"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a>Finance and Operationsi ja teenuse Common Data Service algse sünkroonimise täitmise järjestus

Enne andmete integratsiooni kasutamist peate looma algsed andmed, mis on vajalikud klientide, hankijate ja kontaktide jaoks. Näiteks kui soovite luua uue üksuse **Hankija rühm** ja sätestada selle **Maksetingimused** väärtuses **Net30**, siis enne, kui proovite luua üksuse **Hankija rühm**, peate veenduma, et **Net30** on olemas nii teenustes Finance and Operations kui ka Common Data Service. (Tulevikus anname välja kahesuguse kirjutamise platvormi funktsionaalsuse nimega **Algne sünkroonimine**. See teeb ühekordse andmete sünkroonimise teenustes Finance and Operationsi ja Common Data Service topeltkirjutamise seadistuse osana.)

Näpunäited: me anname välja topeltkirjutamise kaardi kõigi viiteandmete jaoks, sealhulgas **Maksetingimused** (Maksetingimused). Kui teil on juba esialgsed andmed ühes süsteemis, võib väike värskenduse toiming kirjel käivitada selle kirje topeltkirjutamise. 

Peate järgima tellimuse tehtejärjestust ja veenduma, et esialgsed andmed on saadaval nii Finance and Operationsis kui ka teenuses Common Data Service.   

## <a name="vendor"></a>Tarnija

Müüja täitmise järjekord on:

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a>Kliendi organisatsioon

Hankija täitmise järjestus on:

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a>Kontaktisik

Kontakti täitmise järjekord on:

```
Customer
Vendor               
```
