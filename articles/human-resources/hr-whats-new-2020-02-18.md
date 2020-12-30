---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (18. veebruar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 18. veebruari 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 002b1b8b86c4fb40f46c239669cd5dfead251bfe
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526974"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (18. veebruar 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.2903. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="platform-update-32"></a>Platvormivärskendus update 32 

Platvormivärskendus 32 on nüüd saadaval. Lisateavet leiate teemast [Teenuse Finance and Operationsi platvormivärskenduse 32 uued või muudetud funktsioonid (veebruar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a>Otsinguväärtusi mäletatakse, kui sujuva töötaja vormi vaatevalikuid muudetakse (383833)

Uue vorm **Töötaja** jätab nüüd otsinguväärtused meelde, kui muudate vaate suvandeid ja rakendate muudatused.

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a>Hüvituste halduse kokkuvõttepaanid eelvaate funktsioonis suunavad valele vormile (401861)

Põhipalga ja tulemustasu halduspaanid kuvavad nüüd uues vormis **Töötaja** õigeid kirjeid. Kehtib ainult sujuva töötaja vormi eelvaate funktsioonile. Saate lubada selle eelvaate funktsiooni suvandis **Funktsioonihaldus**. Lisateabe saamiseks vaadake jaotist [Funktsioonide haldamine](hr-admin-manage-features.md).

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a>Teenuse Common Data Service osade puhkusetaotluste kirjete väli Olek on tühi (414915)

See muudatus parandab teenuse Common Data Service probleemi, kui väli **Olek** puhkusetaotluses on seatud olekusse **Ülevaatus**. Common Data Service peegeldab nüüd olekut.

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a>Oskuste erinevuse analüüs on võimalik ainult määratud töö jaoks (411390)

Nüüd saate teha oskuste erinevuse analüüsi mis tahes rakenduse Human Resources määratletud töö jaoks.

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a>Süsteemi valuuta ei sünkroonita uutes keskkondades teenusest Common Data Service rakendusse Human Resources (418011)

Süsteemi valuuta saab nüüd sünkroonida teenusest Common Data Service rakendusse Human Resources.

## <a name="in-preview"></a>Eelvaates

- [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [Soodustuste halduse eelvaatefunktsioonid](hr-benefits-management-overview.md)

## <a name="coming-soon"></a>Peagi tulekul

### <a name="updated-common-data-service-solution"></a>Värskendatud lahendus Common Data Service

Uus lahendus Common Data Service on varsti saadaval järgmiste muudatustega.

| Kirjeldus | Muutmine |
| ----------------------------------------- | --- |
| Üksuse **Töö/ametikoht** muudatused | Lisatud **Hüvituspiirkond**</br>Lisatud **Finantsdimensioonid** |
| Üksuse **Töötaja** muudatused | Lisatud **Nimeseeria**</br>Lisatud **Töötab kodust**</br>Lisatud **Keel**</br>Lisatud **Staaži kuupäev**</br>Lisatud **Tähtpäeva kuupäev**</br>Lisatud **Värbamise algne kuupäev** |
| Olemi **Tööhõive** muudatused | Lisatud **Finantsdimensioonid**</br>Lisatud **Lõpetamise põhjus**</br>Suvand **Lõpetamiskuupäev** on nimetatud ümber suvandist **Üleviimise kuupäeva**</br>Lisatud **Katseaja kuupäev** |
| Üksuse **Töötaja aadress** muudatused | Lisatud **Tänavanimi**</br>Suvandid **Aadressirida 1**, **Aadressirida 2** ja **Aadressirida 3** on märgistatud kasutuselt eemaldamiseks |
| Uued ergutussüsteemi seadistuse üksused | **Muutuva hüvitisplaani tüüp**</br>**Kompensatsiooni tulemusplaan**</br>**Pensionireeglid**</br>**Muutuva hüvitisplaani tase** |
| Uus olem **Töötaja kalendri tööhõive** | Lisatud **Töökalendri üksus** |
| Uus olem **Palgaarvestuse ametikoha üksikasjad** | Lisatud **Palgaarvestuse ametikoha üksikasjad** |
| Uus üksus **Ametinimetus** | Lisatud **Ametinimetus**. Uus üksus **Pealkiri** kaasatakse sünkroonimisprotsessi rakenduse Human Resources ja teenuse Common Data Service vahel. Kuid algselt ei viidata sellele üksustelt **Ametikoht** või **Töö**. |

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)