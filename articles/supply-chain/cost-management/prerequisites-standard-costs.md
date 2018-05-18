---
title: Standardkulude eeltingimused
description: "Selles teemas kirjeldatakse standardkulude kasutamise põhisamme."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e63f2b4289b640e601492425331ea8f3804d139a
ms.openlocfilehash: 4f505a2de89863d1a12d415795fdfb82b3557bc0
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---

# <a name="prerequisites-for-standard-costs"></a>Standardkulude eeltingimused

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse standardkulude kasutamise põhisamme. Järgmised etapid sõltuvad ettevõtte toimingutest. Näiteks erinevad need mittetöötleva keskkonna, protsesse mittekasutava töötleva keskkonna ja protsesse kasutava töötleva keskkonna puhul. 

Standardkulude seadistamiseks läbige järgmised etapid.

**1. Looge standardkuludele kauba mudeligrupp.**

Kasutage lehte **Kauba mudeligrupid** standardkuludele uue grupi loomiseks ja määrake üksuse **Standardkulu** laomudel. Kauba mudeligrupi identifikaator peab olema selgitav, nt **Std kulud**. Märkige ruudud näitamaks, et grupp peaks lubama finantsilist negatiivset laovaru ning sisestama füüsilisi ja finantsilisi laovarusid. See standardkulugrupp määratakse kaupadele.

**2. Määrake pearaamatukontod, mis vastavad standardkulu erinevustele.** 

Kasutage lehte **Kontoplaan** standardkulude erinevustele vastavate pearaamatukontode määramiseks. Need pearaamatukontod peavad olema määratud enne, kui need lehele **Sisestamine** määratakse. Pearaamatukontod võivad kajastada kaubagruppe ja kulugruppe.

**3. Määrake pearaamatukontod kaubasisestustele, mis vastavad standardkulu erinevustele.** 

Kasutage lehte **Sisestamine** standardkulu erinevustele vastavate pearaamatukontode määramiseks. Te saate erinevuste pearaamatukontod määrata kauba (või kaubagrupi) ja kulugrupi (või kulugrupi tüübi) alusel või et pearaamatukonto kohanduks kõigile kaupadele ja kulugruppidele. Need valikud vastavad kulusuhetele tabelites, gruppides ja mõlemas). 

Enne kauba sisestusreeglite määratlemist lubage lehel **Kandekombinatsioonid** kulusuhted (tabelites, gruppides ja mõlemas).

**4. Määrake standardkuludele vastavad laoparameetrid.** 

-  Kasutage lehel **Varude parameetrid** olevat vahekaarti **Kooslused**, et määrata kulujuhtimise parameetrid standardkuludele vastavate kahe parameetri määramiseks. 

    -  Valige väljalt **Kulujaotus** suvand **Puudub** või **Alammoodul**. Kui teete valiku **Alammoodul**, on kulude jaotamine*aktiivne*. Aktiivse kulu jaotamine on standardkulu kaubad mitmetasemelises tootmisstruktuuris kulugruppide segmentimise arvutamiseks, säilitamiseks ja vaatamiseks kriitiline toiming. Kui kulude jaotamine on aktiivne, saate kaubavaru, pooleliolevat tööd ja kulugrupi kohta müüdud kaupade kulu kinnitada ja analüüsida üksikul tasemel, mitmetasemeliselt või kogu vormingus. Aktiivne kulude jaotamine tähendab seda, et toodetud kauba kulu aktiveerimine põhjustab kulugrupi segmentimise talletamise kauba kulukirjes. 

    -  Kui teete valiku **Puudub**, ei säilitada standardsete kuluüksuste kulugrupi segmentimist. Teiste sõnadega, toodetud kauba standardkulu arvutatakse ja säilitatakse ühe summana ilma kulugrupi segmentimiseta. Toodetud komponentide kulupanused koondatakse üheks summaks.

-  Tehke väljal **Standardi hälbed** valikud **Summeeritud** või **Kulugrupi kohta**. Valik **Kulugrupi kohta** võimaldab tuvastada ostuhinna hälbeid ja tootmise hälbeid kulugruppide kaupa. Samuti saate tuvastada nelja tüüpi tootmishälbeid: partii suuruse, koguse-, hinna- ja asendushälbeid. Kui tegite valiku **Summeeritud**, ei saa te tuvastada hälbeid kulugrupi alusel ega nelja tüüpi tootmishälbeid. Te saate vaadata vaid summeeritud tootmiskulude hälbeid.

-  Standardi erinevuspoliitika töötab kulujaotumise poliitikast sõltumatult. Teiste sõnadega saate valida kulude jaotumise poliitika üksuse **Puudub** kohta, samuti saate valida erinevused kulugrupi alusel, nii et kulugrupi tootmiskulude hälbed hõlmatakse ikkagi.

**5. Looge standardkulude kuluversioonid.** 

Kasutage lehte **Kuluarvutuse versiooni seadistus**, et luua üks või mitu standardkulude kuluversiooni. Iga kuluversioon peab olema määratud kulutüübiga **Standardkulud** ja võimaldama sisul kuluandmeid lisada.

**6. Valmistage standardkulude kasutamiseks ette olemasolev klient.** 

Kliendid, kes soovivad oma olemasolevaid kaupu muuta standardkulu laomudeliks peavad kasutama lehte **Standardkulu teisendused**.


<a name="related-topics"></a>Seotud dokumendid
--------

[Standardomahinna teisendamise ülevaade](standard-cost-conversion-overview.md)


