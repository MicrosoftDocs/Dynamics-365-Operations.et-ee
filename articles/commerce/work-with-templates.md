---
title: Mallidega töötamine
description: Selles teemas kirjeldatakse, kuidas töötada mallidega rakenduses Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 815565dd203925fa0acca9336c4ddc56db8c4058
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002563"
---
# <a name="work-with-templates"></a>Mallidega töötamine


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas töötada mallidega rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Nagu rääkisime teemas [Mallide ja paigutuste ülevaade](templates-layouts-overview.md), mallid määravad suvandite kogumi, mis on saadaval järgmistele autoritele. Mallid on kasulikud ettevõtte veebiloomismeeskonnale mitmel põhjusel ja hea struktuuriga mallid võivad olla abiks kõikide järgmiste eesmärkide saavutamisel.

- Lihtsustage igapäevase sisu toimetaja rollide loomiskogemust.

    - Filtreerige mooduli suvandeid, nii et lehe konkreetse jaotise kohta kuvatakse ainult asjakohased moodulid. (Näiteks saab malli turunduse jaotist konfigureerida filtreerima välja ebaolulised moodulid, mida ei tohiks kunagi selles kontekstis kasutada ja mis kuvamisel muudavad sisu loomise toimingud keerulisemaks.)
    - Konfigureerige vaikemooduli säte, et aidata muuta loomine tõhusamaks.
    - Määrake lehe vaikefragmendid, et aidata muuta loomine tõhusamaks. (Näiteks kuvatakse päise ja jaluse fragmendid mallis automaatselt igal järgmisel lehel.)

- Hoidke ettevõtte saidid kaubamärgile vastavad, määrates heaks kiidetud mooduli kogumi korralduse ja konfigureerimissuvandid.

    > [!TIP] 
    > Edukat e-kaubanduse saidid pakuvad klientidele tuttavat, korratavat ja kaubamärgile vastavaid kasutuskogemuse (UX) kujunduse mustreid. Malle kasutades aitate reguleerida järjepidavust kogu saidil.

- Parandage otsingumootori optimeerimise (SEO) skoore, tagades korratavad ja programmiliselt määratletud lehedefinitsioonid ja metaandmed.

> [!NOTE]
> Kuigi mallid on mõeldud reguleerima järjepidevust kogu saidil, saab neid teoreetiliselt konfigureerida nii, et need ei jõusta järjepidevust. Kaubamärgi ja saidi adminsitraatorid saavad määrata saidi lehtedele mis tahes varieeruvuse taseme. Näiteks võib malli jätta täiesti tühjaks, et sisu autorid saaksid luua sellise lehekujunduse, nagu ise soovivad. Sellisel juhul ei kehti ükski eeltoodud eelistest.

## <a name="modify-a-template"></a>Malli muutmine

Malle muudetakse malli redaktori abil.

Malli redaktori avamiseks järgige üht järgmistest etappidest.

- Valige saidi navigeerimispaanilt suvand **Mallid** ja seejärel valige muutmiseks mall.
- Olemasoleva lehe redaktorist valige vasakult liigendpuust ülemine sõlm. Seejärel valige paremalt atribuutide paanilt suvand **Redigeeri malli**.

Liigendpuu vaade vasakul kuvab mooduli suvandid ja struktuurid, mis on saadaval alampaigutustele ja -lehtedele. Kui valite liigendpuust mooduli, saate vaadata valitud mooduli malli atribuute paremal atribuutide paanilt. Mõni neist atribuutidest esineb vaid malli redigeerimisel. Atribuutide selgitused leiate järgmisest tabelist.

| Atribuudi nimi | Kirjeldus |
|---|---|
| Miinimum esinemiskorrad | See atribuut määrab valitud mooduli esinemiste minimaalse arvu. Näiteks kui väärtus on **1**, on see moodul järgmiste autorite jaoks kohustuslik, kui aga väärtus on **0** (null), on moodul valikuline. |
| Maksimum esinemiskorrad | See atribuut määrab valitud mooduli esinemiste maksimaalse arvu. Näiteks kui väärtus on **1**, võib moodulit lisada vaid üks kord. |
| Minimaalselt mooduleid (konteinerid) | Teisi mooduleid sisaldavad moodulite (ehk *konteinerite moodulite*) jaoks määrab see atribuut minimaalse arvu kõiki mooduleid, mis tuleks alamatena lisada. Näiteks karussellmooduli korral võib väärtuse seada arvule, mis on suurem kui 1. |
| Maksimaalselt mooduleid (konteinerid) | Konteineri moodulite jaoks määrab see atribuut maksimaalse arvu kõiki mooduleid, mis tuleks alamatena lisada. Näiteks karussellmooduli korral võib väärtuse seada arvule, mis on väiksem kui 10. |
| Lukustatud | Kõikide mooduli põhiatribuutide kõrval kuvatakse **lukustatud** kahendmuutujaga juhtelement. Sellega saab malli autor lukustada malli mooduli sätte. Lukustatud mooduli sätet ei saa üle kirjutada ühegi alampaigutuse või -lehega. See muutub keskselt redigeeritavaks atribuudi väärtuseks kõikidele paigutustele ja lehtedele, mis malli kasutavad. |

## <a name="create-a-new-template"></a>Loo uus mall

Uue malli loomiseks tehke järgmist.

1. Valige saidi navigeerimispaanilt suvand **Mallid**, et avada malli inspektori vaade.
1. Valige suvand **Uus mall**.
1. Sisestage malli loomise dialoogiboksi malli nimi ja kirjeldus. Sisestatud väärtused kuvatakse autoritele, kui nad loovad uusi lehti. Seega sisestage metaandmed, mis on kasulikud teistele lehe autoritele. Näiteks sisestage kirjelduseks fraas **Kasutage seda malli üldiste turunduslehtede loomiseks**. Neid metaandmeid saab hiljem redigeerida.
1. Valige nupp **OK**, et luua uus mall ja avada malli redaktor. Malli redaktor kuvab vasakul liigendpuu ja paremal atribuutide paani.
1. Laiendage liigendpuul sõlmi ja valige pesa **HTML-i päis**.
1. Kui selles pesas veel mooduleid pole, valige kolmikpunkti nupp (**...**) ja valige käsk **Lisa moodul**.
1. Dialoogiaknas **Lisa moodul** valige suvand **Lehe vaikekokkuvõte** ja seejärel valige nupp **OK**.
1. Valige liigendpuust uus moodul ja seejärel sisestage atribuutide paanil mis tahes vaikesätted, mida tuleb automaatselt konfigureerida malli kõikide alamlehtede jaoks. Kui te ei soovi vaikesätteid, jätke need väärtused tühjaks.
1. Valige liigendpuust pesa **Sisu**, valige kolmikpunkti nupp ja seejärel suvand **Lisa moodul**.
1. Valige lehe konteineri moodul (võib olla ainult üks valik) ja valige nupp **OK**.

Uue lehe konteineri mooduli all näete uut pesade kogumit (**Päis**, **Põhi** jne). Siin saate lisada ja konfigureerida mooduli valikuid, mis on saadaval autoritele, kui nad loovad lehti sellest mallist. Kui te pesasse ühtki moodulit ei lisa, on vaikimisi selles pesas toetatud kõik mooduli tüübid.

Mall on nüüd tehniliselt kehtiv ja seda saab salvestada, registreerida ja kasutada uute lehtede loomiseks. Kuid järgmises kolmes jaotises kirjeldatakse teisi vaikesätteid, mida võite soovida kõigepealt konfigureerida.

## <a name="add-a-header-and-a-footer"></a>Päise ja jaluse lisamine

Kui teie saidil juba on päise fragment, järgige neid etappe, et lisada mallile päis ja jalus.

1. Laiendage liigendpuus pesa **Sisu** ja selle alamlehe moodulit.
1. Valige pesa **Päis**.
1. Valige pesa **Päis** kolmikpunkti nupp ja seejärel valige käsk **Lisa fragment**.
1. Otsige ja valige saidi päise fragment ning seejärel valige nupp **OK**.

Kõik lehed, mis malli kasutavad, pärivad nüüd automaatselt selle päise fragmendi.

Kui teie saidil pole veel päise fragmenti, vaadake lisateavet selle loomise kohta teemast [Fragmendi loomine](work-with-fragments.md#create-a-fragment) ja seejärel läbige eelmine protseduur.

## <a name="change-the-template-theme"></a>Malli kujunduse vahetamine

Vaikekujunduse valimiseks kõikidele lehtedele, mis malli kasutavad, tehke järgmist.

1. Laiendage vasakul liigendpuus pesa **Sisu**.
1. Valige pesast **Sisu** lehe konteineri moodul (nt **Vaikeleht**).
1. Valige kujundus paremalt atribuutide paanilt väljast **Kujundus**.

Vaikimisi kasutavad nüüd kõik uued lehed valitud kujundust. Selleks et lehed ei kirjutaks seda sätet paigutuse või lehe tasandil üle, seadke **lukustatud** kahendmuutujaga juhtelemendi väärtuseks **Tõene**.

## <a name="add-a-script-to-a-template"></a>Mallile skripti lisamine

Saate lisada mallile HTML-i **&lt;skripti&gt;** elemente, mis sisaldavad JavaScripti. Nii saate luua oma lehtede HTML-i päisele, sisu alguse ja sisu lõpu jaotistele skripti vaikekäitumised.

Mallile skripti lisamiseks tehke järgmist.

1. Valige vasakult liigendpuust pesa, kuhu soovite lisada **&lt;skripti&gt;** elemendi (nt HTML-i päis, sisu algus või sisu lõpp).
1. Valige pesa kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksist **Lisa moodul** skripti moodul (nt **Väline skript** või **Sisemine skript**).
1. Sisestage skript paremale atribuutide paanile skripti vastava atribuudi juhtelemendi jaoks (nt **Sisemine skript** või **Skripti sildid**).
1. Sisestage atribuutide paanile kõik teised valikulised sätted, mida soovite konfigureerida.

> [!TIP]
> Kui soovite mõnda skripti moodulit teiste mallide jaoks uuesti kasutada, saate need teisendada fragmentideks. Nii aitate muuta loomise protsessi tõhusamaks ja tsentraliseerite värskendamise protsessi. Lisateavet selle kohta, kuidas teisendada skripti moodul fragmendiks, vaadake teemast [Olemasoleva mooduli konfiguratsiooni salvestamine fragmendina](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).

## <a name="save-check-in-preview-and-publish-a-template"></a>Malli salvestamine, registreerimine, eelvaatamine ja avaldamine

Malli salvestamiseks ja kontrollimiseks tehke järgmist.

1. Valige malli redaktorist ülevalt suvand **Salvesta**. Salvestatud muudatused ei mõjuta järgmisi lehti, kuni need registreeritakse.
1. Valige suvand **Registreeri**. Teie muudatused on nüüd leitavad järgmiste töövoogude jaoks.

Muudatuste eelvaatamiseks avage olemasolev leht, mis kasutab malli, või looge mallist uus leht.

Pärast malli muudatuste vaatamist järgige üht alltoodud etappidest malli avaldamiseks reaalajas saidil.

* Valige suvand **Mallid**, valige mall ja seejärel käsk **Avalda**.
* Valige malli redaktorist suvand **Avalda**.
* Avaldage leht, mis viitab avaldamata mallile. Mall avaldatakse automaatselt.

> [!WARNING]
> Kui mall või mõni muu sisuhaldussüsteemi (CMS) üksus avaldatakse, on see Internetist leitav. Ärge avaldage dokumente või varasid, kuni olete valmis need avalikuks muutma. Salvestatud ja registreeritud, aga veel avaldamata dokumentide versioonid on leitavad vaid autenditud süsteemikasutajatele.

## <a name="additional-resources"></a>Lisaressursid

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Eelmääratud paigutustega töötamine](work-with-layouts.md)
