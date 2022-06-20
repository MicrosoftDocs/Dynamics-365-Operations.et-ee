---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (6. september 2021)
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 6. septembril 2021.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 776498b32f8323b1a06f39b518cdc1ae534f9bcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872148"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (6. september 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on Microsoftis uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4443.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Luba puudumiste halduril puhkusi hallata | [Luba puudumiste halduril puhkusi hallata](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Selle väljalaskega värskendame puudumiste halduri tööruumi vaadet. Lisateavet vt jaotisest [Puudumiste halduri konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Manustamisnõuete seadistamine puhkuse tüübi kohta | [Manustamisnõuete seadistamine puhkuse tüübi kohta](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Puhkuseühikute konfigureerimine puhkusetüübi järgi | [Puhkuseühikute konfigureerimine puhkusetüübi järgi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle pärast selle artikli algset avaldamist koostesse.

| Väljaande number | Probleem | Kirjeldus |
|---|---|---|
| 610128 | Viga andmete avaldamisel HcmDiscussionOverallCommentEntity kasutamisel | Kui andmed avaldatakse Exceli töövihikust HcmDiscussionOverralCommentEntity olemisse, ilmneb järgmine tõrge: "Ei leia tüübi HcmTopicOverrall andmeallika kirjet." |
| 589073 | EEO-1 aruanne loeb "Mitte-spetsiifilised" ja tühjad väärtused **Sugu** väljale väärtuseks "Naine". | Kui väljale **Sugu** pole määratud **Mees**, genereerib EEO-1 aruanne vaikeväärtuse **Naine**. |
| 589617 | Eemalolekuaja kaardi saldot, Ostmiseks saadaval ja Müümiseks saadaval saldosid ei kuvata, kui kasutaja rollid on piiratud konkreetse juriidilise olemiga. | Kui kasutaja (töötaja roll) on piiratud kindla juriidilise olemiga, ei kuvata saldosid õigesti kaardil **Eemalolekuaja Saldod** ja väljadel **Ostmiseks saadaval** ning **Müümiseks saadaval**. |
| 604310 | Puudumise halduri vahekaart tuleks peita, kui kasutajale pole määratud puudumishierarhiat. | Konkreetse juriidilise isiku puhul peaks vahekaart **Puudumiste majandaja** olema iseteenindusportaalis peidetud, välja arvatud juhul, kui ettevõtteülene parameeter on lubatud ja kasutajaga on seotud vähemalt üks puudumise hierarhia. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
|---|---|---|
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md) |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Lubage töötajate märkimine kui valmis maksmiseks | [Lubage töötajate märkimine kui valmis maksmiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Maksmiseks valmis](/dynamics365/human-resources/hr-compensation-payroll) |
| Kohandatud väljad jaotises Sobilikkus |[Kohandatud väljade tugi kõlblikkuse töötlemises](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Kohandatud väljade kasutamine kõlblikkuse töötlemises](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funktsioon | Details |
|---|---|
| Platvormi värskendus 10.0.21 (45) | Platvormi värskendus 10.0.21 välja laskmine on kavandatud algama teenuseväljalaskega 4. oktoobril 2021. Lisateavet vt Platvormi värskendustest [versioonile 10.0.21 Finance and Operations rakendustest (oktoober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Soodustuste avaldus | Eeliste avaldus töötaja praeguste eeliste valimiste vaatamiseks. Lisateabe saamiseks vaadake väljalaskelaine dokumendist [Eeliste avaldus](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement). |

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
