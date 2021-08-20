---
title: Algse kliendimakse prognoosimise mudeli hindamine (eelversioon)
description: See teema kirjeldab samme, mida saate teha kliendimakse prognoosimise mudeli mõistmiseks ja selle tõhususe hindamiseks.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: f45392d540b6696d23261a6b2197c3185f5ede2b7c646f6b751480145dcacfdc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768863"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Algse kliendimakse prognoosimise mudeli hindamine (eelversioon)

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas hinnata prognoosimise mudelit pärast seda, kui olete finantsülevaated sisse lülitanud ning loonud ja treeninud oma esimese mudeli. See teema käsitleb kliendimaksete prognoosimise mudeleid. See kirjeldab samme, mida saate teha kliendimakse prognoosimise mudeli mõistmiseks ja selle tõhususe hindamiseks.

## <a name="getting-details-about-the-model"></a>Mudeli üksikasjade hankimine

Rakenduse Microsoft Dynamics 365 Finance lehel **Finantsülevaadete parameetrid** ilmub täpsuse skoori kõrval link **Mudeli täpsuse parandamine**.

[![Mudeli täpsuse parandamise link.](./media/prediction-model.png)](./media/prediction-model.png)

See link viib teid AI Builderisse, kus saate lisateavet praeguse mudeli kohta ja võtta lisaks meetmeid selle parandamiseks. Järgmisel joonisel näidatakse avatud lehte.

[![AI Builder.](./media/what-to-predict.png)](./media/what-to-predict.png)

Avaneb leht kuvab järgmist teavet.

- Jaotises **Jõudlus** annab mudeli jõudluse klass mudeli kvaliteedi kohta perspektiivi. Lisateavet selle klassi kohta vt AI Builderi dokumentatsiooni teemast [Prognoosi mudeli jõudlus](/ai-builder/prediction-performance).
- Jaotis **Kõige mõjukamad andmed** näitab, kui olulised olid teie mudeli jaoks eri andmete sisestustüübid. Saate hinnata seda loendit ja vastavaid protsente, et teha kindlaks, kas teave on kooskõlas sellega, mida te oma ettevõtte ja turu kohta teate.

    [![Prognoosi mudeli jõudluse ja kõige mõjukamate andmete jaotised.](./media/models.png)](./media/models.png)

- Valige jaotises **Jõudlus** suvand **Kuva üksikasjad**, et saada lisateavet klassi ja teiste kaalutluste kohta. Järgmisel illustratsioonil näitavad üksikasjad, et mudel kasutab soovitatust vähem teavet. Seetõttu on süsteem loonud hoiatusteate.

    [![Hoiatused mudeli jõudluse kohta.](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Süvitsi minemine

Kuigi täpsus on mudeli hindamiseks hea lähtepunkt ja jõudluse klass lisab perspektiivi, pakub AI Builder üksikasjalikumaid mõõdikuid, mida saate oma hinnangus kasutada. Üksikasjade allalaadimiseks valige jaotises **Jõudlus** kolmikpunkti nupp (**…**), mis asub nupu **Kasuta mudelit** kõrval, ja valige seejärel käsk **Laadi alla üksikasjalikud mõõdikud**.

[![Üksikasjalike mõõdikute allalaadimise käsk.](./media/performance.png)](./media/performance.png)

Järgmine illustratsioon näitab vormingut, milles saate andmed alla laadida.

[![Allalaaditud andmete vorming.](./media/data-format.png)](./media/data-format.png)

Tulemuste põhjalikumaks analüüsiks on hea lähtepunkt vaadata läbi mõõdik „Segiajamise maatriks”. Näiteks siin on andmed, mis kuvatakse selle mõõdiku jaoks eelmisel illustratsioonil.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

Saate neid andmeid laiendada järgmisel viisil.

| &nbsp;                   | Prognoositud õigel ajal | Prognoositud hilja | Prognoositud väga hilja |
|--------------------------|-------------------|----------------|---------------------|
| Tegelikud õigeaegsed maksed   | **71**            | 0              | 21                  |
| Tegelikud hilinenud maksed      | 5                 | **0**          | 27                  |
| Tegelikud väga hilinenud maksed | 2                 | 0              | **45**              |

Segiajamise maatriks näitab koolitusprotsessi juhuslikult valitud testi andmekogumi tulemusi. Kuna neid suletud arveid ei kasutatud mudeli treenimiseks, on need mudeli jaoks hea testjuhtumid. Lisaks kuna arve tegelik olek on teada, saab vaadata ka mudeli jõudlust.

Esimese asjana tuleb vaadata kõige levinumat tegelikku väärtust. Kuigi see väärtus ei pruugi olla üldise andmekomplektiga täielikult joondatud, on see mõistlik umbkaudne seis. Sel juhul leiab suvand **Tegelikud õigeaegsed maksed** aset 92 korral 171 arvest kokku ja on kõige levinum tegelik väärtus. Seega on see teie mudeli jaoks hea algväärtus. Kui te lihtsalt arvasite, et kõik arved saavad olema tasutud õigeaegselt, siis oli teil õigus 92 korral 171 korrast kokku (st 54 protsenti ajast).

Oluline on mõista, kui tasakaalus teie andmekomplekt on. Antud juhul, 92 arvet 171-st arvest tasuti õigeaegselt, 32 tasuti hilja ja 47 tasuti väga hilja. Need väärtused näitavad mõistlikult tasakaalustatud andmekomplekti, kuna igas klassifikatsioonis on ebatavalisi tulemusi. Olukord, kus ühel olekul on väga vähe tulemusi, võib olla masinõppemudeli jaoks väljakutseks.

Mudeli täpsus näitab testi andmekogumi korrektsete prognooside arvu. Need korrektsed prognoosid on väärtused, mis on eelises näites näidatud paksus kirjas. Antud juhul on väärtuste arvutatud täpsus 67,8 protsenti (= \[71 + 0 + 45\] ÷ 171). See väärtus näitab võrreldes algtaseme oletusega 54 protsenti paranemist 14 protsendi võrra ja on mudeli kvaliteedi üks näitaja.

Kui vaatate segiajamise maatriksit lähemalt, siis märkate, et mudel teeb head tööd õigeaegsete ja väga hiliste arvete tasumiste prognoosimisel. Samas see eksib 32 arve puhul, mis tegelikult tasuti hilja (kuid mitte liiga hilja). See tulemus viitab sellele, et nõutav on mudeli täiendav uurimine ja parandamine.

Arv, mis näitab mudeli jõudlust täpsusest paremini, on F1 makro skoor. See skoor arvestab iga klassifikatsiooni oleku tulemustega (õigel ajal, hilja ja väga hilja). Näiteks siin on andmed, mis kuvatakse F1 makro mõõdiku jaoks eelmisel illustratsioonil.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

Sel juhul näitab F1 makro skoor ligikaudu 49,3 protsenti, et olenemata küllaltki kõrgele üldisele täpsuse skoorile ei paku mudel tõhusaid prognoose iga oleku kohta.

## <a name="improving-the-model"></a>Mudeli parandamine

Pärast oma esimese mudeli tulemuste paremini mõistmist võite tahta oma mudelit parandada, lisades või eemaldades funktsioonide veerge või filtreerides mis tahes andmekomplektide osi, mis ei toeta täpseid prognoose. Sulgege AI Builder ja kasutage seejärel linki **Mudeli parandamine** rakenduses Dynamics 365 Finance, et taaskäivitada AI Builderi protsess. Saate eksperimenteerida erinevate omadustega ilma avaldatud mudelit mõjutamata. Avaldatud mudel on mõjutatud ainult siis, kui valite nupu **Avalda**. Pidage meeles, et teie rakenduse Dynamics 365 Finance eksemplari jaoks kasutatakse ühte mudelit. Seega peate enne selle avaldamist hoolikalt vaatama läbi kõik uued mudelid.

## <a name="for-more-information"></a>Lisateave

Lisateavet prognooside mudelite hindamise kohta vt teemast [Masinõppemudelite tulemid](/confusion-matrix.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
