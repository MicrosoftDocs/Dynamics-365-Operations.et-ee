---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. august 2021)
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 23. augustil 2021.
author: marcelbf
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 91c2cd396ca26cc78c3fd4fab40a29b98a7826c3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909726"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. august 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on Microsoftis uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4419.

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle pärast selle artikli algset avaldamist koostesse.

| Väljaande number | Probleem | Kirjeldus |
| --- | --- | --- |
| 594066 | Kontaktteavet ei saa kustutada | Kui valite töötaja kontaktteabe kirje kustutamise, kustutatakse selle asemel kontaktteabe kirje, mis pole valitud kirje. |
| 611339 | Isikupärastamise lisamisel ignoreerib pangakonto filtrit ja toob esimese kirje | Isikupärastamise lisamisel käivitab pangakonto loend isikupärastamispäringu pärast andmeallika päringu käivitamist, mille tulemuseks on ülemise kirje toomine, hoolimata töötajast, kelle andmeid vaadatakse. |
| 591806 | Põhitähtaegades olevad ülesanded on valesti arvutatud | Tähtajad arvutatakse valesti järgmiste tingimuste olemasolul: loodud kontroll-loendid kasutavad kalendrit, mis kasutab laiendatud ajavahemikku (näide 2005 kuni 2050) ja kasutaja eelistused kasutavad muud ajavööndit kui keskstandardi aeg. |   
| 592749 | **Töötaja iseteeninduses on** puhkuse saldo vale | Kui töötaja töötab rohkem kui ühes juriidilises isikus ja ettevõtteülene puhkusevaade on lubatud, võib puhkuse saldo olla vale. |
| 603133 | Ootamatu hoiatus aja eemaldumisel | Vaba aja nõudes täidab **pool päeva** väli enne **Summa** välja ootamatut hoiatust. |
| 606546 | Valige väli, mis pole kinnitatud aja väljal nähtav | Mitme kinnitatud puhkusetaotluse valimiseks ei olnud märkeruut nähtav. |
| 597059 | Töötaja pole **puhkuse ja puudumiste ettevõtte kalendris** nähtav | Töötaja ei ole **puhkuse ja puudumiste ettevõtte kalendris** nähtav, kui rakendatav kuupäevavahemik sisaldab mis tahes päeva, mille jaoks neile puhkusetaotlusest keelduti. |


## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md)|
| Luba puudumiste halduril puhkusi hallata | [Luba puudumiste halduril puhkusi hallata](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Selle väljalaskega värskendame puudumiste halduri tööruumi vaadet. Lisateavet vt jaotisest [Puudumiste halduri konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Manustamisnõuete seadistamine puhkuse tüübi kohta | [Manustamisnõuete seadistamine puhkuse tüübi kohta](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Puhkuseühikute konfigureerimine puhkusetüübi järgi | [Puhkuseühikute konfigureerimine puhkusetüübi järgi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Lubage töötajate märkimine kui valmis maksmiseks | [Lubage töötajate märkimine kui valmis maksmiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Maksmiseks valmis](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktsioon | Details |
| --- | --- |
| Platvormi värskendus 10.0.21 (45) | Platvormi värskendus 10.0.21 välja laskmine on kavandatud algama teenuseväljalaskega 4. oktoobril 2021. Lisateavet vt Platvormi värskendustest [versioonile 10.0.21 Finance and Operations rakendustest (oktoober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
