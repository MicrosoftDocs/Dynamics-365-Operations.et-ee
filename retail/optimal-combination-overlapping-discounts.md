---
title: "Kattuvate allahindluste optimaalse kombinatsiooni määratlemine"
description: "Kui allahindlused kattuvad, siis peate määrama kattuvate allahindluste kombinatsiooni, mis annab kõige suurema koondallahindluse kõige väiksema kande koondsumma. Kui allahindluse summa ostetavate toodete hinna alusel erineb, nt tavapärase „ostke 1, saate X protsenti allahindlust” (BOGO) jaeallahindluse korral, saab selles protsessist kombinatoorse optimeerimise küsimus."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 598f479c4bba0df289af49076fb0cb7053ee96c1
ms.contentlocale: et-ee
ms.lasthandoff: 04/26/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Kattuvate allahindluste optimaalse kombinatsiooni määratlemine

[!include[banner](includes/banner.md)]


Kui allahindlused kattuvad, siis peate määrama kattuvate allahindluste kombinatsiooni, mis annab kõige suurema koondallahindluse kõige väiksema kande koondsumma. Kui allahindluse summa ostetavate toodete hinna alusel erineb, nt tavapärase „ostke 1, saate X protsenti allahindlust” (BOGO) jaeallahindluse korral, saab selles protsessist kombinatoorse optimeerimise küsimus.

See artikkel puudutab rakendust Microsoft Dynamics AX 2012 R3 (kiirparandusega KB 3105973, välja antud 2. novembril 2015) või uuemat ja Microsoft Dynamics AX-i 2016. aasta veebruari väljaannet. Selleks, et määrata kattuvate allahindluste kombinatsiooni rakendamise õigel ajal ja et jätkata rohkete võimalustega allahindluse funktsiooni pakkumist, mis rakenduses Microsoft Dynamics AX for Retail saadaval on, oleme võtnud kasutusele kattuvate allahindluste rakendamise meetodi. Nimetame seda uut meetodit **marginaali väärtuse hindamiseks**. Marginaali väärtuse hindamist kasutatakse, kui aeg, mis on vajalik kattuvate allahindluste võimalike kombinatsioonide hindamiseks, ületab Dynamics AX-i lehel **Jaemüügi parameetrid** konfigureeritava läve. Marginaali väärtuse hindamise meetodis arvutatakse iga kattuva allahindluse väärtus, kasutades jagatud toodete allahindluse väärtust. Seejärel rakendatakse kattuvad allahindlused kõrgeimast suhtelisest väärtusest madalaima suhtelise väärtuseni. Uue meetodi üksikasjad leiate selle artikli edasisest jaotisest „Marginaali väärtus”. Marginaali väärtuse hindamist ei kasutata, kui toote allahindluse summasid ei mõjuta kandes teine toode. Näiteks ei kasutata seda meetodit kahe lihtsa allahindluse puhul või lihtsa allahindluse ja üksiku toote koguse allahindluse puhul.

## <a name="discount-examples"></a>Allahindluse näited
Dynamics AX-is saate luua ühisele tootekogumile piiramatu arvu jaeallahindlusi. Kuid kuna piirang puudub, võivad tekkida jõudluse probleemid, kui püüate arvutada allahindlusi, mida tuleks erinevatel toodetel kasutada. Järgmised näited illustreerivad seda probleemi üksikasjalikumalt. 1. näites alustame kahe toote ja kahe kattuva allahindlusega. Seejärel näitame 2. näites, kuidas probleem toodete lisamisel edasi areneb.

### <a name="example-1-two-products-and-two-discounts"></a>1. näide: kaks toodet ja kaks allahindlust

Selles näites on vaja kahte toodet mõlema allahindluse jaoks kvalifitseerumiseks ja neid allahindlusi ei saa kombineerida. Selle näite allahindlused on **parima hinna** allahindlused. Mõlemad tooted kvalifitseeruvad mõlemale allahindlusele. Siin on kaks allahindlust. [![Kattuva allahindluse kombinatsioon 01](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) Igasuguse kahe toote puhul oleneb nendest kahest allahindlusest parem kahe toote hindadest. Kui mõlema toote hinnad on võrdsed või peaaegu võrdsed, on 1. allahindlus parem. Kui ühe toote hind on teise toote omast oluliselt madalam, on 2. allahindlus parem. Siin on matemaatiline reegel nende kahe allahindluse hindamiseks üksteise suhtes: [![Kattuva allahindluse kombinatsioon 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) Pange tähele, et kui 1. toote hind võrdub 2. toote hinnast kahe kolmandikuga, siis on kaks allahindlust võrdsed. Selles näites varieerub 1. allahindluse puhul kehtiv allahindluse protsent mõnest protsendist (kui kahe toote hinnad on väga erinevad) kuni maksimaalselt 25 protsendini (kui kahel tootel on sama hind). 2. allahindluse kehtiv allahindluse protsent on fikseeritud. See on alati 20 protsenti. Kuna 1. allahindluse kehtival allahindluse protsendil on vahemik, mis võib olla rohkem või vähem kui 2. allahindlus, siis sõltub parim allahindlus kahe allahindlusega toote hindadest. Selles näites toimub arvutamine kiiresti, kuna ainult kahele tootele rakendatakse ainult kahte allahindlust. Võimalikke kombinatsioone on ainult kaks: üks 1. allahindluse rakendamine või üks 2. allahindluse rakendamine. Puuduvad permutatsioonid, mida arvutada. Iga allahindluse väärtus arvutatakse kahe toote abil ja kasutatakse parimat allahindlust.

### <a name="example-2-four-products-and-two-discounts"></a>2. näide: neli toodet ja kaks allahindlust

Järgmiseks kasutame nelja toodet ja sama kahte allahindlust. Kõik neli toodet kvalifitseeruvad mõlemale allahindlusele. Võimalikke kombinatsioone on kaksteist. Lõpuks rakendatakse kahte allahindlust kandele ühes kolmest kombinatsioonist: 1. allahindlust rakendatakse kaks korda ja 2. allahindlust kaks korda või 1. allahindlust rakendatakse üks kord ja 2. allahindlust 1 kord. Võimalike kombinatsioonide illustreerimiseks vaatame kahte erinevat nelja toote kogumit, millel on erinevad hinnad.

-   Kõigil neljal tootel on sama hind 15.00 dollarit. Sellisel juhul on parim allahindluste kombinatsioon kaks 1. allahindluse rakendamist. Kaks toodet on täishinnaga ja kaks 50 protsenti soodsamad. Allahindlusega koondsumma on kande puhul 45 $ (15 + 15 + 7.50 + 7.50), mis on 15 $ (25 protsenti) odavam kui allahindluseta koondsumma 60 $. 2. allahindlus on ainult 12 $ (20 protsenti).
-   Kaks toodet maksavad kumbki 20 $, üks toode maksab 15 $ ja üks toode 5 $. Sellisel juhul on parim allahindluste kombinatsioon ühekordne 2. allahindluse ja ühekordne 1. allahindluse rakendamine. Järgmine tabel illustreerib allahindlusi.

Tabelite lugemiseks kasutage ühte toodet realt ja ühte toodet veerust. Näiteks kui kombineerite 1. allahindluse tabelis kaks 20 $ toodet, saate 10 $ allahindlust. Kui kombineerite 2. allahindluse tabelis 15 $ toote ja 5 $ toote, saate 4 $ allahindlust. [![Kattuva allahindluse kombinatsioon 03](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) Kõigepealt leiame suurima allahindlust, mis on saadaval mis tahes kahe toote puhul, kasutades ükskõik kumba allahindlust. Kaks tabelit näitavad allahindluse summat kõigi kahe toote kombinatsioonide kohta. Tabelite varjutatud osad kujutavad olukordi, kus toode on paaris iseendaga, mida ei saa teha, või kahe toote pöördsidumine, mis annab sama allahindluse summa ja mida võib eirata. Tabeleid vaadates näete, et 1. allahindlus kahe 20 $ kauba puhul on suurim allahindlus, mis on kummagi allahindluse puhul kõigi nelja toote kohta saadaval. (See allahindlus on esimeses tabelis rohelisena esile tõstetud.) See jätab alles ainult 15 $ toote ja 5 $ toote. Kahte tabelit uuesti vaadates näete, et nende kahe toote puhul on 1. allahindlus 2.50 $, samas kui 2. allahindlus on 4 $. Seega valime 2. allahindluse. Kogu allahindlus on 14 $. Selle arutluskäigu hõlpsamaks visualiseerimiseks on siin veel kaks tabelit, mis näitavad kehtivat allahindluse protsenti kõigi võimalike kahe toote kombinatsioonide korral nii 1. kui ka 2. allahindluse puhul. Lisatud on vaid pool kombinatsioonide loendist, kuna nende kahe allahindluse puhul pole kahele tootele allahindluse rakendamise järjekord oluline. Suurim kehtiv allahindlus (25 protsenti) on rohelisega esile tõstetud ja vähim kehtiv allahindlus (10 protsenti) on punasega esile tõstetud. [![Kattuva allahindluse kombinatsioon 04](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg) **Märkus.** Kui hinnad erinevad ja konkureerib vähemalt kaks allahindlust, on ainus viis parima allahindluste kombinatsiooni garanteerimiseks hinnata mõlemaid allahindluseid ja võrrelda neid.

## <a name="total-possible-combinations"></a>Võimalikud kombinatsioonid kokku
See jaotis jätkab eelmise jaotise näitega. Lisame veel tooteid ja veel ühe allahindluse ja vaatame, kui palju kombinatsioone tuleb arvutada ja võrrelda. Järgmistes tabelites on võimalike allahindluste kombinatsioonide arv tootekoguse kasvades. Tabel näitab, mis juhtub siis, kui kattuvaid allahindlusi on kaks, nagu eelmises näites, ja kui kattuvaid allahindlusi on kolm. Võimalike allahindluste kombinatsioonide arv, mida tuleb hinnata, ületab peagi ka selle piiri, mida isegi kiire arvuti suudab jaetehingute jaoks piisavalt kiiresti arvutada ja võrrelda. [![Kattuva allahindluse kombinatsioon 05](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) Kui rakendatakse veelgi suuremaid koguseid või rohkem kattuvaid allahindlusi, ulatub võimalike allahindluste kombinatsioonide arv kiiresti miljonitesse ja aeg, mis on parima võimaliku kombinatsiooni hindamiseks ja valimiseks vajalik, muutub kiiresti märgatavaks. Jaehinna mootoris on tehtud mõningaid optimeerimisi hinnatavate kombinatsioonide koguarvu vähendamiseks. Kuid kuna kattuvate allahindluste ja tehingute koguste arv pole piiratud, tuleb kattuvate allahindluste korral alati suurt hulka kombinatsioone hinnata. See ongi probleem, mille lahendamisega marginaali väärtuse hindamismeetod tegeleb.

## <a name="marginal-value-method"></a>Marginaali väärtuse meetod
Astmeliselt suureneva hinnatavate kombinatsioonide arvu probleemi lahendamiseks on olemas optimeerimine, mis arvutab tootekogumi korral, millele saab rakendada vähemalt kahte allahindlust, iga allahindluse väärtuse jagatud toote kohta. Nimetame seda väärtust jagatud toodete allahindluse **marginaali väärtuseks**. Marginaali väärtus on kogu allahindluse summa keskmine tootepõhine suurenemine, kui jagatud tooted lisatakse igale allahindlusele. Marginaali väärtus arvutatakse allahindluse kogusummast (DTotal), lahutades allahindluse summa ilma jagatud toodeteta (DMinus\\ Shared) ja jagades selle vahe jagatud toodete arvuga (ProductsShared). [![Kattuva allahindluse kombinatsioon 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) Pärast seda, kui on arvutatud jagatud tootekogumi iga allahindluse marginaali väärtus, rakendatakse allahindlused jagatud toodetele alates kõrgeimast marginaaliväärtusest kuni madalaima marginaaliväärtuseni (ammendavalt). Selle meetodi puhul ei võrrelda kõiki järelejäänud allahindluse võimalusi iga kord pärast üksiku allahindluse rakendamist. Selle asemel võrreldakse kattuvaid allahindlusi üks kord ja seejärel rakendatakse need järjekorras. Lisavõrdlusi ei tehta. Saate läve konfigureerida, et minna üle marginaali väärtuse meetodile lehe **Jaemüügi parameetrid** vahekaardil **Allahindlus**. Koondallahindluse arvutamiseks vastuvõetav aeg erineb jaemüügivaldkondade lõikes. Kuid see aeg jääb üldjuhul kümnete millisekundite ja ühe sekundi vahele.




