---
title: Integreeritud koondplaneerimise ja planeerimise optimeerimise vahelised erinevused
description: Selles teemas loetletakse funktsioonid, mida plaanimise optimeerimine veel ei toeta ja mida pole loetletud planeerimise optimeerimise sobivuse analüüsi lehel.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: c73587015d6714c409819ab19ad68685aaa71cf7
ms.sourcegitcommit: 70289a33b0a6ff3f9418d91a928db452cfd815bd
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2022
ms.locfileid: "8618256"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Integreeritud koondplaneerimise ja planeerimise optimeerimise vahelised erinevused

[!include [banner](../../includes/banner.md)]

Plaanimise optimeerimise tulemused võivad erineda integreeritud koondplaneerimise mootori tulemustest. Erinevusi võivad põhjustada ootel funktsioonid. Selles teemas loetletakse funktsioonid, mida plaanimise optimeerimine veel ei toeta ja mida pole loetletud lehel **[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)**].

| Funktsioon | Plaanimise optimeerimise praegune käitumine |
|---|---|
| Tegeliku kaaluga tooted | Tegeliku kaaluga tooteid peetakse tavalisteks toodeteks.|
| Laiendatavad dimensioonid | Laiendatavad dimensioonid on plaanitud tellimustel tühjad, isegi kui märkeruut **Laovarude planeerimine dimensioonide kaupa** on lehel **Laoala dimensioonigrupid** või **Jälgimisdimensioonigrupid** valitud. |
| Filtreeritud tootmiste käitamised | Lisateavet vt jaotisest [Tootmise planeerimine - filtrid](production-planning.md#filters). |
| Eelarveplaanimine | Prognooside planeerimist ei toetata. Soovitame teil kasutada koondplaneerimist seal, kus koondplaanile on määratud prognoosimudel. |
| Numbrijada plaanitud tellimustele | Numbrijadasid plaanitud tellimustele ei toetata. Plaanitud tellimuste numbrid luuakse teeninduse poolel. Plaanitud tellimuse numbrit näidatakse tavaliselt 10 numbriga, kuid järjestus on tegelikult üles ehitatud 20 tähemärgile, 10 numbrid tähistavad planeerimiste arvu ja ülejäänud 10 numbrit plaanitud tellimuste arvu. |
| Plaani kopeerimine, plaani kustutamine ja plaani versiooni puhastamine | <p>Järgmised üksused on navigeerimispaani jaotises **Koondplaneerimine \> Koondplaneerimine \> Plaanide haldamine** keelatud.</p><ul><li>Plaani koopia</li><li>Kustuta plaan</li><li>Plaani versiooni puhastamine</li></ul> |
| Tagastustellimused | Tagastustellimusi ei arvestata. |
| Planeerimisega seotud funktsioonid | Üksikasju vt teemast [Planeerimine lõpmatu võimsusega](infinite-capacity-planning.md#limitations). |
| Puhvervaru täitmine | Planeerimise optimeerimine kasutab alati *Tänane kuupäev + hankeaeg* valikut **Täitke minimaalselt** välja **Toode katvus** lehe jaoks. See aitab vältida soovimatuid planeeritud tellimusi ja muid probleeme, sest kui turvavarude hankimise aega ei arvestata, lükkuvad väheste varude jaoks loodud kavandatud tellimused alati tähtaja tõttu edasi. |
| Ohutusvaru sidumine ja võrgunõuded | *Turvavarud* nõude tüüp ei kuulu komplekti ja seda ei kuvata lehel **Võrgu nõuded**. Turvavarud ei kujuta endast nõudlust ega ole seotud nõude kuupäevaga. Selle asemel seab see piirangu sellele, kui palju laoseisu peab alati olema. Planeeritud tellimuste arvutamisel üldplaneerimisel võetakse siiski arvesse välja väärtust **Minimum**. Soovitame teil vaadata lehe **Võrgu nõuded** veergu **Kogunenud kogus**, et näha, kas seda väärtust arvestati. |
| Transpordikalendrid | Väärtust lehe **Tarneviisid** veerus **Transpordikalender** eiratakse. |
| Min/max kattekood ilma väärtusteta| Kui kasutate integreeritud plaanimismootorit min/max laovarude koodi, kus pole seadistatud minimaalseid või maksimaalseid väärtusi, käsitleb planeerimismootor kattekoodi vajadusena ja loob iga vajaduse kohta ühe tellimuse. Planeerimise optimeerimise puhul loob süsteem ühe tellimuse päeva kohta, et katta kogu selle päeva summa.  |
| Netonõuded ja käsitsi loodud plaanitud tellimused | Integreeritud plaanimismootoriga kuvatakse kaubale käsitsi loodud tarnetellimused selle kauba netonõuete hulgas automaatselt. Näiteks ostutellimuse loomisel müügitellimusest kuvatakse ostutellimus netonõuete lehel, **ilma** et oleks vaja eelnevaid tegevusi. Seda seetõttu, et integreeritud plaanimismootor logib `inventLogTTS` tabelisse laokanded ja **näitab muudatusi dünaamiliste plaanide** netonõuete lehel. Kuid planeerimise optimeerimise puhul ei kuvata käsitsi loodud tellimusi kauba netonõuete hulgas enne, kui optimeerimine on **\> käitatud (kasutades plaani, mis sisaldab kaupa),** **või** kuni valite netonõuete lehel tegevuspaanil koondplaneerimise värskendamine, mis käivitab kauba koondplaanimise. Lisateavet selle kohta, kuidas netonõuete lehega **töötada**, [vt Netonõuded ja sidumisteave planeerimise optimeerimisega](net-requirements.md). |

## <a name="additional-resources"></a>Lisaressursid

- [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)
- [Parameetrid, mida planeerimise optimeerimine ei kasuta](not-used-parameters.md)
- [Kuupäeva ja kellaaja parameetrid, mida planeerimise optimeerimine ei kasuta](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
