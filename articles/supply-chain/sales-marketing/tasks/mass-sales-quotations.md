---
title: Loo müügipakkumised hulgi
description: See protseduur näitab, kuidas tõhusalt pakkumisi koostada, pakkudes mitmele kliendile toodete või teenuste komplekte.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acb2b49c7cb2024aec1140d04150bd1ab9d75c14
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7573365"
---
# <a name="mass-create-sales-quotations"></a>Loo müügipakkumised hulgi

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas tõhusalt pakkumisi koostada, pakkudes mitmele kliendile toodete või teenuste komplekte. Selle hulgipakkumise koostamine põhineb pakkumise mallidel. Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega.


## <a name="create-a-quotation-template"></a>Pakkumisemalli loomine
1. Avage Müük ja turundus > Seadistamine > Hinnapakkumised > Malligrupid.
2. Klõpsake valikut Uus.
3. Tippige väljale Grupi ID oma valitud ID.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.
7. Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.
8. Klõpsake valikut Uus.
9. Valige väljal Konto tüüp väärtus Klient.
10. Valige või sisestage väärtus väljal Kliendi konto.
11. Klõpsake nuppu OK.
    * Selleks, et hinnapakkumisest saaks mall, tuleb läbida hinnapakkumise päisel seadistusetapid. Seda tuleb teha enne pakkumisse ridade lisamist.   
12. Klõpsake toimingupaanil valikut Suvandid.
13. Klõpsake suvandit Muuda vaadet.
14. Klõpsake suvandit Päisevaade.
15. Laiendage jaotist Seadistus.
16. Sisestage või valige väärtus väljal Grupi ID.
17. Sisestage väärtus väljale Malli nimi.
18. Tehke väljal Aktiivne valik Jah.
    * Uuele müügipakkumisele malli rakendamisel saab kasutada ainult aktiivseid malle.  
19. Klõpsake toimingupaanil valikut Suvandid.
20. Klõpsake suvandit Muuda vaadet.
21. Klõpsake suvandit Reavaade.
22. Valige või sisestage väärtus väljal Kaup.
23. Tippige väärtus väljale Kaup.
24. Sulgege leht.
25. Sisestage arv väljale Allahindlusprotsent.
26. Klõpsake käsku Lisa rida.
27. Valige või sisestage väärtus väljal Kaup.
28. Tippige väärtus väljale Kaup.
29. Sulgege leht.
30. Sisestage väljale Ühiku hind uus hind või muutke olemasolevat hinda.
31. Klõpsake käsku Lisa rida.
32. Valige või sisestage väärtus väljal Kaup.
33. Tippige väärtus väljale Kaup.
34. Sulgege leht.
35. Sisestage arv väljale Kogus.
36. Sisestage number väljale Allahindlus.
37. Klõpsake nuppu Salvesta.

## <a name="apply-the-template-to-create-a-single-quotation"></a>Rakendage malli ühe pakkumise koostamiseks
1. Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.
    * Pange tähele, et äsja koostatud pakkumine on märgitud mallina.  
2. Klõpsake valikut Uus.
3. Valige väljal Konto tüüp väärtus Klient.
4. Valige või sisestage väärtus väljal Kliendi konto.
5. Laiendage jaotist Mall.
6. Sisestage või valige väärtus väljal Grupi ID.
7. Sisestage või valige väärtus väljal Malli nimi.
8. Tehke väljal Arvutusmeetod valik Põhineb näidisväärtustel.
9. Klõpsake nuppu OK.
    * Uus pakkumine on nüüd koostatud, tuginedes malli andmetele ja tingimustele.  
10. Sulgege leht.
11. Sulgege leht.

## <a name="apply-the-template-to-mass-create-quotations"></a>Rakendage malli hulgipakkumiste koostamiseks
1. Avage Müük ja turundus > Müügipakkumised > Pakkumise uuendamine > Pakkumiste hulgiloomine.
2. Valige väljal Konto tüüp väärtus Klient.
3. Sisestage või valige väärtus väljal Grupi ID.
4. Sisestage või valige väärtus väljal Malli nimi.
5. Tehke väljal Arvutusmeetod valik Põhineb näidisväärtustel.
6. Jaotise kaasamiseks laiendage kirjeid.
7. Klõpsake käsku Filtreeri.
8. Määrake väljal Kriteeriumid filter, mis hõlmab klientide hulka, keda soovite hulgipakkumise koostamisse kaasata. Kasutage järgmist vormingut: Customer1..CustomerN.
    * Näiteks saab määrata filtriks US-001..US-004  
9. Klõpsake nuppu OK.
10. Klõpsake nuppu OK.
11. Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.
    * Kontrollige, et pakkumised on koostatud valitud malli põhjal kõigile klientidele, kes on hulgiuuendamise protseduuris määratud.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]