---
title: Modern POS-i (MPOS) ja pilvekassa vahel valimine
description: Selles teemas selgitatakse Modern POS-i ja pilvekassa vahelisi erinevusi. Selles kirjeldatakse ka erinevaid tegureid, mida rakendust Dynamics 365 Commerce kasutusele võtvad jaemüüjad peaksid arvesse võtma, et teha oma nõuetele vastav parim valik.
author: jblucher
ms.date: 10/13/2017
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
ms.openlocfilehash: f19506d66aef22099dae9396fd345c293bf559b7
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193067"
---
# <a name="choose-between-modern-pos-mpos-and-cloud-pos"></a>Modern POS-i (MPOS) ja pilvekassa vahel valimine

[!include [banner](includes/banner.md)]

See teema annab juurutajatele täiendava tausta, näpunäited ja juhiseid tegurite kohta, mida nad peaksid arvesse võtma, kui juurutavad rakendust Dynamics 365 Commerce. Kui juurutajad vaatavad üle ja järgivad juurutusprotsessi osana neid juhiseid, saavad nad vältida probleeme, mis võivad mõjutada kasutaja rahulolu või jõudlust.

## <a name="insights"></a>Ülevaated

Commerce pakub mitmekülgseid juurutuse ja topoloogia valikuid. Seega saavad jaemüüjad valida komponendid ja konfiguratsiooni, mis vastavad nende äri- ja tehnoloogianõuetele kõige paremini. Üks juurutamise aspekt, mis vajab hoolikat kaalumist, on platvormi ja vormiteguri valik kassakomponendi jaoks.

### <a name="pos-platform-and-form-factor-considerations"></a>Kassaplatvormi ja vormiteguri kaalutlused

Commerce toetab järgmisi kassavalikuid.

- Modern POS (MPOS) Microsoft Windowsile
- MPOS Microsoft Windows Phone’i jaoks
- MPOS Apple iPadi või Google Androidi tahvelarvuti jaoks
- Pilvekassa (CPOS), mis toetab brausereid Microsoft Edge, Internet Explorer ja Google Chrome

Kõigil juhtudel jagab kassa (MPOS ja CPOS) sama tuumrakenduse koodi. See punkt on oluline järgmistel põhjustel.

- Kasutajaliides (UI) on järjepidev, olenemata platvormist või vormitegurist.
- Enamik võimalusi on samad, olenemata platvormist või vormitegurist. Kuid on ka olulisi erinevusi. Need erinevused on selles teemas välja toodud.
- Antud kaupluses saab kassavariatsioone kombineerida ja samaaegselt käivitada. Näiteks saab jaemüüja oma peamiste registrite jaoks MPOS-i kasutada arvutites, milles töötab Windows. Kuid jaemüüja saab neid registreid täiendada brauseripõhiste terminalide või mobiilsete seadmetega.
- Kohandamisi ja laiendeid saab hõlpsalt kasutada erinevatel platvormidel ja vormitegurites. Kuna tuumrakenduse kood on jagatud, saab enamikku kohandamisi juurutada ühe korraga, mitte ei pea seda tegema mitu korda.

### <a name="mpos-vs-cpos"></a>MPOS vs CPOS

Kuigi MPOS ja CPOS on suures osas samad, on ka olulisi erinevusi, mida peate mõistma.

#### <a name="mpos"></a>MPOS

Windowsi, iOS-i või Androidi seadmes on MPOS rakendus, mida pakitakse, installitakse ja hooldatakse selles seadmes.

- **Windows** – MPOS Windowsi rakenduse jaoks sisaldab kogu rakenduse koodi ja manustatud Commerce Runtime’i (CRT). 
- **iOS/Android** – nendel platvormidel toimib rakendus CPOS-i rakendusekoodi hostina. Teisisõnu tuleb rakendusekood CPOS-i serverist Microsoft Azure’is või Commerce’i skaala üksuses. Lisateavet vt teemast [Commerce Scale Uniti ülevaade](dev-itpro/retail-store-system-begin.md).

#### <a name="cpos"></a>CPOS

Kuna CPOS töötab brauseris, ei installita rakendust seadmesse. Selle asemel hangib brauser rakenduse koodile juurdepääsu CPOS-i serverist. Seetõttu ei saa CPOS otsejuurdepääsu kassa riistvarale ega saa töötada võrguühenduseta olekus.

### <a name="store-deployment-considerations"></a>Kaupluse juurutamine kaalutlused

Lisaks platvormi ja vormiteguri valimisele peavad jaemüüjad kaupluses valima ka juurutamissuvandi. Järgmises tabelis on näha konfiguratsioonid, mis on iga kassasuvandi jaoks saadaval.

| Kassa rakendus         | Commerce’i skaala üksus | Ühenduseta saadaval |
|-------------------------|---------------|-------------------|
| MPOS Windowsi jaoks        | Pilv või RSSU | Jah               |
| MPOS iOS-i või Androidi jaoks | Pilv või RSSU | Ei                |
| Pilve kassa               | Pilv või RSSU | Ei                |

#### <a name="commerce-scale-unit"></a>Commerce’i skaala üksus

Commerce’i skaala üksus on CRT-d majutav komponent. CRT sisaldab kogu äriloogikat, mida kassa kasutab, ja see võimaldab juurdepääsu kanali andmebaasile. Kui kassa kliendid on võrgus, kasutavad kõik kaupluses olevad kassa kliendid Commerce’i skaala üksust. Commerce’i skaala üksuse saab juurutada kas pilve või kauplusse.

#### <a name="offline-mode"></a>Ühenduseta režiim

MPOS Windowsi jaoks toetab ühenduseta režiimi. Ühenduseta režiimis saab kassa jätkata müügi töötlemist isegi siis, kui ühendus Commerce’i skaala üksusega katkeb. Ühenduse taastumisel saab seda seejärel sünkroonida kanali andmebaasiga. MPOS kasutab oma CRT manustatud eksemplari ja kasutab ajutiselt oma kohalikku andmeallikat (võrguühenduseta SQL Serveri andmebaas). Lisateavet võrguühenduseta funktsioonide kohta vt teemast [Kassa võrguühenduseta funktsioonid](pos-offline-functionality.md).

### <a name="pos-peripheralhardware-considerations"></a>Kassa välisseadmete/riistavara kaalutlused

Jaemüüjad peavad kaaluma ka seda, kuidas kassa saab juurdepääsu seadmetele ja välisseadmetele, nagu printerid, sularahasahtlid ja makseterminalid. Ainult MPOS Windowsi jaoks toetab otsesuhtlust nende seadmetega. MPOS Windows Phone’i, iOS-i või Androidi jaoks ning pilvekassa vajavad neile seadmetele juurdepääsu saamiseks riistvarajaama. Riistvarajaamad saab eraldada kindlale kassaregistrile või kasutada ühiselt kaupluses olevate registrite vahel. Lisateavet riistvarajaamade kohta leiate jaotisest [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md).

## <a name="implementation-considerations"></a>Juurutamise kaalutlused

Kui planeerite kassa juurutamist oma kauplustes, võtke arvesse järgmist teavet.

- **Funktsionaalsed nõuded** – peamised äriprotsessid ja võimalused on samad, olenemata platvormist, vormitegurist või juurutuse topoloogiast. Seetõttu ei pea enamik jaemüüjaid juurutamise planeerimisel funktsionaalsete nõuetega arvestama.
- **Ühenduvus** – võrgu kasutatavus (laivõrk \[WAN\] ja kohtvõrk \[LAN\]) on peamine tegur, mis vajab hoolikat kaalumist. Mis tahes kulu ja kasutuslihtsusega seotud eelised, mis kaasnevad pilve majutatud nulljalajäljega lahendusega, lähevad kaotsi, kui süsteem pole tähtsate äriprotsesside jaoks saadaval.

    Kui antud seadme ühenduvus pole väga töökindel ja vastupidav või kui teatud hulk seisuaega pole jaemüüjale vastuvõetav, soovitame üht järgmistest valikutest.

    - Kasutage MPOSi Windowsis ja lubage ühenduseta režiim.
    - Juurutage asutusesisene Commerce’i skaala üksus.

    Need kaks võimalust ei ole teineteist välistavad. Kõige usaldusväärsema topoloogia saavutamiseks saavad jaemüüjad juurutada kohaliku RSSU, et vähendada sõltuvust Interneti-ühendusest või Azure’i kättesaadavusest, ning kui kohaliku serveri või võrguga esineb probleem, saavad nad juurutada ka kassaregistreid, kui ühenduseta režiim on lubatud.

- **Riistvaraseadmed/välisseadmed** – süsteemi Retail POS üks olulistest aspektidest on võimalus kasutada kassa välisseadmeid, nagu printerid, sularahasahtlid ja makseterminalid. Kuigi kõik saadaolevad kassavalikud saavad kasutada välisseadmeid, toetab neid otse ainult MPOS Windowsi jaoks. Kõigi muude rakenduste jaoks on vaja vähemalt üht riistvarajaama. Kuigi see lähenemisviis lisab paindlikkust, tuleb juurutada, konfigureerida ja hooldada lisakomponente.
- **Süsteeminõuded** – kassarakenduse süsteeminõuded võivad olla erinevad. Enne valiku tegemist kontrollige kindlasti kõige värskemat teavet. Näiteks, kuna CPOS töötab brauseris, toetab see rohkem operatsioonisüsteeme. Lisateavet süsteeminõuete kohta vt teemast [Pilvjuurutuste süsteeminõuded](../fin-ops-core/fin-ops/get-started/system-requirements.md).
- **Juurutamine ja hooldus** – juurutamis- ja hooldusnõuete keerukus võib olenevalt rakendusest ja juurutusvalikutest olla erinev. Näiteks pilves majutatud CPOS-i juurutamisel ei pea te installima ja värskendama kõigis seadmetes. Seega vähendab see lähenemine oluliselt keerukust ja kulusid. Kuid kui juurutate MPOS-i igas registris ja lubate võrguühenduseta režiimi ning juurutate ka ühiskasutuses riistvarajaamu, suurendate oluliselt haldamist vajavate lõpp-punktide arvu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]