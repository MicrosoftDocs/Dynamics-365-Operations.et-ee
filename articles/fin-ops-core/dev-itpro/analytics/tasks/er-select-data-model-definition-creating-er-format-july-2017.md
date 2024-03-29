---
title: Vormingute loomisel andmemudelite määratluste valimine
description: Selle protseduuri toimingute lõpuleviimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“.
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65b3a74f98282f01940c5d17f8aa893d174883da
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290120"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Vormingute loomisel andmemudelite määratluste valimine

[!include [banner](../../includes/banner.md)]

Selle protseduuri toimingute lõpuleviimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“. 

Selle protseduuriga demonstreeritakse, kuidas saab käsitleda mudeli juurkaupa andmemudeli definitsioonina ER-i vormingukonfiguratsioonis, mis on kujundatud elektrooniliste dokumentide loomiseks. Selles näites lisate uue vormingukonfiguratsiooni näidisettevõttele Litware, Inc. 

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia ükskõik, millise andmekomplekti abil.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.  
2. Klõpsake valikut Aruandluse konfiguratsioonid.

## <a name="add-a-new-er-data-model-configuration"></a>Uue elektroonilise aruandluse andmemudeli konfiguratsiooni lisamine
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
    * Lisame uue elektroonilise aruandluse konfiguratsiooni, mis sisaldab andmemudeleid, mida kasutatakse andmeallikatena elektroonilise aruandluse genereerimiseks.  
2. Sisestage nimeväljale tekst „Payment model (fictitious)".
    * Maksemudel (fiktiivne)  
3. Klõpsake Loo konfiguratsioon.
4. Klõpsake valikut Kujundaja.
    * Avage selle konfiguratsiooni andmemudeli struktuuri määramiseks elektroonilise aruandluse koostur.  
    * Oletame, et me loome andmemudeli maksete äridomeeni jaoks, et toetada kahte makseviisi – kreeditülekannet ja otsekorraldust.  
5. Rippdialoogi avamiseks klõpsake valikut Uus.
6. Sisestage nimeväljale tekst „Payments – credit transfer”.
    * Maksed – kreeditiülekanne  
7. Klõpsake vahekaarti Lisa.
8. Rippdialoogi avamiseks klõpsake valikut Uus.
9. Väljale Uus sõlm kui sisestage „Mudeli juur”.
10. Sisestage nimeväljale tekst „Payments – direct debit'.".
    * Maksed – otsekorraldus  
11. Klõpsake vahekaarti Lisa.
12. Klõpsake nuppu Salvesta.
13. Sulgege leht.
14. Klõpsake valikut Muuda olekut.
    * Uue mudeli kättesaadavaks tegemiseks uue mudeli vastendustes ja vormingute viige lõpule mudeli mustandiversioon.  
15. Klõpsake valikut Valmis.
16. Klõpsake nuppu OK.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Hakake sisestama uut elektroonilise aruandluse (ER) konfiguratsiooni
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
2. Sisestage väljale Uus tekst „Format based on data model Payment model (fictitious)".
3. Sisestage või valige väärtus väljal Andmemudeli definitsioon.
    * Pange tähele, et kõik valitud andmemudeli juurkaubad on praegu saadaval andmemudeli definitsioonina valimiseks. Saate jätkata oma vormingu loomist, kui kasutate selleks andmemudeli nõutavaid juurkaupu. Valitud juurkauba puuduv mudelivastendus ei takista teil jätkamast.  
4. Sulgege leht.

## <a name="add-a-new-er-model-mapping-configuration"></a>Uue elektroonilise aruandluse mudelivastenduse konfiguratsiooni lisamine
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
2. Sisestage väljale Uus suvand „Model Mapping based on data model Payment model (fictitious)".
3. Sisestage nimeväljale tekst „Payment model mappings (fictitious)".
    * Maksemudeli vastendused (fiktiivne)  
4. Sisestage või valige väärtus väljal Andmemudeli definitsioon.
5. Klõpsake Loo konfiguratsioon.

## <a name="design-er-model-mappings"></a>Elektroonilise aruandluse (ER) mudelivastenduste loomine
1. Klõpsake valikut Kujundaja.
    * Nõutava juurkauba mudeli vastenduste määramiseks kasutage elektroonilise aruandluse koosturit.  
2. Klõpsake valikut Kujundaja.
    * Saate simuleerida mudeli juurkauba valitud mudelivastenduse sätte.  
3. Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.
4. Klõpsake suvandit Juure lisamine.
5. Sisestage nimeväljale „Ledger”.
6. Sisestage väljale Tabel suvand LedgerJournalTrans.
    * LedgerJournalTrans  
7. Klõpsake nuppu OK.
8. Klõpsake nuppu Salvesta.
9. Sulgege leht.
10. Sulgege leht.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Hakake sisestama veel ühte uut elektroonilise aruandluse (ER) konfiguratsiooni
1. Tehke puul valik „'Payment model (fictitious)".
2. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
3. Sisestage väljale Uus tekst „Format based on data model Payment model (fictitious)".
4. Sisestage või valige väärtus väljal Andmemudeli definitsioon.
    * Pange tähele, et rakenduse andmeallikasse vastendamiseks on nüüd saadaval ainult üks juurkaup. Kui kasutusele on võetud vähemalt üks mudelivastendus, saab elektroonilise aruandluse vormingusse lisada ainult need mudeli juurkaubad, mis on vastendatud rakenduse andmeallikatesse.   
5. Sulgege leht.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
