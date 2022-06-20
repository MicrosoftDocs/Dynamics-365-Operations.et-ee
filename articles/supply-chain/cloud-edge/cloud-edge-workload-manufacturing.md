---
title: Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks
description: See artikkel kirjeldab, kuidas tootmise käivitamise töökoormused töötavad pilve ja servaskaala üksustega.
author: johanhoffmann
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: johanho
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: c73c2440d8807e965e5d2d89105c2a8a6971c849
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865320"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a>Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Tootmise käivitamise töökoormus on praegu saadaval ainult eelvaates.
>
> Mõni ettevõtte funktsionaalsus ei ole avalikus eelvaates täielikult toetatud juhul, kui kasutatakse töökoormuse skaalaüksusi.
>
> Te ei saa käitada eelvaate tootmise käivitamise töökoormust kaaluühikul, kuhu on installitud ka lao käivitamise töökoormus.

Tootmise käivitamisel pakuvad mastaabiüksused järgmisi võimalusi:

- Masina operaatorid ja tööde juhtimise haldurid pääsevad ligi operatiivsele tootmisplaanile.
- Masina operaatorid saavad plaani ajakohasena hoida, töötades eraldi ja menetledes tootmise töid.
- Tööde juhtimise haldur saab tegevuskava korrigeerida.
- Töötajatel on juurdepääs aja ja kohalolekt sisse-ja väljaregistreerimisele serval, et tagada õiglane töötaja tasu arvutamine.

See artikkel kirjeldab, kuidas tootmise käivitamise töökoormused töötavad pilve ja servaskaala üksustega.

## <a name="the-manufacturing-lifecycle"></a>Tootmise elutsükkel

Nagu järgnev illustratsioon näitab, on tootmise elutsükkel jagatud kolmeks faasiks: *Planeeri*, *Käivita* ja *Lõpeta*.

[![Ühe keskkonna kasutamisel on tootmise käivitamise faasid](media/mes-phases.png "Tootmise täideviimisfaasid ühe keskkonna kasutamisel.")](media/mes-phases-large.png)

_Planeerimise_ faas hõlmab toote määratlust, planeerimist, tellimuse loomist ja ajastamist ning müügile laskmist. Müügile laskmise etapp näitab üleminekut _planeerimise_ faasist _käivitamise_ faasi. Kui tootmistellimus on müügile lastud, on tootmistellimuse tööd tootmiskorrusel nähtavad ja valmis täitmiseks.

Kui tootmistöö on märgitud lõpetatuks, liigub see käivitamise _Käivitamise_ faasist _lõpetamise_ faasi. _Lõpetamise_ faasis kinnitatakse *Käivitamise* faasi registreerimised läbi töövoo, kus need arvutatakse, kinnitatakse ja kantakse üle. Sel hetkel on tootmistellimus lõpetatud. Seetõttu luuakse töötajate töötasu alus.

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a>Käivitamise etapi tükeldamine eraldi töökoormuseks

Nagu järgmine illustratsioon näitab, kui kasutatakse astmiku ühikuid, tükeldatakse _Käivitamise_ faas eraldi töökoormusena.

[![Tootmise käivitamise faasid, kui kasutatakse astmiku ühikuid](media/mes-phases-workloads.png "Tootmise käivitamise faasid, kui kasutatakse astmiku ühikuid.")](media/mes-phases-workloads-large.png)

Mudel läheb nüüd kohesest installist mudelile, mis põhineb keskusel ja skaala ühikutel. Faasid _Plaanimine_ ja _Lõpetamine_ käivitatakse keskuses tagatoatoimingutena ja tootmise täideviimise töökoormus käivitatakse skaalaüksustes. Andmed edastatakse asünkroonselt keskuse ja astmiku ühikute vahel.

Kui tootmistellimus vabastatakse keskuses, kantakse kõik tootmise tööde töötlemiseks vajalikud andmed üle skaalajaotise üksusse. Need andmed hõlmavad tootmistellimusi, tootmisviise, materjaliarveid ja tooteid. Andmed, mis ei ole seotud tootmistellimusega (nagu kaudsed tegevused, koodide puudumised ja tootmisprotsessi parameetrid), kantakse samuti keskusest üle astmiku ühikusse. Reeglina, andmed, mis pärinevad keskusest ja mis kantakse üle skaala ühikule, saab luua või uuendada ainult keskuses. Näiteks ei saa uut puudumise koodi või kaudset toimingut luua skaala ühikus&mdash;mida saab kasutada ainult registreerimiseks. Mooduli käivitamisel tehtud registreerimised viiakse seejärel üle keskusesse, kus töödeldakse aja ja kohalolu kinnitust, laoseisu ja finantsvärskendusi.

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a>Tootmise käivitamise toimingud, mida saab töömahu korral käitada

Järgmisi tootmise käivitamise toiminguid saab praegu käitada töömahu puhul, kui kasutatakse skaala ühikuid:

- Sisseregistreerimine, sisselogimine, väljaregistreerimine ja puudumine
- Alusta tööd
- Tööde kogum
- Edenemisest teadaandmine
- Teata praagist
- Kaudne tegevus
- Paus
- Teata lõpetamisest ja ära panemisest (nõuab, et käivitate ka lao käivitamise töökoormuse oma kaaluühikul, vt ka [Lõpetatuna kinnitamine ja mõõtude laadimine kaaluühikul](#RAF))

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a>Töötamine tootmise käivitamise töömahuga keskuses

Tavaliselt käivituvad tootmise käivitamise töökoormuse käitamiseks vajalikud protsessid automaatselt, et hoida keskus ja kõik ühikud sünkroonis vastavalt vajadusele. Kuid kui teil on probleeme, saate käsitsi käivitada töötlemata registreerimiste töötluse, mis on saadud töömahustt ja/või kontrollida registreerimise töötluse logi.

### <a name="manually-process-raw-registrations"></a>Töötlemata registreerimiste käsitsi töötlemine

Pakett-töö töötleb rakenduses Supply Chain Management automaatselt kõiki töökoormusest saadud registreerimisi. See töö loob nõutavad tootmis töölehed ja logiraamatu kirjed, kui valmis tööle on töömahus registreeritud.

Kuigi töö tavaliselt käivitub automaatselt, saate selle käivitada käsitsi mis tahes ajal, logides keskusesse sisse ja minnes **Tootmise kontrolli \> Perioodilised ülesanded \> BackOffice töömahu haldamise \> Töötle töötlemata registreerimisi**.

### <a name="check-the-raw-registration-processing-log"></a>Kontrollige töötlemata registreerimise töötluse logis

Registreerimise töötlemise Logi ülevaatamiseks logige keskusesse sisse ja minge **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse haldamine \> töötlemata registreerimise töötlemise Logi**. Lehel **Töötlemata registreerimise töötluse logi** kuvatakse töötlemata registreerimiste loend ja iga registreerimise olek.

![Töötlemata registreerimise töötluse logi.](media/mes-processing-log.png "Töötlemata registreerimise töötluse logi")

Saate töötada mis tahes registreerimisega loendis valides selle ja seejärel valides Tegevuse Paanilt ühe järgmistest nuppudest:

- **Töötle** – Valitud registreerimise käsitsi töötlemine. See tegevus võib olla kasulik, kui _Protsessi töötlemata registreerimiste_ töö pole käivitatud või kui see nurjus.
- **Tühista** – valitud registreeringu tühistamine.

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a>Töötamine tootmise käivitamise töömahuga skaalaühikus

Tavaliselt käivituvad tootmise käivitamise töökoormuse käitamiseks vajalikud protsessid automaatselt, et hoida keskus ja kõik ühikud sünkroonis vastavalt vajadusele. Kui teil on probleeme, saate kontrollida skaala ühikus töödeldud tellimuste ajalugu või käitada käsitsi _Tootmise keskust, et mastaapida ühiku teate protsessori_ töö.

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a>Vaata skaalaühikus töödeldud tootmistööde ajalugu

Skaala ühikus töödeldud tööde ajaloo ülevaatamiseks logige sisse skaala ühiku masinasse ja minge **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse haldamine \> Tööde töötlemise ajalugu**. Lehel **Tootmise tööde töötluse ajalugu** kuvatakse tootmistellimuste töötluse ajalugu skaalaühikul. Saate töötada mis tahes tootmistellimusega loendis valides selle ja seejärel valides Tegevuse Paanilt ühe järgmistest nuppudest:

- **Töötle** – Valitud tootmistellimuse käsitsi töötlemine.
- **Tühista** – Tühistab valitud tootmistellimuse.

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a>Tootmiskeskus skaala ühiku teade protsessori töö jaoks

_Tootmise keskus skaala ühiku teade protsessori_ töö töötleb andmeid keskusest skaala ühikule. See töö käivitatakse automaatselt, kui tootmise käivitamise töökoormus on kasutusel. Kuid saate seda käitada käsitsi igal ajal, minnes **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse halduse \> Tootmise keskusestt skaala ühiku teate protsessorisse**.

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a>Lõpetamisest ja kõrvale panekust teatamine kaaluühikul

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

Selles väljaandes teavitatakse lõpp- ja varjatud toimingutest (valmistoodete, kaastoodete ja kõrvalsaaduste puhul) mis on toeatatud [varude täiskoormuse puhul](cloud-edge-workload-warehousing.md) (mitte tootmise täiskoormuse puhul). Seetõttu peate selle funktsiooni kasutamiseks, kui see on ühendatud kaaluühikuga, tegema järgmist:

- Installige oma kaaluühikusse nii lao käivitamise töökoormus kui ka tootmise käivitamise töökoormus.
- Warehouse Management mobiilirakenduse abil saate teatada lõpetatund ja töödeldud töödest. Tootmispinna käivitamise liides ei toeta praegu neid protsesse.

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

## <a name="enable-and-use-the-start-operation-on-a-scale-unit"></a>Luba ja kasuta algoperatsiooni kaaluühikus

Praeguses vabastamises toetab tootmise ja partiitellimuste [käivitustoimingut lao käivitamise töökoormus](cloud-edge-workload-warehousing.md) (mitte tootmise käivitamise töökoormus). Seetõttu, et kasutada seda funktsiooni siis, kui olete ühendatud kaaluühikuga, peate lõpule viima need ülesanded:

- Installige oma kaaluühikusse nii lao käivitamise töökoormus kui ka tootmise käivitamise töökoormus.
- Lubage laohalduse *töökoormuse tootmistellimuse käivitamine funktsioonihalduses pilve ja servaskaala* ühiku [funktsiooni puhul](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Kasutage tootmis- või partiitellimuse käivitamiseks laohalduse mobiilirakendust.

## <a name="enable-and-use-material-consumption-on-a-scale-unit"></a>Luba ja kasuta materjali tarbimist kaaluühikus

Praeguses väljaandes toetab [laohalduse](cloud-edge-workload-warehousing.md) mobiilirakenduse voogu materjalitarbimise registreerimiseks lao käivitamise töökoormus (mitte tootmise käivitamise töökoormus). Seetõttu, et kasutada seda funktsiooni siis, kui olete ühendatud kaaluühikuga, peate lõpule viima need ülesanded:

- Installige oma kaaluühikusse nii lao käivitamise töökoormus kui ka tootmise käivitamise töökoormus.
- Lubage materjalitarbimise *registreerimine mobiilirakenduses funktsioonihalduses kaaluühiku*[funktsioonis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Kasutage laohalduse mobiilirakendust materjalitarbimise registreerimiseks.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
