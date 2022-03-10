---
title: Gantti diagramm tööde plaanimiseks
description: Tootmise plaanijad saavad juhtida ja optimeerida tootmisplaane Gantti diagrammide abil.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage, GanttColorTable, GanttReqExplosionColor, GanttReqExplosionSetup, GanttTable, GanttTimescaleSetup, GanttWrkCtr, GanttWrkCtrColor, GanttWrkCtrJobInfo, GanttWrkCtrLoadResources, GanttWrkCtrMoveJob, GanttWrkCtrSetup, GanttWrkCtrView
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 180fb7b31ea826c546aa8472a7ef4025a3b8865a783a5b662ed30b69f98acf92
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730198"
---
# <a name="gantt-chart-for-job-scheduling"></a>Gantti diagramm tööde plaanimiseks

[!include [banner](../includes/banner.md)]

Gantti diagrammi eesmärk on anda tootmise plaanijatele võimalus tootmisplaani juhtimiseks ja optimeerimiseks. Gantti diagramm muudab toiminguvoo läbipaistvaks ja teeb tootmisgraafiku kohandamise lihtsaks, arvestades samas materjali või ressursside puudujääke. see aitab plaanijatel olemasolevaid ressursse kõige paremini kasutada, minimeerida pooleliolevat tööd ja optimeerida tootmistellimuste läbilaskeaegu.

Gantti diagramm on plaanitud tegevuste visuaalne esitus määratletud ajavahemiku jooksul. Tegevused plaanitakse ressurssidele, millel on võimsuse kalendriga määratletud võimsus. Gantti diagrammil saab kuvada järgmist tüüpi tegevused.

-   Tööd töögraafikus olevatest tootmistellimustest.
-   Tööd plaanitud tootmistellimustest.
-   Töö plaanitud projektitegevused tüübiga Tunniprognoosid.

Gantti diagrammi saab avada kahes vaates: **Tellimuse vaade** ja **Ressursivaade**. Suvandi **Tellimusevaade** puhul on tegevused grupeeritud tootmistellimuste alla. Sellest võib olla abi näiteks juhul, kui soovite hoida ülevaadet kõigist samadesse tellimustesse kuuluvatest töödest. **Ressursi vaates** rühmitatakse kõik tööd eraldi ressursside alla. Sellest vaatest võib olla abi plaani optimeerimisel ressursi tasandil (nt masin või masinate grupp). Järgmistel illustratsioonidel olevad Gantti diagrammid näitavad vaateid **Tellimuse vaade** ja **Ressursivaade**, millel on järgmised põhielemendid.

1.  Gantti diagrammi tegevus
2.  Materjali puudujäägi ikoon
3.  Materjali saadavuse ikoon
4.  Tellimuse tarnekuupäeva ikoon
5.  Võimsusriba

## <a name="order-view"></a>Tellimusevaade

[![Tellimuse vaade.](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Ressursivaade
[![Ressursivaade.](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Tegevused
Tegevused kuvatakse ribadena ja need on paigutatud ajaskaala tabelisse koos plaanitud alguse ja lõpu ajaga, mis muudab ribade pikkuse proportsionaalseks tegevuse lõpuleviimiseks vajaliku ajaga. Tegevused kuvatakse vastavalt ajaskaalale. Ajaskaalat saab kohandada menüüs, kus tuleb valida alguse ja lõpu kuupäev ning ajaühik, nt tunnid või päevad. Ajaskaalat kohandades saate määrata fookuse ajavahemikule, milles soovite tegevusi hallata. 

Parema ülevaate saamiseks on erinevaid võimalusi tegevuste värvi juhtimiseks. Saate konfigureerida tegevustele eraldi värvi, kasutada rakenduse kujunduse üldist värvi või seadistada värvi juhtimise tootmistellimuste värvikoodiga. 

Tegevuste ajavahemikul on taustatoon. Valge tooniga perioodid tähistavad tegevuse puhul määratud ressursivõimsusega ajavahemikku, samas kui halli tooniga perioodid tähistavad ajavahemikke, kus võimsust määratud ei ole. 

Diagrammi vasakul poolel on lisateave tegevuse kohta, nt ressurss, millele tegevus on plaanitud, ja tootmistellimuse number. Samasse tellimusse kuuluvate tööde vaheline seos on näidatud noolega. 

Tegevuse kohta saate lisateavet tegevuse dialoogiboksist. Dialoogiboksi avamiseks tehke tegevusel topeltklõps või valige menüü **Teave**. Tegevuse dialoogis saate vaadata plaanitud alguse ja lõpu kuupäeva ning kellaaja teavet nende materjalide kohta, mida on plaanitud tegevuses tarbida. 

Tegevused saab rühmitada grupeerimistasemeteks. Grupeerimistasemed on hierarhilised ja neid saab kasutada loogilise tegevuste grupi loomiseks. Näiteks kui teil on paigutus, kus tootmistegevused on grupeeritud laoala, tootmisüksuste, ressursigruppide ja ressursside järgi, saate kasutada neid rühmitamistasemeid tegevuste rühmitamiseks selle paigutuse kohaselt. Rühmitamise tasemeid saab laiendada ja ahendada kas eraldi rühmitamistasemel või kõigil diagrammi tasemetel, kasutades menüüs nuppe **Laienda kõik** ja **Ahenda kõik**. Saate konfigureerida ka rühmitamistasemete laiendamise või ahendamise diagrammi avamisel.

### <a name="material-availability"></a>Materjali saadavus

Gantti diagrammi saab seadistada nii, et see annaks plaanijale üksikasjalikku teavet eraldi tegevuste materjali oleku kohta. See võib olla abiks näiteks juhtudel, kus materjal hilineb ja mõjutab tootmisplaani. Sel juhul tõstetakse Gantti diagrammis materjali väljaminekud esile, et plaanijal oleks lihtsam tagajärgi mõista ja vajalikke muudatusi teha. 

Töö kuvatakse materjali puudujäägi ikooniga, kui töögraafiku alguskuupäev on töö tarbitavate materjalide puhul hilisem kui materjali saadavuse kuupäev. Materjali saadavuse kuupäev arvutatakse sidumisandmete põhjal dünaamilises koondplaanis. Materjali puudujäägi ikoon kuvatakse näiteks tööl, mis tarbib materjali, mis on seotud ostutellimusega, mille sissetulek on töö plaanitavast alguskuupäevast hilisem.

### <a name="indicator-of-material-availability-date"></a>Materjali saadavuse kuupäeva indikaator

Kui seadistate diagrammi, millel kuvatakse materjali puudujäägiga tööd, saab kuvada ka ikooni, mis näitab töö puhul materjali saadavuse kuupäeva. Ikoon kuvatakse ainult juhul, kui materjali saadavuse kuupäev on diagrammil määratletud ajavahemiku piirides. Kui materjali saadavuse kuupäev jääb väljapoole määratletud ajavahemikku, siis saab üksikasjalikuma materjali saadavuse teabe tuua materjaliloendist töö dialoogiboksis. Loendis on ka ikoon, mis näitab, millised materjalid on selle töö puhul hilinenud. Töö saab ümber plaanida, kasutades alguskuupäevana materjali saadavuse kuupäeva.

### <a name="indicator-of-order-delivery-date"></a>Tellimuse kohaletoimetamise kuupäeva indikaator

See ikoon näitab tootmistellimuse tarnekuupäev. Ikoon kuvatakse ainult tellimuse vaates.

### <a name="capacity-bar"></a>Võimsusriba

Saate konfigureerida diagrammi nii, et see kuvaks ressursi võimsusriba. See riba annab ülevaate ressursi võimsusest tegevuse puhul diagrammi määratletud ajavahemikul. Võimsusriba ei kuvata perioodide kohta, kus ressurssi pole reserveeritud. Perioodidel, kus ressurss on maksimaalselt reserveeritud, kuvatakse võimsusriba pideva ribana. Perioodidel, kus ressurss on üle reserveeritud, kuvatakse riba paksema ja punasena. Näiteks kui kaks tööd kattuvad, näitab võimsusriba kattumise ajavahemikul üle reserveerimist. Võimsusriba uuendatakse töö plaanimisel dünaamiliselt. Võimsusriba saab aktiveerida menüüs **Kuva võimsusriba**. Selle saab kuvada ainult **ressursi vaates**. Kui soovite saada ressursi puhul täiskoormusest üksikasjalikuma vaate, siis kasutage diagrammi **Täiskoormus**, mille saab avada valitud tegevuse menüüst või kontekstimenüüst.

## <a name="job-scheduling-in-the-gantt-chart"></a>Töö plaanimine Gantti diagrammil
Gantti diagramm pakub erinevaid võimalusi tootmisplaani kohandamiseks. Gantti diagrammil saate graafiku menüüs pukseerimise teel tegevusi ümber plaanida. Plaanimisprotsessis võite arvestada ressursi võimsust, ressursi võimeid ja materjali piiranguid.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Töö plaanimine pukseerimistoiminguga

Saate töö määratletud ajavahemikul pukseerimise teel ümber plaanida. Tööd saab ümber plaanida ainult samal ressursil ja plaanida saab ainult ühte tööd korraga.

### <a name="schedule-a-job-from-the-menu"></a>Töö plaanimine menüüst

Menüüs **Tööde plaanimine** saate plaanida vähemalt ühe diagrammil valitud töö plaanimise suuna ja plaanimise kuupäeva/kellaaja alusel. Saadaval on kolm plaanimise suunda.

-   Planeerimiskuupäevast edasi
-   Tagasi planeerimiskuupäevast
-   Materjalide kättesaadavuse kuupäevast edasi

Tööd ei saa plaanida väljaspool Gantti diagrammil määratletud ajavahemikku. Kui nii teete, jäetakse see töö plaanimata ja saate tõrketeate Laaditud ajaperioodile ei saanud tööd plaanida.

### <a name="schedule-previous-jobs"></a>Planeeri eelmised tööd

Tegevuste võrgus, nt samasse tootmistellimusse kuuluvate tööde puhul, saab kasutada funktsiooni **Eelmiste tööde plaanimine** võrgus valitud tööle eelnevate tööde plaanimiseks. Järgmises näites on esile tõstetud tegevus valitud töö. Diagramm kuvatakse enne eelmise töö plaanimist ja pärast eelmise töö plaanimist. 

[![Eelmise töö plaanimine.](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Planeeri järgmised tööd

Võite kasutada funktsiooni **Järgmiste tööde plaanimine** valitud tööle tegevuste võrgus eelnevate tööde plaanimiseks. Järgmises näites on esile tõstetud tegevus valitud töö. Diagramm kuvatakse enne järgmise töö plaanimist ja pärast järgmise töö plaanimist. 

[![Järgmise töö plaanimine.](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Plaani töö ümber

Võite kasutada funktsiooni **Plaani töö ümber** valitud tööle tegevuste võrgus järgnevate ja eelnevate tööde plaanimiseks. Järgmises näites on esile tõstetud tegevus valitud töö. Diagramm kuvatakse enne töö plaanimist ja pärast töö plaanimist. 

[![Plaani töö ümber.](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Korrasta tööd

Funktsiooni **Korrasta** abil saab korrastada valitud tegevused samal ressursil. Need tegevused võivad olla samas tegevuste võrgus, kuid võivad kuuluda ka erinevatesse võrkudesse. Kui kasutate korrastamise funktsiooni, siis eemaldatakse valitud tegevuste vahelised ajaerinevused. Võite kasutada seda funktsiooni ressursside võimsuse kasutuse optimeerimiseks. Diagramm kuvatakse enne töö plaanimist ja pärast töö plaanimist. 

[![Töö korraldamine.](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Tegevuste ümbermääramine ühelt ressursilt teisele

Võite määrata töö ühelt ressursilt teisele ümber. Sellest võib olla abi olukordades, kus masin pole töökorras või on üle reserveeritud ja teil on vaja leida töö tegemiseks teine ressurss.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Tegevuse ümbermääramine pukseerimistoiminguga

Vaates **Ressurss** saate määrata tegevuse Gantti diagrammil pukseerimistoiminguga teisele ressursile. Selleks tuleb valida rida, millel tegevus on plaanitud. Kui rida on valitud, võite lohistada rea ressursile diagrammil, mis on rühmitatud teise ressursigrupi taseme alla.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Tegevuse ümbermääramine menüüst Tööde plaanimine

Töö saab plaanida ümber dialoogiboksist **Töö plaanimine**, mis avaneb menüüst **Töö plaanimine**. Sellest menüüst saate määrata töö ümber ainult sellisele ressursile, mis on juba Gantti diagrammile laaditud. Kui valite ainult ühe töö, siis sorditakse selle ressursi ripploendit rakendatavate ressursside alusel. Kui valite rohkem töid, siis pole mingit teavet ressursiloendist rakendatavate ressursside kohta.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Gantti diagrammile lisaressursside laadimine
**Ressursivaates** on võimalik laadida Gantti diagrammile lisaressursse. See võib olla abiks, kui soovite leida üle reserveeritud või katkiläinud masinale plaanitud tööle alternatiivset ressurssi. Lehel **Lisaressursside laadimine** kuvatakse loend loendi avamise kuupäeva seisuga kehtivatest ressurssidest. Rakendatavad ressursid, mis on Gantti diagrammil valitud tööga seotud, kuvatakse loendis esimesena. Kui teil on valitud mitu tööd, ei kuvata enne loendi avamist mingit teavet rakendatavate ressursside kohta. Lehelt **Lisaressursside laadimine** saate valida vähemalt ühe ressursi, mis laaditakse Gantti diagrammile, kui oma valiku kinnitate. Kui Gantti diagrammi ajavahemikul pole valitud ressursile ühtegi tööd plaanitud, siis pannakse see ressurss Gantti diagrammil tegevuste loendi alumises osas olevale ressursi rühmitamise tasemele.

### <a name="access-the-gantt-chart"></a>Gantti diagrammi avamine

Gantti diagrammi saab avada järgmistelt lehtedelt.


|                                                 <strong>Leht</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Kirjeldus</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Tootmistellimuste loend ja üksikasjad</strong>                                    | Lehel <strong>Tootmistellimuste loend ja üksikasjad</strong> saate avada Gantti diagrammi vähemalt ühest valitud tellimusest. Kui avate diagrammi menüüelemendist <strong>Gantti diagramm</strong>, siis laaditakse kõik valitud tootmistellimustega seotud tööd, kuid ka teiste tootmistellimuste tööd, mis on plaanitud samadele ressurssidele. Diagrammi avamine menüüelemendist <strong>Gantti diagramm – kiirvaade</strong> laadib ainult valitud tootmistellimustega seotud tööd. Selles vaates pole võimalik töid plaanida. |
|                                               <strong>Ressurss</strong>                                                |                                                                                                                                                        Lehel <strong>Ressurss</strong> saate avada Gantti diagrammi menüüelemendist <strong>Gantti diagramm</strong>. Kui see on valitud, laaditakse diagrammile kõik ressursile valitud ajavahemikul plaanitud tööd.                                                                                                                                                         |
|                                            <strong>Ressursigrupp</strong>                                             |                                                                                                                                                 Lehel <strong>Ressursigrupp</strong> saate avada Gantti diagrammi menüüelemendist <strong>Gantti</strong> diagramm. Kui see on valitud, kuvatakse kõik ressursigrupis olevale ressursile plaanitud tööd valitud ajavahemikul.                                                                                                                                                 |
|                                             <strong>Gantti diagrammid</strong>                                              |                                                                                 Lehel <strong>Gantti diagrammid</strong> saate konfigureerida Gantti diagramme ressursside ja ressursigruppide kaupa. Näiteks kui soovite juhtida tootmistegevusi kindlate ressursikogumite või ressursigruppide puhul, siis võite neid <strong>Gantti diagrammide</strong> lehel eraldi konfigureerida. Seejärel saate avada Gantti diagrammi igast konfiguratsioonist.                                                                                 |
|                                       <strong>Tunnieelarved</strong> (projekt)                                        |                                                                                                                              Ressursside töögraafikusse saab panna projektitegevused tüübiga <strong>Tunnieelarve</strong>. Lehel <strong>Tunnieelarve</strong> menüüs <strong>Plaanimine</strong> võite avada tellimuse Gantti diagrammi, et vaadata tunnieelarve tüüpi projektitegevusi töögraafikus.                                                                                                                               |
|           <strong>Tehtav töö</strong> (Loend tööruumis <strong>Tootmisosakonna haldus</strong>)            |                                                                                               Jaotises <strong>Tehtavad tööd tööruumis Tootmisosakonna haldus</strong> on näha töid tootmis- ja partiitellimustest, mis on tööruumi valitud ressurssidel pooleli. Menüüelemendist <strong>Gantti diagramm</strong> saate avada Gantti diagrammi, kus kõik loendist valitud tööd laaditakse diagrammile.                                                                                               |
| <strong>Väljastatavad tootmistellimused</strong> (avatakse tööruumist <strong>Tootmisosakonna haldus</strong>) |                                                                                                                                         Väljastatavate tootmistellimuste leht avaneb tööruumist <strong>Tootmisosakonna haldus</strong>. Sellel lehel kuvatakse väljastamise ootel plaanitud tootmis- ja partiitellimused. Sellelt lehelt saab avada Gantti diagrammi valitud tootmistellimuste kohta.                                                                                                                                          |

## <a name="additional-resources"></a>Lisaressursid  
[Tootmis- ja partiitellimuste visuaalne plaanimine Gantti diagrammiga (video)](https://youtu.be/BtbuShkGj4I)

[Tootmistellimuste visuaalne plaanimine (demoskript)](/dynamics/s-e/)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]