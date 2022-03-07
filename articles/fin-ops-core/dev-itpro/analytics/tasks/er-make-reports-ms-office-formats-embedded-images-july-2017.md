---
title: Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega
description: Selles teemas kirjeldatakse, kuidas kujundada konfiguratsioone, mis loovad Exceli ja Wordi vormingus elektroonilisi dokumente, mis sisaldavad manuspilte.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03a514c5b616d761ef3eb6347e67e645b23eaa1794911775835e77cded4500ac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719341"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega

[!include [banner](../../includes/banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“. See toiming kirjeldab Microsoft Excelis või Wordis manuspilte sisaldavate elektrooniliste dokumentide loomiseks elektroonilise aruandluse (ER) konfiguratsioonide kujundamist. Selles protseduuris loote näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. Need toimingud saab lõpule viia USMF-i andmekomplekti abil. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Enne alustamist laadige alla ja talletage kohalikult järgmised failid. 

| Kirjeldus                                          | Faili nimi                   |
|------------------------------------------------------|-----------------------------|
| ER-i andmemudeli konfiguratsioon                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| Elektroonilise aruandluse vormingu konfiguratsioon                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Ettevõtte logo pilt                                   | [Ettevõtte logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Allkirja pilt                                      | [Allkirja pilt.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Alternatiivne allkirjapilt                          | [Allkirja pilt 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word Maksekontrollide printimise mall  | [Tšeki malli Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
