--- 
title: "Hankija maksete ülevaade"
description: "See ülesande juhend annab ülevaate hankija maksete loomiseks kasutatavate eri meetodite, sh selle kohta, kuidas kasutada maksesoovitust või sisestada ühekordset makset käsitsi."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 44b7c02e7c238dcea83c5900620731a7befbbb42
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="vendor-payment-overview"></a>Hankija maksete ülevaade

[!include[task guide banner](../../includes/task-guide-banner.md)]

See ülesande juhend annab ülevaate hankija maksete loomiseks kasutatavate eri meetodite, sh selle kohta, kuidas kasutada maksesoovitust või sisestada ühekordset makset käsitsi. See protsess kasutab demoettevõtte USMF-i andmeid.

1. Avage Ostureskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
3. Valige maksetööleht, millele hankija maksed salvestada. 
4. Valige tööleht või sisestage see käsitsi.
5. Klõpsake valikut Read.
6. Klõpsake suvandit Maksesoovitus.
7. Klõpsake suvandit Loo maksesoovitus.
    * Maksesoovitus on päring, mida kasutatakse maksearvete valimiseks. Saate redigeerida makstavate arvete loendit enne hankija maksete loomist.  
8. Valige maksearved tähtaja, skonto või mõlema järgi. 
9. Sisestage tähtaja või skontoga võrdlemiseks kuupäev. 
10. Valikuline: sisestage kõikide maksete puhul kasutatav maksekuupäev.
    * Siia sisestatud kuupäev on maksekuupäev kõikide lodud maksete puhul, olenemata maksetähtajast või skonto kuupäevast.  
11. Valikuline: sisestage varaseim maksekuupäev, mida võib maksekuupäevana kasutada.
    * Varaseim maksekuupäev on maksete loomisel kasutatav varaseim kuupäev. Näiteks kui arve tähtaeg on pärast varaseimat maksekuupäeva, muutub tähtaeg varaseima maksekuupäeva asemel maksekuupäevaks, et võimaldada arve maksmist võimalikult hilisel kuupäeval.  
12. Sisestage täiendavad päringu piirangud suvandis Kaasatavad kirjed.
    * Filtrit kasutatakse sageli hankijagrupi või makseviisi makse puhul valitud arvete piiramiseks. Näiteks võite lisada filtri, et maksta selle arvestusperioodi arveid ainult tšekiga.  
13. Sisestage täiendav päringu piirang või makse vaikesätted. 
    * Täiendavaid parameetreid saab kasutada makse valuuta määratlemiseks või selle palgaarvestusperioodi tsentraliseeritud maksete võimaldamiseks.  
14. Klõpsake nuppu OK.
    * Pärast nupu OK klõpsamist kuvatakse päringu tulemused. Kui te ei soovi maksmiseks valitud arvete loendit eelvaadata, saate naasta kiirkaardile Parameetrid ja muuta sätte Maksete loomine ilma arve eelvaateta valikule Jah.  
15. Valige nupp Kuva maksete ülevaade, et vaadata valitud arvel hankija puhul loodavaid makseid.
16. Valige maksete peitmiseks nupp Peida maksete ülevaade. 
17. Klõpsake suvandit Maksete loomine.
    * Enne nupu Loo maksed valimist saate paremklõpsata ruudustikul ja eksportida arvete loendi Excelisse. Nupp Loo maksed loob makse töölehel hankija maksed.  
18. Skannige makseid ja veenduge, et makseviis oleks määratletud kõikide maksete puhul. 
    * Maksete loomisel, nt tšeki printimisel või elektroonilise makse loomisel peab olema määratletud makseviis. Makseviis määrab vaikimisi ka pangakonto, millelt makse tehakse.  
19. Ühekordse makse loomiseks klõpsake nuppu Uus.
    * Ühekordse makse saab maksetöölehele lisada mis tahes ajal enne sisestamist. Selleks klõpsake maksesoovituse kasutamise asemel pigem nuppu Uus ja lisage makseteave käsitsi.  
20. Valige hankija, kellele makse tehakse.
21. Kui makstav arve on olemas, valige arve maksmiseks valimiseks suvand Kannete tasakaalustamine.
    * Kui tegemist on ettemaksuga, on see etapp valikuline. Saate luua makse ilma arvet valimata.  
22. Märkige kõik arved, mis makstakse.
    * Kasutades maksearvete valimiseks suvandit Kannete tasakaalustamine, arvutatakse maksesumma automaatselt selle põhjal, millised arved makse puhul märgite ja millise summa sisestate väljale Tasakaalustatav summa.  
23. Klõpsake nuppu OK.
24. Kui soovite makse kustutada, märkige rida.
25. Klõpsake  Kustuta.
    * Makse kustutamine kustutab ainult makse. Mis tahes makse puhul märgitud arved on teise maksega tasumiseks endiselt saadaval.  
26. Klõpsake nuppu Jah.
27. Valige tšekkide printimiseks või elektroonilise maksefaili loomiseks suvand Loo makse.
28. Valige makseviis, mille soovite luua.
    * Maksetööleht võib sisaldada makseid nii tšekkide kui ka elektrooniliste maksete puhul, kuid saate luua ainult ühe maksetüübi korraga.  
29. Valige pangakonto, millelt makseid luua.
30. Klõpsake nuppu OK.
    * Maksed luuakse ainult maksete puhul, mis ühtivad teie valitud makseviisi ja pangakontoga.  
31. Tšekkide loomisel valige suvand Dokument, tagamaks tšekkidele õige printimise sihtkoht.
32. Klõpsake nuppu OK.
33. Maksete loomiseks klõpsake nuppu OK.
34. Kui kõik maksed on kinnitatud ja loodud, klõpsake käsku Sisesta. 

