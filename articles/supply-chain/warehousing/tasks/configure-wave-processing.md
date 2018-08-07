--- 
title: "Vootöötluse konfigureerimine"
description: "Selles juhendis kirjeldatakse, kuidas seadistada kriteeriumid, mis määravad, milline töö luuakse lao jaoks voo töötlemisel ja kas vooge töödeldakse käsitsi või automaatselt."
author: ShylaThompson
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f7a6db585468c235e07c4a0117a83995ec93f4b0
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="configure-wave-processing"></a>Vootöötluse konfigureerimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles juhendis kirjeldatakse, kuidas seadistada kriteeriumid, mis määravad, milline töö luuakse lao jaoks voo töötlemisel ja kas vooge töödeldakse käsitsi või automaatselt. Kriteeriumite määramiseks seadistage voomallid ja päringud, mis vastavad müügitellimuste, tootmistellimuste ja kanban-tellimuste väljastatud ridadega voole. Voo töötlemist kasutatakse ladudes, mis kasutavad funktsioone laohalduse moodulis, ja mitte nendes, mis kasutavad funktsioone varude halduse moodulis. Võite seda protseduuri käitada demoettevõtte USMF-i andmetega.

1. Avage Laohaldus > Seadistus > Vood > Voomallid.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Voomalli nimi.
    * Kui seadistate voomalli, määrate järjekorra, milles malle vastendatakse väljastatud ridadega müügitellimuste, tootmistellimuste või kanbanide puhul. Kui rida väljastatakse lattu või tootmisse, kasutab see esimese voo malli, mille kriteeriumidele see vastab. Soovitame loendi algusesse panna kõige konkreetsemate kriteeriumidega malli. Mida laiemad on kriteeriumid, seda suurema tõenäosusega täidab rida kriteeriume ja see võib põhjustada ridade määramist valele voole.  
4. Tippige väärtus väljale Voomalli kirjeldus.
5. Sisestage või valige väärtus väljal Koht.
    * Kui te kasutate USMF-i, saate valida tegevuskoha 2.  
6. Sisestage või valige väärtus väljal Ladu.
    * Kui kasutate USMF-i, saate valida lao 24.  
7. Määrake välja Automatiseeri voo loomine väärtuseks Jah.
    * Selle suvandi valimisel luuakse voog automaatselt, kui ostutellimus, tootmistellimus või kanban väljastatakse lattu.  
8. Määrake suvandi Töötle voogu lattu vabastamisel väärtuseks Jah. 
    * Valige see suvand voo automaatseks töötlemiseks ja töö loomiseks, kui rida väljastatakse lattu.  
9. Määrake suvandi Automatiseeri voo vabastamine väärtusele Jah. 
    * Selle suvandi valimisel väljastatakse voog automaatselt. Luuakse komplekteerimistöö ja muudetakse see mobiilsetel seadmetel kättesaadavaks.  
10. Määrake suvandi Määra avatud voogudele väärtuseks Jah. 
    * Read määratakse voogudele voomalli päringufiltri põhjal.  
11. Määrake suvandi Töötle voogu lävele jõudes automaatselt väärtuseks Jah. 
    * Selle suvandi valimisel töödeldakse voogu automaatselt, kui selle väärtused jõuavad väljagrupil Vooläved määratud kaalu, saadetise ja ridade läveni. See suvand on saadaval vaid siis, kui väljal Voo mall on valitud Lähetamine.  
12. Määrake suvandi Automatiseeri täiendustöö väljastamine väärtuseks Jah. 
    * Valige see suvand nõudlusel põhineva täiendustöö loomiseks ja selle automaatseks väljastamiseks. Selleks peab voomallile lisama täiendusvoo meetodi ja looma täiendamismalli tüübiga Voo nõue.  
13. Laiendage jaotist Meetodid.
    * Voomalli meetodid võimaldavad teil juhtida, millises järjekorras töödeldava voo tegevusi tehakse. Näiteks võib teil olla meetod voo täiendamiseks. Meetodi lisamisel viiakse see automaatselt etappide järjekorras õigesse asukohta. Kui olete määranud suvandi Automatiseeri täiendustöö väljastamine olekuks Jah, peate lisama siia täiendamismeetodi.  
    * Voo atribuudid toimivad nagu filtrid, et piirata seda tüüpi kaupu, mis saavad voogu kasutada. Näiteks saate määrata kaubagrupi.  
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.
16. Avage Laohaldus > Seadistus > Laohalduse parameetrid.
17. Laiendage jaotist Voo töötlemine.
18. Sisestage või valige väärtus väljal Voo töötlemise partii grupp.
19. Määrake suvandi Töötle vooge pakktöötlusega väärtuseks Jah.
20. Sisestage väljale Oota lukustust (ms) number.
    * Sisestage aeg (millisekundites), mille jooksul ootab eraldamise etapp süsteemiressurssi, mille on lukustanud muu eraldamise etapp. Kui aeg ületatakse, siis voogu ei töödelda ja kuvatakse tõrketeade.  
21. Klõpsake nuppu Salvesta.
22. Sulgege leht.
23. Avage Tootmise juhtimine > Seadistus > Tootmise juhtimise parameetrid.
24. Valige suvand väljal Lattu väljastamine.
    * Müügitellimuste ja kanban-tellimuste puhul tuleb varud reserveerida enne tellimuse väljastamist lattu. Vastasel korral ei saa kaupu ega eraldamisridu voos töödelda. Tootmistellimuste puhul saate valida ka suvandi Luba osaline reserveerimine. Näiteks on see kasulik, kui teil on olemas tootmise alustamiseks vajalikud materjalid ja on võimalik oodata, kuni täiendavad materjalid kättesaadavaks muutuvad, et protsess lõpule viia. Kui valite selle suvandi, peate lattu väljastamise protsessi käsitsi kordama, kui täiendavad materjalid kättesaadavaks muutuvad.  
25. Sulgege leht.


