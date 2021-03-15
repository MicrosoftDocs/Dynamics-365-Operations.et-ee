---
title: Pearaamatu käibemaksu sisestusgruppide seadistamine
description: Käibemaks arvutatakse ja sisestatakse põhikontodele, mis on määratud pearaamatu sisestusgruppides.
author: twheeloc
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAccountGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cc96cbdb11f24d727bddfa5fd4aaa579537802a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968450"
---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Pearaamatu käibemaksu sisestusgruppide seadistamine

[!include [banner](../../includes/banner.md)]

Käibemaks arvutatakse ja sisestatakse põhikontodele, mis on määratud pearaamatu sisestusgruppides. Pearaamatu sisestusgrupid on seotud iga käibemaksukoodiga. Saate iga käibemaksukoodi jaoks seadistada individuaalseid pearaamatu sisestusgruppe, kasutada ühte pearaamatu sisestusgruppi kõigi käibemaksukoodide jaoks või määrata käibemaksukoodidele mitu pearaamatu sisestusgruppi. Salvestamisel kasutatakse demoettevõtet DEMF. 

1. Avage **Navigeerimispaan > Moodulid > Maks > Seadistus > Käibemaks > Pearaamatu sisestusrühmad**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Pearaamatu sisestusrühm**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Valige väljal **Väljundkäibemaks** põhikonto väljundkäibemaksule, mis makstakse maksuametile. Käibemaksu kogutakse maksuhalduri nimel maksustatavate kaupade ja teenuste müümisel.  
6. Valige väljal **Sisendkäibemaks** põhikonto sisendkäibemaksule, mis saadakse maksuametilt. Hankijad koguvad makse maksuhalduri nimel maksustatavate kaupade ja teenuste ostmisel. See väli ei ole kohaldatav, kui lehel **Pearaamatu parameetrid** on valitud suvand Rakenda käibemaksuga maksustamise reeglid. Selle asemel debiteeritakse hankijatele makstud käibemaks samale kontole kui ost.   
7. Valige väljal **Kasuta maksukulu** põhikonto mahaarvatud kasutusmaksud, mis ei ole sisse nõutud ega maksuametile tarnijate poolt teavitatud vastavalt EL-i pöördmaksustamisele GST/HST. Suvand **Kasuta maksu** peab olema valitud tehingus kasutatavale **Käibemaksukoodile** jaotises **Käibemaksu rühm**. See väli ei ole kohaldatav, kui lehel **Pearaamatu parameetrid** on valitud suvand **Rakenda käibemaksuga maksustamise reeglid**.   
8. Valige väljal **Kasuta väljundkäibemaksu** põhikonto maksuametile makstava sissetuleva kasutusmaksu jaoks. Suvand **Kasutusmaks** peab jaotise **Käibemaksukood** rühmas **Käibemaksurühm** olema valitud, et saaks sisestada **Kasutusmaksu**. Kui lehel **Pearaamatu parameetrid** on valitud suvand **Rakenda käibemaksuga maksustamise reeglid**, sisestatakse vahe tehingu kulukontole.   
9. Valige väljal **Arvelduskonto** põhikonto, millele sisestatakse nende pearaamatu kontode netosaldo, mis on määratletud väljadel **Kasuta väljundkäibemaksu** ja **Sisendkäibemaks**. Saldo luuakse siis, kui käibemaks arveldatakse ja sisestustöö on käitatud.  Kui arveldusperioodi maksuamet on seotud tarnija kontoga, sisestatakse saldo hoopis tarnija kontole.
10. Valige väljal **Tarnija sularaha allahindlus** põhikonto selle pearaamatu sisestusrühmaga seotud käibemaksukoodidele sularaha allahindluse sisestamiseks. See on valikuline ja kui kontot ei sisestata, kasutatakse **Sularaha allahindluskoodide** põhikontot. Võib olla kasulik kasutada erinevaid kontosid **Pearaamatu sisestusrühma** kohta, kui kasutatakse käibemaksu rühmades sularaha allahindluse valikul pöördkäibemaksu.  
11. Valige väljal **Kliendi teenindusjuhtumi allahindlus** põhikonto nende **Käibemaksukoodide** allahindluse sisestamiseks, mis on seotud selle **Pearaamatu sisestusrühmaga**. See on valikuline ja kui kontot ei sisestata, kasutatakse **Sularaha allahindluskoodide** põhikontot. Võib olla kasulik kasutada erinevaid kontosid **Pearaamatu sisestusrühma** kohta, kui kasutatakse **Käibemaksu rühmades** sularaha allahindluse valikul pöördkäibemaksu.  
12. Klõpsake valikut **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]