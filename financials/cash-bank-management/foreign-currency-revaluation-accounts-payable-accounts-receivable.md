---
title: "Ostureskontro ja Müügireskontro välisvaluuta ümberarvutamine"
description: "Vahetuskursside kõikumised põhjustavad välisvaluutades avatud kannete teoreetilise väärtuse (raamatupidamisliku väärtuse) erinevusi ajas. See artikkel annab teavet välisvaluuta ümberarvutamise protsessi kohta, mida kasutatakse avatud kannete väärtuse uuendamiseks Ostureskontros ja Müügireskontros."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f09589a6f0a684752c7c9b98528e9546fedf341e
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="foreign-currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Ostureskontro ja Müügireskontro välisvaluuta ümberarvutamine

[!include[banner](../includes/banner.md)]


Vahetuskursside kõikumised põhjustavad välisvaluutades avatud kannete teoreetilise väärtuse (raamatupidamisliku väärtuse) erinevusi ajas. See artikkel annab teavet välisvaluuta ümberarvutamise protsessi kohta, mida kasutatakse avatud kannete väärtuse uuendamiseks Ostureskontros ja Müügireskontros. 

Välisvaluuta avatud kannete teoreetiline väärtus või raamatupidamislik jääkväärtus muutub aja jooksul sõltuvalt vahetuskursside kõikumisest. Avatud kannete uuendamiseks Ostureskontros ja Müügireskontros käitage välisvaluuta ümberarvutamise protsessi. Välisvaluuta ümberarvutamist saab kasutada nii Ostureskontro kui ka Müügireskontro puhul. Protsess kasutab avatud summade või tasakaalustamata summade ümberarvutamiseks määratud kuupäeva uut valuutakurssi. Algselt sisestatud summade ja ümberarvutatud summade erinevused põhjustavad igale avatud kandele realiseerimata kasumi või kahjumi. Seejärel uuendatakse Ostureskontro ja Müügireskontro alammooduleid, et kajastada realiseerimata kasumit või kahjumit, ja pearaamatusse sisestatakse raamatupidamise kirje.

## <a name="simulate-a-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise simuleerimine
Enne avatud kannete välisvaluuta summade ümberarvutamist saate käitada välisvaluuta ümberarvutamise simulatsiooniaruannet sama kuupäeva ja meetodiga. Simulatsiooniaruande käitamiseks avage lehekülg **Välisvaluuta ümberarvutamine** ja klõpsake nuppu **Simulatsioon**. Aruanne sisaldab realiseerimata kasumi või kahjumi summa eelvaadet, mis põhineb simulatsiooni sätetes määratletud parameetritel.

## <a name="process-a-foreign-currency-revaluation"></a>Välisvaluuta ümberarvutamise töötlemine
Avatud kannete ümberarvutamiseks avage lehe **Välisvaluuta ümberarvutamine** jaotis **Perioodilised ülesanded**. Saate käivitada protsessi reaalajas või ajastada selle käivitamise, kasutades pakki. Kui määratlete ümberarvutamise protsessi sätteid, veenduge, et kinnitate, kas soovite aruande tulemusi printida. Ümberarvutamise aruannet ei saa pärast protsessi lõpule jõudmist enam uuesti printida. Välisvaluuta ümberarvutamise aruandes näidatakse see mitmeid kliendi/hankija ja valuuta tasemel saldosid:

-   klientide või hankijate välisvaluutas tehtud kannetega saldode ümberarvutatud väärtused. Näidatakse järgmisi saldosid:
    -   algne kogusaldo välisvaluutas;
    -   välisvaluuta kogusumma arvestusvaluutas eelmise ümberarvutamise põhjal;
    -   välisvaluuta kogusumma arvestusvaluutas praeguse ümberarvutamise põhjal;
    -   eelmise ja praeguse ümberarvutamise erinevus. See erinevus moodustab täiendava realiseerimata kasumi või kahjumi.
-   realiseerimata kasumi või kahjumi kogusumma iga valuuta puhul.

Välisvaluuta ümberarvutamise käitamisel luuakse alati seda kajastav kirje. Ümberarvutamisel loodud kannete üksikasjaliku loendi vaatamiseks avage lehekülg **Välisvaluuta ümberarvutamine** ja valige **Kanded**. Iga kanne tähistab ümberarvutatud avatud kannet. Kui avatud kannet arvutati ümber rohkem kui ühe korra, näete kaht sama kannet kasutavat kirjet. Üks kirje on eelmise realiseerimata kasumi või kahjumi tühistamiseks ja teine kirje märgib uut realiseerimata kasumit või kahjumit. Ümberarvutamise protsessi käitamiseks klõpsake nuppu **Välisvaluuta ümberarvutamine**. Määratlege järgmiste parameetrite jaoks sobivad sätted.

-   **Meetod** – määrake meetod, mida kasutatakse valitud välisvaluuta ümberarvutamise töös.
    -   **Standardne** – see tähendab, et välisvaluuta ümberarvutamise tööd sisestatakse olenemata sellest, kas tulemuseks on kasum või kahjum.
    -   **Miinimum** – see tähendab, et välisvaluuta ümberarvutamise tööd sisestatakse ainult juhul, kui tulemuseks on kahjum.
    -   **Arve kuupäev** – see tähendab, et välisvaluuta ümberarvutamise töödes kasutatakse kannete algset vahetuskurssi, mis arvutatakse ümber algväärtusse arvestusvaluutas. Varasemate välisvaluuta ümberarvutamiste tulemused tühistatakse.
-   **Kaalutud kuupäev** – kuupäev, millal leitakse kõik kanded, millel on sellel kuupäeval avatud (tasakaalustamata) summad. Välisvaluutas olevad summad arvutatakse ümber vahetuskurssidega, mis sisestatakse vastava kuupäeva kohta lehele **Valuuta vahetuskursi määrad**. Kui välisvaluutas olevad summad vastaval kuupäeval ümber arvutatakse, saab sellest korrigeeritavate kannete puhul viimane välisvaluuta ümberarvutamise kuupäev. Kui käitate korrigeeritud kannete viimasest välisvaluuta ümberarvutamise kuupäevast varasema kaalutud kuupäevaga välisvaluuta ümberarvutamise, siis ei korrigeeri perioodiline töö selliseid kandeid, mis on varasemal kaalutud kuupäeval küll avatud, kuid millel on hilisem viimase välisvaluuta ümberarvutamise kuupäev.
-   **Kursi kuupäev** – kuupäev, mis määrab välisvaluuta ümberarvutamise puhul kasutatava vahetuskursi.
-   **Kasuta sisestusreegleid** – sisestusreegel, mida kasutatakse vaikimisi põhikonto Müügireskontro või Ostureskontro kannete välisvaluuta ümberarvutamise raamatupidamise kannetes.
    -   **Sisestamine** – kasutatakse kliendikande sisestusreeglit.
    -   **Valimine** – sisestusreeglid sisestatakse väljal **Sisestusreeglid**.
-   **Sisestusreeglid** – kui väljal **Kasuta sisestusreegleid** on tehtud valik **Vali**, määratakse välisvaluuta ümberarvutamise kannete sisestusprofiil sellel väljal oleva sisestusprofiiliga.
-   **Finantsdimensioonid** – finantsdimensioonid, mis sisestatakse välisvaluuta ümberarvutamise raamatupidamise kirjetesse.
    -   **Puudub** – finantsdimensioonide pole sisestatud. Nõutava finantsdimensiooni olemasolul konto struktuuris käitatakse siiski ümberarvutamise protsess, mille tulemusena luuakse finantsdimensioonideta raamatupidamise kirjed. Enne aga saate hoiatusteate, nii et saate ümberarvutamise tühistada.
    -   **Tabel** – kliendi või hankija konto finantsdimensioonid sisestatakse välisvaluuta ümberarvutamise kannetesse.
    -   **Sisestamine** – ümber arvutatava kande finantsdimensioonid sisestatakse välisvaluuta ümberarvutamise kannetesse. Vaikimisi kasutatakse algse AR/AP pearaamatukonto finantsdimensioone AR/AP põhikonto ümberarvutamise kandes ning algse kulu/vara/tulu pearaamatukonto kande finantsdimensioone kasutatakse realiseerimata kasumi/kahjumi põhikonto ümberarvutamise kandes.





