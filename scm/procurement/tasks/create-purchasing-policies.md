--- 
title: Ostupoliitikate loomine
description: "See protseduur näitab, kuidas luua ostupoliitikaid, mis sobiksid teie ostu äriprotsessidega."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 51486712d732bba064fd6c9b64dbccb730603877
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-purchasing-policies"></a>Ostupoliitikate loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas luua ostupoliitikaid, mis sobiksid teie ostu äriprotsessidega. Enne ostupoliitikate loomist peate seadistama ostupoliitika parameetrid. Ostupoliitikat on võimalik luua, muuta ja aegunuks määrata, kuid ostupoliitikat ei saa kustutada. Seda protseduuri viib tavaliselt läbi ostujuht. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.


## <a name="set-up-policy-parameters"></a>Saate häälestada poliitikaparameetrid
1. Avage jaotis Ostupoliitikad.
2. Klõpsake valikut Parameetrid.
    * Poliitika tähtsusjärjestuse reeglid kehtivad teie organisatsiooni erinevatele tasanditele. Kuvatavad organisatsiooniüksused olenevad teie organisatsiooni hierarhiast ja sellest, millistele hierarhia tasanditele on hanke sisekontrolli eesmärk määratud. Näiteks võib teie organisatsioonil olla juriidilisi isikuid, kulukeskusi, regioone ja osakondi, kuid vaid mõnel neist võib olla hanke sisekontrolli hierarhia eesmärk. Vaikimisi on saadaval organisatsiooni tüüp Ettevõte.  
3. Klõpsake vahekaarti Poliitika reegli tüübi parameetrid.
4. Valige puult Ostupoliitika \ Ostutaotluse juhtimisreegel.
    * Teie määrate poliitika tasandil poliitika otsuste tähtsuse järjekorra. Kuid mõne poliitika tüübi puhul saate alistada üksiku poliitikareegli tüüpide tähtsuse järjekorra. Näiteks võite määratleda ostupoliitikate tähtsuse järjekorraks: kulukeskus, osakond, ettevõte. Kataloogipoliitika reegli puhul võib tähtsuse järjekord olla: osakond, kulukeskus, ettevõte. Tähtsuse järjekorda saab muuta ainult kataloogipoliitika reeglite puhul. Kui töötaja taotluse loob, määratakse kuvatav kataloog töötaja osakonna, seejärel tema kulukeskuse ja seejärel tema ettevõttega seotud poliitikate alusel.  
    * Kui loetelus on mitu organisatsiooni tasandit, võite kasutada üles-/allanoolt ostutaotluse juhtimisreeglis tähtsusjärjestuse määramiseks.  
5. Sulgege leht.

## <a name="create-a-new-policy"></a>Looge uus poliitika.
1. Klõpsake valikut Uus.
2. Sisestage väärtus väljale Nimi.
3. Sisestage väljale Kirjeldus soovitud väärtus.
    * Ühe ostupoliitika saab rakendada ainult ühele organisatsiooni hierarhiale. Näiteks võib teil olla üks hierarhia nimega Geograafiline ja üks nimega Osakond ja kummalgi võib olla erinev ostupoliitika.  
    * Valige organisatsioon, millele poliitika peaks kehtima.  
4. Klõpsake noolt valitud organisatsiooni lisamiseks.
    * Seda protsessi saab korrata, lisades veel organisatsioone.  

## <a name="add-a-policy-rule"></a>Poliitikareegli lisamine
1. Tehke loendis Poliitikareegli tüüp valik Taotluse eesmärgi reegel.
    * Saate luua reegli, mis määrab taotluse vaike-eesmärgi tüübiks tarbimise, kuid laseb selle asemel valida tüübi Täiendamine.  
2. Klõpsake valikut Loo poliitika reegel.
3. Tehke väljal Luba käsitsi alistamine valik Jah.
4. Klõpsake valikut Sule.
    * Nüüd saate seadistada ostupoliitikale teisi poliitikareegleid.   Pange tähele, et poliitikareegli tüübil ei saa olla kattuvaid reegleid, mis on ühes hankepoliitikas korraga aktiivsed.  
5. Sulgege leht.
6. Sulgege leht.


