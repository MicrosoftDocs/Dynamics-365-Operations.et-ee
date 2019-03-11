---
title: Spikrisüsteemi ühendamine
description: Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 for Finance and Operations spikrisüsteemi komponente ja antakse ülevaade nende ühendamisest ning kokkuvõte kohandatud spikri loomisest.
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 673b01648127fe1d19fb3c75c4d6812c4f22c761
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "317725"
---
# <a name="connect-the-help-system"></a>Spikrisüsteemi ühendamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 for Finance and Operations spikrisüsteemi komponente. Antakse ülevaade nende komponentide ühendamisest ning kokkuvõte kohandatud spikri loomisest.

## <a name="help-architecture"></a>Spikri arhitektuur

Järgmisel joonisel on näidatud Finance and Operationsi spikrisüsteemi osad. Toote sisespikri süsteem toob artikleid Finance and Operationsi saidilt https://docs.microsoft.com ja tegevusejuhistest, mis on salvestatud teenuse Microsoft Dynamics Lifecycle Services (LCS) äriprotsesside modelleerijasse.

> [!NOTE]
> Joonisel tärniga (\*) märgitud funktsioonid on meil plaanis, kuid pole veel saadaval.

[![Spikri arhitektuur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Spikrisüsteemi ühendamine

> [!NOTE]
> Vahekaart **Tegevusjuhised** ei ole praegu rakendustes Microsoft Dynamics 365 for Talent ega Microsoft Dynamics 365 for Retail saadaval. Tegeleme praegu selle funktsiooni lubamisega mõnes tulevases väljaandes. Tegevusjuhised rakenduse Talent jaotises Alustamine jäävad kättesaadavaks, hõlmates põhifunktsioone. Protseduurispikker on saadaval ka lehel docs.microsoft.com site ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) nii rakenduse Retail kui ka Talent puhul.

Lehel **Süsteemiparameetrid** saavad süsteemiadministraatorid spikrisüsteemi osad juurutamiseks ühendada.

[![Süsteemi parameetrite vorm koos spikrisätetega](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Tehke lehel **Süsteemi parameetrid** järgmist.

> [!IMPORTANT]
> Vahekaardi **Spikker** esmakordsel avamisel peate looma ühenduse elutsükli teenustega. Klõpsake kindlasti vormi keskel olevat linki, oodake, kuni ühendus on loodud, sulgege dialoogiboks ja seejärel klõpsake **OK**, et avada **Parameetrite vormid**.
>
> [![LCS loomiseks](./media/connect-to-lcs-crop-1024x365.png "LCS loomiseks")](./media/connect-to-lcs-crop.png)

1. Valige elutsükli teenuste projekt, millega ühendus luua.
2. Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.

    - Finance and Operationsi puhul valige Microsofti sisu jaoks uusim Finance and Operationsi APQC ühendatud teek.
    - Retaili jaoks anname teegi välja lähitulevikus.
    - Talenti jaoks pole vaja teeki valida – ühendus õige teegiga on teie eest loodud.

3. Valige BPM-i teekide kuvamise järjekord. See määrab teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.

Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja klõpsata vahekaarti **Tegevuse juhised**. Näete nüüd tegevuse juhiseid, mis rakenduvad lehele, millel parajasti Finance and Operationsis olete. Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.

### <a name="showing-translated-task-guides"></a>Tõlgitud tegevusjuhiste kuvamine

Tõlgitud tegevusjuhised edastati esmakordselt 2016. aasta mai APQC ühendatud teegis ja teegis Alustamine. Finance and Operationsis lokaliseeritud tegevusjuhise vaatamiseks veenduge, et teil oleks ühendus mai teegiga. Keelt, milles tegevusjuhis kuvatakse, juhitakse iga kasutaja puhul keelesätetega jaotises **Suvandid** &gt; **Eelistused**.

> [!NOTE]
> Kuigi paljud tegevusjuhised on tõlgitud, ei kuva Finance and Operationsi klient praegu tõlgitud tegevusjuhiste nimesid. Samuti on praegu 2016. aasta mai teegis tõlkena saadaval ainult veebruaris välja antud tegevusjuhised. Anname välja värskendatud teegi täiendavate tõlgetega.
>
> - Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.
> - Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).

## <a name="creating-custom-help"></a>Kohandatud spikri loomine

Ülesande juhiseid saate kasutada kohandatud spikri loomiseks või veebisaidi ühendamiseks spikripaaniga.

### <a name="create-custom-help-with-task-guides"></a>Kohandatud spikri loomine ülesande juhistega

Saate luua oma Finance and Operationsi ja Retaili eksemplarile kohandatud spikri, luues tegevuste salvestised, mis kajastavad teie eksemplari, ja salvestades need LCS-i äriprotsesside teeki. Kohandatud tegevusjuhiseid ei saa luua Talenti puhul.

Partneritele: kui teete olemasoleva teegi ettevõtte teegiks ja lisate selle lahendusse, on see teie klientidele kättesaadav. Võite teha koopia ka APQC teegist Unified global library ja avada siis oma eksemplari, avada selle tegevuste salvestised, muuta neid ja salvestada salvestised oma muudatustega. Lisateavet leiate teemast [Kuidas luua tegevuste salvestisi koolitusel dokumentatsioonina kasutamiseks](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Kohandatud saidi ühendamine

Microsoft pakub tehnilist ülevaadet ja näidiskoodi, mis kirjeldavad kohandatud spikrisaidi loomist ja ühendamist spikripaaniga. Lisateabe saamiseks vt:

- [Kohandatud spikri loomine rakendusele Finance and Operations(tehniline ülevaade)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Kohandatud spikker – GitHubi hoidla](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Lisaressursid

[Spikri ülevaade](help-overview.md)

[Tegevuse salvestaja ülevaade](../../dev-itpro/user-interface/task-recorder.md)

[Kuidas luua tegevuse salvestist dokumentide või koolitusena kasutamiseks](../../dev-itpro/user-interface/task-recorder-training-docs.md)
