---
title: (ER) Konfiguratsioonide importimine RCS-ist
description: Selles teemas kirjeldatakse, kuidas saab kasutaja importida elektroonilise aruandluse konfiguratsiooni uut versiooni RCS-ist.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
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
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55d548a97a2f93bffeb5aa4b0ce6b0c4ca5f8819
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769828"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfiguratsioonide importimine RCS-ist

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Regulatory Configuration Services (RCS). Selles näites valite elektroonilise aruandluse konfiguratsiooni versiooni, mis on konfigureeritud RCS-i eksemplaris, ja impordite selle praegusesse eksemplari näidisettevõtte Litware, Inc. jaoks. Neid etappe saab läbida igas ettevõttes, kuna elektroonilise aruandluse konfiguratsioonid on ettevõtete ühiskasutuses. Etappide lõpuleviimiseks, peate esmalt läbima etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md). Nende etappide läbimiseks peab teil olema ka juurdepääs RCS-i eksemplarile, mis sisaldab vähemalt üht elektroonilise aruandluse konfiguratsiooni olekuga **Lõpetatud** või **Ühine**.

1. Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**. 
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised. 
3. Kui teie ettevõtte jaoks pole RCS-i keskkonda eraldatud, klõpsake välist linki **Regulatory services – konfigureerimine** ja järgige juhiseid RCS-i keskkonna eraldamiseks. 
4. Klõpsake valikut **Elektroonilise aruandluse parameetrid**. 
5. Klõpsake vahekaarti **RCS**. 
6. Kui RCS-i keskkond on juba teie ettevõtte jaoks eraldatud, kasutage sellele ligipääsemiseks lehe URL-i. 
7. Sulgege leht. 

## <a name="register-a-new-er-repository"></a>Registreerige uus elektroonilise aruandluse hoidla. 
1. Märkige loendis valitud rida. 
2. Valige pakkuja Litware, Inc. 
3. Klõpsake valikut Hoidlad. 
4. Klõpsake valikut Lisa rippdialoogi avamiseks. 
5. Sisestage väljale Konfiguratsioonihoidla tüüp valik RCS. 
6. Klõpsake käsku Loo hoidla. 
7. Valige või sisestage väärtus väljal RCS keskkonna kuvatav nimi. 
8. Valige soovitud RCS-i eksemplar. Pange tähele, et neid võib olla mitu. 
9. Klõpsake nuppu OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Elektroonilise aruandluse konfiguratsioonide importimine RCS-põhisest hoidlast
1. Klõpsake nuppu **Näita filtreid**. 
2. Sisestage filtri tehtemärgi **algab väärtusega** abil filtri väärtus **Nimi**. 
3. Kui avate valitud hoidla, klõpsake lehel **Loo ühendus teenusega Regulatory Configuration Services** linki **Klõpsake siin teenusega Regulatory Configuration Services ühenduse loomiseks**. 
4. Klõpsake nuppu **Ava**. 
5. Klõpsake valikut **Sule**. 
6. Valige elektroonilise aruandluse konfiguratsiooni sobiv versioon ja klõpsake nuppu **Impordi**, et viia see praegusesse eksemplari.

