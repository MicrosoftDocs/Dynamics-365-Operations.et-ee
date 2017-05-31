---
title: "Spikrisüsteemi ühendamine"
description: "Selles teemas kirjeldatakse Microsoft Dynamics 365 for Operationsi spirkisüsteemi komponente ning antakse ülevaade nende ühendamisest ja kokkuvõte kohandatud spikri loomisest."
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 86c7cb3961ba5170c32979e77aaa5f506ffac8a1
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="connect-the-help-system"></a>Spikrisüsteemi ühendamine

[!include[banner](../includes/banner.md)]


Selles teemas kirjeldatakse Microsoft Dynamics 365 for Operationsi spikrisüsteemi komponente. Antakse ülevaade nende komponentide ühendamisest ning kokkuvõte kohandatud spikri loomisest. 

<a name="help-architecture"></a>Spikri arhitektuur
-----------------

Järgmisel joonisel on näidatud Microsoft Dynamics 365 for Operationsi spikrisüsteemi osad. Toote sisespikri süsteem toob artikleid Dynamics 365 for Operationsi saidilt https://docs.microsoft.com ja tegevusejuhistest, mis on salvestatud teenuse Microsoft Dynamics Lifecycle Services (LCS) äriprotsesside modelleerijasse. 
**Märkus** Joonisel tärniga (\*) märgitud funktsioonid on meil plaanis, kuid pole veel saadaval. [![Spikri arhitektuur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Spikrisüsteemi ühendamine
Lehel **Süsteemiparameetrid** saavad süsteemiadministraatorid spikrisüsteemi osad juurutamiseks ühendada. [![Süsteemi parameetrite vorm koos spikri sätetega](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Järgige lehel **Süsteemi parameetrid** järgmisi etappe.

> [!IMPORTANT]
> Vahekaardi **Spikker** esmakordsel avamisel peate looma ühenduse elutsükli teenustega. Klõpsake kindlasti vormi keskel olevat linki, oodake, kuni ühendus on loodud, sulgege dialoogiboks ja seejärel klõpsake lehe **Süsteemi parameetrid** avamiseks **OK**.[![LCS-iga ühenduse loomine](./media/connect-to-lcs-crop-1024x365.png "Connect to LCS")](./media/connect-to-lcs-crop.png)

1.  Valige elutsükli teenuste projekt, millega ühendus luua.
2.  Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.
3.  Valige BPM-i teekide kuvamise järjekord. See määrab teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.

Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja klõpsata vahekaarti **Tegevuse juhised**. Näete nüüd tegevusejuhiseid, mis kohalduvad lehele, millel parajasti Dynamics 365 for Operationsis olete. Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.

### <a name="showing-translated-task-guides"></a>Tõlgitud tegevusjuhiste kuvamine

Tõlgitud tegevusjuhised edastati esmakordselt 2016. aasta mai APQC ühendatud teegis ja teegis Alustamine. Dynamics 365 for Operationsis lokaliseeritud tegevusjuhise vaatamiseks veenduge, et teil oleks ühendus mai teegiga. Keelt, milles tegevusjuhis kuvatakse, juhitakse iga kasutaja puhul keelesätetega jaotises **Suvandid** &gt; **Eelistused**. 

> [!NOTE]
> Kuigi paljud tegevusjuhised on tõlgitud, ei kuva Dynamics 365 for Operationsi klient praegu tõlgitud tegevusjuhiste nimesid. Samuti on praegu 2016. aasta mai teegis tõlkena saadaval ainult veebruaris välja antud tegevusjuhised. Anname välja värskendatud teegi täiendavate tõlgetega.
> -   Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.
> -   Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).

## <a name="creating-custom-help"></a>Kohandatud spikri loomine
Saate luua oma Dynamics 365 for Operationsi eksemplarile kohandatud spikri, luues tegevuste salvestised, mis kajastavad teie eksemplari, ja salvestades need LCS-i äriprotsesside teeki. Partneritele: kui teete olemasoleva teegi ettevõtte teegiks ja lisate selle lahendusse, on see teie klientidele kättesaadav. Võite teha koopia ka APQC teegist Unified global library ja avada siis oma eksemplari, avada selle tegevuste salvestised, muuta neid ja salvestada salvestised oma muudatustega. Lisateavet leiate teemast [Kuidas luua tegevuste salvestisi koolitusel dokumentatsioonina kasutamiseks](../user-interface/task-recorder.md).

<a name="see-also"></a>Vt ka
--------

[Spikri ülevaade](help-overview.md)

[Tegevuse salvestaja ülevaade](../user-interface/task-recorder.md)

[Kuidas luua tegevuse salvestist dokumentide või koolitusena kasutamiseks](../user-interface/task-recorder-training-docs.md)





