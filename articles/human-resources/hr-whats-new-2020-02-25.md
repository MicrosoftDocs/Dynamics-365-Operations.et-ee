---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (25. veebruar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 25. veebruari 2020 uusi või muutunud funktsioone.
author: andreabichsel
manager: tfehr
ms.date: 02/25/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-02-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4faecb83518f3ef8af825872abc2a6ffb94162fc
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5128018"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-25-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (25. veebruar 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.2927. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="enable-case-management-navigation-and-data-management-framework-dmf-entity-414754"></a>Juhtumihalduse navigeerimise ja andmete haldamise raamistiku (DMF) üksuse lubamine (414754)

See eelvaate funktsioon lubab juhtumihalduse juhtumite täiendava navigeerimise. Saate lubada selle eelvaate funktsiooni tööruumis **Funktsioonihaldus**. Need menüü üksused kuvatakse Dynamics 365 Human Resourcesi tööruumis **Vastavus**. Selle muudatusega on Human Resourcesil juurdepääs järgnevale:

- Kõik juhtumid
- Minu juhtumid
- Minu avatud juhtumid
- Minu tähtaja ületanud juhtumid
- Mulle töövoo kaudu määratud juhtumid

Koos uute vaadetega juhtumitele on saadaval ka DMF-i üksus **Juhtumi üksikasjad**.

## <a name="enable-relationship-definitions-in-global-address-bbook-414762"></a>Seoste määratluste lubamine globaalses aadressiraamatus (414762)

Seosed on nüüd globaalses aadressiraamatus lubatud. Enne selle nädala väljalaset kuvati kiirinfos **Seos** kõik süsteemi määratletud seosed. Nüüd saate määratleda need seosed globaalse aadressiraamatu lehel.

## <a name="a-position-can-be-removed-when-active-compensation-records-exist-for-the-position-414568"></a>Ametikoha saab eemaldada, kui selle jaoks on olemas aktiivsed kompensatsioonikirjed (414568)

Selle muudatusega kuvatakse hoiatus, kui proovite kustutada ametikohta, kuid töötajal on aktiivne kompensatsioonikirje sellel ametikohal. Sel juhul peate enne ametikoha eemaldamist uuendama töötaja põhipalga kirje.

## <a name="performance-review-workflow-occasionally-adds-sign-offs-from-people-who-are-not-part-of-the-process-414171"></a>Tulemuslikkuse hindamise töövoog lisab aeg-ajalt nõusolekuid inimestelt, kes ei ole protsessi osa (414171)

See muudatus lahendab probleemi, mille puhul lisatakse tulemuslikkuse hindamisse täiendavaid nõusoleku andnud osalejaid.

## <a name="worker-position-assignment-not-created-in-dataverse-when-selected-on-the-new-worker-dialog-413479"></a>Töötaja ametikoha määramist ei looda Dataverse'is, kui see valitakse uue töötaja dialoogis (413479)

See muudatus lahendab probleemi uue töötaja palkamisel ja talle ametikoha määramisel dialoogi **Uus töötaja** kaudu. Ametikoha määramine kajastub nüüd Dataverse'is.

## <a name="coming-soon"></a>Peagi tulekul

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

Paari järgneva nädala jooksul on need üksusemuudatused saadaval kõikides keskkondades. Human Resourcesi uusima Dataverse'i lahenduse käsitsi installimiseks tehke järgmist.

1.  Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2.  Valige **Keskkonnad**.

3.  Otsige üles keskkond, mida soovite uuendada. See peab vastama **Keskkonna nimele** jaotises **Common Data Service'i teave** Human Resourcesi vormil **Teave**.

4.  Keskkonna üksikasjade vaatamiseks valige keskkond.

5.  Valige ülaosast toiminguribalt nupp **Halda lahendusi**. Avaneb uus brauseri aken, seejärel liikuge oma keskkonna kontekstis jaotisesse **Dynamics 365 halduskeskus**.

6.  Loendis **Lahendus** valige **Dynamics 365 Human Resourcesi ankurdaja**.

7.  Uusima lahenduse rakendamiseks valige **Uuenda**.

## <a name="in-preview"></a>Eelvaates

3. veebruarist 2020 on saadaval järgmised eelvaatefunktsioonid.

- **Puhkuste ja puudumiste eelvaatefunktsioonid** – lisateavet vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Soodustuste halduse eelvaatefunktsioon** – lisateavet, sh teadaolevaid probleeme vt [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]