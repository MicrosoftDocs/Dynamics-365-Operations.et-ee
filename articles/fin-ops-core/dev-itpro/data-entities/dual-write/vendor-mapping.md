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
ms.openlocfilehash: 8d531ed4e46d8ee5d2b0937b6efc480e051fe708
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173104"
---
# <a name="integrated-vendor-master"></a>Integreeritud hankija koondandmed

[!include [banner](../../includes/banner.md)]



Termin *hankija* viitab tarnijariigi organisatsioonile või ainuomanikule, kes tarnib ettevõttele kaupu või teenuseid. Kuigi *hankija* on loodud mõiste teenusekomplektis Microsoft Dynamics 365 Supply Chain Management, pole teistes Dynamics 365 mudeljuhitud rakendustes mõistet hankija olemas. Kuid hankija teabe talletamiseks saate ülekoormata üksuse **Konto/kontakt**. Integreeritud hankija koondandmed tutvustavad Dynamics 365 mudeljuhitud rakendustes selgesõnalist hankija mõistet. Saate kasutada kas uut hankija kujundust või talletada hankija andmeid üksuses **Konto/kontakt**. Topeltkirjutus toetab mõlemat lähenemist.

Mõlemas lähenemisviisis on hankija andmed integreeritud Dynamics 365 Supply Chain Managementi, Dynamics 365 Salesi, Dynamics 365 Field Service'i ja Power Appsi portaalide vahel. Supply Chain Managementis on andmed saadaval töövoogudele (nt ostutaotlused ja ostutellimused).

## <a name="vendor-data-flow"></a>Hankijaandmete voog

Kui te ei soovi talletada hankija andmeid Common Data Service'i üksuses **Konto/kontakt**, saate kasutada uut hankija kujundust.

![Hankijaandmete voog](media/dual-write-vendor-data-flow.png)

Kui soovite jätkata hankija andmete talletamist üksuses **Konto/kontakt**, saate kasutada laiendatud hankija kujundust. Laiendatud hankija kujunduse kasutamiseks peate konfigureerima hankija töövood topeltkirjutuse lahendusepaketis. Lisateavet vaadake teemast [Hankija kujunduste vahel vahetamine](vendor-switch.md).

![Hankijaandmete laiendatud voog](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Kui kasutate iseteeninduse hankijate Power Appsi portaale, võib hankija teave liikuda otse Finance and Operationsi rakendustesse.

## <a name="templates"></a>Mallid

Hankijaandmed sisaldavad kogu teavet hankija kohta (nt hankijagrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil). Olemikaartide kogum toimib koos hankijaandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operations rakendused | Muud Dynamics 365 rakendused     | Kirjeldus
----------------------------|-----------------------------|------------
Hankija V2                   | Konto                     | Ettevõtted, mis kasutavad hankija teabe talletamiseks olemit Konto, saavad jätkata selle kasutamist samal viisil. Nad saavad Finance and Operationsi rakenduste integratsiooni tõttu kasutada ka konkreetseid hankijafunktsioone.
Hankija V2                   | Msdyn\_vendors              | Ettevõtted, mis kasutavad hankijate jaoks kohandatud lahendusi, saavad kasutada valmislahendusena hankija eeliseid, mis on Finance and Operationsi rakenduste integratsiooni tõttu juurutatud teenuses Common Data Service. 
Hankijagrupid               | msdyn\_vendorgroups         | See mall sünkroonib hankijagrupi teabe.
Tarnija makseviis       | msdyn\_vendorpaymentmethods | See mall sünkroonib hankija makseviisi teabe.
CDS-i kontaktid V2             | kontaktid                    | [Kontaktide](customer-mapping.md#cds-contacts-v2-to-contacts) mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.
Maksegraafiku read      | msdyn\_paymentschedulelines | [Maksegraafiku ridade](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) mall sünkroonib klientide ja hankijate viiteandmed.
Maksegraafik            | msdyn\_paymentschedules     | [Maksegraafikute](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.
CDS V2 maksepäeva read    | msdyn\_paymentdaylines      | [Maksepäeva ridade](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) mall sünkroonib klientide ja hankijate maksepäeva ridade viiteandmed.
CDS-i maksepäevad            | msdyn\_paymentdays          | [Maksepäevade](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.
Maksetingimused            | msdyn\_paymentterms         | [Maksetingimuse](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.
Nime liited                | msdyn\_nameaffixes          | [Nimeliidete](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
