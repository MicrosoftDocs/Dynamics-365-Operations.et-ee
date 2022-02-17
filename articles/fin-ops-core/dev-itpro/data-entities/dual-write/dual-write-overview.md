---
title: Topeltkirjutuse ülevaade
description: See teema annab ülevaate kahekordsest kirjutamisest, mis pakub peaaegu reaalajas suhtlust klientide kaasamise rakenduste ja Finance and Operationsi rakenduste vahel.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f39322a0c2ef50ef2bbeb256c80096e0687c4642
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061330"
---
# <a name="dual-write-overview"></a>Topeltkirjutuse ülevaade

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Mis on topeltkirjutus?

Kahekordne kirjutamine on kasutusel olev infrastruktuur, mis pakub peaaegu reaalajas suhtlust klientide kaasamise rakenduste ja Finance and Operationsi rakenduste vahel. Kui andmed klientide, toodete, inimeste ja operatsioonide kohta liiguvad rakenduse piiridest välja, omavad organisatsiooni kõik osakonnad võimalust.

Kahekordne kirjutamine tagab tihedalt seotud kahesuunalise integratsiooni Finance and Operationsi rakenduste ja Dataverse. Kõik andmemuudatused Finance and Operationsi rakendustes põhjustavad kirjutusi Dataverse ja mis tahes andmete muudatused Dataverse põhjustab Finance and Operationsi rakendustesse kirjutamisi. See automatiseeritud andmevoog pakub rakenduste vahel integreeritud kasutuskogemust.

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

Kahekordne kirjutamine loob vastendamise kontseptsioonide vahel Finance and Operationsi rakendustes ja kontseptsioonide vahel klientide kaasamise rakendustes. See integratsioon toetab järgmisi stsenaariumeid.

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

+ Topeltkirjutus pakub tihedalt ühendatud, peaaegu reaalajas ja kahesuunalist integratsiooni finants- ja tegevusrakenduste ja kliendikaasamise rakenduste vahel. See integratsioon muudab Microsoft Dynamics 365 ühe peatuse poeks kõigi teie ärilahenduste jaoks. Kliendid, kes kasutavad rakendusi Dynamics 365 Finance ja Dynamics 365 Supply Chain Management, kuid kasutavad kliendisuhte halduseks (CRM) mitte-Microsofti lahendusi, liiguvad Dynamics 365 suunas selle topeltkirjutamise toe jaoks.
+ Klientide, toodete, operatsioonide, projektide ja asjade Interneti (IoT) andmed voolavad automaatselt topeltkirjutuse kaudu teenusesse Dataverse. See ühendus on kasulik ettevõtetele, kes on huvitatud Power Platformi laiendustest.
+ Topeltkirjutuse infrastruktuur järgib puuduva koodi / vähese koodi põhimõtet. Standardsete tabelist tabelisse kaartide laiendamiseks ja kohandatud kaartide kaasamiseks on vajalik minimaalne projekteerimise panus.
+ Topeltkirjutus toetab nii ühendusega režiimi kui ka võrguühenduseta režiimi. Microsoft on ainus ettevõte, mis pakub ühendusega ja võrguühenduseta režiimide tuge.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Mida tähendab topeltkirjutus klientide kaasamise rakenduste arendajate ja arhitektide jaoks?

Kahekordne kirjutamine automatiseerib andmevoo Finance and Operationsi rakenduste ja klientide kaasamise rakenduste vahel. Topeltkirjutamine koosneb kahest AppSource'i lahendusest, mis on installitud Dataverse'isse. Lahendused laiendavad Dataverse’i tabeli skeemi, lisandmooduleid ja töövooge, et neid saaks sobitada ERP suurusega. Edukaks rakendamiseks peavad klientide kaasamise rakenduste arendajad ja arhitektid neid muudatusi mõistma ning tegema koostööd oma partneritega Finance and Operationsi rakenduste osas.

Finance and Operationsi rakendustega võrdsuse loomiseks teeb kahekordne kirjutamine rakenduses mõned olulised muudatused Dataverse skeem. Kui te seda plaani mõistate, saate tulevikus vältida mõnda kujundamise ja arendamisega seotud taastöötlust.

+ Kui AppSource'i topeltkirjutamisega pakett on installitud, on Dataverse'il uued mõisted (nt ettevõte ja osapool). Need kontseptsioonid aitavad rakendusi üles ehitada Dataverse, sealhulgas Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service ja Dynamics 365 Field Service, et Finance and Operationsi rakendustega sujuvalt suhelda.

+ Tegevused ja märkmed on ühtlustatud ning laiendatud, et toetada nii C1-sid (süsteemi kasutajaid) kui ka C2-sid (süsteemi kliendid).

+ Andmete kadumise vältimiseks rahaülekande rakenduste Finance and Operations ja rakenduse vahel Dataverse, saate klientide kaasamise rakenduste valuutaandmete tüübi komakohtade arvu suurendada. Funktsioon teisendab metaandmete kihis olemasolevad read uude laiendatud olekusse automaatselt. Selle protsessi käigus teisendatakse valuuta väärtus raha andmetüübi asemel kümnendkoha andmetüübiks ja valuuta väärtus toetab 10 kümnendkohta. See funktsioon on valikuline ja organisatsioonid, kes ei vaja rohkem kui nelja kümnendkohta, ei pea seda kasutama. Lisateavet vt [Valuuta andmetüübi migratsioon topeltkirjutamise jaoks](currrency-decimal-places.md).

+ [Kuupäeva jõustumine](../../dev-tools/date-effectivity.md) lisatakse Dataverse'isse. See toetab samas tabelis mineviku, oleviku ja tuleviku andmeid.

+ Toodete, pakkumiste, tellimuste ja arvete korral toetatakse toote [ühiku teisendusi](../../../../supply-chain/pim/tasks/manage-unit-measure.md).

Lisateavet eelseisvate muudatuste kohta leiate teemast [Mis on uut või mida on muudetud topeltkirjutuses?](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
