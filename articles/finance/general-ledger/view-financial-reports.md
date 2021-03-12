---
title: Finantsaruannete vaatamine
description: Selles teemas kirjeldatakse, kuidas kuvada ja uurida finantsaruandeid Microsoft Dynamics 365 Financeis. See sisaldab teavet mitmesuguste võimaluste kohta, mida saate finantsaruannetele rakendada, et muuta nende välimust ja andmeid, mida need sisaldavad.
author: kweekley
manager: AnnBe
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 066f37c399754f795639ab04ddca09abc01a43eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975453"
---
# <a name="view-financial-reports"></a>Finantsaruannete vaatamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kuvada ja uurida finantsaruandeid. See sisaldab teavet mitmesuguste võimaluste kohta, mida saate finantsaruannetele rakendada, et muuta nende välimust ja andmeid, mida need sisaldavad.

<a name="financial-reporting-overview"></a>Finantsaruandluse ülevaade
----------------------------

## <a name="open-a-financial-report"></a>Finantsaruande avamine
Aruande avamiseks valige aruande nimi. Aruande esmakordsel avamisel koostatakse see automaatselt eelmise kuu kohta. Näiteks kui avate aruande esmakordselt augustis 2015, koostatakse aruanne 31. juuli 2015 kohta. Pärast aruande avamist saab seda uurida, minnes süvitsi konkreetsetes andmehulkades ja muutes aruande valikuid.

## <a name="drill-down-on-a-financial-report"></a>Finantsaruandesse süvitsiminek
Finantsaruanded võivad sisaldada mitut üksikasjataset. Rahaline tase on esimene tase, mida finantsaruande avamisel näete. Konto tasemele minekuks valige andmed, millesse süvitsi minna. Näiteks müügi konto üksikasjade vaatamiseks valige müügi andmed, mida soovite uurida. Konto tasemelt saate minna süvitsi, et vaadata kandeid, mis moodustavad konto saldo. On kaks võimalust kannete vaatamiseks: aruandekanded ja kande tehingukanded.

-   **Aruandekanded** – kanded kuvatakse finantsaruandes sisalduvas vormindatud vaates. Kannete kuvamiseks vormindatud vaates valige andmed, milles süvitsi minna, ja klõpsake siis valikut **Aruande kande tasandile süvitsiminek**.
-   **Kande tehingukanded** – avab kande tehingukande päring, kus saate kandeid vaadata. Kannete kuvamiseks kande tehingukande päringus valige andmed, milles süvitsi minna, ja klõpsake siis valikut **Kontokannete avamine**.

Kui andmed on eelarveandmed, saate avada eelarvekonto kirjed. Aruande tasemete sulgemiseks ja alguspunkti naasmiseks võite vajutada paoklahvi Esc või klõpsata nuppu **Sule** (**X**) ülal paremas nurgas.

## <a name="change-report-options"></a>Aruande suvandite muutmine
Saate rakendada atribuudi- ja dimensioonifiltreid või muuta eelarvestsenaariumi aruandes **Tegelik vs eelarve**. Klõpsake tegumiribal valikut **Aruandevalikud** ja tehke siis vähemalt üks järgmistest toimingutest.

-   Aruandele atribuudifiltrite rakendamiseks valige käsk **Lisa atribuudifilter**. Valige atribuudi tüüp, tippige atribuudi väärtus ja klõpsake siis **OK**. Näiteks kui valite atribuudi **Konto kategooria**, sisestage atribuudi väärtuseks **MÜÜK**. Atribuudifiltri eemaldamiseks klõpsake käsku **Tühjenda**.
-   Aruandele dimensioonifiltrite rakendamiseks valige **Lisa dimensioonifilter**. Valige dimensioon ja seejärel sisestage dimensiooni ID või valige loendist dimensioon. Dimensioonifiltri eemaldamiseks klõpsake käsku **Tühjenda**.
-   Aruandes **Tegelik vs eelarve** stsenaariumi muutmiseks valige uus stsenaarium ja klõpsake siis nuppu **OK**. Kui valitud stsenaarium on erineva finantsaasta kohta, ei esitata tulemusi. Näiteks kui aruanne on loodud FY2015 jaoks ja praegune stsenaarium on FY2015 jaoks ja uus stsenaarium valitakse FY2016 jaoks, tulemusi ei näidata. Kui vajatakse uut stsenaariumi erineva finantsaasta kohta, looge stsenaariumiga seotud finantsaastale uus aruande versioon.

Kui klõpsate **OK**, rakendatakse kõik valitud suvandid aruandele. Kui otsustate, et ei soovi valitud suvandeid rakendada, klõpsake käsku **Tühista**.

## <a name="update-a-financial-report"></a>Finantsaruande värskendamine
Saate värskendada (uuendada) finantsaruannet nii, et seal oleks kuvatud kõige värskemad andmed selle perioodi ja aasta kohta, mille jaoks aruanne koostati. Näiteks kui värskendate finantsaruannet, mis koostati 2015. aasta oktoobri kohta, kajastab aruande kõiki uusi kandeid, mis 2015. aasta oktoobri kohta sisestati. Finantsaruande värskendamiseks klõpsake tegumiribal käsku **Värskenda**. Värskendatud aruanne on kättesaadaval vaid seda värskendanud inimesele. Selleks, et teised inimesed samu andmeid näeksid, tuleb aruanne avaldada.

## <a name="publish-a-financial-report"></a>Finantsaruande avaldamine
Pärast finantsaruande värskendamist saate selle avaldada. Siis saavad teised organisatsiooni inimesed seda vaadata. Aruande avaldamiseks klõpsake tegumiribal käsku **Avalda**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Finantsaruande kuvamine teises valuutas
Finantsaruande saab kuvada alati soovitud valuutas. Aruande kuvamiseks teises valuutas klõpsake tegumiribal nuppu **Valuuta** ja seejärel valige valuuta. Aruande teisendatakse sellesse valuutasse ja kuvatakse tulemused. Aruande kujunduses sisalduvaid valuutakoode või sümboleid muudetakse nii, et need kajastaksid uut valuutat. Loendis kuvatavad valuutad on Finance’is konfigureeritud aruandlusvaluutad.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Finantsaruande kokkuvõttevaate kuvamine
Finantsaruanne võib sisaldada üksikasjaridu ja kokkuvõtteridu. Üksikasjaread on read, mis sisaldavad põhikontosid või dimensioone. Kokkuvõtteread on kirjelduse, koondsumma ja arvutuste read. Ainult aruande kokkuvõtteridade kuvamiseks klõpsake nuppu **Kuva** ja seejärel valikut **Ainult kokkuvõtteread**. Aruanne ahendatakse ning kuvatakse ainult kokkuvõtteread. Üksikasjaridade kuvamiseks koos kokkuvõtteridadega klõpsake nuppu **Kuva** ja seejärel uuesti valikut **Ainult kokkuvõtteread**.

## <a name="print-a-financial-report"></a>Finantsaruande printimine
Finantsaruande printimine loob PDF-faili, mille saab seejärel käsitsi printida. Prinditava finantsaruande loomiseks klõpsake tegumiribal nuppu **Prindi** ja tehke siis vähemalt üks järgmistest toimingutest prindisuvandite määramiseks.

-   Prinditud aruandesse mitmesuguste üksikasjatasemete lisamiseks määrake liuguri asendiks **Jah** või **Ei**. Kui aruandes kasutatakse aruandluspuud, saate lisada kõik aruandlusüksused või ainult praeguse aruandlusüksuse.
-   Lehe suuruse määramiseks valige loendist lehe suurus.
-   Lehe paigutuse määramiseks valige loendist paigutus. Kui soovite sobitada aruande sisu enda valitud laiusega, määrake liuguri asendiks **Jah**.
-   Lehe ääriste määramiseks tippige ülemise, alumise, vasaku ja parema äärise suurus tollides.

Kui olete prindisuvandite määramise lõpetanud, klõpsake jätkamiseks nuppu **Prindi** ja teilt küsitakse, kas soovite faili alla laadida või selle OneDrive’i või SharePointi salvestada. Kui te ei soovi jätkata, klõpsake selle asemel nuppu **Tühista**. Kui jätkate, hakatakse aruannet serveris renderdama ja teil palutakse aruanne PDF-vormingus alla laadida. Nüüd saate oma aruannet vaadata PDF-i vaaturis ja siin saate valida printeri, kuhu aruanne saata, ning teha prindisuvanditele täiendavaid kohandusi.

## <a name="export-a-financial-report"></a>Finantsaruande eksportimine
Finantsaruande eksportimiseks klõpsake tegumiribal käsku **Ekspordi**. Aruanne eksporditakse Microsoft Excelisse ja brauser küsib, kas soovite eksporditud faili avada või salvestada. Aruande kujunduses määratletud ekspordisätted rakendatakse eksporditud aruandele.    

<a name="additional-resources"></a>Lisaressursid
--------

[Finantsaruandlus](../../dev-itpro/analytics/financial-reporting-intro.md)




