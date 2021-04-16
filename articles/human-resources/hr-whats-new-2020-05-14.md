---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (14. mai 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 14. mai 2020 uusi või muutunud funktsioone.
author: andreabichsel
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e70d8fc62150d68503552754e94c7130d8960c76
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802355"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (14. mai 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3244. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Lifecycle Services (LCS).

## <a name="platform-changes"></a>Platvormi muudatused

Selle nädala väljalaske hulka kuuluvad platvormi muudatused. Lisateavet leiate teemast [Finance and Operationsi rakenduste versiooni 10.0.10 platvormivärskendused (mai 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). See väljalase sisaldab veaparandusi ja salvestatud vaadete muudatusi.
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>Dataverse'i märkeloendi puhkuse loeteludega kooskõlas olemises veendumine (436343)

Dataverse'i märkeloendid on nüüd puhkuse loeteludega kooskõlas.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Kasutajatele puhkusetaotluse töövoo konfigureerimise lubamine taotluse summa põhjal (300044)

Kasutajad saavad konfigureerida puhkusetaotluse töövoogusid taotluse summa põhjal.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Uus töötaja vorm näitab andmed menüü Vaade kaudu, kui täiustatud turve on lubatud (403185)

Selles väljalaskes on parandtud erinevate juriidiliste isikute lõikes töötajate kuvamise kogemust, kui täiustatud juurdepääs on lubatud ja teiste ettevõtete töötajad on juurdepääsetavad.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Puhkuse viitvõlgade käitamise lubamine üksikule plaanile või ettevõttele (318844)

Selle muudatusega saate käitada ettevõtte või plaani viitvõlgasid.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Ametikoha täistööajaga võrdse väärtuse (FTE) kuvamine vormil Registreeritud töötajad (414658)

Töötaja ametikoha FTE-väärtus määrab töötaja viitvõlgade määra, kui puhkuse tüübil on lubatud suvand FTE. See väli on nüüd kaasatud vormi **Registreeritud töötajad** ja dialoogi **Hulgiregistreerimine**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Puhkuse saldo aegumise pakett-töö lisamine (431266)

Uus igapäevaselt käitatav pakett-töö on nüüd saadaval. See vähendab järelejäänud puhkuse saldot aegumise kuupäevade kättejõudmisel.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Töövõtja isiklike kontaktide eksportimine üksuse Töövõtja isikliku kontaktisik abil, ei ekspordi isiklikke kontakte koos tüübiga Peamine suhe (345893)

Andmeüksus **Töötaja isiklik kontaktisik** (DMF-i **HcmPersonalContactPersonEntity** ja OData **PersonalContactPerson**) ei saanud eksportida isiklikke kontakte, mille suhte tüüp on **Peamine**. See probleem on lahendatud pärast seda muudatust loodud isiklike kontaktide jaoks. Olemasolevad isiklikud kontaktid tüübiga **Peamine** parandatakse hilisemas väljalaskes.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Põhjusekoode kuvatakse erinevate stsenaariumide korral, kui suvandi väärtuseks on määratud Puhkused ja puudumised ning sujuva töövõtja vorm on lubatud (434163)

Selle muudatusega seatakse põhjusekoodide piiranguks ainult koodid Puhkused ja puudumised, kui lubate sujuva töövõtja kirje.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Eelvaatefunktsioon Töövõtjale puhkuseplaani määramine tulevikku kuvab tõrke (433555)

Selle muudatusega parandatakse tõrge, kus puhkuseplaanile on määratud kaks puhkuse tüüpi ja üritate määrata töötajat.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Ribareklaami Alustamine kuvatakse kõigile kasutajatele (441731)

Selle muudatusega peidetakse ribareklaam Alustamine nende kasutajate jaoks, kes ei ole süsteemiadministraatorid või andmehalduse administraatorid. 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Dataverse'i üksuse Töötaja aadress kehtivuskuupäevade kuupäevad ja kellaajad töötavad teisiti kui Human Resourcesis (425071)

See muudatus tagab aadressi teabe järjepidevuse aadressi kuupäevade alusel teatud stsenaariumides.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Manust ei saa lisada kinnitatud puhkusetaotlusele (425407)

Selle nädala väljalaskega saate lisada manuseid kinnitatud puhkusetaotlustele ilma taotlust muutmata.

## <a name="in-preview"></a>Eelvaates

## <a name="leave-suspension"></a>Puhkuse peatamine

Saate peatada töövõtja puhkuse Human Resourcesis. Puhkuse peatamine lõpetab puhkuse viitvõlad valitud puhkusetüüpide puhul. Kui peatamine toimub pärast viitvõla töötlemist, loob peatatav puhkus eelmääratud korrigeerimise töötaja puhkusesaldo jaoks. Lisateabe saamiseks vt [Puhkuse peatamine](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Kasutajakogemuse uuendamine viitvõla näitamiseks on peatatud (429550)

Kasutajakogemuses on nüüd näidatud, et plaani viitvõlg on peatatud.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Kindlate puhkusetüüpide puhkuse viitvõla peatamine (272447)

Selles väljalaskes saab inimressursside haldur luua reegli, et peatada selliste töötajate puhkuse viitvõlg, kes on esitanud tasustamata puhkuse taotluse. Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla. Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-üksus on saadaval viitvõlgade peatamiseks (429549)

Nüüdsest on viitvõlgade peatamiseks saadaval DMF-üksus.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Lisa viitvõlgade peatamisele põhjusekood (429547)

Viitvõla peatamisele on lisatud põhjusekood.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Inimressursside parameetritelt puhkuse ja puudumise parameetritele ülemineku alustamine

Selles väljalaskes on alustatud inimressursside parameetrite kombineerimist puhkuse ja puudumise parameetritega.

## <a name="carry-forward-rules"></a>Edasikandmise reeglid

Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle. Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi. Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]