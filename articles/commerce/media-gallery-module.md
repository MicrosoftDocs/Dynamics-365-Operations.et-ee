---
title: Meediumigalerii moodul
description: See teema hõlmab meediumigalerii mooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a4a16391f7eb8b75ea77fe524593c089e24b0cb7
ms.sourcegitcommit: 074fe7e77feb795148c3daf2e6ccbb8a88679343
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2020
ms.locfileid: "3645880"
---
# <a name="media-gallery-module"></a>Meediumigalerii moodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

See teema hõlmab meediumigalerii mooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Meediumigalerii moodulites kuvatakse galeriivaates üks pilt või mitu. Meediumigalerii moodulid toetavad pisipilte, mida saab paigutada kas horisontaalselt (reana pildi all) või vertikaalselt (veeruna pildi kõrval). Meediumigalerii moodulid pakuvad ka võimalust pilte suumida (suurendada) või täisekraanirežiimis vaadata. Meediumigalerii moodulis renderdamiseks peab pilt olema saadaval Commerce'i saidiehitaja meediumiteegis. Praegu toetavad meediumigalerii moodulid ainult pilte.

Vaikerežiimis kasutab meediumigalerii moodul asjaomaste tootepiltide renderdamiseks toote ID-d, mis on saadaval toote üksikasjade lehe (PDP) lehe kontekstis. Meediumifaili tee peab Commerce'i peakontoris kõigi toodete jaoks olema määratud. Pildid tuleks seejärel üles laadida saidiehitaja meediumiteeki failitee järgi, mis määrati toodetele Commerce'i peakontoris. Need pildid hõlmavad toodete ja tootevariantide pilte. Lisateavet piltide üleslaadimise kohta saidiehitaja meediumiteeki leiate teemast [Piltide üleslaadimine](dam-upload-images.md).

Alternatiivselt võib meediumigalerii moodul majutada pildigalerii lehel hoolikalt valitud pilte, sõltumata toote ID-st või lehe kontekstist. Sel juhul tuleb pildid saidiehitaja meediumiteeki üles laadida ja saidiehitajas täpsustada.

Siin on mõned näited meediumigalerii moodulite kasutamise kohta.

- Tootepiltide renderdamine toote üksikasjade lehel
- Tootepiltide renderdamine toote turunduslehel
- Hoolikalt valitud piltide näitamine turunduslehel, näiteks galeriilehel

Järgmisel illustratsioonil on toodud näide toote üksikasjade lehel olevast ostukastist, mis majutab tootepilte meediumigalerii mooduli abil.

![Näide toote üksikasjade lehel olevast ostukastist, mis majutab tootepilte meediumigalerii mooduli abil](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Meediumigalerii atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pildi allikas | **Lehe kontekst** või **Toote ID** | Vaikeväärtus on **Lehe kontekst**. Kui valitud on **Lehe kontekst**, eeldab moodul, et lehel pakutakse toote ID teavet. Kui valitud on **Toote ID**, peab pildi toote ID olema esitatud atribuudi **Toote ID** väärtusena. See võimalus on saadaval Commerce'i versioonis 10.0.12. |
| Toote ID | Toote ID | See atribuut on vajalik ainult juhul, kui atribuudi **Pildi allikas** väärtus on **Toote ID**. |
| Pildi suum | **Tekstisisene** või **Konteiner** | See atribuut võimaldab kasutajal meediumigalerii moodulis pilte suumida. Pilti saab suumida kas tekstisiseselt või pildi kõrval olevas eraldi konteineris. See võimalus on saadaval versioonis 10.0.12 |
| Suumiskaala | Kümnendarv | See atribuut määrab teisendusteguri piltide suumimiseks. Näiteks kui väärtuseks on seatud **2.5**, suurendatakse pilte 2,5 korda.|
| Täisekraan | **Tõene** või **Väär** | See atribuut määrab, kas pilte saab täisekraanirežiimis vaadata. Täisekraanirežiimis saab pilte veelgi suurendada, kui suumimise võimalus on sisse lülitatud. See võimalus on saadaval Commerce'i versioonis 10.0.13. |
| Pildid | Saidiehitaja meediumiteegist valitud pildid | Lisaks tootest tuletamisele saab pilte ka meediumigalerii mooduli jaoks valida. Need pildid lisatakse kõikide saadaolevate tootepiltide lõppu. See võimalus on saadaval Commerce'i versioonis 10.0.12. |
| Pisipildi paigutus | **Vertikaalne** või **Horisontaalne** | See atribuut määrab, kas pisipilte tuleb kuvada vertikaalse või horisontaalse ribana. |

Järgmisel illustratsioonil on näha meediumigalerii mooduli näide, mille puhul on saadaval täisekraanirežiimi ja suumimise suvandid.

![Meediumigalerii mooduli näide, mille puhul on saadaval täisekraanirežiimi ja suumimise suvandid](./media/ecommerce-media-zoom.png)

Järgmisel illustratsioonil on näha meediumigalerii mooduli näide, milles on valitud pildid (st need pildid ei sõltu toote ID-st või lehe kontekstist).

![Meediumigalerii mooduli näide, milles on valitud pildid](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Kui pildi allikas tuletatakse lehe kontekstist, kasutatakse piltide toomiseks toote üksikasjade lehelt pärit toote ID-d. Meediumigalerii moodul toob toodete jaoks pildi failitee Commerce Scale Uniti rakendusliideste (API-de) abil. Seejärel tuuakse pildid meediumiteegist, et neid saaks moodulis renderdada.

## <a name="add-a-media-gallery-module-to-a-page"></a>Meediumigalerii mooduli lisamine lehele

Meediumigalerii mooduli lisamiseks turunduslehel tehke järgmist.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Turundusmall** ja valige seejärel **OK**.
1. Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.
1. Valige vaikelehe pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Vali mall** mall **Turundusmall**. Sisestage jaotises **Lehe nimi** väärtus **Meediumigalerii leht** ja seejärel klõpsake **OK**.
1. Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Meediumigalerii** ja klõpsake seejärel **OK**.
1. Valige meediumigalerii mooduli atribuudipaanil jaotises **Pildi allikas** väärtus **Toote ID**. Seejärel sisestage toote ID väljale **Toote ID**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Te peaksite toote pilte galeriivaates nägema.
1. Ainult valitud piltide kasutamiseks valige atribuudipaani jaotises **Pildi allikas** väärtus **Toote ID**. Seejärel valige jaotises **Pildid** suvand **Lisa pilt** nii mitu korda, kui on vaja piltide lisamiseks meediumiteegist.
1. Seadke täiendavad atribuudid, mida soovite seada, nt **Pildi suum**, **Suumitegur** ja **Pisipiltide paigutus**.
1. Pärast lõpetamist valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Ostukasti moodul](add-buy-box.md)

[Konteineri moodul](add-container-module.md)

[Piltide üleslaadimine](dam-upload-images.md)