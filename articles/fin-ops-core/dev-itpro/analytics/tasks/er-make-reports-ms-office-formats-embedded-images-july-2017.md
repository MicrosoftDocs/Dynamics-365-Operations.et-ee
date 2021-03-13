---
title: Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega
description: Selles teemas kirjeldatakse, kuidas kujundada konfiguratsioone, mis loovad Exceli ja Wordi vormingus elektroonilisi dokumente, mis sisaldavad manuspilte.
author: NickSelin
manager: AnnBe
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b60ed6b07851c44ceb4b8f313bc65f04b802e646
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093666"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega

[!include [banner](../../includes/banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“. See toiming kirjeldab Microsoft Excelis või Wordis manuspilte sisaldavate elektrooniliste dokumentide loomiseks elektroonilise aruandluse (ER) konfiguratsioonide kujundamist. Selles protseduuris loote näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. Need toimingud saab lõpule viia USMF-i andmekomplekti abil. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Enne alustamist laadige alla ja salvestage spikriteemas loetletud failid [Piltide ja vormide manustamine ER-i abil loodavatesse dokumentidesse](../electronic-reporting-embed-images-shapes.md). Failid on järgmised: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.

## <a name="verify-prerequisites"></a>Eeltingimuste kontrollimine  
 1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.  
 2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.   
 3. Klõpsake valikut Aruandluse konfiguratsioonid.  
 
## <a name="add-a-new-er-model-configuration"></a>Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine  
 1. Uue mudeli loomise asemel saate laadida ER-i mudeli konfiguratsioonifaili (Model for cheques.xml), mille varem salvestasite. Fail sisaldab maksetšekkide näidisandmemudelit ning andmemudeli ja rakenduse Dynamics 365 for Operations andmekomponentide vastendust.   
 2. Klõpsake versioonide kiirkaardil nuppu Vahetus.   
 3. Klõpsake nuppu Laadi XML-failist.  
 4. Klõpsake käsku Sirvi ja seejärel valige fail Model for cheques.xml.   
 5. Klõpsake nuppu OK.  
 6. Laaditud mudelit kasutatakse Wordis ja Excelis andmeallikana pilte sisaldavate dokumentide loomiseks.  

## <a name="add-a-new-er-format-configuration"></a>Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine  
 1. Uue vormingu loomise asemel saate laadida ER-i vormingu konfiguratsioonifaili (Cheques printing format.xml), mille varem salvestasite. See fail sisaldab eelprinditud vormi abil tšekkide printimise vormingu näidispaigutust ning vormingu ja andmemudeli „Tšekkide mudel” vastendust.   
 2. Klõpsake nuppu Vahetus.  
 3. Klõpsake nuppu Laadi XML-failist.  
 4. Klõpsake valikut Sirvi ja valige tšekkide printimise fail format.xml.   
 5. Klõpsake nuppu OK.  
 6. Laiendage puus valik Tšekkide mudel.  
 7. Valige puus „Model for cheques\Cheques printing format“.  
 8. Laaditud vormingut kasutatakse Wordis ja Excelis pilte sisaldavate dokumentide loomiseks.   

## <a name="configure-er-user-parameters"></a>Elektroonilise aruandluse kasutaja parameetrite konfigureerimine  
 1. Klõpsake tegumiribal valikut Konfiguratsioonid.  
 2. Klõpsake valikut Kasutaja parameetrid.  
 3. Tehke väljal Käivita sätted valik Jah.  
  Lülitage sisse lipp „Käivita mustand”, et käivitada valitud vormingu mustandiversioon, mitte lõpule viidud versioon.  
 4. Klõpsake nuppu OK.  

## <a name="configure-cash--bank-management-parameters"></a>Sularaha- ja pangahalduse parameetrite konfigureerimine  
 1. Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.  
 2. Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega USMF OPER.  
 3. Klõpsake tegumiribal valikut Seadistus.  
 4. Klõpsake nuppu Kontrolli.  
 5. Laiendage jaotist Seadistus.  
 6. Klõpsake nuppu Redigeeri.  
 7. Tehke väljal Ettevõtte logo valik Jah.  
 8. Klõpsake ettevõtte logo.  
 9. Klõpsake käsku Muuda.  
 10. Klõpsake käsku Sirvi ja valige varem allalaaditud fail Company logo.png.   
 11. Klõpsake nuppu Salvesta.  
 12. Sulgege leht.  
 13. Laiendage jaotist Allkiri.  
 14. Valige väljal Esimese allkirja printimine suvand Jah.  
 15. Klõpsake käsku Muuda.  
 16. Klõpsake käsku Sirvi ja valige varem allalaaditud fail Signature image.png.   
 17. Laiendage jaotis Eksemplare.  
 18. Tehke väljal Vesimärk valik.  
 19. Valige väljal Üldine elektrooniline ekspordivorming suvand Jah.  
 20. Saate valida konfiguratsiooni „Tšekkide printimise vorm”.  
 21. Nüüd kasutatakse valitud ER-i vormingut tšekkide printimiseks.  
 22. Klõpsake suvandit Manusta.  
 23. Klõpsake valikut Uus.  
 24. Klõpsake suvandit Fail.  
 25. Klõpsake käsku Sirvi ja valige varem allalaaditud fail Signature image 2.png.   
 26. Sulgege leht.  
 27. Sulgege leht.  
 28. Sulgege leht.  
 29. Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.  
 30. Väljal „Luba eelpäringu loomine passiivsetel pangakontodel:” valige Jah.  
 31. Klõpsake nuppu Salvesta.  
 32. Sulgege leht.  
