---
title: Kindlaks optimaalne kombinatsioon kattuvate allahindlusi
description: "Kui allahindluste kattuvad, peab otsustama kattuvate allahindlusi, et madalaima võimaliku tehingu kogusumma või kokku allahindlust. Kui allahindluse summa sõltub ostetavate toodete, näiteks ühise &quot;osta 1, 1 X % väljuge&quot; (BOGO) jaemüügi allahindlused, see protsess muutub küsimus kombinatoorne optimeerimine."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 89643
ms.assetid: 09843c9a-3e19-4e4a-a8ce-80650f2095f9
ms.search.region: global
ms.search.industry: Retail
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 31e5104045ed5b8fbfa3677a7f5702d551de4231
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-optimal-combination-of-overlapping-discounts"></a>Kindlaks optimaalne kombinatsioon kattuvate allahindlusi

Kui allahindluste kattuvad, peab otsustama kattuvate allahindlusi, et madalaima võimaliku tehingu kogusumma või kokku allahindlust. Kui allahindluse summa sõltub ostetavate toodete, näiteks ühise "osta 1, 1 X % väljuge" (BOGO) jaemüügi allahindlused, see protsess muutub küsimus kombinatoorne optimeerimine.

See artikkel kehtib Microsoft Dynamics AX 2012 R3 KB 3105973 (avaldatud November 2, 2015) või hiljem ja veebruar 2016 vabastada Microsoft Dynamics AX. Kombineeritud kattuvate allahindlusi õigeaegseks rakendamiseks ja jätkuvalt rikas diskonteerimise funktsioone, mis on saadaval Microsoft Dynamics AX Retail määramiseks oleme juurutanud kattuvate allahindlusi kohaldamise meetod. Kutsume uue meetodi **marginaalne väärtus pingerida**. Marginaalne väärtus pingerida kasutatakse kui võimalike kombinatsioonide kattuvate allahindlusi hindamiseks vajalik aeg on seadistatav kohta, mis on **hulgi parameetrid** Dynamics AX-i lehel. Järjestamise meetod marginaalne väärtuse väärtus arvutatakse iga kattuva allahindlust abil selle hinnaalandi väärtus jagatud toodetele. Kattuv allahindlusi siis väljastavad suhteline miinimumväärtuseni kõrgeima väärtuse. Uue meetodi kohta täpsemalt Vaata "Marginaalne väärtus" jagu käesoleva artikli. Marginaalne väärtus pingerida ei kasutata toote hinnaalandisummad ei ole mõjutatud teise toote tehingus. Näiteks ei ole seda meetodit kasutada kahe lihtsa allahindlusi või lihtne allahindlust ja koguselt tootena.

## <a name="discount-examples"></a>Soodus näited
Dynamics AX-is saate luua piiramatu arvu jaemüügi allahindlused toodete ühised. Aga kuna ei ole piiratud, saab jõudluse probleemid ilmnevad, kui arvutamiseks võib kasutada eri tooteid varasemad. Järgmised näited selgitavad seda küsimust üksikasjalikumalt. Näite 1 puhul alustame kahe toote ja kaks kattuvad allahindlusi. Seejärel, Näide 2, näitame kuidas probleemi areneb rohkem tooteid lisamisel.

### <a name="example-1-two-products-and-two-discounts"></a>Näide 1: Kaks toodet ning kahest allahindlusest

Selles näites kaks toodet on iga allahindluse saamiseks nõutavad ja allahindlusi ei saa kombineerida. Selles näites hinnaalandid **parim hind** allahindlusi. Mõlemad tooted saada nii allahindlusi. Järgnevalt kahest allahindlusest. [![Kattuvate Soodus combo 01](./media/overlapping-discount-combo-01.jpg)](./media/overlapping-discount-combo-01.jpg) kaks toodetele sõltub sellest kaks soodustust parem kahe toote eest. Kui mõlema toote hind on ühesugune või peaaegu ühesugune, allahindlus 1 on parem. Kui ühe toote hind on tunduvalt väiksem kui teise toote hind, allahindlus 2 on parem. Siin on neist kahest allahindlusest teisi hindamiseks matemaatiline reegel: [![Overlapping allahindlust combo 02](./media/overlapping-discount-combo-02.jpg)](./media/overlapping-discount-combo-02.jpg) tähele, et kui toote 1 võrdub 2-toote kaks, kahest allahindlusest on võrdsed. Selles näites tõhus hinnaalandi protsenti allahindlust 1 varieerub paar protsenti (kui kahe toote hinnad on kaugel) kuni 25% (kui kaks toodet on sama hind). Tõhus hinnaalandi protsenti allahindlust 2 on fikseeritud. Alati on 20 protsenti. Kuna tõhus hinnaalandi protsenti allahindlust 1 vahemik, mis võib olla rohkem või vähem kui 2 Soodus, parim hinnaaland sõltub lähtumise kahe toote eest. Selles näites arvutus on valmis kiiresti, sest ainult kaks allahindluste rakendamist ainult kahe toote kohta. On ainult kaks võimalikke kombinatsioone: allahindlus 1 või üks soodustus 2 kohaldamist ühe taotluse. Ei ole permutatsioonide arvutamiseks. Iga allahindluse väärtus arvutatakse mõlema toote abil ja kasutatakse parimat allahindlust.

### <a name="example-2-four-products-and-two-discounts"></a>2. Näide: Nelja toote ja kahest allahindlusest

Järgmine, me kasutame nelja toote ja sama kahest allahindlusest. Kõigi nelja toote saada nii allahindlusi. On kaksteist võimalikke kombinatsioone. Lõpuks seotakse kahest allahindlusest tehingu üks kolmest kombinatsioonist: kaks taotlust allahindlus 1, kaks taotlust Allahindlus Allahindlus 1 ja üks kohaldamise allahindlust 2 2 või ühe taotluse. Selgitada võimalikud kombinatsioonid, me vaatame kahte eri nelja toote, millel on erinevad hinnad:

-   Kõik neli tooted on sama hinnaga, $15.00. Sel juhul on parim allahindlus kaks taotlust allahindlus 1. Kaks toodet saab täishind ja kaks saab 50 protsenti välja. Diskonteeritud summa kande asub diskonteerimata kokku $60 $45 (15 + 15 + 7,50 + 7,50), mis on $15 (25%). Allahindlus 2 on ainult $12 (20%).
-   Kaks toodet on $20 iga üks toode on $15 ja üks toode on $5. Sel juhul allahindlust parim on allahindlus 1 allahindlust 2, ning kohaldamise ühe taotluse. Järgmistes tabelites illustreerib allahindlused.

Lugeda tabeleid, saate ühe toote rea ja veeruga ühe toote. Näiteks tabeli 1 allahindlust, kui sa ühendada kaks $20 tooted, olete valesti $10. Allahindlust 2 tabeli $15 toote ja toote $5 kombineerides saad $4. [![Kattuvate Soodus combo 03](./media/overlapping-discount-combo-03.jpg)](./media/overlapping-discount-combo-03.jpg) Esiteks leiame suurim allahindlus, mis on saadaval kahe toote kas allahindlust. Kaks tabelit näitavad hinnaalandi summa kõigi kombinatsioonide kahe toote. Varjutatud osa tabelid esindavad kas juhtudel, kui toode on ühendatud ise, mis me ei või vastupidine sidumine kahe toote, mis toodab sama allahindlussumma ja loodusest. Tabeleid vaadates näete, et $20 kahest 1 soodustus on mõeldud kas soodustust kõigi nelja toote suurim allahindlus. (Soodustus on rõhutatud roheline esimeses tabelis). See jätab $15 toote ja $5 toode. Vaadates tabeleid uuesti, näete, et nende kahe toote allahindlus 1 annab $2.50 allahindlust, soodustust 2 antakse $4 soodustust. Seetõttu valime allahindlust 2. Lõppallahindluse on $14. Et see arutelu lihtsam visualiseerida, siin on kaks täiendavaid tabeleid, mis näitab kõiki võimalikke kahe toote kombinatsioone nii allahindlus 1 tõhus hinnaalandi protsendimäära ja Soodus 2. Ainult pool kombinatsioonide loetelu on lisatud, sest need kaks soodustust tellimuse, kus pannakse kahe toote allahindlus ei ole oluline. Tõhus allahindlust (25%) on rõhutatud roheline ja madalaim efektiivne soodustus (10%) punasega. [![Kattuvate Soodus combo 04](./media/overlapping-discount-combo-04.jpg)](./media/overlapping-discount-combo-04.jpg)**Märkus:** erinevad, kui kahe või enama allahindluse konkureerida, ainus viis tagada parim kombinatsioon allahindlused on arvestada nii allahindluste ja võrrelda neid.

## <a name="total-possible-combinations"></a>Kokku võimalikke kombinatsioone
Käesoleva jätkub näiteks eelmises osas. Me lisada rohkem tooteid ja teise allahindluse ja vaata kui palju kombinatsioone tuleb arvutada ja võrrelda. Järgmine tabel näitab võimalikke allahindluskombinatsioone arvu kui toote kogus suureneb. Tabel näitab, mis juhtub nii kui on kaks kattuva allahindlusi, nagu eelmises näiteks, ja kui on kolm kattuvad soodustused. Tuleb hinnata võimalikke allahindluskombinatsioone arv ületab kiiresti, isegi kiire arvuti saate arvutada ja võrrelda mõeldud jaemüügiettevõtetele tehingute piisavalt kiiresti. [![Kattuvate Soodus combo 05](./media/overlapping-discount-combo-05.jpg)](./media/overlapping-discount-combo-05.jpg) kui isegi suuremates kogustes või rohkem kattuvate allahindluste rakendamist, võimalikke allahindluskombinatsioone arv kiiresti läheb miljoneid ja aeg, mis on vajalikud hindavad ja valivad head kiiresti muutub märgatav. Jaemüügi hind mootori kombinatsioonid, mida tuleb hinnata arvu vähendamiseks on tehtud mõned optimeerimine. Aga kuna number kattuvad allahindluste ning koguste tehingus ei ole piiratud, on alati palju kombinatsioone, hinnata kui on kattuvaid allahindlusi. See on marginaalne väärtus järjestamise meetod lahendab probleemi.

## <a name="marginal-value-method"></a>Marginaalne meetodil
Eksponentsiaalselt üha rohkem kombinatsioonid, mida tuleb hinnata probleemi lahendamiseks olemas on optimeerimise, mis arvutab ühe ühise toote iga soodustust sätestatud kaks või mitu hinnaalandit saab rakendada toodete väärtuse. Me nimetame seda väärtust, mis on **marginaalne väärtus** jagatud toodete hinnaalandi. Marginaalne väärtus on toote suurenemine allahindlussumma kokku Keskmine kui jagatud tooted on kaasatud iga allahindlust. Marginaalne väärtuse arvutamisel võetakse ilma jagatud toodete hinnaalandi summa lahutamist lõppallahindluse summa (DTotal) (DMinus\\ jagatud), ning jagatakse see vahe jagatud toodete (ProductsShared) arv. [![Kattuvate Soodus combo 06](./media/overlapping-discount-combo-06.jpg)](./media/overlapping-discount-combo-06.jpg) pärast iga soodustust jagatud komplekti tooted marginaalne väärtus arvutatakse, on allahindluste rakendamist jagatud toodete et, ammendavalt, kõrgeim marginaalne väärtusest madalaim marginaalse väärtuseni. Selle meetodi puhul ei ole kõik ülejäänud hinnaalandi võimalused võrreldes iga kord pärast ühekordsest soodustust rakendatakse. Selle asemel kattuvaid allahindlused võrreldes üks kord ja seejärel rakendatakse järjestuses. Ei ole täiendavaid võrdlusi on tehtud. Konfigureerimiseks künnis marginaalne väärtuse meetodi sisselülitamiseks on **Soodus** vahekaardil on **hulgi parameetrid** lehel. Sobiv kellaaeg lõppallahindluse arvutamise erinev jaekaubanduse. Kuid seekord läheb tavaliselt vahemikus kümneid millisekundeid ühe sekundi.


