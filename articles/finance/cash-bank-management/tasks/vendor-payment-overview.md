---
title: Hankija maksete ülevaade
description: See ülesande juhend annab ülevaate hankija maksete loomiseks kasutatavate eri meetodite, sh selle kohta, kuidas kasutada maksesoovitust või sisestada ühekordset makset käsitsi.
author: kweekley
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4402be4be52f71bf346a1f85155aad4b9890b3bc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827286"
---
# <a name="vendor-payment-overview"></a>Hankija maksete ülevaade

[!include [banner](../../includes/banner.md)]

See ülesande juhend annab ülevaate hankija maksete loomiseks kasutatavate eri meetodite, sh selle kohta, kuidas kasutada maksesoovitust või sisestada ühekordset makset käsitsi. See protsess kasutab demoettevõtte USMF-i andmeid.

1. Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksed > Maksete tööleht**.
2. Klõpsake valikut **Uus**.
3. Valige maksetööleht, millele hankija maksed salvestada. 
4. Valige tööleht või sisestage see käsitsi.
5. Klõpsake **Read**.
6. Klõpsake **tegevuspaanil** valikut **Maksesoovitus**.
7. Klõpsake suvandit **Loo maksesoovitus**. Maksesoovitus on päring, mida kasutatakse maksearvete valimiseks. Saate redigeerida makstavate arvete loendit enne hankija maksete loomist.
8. Valige maksearved tähtaja, skonto või mõlema järgi. 
9. Sisestage tähtaja või skontoga võrdlemiseks kuupäev. 
10. Valikuline: sisestage kõikide maksete puhul kasutatav maksekuupäev. Siia sisestatud kuupäev on maksekuupäev kõikide lodud maksete puhul, olenemata maksetähtajast või skonto kuupäevast.  
11. Valikuline: sisestage varaseim maksekuupäev, mida võib maksekuupäevana kasutada. Varaseim maksekuupäev on maksete loomisel kasutatav varaseim kuupäev. Näiteks kui arve tähtaeg on pärast varaseimat maksekuupäeva, muutub tähtaeg varaseima maksekuupäeva asemel maksekuupäevaks, et võimaldada arve maksmist võimalikult hilisel kuupäeval.
12. Sisestage täiendavad päringu piirangud jaotises **Kaasatavad kirjed**. Filtrit kasutatakse sageli hankijagrupi või makseviisi makse puhul valitud arvete piiramiseks. Näiteks võite lisada filtri, et maksta arveid ainult selle palgaarvestusperioodi registreerimise järgi.
13. Sisestage täiendav päringu piirang või makse vaikesätted. Täiendavaid parameetreid saab kasutada makse valuuta määratlemiseks või selle palgaarvestusperioodi tsentraliseeritud maksete võimaldamiseks.  
14. Klõpsake valikut **OK**. Pärast nupu **OK** klõpsamist kuvatakse päringu tulemused. Kui te ei soovi maksmiseks valitud arvete loendit eelvaadata, saate naasta kiirkaardile **Parameteetrid** ja muuta sätte **Maksete loomine ilma arve eelvaateta** valikule Jah.  
15. Valige nupp **Kuva maksete ülevaade**, et vaadata valitud arvel hankija puhul loodavaid makseid.
16. Valige maksete peitmiseks nupp **Peida maksete ülevaade**. 
17. Klõpsake suvandit **Maksete loomine**. Enne nupu **Loo maksed** valimist saate paremklõpsata ruudustikul ja eksportida arvete loendi Excelisse. Nupp **Loo maksed** loob makse töölehel hankija maksed.  
18. Skannige makseid ja veenduge, et makseviis oleks määratletud kõikide maksete puhul. Maksete loomisel, nt tšeki printimisel või elektroonilise makse loomisel peab olema määratletud makseviis. Makseviis määrab vaikimisi ka pangakonto, millelt makse tehakse.  
19. Ühekordse makse loomiseks klõpsake nuppu **Uus**. Ühekordse makse saab maksetöölehele lisada mis tahes ajal enne sisestamist. Selleks klõpsake **Maksesoovituse** kasutamise asemel pigem nuppu **Uus** ja lisage makseteave käsitsi.  
20. Valige hankija, kellele makse tehakse.
21. Kui makstav arve on olemas, valige arve maksmiseks valimiseks suvand **Kannete tasakaalustamine**. Kui tegemist on ettemaksuga, on see etapp valikuline. Saate luua makse ilma arvet valimata. 
22. Märkige kõik arved, mis makstakse. Kasutades maksearvete valimiseks suvandit **Kannete tasakaalustamine**, arvutatakse maksesumma automaatselt selle põhjal, millised arved makse puhul märgite ja millise summa sisestate väljale **Tasakaalustatav summa**.
23. Klõpsake valikut **OK**.
24. Kui soovite makse kustutada, märkige rida.
25. Klõpsake  **Kustuta**. Makse kustutamine kustutab ainult makse. Mis tahes makse puhul märgitud arved on teise maksega tasumiseks endiselt saadaval.
26. Klõpsake nuppu **Jah**.
27. Valige tšekkide printimiseks või elektroonilise maksefaili loomiseks suvand **Loo makse**.
28. Valige makseviis, mille soovite luua. Maksetööleht võib sisaldada makseid nii tšekkide kui ka elektrooniliste maksete puhul, kuid saate luua ainult ühe maksetüübi korraga.
29. Valige pangakonto, millelt makseid luua.
30. Klõpsake valikut **OK**. Maksed luuakse ainult maksete puhul, mis ühtivad teie valitud **makseviisi** ja **pangakontoga**.
31. **Tšekkide** loomisel valige suvand **Document**, tagamaks tšekkidele õige printimise sihtkoht.
32. Klõpsake valikut **OK**.
33. Maksete loomiseks klõpsake nuppu **OK**.
34. Kui kõik maksed on kinnitatud ja loodud, klõpsake käsku **Sisesta**. 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]