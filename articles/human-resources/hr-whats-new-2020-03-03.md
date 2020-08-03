---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (3. märts 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d85ce8ccfcd7f1b975244cc2f65535101013ac89
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555287"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-3-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (3. märts 2020)

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.2955. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service' lahendus on nüüd saadaval, sisaldades järgmisi muudatusi:

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

Paari järgneva nädala jooksul on need üksusemuudatused saadaval kõikides keskkondades. Human Resourcesi uusima Common Data Service'i lahenduse käsitsi installimiseks tehke järgmist.

1.  Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2.  Valige **Keskkonnad**.

3.  Otsige üles keskkond, mida soovite uuendada. Keskkond peab vastama **Keskkonna nimele** jaotises **Common Data Service'i teave** Human Resourcesi vormil **Teave**.

4.  Keskkonna üksikasjade vaatamiseks valige keskkond.

5.  Valige ülaosast toiminguribalt nupp **Halda lahendusi**. Avaneb uus brauseri aken, seejärel liikuge oma keskkonna kontekstis jaotisesse **Dynamics 365 halduskeskus**.

6.  Loendis **Lahendus** valige **Dynamics 365 Human Resourcesi ankurdaja**.

7.  Uusima lahenduse rakendamiseks valige **Uuenda**.

## <a name="import-issues-with-the-leave-enrollment-data-entity-406082"></a>Probleem andmeüksuse Puhkuse registreerimine importimisel (406082)

Te saate nüüd registreerida töötajale uue sama tüüpi puhkuseplaani, kui uus registreerimise kuupäev on hilisem kui eelmise plaani aegumiskuupäev.

## <a name="issue-with-exporting-contribution-rates-in-the-401k-payrollworkerenrolledbenefitdetail-entity-in-dmf-420700"></a>Probleem üksuse 401k payrollWorkerEnrolledBenefitDetail kasumimäära eksportimisel DMF-is (420700)

See muudatus parandab üksuse **payrollWorkerEnrolledBenefitDetail** eksportimise funktsiooni, et see näitaks töötaja panuse hetkeväärtusi.

## <a name="searching-in-the-streamlined-worker-form-causes-message-saying-person-field-must-be-filled-in-402525"></a>Sujuva töötaja vormi otsing annab teate, et isiku väli peab olema täidetud (402525)

Töötaja otsimisel ei saa te enam teadet, mis ütleb, et peate täitma välja **Isik**.

## <a name="note-field-value-doesnt-render-on-the-add-more-skills-form-380134"></a>Märkuse välja väärtus ei renderda vormil Lisa veel oskusi (380134)

See muudatus lahendab probleemi vormi **Lisa veel oskusi** personaliseerimisel Töötaja iseteeninduses.

## <a name="multiple-fixed-compensation-plans-dont-expire-when-transferring-employees-389466"></a>Mitu põhipalga plaani ei aegu töötajate ülekandmisel (389466)

Selle muudatusega aeguvad kõik vana ametikoha aktiivsed põhipalga kirjed ülekandmise kuupäeval.

## <a name="in-preview"></a>Eelvaates

3. veebruarist 2020 on saadaval järgmised eelvaatefunktsioonid.

- **Puhkuste ja puudumiste eelvaatefunktsioonid** – lisateavet vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Soodustuste halduse eelvaatefunktsioon** – lisateavet, sh teadaolevaid probleeme vt [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)