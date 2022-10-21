---
title: Tootmise viivituste stsenaarium
description: See artikkel kirjeldab tootmise viivituste stsenaariumi, mis loob teatise, kui tootmise läbilask langeb allapoole kindlat läviväärtust.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690017"
---
# <a name="the-production-delays-scenario"></a>Tootmise viivituste stsenaarium

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Tootmise *viivituste* stsenaarium loob teatise, kui tootmise läbilaske langeb allapoole kindlat läviväärtust. Selles stsenaariumis saadetakse *IoT keskusele* Microsoft Azure iga toodetud kauba kohta osalise väljamineku prognoos. Tellimuse Dynamics 365 Supply Chain Management viivituse arvutamisel võetakse aluseks tootmistellimuse plaanitud käitusaeg, toodetavate kaupade arv, *töö* töötamise aeg ja saadud osalise väljamineku signaalide arv. Luuakse viivituse teatis, kui töö osalise väljamineku *signaalide* arv langeb allapoole läviväärtust.

## <a name="scenario-dependencies"></a>Stsenaariumi sõltuvused

Tootmise *viivituste* stsenaariumi sõltuvused on järgmised:

- Teatist saab käivitada ainult juhul, kui tootmistellimus töötab vastendatud masinal.
- IoT keskusele tuleb *saata* märguanne, mis tähistab kaardistatud masina osalise väljamineku signaali ja kordumatu atribuudi nimi peab olema lisatud.
- Azure'i IoT keskuse teade peab sisaldama UNIX-i atribuuti ajatempel, mille väärtust väljendatakse millisekundites (ms).

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Toote viivituste stsenaariumi demoandmete ettevalmistamine

Kui soovite *kasutada* demosüsteemi tootmise viivituste testimiseks, kasutage süsteemi, [kuhu on installitud demoandmed](../../fin-ops-core/fin-ops/get-started/demo-data.md), *valige USMF* juriidiline isik (ettevõte) ja valmistage täiendavad demoandmed ette selles jaotises kirjeldatud viisil. Kui kasutate oma anduriid ja andmeid, võite selle jaotise vahele jätta.

### <a name="set-up-sensor-simulator"></a>Saate häälestada anduri simulaatoreid.

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

## <a name="set-up-the-production-delays-scenario"></a>Saate häälestada tootmise viivituste stsenaariumit.

Järgige neid samme, et seadistada tarneahela *halduses* tootmise viivituste stsenaarium.

1. Minge tootmisjuhtimise **häälestuse \> andteabe \> stsenaariumite \> installi**.
1. Väljal Tootmise **viivitused valige suvand Konfigureeri** **selle stsenaariumi jaoks häälestusviisardi** avamiseks.
1. **Lehel Andurid** valige anduri **lisamiseks** ruudustikule uus. Seejärel määrake selle jaoks järgmised väljad:

    - **Anduri ID – sisestage selle anduri ID**, mida kasutate. (Kui kasutatePakkumiste PI Azure IoT Online Simulaator ja olete seadistanud selle vastavalt kirjeldusele [Seadistage simuleeritud andur testimiseks](sdi-set-up-simulated-sensor.md), sisestage *ProductionDelay*.)
    - **Anduri** kirjeldus – sisestage anduri kirjeldus.

1. Korrake eelmist sammu iga lisaanduri korral, mida soovite nüüd lisada. Saate igal ajal tagasi tulla ja lisada rohkem anduriid.
1. Valige **Edasi**.
1. **Jaotises Andurid** ärikirjete **vastendamise lehel** valige kirje ühe äsja lisatud andurite jaoks.
1. Jaotises Ärikirjete **vastendamine** valige **suvand** Uus, et lisada rida ruudustikku.
1. Seadke uuel real töökirje **ressurssi**, mida kasutate jälgimiseks valitud andurit. (Kui kasutate varem selles artiklis loodud demoandmeid, *seadistage selle väärtuseks 3118, Andmete lõikamise masin*.)
1. Valige **Edasi**.
1. Tootmise viivituse **hälbe** läve lehel, kui kasutate varem selles artiklis loodud demoandmeid, järgige neid samme.

    1. Veeru Kaubaseose **veerupäise** valimiseks, et avada rippmenüü, mis sisaldab veeru otsingufiltreid. Sisestage *otsinguboksi P0111* ja seejärel valige **rakenda.**
    2. Valige rida, kus toimingu **väli** on seatud valikule *Kärbi/lõika*. Seadke välja **Viivituse teatis lävi (%)** lävele (protsendina), mille juures teatis tuleb saata.

1. Valige **Edasi**.
1. Andurite **aktiveerimise lehe** ruudustikus valige lisatud andur ja seejärel valige aktiveeri **.** Iga aktiveeritud anduri puhul ruudustikus kuvatakse märge veerus **Aktiivne**.
1. Valige **Lõpeta**.

## <a name="work-with-the-production-delays-scenario"></a>Tööta tootmise viivituste stsenaariumiga

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Tootmise viivituse andmete vaatamine ressursi olekulehel

Ressursi oleku **lehel saavad** ülevaatajad jälgida ajajoont, mis on saadud igale masinaressursile vastendatud anduritest. Järgige neid samme ajajoone konfigureerimiseks.

1. Minge tootmise **juhtimise tootmise käivitamise \> ressursi \> olekusse**.
1. **Seadke dialoogiboksis** Konfigureerimine järgmised väljad:

    - **Ressurss** – valige ressursid, mida soovite jälgida. (Kui töötate demoandmetega, valige *3118*.)
    - **Ajaseeria 1** – valige kirje (mõõduvõti), mille nime vorming on järgmine: *ProductionJobDelayed:ActualQuantity:&lt; JobId&gt;*
    - **Kuvatav nimi**: sisestage *osad välja.*
