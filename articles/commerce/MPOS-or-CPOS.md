---
title: Valige poe äri ja pilve kassa vahel
description: See teema selgitab võtmeerinevusi poe äri ja pilve kassa vahel ning kirjeldab erinevaid tegureid, Dynamics 365 Commerce mida juurutavad jaemüüjad peaksid tegema oma nõuete jaoks parim valik.
author: jblucher
ms.date: 04/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b62e1737bc9e3b9d9e25a7a88e693a9aece80776
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629286"
---
# <a name="choose-between-store-commerce-and-cloud-pos"></a>Valige poe äri ja pilve kassa vahel

[!include [banner](includes/banner.md)]

See teema selgitab võtmeerinevusi poe äri ja pilve kassa vahel ning kirjeldab erinevaid tegureid, Dynamics 365 Commerce mida juurutavad jaemüüjad peaksid tegema oma nõuete jaoks parim valik. See annab ka juurutajatele täiendava tausta, näpunäidete ja juhendid teguritele, mida nad peaks juurutamisel kaaluma Dynamics 365 Commerce. Kui juurutajad vaatavad üle ja järgivad juurutusprotsessi osana neid juhiseid, saavad nad vältida probleeme, mis võivad mõjutada kasutaja rahulolu või jõudlust.

## <a name="insights"></a>Ülevaated

Commerce pakub mitmekülgseid juurutuse ja topoloogia valikuid. Seega saavad jaemüüjad valida komponendid ja konfiguratsiooni, mis vastavad nende äri- ja tehnoloogianõuetele kõige paremini. Üks juurutamise aspekt, mis vajab hoolikat kaalumist, on platvormi ja vormiteguri valik kassakomponendi jaoks.

### <a name="pos-platform-and-form-factor-considerations"></a>Kassaplatvormi ja vormiteguri kaalutlused

Commerce toetab järgmisi kassavalikuid.

- Rakenduse Store Commerce:<a1/& Microsoft Windows
- Store Commerce iOS-ile ja Android
- Cloud POS (CPOS), mis toetab Microsoft Edge Ja Chrome'i brauseriid
- Modern POS (MPOS) for Microsoft Windows (MPOS on taunitud oktoober 2023.) 

Kõigil juhtudel jagab kassa (Store Commerce ja CPOS) sama põhirakenduse koodi. See punkt on oluline järgmistel põhjustel.

- Kasutajaliides (UI) on järjepidev, olenemata platvormist või vormitegurist.
- Enamik võimalusi on samad, olenemata platvormist või vormitegurist. Kuid on ka olulisi erinevusi. Need erinevused on selles teemas välja toodud.
- Igas kaupluses saab kassa variatsioone kombineerida ja samaaegselt käitada. Näiteks võib jaemüüja oma peamiste registrite jaoks kasutada Store Commerce'i Windowsit kasutatavates arvutites. Kuid jaemüüja saab neid registreid täiendada brauseripõhiste terminalide või mobiilsete seadmetega.
- Kohandamisi ja laiendeid saab hõlpsalt kasutada erinevatel platvormidel ja vormitegurites. Kuna tuumrakenduse kood on jagatud, saab enamikku kohandamisi juurutada ühe korraga, mitte ei pea seda tegema mitu korda.

### <a name="store-commerce-vs-cpos"></a>Kaupluse äri vs. CPOS

Kuigi store Commerce ja CPOS on sama kuupäevad, on seal mõned olulised erinevused, mida peate aru saama.

#### <a name="store-commerce"></a>Store Commerce

Store Commerce on töölauarakendus, mis on seadmesse installitud ja mida teenuses kasutatakse.

- **Windows** – Windowsi poe rakendus sisaldab kõiki rakenduse koode Commerce Runtime (CRT) ja riistvarajaama (HWS).
- **iOS/Android** – nendel platvormidel toimib rakendus CPOS-i rakendusekoodi hostina. See tähendab, et rakenduse kood pärineb Commerce Scale Unitis majutatud CPOS-serverist. Lisateavet vt teemast [Commerce Scale Uniti ülevaade](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Kuna CPOS töötab brauseris, ei installita rakendust seadmesse. Selle asemel hangib brauser rakenduse koodile juurdepääsu CPOS-i serverist. Seetõttu ei saa CPOS otsejuurdepääsu kassa riistvarale ega saa töötada võrguühenduseta olekus.

### <a name="store-deployment-considerations"></a>Kaupluse juurutamine kaalutlused

Lisaks platvormi ja vormiteguri valimisele peavad jaemüüjad kaupluses valima ka juurutamissuvandi. Järgmises tabelis on näha konfiguratsioonid, mis on iga kassasuvandi jaoks saadaval.

| Kassa rakendus            | Commerce Scale Unit | Ühenduseta saadaval | Kohaliku HWS-i tugi |
|----------------------------|---------------------|-------------------|-------------------|
| Windowsi poe äri | Pilv või RSSU       | Jah               | Jah               |
| Rakenduse Store Commerce:<a1/& Android | Pilv või RSSU       | Nr                | Jah               |
| Store Commerce iOS-ile     | Pilv või RSSU       | Nr                | Nr                |
| Pilve kassa                  | Pilv või RSSU       | Nr                | Nr                |

#### <a name="commerce-scale-unit"></a>Commerce Scale Unit

Commerce’i skaala üksus on CRT-d majutav komponent. CRT sisaldab kogu äriloogikat, mida kassa kasutab, ja see võimaldab juurdepääsu kanali andmebaasile. Kui kassa kliendid on võrgus, kasutavad kõik kaupluses olevad kassa kliendid Commerce’i skaala üksust. Commerce’i skaala üksuse saab juurutada kas pilve või kauplusse.

#### <a name="offline-mode"></a>Ühenduseta režiim

Windowsi poe äri toetab võrguühenduseta režiimi. Ühenduseta režiimis saab kassa jätkata müügi töötlemist isegi siis, kui ühendus Commerce’i skaala üksusega katkeb. Ühenduse taastumisel saab seda seejärel sünkroonida kanali andmebaasiga. Store Commerce kasutab oma rakenduse manustatud eksemplari ja CRT kasutab ajutiselt oma kohalikku andmeallikat (võrguühenduseta SQL Serveri andmebaasi). Lisateavet võrguühenduseta funktsioonide kohta vt teemast [Kassa võrguühenduseta funktsioonid](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>Kassa välisseadmete/riistavara kaalutlused

Jaemüüjad peavad kaaluma ka seda, kuidas kassa saab juurdepääsu seadmetele ja välisseadmetele, nagu printerid, sularahasahtlid ja makseterminalid. Riistvarajaamad saab eraldada kindlale kassaregistrile või kasutada ühiselt kaupluses olevate registrite vahel.

| Kassa rakendus            | Kohalik HWS-i OPOS | Võrgu välisseadmed | HWS-i jagatud tugi |
|----------------------------|----------------|---------------------|--------------------|
| Windowsi poe äri | Jah            | Jah                 | Jah                |
| Rakenduse Store Commerce:<a1/& Android | Nr             | Jah                 | Jah                |
| Store Commerce iOS-ile     | Nr             | Nr                  | Jah                |
| Pilve kassa                  | Nr             | Nr                  | Jah                |

Lisateavet riistvarajaamade kohta leiate jaotisest [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Juurutamise kaalutlused

Kui planeerite kassa juurutamist oma kauplustes, võtke arvesse järgmist teavet.

- **Funktsionaalsed nõuded** – peamised äriprotsessid ja võimalused on samad, olenemata platvormist, vormitegurist või juurutuse topoloogiast. Seetõttu ei pea enamik jaemüüjaid juurutamise planeerimisel funktsionaalsete nõuetega arvestama.
- **Ühenduvus** – võrgu kasutatavus (laivõrk \[WAN\] ja kohtvõrk \[LAN\]) on peamine tegur, mis vajab hoolikat kaalumist. Mis tahes kulu ja kasutuslihtsusega seotud eelised, mis kaasnevad pilve majutatud nulljalajäljega lahendusega, lähevad kaotsi, kui süsteem pole tähtsate äriprotsesside jaoks saadaval.

    Kui antud seadme ühenduvus pole väga töökindel ja vastupidav või kui teatud hulk seisuaega pole jaemüüjale vastuvõetav, soovitame üht järgmistest valikutest.

    - Kasutage Windowsis poe äri ja lubage ühenduseta režiim.
    - Juurutage asutusesisene Commerce’i skaala üksus.

    Need kaks võimalust ei ole teineteist välistavad. Kõige usaldusväärsema topoloogia saavutamiseks saavad jaemüüjad juurutada kohaliku RSSU, et vähendada sõltuvust Interneti-ühendusest või Azure’i kättesaadavusest, ning kui kohaliku serveri või võrguga esineb probleem, saavad nad juurutada ka kassaregistreid, kui ühenduseta režiim on lubatud.

- **Riistvaraseadmed/välisseadmed** – süsteemi Retail POS üks olulistest aspektidest on võimalus kasutada kassa välisseadmeid, nagu printerid, sularahasahtlid ja makseterminalid. Kuigi kõik saadaolevad müügikoha valikud saavad kasutada välisseadmeid, toetab neid otse vaid Windowsi poe äri. Kõigi muude rakenduste jaoks on vaja vähemalt üht riistvarajaama. Kuigi see lähenemisviis lisab paindlikkust, tuleb juurutada, konfigureerida ja hooldada lisakomponente.
- **Süsteeminõuded** – kassarakenduse süsteeminõuded võivad olla erinevad. Enne valiku tegemist kontrollige kindlasti kõige värskemat teavet. Näiteks, kuna CPOS töötab brauseris, toetab see rohkem operatsioonisüsteeme. Lisateavet süsteeminõuete kohta vt teemast [Pilvjuurutuste süsteeminõuded](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Juurutamine ja hooldus** – juurutamis- ja hooldusnõuete keerukus võib olenevalt rakendusest ja juurutusvalikutest olla erinev. Näiteks pilves majutatud CPOS-i juurutamisel ei pea te installima ja värskendama kõigis seadmetes. Seega vähendab see lähenemine oluliselt keerukust ja kulusid. Kuid kui juurutate rakenduse Store Commerce iga kassaaparaati ja lubate ühenduseta režiimis ning juurutate ka ühise riistvara, suurendate oluliselt lõpp-punktide arvu, mida tuleb hallata.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
