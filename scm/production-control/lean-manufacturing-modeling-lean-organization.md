---
title: Efektiivse organisatsiooni modelleerimine
description: "Artiklis antakse teavet efektiivse organisatsiooni mudeldamise põhimõistete kohta."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 53141
ms.assetid: 4f272f2f-ec2c-4b0d-a652-00a63b719b9e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 9262dcaa3b326d8c31b7d7416b102920795da94b
ms.openlocfilehash: c5bb642df692451e975be74bd8aa7d856b964a68
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="modeling-a-lean-organization"></a>Efektiivse organisatsiooni modelleerimine

[!include[banner](../includes/banner.md)]


Artiklis antakse teavet efektiivse organisatsiooni mudeldamise põhimõistete kohta. 

Lean manufacturingi stsenaarium on tavaliselt enamat kui seosetute kanban-reeglite või materjali tarnepoliitikate kogum. Materjali ja toodete voogu läbi kindla tootmis- või tarnimisstsenaariumi töörakkude ja asukohtade võib kirjeldada järgnevusena või protsessi või ülekandetegevuste väikese võrgustikuna. Seda seeriat või võrku nimetatakse tootmisvooks.

## <a name="production-flows-in-lean-manufacturing"></a>Tootmisvood lean manufacturingis
Tootmistellimustel põhinevate tootmisstsenaariumide puhul väljastatakse materjal kindlale tootmistellimusele. Kooslustel ja protsessidel põhinevate operatsioonijadade ajal luuakse tooted ja võetakse need vastu tarne asukohas. Tootmistellimuste läbilaskeaeg võib erineda ja jääda vahemikku minutitest nädalateni. Kõik seotud kulud, materjalid ja tööjõud kogutakse tootmistellimusse. 

Partii tootmise põhjustatud tarne täitmisaegade lühendamiseks ja laotasemete ülejääkide vähendamiseks töökeskuste vahel tutvustab lean manufacturing kanbani täiendamist ning lõppladusid tootmise ja lao täiendamisel. Tavaliselt häirivad need funktsioonid osaliselt sõltumatute kanban-tsüklite tootmist. Kanbani täiendamist pooltootele ei käivita enam lõpptoote tellimus. 

Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni soovitatud erinevatele kanbani stsenaariumidele tootmise ja kulude konteksti taastamiseks võetakse tegevuspõhised tootmisvood kasutusse lean manufacturingi selgroona. Kõik kanban-reeglid viitavad sellele eelmääratletud struktuurile. Tegevuspõhine mudel toetab suurema hulga stsenaariumide seadistamist kui eelmised Dynamics AX-i toetatud Lean manufacturingi versioonid. Kuid see mudel ei lisa keerukust tegevtöötajatele, sest kõik stsenaariumid kasutavad sama tegevuspõhist kasutajaliidest.

## <a name="semi-finished-products-non-bom-levels"></a>Pooltooted (mitte kooslusetasemed)
Dynamics AX-i Lean manufacturing integreerib kanbanid ühes raamistikus laotoodeteks ja pooltoodeteks ja pakub seega igal juhul ühendatud kasutajakogemust. Selle ülesehituse tõttu ei pea enam kasutama täiendavaid kooslusetasemeid, et lubada pooltoodete puhul kasutatavaid kanbane. See ülesehitus aitab ka vähendada laokandeid miinimumini.

## <a name="products-and-material-in-work-in-progress"></a>Tooted ja materjal lõpetamata toodangus
Partii suuruse vähendamine lean manufactoringi ühe tüki voo ideaalsesse olekusse võib põhjustada laokannete olulise kasvu, kui iga komplekteerimisprotsess või kanbani registreerimine põhjustab tarbitud kaupade kandeid. Tootmisvoo arhitektuur lubab matrejalide üleviimist tootmisvoogu tagastamiskanbanidega laos või transpordi käsitlemise üksuste suurustes. Väljastatud materjali väärtus lisatakse tootmisvooga seotud poolelioleva toodangu (WIP) kontole. See sarnaneb tootmistellimusele väljastatava materjali toimimisele. Sama põhimõtet saab rakendada toodete ja pooltoodete puhul. Kui neid tooteid ei looda, ei kanta üle ega tarbita tootmisvoos, on need valikulised. Kui tooted sisestatakse varudesse, vähendatakse tootmisvoo WIP-kontot, arvates maha seotud standardne hind.

## <a name="value-streams-and-value-stream-mapping"></a>Väärtuse vood ja väärtuste voo vastendamine
Dynamics AX-i Lean manufacturingi arhitektuur on inspireeritud 5 Leani põhimõttest, mille on sõnastanud Womack ja Jones: kliendi väärtus, väärtuse voog, voog, tõmbamine ja täiuslikkus. Üks kinnitatud meetod lean manufacturingi lahenduste juurutamiseks reaalses tootmismaailmas on väärtuse voo vastendamine (VSM). Seda meetodit tutvustasid Rother ja Shook oma väljaandes „Learning to See” Lean Manufacturingi instituudis. 

Dynamics AX-is saab tulevase oleku väärtuse voogu mudeldada tootmisvoo versioonina. Kõik väärtuse oo protsessid mudeldatakse protsessi tegevustena. Liikumisi või kandeid saab mudeldada ülekandetegevustena, kui ülekande olek peab olema registreeritud või kui nõutav on integreerimine varude komplekteerimiseks või konsolideeritud saadetisteks. 

Väärtuse voog ise on Dynamics AX-is mudeldatud tootmisüksusena. Seetõttu saab väärtuse voogu kasutada finantsdimensioonina.

## <a name="costing-for-lean-manufacturing-based-on-the-production-flow"></a>Lean manufacturingi jaoks kuluarvutuste tegemine tootmisvoo alusel
Tootmisvoo kulu perioodiline konsolideerimine parandab seotud WIP-konto ja lubab hälvete määratlemise toodetele , mida pakub tootmisvoog.

## <a name="continuous-improvement"></a>Pidevad parandused
Pidevate paranduste paremini toetamiseks juurutatakse tootmisvoogusid ajatõhusates versioonides. Seetõttu saab olemasoleva tootmisvoo versiooni koos kõigi seotud kanban-reeglitega kopeerida tootmisvoo tulevasse versiooni. Lisaks saab tulevase oleku tootmisvoogu muuta enne selle kinnitamist ja aktiveerimist tootmiseks. Olemasolevad kanbanid vanast tootmisvoo versioonist seotakse automaatselt uue verisooniga, et tagada sujuv materjalide voog siirde kuupäeval ja edaspidi.

## <a name="simplicity"></a>Lihtsus
Lean manufacturingi juurutamisel Microsoft Dynamics AX-is valime tootmisvoo ja tegevuse lähenemise, mis võimaldab lihtsate ja keeruliste tootmisstsenaariumite modelleerimist ühes skaleeritavas arhitektuuris. Tegevuse kontseptsiooni lähem vaatlus paljastab uue lihtsuse neile, kes seda tõesti vajavad: tööde juhtijatele ja logistikatöötajatele. Laokannete asemel tegevuspõhistest töödest teavitades kannab kõikide lean manufacturingi variantide ühine kasutajaliides äri keerukuse kasutajaliidesest üle sinna, kuhu see kuulub: tootmisvoog lean manufacturingi selgroona.




