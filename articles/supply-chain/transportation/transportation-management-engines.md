---
title: Transpordihalduse mootorid
description: Transpordihalduse mootorid määratlevad loogika, mida kasutatakse transpordihindade loomiseks ja töötlemiseks moodulis Transpordihaldus.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4a49ed7a91ec9a1b89564d40bef38cc4ea45532
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669596"
---
# <a name="transportation-management-engines"></a>Transpordihalduse mootorid

[!include [banner](../includes/banner.md)]

Transpordihalduse mootorid määratlevad loogika, mida kasutatakse transpordihindade loomiseks ja töötlemiseks moodulis Transpordihaldus. 

Transpordihalduse mootor arvutab toimingud nagu vedaja transpordihind. Mootorisüsteem võimaldab muuta käitusajal arvutusstrateegiaid, tuginedes Supply Chain Managementi andmetele. Transpordihalduse mootor sarnaneb konkreetse vedaja lepinguga seotud lisandmoodulile.

## <a name="what-engines-are-available"></a>Millised mootorid on olemas?
Järgmises tabelis on näha saadaolevad transpordihalduse mootorid.

| Transpordihalduse mootor | Kirjeldus                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Määramootor**                  | Arvutab hinnad.                                                                                                                                                                                                                                                                                                           |
| **Üldine mootor**               | Lihtsad lisamootorid, mida kasutavad teised mootorid ja mis ei nõua Supply Chain Managementi andmeid, näiteks jaotamise mootor. Jaotamise mootoreid kasutatakse transpordi lõplike kulude vähendamiseks konkreetsete tellimuste ja ridade põhjal, mis põhinevad dimensioonidel (nt maht ja kaal). |
| **Läbisõidu mootor**               | Arvutab transpordi kauguse.                                                                                                                                                                                                                                                                                     |
| **Transiitaja mootor**          | Arvutab lähtepunktist sihtpunkti liikumiseks vajaliku aja.                                                                                                                                                                                                                                       |
| **Tsooni mootor**                  | Arvutab tsooni praeguse aadressi põhjal ja tsoonide arvu, mis tuleb aadressilt A aadressile B liikumiseks läbida.                                                                                                                                                                    |
| **Veoarve tüüp**            | Standardiseerib veose arve ja veoarve read ning kasutatakse automaatseks veoarve võrdlemiseks.                                                                                                                                                                                                                |


## <a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Millised mootorid tuleb saadetise hindamiseks konfigureerida?

Saadetise hindamiseks konkreetset vedajat kasutades tuleb konfigureerida mitu transpordihalduse mootorit. **Määramootor** on nõutav, kuid **määramootori**  toetamiseks võivad olla vajalikud teised transpordihalduse mootorid. Näiteks saab **määramootorit** kasutada andmete toomiseks **läbisõidumootorist** hinna arvutamiseks lähte- ja sihtpunkti vahelise kauguse alusel.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Mida on vaja transpordihalduse mootori lähtestamiseks?
Et transpordihalduse mootor teatud viisil toimiks, on vaja seadistada lähtestamise andmed. Seadistus võib hõlmata järgmisi andmetüüpe.
-   Viited teistele transpordihalduse mootoritele. Üksikasjad leiate selle jaotise konfiguratsiooninäitest.
-   Viited .NET-tüüpidele, mida transpordihalduse mootor kasutab.
-   Lihtsad konfiguratsiooniandmed.

Enamasti võite lähtestamise andmete konfigureerimiseks klõpsata nuppu **Parameetrid** transpordihalduse mootori seadistusvormidel. **Läbisõidumootorile viitava määramootori konfigureerimise näide.** Järgmises näites on toodud seadistus, mis on .NET-mootori tüübil Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine põhineva määramootori puhul nõutav ja mis viitab läbisõidumootorile.

|          Parameeter           |                                                                                  Kirjeldus                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | .NET-tüüp, mis tõlgendab hinna aluse määrangu andmeid konkreetse skeemi puhul. Parameetri väärtuse süntaks koosneb kahest segmendist, mis on piiritletud vertikaalribaga ( |
|  <em>MileageEngineCode</em>  |                       Läbisõidumootori kood, mis tähistab läbisõidumootori kirjet andmebaasis.                        |
| <em>ApportionmentEngine</em> |                        Üldise mootori kood, mis tähistab jaotamise mootorit andmebaasis.                        |

## <a name="how-is-metadata-used-in-transportation-management-engines"></a>Kuidas kasutatakse transpordihalduse mootorites metaandmeid?

Supply Chain Managementis määratletud andmetele tuginevad transpordihalduse mootorid võivad kasutada teistsuguseid andmeskeeme. Transpordihalduse süsteem võimaldab erinevatel transpordihalduse mootoritel kasutada samu üldise füüsilise andmebaasi tabeleid. Veendumaks, et mootori andmete käitusaja tõlgendus on õige, saate määratleda andmebaasitabelite metaandmed. See vähendab uute transpordihalduse mootorite loomise kulu, kuna Operationsis pole vaja täiendavaid tabeli- ja vormistruktuure.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Mida saab hinnaarvutustes otsinguandmetena kasutada?
Andmeid, mida hindade arvutamiseks kasutate, kontrollitakse metaandmete konfiguratsiooniga. Näiteks kui soovite otsida hindu sihtnumbrite põhjal, peate seadistama metaandmed sihtnumbri otsingutüübi alusel.

## <a name="do-all-engine-configurations-require-metadata"></a>Kas kõik mootorikonfiguratsioonid nõuavad metaandmeid?
Ei, hinnaarvutuseks välistest süsteemidest andmete toomiseks kasutatavad transpordihalduse mootorid ei vaja metaandmeid. Nende mootorite jaoks saab hinnaandmed tuua välistest vedaja süsteemidest, tavaliselt veebiteenuse kaudu. Näiteks saate kasutada läbisõidumootorit, mis toob andmed otse Bingi kaartidest, seega pole selle mootori jaoks metaandmeid vaja.

| **Märkus.**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Transpordihalduse mootorid, mis on Supply Chain Managementiga kaasas, tuginevad rakendusest toodud andmetele. Väliste süsteemidega ühenduvaid mootoreid pole Operationsiga kaasas. Kuid mootoripõhise laiendatavusega mudel võimaldab luua laiendusi, kasutades rakenduse Visual Studio tööriistu. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Kuidas konfigureerida transpordihalduse mootori metaandmeid?
Transpordihalduse mootorite metaandmed konfigureeritakse erinevate mootori tüüpide puhul erinevalt.

| Transpordihalduse mootor               | Metaandmete konfigureerimine                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Määramootor**                                | Nõuab **määra alustüüpi**. Hinna aluse tüüp sisaldab hinna aluse andmete ja hinna aluse määrangu andmete metaandmeid. Hinna aluse metaandmete struktuur määratakse määra mootori tüübiga. Hinna aluse määrangu metaandmete struktuur määratakse hinna aluse määraja tüübiga, mis on selle määra mootoriga seotud. Määramootori määra alustüübi saate seadistada lehel **Määramootor** ja lehel **Koondmäär**. |
| **Tsooni mootor**                                | See nõuab metaandmete otsest seadistamist tsooni koondandmetes.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Transiidiaja mootor** ja **läbisõidumootor** | Toob metaandmed otse läbisõidu mootori konfiguratsiooni seadistamise vormilt.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Määramootori metaandmete näide.** Transpordihalduse mootor nõuab päritoluaadressi, sihtosariigi ja -riigi/-piirkonna ning saadetise lähte- ja sihtpunkti märkimist. Nende nõuete järgi näeksid metaandmed välja nagu järgmises tabelis olevad andmed. Tabel sisaldab ka teavet sisendandmete nõutava tüübi kohta.
-   Määratlege see teave valikus **Transpordihaldus** &gt; **Seadistus** lehel **Hinna aluse tüüp**.

| Järjestus | Nimi                          | Välja tüüp | Andmetüüp | Otsingu tüüp    | Kohustuslik |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Lähtekoha sihtnumber            | Määramine | String    | Sihtnumber    | Valitud  |
| 2        | Sihtkoha osariik             | Määramine | String    | Osariik          |           |
| 3        | Sihtkoha alguse sihtnumber | Määramine | String    | Sihtnumber    | Valitud  |
| 4        | Sihtkoha lõpu sihtnumber   | Määramine | String    | Sihtnumber    | Valitud  |
| 5        | Sihtriik           | Määramine | String    | Riik/regioon |           |

### <a name="whitepaper"></a>Tehniline ülevaade

Lisateabe saamiseks laadige alla järgmine tehniline ülevaade (kirjutatud versiooni AX2012 toetamiseks, kuid kehtib ka rakendusele Dynamics 365 Supply Chain Management)

- [Transpordihalduse mootorid](https://download.microsoft.com/download/e/0/9/e0957665-c12f-43c7-94c0-611cc49d7d61/TransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]