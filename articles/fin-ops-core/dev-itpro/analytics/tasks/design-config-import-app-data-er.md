---
title: Elektroonilise aruandluse konfiguratsioonide kujundamine sissetulevate dokumentide sõelumiseks
description: Protseduur näitab, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone sissetuleva elektroonilise dokumendi sõelumiseks.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7235d75aee3b8fdf39492cfbc1760bf6eae4b82e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562852"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a>Elektroonilise aruandluse konfiguratsioonide kujundamine sissetulevate dokumentide sõelumiseks

[!include [banner](../../includes/banner.md)]

Protseduur näitab, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone sissetuleva elektroonilise dokumendi sõelumiseks. Selles protseduuris selgitatakse, kuidas importida näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioone ja neid kasutada sissetulevate elektrooniliste dokumentide sõelumiseks. Selle protseduuri toimingute lõpuleviimiseks peate esmalt läbima protseduuri „ER Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks”.

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.

Need etapid saab lõpule viia ükskõik millise andmekomplekti abil. Enne alustamist laadige alla ja salvestage teemas „Sissetulevate dokumentide sõelumine avalduse andmete värskendamiseks” loetletud failid ([Sissetulevate dokumentide sõelumine](../parse-incoming-electronic-documents.md)). Failid on järgmised: EFSTA model.xml EFSTA format.xml Response1.xml Response2.xml Response3.xml, Response4.xml.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.
2. Valige Aruandluse konfiguratsioonid.
    * Järgmise stsenaariumiga demonstreeritakse sissetulevate XML-vormingus elektrooniliste dokumentide sõelumisfunktsioone: ERP rakendus taotleb andmeid veebiteenusest (nt [efsta](http://efsta.org/) finantsteenus) ja sõelub sissetulevad vastused, et värskendada sobival moel avalduse andmeid. Kõige tõhusamaks sõelumiseks kasutatakse üht ER-i vormingut olenemata eeldatavate sissetulevate XML-vormingus dokumentide erinevast struktuurist.

## <a name="import-and-review-er-configurations"></a>ER-i konfiguratsioonide importimine ja ülevaatamine

Importige ER-i mudeli konfiguratsioon, mis sisaldab näidisandmemudelit, mis on mõeldud sissetuleva faili andmete talletamiseks.

1. Valige Exchange.
2. Valige Laadi XML-failist.
    * Valige suvand Sirvi ja vali EFSTA fail model.xml.
3. Valige nupp OK.
4. Valige puul väärtus „EFSTA mudel”.
5. Valige Kujundaja.
    * Vaadake üle imporditud andmemudeli struktuur. Loetelu enumType määratletakse järgmist tüüpi teenuse vastuste tuvastamiseks: kande esitamise kinnituse saamiseks, viimase esitatud kande kohta teabe saamiseks ja toetamata vastusetüüpide tuvastamiseks.
6. Laiendage puul väärtust „Vastus”.
    * Juurüksus „Vastus” määratletakse selleks, et määrata, millist tüüpi andmeid tuleb toetatud teenuse vastusest hankida, et avalduse andmeid värskendada.
7. Sulgege leht.
    * Impordite ER-i vormingu konfiguratsiooni, mis määrab, kuidas sissetulevaid dokumente sõelutakse ER-i andmemudelisse andmete talletamiseks.
8. Valige Exchange.
9. Valige Laadi XML-failist.
    * Valige suvand Sirvi ja vali EFSTA fail format.xml.
10. Valige nupp OK.
11. Laiendage puul väärtust „EFSTA mudel”.
12. Valige puul väärtus „EFSTA mudel\EFSTA vorming”.
13. Valige Kujundaja.
14. Valige Laienda/ahenda.
    * Vormingus CASE elementi kasutatakse juurena ja see sisaldab kolme pesastatud elementi FILE, mis tähendab, et see vorming on loodud mitmes vormingus sissetulevate failide sõelumiseks.
15. Valige puul väärtus „Vastused\Kande lõpuleviimine\TraC”.
    * Esitatud kande vastus algab juurelemendist „TraC”.
16. Valige puul „Vastused\Viimane kande taotlus\Tra”.
    * Esitatud viimase kande vastus algab juurelemendist „Era”.
17. Valige puul „Vastused\Ootamatu vastus\Tekst”.
    * Lisati kolmas element FILE pesastatud elemendiga TEXT, et tuvastada muud tüüpi vastuseid, mis erinevad ülalmainitust.
18. Valige Vormingu vastendamine mudeliga.
    * Mudeli vastendus sisaldab andmevoo definitsiooni, millega talletada sõelutud sissetuleva dokumendi üksikasju, kasutades andmemudeli üksusi.
19. Valige Kujundaja.
20. Laiendage puul valikut „format”.
21. Laiendage puul valikut „format\Responses: Case(Responses)”.
    * Vaadake üle andmeallika „Vorming” struktuur. Kõiki kolme vastusetüüpi pakutakse eraldi.
22. Valige puul „format\Responses: Case(Responses)\aType”.
    * Lisati andmeallika üksus „aType”, et näidata vastuse tüüpi. See on seotud andmemudeli üksusega „Tüüp”.
23. Valige vahekaart Kinnitused.
24. Valige puul „Type = format.Responses.aType”.
    * ER-i kinnitamine on konfigureeritud selleks, et teavitada kasutajat olukorrast, kui vastuse struktuur ei ühti kande esitamise kinnitusega või viimati esitatud kande teabega (toetamata vastuse puhul).
25. Sulgege leht.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Sissetulevate failide sõelumiseks konfigureeritud ER-i vormingu mudelivastenduse käitamine

Käivitate loodud mudeli vastendamise testimise eesmärgil, et vaadata, kuidas konfigureeritud ER-i vorming sõelub sissetulevaid teenuse vastuseid. See etapp kasutab erinevaid XML-faile, et simuleerida veebiteenuste vastuste eri tüüpe.

1. Avage fail Response1.xml XML-lugeris, nt veebibrauseris. See fail sisaldab lõpuleviidud kande kinnituse üksikasju (juurelement on „TraC”).
2. Valige käsk Käitus.
    * Valige käsk Sirvi ja vali fail Response1.xml.
3. Valige nupp OK.
    * Vaadake loodud väljundit. Vastuse tüüp on õigesti tuvastatud ja sõelutud (`ERModelEnumDataSourceHandler#EFSTA model#enumType#C` tähendab tehingu lõpetamise juhtumit).
    * Avage fail Response2.xml XML-lugejas. See fail sisaldab viimase lõpuleviidud kande teavet (juurelement on „`Tra`”).
4. Valige käsk Käitus.
    * Valige käsk Sirvi ja vali fail Response2.xml.
5. Valige nupp OK.
    * Vaadake loodud väljundit. Vastuse tüüp on õigesti tuvastatud ja sõelutud (`ERModelEnumDataSourceHandler#EFSTA model#enumType#R` tähendab süsteemi taaskäivitamise juhtumit).
    * Avage fail Response3.xml XML-lugejas. See fail algab juurüksusest TraZ ja seda struktuuri ei konfigureeritud ER-i vormingus.
6. Valige käsk Käitus.
    * Valige käsk Sirvi ja vali fail Response3.xml.
7. Valige nupp OK.
    * Vaadake loodud väljundit. Vastuse tüüp on õigesti tuvastatud kui mitte toetatud (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Vastav teade lisati teabelogisse (ER-i kinnitamissätte kohaselt) ja enamik andmemudelist pole täidetud.
    * Avage fail Response4.xml XML-lugejas. Selle faili struktuur on peaaegu sama mis sõelutud failil Response1.xml, v.a juurelemendi „TraC” pesastatud elementide seeria.
8. Valige käsk Käitus.
    * Valige käsk Sirvi ja vali fail Response4.xml.
9. Valige nupp OK.
    * Vaadake loodud väljundit. Vastuse tüüp on õigesti tuvastatud kui mitte toetatud (`ERModelEnumDataSourceHandler#EFSTA model#enumType#U`). Vastav teade lisati teabelogisse ja enamik andmemudelist pole täidetud. Selle käitumise põhjuseks on see, et ER-i vormingu praegune säte eeldab sissetuleva faili juurüksuse pesastatud elementide teatud jada.
10. Sulgege leht.
11. Valige puul väärtus „Vastused\Kande lõpuleviimine\TraC”.
12. Väljal Pesastatud elementide sõelumise järjekord valige „Kõik”.
    * Väljal „Pesastatud elementide sõelumise järjestus” valige Mis tahes, et lubada XML-juurüksuse jaoks pesastatud elementide mis tahes seeria.
13. Valige käsk Salvesta.
14. Valige Vormingu vastendamine mudeliga.
15. Valige käsk Käitus.
    * Valige käsk Sirvi ja vali fail Response4.xml.
16. Valige nupp OK.
    * Vaadake loodud väljundit. Vastusetüüpi on nüüd tuvastatud õigesti failiga Response1.xml võrdsena.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]