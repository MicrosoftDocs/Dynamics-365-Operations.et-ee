---
title: Tulu eraldamine
description: See artikkel selgitab, kuidas kasutada tulu eraldamist kordustellimuse arvelduses.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 18739e0871592bc9eefcdf00f67dd4dd18f5d6f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864364"
---
# <a name="revenue-allocation"></a>Tulu eraldamine

See artikkel selgitab, kuidas seadistada tulu eraldusparameetreid arveldusgraafiku jaoks. Tulu eraldamise saate seadistada või muuta arveldusgraafiku loomisel. Aktiivse või lõpetatud **arveldusgraafiku** tulueralduse lehe avamisel on väljad kirjutuskaitstud.

## <a name="specify-the-revenue-allocation-for-a-billing-schedule"></a>Määrake tulu eraldamine arveldusgraafiku jaoks

Arveldusgraafiku tulu eralduse määramiseks järgige neid samme.

1. Valige kõigi **/aktiivsete arveldusgraafikute** loendilehel arveldusgraafik või arveldusgraafiku rida.
2. **Valige lehe ülaosas** oleval vahekaardil Tulu eraldamine suvand Tulu **eraldamine**.
3. Valige mitme **elemendi kokkuleppetüübi** väljal mitme elemendi kokkulepe (MEA).
4. Väljal Mitme **elemendi kokkulepe number** määrake MEA-number. Seejärel määrake väljal **Viitlepingu tulukonto** viitlepingu tulukonto.

    Kui seate mitme **elemendiga kokkuleppe tüübi** välja väärtuseks **Üksik**, **·** **kehtivad** igale reale sama mitme elemendi kokkuleppe number ja viit-lepingu tulu konto väärtused. Kui seate mitme **elemendiga kokkuleppe tüübi** **välja väärtuseks Kordne**, **·** **saate** igale reale määrata erineva mitme elemendi kokkuleppe numbri ja viit-lepingu tulu konto väärtused.
    
    MEA-numbrit saab määrata ainult kahele või enamale kaubale. Ühel real ei saa olla oma MEA-numbrit.

5. Valige käsk **Salvesta**.

### <a name="fields"></a>Väljad

Mitme **elemendiga sisukorra** leht sisaldab järgmisi välju.

| Väli | Kirjeldus |
|---|---| 
| Mitme elemendi paigutuse tüüp | <p>Valige kandele MEA-tüüp:</p><ul><li>**Kordne** – kandes olevad reaüksused on MEA osa või on olemas rohkem kui üks korraldus.</li><li>**Pole** – kanne on standardne kanne, mille puhul tulu ei eraldata.</li><li>**Üksik** – kõik kandes olevad kaubad on ühe MEA osa.</li></ul> |
| Mitme elemendi paigutuse number | <p>Rea MEA-number. See väli on saadaval, kui mitme **elemendiga korraldustüübi** välja väärtuseks on seatud **Kordne**.</p><p>Kui see väli on tühi ja te määrate MEA-numbri, **·** **uuendatakse** eraldiseisev müügihinna päritolu ja eraldiseisev müügihinna väljad automaatselt kauba eraldi müügihinna lehe väärtuste **alusel.** Saadaval on ainult müügitellimuse teistele ridadele määratud MEA-numbrid.</p> |
| Edasi lükatud lepingu tulude konto | Määratlege konto, mida kasutada töölehe sisestuste jaoks MEA lepingu arve loomisel. See väli on saadaval ainult korduva lepingu arvelduse kasutamisel. |
| **Read** | |
| Variandi number | Müügitellimuse variandinumber. |
| Kaubakood | Kauba kood müügitellimusest. |
| Arveldamissagedus | Tulu eraldamise sagedus: kord **päevas**, kord **kuus**, **kvartali** kaupa, **poolaasta või** kord **aastas**. |
| Kogus | Müügitellimuse väärtus. |
| Lepingu väärtus | Lepingu väärtus. |
| Mitme elemendi paigutuse number | <p>Rea MEA-number. See väli on saadaval, kui mitme **elemendiga korraldustüübi** välja väärtuseks on seatud **Kordne**.</p><p>Kui see väli on tühi ja te määrate MEA-numbri, **·** **uuendatakse** eraldiseisev müügihinna päritolu ja eraldiseisev müügihinna väljad automaatselt kauba eraldi müügihinna lehe väärtuste **alusel.** Saadaval on ainult müügitellimuse teistele ridadele määratud MEA-numbrid. Kui neid väärtusi ei ole kauba jaoks seadistatud, kasutatakse mitme **elemendi tulu eraldusparameetrite** lehe väärtusi.</p> | 
| Eraldiseisva müügihinna lähtekoht | <p>Eraldiseisev müügihinna päritolu:</p><ul><li>**Summa** – eraldiseisev müügihind on summa, mille määrate rohkem kui 0 (null). Summa teisendatakse vastavalt vajadusele funktsionaalsete ja algsete valuutade vahel.</li><li>**Baasmüügihind** – eraldiseisev müügihind vastab kauba baasmüügihinnale.</li><li>**Arve hind** – eraldiseisev müügihind vastab kauba arvehinnale.</li><li>**Kauba** protsent – eraldiseisev müügihind määratakse protsendi väärtusena ja arvutatakse kauba hinna alusel. Kui see suvand on valitud, määrake vaikeprotsent.</li><li>**Eraldage järelejääv** summa *– eraldi müügihinna päritolu arvutatakse emakauba kogu lepinguväärtusena* – *tütarüksuste eraldiseisev müügihind kokku*:</p><ul><li>*Emakauba kogu lepinguväärtus* on neto- või arveldatud summa.</li><li>*Tütarüksuste eraldiseisev* müügihind kokku on kõigi tütarüksuste laiendatud või lepingu eraldi müügihinna summa, v.a tütarkaup, mis kasutab seda eraldiolevat müügihinna päritolu.</li></ul><p>Kui arvutatud summa on negatiivne väärtus, seatakse summaks 0 (null).</p><p>**Märkus:** seda valikut saab tulu tükeldades valida ainult ühe tütarkauba puhul.</p></li><li>**Pole** – eraldi müügihinna päritolu põhineb tütarüksustel. See valik kehtib kaupadele, mis on määratletud tulu tükeldamismallis emaüksustena. Kui on **märgitud ruut** Tulu tükeldamine, valitakse see suvand automaatselt ning sätet ei saa muuta.</li><li>**Emaarve hinna** protsent – eraldi müügihinna päritolu on emakauba arvehinna protsent. See valik on saadaval ainult tulu tükeldamismallis tütarüksuste puhul.</li><li>**Emastandardi** protsent – eraldi müügihinna päritoluks on emakauba standardhinna protsent. See valik on saadaval ainult tulu tükeldamismallis tütarüksuste puhul. Kui **tütarkauba** **·** **·** **valik** muudetakse emastandardi hinna protsendist emaarvehinna protsendiks või emaarve hinna protsendiks emastandardi hinna protsendiks, uuendatakse ka arvutatud väärtused.</li></ul> |
| Eraldiseisev müügihind | <p>Rea eraldi müügihind kandevaluutas.</p><p>Väärtus väljal Summa on **kas** sisestatud või arvutatud.</p> |
| Lepingust eraldiseisev müügihind | Lepingu eraldiseisev müügihind. |
| Allesjäänud lepingu tulu | Lepingu järelejäänud tulu summa. See summa on kõigi nende ridade summa, mille jaoks pole arveid veel loodud. |
| Lepingu tulu kokku | Rea kogu lepingutulu summa See summa on kõigi ridade summa, sõltumata sellest, kas arved on nende jaoks loodud. |
| Edasi lükatud lepingu tulude konto | <p>Määratlege konto, mida kasutada töölehe sisestuste jaoks MEA lepingu arve loomisel.</p><p>See väli on saadaval ainult korduva lepingu arvelduse kasutamisel.</p> |
| Viga | Tulu eraldamisel ilmnenud tõrked. |

## <a name="use-revenue-allocation-on-a-sales-order"></a>Kasuta müügitellimusel tulu eraldust

Müügitellimusel tulu eraldusfunktsiooni kasutamiseks järgige neid samme.

1. **Looge leheküljel Kõik müügitellimused** kaupadega müügitellimus.
2. Valige vahekaardi **Arve** jaotises Tulu eraldamine **suvand** Tulu **eraldamine**.
3. Valige mitme **elemendiga kokkuleppetüübi** väljal MEA-tüüp.
4. Väljal Mitme **elemendi kokkulepe number** määrake MEA-number.
5. Kui mitme **elemendi tüüpi väli** on seatud väärtusele **Kordne**, valige soovitud read ja valige suvand **Rakenda valile**.
6. Valige käsk **Salvesta**.

Kui kasutate tulu- ja kulu viitvõlgu, luuakse viitvõlagraafik automaatselt. Seda saate vaadata lehel **Kõik viitvõlagraafikud**.
