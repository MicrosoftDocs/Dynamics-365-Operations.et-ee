---
title: Finantsaruannete vaatamine
description: Selles artiklis kirjeldatakse, kuidas kuvada ja uurida finantsaruandeid Microsoft Dynamics 365 for Finance and Operationsis. See sisaldab teavet mitmesuguste võimaluste kohta, mida saate finantsaruannetele rakendada, et muuta nende välimust ja andmeid, mida need sisaldavad.
author: kweekley
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 10334
ms.assetid: d20f435f-fb65-4068-ab09-7efc7be683a6
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a939ce2f43645963392363fc6452f8bc55bd963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "312941"
---
# <a name="view-financial-reports"></a>Finantsaruannete vaatamine

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas kuvada ja uurida finantsaruandeid Microsoft Dynamics 365 for Finance and Operationsis. See sisaldab teavet mitmesuguste võimaluste kohta, mida saate finantsaruannetele rakendada, et muuta nende välimust ja andmeid, mida need sisaldavad.

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
Saate muuta aruande kuupäeva, rakendada atribuudi- ja dimensioonifiltreid või muuta eelarvestsenaariumi aruandes **Tegelik vs eelarve**. Klõpsake tegumiribal valikut **Aruandevalikud** ja tehke siis vähemalt üks järgmistest toimingutest.

-   Aruande baasperioodi ja baasaasta kasutamiseks valige vaasperiood ja baasaasta ning klõpsake nuppu **OK**.
-   Aruandele atribuudifiltrite rakendamiseks valige käsk **Lisa atribuudifilter**. Valige atribuudi tüüp, tippige atribuudi väärtus ja klõpsake siis **OK**. Näiteks kui valite atribuudi **Konto kategooria**, sisestage atribuudi väärtuseks **MÜÜK**. Atribuudifiltri eemaldamiseks klõpsake käsku **Tühjenda**.
-   Aruandele dimensioonifiltrite rakendamiseks valige **Lisa dimensioonifilter**. Valige dimensioon ja seejärel sisestage dimensiooni ID või valige loendist dimensioon. Dimensioonifiltri eemaldamiseks klõpsake käsku **Tühjenda**.
-   Aruandes **Tegelik vs eelarve** stsenaariumi muutmiseks valige uus stsenaarium ja klõpsake siis nuppu **OK**. Kui valitud stsenaarium on teise aasta kohta, muutke kindlasti baasaastat. Näiteks kui praegune stsenaarium on finantsaasta 2015 jaoks ja valite uue stsenaariumi, mis on finantsaasta 2016 jaoks, tuleb baasaastaks märkida **2016**.

Kui klõpsate **OK**, rakendatakse kõik valitud suvandid aruandele. Kui otsustate, et ei soovi valitud suvandeid rakendada, klõpsake käsku **Tühista**.

## <a name="update-a-financial-report"></a>Finantsaruande värskendamine
Saate värskendada (uuendada) finantsaruannet nii, et seal oleks kuvatud kõige värskemad andmed selle perioodi ja aasta kohta, mille jaoks aruanne koostati. Näiteks kui värskendate finantsaruannet, mis koostati 2015. aasta oktoobri kohta, kajastab aruande kõiki uusi kandeid, mis 2015. aasta oktoobri kohta sisestati. Finantsaruande värskendamiseks klõpsake tegumiribal käsku **Värskenda**. Värskendatud aruanne on kättesaadaval vaid seda värskendanud inimesele. Selleks, et teised inimesed samu andmeid näeksid, tuleb aruanne avaldada.

## <a name="publish-a-financial-report"></a>Finantsaruande avaldamine
Pärast finantsaruande värskendamist saate selle avaldada. Siis saavad teised organisatsiooni inimesed seda vaadata. Aruande avaldamiseks klõpsake tegumiribal käsku **Avalda**.

## <a name="display-a-financial-report-in-a-different-currency"></a>Finantsaruande kuvamine teises valuutas
Finantsaruande saab kuvada alati soovitud valuutas. Aruande kuvamiseks teises valuutas klõpsake tegumiribal nuppu **Valuuta** ja seejärel valige valuuta. Aruande teisendatakse sellesse valuutasse ja kuvatakse tulemused. Aruande kujunduses sisalduvaid valuutakoode või sümboleid muudetakse nii, et need kajastaksid uut valuutat. Loendis kuvatavad valuutad on Finance and Operationsis konfigureeritud aruandlusvaluutad.

## <a name="display-a-summarized-view-of-the-financial-report"></a>Finantsaruande kokkuvõttevaate kuvamine
Finantsaruanne võib sisaldada üksikasjaridu ja kokkuvõtteridu. Üksikasjaread on read, mis sisaldavad põhikontosid või dimensioone. Kokkuvõtteread on kirjelduse, koondsumma ja arvutuste read. Ainult aruande kokkuvõtteridade kuvamiseks klõpsake nuppu **Kuva** ja seejärel valikut **Ainult kokkuvõtteread**. Aruanne ahendatakse ning kuvatakse ainult kokkuvõtteread. Üksikasjaridade kuvamiseks koos kokkuvõtteridadega klõpsake nuppu **Kuva** ja seejärel uuesti valikut **Ainult kokkuvõtteread**.

## <a name="open-a-financial-report-from-a-previous-month"></a>Eelmine kuu finantsaruande avamine
Saate vaadata praeguse või eelmise kuu aruandeid, ilma aruannet uuesti koostamata. Eelneva kuu aruande avamiseks klõpsake nuppu **Näita** ja seejärel nuppu **Eelmised aruanded**. Ilmub loend eelnevatest kuudest, mille jaoks aruanne loodi. Laiendage kuud, mille kohta soovite aruannet kuvada, valige kuupäev ja klõpsake siis nuppu **OK**. Kuvatakse eelmise kuu aruanne. Praeguse kuu aruande juurde naasmiseks klõpsake nuppu **Tühista**.

## <a name="print-a-financial-report"></a>Finantsaruande printimine
Finantsaruande printimiseks klõpsake tegumiribal nuppu **Prindi** ja tehke siis vähemalt üks järgmistest toimingutest prindisuvandite määramiseks.

-   Prinditud aruandesse mitmesuguste üksikasjatasemete lisamiseks määrake liuguri asendiks **Jah** või **Ei**. Kui aruandes kasutatakse aruandluspuud, saate lisada kõik aruandlusüksused või ainult praeguse aruandlusüksuse.
-   Lehe suuruse määramiseks valige loendist lehe suurus.
-   Lehe paigutuse määramiseks valige loendist paigutus. Kui soovite sobitada aruande sisu enda valitud laiusega, määrake liuguri asendiks **Jah**.
-   Lehe ääriste määramiseks tippige ülemise, alumise, vasaku ja parema äärise suurus tollides.

Kui olete printimisvalikute seadistamise lõpetanud, klõpsake nuppu **Prindi** aruande printimiseks. Kui te ei soovi aruannet printida, klõpsake selle asemel nuppu **Tühista**. Kuvatakse prinditud aruande eelvaade. Saate valida printeri, kuhu aruanne edastada, ja kohandada prindisuvandeid.

## <a name="export-a-financial-report"></a>Finantsaruande eksportimine
Finantsaruande eksportimiseks klõpsake tegumiribal käsku **Ekspordi**. Aruanne eksporditakse Microsoft Excelisse ja brauser küsib, kas soovite eksporditud faili avada või salvestada. Aruande kujunduses määratletud ekspordisätted rakendatakse eksporditud aruandele.    

<a name="additional-resources"></a>Lisaressursid
--------

[Finantsaruandlus rakendusele Microsoft Dynamics AX](../../dev-itpro/analytics/financial-reporting-intro.md)




