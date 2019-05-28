---
title: BOM arvutused
description: Kulu ümardamist ja müügihinna kalkulatsioone nimetatakse koosluse kalkulatsiooniks (BOM) ja neid saate käivitada lehelt Arvestused. Teema sisaldab teavet koosluse kalkulatsioonide kohta.
author: AndersGirke
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 29ea9ddefba3416a33cd0e2f873624cc5c781a55
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552690"
---
# <a name="bom-calculations"></a>BOM arvutused

[!include [banner](../includes/banner.md)]

Kulu ümardamist ja müügihinna kalkulatsioone nimetatakse koosluse kalkulatsiooniks (BOM) ja neid saate käivitada lehelt Arvestused. Teema sisaldab teavet koosluse kalkulatsioonide kohta.

Kulu ümardamist ja müügihinna kalkulatsioone nimetatakse koosluse kalkulatsiooniks (BOM) ja neid saate käivitada lehelt **Arvestused**. Lehelt **Arvestused** saate teha järgmisi ülesandeid.

-   Arvutada toodetud kauba kulu ning luua seostatud kauba kulukirjet kuluversioonis.
-   Arvutada toodetud kauba müügihinda ning luua seostatud kauba müügihinna kirjet kuluversioonis.

Lehe **Arvestused** kasutamise viis varieerub veidi, sõltuvalt sellest, kuidas te koosluse kalkulatsioone käivitate. Lehe **Arvestused** kasutamise viis sõltub ka sellest, kas koosluse kalkulatsioonid hõlmavad standardkulude või planeeritud kulude kuluversiooni, ning ka mitmetest poliitikatest, mis on määratud koosluse kalkulatsioonides kasutatavas kuluversioonis. **Märkus!** Lehe **Arvestused** variatsiooni kasutatakse müügitellimuse, müügipakkumise ja müügitellimuse rea kauba kontekstis. Neid kalkulatsioone nimetatakse tellimusomasteks koosluse kalkulatsioonideks. Tellimusomane koosluse kalkulatsioon ei loo kauba kulukirjet hinnaarvestuse versiooni piires. Selle asemel loob see kalkulatsioonikirje, mis kuvatakse lehel **Koosluse arvutamise üksikasjad**. See kalkulatsioonikirje sisaldab arvutatud kulu ja arvutatud müügihinda. Lehe **Arvestused** saab avada ühe toodetud kauba või kuluversiooni jaoks.

-   Ühe toodetud kauba kulude arvutamiseks käivitage koosluse kalkulatsioonid lehelt **Kauba hind**. Leht **Arvestused** pärib kauba identifikaatori. Määrata tuleb kuluarvutuse versioon, koosluse versioon, protsessi versioon, kalkulatsiooni kogus, arvutamiskuupäev ja tegevuskoht.
    -   Vaikimisi on koosluse versioon ja protsessi versioon määratud kauba, tegevuskoha, kuupäeva ja kalkulatsiooni koguse aktiivsete versioonidega. Saate siiski alistada vaikeväärtused kinnitatud versioonidega.
    -   Vaikimisi on kalkulatsiooni kogus määratud kauba standardtellimuse kogusega. Saate siiski vaikeväärtust alistada.
    -   Arvutamiskuupäeva või tegevuskohta saab kuluversiooniga volitada, või kasutajapõhiseid väärtusi saab seadistada, kui kuupäev või tegevuskoht pole kuluversioonis volitatud. Tulevane arvutamiskuupäev määrab, kuidas ootel kulukirjeid kasutatakse. Koosluse kalkulatsioonid kasutavad ootel kulukirjeid, millel on lähim alguskuupäev kas arvutamiskuupäeval või enne seda.
-   Selleks, et kõigi toodetud kaupade või valitud kaupade kulusid arvutada, või värskendada kaupu kasutuskoha alusel, käivitage koosluse kalkulatsioonid lehelt **Kuluarvutuse versiooni seadistus** või lehelt **Kuluarvutuse versiooni hooldus**. Leht **Arvestused** pärib kuluversiooni.
    -   Arvutuste puhul eeldatakse, et toodetud kauba (ja seotud tegevuskoha, kuupäeva ja koguse) puhul kasutatakse aktiivset koosluse versiooni ja protsessi versiooni, välja arvatud juhul, kui toodetud komponendil on määratletud alamkooslus või alamprotsess.
    -   Arvutuste puhul eeldatakse, et toodetud kaupade puhul kasutatakse standardtellimuse kogust. Standardtellimuse kogus on aluseks komponendi koguste arvutamisel, asjakohaste koosluse versioonide ja protsessi versioonide määramisel (kui kasutate kogusetundlike koosluse versioone või protsessi versioone), ning püsikulude amortiseerimisel. Siiski, kui toodetud komponendil on kooslusrea tüüp **Tootmine** või **Hankija**, või kui kasutate koosluse kalkulatsioonideks vastavalt tellimusele tehtud koosnevusarvutuse režiimi, siis see eeldus ei kehti, kuna kogused kajastavad määratletud kalkulatsiooni kogust.
    -   Arvutamiskuupäeva või tegevuskohta saab kuluversiooniga volitada, või kasutajapõhiseid väärtusi saab seadistada, kui kuupäev või tegevuskoht pole kuluversioonis volitatud.

Muud koosluse kalkulatsioonide variatsioonid kajastavad kulutüüpi ja kuluversiooni piiranguid.

-   Standardkulusid kasutavaid koosluse kalkulatsioone peab piirama kuluversiooni poliitikatega, kuna piirangud aitavad tagada standardsete omahinna arvutamise põhimõtete kasutamist. Standardsed omahinna arvutamise põhimõtted nõuavad piirangute rakendamist ostetud kaupade standardsete kulude, ühetasemelise koosnevusarvutuse režiimi ja lisakulude kaasamise kohta ühiku hinda.
-   Plaanitud kulusid kasutavad koosluse kalkulatsioonid ei pea järgima standardseid omahinna arvutamise põhimõtteid. Need koosluse kalkulatsioonid võivad kasutada erinevaid koosnevusarvutuse režiime, ostetud kaupade kuluandmete alternatiivallikaid ja piirangute valikulist rakendamist kuluversiooni piires.

### <a name="bom-calculations-that-use-standard-costs"></a>Koosluse kalkulatsioonid, mis kasutavad standardseid kulusid

Kuluversiooni piires olevad põhimõtted (standardsete kulude puhul) võivad volitada viie koosluse kalkulatsiooni poliitika rakendamist. Kuluversioonis asuv suvand **Piirangu kirjendamine** volitab üht neist põhimõtetest, kus lisakulud peavad olema ühiku hinda kaasatud. Ostetud kaupade lisakulusid saab sisestada käsitsi, samas kui toodetud kaupade lisakulud kajastavad püsikulude arvutatud amortisatsiooni. Kuluversioonis asuv suvand **Kalkulatsioonipiirang** volitab ülejäänud nelja koosluse kalkulatsiooni poliitikat.

-   Ostetud kaupade kulupanuste allikas peab põhinema standardkuludel. Teisisõnu: koosluse kalkulatsioonid peavad kasutama kauba kulukirjeid määratletud kuluversiooni piires või standardseid kulusid sisaldavas taandes.
-   Täpse ja tervikliku standardkulude kalkulatsiooni tagamiseks peab koosnevusarvutuse režiim olema ühe tasandiga.
-   Kaupade müügihinna arvutamisel ühtlaste tulemuste tagamiseks peab kasumisäte olema volitatud. Kasumisätet saab kasutada ja kauba müügihinna kirjeid saab luua vaid siis, kui kuluversioon lubab müügihindade sisu.
-   Taande põhimõte peab olema volitatud ja seda saab määrata olekusse **Pole**, **Aktiivne** (aktiivsete kulukirjete puhul) või **Kuluversioon** (määratud kuluversiooni puhul).

### <a name="bom-calculations-that-use-planned-costs"></a>Koosluse kalkulatsioonid, mis kasutavad plaanitud kulusid

Kuluversiooni piires olevad põhimõtted (plaanitud kulude puhul) võivad valikuliselt volitada viie koosluse kalkulatsiooni poliitika rakendamist. Teise võimalusena pakuvad poliitikad vaid vaikeväärtusi. Kuluversioonis asuv suvand **Piirangu kirjendamine** määrab, kas koosluse kalkulatsiooni põhimõte lisakulude kohta on volitatud või toimib vaikeväärtusena. Lisakulusid saab valikuliselt kaasata ühiku hinda. Kuluversioonis asuv suvand **Kalkulatsioonipiirang** määrab, kas ülejäänud neli koosluse kalkulatsiooni põhimõtet on volitatud või toimivad vaikeväärtustena.

-   Ostetud kauba kulupanuste allikaks võivad olla kuluversioonis olevad kauba kulukirjed. Teise võimalusena võib allikat määratleda kaubale määratud koosluse kalkulatsioonigrupp. Näiteks saab koosluse kalkulatsioonigrupp määrata ostuhinna kaubanduslepped kulupanuse andmete allikana.
-   Koosnevusarvutuse režiim võib olla ühetasandiline, mitmetasandiline, tehtud vastavalt tellimusele või põhineda koosluserea kaubal. Koosluserea tüübi koosnevusarvutuse režiim kopeerib tootetellimuse hinnangute kuluarvutuste loogikat.
-   Kasumisäte võib olla volitatud või vaikeväärtus. Kasumisätet saab kasutada ja kauba müügihinna kirjeid saab luua vaid siis, kui kuluversioon lubab müügihindade sisu.
-   Taande põhimõte võib olla volitatud või vaikeväärtus. Taande põhimõtet saab määrata olekusse **Pole**, **Aktiivne** (aktiivsete kulukirjete puhul) või **Kuluversioon** (määratud kuluversiooni puhul).

Koosluse kalkulatsioonid loovad hoiatusteateid ja muud tüüpi teateid. Mitmed koosluse kalkulatsiooni põhimõtted määravad teadete tüübid. Hoiatustingimused on määratletud kaupadele määratud koosluse kalkulatsioonigrupis. Saate siiski koosluse kalkulatsiooni käivitamisel need hoiatustingimused alistada. Kui kasutate taandepõhimõtet, on sageli abiks taandeteabe kuvamine teabeteatena. Kui üritate värskendada arvutatud kulusid puuduvate kulukirjetega kaupadele, on abiks ka see, kui teabeteade tuvastab värskendamata kaupu.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Taande põhimõtet kasutavate koosluse kalkulatsioonid
Järgmised olukorrad näitavad taande põhimõtte kaht kasutamist:

-   **Kaheversiooniline meetod standardkulu värskendamiseks** \– kuluversioon võib hõlmata standardkulude astmelisi muutusi, nt ootel kulukirjeid, mis tähistavad uusi kaupu või kulu muudatusi. Sellisel juhul saab taande põhimõte tuvastada muudes kuluversioonides sisalduvate aktiivsete standardkulude kasutamist.
-   **Kulu mõju simuleerimine plaanitud kulude abil** \– plaanitud kulude kuluversioon võib simulatsiooni jaoks sisaldada astmelisi muutusi. See kuluversioon hõlmab ootel kulukirjeid, mis tähistavad kaupade, kulukategooriate ja kaudsete kulude arvutusvalemite simuleeritud kulu muudatusi. Sellisel juhul saab taande põhimõte tuvastada muudes kuluversioonides sisalduvate aktiivsete standardkulude kasutamist.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Soovitatava müügihinna koosluse arvutamine
Kui kasutate kulu pluss hinnalisandi meetodit, kajastab kauba arvutatud müügihind kasumit sätestavate protsentide kogumit, mis on määratud koosluse kalkulatsiooniks ja kuludeks, mis seostuvad kauba komponentidega, protsessi toimingutega ja asjakohaste tootmise üldkuludega. Hinnalisand kajastab kasumit sätestavaid protsente, mis on määratud kulugruppidele ja kaupadele määratud kulugruppidele, protsessi toimingute kulukategooriatele ning tootmise üldkulude kaudse kulu arvutamise valemitele. Kasumit sätestavate protsentide kogumid on tähistatud siltidega **Standardne**, **Kasum 1**, **Kasum 2** ja **Kasum 3**. Näiteks saab kogumis Kasum 1 määrata 50-protsendilise kasumit sätestava protsendi kulugrupile, mis on määratud ostetud materjalile, ja 80-protsendilise kasumit sätestava protsendi kulugrupile, mis on määratud protsessi toimingute kulugrupile. Koosluse arvutamise kontekst määrab, kuidas arvutatava müügihinna tulemusi käsitletakse.

-   **Koosluse arvutamine kauba ja määratud kuluversiooni jaoks** \– koosluse kalkulatsioon loob kuluversioonis ootel müügihinna kirje. See müügihinna kirje loob kalkulatsiooni üksikasjade vaatamiseks alguspunkti (näiteks lehel **Kauba kulu arvutamine**. Müügihinna kirje toimib peamiselt viiteteabena ja seda ei kasutata müügitellimuste müügihinna alusena.
-   **Tellimusekohane koosluse kalkulatsioon** \– lehe **Koosluse kalkulatsioon** variatsiooni kasutatakse müügitellimuse, müügipakkumise või hooldustellimuse rea kauba kontekstis. Tellimusekohane koosluse kalkulatsioon ei loo kirjet kuluversioonis. Selle asemel loob see kalkulatsioonikirje, mis kuvatakse lehel **Koosluse arvutamise tulemused**. See kalkulatsiooni kirje loob kalkulatsiooni üksikasjade vaatamiseks alguspunkti (näiteks lehel **Kauba kulu arvutamine**. Valitud kalkulatsiooni kirjet puudutavat teavet saab üle kanda algsele reaüksusele. Näiteks saab arvutatud müügihinda üle kanda müügitellimuse rea kaubale.

## <a name="order-specific-bom-calculations"></a>Tellimusepõhised koosluse kalkulatsioonid
Tellimusomane koosluse kalkulatsioon esindab koosluse arvutamise varianti toodetud kauba puhul. Tellimusekohase koosluse kalkulatsioon sooritatakse müügitellimuse müügipakkumise või müügitellimuse reaüksuse kontekstis. Tellimusekohane koosluse kalkulatsioon loob kalkulatsioonikirje, mis ilmub lehel **Koosluse kalkulatsiooni tulemused**. Kalkulatsioonikirje hõlmab arvutatud kaalu, arvutatu kulu (põhinevad aktiivsetel kulukirjetel) ning arvutatud müügihinda. Kalkulatsioonikirje, mille iga tellimusekohane kauba koosluse kalkulatsioon loob lehel **Koosluse kalkulatsiooni tulemused**, ainuidentifikaatoriks on kalkulatsiooni number. Kalkulatsioonikirje tulemusi saab valikuliselt üle kanda algsele reaüksusele. Tellimusekohane koosluse kalkulatsioon erineb toodetud kauba koosluse kalkulatsioonist kahel viisil.

-   Tellimusomane koosluse kalkulatsioon ei loo kauba kulukirjet hinnaarvestuse versiooni piires. See tähendab, et koosluse kalkulatsioonipoliitikaid ei rakendata kauba kulukirje loomisel või kulukirje üle kirjutamisel.
-   Tellimusomane koosluse kalkulatsioon kasutab alati aktiivseid kulukirjeid komponentide, kulukategooriate ja kaudsete kuluarvutusvalemite jaoks.





