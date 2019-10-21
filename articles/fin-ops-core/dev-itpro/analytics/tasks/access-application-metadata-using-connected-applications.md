---
title: Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil
description: Selle teema sammud selgitavad, kuidas Regulatory configuration service (RCS) kasutaja saab kujundada uut elektroonilise aruandluse (ER) mudeli kaardistamise, kasutades metaandmeid Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a476163ba6f66ab60ed8bfea6198d02f13ac5136
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182711"
---
# <a name="access-application-metadata-by-using-connected-applications"></a>Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmised etapid selgitavad, kuidas süsteemi administraatori või elektroonilise aruandluse arendaja rolliga lahenduse Regulatory Configuration Service (RCS) kasutaja saab kavandada uue elektroonilise aruandluse (ER) mudelivastenduse kasutades Finance and Operationsi metaandmeid. Rakenduse metaandmete saab online-juurdepääsu RCS-ga ühendatud rakenduse abil. Väliskaubanduse kannetele juurdepääsuks konfigureeritakse elektroonilise aruandluse mudeli vastenduse näidis. Etappide lõpuleviimiseks, peate RCS-is esmalt läbima etapid teemas [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](er-configuration-provider-mark-it-active-2016-11.md). Kui te ei ole viinude lõpule etappe teemas [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](access-application-metadata-er-configuration.md), avage [Elektroonilise aruandluse näidiste leht](https://go.microsoft.com/fwlink/?linkid=862266), et laadida alla ja salvestada järgmised elektroonilise aruandluse konfiguratsioonid: Väliskaubanduse metaandmed.xml; Väliskaubanduse mudel.xml; Väliskaubanduse vastendamine.xml, ja seejärel viige protseduuri etapid lõpuni.

## <a name="prerequisites"></a>Eeltingimused
1. Avage **Kõik tööruumid** > **Elektrooniline aruandlus**. 
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](er-configuration-provider-mark-it-active-2016-11.md) toodud etapid. 

## <a name="get-required-er-configurations"></a>Vajalike elektroonilise aruandluse konfiguratsioonide hankimine
1. Klõpsake valikut **Aruandluse konfiguratsioonid**. 
2. Kui olete varem selles teemas protseduuri [(RCS) Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](access-application-metadata-er-configuration.md) etapid lõpule viinud, on teil praeguses RCS-i eksemplaris juba kõik vajalikud elektroonilise aruandluse konfiguratsioonid (väliskaubanduse metaandmete, mudeli ja vastenduse konfiguratsioonid). Võite kõik selle alamülesande ülejäänud etapid vahele jätta. 
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
5. Veenduge, et konfigureeritud rakendus on Azura põhine ja et see on praegusele RCS-i kasutajatele juurdepääsetav. Samuti on vajalik, et praegusel RCS-i kasutajal on juurdepääs valitud rakendusele ja ta on registreeritud selle rakenduse kasutajaks, kellel on roll, mis annab talle õigused rakenduse metaandmetele juurdepääsuks. 
6. Klõpsake valikut **Uus**. 
7. Trükkige "MyConnectedApp" väljale **Nimi**. 
8. Trükkige väljale **Rakendus** suvand "https:// mycompany.operations.dynamics.com". 
9. Trükkige väljale **Rentnik** suvand "mycompany.onmicrosoft.com". 
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
