---
title: Inimressursside linkide loomine teise keskkonda
description: See teema kirjeldab, kuidas luua Microsoftilt teisele Dynamics 365 Human Resources Dynamics 365 keskkonnale linki.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d20eef4b4861d85ead1d47ca493c3a5c2d2d85e8
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712784"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Inimressurssidest teise finantskeskkonna linkide loomine

Kliendil võib olla kaks Dynamics 365 keskkonda, kus nad töötavad. Näiteks võib kliendil olla keskkond Finantside Dynamics 365 Human Resources infrastruktuuris ja peab ühenduma teise Dynamics 365 Finance keskkonnaga. 

See funktsioon lubab linke inimressursside leheküljelt konkreetsele lehele teises finantskeskkonnas. Kui lingid on konfigureeritud, saate määrata, kus link on Inimressurssides saadaval, ja sihtlehe, mis avatakse teises keskkonnas.

> [!Note] 
> Selle funktsiooni saamiseks peate **lülitama sisse inimressursside kasutajakogemuse** täiustused **funktsioonihalduses**.

## <a name="configure-target-systems"></a>Sihtsüsteemide konfigureerimine

Inimressurssides saavad süsteemi administraatorid määrata lingid, mis on inimressursside lehtedel **pinnaks**. Konfiguratsiooni osad on finantskeskkonnad, milleni soovite navigeerida lingi sihina. 

Sihtsüsteemi konfigureerimiseks:
1. Valige lehel **Linkide** konfigureerimine suvand **Konfigureeri sihtsüsteem**.  
2. Sisestage sihtsüsteemi nimi ja sisestage finantskeskkonna URL. Pärast sihtsüsteemide konfigureerimist saate määratleda oma lingid.

## <a name="configure-links"></a>Konfigureeri lingid

Igal teie poolt valitud lingil on määratud järgmine teave:
 - **Link**: lingi nimi. Kasutatakse ainult tuvastamiseks.
 - **Lubage see link**: määrake väärtusele **Jah**, kui soovite kuvada lingi Inimressursside kasutajatele.
 - **Kuvatav** nimi: sisestage nimi, mis kuvatakse seosena teisese keskkonnaga. 
 - **Surface'i link vormil**: valige, mis lehel soovite linki kuvada. Linke saab pinnaks teha ainult Töötaja **iseteeninduse** tööruumil ning **töö**, **positsiooni**, töötaja **ja** sujuvamaks **töötaja lehtedel**.
 - **Grupp** – saate oma linke korraldada gruppide abil. Valige olemasolev grupp või looge uus, kasutades veergu **Grupp**.
 - **Sihtsüsteem**: valige sihtsüsteem, mis loodi sihtsüsteemi valiku **konfigureerimisel**. See on teisene keskkond, mida kasutatakse lingil navigeerimisel.
 - **Kasutage kasutaja praegust ettevõtet**: valige **Jah,** et kasutada kasutaja praegust ettevõtet finantsis navigeerides. Valige **Ei**, et valida kasutatav ettevõte.
 - **Sihtmenüü** üksus: sisestage finantskeskkonnast menüükäsk, mida link peaks navigeerimise ajal kasutama. Otse navigeeritavad menüü-üksused ei ole saadaval. 

   Nõutava menüükäsu leidmiseks:
   1. Minge finantskeskkonda ja avage leht, mis on navigeerimise sihtmärk. 
   2. Kopeerige menüü-üksus URL-ist. Kui soovite näiteks, et link viiks teid töövõtjate loendisse Finance ja Operationsis, sisestage väärtus, mis kuvatakse URL-is pärast "&mi"-d. 
   3. Töövõtja loendi lehele navigeerimise menüü-üksus on selles näites: HcmWorkerListPage_Employees.

 - **Link andmeallikale**: valige andmeallikas, millele link viitab. Saadaval on kõige tavalisemad allikad nagu **Töötaja** ja **Ametikoht**.

### <a name="access-to-links"></a>Juurdepääs linkidele

Süsteemiadministraatorid näevad vastloodud linke määratletud lehtedel isegi siis, kui **Lingi lubamise** suvandiks on määratud **Ei**. Seda saab kasutada linkide kontrollimiseks enne nende ilmutamist teistele töövõtjatele. Kõik teised rollid näevad ainult konfigureeritud linke, kui suvandi **Luba see link** väärtuseks on määratud **Jah**. Töövõtjatel, kellel on juurdepääs lehekülgedele, kuhu lingid on ilmutatud, on juurdepääs ka linkidele.

Kasutajatel peavad olema turvaõigused teiseses keskkonnas määratletud juurdepääsuks selle keskkonna lehtedele. Kui õiguseid ei ole, kuvatakse lingi kasutamisel turva dialoogiboks.

