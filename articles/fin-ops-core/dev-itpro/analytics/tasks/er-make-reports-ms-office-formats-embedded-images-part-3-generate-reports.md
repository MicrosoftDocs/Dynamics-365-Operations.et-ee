---
title: Manuspiltidega aruannete loomine Office’i vormingus
description: See artikkel kirjeldab, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone, et luua Exceli ja Wordi elektroonilisi dokumente, mis sisaldavad manustatud pilte.
author: kfend
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dfd4aca1013d7fdf408f9057810feedc4b44e586
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290270"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a>Manuspiltidega aruannete loomine Office’i vormingus

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua elektroonilise aruandluse (ER) konfiguratsioone manuspilte sisaldavate elektrooniliste dokumentide loomiseks MS Office'i vormingutes (Excel ja Word).

Selles näites kasutate näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse konfiguratsioone.  Toimingute teostamiseks peab esmalt täitma juhendis „ER MS Office'i vormingutes manuspiltidega aruannete koostamine (2. osa: konfiguratsioonide ülevaatamine)” toodud toimingud. Neid toiminguid saab teha ettevõttes USMF.


## <a name="run-format-with-initial-model-mapping"></a>Vormingu käivitamine algse mudelivastendusega
1. Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.
2. Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega USMF OPER.
3. Klõpsake tegumiribal valikut Seadistus.
4. Klõpsake nuppu Kontrolli.
5. Klõpsake valikut Prindi test.
    * Käivitage testimiseks vorming.  
6. Valige väljal Käibiv tšekivorming väärtus Jah.
7. Klõpsake nuppu OK.
    * Vaadake loodud väljund üle. Aruandes on esitatud nii ettevõtte logo kui ka volitatud isiku allkiri. Allkirja pilt võetakse valitud pangakontoga seotud tšeki paigutusekirje andmetüübi väljalt „Konteiner”.  
8. Laiendage jaotis Eksemplare.
9. Klõpsake nuppu Redigeeri.
10. Sisestage väljale Vesimärk tekst Prindi vesimärk kui Tühista.
    * Muutke vesimärgi paigutuse sätet, et kuvada vesimärgi tekst dokumendi genereerimisel Exceli kujunduselemendis.  
11. Klõpsake valikut Prindi test.
12. Klõpsake nuppu OK.
    * Vaadake loodud väljund üle. Vesimärk kuvatakse loodud aruandes vastavalt valitud suvandile.  
13. Sulgege leht.
14. Klõpsake toimingupaanil valikut Maksete haldamine.
15. Klõpsake nuppu Kontrolli.
16. Klõpsake suvandit Näita filtreid.
17. Rakendage järgmised filtrid: sisestage väljale Tšeki number filtriväärtus „381“, „385“, „389“, kasutades filtri tehtemärki „üks (mitmest)“.
18. Märkige loendis kõik read.
19. Klõpsake valikut Tšeki koopia printimine.
    * Käivitage vorming valitud tšekkide uuesti printimiseks.  
    * Vaadake loodud väljund üle. Valitud tšekid on uuesti prinditud. Ettevõtte logo ja silte ei prindita, kuna need on esitatakse eelprinditud vormil.  

## <a name="modify-the-mapping-of-the-imported-data-model"></a>Imporditud andmemudeli vastenduse muutmine
1. Sulgege leht.
2. Sulgege leht.
3. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
4. Valige puus väärtus Tšekkide mudel.
5. Klõpsake valikut Kujundaja.
6. Klõpsake suvandit Mudeli vastendamine andmeallikaga.
7. Klõpsake valikut Kujundaja.
    * Muudame andmemudeli allkirjaüksuse sidumist, et tuua allkirja pilt failist, mis on manustatud valitud pangakontoga seostatud tšeki paigutusekirjele.  
8. Lülitage välja säte Näita üksikasju.
9. Laiendage puus valik layout.
10. Laiendage puus valik „layout\signature“.
11. Valige puus „layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp“.
12. Laiendage puus valik chequesaccount.
13. Laiendage puus valikut „chequesaccount\<Relations“.
14. Laiendage puus valikut „chequesaccount\<Relations\BankChequeLayout“.
15. Laiendage puus valik „chequesaccount\<Relations\BankChequeLayout\<Relations“.
16. Laiendage puus valik „chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents“.
17. Valige puus „chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()“.
18. Klõpsake valikut Seo.
19. Klõpsake nuppu Salvesta.
20. Sulgege leht.
21. Sulgege leht.
22. Sulgege leht.
23. Sulgege leht.

## <a name="run-format-using-the-adjusted-model-mapping"></a>Vormingu käivitamine kohandatud mudelivastendusega
1. Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate välja Pangakonto filtreerida väärtuse USMF OPER alusel.
3. Klõpsake tegumiribal valikut Seadistus.
4. Klõpsake nuppu Kontrolli.
5. Klõpsake valikut Prindi test.
6. Klõpsake nuppu OK.
    * Vaadake loodud väljund üle. Dokumendihalduse manusest pärit pilt on esitatud volitatud isiku allkirjana.  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a>MS Wordi dokumendi kasutamine imporditud vormingus mallina
1. Sulgege leht.
2. Sulgege leht.
3. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
4. Laiendage puus valik Tšekkide mudel.
5. Valige puus „Model for cheques\Cheques printing format“.
6. Klõpsake valikut Kujundaja.
7. Klõpsake suvandit Manused.
8. Klõpsake Kustuta.
9. Klõpsake nuppu Jah.
10. Klõpsake valikut Uus.
11. Klõpsake suvandit Fail.
    * Klõpsake nuppu Sirvi ja valige eelnevalt allalaaditud fail „Cheque template Word.docx“.  
12. Sulgege leht.
13. Sisestage või valige väärtus väljal Mall.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.
16. Klõpsake nuppu Redigeeri.
17. Tehke väljal Käivita mustand valik Jah.
18. Sulgege leht.
19. Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.
20. Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega USMF OPER.
21. Klõpsake nuppu Kontrolli.
22. Klõpsake valikut Prindi test.
23. Klõpsake nuppu OK.
    * Vaadake loodud väljund üle. Väljund on loodud manuspiltidega Wordi dokumendina, kus on ettevõtte logo, volitatud isiku allkiri ning vesimärgi jaoks valitud tekst.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
