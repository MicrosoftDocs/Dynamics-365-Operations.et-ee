---
title: Eelarve plaanimine
description: "See lab eesmärk on anda giidiga ülevaade Microsoft Dynamics 365 toimingute funktsioonide värskendusi eelarve planeerimise valdkonnas. Selle ülesande eesmärk on illustreerida kiiret eelarve plaanimise mooduli konfigureerimise näidet ja näidata, kuidas selle konfiguratsiooni abil on võimalik eelarvet plaanida.  See lab keskendub konkreetselt järgmiste äriprotsesse või ülesannete--luua organisatsiooni hierarhia eelarve planeerimine ja seadistamine kasutaja turvalisus - eelarve kava stsenaariumid, eelarve kava veerud, skeemid ja Exceli Mallid - loomise ja eelarve planeerimise protsessi - loomise kava eelarvedokumendi poolt tegelikud pearaamatukandeid tõmmates - kasutab eraldised eelarve kava dokumendi andmete täpsustamiseks - toimetamine eelarve kava dokumendi andmete Exceli aktiveerimine"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>Eelarve plaanimine

See lab eesmärk on anda giidiga ülevaade Microsoft Dynamics 365 toimingute funktsioonide värskendusi eelarve planeerimise valdkonnas. Selle ülesande eesmärk on illustreerida kiiret eelarve plaanimise mooduli konfigureerimise näidet ja näidata, kuidas selle konfiguratsiooni abil on võimalik eelarvet plaanida.  See lab keskendub konkreetselt järgmiste äriprotsesse või ülesannete--luua organisatsiooni hierarhia eelarve planeerimine ja seadistamine kasutaja turvalisus - eelarve kava stsenaariumid, eelarve kava veerud, skeemid ja Exceli Mallid - loomise ja eelarve planeerimise protsessi - loomise kava eelarvedokumendi poolt tegelikud pearaamatukandeid tõmmates - kasutab eraldised eelarve kava dokumendi andmete täpsustamiseks - toimetamine eelarve kava dokumendi andmete Exceli aktiveerimine 

<a name="prerequisites"></a>Eeltingimused 
------------------

Õpetamisel, peate juurdepääsu Dynamics 365 tegevuse keskkond Contoso demo andmetega ja administraatorina eksemplaris ette valmistada. Kasuta In eraldi brauseri režiimi lab - vajadusel brauseri korral mistahes kontolt väljalogimine ja Logi sisse Dynamics 365 toimingute administraatori mandaati. Sisenedes Dynamics 365 korral te **peab** ruut "Logi sisse". See loob püsiva küpsise, mida Exceli rakendus praegu vajab. Kui logite Dynamics 365 toiminguteks kasutada peale IE brauserit, siis palutakse logida rakenduses Excel. Exceli rakenduses suvandi Sisselogimine klõpsamine avab IE hüpikakna ja sisselogimisel **PEATE** märkima ruudu Hoia mind sisselogituna. Kui Exceli rakenduses suvandi Sisselogimine klõpsamine midagi ei tee, peaksite IE küpsiste vahemälu tühjendama.

## <a name="scenario-overview"></a>**Scenario overview**
Julia töötab Saksamaa ettevõttes Contoso Entertainment Systems (DEMF) finantshaldurina. FY2016 lähenemisel peab ta töötama eelseisva aasta ettevõtte eelarve seadistamise osas. Eelarve koostamine näeb välja järgmine.

1.  Julia kasutab eelarve loomise lähtepunktina eelmise aasta tegelikke summasid.
2.  Eelmise aasta tegelike summade põhjal loob ta eelseisva aasta 12 kuu hinnangud.
3.  Julia vaatab eelarve CFO-ga üle. Kui see on tehtud, teeb ta eelarveplaani vajalikke korrigeerimisi ja lõpetab eelarve koostamise.

Eelarve planeerimine konfiguratsioon skeemi stsenaariumi näeb välja järgmine:

![Screenshot1](./media/screenshot1-300x152.png)

Julia kasutab Exceli mall koostab eelarve:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>1. harjutus: konfiguratsioon
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**Ülesanne 1: Luua organisatsiooni hierarhia**
Kuna kogu eelarveprotsess toimub finantsosakonnas, peab Julia seega looma väga lihtsa organisatsiooni hierarhia – mis koosneb ainult finantsosakonnast. 1.1. Liikuge organisatsiooni hierarhia (organisatsiooni haldamine &gt;organisatsioonide &gt;organisatsiooni hierarhia) ja klõpsake nuppu Uus

![Screenshot3](./media/screenshot3.png) 

1.2. Organisatsiooni hierarhia nimi ja klõpsake nuppu Määra eesmärk

[![Screenshot4](./media/screenshot4.png)](./media/screenshot4.png) 

1.3. Valige eelarve planeerimise eesmärk, klõpsake nuppu Lisa ning määravad vastloodud organisatsiooni hierarhiale: 

[![Screenshot5](./media/screenshot5.png)](./media/screenshot5.png)

1.4. Korrake ülaltoodud etappi organisatsiooni turvalisuse eesmärgi puhul. Lõpetamisel sulgege vorm.

[![Screenshot6](./media/screenshot6.png)](./media/screenshot6.png)

1.5. Klõpsake vormil Organisatsiooni hierarhia nuppu Kuva. Klõpsake hierarhia kujundajas nuppu Redigeeri ja looge hierarhia, klõpsates nuppu Lisa.

[![Screenshot7](./media/screenshot7.png)](./media/screenshot7.png) 

1.6. Valige eelarvehierarhia puhul finantsosakond. 

[![Screenshot8](./media/screenshot8.png)](./media/screenshot8.png)

1.7. Kui olete lõpetanud, klõpsake nuppu Avalda ja Sule. Valige hierarhia avaldamise jõustumiskuupäevana 1/1/2015.

[![Screenshot9](./media/screenshot9.png)](./media/screenshot9.png)

## <a name="task-2-configure-user-security"></a>2. ülesanne: kasutaja turvalisuse konfigureerimine
Eelarve plaanimine kasutab eelarveplaanide andmetele juurdepääsu konfigureerimiseks erilisi turbepoliitikaid. Julial peab olema juurdepääs Finantside eelarveplaanidele. 2.1. Aktiveerige DEMF juriidilise konteksti: [![Screenshot10](./media/screenshot10.png)](./media/screenshot10.png) 2.2. Liikuge eelarve koostamise &gt;Setup &gt;eelarve planeerimise &gt;eelarve planeerimise konfiguratsiooni. Parameetrid vahekaardil valitud turvalisuse mudel väärtuse põhjal organisatsioonide sees [![Screenshot11](./media/screenshot11.png)](./media/screenshot11.png) 2.3. Liikuge süsteemihaldus &gt;kasutajate &gt;kasutajatele. Andke kasutajale Administraator (Julia Funderburk) eelarve halduri roll. [![Screenshot12](./media/screenshot12.png)](./media/screenshot12.png) 2.4. Valige kasutaja rolli ja klõpsake nuppu Määra organisatsioonide [![Screenshot13](./media/screenshot13.png)](./media/screenshot13.png)2.5. Valige suvand Anna juurdepääs konkreetsetele organisatsioonidele. Valige esimeses etapis loodud organisatsiooni hierarhia. Vali Finance sõlme ja kliki toetus laste nuppu ***NB!*** *– Teha kindel, et DEMF juriidiline isik kontekstis selle ülesande täitmisel organisatsiooni turvalisuse eest juriidiline isik mõistetakse*[![Screenshot14](./media/screenshot14.png)](./media/screenshot14.png)

## <a name="task-3-create-scenarios"></a>3. ülesanne: stsenaariumide loomine
3.1. Liikuge eelarve koostamise&gt;Setup &gt;eelarve planeerimise &gt;eelarve planeerimise konfiguratsiooni. Märkige lehel Stsenaariumid need stsenaariumid, mida hakata kasutama selles ülesandes edaspidi: Eelmine aasta tegelikud summad ja Eelarves plaanitud. *Märkus. Soovi korral saate selle harjutuse puhul luua uued stsenaariumid ja kasutada hoopis neid.* [![Screenshot15](./media/screenshot15.png)](./media/screenshot15.png)*Märkus: Julia kasutab ametliku kinnitamise protsessi eelarve koostamiseks, siis Jätka töövood, etapid ja töövoo etapi setup see lab ja kasutab olemasolevat seadistust Auto – kinnitab töövoo. Vt. selle töövoo konfiguratsiooni puhul.*

## <a name="task-4-create-budget-plan-columns"></a>4. ülesanne: eelarveplaani veergude loomine
Eelarveplaani veerud on kas valuuta- või kogusepõhised veerud, mida saab kasutada eelarveplaani dokumendipaigutuses. Käesolevas näites tuleb luua veerg eelmise aasta tegelike summade puhul ja 12 veergu, mis tähistavad eelarveaasta iga kuud. Veerge saab luua kas lihtsalt nuppu Lisa klõpsates ja väärtusi täites või andmeüksuse abil. Selles ülesandes kasutatakse väärtuste sisestamiseks suvandit Andmeüksus. 4.1. Aastal eelarve koostamise&gt;Setup &gt;eelarve planeerimise &gt;eelarve planeerimise avatud veergude konfigureerimislehe. Klõpsake Office'i nuppu vormi paremas ülanurgas ja valige veerud (filtreerimata) [![Screenshot16](./media/screenshot16.png)](./media/screenshot16.png) 4.2. Süsteem avab väärtuste sisestamiseks kasutatava Exceli töövihiku. Küsimisel nuppu Luba redigeerimine ja usaldate seda app [![Screenshot18](./media/screenshot18.png)](./media/screenshot18.png)[![Screenshot17](./media/screenshot17.png)](./media/screenshot17.png) 4.3. Me vajame rohkem veerge täita väärtused. Klõpsake parempoolsel paanil lisada veerud koordinaatvõrk disain: [![Screenshot19](./media/screenshot19.png)](./media/screenshot19.png) 4.4. Klõpsake väike pliiats nuppu kõrval näha saadaolevate veergude lisamiseks grid PlanColumns [![Screenshot20](./media/screenshot20.png)](./media/screenshot20.png) 4.5. Topeltklõpsake iga saadaval välja lisamiseks valitud väljad ja klõpsake nuppu Värskenda [![Screenshot21](./media/screenshot21.png)](./media/screenshot21.png) 4.6. Lisage Exceli tabelisse kõik veerud, mis tuleb lisada. Ridade kiireks lisamiseks kasutage Exceli automaattäitmise funktsiooni AutoFill. Veenduge, et tabeli osa lisatakse read (vertikaalne kerimisriba kasutamisel te tuleks vaadata veerupäised peal grid) [![Screenshot22](./media/screenshot22.png)](./media/screenshot22.png) 4.7. Tagasi Dynamics 365 operatsioonide ja värskendage lehte. Publitseeritud väärtuste kuvatakse Dynamics 365 toiminguteks. [![Screenshot23](./media/screenshot23.png)](./media/screenshot23.png)

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>5. ülesanne: eelarveplaani dokumendipaigutuste ja mallide loomine
Paigutus määratleb, kuidas eelarveplaani dokumendi ridade ruudustik välja näeb, kui kasutaja eelarveplaani dokumendi avab. Eelarveplaani dokumendi paigutust on võimalik vahetada ka samade andmete nägemiseks eri nurkade all. Kohe kui Julia saab meie eelarveplaani dokumendis kasutatavad veerud määratletud, peab ta looma eelarveplaani dokumendipaigutuse, mis sarnaneb Exceli tabelile, mida ta kasutab eelarveandmete loomiseks (vt selle ülesande jaotist Stsenaariumi ülevaade) 5.1. Aastal eelarve koostamise&gt;Setup &gt;eelarve planeerimise &gt;eelarve planeerimise avatud paigutusega konfigureerimislehe. Looge igakuise eelarvekirje uus paigutus järgmiselt.

-   Valige MA + BU dimensioonikogum põhikontode ja äriüksuste kaasamiseks paigutusse.
-   Loetlege kõik jaotise Elemendid eelmises etapis loodud eelarveplaani veerud. Muutke redigeeritavaks kõik peale eelmise aasta tegelike summade.
-   Klõpsake nuppu Kirjeldused, et valida, millised finantsdimensioonid peaks ruudustikus kirjeldusi kuvama.

[![Screenshot24](./media/screenshot24.png)](./media/screenshot24.png) põhinev eelarve kava paigutuse määratlus saame luua Exceli malli kasutatakse alternatiivsel viisil eelarve andmete muutmiseks. Kuna Exceli mall peab ühtima eelarveplaani paigutuse määratlusega, ei saa te eelarveplaani paigutust muuta pärast Exceli malli loomist, mistõttu tuleks see ülesanne täita pärast kõikide paigutuse komponentide määratlemist. 5.2. Loodud skeem on 5.1. Samm, klõpsake nuppu Mall &gt;Loo. Kinnitage hoiatusteade. Malli, klõpsake malli &gt;vaade. *Märkus: Ärge unustage valige "Save as" ja valige koht, kus Mall tuleb hoida selleks, et seda redigeerida. Kui kasutaja valib "Avatud" dialoogis salvestamata, säilitatakse muudatusi teha faili faili sulgemisel.* [![Screenshot25](./media/screenshot25.png)](./media/screenshot25.png) 5.3. &lt;Valikuline samm&gt; muuta Exceli mall teha see välja rohkem kasutaja sõbralik – lisada kokku valemeid, päiseväljad, vormindamise jne. Muudatused salvestada ja laadida faili eelarve kava paigutus nuppu paigutus &gt;laadida [![Screenshot26](./media/screenshot26.png)](./media/screenshot26.png)

## <a name="task-6-create-a-budget-planning-process"></a>6. ülesanne: eelarve plaanimise protsessi loomine
Julia peab looma ja aktiveerima uue eelarve plaanimise protsessi, mis ühendab kogu ülaltoodud seadistust, et alustada eelarveplaanide sisestamist. Eelarve plaanimise protsess määratleb, milliseid eelarveorganisatsioone, millist töövoogu, paigutusi ja malle eelarveplaanide loomiseks kasutatakse. 6.1. Liikuge eelarve koostamise &gt;Setup &gt;eelarve planeerimise &gt;eelarve planeerimise protsessi ja uue kirje loomine.

-   Eelarve plaanimise protsess – DEMF-i eelarvestamine FY2016
-   Eelarvetsükkel – FY2016
-   Pearaamat – DEMF
-   Vaikimisi konto struktuur – tootmise kasumiaruanne
-   Organisatsiooni hierarhia – valige ülesande alguses loodud hierarhia
-   Eelarve plaanimise töövoog – automaatne määramine – finantsosakonna kinnitamise töövoog
-   Valige eelarve plaanimise etapi reeglites ja mallides iga eelarve plaanimise etapi töövoo puhul, kas ridade lisamine ja ridade muutmine on lubatud ja millist paigutust tuleks kasutada vaikimisi

*Märkus. Saate luua täiendavaid dokumendipaigutusi ja määrata need eelarve plaanimise töövoo etapis saadaolevaks, klõpsates nuppu Alternatiivsed paigutused.* [![Screenshot27](./media/screenshot27.png)](./media/screenshot27.png) 6.2. Valige toimingud &gt;Aktiveeri, et aktiveerida see eelarve planeerimise töövoo [![Screenshot28](./media/screenshot28.png)](./media/screenshot28.png)

<a name="exercise-2-process-simulation"></a>2. harjutus: protsessi simulatsioon
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>7. ülesanne: eelarveplaani algandmete loomine pearaamatust
7.1. Liikuge eelarve koostamise &gt;perioodiline &gt;Loo eelarveplaan pearaamatukandeid. Täitke perioodilise protsessi parameetrid ja klõpsake nuppu Loo. [![Screenshot29](./media/screenshot29.png)](./media/screenshot29.png) 7.2. Liikuge eelarve koostamise &gt;eelarvekavad leida Loo käigus loodud eelarve plaan. [![Screenshot30](./media/screenshot30.png)](./media/screenshot30.png) 7,3. Avage dokumendi üksikasjad, klõpsates dokumendi numbri hüperlinki. Eelarve kava kuvatakse määratletud ajal see lab paigutus [![Screenshot31](./media/screenshot31.png)](./media/screenshot31.png)

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>8. ülesanne: jooksva aasta eelarve loomine eelmise aasta tegelike summade alusel
Eraldusmeetodeid saab eelarveplaanis kasutada eelarveplaanide teabe hõlpsaks kopeerimiseks ühest stsenaariumist teise / nende jaotamiseks perioodides / dimensioonidele eraldamiseks. Kasutame eraldamisi jooksva aasta eelarve loomiseks eelmise aasta tegelikest summadest. 8.1. Vali kõik read eelarve kava dokumendi koordinaatvõrku ja klõpsake nuppu Eralda eelarve [![Screenshot32](./media/screenshot32.png)](./media/screenshot32.png) 8.2. Valige jaotusmeetod, perioodi võti, lähte- ja stsenaariume ja klõpsake nuppu Eralda 

[![Screenshot33](./media/screenshot33.png)](./media/screenshot33.png)

Eelmise aasta tegelikud summad kopeeritakse jooksva aasta eelarve ja jaotada kogu müügi kõver perioodi võti kasutades. 

[![Screenshot34](./media/screenshot34.png)](./media/screenshot34.png)

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>9. ülesanne: eelarveplaani dokumendi korrigeerimine Exceliga ja dokumendi lõpetamine
9.1. Klõpsake nuppu töölehe Exceli dokumendi sisu avamiseks

[![Screenshot35](./media/screenshot35.png)](./media/screenshot35.png)

9.2. Exceli töövihiku avamisel korrigeerige eelarveplaani dokumendi arve ja klõpsake nuppu Avalda.

[![Screenshot36](./media/screenshot36.png)](./media/screenshot36.png)

9.3. Tagasi kava eelarvedokumendi Dynamics 365 toiminguteks. Klõpsake töövoo &gt;Auto kinnitamiseks esitada dokumendi

[![Screenshot37](./media/screenshot37.png)](./media/screenshot37.png) 

Kui töövoog on lõpule jõudnud, eelarve kava dokumendi etapi olekuks kinnitatud. [![Screenshot38](./media/screenshot38.png)](./media/screenshot38.png)

<a name="appendix"></a>Lisa
========

### <a name="auto-approve-workflow-configuration"></a>Automaatse kinnitamise töövoo konfiguratsioon

A. Eelarve koostamine &gt;Setup &gt;eelarve planeerimise &gt;eelarve koostamise töövooge luua uue töövoo malli eelarve planeerimise töövoogude kasutamise:

[![Screenshot39](./media/screenshot39.png)](./media/screenshot39.png)

See töövoog sisaldab ainult üks ülesanne-etappi ülemineku eelarveplaan 

[![Screenshot40](./media/screenshot40.png)](./media/screenshot40.png) 

Salvesta ja Aktiveeri töövoo. 

B. Liikuge eelarve koostamise &gt;Setup &gt;eelarve planeerimise &gt;eelarve planeerimise konfiguratsiooni. Etapis vahekaarti Loo 2 etappi-alg- ja esitatavad 

[![Screenshot41](./media/screenshot41.png)](./media/screenshot41.png)

C. Liikuge eelarve koostamise &gt;Setup &gt;eelarve planeerimise &gt;eelarve planeerimise konfiguratsiooni. Töövoo etapid vahekaardil saate töövoo automaatselt seostada – kinnitab staadiumid esma- ja esitatakse juhises loodud 

[![Screenshot42](./media/screenshot42.png)](./media/screenshot42.png)  


