---
title: "Pangahalduse tööruum"
description: "Teema annab teavet pangahalduse tööruumi kohta. See tööruum näitab ettevõtte pangakontodega seotud andmeid ja sisaldab kokkuvõttevaadet ning analüüsi lehte. Kokkuvõttevaade näitab kokkuvõttepaane, pangakonto andmeid, saldodiagrammi ja seotud andmeid. Analüüsi leht kasutab Microsoft Power BI võimalusi pangakonto saldodega seotud visuaalide kuvamiseks."
author: saraschi
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: 759de82e9cd1c08f86c0a8eb55fa7bae5c4f740f
ms.contentlocale: et-ee
ms.lasthandoff: 06/14/2017

---
# <a name="bank-management-workspace"></a>Pangahalduse tööruum

Tööruum **Pangahaldus** näitab ettevõtte pangakontodega seotud andmeid. See tööruum sisaldab vaadet **Kokkuvõte** ja lehte **Analüüs**. Vaade **Kokkuvõte** näitab kokkuvõttepaane, pangakonto andmeid, saldodiagrammi ja seotud andmeid. Leht **Analüüs** kasutab Microsoft Power BI võimalusi pangakonto saldodega seotud visuaalide kuvamiseks.

## <a name="summary-view"></a>Kokkuvõttevaade

### <a name="summary"></a>Kokkuvõte

Paanid jaotises **Kokkuvõte** annavad ülevaate pangakontodest ja kiire juurdepääsu lehtedele, mida on vaja kõige sagedamini kasutada. Panga vastavusseviimise teave on täpsema panga vastavusseviimise funktsiooni põhine. Lisatakse teave ainult nende pangakontode kohta, millel valiku **Täpsem panga vastavusseviimine** on seatud olekusse **Jah** lehel **Pangakonto**. Jaotisest **Kokkuvõte** saate importida elektroonilisi pangafaile pangakontodele kõigi juriidiliste isikute lõikes.

### <a name="bank-accounts"></a>Pangakontod

Iga pangakonto juriidilises isikus on kajastatud kaardiga jaotises **Pangakontod**. Kuvatakse jooksev saldo ja saate minna süvitsi kannetesse, millest see koondsaldo summa koosneb. Summa **Vahekonto kanded** võimaldab minna süvitsi kannetesse, millest see koondsumma koosneb. Vahekonto kanded on kõik ootel kanded, mis on funktsiooni Vahekonto abil sisestatud, kuid mida pole veel sobivaks märgitud. Summa **Ootel saldo** on jooksev saldo, millest on lahutatud vahekonto kanded või ootel kanded.

See kaart näitab ka pangakonto viimase vastavusseviimise aega. See teave kuvatakse ainult juhul, kui pangakontol on täpsem panga vastavusseviimine lubatud.

### <a name="balance"></a>Saldo

Diagramm **Saldo** näitab varasemat saldoteavet jaotises **Pangakontod** valitud pangakonto kohta või varasemat saldoteavet kõigi juriidilise isiku pangakontode kohta. See teave on saadaval mitmesuguste perioodide kohta: jooksev nädal, jooksev kuu, jooksev aasta, viimased viis aastat ja kõik perioodid (pangakonto täielik ajalugu). 

Kui vaatate diagrammi **Saldo** ühe pangakonto kohta, kuvatakse varasemad saldod pangakonto valuutas. Kui vaatate diagrammi kõigi juriidilise isiku pangakontode kohta, kuvatakse varasemad saldod arvestusvaluutas.

Teave andmete viimase uuendamise kohta kuvatakse diagrammi ülaosas. Andmeid saab vajalikul viisil uuendada.

### <a name="related-information"></a>Seostuv teave

Jaotisest **Seotud andmed** saab avada lehe **Päevaraamat** pangaülekannete tegemiseks. Saate avada kiiresti ka lehti **Pangakanded** ja **Vahekonto kanded**.

## <a name="analytics-view"></a>Analüüsivaade

Lehel **Analüüs** on olulised mõõdikud pangakontode kohta praeguses ettevõttes. Lehel on saadaval järgmised visualisatsioonid.

-   Kogu pangasaldo süsteemi valuutas
-   Saldo juriidilise isiku järgi
-   Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas
-   Saldo pangakonto järgi
-   Saldo valuuta järgi

Pangaanalüüsi saab vaadata kõigi ettevõtete lõikes tööruumis **Kassa ülevaade – kõik ettevõtted**.

