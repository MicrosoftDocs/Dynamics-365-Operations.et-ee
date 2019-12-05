---
title: Integreeritud klientide koond
description: Selles teemas kirjeldatakse kliendiandmete integreerimist Finance and Operationsi ja Common Data Service'i vahel.
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
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769679"
---
# <a name="integrated-customer-master"></a>Integreeritud klientide koond

[!include [banner](../includes/banner.md)]

Kliendikirjete loomine mitmes rakenduses on tavaline. Näiteks võib müügitegevus tuua ärikliendi kirjeid rakenduse Sales kaudu ja e-kaubandus või jaemüük võivad tuua kliendikirjeid rakenduse Finance and Operations kaudu. Olenemata sellest, kust kliendikirje pärineb, on see integreeritud kulisside taga üle rakenduste piiride ja taristute erinevuste. Integreeritud klientide loomine aitab käsitleda mitut loodud stsenaariumi ja annab põhjaliku kliendivaate Dynamics 365 rakenduse komplektile.

## <a name="customer-data-flow"></a>Kliendiandmete voog

*Klient* on rakendustes täpselt määratletud mõiste. Seetõttu hõlmab kliendiandmete integreerimine lihtsalt kliendikontseptsiooni ühtlustamist kahe rakenduse vahel. Järgmine illustratsioon näitab kliendiandmete voogu.

![Kliendiandmete voog](media/dual-write-customer-data-flow.png)

Kliente saab laias laastus liigitada kahte tüüpi: äri-/organisatsioonikliendid ning tarbijad/lõppkasutajad. Neid kahte tüüpi kliente talletatakse ja käsitletakse rakendustes Finance and Operations ja Common Data Service erinevalt.

Rakenduses Finance and Operations luuakse nii äri-/organisatsioonikliendid kui ka tarbijad/lõppkasutajad ühed tabelis nimetusega **CustTable** (CustomerCustomerV3Entity) ja neid liigitatakse atribuudi **Tüüp** järgi. (Kui atribuudiks **Tüüp** on määratud **Organisatsioon**, on klient äri-/organisatsiooniklient ja kui atribuudiks **Tüüp** on määratud **Isik**, on klient tarbija/lõppkasutaja.) Esmase kontaktisiku teavet töödeldakse olemi SMMContactPersonEntity kaudu.

Rakenduses Common Data Service luuakse äri-/organisatsioonikliendid olemis Konto ja tuvastatakse klientidena, kui atribuudiks **Seose tüüp** on määratud **Klient**. Nii tarbijaid/lõppkasutajaid kui ka kontaktisikut esindab olem Kontakt. Et tagada tarbija/lõppkasutaja ja kontaktisiku selge eristamine, on olemil**Kontakt** loogikalipp nimega **Müüdav**. Kui **Müüdav** on **Tõene**, on kontakt tarbija/lõppkasutaja ja selle kontakt jaoks saab luua pakkumisi ja tellimusi. Kui **Müüdav** on **Väär**, on kontakt vaid kliendi esmane kontaktisik.

Kui mittemüüdav kontakt osaleb pakkumise või tellimuse toimingus, on atribuudiks **Müüdav** määratud **Tõene**, et märkida kontakt lipuga müüdava kontaktina. Kontakt, kes on saanud müüdavaks kontaktiks, jääb müüdavaks kontaktiks.

## <a name="templates"></a>Mallid

Kliendiandmed sisaldavad kogu teavet kliendi kohta (nt. kliendigrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil ja püsikliendi olek). Olemikaartide kogum toimib koos kliendiandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operationsi rakendused | Muud Dynamics 365 rakendused         | Kirjeldus
----------------------------|---------------------------------|------------
CDS-i kontaktid V2             | kontaktid                        | See mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.
Kliendigrupid             | msdyn_customergroups            | See mall sünkroonib kliendigrupi teabe.
Kliendi makseviis     | msdyn_customerpaymentmethods    | See mall sünkroonib kliendi makseviisi teabe.
Kliendid V3                | kontod                        | See mall sünkroonib äri-ja organisatsiooniklientide kliendi koondteabe.
Kliendid V3                | kontaktid                        | See mall sünkroonib tarbijate ja lõppkasutajate kliendi koondandmed.
Kliendikaart                | msdyn_loyaltycards              | See mall sünkroonib kliendikaardi teabe.
Nime liited                | msdyn_nameaffixes               | See mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.
CDS V2 maksepäeva read    | msdyn_paymentdaylines           | See mall sünkroonib nii klientide kui ka hankijate maksepäeva ridade viiteandmed.
CDS-i maksepäevad            | msdyn_paymentdays               | See mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.
Maksegraafiku read      | msdyn_paymentschedulelines      | Sünkroonib nii klientide kui ka hankijate maksegraafiku ridade viiteandmed.
Maksegraafik            | msdyn_paymentschedules          | See mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.
Maksetingimused            | msdyn_paymentterms              | See mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
