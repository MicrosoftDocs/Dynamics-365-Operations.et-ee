---
title: (ER) Konfiguratsioonide importimine RCS-ist
description: See artikkel annab teavet selle kohta, kuidas kasutaja saab ER-i konfiguratsiooni uut versiooni RCS-st importida.
author: NickSelin
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5317b1f7c8c0af6cd5c839e065c590c4474c84de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850139"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Konfiguratsioonide importimine RCS-ist

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Regulatory Configuration Services (RCS). Selles näites valite elektroonilise aruandluse konfiguratsiooni versiooni, mis on konfigureeritud RCS-i eksemplaris, ja impordite selle praegusesse eksemplari näidisettevõtte Litware, Inc. jaoks. Neid etappe saab läbida igas ettevõttes, kuna elektroonilise aruandluse konfiguratsioonid on ettevõtete ühiskasutuses. Nende sammude lõpuleviimiseks peate esmalt täitma artikli sammud, [looma konfiguratsiooni pakkujad ja märkima need aktiivseks](er-configuration-provider-mark-it-active-2016-11.md). Nende etappide läbimiseks peab teil olema ka juurdepääs RCS-i eksemplarile, mis sisaldab vähemalt üht elektroonilise aruandluse konfiguratsiooni olekuga **Lõpetatud** või **Ühine**.

1. Avage **Organisatsiooni haldamine** > **Tööruumid** > **Elektrooniline aruandlus**. 
2. Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, viige artikli sammud lõpule, [looge konfiguratsiooni pakkujad ja märkige need aktiivseks](er-configuration-provider-mark-it-active-2016-11.md). 
3. Kui teie ettevõtte jaoks pole RCS-i keskkonda eraldatud, valige väline link **Regulatory services – konfigureerimine** ja järgige juhiseid RCS-i keskkonna eraldamiseks. 
4. Valige **Elektroonilise aruandluse parameetrid**. 
5. Valige vahekaart **RCS**. 
6. Kui RCS-i keskkond on juba teie ettevõtte jaoks eraldatud, kasutage sellele ligipääsemiseks lehe URL-i. 
7. Sulgege leht. 

## <a name="register-a-new-er-repository"></a>Registreerige uus elektroonilise aruandluse hoidla. 
1. Märkige loendis valitud rida. 
2. Valige pakkuja Litware, Inc. 
3. Valige Hoidlad. 
4. Klõpsake valikut Lisa rippdialoogi avamiseks. 
5. Sisestage väljale Konfiguratsioonihoidla tüüp valik RCS. 
6. Valige käsk Loo hoidla. 
7. Valige või sisestage väärtus väljal RCS keskkonna kuvatav nimi. 
8. Valige soovitud RCS-i eksemplar. Teil võib neid olla mitu. 
9. Valige nupp OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>Elektroonilise aruandluse konfiguratsioonide importimine RCS-põhisest hoidlast
1. Valige **Kuva filtrid**. 
2. Sisestage filtri tehtemärgi **algab väärtusega** abil filtri väärtus **Nimi**. 
3. Kui avate valitud hoidla, valige lehel **Loo ühendus teenusega Regulatory Configuration Services** link **Valige siin teenusega Regulatory Configuration Services ühenduse loomiseks**. 
4. Valige **Avamine**. 
5. Valige suvand **Sule**. 
6. Valige elektroonilise aruandluse konfiguratsiooni sobiv versioon ja valige nupp **Impordi**, et viia see praegusesse eksemplari.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]