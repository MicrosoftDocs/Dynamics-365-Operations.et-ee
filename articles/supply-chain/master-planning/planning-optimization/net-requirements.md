---
title: Netonõuded ja sidumisteave
description: See artikkel annab teavet arvutatud netonõuete ja sidumisteabe kohta.
author: t-benebo
ms.date: 7/28/2021
ms.topic: article
ms.search.form: ReqTransOverview
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a31ff5490b08d92f0d966388b65de02bca25b050
ms.sourcegitcommit: 613be2f35e600ae1a1fa7ea2ae30e78984ca398a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9748434"
---
# <a name="net-requirements-and-pegging-information"></a>Netonõuded ja sidumisteave

[!include [banner](../../includes/banner.md)]

Üldplaneeringu käivitamisel on oluline mõista selle väljundit, seda, kuidas olemasolev pakkumine katab nõudluse ja miks konkreetne pakkumine loodi. Saate kasutada lehekülge **Netonõuded**, et paremini mõista arvutatud vajadusi, mida koondplaneerimine toodab.

Netonõuete **lehel** kuvatakse netonõuded, mille kohta on arvutatud koondplaneerimine. Samuti kuvatakse selles koondplaneerimise käituse ajal rakendatud laovarude sätted, kogusummade jaotus kandetüübi ja sidumisteabe alusel.

## <a name="open-the-net-requirements-page"></a>Ava netonõuete leht

Saate avada **Netonõuded** lehe järgmistel viisidel:

- Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**. Valige või avage toode. Seejärel tehke tegumiriba vahekaardil **Plaan** grupis **Nõue** valik **Netonõuded**.
- Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**. Ava müügitellimus. Seejärel valige tööriistaribal **Müügitellimuse read** kiirkaardil **Toode ja tarne \> Netonõuded**.
- Avage **Koondplaneerimine \> Koondplaneerimine \> Plaanitud tellimused**. Valige või avage plaanitud tellimus. Seejärel tehke tegumiriba vahekaardil **Kuva** grupis **Nõuded** valik **Nõudeprofiil**.

## <a name="use-the-net-requirements-page"></a>Kasuta netonõuete lehte

Leht **Netonõuded** koosneb ülemistest ja alumistest lõikudest. Sellel lehel oleval toimingupaanil on nupp **Uuenda**. Kui see nupp on valitud, kuvatakse käskude menüü.

### <a name="select-a-master-plan-to-view"></a>Valige kuvamiseks koondplaan

Enne toote netonõuete ülevaatamist valige kindlasti lehe ülaosas väljal **Plaan** vastav koondplaan.

### <a name="upper-section"></a>Ülemine jaotis

Lehe ülemises jaotises on järgmised vahekaardid:

- **Ülevaade** – saate vaadata tootedimensioonide kauba nõudeid.
- **Kauba laovarud** - vaadake laovarude sätteid, mida kasutati nõuete arvutamisel.
- **Kokkuvõte** - vaadake nõuete kogusummade jaotust kande tüübi kaupa.
- **Periood** – saate vaadata iga perioodimalli määratud perioodi sissetulekuid, väljaminekuid ja prognoositud saadaolevaid laovarusid. Samuti saate kuvada graafilise vaate prognoositud saadaolevast laovarust.

### <a name="lower-section"></a>Alumine jaotis

Lehe alumises jaotises on järgmised vahekaardid:

- **Ülevaade** – vaadake koondplaneerimise käivitamisel arvutatud tootenõuete loendit koos nõuetele vastavate väljaminek ja sissetulekukannetega. Vaikimisi sorditakse loend nõude kuupäeva järgi. Nõude valimisel kuvatakse alumises jaotises oleval **Sidumine** kiirkaardil kas nõude allikas või nõudele vastavad tehingud.
- **Üldine** - vaadake valitud nõude kohta üksikasjalikku teavet.
- **Tegevus** - vaadake nõuete tegevussõnumeid.

### <a name="the-action-pane"></a>Tegumiriba

Tegumiribal on saadaval järgmised käsud:

- **Värskendamine \> Koondplaneerimine** – käivitage koondplaneerimine otse **Netonõuete** lehelt.
- **Värskendamine \> Prognooside planeerimine** – käivitage prognooside planeerimine otse **Netonõuete** lehelt. Plaanimine optimeerimine ei toeta seda toimingut.
- **Värskendamine \> Järjepidevuse ajastamine** – käivitage järjepidevuse plaanimine otse lehelt **Netonõuded**. Plaanimine optimeerimine ei toeta seda toimingut.

## <a name="example-scenario"></a>Näidisstsenaarium

See näide näitab, kuidas sidumisteavet **Netonõuete** lehel esitatakse.

### <a name="prerequisites"></a>Eeltingimused

Enne stsenaariumi läbimist valmistage ette järgmised eeltingimused:

1. Peate töötama süsteemis, kus on saadaval standardsed näidisandmed, ning häälestama juriidilise isiku *USMF*-ile.
2. Selles näites kasutatakse toodet *1000*, mis on osa USMF-i näidisandmetest. Veenduge, et see toode on saadaval ja et see on seadistatud järgmiselt.

    - **Vaikimisi tellimuse tüüp:** *ostutellimus*
    - **Vaba kaubavaru:** *10,00*

3. Looge müügitellimus kogusele *25,00* tootest *1000*. Kasutage ladustamismõõte seal, kus varud asuvad.
4. Käivitage *DynPlan* koondplaani koondplaneerimine.

### <a name="review-the-calculated-requirements"></a>Vaadake üle arvutatud nõuded

Seejärel avate toote *1000* **Netonõuete** lehe, et vaadata, kuidas arvutatud nõuded üksteisele vastavad.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige toode, mille **kaubakoodi** väärtus on *1000*.
1. Tehke tegumiriba vahekaardil **Plaan** grupis **Nõue** valik **Netonõuded**.
1. Seadke **Netonõuete** lehel välja **Plaan** väärtuseks *DynPlan*.
1. Lehe alumises osas oleval vahekaardil **Ülevaade** veenduge, et ruudustiku ridadena on loetletud järgmised nõuded.

    | Viide | Vajaduse kogus | Akumuleeritud |
    |---|---|---|
    | Laoseis | 10.00 | 10.00 |
    | Plaanitud ostutellimused | 15.00 | 25.00 |
    | Müügitellimus | -25,00 | (tühi) |

    > [!NOTE]
    > Väli **Nõude kogus** tähistab kogust, mida vajadus nõuab (kui väärtus on negatiivne) või tarne (kui väärtus on positiivne). Väljal **Akumuleeritud** kuvatakse kogu sissetuleku- ja väljaminekukogused, mis on akumuleeritud valitud perioodi jooksul.

1. Valige *vaba* kaubavaru vajaduse rida ja seejärel vaadake **Sidumine** kiirkaardil üle selle tarnega kaetud nõuded. Järgmine rida peab olema seal.

    | Viide | Vajaduse kogus | Kaetud kogus |
    |---|---|---|
    | Müügitellimus | -25,00 | -10,00 |

    Olemasolev vaba kaubavaru katab osaliselt müügitellimusest tuleneva nõudluse.

    ![Vaba kaubavaru sidumisteave](media/pegging-on-hand.png "Vaba kaubavaru sidumisteave")

1. Valige *Planeeritud ostutellimused* kaubavaru vajaduse rida ja seejärel vaadake **Sidumine** kiirkaardil üle selle tarnega kaetud nõuded. Järgmine rida peab olema seal.

    | Viide | Vajaduse kogus | Kaetud kogus |
    |---|---|---|
    | Müügitellimus | -25,00 | -15,00 |

    Kuna müügitellimus on juba osaliselt kaetud, loob süsteem ülejäänud katmata koguse jaoks kavandatud ostutellimuse.

    ![Plaanitud ostutellimuse sidumisteave](media/pegging-planned-purchase-order.png "Plaanitud ostutellimuse sidumisteave")

1. Valige *Müügitellimus* kaubavaru nõudluse rida ja seejärel vaadake **Sidumine** kiirkaardil üle selle tarnega kaetud nõuded. Järgmised read peavad olema seal.

    | Viide | Vajaduse kogus | Kaetud kogus |
    |---|---|---|
    | Laoseis | 10.00 | 10.00 |
    | Plaanitud ostutellimused | 15.00 | 15.00 |

    ![Müügitellimuse sidumisteave](media/pegging-planned-purchase-order.png "Müügitellimuse sidumisteave")

> [!NOTE]
> Turvavarude *nõue* pole netonõuete lehel **kaasatud**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
