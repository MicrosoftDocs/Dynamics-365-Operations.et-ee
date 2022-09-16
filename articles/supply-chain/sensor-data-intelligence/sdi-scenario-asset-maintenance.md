---
title: Vara hoolduse stsenaarium
description: See artikkel kirjeldab vara hoolduse stsenaariumi, mis võimaldab teil kasutada anduriandmeid, et luua loendurikirjeid, mis jälgivad masina vara kasutamist.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, EntAssetCounter
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: ff3944b987314a688a5829b05f8627479e3e79ed
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428966"
---
# <a name="the-asset-maintenance-scenario"></a>Vara hoolduse stsenaarium

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Vara *hoolduse stsenaarium* võimaldab kasutada anduriandmeid loendurikirjete loomiseks. Kassakirjed jälgivad masina vara kasutamist ja neid kasutatakse sisendina masinavarade hooldusgraafiku loomisel.

## <a name="prepare-demo-data-for-the-asset-maintenance-scenario"></a>Vara hoolduse stsenaariumi demoandmete ettevalmistamine

Kui soovite vara hoolduse stsenaariumi testimiseks kasutada *demosüsteemi*, kasutage süsteemi, [kuhu demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md) on installitud, *valige USMF-juriidiline* isik (ettevõte) ja valmistage täiendavad demoandmed ette selles jaotises kirjeldatud viisil. Kui kasutate oma anduriid ja andmeid, võite selle jaotise vahele jätta.

Selles jaotises seadistate näitena *AK-101,* lennu põhivara demoandmetes. Seejärel näete, kuidas eesseisva hooldustöö saab prognoosida anduri signaalide põhjal, mis mõõdavad lennuseadmete töötamise tundide arvu. Samuti seadistate te hooldusplaani, kus lennufirmat tuleb hooldada iga 10 000 tunni järel.

### <a name="set-up-a-sensor-simulator"></a>Anduri simulaator häälestamine

Kui soovite seda stsenaariumi proovida ilma füüsilise andurita, saate seadistada simulaator, mis loob nõutavad signaalid. Lisateabe saamiseks vt simuleeritud [anduri seadistamist testimiseks](sdi-set-up-simulated-sensor.md).

### <a name="create-an-asset-counter-to-track-production-hours"></a>Põhivaraloenduri loomine tootmistundide jälgimiseks

Järgige neid samme põhivaraloenduri loomiseks, et jälgida tootmistunde.

1. Avage **Varahaldus \> Seadistus \> Vara tüübid \> Loendurid**.
1. Tegevuspaanil valige loenduri **loomiseks** uus.
1. Määrake päises järgmised väärtused.

    - **Loendur:** *Production Pealek*
    - **Nimi: tootmistunnid** *·*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Ühik:** *hr*
    - **Värskendus:** *käsitsi*
    - **Kokkuvõtte kokkuvõtted:** *summa*

1. Valige varatüüpide **kiirkaardil** suvand **Lisa rida**.
1. Uuel real seadke varatüübi välja **väärtuseks** *Õhul*.

### <a name="create-a-maintenance-plan-for-the-asset"></a>Vara hooldusplaani loomine

Järgige neid samme varale hooldusplaani loomiseks.

1. Minge varahalduse **seadistamise ennetusliku \>\> hoolduse \> plaani**.
1. Tegevuspaanil valige hooldusplaani **loomiseks** uus.
1. Määrake päises järgmised väärtused.

    - **Hooldusplaan:** *AirKnife*
    - **Nimi:** *lennuplaani nimi*

1. Määrake kiirkaardil **Üksikasjad** järgmised väärtused.

    - **Plaani kuupäev:** sisestage tänane kuupäev.
    - **Aktiivne:** *jah*

1. Valige kiirkaardil **Read** suvand **Lisa vara kassarida**, et lisada rida ruudustikule. Seejärel määrake selle jaoks järgmised väärtused:

    - **Töötellimuse kirjeldus:** *lennutranspordi hooldus*
    - **Hooldustöö tüüp: ennetav** *·*
    - **Intervalli tüüp:** *korduv viimasest töötellimusest*
    - **Perioodi sagedus:** *10000*
    - **Loendur:** *Production Pealek*

## <a name="set-up-the-asset-maintenance-scenario"></a>Saate häälestada vara hoolduse stsenaariumit.

Järgige neid samme vara haldamise stsenaariumi *häälestamiseks* tarneahela halduses.

1. Minge varahalduse **häälestuse \> andmeteabe \> stsenaariumite \> installi**.
1. Vara hoolduse **stsenaariumi kastis** valige suvand **Konfigureeri**, et avada selle stsenaariumi jaoks häälestusviisard.
1. **Lehel Andurid** valige anduri **lisamiseks** ruudustikule uus. Seejärel määrake selle jaoks järgmised väljad:

    - **Anduri ID – sisestage selle anduri ID**, mida kasutate. (Kui kasutatePakkumiste PI Azure IoT Online Simulaator ja olete seadistanud selle vastavalt kirjeldusele [Seadistage katsetamiseks simuleeritud andur](sdi-set-up-simulated-sensor.md), sisestage *AssetMaintenance*.)
    - **Anduri** kirjeldus – sisestage anduri kirjeldus.

1. Korrake eelmist sammu iga lisaanduri korral, mida soovite nüüd lisada. Saate igal ajal tagasi tulla ja lisada rohkem anduriid.
1. Valige **Edasi**.
1. **Jaotises Andurid** ärikirjete **vastendamise lehel** valige kirje ühe äsja lisatud andurite jaoks.
1. Jaotises Ärikirjete **vastendamine** valige **suvand** Uus, et lisada rida ruudustikku.
1. Uuel real tuleks välja **Ärikirje tüüp** väärtuseks automaatselt seada *Assets(EntAssetObjectTable)*. Seadistage **ärikirje** väli ressursile, mida kasutate valitud andurit jälgimiseks. (Kui kasutate varem selles artiklis loodud demoandmeid, seadke selle väärtuseks *AK-101, AK-101 1. rea õhutranspordi liin*)
1. Kohe pärast eelmises sammus lisatud rea ärikirje tüübi valimist lisatakse ruudustikku automaatselt teine rida. Selles reas tuleks välja **Ärikirje tüüp** väärtuseks määrata *Counters(EntAssetCounterType).* Seadistage **väli Ärikirje** varaloendurile, mida uuendate valitud anduri signaalide põhjal. (Kui kasutate varem selles artiklis loodud demoandmeid, seadke selle väärtuseks *ProductionToodang, Tootmistunnid*.)
1. Valige **Edasi**.
1. Andurite **aktiveerimise lehe** ruudustikus valige lisatud andur ja seejärel valige aktiveeri **.** Iga aktiveeritud anduri puhul ruudustikus kuvatakse märge veerus **Aktiivne**.
1. Valige **Lõpeta**.

## <a name="work-with-the-asset-maintenance-scenario"></a>Tööta vara hoolduse stsenaariumiga

### <a name="view-counter-values"></a>Loenduriväärtuste kuvamine

Kui andmed on ette *valmistatud* ja vara hoolduse stsenaarium konfigureeritud ja aktiveeritud, saate vaadata, kuidas põhivara loenduri kirjed on vastavalt arvutiandmetele sisestatud.

1. Minge varade **haldusse \> Kõik \> varad**.
1. Otsige ja valige vara, mida soovite üle vaadata. (Kui kasutate varem selles artiklis loodud demoandmeid, valige *AK-101*.)
1. Selleks et avada põhivara **AK-101 loendurikirjete leht,** **·** **valige** tegevuspaani vahekaardil Vara grupp Ennetusloendurid.*·*

### <a name="generate-maintenance-work-orders"></a>Hooldustöötellimuste loomine

Pärast vara hoolduse stsenaariumi *lubamist* ja hooldusplaani seadistamist saate käivitada hooldusgraafiku hooldustöö tellimuste loomiseks. Lisateavet ennetushooldusega seotud töö kohta vt ennetushoolduse [ülevaatest](../asset-management/preventive-and-reactive-maintenance/preventive-maintenance-overview.md).
