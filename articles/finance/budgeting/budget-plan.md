---
title: Eelarve plaanimine
description: Selle ülesande eesmärk on anda juhendatud ülevaade Microsoft Dynamics 365 Finance'i funktsioonivärskendustest eelarve plaanimise alal. Selle ülesande eesmärk on illustreerida kiiret eelarve plaanimise mooduli konfigureerimise näidet ja näidata, kuidas selle konfiguratsiooni abil on võimalik eelarvet plaanida.
author: ShylaThompson
ms.date: 06/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f6223cce4a960d3fa3db1f3a17b324201085ea04
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822223"
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
Kuna kogu eelarveprotsess toimub finantsosakonnas, peab Julia seega looma väga lihtsa organisatsiooni hierarhia – mis koosneb ainult finantsosakonnast. 

1.1. Navigeerige organisatsioonihierarhiasse (Organisatsioonihaldus &gt; Organisatsioon &gt; Organisatsioonihierarhiad) ja klõpsake nuppu Uus.

![Organisatsiooni hierarhiad](./media/screenshot3.png) 

1.2. Tippige nime väljale organisatsioonihierarhia nimi ja klõpsake valikut Määra eesmärk.

1.3. Valige eelarve planeerimise eesmärk, klõpsake nuppu Lisa ja määrake vastloodud organisatsioonihierarhia. 

[![Eesmärgi määramine](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Korrake ülaltoodud etappi turbekorralduse eesmärgil. Lõpetamisel sulgege vorm.

1.5. Klõpsake Organisatsioonihierarhia vormil valikut Vaata. Klõpsake Hierarhiakujundajas valikut Redigeeri ja looge hierarhia, klõpsates valikut Sisesta.

[![Lisa](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Valige eelarvehierarhia puhul finantsosakond. 

[![Finantsid](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kui olete lõpetanud, klõpsake valikuid Avalda ja Sule. Valige hierarhia avaldamise kuupäevaks 1.01.2015.

[![Kehtivuse algus](./media/screenshot9.png)](./media/screenshot9.png)

### <a name="task-2-configure-user-security"></a>2. ülesanne: kasutaja turvalisuse konfigureerimine
Eelarve plaanimine kasutab eelarveplaanide andmetele juurdepääsu konfigureerimiseks erilisi turbepoliitikaid. Julial peab olema juurdepääs Finantside eelarveplaanidele. 

2.1. Aktiveerige DEMF-i juriidilise isiku kontekst. 


2.2. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Seadke vahekaardil Parameetrid turbemudeli väärtuseks Põhineb turbeorganisatsioonidel. 

[![Parameetrid](./media/screenshot11.png)](./media/screenshot11.png) 

2.3. Navigeerige jaotisse Süsteemihaldus &gt; Kasutajad &gt; Kasutajad. Andke kasutajale Administraator (Julia Funderburk) eelarve halduri roll. 

[![Eelarvehaldur](./media/screenshot12.png)](./media/screenshot12.png) 

2.4. Valige kasutajaroll ja klõpsake valikut Määra organisatsioonid. 

[![Organisatsioonide määramine](./media/screenshot13.png)](./media/screenshot13.png)

2.5. Valige suvand Anna juurdepääs konkreetsetele organisatsioonidele. Valige esimeses etapis loodud organisatsioonihierarhia. Valige rahandussõlm ja klõpsake nuppu Juurdepääs tütardega. 

***Tähtis!** _ _Veenduge, et oleksite selle ülesande tegemisel DEMF-i juriidilise isiku kontekstis, kuna organisatsiooni turvet rakendatakse juriidilise isiku kohta* 

### <a name="task-3-create-scenarios"></a>3. ülesanne: stsenaariumide loomine
3.1. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Märkige lehel Stsenaariumid need stsenaariumid, mida hakata kasutama selles ülesandes edaspidi: Eelmine aasta tegelikud summad ja Eelarves plaanitud. 

*Märkus. Soovi korral saate selle harjutuse puhul luua uued stsenaariumid ja kasutada hoopis neid.* 

[![Uued stsenaariumid](./media/screenshot15.png)](./media/screenshot15.png) 

*Märkus. Kuna Julia ei kasuta eelarve ettevalmistamiseks ametlikku heakskiitmisprotsessi, jäetakse selles ülesandes vahele suvandite Töövood, Etapid ja Töövooetapid seadistus ja kasutatakse töövoo Automaatne heakskiitmine olemasolevat seadistust. Vt selle töövoo konfiguratsiooni lisa.*

### <a name="task-4-create-budget-plan-columns"></a>4. ülesanne: eelarveplaani veergude loomine
Eelarveplaani veerud on kas valuuta- või kogusepõhised veerud, mida saab kasutada eelarveplaani dokumendipaigutuses. Käesolevas näites tuleb luua veerg eelmise aasta tegelike summade puhul ja 12 veergu, mis tähistavad eelarveaasta iga kuud. Veerge saab luua kas lihtsalt nuppu Lisa klõpsates ja väärtusi täites või andmeüksuse abil. Selles ülesandes kasutatakse väärtuste sisestamiseks suvandit Andmeüksus. 

4.1. Avage jaotises Eelarve &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon leht Veerud. Klõpsake vormi paremas ülanurgas nuppu Office ja valige Veerud (filtreerimata). 

[![Filtrimata veerud](./media/screenshot16.png)](./media/screenshot16.png) 

4.2. Süsteem avab väärtuste täitmiseks Exceli töövihiku. Viiba kuvamisel klõpsake valikuid Luba redigeerimine ja Usalda rakendust. 

4.3. Väärtuste sisestamiseks on vaja rohkem veerge. Klõpsake paremal paanil valikut Kujundus, et lisada ruudustikku veerge. 

[![Kujundus](./media/screenshot19.png)](./media/screenshot19.png) 

4.4. Klõpsake valiku PlanColumns kõrval olevat pliiatsinuppu, et näha saadaolevaid veerge, mida ruudustikku lisada. 

[![Redigeeri](./media/screenshot20.png)](./media/screenshot20.png) 

4.5. Topeltklõpsake iga saadaolevat välja, et lisada need väljale Valitud, ja klõpsake nuppu Värskenda. 

4.6. Lisage Exceli tabelis kõik veerud, mis on vaja luua. Kasutage ridade kiireks lisamiseks Exceli automaattäite funktsiooni. Veenduge, et read oleks lisatud tabeli osana (vertikaalse kerimise kasutamisel peaksite nägema ruudu ülaosas veerupäiseid). 

4.7. Naaske rakendusse ja värskendage lehte. Avaldatud väärtused kuvatakse. 

[![Värskendamine](./media/screenshot23.png)](./media/screenshot23.png)

### <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>5. ülesanne: eelarveplaani dokumendipaigutuste ja mallide loomine
Paigutus määratleb, kuidas eelarveplaani dokumendi ridade ruudustik välja näeb, kui kasutaja eelarveplaani dokumendi avab. Eelarveplaani dokumendi paigutust on võimalik vahetada ka samade andmete nägemiseks eri nurkade all. Kohe kui Julia saab meie eelarveplaani dokumendis kasutatavad veerud määratletud, peab ta looma eelarveplaani dokumendipaigutuse, mis sarnaneb Exceli tabelile, mida ta kasutab eelarveandmete loomiseks (vt selle ülesande jaotist Stsenaariumi ülevaade) 

5.1. Avage jaotises Eelarve &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon leht Paigutused. Looge igakuise eelarvekirje uus paigutus järgmiselt.

-   Valige MA + BU dimensioonikogum põhikontode ja äriüksuste kaasamiseks paigutusse.
-   Loetlege kõik jaotise Elemendid eelmises etapis loodud eelarveplaani veerud. Muutke redigeeritavaks kõik peale eelmise aasta tegelike summade.
-   Klõpsake nuppu Kirjeldused, et valida, millised finantsdimensioonid peaks ruudustikus kirjeldusi kuvama.

[![Kirjeldused](./media/screenshot24.png)](./media/screenshot24.png) 

Eelarveplaani paigutuse määratluse põhjal saame luua Exceli malli, mida kasutada eelarveandmete redigeerimise alternatiivse meetodina. Kuna Exceli mall peab ühtima eelarveplaani paigutuse määratlusega, ei saa te eelarveplaani paigutust muuta pärast Exceli malli loomist, mistõttu tuleks see ülesanne täita pärast kõikide paigutuse komponentide määratlemist. 

5.2. Etapis 5.1 loodud paigutuse puhul klõpsake nuppe Mall &gt; Loo. Kinnitage hoiatusteade. Malli kuvamiseks klõpsake nuppe Mall &gt; Kuva. 

*Märkus. Veenduge, et valiksite käsu Salvesta nimega ja valiksite koha, kuhu mall tuleks redigeerimiseks salvestada. Kui kasutaja valib dialoogis käsu Ava ilma salvestamata, ei säilitata faili sulgemisel sellele tehtud muudatusi.* 
[![Template view](./media/screenshot25.png)](./media/screenshot25.png) 

5.3. &lt; Valikuline etapp&gt; Muutke Exceli malli, et see näeks välja kasutajasõbralikum – lisage kogu valemid, päiseväljad, vorming jne. Salvestage muudatused ja laadige fail eelarveplaani paigutusse üles, klõpsates valikuid Paigutus &gt; Laadi üles. 


### <a name="task-6-create-a-budget-planning-process"></a>6. ülesanne: eelarve plaanimise protsessi loomine
Julia peab looma ja aktiveerima uue eelarve plaanimise protsessi, mis ühendab kogu ülaltoodud seadistust, et alustada eelarveplaanide sisestamist. Eelarve plaanimise protsess määratleb, milliseid eelarveorganisatsioone, millist töövoogu, paigutusi ja malle eelarveplaanide loomiseks kasutatakse. 

6.1. Navigeerige jaotisse Eelarve &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise protsess ja looge uus kirje.

-   Eelarve plaanimise protsess – DEMF-i eelarvestamine FY2016
-   Eelarvetsükkel – FY2016
-   Pearaamat – DEMF
-   Vaikimisi konto struktuur – tootmise kasumiaruanne
-   Organisatsiooni hierarhia – valige ülesande alguses loodud hierarhia
-   Eelarve plaanimise töövoog – automaatne määramine – finantsosakonna kinnitamise töövoog
-   Valige eelarve plaanimise etapi reeglites ja mallides iga eelarve plaanimise etapi töövoo puhul, kas ridade lisamine ja ridade muutmine on lubatud ja millist paigutust tuleks kasutada vaikimisi

*Märkus. Saate luua täiendavaid dokumendipaigutusi ja määrata need eelarve plaanimise töövoo etapis saadaolevaks, klõpsates nuppu Alternatiivsed paigutused.* 

[![Alternatiivsed paigutused](./media/screenshot27.png)](./media/screenshot27.png) 

6.2. Valige selle eelarve plaanimise töövoo aktiveerimiseks Toimingud &gt; Aktiveeri. 

[![Aktiveeri](./media/screenshot28.png)](./media/screenshot28.png)

## <a name="exercise-2-process-simulation"></a>2. harjutus: protsessi simulatsioon

### <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>7. ülesanne: eelarveplaani algandmete loomine pearaamatust
7.1. Navigeerige jaotisse Eelarvestus &gt; Perioodiline &gt; Eelarveplaani loomine pearaamatust. Täitke perioodilised protsessiparameetrid ja klõpsake nuppu Genereeri. 

7.2. Navigeerige jaotisse Eelarve &gt; Eelarve plaanimine, et leida genereerimisprotsessi loodud eelarveplaan. 

[![Eelarveplaan](./media/screenshot30.png)](./media/screenshot30.png) 

7.3. Avage dokumendi üksikasjad, klõpsates dokumendi numbri hüperlinki. Eelarveplaani kuvatakse vastavalt selle labori ajal loodud paigutusele. 

[![Eelarveplaani kuva](./media/screenshot31.png)](./media/screenshot31.png)

### <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>8. ülesanne: jooksva aasta eelarve loomine eelmise aasta tegelike summade alusel
Eraldusmeetodeid saab eelarveplaanis kasutada eelarveplaanide teabe hõlpsaks kopeerimiseks ühest stsenaariumist teise / nende jaotamiseks perioodides / dimensioonidele eraldamiseks. Kasutame eraldamisi jooksva aasta eelarve loomiseks eelmise aasta tegelikest summadest. 

8.1. Valige kõik eelarveplaani dokumentide ruudustiku read ja klõpsake nuppu Eelarve eraldamine. 

[![Kõik read](./media/screenshot32.png)](./media/screenshot32.png) 

8.2. Valige eraldamisviis, perioodiklahv, allika ja sihtkoha stsenaariumid ning klõpsake nuppu Eralda. 

[![Eralda](./media/screenshot33.png)](./media/screenshot33.png)

Eelmise aasta tegelikud summad kopeeritakse jooksva aasta eelarvesse ja need eraldatakse perioodide kaupa, kasutades müügi kõvera perioodi klahvi. 

[![Müügikõver](./media/screenshot34.png)](./media/screenshot34.png)

### <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>9. ülesanne: eelarveplaani dokumendi korrigeerimine Exceliga ja dokumendi lõpetamine
9.1. Klõpsake Excelis dokumendi sisu avamiseks nuppu Tööleht.

9.2. Kui Exceli töövihik avaneb, korrigeerige eelarveplaani dokumendis olevaid numbreid ja klõpsake nuppu Avalda.

9.3. Eelarveplaani dokumentidesse naasmine Klõpsake dokumendi automaatselt kinnitamiseks valikuid Töövoog &gt; Esita.

[![Automaatne heakskiitmine](./media/screenshot37.png)](./media/screenshot37.png) 

Kui töövoog lõpule jõuab, muutub eelarveplaani dokumendi etapp väärtusele Kinnitatud. [![Kinnitatud](./media/screenshot38.png)](./media/screenshot38.png)

## <a name="appendix"></a>Lisa

### <a name="auto-approve-workflow-configuration"></a>Automaatse kinnitamise töövoo konfiguratsioon

A. Eelarve &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve töövood. Looge eelarve plaanimise töövoogude abil uus töövoog.

[![Uue töövoo loomine](./media/screenshot39.png)](./media/screenshot39.png)

See töövoog sisaldab ainult ühte ülesannet – etapi ülemineku eelarveplaan. 

[![Etapi ülemineku eelarveplaan](./media/screenshot40.png)](./media/screenshot40.png) 

Salvestage ja aktiveerige töövoog. 

B. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Looge vahekaardil Etapid 2 etappi – Algne ja Esitatud. 

[![Algne ja Esitatud](./media/screenshot41.png)](./media/screenshot41.png)

C. Navigeerige jaotisse Eelarvestus &gt; Seadistus &gt; Eelarve plaanimine &gt; Eelarve plaanimise konfiguratsioon. Seostage vahekaardil Töövoo etapid etapis A loodud töövoog Automaatne kinnitamine etappidega Algne ja Esitatud.

[![Eelarvestamine ja eelarve plaanimine](./media/screenshot42.png)](./media/screenshot42.png)  





[!INCLUDE[footer-include](../../includes/footer-banner.md)]