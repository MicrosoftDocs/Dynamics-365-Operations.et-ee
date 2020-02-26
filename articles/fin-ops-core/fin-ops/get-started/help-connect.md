---
title: Spikrisüsteemi ühendamine
description: Selles teemas kirjeldatakse rakenduse Finance and Operations spikrisüsteemi komponente, antakse ülevaade nende ühendamisest ja tehakse kokkuvõte kohandatud spikri loomisest.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4427388d75c1aef40a978ce35c831d5b714f2562
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006168"
---
# <a name="connect-the-help-system"></a>Spikrisüsteemi ühendamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse rakenduse Finance and Operations spikrisüsteemi komponente, nt Dynamics 365 Finance, Supply Chain Management, Commerce ja Human Resources. Antakse ülevaade nende komponentide ühendamisest ning kokkuvõte kohandatud spikri loomisest.

## <a name="help-architecture"></a>Spikri arhitektuur

Järgmisel joonisel on näidatud spikrisüsteemi osad. Toote sisespikri süsteem toob artikleid saidilt https://docs.microsoft.com ja tegevusejuhistest, mis on salvestatud teenuse Business Process Modeler Lifecycle Services (LCS) äriprotsesside modelleerijasse.

> [!NOTE]
> Joonisel tärniga (\*) märgitud funktsioonid on meil plaanis, kuid pole veel saadaval.

[![Spikri arhitektuur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Spikrisüsteemi ühendamine

> [!NOTE]
> Vahekaart **Tegevusjuhised** ei ole praegu rakendustes Dynamics 365 Human Resources ega Commerce saadaval. Tegeleme praegu selle funktsiooni lubamisega mõnes tulevases väljaandes. Rakenduse Human Resources alustuskogemuse tegevusjuhised jäävad põhifunktsioonide pakkumiseks saadavaks. Nii rakenduse Human Resources kui ka Commerce protseduurispikker on saadaval ka lehel docs.microsoft.com.

Lehel **Süsteemiparameetrid** saavad süsteemiadministraatorid spikrisüsteemi osad juurutamiseks ühendada.

[![Süsteemi parameetrite vorm koos spikrisätetega](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Tehke lehel **Süsteemi parameetrid** järgmist.

> [!IMPORTANT]
> Vahekaardi **Spikker** esmakordsel avamisel peate looma ühenduse elutsükli teenustega. Klõpsake kindlasti vormi keskel olevat linki, oodake, kuni ühendus on loodud, sulgege dialoogiboks ja seejärel klõpsake **OK**, et avada **Parameetrite vormid**.
>
> [![Ühenda LCS-iga](./media/connect-to-lcs-crop-1024x365.png "Ühenda LCS-iga")](./media/connect-to-lcs-crop.png)

1. Valige elutsükli teenuste projekt, millega ühendus luua.
2. Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.
3. Valige BPM-i teekide kuvamise järjekord. See määrab teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.

Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja klõpsata vahekaarti **Tegevusjuhised**. Näete nüüd tegevusjuhiseid, mis rakenduvad lehele, millel parajasti rakenduses Finance and Operations olete. Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.

### <a name="showing-translated-task-guides"></a>Tõlgitud tegevusjuhiste kuvamine

Tõlgitud tegevusjuhised edastati esmakordselt 2016. aasta mai APQC ühendatud teegis ja teegis Alustamine. Rakenduse Finance and Operations lokaliseeritud tegevusjuhise vaatamiseks veenduge, et teil oleks ühendus mai teegiga. Keelt, milles tegevusjuhis kuvatakse, juhitakse iga kasutaja puhul keelesätetega jaotises **Suvandid** &gt; **Eelistused**.

> [!NOTE]
> Kuigi paljud tegevusjuhised on tõlgitud, ei kuva klient praegu tõlgitud tegevusjuhiste nimesid. Samuti on praegu 2016. aasta mai teegis tõlkena saadaval ainult veebruaris välja antud tegevusjuhised. Anname välja värskendatud teegi täiendavate tõlgetega.
>
> - Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.
> - Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).

## <a name="creating-custom-help"></a>Kohandatud spikri loomine

Ülesande juhiseid saate kasutada kohandatud spikri loomiseks või veebisaidi ühendamiseks spikripaaniga.

### <a name="create-custom-help-with-task-guides"></a>Kohandatud spikri loomine ülesande juhistega

Saate rakendustele Finance, Supply Chain Management ja Commerce luua kohandatud spikri, luues teie eksemplari kajastavad tegevuste salvestised ja salvestades need LCS-i äriprotsesside teeki. Rakenduse Human Resources jaoks ei saa te kohandatud tegevusjuhiseid luua.

Partneritele: kui teete olemasoleva teegi ettevõtte teegiks ja lisate selle lahendusse, on see teie klientidele kättesaadav. Võite teha koopia ka APQC teegist Unified global library ja avada siis oma eksemplari, avada selle tegevuste salvestised, muuta neid ja salvestada salvestised oma muudatustega. Lisateavet vt [Tegevuse salvestaja ressursid](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Kohandatud saidi ühendamine

Microsoft pakub tehnilist ülevaadet ja näidiskoodi, mis kirjeldavad kohandatud spikrisaidi loomist ja ühendamist spikripaaniga. Lisateabe saamiseks vt:

- [Kohandatud spikri loomine Finance and Operationsi rakendustele (tehniline ülevaade)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Kohandatud spikker – GitHubi hoidla](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Lisaressursid

[Spikrisüsteem](help-overview.md)

[Tegevuse salvestaja ressursid](../../dev-itpro/user-interface/task-recorder.md)

[Dokumentide või koolituse loomine tegevuse salvestaja abil](../../dev-itpro/user-interface/task-recorder-training-docs.md)
