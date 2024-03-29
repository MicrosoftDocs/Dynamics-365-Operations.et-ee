---
title: Eelarve koostamise ülevaade
description: Peaaegu iga ettevõte, mis kasutab Microsoft Dynamics finantsfunktsioone rakenduses 365 Finance, peab saama luua aruandeid eelarve vs. tegelike kohta. See artikkel selgitab minimaalset konfiguratsiooni, mida on vaja eelarvete loomiseks finantsis ja toimingutes või nende laadimiseks kolmanda osapoole programmist.
author: panolte
ms.date: 04/29/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: kfend
ms.custom:
- "60113"
- intro-internal
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 380afc399a050215bb2d7b1e5ddb20088226f654
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068956"
---
# <a name="budgeting-overview"></a>Eelarve koostamise ülevaade

[!include [banner](../includes/banner.md)]

Peaaegu iga ettevõte, mis kasutab Microsoft Dynamics finantsfunktsioone rakenduses 365 Finance, peab saama luua aruandeid eelarve vs. tegelike kohta. See artikkel selgitab minimaalset konfiguratsiooni, mida on vaja eelarvete loomiseks finantsis ja toimingutes või nende laadimiseks kolmanda osapoole programmist.

## <a name="overview"></a>Ülevaade

Juriidilise isiku kinnitatud eelarve talletatakse dokumendis, mida nimetatakse *eelarveregistri kandeks*. Eelarveregistri kirje dokumendi ridu nimetatakse *eelarvekonto* kirjeteks ning need sisaldavad finantsdimensiooni teavet, kuupäevi ja kinnitatud eelarve summasid. Eelarveregistri kirje dokument on integreeritud põhifinantsaruannetega ja päringulehtedega, kus pearaamatu tegelikke summasid võrreldakse eelarvesummadega. 

Eelarveregistri kirjete loomiseks on mitu võimalust.

-   Sisestage käsitsi dokumendi teave lehele **Eelarveregistri kirjed**.
-   Kasutage Microsoft Exceli malli, mille saate avada, klõpsates nuppu **Ava Excelis** lehel **Eelarveregistri kirjed**.
-   Kasutage eelarveregistri kirjete importimiseks andmeüksust **Eelarvekonto kirjed** jaotises Andmehaldus. Kaaluge selle meetodi kasutamist ja parameetri **Komplektil põhinev töötlemine** sisselülitamist, kui peate importima süsteemi palju eelarvekonto kirjeid.
-   Kui ettevõte kasutab eelarve andmete ettevalmistamiseks funktsiooni Eelarve plaanimine, saate kasutada perioodilist protsessi **Loo eelarveregistri kirje**.

Eelarveregistri kirje loetakse lõpetatuks, kui eelarvesaldosid on värskendatud. Klõpsake lehel **Eelarveregistri kirjed** valikut **Eelarvesaldode värskendamine** valitud eelarveregistri kirje või mitme kirje jaoks. Pärast eelarvesaldode värskendamist saab eelarveregistri olekuks **Lõpule viidud**. Lõpule viidud eelarveregistri kirjet ei saa redigeerimiseks uuesto avada. Seega kui eelarveandmeid tuleb korrigeerida, peate looma uue eelarveregistri kirje, mitte parandama andmeid lõpetatud eelarveregistri kirjet.

## <a name="configuration"></a>Konfiguratsioon
Kui konfigureerite eelarve koostamist, alustage lehel **Eelarvestuse parameetrid**. Sellel lehel peate määratlema eelarve töölehe, eelarveregistri kirjete numbriseeria ja tööruumide vaikekäitumise.

Kui on poliitikaid, mis juhivad eelarveregistri kirjete kinnitamist eelarve tüübi alusel (nt ülekanded või revisjonid), peate looma lehel **Eelarvestuse töövood** eelarveregistri kirje töövood. Kui on stsenaariume, mille puhul on kanded lubatud ilma töövoo kinnituseta, saate määratleda eelarvekannete reeglid stsenaariumite toetamiseks. 

Lehel **Eelarvestamise dimensioonid** peate valima finantsdimensioonid, mida kasutatakse eelarvestamiseks kontoplaanis kasutatavate dimensioonide alusel. Saate eelarvestamiseks valida kõik finantsdimensioonid või dimensioonid alamkogumi.

Määratlege *eelarvemudel* mis vastab kõigile või mõnele eelarvele. Saate kasutada ühte eelarvemudelit kõikide eelarveregistri kirjete puhul. Teise võimalusena saate luua eraldi mudelid, mis põhinevad eelarvetüübil, geograafilisel asukohal või muul, mille järgi saab eelarvet klassifitseerida. 

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

365 Microsoft Dynamics Finantsversioonis 10.0.7 (jaanuar 2020) tutvustatud funktsioon lisas eelarve registrikirjete võimalusi ja paindlikkust. Nende täiustuste lubamiseks avage tööruum **Funktsioonihaldus** ning valige **Eelarve registrikirjed ainult koguse kohta** ja/või **Eelarve registrikirjed vaikesummatüübiga**.

Funktsioon **Eelarve registrikirjed ainult koguse kohta** võimaldab teil sisestada eelarve registrikirje ainult kogustega. Näiteks saate sisestada eelarvekirje kogusega 32 ja nullihinnaga, mille tulemuseks on nullsumma. Seejärel saate seda kogust kasutada finantsaruande kontekstis, et määrata hind koguse kohta. Pidage meeles, et selle funktsiooni osana ei värskendatud ühtegi päringut ega aruannet. See funktsioon lihtsalt võimaldab teil sisestada nullsumma.

Funktsioon **Eelarve registrikirjed vaikesummatüübiga** võimaldab sisestada eelarve registrikirjena vaikimesummatüübi, mis ei ole kulu. Kui põhikonto tüüp on kulu, siis on eelarve registrikirje rea vaikeväärtus kulu; kui põhikonto tüüp on tulu, siis on vaikeväärtus tulu; ja kõigi muude kontotüüpide korral on vaikeväärtus kulu.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Tööruumide ja päringulehtede kasutamine eelarve vs tegelike kulude jälgimiseks
Eelarvehaldur saab praguse eelarve oleku üle vaadata tööruumis **Pearaamatu eelarved ja prognoosid**. Vahekaardid **Kulu ületab eelarve** ja **Tulu on eelarvest väiksem** annavad kiire ülevaate finantsdimensiooni kombinatsioonidest, kui eelarve eesmärke ei täideta või kui need lähenevad lävile. Saate isikupärastada eelarvelävi protsenti ja finantsdimenesioonide komplekte, mida nende vahekaartidega kasutatakse, klõpsates suvandit **Minu tööruumi konfigureerimine**. Saate klõpsata suvandit **Üksuse juhid**, et näha töötajaid, kes vastutavad kindla finantsdimensioonide kombinatsioonide eest, mis valitakse nendel vahekaartidel. Näiteks kui näete, et operatsiooniosakonna kulueelarve ületab eelarvelävi, leiate hõlpsasti operatsiooniosakonna juhi, võtate temaga ühendust ja arutate probleemi. 

> [!NOTE] 
> Väli **Osakonnajuhataja** lehel **Organisatsiooni üksused** määrab, millised juhid toetavad kindlaid finantsdimensioonide kombinatsioone. Klõpsake vahekaardi allosas suvandit **Vt lisa**, et avada päringuleht **Eelarveline vs tegelik**, et saada lisateavet eelarvesummade ja tegelike summade kohta. 

Päringuleht **Tegelik võrreldes eelarvega** võimaldab süveneda eelarvesummade ja tegelike summade üksikasjadesse. Valige päringulehel rida ja klõpsake siis suvandit **Perioodi saldod**, et näha, kuidas eelarve ja tegelikud summad rahandusperioodil jaotuvad. Lehel **Eelarvekonto kirjed** saab süveneda eelarveregistri kirjetes oleva eelarvesumma üksikasjadesse. Leht **Üldised töölehe sisestused** avab pearaamatu kanded, mis on lisatud arvutatud summale **Tegelikud**. 

Funktsiooni Eelarve planeerimine kasutav ettevõte saab luua *eelarveprognoose* ja neid kasutada tööruumis **Pearaamatu eelarved ja prognoosid**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

