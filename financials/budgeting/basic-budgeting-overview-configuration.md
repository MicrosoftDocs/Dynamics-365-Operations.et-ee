---
title: "Eelarve koostamise ülevaade"
description: "Peaaegu iga ettevõte, mis kasutab finantside funktsiooni Microsoft Dynamics 365 toiminguteks peab suutma luua aruanded eelarve vrd tegelikud näitajad. Selles artiklis selgitatakse minimaalne konfiguratsioon, mis on vajalikud Dynamics 365 operatsioonide eelarveid luua või laadida mõne muu programmi."
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

Peaaegu iga ettevõte, mis kasutab finantside funktsiooni Microsoft Dynamics 365 toiminguteks peab suutma luua aruanded eelarve vrd tegelikud näitajad. Selles artiklis selgitatakse minimaalne konfiguratsioon, mis on vajalikud Dynamics 365 operatsioonide eelarveid luua või laadida mõne muu programmi.

<a name="overview"></a>Ülevaade
--------

Juriidilise isiku kinnitatud eelarve talletatakse dokumendis, mida nimetatakse *eelarveregistri kandeks*. Eelarve registri kande dokumendi ridu on tuntud *eelarve konto* kirjed, ja sisaldavad rahalise dimensiooniteavet, kuupäevad ja summad kinnitatud eelarve. Registri kanne eelarvedokumendi on integreeritud põhilised finantsaruanded ja uurimise lehekülgi kus pearaamatu tegelikud summad on võrreldes eelarve summad. 

On mitu meetodit, luua eelarvekanded registri Dynamics 365 toiminguteks.

-   Sisestage käsitsi dokumendi teave lehele **Eelarveregistri kirjed**.
-   Kasutage Microsoft Exceli malli, mille saate avada, klõpsates nuppu **Ava Excelis** lehel **Eelarveregistri kirjed**.
-   Kasutage eelarveregistri kirjete importimiseks andmeüksust **Eelarvekonto kirjed** jaotises Andmehaldus. Kaaluge selle meetodi ja sisselülitamine ning **kooditabel,** ** töötlemise ** parameeter kui te importimise palju konto süsteemi.
-   Kui ettevõte kasutab eelarve andmete ettevalmistamiseks funktsiooni Eelarve plaanimine, saate kasutada perioodilist protsessi **Loo eelarveregistri kirje**.

Eelarve registrikande peetakse, kui eelarvesaldod on värskendatud. Kohta ning **eelarve toimingud** klõpsake valikul **muudetud eelarve tasakaalu** valitud eelarve registrisse kandmise või mitu kirjet. Pärast eelarvesaldode värskendamist saab eelarveregistri olekuks **Lõpule viidud**. Lõpule viidud eelarveregistri kirjet ei saa redigeerimiseks uuesto avada. Seega kui eelarveandmeid tuleb korrigeerida, peate looma uue eelarveregistri kirje, mitte parandama andmeid lõpetatud eelarveregistri kirjet.

## <a name="configuration"></a>Konfiguratsioon
Kui konfigureerite eelarve koostamist, alustage lehel **Eelarvestuse parameetrid**. Sellel lehel peate määratlema eelarve töölehe, eelarveregistri kirjete numbriseeria ja tööruumide vaikekäitumise.

Kui on poliitikaid, mis juhivad eelarveregistri kirjete kinnitamist eelarve tüübi alusel (nt ülekanded või revisjonid), peate looma lehel **Eelarvestuse töövood** eelarveregistri kirje töövood. Kui on stsenaariume, mille puhul on kanded lubatud ilma töövoo kinnituseta, saate määratleda eelarvekannete reeglid stsenaariumite toetamiseks. 

Lehel **Eelarvestamise dimensioonid** peate valima finantsdimensioonid, mida kasutatakse eelarvestamiseks kontoplaanis kasutatavate dimensioonide alusel. Saate eelarvestamiseks valida kõik finantsdimensioonid või dimensioonid alamkogumi.

Määratleda ka * eelarvemudeli * vastavad kõik või osa eelarvest. Saate kasutada ühte eelarvemudelit kõikide eelarveregistri kirjete puhul. Teise võimalusena saate luua eraldi mudelid, mis põhinevad eelarvetüübil, geograafilisel asukohal või muul, mille järgi saab eelarvet klassifitseerida. 

> [!NOTE] 
> Eelarve kontrolli kasutamisel saate seostada ainult ühe eelarvemudeli konkreetne eelarve tsükliliselt aja jooksul. 

Looge *eelarvekoodid*, mis tuvastavad kirje ja seotud töövoo eelarvekannete tüübi. Eelarvekoodid toetavad järgmisi eelarvetüüpe.

-   Algne eelarve
-   Ülekanne
-   Revisjon
-   Pandiõigus
-   Eelpandiõigus
-   Ülekantav eelarve

Eelarvetüübid võimaldavad teil kasutada kinnitatud eelarvemuudatuste kontrolljälge kogu eelarvetsükli jooksul. Kui töövoog on seotud eelarve tähise, lubatakse töövoo jaoks kõik eelarve registrikanded, mida selle eelarve tähise ja töövoo samme tuleb lõpetada enne registrikande eelarve võib ulatuda ka **valminud** etapi.  

Saate ka seadistada *eelarvesse ülekandmise eeskirjad*. Eelarvesse ülekandmise eeskirjad kasutamiseks valige **reegleid kasutada eelarve ülekannete** kohta on **eelarve parameetrid** lehel. Eelarve ülekandereeglite kasutamisel, kui kasutaja loob dokumendi, kasutades eelarvekoodi tüüpi **Ülekanne**, ei värskendata eelarvesaldosid, kui eelarve ülekandereegleid on rikutud. Näiteks saate lubada eelarve ülekandedokumendid, kui kulueelarve kantakse üle põhikontode müügi- ja turundusosakondade vahel, kuid saate keelata eelarve ülekandmise sellest osakonnast või sellesse osakonda, kui seda tüüpi eelarvekonto kirjele ei ole antud töövoo kinnitust.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Tööruumide ja päringulehtede kasutamine eelarve vs tegelike kulude jälgimiseks
Eelarvehaldur saab praguse eelarve oleku üle vaadata tööruumis **Pearaamatu eelarved ja prognoosid**. Vahekaardid **Kulu ületab eelarve** ja **Tulu on eelarvest väiksem** annavad kiire ülevaate finantsdimensiooni kombinatsioonidest, kui eelarve eesmärke ei täideta või kui need lähenevad lävile. Saate isikupärastada eelarvelävi protsenti ja finantsdimenesioonide komplekte, mida nende vahekaartidega kasutatakse, klõpsates suvandit **Minu tööruumi konfigureerimine**. Saate klõpsata suvandit **Üksuse juhid**, et näha töötajaid, kes vastutavad kindla finantsdimensioonide kombinatsioonide eest, mis valitakse nendel vahekaartidel. Näiteks kui näete, et operatsiooniosakonna kulueelarve ületab eelarvelävi, leiate hõlpsasti operatsiooniosakonna juhi, võtate temaga ühendust ja arutate probleemi. 

> [!NOTE] 
> Selle **osakonna juhataja** sisse-välja ning **organisatsiooniüksuse** leht määrab, millised juhid toetavad konkreetse rahalise Dimensioonikombinatsioonid. Klõpsake vahekaardi allosas suvandit **Vt lisa**, et avada päringuleht **Eelarveline vs tegelik**, et saada lisateavet eelarvesummade ja tegelike summade kohta. 

Päringuleht **Tegelik võrreldes eelarvega** võimaldab süveneda eelarvesummade ja tegelike summade üksikasjadesse. Valige päringulehel rida ja klõpsake siis suvandit **Perioodi saldod**, et näha, kuidas eelarve ja tegelikud summad rahandusperioodil jaotuvad. Lehel **Eelarvekonto kirjed** saab süveneda eelarveregistri kirjetes oleva eelarvesumma üksikasjadesse. Leht **Üldised töölehe sisestused **avab pearaamatu kanded, mis on lisatud arvutatud summale **Tegelikud**. 

Funktsiooni Eelarve planeerimine kasutav ettevõte saab luua *eelarveprognoose *ja neid kasutada tööruumis **Pearaamatu eelarved ja prognoosid**.


