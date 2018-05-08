--- 
title: "Pearaamatu käibemaksu sisestusgruppide seadistamine"
description: "Käibemaks arvutatakse ja sisestatakse põhikontodele, mis on määratud pearaamatu sisestusgruppides."
author: twheeloc
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: e50fc2b6b8f4cd91e9a5593297fff2e9a6ef5525
ms.contentlocale: et-ee
ms.lasthandoff: 10/26/2017

---
# <a name="set-up-ledger-posting-groups-for-sales-tax"></a>Pearaamatu käibemaksu sisestusgruppide seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Käibemaks arvutatakse ja sisestatakse põhikontodele, mis on määratud pearaamatu sisestusgruppides. Pearaamatu sisestusgrupid on seotud iga käibemaksukoodiga. Saate iga käibemaksukoodi jaoks seadistada individuaalseid pearaamatu sisestusgruppe, kasutada ühte pearaamatu sisestusgruppi kõigi käibemaksukoodide jaoks või määrata käibemaksukoodidele mitu pearaamatu sisestusgruppi. Salvestamisel kasutatakse demoettevõtet DEMF. 

1. Avage Maks > Seadistus > Käibemaks > Pearaamatu sisestusgrupid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Pearaamatu sisestusgrupp.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Valige väljal Tasumisele kuuluv käibemaks põhikonto maksuametile makstava väljamineva käibemaksu puhul.
    * Käibemaksu kogutakse maksuhalduri nimel maksustatavate kaupade ja teenuste müümisel.  
6. Valige väljal Saadaolev käibemaks põhikonto maksuametilt saadavate sissetulevate maksude puhul.
    * Hankijad koguvad makse maksuhalduri nimel maksustatavate kaupade ja teenuste ostmisel. See väli pole saadaval, kui lehel Pearaamatu parameetrid on valitud suvand Rakenda käibemaksu maksustamisreeglid. Selle asemel debiteeritakse hankijatele makstud käibemaks samale kontole kui ost.   
7. Valige väljal Kasutusmaksu kulu põhikonto mahaarvatavate kasutusmaksude sisestamiseks, mida hankijad pole EL-i GST/HST pöördmaksu osana maksuametile deklareerinud või mille kohta aruandlust esitanud.
    * Suvand Kasutusmaks peab olema valitud käibemaksukoodi puhul kandes kasutatavas käibemaksugrupis.  See väli pole saadaval, kui lehel Pearaamatu parameetrid on valitud suvand Rakenda käibemaksu maksustamisreeglid.   
8. Valige väljal Kasutusmaksu kohustus põhikonto maksuametile makstavate sissetulevate kasutusmaksude sisestamiseks.
    * Suvand Kasutusmaks peab olema kasutusmaksu sisestamiseks käibemaksugrupi käibemaksukoodis valitud. Kui suvand Rakenda käibemaksu maksustamisreeglid on pearaamatu parameetrites valitud, sisestatakse vastaskonto kande kulukontole.   
9. Valige väljal Tasakaalustuskonto põhikonto, millele väljadel Kasutusmaksu kohustus ja Saadaolev käibemaks määratud pearaamatukontode netosaldo sisestatakse.
    * Saldo luuakse käibemaksu tasakaalustamisel ja sisestatud töö käitamisel.  Kui tasakaalustusperioodi maksuhaldur on seotud hankija kontoga, sisestatakse saldo hoopis hankija kontole.   
10. Valige väljal Hankija skonto põhikonto selle pearaamatu sisestusgrupiga seotud käibemaksukoodide skonto sisestamiseks.
    * See on valikuline ja kui kontot pole sisestatud, kasutatakse skonto koodide põhikontot. Pearaamatu sisestusgrupi kohta võib olla kasulik kasutada eri kontosid käibemaksugrupi suvandil skonto pöördkäibemaksu kasutamisel.  
11. Valige väljal Kliendi skonto põhikonto selle pearaamatu sisestusgrupiga seotud käibemaksukoodide skonto sisestamiseks.
    * See on valikuline ja kui kontot pole sisestatud, kasutatakse skonto koodide põhikontot. Pearaamatu sisestusgrupi kohta võib olla kasulik kasutada eri kontosid käibemaksugrupi suvandil skonto pöördkäibemaksu kasutamisel.  
12. Klõpsake nuppu Salvesta.


