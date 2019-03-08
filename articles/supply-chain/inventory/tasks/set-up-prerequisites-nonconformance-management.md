---
title: Eeltingimuste seadistamine mittevastavuse halduseks
description: Kasutage seda protseduuri, et lubada mittevastavuse haldamise protsessid.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a4062acc91e024e3a0a41c0b3cb35ff5ffe2a4a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "337666"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Eeltingimuste seadistamine mittevastavuse halduseks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kasutage seda protseduuri, et lubada mittevastavuse haldamise protsessid. Mittevastavus kirjeldab protseduuri või kaupa, millel on kvaliteediprobleem, kus kirjeldav teave sisaldab probleemi allikat ja tüüpi. Protseduur kasutab demoettevõtte USMF andmeid. Tavaliselt teostab selle protseduuri kvaliteedijuht.


## <a name="enable-quality-management-processes-within-the-company"></a>Ettevõttes kvaliteedijuhtimise protsesside lubamine
1. Avage Varude haldus > Seadistus > Varude ja lao halduse parameetrid.
2. Klõpsake vahekaarti Kvaliteedijuhtimine.
3. Tehke väljal Kasuta kvaliteedijuhtimist valik Jah.
    * Valige see parameeter ettevõtte jaoks kvaliteedi haldamise protsesside lubamiseks.  
4. Sisestage väljale Tunnimäär number.
    * Kasutage välja Tunnimäär, et sisestada tunnitasu kohalikus valuutas. Tunnimäära kasutatakse mittevastavusega seotud toimingute kulude arvutamiseks. Tunnimäär ja arvutatud kulud annavad viiteteavet mittevastavuse kohta ega mõjuta teisi funktsioone.  
5. Klõpsake suvandit Aruande seadistus.
    * See leht võimaldab määratleda kvaliteediaruande märkuse tüübid, mida kasutatakse erinevatel kvaliteedijuhtimise aruannetel.  
6. Sulgege leht.
7. Sulgege leht.

## <a name="enable-user-for-nonconformance-processing"></a>Mittevastavuse töötlemise lubamine kasutaja jaoks
1. Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.
    * Mittevastavuse kinnitamise töötlemiseks peab mittevastavusi kinnitavale või tagasilükkavale kasutajale olema lehel Kasutajad määratud väärtus Nimi. Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.  
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtreerida välja Nimi väärtuse „Ricardo” järgi.
    * Kasutage filtrit, et otsida kasutajat, kes mittevastavuse kirjeid kinnitab või tagasi lükkab.  
3. Klõpsake loendis valitud real olevat linki.
    * Mittevastavuse kinnitamise töötlemiseks peab mittevastavusi kinnitavale või tagasilükkavale kasutajale olema lehel Kasutajad määratud väärtus Nimi.  
4. Klõpsake suvandit Kasutaja suvandid.
5. Klõpsake vahekaarti Eelistused.
6. Tehke väljal Luba dokumenditöötlus valik Jah.
    * Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.  
7. Sulgege leht.
8. Sulgege leht.
9. Sulgege leht.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks diagnostikatüüpide määratlemine
1. Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Diagnostika tüübid.
    * Kasutage lehte Diagnostika tüübid diagnostiliste toimingute klassifikatsiooni määratlemiseks. Parandus tuvastab, mis tüüpi diagnostilist tegevust tuleks kinnitatud mittevastavuse korral kasutada, kes peaks seda tegema ja soovitud ja planeeritud lõpetamiskuupäev.  
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Diagnostika.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sulgege leht.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks kvaliteedikulude määratlemine
1. Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Kvaliteedikulud.
    * Kasutage lehte Kvaliteedikulud, et määratleda kulude klassifikatsioon, mida kasutatakse mittevastavustega seotud toimingutes.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Tasukood.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sulgege leht.

## <a name="define-the-operations-for-nonconformance-processing"></a>Mittevastavuste töötlemise jaoks toimingute määratlemine
1. Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Toimingud.
    * Kasutage lehte Toimingud, et määratleda klassifikatsioon tööle, mida saab teha kinnitatud mittevastavuse puhul. Kui seote toimingu mittevastavusega, saate määrata toimingu tegemiseks nõutava teabe seotud materjali, töötundide ja lisakulude kohta. Selle teabe alusel arvutatakse toimingu tegemise hinnanguline kulu.  
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Toimingud.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sulgege leht.

## <a name="define-problem-types-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks probleemitüüpide määatlemine
1. Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Probleemi tüübid.
    * Kasutage lehte Probleemi tüübid mitmesugustes mittevastavuse tüüpides ilmnevate kvaliteediprobleemide klassifikatsiooni määratlemiseks. Mittevastavuse tüübid on Sisemine, Klient, Hankija, Teenuse päring, Tootmine ja Kaastoote tootmine. Üks probleemi tüüp võib olla seotud mitme mittevastavuse tüübiga.  
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Probleemi tüüp.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake suvandit Mittevastavuse tüübid.
    * Kasutage lehte Mittevastavuse tüübid, et lubada probleemi tüübi kasutamine ühes või enamas mittevastavuse tüübis. Näiteks veakoodiga seotud probleemitüüpi saab rakendada kõigis mittevastavuse tüüpides, samas kui kliendikaebuste probleemitüüpi saab rakendada ainult kliendi ja teenuse taotluse mittevastavuse tüüpides.  
6. Klõpsake valikut Uus.
7. Märkige loendis valitud rida.
8. Valige suvand väljal Mittevastavuse tüüp.
9. Sulgege leht.
10. Sulgege leht.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks vahelao tsoonide määratlemine
1. Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Vahelao tsoonid.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Vahelao tsoon.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sulgege leht.

