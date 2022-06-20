---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (9. august 2021)
description: See artikkel kirjeldab funktsioone, mis on kas uued või Microsoftis Dynamics 365 Human Resources muudetud 9. augustil 2021.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad1397084dd3eb210065fe6d8c20c5b8253cd206
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882862"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (9. august 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on Microsoftis uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4393.

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle pärast selle artikli algset avaldamist koostesse.

| Väljaande number | Probleem | Kirjeldus |
| --- | --- | --- |
| 558385 | Vaikimisi volitatud isikut ei valita, kui suvand **Automaatne volitatud isikute valimine** on vaikimisi volitatud isikute jaoks sisse lülitatud. | See probleem on nüüd lahendatud. Sobivates plaanides valitakse automaatselt mitu vaikimisi volitatud isikut, kui suvand **Automaatne volitatud isikute valimine** lehel **Inimressursside jagatud parameetrid** on sisse lülitatud. |
| 589617 | Lehel **Vaba aeg** on saldod **Ostmiseks saadaval** ja **Müümiseks saadaval** tühjad, kui juurdepääs teatud ettevõttele on piiratud. | See probleem on nüüd lahendatud. Lehel **Vaba aeg** kuvatakse õigeid saldosid **Ostmiseks saadaval** ja **Müümiseks saadaval**, kui kasutaja on piiratud teatud ettevõttega. |

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
