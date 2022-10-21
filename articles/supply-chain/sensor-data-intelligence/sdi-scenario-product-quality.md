---
title: Tootekvaliteedi stsenaarium
description: See artikkel annab teavet toote kvaliteedi stsenaariumi kohta. See stsenaarium kasutab andurit tootepartii kvaliteedi mõõtmise mõõtmiseks ja loob teatise, kui mõõtmine langeb väljapoole määratletud läve.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: c0f1c57251234921779f67faf61d47cdde119e64
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690044"
---
# <a name="the-product-quality-scenario"></a>Tootekvaliteedi stsenaarium

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Toote kvaliteedi *stsenaariumis* seadistatakse andur tootepartii kvaliteedi mõõtmiseks tööde juhtimises. Kui mõõtmine langeb väljapoole toote määratletud läve, kuvatakse teatis ülevaataja armatuurlaudal. Näiteks mõõtmisb andur tootmisreast välja tulev toidutoote mõõtu. Kui mõõtmine on väljaspool toote maksimaalne lubatud miinimum- või maksimumväärtust, luuakse teatis.

## <a name="scenario-dependencies"></a>Stsenaariumi sõltuvused

Toote *kvaliteedistsenaariumi* sõltuvused on järgmised:

- Teatise saab käivitada ainult siis, kui tootmistellimus töötab kaardistatud masinas ja kui see masin toodab toodet, mille partii atribuut on vastendatud.
- Partiiatribuuti esindav märguanne tuleb saata IoT keskusesse koos kordumatu atribuudinimega.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Toote kvaliteedistsenaariumi demoandmete ettevalmistamine

Kui soovite toote kvaliteedi stsenaariumi testimiseks kasutada *demosüsteemi*, kasutage süsteemi, [kuhu demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md) on installitud, *valige USMF-juriidiline* isik (ettevõte) ja valmistage täiendavad demoandmed ette selles jaotises kirjeldatud viisil. Kui kasutate oma anduriid ja andmeid, võite selle jaotise vahele jätta.

Selles jaotises seadistate demoandmed nii *, et saate toote kvaliteedistsenaariumiga kasutada väljastatud toodet P0111* (*Liitjuhtum* *·*). Selles stsenaariumis jälgib süsteem, kas anduriga mõõdetud partii atribuudi väärtus on väljaspool tootega seostatud partii atribuudi määratletud läve.

### <a name="set-up-a-sensor-simulator"></a>Anduri simulaator häälestamine

Kui soovite seda stsenaariumi proovida ilma füüsilise andurita, saate seadistada simulaator, mis loob nõutavad signaalid. Lisateabe saamiseks vt simuleeritud [anduri seadistamist testimiseks](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Partii atribuudi ja ressursi seostamine tootega P0111

Järgige neid samme, et *seostada partii atribuut tootega P0111* (*Liitjuhtum*) *ja veenduge, et selle jaoks kasutatakse ressurssi 3118* (*"Jälitamismasin*").

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige ja valige toode, kus kaubakoodi **väljal** on valitud väärtus *P0111*.
1. Valige tegevuspaani vahekaardil **Varude haldamine grupi** Partii atribuudid suvand **Tootespetsiifiline** **.**
1. Tootepõhise **partii** atribuudi loomiseks **valige** lehel Tootespetsiifiline väärtus Uus.
1. Seadke päises järgmised väljad:

    - **Atribuudi kood** – valige jälgida kuuluvate atribuutide ulatus (*Tabel*, *Grupp* või *Kõik*). Valige selle stsenaariumi puhul *tabel*, sest jälgite alati ühte atribuuti.
    - **Atribuudi seos**: valige atribuut, mille väärtuse jälgimiseks *kasutate* toote kvaliteedi stsenaariumi. Selle näite puhul valige *kontsentratsioon*, mis on standardsete demoandmete hulka kaasatud atribuut.

1. Määratlege **kiirkaardi** Väärtused väljadel **Miinimum** ja **Maksimum** lubatud väärtuste vahemik, mille kohta peab atribuut kvaliteedikontrolli läbimiseks aruande esitama. Kui andur esitab väljaspool seda vahemikku väärtuse, määratleb süsteem selle kvaliteedi rikkumisena. Teised selle kiirkaardi väljad ei ole toote kvaliteedi stsenaariumi *puhul asjakohased*. Praegu nähavad vaikeväärtused tulevad demoandmetest. Seega jätke need nii nagu nad on ja **sulgege** tootespetsiifiline **leht** *, et naasta kauba P0111 väljastatud toote üksikasjade lehele*.
1. Valige tegevuspaani vahekaardil **Insener** grupis **Vaade** suvand **Protsess**.
1. **Valige lehe** allservas oleval **vahekaardil** Ülevaade protsessilehel rida, kus **välja Oper. nr.** Välja <a0/& väärtuseks *on seatud 30*.
1. Veenduge, **et** *ressurss 3118* (*Aparaatide* lõikamismasin) on toiminguga seotud, vahekaardil Ressursinõuded.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Tootmistellimuse loomine ja vabastamine tootele P0111

Toote P0111 jaoks tootmistellimuse loomiseks ja *vabastamiseks järgige neid samme*.

1. Avage **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**.
1. Valige tegevuspaanil **leheküljel** Kõik tootmistellimused väärtus Uus **partiitellimus**.
1. Seadke dialoogiboksis **Partii** loomine järgmised väärtused:

    - **Kauba kood:** *P0111*
    - **Kogus:** *10*

1. Valige **loo**, et luua tellimus ja naasta leheküljele **Kõik tootmistellimused**.
1. Kasutage välja **Filter** tootmistellimuste otsimiseks, kus kaubakoodi **väli** on seadistatud väärtusele *P0111*. Seejärel otsige ja valige äsja loodud tootmistellimus.
1. Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Hinda**.
1. Hinnangu käivitamiseks **valige** dialoogiboksis **Hinnang nupp OK**.
1. Valige tegevuspaani vahekaardil Tootmistellimus **grupis** Protsess **suvand Vabasta** **.**
1. **Dialoogiboksis Vabastage** äsja loodud partiitellimuse numbri märkus.
1. Valige **OK** tellimuse vabastamiseks.

### <a name="configure-the-production-floor-execution-interface"></a>Tootmisosakonna täideviimisliidese konfigureerimine

Kui te pole seda juba teinud, konfigureerige tootmispinna täitmisliides, et näidata töid, *mis on määratud ressursile 3118* (*Ruutu lõikav masin*). Juhiseid vt järgmistest jaotistest:

- [Tootmisosakonna täideviimisliidese konfigureerimine](sdi-scenario-equipment-downtime.md#config-pfe)
- [Otsingussuvandi lubamine tootmispinna käivitamise liideses](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>Alusta pakett-tellimuse esimest tööd

Järgige neid samme, et käivitada esimene töö pakett-töö järjestuses.

1. Avage **Tootmise juhtimine \> Tootmise käivitamine \> Tootmisosakonna käivitus**.
1. **Väljale Badge ID** sisestage *123*. Seejärel valige **sisselogimine**.
1. Kui teilt küsitakse puudumise põhjust, valige üks puudumiskaartidest ja seejärel valige **OK**.
1. Sisestage **väljale** Otsing partiitellimuse number, mille kohta olete eelnevalt märkuse teinud. Seejärel valige **tagastusvõti**.
1. Valige tellimus ja seejärel käivitage **töö**.
1. Dialoogiaknas **Alusta** tööd valige **Alusta**.

## <a name="set-up-the-product-quality-scenario"></a>Saate häälestada toote kvaliteedistsenaariumi.

Järgige neid samme toote kvaliteedi stsenaariumi *häälestamiseks* tarneahela halduses.

1. Minge tootmisjuhtimise **häälestuse \> andteabe \> stsenaariumite \> installi**.
1. Valige väljal **Toote kvaliteedi** stsenaarium suvand **Konfigureeri**, et avada selle stsenaariumi jaoks häälestusviisard.
1. **Lehel Andurid** valige anduri **lisamiseks** ruudustikule uus. Seejärel määrake selle jaoks järgmised väljad:

    - **Anduri ID – sisestage selle anduri ID**, mida kasutate. (Kui kasutatePakkumiste PI Azure IoT Online Simulaator ja olete seadistanud selle vastavalt kirjeldusele [Seadistage simuleeritud andur testimiseks](sdi-set-up-simulated-sensor.md), sisestage *kvaliteet*.)
    - **Anduri** kirjeldus – sisestage anduri kirjeldus.

1. Korrake eelmist sammu iga lisaanduri korral, mida soovite nüüd lisada. Saate igal ajal tagasi tulla ja lisada rohkem anduriid.
1. Valige **Edasi**.
1. **Jaotises Andurid** ärikirjete **vastendamise lehel** valige kirje ühe äsja lisatud andurite jaoks.
1. Jaotises Ärikirjete **vastendamine** valige **suvand** Uus, et lisada rida ruudustikku.
1. Uuel real tuleks välja **Ärikirje tüüp** väärtuseks automaatselt *seada Resources (WrkCtrTable)*. Seadistage **ärikirje** väli ressursile, mida kasutate valitud andurit jälgimiseks. (Kui kasutate varem selles artiklis loodud demoandmeid, *seadistage selle väärtuseks 3118, Andmete lõikamise masin*.)
1. Kohe pärast eelmises sammus lisatud rea ärikirje tüübi valimist lisatakse ruudustikku automaatselt teine rida. Selles reas tuleb välja **Ärikirje tüüp** väärtuseks *määrata Partii atribuudid (PdsBatchAttrib).* Seadke väli **Ärikirje** partii atribuudile, mida kasutate valitud andurit jälgimiseks. (Kui kasutate varem selles artiklis loodud demoandmeid, seadke selle väärtuseks *Väljaminek, kusekuse protsent*.)
1. Valige **Edasi**.
1. Andurite **aktiveerimise lehe** ruudustikus valige lisatud andur ja seejärel valige aktiveeri **.** Iga aktiveeritud anduri puhul ruudustikus kuvatakse märge veerus **Aktiivne**.
1. Valige **Lõpeta**.

## <a name="work-with-the-product-quality-scenario"></a>Tööta toote kvaliteedi stsenaariumiga

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Toote kvaliteediandmete vaatamine ressursi oleku lehel

Ressursi oleku **lehel** saavad ülevaatajad jälgida toote kvaliteedi signaali ajajoont, mis on saadud igale masina ressursile vastendatud anduritest. Järgige neid samme ajajoone konfigureerimiseks.

1. Minge tootmise **juhtimise tootmise käivitamise \> ressursi \> olekusse**.
1. **Seadke dialoogiboksis** Konfigureerimine järgmised väljad:

    - **Ressurss** – valige ressursid, mida soovite jälgida. (Kui töötate demoandmetega, valige *3118*.)
    - **Ajaseeria 1** – valige kirje (mõõduvõti), mille nime vorming on järgmine: *ProductQuality:&lt; JobId&gt;:&lt; AttributeName&gt;*
    - **Kuvatav nimi** : sisestage *partii atribuudi väärtused*.

Järgmine näide näitab toote kvaliteediandmete näidet ressursi oleku **lehel, kui väärtus on** vastuvõetavate väärtuste vahemikus.

![Toote kvaliteediandmed ressursi oleku lehel, kui väärtus on vahemikus](media/sdi-product-quality-in-range.png "Toote kvaliteediandmed ressursi oleku lehel, kui väärtus on vahemikus")

Järgmine näide toote kvaliteediandmete kohta vahemikust väljamineva väärtuse tuvastamisel.

![Toote kvaliteediandmed ressursi oleku lehel, kui tuvastati vahemikust väljas väärtus.](media/sdi-product-quality-out-of-range.png "Toote kvaliteediandmed ressursi oleku lehel, kui tuvastati vahemikust väljas väärtus")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Toote kvaliteediandmete kuvamine teatiste lehel

Ülevaatajad **saavad** lehel Teatised vaadata teatist, mis luuakse, kui andur läveks ületab partii atribuudi väärtuse, mis langeb väljapoole partii atribuudi määratletud läve. Iga teatis annab ülevaate tootmistööst, mida väljaminek mõjutab, ja annab valiku määrata mõjutatud töö ümber teisele ressursile.

Teavituse lehe **avamiseks** minge tootmise juhtimise päringute **ja \> aruannete seadme andmeteabe \> teatiste \> lehele**.

Järgmine näide toote kvaliteediteatise kohta.

![Toote kvaliteediteatise näide](media/sdi-product-quality-notification.png "Toote kvaliteediteatise näide")
