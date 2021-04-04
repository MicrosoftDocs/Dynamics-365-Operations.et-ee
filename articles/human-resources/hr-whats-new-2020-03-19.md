---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (19. märts 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 19. märtsi 2020 uusi või muutunud funktsioone.
author: andreabichsel
manager: tfehr
ms.date: 03/19/2020
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
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a594e5fdf67d22005800cc679d3db60dc900a016
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463666"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-19-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (19. märts 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3014. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Lifecycle Services (LCS).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Keskkonna Human Resources piirangud põhinevad nüüd värskendatud litsentsimisele (394595)

Teenuse Lifecycle Services (LCS) keskkondade arvu piirang projekti kohta on muutunud. Varasem piirang oli kaks keskkonda. LCS-i keskkonna Human Resources loodavate tootmis- ja liivakastikeskkondade arvu piirang põhineb nüüd värskendatud litsentsimisele. Nüüd saate ühe LCS-i projekti kohta luua nii palju keskkondi kui vaja, sõltuvalt ostetud litsentside arvust. Uus 1. veebruaril 2020. aastal värskendatud litsentsimine võimaldab klientidel osta täiendavaid keskkondi. Lisateabe saamiseks täiendavate keskkondade litsentsimise nõuete kohta vaadake teemat [Dynamics 365 litsentsijuhend](https://dynamics.microsoft.com/pricing/#HumanResources).

## <a name="provide-cross-company-viewing-of-compensation-data-for-employees-and-managers-403904"></a>Ettevõtteüleste kompensatsiooniandmete vaatamine töötajatele ja ülemustele (403904)

Lülitage see funktsioon sisse tööruumis **Funktsioonide haldus**. Lisateavet leiate teemast [Eelvaatefunktsioonide lubamine või keelamine](hr-admin-manage-features.md#enable-or-disable-preview-features).

Kui lubate selle funktsiooni, näevad ülemused otseseid ja laiendatud kompensatsiooni aruandeid, ilma tööettevõttesse sisse logimata. Kompensatsiooni täielik ajalugu on saadaval mis tahes sisselogitud ettevõttes, millele ülemusel on juurdepääs. Lisateavet leiate teemast [Töötaja ja ülemuse iseteeninduse ülevaade](hr-employee-manager-self-service-overview.md).

## <a name="enable-global-address-book-merge-functionality-427189"></a>Globaalse aadressiraamatu ühendamise funktsiooni lubamine (427189)

Nüüd saate ühendada dubleeritud aadressiraamatu kirjed, valides duplikaatkirje ja lehel **Globaalne aadressiraamat** suvandi **Ühenda**.

## <a name="unable-to-adjust-leave-balance-for-a-plan-with-no-accruals-that-was-created-with-the-multiple-leave-type-feature-on-419635"></a>Plaani puhkusesaldot ei saanud kohandada ilma viitvõlata, mis loodi mitme puhkusetüübi funktsiooniga (419635)

Nüüd saate kohandada puhkuseplaanide saldosid, mis loodi funktsioonihalduse eelvaatefunktsiooniga **Mitme puhkuse tüüp**.

## <a name="primary-position-field-in-the-workerpositionassignmententity-when-an-employee-is-terminated-420774"></a>Üksuse WorkerPositionAssignmentEntity esmase ametikoha väli töötaja lepingu lõpetamisel (420774)

Üksuses kuvatakse lõpetatud töösuhtega töötaja esmane aktiivne ametikoht töölepingu lõpetamise hetkel. Integratsioonide puhul ei looda enam duplikaatkirjet töötaja ametikoha määramisel. 

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse' lahendus on nüüd saadaval, sisaldades järgmisi muudatusi:

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
| Uus üksus **Ametinimetus** | <ul><li>Lisatud **Ametinimetus**</li></ul>Uus üksus **Ametinimetus** on lisatud Dataverse'isse, kuid seda ei viidata praegu üksustes **Ametikoht** või **Töö**. |

> [!NOTE]
> Ametikoha ja tööhõive finantsdimensioonid loovad ühesuunalise integratsiooni Human Resourcesi värskendamiseks Dataverse'isse. Finantsdimensioonide värskendusi ei sünkroonita praegu Dataverse'ist Human Resourcesisse.

Paari järgneva nädala jooksul on need üksusemuudatused saadaval kõikides keskkondades. Human Resourcesi uusima Dataverse'i lahenduse käsitsi installimiseks tehke järgmist.

1.  Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2.  Valige **Keskkonnad**.

3.  Otsige üles keskkond, mida soovite uuendada. Keskkond peab vastama **Keskkonna nimele** jaotises **Common Data Service'i teave** Human Resourcesi vormil **Teave**.

4.  Keskkonna üksikasjade vaatamiseks valige keskkond.

5.  Valige ülaosast toiminguribalt nupp **Halda lahendusi**. Avaneb uus brauseri aken, seejärel liikuge oma keskkonna kontekstis jaotisesse **Dynamics 365 halduskeskus**.

6.  Loendis **Lahendus** valige **Dynamics 365 Human Resourcesi ankurdaja**.

7.  Uusima lahenduse rakendamiseks valige **Uuenda**.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePointi eelvaade ei tööta mõnes keskkonnas

Kui SharePointi talletatud dokumentide dokumendieelvaade ei tööta, proovige järgmist toimingut.

1. Kinnitage, et administraatori kasutajakontol on kasutaja kirjega seotud meiliaadress. Seda teavet saate vaadata lehel **Kasutaja**. Kui meiliaadressi ei ole seadistatud, peate lisama meili ja pakkuja OData Exceli lisandmooduli kaudu. Vaikimisi ei ole Exceli kujunduses meiliaadressi kaasatud. Peate redigeerima Exceli kujundust, lisama kõik väljad, rakendama ja värskendama. Kui olete need toimingud teinud, saate värskendada administraatori kontot.

2. Kui administraatoril on seostatud meilikonto, logige sisse Human Resourcesisse administraatori mandaatidega.

3. Juurdepääs SharePointi manusele dokumendieelvaate käivitamiseks.

4. Logige sisse teise kasutajakontoga, millel on juurdepääs manustele ja kinnitage, et eelvaade töötab ootuspäraselt.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="platform-update-33"></a>Platvormivärskendus update 33

- Täisleheküljelised rakendused (Eelvaade) – see eelvaatefunktsioon, mis nõuab teilt Salvestatud vaadete funktsiooni lubamist, võimaldab Power Appsi ja muude tootjate rakendusi lisada armatuurlaua kaudu täislehekülje funktsioonidena.

- Salvestatud vaated (Eelvaade) – see eelvaate funktsioon lubab salvestatud vaated, mis pakub olulist täiustust isikupärastamise alamsüsteemile. See funktsioon lubab kasutajatele mitme nimega isikupärastamise kogumit lehekülje kohta. Samuti saate avaldada turberollide vaateid.

- Optimeeritud fltreerimise kogemus „üks mitmest” – see funktsioon lubab optimeeritud filtreerimise kogemuse „üks mitmest“ kasutust, mis hõlbustab mitme filtriväärtuse sisestamist, sellel on lihtsam mehhanism üksiku või kõigi filtriväärtuste eemaldamiseks ning filtriväärtuste kompaktsem ja intuitiivsem visualiseering.

- Soovitatavad väljad – kasutajad peavad sageli lisama välju ruudustikule või lehele. See võib olla keeruline nii paljude saadaolevate väljadega. Selle asemel, et peaks pika loendi läbi otsima, võimaldab see funktsioon süsteemil luua soovitatud väljade kogumi, lähtudes sellest, mida teised kasutajad kõige sagedamini sarnastes olukordades lisavad.

- Tabelite vaikimisi kleepetegevused – see funktsioon tagab, et tabeli vaiketegevus on lingitud tabeli konkreetse veeruga olenemata sellest, kas veerg on teisaldatud või peidetud.

## <a name="new-production-release-cadence"></a>Uus tootmise väljalaskesagedus

Alates aprillist läheb Human Resourcesi väljalaskesagedus üle iganädalaselt värskenduselt kahenädalasele. See tagab kooskõla turvaliste juurutuspraktikatega ning säilitab teenuse stabiilsuse ja usaldusväärsuse kõrged standardid. Me lisame täiendavaid katsetamis- ja jälgimismeetodeid, et kinnitada edukat juurutamist protsessi igas etapis. Väljalaskesageduse kohta lisateabe saamiseks vaadake teemat [Värskendusprotsess](hr-admin-setup-update-process.md).

## <a name="in-preview"></a>Eelvaates

3. veebruaril 2020 on saadaval järgmised eelvaatefunktsioonid.

- **Puhkuste ja puudumiste eelvaatefunktsioonid** – lisateavet vt [Puhkuste ja puudumiste eelvaatefunktsioonid](hr-leave-and-absence-overview.md?leave-and-absence-preview-features).

- **Soodustuste halduse eelvaatefunktsioon** – lisateavet, sh teadaolevaid probleeme vt [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]