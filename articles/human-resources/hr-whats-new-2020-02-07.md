---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (7. veebruar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 7. veebruari 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/07/2020
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
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 42fac6e34db10efb047b4cb0fc3c7752330e5bcf
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4526830"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-7-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (7. veebruar 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.2835. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

## <a name="learning-analytics-doesnt-show-the-course-if-the-classroom-is-blank-388289"></a>Õppeanalüüs ei näita kursust, kui klassiruumis on tühi (388289)

Õppeanalüüsi leht kuvab nüüd kursuse, kui klassiruumis on tühi.

## <a name="position-lookup-doesnt-take-the-time-zone-into-account-405344"></a>Ametikoha otsing ei võtta arvesse ajavööndit (405344)

Avatud ametikohtade otsing arvestab nüüd ametikoha saadaval olemise kinnitamisel ajavööndiga.

## <a name="current-balance-analysis-view-doesnt-update-with-the-correct-current-leave-balance-after-submitting-time-off-requests-409756"></a>Praeguse saldo analüüsi vaade ei värskenda pärast vaba aja taotluse esitamist õiget hetkelist puhkusesaldot (409756)

Praegune saldo sisaldab nüüd esitatud vaba aja taotlusi.

## <a name="in-preview"></a>Eelvaates

3. veebruaril 2020 on saadaval järgmised eelvaatefunktsioonid.

- **Puhkuste ja puudumiste eelvaatefunktsioonid** – lisateavet vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Soodustuste halduse eelvaatefunktsioon** – lisateavet, sh teadaolevaid probleeme vt teemast [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Peagi tulekul

### <a name="platform-update-32"></a>Platvormivärskendus update 32 

Platvormivärskendus 32 on peagi saadaval. [Lisateavet platvormivärskenduse 32 kohta leiate siit](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).

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