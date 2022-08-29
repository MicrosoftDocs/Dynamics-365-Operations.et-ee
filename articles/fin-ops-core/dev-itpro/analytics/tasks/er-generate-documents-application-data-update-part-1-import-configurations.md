---
title: Konfiguratsioonide importimine rakendusandmetega dokumentide loomiseks
description: Selle protseduuri sammude lõpuleviimiseks peate esmalt lõpule viima protseduuri. "ER Looge konfiguratsioonipakkuja ja märkige see aktiivseks".
author: kfend
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ccff17ad83b6840b5e8f327e24f8ac8a5e8ff620
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290570"
---
# <a name="import-configurations-to-generate-documents-that-have-application-data"></a>Konfiguratsioonide importimine rakendusandmetega dokumentide loomiseks

[!include [banner](../../includes/banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt läbima protseduuri „ER Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks”.

Konfiguratsioonipakkuja loomine ja aktiivseks märkimine". Selles protseduuris selgitatakse, kuidas importida näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioone ja neid kasutada elektroonilise dokumendi genereerimiseks. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia DEMF-i andmekomplekti abil. Enne alustamist laadige alla ja salvestage spikridokumendis loetletud failid" "Elektrooniliste dokumentide loomine ja rakendusandmete uuendamine ER-tööriistaga" (genereeri elektrooniliste dokumentide uuendamise/rakenduse andmed). Failid on Intrastat (model).xml, Intrastat (mapping).xml ja Intrastat (format).xml.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.  
    * Selle protseduuri toimingutes kirjeldatakse, kuidas kasutada elektroonilise aruandluse funktsioone rakenduse andmete värskendamise lõpuleviimiseks ja kuidas luua Intrastati aruannet. Aruandlusprotsessi üksikasjad arhiivitakse rakenduse tabelites. Kui praegu aktiveeritakse Intrastat-aruandluse protsess Inrtastati vormilt, toimub arhiivimine olemasolevas lähtekoodis programmeeritud loogika põhjal. Selles protseduuris konfigureerite sarnase ent samas lihtsustatud rakenduste andmete loogika ainult elektroonilise aruandluse raamistikku kasutades. Lähtekoodi ei muudeta.   

## <a name="import-er-configurations"></a>Elektroonilise aruandluse konfiguratsioonide importimine
1. Klõpsake valikut Aruandluse konfiguratsioonid.
2. Klõpsake nuppu Vahetus.
3. Klõpsake nuppu Laadi XML-failist.
    * Importige elektroonilise aruandluse konfiguratsioon, mis sisaldab andmemudelit, mida kasutatakse andmeallikatena Intrastat-aruande genereerimiseks. Hiljem saate seda andmemudelidefinitsiooni laiendada, et seda kasutada rakenduse andmete värskendamiseks, et arhiivida Intrastat-aruandluse protsessi üksikasju.   
    * Klõpsake valikut Sirvi ja vali Intrastati fail (model).xml.  
4. Klõpsake nuppu OK.
5. Tehke puul valik „Intrastat (model)".
6. Klõpsake valikut Kujundaja.
7. Laiendage puul valikut „For outgoing document”.
8. Laiendage puul valikut „For outgoing document\Transactions".
    * Vaadake üle imporditud andmemudeli struktuur. Pange tähele, et juurkaup „Väljamineva dokumendi jaoks” on määratletud selleks, et määrata andmevoog andmete saamiseks avaldusest ja kasutada seda andmeallikana Intrastat-aruande genereerimisel. „Kanded: (Kirjete loend)” on kasutuses teavitamist nõudvate Intrastat-kannete loendi esitamiseks. Kuna arhiivite teavitatud artiklikoodid, on selles andmevoos vaja ühe artiklikoodi „Commodity rec id (Int64)” kordumatut identifikaatorit.   
9. Sulgege leht.
10. Klõpsake nuppu Vahetus.
11. Klõpsake nuppu Laadi XML-failist.
    * Importige elektroonilise aruandluse vastenduskonfiguratsioon, mis määrab avaldusest hangitavate andmete andmevoo ja seejärel kasutab seda Intrastat-aruande genereerimiseks. Hiljem saate seda mudelivastenduse definitsiooni laiendada andmete hankimiseks Intrastat-aruandest ja kasutada seda avalduse andmete värskendamiseks, et arhiivida Intrastat-aruandluse protsessi üksikasju.   
    * Klõpsake valikut Sirvi ja vali Intrastati fail (mapping).xml.  
12. Klõpsake nuppu OK.
13. Laiendage puul valikut „Intrastat (model)".
14. Tehke puul valik „Intrastat (model)\Intrastat (mapping)".
15. Klõpsake valikut Kujundaja.
    * Pange tähele, et praegune mudelivastendus sisaldab väljal Suund väärtust „Mudelini”. See tähendab, et selle mudeli vastendamine on mõeldud andmete hankimiseks avaldusest ja selle talletamiseks andmemudelisse.  
16. Klõpsake valikut Kujundaja.
17. Laiendage puul valikut „List".
18. Laiendage puul valikut „Transactions= List".
    * Vaadake üle mudeli vastendamise struktuur, mis kasutab juurkauba „Väljamineva dokumendi jaoks“ põhjal filtreeritud andmemudelit. Pange tähele, et lisatud andmeallikas „Loend“ annab juurdepääsu vajalikele avaldusandmetele ehk Intrastati tabeli kirjete loendile.  
19. Sulgege leht.
20. Sulgege leht.
21. Klõpsake nuppu Vahetus.
22. Klõpsake nuppu Laadi XML-failist.
    * Importige elektroonilise aruandluse (ER) vormingu konfiguratsioon, mis määrab Inrtastat-aruande paigutuse ja andmete asustamise protsessi aruandesse. Hiljem saate seda vormingu definitsiooni laiendada andmete paigutamiseks Intrastat-aruandest andmemudelisse ja seejärel kasutada seda avalduse andmete värskendamiseks, et arhiivida Intrastat-aruandluse protsessi üksikasju.   
    * Klõpsake valikut Sirvi ja vali Intrastati fail (format).xml.  
23. Klõpsake nuppu OK.
24. Tehke puul valik „Intrastat (model)\Intrastat (format)".
25. Klõpsake valikut Kujundaja.
26. Klõpsake nuppu Laienda/ahenda.
27. Tehke puul valik „File\Declaration".
28. Klõpsake vahekaarti Vastendus.
29. Tehke puul valik „File".
    * Vaadake üle Intrastat-aruande genereerimiseks kasutatud vormingu struktuur. Pange tähele, et see on mõeldud XML-faili genereerimiseks andmete asustamise abil andmemudelist, mille aluseks on juurkaup „Väljamineva dokumendi jaoks”. Kontrollige, kas genereeritud faili nimi on määratud kasutaja dialoogi vormil (selle jaoks kasutatakse andmeallikat „fn”).   
30. Sulgege leht.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
