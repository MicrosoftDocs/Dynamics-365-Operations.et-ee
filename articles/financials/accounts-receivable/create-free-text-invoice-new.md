--- 
title: Vabas vormis arve loomine
description: See artikkel kirjeldab, kuidas luua vabas vormis arveid.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: et-ee
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a>Vabas vormis arve loomine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas luua vabas vormis arveid. Selle protseduuri jaoks kasutage demoettevõtte USMF andmeid.

## <a name="create-a-free-text-invoice"></a>Vabas vormis arve loomine

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

## <a name="copy-lines"></a>Kopeeri read
Vabas vormis arve ridade kopeerimiseks valige üks või mitu rida ja klõpsake nuppu Kopeeri valitud read. Saate määrata soovitud koopiate arvu ning saate ka kopeerida märkusi ja manused. Saate kopeerida jaotused või lubada sisestamisel nende uuesti loomise. Kui olete read kopeerinud, saate redigeerida teavet vastavalt vajadusele. 

## <a name="create-a-free-text-invoice-from-a-template"></a>Vabas vormis arve loomine mallist
Saate luua vabas vormis arve mallist. Kui valite vahekaardil Arve suvandi Uus mallist, saate uue vabas vormis malli jaoks valida malli nime ja kliendikonto. Saate valida ka vaikeväärtused, nt maksetingimused ja kliendi makseviisi jaoks, või kasutada malliga salvestatud väärtusi. Luuakse uus vabas vormis arve, mille väärtusi saate redigeerida. 


