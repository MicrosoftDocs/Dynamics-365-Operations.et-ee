---
title: Kassa tellimuse teatiste kuvamine
description: Selles teemas kirjeldatakse tellimuse teatiste kuvamise lubamist kassas ja teatiste raamistikku.
author: ShalabhjainMSFT
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations, RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2017-10-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: f7b28a33dff4af6bf2b97db825a5a8304213f3a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796482"
---
# <a name="show-order-notifications-in-the-point-of-sale-pos"></a>Kassa tellimuse teatiste kuvamine

[!include [banner](includes/banner.md)]

Kaupluseseostele võidakse määrata kaupluses erinevaid ülesandeid, nt tellimuste täitmine või lao vastuvõttu või laoin inventuuri sooritamine. Kassa klient pakub üht rakendust, kus töötajad saavad täita kõiki neid ülesandeid ja veel palju muud. Kassa teatiste raamistik võimaldab jaemüüjatel konfigureerida rollipõhiseid teatisi. Alustades Dynamics 365 Retail rakendusevärskendusega 5 võimaldab neid teatisi konfigureerida ainult kassatoimingutele.

Süsteem saab kuvada *tellimuse täitmise* toimingu teavitusi ja äriversiooni 10.0.18 teatisi saab näidata ka tellimuse *tagasikutsumise toimingu* korral. Kuid kuna raamistik on kujundatud laiendatavana, saavad arendajad edaspidi [kirjutada teatiseohjuri](dev-itpro/extend-pos-notification.md) mis tahes toimingu jaoks ja kuvada selle toimingu teatised kassas.

## <a name="enable-notifications-for-order-fulfillment-or-recall-order-operations"></a>Teatiste lubamine tellimuse täitmise toimingute puhul

Teatiste lubamiseks tellimuse täitmise toimingute puhul järgige järgmisi etappe.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassa \> Toimingud**.
1. Otsige toimingut **Tellimuse täitmistoiming** ja valige märkeruut **Korda tellimust** ja **Teatiste lubamine** et määratleda, et teatiste raamistik peab selle toimingu korral ohjurit kuulama. Kui ohjur on juurutatud, kuvatakse selle toimingu teatised kassas.
1. Avage **Jaemüük ja kaubandus \> Töövõtjad \> Töötajad**.
1. Valige **Äri** vahekaart, valige töötaja rida ja seejärel valige **kassaload**. Valige **teavituste** kiirkaart selle laiendamiseks ja seejärel lisage toimingud, mille jaoks olete teatised lubanud. Kui konfigureerite töötaja kohta ühe teatise, veenduge, et **kuvatellimuse** väärtuseks on seatud **1**. Kui konfigureerite rohkem kui ühe toimingu, seadistage **Kuvamisjärjestuse** väärtused järjekorda, et näidata, milles teatised tuleks kuvada. 

      Teatised kuvatakse ainult nende toimingute puhul, mis on lisatud **teatised** kiirkaardile. Saate sinna operatsioone lisada ainult siis, kui kassatoimingute lehel on märgitud nende toimingute **Luba teatised** lehel **kassaoperatsioonid**. Lisaks kuvatakse toimingu teatisi töötajatele ainult siis, kui vastav toiming on lisatud nende töötajate kassa lubadesse.

    > [!NOTE]
    > Teatisi saab kasutaja tasemel alistada. Avage töötaja kirje, valige **kassaload**, ja redigeerige seejärel kasutaja teatise tellimust.

1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Väljal **Teatise intervall** määrake, kui tihti teatisi tuleb kuvada. Mõne teatise puhul peab kassa tegema kontorirakendusse reaalajas kõnesid. Need kõned kulutavad kontorirakenduse arvutusmahtu. Seetõttu soovitame teatise intervalli määramisel arvestada nii teie ärivajadustega kui ka reaalajas kõnede mõjuga kontorirakendusele. Väärtus **0** (null) lülitab teatised välja.
1. Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**. Valige teatise tellimuse sätete sünkroonimiseks graafik **1060** (**personal**) ja siis valige **Käivita kohe**. Seejärel valige loa intervalli sünkroonimiseks graafik **1070** (**kanali konfigureerimine**) ja seejärel valige **Käivita kohe**.

## <a name="view-notifications-in-the-pos"></a>Teatiste kuvamine kassas

Pärast eelnevate etappide lõpule viimist saavad töötajad kassas teatisi vaadata. Teatiste kuvamiseks vajutage kassa üleval paremas nurgas teatiseikooni. Kuvatakse teatisepaneel ja kuvatakse töötaja jaoks konfigureeritud toimingute teatised. 

Selleks et **tellida täitmistoiming** peaks kuvama tellimuse täitmise toimingus järgmised grupid:

- **Kauplusest kättesaamine** – selles grupis kuvatakse tellimuste arv, mille tarneviis on Kättesaamine ja mille kättesaamine on planeeritud praegusest kauplusest. Saate valida grupi numbri, et avada **tellimuse täitmistoiming** filtriga, nii et see näitaks ainult aktiivseid tellimuse ridu, mis on seadistatud praegusest kauplusest peale võtta.
- **Saada kauplusest** – see grupp näitab kasutaja praegusest kauplusest lähetamiseks konfigureeritud üksikute tellimuseridade arvu. Saate valida grupi numbri, et avada **tellimuse täitmistoiming** filtriga, nii et see näitaks ainult aktiivseid tellimuse ridu, mis on seadistatud praegusest kauplusest peale võtta.

Selleks et **tellimuse tagasikutsumise toiming** peaks kuvama tellimuse täitmise toimingus järgmised grupid:

- **Täitmistellimused** – see grupp näitab tellimuste arvu, mis on konfigureeritud kasutaja praeguse kaupluse jaoks kas peale- või lähetuse täitmiseks. Grupil oleva arvu saate valida, et avada **tellimuse tagasikutsumistoiming** filtreeritud vaatega, mis näitab ainult avatud tellimusi, mis tuleb kasutaja praeguses kaupluses täita, et kauplusesse sisse võtta või kauplusest lähetada.
- **Kauplusest kättesaamine** – selles grupis kuvatakse tellimuste arv, mille tarneviis on kättesaamine ja mille kättesaamine on planeeritud praegusest kauplusest. Grupil oleva arvu saate valida, et avada **tellimuse tagasikutsumistoiming** filtreeritud vaatega, mis näitab ainult avatud tellimusi, mis tuleb kasutaja praeguses kaupluses täita, et kauplusesse sisse võtta või kauplusest lähetada.
- **Lähetamistellimused** – see grupp näitab kasutaja praegusest kauplusest lähetatavate tellimuste arvu. Grupil oleva arvu saate valida, et avada **tellimuse tagasikutsumistoiming** filtreeritud vaatega, mis näitab ainult avatud tellimusi, mis tuleb kasutaja praeguses kaupluses täita, et kauplusesse sisse võtta või kauplusest lähetada.

Kui kauplusele määratakse täitmiseks uusi tellimusi, muutub teatiseikoon, näidates uute teatiste olemasolu ja vastavate gruppide arvu värskendatakse. Kuigi gruppe värskendatakse kindlate ajavahemike järel, saavad kassa kasutajad gruppe igal ajal käsitsi värskendada, valides selleks grupi kõrval nupu **Värskenda**. Lõpuks, kui grupis on uus kaup, mida praegune töötaja pole näinud, kuvatakse plahvatusikoon, mis näitab, et selles grupis on uus kaup.

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
