---
title: Erinevused plaanimise optimeerimise ja taunitud koondplaneerimise mootori vahel
description: Selles artiklis loetletakse funktsioonid, mida plaanimise optimeerimine veel ei toeta ja mis pole loetletud planeerimise optimeerimise sobivuse analüüsi lehel.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745357"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Erinevused plaanimise optimeerimise ja taunitud koondplaneerimise mootori vahel

[!include [banner](../../includes/banner.md)]

Plaanimise optimeerimise tulemused võivad erineda taunitud koondplaneerimise mootori tulemustest. Erinevusi võivad põhjustada ootel funktsioonid. Selles artiklis loetletakse funktsioonid, mida plaanimise optimeerimine veel ei toeta ja mis pole loetletud planeerimise optimeerimise **[sobivuse analüüsi](planning-optimization-fit-analysis.md)** lehel.

| Funktsioon | Plaanimise optimeerimise praegune käitumine |
|---|---|
| Tegeliku kaaluga tooted | Tegeliku kaaluga tooteid peetakse tavalisteks toodeteks.|
| Laiendatavad dimensioonid | Plaanimise optimeerimine ei toeta laiendavaid dimensioone. Kui kasutate planeerimise optimeerimist, on laiendatavad dimensioonid plaanitud tellimustel tühjad, **isegi** kui laoala dimensioonigruppide või jälgimisdimensioonigruppide lehel **on** **märgitud ruut Laovarude plaan dimensiooni** järgi. |
| Filtreeritud tootmiste käitamised | Lisateavet vt jaotisest [Tootmise planeerimine - filtrid](production-planning.md#filters). |
| Eelarveplaanimine | Prognooside planeerimist ei toetata. Soovitame teil kasutada koondplaneerimist seal, kus koondplaanile on määratud prognoosimudel. |
| Numbrijada plaanitud tellimustele | Numbrijadasid plaanitud tellimustele ei toetata. Plaanitud tellimuste numbrid luuakse teeninduse poolel. Plaanitud tellimuse numbrit näidatakse tavaliselt 10 numbriga, kuid järjestus on tegelikult üles ehitatud 20 tähemärgile, 10 numbrid tähistavad planeerimiste arvu ja ülejäänud 10 numbrit plaanitud tellimuste arvu. |
| Plaani kopeerimine, plaani kustutamine ja plaani versiooni puhastamine | <p>Järgmised üksused on navigeerimispaani jaotises **Koondplaneerimine \> Koondplaneerimine \> Plaanide haldamine** keelatud.</p><ul><li>Plaani koopia</li><li>Kustuta plaan</li><li>Plaani versiooni puhastamine</li></ul> |
| Tagastustellimused | Tagastustellimusi ei arvestata. |
| Planeerimisega seotud funktsioonid | Üksikasju vt teemast [Planeerimine lõpmatu võimsusega](infinite-capacity-planning.md#limitations). |
| Puhvervaru täitmine | Planeerimise optimeerimine kasutab alati *Tänane kuupäev + hankeaeg* valikut **Täitke minimaalselt** välja **Toode katvus** lehe jaoks. See aitab vältida soovimatuid planeeritud tellimusi ja muid probleeme, sest kui turvavarude hankimise aega ei arvestata, lükkuvad väheste varude jaoks loodud kavandatud tellimused alati tähtaja tõttu edasi. |
| Ohutusvaru sidumine ja võrgunõuded | *Turvavarud* nõude tüüp ei kuulu komplekti ja seda ei kuvata lehel **Võrgu nõuded**. Turvavarud ei kujuta endast nõudlust ega ole seotud nõude kuupäevaga. Selle asemel seab see piirangu sellele, kui palju laoseisu peab alati olema. Planeeritud tellimuste arvutamisel üldplaneerimisel võetakse siiski arvesse välja väärtust **Minimum**. Soovitame teil vaadata lehe **Võrgu nõuded** veergu **Kogunenud kogus**, et näha, kas seda väärtust arvestati. Kuna sidumine on erinev, võidakse soovitada erinevaid tegevusi. |
| Transpordikalendrid | Väärtust lehe **Tarneviisid** veerus **Transpordikalender** eiratakse. |
| Min/max kattekood ilma väärtusteta| Taunitud koondplaneerimise mootoriga, kui kasutate min/max laovarude koodi, kus pole määratud miinimum- või maksimumväärtusi, käsitleb planeerimismootor kattekoodi vajadusena ja loob iga vajaduse kohta ühe tellimuse. Planeerimise optimeerimise puhul loob süsteem ühe tellimuse päeva kohta, et katta kogu selle päeva summa.  |
| Netonõuded ja käsitsi loodud plaanitud tellimused | Taunitud koondplaneerimise mootoriga kuvatakse kaubale käsitsi loodud tarnetellimused selle kauba netonõuete hulgas automaatselt. Näiteks ostutellimuse loomisel müügitellimusest kuvatakse ostutellimus netonõuete lehel, **ilma** et oleks vaja eelnevaid tegevusi. Seda seetõttu, et taunitud koondplaneerimise `inventLogTTS`**mootor logib varude kanded tabelisse ja näitab muudatusi dünaamiliste** plaanide netonõuete lehel. Kuid planeerimise optimeerimise puhul ei kuvata käsitsi loodud tellimusi kauba netonõuete hulgas enne, kui optimeerimine on **\> käitatud (kasutades plaani, mis sisaldab kaupa),** **või** kuni valite netonõuete lehel tegevuspaanil koondplaneerimise värskendamine, mis käivitab kauba koondplaanimise. Lisateavet selle kohta, kuidas netonõuete lehega **töötada**, vt Netonõuded [ja sidumisteave](net-requirements.md). |
| Ressursi määramine | Piiramatu võimsusega töötamisel määrab taunitav koondplaanimise mootor kõik plaanitud tellimused antud ressursigrupis samale ressursile. Plaanimise optimeerimine parandab seda, valides juhuslikult ressursse, et erinevad tootmistellimused saaksid kasutada erinevaid ressursse. Kui soovite kasutada sama ressurssi kõigi plaanitud tellimuste puhul, peate protsessis määrama selle ressursi. |
| Laiendatud andmetüübid (EDT-d) | Plaanimine optimeerimine ei toeta EDT-de täpsuse muudatusi. See tähendab, et protsessi ei toetata ametlikult ja see ei ole enam töö jaoks tagatud. |
| Puhvervaru täitmine | Plaanimise optimeerimise puhul kasutatakse **alati täitmise miinimumi** *, mis on tänane kuupäev + hankeaeg*. See valmistab süsteemi ette tulevikus lihtsustatud plaanimisseadistuse kasutamiseks ja annab tegevustava tulemuse. Kui ohutusvaru puhul hankeaega ei kaasata, hilineb madala vaba kaubavaru jaoks loodud plaanitud tellimus täitmisaja tõttu alati. Selline käitumismudel võib põhjustada palju müra ja soovimatuid plaanitud tellimusi. Parim tava on muuta sätet, et kasutada tänast *kuupäeva + hankeaega*. Värskendage koondandmeid, et vältida hoiatusi. |
| Staatilise plaani kopeerimine dünaamilisse plaani | Planeerimise optimeerimine ei kopeeri staatilisi plaane dünaamilisse plaani, hoolimata koondplaneerimise **parameetrite lehe sättest**. Üldiselt on see toiming vähem oluline, kuna planeerimis optimeerimise pakub kiirust ja täielikku taastootmist. Kui kasutatakse kaht või enamat plaani, tuleb iga plaani jaoks käivitada koondplaneerimine. |

## <a name="additional-resources"></a>Lisaressursid

- [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)
- [Parameetrid, mida planeerimise optimeerimine ei kasuta](not-used-parameters.md)
- [Kuupäeva ja kellaaja parameetrid, mida planeerimise optimeerimine ei kasuta](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
