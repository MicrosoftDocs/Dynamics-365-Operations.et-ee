---
title: Töökäskude plaanimine
description: Selles teemas tutvustatakse, kuidas ajastada töökäske varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e98a30a03856f5532d420e516cb35d66acffb278
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383478"
---
# <a name="schedule-work-orders"></a>Töökäskude plaanimine

[!include [banner](../../includes/banner.md)]

 

Selles teemas tutvustatakse, kuidas ajastada töökäske varahalduses. 

Töökäsu vajalikku tundide arvu määramiseks lahutatakse prognoositud tundide arvust sisestatud tunnid. Kui vaja on rohkem aega, tuleb prognoosi vastavalt kohandada. Jaotises **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud** saate vaadata või redigeerida töökäsu prognoose, valides selleks töökäsu ja klõpsates nuppu **Prognoos** vahekaardil **Töökäsk**. Kui töökäsud on loodud ja prognoositud, on järgmiseks sammuks töökäsu täitmisel vajalike hooldustöötajate ja tööriistade määramine.

Ajastada saab ainult sellise töökäsu töötsükli olekuga töökäske, mis lubavad ajastamist. Ajastamise lubamist seadistatakse jaotises **Varahaldus** > **Seadistus** > **Töökäsud** > **Töötsükli olekud** > **Üldine** kiirkaart > tumblernupp **Luba ajastamine**.

1. Klõpsake **Varahaldus** > **Üldine** > **Töökäsud** > **Kõik töökäsud**.

2. Valige loendist need töökäsud, mida soovite ajastada. Näiteks võite loendit sortida, võttes aluseks **Praeguse töötsükli oleku**.

3. Klõpsake vahekaardil **Üldine** suvandit **Ajasta**.

4. Dialoogis **Töökäskude ajastamine** saate vajadusel lisada valikuid vastavalt oodatavale alguskuupäevale ja teenindustasemele. Kui kavandamisprotsess peaks jälgima teistele töödele juba kavandatud ressursside võimsuse piiranguid, veenduge et tumblernuppude **Vara**, **Tööriist** ja **Töötaja** väärtus on „Jah“.

    [!NOTE]
    Kui seate tumblernuppude **Vara**, **Tööriist** ja **Töötaja** väärtuseks "Ei", ignoreeritakse olemasolevaid reserveeringuid. Infologis kuvatakse kattuvate töökäsu graafikute loendit ja te saate vajadusel klõpsata teatistel, et avada töökäsk ja muuta selle ajastust.

5. Et näha üksikasjalikumat teavet ajastamisprotsessi kohta, valige tumblernupu **Paljusõnaline** väärtuseks „Jah“. See tähendab, et töökäskude ja hooldustöötajate arvutatud skooride üksikasjalikku teavet näidatakse Infologis.

6. Klõpsake **OK**, et alustada ajastamise protsessi.

7. Kui ajastamine on lõpetatud, näitab Infolog ajastatud töökäskude arvu ja ka üksikasjalikumaid andmeid, kui tumblernupp **Verbose** on seadistatud väärtusele "Jah".

>[!NOTE]
>Töökäsud on ajastatud ühte tsüklisse töökäsu kohta, mitte töökäsu töö kohta. Võite avada dialoogi **Töökäskude ajastamine** ka otse jaotises **Varahaldus** > **Perioodiline** > **Töökäsud** > **Töökäskude ajastamine**. Töökäsu ajastamise alustamiseks tehke oma valikud ja klõpsake **OK**. Töökäsu ajastamist on võimalik seadistada pakett-tööna dialoogis **Töökäskude ajastamine** > kiirkaardil **Käivita taustal**.

*Näide:* alloleval joonisel väljale **Oodatav algus** sisestatud valem loob töökäsu ajastamise kõigile töökäskudele, mille oodatud alguskuupäev on nädala pärast ja hiljem. See valem võib olla kasulik, kui käivitate töökäsu ajastamisi pidevalt, kuid tahate kindlustada, et järgmisele 5-6 päevale kavandatud töökäske uuesti ei ajastataks.

![Joonis 1](media/03-work-order-scheduling.png)

Töökäskudega seotud töökäsu tüüp võib seadistada ajastamise ühele hooldustöötajale (**Varahaldus** > **Seadistus** > **Töökäsud** > **Töökäsu tüübid** > **Üks hooldustöötaja** tumblervõti seadistatud olekusse "Jah"). See tähendab, et kui töökäsu juures kasutatakse töökäsu tüüpi, seadistatakse tumblernupp **Üks hooldustöötaja** jaotise **Kõik töökäsud** üksikasjade lehe > vaates **Päis** > vahekaardil **Ajakava** automaatselt olekusse "Jah". Töökäsu ajastamise ajal ajastatakse kõik töökäsule loodud töökäsu hooldustööd hiljem samale hooldustöötajale. Vajadusel saate redigeerida tumblernupu **Üks hooldustöötaja** valikut jaotises **Kõik hooldustöötajad**, et võimaldada töökäsu töödele mitme töötaja või ühe töötaja ajastamine.

Ajastamise protsess varahalduses sisaldab ajastamise arvutuses mitmeid faktoreid.

- Nii töökäskude kui hooldustöötajate skooride arvutamine. Töökäskude ja hooldustöötajate skoorid on seadistatud jaotises **Varahalduse parameetrid**. 
- Töö teostamiseks on nõutav sobivate pädevuste, see tähendab oskuste ja sertifikaatide, kontrollimine. Oskused ja sertifikaadid seadistatakse hooldustöötajatele moodulis **Inimressursid** (**Inimressursid** > **Töötajad** > **Töötajad** > valige loendist tööaja > vahekaart **Töötaja** jaotis > **Pädevused** > nupud **Oskused** ja **Sertifikaadid**). Oskusi ja sertifikaate saab lisada ka hooldustööde tüüpidele ja hooldustööde vahetustele. Lugege pädevuste ja hooldustööde tüüpide kohta lisa jaotisest [Hooldustöö tüübi kategooriad ja hooldustöö tüübid, hooldustöö tüübi variandid, hooldustöö vahetused ja hoolduse kontrollnimekiri](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).  

## <a name="scores-used-in-work-order-scheduling"></a>Töökäsu ajastamises kasutatud skoorid

Töökäsu töö skooride arvutamine põhineb töökäsu oodataval alguskuupäeval ja teenindustasemel.

**Alguskuupäeva** arvutamine: iga oodatud alguskuupäevast arvutatud tulevase kuupäeva korral lahutatakse alguskuupäeva skoor ja korrutatakse skooriga, mis allolevates näidetes on "10".

**Kriitilisuse** arvutamine: kriitilisuse skoor korrutatud töökäsu kriitilisusega.

**Teenindustaseme** arvutamine: teenindustaseme skoor jagatud töökäsu teenindustasemega.

Allolevates näidetes on kriitilisuse skoor "2" ja teenindustaseme skoorid on "5" ja "100".

**Näide 1.**

| Töökäsu ID | Eeldatav alguskuupäev | Töökäsu kriitilisus | Töökäsu teenuse tase | Kalkulatsioon               | Punktisumma      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Homme            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | Kaks päeva alates tänasest   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | Kaks päeva alates tänasest   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

Töökäsud ajastatakse järgmises järjekorras: WO-000108**16**, WO-000108**18**, WO-000108**17**.

**Näide 2.**

| Töökäsu ID | Eeldatav alguskuupäev | Töökäsu kriitilisus | Töökäsu teenuse tase | Kalkulatsioon                 | Punktisumma    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Homme            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | Kaks päeva alates tänasest   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | Kaks päeva alates tänasest   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Kui teenindustaseme skoor on tõstetud "5" asemel "100" peale, on ajastamise järjekord: WO-000108**18**, WO-000108**16**, WO-000108**17**.

Hinnangu skoorid seoses arvutamisega, millised hooldustöötajad peaksid töötama töökäskudega, on kõik seadistatud arvudena, mis lisatakse igale hooldustöötaja arvutusele töökäsu ajastamise käigus. Töökäsule valitakse kõrgeima skooriga hooldustöötaja. Siin on hooldustöötajate skooride lühike kirjeldus.

| Hooldustöötaja skoor| Kirjeldus |
|---|---|
| Vastutav töötaja | Kui hooldustöötaja valitakse töökäsu vastutavaks töötajaks, skoor liidetakse. |
| Vastutav hooldustöötajate grupp | Kui hooldustöötaja on töökäsu vastutavate hooldustöötajate rühma liige, lisatakse skoor. |
| Eelistatud hooldustöötaja         | Kui hooldustöötaja valitakse vara eelistatud hooldustöötajaks, skoor liidetakse. |
| Eelistatud hooldustöötajate grupp   | Kui töötaja on vara eelistatud hooldustöötajate rühma osa, skoor liidetakse.  |
| Koht  | Kui teie ettevõte kasutab töö asukohti, saavad hooldustöötajad täisskoori, kui nad asuvad varaga seotud töö asukohas. Kui vara töö asukohal on peamine asukoht, saavad selle töö asukoha hooldustöötajad 1/2 skoori. Kui sellel asukohal on samuti peamine asukoht, saavad selle töö asukoha hooldustöötajad 1/3 skoori. Kui sellel asukohal on samuti peamine asukoht, saavad selle töö asukoha hooldustöötajad 1/4 skoori ja nii edasi. Kui teie ettevõte kasutab vara asukohta, mida me ei soovita, kasutatakse asukoha skooride arvutamiseks asukohta, piirkonda ja tsooni. Töötajad saavad täiskoori, kui nad asuvad varaga seotud asukohas, alal ja tsoonis. Kui töötaja asukoht kattub ainult asukoha ja piirkonnaga, on hooldustöötaja hinnangu skoor 2/3 täisskoorist. Kui hooldustöötaja asukoht kattub ainult asukohaga, on hooldustöötaja hinnangu skoor 1/3 täisskoorist. |
| Töötaja töösuhte alguskuupäev  | Iga kuupäeva kohta, millal ajastatud alguskuupäev on oodatavast alguskuupäevast hilisem, skoor lahutatakse.  |

>[!NOTE]
>Kui skooriks on määratud "0", seda skoori ei arvestata. See on kasulik, kui te näiteks ei soovi vastutavat töötajat oma plaani kaasata.

## <a name="competencies-used-in-work-order-scheduling"></a>Töökäsu ajastamises kasutatavad pädevused

Oskuste ja sertifikaadi nõudeid saab seadistada hooldustöö tüüpidele (**Varahaldus** > **Seadistus** > **Tööd** > **Hooldustöö tüübid**) ja hooldustöö vahetustele (**Varahaldus** > **Seadistus** > **Tööd** > **Hooldustööde vahetus**). 

Hooldustöö tüübid ja hooldustöö vahetused valitakse töökäsu töödele. Kui hooldustöö tüübile või hooldustöö vahetusele on valitud oskused või sertifikaadid ja seda hooldustöö tüüpi või hooldustöö vahetust kasutatakse töökäsu tööl, ajastatakse töökäsuga töötamiseks ainult sobivate oskuste ja sertifikaatidega hooldustöötajad.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Töö plaanitud töökäskudega Gantti diagrammi abil

**Plaanitud töökäskude Gantti diagramm** pakub graafilist liidest, kus saate oma töökäske vaadata ja ümber plaanida.

Gantti diagrammi vaatamiseks ja sellega töötamiseks tehke järgmist.

1. Avage jaotis **Varahaldus > Töökäsud > Plaanitud töökäskude Gantti diagramm**.

1. Kasutage jaotises **Sätted** ripploendeid ja välju, et seadistada Gantti diagrammis kuvatav töö asukoht, ajavahemik ja ajaskaala.

1. Valige **Rakendamine**.

    - Gantti diagrammi värskendatakse, et näidata teie sätetele vastavaid plaanitud töökäske. Iga töökäsku esindab sinine ristkülik.
    - Kuvatud töökäsu uuesti plaanimiseks valige ja lohistage see sobivale uuele kuupäevale ja kellaajale.

1. Kui tegite muudatusi, valige nende salvestamiseks Toimingupaanil käsk **Salvesta**.
