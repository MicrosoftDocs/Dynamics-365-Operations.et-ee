---
title: Konteinermoodul
description: See teema hõlmab konteinermooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9bb2c7d56184d009492b4aa839a3546160ad342f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411610"
---
# <a name="container-module"></a>Konteinermoodul

[!include [banner](includes/banner.md)]

See teema hõlmab konteinermooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Konteinermoodul on moodul, mis majutab endas teisi mooduleid. Konteinermooduli esmane eesmärk on määratleda selle jaoks määratud atribuutide kaudu selles sisalduvate moodulite paigutus. Näiteks võivad need moodulid esineda kõrvuti kahe veeruga, kolme veeruga, nelja veeruga või kuue veeruga paigutuses. Need võivad olla ka piiratud konteineri laiusega või täita ekraani. Igale konteinermoodulile võib lisada ka pealkirja.

Olemas on kolme konteinermooduli tugi: konteiner, kahe pesaga konteiner ja kolme pesaga konteiner. Nendesse konteineritesse saab lisada mis tahes tüübi mooduleid. 

> [!NOTE] 
> Soovitame panna moodulid alati konteinermoodulisse, et neid saaks piirata konteineri laiusega.

## <a name="examples-of-container-modules-in-e-commerce"></a>E-kaubanduse konteinermoodulite näited

- Saidi autor soovib kolme veeruga paigutust, kus kolm moodulit kuvatakse kõrvuti. Seega kasutab saidi autor kolme pesaga konteineri tüüpi konteinermoodulit.
- Saidi autor soovib kuue veeruga paigutust, kus kuus moodulit kuvatakse kõrvuti. Seega kasutab saidi autor mahutamistüübi konteinerit, mille sees on kuus veergu.
- Saidi autor soovib lisada lehele mooduli, kuid ei taha, et see täidaks ekraani. Seega lisab saidi autor mooduli konteinermoodulisse ja määrab konteineri atribuudi **Laius** väärtusele **Mahuta konteiner**.

Järgmisel pildil on toodud näide konteinermoodulist, mis sisaldab Commerce'i saidiehitajas karussellmoodulit. Selles näites on konteinermooduli atribuudi **Laius** väärtuseks seatud **Täida ekraan**.

![Konteinermooduli näide](./media/ecommerce-container.PNG)

## <a name="container-module-properties"></a>Konteinermooduli atribuudid

| Atribuudi nimi     | Väärtused | Kirjeldus |
|-------------------|--------|-------------|
| Pealkiri           | Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**) | Konteinerile saab lisada valikulise pealkirja. Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**. Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele. |
| Laius             | **Mahuta konteinerisse** või **Täida ekraan** | Kui väärtuseks on seatud **Mahuta konteinerisse** (vaikeväärtus), on konteineris olevad moodulid piiratud konteineri laiusega. Kui väärtuseks on seatud **Täida ekraan**, ei ole moodulid konteineri laiusega piiratud, vaid võivad täita ekraani. |
| Veergude arv | **1**, **2**, **3**, **4**, **6** või **12** | See atribuut määratleb konteineri veergude arvu. Konteineril võib olla kuni 12 veergu. |

## <a name="container-with-2-slots"></a>Konteiner 2 pesaga

Kahe pesaga tüüpi konteiner on optimeeritud kahe veeruga paigutuseks. Seda tüüpi konteineril on kaks pesa, mis võimaldavad sisalduvate moodulite kõrvuti kuvamist.

Erinevate vaateportide (mobiilsed seadmed, tahvelarvutid, arvutid jne) jaoks paigutuse optimeerimiseks saab kasutada täiendavaid atribuute. Iga vaatepordi jaoks on võimalik määratleda iga veeru laius. Saadaval on järgmised veeru laiuse sätted.

- **75%/25%** – esimesel moodulil on veeru laius 75 protsenti ja teisel moodulil on veeru laius 25 protsenti. Samuti on saadaval valik **25%/75%**.
- **50%/50%** – mõlemal moodulil on võrdne veeru laius.
- **67%/33%** – esimesel moodulil on veeru laius 67 protsenti ja teisel moodulil on veeru laius 33 protsenti. Samuti on saadaval valik **33%/67%**.
- **100%** – mõlemal moodulil on veeru täielik laius. Seega on moodulid virnastatud vertikaalselt ühes veerus. Kuigi see ühe veeruga paigutus läheb vastuollu kahe pesaga tüüpi konteineri eesmärgiga, võib see mõne vaatepordi jaoks olla eelistatav (nt eriti väikesed vaatepordid, nagu mobiili seadmed).

### <a name="container-with-2-slots-properties"></a>Kahe pesaga atribuutidega konteiner

| Atribuudi nimi                   | Väärtused | Kirjeldus |
|---------------------------------|--------|-------------|
| Pealkiri                         | Pealkirja tekst ja pealkirja silt | Konteinerile saab lisada valiku. |
| Eriti väikese vaatepordi konfigureerimine | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** või **100%** | See atribuut määratleb eriti väikeste vaateportide paigutuse. |
| Väikese vaatepordi konfigureerimine   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** või **100%** | See atribuut määratleb väikeste vaateportide paigutuse, nagu mobiili seadmed. |
| Keskmise vaatepordi konfigureerimine  | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** või **100%** | See atribuut määratleb keskmiste vaateportide paigutuse, nagu tahvelarvutid. |
| Suure vaatepordi konfigureerimine   | **25%/75%**, **75%/25%**, **50%/50%**, **67%/33%**, **33%/67%** või **100%** | See atribuut määratleb suurte vaateportide paigutuse, nagu arvutid. |

## <a name="container-with-3-slots"></a>Konteiner 3 pesaga

Kolme pesaga moodulite tüüpi konteiner on optimeeritud kolme veeruga paigutuseks.

Erinevate portide paigutuse optimeerimiseks saab kasutada täiendavaid atribuute. Iga vaatepordi jaoks on võimalik määratleda iga veeru laius. Saadaval on järgmised veeru laiuse sätted.

- **33%/33%/33%** – kõigil kolmel moodulil on võrdne veeru laius.
- **50%/25%/25%** – esimesel moodulil on veeru laius 50 protsenti ja kahel ülejäänud moodulil on veeru laius 25 protsenti. Valikud **25%/50%/25%** ja **25%/25%/50%** on samuti saadaval.
- **16%/16%/67%** – esimesel kahel moodulil on veeru laius 16 protsenti ja kolmandal moodulil on veeru laius 67 protsenti. Valikud **16%/67%/16%** ja **67%/16%/16%** on samuti saadaval.

### <a name="container-with-3-slots-properties"></a>Kolm pesaga atribuutidega konteiner

| Atribuudi nimi                   | Väärtused | Kirjeldus |
|---------------------------------|--------|-------------|
| Pealkiri                         | Pealkirja tekst ja pealkirja silt | Konteinerile saab lisada valikulise pealkirja. |
| Eriti väikese vaatepordi konfigureerimine | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** või **67%/16%/16%** | See atribuut määratleb eriti väikeste vaateportide paigutuse. |
| Väikese vaatepordi konfigureerimine   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** või **67%/16%/16%** | See atribuut määratleb väikeste vaateportide paigutuse, nagu mobiili seadmed. |
| Keskmise vaatepordi konfigureerimine  | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** või **67%/16%/16%** | See atribuut määratleb keskmiste vaateportide paigutuse, nagu tahvelarvutid. |
| Suure vaatepordi konfigureerimine   | **33%/33%/33%**, **50%/25%/25%**, **25%/50%/25%**, **25%/25%/50%**, **16%/16%/67%**, **16%/67%/16%** või **67%/16%/16%** | See atribuut määratleb suurte vaateportide paigutuse, nagu arvutid. |

## <a name="add-a-container-module-to-a-page"></a>Konteineri mooduli lisamine lehele

Uuele lehele konteineri esitamise mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Konteineri mall** ja valige seejärel **OK**.
1. Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. 
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Vali mall** teie loodud videopleieri mall. Sisestage jaotises **Lehe nimi** väärtus **Konteineri leht** ja seejärel valige **OK**.
1. Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Konteinermooduli atribuudipaanil määrake atribuut **Veergude arv** väärtusele **1** ja atribuut **Laius** väärtusele **Täida konteiner**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Sisuplokk** ja klõpsake seejärel **OK**.
1. Konfigureerige sisuploki mooduli atribuudipaani pealkiri, pilt ja paigutus.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Peaksite nägema ühte funktsioonimoodulit, mis mahub konteinermooduli laiusse.
1. Konteinermooduli atribuudipaanil muutke atribuudi **Veergude arv** väärtuseks **3**.
1. Lisage konteinermoodulile veel kaks sisuploki moodulit ja konfigureerige need.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Nüüd peaksite nägema kolme sisuploki moodulit, mis ilmuvad kõrvuti.
1. Kui olete saavutanud soovitud paigutuse, siis valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Akordionmoodul](add-accordion.md)

[Vahekaardimoodul](add-tab.md)

[Karusellmoodul](add-carousel.md)

[Tekstiploki moodul](add-content-rich-block.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Väljaregistreerimismoodul](add-checkout-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
