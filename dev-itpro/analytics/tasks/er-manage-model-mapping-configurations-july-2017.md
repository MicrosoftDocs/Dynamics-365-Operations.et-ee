--- 
title: Elektroonilise aruandluse (ER) mudelivastenduse konfiguratsioonide haldamine
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad hallata elektroonilise aruandluse (ER) mudelivastendusi eraldi ER-i konfiguratsioonides."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 65db27e59ce5f9234eeb486efeb9bb6e9dad40f7
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) mudelivastenduse konfiguratsioonide haldamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad hallata elektroonilise aruandluse (ER) mudelivastendusi eraldi ER-i konfiguratsioonides. Juhendit järgides loote näidisettevõtte Litware, Inc. jaoks vajalikud ER-i konfiguratsioonid. Juhendis ülesannete lõpetamiseks peab esmalt täitma juhises "ER konfiguratsioonipakkuja loomine" toodud toimingud ja märkida see aktiivseks. 

Kuna ER-i konfiguratsioonid on ettevõtete vahel ühisjagamises, võite läbida juhendi toimingud ükskõik, millise ettevõtte andmekogumiga. Selle tööjuhendi funktsioonid on saadaval, kui olete installinud ühe järgmistest kiirparandustest: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 rakenduse Dynamics AX versioonile 7.0 või https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 rakenduse Dynamics 365 for Operations versioonile.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima tegevuse juhises „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” esitatud toimingud.   

## <a name="add-a-new-er-model-configuration"></a>Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine
1. Klõpsake valikut Aruandluse konfiguratsioonid.
    * Lisage uus elektroonilise aruandluse mudeli konfiguratsioon. Nimi peab konfiguratsioonide puus olema kordumatu.  
2. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
3. Tippige nimeväljale tekst „Sample data model".
    * Näidisandmemudel  
4. Klõpsake Loo konfiguratsioon.
5. Klõpsake valikut Kujundaja.
6. Rippdialoogi avamiseks klõpsake valikut Uus.
7. Tippige Juur väljale Nimi.
    * Juur  
8. Klõpsake vahekaarti Lisa.
9. Rippdialoogi avamiseks klõpsake valikut Uus.
10. Sisestage väljale Nimi suvand Ettevõte.
    * Ettevõte  
11. Klõpsake vahekaarti Lisa.
12. Sisestage väljale Kirjeldus tekst, juriidilise isiku või ettevõtte kirjeldus, millesse kasutaja logis sisse käitusajal. 
    * Juriidiline isiku või ettevõtte kirjeldus kuhu kasutaja logis sisse käitusajal.  
13. Valige "Juure viide".
14. Klõpsake nuppu OK.
15. Klõpsake nuppu Salvesta.
16. Sulgege leht.
17. Klõpsake valikut Muuda olekut.
18. Klõpsake valikut Valmis.
19. Klõpsake nuppu OK.

## <a name="add-a-new-er-model-mapping-configuration"></a>Uue elektroonilise aruandluse mudelivastenduse konfiguratsiooni lisamine
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
2. Sisestage väljale Uus suvand "Andmemudelil Näidisandmemudel põhinev mudelivastendus".
3. Sisestage nimeväljale tekst „Sample mapping".
    * Näidisvastendamine  
4. Klõpsake Loo konfiguratsioon.
5. Laiendage jaotist Eeltingimused.
    * Pange tähele, et juurutuste eeltingimuste grupp on lisatud automaatselt. Grupi sisaldab eeltingimuse komponenti, mis viitab ülataseme andmemudeli konfiguratsioonile ning see on märgitud juurutuseks. See tähendab, et seda näidisvastendusmudeli vastenduskonfiguratsiooni peetakse andmemudeli, näidisandmemudeli, juurutamiseks. Seetõttu sunnib see komponent elektroonilist aruandlust alla laadima mudelivastenduse konfiguratsiooni, näidisvastendust elektroonilise aruandluse hoidlast, kui mudeli konfiguratsioon, näidisandmemudel, on alla laaditud.   
6. Klõpsake valikut Kujundaja.
    * Pange tähele, et loodud mudelivastenduse konfiguratsiooni sisaldab uut tühja vastendamist, millel on loodud konfiguratsiooniga sama nimi. Võtke arvesse, et kui valitud ülataseme mudeli konfiguratsioon sisaldab mudelivastendusi, kopeeritakse need uude mudelivastenduse konfiguratsiooni.   
7. Klõpsake valikut Kujundaja.
8. Valige puul suvand „Dynamics 365 for Operations\tabel“.
9. Klõpsake suvandit Juure lisamine.
10. Sisestage väljale Nimi suvand Ettevõte.
    * Ettevõte  
11. Sisestage väljale Tabel suvand CompanyInfo.
    * CompanyInfo  
12. Klõpsake nuppu OK.
13. Laiendage puul väärtust "Company".
14. Laiendage puul valikut „Company\find()“.
15. Tehke puul valik „Company\find()\Name".
16. Klõpsake valikut Seo.
17. Klõpsake nuppu Salvesta.
18. Sulgege leht.
19. Sulgege leht.
20. Klõpsake tegumiribal valikut Konfiguratsioonid.
21. Klõpsake valikut Kasutaja parameetrid.
22. Tehke väljal Käivita sätted valik Jah.
23. Klõpsake nuppu OK.
24. Klõpsake nuppu Redigeeri.
25. Tehke väljal Käivita mustand valik Jah.

## <a name="add-a-new-er-format-configuration"></a>Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine
1. Tehke puul valik „Sample data model".
2. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
3. Sisestage väljale Uus suvand „Format based on data model Sample data model".
4. Sisestage nimeväljale suvand „Sample format".
    * Näidise vorming  
5. Klõpsake Loo konfiguratsioon.
6. Klõpsake valikut Kujundaja.
7. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
8. Valige puul suvand Tekst\String.
9. Klõpsake nuppu OK.
10. Klõpsake vahekaarti Vastendus.
11. Laiendage puus sõlme „model”.
12. Tehke puul valik „model\Company".
13. Klõpsake valikut Seo.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.
    * Käivitage loodud vormingu mustandiversioon testimise eesmärgil.  
16. Klõpsake nuppu Käivita.
    * Klõpsake Versioonide kiirkaardil nuppu Käivita.  
17. Klõpsake nuppu OK.
    * Vaadake toodangu, mis sisaldab kasutaja, kes töötab sellele vormingu konfiguratsioonile loginud ettevõtte nimi. Pange tähele, et see vormingukonfiguratsioon kasutab loodud mudelivastenduskonfiguratsiooni, kuna see on ainus saadaolev konfiguratsioon, mis sisaldab nõutavaid mudelivastendusi.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Alternatiivse elektroonilise aruandluse mudelivastenduse konfiguratsiooni lisamine
1. Tehke puul valik „Sample data model".
2. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
3. Sisestage väljale Uus suvand "Andmemudelil Näidisandmemudel põhinev mudelivastendus".
4. Sisestage nimeväljale tekst „Sample mapping (alternative)".
    * Näidise vastendamine (alternatiivne)  
5. Klõpsake Loo konfiguratsioon.
6. Klõpsake valikut Kujundaja.
7. Klõpsake valikut Kujundaja.
8. Valige puul suvand „Dynamics 365 for Operations\tabel“.
9. Klõpsake suvandit Juure lisamine.
10. Sisestage väljale Nimi suvand Ettevõte.
    * Ettevõte  
11. Sisestage väljale Tabel suvand CompanyInfo.
    * CompanyInfo  
12. Klõpsake nuppu OK.
13. Klõpsake nuppu Redigeeri.
14. Valige puul suvand String\ÜHENDA.
15. Klõpsake suvandit Funktsiooni lisamine.
16. Laiendage puul väärtust "Company".
17. Laiendage puul valikut „Company\find()“.
18. Tehke puul valik „Company\find()\Name".
19. Klõpsake suvandit Andmeallika lisamine.
20. Sisestage väärtus väljale Valem.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Tehke puul valik „Company\find()\Company(DataArea)".
22. Klõpsake suvandit Andmeallika lisamine.
23. Sisestage väärtus väljale Valem.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Klõpsake nuppu Salvesta.
25. Sulgege leht.
26. Klõpsake nuppu Salvesta.
27. Sulgege leht.
28. Sulgege leht.
29. Tehke väljal Käivita mustand valik Jah.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Olemasoleva elektroonilise aruandluse mudelivastenduse konfiguratsiooni kasutamine
1. Tehke puul valik „Näidisandmemudel\Näidisformaat".
2. Klõpsake nuppu Käivita.
    * Pange tähele, et valitud ER-vormingu konfiguratsiooni mustandiversiooni ei saa käivitada, kuna määratlemata andmemudeli jaoks, mis on valitud käivitatud ER-i vormingu andmeallikana, sisaldab mitut mudelivastenduse konfiguratsiooni.   
    * Seejärel määratlege alternatiivne mudelivastenduskonfiguratsioon sellena, millest mudelivastendusi kasutatakse andmeallikana käivitatud ER-vormingu jaoks.   
3. Tehke puul valik „Näidisandmemudel\Näidisvastendamine (alternatiivne)".
4. Väljal Mudelivastenduse vaikeväärtus valige Jah.
5. Tehke puul valik „Näidisandmemudel\Näidisformaat".
6. Klõpsake nuppu Käivita.
7. Klõpsake nuppu OK.
    * Pange tähele, et mudelivastenduse vaikekonfiguratsiooni kasutab see vormingukonfiguratsioon elektroonilise dokumendi genereerimiseks (loodud väljund sisaldab ettevõtte koodi).  


