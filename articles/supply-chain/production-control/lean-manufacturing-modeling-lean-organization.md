---
title: Efektiivse organisatsiooni modelleerimine
description: Artiklis antakse teavet efektiivse organisatsiooni mudeldamise põhimõistete kohta.
author: cvocph
manager: tfehr
ms.date: 09/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33e734aef938c7b58d5c936f6eae32e4f0ab3ba7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211441"
---
# <a name="modeling-a-lean-organization"></a>Efektiivse organisatsiooni modelleerimine

[!include [banner](../includes/banner.md)]

Artiklis antakse teavet efektiivse organisatsiooni mudeldamise põhimõistete kohta. 

Lean manufacturingi stsenaarium on tavaliselt enamat kui seosetute kanban-reeglite või materjali tarnepoliitikate kogum. Materjali ja toodete voogu läbi kindla tootmis- või tarnimisstsenaariumi töörakkude ja asukohtade võib kirjeldada järgnevusena või protsessi või ülekandetegevuste väikese võrgustikuna. Seda seeriat või võrku nimetatakse tootmisvooks.

## <a name="production-flows-in-lean-manufacturing"></a>Tootmisvood lean manufacturingis
Tootmistellimustel põhinevate tootmisstsenaariumide puhul väljastatakse materjal kindlale tootmistellimusele. Kooslustel ja protsessidel põhinevate operatsioonijadade ajal luuakse tooted ja võetakse need vastu tarne asukohas. Tootmistellimuste läbilaskeaeg võib erineda ja jääda vahemikku minutitest nädalateni. Kõik seotud kulud, materjalid ja tööjõud kogutakse tootmistellimusse. 

Partii tootmise põhjustatud tarne täitmisaegade lühendamiseks ja laotasemete ülejääkide vähendamiseks töökeskuste vahel tutvustab lean manufacturing kanbani täiendamist ning lõppladusid tootmise ja lao täiendamisel. Tavaliselt häirivad need funktsioonid osaliselt sõltumatute kanban-tsüklite tootmist. Kanbani täiendamist pooltootele ei käivita enam lõpptoote tellimus. 

Soovitatud erinevatele kanbani stsenaariumidele tootmise ja kulude konteksti taastamiseks võetakse tegevuspõhised tootmisvood kasutusse lean manufacturingi selgroona. Kõik kanban-reeglid viitavad sellele eelmääratletud struktuurile. Tegevuspõhine mudel toetab suure valiku stsenaariumide seadistamist. Kuid see mudel ei lisa keerukust tegevtöötajatele, sest kõik stsenaariumid kasutavad sama tegevuspõhist kasutajaliidest.

## <a name="semi-finished-products-non-bom-levels"></a>Pooltooted (mitte kooslusetasemed)
Lean manufacturing integreerib kanbanid ühes raamistikus laotoodeteks ja pooltoodeteks ja pakub seega igal juhul ühendatud kasutajakogemust. Selle ülesehituse tõttu ei pea enam kasutama täiendavaid kooslusetasemeid, et lubada pooltoodete puhul kasutatavaid kanbane. See ülesehitus aitab ka vähendada laokandeid miinimumini.

## <a name="products-and-material-in-work-in-progress"></a>Tooted ja materjal lõpetamata toodangus
Partii suuruse vähendamine lean manufactoringi ühe tüki voo ideaalsesse olekusse võib põhjustada laokannete olulise kasvu, kui iga komplekteerimisprotsess või kanbani registreerimine põhjustab tarbitud kaupade kandeid. Tootmisvoo arhitektuur lubab matrejalide üleviimist tootmisvoogu tagastamiskanbanidega laos või transpordi käsitlemise üksuste suurustes. Väljastatud materjali väärtus lisatakse tootmisvooga seotud poolelioleva toodangu (WIP) kontole. See sarnaneb tootmistellimusele väljastatava materjali toimimisele. Sama põhimõtet saab rakendada toodete ja pooltoodete puhul. Kui neid tooteid ei looda, ei kanta üle ega tarbita tootmisvoos, on need valikulised. Kui tooted sisestatakse varudesse, vähendatakse tootmisvoo WIP-kontot, arvates maha seotud standardne hind.

## <a name="value-streams-and-value-stream-mapping"></a>Väärtuse vood ja väärtuste voo vastendamine
Lean manufacturingi arhitektuur on inspireeritud 5 Leani põhimõttest, mille on sõnastanud Womack ja Jones: kliendi väärtus, väärtuse voog, voog, tõmbamine ja täiuslikkus. Üks kinnitatud meetod lean manufacturingi lahenduste juurutamiseks reaalses tootmismaailmas on väärtuse voo vastendamine (VSM). Seda meetodit tutvustasid Rother ja Shook oma väljaandes „Learning to See” Lean Manufacturingi instituudis. 

Tulevase oleku väärtuse voogu saab mudeldada tootmisvoo versioonina. Kõik väärtuse oo protsessid mudeldatakse protsessi tegevustena. Liikumisi või kandeid saab mudeldada ülekandetegevustena, kui ülekande olek peab olema registreeritud või kui nõutav on integreerimine varude komplekteerimiseks või konsolideeritud saadetisteks. 

Väärtuse voog ise on mudeldatud tootmisüksusena. Seetõttu saab väärtuse voogu kasutada finantsdimensioonina.

Lisateavet tootmisüksuste loomise kohta vt teemast [Tootmisüksuse loomine](../../fin-and-ops/organization-administration/tasks/create-operating-unit.md).

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Lean manufacturingi jaoks kuluarvutuste tegemine tootmisvoo alusel
Tootmisvoo kulu perioodiline konsolideerimine parandab seotud WIP-konto ja lubab hälvete määratlemise toodetele , mida pakub tootmisvoog.

## <a name="continuous-improvement"></a>Pidevad parandused
Pidevate paranduste paremini toetamiseks juurutatakse tootmisvoogusid ajatõhusates versioonides. Seetõttu saab olemasoleva tootmisvoo versiooni koos kõigi seotud kanban-reeglitega kopeerida tootmisvoo tulevasse versiooni. Lisaks saab tulevase oleku tootmisvoogu muuta enne selle kinnitamist ja aktiveerimist tootmiseks. Olemasolevad kanbanid vanast tootmisvoo versioonist seotakse automaatselt uue verisooniga, et tagada sujuv materjalide voog siirde kuupäeval ja edaspidi.

## <a name="simplicity"></a>Lihtsus
Lean manufacturingi juurutamisel valime tootmisvoo ja tegevuse lähenemise, mis võimaldab lihtsate ja keeruliste tootmisstsenaariumite modelleerimist ühes skaleeritavas arhitektuuris. Tegevuse kontseptsiooni lähem vaatlus paljastab uue lihtsuse neile, kes seda tõesti vajavad: tööde juhtijatele ja logistikatöötajatele. Laokannete asemel tegevuspõhistest töödest teavitades kannab kõikide lean manufacturingi variantide ühine kasutajaliides äri keerukuse kasutajaliidesest üle sinna, kuhu see kuulub: tootmisvoog lean manufacturingi selgroona.



