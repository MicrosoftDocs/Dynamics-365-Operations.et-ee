---
title: Meediumigalerii moodul
description: See artikkel käsitleb meediamoodulite mooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 5e2d0a4422341badee906c71bebdd491e18a38cc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273454"
---
# <a name="media-gallery-module"></a>Meediumigalerii moodul

[!include [banner](includes/banner.md)]

See artikkel käsitleb meediamoodulite mooduleid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Meediumigalerii moodulites kuvatakse galeriivaates üks pilt või mitu. Meediumigalerii moodulid toetavad pisipilte, mida saab paigutada kas horisontaalselt (reana pildi all) või vertikaalselt (veeruna pildi kõrval). Meediumigalerii moodulid pakuvad ka võimalust pilte suumida (suurendada) või täisekraanirežiimis vaadata. Meediumigalerii moodulis renderdamiseks peab pilt olema saadaval Commerce'i saidiehitaja meediumiteegis. Praegu toetavad meediumigalerii moodulid ainult pilte.

Vaikerežiimis kasutab meediumigalerii moodul asjaomaste tootepiltide renderdamiseks toote ID-d, mis on saadaval toote üksikasjade lehe (PDP) lehe kontekstis. Meediumifaili tee peab Commerce'i peakontoris kõigi toodete jaoks olema määratud. Pildid tuleks seejärel üles laadida saidiehitaja meediumiteeki failitee järgi, mis määrati toodetele Commerce'i peakontoris. Need pildid hõlmavad toodete ja tootevariantide pilte. Lisateavet piltide üleslaadimise kohta saidiehitaja meediumiteeki leiate teemast [Piltide üleslaadimine](dam-upload-images.md).

Alternatiivselt võib meediumigalerii moodul majutada pildigalerii lehel hoolikalt valitud pilte, sõltumata toote ID-st või lehe kontekstist. Sel juhul tuleb pildid saidiehitaja meediumiteeki üles laadida ja saidiehitajas täpsustada.

Siin on mõned näited meediumigalerii moodulite kasutamise kohta.

- Tootepiltide renderdamine toote üksikasjade lehel
- Tootepiltide renderdamine toote turunduslehel
- Hoolikalt valitud piltide näitamine turunduslehel, näiteks galeriilehel

Järgmisel illustratsioonil on toodud näide toote üksikasjade lehel olevast ostukastist, mis majutab tootepilte meediumigalerii mooduli abil.

![Näide toote üksikasjade lehel olevast ostukastist, mis majutab tootepilte meediumigalerii mooduli abil.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Meediumigalerii atribuudid

| Atribuudi nimi | Väärtused | Kirjeldus |
|---------------|--------|-------------|
| Pildi allikas | **Lehe kontekst** või **Toote ID** | Vaikeväärtus on **Lehe kontekst**. Kui valitud on **Lehe kontekst**, eeldab moodul, et lehel pakutakse toote ID teavet. Kui valitud on **Toote ID**, peab pildi toote ID olema esitatud atribuudi **Toote ID** väärtusena. See võimalus on saadaval Commerce'i versioonis 10.0.12. |
| Toote ID | Toote ID | See atribuut on vajalik ainult juhul, kui atribuudi **Pildi allikas** väärtus on **Toote ID**. |
| Pildi suum | **Tekstisisene** või **Konteiner** | See atribuut võimaldab kasutajal meediumigalerii moodulis pilte suumida. Pilti saab suumida kas tekstisiseselt või pildi kõrval olevas eraldi konteineris. See võimalus on saadaval versioonis 10.0.12. |
| Suumitegur | Kümnendarv | See atribuut määrab teisendusteguri piltide suumimiseks. Näiteks kui väärtuseks on seatud **2.5**, suurendatakse pilte 2,5 korda. |
| Täisekraan | **Tõene** või **Väär** | See atribuut määrab, kas pilte saab täisekraanirežiimis vaadata. Täisekraanirežiimis saab pilte veelgi suurendada, kui suumimise võimalus on sisse lülitatud. See võimalus on saadaval Commerce'i versiooni 10.0.13 väljalaskes. |
| Suumitud pildi kvaliteet | Arv 1-st kuni 100-ni, mis tähistab protsenti ja mis valitakse juhtriba juhtelemendi abil | See atribuut määratleb sissesuumitud piltide pildi kvaliteedi. Selle väärtuseks saab seada 100 protsenti kindlustamaks, et suumitud pilt kasutaks alati kõrgeimat võimalikku eraldusvõimet. See atribuut ei kehti PNG-failide puhul, sest need kasutavad kadudeta vormingut. See võimalus on saadaval alates Commerce'i versiooni 10.0.19 väljalaskest. |
| Pildid | Saidiehitaja meediumiteegist valitud pildid | Lisaks tootest tuletamisele saab pilte ka meediumigalerii mooduli jaoks valida. Need pildid lisatakse kõikide saadaolevate tootepiltide lõppu. See võimalus on saadaval Commerce'i versioonis 10.0.12. |
| Pisipildi paigutus | **Vertikaalne** või **Horisontaalne** | See atribuut määrab, kas pisipilte tuleb kuvada vertikaalse või horisontaalse ribana. |
| Peida variandi põhitoote pildid | **Tõene** või **Väär** | Kui see atribuut on seatud väärtusele **Tõene**, siis on variandi valimisel põhitoote pildid peidetud, kui variandil ei ole pilte. See atribuut ei mõjuta variantideta tooteid. |
| Dimensioonivaliku meediumi värskendamine | **Tõene** või **Väär** | Kui selle atribuudi väärtuseks on seatud **Tõene**, värskendatakse meediumiteegi pilte, kui valitud on mõni dimensioon (nt värv, laad või suurus) ja kui pilt on saadaval. See atribuut aitab sirvimiskogemust lihtsustada, kuna vastava pildi värskendamiseks ei pea valima kõiki tootevariandi dimensioone. See atribuut on saadaval **Täpsemalt** vahekaardil. |

> [!IMPORTANT]
> **Värskenda meediumit dimensioonide valimisel** on saadaval alates Commerce'i versiooni 10.0.21 väljalaskest. See nõuab Commerce mooduli teegi paketi versiooni 9.31 installimist.

Järgmisel illustratsioonil on näha meediumigalerii mooduli näide, mille puhul on saadaval täisekraanirežiimi ja suumimise suvandid.

![Meediumigalerii mooduli näide, mille puhul on saadaval täisekraanirežiimi ja suumimise suvandid.](./media/ecommerce-media-zoom.png)

Järgmisel illustratsioonil on näha meediumigalerii mooduli näide, milles on valitud pildid (st need pildid ei sõltu toote ID-st või lehe kontekstist).

![Meediumigalerii mooduli näide, milles on valitud pildid.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Kui pildi allikas tuletatakse lehe kontekstist, kasutatakse piltide toomiseks toote üksikasjade lehelt pärit toote ID-d. Meediumigalerii moodul toob toodete jaoks pildi failitee Commerce Scale Uniti rakendusliideste (API-de) abil. Seejärel tuuakse pildid meediumiteegist, et neid saaks moodulis renderdada.

## <a name="add-a-media-gallery-module-to-a-page"></a>Meediumigalerii mooduli lisamine lehele

Meediumigalerii mooduli lisamiseks turunduslehel tehke järgmist.

1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Dialoogiboksis Uus **mall** sisestage malli nime **all** turundusmall **ja** seejärel valige **OK**.
1. Kehapesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige vaikelehemoodul **ja** seejärel valige **OK**.
1. **Vaikelehe** põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Dialoogiaknas **Loo uus lehekülg** sisestage dialoogiakna **Lehe nimi** väljale Meediagalerii **ja** seejärel valige väärtus **Edasi**.
1. Valige **valiku Vali mall** all loodud **turundusmall** ja seejärel **edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui teil on vaja lehekülje teavet redigeerida, valige **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**. 
1. Uue lehekülje põhipesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige konteinerimoodul **ja** seejärel valige **OK**.
1. Valige konteineri pesast kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige meediamoodulis **ja** seejärel valige **OK**.
1. Valige meediumigalerii mooduli atribuudipaanil jaotises **Pildi allikas** väärtus **Toote ID**. Seejärel sisestage toote ID väljale **Toote ID**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Te peaksite toote pilte galeriivaates nägema.
1. Ainult valitud piltide kasutamiseks valige atribuudipaani jaotises **Pildi allikas** väärtus **Toote ID**. Seejärel valige jaotises **Pildid** suvand **Lisa pilt** nii mitu korda, kui on vaja piltide lisamiseks meediumiteegist.
1. Seadke täiendavad atribuudid, mida soovite seada, nt **Pildi suum**, **Suumitegur** ja **Pisipiltide paigutus**.
1. Pärast lõpetamist valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Konteinermoodul](add-container-module.md)

[Piltide üleslaadimine](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
