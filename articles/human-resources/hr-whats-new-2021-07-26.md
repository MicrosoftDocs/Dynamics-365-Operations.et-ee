---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (26. juuli 2021)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 26. juuli 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4e124655ca96e34e53723ea2608227661034d58b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694707"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (26. juuli 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4384.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Platvormivärskendus update 10.0.20 | -- | [Platvormi värskendused versioonile 10.0.20 finantside ja toimingute rakendustele (august 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 600422 | Maksevalmis palgaarvestuse aadressi kinnitamine ebaõnnestus. | Kinnitamist värskendati, et nõuda ainult üht aadressi, mille tüüp on 'Palgaarvestuse asukoht' ja ainult üks aadress tüübiga 'Palgatöö asukoht'. |
| 601226 | Andmete integreerimise probleem: palga integreerimise ekspordiprojektil pole valikut täielikuks tõukamiseks | Palga integratsioon Ceridani DayForce'iga tegi täiskoormuse asemel astmelist tõukamist. Ceridian nõuab alati täielikku värskendamist. Probleem on nüüd parandatud, andmeekspordiprojekti üksused ei pööra enam astmelisele tõukele. |
| 602272 | Töötaja iseteeninduse tööruumi lisatud paanid puuduvad ja paanisid ei saa enam sellele lisada | Töötaja iseteeninduse isikupärastamise probleemi on fikseeritud. Vaatesse saab lisada uusi paane ja mis tahes olemasoleva isikupärastamine on kasutajatele nähtav |
| 600711 | Pool päeva määratluse valikuväli on täispäeva puhkuse taotluste puhul lubatud | See probleem on nüüd fikseeritud ja pool päeva määratlusväli lubatakse ainult siis, kui töötajad valivad puhkuse tüübi, mille poole päeva definitsioon on lubatud, ja pool päeva valitud summaväärtusena |
| 602208 | Tekkepõhise määra ühikud, mis kuvavad päevade asemel tunde | See probleem on nüüd lahendatud. Vorm **Vaba aeg** vormis kuvatakse viit võlamäära veeru (tunnid või päevad) **õige puhkuseühik** jaoks. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md)|
|  Luba puudumiste halduril puhkusi hallata | [Luba puudumiste halduril puhkusi hallata](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Selle väljalaskega värskendame puudumiste halduri tööruumi vaadet. Lisateavet vt jaotisest [Puudumiste halduri konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Manustamisnõuete seadistamine puhkuse tüübi kohta | [Manustamisnõuete seadistamine puhkuse tüübi kohta](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Puhkuseühikute konfigureerimine puhkusetüübi järgi | [Puhkuseühikute konfigureerimine puhkusetüübi järgi](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Puhkuste ja puudumiste tüüpide konfigureerimine](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Lubage töötajate märkimine kui valmis maksmiseks | [Lubage töötajate märkimine kui valmis maksmiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Maksmiseks valmis](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2021. aasta väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
