---
title: Tasu registreerimiste põhjal
description: Selles teemas kirjeldatakse, kuidas arvutatakse tasu töötaja registreerimiste põhjal.
author: johanhoffmann
manager: AnnBe
ms.date: 03/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgCalcApproveWeekView
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: f36c411ce24dfd8cceacda3d4659ec9a98fd5aa9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548971"
---
# <a name="pay-based-on-registrations"></a>Tasu registreerimiste põhjal

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse üksikasjalikult, kuidas arvutatakse tasu töötaja registreerimiste põhjal. See sisaldab näiteid, mis näitavad, kuidas mõjutavad tulemust arvutamiseks saadaolevad seadistussuvandite eri kombinatsioonid. Allpool on teemad, millest selles jaotises räägitakse.

- Paindaeg
- Ületunnitöö
- Vaheajad
- Lülituse koodid
- Tasuüksused
- Tasulepped
- Tööajaarvestuse arvutuse parameetrid
- Puudumine

## <a name="the-use-of-flex-time"></a>Paindaja kasutamine

Paindaja perioodid seadistatakse ajareeglites, mis tööajaarvestuses kasutatakse. Olemas on kaks paindreegli tüüpi: **Paind+** ja **Paind–**. Kui töötaja registreerib aja paind+ perioodis, suurendatakse töötaja paindsaldot töötatud tundide võrra. Töötaja ei saa kompensatsiooni tundide eest, mis töötati paind+ perioodi jooksul. Kuid töötaja saab paind– perioodide jooksul võtta vabu päevi ja saada kompensatsiooni oma paindsaldo tundidega. Seetõttu peab süsteem vaba aega paindperioodide jooksul puudumiseks.

## <a name="scenarios-based-on-flex-periods"></a>Paindperioodidel põhinevad stsenaariumid

Kaks järgnevat stsenaariumi põhinevad paindreeglil, mis kujutab tööpäeva. Mõlema stsenaariumi korral arvutatakse tasu paindperioodi järgi, millal töötaja sisse ja välja registreerub.

### <a name="flex-profile-for-one-workday"></a>Ühe tööpäeva paindreegel

| Profiili tüüp  | Käivita    | Lõpp      | Päev     |
|---------------|----------|----------|---------|
| Ületunnitöö     | 00:00 | 06:00 | esmaspäev  |
| Paind+         | 06:00 | 07:00 | esmaspäev  |
| Sisseregistreerimine      | 07:00 | 07:00 | esmaspäev  |
| Standardaeg | 07:00 | 14:30 | esmaspäev  |
| Paind-         | 14:30 | 15:30 | esmaspäev  |
| Väljaregistreerimine     | 15:30 | 15:30 | esmaspäev  |
| Ületunnitöö     | 15:30 | 06:00 | teisipäev |

### <a name="scenario-1-a-worker-registers-clock-in-during-a-flex-period-and-clock-out-during-a-flex--period"></a>Stsenaarium 1: töötaja registreerub sisse paind+ ja välja paind– perioodi jooksul

Töötaja selle päeva registreerimised näevad välja järgmised.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      |
|---------------------------|----------|----------|
| Sisseregistreerimine                  | 06:30 | 06:30 |
| Tootmistöö            | 06:30 | 14:45 |
| Väljaregistreerimine                 | 14:45 | 14:45 |

Töötaja selle päeva registreerimised arvutatakse ja edastatakse, et tasuda lehel **Kinnita** (**Tööajaarvestus** &gt; **Ülevaatamine ja kinnitamine** &gt; **Kinnita**). Kui registreerimised on arvutatud, saab arvutuse tulemust vaadata vahekaardil **Ajad**. 

Selle stsenaariumi mõistmiseks vaadake järgmisi välju.

| Paind+ | Paind– | Aeg | Tasustatav aeg |
|--------|--------|------|----------|
| 0,50   | 0.75   | 8,25 | 8,50     |

#### <a name="calculation-of-flex"></a>Paind+ arvutamine

Paindreegli kohaselt on aeg kella 06:00 ja 07:00 AM vahel paind+ periood. Nii et kui töötaja registreerub sisse kell 06:30, teenib ta 0,5 tundi. See ajahulk lisatakse töötaja paindkontole.

#### <a name="calculation-of-flex-"></a>Paind– arvutamine

Paindreegli järgi algab paind– periood kell 14:30 ja lõppeb 15:30. Nii et kui töötaja registreerub välja kell 14:45, registreeritakse paind– perioodi jäänud 45 minutit (0,75 tundi) tasustatava ajana ning sama ajahulk võetakse maja töötaja paindkontolt. Need 45 minutit arvestatakse tasustatava aja sisse, kuna töötajale võimaldatakse tasu paind– perioodi ülejäänud 45 minuti eest. Kui töötaja puudub paind– perioodil, arvatakse 45 minutit tema paindkontolt maha.

#### <a name="calculation-of-time"></a>Aja arvutamine

Aeg arvutatakse sisse- ja väljaregistreerimise vahelise ajana, s.t 06:30 kuni 14:45, mis võrdub 8,25 tunniga.

#### <a name="calculation-of-pay-time"></a>Tasustava aja arvutamine

Tasustatav aeg on aeg, mille eest on töötajale tagatud tasu. Sellest stsenaariumis on töötaja tööl 8,25 tundi (**Aeg**). Kuid **tasustatav aeg** arvutatakse 8,50 tunnina, kuna töötajale on tagatud tasu paind– perioodi jooksul pärast väljaregistreerimist. Tasustatav aeg võrdub plaanitud töötundidega, kuna paind+ aeg lisatakse töötaja paindkontole, mitte tasustatavale ajale. Puudumise aeg paind– perioodi jooksul kompsenseeritakse tasustatava ajaga ja arvestatakse maha töötaja paindkontolt.

| Aeg              | Registreerimise tüüp | Tasustatav aeg (tundides)      |
|-------------------|-------------------|-----------------------|
| 6:30–7:00 | Paind+             | 0                     |
| 7:00–14:45 | Standardaeg     | 7,75                  |
| 14:45–15:30 | Paind-             | 0,75 (puudumisperiood) |
|                   | Kokku             | 8,50                  |

### <a name="scenario-2-a-worker-works-during-the-whole-flex--period-and-also-works-overtime"></a>Stsenaarium 2: töötaja töötab kogu paind– perioodi ja teeb ka ületunnitööd

Töötaja selle päeva registreerimised näevad välja järgmised.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      |
|---------------------------|----------|----------|
| Sisseregistreerimine                  | 06:30 | 06:30 |
| Tootmistöö            | 06:30 | 17:00 |
| Väljaregistreerimine                 | 17:00 | 17:00 |

Kui olete arvutanud töölehe registreerimised lehel **Kinnita**, saate vaadata arvutustulemust vahekaardil **Ajad**. Selle stsenaariumi mõistmiseks vaadake järgmisi välju.

| Paind+ | Paind– | Aeg  | Tasustatav aeg | Tasustatav ületunnitöö |
|--------|--------|-------|----------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 1.50         |

#### <a name="calculation-of-flex"></a>Paind+ arvutamine

Paindreegli kohaselt on aeg kella 06:00 ja 07:00 AM vahel paind+ periood. Nii et kui töötaja registreerub sisse kell 06:30, teenib ta paindkontol 0,5 tundi paind+ aega.

#### <a name="calculation-of-flex-"></a>Paind– arvutamine

Kuna töötaja töötab paind– perioodi jooksul, siis paind– ei arvutata. Paind– arvutatakse ainult siis, kui töötaja puudub paind– perioodil. Makse perspektiivist on töötajale tagatud tasumäär, mis on määratud standardaja kohta, kui ta töötab paind– perioodi jooksul. Kui töötaja puudub paind– perioodil, arvatakse 45 minutit tema paindkontolt maha.

#### <a name="calculation-of-time"></a>Aja arvutamine

Aeg arvutatakse sisseregistreerimise aja kell 06:30 ja väljaregistreerimise aja kell 17:00 vahelise ajana ehk 10,50 tundi.

#### <a name="calculation-of-pay-time"></a>Tasustava aja arvutamine

Sellest stsenaariumis töötab töötaja 10,50 tundi (**Aeg**). Kuid **tasustatav aeg** arvutatakse 10,00 tunnina, kuna töötajale on tagatud tasu paind+ perioodi jooksul.

#### <a name="calculation-of-pay-overtime"></a>Tasustava ületunnitöö arvutamine

| Aeg               | Registreerimise tüüp | Tasustatav aeg (tundides) |
|--------------------|-------------------|------------------|
| 6:30–7:00  | Paind+             | 0                |
| 7:00–14:30  | Standardaeg     | 7,50             |
| 14:30–15:30  | Paind-             | 1,00             |
| 15:30–17:00 | Ületunnitöö          | 1.50             |
|                    | Kokku             | 10.00            |

### <a name="generation-of-pay-items"></a>Tasuüksuste loomine

Töötaja päeva registreerimisi saab lehelt **Kinnita** üle kanda. Ülekandmise ajal luuakse tasuüksused ja üle kantud registreerimised. Tasuüksused kujutavad tasustatava aja jaotust standardajaks, ületunnitööks, tasustatud vaheajaks jne.

Tasuüksuste loendi avamiseks valige **Tööajaarvestus** &gt; **Ülevaatamine ja kinnitamine** &gt; **Kinnita**. Seejärel valige **Päring** &gt; **Üle kantud registreerimised**.

Tasuüksused on töötaja tasu aluseks. Saate luua faili, mis sisaldab teavet tasuüksustest, ja kanda selle faili palgasüsteemi.

Osana ülekandmise protsessist kantakse aeg ja kulu tootmis- ning projektitegevustest tootmise ja projekti töölehtedesse, et arvestada aja ja kulu kulutusi. Üle kantud registreerimised on tootmistellimuste ja projektide aja ja kulu tunnihinna aluseks. Üle kantud registreerimisi saab avada menüüga **Päring** lehel **Kinnita**.

Näiteks luuakse stsenaariumi 2 jaoks järgmise tasuüksused.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss  | Kogumaksumus |
|---------------|----------|-----------|-------|------------|
| Standardaeg | 1201     | 10,0      | 10    | 100        |
| Ületunnitöö      | 1301     | 1.50      | 5     | 7,50       |
|               |          |           | Kokku | 107,50     |

Standardaja tasuüksuse makseühik on 10 tundi, mis katab standardaja, paind– aja ja ületunnitöö. Standardaeg, paind– aeg ja ületunnitöö liidetakse ühte tasuüksusesse, kuna kõiki neid tüüpe arvutatakse standardajana, lähtudes parameetri vaikesättest lehel **Arvutuse parameetrid** (**Tööajaarvestus** &gt; **Seadistamine** &gt; **Arvutuse parameetrid**). Ületunnitöö arvutatakse lisaks standardajale, kasutades lisamäära 5.

Kui soovite selgelt eristada standardaega ja ületunnitööd, nii et tasutüüpide tasuühikud kataksid ainult tegelikku standardajale ja ületunnitööle kulutatud aega, tuleb standardaja tasuühikud arvutada 8,50-na ning ületunnitöö tasuühikud tuleb arvutada 1,50-na.

Süsteemi konfigureerimiseks nii, et see eristaks selgelt standardaega ja ületunnitööd, peate ületunnitöö standardajast välja arvama. Peate ka muutma ületunnitöö tasutüübi seadistust, nii et ületunnitöö tasumäär kataks kõiki makseid tundide kohta, mis ületunnitööle kulutati.

### <a name="exclude-overtime-from-the-standard-time"></a>Ületunnitöö väljaarvamine standardajast

Valige lehel **Arvutuse parameetrid** profiili määratlustüübiks **Ületunnitöö** ja määrake suvand **Tasustatav aeg** väärtusele **Ei**, nagu on näidatud siin.

| Reg. spetsifikatsioon | Profiili täpsustuse tüüp | Kalkulatsioon   |     | Makstud         |     |
|--------------------|----------------------------|---------------|-----|--------------|-----|
| Tööaeg       | Ületunnitöö                   | Standardaeg | Jah | Tasustatav aeg     | Ei  |
|                    |                            | Tasustatav aeg      | Jah | Tasustatav ületunnitöö | Jah |

Pärast arvutuse parameetrite korrigeerimist luuakse järgmised tasuüksused.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss  | Kogumaksumus |
|---------------|----------|-----------|-------|------------|
| Standardaeg | 1201     | 8,50      | 10    | 85,0       |
| Ületunnitöö      | 1301     | 1.50      | sept.    | 22,50      |
|               |          |           | Kokku | 107,50     |

> [!NOTE]
> Arvutuse parameetritel on soovituslik standardsäte. Üldiselt peaksite neid parameetreid muutes olema ettevaatlik. Soovituslike standardsätete taastamiseks valige lehel **Arvutuse parameetrid** käsk **Taasta väärtused**.

### <a name="allow-a-deviation-from-the-standard-pay-profiles"></a>Hälbe lubamine standardtasu profiilidest

Lehel **Profiilid** (**Tööajaarvestus** &gt; **Seadistamine** &gt; **Ajareeglid** &gt; **Profiilid**) saate seadistada profiilitüübid, mis sisaldavad lülituskoode ja vaheaegu.

### <a name="switch-codes"></a>Lülituse koodid

Lülituskoode saate kasutada selleks, et lubada töötajatel oma profiilitüübist hälbida, muutes profiilitüüpi. Näiteks saate lubada töötajal minna üle paind+ ajalt ületunnitööle. Töötaja saab registreerimise ajal lülituskoodi lisada või teie saate määrata lülituskoodi lisamise ülesande registreerimiste kinnitajale.

Enne kui lülituskoodi saab kasutada, peate selle määrama kaudse tegevuse tüübina. Seejärel peate lisama lülituskoodi selle perioodi ajaprofiilile, mille profiilitüübi muutust soovite lubada. Näiteks järgige neid etappe, et luua lülituskood, millega saab paind+ perioodi muuta kell 06:00 kuni 07:00 ületunnitööks.

1. Looge lülituskood nimega **OTBCI (mine enne sisseregistreerimist paindeajalt üle ületunnitööle)**. Valige **Tööajaarvestus** &gt; **Kaudsete tegevuste haldamine** &gt; **Kaudsed tegevused**.
2. Lisage veergu **Lülituskood** ajaprofiili paind+ reale OTBCI.
3. Veergu **Teisene** lisage profiilitüüp **Ületunnitöö**.

Arvestage järgmist paindprofiili, mis kujutab tööpäeva.

| Profiili tüüp  | Käivita    | Lõpp      | Päev     |
|---------------|----------|----------|---------|
| Ületunnitöö     | 00:00 | 06:00 | esmaspäev  |
| Paind+         | 06:00 | 07:00 | esmaspäev  |
| Sisseregistreerimine      | 07:00 | 07:00 | esmaspäev  |
| Standardaeg | 07:00 | 14:30 | esmaspäev  |
| Paind-         | 14:30 | 15:30 | esmaspäev  |
| Väljaregistreerimine     | 15:30 | 15:30 | esmaspäev  |
| Ületunnitöö     | 15:30 | 06:00 | teisipäev |

Siin on töötaja selle päeva registreerimised.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      |
|---------------------------|----------|----------|
| Sisseregistreerimine                  | 06:30 | 06:30 |
| Tootmistöö            | 06:30 | 14:45 |
| Väljaregistreerimine                 | 17:00 | 17:00 |

Pärast ülekandmist luuakse järgmised tasuüksused.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss  | Kogumaksumus |
|---------------|----------|-----------|-------|------------|
| Standardaeg | 1201     | 8,50      | 10    | 85,0       |
| Ületunnitöö      | 1305     | 1.50      | sept.    | 22,50      |
|               |          |           | Kokku | 107,50     |

Võtke lehel **Kinnita** ülekandmine tagasi ja kasutage seejärel menüüd **Lülituskood**, et rakendada lülituskoodi **OTBCI**. Kui kannate registreerimise üle teist korda, luuakse järgmised tasuüksused.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss  | Kogumaksumus |
|---------------|----------|-----------|-------|------------|
| Standardaeg | 1201     | 8,50      | 10    | 80,0       |
| Ületunnitöö      | 1305     | 2.00      | sept.    | 30,0       |
|               |          |           | Kokku | 107,50     |

> [!NOTE]
> Lülituskoodi rakendades suureneb ületunnitöö 0,5 tunni võrra 1,50-lt 2,00-le. 0,5 tundi on registreeritud paind+ aja 6:30 kuni 07:00 teisendus ületunnitööks.

### <a name="breaks"></a>Vaheajad

Tööpausid mõjutavad töötaja tasu arvutamist. Pausid määratletakse kaudse tegevuse tüübina. Neid saab määratleda kui **Tasustatud**, et pausi saaks lisada töötaja tasule, või kui **Tasustamata**, et pausi ei saaks lisada töötaja tasule. Pausi saab määratleda ka kui **Plaanitud** või **Registreeritud**.

#### <a name="planned-breaks"></a>Plaanitud pausid

Kui ettevõttel on fikseeritud vaheaeg, nt kindlaks määratud lõunapaus, saab pausi ajaprofiilis eelmääratleda. Sellisel juhul ei pea töötaja registreerima pausi töökaardi lehtedel. Selle asemel arvestatakse pausiga automaatselt, kui töötaja registreerimised arvutatakse lehel **Kinnita**.

#### <a name="registered-breaks"></a>Registreeritud puhkepausid

Kui ettevõttel puuduvad plaanitud pausid, saavad töötajad pause registreerida tööpäeva jooksul. Registreeritud pause saab kasutada näiteks siis, kui töötaja töötab paindaja profiiliga, millel puuduvad määratletud sisse- ja väljaregistreerimisajad. Registreeritud pausid on kaudse tegevuse tüübid. Töötaja registreerib pausi **töökaardi** terminali lehel või **töökaardi** seadme lehel. Mõlemal lehel saab kasutaja valida pausi tüübi eelmääratud pausitegevuste loendist.

#### <a name="paid-and-unpaid-breaks"></a>Tasustatud ja tasustamata pausid

Pausitegevusi saab seadistada kui **Tasustatud** või **Tasustamata**. Tasustatud paus lisatakse tasustatud aja arvutusse ja süsteem kasutab tasutüüpi, mis on määratletud **pausi** registreerimise tüübi tasuleppes.

### <a name="example-of-a-planned-break"></a>Plaanitud pausi näide

Arvestage järgmist ajaprofiili, mis sisaldab maksmata lõunapausi.

| Profiili tüüp  | Käivita    | Lõpp      | Päev     |
|---------------|----------|----------|---------|
| Ületunnitöö     | 00:00 | 06:00 | esmaspäev  |
| Paind+         | 06:00 | 07:00 | esmaspäev  |
| Sisseregistreerimine      | 07:00 | 07:00 | esmaspäev  |
| Standardaeg | 07:00 | 12:00 | esmaspäev  |
| Paus         | 12:00 | 12:30 | esmaspäev  |
| Standardaeg | 12:30 | 14:30 | esmaspäev  |
| Paind-         | 14:30 | 15:30 | esmaspäev  |
| Väljaregistreerimine     | 15:30 | 15:30 | esmaspäev  |
| Ületunnitöö     | 15:30 | 06:00 | teisipäev |

Siin on töötaja selle päeva registreerimised.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      |
|---------------------------|----------|----------|
| Sisseregistreerimine                  | 06:30 | 06:30 |
| Tootmistöö            | 06:30 | 14:45 |
| Väljaregistreerimine                 | 17:00 | 17:00 |

Kui olete arvutanud töölehe registreerimised lehel **Kinnita**, saate vaadata arvutustulemust vahekaardil **Ajad**. Selle stsenaariumi mõistmiseks vaadake järgmisi välju.

| Paind+ | Paind– | Aeg  | Tasustatav aeg | Tasustamata vaheaja aeg | Tasustatav ületunnitöö |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

> [!NOTE] 
> Süsteem arvutas tasustamata vaheaja ajast 0,5 tundi ja see aeg pole osa tasustatud ajast.

### <a name="example-of-a-registered-break"></a>Registreeritud pausi näide

Arvestage järgmist ajaprofiili, mis ei sisalda plaanitud pause.

| Profiili tüüp  | Käivita    | Lõpp      | Päev     |
|---------------|----------|----------|---------|
| Ületunnitöö     | 00:00 | 06:00 | esmaspäev  |
| Paind+         | 06:00 | 07:00 | esmaspäev  |
| Sisseregistreerimine      | 07:00 | 07:00 | esmaspäev  |
| Standardaeg | 07:00 | 14:30 | esmaspäev  |
| Paind-         | 14:30 | 15:30 | esmaspäev  |
| Väljaregistreerimine     | 15:30 | 15:30 | esmaspäev  |
| Ületunnitöö     | 15:30 | 06:00 | teisipäev |

Siin on töötaja selle päeva registreerimised.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      |
|---------------------------|----------|----------|
| Sisseregistreerimine                  | 06:30 | 06:30 |
| Tootmistöö            | 06:30 | 17:00 |
| Paus                     | 12:03 | 12:32 |
| Väljaregistreerimine                 | 17:00 | 17:00 |

Registreerimiste arvutamisel arvutatakse tegevuste aeg.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      | Aeg  |
|---------------------------|----------|----------|-------|
| Sisseregistreerimine                  | 06:30 | 06:30 |       |
| Tootmistöö            | 06:30 | 17:00 | 10.00 |
| Paus                     | 12:03 | 12:32 | 0,50  |
| Väljaregistreerimine                 | 17:00 | 17:00 |       |

> [!NOTE]
> Vaheaja aeg on paralleelne tegevuse ajaga (selles näites tootmistöö). Sellist käitumist kasutatakse alati pausitegevuste jaoks. Registreerimiste arvutamistel lahutatakse vaheaja aeg tegevuse ajast maha. Sellisel juhul on tootmistöö kestus 10,50 tundi, aga aeg arvutatakse 10-na, kuna vaheaja aeg 0,5 tundi lahutatakse tegevuse ajast maha.

Kui olete arvutanud töölehe registreerimised lehel **Kinnita**, saate vaadata arvutustulemust vahekaardil **Ajad**. Selle stsenaariumi mõistmiseks vaadake järgmisi välju.

| Paind+ | Paind– | Aeg  | Tasustatav aeg | Tasustamata vaheaja aeg | Tasustatav ületunnitöö |
|--------|--------|-------|----------|---------------------|--------------|
| 0,50   | 0,00   | 10,50 | 9,50     | 0,5                 | 1.50         |

Kui plaanitud paus on tasustatud, mitte tasustamata, näeb arvutustulemus välja selline.

| Paind+ | Paind– | Aeg  | Tasustatav aeg | Tasustatud vaheaja aeg | Tasustatav ületunnitöö |
|--------|--------|-------|----------|-----------------|--------------|
| 0,50   | 0,00   | 10,50 | 10.00    | 0,5             | 1.50         |

### <a name="pay-items-and-paid-breaks"></a>Tasuüksused ja tasustatud pausid

Kui kannate registreerimised üle lehele **Kinnita**, luuakse tasuüksused. Tasustatud pauside jaoks luuakse eraldi tasuüksus.

Tasustatud pausi jaoks määratakse tasumäär tasutüübi järgi, mis on seadistatud pausi tasuleppes. Tasutüübi kasutamise asemel saate seadistada pausi tunni omahinna määratud kuupäevaintervallis.

Juhinduge järgmisest ajaprofiilist.

| Profiili tüüp  | Käivita    | Lõpp      | Päev     |
|---------------|----------|----------|---------|
| Ületunnitöö     | 00:00 | 06:00 | esmaspäev  |
| Paind+         | 06:00 | 07:00 | esmaspäev  |
| Sisseregistreerimine      | 07:00 | 07:00 | esmaspäev  |
| Standardaeg | 07:00 | 14:30 | esmaspäev  |
| Paind-         | 14:30 | 15:30 | esmaspäev  |
| Väljaregistreerimine     | 15:30 | 15:30 | esmaspäev  |
| Ületunnitöö     | 15:30 | 06:00 | teisipäev |

Siin on töötaja selle päeva registreerimised.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      | Aeg |
|---------------------------|----------|----------|------|
| Sisseregistreerimine                  | 07:00 | 07:00 |      |
| Tootmistöö            | 07:00 | 15:00 | 7,5  |
| Paus (tasustatud)              | 12:00 | 12:30 | 0,5  |
| Väljaregistreerimine                 | 15:00 | 15:00 |      |

Selles näites on standardaja tasutüüp seatud väärtusele **1201** ja tasuleppes on seadistatud tasumäär **10**. Tasustatud pausi tüüp on **1301** ja tasumäär on **8**. Kui registreerimise kantakse üle teist korda, luuakse järgmised tasuüksused.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 7,50      | 10   |
| Paind-         | 1201     | 0,50      | 10   |
| Paus (tasustatud)  | 1301     | 0,50      | 8    |

## <a name="how-the-cost-of-paid-breaks-is-allocated-to-projects-and-production-orders"></a>Tasustatud pauside tulu jaotus eraldamine projektidele ja tootmistellimustele

Projekti tegevuste ja tootmistööde tunnikulu saab seadistada nii, et see määratakse kas tasumäärade järgi, mis arvutatakse tööajaarvestuses, või kulukategooriate järgi, mis määratakse tegevuste jaoks.

Kulukategooria seadistamiseks valige **Tootmise juhtimine** &gt; **Setup** &gt; **Tootmise käivitamine** &gt; **Tootmistellimuse vaikesätted** ja määrake väli **Kulukategooria** väärtusele **Jah** või **Ei**.

- **Ei** – kulu arvutatakse tööajaarvestuse registreerimistüüpide jaoks määratud tasumäärade põhjal.
- **Jah** – kulu arvutatakse tootmis- ja projektitegevuste kulukategooriate põhjal.

### <a name="cost-calculation-based-on-pay-rates-that-are-calculated-in-time-and-attendance"></a>Tööajaarvestuses arvutatud tasumääradel põhinev kuluarvutus

Järgmises näites on näidatud, kuidas arvutatakse tunnikulu, kui kulu on seadistatud nii, et see arvutatakse tasumäärade põhjal.

Tunnikulu määr, mida tootmistellimuste ja projektide jaoks kasutatakse, arvutatakse ülekandeprotsessi ajal. Tegevuse tunnimäära vaatamiseks avage tööajaarvestuses leht **Kinnita** ja valige **Päring** &gt; **Üle kantud registreerimised**. Registreerimise tunni kulumäära leiate vahekaardilt **Omahinnad**.

Arvestage järgmisi registreerimisi, mis kasutavad sama ajaprofiili kui eelmises näites.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      | Aeg |
|---------------------------|----------|----------|------|
| Sisseregistreerimine                  | 07:00 | 07:00 |      |
| Protsess (tellimus: 4711)     | 07:00 | 11:00 | 4    |
| Protsess (tellimus: 4712)     | 11:00 | 15:00 | 3,50 |
| Paus (tasustatud)              | 12:00 | 12:30 | 0,50 |
| Väljaregistreerimine                 | 15:00 | 15:00 |      |

Pärast registreerimiste ülekandmist, luuakse järgmised üle kantud registreerimised.

| Registreerimise tüüp     | Aeg | Tunni omahind |
|-----------------------|------|---------------------|
| Sisseregistreerimine              | 0,00 | 0,00                |
| Protsess (tellimus: 4711) | 4,00 | 10.00               |
| Protsess (tellimus: 4712) | 3,50 | 11,14               |
| Paus (tasustatud)          | 0,50 | 0,00                |
| Väljaregistreerimine             | 0,00 | 0,00                |

Tasustatud pausi tunni kuluhinna arvutus oleneb otseste palgakulude sättest. Valige **Tööajaarvestus** &gt; **Seadistus** &gt; **Tööajaarvestuse parameetrid**. Vahekaardil **Omahind** jaotises **Otsesed palgakulud** väljas **Standardaeg** saate valida väärtuse **Jah**, **Ei** või **Eraldamine**.

- **Jah** – seda väärtust kasutatakse eelnevas näites. Kulu eraldatakse tootmis- või projektitegevusele, mis on paralleelne tasustatud pausi tegevusega. Näites on see tegevus tellimuse 4712 tootmistöö. Nagu näete, on tasustatud pausi tunni omahind 0 (null) ja see eraldatakse tööle, mis on paralleelne pausiga.

    Tasustatud pausi kestus on 0,5 tundi ja tasumäär on 8. Seega on tasustatud pausi kogukulu 4. Seejärel eraldatakse kogukulu 3,5-tunnisele protsessitööle. Seega panustab tasustatud paus kulusse 1,14 tunni kohta (4 ÷ 3,5 = 1,14).

- **Eraldamine** – tasustatud paus jagatakse võrdselt selle päeva kohta registreeritud töödele. Kui seda väärtust kasutatakse eelnevas näites, luuakse järgmised üle kantud registreerimised.

    | Registreerimise tüüp     | Aeg | Tunni omahind |
    |-----------------------|------|---------------------|
    | Sisseregistreerimine              | 0,00 | 0,00                |
    | Protsess (tellimus: 4711) | 4,00 | 10,53               |
    | Protsess (tellimus: 4712) | 3,50 | 10,53               |
    | Paus (tasustatud)          | 0,50 | 0,00                |
    | Väljaregistreerimine             | 0,00 | 0,00                |

    Kahe tootmistöö töötlemisaeg kokku on 7,5 tundi ja tasustatud pausi kogukulu on 4. Seega on pausi kulu arvutustulemus 0,53 (= 4 ÷ 7,5).

- **Ei** – tasustatud pausi kulu ei suurenda protsessitegevuste tunnikulu.

    | Registreerimise tüüp     | Aeg | Tunni omahind |
    |-----------------------|------|---------------------|
    | Sisseregistreerimine              | 0,00 | 0,00                |
    | Protsess (tellimus: 4711) | 4,00 | 10.00               |
    | Protsess (tellimus: 4712) | 3,50 | 10.00               |
    | Paus (tasustatud)          | 0,50 | 0,00                |
    | Väljaregistreerimine             | 0,00 | 0,00                |

## <a name="absence"></a>Puudumine

Töötaja puudumise perioodi registreerimiseks kasutatakse puudumiskoodi. Puudumiskood on, nagu pausid ja lülituskoodid, kaudse tegevuse tüüp. Puudumise aeg võib olla plaanitud või registreeritud ja puudumine võib olla põhjusega või põhjuseta. Põhjusega puudumise näited on arstivisiit, seminar või vandekohtuniku kohustuse täitmine. Põhjuseta puudumine on puudumine, mille pole head põhjust, näiteks hilinemine tööle. Tavaliselt ei vähenda põhjusega puudumine töötaja tasu, põhjuseta puudumine aga vähendab.

### <a name="planned-absence"></a>Planeeritud puudumine

Saate töötajate luua plaanitud puudumisi lehel **Plaanitud puudumise loomine** (**Tööajaarvestus** &gt; **Plaanitud puudumise loomine**). Seal registreeritakse plaanitud puudumine töölt puudumisena konkreetse kuupäeva ja kellaaja intervalliga.

Töö põhineb päringul. Seega saate luua plaanitud puudumise mitmele töötajale, näiteks töötajatele, kes kuuluvad samasse kalkulatsioonigruppi. Kui plaanitud puudumine kehtib ühele töötajale, saab registreerimise sisestada lehel **Kohalolek** või **Kellaaja registreerimisega töötajad**.

- Puudumise registreerimise sisestamiseks lehel **Kohalolek** valige **Tööajaarvestus** &gt; **Päringud ja aruanded** &gt; **Kohalolek** &gt; **Kohalolek** ja seejärel valige **Puudumise registreerimine**.
- Puudumise registreerimise sisestamiseks lehelt *<strong><em>Ajalise registreerimise töötajad</em></strong>* valige <strong>Tööajaarvestus</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Kellaaja registreerimisega töötajad</strong> ja seejärel valige vahekaardil <strong>Kellaaeg</strong> jaotises <strong>Kellaaja määramine</strong> suvand <strong>Puudumise registreerimised</strong>.

Aruannet **Plaanitud puudumised** saate kasutada töötajate plaanitud puudumiste ülevaate nägemiseks. Aruande avamiseks valige **Tööajaarvestus** &gt; **Päringud ja aruanded** &gt; **Puudumise aruanded** &gt; **Plaanitud puudumised**.

### <a name="registered-absence"></a>Registreeritud puudumine

Üldiselt arvestatakse töötajad puuduvaks siis, kui nad pole plaanitud sisse- ja väljaregistreerimise ajal mingi perioodi jooksul tööl. Kui töötajad registreeruvad sisse plaanitust hiljem või registreeruvad välja plaanitust varem, palutakse neil valida puudumiskood, et esitada puudumise põhjus. Puudumiskoodi saab seadistada nii, et see oleks kohaldatav registreerimisele. Ainult kohaldatavad koodid on loendis valimiseks saadaval.

## <a name="scenarios-based-on-various-combinations-of-work-hour-registrations"></a>Töötundide registreerimiste eri kombinatsioonidel põhinevad stsenaariumid

Järgmised stsenaariumid näitavad tasuüksuseid ja kinnitatavaid kirjeid, mis luuakse töötajatele nende registreerimiste põhjal. Kõik need stsenaariumid põhinevad järgmisel ajaprofiilil.

| Profiili tüüp  | Käivita    | Lõpp      | Päev     |
|---------------|----------|----------|---------|
| Ületunnitöö     | 00:00 | 06:00 | esmaspäev  |
| Paind+         | 06:00 | 07:00 | esmaspäev  |
| Sisseregistreerimine      | 07:00 | 07:00 | esmaspäev  |
| Standardaeg | 07:00 | 14:30 | esmaspäev  |
| Paind-         | 14:30 | 15:30 | esmaspäev  |
| Väljaregistreerimine     | 15:30 | 15:30 | esmaspäev  |
| Ületunnitöö     | 15:30 | 06:00 | teisipäev |

### <a name="scenario-1-the-worker-clocks-in-later-than-planned"></a>Stsenaarium 1: töötaja registreerib sisse plaanitust hiljem

Töötaja registreerib sisse kell 08:30. Kuna plaanitud sisseregistreerimise aeg on 07:00, jääb töötaja tööle 1,50 tundi hiljaks. Kuna seda 1,50 tundi arvestatakse puudumisena, palutakse töötajal valida puudumiskood. Töötaja lahkub töölt kell 15:30, mis on plaanitud väljaregistreerimise aeg. Kui töötaja registreerimised arvutatakse ja kinnitatakse, kuvatakse ajavahemiku 07:00 kuni 08:30 kohta puudumise registreerimine koos töötaja valitud puudumiskoodiga.

Ajaprofiilis saate konfigureerida registreerimistüübi **Sisseregistreerimine** nii, et töötajate hilinemise korral on olemas kõikumine. Näiteks kui seadistate kõikumise väärtusega 5, palutakse töötajal sisestada puudumiskood, kui ta registreerib sisse hiljem kui 07:05.

Sellisel juhul valib töötaja põhjuseta puudumise jaoks määratud puudumiskoodi, kuna tal puudub hilinemiseks hea põhjus. Puudumiskoodi arvestatakse põhjuseta puudumise suhtes kehtivaks, kui ületunnitöö mahaarvamise säte on lubatud selles puudumisgrupis, kuhu puudumiskood kuulub. Sätte seadistamiseks valige **Tööajaarvestus** &gt; **Seadistamine** &gt; **Grupid** &gt; **Puudumisgrupid** ja seejärel märkeruut **Arva ületunnitöö maha**.

Siit näete, kuidas näevad välja töötaja registreerimised päeva kohta lehel **Kinnita** pärast arvutamist.

| Töölehe registreerimise tüüp         | Käivita    | Lõpp      | Aeg |
|-----------------------------------|----------|----------|------|
| Puudumine (põhjuseta – hilinemine tööle) | 07:00 | 08:30 | 1.5  |
| Sisseregistreerimine                          | 08:30 | 08:30 |      |
| Tootmistöö                    | 07:30 | 15:30 | 7.0  |
| Väljaregistreerimine                         | 15:30 | 15:30 |      |

Siin on toodud tulemuseks saadud tasuüksus pärast registreerimiste ülekandmist.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 7,00      | 10   |

### <a name="scenario-2-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-standard-time-period"></a>Stsenaarium 2: töötaja registreerib välja enne plaanitud väljaregistreerimise aega standardse ajaperioodi jooksul

Töötaja teeb sisseregistreerimise kell 07:00 ja varase väljaregistreerimise kell 13:00. Kuna 13:00 on enne plaanitud väljaregistreerimist kell 15:30 ja 13:00 jääb standardse ajaperioodi sisse, palutakse töötajal valida puudumiskood. Töötaja valib arstivisiidi puudumiskoodi, mis on määratud põhjusega puudumisena. Põhjusega puudumise tasumäär on määratud registreerimistüübi **Puudumine** tasulepetes (**Tööajaarvestus** &gt; **Seadistamine** &gt; **Palk** &gt; **Tasulepped**).

Siit näete, kuidas näevad välja töötaja registreerimised päeva kohta lehel **Kinnita** pärast arvutamist.

| Töölehe registreerimise tüüp              | Käivita    | Lõpp      | Aeg |
|----------------------------------------|----------|----------|------|
| Sisseregistreerimine                               | 07:00 | 07:00 |      |
| Tootmistöö                         | 07:00 | 13:00 | 4,0  |
| Väljaregistreerimine                              | 13:00 | 13:00 |      |
| Puudumine (põhjusega – arstivisiit) | 13:00 | 15:30 | 3.5  |

Siin on toodud tulemuseks saadud tasuüksus pärast registreerimiste ülekandmist.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 7,50      | 10   |

### <a name="scenario-3-the-worker-clocks-out-before-the-planned-clock-out-time-during-a-flex--period"></a>Stsenaarium 3: töötaja registreerib välja enne plaanitud väljaregistreerimise aega paind– perioodi jooksul

Töötaja registreerib sisse kell 07:00 ja välja kell 14:15, mis jääb plaanitud paind– perioodi sisse. Aeg tegeliku väljaregistreerimise aja ja plaanitud väljaregistreerimise aja vahel ei arvestata puudumisena ning töötajal ei paluta valida puudumiskoodi. Summa arvestatakse töötaja paindkontolt maha ja töötajale tagatakse tasu ülejäänud paind– perioodi jooksul ajavahemikus 14:15 kuni 15:30.

Siit näete, kuidas näevad välja töötaja registreerimised päeva kohta lehel **Kinnita** pärast arvutamist.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      | Aeg |
|---------------------------|----------|----------|------|
| Sisseregistreerimine                  | 07:00 | 07:00 |      |
| Tootmistöö            | 07:00 | 14:15 | 7,25 |
| Väljaregistreerimine                 | 14:15 | 14:15 |      |

Siin on toodud tulemuseks saadud tasuüksus pärast registreerimiste ülekandmist.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 8,50      | 10   |

### <a name="scenario-4-the-worker-clocks-in-late-and-clocks-out-after-the-planned-clock-out-time-during-an-overtime-period"></a>Stsenaarium 4: töötaja registreerib sisse hilja ja registreerib välja pärast plaanitud väljaregistreerimise aega ületunnitöö perioodi jooksul

Töötaja registreerib sisse hilja kell 09:30 ja teeb hilinemise kompenseerimiseks ületunnitööd ning registreerib välja kell 17:00. Kuna töötaja saabus hilja ja kompenseeris seda hilja töötamisega, ei taha ettevõte tagada töötajale ületunnitöötasu aja eest, mis ta töötas plaanitud väljaregistreerimise aja kell 15:30 ja tegeliku väljaregistreerimise aja kell 17:00 eest, isegi kui see periood on ajaprofiilis määratletud kui ületunnitöö.

Selle stsenaariumiga tegelemiseks saab puudumiskoodi seada vähendama ületunnitöö tunde põhjuseta puudumise tundide võrra, mis on töötajal tekkinud sama päeva jooksul. Valige **Tööajaarvestus** &gt; **Seadistamine** &gt; **Grupid** &gt; **Puudumisgrupid** ja seejärel märkeruut **Arva ületunnitöö maha**, et arvestada põhjuseta puudumine maha ületunnitöö tundidelt.

Siit näete, kuidas näevad välja töötaja registreerimised päeva kohta lehel **Kinnita** pärast arvutamist.

| Töölehe registreerimise tüüp         | Käivita    | Lõpp      | Aeg |
|-----------------------------------|----------|----------|------|
| Puudumine (põhjuseta – hilinemine tööle) | 07:00 | 09:30 | 1.5  |
| Sisseregistreerimine                          | 09:30 | 09:30 |      |
| Tootmistöö                    | 09:30 | 17:00 | 7,5  |
| Väljaregistreerimine                         | 17:30 PM | 17:30 PM |      |

Kui valitud puudumiskoodi kohta on valitud märkeruut **Arva ületunnitöö maha**, arvatakse ületunnitöö tasust maha tunnid, mille jooksul töötaja põhjuseta puudus. Sellisel juhul luuakse pärast registreerimise ülekandmist järgmised tasuüksused.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 9,00      | 10   |
| Ületunnitöö      | 1301     | 0,5       | sept.   |

Siin arvatakse 1,5 tundi põhjuseta puudumist ajavahemikus 07:00 kuni 09:30 maha 2,0 tunnist ületunnitööst ajavahemikus 15:30 kuni 17:30. Registreerimise tulemus on 1,5 tundi standardaega ja 0,5 tundi ületunnitööd.

Kui aga märkeruut **Arva ületunnitöö maha** ei ole puudumiskoodi jaoks valitud, tagatakse töötajale tasu ületunnitöö eest, isegi kui ta tööle hilines ja tal oli põhjuseta puudumine. Sellisel juhul luuakse pärast registreerimise ülekandmist järgmised tasuüksused.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 7,50      | 10   |
| Ületunnitöö      | 1301     | 2,0       | sept.   |

### <a name="scenario-5-the-worker-clocks-out-before-the-planned-clock-out-time-and-can-convert-the-absence-period-to-a-flex--period"></a>Stsenaarium 5: töötaja registreerib välja enne plaanitud väljaregistreerimise aega ja saab puudumisperioodi teisendada paind– perioodiks

Järgmises näites on näha, kuidas saab töötaja paindkontot vähendada, teisendades puudumisperioodi paind– perioodiks.

Töötaja teeb sisseregistreerimise kell 07:00 ja väljaregistreerimise kell 13:00. Tal on ülevaatajaga kokkulepe, et ta võib minna nädalavahetuseks koju, kui arvestab need tunnid oma paindkontolt maha. Kui töötaja registreerib välja kell 13:00, palutakse tal valida puudumiskood, kuna tööpäeva ülejäänud osa puudumisperiood ei ole plaanitud paind– periood. Tööpäeva ülejäänud osa teisendamiseks paind– perioodiks saab töötaja valida puudumiskoodi, mis seadistatakse tema paindkonto vähendamiseks.

Paindtundide saldo vähendamiseks töötajatel, kes registreerivad puudumise tööpäeval, valige **Tööajaarvestus** &gt; **Seadistamine** &gt; **Grupid** &gt; **Puudumisgrupid** ja valige märkeruut **Vähenda paindväärtust**.

Siit näete, kuidas näevad välja töötaja registreerimised päeva kohta lehel **Kinnita** enne arvutamist.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      | Aeg |
|---------------------------|----------|----------|------|
| Sisseregistreerimine                  | 07:00 | 07:00 |      |
| Tootmistöö            | 07:00 | 13:00 | 6,0  |
| Väljaregistreerimine                 | 13:00 | 13:00 |      |

Kui töötaja valib põhjuseta puudumise jaoks puudumiskoodi, siis näeb tulemuseks saadud tasuüksus pärast registreerimise ülekandmist välja selline.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 6,00      | 10   |

Kui töötaja valib põhjuseta puudumisele puudumiskoodi ja puudumiskood on seadistatud vähendama tema paindkontot, siis tulemuseks saadud tasuüksused näevad pärast registreerimiste ülekandmist välja sellised.

| Töötasu tüüp     | Tasu tüüp | Makseühikud | Kurss |
|---------------|----------|-----------|------|
| Standardaeg | 1201     | 8,50      | 10   |

Sellisel juhul vähendatakse töötaja paindsaldot tundide võrra tegeliku ja plaanitud väljaregistreerimise aja vahel (ehk 2,5 tundi ajavahemikus 13:00 kuni 15:30).

> [!NOTE]
> Me ei soovita puudumiskoodi jaoks valida nii märkeruudu **Arva paindväärtus maha** kui ka märkeruudu **Arva ületunnitöö maha**, kuna see seadistus arvestab maha põhjuseta puudumise tunnid töötaja ületunnitöölt ja vähendab samas töötaja paindkontot.

### <a name="scenario-6-there-is-no-planned-absence-for-the-day-and-no-worker-attendance-for-the-day"></a>Stsenaarium 6: päeval puudub plaanitud puudumine ja töötaja ei ilmu tööle

Kui töötaja ei ilmu tööpäeval tööle ja tal puudub sel päeval plaanitud puudumine, kasutatakse töötaja registreerimiste arvutamiseks vaikimisi puudumiskoodi. Vaikimisi puudumiskoodide määramiseks valige **Tööajaarvestus** &gt; **Tööajaarvestuse parameetrid**. Seejärel saate valida puudumiskoodi järgmistes väljades.

- Paind– automaatsisestus
- Puudumise automaatsisestus

Kui arvutatakse päevased registreerimised töötaja kohta, kellel on paindtunnid lubatud, kasutatakse väljas **Paind– automaatsisestus** määratud puudumiskoodi vaikimisi puudumiskoodina. Kui töötajal ei ole paindtunnid lubatud, kasutatakse väljas **Puudumise automaatsisestus** määratud puudumiskoodi. Kui ettevõttel on kombinatsioon töötajatest, kellel on paindtunnid lubatud, ja töötajatest, kellel ei ole paindtunnid lubatud, tuleb seadistada mõlemad parameetrid.
