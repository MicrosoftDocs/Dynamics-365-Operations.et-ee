---
title: "Eelarve koostamise ülevaade"
description: "Peaaegu igal ettevõttel, mis kasutab Microsoft Dynamics 365 for Operationsis funktsiooni Finantsid, on võimalik luua aruandeid, milles võrreldakse eelarvet tegelike näitajatega. See artikkel selgitab minimaalset konfiguratsiooni, mis on nõutav Dynamics 365 for Operationsis eelarvete loomiseks või nende laadimiseks kolmanda osapoole programmist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Eelarve koostamise ülevaade

[!include[banner](../includes/banner.md)]


Peaaegu igal ettevõttel, mis kasutab Microsoft Dynamics 365 for Operationsis funktsiooni Finantsid, on võimalik luua aruandeid, milles võrreldakse eelarvet tegelike näitajatega. See artikkel selgitab minimaalset konfiguratsiooni, mis on nõutav Dynamics 365 for Operationsis eelarvete loomiseks või nende laadimiseks kolmanda osapoole programmist.

<a name="overview"></a>Ülevaade
--------

Juriidilise isiku kinnitatud eelarve talletatakse dokumendis, mida nimetatakse *eelarveregistri kandeks*. Eelarveregistri kirje dokumendi ridu nimetatakse *eelarvekonto* kirjeteks ning need sisaldavad finantsdimensiooni teavet, kuupäevi ja kinnitatud eelarve summasid. Eelarveregistri kirje dokument on integreeritud põhifinantsaruannetega ja päringulehtedega, kus pearaamatu tegelikke summasid võrreldakse eelarvesummadega. 

Microsoft Dynamics 365 for Operationsis on eelarveregistri kirjete loomiseks mitu võimalust.

-   Sisestage käsitsi dokumendi teave lehele **Eelarveregistri kirjed**.
-   Kasutage Microsoft Exceli malli, mille saate avada, klõpsates nuppu **Ava Excelis** lehel **Eelarveregistri kirjed**.
-   Kasutage eelarveregistri kirjete importimiseks andmeüksust **Eelarvekonto kirjed** jaotises Andmehaldus. Kaaluge selle meetodi kasutamist ja parameetri **Komplektil põhinev** **töötlemine** sisselülitamist, kui peate importima süsteemi palju eelarvekonto kirjeid.
-   Kui ettevõte kasutab eelarve andmete ettevalmistamiseks funktsiooni Eelarve plaanimine, saate kasutada perioodilist protsessi **Loo eelarveregistri kirje**.

Eelarveregistri kirje loetakse lõpetatuks, kui eelarvesaldosid on värskendatud. Klõpsake lehel **Eelarveregistri kirjed** valikut **Eelarvesaldode värskendamine** valitud eelarveregistri kirje või mitme kirje jaoks. Pärast eelarvesaldode värskendamist saab eelarveregistri olekuks **Lõpule viidud**. Lõpule viidud eelarveregistri kirjet ei saa redigeerimiseks uuesto avada. Seega kui eelarveandmeid tuleb korrigeerida, peate looma uue eelarveregistri kirje, mitte parandama andmeid lõpetatud eelarveregistri kirjet.

## <a name="configuration"></a>Konfiguratsioon
Kui konfigureerite eelarve koostamist, alustage lehel **Eelarvestuse parameetrid**. Sellel lehel peate määratlema eelarve töölehe, eelarveregistri kirjete numbriseeria ja tööruumide vaikekäitumise.

Kui on poliitikaid, mis juhivad eelarveregistri kirjete kinnitamist eelarve tüübi alusel (nt ülekanded või revisjonid), peate looma lehel **Eelarvestuse töövood** eelarveregistri kirje töövood. Kui on stsenaariume, mille puhul on kanded lubatud ilma töövoo kinnituseta, saate määratleda eelarvekannete reeglid stsenaariumite toetamiseks. 

Lehel **Eelarvestamise dimensioonid** peate valima finantsdimensioonid, mida kasutatakse eelarvestamiseks kontoplaanis kasutatavate dimensioonide alusel. Saate eelarvestamiseks valida kõik finantsdimensioonid või dimensioonid alamkogumi.

Määratlege *eelarvemudel*, mis vastab kõigile või mõnele eelarvele. Saate kasutada ühte eelarvemudelit kõikide eelarveregistri kirjete puhul. Teise võimalusena saate luua eraldi mudelid, mis põhinevad eelarvetüübil, geograafilisel asukohal või muul, mille järgi saab eelarvet klassifitseerida. 

> [!NOTE] 
> Kui kasutatakse eelarve juhtimist, saate kindla eelarvetsükli perioodiga seostada ainult ühe eelarvemudeli. 

Looge *eelarvekoodid*, mis tuvastavad kirje ja seotud töövoo eelarvekannete tüübi. Eelarvekoodid toetavad järgmisi eelarvetüüpe.

-   Algne eelarve
-   Ülekanne
-   Revisjon
-   Pandiõigus
-   Eelpandiõigus
-   Ülekantav eelarve

Eelarvetüübid võimaldavad teil kasutada kinnitatud eelarvemuudatuste kontrolljälge kogu eelarvetsükli jooksul. Kui töövoog on seostatud eelarvekoodiga, lubatakse töövoog kõigi eelarveregistri kirjete puhul, mis seda eelarvekoodi kasutavad, ja töövoo etapid tuleb lõpule viia, enne kui eelarveregistri kirje jõuab olekusse **Lõpule viidud**.  

Soovi korral saate seadistada ka *eelarve ülekandereegleid*. Eelarve ülekandereeglite kasutamiseks valige lehel **Eelarve parameetrid** suvand **Kasuta eelarveülekannete reegleid**. Eelarve ülekandereeglite kasutamisel, kui kasutaja loob dokumendi, kasutades eelarvekoodi tüüpi **Ülekanne**, ei värskendata eelarvesaldosid, kui eelarve ülekandereegleid on rikutud. Näiteks saate lubada eelarve ülekandedokumendid, kui kulueelarve kantakse üle põhikontode müügi- ja turundusosakondade vahel, kuid saate keelata eelarve ülekandmise sellest osakonnast või sellesse osakonda, kui seda tüüpi eelarvekonto kirjele ei ole antud töövoo kinnitust.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Tööruumide ja päringulehtede kasutamine eelarve vs tegelike kulude jälgimiseks
Eelarvehaldur saab praguse eelarve oleku üle vaadata tööruumis **Pearaamatu eelarved ja prognoosid**. Vahekaardid **Kulu ületab eelarve** ja **Tulu on eelarvest väiksem** annavad kiire ülevaate finantsdimensiooni kombinatsioonidest, kui eelarve eesmärke ei täideta või kui need lähenevad lävile. Saate isikupärastada eelarvelävi protsenti ja finantsdimenesioonide komplekte, mida nende vahekaartidega kasutatakse, klõpsates suvandit **Minu tööruumi konfigureerimine**. Saate klõpsata suvandit **Üksuse juhid**, et näha töötajaid, kes vastutavad kindla finantsdimensioonide kombinatsioonide eest, mis valitakse nendel vahekaartidel. Näiteks kui näete, et operatsiooniosakonna kulueelarve ületab eelarvelävi, leiate hõlpsasti operatsiooniosakonna juhi, võtate temaga ühendust ja arutate probleemi. 

> [!NOTE] 
> Väli **Osakonnajuhataja** lehel **Organisatsiooni üksused** määrab, millised juhid toetavad kindlaid finantsdimensioonide kombinatsioone. Klõpsake vahekaardi allosas suvandit **Vt lisa**, et avada päringuleht **Eelarveline vs tegelik**, et saada lisateavet eelarvesummade ja tegelike summade kohta. 

Päringuleht **Tegelik võrreldes eelarvega** võimaldab süveneda eelarvesummade ja tegelike summade üksikasjadesse. Valige päringulehel rida ja klõpsake siis suvandit **Perioodi saldod**, et näha, kuidas eelarve ja tegelikud summad rahandusperioodil jaotuvad. Lehel **Eelarvekonto kirjed** saab süveneda eelarveregistri kirjetes oleva eelarvesumma üksikasjadesse. Leht **Üldised töölehe sisestused **avab pearaamatu kanded, mis on lisatud arvutatud summale **Tegelikud**. 

Funktsiooni Eelarve planeerimine kasutav ettevõte saab luua *eelarveprognoose *ja neid kasutada tööruumis **Pearaamatu eelarved ja prognoosid**.



