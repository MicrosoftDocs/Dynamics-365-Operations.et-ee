---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (10. märts 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/10/2020
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
ms.search.validFrom: 2020-03-10
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1843095c41428d377341154c9f2140085831e770
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555245"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-10-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (10. märts 2020)

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.2985. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="cant-access-skill-gap-analysis-report-394460"></a>Erinevuste analüüsi aruannet ei saa avada (394460)

Seda aruannet ei toetata Dynamics 365 Human Resourcesis. SSRS-aruande printimise menüü üksus on eemaldatud.

## <a name="incorrect-message-accessing-the-getting-started-page-417950"></a>Vale teade, mis pääseb lehele Alustamine (417950)

Selle muudatusega peidab turve selle menüü üksuse, kui teil puudub juurdepääs vormile.

## <a name="streamlined-task-maintenance-for-employees-380538"></a>Sujuvam ülesandehaldus töövõtjatele (380538)

Töötaja ülesandehalduse vorm loetleb töövõtja kõik ülesanded sisseelamise, kontrollimise, üleminekute ja äriprotsesside üleselt. Saate ülesande oleku kas kustutada, ümber määrata või seda värskendada.

Näide: Benjamin Martin on soodustuste haldur. Töövõtja sisseelamise ajal luuakse Benjamini jaoks ülesandeid, et vaadata üle uue töötaja soodustuste valik. Benjamin on möödunud ülesanded lõpule viinud ja tulevasi ülesandeid, mida ta veel peab täitma. Benjamin otsustab ettevõttest lahkuda, nii et tema ülesanded tuleb kas ümber määrata või eemaldada. Ülesandehalduse vorm (Vormi **Töötaja** tegevuse paanil) võimaldab kõik Benjamini ülesanded teisele töötajale ümber määrata või eemaldada.  

## <a name="common-data-service-solution-is-now-available-with-the-following-changes"></a>Common Data Service' lahendus on nüüd saadaval, sisaldades järgmisi muudatusi:

| Kirjeldus | Muutmine |
| --- | --- |
| Üksuse **Töö/ametikoht** muudatused | <ul><li>Lisatud **Hüvituspiirkond**</li>|
| Olem **Ametikoha dimensioon** lisatud | <ul><li>Lisatud **Finantsdimensioonid**</li>
| Üksuse **Töötaja** muudatused | <ul><li>Lisatud **Nimeseeria**</li><li>Lisatud **Töötab kodust**</li><li>Lisatud **Keel**</li><li>Lisatud **Staaži kuupäev**</li><li>Lisatud **Tähtpäeva kuupäev**</li><li>Lisatud **Värbamise algne kuupäev**</li></ul> |
| Olemi **Tööhõive** muudatused | <ul><li>Lisatud **Finantsdimensioonid**</li><li>Lisatud **Lõpetamise põhjus**</li><li>Suvand **Lõpetamiskuupäev** on nimetatud ümber suvandist **Üleviimise kuupäeva**</li><li>Lisatud **Katseaja kuupäev**</li></ul> |
| Üksuse **Töötaja aadress** muudatused | <ul><li>Lisatud **Tänavanimi**</li><li>Suvandid **Aadressirida 1**, **Aadressirida 2** ja **Aadressirida 3** on märgistatud kasutuselt eemaldamiseks</li></ul> |
| Uued ergutussüsteemi seadistuse üksused | <ul><li>**Muutuva hüvitisplaani tüüp**</li><li>**Kompensatsiooni tulemusplaan**</li><li>**Pensionireeglid**</li><li>**Muutuva hüvitisplaani tase**</li></ul> |
| Uus olem **Töötaja kalendri tööhõive** | <ul><li>Lisatud **Töökalendri üksus**</li></ul> |
| Uus olem **Palgaarvestuse ametikoha üksikasjad** | <ul><li>Lisatud **Palgaarvestuse ametikoha üksikasjad**</li></ul> |
| Uus üksus **Ametinimetus** | <ul><li>Lisatud **Ametinimetus**</li></ul> Uus üksus **Ametinimetus** on lisatud Common Data Service'isse, kuid seda ei viidata praegu üksustes **Ametikoht** või **Töö**. |

> [!NOTE]
> Ametikoha ja tööhõive finantsdimensioonid loovad ühesuunalise integratsiooni Human Resourcesi värskendamiseks Common Data Service'isse. Finantsdimensioonide värskendusi ei sünkroonita praegu Common Data Service'ist Human Resourcesisse.

Paari järgneva nädala jooksul on need üksusemuudatused saadaval kõikides keskkondades. Human Resourcesi uusima Common Data Service'i lahenduse käsitsi installimiseks tehke järgmist.

1.  Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2.  Valige **Keskkonnad**.

3.  Otsige üles keskkond, mida soovite uuendada. Keskkond peab vastama **Keskkonna nimele** jaotises **Common Data Service'i teave** Human Resourcesi vormil **Teave**.

4.  Keskkonna üksikasjade vaatamiseks valige keskkond.

5.  Valige ülaosast toiminguribalt nupp **Halda lahendusi**. Avaneb uus brauseri aken, seejärel liikuge oma keskkonna kontekstis jaotisesse **Dynamics 365 halduskeskus**.

6.  Loendis **Lahendus** valige **Dynamics 365 Human Resourcesi ankurdaja**.

7.  Uusima lahenduse rakendamiseks valige **Uuenda**.

## <a name="in-preview"></a>Eelvaates

3. veebruaril 2020 on saadaval järgmised eelvaatefunktsioonid.

- **Puhkuste ja puudumiste eelvaatefunktsioonid** – lisateavet vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Soodustuste halduse eelvaatefunktsioon** – lisateavet, sh teadaolevaid probleeme vt [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

## <a name="coming-soon"></a>Peagi tulekul

### <a name="platform-update-33"></a>Platvormivärskendus update 33

- Täisleheküljelised rakendused (Eelvaade) – see eelvaatefunktsioon, mis nõuab teilt Salvestatud vaadete funktsiooni lubamist, võimaldab Power Appsi ja muude tootjate rakendusi lisada armatuurlaua kaudu täislehekülje funktsioonidena.

- Salvestatud vaated (Eelvaade) – see eelvaate funktsioon lubab salvestatud vaated, mis on oluline täiustus isikupärastamise alamsüsteemile. See funktsioon lubab kasutajatele mitme nimega isikupärastamise kogumit lehekülje kohta. Samuti saate avaldada turberollide vaateid.

- Optimeeritud fltreerimise kogemus „üks mitmest” – see funktsioon lubab optimeeritud filtreerimise kogemuse „üks mitmest“ kasutust, mis hõlbustab mitme filtriväärtuse sisestamist, sellel on lihtsam mehhanism üksiku või kõigi filtriväärtuste eemaldamiseks ning filtriväärtuste kompaktsem ja intuitiivsem visualiseering.

- Soovitatavad väljad – kasutajad peavad sageli lisama välju ruudustikule või lehele. See võib olla keeruline nii paljude saadaolevate väljadega. Selle asemel, et peaks pika loendi läbi otsima, võimaldab see funktsioon süsteemil luua soovitatud väljade kogumi, lähtudes sellest, mida teised kasutajad kõige sagedamini sarnastes olukordades lisavad.

- Tabelite vaikimisi kleepetegevused – see funktsioon tagab, et tabeli vaiketegevus on lingitud tabeli konkreetse veeruga olenemata sellest, kas veerg on teisaldatud või peidetud.

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)