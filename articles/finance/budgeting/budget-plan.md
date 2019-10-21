---
title: Eelarve plaanimine
description: Selle ülesande eesmärk on anda juhendatud ülevaade Microsoft Dynamics 365 Finance'i funktsioonivärskendustest eelarve plaanimise alal. Selle ülesande eesmärk on illustreerida kiiret eelarve plaanimise mooduli konfigureerimise näidet ja näidata, kuidas selle konfiguratsiooni abil on võimalik eelarvet plaanida.
author: ShylaThompson
manager: AnnBe
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a59ff16555bfcb55d2f21c09675e7ae0637bca8f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188598"
---
# <a name="budget-planning"></a>Eelarve plaanimine

[!include [banner](../includes/banner.md)]

Selle ülesande eesmärk on anda juhendatud ülevaade Microsoft Dynamics 365 Finance'i funktsioonivärskendustest eelarve plaanimise alal. Selle ülesande eesmärk on illustreerida kiiret eelarve plaanimise mooduli konfigureerimise näidet ja näidata, kuidas selle konfiguratsiooni abil on võimalik eelarvet plaanida.  See ülesanne keskendub konkreetselt järgmistele äriprotsessidele või ülesannetele.
- Organisatsiooni hierarhia loomine eelarve plaanimise jaoks ja kasutaja turvalisuse konfigureerimine
- Eelarveplaani stsenaariumide, eelarveplaani veergude, paigutuste ja Exceli mallide määratlemine
- Eelarve plaanimise protsessi loomine ja aktiveerimine
- Eelarveplaani dokumendi loomine pearaamatust tegelikke kulusid tõmmates
- Eraldamiste kasutamine eelarveplaani dokumendi andmete korrigeerimiseks
- Eelarveplaani dokumendi andmete redigeerimine Excelis 

<a name="prerequisites"></a>Eeltingimused 
------------------

Selle õppetüki saamiseks vajate juurdepääsu Microsoft Dynamics 365 Finance keskkonda Contoso demoandmetega ja peate olema eksemplaris administraatori õigustega. Ärge kasutage selle ülesande puhul privaatbrauseri režiimi – vajaduse korral logige brauseri muult kontolt välja ja logige sisse administraatori mandaatidega. Sisselogimisel **PEATE** märkima ruudu Hoia mind sisselogituna. See loob püsiva küpsise, mida Exceli rakendus praegu vajab. Kui logite rakendusse sisse muu brauseriga kui IE, siis palutakse teil Exceli rakenduses sisse logida. Exceli rakenduses suvandi Sisselogimine klõpsamine avab IE hüpikakna ja sisselogimisel **PEATE** märkima ruudu Hoia mind sisselogituna. Kui Exceli rakenduses suvandi Sisselogimine klõpsamine midagi ei tee, peaksite IE küpsiste vahemälu tühjendama.

## <a name="scenario-overview"></a>**Stsenaariumi ülevaade**
Julia töötab Saksamaa ettevõttes Contoso Entertainment Systems (DEMF) finantshaldurina. FY2016 lähenemisel peab ta töötama eelseisva aasta ettevõtte eelarve seadistamise osas. Eelarve koostamine näeb välja järgmine.

1.  Julia kasutab eelarve loomise lähtepunktina eelmise aasta tegelikke summasid.
2.  Eelmise aasta tegelike summade põhjal loob ta eelseisva aasta 12 kuu hinnangud.
3.  Julia vaatab eelarve CFO-ga üle. Kui see on tehtud, teeb ta eelarveplaani vajalikke korrigeerimisi ja lõpetab eelarve koostamise.

Eelarve plaanimise konfiguratsiooniskeem stsenaariumi puhul näeb välja järgmine.

![Eelarve plaanimise konfiguratsiooniskeem](./media/screenshot1-300x152.png)

Julia kasutab eelarve ettevalmistamiseks järgmist Exceli malli.

[![Exceli mall](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

## <a name="exercise-1-configuration"></a>1. harjutus: konfiguratsioon

### <a name="task-1-create-organizational-hierarchy"></a>**1. ülesanne: organisatsioonihierarhia loomine**
Kuna kogu eelarveprotsess toimub finantsosakonnas, peab Julia seega looma väga lihtsa organisatsiooni hierarhia – mis koosneb ainult finantsosakonnast. 1.1. Navigeerige jaotisse Organisatsioonihierarhiad (Organisatsiooni haldus &gt; Organisatsioonid &gt; Organisatsioonihierarhiad) ja klõpsake nuppu Uus

![Organisatsioonihierarhia](./media/screenshot3.png) 

1.2. Tippige organisatsioonihierarhia nimi ja klõpsake nuppu Määra eesmärk

[![Nimi](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Valige suvand Eelarve plaanimise eesmärk, klõpsake nuppu Lisa ja määrake vastloodud organisatsioonihierarhia: 

[![Eesmärgi määramine](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Korrake ülaltoodud etappi organisatsiooni turvalisuse eesmärgi puhul. Lõpetamisel sulgege vorm.

[![Turvaorganisatsioon](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Klõpsake vormil Organisatsiooni hierarhia nuppu Kuva. Klõpsake hierarhia kujundajas nuppu Redigeeri ja looge hierarhia, klõpsates nuppu Lisa.

[![Lisa](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Valige eelarvehierarhia puhul finantsosakond. 

[![Finantsid](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kui olete lõpetanud, klõpsake nuppu Avalda ja Sule. Valige hierarhia avaldamise jõustumiskuupäevana 1/1/2015.

[![Jõustumiskuupäev](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>2. ülesanne: kasutaja turvalisuse konfigureerimine
Eelarve plaanimine kasutab eelarveplaanide andmetele juurdepääsu konfigureerimiseks erilisi turbepoliitikaid. Julial peab olema juurdepääs Finantside eelarveplaanidele. 

2.1. Aktiveerige DEMF-i juriidilise isiku kontekst. 


2.2. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Määrake vahekaardil Parameetrid väärtus Turvamudel valikule Põhineb turvaorganisatsioonidel 

[![Parameetrid](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Navigeerige jaotisse Süsteemihaldus &gt; Kasutajad &gt; Kasutajad. Andke kasutajale Administraator (Julia Funderburk) eelarve halduri roll. 

[![Eelarvehaldur](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Valige kasutaja roll ja klõpsake valikut Määra organisatsioonid 

[![Määra org.](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Valige suvand Anna juurdepääs konkreetsetele organisatsioonidele. Valige esimeses etapis loodud organisatsiooni hierarhia. Valige sõlm Finantsid ja klõpsake nuppu Juurdepääs tütardega 

***Tähtis!*** *Veenduge, et oleksite selle ülesande tegemisel DEMF-i juriidilise isiku kontekstis, kuna organisatsiooni turvet rakendatakse juriidilise isiku kohta* 

### <a name="task-3-create-scenarios"></a>3. ülesanne: stsenaariumide loomine
3.1. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Märkige lehel Stsenaariumid need stsenaariumid, mida hakata kasutama selles ülesandes edaspidi: Eelmine aasta tegelikud summad ja Eelarves plaanitud. 

*Märkus. Soovi korral saate selle harjutuse puhul luua uued stsenaariumid ja kasutada hoopis neid.* 

[![Uued stsenaariumid](./media/screenshot15.png)](./media/screenshot15.png) 

*Märkus. Kuna Julia ei kasuta eelarve ettevalmistamiseks ametlikku heakskiitmisprotsessi, jäetakse selles ülesandes vahele suvandite Töövood, Etapid ja Töövooetapid seadistus ja kasutatakse töövoo Automaatne heakskiitmine olemasolevat seadistust. Vt selle töövoo konfiguratsiooni lisa.*

### <a name="task-4-create-budget-plan-columns"></a>4. ülesanne: eelarveplaani veergude loomine
Eelarveplaani veerud on kas valuuta- või kogusepõhised veerud, mida saab kasutada eelarveplaani dokumendipaigutuses. Käesolevas näites tuleb luua veerg eelmise aasta tegelike summade puhul ja 12 veergu, mis tähistavad eelarveaasta iga kuud. Veerge saab luua kas lihtsalt nuppu Lisa klõpsates ja väärtusi täites või andmeüksuse abil. Selles ülesandes kasutatakse väärtuste sisestamiseks suvandit Andmeüksus. 

4.1. Avage jaotises Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon leht Veerud. Klõpsake vormi üleval paremas nurgas Office’i nuppu ja valige suvand Veerud (filtrimata) 

[![Filtrimata veerud](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Süsteem avab väärtuste sisestamiseks kasutatava Exceli töövihiku. Kui kuvatakse viip, klõpsake nuppe Luba redigeerimine ja Usalda seda rakendust 

[![Luba redigeerimine](./media/screenshot18.png)](./media/screenshot18.png) 

[![Usalda seda rakendust](./media/screenshot17.png)](./media/screenshot17.png)

4.3. Väärtuste sisestamiseks on vaja rohkem veerge. Ruudustikku veergude lisamiseks klõpsake paremal paanil olevat valikut Kujundus: 

[![Kujundus](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Veergude nägemiseks, mis on ruudustikku lisamiseks saadaval, klõpsake valiku Plaani veerud kõrval olevat väikest pliiatsiikooni 

[![Redigeeri](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Topeltklõpsake igat saadaolevat välja nende lisamiseks valitud väljade hulka ja siis klõpsake valikut Värskenda 

![Värskendamine](./media/screenshot21.png)](./media/screenshot21.png) 

4.6. Lisage Exceli tabelisse kõik veerud, mis tuleb lisada. Ridade kiireks lisamiseks kasutage Exceli automaattäitmise funktsiooni AutoFill. Veenduge, et read lisataks tabeli osana (vertikaalsel kerimisel peaksite nägema ruudustiku ülaosas olevaid veerupäiseid) 

[![Automaattäide](./media/screenshot22.png)](./media/screenshot22.png) 

4.7. Värskendage leht ja naaske rakendusse. Avaldatud väärtused kuvatakse. 

[![Värskendamine](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>5. ülesanne: eelarveplaani dokumendipaigutuste ja mallide loomine
Paigutus määratleb, kuidas eelarveplaani dokumendi ridade ruudustik välja näeb, kui kasutaja eelarveplaani dokumendi avab. Eelarveplaani dokumendi paigutust on võimalik vahetada ka samade andmete nägemiseks eri nurkade all. Kohe kui Julia saab meie eelarveplaani dokumendis kasutatavad veerud määratletud, peab ta looma eelarveplaani dokumendipaigutuse, mis sarnaneb Exceli tabelile, mida ta kasutab eelarveandmete loomiseks (vt selle ülesande jaotist Stsenaariumi ülevaade) 

5.1. Avage jaotises Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon leht Paigutused. Looge igakuise eelarvekirje uus paigutus järgmiselt.

-   Valige MA + BU dimensioonikogum põhikontode ja äriüksuste kaasamiseks paigutusse.
-   Loetlege kõik jaotise Elemendid eelmises etapis loodud eelarveplaani veerud. Muutke redigeeritavaks kõik peale eelmise aasta tegelike summade.
-   Klõpsake nuppu Kirjeldused, et valida, millised finantsdimensioonid peaks ruudustikus kirjeldusi kuvama.

[![Kirjeldused](./media/screenshot24.png)](./media/screenshot24.png) 

Eelarveplaani paigutuse määratluse põhjal saame luua Exceli malli, mida kasutada eelarveandmete redigeerimise alternatiivse meetodina. Kuna Exceli mall peab ühtima eelarveplaani paigutuse määratlusega, ei saa te eelarveplaani paigutust muuta pärast Exceli malli loomist, mistõttu tuleks see ülesanne täita pärast kõikide paigutuse komponentide määratlemist. 

5.2. Etapis 5.1 loodud paigutuse puhul klõpsake nuppe Mall &gt; Loo. Kinnitage hoiatusteade. Malli kuvamiseks klõpsake nuppe Mall &gt; Kuva. 

*Märkus. Veenduge, et valiksite käsu Salvesta nimega ja valiksite koha, kuhu mall tuleks redigeerimiseks salvestada. Kui kasutaja valib dialoogis käsu Ava ilma salvestamata, ei säilitata faili sulgemisel sellele tehtud muudatusi.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Valikuline etapp &gt; Muutke Exceli malli, et muuta see kasutajasõbralikumaks – lisage koguvalemeid, päisevälju, vorminguid jne. Salvestage muudatused ja laadige fail eelarveplaani paigutusse, klõpsates suvandeid Paigutus &gt; Laadi üles [![Üleslaadimine](./media/screenshot26.png)](./media/screenshot26.png)

### <a name="task-6-create-a-budget-planning-process"></a>6. ülesanne: eelarve plaanimise protsessi loomine
Julia peab looma ja aktiveerima uue eelarve plaanimise protsessi, mis ühendab kogu ülaltoodud seadistust, et alustada eelarveplaanide sisestamist. Eelarve plaanimise protsess määratleb, milliseid eelarveorganisatsioone, millist töövoogu, paigutusi ja malle eelarveplaanide loomiseks kasutatakse. 

6.1. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise protsess ja looge uus kirje.

-   Eelarve plaanimise protsess – DEMF-i eelarvestamine FY2016
-   Eelarvetsükkel – FY2016
-   Pearaamat – DEMF
-   Vaikimisi konto struktuur – tootmise kasumiaruanne
-   Organisatsiooni hierarhia – valige ülesande alguses loodud hierarhia
-   Eelarve plaanimise töövoog – automaatne määramine – finantsosakonna kinnitamise töövoog
-   Valige eelarve plaanimise etapi reeglites ja mallides iga eelarve plaanimise etapi töövoo puhul, kas ridade lisamine ja ridade muutmine on lubatud ja millist paigutust tuleks kasutada vaikimisi

*Märkus. Saate luua täiendavaid dokumendipaigutusi ja määrata need eelarve plaanimise töövoo etapis saadaolevaks, klõpsates nuppu Alternatiivsed paigutused.* 

[![Alternatiivsed paigutused](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Selle eelarve plaanimise töövoo aktiveerimiseks valige Toimingud &gt; Aktiveeri 

[![Aktiveeri](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>2. harjutus: protsessi simulatsioon

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>7. ülesanne: eelarveplaani algandmete loomine pearaamatust
7.1. Navigeerige jaotisse Eelarvestus &gt; Perioodiline &gt; Eelarveplaani loomine pearaamatust. Täitke perioodilise protsessi parameetrid ja klõpsake nuppu Loo. 

[![Loo](./media/screenshot29.png)](./media/screenshot29.png) 

7.2. Loomisprotsessiga loodud eelarveplaani leidmiseks navigeerige jaotisse Eelarvestus &gt; Eelarveplaanid. 

[![Eelarveplaan](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Avage dokumendi üksikasjad, klõpsates dokumendi numbri hüperlinki. Eelarveplaan kuvatakse selles ülesandes loodud paigutuses määratletu järgi 

[![Eelarveplaani kuva](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>8. ülesanne: jooksva aasta eelarve loomine eelmise aasta tegelike summade alusel
Eraldusmeetodeid saab eelarveplaanis kasutada eelarveplaanide teabe hõlpsaks kopeerimiseks ühest stsenaariumist teise / nende jaotamiseks perioodides / dimensioonidele eraldamiseks. Kasutame eraldamisi jooksva aasta eelarve loomiseks eelmise aasta tegelikest summadest. 

8.1. Valige eelarveplaani dokumendi ruudustikus kõik read ja klõpsake nuppu Eralda eelarve 

[![Kõik read](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Valige eraldusmeetod, perioodi võti, lähte- ja sihtstsenaarium ning klõpsake nuppu Eralda. 

[![Eralda](./media/screenshot33.png)](./media/screenshot33.png)

Eelmise aasta tegelikud summad kopeeritakse praeguse aasta eelarvesse ja eraldatakse need perioodidele, kasutades perioodivõtit Müügikõver. 

[![Müügikõver](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>9. ülesanne: eelarveplaani dokumendi korrigeerimine Exceliga ja dokumendi lõpetamine
9.1. Dokumendi sisu avamiseks Excelis klõpsake nuppu Tööleht

[![Excel](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Exceli töövihiku avamisel korrigeerige eelarveplaani dokumendi arve ja klõpsake nuppu Avalda.

[![Avaldamine](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Eelarveplaani dokumentidesse naasmine Klõpsake dokumendi automaatseks heakskiitmiseks valikuid Töövoog &gt; Esita.

[![Automaatne heakskiitmine](./media/screenshot37.png)](./media/screenshot37.png) 

Kui töövoog on lõpule jõudnud, muutub eelarveplaani dokumendi etapiks Heaks kiidetud. [![Heaks kiidetud](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Lisa

### <a name="auto-approve-workflow-configuration"></a>Automaatse kinnitamise töövoo konfiguratsioon

A. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve töövood ja looge uus töövoog, kasutades malli Eelarve plaanimise töövood:

[![Uue töövoo loomine](./media/screenshot39.png)](./media/screenshot39.png)

See töövoog sisaldab ainult üht ülesannet: eelarveplaani etapi üleminek 

[![Eelarveplaani etapi üleminek](./media/screenshot40.png)](./media/screenshot40.png) 

Salvestage ja aktiveerige töövoog. 

B. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Looge vahekaardil Etapid kaks etappi: Algne ja Esitatud 

[![Algne ja Esitatud](./media/screenshot41.png)](./media/screenshot41.png)

C. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Seostage vahekaardil Töövooetapid etapis A loodud töövoog Automaatne heakskiitmine etappidega Algne ja Esitatud 

[![Eelarvestamine ja eelarve plaanimine](./media/screenshot42.png)](./media/screenshot42.png)  



