---
title: Elektroonilise aruandluse (ER) mudelivastenduse konfiguratsioonide loomine
description: Selle protseduuriga saate kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23bc3a525be9f65b7e5100114d02f6b79a286fb5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682065"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>Elektroonilise aruandluse (ER) mudelivastenduse konfiguratsioonide loomine

[!include [banner](../../includes/banner.md)]

Selle protseduuriga saate kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks. Selles protseduuris loote konfiguratsiooni näidisettevõttele Litware, Inc. 

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.

Need etapid saab lõpule viia ükskõik millise andmekomplekti abil. Etappide lõpuleviimiseks, peate esmalt läbima protseduuri „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” etapid.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.  
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Klõpsake suvandit Näita filtreid.
4. Sisestage väljale „Nimi” filtriväärtus „Intrastat” ja kasutage filtri tehtemärki „algab järgmisega”.
    * Rakendage see filter, et leida andmemudeli konfiguratsioon „Intrastat”. See mudel on võib-olla juba konfiguratsioonide puus olemas. Kui on, jätke järgmine alamülesanne vahele.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>Microsofti pakutava Intrastati mudeli konfiguratsiooni hankimine
1. Sulgege leht.
2. Sulgege leht.
3. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
4. Otsige loendist ja valige soovitud kirje.
    * Valige Microsofti pakkuja paan.  
5. Klõpsake valikut Hoidlad.
    * Klõpsake Microsofti pakkuja paanil valikut Hoidlad.  
6. Klõpsake suvandit Näita filtreid.
7. Sisestage väljale „Tüübi nimi” filtriväärtus „ressursid” ja kasutage filtri tehtemärki „sisaldab”. 
8. Klõpsake valikut Ava.
9. Tehke puul valik „Intrastati mudel”.
10. Klõpsake Import.
11. Klõpsake nuppu Jah.
    * Importisite ER-i mudeli konfiguratsiooni, mis sisaldab andmemudelit, millega saate uurida, kuidas saab kasutada uut ER-i funktsiooni.  
12. Sulgege leht.
13. Sulgege leht.
14. Klõpsake valikut Aruandluse konfiguratsioonid.

## <a name="add-a-new-model-mapping-configuration"></a>Uue mudelivastenduse konfiguratsiooni lisamine
1. Tehke puul valik „Intrastati mudel”.
2. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
3. Väljale Uus sisestage „Intrastati andmemudelil põhinev mudeli vastendamine”.
4. Sisestage nimeväljale tekst „Intrastati näidise vastendamine”.
    * Intrastati näidise vastendamine  
5. Klõpsake Loo konfiguratsioon.

