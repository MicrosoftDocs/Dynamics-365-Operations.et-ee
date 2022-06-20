---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (26. september 2020)
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 26. septembriks 2020.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1b7a89ae8a2132c8548d9451aa235d1bccb88809
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874242"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (26. september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources. Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3589-hf.3.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tuleb üldiselt kättesaadavaks järgmine funktsioon.

- **Platvormi värskendus 10.0.13** on [nüüd saadaval: uuenduste kohta leiate lisateavet rakenduse Finance and Operations rakenduste versioonist 10.0.13 platvormi värskendustest (oktoober 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md).

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võib olla värskendusi sellele artiklile, et kaasata parandused, mis muutsid selle pärast selle artikli algset avaldamist järguks.

| Väljaande number | Probleem | Kirjeldus |
| --- | --- | --- |
| 469495 | Finantsdimensioonide vaikeruudustiku ja dialoogiboksi värskendamine | Finantsdimensioonide vaikeruudustik ja dialoogiboks on värskendatud Human Resourcesis. |
| 474887 | Puhkusetaotluse tööüksus avab vale lingi käsitsi otsuses | Kui töövoo konfiguratsioon sisaldab käsitsi otsust, avaneb puhkusetaotluse vormile **Mulle määratud tööüksused** navigeerimisel vale link, mis kuvab tühja vormi või praeguse kasutaja loodud puhkusetaotlust, mitte seda, mis määrati talle käsitsi ostusega. |
| 474962 | Puhkuste ja puudumiste parameetrite üksusel on ebamääraste siltidega väljad | Puhkuste ja puudumiste parameetrite üksuse silte värskendati, et need oleksid selgemad. |
| 481401 | Viitvõlgade töötlus hangub, kui viitvõlgade kuupäeva alus on viitvõlgade alguskuupäevast hilisem ja kuu lõpus | Viitvõlgade töötlust värskendati, et ei oleks viivitust, kui viitvõlgade kuupäeva alus on viitvõlgade alguskuupäevast hilisem ja kuu lõpus. |
| 447167 | Aeguvate kirjete loendites on passiivseid töötajaid | Jaotise **Personalihaldus** vahekaardil **Aeguvad kirjed** oli passiivseid töötajaid. Nüüd sisaldab see ainult aktiivseid töötajaid. |
| 486840 | Jaotises **Mulle määratud tööüksused** avaneb vale puhkusetaotlus | Puhkusetaotluse valimine jaotises **Mulle määratud tööüksused** ei ava enam praegusele kasutajale määratud kõige uuemat puudumise taotlust. |
| 506868 | Dataverse'i välja **Amet** pole määratud üksusele **Ametikoht** | Väli **Amet** on määramata üksustes **Töö** ja **Ametikoht**. Välja **Amet** kuvatakse nüüd. |
| 430359 | Määratud juhi ja töövõtja rollidega ei pääse juurde kontroll-loendi ülesannetele | Tulevase lepingu lõpetamise kuupäevaga töötajad ei pääsenud kontroll-loendi ülesannete juurde, kui neil oli ainult töövõtja või juhi roll. Nüüd saavad tulevase lepingu lõpetamise kuupäevaga kasutajad, kellel on ainult töövõtja või juhi roll, juurdepääsu kontroll-loendi ülesannetele. |
| 458102 | Uut töövõtjat ei kuvata loomisel üksusel **Töötaja palgateave** | Uued töövõtjad lisatakse töötaja palgateabe üksusesse, ilma et peaksite enne üksuse eksportimist töövõtja palgateavet avama. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| Täiustatud töövoo taotlused ja kinnitused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Peagi tulekul

Järgmine uus funktsioon on planeeritud tulevase väljalaske jaoks:

- [Kohandatud lingid juhi iseteeninduses](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2019. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Lisaressursid

[Mis on uut või muudetud Human Resourcesis](hr-admin-whats-new.md)
[Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Värskendamisprotsess](hr-admin-setup-update-process.md)
[Funktsioonide haldus](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]