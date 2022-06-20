---
title: Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil
description: Selle artikli sammud selgitavad, kuidas regulatiivse konfiguratsiooni teenuse kasutaja saab uue elektroonilise aruandlusmudeli vastenduse metaandmeid kasutades kujundada.
author: NickSelin
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 330683da986a551a9694833655122768d30499b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906764"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil

[!include [banner](../../includes/banner.md)]

Järgmised etapid selgitavad, kuidas süsteemi administraatori või elektroonilise aruandluse arendaja rolliga lahenduse Regulatory Configuration Service (RCS) kasutaja saab kavandada uue elektroonilise aruandluse (ER) mudelivastenduse kasutades Finance and Operationsi metaandmeid. Rakenduse metaandmete saab online-juurdepääsu RCS-ga ühendatud rakenduse abil. Väliskaubanduse kannetele juurdepääsuks konfigureeritakse elektroonilise aruandluse mudeli vastenduse näidis. Nende sammude lõpuleviimiseks peate RCS-is esmalt täitma artikli sammud, [looma konfiguratsiooni pakkujad ja märkima need aktiivseks](er-configuration-provider-mark-it-active-2016-11.md). Kui te pole artikli samme täitnud, [pääsete ER-konfiguratsiooni](access-application-metadata-er-configuration.md) abil rakenduse metaandmete juurde, [laadige](https://download.microsoft.com/download/0/4/e/04e13839-e423-442b-a6c2-dd35b1045c2d/Dynamics%20365%20for%20Finance%20and%20Operations%208.1%20Electronic%20reporting%20task%20guides.zip) alla elektroonilise aruandluse näited ja salvestage järgmised ER-konfiguratsioonid: väliskaubanduse metaandmed.xml; Väliskaubanduse mudel.xml; Väliskaubanduse vastendus.xml ja viige seejärel protseduuri sammud lõpule.

## <a name="prerequisites"></a>Eeltingimused
1. Avage **Kõik tööruumid** > **Elektrooniline aruandlus**. 
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised. 

## <a name="get-required-er-configurations"></a>Vajalike elektroonilise aruandluse konfiguratsioonide hankimine
1. Klõpsake valikut **Aruandluse konfiguratsioonid**. 
2. Kui viisite need etapid juba protseduuris [Juurdepääs rakenduse metaandmetele ER-i konfiguratsiooni abil](access-application-metadata-er-configuration.md) lõpule, on teil juba kõik vajalikud ER-i konfiguratsioonid (väliskaubanduse metaandmed, mudel ja kaardistamise konfiguratsioonid) praeguses RCS-i eksemplaris olemas. Võite kõik selle alamülesande ülejäänud etapid vahele jätta. 
3. Klõpsake valikut **Vahetus**. 
4. Klõpsake valikut **Laadi XML-failist**. 
5. Klõpsake **Sirvi** ja valige fail **Väliskaubanduse metaandmed.xml**. 
6. Klõpsake valikut **OK**. 
7. Klõpsake valikut **Vahetus**. 
8. Klõpsake valikut **Laadi XML-failist**. 
9. Klõpsake **Sirvi** ja valige fail **Väliskaubanduse mudel.xml**. 
10. Klõpsake valikut **OK**. 
11. Klõpsake valikut **Vahetus**. 
12. Klõpsake valikut **Laadi XML-failist**. 
13. Klõpsake **Sirvi** ja valige fail **Väliskaubanduse vastendamine.xml**. 
14. Klõpsake valikut **OK**. 

## <a name="register-a-connected-application"></a>Ühendatud rakenduse registreerimine
1. Sulgege leht. 
2. Sulgege leht. 
3. Avage **Kõik tööruumid** > **Elektrooniline aruandlus**. 
4. Klõpsake **Ühendatud rakendused**. 
5. Veenduge, et konfigureeritud rakendus on Azure'i põhine ja et see on praegusele RCS-i kasutajatele juurdepääsetav. Samuti on vajalik, et praegusel RCS-i kasutajal on juurdepääs valitud rakendusele ja ta on registreeritud selle rakenduse kasutajaks, kellel on roll, mis annab talle õigused rakenduse metaandmetele juurdepääsuks. 
6. Klõpsake valikut **Uus**. 
7. Trükkige "MyConnectedApp" väljale **Nimi**. 
8. Trükkige väljale **Rakendus** suvand "https:// mycompany.operations.dynamics.com". 
9. Trükkige väljale **Rentnik** suvand „mycompany.onmicrosoft.com”. 
10. Klõpsake valikut **Salvesta**. 
11. Kui kontrollite konfigureeritud rakenduse ühendust, valige lehel **Ühenda kaugrakendusega** link **Klõpsake siin valitud kaugrakendusega ühendamiseks**. 
12. Klõpsake nupul **Kontrolli ühendust**. 
13. Klõpsake valikut **Sule**. 
14. Pärast edukat ühenduse kontrollimist uuendatakse praeguses ruudustikus konfigureeritud rakenduse versioon ja rentniku andmed. 

## <a name="review-existing-model-mapping-configuration"></a>Olemasoleva mudelivastenduse üle vaatamine
1. Sulgege leht. 
2. Klõpsake valikut **Aruandluse konfiguratsioonid**. 
3. Laiendage puul valikut **Väliskaubanduse mudel**. 
4. Valige puul väärtus **Väliskaubanduse mudel\Väliskaubanduse vastendamine**. 
5. Laiendage jaotist **Eeltingimused**. 

    > [!NOTE]
    > Praegu viitab see vastendamine metaandmete konfiguratsioonile. Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal. 

6. Klõpsake valikut **Kujundaja**. 
7. Klõpsake valikut **Kujundaja**. 
8. Valige puul väärtus **Dynamics 365 for Operations\Tabeli kirjed**. 
9. Klõpsake suvandil **Juure lisamine**. 
10. Sisestage või valige väärtus väljalt **Tabel**. 

    > [!NOTE]
    > Praegu viitab see vastendamine metaandmete konfiguratsioonile. Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal. 

11. Klõpsake **Tühista**. 
12. Sulgege leht. 
13. Sulgege leht. 

## <a name="assign-connected-application-to-model-mapping"></a>Määrake ühendatud rakendus mudelivastendusele 
1. Klõpsake valikut **Redigeeri**. 
2. Valige rakendus **MyConnectedApp**. 

    > [!NOTE]
    > Praegu viitab see vastendamine valitud ühendatud rakenduse metaandmetele. Kui sama vastendamine viitab metaandmete konfiguratsioonile ja ühendatud rakendusele samaaegselt, kasutatakse ühendatud rakenduse metaandmeid. 

3. Klõpsake valikut **Kujundaja**. 
4. Klõpsake valikut **Kujundaja**. 
5. Valige puul väärtus **Dynamics 365 for Operations\Tabeli kirjed**. 
6. Klõpsake suvandil **Juure lisamine**. 
7. Sisestage või valige väärtus väljalt **Tabel**. 

    > [!NOTE]
    > Praegu pakuti rohkem kui kahte rakenduse tabelit, sest see vastendamine kasutab kõiki sellele määratud ühendatud rakenduse metaandmeid. 

8. Klõpsake **Tühista**. 
9. Klõpsake valikut **Kinnita**. 

    > [!NOTE]
    > Oleme andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on kirjeldatud kasutades sellele vastendusele määratud ühendatud rakenduse metaandmete üksikasju. 

10. Sulgege leht. 
11. Sulgege leht. 

Kui peate hindama seda mudeli vastendust, kasutades rakenduse teise versiooni metaandmeid, registreerige teine ühendatud rakendus, määrake see mudeli vastendamiseks ja kinnitage see uute metaandmetega.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
