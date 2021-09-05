---
title: Spikri kasutuskogemuse konfigureerimine Finance and Operationsi rakendustes
description: Selles teemas antakse teavet osade Microsoft Dynamics 365 rakenduste spikrisüsteemi komponentide kohta.
author: margoc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f793068a5d4df6206229249c5b37bee0ef34da8d
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343808"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>Spikri kasutuskogemuse konfigureerimine Finance and Operationsi rakendustes

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade Finance and Operationsi rakenduste spikrisüsteemi komponentide kohta, nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources. Samuti selgitatakse selles teemas, kuidas neid komponente ühendada ja esitatakse kohandatud spikri loomise protsessi kokkuvõte.

## <a name="help-architecture"></a>Spikri arhitektuur

Finance and Operationsi rakendused hõlmavad mõistete ülevaateid ja muid teemasid, mida avaldatakse saidil [https://docs.microsoft.com/dynamics365](/dynamics365/). Selle sisu juurde pääseb seejärel tootesisese paani **Spikker** kaudu. Järgmisel joonisel on näidatud spikrisüsteemi osad.

[![Spikri arhitektuur.](./media/help-architecture.png)](./media/help-architecture.png)

Tootesisene spikrisüsteem toob artikleid saidilt docs.microsoft.com ja teistelt ühendatud veebisaitidelt. See toob ka teenuse Microsoft Dynamics Lifecycle Services (LCS) äriprotsesside modelleerijas talletatud tegevuse juhiseid.

## <a name="adding-task-guides"></a>Tegevuse juhiste lisamine

> [!NOTE]
> Vahekaart **Tegevuse juhised** ei ole praegu rakendustes Human Resources ega Commerce saadaval. <!--We are currently working to enable this functionality in a future release.--> Kuid rakenduse Human Resources alustuskogemuse tegevuse juhised jäävad põhifunktsioonide pakkumiseks saadavaks. Nii rakenduse Human Resources kui ka Commerce protseduurispikker on saadaval ka saidil [https://docs.microsoft.com/dynamics365](/dynamics365/).

Süsteemiadministraatorid saavad lehel **Süsteemi parameetrid** konfigureerida vastavatele tegevuse juhiste teekidele juurdepääsu rakendamise jaoks.

> [!NOTE]
> - Spikri konfigureerimiseks peate logima sisse kontoga samas rentnikus, kuhu rakendus juurutatakse.
> - LCS-teegiga ei saa luua ühendust rakenduse eksemplarist, mis töötab virtuaalsel kõvakettal (VHD).

[![Süsteemi parameetrite vorm koos spikrisätetega.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Lahenduse jaoks tegevuse juhiste konfigureerimiseks, järgige lehel **Süsteemi parameetrid** toodud juhiseid.

> [!IMPORTANT]
> Vahekaardi **Spikker** esmakordsel avamisel peate looma ühenduse elutsükli teenustega. Valige kindlasti vormi keskel olev link, oodake, kuni ühendus on loodud, sulgege dialoogiboks ja seejärel valige **OK**, et avada **Parameetrite vormid**.
>
> [![Ühenda LCS-iga](./media/connect-to-lcs-crop-1024x365.png "Ühenda LCS-iga.")](./media/connect-to-lcs-crop.png)

1. Valige elutsükli teenuste projekt, millega ühendus luua.
2. Valige BPM-i teegid (valitud projektis), kust tegevuse salvestised tuua.
3. Valige BPM-i teekide kuvamise järjekord. Kuvamise järjekord määratleb teekidest pärinevate tegevuse salvestiste kuvamise järjekorra paanil **Spikker**.

Kui olete need toimingud lõpetanud, võite avada paani **Spikker** ja valida vahekaardi **Tegevuse juhised**. Teile kuvatakse nüüd tegevuse juhiseid, mis rakenduvad lehele, millel parajasti rakenduses Finance and Operations olete. Kui ühtegi ülesande juhist ei leita, saate sisestada märksõnu otsingu kitsendamiseks.

### <a name="showing-translated-task-guides"></a>Tõlgitud tegevusjuhiste kuvamine

Tõlgitud tegevuse juhised avaldati esmakordselt 2016. aasta mai APQC ühendatud teegis ja teegis Alustamine. Lokaliseeritud tegevuse juhise Spikker vaatamiseks veenduge, et teie Dynamics 365 lahendus oleks ühendatud 2016. aasta mai teegiga. Kasutajad saavad muuta keelt, milles tegevuse juhis kuvatakse, muutes keelesätetteid jaotises **Suvandid** &gt; **Eelistused**.

> [!NOTE]
> Kuigi paljud tegevuse juhised on tõlgitud, ei kuva klient praegu tõlgitud tegevuse juhiste nimesid. Samuti on praegu 2016. aasta mai teegis tõlkena saadaval ainult 2016. aasta veebruaris välja antud tegevuse juhised. Microsoft annab välja värskendatud teegi, mis sisaldab täiendavaid tõlkeid.
>
> - Kui tegevusjuhis on tõlgitud, siis kuvatakse tegevusjuhise avamisel kogu selle tekst teie valitud keeles.
> - Kui tegevusjuhist pole veel tõlgitud, siis kuvatakse tegevusjuhise avamisel teie valitud keeles ainult osa tekstist (juhtelementide tekst).

## <a name="adding-custom-help"></a>Kohandatud spikri lisamine

Tegevuse juhiseid saate kasutada kohandatud spikri loomiseks või spikri veebisaidi ühendamiseks paaniga **Spikker**.

### <a name="create-custom-help-by-using-task-guides"></a>Kohandatud spikri loomine tegevuse juhiste abil

Saate luua oma toetatud rakendustele kohandatud spikri, luues tegevuse salvestised, mis kajastavad teie eksemplari, ja salvestades need LCS-i äriprotsesside teeki. Rakenduse Human Resources jaoks ei saa te kohandatud tegevuse juhiseid luua.

Kui olete partner ja viite teegi üle ettevõtte teegiks ning lisate selle lahendusse, on see teie klientidele kättesaadav. Võite teha koopia ka APQC teegist Unified Library ja avada siis tegevuse salvestised selles koopias, redigeerida neid ja salvestada oma muudatused. Lisateavet vt [Tegevuse salvestaja ressursid](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-help-site"></a>Kohandatud spikrisaidi ühendamine

Finance and Operationsi rakendusi kasutatakse harva nende valmislahenduse kujul. Selle asemel lahendust kohandatakse ja laiendatakse organisatsiooni vajadustele vastavalt. Saate kohandada ja laiendada ka spikri kasutuskogemust. Saate näiteks lisada kohandatud spikri tootesisesele paanile **Spikker**.

Microsoft pakub tööriistakomplekti, mis aitab teil juurutada ja ühendada kohandatud spikrit paanile **Spikker**. Lisateavet selle kohta, kuidas seadistada kohandatud spikri lahendust, mis oleks ühendatud paaniga **Spikker**, vaadake teemast [Kohandatud spikri ülevaade](../../dev-itpro/help/custom-help-overview.md).

Kui soovite teha Microsoftiga koostööd spikri kohandamiseks vajalike tööriistade ja protsessidega, täitke vorm aadressil [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Vt ka

[Spikrisüsteem](help-overview.md)  
[Kohandatud spikri ülevaade](../../dev-itpro/help/custom-help-overview.md)  
[Tegevuse salvestaja ressursid](../../dev-itpro/user-interface/task-recorder.md)  
[Dokumentide või koolituse loomine tegevuse salvestaja abil](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Kohandatud spikri GitHubi hoidla](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
