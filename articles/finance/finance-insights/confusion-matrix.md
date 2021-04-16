---
title: Masinõppemudelite tulemused (eelversioon)
description: Selles teemas käsitletakse segaduse maatrikseid, klassifitseerimisprobleeme ja täpsust masinõppe (ML) mudelites. Eesmärk on parandada oma arusaamist ML-i prognoosimise tulemuste täpsusest.
author: ShivamPandey-msft
ms.date: 06/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-14
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d6e8f63ef00f714109ae650d3cedaf19e5159325
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818748"
---
# <a name="results-of-machine-learning-models-preview"></a>Masinõppemudelite tulemused (eelversioon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Selles teemas käsitletakse segaduse maatrikseid, klassifitseerimisprobleeme ja täpsust masinõppe (ML) mudelites. Eesmärk on parandada oma arusaamist ML-i prognoosimise tulemuste täpsusest. Sihtrühma kuuluvad insenerid, analüütikud ja juhid, kes soovivad luua oma teadmisi ja oskusi andmeteaduses.

## <a name="confusion-matrix"></a>Segaduse maatriks
Pärast seda kui jälgitav ML-i probleem on ajalooliste andmete komplekti põhjal koolitatud, seda testitakse kasutades andmeid, mis on koolitusprotsessist eemale jäänud. Sel viisil saate võrrelda koolitatud mudeli prognoose tegelike väärtustega. Segaduse maatriks annab võimaluse hinnata, kui edukas klassifitseerimise probleem on ja kus see teeb vigu (st kus see läheb segadusse).

Näiteks teie eesmärk on ennustada, kas lemmikloom on koer või kass, mis põhineb osadel füüsilistel ja käitumuslikel atribuutidel. Kui teil on testimise andmekomplektis 30 koera ja 20 kassi, võib segaduse maatriks sarnaneda järgmise illustratsiooniga.

![Liikide prognoosimise näide](media/species-prediction-matrix.png)

Roheliste lahtrite numbrid tähistavad õigeid prognoose. Nagu näete, mudel ennustas protsentuaalselt suurema osa kassidest õigesti. Mudeli üldist täpsust on lihtne arvutada. Sel juhul on see 42 ÷ 50 või 0,84.

### <a name="multi-class-classifiers-in-a-confusion-matrix"></a>Mitmeklassilised klassifikaatorid segaduse maatriksis

Enamik arutelusid segaduse maatriksis on keskendunud binaarsetele klassifikaatoritele, nagu eelmises näites. See juhtum on erijuhtum, kus võib kaaluda muid mõõdikuid, näiteks tundlikkust ja tagasikutsumist.

Järgmiseks vaatleme kolme olekuga finantsstsenaariumi klassifitseerimisprobleemi. Mudel ennustab, kas kliendiarve tasutakse õigel ajal, hilja või väga hilja. Näiteks 100 testarve seast 50 tasuti õigeaegselt, 35 tasuti hilja ja 15 tasuti väga hilja. Sel juhul võib mudel tekitada segaduse maatriksi, mis sarnaneb järgmise illustratsiooniga.

![Mudel 1](media/payment-prediction-matrix.png)]

Segaduse maatriks annab oluliselt rohkem teavet kui lihtne täpsusmõõdik. Samas see on seda suhteliselt lihtne mõista. Segaduse maatriks näitab, kas teil on tasakaalustatud andmekogum, kus väljundklassidel on sarnased arvud. Mitmeklassilise stsenaariumi puhul näitab see, kui kaugel võib ennustus olla, kui väljundklassid on järgklassid, nagu eelmises näites kliendimaksete kohta.

## <a name="model-accuracy"></a>Mudeli täpsus 
Erinevad täpsusmõõdikud on mudeli kvaliteedi kvantifitseerimise eeliseks. 

Kuna täpsus on kergesti mõistetav, on see hea lähtepunkt mudeli selgitamiseks teistele inimestele, eriti mudeli kasutajatele, kes ei ole andmeteadlased. Mudeli täpsuse mõistmiseks ei ole vaja statistikat. Kui segaduse maatriks on saadaval, annab see täiendava ülevaate mudeli jõudlusest.

Samas põhjalikuma arusaamise huvides tuleks siiski pöörata tähelepanu mitmetele täpsusega seotud probleemile. Mõõdik sõltub probleemi kontekstist. Küsimus, mis sageli tekib seoses mudeli tulemuslikkusega, on: „Kui hea mudel on?” Kuid vastata sellele küsimusele ei ole tingimata lihtne. Kaaluge järgmist segiajamise maatriksit (mudel 2).

![Makse ennustamise näide suurema näidisega](media/payment-prediction-matrix-2.png)

Kiire kalkulatsioon näitab, et selle mudeli täpsus on (70 + 10 + 3) ÷ 100 või 0,83. Eemalt vaadates tundub, et tulemus on parem kui eelmise mitme klassi mudeli tulemus (mudel 1), mis oli 0,73 täpsusega. Aga kas see on parem?

Selle küsimuse lahendamiseks arvestage naiivne oletuse täpsusega. Klassifikatsiooni probleemi puhul ennustab tavaline oletus alati kõige levinumat klassi. Mudeli 1 puhul on see „õigel ajal” ja see loob täpsuse 0,50. Mudeli 2 oletuse puhul on see „õigel ajal” ja see loob täpsuse 0,80. Kuna mudel 1 parandab naiivset oletust 0,73 – 0,50 = 0,23 võrra, siis mudel 2 parandab naiivset oletust 0,83 – 0,80 = 0,03 võrra, mistõttu mudel 1 on parem mudel, kuigi selle täpsus on väiksem. Arvutus näitab, et mudeli kvaliteedi tõhus hindamine nõuab rohkem konteksti kui täpsuse väärtus.

Tähelepanu väärib veel üks asjaolu. Kaaluge stsenaariumi, kus meditsiinilise testi abil tuvastatakse patsiendi haigus. See probleem on binaarne klassifikatsiooni probleem, kus positiivne tulemus näitab, et patsiendil on haigus. Selle stsenaariumi puhul tuleb mõelda järgmiste vigade mõjule.

- Valepositiivsed, kus test ütleb, et patsient on haige, kuid tegelikult tal haigust pole
- Valenegatiivsed, kus test ütleb, et patsiendil ei ole haigust, kuid tegelikult tal on haigus

Loomulikult, mõlemat tüüpi viga on soovimatu, kuid mis on halvem? Jällegi, see sõltub asjaoludest. Eluohtliku haiguse korral, mis nõuab kiiret ravi, on prioriteediks valenegatiivsete andmete minimeerimine (loodetavasti järgnevad sellele täiendavaid teste). Teiste vähem kriitiliste olukordade puhul võivad mudeli loojad selle asemel minimeerida valepositiivseid. Igal juhul on mõistlik järeldada, et mudeli kvaliteedi tõhususe määramiseks peab teil olema rohkem teavet kui täpsuse mõõdik annab.

### <a name="recommendations"></a>Soovitused

Täpsus on oluline vahend suhtlemiseks domeeni asjatundjatega, kes ei ole statistikaga tuttavad. Selleks, et teave oleks kasulik, on oluline, et täiendav kontekst antaks koos täpsuse väärtusega.

Makse prognoosimise stsenaariumi puhul saate seada eesmärgi ML-i mudeli jaoks, mis sisaldab erinevate makse käitumise tegureid. Eesmärk on, et mudel peaks paranema pärast naiivset oletust, vähendades valede vastuste arvu vähemalt 50 protsendi võrra. Teisisõnu on eesmärgiks täpsus, mis eraldab erineva täpsusega naiivse oletuse ja 100 protsenti.

Järgmises tabelis summeeritakse see põhimõte selle teema segaduse maatriksite jaoks.

| Mudel   | Naiivne oletus | Sihtkoht | Mudeli täpsus | Kas eesmärk on täidetud?                                          |
|---------|-------------|--------|----------------|-----------------------------------------------------------|
| Mudel 1 | 0.50        | 0.75   | 0.73           | Peaaegu. See mudel parandab oluliselt oletust. |
| Mudel 2 | 0.80        | 0.90   | 0.83           | Nr Parandamine on nõutav.                              |

## <a name="classification-f1-accuracy"></a>Klassifikatsiooni F1 täpsus

Selle teema lõplik kasu on täpsem mõõtmise klassifikatsioon ML-i jõudluse kohta, mida tuntakse kui F1 täpsuse nime all.

Enne kui F1 täpsust saab määratleda, tuleb kehtestada kaks täiendavat mõõdikut: täpsus ja tagasikutsumine. Täpsus näitab, mitu positiivsete prognooside koguarvu on õigesti määratud. Seda mõõdikut tuntakse ka positiivse prognoositava väärtusena. Tagasikutsumine on tegelike positiivsete juhtumite koguarv, mida ennustati õigesti. Seda mõõdikut nimetatakse ka tundlikkuseks.

[![Tegelikud tulemused vs valed tulemused](./media/tn-fn.png)](./media/tn-fn.png)

Eelmise illustratsiooni segiajamise maatriksis arvutatakse need mõõdikud järgmiselt.

- Täpsus = TP ÷ (TP + FP)
- Tagasikutsumine = TP ÷ (TP + FN)

F1 mõõt ühendab täpsust ja tagasikutsumist. Tulemuseks on kahe väärtuse harmooniline keskväärtus. See arvutatakse järgmiselt.

- F1 = 2 × (täpsus × tagasikutsumine) ÷ (täpsus + tagasikutsumine)

Vaatame konkreetset näidet. Selle teema alguses oli näide mudelist, mis ennustas, kas loom on koer või kass. Illustratsiooni korratakse siin.

[![Liikide prognoosi näide (korduv)](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)

Siin on tulemused, kui positiivse vastusena kasutatakse valikut „koer”.

- Täpsis = 24 ÷ (24 + 2) = 0,9231
- Tagasikutsumine = 24 ÷ (24 + 6) = 0,8
- F1 = 2 × (0,9231 × 0,8) ÷ (0,9231 + 0,8) = 0,8572

Nagu näete, on F1 väärtus täpsuse ja tagasikutsumise väärtuste vahel.

Kuigi F1 täpsust ei ole nii lihtne mõista, lisab see nüansse täpsuse üldise täpsuse numbrile. Samuti võib see aidata tasakaalustamata andmekogumite puhul, kuna kuvatakse järgmine arutelu.

Selle teema jaotises [Mudeli täpsus](#model-accuracy) võrreldi järgmisi kahte segiajamise maatriksit. Kuigi esimesel mudelil oli madalam täpsus, peeti seda kasulikumaks mudeliks, sest see näitas suuremat paranemist, kui õigeaegselt tasumine.

![Makse ennustus vs. tegelike näide](media/payment-prediction-matrix.png)

![Makseprognoosi näide suurema valimiga (korduv)](media/payment-prediction-matrix-2.png)

Vaatame, kuidas neid kahte mudelit võrreldakse, kui kasutatakse F1 skoori. F1 skoori koefitsiendi täpsusega ja tagasikutsumisega on iga oleku jaoks ja F1 makro arvutamine seejärel keskmiselt F1 skoor kõikide olekute üleselt, et määrata üldine F1 skoor. On ka teisi F1 variante, kuid suurem huvi on kasutada makro versiooni, arvestades kõigi kolme oleku võrdset kaalumist.

Arvutuste lihtsustamiseks ehitati valimi massiivid, et sobitada tegelike ja prognoositavate väärtustega. Need massiivid kasutasid Pythonis sklearni mõõdikute teeki, et arvutada väärtused. Tulemus on järgmine.

| Mudel   | Naiivne oletus | Täpsus | F1 makro |
|---------|-------------|----------|----------|
| Mudel 1 | 0.5         | 0.73     | 0.67     |
| Mudel 2 | 0.80        | 0.83     | 0.66     |

Üksikasjalikumat teavet selle kalkulatsiooni töötamise kohta leiate sklearni mõõdikute klassifikatsiooni aruandest mudelile 1. Kolm olekut „õigel ajal”, „hilja” ja „väga hilja” tähistavad ridu, mis on vastavalt märgistatud kui 1, 2 ja 3. Makro keskmine on ainult veeru F1 skoori keskmine.

|           | täpsus | tagasikutsumine   | f1-score |
|-----------|-----------|----------|----------|
| **1**     | 0.83      | 0.80     | 0.82     |
| **2**     | 0.68      | 0.71     | 0.69     |
| **3**     | 0.50      | 0.50     | 0.50     |

Need tulemused näitavad, et kahel mudelil on peaaegu identne F1 makro täpsuse punktisumma. Selles ja paljudel muudel juhtudel annab F1 täpsus mudeli võimekuse parema näidiku. Täpsuse puhul nõuab tulemuste tõlgendamine, et mõistaksite, millega tuleb mudelis arvestada.

#### <a name="privacy-notice"></a>Privaatsusavaldus
Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]