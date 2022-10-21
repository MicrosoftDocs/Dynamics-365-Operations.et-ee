---
title: Arvuti oleku stsenaarium
description: See artikkel kirjeldab masina oleku stsenaariumi, mis võimaldab teil kasutada seadme kättesaadavuse jälgimiseks seadme andmeid.
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
ms.openlocfilehash: 30fdfb898384aea4c1f8cb2f36f9e104cd316f90
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689635"
---
# <a name="the-machine-status-scenario"></a>Arvuti oleku stsenaarium

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Masina *oleku* stsenaarium võimaldab teil kasutada anduriandmeid seadmete kättesaadavuse jälgimiseks. Kui seadistate anduri, mis edastab signaali, kui masina ressursi tootmistöö väljundit toodab, kuid teatud intervalliga pole ühtegi signaali saadud, näidatakse teatist ülevaataja armatuurlauda.

## <a name="scenario-dependencies"></a>Stsenaariumi sõltuvused

Masina *oleku* stsenaariumi sõltuvused on järgmised:

- Teatist saab käivitada ainult siis, kui vastendatud masinas on pooleli tootmistöö.
- IoT keskusele *tuleb* saata väljamineku märguanne.

## <a name="prepare-demo-data-for-the-machine-status-scenario"></a>Valmistage ette demoandmed masina oleku stsenaariumi jaoks

Kui soovite kasutada demosüsteemi *masina* oleku testimiseks, kasutage süsteemi, [kuhu demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md) on installitud, *valige USMF-juriidiline* isik (ettevõte) ja valmistage täiendavad demoandmed ette selles jaotises kirjeldatud viisil. Kui kasutate oma anduriid ja andmeid, võite selle jaotise vahele jätta.

### <a name="set-up-a-sensor-simulator"></a>Anduri simulaator häälestamine

Kui soovite seda stsenaariumi proovida ilma füüsilise andurita, saate seadistada simulaator, mis loob nõutavad signaalid. Lisateabe saamiseks vt simuleeritud [anduri seadistamist testimiseks](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Veenduge, et ressurssi 3118 kasutatakse toote P0111 jaoks.

Tootmistellimus planeeritakse ja vabastatakse. Seetõttu vabastatakse tootmistöö ressursile *3118* (*Tootmisprotsessi lõikamismasin*). Järgige neid samme kontrollimaks, et *ressurssi 3118* kasutatakse toote *P0111 jaoks teie* demoandmetes.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Otsige ja valige toode, kus kaubakoodi **väljal** on valitud väärtus *P0111*.
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

### <a name="configure-the-production-floor-execution-interface"></a><a name="config-pfe"></a>Tootmisosakonna täideviimisliidese konfigureerimine

Kasutate tootmispinna käivitamise liidest eelmises jaotises kaubale number *P0111* planeeritud ja vabastatud töö alustamiseks. Järgige neid samme tootmispinna käivitamise liidese konfigureerimiseks.

1. Avage **Tootmise juhtimine \> Tootmise käivitamine \> Tootmisosakonna käivitus**.
1. Kui te pole liidest varem seadistanud, kuvatakse sisselogimisleht. Sisestage oma identimisteave.
1. Tervituslehel valige konfigureerimisviisard **seadme** **konfigureerimise viisardi** avamiseks.
1. **Seadme konfigureerimise lehel – 1. etapp – valige konfigureerimislehel** vaikekonfiguratsioon *·*.
1. Valige **Edasi**.
1. **Seade konfigureerimine – 2. etapp – määratlege tootmise põhiala** leht, seadke **välja** Ressurss väärtuseks *3118*.
1. Valige nupp **OK**.

### <a name="enable-the-search-option-in-the-production-floor-execution-interface"></a><a name="enable-pfe-search"></a> Otsingussuvandi lubamine tootmispinna käivitamise liideses

Et hõlbustada varem vabastatud tootmistellimuse tootmistöö otsimist, järgige neid samme, et lubada otsingusuvand tootmispinna käivitamise liideses.

1. Avage **Tootmise juhtimine \> Seadistus \> Tootmise käivitamine \> Tootmisosakonna käivituse konfigureerimine**.
1. Valige *vaikekonfiguratsioon*.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Seadke kiirkaardi **Üldine** valiku Luba otsing **väärtuseks** *Jah*.
1. Sulgege leht.

### <a name="start-the-first-job-in-the-batch-order"></a>Alusta pakett-tellimuse esimest tööd

Järgige neid samme ressursil *3118 plaanitud töö alustamiseks*.

1. Avage **Tootmise juhtimine \> Tootmise käivitamine \> Tootmisosakonna käivitus**.
1. **Väljale Badge ID** sisestage *123*. Seejärel valige **sisselogimine**.
1. Kui teilt küsitakse puudumise põhjust, valige üks puudumiskaartidest ja seejärel valige **OK**.
1. Sisestage **väljale** Otsing partiitellimuse number, mille kohta olete eelnevalt märkuse teinud. Seejärel valige **tagastusvõti**.
1. Valige tellimus ja seejärel käivitage **töö**.
1. Dialoogiaknas **Alusta** tööd valige **Alusta**.

## <a name="set-up-the-machine-status-scenario"></a>Saate häälestada masina oleku stsenaariumit.

Järgige neid samme masina oleku stsenaariumi *häälestamiseks* tarneahela haldamises.

1. Minge tootmisjuhtimise **häälestuse \> andteabe \> stsenaariumite \> installi**.
1. Väljal Masina **olekustsenaarium** valige suvand Konfigureeri **selle** stsenaariumi jaoks häälestusviisardi avamiseks.
1. **Lehel Andurid** valige anduri **lisamiseks** ruudustikule uus. Seejärel määrake selle jaoks järgmised väljad:

    - **Anduri ID – sisestage selle anduri ID**, mida kasutate. (Kui kasutatePakkumiste PI Azure IoT Online Simulaator ja olete seadistanud selle vastavalt kirjeldusele [Seadistage simuleeritud andur testimiseks](sdi-set-up-simulated-sensor.md), sisestage *MachineStatus*.)
    - **Anduri** kirjeldus – sisestage anduri kirjeldus.

1. Korrake eelmist sammu iga lisaanduri korral, mida soovite nüüd lisada. Saate igal ajal tagasi tulla ja lisada rohkem anduriid.
1. Valige **Edasi**.
1. **Jaotises Andurid** ärikirjete **vastendamise lehel** valige kirje ühe äsja lisatud andurite jaoks.
1. Jaotises Ärikirjete **vastendamine** valige **suvand** Uus, et lisada rida ruudustikku.
1. Seadke uuel real välja **Ärikirje väärtuseks** ressurss, mida kasutate seireks valitud andurit. (Kui kasutate varem selles artiklis loodud demoandmeid, *seadistage välja väärtuseks 3118, Teabebaasi lõikemasin*.)
1. Valige **Edasi**.
1. Määratlege **masina olekuläve** lehel, kui kaua pärast *viimast väljamineku* märguannet peab süsteem saatma masina olekuteatise. Läve määratlemiseks on kaks võimalust:

    - **Vaikelävi (minutites)** – seadistage see väli vaikeläve määratlemiseks. Väärtus rakendub siis kõigile ressurssidele, kus **lävi masina mittevastamise (minutite)** välja väärtuseks on seatud kaks minutit või vähem. Minimaalne väärtus on *2* (minutites).
    - **Lävi, mis määrab, et masin ei vasta (minutites)** – iga ruudustikus ressursi puhul, mille puhul te ei soovi vaikeläve kasutada, sisestage sellele väljale alistamisväärtus. Ressursid, mis on määratud kasutama lävi 2 või vähem minutit, kasutavad selle **asemel vaikeläve (minutites)** sätet.

    > [!NOTE]
    > Tavaliselt kasutatakse väljaminev märguanne *masina* oleku jälgimiseks. Seetõttu peaksite kontrollima, et iga masina ressursi lävi on pikem, kui masin vajab iga osa tootmiseks.

1. Valige **Edasi**.
1. Andurite **aktiveerimise lehe** ruudustikus valige lisatud andur ja seejärel valige aktiveeri **.** Iga aktiveeritud anduri puhul ruudustikus kuvatakse märge veerus **Aktiivne**.
1. Valige **Lõpeta**.

## <a name="work-with-the-machine-status-scenario"></a>Tööta masina oleku stsenaariumiga

Pärast oma andurite installimist ja stsenaariumi konfigureerimist saate vaadata masina oleku sündmusi tarneahela halduses. Selles jaotises kirjeldatakse, kus ja kuidas seda teavet vaadata.

### <a name="view-machine-status-data-on-the-resource-status-page"></a>Kuva masina olekuandmed ressursi oleku lehel

Ressursi oleku **lehel** saavad ülevaatajad jälgida osa-/väljaminev signaali ajajoont, *mis* on saadud iga arvutiressursiga vastendatud anduritest. Järgige neid samme ajajoone konfigureerimiseks.

1. Minge tootmise **juhtimise tootmise käivitamise \> ressursi \> olekusse**.
1. **Seadke dialoogiboksis** Konfigureerimine järgmised väljad:

    - **Ressurss** – valige ressursid, mida soovite jälgida. (Kui töötate demoandmetega, valige *3118*.)
    - **Ajaseeria 1** – valige kirje (meetermõõdustik), mille nime vorming on järgmine: *MachineReportingStatus:&lt; Reporter&gt;*
    - **Kuvatav nimi**: sisestage *osad välja.*

Järgmine näide näitab näiteid masina olekuandmete kohta ressursi **oleku lehel** standardoperatsiooni ajal.

![Masina oleku andmed ressursi oleku lehel standardtoimingu ajal](media/sdi-resource-status-downtime-up.png "Masina oleku andmed ressursi oleku lehel standardtoimingu ajal")

Järgmine näide näitab masina olekuandmete näidet, kui ülestunnitöö tuvastatakse.

![Ressursi oleku lehel olevad masina olekuandmed, kui ülestunnid tuvastatakse.](media/sdi-resource-status-downtime-down.png "Masina olekuandmed ressursi oleku lehel, kui ülestunnitöö tuvastatakse")

### <a name="view-machine-status-on-the-notifications-page"></a>Kuva teatiste lehel masina olek

Ülevaatajad **saavad** teatisi vaadata lehel Teatised, mis on loodud liiga palju aega möödas *pärast seda, kui andja on viimasena välja lülitanud osalise signaali*. Iga teatis annab ülevaate tootmistööst, mida väljaminek mõjutab, ja annab valiku määrata mõjutatud töö ümber teisele ressursile.

Teavituse lehe **avamiseks** minge tootmise juhtimise päringute **ja \> aruannete seadme andmeteabe \> teatiste \> lehele**.

Järgmine näide masina olekuteatise kohta.

![Näide masina olekuteatise kohta.](media/sdi-resource-status-downtime-notification.png "Näide masina olekuteatisest")
