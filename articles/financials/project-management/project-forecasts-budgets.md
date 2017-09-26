---
title: Projekti prognoosid ja eelarved
description: 
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 835a92a8f95c7d75b02f5991cc2528c6a209540a
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="project-forecasts-and-budgets"></a>Projekti prognoosid ja eelarved

[!include[banner](../includes/banner.md)]




Microsoft Dynamics 365 for Finance and Operations, Enterprise edition võimaldab hallata ja juhtida projekte kahel viisil: projekti prognoosid ja projekti eelarved. 

Kasutage projekti prognoosi, kui teie organisatsioonil on tegevustele suunatud perspektiiv ja keskendutakse konkreetsetest tehingutest tulenevatele tuludele ja kuludele. Kasutage projekti eelarvet, kui teie organisatsioon keskendub rohkem rahasummadele. 

Nii projekti prognoosid kui ka projekti eelarved kasutavad plaanitud kandesummade paigutamiseks prognoosimudeleid. 

Kummalgi meetodil on omad eelised. Enne organisatsiooni jaoks meetodi valimist tuleks arvestada järgmisi punkte.

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | **Projekti prognoosi koostamine**                                                                                                                                                                                                                                 | **Projekti eelarve koostamine**                                                                                                                                                   |
| **Perioodi eraldamine**     | Kandeid ei saa konkreetselt rahandusperioodile jaotada. Selle asemel põhinevad prognoos ja prognoosi juhtimine projekti kestusel. Kuna prognoosid põhinevad konkreetsel kuupäeval, tuleb periood tuletada kuupäevast. | Saate eraldada kanded kogu projektile või rahandusperioodile. Kui eraldate perioodile, saate viia kasutamata summad järgmisse rahandusperioodi üle. |
| **Kannete kuvamine**  | Saate kuvada kanded prognoosi vormidel, kus on näha kogu ettevõtte ja kõigi projektide prognoosid, olenemata hierarhiast. Konkreetsele projektile keskendumiseks saate andmeid filtreerida.                                       | Saate vaadata ühe projektihierarhia eelarvelisi kandeid. Seega saate vaadata põhiprojekti ja selle alamprojektide kannete üksikasju.                 |
| **Kande muutujad** | Prognoosi kannete sisestamisel saate kasutada iga atribuuti, mis tegelikul kandel on. See võimaldab üksikasjalikumat prognoosi. Näiteks saate sisestada koguse, töötajate, kaupade või reaatribuutide üksikasjad.         | Eelarve üksikasjade sisestamisel saate kasutada ainult summasid, kategooriaid ja tegevusi.                                                                                    |
| **Turvalisus**              | Prognoosimine põhineb prognoosi vormidele sisestatud kannetel ega hõlma ühtegi protsessi kontrollimehhanismi. Töötaja, kellel on prognoosivormi load, saab parandada andmeid ilma kinnituseta.                                        | Eelarve koostamisel kasutatakse töövoo süsteemi, mis võimaldab muudatuste haldamist ja võimaldab säilitada versiooniajalugu.                                                       |
| **Kirjete tüübid**           | Prognoosi kandekirjed põhinevad ühikute arvul ning kulul ja müügiüksuste hindadel.                                                                                                                                                       | Eelarve üksikasjad põhinevad summadel, mis on jagatud tuludeks ja kuludeks.                                                                                        |
| **Eelarvemudelid**       | Kuna iga eelarve tuleb seostada mudeliga, saate luua mitu eelarvemudelit ja seadistada ka alammudeleid.                                                                                                                               | Projekti eelarve piirab eelarvestamiseks kasutatavaid eelarvemudeleid. Väiksem eelarvemudelite arv aitab suurendada plaanide järjepidevust.                           |
| **Kulu ületamine**         | Saate ainult lubada või keelata kanded, mis põhjustavad kulu ületamise.                                                                                                                                                                | Projekti eelarve koostamine annab kasutajatele juhtimiseks lisavõimalusi. Saate lubada hoiatused ja ülekulu.                                                                   |
| **Juhtimine**               | Prognoosi juhtimine toimub prognoosi vähendamise abil. Tegelikud summad lahutatakse eelarvekande saldodest ilma igasuguse kontrolljäljeta. See võib tegelike kannete toimumiskoha tuvastamise keerukamaks muuta.                   | Projekti eelarve juhtimisel lahutatakse tegelikud summad järelejäänud eelarve summadest. See tagab selgema kontrolljälje.                                   |

## <a name="project-forecasts"></a>Projekti eelarved
Projekti prognoosimise kasutamisel saate sisestada eelarvekanded iga kandetüübi puhul prognoosivormidele. Prognoosi kande jaoks saab kasutada iga atribuuti, mis on saadaval tegeliku kande jaoks – nt rea tulusus, rea atribuudid, töötajad või kirjeldused. Samuti saate plaanida, kui pika aja jooksul pärast kulu kandmist kliendile arve esitate. 

Projekti eelarvekanded põhinevad ühikutel ja summadel. 

Iga projektiprognoos tuleb seostada prognoosimudeliga. Kui prognoosikande sisestate, soovitatakse automaatselt prognoosimudelit. Prognoosimudel toimib prognoosikannete konteinerina. 

Saate määrata prognoosimudelid mudeli alammudeliteks. See võimaldab prognoosida piirkonna, ajavahemiku või osakonna alusel. Mudeli prognoosikandeid saate uue mudeli loomiseks mudelisse kopeerida ning kandeid ka pearaamatusse üle kanda. Kuna prognoosi ja mudeli vahel on üks-ühele suhe, moodustab iga eelarvemudel projekti jaoks eraldi eelarve. 

Eelarvemudelid saavad projektide kontrollimehhanismina kasutada prognoosi vähendamist. Prognoosi vähendamisega vähendavad tegelikud kanded prognoosi kandesaldosid. Kuna prognoosi vähendamine rakendatakse hierarhia kõrgeimale projektile, pakub see prognoosi muudatustele piiratud vaadet. Näiteks kui töötaja on seostatud alamprojektiga, sisestatakse töötaja tegelikud kanded peaprojekti. Seetõttu võib olla keeruline muutusi jälgida, kuna pole võimalik hõlpsasti määrata, milline kanne millises alamprojektis põhjustas prognoosisumma vähenemise. Seetõttu tasub kopeerida prognoosimudel prognoosi vähendamises kasutamiseks. Seejärel saate algselt prognoositud andmete vaatamiseks aruandeid kasutada. 

Projekti prognoose saab parandada, kopeerida või edastada pearaamatu eelarvesse. Kuid protsessijuhtimine puudub. Iga prognoosivormi loaga töötaja saab teha parandusi ilma ülevaatuseta.

-   **Paranda ** – prognoosikandeid saate parandada samadel vormidel, kus tehti algsed kanded.
-   **Kopeeri või kustuta** – prognoosikannete kopeerimisel kopeerige ühe prognoosimudeli kanderead teise prognoosimudelisse. Prognoosi kustutamisel kustutate eelarvekanded eelarvemudelist. Kopeeritavate või kustutatavate prognoosikannete piiramiseks saate valida kindlad kandetüübid ja kuupäevad. See võimaldab teil kopeerida või kustutada ainult kindlaid prognoosi osi.
-   **Ülekanne** – projekti prognoosi ülekandmisel pearaamatu eelarvesse kannate sellesse üle prognoosimudeli prognoosikanded. Kõiki pearaamatu eelarvesse, kuhu oma projekti prognoosi üle kannate, varem üle kantud kandeid saab üle kirjutada.

## <a name="project-budgets"></a>Projekti eelarved
Projekti eelarve koostamine on prognoosi koostamisest lihtsam meetod, kuid seda saab integreerida prognoosimudelitega. See kasutab ühte sisestusvormi algsete eelarveüksikasjade ja paranduste jaoks ning võimaldab teha plaane, mis põhinevad ainult summal, kategoorial või tegevusel. 

Projekti eelarve koostamisel tuleb kõik algsed eelarved ja parandused saata projekti töövoogu kinnitamiseks. Töövood annavad suurema kontrolli protsessi üle ja loovad muudatuste ajaloo kirje. 

Projekti eelarve koostamine sarnaneb pearaamatu eelarve koostamisele, kuid selle seadistamine on kiirem ja lihtsam. Paljusid pearaamatu eelarve koostamise valikuid (nt numbriseeriad või valuutad) ei ole vaja projektidele eraldi seadistada.

Projekti eelarveid seostatakse automaatselt kahe eelarvemudeliga: üks algse eelarve jaoks ja teine eelarvejäägi jaoks. Seetõttu saab aruannetes, mis põhinevad eelarvemudelitel, kasutada eelarve andmeid. Kooskõlastatud projekti eelarve puhul loob süsteem seotud mudelite põhjal prognoosikanded, mida kasutatakse aruandluseks ja kontrollimise eesmärgil.

## <a name="forecast-models"></a>Prognoosimudelid
Prognoosimudelitel on ühekihiline hierarhia. See tähendab, et üks projektiprognoos tuleb seostada ühe prognoosimudeliga.

Projekti prognoosi kasutamisel saate märkida mudelid alammudeliteks. Seejärel saate koostada prognoose osakonna, ajavahemiku või piirkonna alusel. Näiteks võite luua prognoosimudeli aasta kohta ja luua siis alammudelid kirde-, kagu-, edela- ja loodepiirkonna prognooside jaoks, mida piirkondlikud juhid esitavad. Erinevate valikutega olemasolevates aruannetes saate vaadata andmeid kogu prognoosi või alammudeli järgi.




