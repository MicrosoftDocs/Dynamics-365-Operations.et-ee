---
title: Integreeritud klientide koond
description: Selles teemas kirjeldatakse kliendiandmete integreerimist rakenduse Finance and Operations ja teenuse Dataverse vahel.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 48070628aafd7daac65327a484c87dc01ffb3954
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781686"
---
# <a name="integrated-customer-master"></a>Integreeritud kliendi koondandmed

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Kliendiandmeid saab luua rohkem kui ühes Dynamics 365 rakenduses. Näiteks kliendirida võib pärineda Dynamics 365 Salesi müügitegevusest (kliendikaasamise rakendus) või Dynamics 365 Commerce'i jaemüügi tegevusest (finants- ja tegevusrakendus). Olenemata sellest, kust kliendiandmed pärinevad, on see integreeritud kulisside taga. Integreeritud kliendi koondandmed annavad teile paindlikkuse luua kliendiandmeid kõigis Dynamics 365 rakendustes ja põhjaliku ülevaate kliendi kohta Dynamics 365 rakenduse komplektis.

## <a name="customer-data-flow"></a>Kliendiandmete voog

*Klient* on rakendustes täpselt määratletud mõiste. Seetõttu hõlmab kliendiandmete integreerimine lihtsalt kliendikontseptsiooni ühtlustamist kahe rakenduse vahel. Järgmine illustratsioon näitab kliendiandmete voogu.

![Kliendiandmete voog.](media/dual-write-customer-data-flow.png)

Kliente saab laias laastus liigitada kahte tüüpi: äri-/organisatsioonikliendid ning tarbijad/lõppkasutajad. Neid kahte tüüpi kliente talletatakse ja käsitletakse rakendustes Finance and Operations ja Dataverse erinevalt.

Rakenduses Finance and Operations luuakse nii äri-/organisatsioonikliendid kui ka tarbijad/lõppkasutajad ühed tabelis nimetusega **CustTable** (CustCustomerV3Entity) ja neid liigitatakse atribuudi **Tüüp** järgi. (Kui atribuudiks **Tüüp** on määratud **Organisatsioon**, on klient äri-/organisatsiooniklient, ja kui atribuudiks **Tüüp** on määratud **Isik**, on klient tarbija/lõppkasutaja.) Esmase kontaktisiku teavet töödeldakse tabeli SMMContactPersonEntity kaudu.

Rakenduses Dataverse luuakse äri-/organisatsioonikliendid tabelis Konto ja tuvastatakse klientidena, kui atribuudiks **Seose tüüp** on määratud **Klient**. Nii tarbijaid/lõppkasutajaid kui ka kontaktisikut esindab tabel Kontakt. Et tagada tarbija/lõppkasutaja ja kontaktisiku selge eristamine, on tabelil **Kontakt** loogikalipp nimega **Müüdav**. Kui **Müüdav** on **Tõene**, on kontakt tarbija/lõppkasutaja ja selle kontakt jaoks saab luua pakkumisi ja tellimusi. Kui **Müüdav** on **Väär**, on kontakt vaid kliendi esmane kontaktisik.

Kui mittemüüdav kontakt osaleb pakkumise või tellimuse toimingus, on atribuudiks **Müüdav** määratud **Tõene**, et märkida kontakt lipuga müüdava kontaktina. Kontakt, kes on saanud müüdavaks kontaktiks, jääb müüdavaks kontaktiks.

## <a name="templates"></a>Mallid

Kliendiandmed sisaldavad kogu teavet kliendi kohta (nt. kliendigrupp, aadressid, kontaktandmed, makseprofiil, arveprofiil ja püsikliendi olek). Tabeli vastenduste kogum toimib koos kliendiandmete suhtluse ajal, nagu on näidatud järgmises tabelis.

Finance and Operations rakendused | Klientide kaasamise rakendused         | Kirjeldus
----------------------------|---------------------------------|------------
[CDS-i kontaktid V2](mapping-reference.md#115) | kontaktid | See mall sünkroonib nii klientide kui hankijate kõik esmased, sekundaarsed ja tertsiaarsed kontaktandmed.
[Kliendigrupid](mapping-reference.md#126) | msdyn_customergroups | See mall sünkroonib kliendigrupi teabe.
[Kliendi makseviis](mapping-reference.md#127) | msdyn_customerpaymentmethods | See mall sünkroonib kliendi makseviisi teabe.
[Kliendid V3](mapping-reference.md#101) | kontod | See mall sünkroonib äri-ja organisatsiooniklientide kliendi koondteabe.
[Kliendid V3](mapping-reference.md#116) | kontaktid | See mall sünkroonib tarbijate ja lõppkasutajate kliendi koondandmed.
[Nime liited](mapping-reference.md#155) | msdyn_nameaffixes | See mall sünkroonib nii klientide kui ka hankijate nimeliidete viiteandmed.
[CDS V2 maksepäeva read](mapping-reference.md#157) | msdyn_paymentdaylines | See mall sünkroonib nii klientide kui ka hankijate maksepäeva ridade viiteandmed.
[CDS-i maksepäevad](mapping-reference.md#158) | msdyn_paymentdays | See mall sünkroonib nii klientide kui ka hankijate maksepäevade viiteandmed.
[Maksegraafiku read](mapping-reference.md#159) | msdyn_paymentschedulelines | Sünkroonib nii klientide kui ka hankijate maksegraafiku ridade viiteandmed.
[Maksegraafik](mapping-reference.md#160) | msdyn_paymentschedules | See mall sünkroonib nii klientide kui ka hankijate maksegraafiku viiteandmed.
[Maksetingimused](mapping-reference.md#161) | msdyn_paymentterms | See mall sünkroonib nii klientide kui ka hankijate maksetingimuste viiteandmed.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
