---
title: Topeltkirjutuse ülevaade
description: See artikkel annab ülevaate topeltkirjutuse kohta, mis annab reaalajas lähedalasuvad suhtlused kliendikogemuse rakenduste ning finantside ja toimingute rakenduste vahel.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 599cfdab8232cab28c59c5098094c4afd351df77
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112390"
---
# <a name="dual-write-overview"></a>Topeltkirjutuse ülevaade

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Mis on topeltkirjutus?

Topeltkirjutus on boksist väljas infrastruktuur, mis pakub reaalajas lähedalasulist suhtlust kliendikogemuse rakenduste ning finantside ja toimingute rakenduste vahel. Kui andmed klientide, toodete, inimeste ja operatsioonide kohta liiguvad rakenduse piiridest välja, omavad organisatsiooni kõik osakonnad võimalust.

Topeltkirjutus võimaldab rangelt kahesuunalist integratsiooni finantside ja operatsioonide rakenduste ning rakenduste vahel Dataverse. Kõik finantside ja toimingute rakenduste andmemuutused põhjustavad kirjutamist Dataverse Dataverse ja mis tahes andmete muutus põhjustab finantside ja toimingute rakenduste kirjutamist. See automatiseeritud andmevoog pakub rakenduste vahel integreeritud kasutuskogemust.

![Andmete seos rakenduste vahel.](media/dual-write-overview.jpg)

Topeltkirjutusel on kaks aspekti: *taristu* aspekt ja *rakenduse* aspekt.

### <a name="infrastructure"></a>Taristu

Topeltkirjutuse taristu on laiendatav ja usaldusväärne ning sisaldab järgmisi põhifunktsioone.

+ Sünkroonne ja kahesuunaline andmeedastus rakenduste vahel
+ Sünkroonimine koos esituse, peatamise ja järele jõudmise režiimidega, et toetada süsteemi veebipõhiste ja veebiväliste/asünkroonsete režiimide ajal.
+ Võime sünkroonida algandmeid rakenduste vahel
+ Tegevuse ja vigade logide kombineeritud vaade andmete administraatoritele
+ Võime konfigureerida kohandatud teatisi ja lävendeid ning tellida teatisi
+ Intuitiivne kasutajaliides (UI) filtreerimiseks ja teisendusteks
+ Võime määrata ja kuvada tabeli sõltuvusi ja seoseid
+ Laiendatavus nii standardsete kui ka kohandatud tabelite ja kaartide jaoks
+ Usaldusväärne rakenduse elutsükli haldus
+ Valmiskujul seadistuse kogemus uutele klientidele

### <a name="application"></a>Avaldus

Topeltkirjutusega luuakse finantside ja toimingute rakenduste mõistete ja kliendi kaasamise rakenduste mõistete vaheline vastendus. See integratsioon toetab järgmisi stsenaariumeid.

+ Integreeritud kliendi koondandmed
+ Juurdepääs kliendi kliendikaartidele ja preemiapunktidele
+ Ühendatud tooteetaloni kasutusfunktsionaalsus
+ Organisatsiooni hierarhia teadlikkus
+ Integreeritud hankija koondandmed
+ Juurdepääs finantsilistele ja maksude viiteandmetele
+ Nõudmisel hinnakujunduse mootori kogemus
+ Integreeritud potentsiaalse kliendi sularaha kogemus
+ Võime teenindada nii majasiseseid varasid kui ka väliagentide kaudu kliendi varasid
+ Integreeritud maksmiseks hankimise kogemus
+ Kliendiandmetele ja dokumentide integreeritud tegevused ja märkused
+ Võimalus otsida vabade varade saadavust ja üksikasju
+ Projektist sularahaks kogemus
+ Võime käsitseda osapoole kontseptsiooni kaudu mitut aadressi ja rolli


## <a name="top-reasons-to-use-dual-write"></a>Topeltkirjutuse kasutamise peamised põhjused

Topeltkirjutus võimaldab Microsoft Dynamics 365 rakenduste üleselt andmete integreerimist. See jõuline raamistik ühendab keskkondasid ja võimaldab erinevatel ärirakendustel koos töötada. Siin on peamised põhjused, miks peaksite topeltkirjutust kasutama.

+ Topeltkirjutus pakub tihedalt ühendatud, peaaegu reaalajas ja kahesuunalist integratsiooni finants- ja tegevusrakenduste ja kliendikaasamise rakenduste vahel. See integratsioon muudab Microsoft Dynamics 365 ühe peatuse poeks kõigi teie ärilahenduste jaoks. Kliendid, kes kasutavad Dynamics 365 Finance'i Dynamics 365 Supply Chain Management ja, kuid kes kasutavad kliendisuhete halduseks (CRM) Mitte-Microsofti lahendusi, teisaldavad Dynamics 365 poole oma topeltkirjutuse toe saamiseks.
+ Klientide, toodete, operatsioonide, projektide ja asjade Interneti (IoT) andmed voolavad automaatselt topeltkirjutuse kaudu teenusesse Dataverse. See ühendus on kasulik ettevõtetele, kes on huvitatud Power Platformi laiendustest.
+ Topeltkirjutuse infrastruktuur järgib puuduva koodi / vähese koodi põhimõtet. Standardsete tabelist tabelisse kaartide laiendamiseks ja kohandatud kaartide kaasamiseks on vajalik minimaalne projekteerimise panus.
+ Topeltkirjutus toetab nii ühendusega režiimi kui ka võrguühenduseta režiimi. Microsoft on ainus ettevõte, mis pakub ühendusega ja võrguühenduseta režiimide tuge.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Mida tähendab topeltkirjutus klientide kaasamise rakenduste arendajate ja arhitektide jaoks?

Topeltkirjutusega automatiseerib andmevoog finantside ja toimingute rakenduste ja kliendi kaasamise rakenduste vahel. Topeltkirjutamine koosneb kahest AppSource'i lahendusest, mis on installitud Dataverse'isse. Lahendused laiendavad Dataverse’i tabeli skeemi, lisandmooduleid ja töövooge, et neid saaks sobitada ERP suurusega. Eduka rakenduse jaoks peavad kliendi kaasamise rakenduste arendajad ja arhitektid neid muudatusi mõista ja tegema koostööd finantside ja toimingute rakendustes teiste partneritega.

Paarsuse loomiseks finantside ja toimingute rakendustega teeb topeltkirjutus skeemis mõned olulised Dataverse muudatused. Kui te seda plaani mõistate, saate tulevikus vältida mõnda kujundamise ja arendamisega seotud taastöötlust.

+ Kui AppSource'i topeltkirjutamisega pakett on installitud, on Dataverse'il uued mõisted (nt ettevõte ja osapool). Need mõisted Dataverse aitavad rajatud rakendusi, sh Dynamics 365 Müük, Dynamics 365 Marketing, Dynamics 365 Customer Service, Dynamics 365 Field Service ja, et suhelda sujuvalt finantside ja toimingute rakendustega.

+ Tegevused ja märkmed on ühtlustatud ning laiendatud, et toetada nii C1-sid (süsteemi kasutajaid) kui ka C2-sid (süsteemi kliendid).

+ Et vältida andmekadu Dataverse valuuta edastamisel finantside ja toimingute rakenduste ning rakenduste vahel, on teil võimalik klientide rakenduste valuuta andmetüübis kümnendkohti suurendada. Funktsioon teisendab metaandmete kihis olemasolevad read uude laiendatud olekusse automaatselt. Selle protsessi käigus teisendatakse valuuta väärtus raha andmetüübi asemel kümnendkoha andmetüübiks ja valuuta väärtus toetab 10 kümnendkohta. See funktsioon on valikuline ja organisatsioonid, kes ei vaja rohkem kui nelja kümnendkohta, ei pea seda kasutama. Lisateavet vt [Valuuta andmetüübi migratsioon topeltkirjutamise jaoks](currrency-decimal-places.md).

+ [Kuupäeva jõustumine](../../dev-tools/date-effectivity.md) lisatakse Dataverse'isse. See toetab samas tabelis mineviku, oleviku ja tuleviku andmeid.

+ Toodete, pakkumiste, tellimuste ja arvete korral toetatakse toote [ühiku teisendusi](../../../../supply-chain/pim/tasks/manage-unit-measure.md).

Lisateavet eelseisvate muudatuste kohta leiate teemast [Mis on uut või mida on muudetud topeltkirjutuses?](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

