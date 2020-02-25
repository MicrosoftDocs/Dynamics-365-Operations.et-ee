---
title: Integreeritud hankija koondandmed
description: Selles teemas kirjeldatakse hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
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
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019734"
---
# <a name="integrated-vendor-master"></a>Integreeritud hankija koondandmed

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Termin *hankija* viitab tarnijariigi organisatsioonile või ainuomanikule, kes on tarneahela protsessi osa ja tarnib ettevõttele kaupu. Kuigi *hankija* on loodud mõiste teenusekomplekti Finance and Operations rakendustes, pole teistes Dynamics 365 rakendustes mõistet hankija olemas. Selle asemel on mõned ettevõtted olemi Konto üle koormanud nii kliendi- kui ka hankijateabega. Teised ettevõtted kasutavad kohandatud hankija mõistet. Common Data Service'i integratsioon toetab mõlemat lahendust. Seetõttu saate olenevalt oma äristsenaariumist lubada ühe neist lahendustest.

Hankija andmete integreerimine Finance and Operationsi rakenduste ja teiste Dynamics 365 rakenduste vahel võimaldab teil hankida mitmeid koondandmeid. Olenemata sellest, kust hankijaandmed pärinevad, on need integreeritud kulisside taga üle rakenduste piiride ja taristute erinevuste. 

### <a name="vendor-data-flow"></a>Hankijaandmete voog

Kui soovite kasutada hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite isoleerida hankijateabe klienditeabest, saate kasutada uut hankijalahendust.

![Hankijaandmete voog](media/dual-write-vendor-data-flow.png)

Kui soovite kasutada hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite hankijaandmete salvestamiseks jätkata olemi Konto kasutamist, saate kasutada uut, laiendatud hankijalahendust. Selles lahenduses on hankija üksikasjadesse talletatud laiendatud hankijateave (nt hankijagrupp ja hankija sisestuse profiil).

![Hankijaandmete laiendatud voog](media/dual-write-vendor-detail.jpg)

Hankija kontaktteave meenutab kliendi kontaktteavet. Kulisside taga talletatakse kontaktisiku teave ja tuuakse need samadest üksustest.

## <a name="templates"></a>Mallid

Hankijaandmed sisaldavad kogu teavet hankija kohta (nt hankijagrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil). Olemikaartide kogum toimib koos hankijaandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operations rakendused | Muud Dynamics 365 rakendused         | Kirjeldus
----------------------------|---------------------------------|------------
Hankija V2               | Konto | Ettevõtted, mis kasutavad hankija teabe talletamiseks olemit Konto, saavad jätkata selle kasutamist samal viisil. Nad saavad Finance and Operationsi rakenduste integratsiooni tõttu kasutada ka konkreetseid hankijafunktsioone.
Hankija V2               | Msdyn\_vendors | Ettevõtted, mis kasutavad hankijate jaoks kohandatud lahendusi, saavad kasutada valmislahendusena hankija eeliseid, mis on Finance and Operationsi rakenduste integratsiooni tõttu juurutatud teenuses Common Data Service. 
Hankijagrupid | msdyn_vendorgroups | See mall sünkroonib hankijagrupi teabe.
Tarnija makseviis | msdyn_vendorpaymentmethods | See mall sünkroonib hankija makseviisi teabe.
CDS-i kontaktid V2             | kontaktid                        | [Kontaktide](customer-mapping.md#cds-contacts-v2-to-contacts) mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.
Maksegraafiku read      | msdyn_paymentschedulelines      | [Maksegraafiku ridade](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) mall sünkroonib klientide ja hankijate viiteandmed.
Maksegraafik            | msdyn_paymentschedules          | [Maksegraafikute](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.
CDS V2 maksepäeva read    | msdyn_paymentdaylines           | [Maksepäeva ridade](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) mall sünkroonib klientide ja hankijate maksepäeva ridade viiteandmed.
CDS-i maksepäevad            | msdyn_paymentdays               | [Maksepäevade](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.
Maksetingimused            | msdyn_paymentterms              | [Maksetingimuse](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.
Nime liited                | msdyn_nameaffixes               | [Nimeliidete](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
