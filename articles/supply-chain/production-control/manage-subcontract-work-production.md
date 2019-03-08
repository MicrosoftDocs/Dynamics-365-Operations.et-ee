---
title: Allhanketöö haldamine tootmises
description: Selles teemas selgitatakse, kuidas hallatakse Microsoft Dynamics 365 for Finance and Operationsis allhanketööd. Teisisõnu selgitab see, kuidas hankija haldab ressursile määratud tootmisoperatsioone.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanDocumentServiceCreation, PlanActivity, ProdBOMVendorListPage, ProdRoute, ProdTable, ProdTableListPage, PurchAgreementSubcontractorLookup, RouteTable, WrkCtrResourceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 268174
ms.assetid: fe47c498-4f48-42a2-a0cf-5436c19ab3ea
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f41f13bf1b587cb802579cc3b27ef4eea70a0380
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "326580"
---
# <a name="manage-subcontracting-work-in-production"></a>Allhanketöö haldamine tootmises

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas hallatakse Microsoft Dynamics 365 for Finance and Operationsis allhanketööd. Teisisõnu selgitab see, kuidas hankija haldab ressursile määratud tootmisoperatsioone.

[Tootmisprotsessides](production-process-overview.md) võivad tööd teha ressursid, mille omanikud on või mida haldavad hankijad. Tavaliselt kasutatakse hankija ressursse perioodilise liigse nõudluse tasakaalustamiseks, kui see ületab ettevõtte oma ressursside mahtu. Võib-olla saab hankija pakkuda ka konkreetseid [ressursivõimalusi](resource-capabilities.md)või ressursse madalama hinnaga.  

Olenevalt tootmisprotsessis kasutatavatest hankija ressurssidest on [protsessil](routes-operations.md) sageli täiendavad logistilised nõuded, kuna materjal ja pooltooted tuleb esmalt hankija tegevuskohta transportida. Seejärel tuleb allhanketöö tulemus transportida järgmise toimingu jaoks mõeldud asukohta või valmistoodete lattu.  

Kui kasutatakse allhankeoperatsioone või -tegevusi, siis mõjutavad need kõiki tegevuste etappe, alates tootmises vajalike operatsioonide määratlemisest, kuluarvestusest, prognoosimisest, plaanimisest ja ajakava koostamisest kuni materjali, pooltoodete ja valmistoodete logistika haldamiseni. Lõpuks nõuavad need ressursid oma raamatupidamis- ja kulujuhtimisprotsesse.  

Sisemiste ressursside puhul eraldatakse teatud perioodiks tavaliselt kindel kulumäär. Seevastu allhankeressursside maksumus põhineb seotud teenuse ostuhinnal. Teenus määratletakse teise tootena ja seda kasutatakse antud allhangitud operatsiooni hanke- ning ostuprotsesside juhtimiseks.  

Praegu ei ole Microsoft Dynamics 365 for Finance and Operationsis sõnaselget pooltoodete mõistet. Tootmistellimuse puhul, mis nõuab tooraine valmiskaubaks muutmiseks mitut operatsiooni, sisestatakse valmistoode varudesse tagasi alles viimases toimingus. Varasemate operatsioonide käigus saadud pooltooted registreeritakse poolelioleva tööna (WIP), kuid neid ei sisestata ega jälgita varudes. Kuigi võite protsessid ja kooslused mitmeks väiksemaks üksuseks jagada, suurendab see lähenemine hallatavate toodete, koosluste ja protsesside arvu.  

Allhanketöö modelleerimiseks tootmisoperatsioonide jaoks on kaks meetodit. Need meetodid erinevad selle poolest, kuidas allhankeprotsessi saab modelleerida, kuidas pooltooteid protsessis kajastatakse ja kuidas toimub kuluhaldus.

-   Protsessioperatsioonide allhange tootmistellimuste või partiitellimuste puhul
    -   Teenusetoode peab olema ladustatud toode ja kuuluma kooslusse.
    -   See meetod toetab elavjärjekorra (FIFO) või standardkulu meetodit.
    -   Pooltooted kajastatakse protsessis teenusetootena.
    -   Kulude juhtimine eraldab allhanketööga seotud kulud materjalikuludesse.
-   Tootmisvoo tegevuste allhange säästlikus tootmisvoos
    -   See teenus on mitteladustatud teenusetoode ega kuulu koosluse hulka.
    -   See meetod kasutab ostulepinguid ja teeninduslepinguid.
    -   See meetod kasutab omahinna tagasiarvestust.
    -   See meetod võimaldab koondatud ja asünkroonset hanget. (Materjalivoog ei sõltu hankeprotsessist.)
    -   Kulude juhtimine eraldab allhanketöö eraldi kulujaotuse plokki.

## <a name="subcontracting-of-route-operations"></a>Protsessioperatsioonide allhange
Partiitellimuste tootmise protsessioperatsioonide jaoks allhanke kasutamiseks tuleb teenusetoode, mida teenuse ostmiseks kasutatakse, määratleda tootena, mille tüüp on **Teenus**. Lisaks peab sellel olema kauba mudeligrupp, mille valiku **Ladustatav toode** väärtuseks jaotises **Varude poliitika** on määratud **Jah**. See valik määratleb, kas toodet käsitletakse toote sissetulekul varudena (**Ladustatav toode** = **Jah**) või toode kantakse kasumi ja kahjumi kontol kuludesse (**Ladustatud toode** = **Ei**). Kuigi see käitumine võib paista vastuoluline, põhineb see asjaolul, et ainult selle poliitikaga tooted tekitavad laokandeid, mida saab kasutada kulude juhtimises plaanitud kulu arvutamiseks ja tegeliku kulu määramiseks, kui tootmistellimus lõpetatakse.  

Plaanimises ja kuluarvutuses arvestamiseks tuleb teenus kooslusse lisada. Koosluse rea tüüp peab olema **Hankija** ja see tuleb määrata protsessioperatsioonile, millele teenus on määratud. Sellel protsessioperatsioonil peab olema kuluarvutuse ressurss ja ressursitingimus, mis osutavad ressursile tüübiga **Hankija**, mis ühendab operatsiooni ja seotud teenuse vastava hankija kontoga.  

Selle konfiguratsiooni kasutamisel koostatakse seotud teenusetootele ostutellimus, mis põhineb tootmistellimuse prognoosil. Teenuse tootmistellimust kasutatakse allhangitud toimingute ankruna. Allhanketööd saab hallata loendilehe **Allhanketöö** kaudu tootmise juhtimises. Allhanketööd kasutatakse tooraine ja lõpuks pooltoote lähetamiseks hankijale operatsiooniks valmistumisel. Samuti kasutatakse seda allhangitud operatsiooniga tekitatud toote vastuvõtmiseks kauba saabumisel, kus teenusetoodet kasutatakse pooltoote saabumise tuvastamiseks. Ostutellimuse rea vastuvõtmisel märgitakse tootmisoperatsioon lõpetatuks.  

Tootmistellimusel võib olla mitu operatsiooni ja iga operatsiooni saab määrata erinevale hankijale. Seega võib terve tootmistellimus käivitada mitu ostutellimust.

## <a name="subcontracting-of-production-flow-activities"></a>Tootmisvoo tegevuste allhange
[Lean manufacturingi](lean-manufacturing-overview.md) lahendus modelleerib allhanketööd teenusena, mis on seotud [tootmisvoo](tasks/create-production-flow-version.md) tegevusega (tegevuse juhise teema). Seetõttu nimetatakse seda tüüpi allhanget ka [tegevusepõhiseks allhankeks.](activity-based-subcontracting.md) Kasutusele on võetud kulugrupi eritüüp **Otse sisseostmine** ja allhanketeenused ei ole enam valmis kauba koosluse osa. Lean manufacturingi kasutamisel määratletakse kõik tegevused kanbanidega, mille saab seostada vähemalt ühe tootmisvoo tegevusega. Siiamaani kõlab see selgitud täpselt nagu tootmistellimuste selgitus. Kuid kui tootmistellimused peavad alati lõppema valmis tootega, siis kanbane saab luua pooltoote tarnimiseks. Uut toodet ja koosluse taset pole vaja tekitada.  

Kuna kanbani reeglid võivad olla väga dünaamilised, saate modelleerida sama toote jaoks tootmisvoos erinevaid tarnevariante. Säästliku allhanke kasutamisel on materjalivoog ja finantsvoog rangelt eraldatud. Kogu materjalivoog kajastatakse kanban-tegevustega. Teenusetoodete ostutellimused ja nende teenuste kviitungite sisestamised saab automatiseerida, tuginedes kanban-tööde olekule tootmisvoos. Kanban-töid saab alustada ja lõpetada isegi enne ostutellimuste loomist. Allhankedokumendid (ostutellimus ja teenuse ostukviitung) saab koondada perioodi ja teenuse järgi. Seega saab ostudokumentide ja ridade arvu väiksena hoida, isegi rohkete korduvate operatsioonide puhul, kui hankijad osutavad allhanketeenuseid üheosalises voos.

### <a name="modeling-subcontracting-in-a-production-flow"></a>Allhanke modelleerimine tootmisvoos

[Säästlikus tootmisvoos](lean-manufacturing-modeling-lean-organization.md) saab protsessitegevuse määratleda allhankena, kui see on määratud ühe hankija ressursiga töörakule (ressursigrupile). Tööraku allhanke puhul peavad seotud protsessitegevused olema seotud aktiivse ostulepingu reaga, mis sisaldab teenuseüksust ja teenuse hinda. Tegevuse teenuseleping määratleb ka arvutussuhte kanban-töö toote koguse ja saadud teenuse koguse vahel. Saate valida, kas teenuse kogus arvutatakse tööde arvu, tööde puhul registreeritud nõuetele vastavate toodete koguse või toodete üldkoguse põhjal (see üldkogus sisaldab praaktooteid).  

Ülekandetegevusi saab samuti allhankena määratleda. Selline määratlemine toimub iseenesest, kui valite ülekandetegevusest saatmise eest vastutava osapoole. Kui valite **Saatja** või **Vastuvõtja**, siis kui vastav lähte- või sihtladu on hankija hallatav ladu, käsitletakse tegevust allhankena. Kui valite **Vedaja**, on tegevus alati allhange. Nagu allhankeprotsessi tegevused, peab ka allhangitud ülekandetegevus olema seotud teenuselepinguga, enne kui tootmisvoo saab aktiveerida.

### <a name="backflush-costing"></a>Omahinna tagasiarvestus

Allhanketöö kuluarvestus on täielikult integreeritud lean manufacturingi kululahendusse (omahinna tagasiarvestus). Kui sisestatakse teenuse ostutellimuse sissetulek või kui toimub arveldamine, siis määratakse teenuse kulu tootmisvoole. Omahinna tagasiarvestuseks arvutatakse allhangitud teenuste hälve, tasakaalustades vastuvõetud toodete standardkulu allhankeploki tegelike vastu võetud ja arveldatud teenusekogustega.

## <a name="material-supply-for-subcontracted-operations"></a>Materjali tarnimine allhankeoperatsioonide jaoks
Pooltooted ja muud seotud materjalid tuleb edastada kohta, kus töö füüsiliselt tehakse. Kui kasutate allhangitud operatsioone ja toiminguid, on see üleviimine sageli seotud täiendava transpordiga hankija tegevuskohta. Koosluses oleva materjali eraldamisega allhankeoperatsioonile kinnitate, et materjal tuleb koondada määratud ressursi ressursirühma sisendasukohta. Seejärel eraldab koondplaanimine või säästlik täiendamine materjali sellesse asukohta.  

Hankija tegevuskohas asuvate varude modelleerimiseks on valdkonna parim tava määratleda hankija hallatav ladu. Hankija hallatava lao saab hõlpsasti määratleda, luues uue lao ja määrates hankija konto. Dokumenteerimiseks, et materjal tuleb enne operatsiooni tegemist hankijale edastada, tuleb määrata hankija hallatav ladu ressurssi sisaldava ressursigrupi sisendlaoks.  

Materjali lisamiseks sellesse lattu võite kasutada mitut strateegiat.

-   Üleviimistellimused
-   Töölehtede ülekandmine
-   Kanbani väljaminek
-   Otsene ost hankija asukohta

Pooltoote on selle reegli erand. Pooltoodete üleviimiseks on ainult järgmised võimalused.

-   Tootmise ja partiitellimuste puhul saab pooltooteid viia üle ainult loogiliselt, kasutades loendilehe **Allhanketöö** töölehte Komplekteerimisleht. See tööleht koostab tarneteate dokumendi, mida saab kasutada pooltoodete ja tooraine edastamiseks hankijale.
-   Allhankeoperatsioonide puhul tootmisvoogudes dokumenteeritakse pooltoodete üleviimine tootmise kanbanide väljavõtmise kviitungiga hankija tegevuskohas. Otsese üleviimistegevuse modelleerimiseks võite lõpetada tootmise kanbani täiendava üleviimistegevusega.

**Märkus.** Ühe tootmistellimuse tootmisprotsess ei või hõlmata mitut laoala. See reegel kehtib ka allhanketöö puhul. Seetõttu tuleb hankija hallatava materjali asukohti kajastavad laod määratleda samal laoalal, kus asuvad selles protsessis kasutatavad sisemised ressursid. Kuigi tootmisvood võivad hõlmata mitut laoala, ei saa need pooltooteid ühelt laoalalt teisele transportida, kuna see toiming viitab kulukonteksti muutumisele.  

Tavaliselt on väljundladu ja allhanke ressursigrupi asukoht määratud otse protsessi või tootmisvoo operatsiooni järgmisse etappi. Selline seadistus aitab vähendada tööde registreerimist või täiendavate üleviimisoperatsioonide arvu, mida tuleb modelleerida.



