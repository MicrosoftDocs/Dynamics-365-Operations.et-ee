--- 
title: Vabas vormis arve loomine
description: "Selles tegevuse juhises näitlikustatakse, kuidas vabas vormis arvet luua."
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: a9f9a780868926009f30cee6aa634c53ca870b3f
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-free-text-invoice"></a>Vabas vormis arve loomine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selles tegevuse juhises näitlikustatakse, kuidas vabas vormis arvet luua. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage Müügireskontro > Arved > Kõik vabas vormis arved.
2. Klõpsake valikut Uus.
3. Valige väärtus väljal Kliendi konto.
    * Arvekonto on vaikimisi sama konto, mida kasutatakse kliendikontona.   
    * Kui arve pole sisestatud, algab raamatupidamisolek sõnaga „Pooleli”.   
    * Pärast arve sisestamist määratakse arve number.  
    * Kui kasutate SEPA lubasid, täidetakse kliendikonto valimisel otsekorralduse luba loaga automaatselt.  
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Määrake valik kontonumber ilma dimensioonideta väljal Põhikonto.
    * Samuti saate konto leidmiseks kasutada otsingut, sisestades põhikonto kohta ühe või mitu märki. Selles juhises saate hiljem ka dimensioonid sisestada.  
6. Põhikontole dimensioonide lisamiseks laiendage kiirkaart Rea üksikasjad.
7. Klõpsake vahekaarti Finantsdimensiooni rida.
    * Dimensioonid on ette nähtud ainult valitud reale.    
    * Käibemaksugrupp täidetakse kliendilt. Kui kliendil ei ole käibemaksugruppi, kasutatakse põhikonto käibemaksugruppi.  
    * Kauba käibemaksugrupp täidetakse põhikontolt. Kui põhikontol pole kauba käibemaksugruppi, kasutatakse pearaamatu käibemaksuparameetrite lehel olevat kauba käibemaksugruppi.    
8. Sisestage arv väljale Kogus.
    * Kogus on valikuline.  
9. Sisestage arv väljale Ühiku hind.
    * Ühiku hind on valikuline.  
    * Summa arvutamiseks korrutatakse kogus ühikuhinnaga. Teil on ka võimalus see arvutus tühistada ja sisestada summa.  
10. Arve jaoks arvutatud käibemaksu kuvamiseks klõpsake valikut Käibemaks.
    * Käibemaksusummasid saate vaadata sellelt lehelt või tühistada summad vahekaardil Korrigeerimine.  
11. Klõpsake nuppu OK.
12. Arvele tasu lisamiseks klõpsake valikut Tasud. 
13. Sisestage väärtus väljale Tasukood.
14. Sisestage arv väljale Tasude väärtus.
15. Sulgege leht.
16. Lõpparve üksikasjade ja kogusummade kuvamiseks klõpsake valikut Kogusummad.
17. Klõpsake valikut Sule.
18. Arve sisestamiseks klõpsake nuppu Sisesta. Enne sisestamist saate toimingu tühistada.
    * Arve printimisaja muutmiseks klõpsake nuppu Praegu, kui soovite igat arvet pärast selle uuendamist printida, või nuppu Pärast, kui soovite printida pärast kõikide arvete uuendamist.  
    * Kui soovite muuta, kuidas kliendi krediidilimiiti enne sisestamist kontrollitakse, muutke suvandit Krediidilimiidi tüüp.  
    * Kui soovite arve printida, valige Jah.  
    * Kui soovite arve sisestada, valige Jah. Saate arve ilma sisestamata printida.  
19. Klõpsake nuppu OK.


