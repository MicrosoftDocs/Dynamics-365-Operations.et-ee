---
title: Integreeritud klientide koond
description: Selles teemas kirjeldatakse kliendiandmete integreerimist rakenduse Finance and Operations ja teenuse Dataverse vahel.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b7e9cd27bb918dc3a6088b45803329deb01a864e
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744397"
---
# <a name="integrated-customer-master"></a>Integreeritud kliendi koondandmed

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Kliendiandmeid saab luua rohkem kui ühes Dynamics 365 rakenduses. Näiteks kliendirida võib pärineda Dynamics 365 Salesi müügitegevusest (mudeljuhitud Dynamics 365 rakendus) või Dynamics 365 Commerce'i jaemüügi tegevusest (Finance and Operationsi rakendus). Olenemata sellest, kust kliendiandmed pärinevad, on see integreeritud kulisside taga. Integreeritud kliendi koondandmed annavad teile paindlikkuse luua kliendiandmeid kõigis Dynamics 365 rakendustes ja põhjaliku ülevaate kliendi kohta Dynamics 365 rakenduse komplektis.

## <a name="customer-data-flow"></a>Kliendiandmete voog

*Klient* on rakendustes täpselt määratletud mõiste. Seetõttu hõlmab kliendiandmete integreerimine lihtsalt kliendikontseptsiooni ühtlustamist kahe rakenduse vahel. Järgmine illustratsioon näitab kliendiandmete voogu.

![Kliendiandmete voog](media/dual-write-customer-data-flow.png)

Kliente saab laias laastus liigitada kahte tüüpi: äri-/organisatsioonikliendid ning tarbijad/lõppkasutajad. Neid kahte tüüpi kliente talletatakse ja käsitletakse rakendustes Finance and Operations ja Dataverse erinevalt.

Rakenduses Finance and Operations luuakse nii äri-/organisatsioonikliendid kui ka tarbijad/lõppkasutajad ühed tabelis nimetusega **CustTable** (CustCustomerV3Entity) ja neid liigitatakse atribuudi **Tüüp** järgi. (Kui atribuudiks **Tüüp** on määratud **Organisatsioon**, on klient äri-/organisatsiooniklient, ja kui atribuudiks **Tüüp** on määratud **Isik**, on klient tarbija/lõppkasutaja.) Esmase kontaktisiku teavet töödeldakse tabeli SMMContactPersonEntity kaudu.

Rakenduses Dataverse luuakse äri-/organisatsioonikliendid tabelis Konto ja tuvastatakse klientidena, kui atribuudiks **Seose tüüp** on määratud **Klient**. Nii tarbijaid/lõppkasutajaid kui ka kontaktisikut esindab tabel Kontakt. Et tagada tarbija/lõppkasutaja ja kontaktisiku selge eristamine, on tabelil **Kontakt** loogikalipp nimega **Müüdav**. Kui **Müüdav** on **Tõene**, on kontakt tarbija/lõppkasutaja ja selle kontakt jaoks saab luua pakkumisi ja tellimusi. Kui **Müüdav** on **Väär**, on kontakt vaid kliendi esmane kontaktisik.

Kui mittemüüdav kontakt osaleb pakkumise või tellimuse toimingus, on atribuudiks **Müüdav** määratud **Tõene**, et märkida kontakt lipuga müüdava kontaktina. Kontakt, kes on saanud müüdavaks kontaktiks, jääb müüdavaks kontaktiks.

## <a name="templates"></a>Mallid

Kliendiandmed sisaldavad kogu teavet kliendi kohta (nt. kliendigrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil ja püsikliendi olek). Tabeli vastenduste kogum toimib koos kliendiandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operations rakendused | Muud Dynamics 365 rakendused         | Kirjeldus
----------------------------|---------------------------------|------------
CDS-i kontaktid V2             | kontaktid                        | See mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.
Kliendigrupid             | msdyn_customergroups            | See mall sünkroonib kliendigrupi teabe.
Kliendi makseviis     | msdyn_customerpaymentmethods    | See mall sünkroonib kliendi makseviisi teabe.
Kliendid V3                | kontod                        | See mall sünkroonib äri-ja organisatsiooniklientide kliendi koondteabe.
Kliendid V3                | kontaktid                        | See mall sünkroonib tarbijate ja lõppkasutajate kliendi koondandmed.
Nime liited                | msdyn_nameaffixes               | See mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.
CDS V2 maksepäeva read    | msdyn_paymentdaylines           | See mall sünkroonib nii klientide kui ka hankijate maksepäeva ridade viiteandmed.
CDS-i maksepäevad            | msdyn_paymentdays               | See mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.
Maksegraafiku read      | msdyn_paymentschedulelines      | Sünkroonib nii klientide kui ka hankijate maksegraafiku ridade viiteandmed.
Maksegraafik            | msdyn_paymentschedules          | See mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.
Maksetingimused            | msdyn_paymentterms              | See mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]
