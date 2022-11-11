---
title: Eelarve planeerimise koefitsiendid
description: Selles artiklis esitatakse näited, mis näitavad, kuidas seadistada vähendusvõtit. Selles on teave mitmesuguste planeerimise koefitsiendi sätete ja nende tulemuste kohta. Planeerimise koefitsiendi abil saate määratleda, kuidas eelarvevajadusi vähendada.
author: t-benebo
ms.date: 04/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqReduceKeyDefaultDataWizard, ReqReduceKey
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0efd7245d100730622e9862554f484ed6b17d1ed
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739920"
---
# <a name="forecast-reduction-keys"></a>Eelarve planeerimise koefitsiendid

[!include [banner](../includes/banner.md)]

See artikkel annab teavet erinevate meetodite kohta, mida kasutatakse eelarvenõuete vähendamiseks. Iga meetodi tulemuste kohta on toodud näited. Samuti selgitatakse, kuidas eelarve planeerimise koefitsienti luua, seadistada ja kasutada. Mõni meetod kasutab eelarvevajaduste vähendamiseks eelarve planeerimise koefitsienti.

## <a name="methods-that-are-used-to-reduce-forecast-requirements"></a>Meetodid, mida kasutatakse eelarvevajaduste vähendamiseks

Kui kaasate koondplaani eelarve, saate valida, kuidas vähendatakse eelarvevajadusi, kui kaasatud on tegelik nõudlus. Pange tähele, et koondplaneerimine välistab mineviku eelarvevajadused ehk kõik eelarvevajadused enne tänast kuupäeva.

Selleks, et eelarve koondplaani kaasata ja eelarvevajaduste vähendamise meetod valida, valige **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**. Valige väljal **Eelarvemudel** sobiv eelarvemudel. Valige väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** sobiv meetod. Valikud on järgmised:

- Puudub
- Protsent – planeerimise koefitsient
- Kanded – planeerimise koefitsient
- Kanded – dünaamiline periood

Järgmised jaotised annavad iga suvandi kohta lisateavet.

### <a name="none"></a>Puudub

Kui valite suvandi **Puudub**, siis ei vähendata koondplaneerimisel eelarvevajadusi. Sellisel juhul loob koondplaneerimine plaanitud tellimused, et täita prognoositud nõudlust (eelarvevajadusi). Need plaanitud tellimused hoiavad soovitatud kogust vaatamata teistele nõudlustüüpidele. Näiteks loob koondplaneerimine müügitellimuste esitamisel täiendavad plaanitud tellimused, et müügitellimusi täita. Eelarvevajaduste kogust ei vähendata.

### <a name="percent--reduction-key"></a>Protsent – planeerimise koefitsient

Kui valite suvandi **Protsent – planeerimise koefitsient**, siis vähendatakse eelarvevajadusi planeerimise koefitsiendiga määratud protsentide ja perioodide kohaselt. Sellisel juhul loob koondplaneerimine plaanitud tellimusi, milles arvutatakse kogust iga perioodi jaoks valemiga hinnanguline kogus × planeerimise koefitsient. Kui teisi nõudlustüüpe pole, siis loob koondplaneerimine nõudluse täitmiseks ka plaanitud tellimused.

#### <a name="example-percent--reduction-key"></a>Näide: valik Protsent – planeerimise koefitsient

See näide selgitab, kuidas vähendab planeerimise koefitsient nõudluse prognoosi nõudeid planeerimise koefitsiendiga määratletud protsentide ja perioodide alusel.

Selle näite jaoks kaasate koondplaani järgmised nõudluse prognoosid.

| Kuu    | Nõudluse prognoos |
|----------|-----------------|
| Jaanuar  | 1000           |
| veebruar | 1000           |
| märts    | 1000           |
| aprill    | 1000           |

Seadistage lehel **Planeerimise koefitsiendid** järgmised read.

| Muutmine | Ühik  | Protsent |
|--------|-------|---------|
| 1      | Kuu | 100     |
| 2      | Kuu | 75      |
| 3      | Kuu | 50      |
| 4      | Kuu | 25      |

Määrake planeerimise koefitsient kauba laovarude grupile. Seejärel valige lehe **Koondplaanid** väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** suvand **Protsent – planeerimise koefitsient**.

Kui käivitate sellisel juhul eelplaneerimise 1. jaanuaril, tarbitakse nõudluse prognoosi nõudeid lehel **Planeerimise koefitsiendid** seadistatud protsentide järgi. Koondplaani kantakse üle järgmised vajaduse kogused.

| Kuu                | Plaanitud tellimuse kogus | Kalkulatsioon    |
|----------------------|------------------------|----------------|
| Jaanuar              | 0                      | = 0% × 1000   |
| veebruar             | 250                    | = 25% × 1000  |
| märts                | 500                    | = 50% × 1000  |
| aprill                | 750                    | = 75% × 1000  |
| Mai kuni detsember | 1000                  | = 100% × 1000 |

### <a name="transactions--reduction-key"></a>Kanded – planeerimise koefitsient

Kui seate välja **Eelarvenõuded vähendamiseks kasutatava meetodi** väärtuseks *Kanded – vähendamise klahv* vähendatakse eelarve vajadusi kvalifitseeritud nõudluse kannete võrra, mis toimuvad vähendamisvõtmega määratletud perioodidel.

Kvalifitseeritud nõudluse määratleb **Vähenda lprognoosi** väli **Katvusgrupid** leht. Kui seate **Vähenda prognoosi** välja seadeks *Tellimused*, ainult müügitellimuse kanded kvalifitseeritud nõudluseks. Kui seadistate selle *Kõigile kannetele*, peetakse kõiki mitte kontsernisiseseid väljamineku laokandeid kvalifitseeritud nõudluseks. Kui prognoosi vähendamisel tuleks kaasata kontsernisisesed tellimused, seadke suvandi **Kaasa kontsernisisesed tellimused väärtuseks** väärtuseks *Jah*.

Prognoosi vähendamine algab nõudluse esimese (varaseima) prognoosi kirjega vähendamisest võtme perioodil. Kui kvalifitseeritud laokannete kogus on suurem kui nõudluse prognoosi ridade kogus samas vähendamise võtme perioodis, kasutatakse laokannete koguse saldot nõudluse prognoosi koguse vähendamiseks eelmises perioodis (kui on kinnitamata prognoos).

Kui eelmisesse vähendusvõtme perioodi ei ole jäänud ühtegi kinnitamata eelarvet, kasutatakse laokannete koguse saldot eelarve koguse vähendamiseks järgmisel kuul (kui prognoosi pole kokkuleppinud).

**Protsendi** välja väärtus kui **eelarvenõuete vähendamiseks kasutatava meetodi** väli on seatud väärtusele *Kanded – vähendamisvõti*. Vähendusvõtme perioodi määratlemiseks kasutatakse ainult kuupäevi.

> [!NOTE]
> Kõiki tänasele kuupäevale või enne seda sisestatud eelarvet ignoreeritakse ja seda ei kasutata plaanitud tellimuste loomiseks. Näiteks kui teie kuu nõudluse prognoos on loodud 1. jaanuaril ja te käivitate koondplaanimise, mis hõlmab nõudluse prognoosi 2. jaanuaril, ignoreerib kalkulatsioon nõudluse prognoosi rida, mille kuupäev on 1. jaanuar.

#### <a name="example-transactions--reduction-key"></a>Näide: valik Kanded – planeerimise koefitsient

See näide selgitab, kuidas vähendavad planeerimise koefitsiendiga määratletud perioodide ajal tehtavad tegelikud tellimused nõudluse prognoosi nõudeid.

Selle näite jaoks valige lehe **Koondplaanid** väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** suvand **Kanded – planeerimise koefitsient**.

1. jaanuaril on olemas järgmised müügitellimused.

| Kuu    | Tellitud tükkide arv |
|----------|--------------------------|
| Jaanuar  | 956                      |
| Veebruar | 1,176                    |
| Märts    | 451                      |
| Aprill    | 119                      |

Kui kasutate sama nõudluse prognoosi (1000 tk kuus), mida kasutati eelmises näites, kantakse koondplaani üle järgmised vajaduse kogused.

| Kuu                | Vajalik tükkide arv |
|----------------------|---------------------------|
| Jaanuar              | 44                        |
| veebruar             | 0                         |
| märts                | 549                       |
| aprill                | 881                       |
| Mai kuni detsember | 1000                     |

### <a name="transactions--dynamic-period"></a>Kanded – dünaamiline periood

Kui valite suvandi **Kanded – dünaamiline periood**, siis vähendatakse eelarvevajadusi dünaamilise perioodi jooksul toimuvate tegelike tellimuste kannete võrra. Dünaamiline periood katab praeguse eelarve kuupäevad ja lõpeb järgmise prognoosi algusega. Sellisel juhul loob koondplaneerimine plaanitud tellimused, et täita prognoositud nõudlust (eelarvevajadusi). Sellegipoolest vähendatakse eelarvevajadusi tegelike tellimuste kannete esitamisel. Tegelikud kanded tarbivad osa eelarvevajadustest.

Selle suvandi kasutamisel ilmneb järgmine käitumine.

- Planeerimise koefitsiendid pole vajalikud või neid ei kasutata. 
- Prognoosi täielikul vähendamisel muutub praeguse prognoosi eelarvevajaduseks 0 (null).
- Kui tulevasi prognoose pole, vähendatakse eelarvevajadusi viimati sisestatud prognoosist.
- Nõudluse prognoosi vähendamise ajapiiri ei kaasata prognoosi vähendamise arvutamisse. Selle asemel kasutatakse planeerimisel laovarude grupi ajapiiri.
- Prognoosi vähenduse arvutamisse kaasatakse positiivne päevade arv.
- Kui tellimuse tegelikud kanded ületavad eelarvevajadusi, ei edastata järelejäänud kandeid järgmisse prognoosiperioodi.

#### <a name="example-1-transactions--dynamic-period"></a>Näide 1: valik Kanded – dünaamiline periood

Selles lihtsas näites demonstreeritakse, kuidas toimib meetod **Kanded – dünaamiline periood**.

Selle näite jaoks kaasate koondplaani järgmised nõudluse prognoosid.

| Kuupäev       | Nõudluse prognoos |
|------------|-----------------|
| 1. jaanuar  | 1000           |
| 1. veebruar | 1000             |

Samuti looge järgmised müügitellimused.

| Kuupäev        | Müügitellimuse kogus |
|-------------|----------------------|
| 15. jaanuar  | 200                  |
| 15. veebruar | 400                  |

Sellisel juhul luuakse järgmised plaanitud tellimused.

| Nõudluse prognoosi kuupäev | Kogus | Selgitus                           |
|--------------------- |----------|---------------------------------------|
| 1. jaanuar            | 800      | Eelarvevajadused (= 1000 – 200) |
| 15. jaanuar           | 200      | Müügitellimuste vajadus             |
| 1. veebruar           | 600      | Eelarvevajadused (= 1000 – 400) |
| 15. veebruar          | 400      | Müügitellimuste vajadus             |

#### <a name="example-2-transactions--dynamic-period"></a>Näide 2: valik Kanded – dünaamiline periood

Enamasti on süsteemid seadistatud nii, et kanded vähendavad nõudluse prognoosi teatud prognoosiperioodis (nädalad, kuud jne). Need perioodid on määratletud planeerimise koefitsiendis. Siiski võib ka kahe nõudluse perioodi rea vaheline aeg *tähendada* perioodi.

Selle näite jaoks looge nõudluse prognoos järgmiste kuupäevade ja koguste kohta.

| Kuupäev       | Nõudluse prognoos |
|------------|-----------------|
| 1. jaanuar  | 1000           |
| 5. jaanuar  | 500             |
| 12. jaanuar | 1000           |

Pange tähele, et selles prognoosis pole eelarve kuupäevade vahel kindlat perioodi. Esimese ja teise kuupäeva vahel on neljapäevane vahemik ning teise ja kolmanda kuupäeva vahel on seitsmepäevane vahemik. Need vahemikud on dünaamilised perioodid.

Samuti looge järgmised müügitellimuste read.

| Kuupäev                             | Müügitellimuse kogus |
|----------------------------------|----------------------|
| Eelmise aasta 15. detsember | 500                  |
| 3. jaanuar                        | 100                  |
| 10. jaanuar                       | 200                  |

Sellisel juhul vähendatakse prognoosi järgmiselt.

- Kuna esimene müügitellimus ei jää ühegi perioodi piiresse, ei vähenda see ühtki prognoosi.
- Kuna teine müügitellimus jääb 1. jaanuari ja 5. jaanuari vahele, vähendab see prognoosi 1. jaanuariks 100 võrra.
- Kuna kolmas müügitellimus jääb 5. jaanuari ja 12. jaanuari vahele, vähendab see prognoosi 5. jaanuariks 200 võrra.

Seega luuakse järgmised plaanitud tellimused.

| Nõudluse prognoosi kuupäev             | Kogus | Selgitus                                                         |
|----------------------------------|----------|---------------------------------------------------------------------|
| Eelmise aasta 15. detsember | 500      | Müügitellimuste vajadus                                            |
| 1. jaanuar                        | 900      | Eelarvevajaduse periood 1. jaanuarist kuni 5. jaanuarini (= 1000 – 100) |
| 3. jaanuar                        | 100      | Müügitellimuste vajadus                                            |
| 5. jaanuar                        | 300      | Eelarvevajaduse periood 5. jaanuarist kuni 10. jaanuarini (= 500 – 200)  |
| 12. jaanuar                       | 1000    | Eelarvevajaduse periood 12. jaanuarist lõpuni                      |

## <a name="create-and-set-up-a-forecast-reduction-key"></a>Eelarve planeerimise koefitsiendi loomine ja seadistamine

Meetodites **Kanded – planeerimise koefitsient** ja **Protsent – planeerimise koefitsient** kasutatakse eelarvevajaduste vähendamiseks eelarve planeerimise koefitsienti. Järgige neid samme, et luua ja seadistada planeerimise koefitsienti.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Planeerimise koefitsiendid**.
2. Valige uue planeerimise koefitsiendi loomiseks **Uus**.
3. Sisestage väljale **Planeerimise koefitsient** eelarve planeerimise koefitsiendi jaoks kordumatu identifikaator. Seejärel sisestage nimi väljal **Nimi**. 
4. Määratlege iga perioodi jaoks perioodid ja planeerimise koefitsiendi protsent.

    - Väli **Jõustumiskuupäev** tähistab kuupäeva, millal perioodide loomine algab. Kui suvandi **Kasuta jõustumiskuupäeva** olekuks on määratud **Jah**, siis algavad perioodid jõustumiskuupäeval. Kui suvandi olek on **Ei**, siis algavad perioodid kuupäeval, mil koondplaneerimine käitatakse.
    - Määrake perioodid, mille jooksul eelarvevähendus peaks toimuma.
    - Määrake konkreetse perioodi jaoks protsendid, mille võrra eelarvevajadusi vähendama peaks. Vajaduste vähendamiseks saate sisestada positiivsed väärtused, suurendamiseks negatiivsed väärtused.

## <a name="use-a-reduction-key"></a>Planeerimise koefitsiendi kasutamine

Planeerimise koefitsient peab olema määratud kauba laovarude grupile. Järgige neid samme, et määrata kauba laovarude grupile planeerimise koefitsient.

1. Valige **Koondplaneerimine \> Seadistus \> Laovarud \> Laovarude grupid**.
2. Valige kiirkaardi **Muud** väljal **Planeerimise koefitsient** planeerimise koefitsient, mida laovarude grupile määrata. Planeerimise koefitsient rakendub seejärel kõikidele kaupadele, mis sellesse laovarude gruppi kuuluvad.
3. Selleks, et kasutada planeerimise koefitsienti koondplaneerimise ajal prognoosi vähendamise arvutamiseks, peate määratlema selle sätte koondplaani eelarveplaani seadistuses. Minge ühele järgmistest asukohtadest.

    - Koondplaneerimine \> Seadistus \> Plaanid \> Eelarveplaanid
    - Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid

4. Valige lehe **Eelarveplaanid** või **Koondplaanid** kiirkaardi **Üldine** väljal **Eelarvevajaduste vähendamiseks kasutatav meetod** suvand **Protsent – planeerimise koefitsient** või **Kanded – planeerimise koefitsient**.

## <a name="reduce-a-forecast-by-transactions"></a>Eelarve vähendamine kannetega

Kui valite eelarvevajaduste vähendamise meetodiks **Kanded – planeerimise koefitsient** või **Kanded – dünaamiline periood**, siis saate määrata, millised kanded eelarvet vähendavad. Valige lehe **Laovarude grupid** kiirkaardi **Muud** väljal **Prognoosi vähendamisalus:** suvand **Kõik kanded**, kui prognoosi peaks vähendama kõik kanded, või **Tellimused**, kui prognoosi peaks vähendama ainult müügitellimused.

## <a name="additional-resources"></a>Lisaressursid

- [Koondplaanide ülevaade](master-plans.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
