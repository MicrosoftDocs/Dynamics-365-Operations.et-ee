---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (3. aprill, 2020)?
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 3. aprilli 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 04/03/2020
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
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 03fe38c8e2a8de6957cdc1adf5e89d7d0421d997
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712481"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (3. aprill, 2020)?

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3111. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Lifecycle Services (LCS).

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Funktsioonid, mis on üldiselt kättesaadavad 6. aprillil

- **Puhkuste ja puudumiste funktsioonid** – lisateabe saamiseks vt [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md).

- **Soodustuste halduse funktsioonid** – lisateabe saamiseks vt [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Keskkonna Human Resources piirangud põhinevad nüüd värskendatud litsentsimisele (394595)

Teenuse LCS keskkondade arvu piirang projekti kohta on muutunud. Varasem piirang oli kaks keskkonda. LCS-i keskkonna Human Resources loodavate tootmis- ja liivakastikeskkondade arvu piirang põhineb nüüd värskendatud litsentsimisele. Nüüd saate ühe LCS-i projekti kohta luua nii palju keskkondi kui vaja, sõltuvalt ostetud litsentside arvust. Uus 1. veebruaril 2020. aastal värskendatud litsentsimine võimaldab klientidel osta täiendavaid keskkondi. Lisateabe saamiseks täiendavate keskkondade litsentsimise nõuete kohta vaadake teemat [Dynamics 365 litsentsijuhend](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Tõrge küsimustiku kustutamise katsel (428603)

Selle nädala värskendusega lahendatakse probleem, kus küsimustiku kustutamise katsel kuvatakse järgmine tõrge.

Tuvastati tasakaalustamata X++ TTSBEGIN/TTSCOMMIT paar.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Probleem jõudluse töölehe ja professionaalsete sertide turbega (428499)

See muudatus piirab nii jõudluse töölehtede kui ka professionaalsete sertide nähtavust selle põhjal, mis ettevõtetele neil on juurdepääs. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Quebeci ja Manitoba lühend (387510)

Algandmed on värskendatud kajastama Manitoba ja Quebeci õiget lühendit.

## <a name="new-entities-available-in-data-management-framework"></a>Uued üksused on saadaval andmehaldusraamistikus

Järgmised üksused on nüüd saadaval. Kui te ei näe neid üksuseid üksuste loendis, kasutage jaotises **Raamistiku parameetrid > Üksuse sätted > Värskenda üksuste loendit** suvandit **Värskenda üksuseid**.

 - Puhkuste ja puudumise panga kanne V2
 - Puhkuse ja puudumise registreerimine V2
 - Puhkuse ja puudumise plaani järk V2
 - Puhkuse ja puudumise plaan V2

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
| Uus üksus **Ametinimetus** | <ul><li>Lisatud **Ametinimetus**</li></ul>Uus üksus **Ametinimetus** on lisatud Common Data Service'isse, kuid seda ei viidata praegu üksustes **Ametikoht** või **Töö**. |

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

## <a name="leave-suspension"></a>Puhkuse peatamine

Saate peatada töövõtja puhkuse Human Resourcesis. Puhkuse peatamine lõpetab puhkuse viitvõlad valitud puhkusetüüpide puhul. Kui peatamine toimub pärast viitvõla töötlemist, loob peatatav puhkus eelmääratud korrigeerimise töötaja puhkusesaldo jaoks. Lisateabe saamiseks vt [Puhkuse peatamine](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Edasikandmise reeglid

Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle. Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi. Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Peagi tulekul

## <a name="new-production-release-cadence"></a>Uus tootmise väljalaskesagedus

Alates aprillist läheb Human Resourcesi väljalaskesagedus üle iganädalaselt värskenduselt kahenädalasele. Ohutute juurutustavadega vastavusse viimise tagamiseks ning teenuse stabiilsuse ja töökindluse kõrgete standardite säilitamiseks kestab teenusevärskenduste juurutamine kõigisse piirkondadesse kaks nädalat. Täiendavad katsetamis- ja jälgimismeetodid peavad olema täidetud, et kinnitada edukat juurutamist protsessi igas etapis. Väljalaskesageduse kohta lisateabe saamiseks vaadake teemat [Värskendusprotsess](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Teadaolevad probleemid

## <a name="employment-detail-entity"></a>Tööhõive üksikasjade üksus

**Tööhõive üksikasjade** üksust on värskendatud järgmiste väljadega: **Maksesagedus**, **Tööhõive kategooria ID**, **Tööhõive tüüp**, **Tööhõive tüübi ID** ja **Soodustuse tööhõive olek**. Nende väljade häälestamise andmed sõltuvad funktsioonihalduses lubatavast eeliste haldusest. Neid välju ei tohiks olemis **Tööhõive üksikasjad** asustada ega värskendada, kuna see põhjustab importimisel tõrkeid.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePointi eelvaade ei tööta mõnes keskkonnas

Kui SharePointi talletatud dokumentide dokumendieelvaade ei tööta, proovige järgmist toimingut.

1. Kinnitage, et administraatori kasutajakontol on kasutaja kirjega seotud meiliaadress. Seda teavet saate vaadata lehel **Kasutaja**. Kui meiliaadressi ei ole seadistatud, peate lisama meili ja pakkuja OData Exceli lisandmooduli kaudu. Vaikimisi ei ole Exceli kujunduses meiliaadressi kaasatud. Peate redigeerima Exceli kujundust, lisama kõik väljad, rakendama ja värskendama. Kui olete need toimingud teinud, saate värskendada administraatori kontot.

2. Kui administraatoril on seostatud meilikonto, logige sisse Human Resourcesisse administraatori mandaatidega.

3. Juurdepääs SharePointi manusele dokumendieelvaate käivitamiseks.

4. Logige sisse teise kasutajakontoga, millel on juurdepääs manustele ja kinnitage, et eelvaade töötab ootuspäraselt.

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)