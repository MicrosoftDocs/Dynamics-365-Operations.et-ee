---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (12. veebruar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 12. veebruari 2020 uusi või muutunud funktsioone.
author: andreabichsel
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ce265627bf5cef023770be3f8953e12d49866be
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686907"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-12-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (12. veebruar 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.2867. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

## <a name="existing-entities-compfixedempls-and-hcmpersonimage-should-be-accessible-from-odata-414178"></a>Olemasolevad olemid CompFixedEmpls ja HcmPersonImage peaksid olema OData kaudu juurdepääsetavad (414178)

Selle nädala väljalaskega on üksused **CompFixedEmpls** ja **HcmPersonImage** nüüd avalikud ja OData kaudu saadaval.

## <a name="delete-employment-from-dataverse-doesnt-work-when-employment-details-arent-active-403193"></a>Tööhõive kustutamine teenusest Dataverse ei tööta, kui töötamise üksikasjad pole aktiivsed (403193)

See muudatus võimaldab nüüd töösuhte teenuse Dataverse kaudu kustutada, kui aktiivseid tööhõive üksikasju pole.

## <a name="course-registration-workflow-changes-status-to-complete-and-errors-after-second-approval-409749"></a>Kursuse registreerimise töövoog muudab oleku lõpetatuks ja pärast teist kinnitamist esineb tõrge (409749)

Kursuse registreerimise töövoogu on värskendatud, et lubada mitu kinnitajat.

## <a name="in-preview"></a>Eelvaates

3. veebruaril 2020 on saadaval järgmised eelvaatefunktsioonid.

- **Puhkuste ja puudumiste eelvaatefunktsioonid** – lisateavet vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Soodustuste halduse eelvaatefunktsioon** – lisateavet, sh teadaolevaid probleeme vt [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Peagi tulekul

### <a name="platform-update-32"></a>Platvormivärskendus update 32 

Platvormivärskendus 32 on peagi saadaval. [Lisateavet platvormivärskenduse 32 kohta leiate siit](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md).

### <a name="updated-dataverse-solution"></a>Värskendatud lahendus Dataverse

Uus lahendus Dataverse on varsti saadaval järgmiste muudatustega.

| Kirjeldus | Muutmine |
| ----------------------------------------- | --- |
| Üksuse **Töö/ametikoht** muudatused | Lisatud **Hüvituspiirkond**</br>Lisatud **Finantsdimensioonid** |
| Üksuse **Töötaja** muudatused | Lisatud **Nimeseeria**</br>Lisatud **Töötab kodust**</br>Lisatud **Keel**</br>Lisatud **Staaži kuupäev**</br>Lisatud **Tähtpäeva kuupäev**</br>Lisatud **Värbamise algne kuupäev** |
| Olemi **Tööhõive** muudatused | Lisatud **Finantsdimensioonid**</br>Lisatud **Lõpetamise põhjus**</br>Suvand **Lõpetamiskuupäev** on nimetatud ümber suvandist **Üleviimise kuupäeva**</br>Lisatud **Katseaja kuupäev** |
| Üksuse **Töötaja aadress** muudatused | Lisatud **Tänavanimi**</br>Suvandid **Aadressirida 1**, **Aadressirida 2** ja **Aadressirida 3** on märgistatud kasutuselt eemaldamiseks |
| Uued ergutussüsteemi seadistuse üksused | **Muutuva hüvitisplaani tüüp**</br>**Kompensatsiooni tulemusplaan**</br>**Pensionireeglid**</br>**Muutuva hüvitisplaani tase** |
| Uus olem **Töötaja kalendri tööhõive** | Lisatud **Töökalendri üksus** |
| Uus olem **Palgaarvestuse ametikoha üksikasjad** | Lisatud **Palgaarvestuse ametikoha üksikasjad** |
| Uus üksus **Ametinimetus** | Lisatud **Ametinimetus**. Uus üksus **Pealkiri** kaasatakse sünkroonimisprotsessi rakenduse Human Resources ja teenuse Dataverse vahel. Kuid algselt ei viidata sellele üksustelt **Ametikoht** või **Töö**. |

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]