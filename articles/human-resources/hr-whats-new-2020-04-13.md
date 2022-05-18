---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (13. aprill, 2020)?
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 13. aprilli 2020 uusi või muutunud funktsioone.
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d9219e3f2da4d398ed7e8bb27337835d42403925
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692803"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (13. aprill, 2020)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3136. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="new-production-release-cadence"></a>Uus tootmise väljalaskesagedus

Alates selle nädala väljalaskest läheb Human Resourcesi väljalaskesagedus üle iganädalaselt värskenduselt kahenädalasele. Ohutute juurutustavadega vastavusse viimise tagamiseks ning teenuse stabiilsuse ja töökindluse kõrgete standardite säilitamiseks kestab teenusevärskenduste juurutamine nüüd kõigisse piirkondadesse kaks nädalat. Täiendavad katsetamis- ja jälgimismeetodid on täidetud, et kinnitada edukat juurutamist protsessi igas etapis. Väljalaskesageduse kohta lisateabe saamiseks vaadake teemat [Värskendusprotsess](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Ümardamistäpsuse välja ei saa pärast ümardamise tüübi määramist redigeerida (435616)

Selle muudatusega on väli **Ümardamistäpsus** nüüd saadaval pärast välja **Ümardamise tüüp** värskendamist.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Puhkuse registreerimise lõppkuupäeva ei saa redigeerida, kui puhkuse plaanil pole viitvõlgade perioode (413628)

Nüüd saate muuta registreerimise lõppkuupäeva, ilma et kuvatakse tõrketeate „Välja lisandumise kuupäeva alus peab olema täidetud”.

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>Tööhõive üksust ei sünkroonita Dataverse'iga (430834)

See muudatus parandab probleemi, mille korral töötamise andmeid ei sünkroonitud Dataverse'iga pärast finantsdimensioonide lisamist. 

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
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]