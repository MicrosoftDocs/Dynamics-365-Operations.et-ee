---
title: Tellimuse teatiste kuvamine kassas
description: Selles teemas kirjeldatakse tellimuse teatiste kuvamist kassas ja teatiste raamistikku, mida saab laiendada ka muudele toimingutele.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.search.scope: 
ms.search.region: Global
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: ec6cb212766dd90fa9db7719a2119419ecb935c7
ms.openlocfilehash: aea36591a81f727059e37a958efa62a9ebde9d9d
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2017

---

# <a name="display-notifications-in-point-of-sale"></a>Teatiste kuvamine kassas

Tänapäevases jaemüügikeskkonnas on kaupluse töötajatele määratud mitmesuguseid ülesandeid, näiteks klientide abistamine, kannete sisestamine, laoinventuuri tegemine ja kaupluses tellimuste vastuvõtmine. Kassa klientrakendus toetab töötajaid nende ülesannete täitmisel ja palju muu juures, tehes kõike seda ühes rakenduses. Päeva jooksul mitmete ülesannete täitmisel on töötajaid vaja teavitada, kui miski nõuab nende tähelepanu. Kassa teatiste raamistik lahendab selle probleemi, võimaldades jaemüüjatel konfigureerida rollipõhiseid teatisi. Dynamics 365 for Retail rakendusevärskendusega 5 võimaldab neid teatisi konfigureerida ainult kassatoimingutele.

Praegu võimaldab süsteem kuvada teatisi tellimuse täitmise toimingute puhul, kuid raamistik on kujundatud laiendatavana, seega tulevikus saavad arendajad kirjutada teatise mis tahes toimingu jaoks ja kuvada teatised kassas.  

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Teatiste lubamine tellimuse täitmise toimingute puhul

Teatiste lubamiseks tellimuse täitmise toimingute puhul vaadake järgmisi etappe.

 - Avage leht **Operations** (**Jaemüük** > **Kanali seadistus** > **Kassa seadistus** > **Kassa** > **Toimingud**).
 - Otsige tellimuse täitmise toimingut ja märkige selle toimingu ruut **Luba teatised**. See annab teatiste raamistikule korralduse kuulata tellimuse täitmise toimingu ohjurit. Ohjuri rakendamisel kuvatakse teatised kassas, muidu teatisi selle toimingu puhul ei kuvata.
- Avage töötajatega seostatud kassaload ja lisage kiirkaardil **Teatised** tellimuse täitmise toiming, märkides suvandi Kuvamisjärjestus väärtuseks 1. Kui konfigureeritud on rohkem kui üks teatis, kasutatakse kuvamisjärjestust teatiste korraldamiseks ülalt alla, nii et 1 asub ülal. Lisada saab ainult neid toiminguid, mille puhul on ruut **Luba teatised** märgitud. Samuti kuvatakse teatised ainult nende toimingute puhul, mis on lisatud siin, ja ainult neile töötajatele, kelle puhul on toimingud lisatud vastavatele kassaõigustele. 

> [!NOTE]
> Teatisi saab tühistada kasutajatasemel, minnes töötaja kirjesse, valides suvandi **Kassaload** ja seejärel redigeerides selle kasutaja teatiste tellimust.

 - Avage leht **Funktsionaalsusprofiil** (**Jaemüük** > **Kanali seadistus** > **Kassa seadistus** > **Kassaprofiilid** > **Funktsionaalsusprofiilid**). Värskendage atribuuti **Teatise intervall**, määrates minutites intervalli, mille järel teatisi tuleb tõmmata. Soovitame seada selle väärtuseks 10 minutit, et vältida ebavajalikku sidet peakontoriga. Teatise intervalli seadmine väärtusele 0 lülitab teatised välja.  

 - Minge jaotisse **Jaemüük** > **Jaemüügi IT** > **Jaotusgraafik**. Valige teatiste tellimuse sätete sünkroonimiseks graafik 1060-töötajad ja siis klõpsake käsku **Käivita kohe**. Seejärel sünkroonige loa intervall, valides suvandi 1070-kanali konfiguratsioon, ja seejärel klõpsake käsku **Käivita kohe**. 

## <a name="view-notifications-in-pos"></a>Teatiste kuvamine kassas

Kui ülaltoodud etapid on tehtud, saavad töötajad, kelle jaoks on teatised seadistatud, vaadata teatisi kassas. Teatiste kuvamiseks klõpsake kassa tiitliribal teatiseikooni. See kuvab teatisekeskuse koos teatistega tellimuse täitmise toimingu jaoks. Teatisekeskus peaks kuvama tellimuse täitmise toimingus järgmised grupid. 

- **Ootel tellimused** – selles grupis kuvatakse ootel olekuga tellimuste arv, näiteks tellimused, mille peab aktsepteerima kaupluse tellimuse täitmiseks vajalike õigustega kassatöötaja. Grupis numbril klõpsamine avab lehe **Tellimuse täitmine**, mis on filtreeritud kuvama ainult kauplusele tellimuse täitmiseks määratud ootel tellimusi. Kui tellimused on kaupluse puhul automaatselt aktsepteeritud, on selle grupi arv null.

- **Kauplusest kättesaamine** – selles grupis kuvatakse tellimuste arv, mille tarneviis on **Kättesaamine** ja kättesaamine on planeeritud praegusse kauplusse. Grupis numbril klõpsamine avab lehe **Tellimuse täitmine**, mis on filtreeritud kuvama aktiivseid tellimusi, mis on seadistatud kätte saama praegusest kauplusest.

- **Kauplusest lähetamine** – selles grupis kuvatakse tellimuste arv, mille tarneviis on **Lähetamine** ja lähetamine on planeeritud praegusest kauplusest. Grupis numbril klõpsamine avab lehe **Tellimuse täitmine**, mis on filtreeritud kuvama aktiivseid tellimusi, mis on seadistatud lähetama praegusest kauplusest.

Kui kauplusele on täitmiseks määratud uusi tellimusi, muutub teatiseikoon, näidates uute teatiste olemasolu, ja vastavate gruppide arvu värskendatakse. Kasutaja saab ka klõpsata värskendamisikoonil, mis asub toimingu nime kõrval, et gruppide arvu kohe värskendada. Arvu värskendatakse ka eelmääratletud intervalliga. Igas grupis, milles on mõni uus kaup, mida praegune töötaja pole näinud, kuvab plahvatusikooni, näidates, et selles grupis on uus kaup. Teatistes paanide klõpsamine avab konkreetse toimingu, mille jaoks see teatis on konfigureeritud. Ülaltoodud stsenaariumide korral avab teatiste klõpsamine lehe **Tellimuse täitmine** ja edastatakse asjakohased parameetrid: ootel tellimused, kauplusest kättesaamine ja kauplusest lähetamine. 

> [!NOTE]
> Ootel tellimuste teatised lubatakse rakenduse Dynamics 365 for Retail tulevases värskendused. 


