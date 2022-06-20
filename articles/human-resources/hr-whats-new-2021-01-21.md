---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 21. jaanuar 2021
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 21. jaanuariks 2021.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9f1f660b7993804901f5fc9d3b608c141882bff5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901085"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 21. jaanuar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3866.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Platform update 10.0.16(40) | -- | [Platvormi värskendused versioonile 10.0.16 finantside ja toimingute rakendustele (veebruar 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Täiustatud töövoo taotlused ja kinnitused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Taskukohase ravikindlustuse eelnõu (ACA) vastavuse värskendused vormile 1095-C, vormile 1095-B ja elektroonilisele aruandlusele pärandrakenduses Soodustused | -- | -- | 
| Soodustuste haldus toetab nüüd ACA vastavuse aruandlust USA-põhistele juriidilistele isikutele | -- | [ACA-aruannete loomine Soodustuste halduses](hr-benefits-management-aca-reports.md) |
| Soodustuste halduses on nüüd soodustusmäära tasemed ja soodustusmäära kahetasandilised üksused avatud  | -- | -- |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle järku pärast selle artikli algset avaldamist.

| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 533079 | Mahaarvamiste otsimisel ilmnes navigeerimistõrge "Vorm käivitati valesti". | Parandatud tõrge soodustuste mahaarvamiste otsimisel vaates **Kuupäevast**. |
| 543641 | Elektroonilises aruandluses ei täideta sihtnumbrit.  | Parandatud sisemine viga, mil sihtnumbrit ei kuvata ACA soodustuste halduse elektroonilistes aruannetes, kui kindlustuskaitse kood on M kuni Q. |
| 542815 | Töötaja iseteeninduse isikliku kontakti kuva võimaldab töötajatel näha teiste isiklikke kontakte. | Parandatud tõrge, kui töötaja iseteeninduse isiklike kontaktide vorm **Redigeerimine** ei piira selle päringut piisavalt, et tagada ainult ühe isikliku kontakti toomine, võimaldades kasutajal kasutada klaviatuuri otseteid teiste inimeste kontaktide vaatamiseks. |
| 536157 | Ei saa avada lehte **Microsoft Dataverse'i integratsioon** Süsteemihalduses IsVirtualEntityPackageInstalled() kutse tõttu. | Probleem takistab **Microsoft Dataverse'i integratsiooni** lehe laadimist Human Resourcesis. |
| 533079 | Mahaarvamiste otsimisel ilmnes navigeerimistõrge "Vorm käivitati valesti". | Parandatud tõrge Soodustuste halduse vormi **Mahaarvamised** kuvamisel **Kuupäevast** alusel. |
| 537264 | Kandidaadi kirjest puudub kiirkaart **Isikuandmed**. | Kandidaadi isikuandmed on nüüd kandidaadi kirjes saadaval. |
| 537267 | **Töökogemust** ei kuvata sisemistes kandidaadikirjetes. | Kiirkaarti **Töökogemus** kuvatakse nüüd sisemistes kandidaadikirjetes. Varem, kui kandidaat oli sisemine, asendati **Töökogemus** **Töösuhte ajalooga**, mis on kandidaadi töösuhte ajalugu organisatsioonis. Mõlemad on rakendatavad ja need tuleb kuvada sisemiste kandidaatide kohta. |
| 537067 | Ei kuvata valikut **Lubatud tööandjaga ühendust võtta**. | Juhtelement **Lubatud tööandjaga ühendust võtta** lisati kandidaadikirje paanile **Redigeeri töökogemust**. |
| 525957 | **Kandidaadi olekut** ei värskendata ettevõttesiseseste kandidaatide korral, kui üleviimine on lõpetatud. | Kui üleviimine on lõpetatud (nupp **Muuda ametikohta** või **Jätka** on valitud lehel **Töötaja üleviimine uuele ametikohale**), peab kandidaadikirje **Olekuks** kuvatama **Palgatud**. |
| 537051 | India ruupia ja Türgi liir valuutasümbolid ei sünkroonita õigesti rakendusse Dataverse | India ruupia ja Türgi liir valuutasümbolid sünkroonitakse nüüd õigesti rakendusse Dataverse, |
| 534846 | Andmehalduse jaoks peavad värbamistabelid olema lubatud. | Värbamistaotluste ja kandidaatide jaoks loodud uued tabelid on nüüd andmehalduses lubatud. See võimaldab lubada tabelite jaoks muudatuste jälitamise, lubades OData muudatuste jälgimise Dataverse'i virtuaaltabelites. |
| 533474 | Parandada puuduv viide Failile Microsoft.SqlServer.XEvent.dll. | Assembleri koormuse erandid Microsoft.SqlServer.XEvent.dll jaoks blokeerisid Dataverse'i virtuaaltabeleid mõnedes keskkondades häälestamisel. |
| 481122 | **Inimeste** tööruum kuvab kustutatud ametikohti. | Kustutatud ametikohad kuvati avatud ametikohtadena tööruumis **Inimesed**. Kustutatud ametikohti ei kuvata enam. | 
| 541978 | BaseWorker olemile esmase meiliaadressi lisamine. | See muudatus lisas töötaja peamise meiliaadressi aadressi olemile HcmWorkerBaseEntity. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| LinkedIn talent Hubiga integreerimine | [LinkedIn talent Hubiga integreerimine](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn talent Hubiga integreerimine](./hr-admin-integration-linkedin.md) |
| Kogu ettevõtte puhkusete vaade juhtidele | [Kogu ettevõtte töövõtjate puhkuste vaade juhtidele](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Puhkuste ja puudumiste parameetrite konfigureerimine](./hr-leave-and-absence-parameters.md) |
|Täiendava ülevaate andmine puhkusesaldodest| [Täiendava ülevaate andmine puhkusesaldodest](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Töötaja puhkuse haldamine](./hr-leave-and-absence-manage-employee-leave.md) |
| Juhid saavad esitada ametikohtade värbamistaotlusi | [Juhid saavad esitada avatud ametikohtade värbamistaotluse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Värbamistaotluse lisamine](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Täiustatud kandidaadi profiil personalihalduses | [Täiustatud kandidaadi profiil personalihalduses](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Kandidaadi profiili lisamine või muutmine](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Lihtsustatud integreerimise lubamine värbamispakkujatega | [Lihtsustatud integreerimise lubamine värbamispakkujatega](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaatide värbamine](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Peagi tulekul
| Funktsioon | Details |
| --- | --- |
| Soodustuste registreerimise meilikinnitus | Kui see funktsioon annab võimaluse saata töövõtjatele kinnitusmeili, kui nad registreerivad soodustuste registreerimise kogemuse töövõtja iseteeninduse kaudu. Lisateavet vaadake jaotisest [Soodustuste halduri parameetrite konfigureerimine ettevõtte alusel](hr-benefits-setup-parameters-per-company.md). |
| Töövoog saab automaatselt heaks kiita juhataja poolt töötajate jaoks sisestatud oskused. | Peagi tulekul. |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse'i terminoloogia uuendused

Alates novembrist 2020, on Common Data Service nimetatud ümber rakenduseks [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Vt [ametlikku teadaannet](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) Power Appsi blogist. Seoses selle nime muudatusega on uuendatud mõnda Dataverse'i terminoloogiat. Näiteks *olem* on nüüd *tabel* ja *väli* on nüüd *veerg*. Lisateavet leiad artiklist [Terminoloogia uuendused](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Selles väljalaskes on Dynamics 365 Human Resources'i Dataverse'iga integreerimisega seotud terminoloogiat uuendatud kogu rakenduses, et kajastada neid muudatusi. Näiteks **Common Data Service'i integreerimisvorm** on nüüd **Microsoft Dataverse'i integratsioon**.

Rakenduse Dynamics 365 Human Resources rakendusega Microsoft Dataverse integreerimise kohta leiate lisateavet jaotisest [Microsoft Dataverse'i integratsiooni konfigureerimine](./hr-admin-integration-common-data-service.md) ja [Microsoft Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2020 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]