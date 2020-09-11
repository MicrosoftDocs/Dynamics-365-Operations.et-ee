---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (13. aprill, 2020)?
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 13. aprilli 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 729490e7516d8c7aef7232c9f5c227d3207dcd68
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712420"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (13. aprill, 2020)?

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3136. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="new-production-release-cadence"></a>Uus tootmise väljalaskesagedus

Alates selle nädala väljalaskest läheb Human Resourcesi väljalaskesagedus üle iganädalaselt värskenduselt kahenädalasele. Ohutute juurutustavadega vastavusse viimise tagamiseks ning teenuse stabiilsuse ja töökindluse kõrgete standardite säilitamiseks kestab teenusevärskenduste juurutamine nüüd kõigisse piirkondadesse kaks nädalat. Täiendavad katsetamis- ja jälgimismeetodid on täidetud, et kinnitada edukat juurutamist protsessi igas etapis. Väljalaskesageduse kohta lisateabe saamiseks vaadake teemat [Värskendusprotsess](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Ümardamistäpsuse välja ei saa pärast ümardamise tüübi määramist redigeerida (435616)

Selle muudatusega on väli **Ümardamistäpsus** nüüd saadaval pärast välja **Ümardamise tüüp** värskendamist.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Puhkuse registreerimise lõppkuupäeva ei saa redigeerida, kui puhkuse plaanil pole viitvõlgade perioode (413628)

Nüüd saate muuta registreerimise lõppkuupäeva, ilma et kuvatakse tõrketeate „Välja lisandumise kuupäeva alus peab olema täidetud”.

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a>Tööhõive üksust ei sünkroonita Common Data Service'iga (430834)

See muudatus parandab probleemi, mille korral töötamise andmeid ei sünkroonitud Common Data Service'iga pärast finantsdimensioonide lisamist. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Töökalendri ajaintervalli üksuse (431775) mitme ülemüksuse eemaldamine

See muudatus eemaldab **töökalendri ajaintervalli** üksuse mitu ülemüksust.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filtri CAST funktsiooniga ei tööta OData kutse ametikoha töötaja määramise üksuses (431699)

See värskendus sisaldab muudatust, et lubada ODatas CAST-i funktsiooniga filter üksuse **Ametikoha töötaja määramine** jaoks.

## <a name="in-preview"></a>Eelvaates

## <a name="leave-suspension"></a>Puhkuse peatamine

Saate peatada töövõtja puhkuse Human Resourcesis. Puhkuse peatamine lõpetab puhkuse viitvõlad valitud puhkusetüüpide puhul. Kui peatamine toimub pärast viitvõla töötlemist, loob peatatav puhkus eelmääratud korrigeerimise töötaja puhkusesaldo jaoks. Lisateabe saamiseks vt [Puhkuse peatamine](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Edasikandmise reeglid

Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle. Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi. Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Teadaolevad probleemid

## <a name="employment-details-entity"></a>Tööhõive üksikasjade üksus

**Tööhõive üksikasjade** üksus on värskendatud järgmiste väljadega:

- **Maksesagedus**
- **Tööhõive kategooria ID**
- **Tööhõive tüüp**
- **Tööhõive tüübi ID**
- **Soodustuse tööhõive olek**

Nende väljade häälestamise andmed sõltuvad **funktsioonihalduses** lubatavast eeliste haldusest. Ärge asustage ega värskendage neid välju olemis **Tööhõive üksikasjad**, kuna see põhjustab importimisel tõrkeid.

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