---
title: "Valimine tänapäevase kassa ja pilvekassa vahel"
description: "Selles teemas selgitatakse, mis on põhierinevused jaemüügi tänapäevase kassa ja pilvekassa vahel. Selles kirjeldatakse ka erinevaid tegureid, mida lahendust Microsoft Dynamics 365 for Retail rakendavad jaemüüjad peaksid arvesse võtma, et nad saaksid oma nõuetele vastavalt teha parima valiku."
author: jblucher
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2017-10-12
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7eb15f9f73f4773d98160e1b0ec5ce74c159cdea
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---

# <a name="choose-between-modern-pos-and-cloud-pos"></a>Valimine tänapäevase kassa ja pilvekassa vahel

[!include [banner](includes/banner.md)]

See teema annab juurutajatele täiendava tausta, näpunäited ja juhiseid tegurite kohta, mida nad peaksid arvesse võtma, kui nad rakendavad lahendust Microsoft Dynamics 365 for Retail. Kui juurutajad vaatavad üle ja järgivad juurutusprotsessi osana neid juhiseid, saavad nad vältida probleeme, mis võivad mõjutada kasutaja rahulolu või jõudlust.

## <a name="insights"></a>Ülevaated
Retail pakub mitmekülgseid juurutuse ja topoloogia valikuid. Seega saavad jaemüüjad valida komponendid ja konfiguratsiooni, mis vastavad nende äri- ja tehnoloogianõuetele kõige paremini. Üks juurutamise aspekt, mis vajab hoolikat kaalumist, on platvormi ja vormiteguri valik kassakomponendi jaoks.

### <a name="pos-platform-and-form-factor-considerations"></a>Kassaplatvormi ja vormiteguri kaalutlused
Retail toetab järgmisi kassavalikuid.

- Jaemüügi tänapäevane kassa (MPOS) Microsoft Windowsi jaoks
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

Windows-, iOS- või Android-seadmes on MPOS rakendus, mida pakitakse, installitakse ja hooldatakse selles seadmes.

- **Windows** – MPOS Windowsi rakenduse jaoks sisaldab kogu rakenduse koodi ja manustatud kaubanduse käitusaega (CRT). 
- **iOS/Android** – nendel platvormidel toimib rakendus CPOS-i rakenduse koodi hostina. Teisisõnu, rakenduse kood pärineb Microsoft Azure’i või Retail Store Scale Uniti (RSSU) CPOS-i serverist. Lisateavet vt teemast [Retail Store Scale Uniti ülevaade](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/dev-itpro/retail-store-system-begin).

#### <a name="cpos"></a>CPOS

Kuna CPOS töötab brauseris, ei installita rakendust seadmesse. Selle asemel hangib brauser rakenduse koodile juurdepääsu CPOS-i serverist. Seetõttu ei saa CPOS otsejuurdepääsu kassa riistvarale ega saa töötada võrguühenduseta olekus.

### <a name="store-deployment-considerations"></a>Kaupluse juurutamine kaalutlused
Lisaks platvormi ja vormiteguri valimisele peavad jaemüüjad kaupluses valima ka juurutamissuvandi. Järgmises tabelis on näha konfiguratsioonid, mis on iga kassasuvandi jaoks saadaval.

| Kassa rakendus         | Jaemüügiserver | Ühenduseta saadaval |
|-------------------------|---------------|-------------------|
| MPOS Windowsi jaoks        | Pilv või RSSU | Jah               |
| MPOS iOS-i või Androidi jaoks | Pilv või RSSU | Ei                |
| Cloud POS               | Pilv või RSSU | Ei                |

#### <a name="retail-server"></a>Jaemüügiserver

Jaemüügiserver on CRT-d majutav komponent. CRT sisaldab kogu äriloogikat, mida kassa kasutab, ja see võimaldab juurdepääsu kanali andmebaasile. Kui kassakliendid on võrgus, kasutavad kõik kaupluses olevad kassakliendid jaemüügiserverit. Jaemüügiserveri saab juurutada kas pilve või kauplusse (RSSU).

#### <a name="offline-mode"></a>Ühenduseta režiim

MPOS Windowsi jaoks toetab ühenduseta režiimi. Ühenduseta režiimis saab kassa jätkata müügi töötlemist isegi siis, kui ühendus jaemüügiserveriga katkeb. Ühenduse taastumisel saab seda seejärel sünkroonida kanali andmebaasiga. MPOS kasutab oma CRT manustatud eksemplari ja kasutab ajutiselt oma kohalikku andmeallikat (võrguühenduseta SQL Serveri andmebaas). Lisateavet võrguühenduseta funktsioonide kohta vt teemast [Kassa võrguühenduseta funktsioonid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/pos-offline-functionality).

### <a name="pos-peripheralhardware-considerations"></a>Kassa välisseadmete/riistavara kaalutlused
Jaemüüjad peavad kaaluma ka seda, kuidas kassa saab juurdepääsu seadmetele ja välisseadmetele, nagu printerid, sularahasahtlid ja makseterminalid. Ainult MPOS Windowsi jaoks toetab otsesuhtlust nende seadmetega. MPOS Windows Phone’i, iOS-i või Androidi jaoks ning pilvekassa vajavad neile seadmetele juurdepääsu saamiseks riistvarajaama. Riistvarajaamad saab eraldada kindlale kassaregistrile või kasutada ühiselt kaupluses olevate registrite vahel. Lisateavet riistvarajaamade kohta leiate jaotisest [Jaemüügi riistvarajaama konfigureerimine ja installimine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/retail-hardware-station-configuration-installation).

## <a name="implementation-considerations"></a>Juurutamise kaalutlused
Kui planeerite kassa juurutamist oma jaekauplustes, võtke arvesse järgmist teavet.

- **Funktsionaalsed nõuded** – peamised äriprotsessid ja võimalused on samad, olenemata platvormist, vormitegurist või juurutuse topoloogiast. Seetõttu ei pea enamik jaemüüjaid juurutamise planeerimisel funktsionaalsete nõuetega arvestama.
- **Ühenduvus** – võrgu kasutatavus (laivõrk \[WAN\] ja kohtvõrk \[LAN\]) on peamine tegur, mis vajab hoolikat kaalumist. Mis tahes kulu ja kasutuslihtsusega seotud eelised, mis kaasnevad pilve majutatud nulljalajäljega lahendusega, lähevad kaotsi, kui süsteem pole tähtsate äriprotsesside jaoks saadaval.

    Kui antud seadme ühenduvus pole väga töökindel ja vastupidav või kui teatud hulk seisuaega pole jaemüüjale vastuvõetav, soovitame üht järgmistest valikutest.

  - Kasutage MPOSi Windowsis ja lubage ühenduseta režiim.
  - Juurutage kohapealne RSSU.

    Need kaks võimalust ei ole teineteist välistavad. Kõige usaldusväärsema topoloogia saavutamiseks saavad jaemüüjad juurutada kohaliku RSSU, et vähendada sõltuvust Interneti-ühendusest või Azure’i kättesaadavusest, ning kui kohaliku serveri või võrguga esineb probleem, saavad nad juurutada ka kassaregistreid, kui ühenduseta režiim on lubatud.

- **Riistvaraseadmed/välisseadmed** – süsteemi Retail POS üks olulistest aspektidest on võimalus kasutada kassa välisseadmeid, nagu printerid, sularahasahtlid ja makseterminalid. Kuigi kõik saadaolevad kassavalikud saavad kasutada välisseadmeid, toetab neid otse ainult MPOS Windowsi jaoks. Kõigi muude rakenduste jaoks on vaja vähemalt üht riistvarajaama. Kuigi see lähenemisviis lisab paindlikkust, tuleb juurutada, konfigureerida ja hooldada lisakomponente.
- **Süsteeminõuded** – kassarakenduse süsteeminõuded võivad olla erinevad. Enne valiku tegemist kontrollige kindlasti kõige värskemat teavet. Näiteks, kuna CPOS töötab brauseris, toetab see rohkem operatsioonisüsteeme. Lisateavet süsteeminõuete kohta vt teemast [Pilvjuurutuste süsteeminõuded](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/system-requirements).
- **Juurutamine ja hooldus** – juurutamis- ja hooldusnõuete keerukus võib olenevalt rakendusest ja juurutusvalikutest olla erinev. Näiteks pilves majutatud CPOS-i juurutamisel ei pea te installima ja värskendama kõigis seadmetes. Seega vähendab see lähenemine oluliselt keerukust ja kulusid. Kuid kui juurutate MPOS-i igas registris ja lubate võrguühenduseta režiimi ning juurutate ka ühiskasutuses riistvarajaamu, suurendate oluliselt haldamist vajavate lõpp-punktide arvu.

