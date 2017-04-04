---
title: "Spikrisüsteemi ühendamine"
description: "Selles teemas kirjeldatakse Microsoft Dynamics 365 for Operationsi spirkisüsteemi komponente ning antakse ülevaade nende ühendamisest ja kokkuvõte kohandatud spikri loomisest."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Spikrisüsteemi ühendamine

Teema käsitleb Microsoft Dynamics 365 toimingute abiinfo süsteemi komponendid. See annab ülevaate, kuidas need komponendid ühendada ja kokkuvõte, kuidas luua kohandatud abi. 

<a name="help-architecture"></a>Spikri arhitektuur
-----------------

Järgmisel joonisel on Dynamics 365 toimingute aidata süsteemi osa. -Toote spikrisüsteemist tõmbab artiklite Dynamics 365 toimingute saidi https://docs.microsoft.com, samuti ülesandeks juhendid talletatakse Business protsessi Modeler elutsükli teenused (LCS). 
**Märkus:** funktsioonid, mis on loetletud tabelis tärniga (\*) on planeeritud, kuid ei ole veel saadaval. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Abiinfo süsteemi ühendamine
Kasutades on **süsteemi parameetrid** leht, süsteemiadministraatorid ühendust metallitükid Abiinfo süsteemi rakendamist. [![Süsteemi parameetrid vormi abi seaded](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) kohta on **süsteemi parameetrid** lehekülg, järgige neid samme:

1.  **Tähtis:** esimene kord, kui avate selle **aidata** jaotises ühendamist elutsükli teenuseid. Kindlasti klõpsake linki keset vormi, oodake ühendust, sulgege see ja klõpsake **OK** saada selle **süsteemi parameetrid** lehel. [![Ühendada LCS](./media/connect-to-lcs-crop-1024x365.png "ühendada LCS")](./media/connect-to-lcs-crop.png)
2.  Valige elutsükli teenuste projekt, millega ühendus luua.
3.  Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.
4.  Valige BPM-i teekide kuvamise järjekord. See määrab teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.

Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja klõpsata vahekaarti **Tegevuse juhised**. Näete nüüd tegevusejuhiseid, mis kohalduvad lehele, millel parajasti Dynamics 365 for Operationsis olete. Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.

### <a name="showing-translated-task-guides"></a>Tõlgitud tegevusjuhiste kuvamine

Tõlgitud ülesandeks juhendid esimesena lähetati mais 2016 APQC ühendatud raamatukogu ja raamatukogu alustamine. Dynamics 365 for Operationsis lokaliseeritud tegevusjuhise vaatamiseks veenduge, et teil oleks ühendus mai teegiga. Keel, mis kuvatakse ülesande juhend reguleerib iga kasutaja keele seaded all **Valikud**&gt;**eelistused**. **Märkus:** kuigi paljud tegevusjuhised on tõlgitud, ei kuva Dynamics 365 for Operationsi klient praegu tõlgitud tegevusjuhiste nimesid. Samuti puuduvad ainult ülesandeks juhendid, mis anti välja veebruaris 2016 mai Raamatukogu tõlge. Anname välja värskendatud teegi täiendavate tõlgetega.

-   Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.
-   Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).

## <a name="creating-custom-help"></a>Kohandatud spikri loomine
Saate luua oma Dynamics 365 for Operationsi eksemplarile kohandatud spikri, luues tegevuste salvestised, mis kajastavad teie eksemplari, ja salvestades need LCS-i äriprotsesside teeki. Partneritele: kui teete olemasoleva teegi ettevõtte teegiks ja lisate selle lahendusse, on see teie klientidele kättesaadav. Võite teha koopia ka APQC teegist Unified global library ja avada siis oma eksemplari, avada selle tegevuste salvestised, muuta neid ja salvestada salvestised oma muudatustega. Lisateabe saamiseks vaadake [tööülesande salvestamine kasutada või koolituse loomine](../user-interface/task-recorder.md).

<a name="see-also"></a>Vt ka
--------

[Help overview](help-overview.md)

[Ülesanne salvesti ülevaade](../user-interface/task-recorder.md)

[Kuidas luua tegevuse salvestist dokumentide või koolitusena kasutamiseks](../user-interface/task-recorder-training-docs.md)

[Uus koolitus teekide loomise Dynamics 365 piires elutsükli teenuste kasutamise lindistaja ülesanne (External link)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


