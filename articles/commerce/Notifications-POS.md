---
title: Kassa tellimuse teatiste kuvamine
description: Selles teemas kirjeldatakse tellimuse teatiste kuvamise lubamist kassas ja teatiste raamistikku.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: c3b8e2774a189f2afefa757e7c4f3885b674918c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976784"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Kassa tellimuse teatiste kuvamine

[!include [banner](includes/banner.md)]

Modernses jaemüügikeskkonnas on kaupluse töötajatele määratud mitmesuguseid ülesandeid, näiteks klientide abistamine, kannete sisestamine, laoinventuuri tegemine ja kaupluses tellimuste vastuvõtmine. Kassa klient pakub üht rakendust, kus töötajad saavad täita kõiki neid ülesandeid ja palju muud. Kuna päeva jooksul tuleb täita erinevaid ülesandeid, võib juhtuda, et töötajaid tuleb teavitada, kui miski nõuab nende tähelepanu. Kassa teatiste raamistik võimaldab jaemüüjatel konfigureerida rollipõhiseid teatisi. Alates Dynamics 365 for Retaili rakendusevärskendusest 5 on neid teatisi võimalik konfigureerida ainult kassatoimingutele.


Praegu saab süsteem kuvada teatisi ainult tellimuse täitmise toimingute korral. Kuid kuna raamistik on kujundatud laiendatavana, saavad arendajad edaspidi kirjutada teatiseohjuri mis tahes toimingu jaoks ja kuvada selle toimingu teatised kassas.

## <a name="enable-notifications-for-order-fulfillment-operations"></a>Teatiste lubamine tellimuse täitmise toimingute puhul

Teatiste lubamiseks tellimuse täitmise toimingute puhul järgige järgmisi etappe.

1. Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Toimingud**.
2. Otsige toimingut **Tellimuse täitmine** ja valige märkeruut **Teatiste lubamine**, et määratleda, et teatiste raamistik peab selle toimingu korral ohjurit kuulama. Kui ohjur on juurutatud, kuvatakse selle toimingu teatised kassas.
3. Avage **Jaemüük ja kaubandus** &gt; **Töövõtjad** &gt; **Töötajad** &gt; ning vahekaardil Commerce avage töötajaga seotud kassaload. Laiendage kiirkaarti **Teatised**, lisage toiming **Tellimuse täitmine** ja seadistage väli **Kuvamisjärjestus** väärtusele **1**. Kui konfigureeritud on mitu teatist, kasutatakse seda välja teatiste korraldamiseks. Teatised, millel on madalam **kuvamisjärjestuse** väärtus, kuvatakse suurema väärtusega teatiste kohal. Teatised, mille **kuvamisjärjestuse** väärtus on **1**, on kõige kõrgemal.

    Teatised kuvatakse ainult toimingute jaoks, mis on lisatud kiirkaardile **Teatised** ja te saate toiminguid sinna lisada ainult siis, kui lehel **Kassatoimingud** on nende toimingute jaoks valitud märkeruut **Luba teatised**. Lisaks kuvatakse toimingu teatisi töötajatele ainult siis, kui vastav toiming on lisatud nende töötajate kassalubadesse.

    > [!NOTE]
    > Teatisi saab kasutaja tasemel alistada. Avage töötaja kirje, valige **kassaload** ja redigeerige seejärel kasutaja teatise tellimust.

4. Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassaprofiilid** &gt; **Funktsiooniprofiilid**. Väljal **Teatise intervall** määrake, kui tihti teatisi tuleb kuvada. Mõne teatise puhul peab kassa tegema kontorirakendusse reaalajas kõnesid. Need kõned kulutavad kontorirakenduse arvutusmahtu. Seetõttu soovitame teatise intervalli määramisel arvestada nii teie ärivajadustega kui ka reaalajas kõnede mõjuga kontorirakendusele. Väärtus **0** (null) lülitab teatised välja.
5. Avage **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafik**. Valige teatise tellimuse sätete sünkroonimiseks graafik **1060** (**personal**) ja siis valige **Käivita kohe**. Seejärel valige loa intervalli sünkroonimiseks graafik **1070** (**kanali konfigureerimine**) ja seejärel valige **Käivita kohe**.

## <a name="view-notifications-in-the-pos"></a>Teatiste kuvamine kassas

Pärast eelnevate etappide lõpule viimist saavad töötajad kassas teatisi vaadata. Teatiste kuvamiseks vajutage kassa üleval paremas nurgas teatiseikooni. Kuvatakse teatisekeskuses koos teatistega tellimuse täitmise toimingu jaoks. Teatisekeskus peaks kuvama tellimuse täitmise toimingus järgmised grupid.

- **Kauplusest kättesaamine** – selles grupis kuvatakse tellimuste arv, mille tarneviis on **Kättesaamine** ja mille kättesaamine on planeeritud praegusest kauplusest. Saate vajutada grupis oleval numbril, et avada leht **Tellimuse täitmine**. Sel juhul filtreeritakse leht kuvama ainult aktiivseid tellimusi, mille kättesaamine on seadistatud praegusest kauplusest.
- **Kauplusest lähetamine** – selles grupis kuvatakse tellimuste arv, mille tarneviis on **Lähetamine** ja lähetamine on planeeritud praegusest kauplusest. Saate vajutada grupis oleval numbril, et avada leht **Tellimuse täitmine**. Sel juhul filtreeritakse leht kuvama ainult aktiivseid tellimusi, mille lähetamine on seadistatud praegusest kauplusest.

Kui kauplusele määratakse täitmiseks uusi tellimusi, muutub teatiseikoon, näidates uute teatiste olemasolu, ja vastavate gruppide arvu värskendatakse. Kuigi gruppe värskendatakse kindlate ajavahemike järel, saavad kassa kasutajad gruppe igal ajal käsitsi värskendada, valides grupi kõrval nupu **Värskenda**. Lõpuks, kui grupis on uus kaup, mida praegune töötaja pole näinud, kuvatakse plahvatusikoon, mis näitab, et selles grupis on uus kaup.

## <a name="enable-live-content-on-pos-buttons"></a>Reaalajas sisu lubamine kassa nuppudel

Kassa nupud saavad nüüd kuvada arvu, mis võimaldab töötajatel hõlpsalt näha, millised ülesanded vajavad viivitamatut tähelepanu. Selle arvu kuvamiseks kassa nupul peate lõpule viima eelnevalt selles teemas kirjeldatud teatise seadistamise (st, peate lubama toimingu teavitused, seadistama teatise intervalli ja uuendama töötaja kassaloa gruppi). Lisaks peate avama nupupaneeli koostaja, vaatama nupu atribuute ja valima märkeruudu **Luba reaalajas sisu**. Väljal **Sisu joondamine** saate valida, kas arv kuvatakse nupu parempoolses ülemises nurgas (**Üleval paremal**) või keskel (**Keskel**).

> [!NOTE]
> Reaalajas sisu saab lubada toimingute jaoks ainult juhul, kui nende jaoks on lehel **Kassatoimingud** valitud märkeruut **Teatiste lubamine**, nagu kirjeldati selles teemas eespool.

Järgmine joonis näitab reaalajas sisu sätteid nupupaneeli koostajas.

![Reaalajas sisu sätted nupupaneeli koostajas](./media/ButtonGridDesigner.png "Reaalajas sisu sätted nupupaneeli koostajas")

Nupul teatiste arvu kuvamiseks peate veenduma, et uuendatakse õiget ekraani paigutust. Kassa kasutatava ekraani paigutuse määramiseks valige ülemises parempoolses nurgas ikoon **Sätted** ja märkige **Ekraani paigutuse ID** ja **Paigutuse eraldusvõime** Kasutades brauserit Edge, minge lehele **Ekraani paigutus**, leidke ülal tuvastatud **Ekraani paigutuse ID** ja **Paigutuse eraldusvõime** ning valige märkeruut **Luba reaalajas sisu**. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik** ja käivitage töö 1090 (registrid), et sünkroonida paigutuse muudatused.


![Kassa kasutatava ekraani paigutuse leidmine](./media/Choose_screen_layout.png "Ekraanipaigutuse otsing")

Järgmisel joonisel on näidatud, mis on vahet valikul **Üleval paremal** ja **Keskel** väljal **Sisu joondamine** erinevates suurustes nuppude korral.

![Reaalajas sisu kassa nuppudel](./media/ButtonsWithLiveContent.png "Reaalajas sisu kassa nuppudel")


[!INCLUDE[footer-include](../includes/footer-banner.md)]