---
title: Organisatsioonihalduse kodulehekülg
description: Selles teemas on toodud viited ressurssidele, mis aitavad teil Microsoft Dynamics 365 for Finance and Operationsi oma organisatsioonis kasutada.
author: sericks007
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 20421
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a693529b55b66eb940f8215a336d5c4ae0acedd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545852"
---
# <a name="organization-administration-home-page"></a>Organisatsioonihalduse kodulehekülg

[!include [banner](../includes/banner.md)]

Teemas on toodud viited, mis aitavad lauskasutajatel ja administraatoritel konfigureerida rakendust Microsoft Dynamics 365 for Finance and Operations. See sisu aitab neil konfigureerida süsteemi nii, et see töötaks teie organisatsiooni ja äritegevuse puhul sujuvalt ning tulemuslikult.

Suur osa siin nimetatud sisust kohaldub mooduli **Organisatsiooni haldus** funktsioonidele. Kuid on mõned toimingud, nt kirje malli loomine ja kasutamine, mida saab rakendada mis tahes moodulis, et teie organisatsioon tõhusamalt toimiks.

## <a name="number-sequences"></a>Numbriseeriad

Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid. Koondandmete kirjet või kandekirjet, mis nõuab ID-d, nimetatakse *viiteks*. Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma.

- [Numbriseeriate ülevaade](number-sequence-overview.md)
- [Numbriseeriate seadistamine viisardit kasutades](tasks/set-up-number-sequences-wizard.md) (tegevusjuhis)
- [Eraldi numbriseeriate seadistamine](tasks/set-up-number-sequences-individual-basis.md) (tegevusjuhis)

## <a name="organizations"></a>Organisatsioonid

Organisatsiooni on grupp inimesi, kes töötavad koos äriprotsessi või eesmärgi saavutamiseks. Organisatsiooni hierarhia kajastab teie ettevõttesse kuuluvate organisatsioonide vahelisi seoseid.

Organisatsioonide ja organisatsiooni hierarhiate seadistamiseks rakenduses Finance and Operations plaanige kindlasti oma ettevõtte mudel. Organisatsioonimudelil on rakenduse Finance and Operations juurutamisele ja äriprotsessidele oluline mõju.

- [Organisatsioonid ja organisatsiooni hierarhiad](organizations-organizational-hierarchies.md)
- [Organisatsiooni hierarhia kavandamine](plan-organizational-hierarchy.md)
- [Organisatsiooni hierarhia loomine](tasks/create-organization-hierarchy.md) (tegevusjuhis)
- [Juriidilise isiku loomine](tasks/create-legal-entity.md) (tegevusjuhis)
- [Tootmisüksuse loomine](tasks/create-operating-unit.md) (tegevusjuhis)

## <a name="address-books"></a>Aadressiraamatud

Globaalne aadressiraamat on tsentraalne hoidla, kus hoitakse koondandmeid, mida on vaja säilitada kõigi ettevõttesiseste ja väliste isikute ning organisatsioonide kohta, kellega ettevõte suhtleb. Osapoole kirjetega seotud andmete hulka kuuluvad osapoole nimi, aadress ja kontaktandmed.

Pärast globaalse aadressiraamatu loomist, saate luua vajaduse järgi täiendavaid aadressiraamatuid, näiteks eraldi aadressiraamatu iga ettevõtte jaoks oma organisatsioonis või iga tegevusala jaoks.

- [Globaalne aadressiraamat](overview-global-address-book.md)
- [Globaalse aadressiraamatu ja täiendavate aadressiraamatute konfigureerimise plaan](plan-configuration-global-address-book-additional-address-books.md)
- [Globaalse aadressiraamatu konfigureerimine](tasks/configure-global-address-book.md)
- [Aadressiraamatute KKK](qa-address-books.md)

## <a name="workflow"></a>Töövoog

Töövoog on Finance and Operationsisse installitud süsteem, mida saab kasutada eraldi töövoogude või äriprotsesside loomiseks. Töövoo loomisel määratlete dokumendi liikumise või teekonna läbi süsteemi, näidates, kes peab ülesande täitma, otsuse tegema või dokumendi kinnitama.

- [Töövoo ülevaade](overview-workflow-system.md)
- [Töövoo elemendid](workflow-elements.md)
- [Töövoo tegevused](workflow-actions.md)
- [Töövoo loomine](create-workflow.md)

## <a name="electronic-signatures"></a>Digitaalallkirjad

Elektronallkiri kinnitab isiku, kes käivitab või kinnitab protsessi. Mõnes tööstuses on elektronallkiri juriidiliselt sama siduv kui käsitsi kirjutatud allkiri. Elektronallkirjad on määrustele vastavuse nõue mitmes reguleeritud tööstusharus, nt farmaatsia-, toiduainete- ja joogi-, ja lennundus ja kaitsetööstuses.

Finance and Operationsis saate kasutada tähtsateks äriprotsessideks elektronallkirju. Mõnedel protsessidel on sisseehitatud elektronallkirja võimalused. Igale andmebaasi tabelile või väljale saate luua ka allkirjanõuded.

- [Digitaalallkirja ülevaade](electronic-signature-overview.md)
- [Digitaalallkirjade seadistamine](tasks/set-up-electronic-signatures.md) (tegevusjuhis)

## <a name="case-management"></a>Juhtumihaldus

Juhtumite plaanimise, jälgimise ja analüüsimisega saate arendada tõhusaid lahendusi, mida sarnaste probleemide puhul kasutada. Näiteks kui klienditeeninduse esindajad või inimressursside spetsialistid loovad juhtumeid, leiavad nad teadmusartiklitest teavet, mis aitab neil juhtumitega tõhusamalt töötada või neid lahendada.

- [Juhtumihalduse ülevaade](cases.md)
- [Juhtumi turbe, protsesside ja kategooriate konfigureerimine](plan-case-management.md)

## <a name="record-templates"></a>Kirjemallid

Kirjemallid võivad aidata kiiremini kirjeid luua. Saate luua kirje malli nii, et sageli kasutatavaid välja väärtuseid ei pea iga uue kirje jaoks sõnaselgelt sisestama.

- [Kirjemallid](record-templates.md)
- [Andmesisestuse hõlbustamiseks kirje malli loomine](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (tegevuse juhis)
- [Kirje malli abil uue kirje loomine](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (tegevuse juhis)

## <a name="general-organization-administration"></a>Üdine organisatsiooni haldus

- [Ribareklaami või logo muutmine](../get-started/tasks/change-banner-or-logo.md) (tegevusjuhis)
- [Dokumendihalduse konfigureerimine](configure-document-management.md)
- [Meilisõnumi konfigureerimine ja saatmine](configure-email.md)
- [Kuupäeva/kellaaja andmed ja ajavööndid](date-time-zones.md)
