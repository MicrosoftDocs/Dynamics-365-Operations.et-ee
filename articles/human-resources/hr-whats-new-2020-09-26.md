---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (26. september 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 26. septembri 2020 uusi või muutunud funktsioone.
author: jcart1106
manager: tfehr
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ac72489c3b2dacfde280606a83221e8514793701
ms.sourcegitcommit: 2190be6c205d7d9e43bdb99b9190cc0112f9f093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/10/2021
ms.locfileid: "5152193"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (26. september 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone. Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3589-hf.3.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tuleb üldiselt kättesaadavaks järgmine funktsioon.

- **Platvormi versiooni 10.0.13 värskendus on nüüd saadaval**: lisateavet värskenduse kohta leiate teemast [Finance and Operationsi rakenduste platvormi versiooni 10.0.13 värskendused (oktoober 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13).

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Seda teemat võidakse värskendada, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Väljasta | Kirjeldus |
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
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| Täiustatud töövoo taotlused ja kinnitused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Peagi tulekul

Järgmine uus funktsioon on planeeritud tulevase väljalaske jaoks:

- [Kohandatud lingid juhi iseteeninduses](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2019. aasta 2. väljalaskevoo ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Lisaressursid

[Mis on uut või muudetud Human Resourcesis](hr-admin-whats-new.md)
[Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Värskendamisprotsess](hr-admin-setup-update-process.md)
[Funktsioonide haldus](hr-admin-manage-features.md)
