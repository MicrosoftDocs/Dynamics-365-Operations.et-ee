---
title: Eeltingimuste seadistamine mittevastavuse halduseks
description: Kasutage seda teemat, et lubada mittevastavuse haldamise protsessid.
author: perlynne
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 80a7ae2249179c561d03f7b729ebb942ba856046
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961506"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a>Eeltingimuste seadistamine mittevastavuse halduseks

[!include [banner](../../includes/banner.md)]

Kasutage seda teemat, et lubada mittevastavuse haldamise protsessid. Mittevastavus kirjeldab protseduuri või kaupa, millel on kvaliteediprobleem, kus kirjeldav teave sisaldab probleemi allikat ja tüüpi. Protseduur kasutab demoettevõtte USMF andmeid. Tavaliselt teostab selle protseduuri kvaliteedijuht.


## <a name="enable-quality-management-processes-within-the-company"></a>Ettevõttes kvaliteedijuhtimise protsesside lubamine
1. Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Ladu > Varude ja laohalduse parameetrid**.
2. Klõpsake vahekaardil **Kvaliteedijuhtimine**.
3. Valige **Jah** väljal **Kasuta kvaliteedijuhtimist**, et lubada kvaliteedijuhtimise protsessid ettevõttele.
4. Sisestage väljale **Tunnimäär** tunnitasu kohalikus valuutas. Tunnimäära kasutatakse mittevastavusega seotud toimingute kulude arvutamiseks. Tunnimäär ja arvutatud kulud annavad viiteteavet mittevastavuse kohta ega mõjuta teisi funktsioone.  
5. Valige **Aruande seadistus**, et määratleda kvaliteediaruande märkuse tüübid, mida kasutatakse erinevatel kvaliteedijuhtimise aruannetel.

## <a name="enable-user-for-nonconformance-processing"></a>Mittevastavuse töötlemise lubamine kasutaja jaoks
1. Avage navigeerimispaneel, seejärel **Moodulid > Süsteemiadministraator > Kasutajad > Kasutajad**. 
2. Kasutage kiirfiltrit, et otsida kasutajat, kes mittevastavuse kirjeid kinnitab või tagasi lükkab. Näiteks saate filtrida välja **Nimi** väärtuse `Ricardo` järgi. Mittevastavuse kinnitamise töötlemiseks peab mittevastavusi kinnitavale või tagasilükkavale kasutajale olema lehel **Kasutajad** määratud väärtus „Nimi”. Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.  
3. Märkige soovitud kirje rida.
4. Valige **Kasutaja valikud**.
5. Valige vahekaart **Eelistused**.
6. Tehke väljal **Luba dokumenditöötlus** valik **Jah**.

## <a name="define-diagnostic-types-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks diagnostikatüüpide määratlemine
1. Navigeerimispaneelil avage **Moodulid > Varude haldus > Seadistus > Kvaliteedihaldus > Diagnostilised tüübid**. Kasutage lehte **Diagnostika tüübid** diagnostiliste toimingute klassifikatsiooni määratlemiseks. Parandus tuvastab, mis tüüpi diagnostilist tegevust tuleks kinnitatud mittevastavuse korral kasutada, kes peaks seda tegema ja soovitud ja planeeritud lõpetamiskuupäev.  
2. Valige suvand **Uus**.
3. Tippige väärtus välja **Diagnostika**.
4. Sisestage väärtus väljale **Kirjeldus**.

## <a name="define-quality-charges-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks kvaliteedikulude määratlemine
1. Navigeerimispaneelil avage **Moodulid > Varude haldus > Seadistus > Kvaliteedihaldus > Kvaliteedikulud**. Kasutage lehte **Kvaliteedikulud**, et määratleda kulude klassifikatsioon, mida kasutatakse mittevastavustega seotud toimingutes.  
2. Valige suvand **Uus**.
3. Sisestage väärtus väljale **Tasukood**.
4. Sisestage väärtus väljale **Kirjeldus**.

## <a name="define-the-operations-for-nonconformance-processing"></a>Mittevastavuste töötlemise jaoks toimingute määratlemine
1. Navigeerimispaneelil avage **Moodulid > Varude haldus > Seadistus > Kvaliteedihaldus > Toimingud**. Kasutage lehte **Toimingud**, et määratleda klassifikatsioon tööle, mida saab teha kinnitatud mittevastavuse puhul. Kui seote toimingu mittevastavusega, saate määrata toimingu tegemiseks nõutava teabe seotud materjali, töötundide ja lisakulude kohta. Selle teabe alusel arvutatakse toimingu tegemise hinnanguline kulu.  
2. Valige suvand **Uus**.
3. Tippige väärtus väljale **Toimingud**.
4. Sisestage väärtus väljale **Kirjeldus**.

## <a name="define-problem-types-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks probleemitüüpide määatlemine
1. Navigeerimispaneelil avage **Moodulid > Varude haldus > Seadistus > Kvaliteedihaldus > Probleemitüübid**. Kasutage lehte **Probleemi tüübid** mitmesugustes mittevastavuse tüüpides ilmnevate kvaliteediprobleemide klassifikatsiooni määratlemiseks. Mittevastavuse tüübid on **Sisemine**, **Klient**, **Hankija**, **Teenuse päring**, **Tootmine** ja **Kaastoote tootmine**. Üks probleemi tüüp võib olla seotud mitme mittevastavuse tüübiga.  
2. Valige suvand **Uus**.
3. Tippige väärtus väljale **Probleemi tüüp**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige **Mittevastavuse tüübid**. Kasutage lehte **Mittevastavuse tüübid**, et lubada probleemi tüübi kasutamine ühes või enamas mittevastavuse tüübis. Näiteks veakoodiga seotud probleemitüüpi saab rakendada kõigis mittevastavuse tüüpides, samas kui kliendikaebuste probleemitüüpi saab rakendada ainult kliendi ja teenuse taotluse mittevastavuse tüüpides.  
6. Valige suvand **Uus**.
7. Valige suvand väljal **Mittevastavuse tüüp**.

## <a name="define-quarantine-zones-for-nonconformance-processing"></a>Mittevastavuse töötlemise jaoks vahelao tsoonide määratlemine
1. Avage navigeerimispaneelil **Moodulid > Varude haldus > Seadistus > Kvaliteedihaldus > Vahelao tsoonid**.
2. Valige suvand **Uus**.
3. Tippige väärtus väljale **Vahelao tsoon**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Sulgege leht.

