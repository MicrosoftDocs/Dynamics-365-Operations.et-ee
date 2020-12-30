---
title: Ostupoliitikate loomine
description: See protseduur näitab, kuidas luua ostupoliitikaid, mis sobiksid teie ostu äriprotsessidega.
author: mkirknel
manager: tfehr
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicyParameters, SysPolicy, RequisitionPurposeRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d4ba2a23f84972391283eaf01cef70a161c75226
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426198"
---
# <a name="create-purchasing-policies"></a>Ostupoliitikate loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua ostupoliitikaid, mis sobiksid teie ostu äriprotsessidega. Enne ostupoliitikate loomist peate seadistama ostupoliitika parameetrid. Ostupoliitikat on võimalik luua, muuta ja aegunuks määrata, kuid ostupoliitikat ei saa kustutada. Seda protseduuri viib tavaliselt läbi ostujuht. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.


## <a name="set-up-policy-parameters"></a>Saate häälestada poliitikaparameetrid
1. Avage navigeerimispaanil **Moodulid > Jange > Häälestus > Poliitika > Ostupoliitika**.
2. Valige toimingupaanil **Parameetrid**.
- Poliitika tähtsusjärjestuse reeglid kehtivad teie organisatsiooni erinevatele tasanditele. Kuvatavad organisatsiooniüksused olenevad teie organisatsiooni hierarhiast ja sellest, millistele hierarhia tasanditele on hanke sisekontrolli eesmärk määratud. Näiteks võib teie organisatsioonil olla juriidilisi isikuid, kulukeskusi, regioone ja osakondi, kuid vaid mõnel neist võib olla hanke sisekontrolli hierarhia eesmärk. Vaikimisi on saadaval organisatsiooni tüüp Ettevõte.  
3. **Klõpsake vahekaarti Poliitika reegli tüübi parameetrid.**
4. **Valige puult Ostupoliitika \ Ostutaotluse juhtimisreegel.**
- Teie määrate poliitika tasandil poliitika otsuste tähtsuse järjekorra. Kuid mõne poliitika tüübi puhul saate alistada üksiku poliitikareegli tüüpide tähtsuse järjekorra. Näiteks võite määratleda ostupoliitikate tähtsuse järjekorraks: kulukeskus, osakond, ettevõte. Kataloogipoliitika reegli puhul võib tähtsuse järjekord olla: osakond, kulukeskus, ettevõte. Tähtsuse järjekorda saab muuta ainult kataloogipoliitika reeglite puhul. Kui töötaja taotluse loob, määratakse kuvatav kataloog töötaja osakonna, seejärel tema kulukeskuse ja seejärel tema ettevõttega seotud poliitikate alusel.  
- Kui loetelus on mitu organisatsioonitasandit, võite kasutada üles-/allanoolt ostutaotluse juhtimisreeglis tähtsusjärjestuse määramiseks.  
5. Sulgege leht.

## <a name="create-a-new-policy"></a>Looge uus poliitika.
1. Valige suvand **Uus**.
2. Sisestage väärtus väljale **Nimi**.
3. Sisestage väärtus väljale **Kirjeldus**.
- Ühe ostupoliitika saab rakendada ainult ühele organisatsiooni hierarhiale. Näiteks võib teil olla üks hierarhia nimega „Geograafiline” ja üks nimega „Osakond” ja kummalgi võib olla erinev ostupoliitika.  
- Valige organisatsioon, millele poliitika peaks kehtima.  
4. Klõpsake noolt valitud organisatsiooni lisamiseks.
- Seda protsessi saab korrata, lisades veel organisatsioone.  

## <a name="add-a-policy-rule"></a>Poliitikareegli lisamine
1. Tehke loendis **Poliitikareegli tüüp** valik **Taotluse eesmärgi reegel**.
- Saate luua reegli, mis määrab taotluse vaike-eesmärgi tüübiks tarbimise, kuid laseb selle asemel valida tüübi Täiendamine.  
2. Valige **Poliitika reegli loomine**.
3. Tehke väljal **Luba käsitsi alistamine** valik **Jah**.
4. Valige suvand **Sule**.
- Nüüd saate seadistada ostupoliitikale teisi poliitikareegleid. Pange tähele, et poliitikareegli tüübil ei saa olla kattuvaid reegleid, mis on ühes hankepoliitikas korraga aktiivsed.  

