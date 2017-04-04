---
title: "Elektroonilise aruandluse konfiguratsiooni elutsükli haldamine"
description: "See teema käsitleb elektroonilise aruandluse (ER) koosseisudesse toimingute lahendus Microsoft Dynamics 365 elutsükli haldamist."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: f4d8994f6548119789715a4879b6bc02d25598e9
ms.lasthandoff: 03/31/2017


---

# <a name="manage-the-electronic-reporting-configuration-lifecycle"></a>Elektroonilise aruandluse konfiguratsiooni elutsükli haldamine

See teema käsitleb elektroonilise aruandluse (ER) koosseisudesse toimingute lahendus Microsoft Dynamics 365 elutsükli haldamist.

<a name="overview"></a>Ülevaade
--------

Elektrooniline aruandlus (ER) on mootor seadusega kehtestatud ja riigipõhiste elektrooniliste dokumentide toetamiseks Microsoft Dynamics 365 for Operationsis. Üldjuhul eeldab ER võimalust teha üksiku elektroonilise dokumendi puhul järgmisi toiminguid. Üksikasjalikumat, Vaata [elektroonilise aruandluse ülevaade](general-electronic-reporting.md).

-   Elektroonilise dokumendi malli kujundamine.
    -   Tuvastage nõutavad andmeallikad, mida saab dokumendis esitada:
        -   Aluseks Dynamics 365 operatsioonide andmeid nt andmetabelid, andmete üksuste ja klassid.
        -   Protsessipõhised omadused, näiteks täitmise kuupäeva, kellaaja ja ajavööndi.
        -   Kasutaja parameetrid, määratud lõppkasutaja käitusajal.
    -   Määratlege vajalikud dokumendielemendid ja nende topoloogia lõppdokumendi vormingu määramiseks.
    -   Konfigureerige soovitud andmevoog valitud andmeallikatest määratletud dokumendielementidele (andmeallika sidumiste kaudu dokumendivormingu komponentidega) ja määrake protsessi juhtimisloogika.
-   Tehke mall kättesaadavaks, et seda saaks teistes Dynamics 365 for Operationsi eksemplarides kasutada.
    -   Teisendage Dynamics 365 for Operationsis loodud dokumendimall ER-i konfiguratsiooniks ja eksportige konfiguratsioon praegusest Dynamics 365 for Operationsi eksemplarist XML-paketina, mille saab salvestada kohalikult või LCS-i.
    -   Teisendage ER-i konfiguratsioon Dynamics 365 for Operationsi dokumendimalliks.
    -   Importige kohalikult või LCS-i salvestatud XML-pakett praegusesse Dynamics 365 for Operationsi eksemplari.
-   Kohandage elektroonilise dokumendi malli.
    -   Tooge mall LCS-ist praegusesse Dynamics 365 for Operationsi eksemplari ER-i konfiguratsioonina.
    -   Kujundage ER-i konfiguratsioonist kohandatud versioon ja säilitage viide selle alusversioonile.
-   Integreerige mall konkreetse äriprotsessiga, nii et see oleks Dynamics 365 for Operationsis saadaval.
    -   Konfigureerige sätted nii, et Dynamics 365 for Operations hakkaks kasutama ER-i konfiguratsiooni, viidates sellele konfiguratsioonile protsessiga seotud parameetris. Näiteks vaadake ER konfiguratsiooni konkreetse kontode maksta makse meetod, et tekitada elektrooniline sõnum arvete töötlemiseks.
-   Kasutage malli kindlas äriprotsessis.
    -   ER konfiguratsiooni sõidetud konkreetse äriprotsessi. Näiteks elektroonilise makse sõnumi töötlemise arvete maksmise viis, mis viitab ER konfiguratsiooni loomiseks valitud.

## <a name="concepts"></a>Mõisted
Järgmisi rolle ja nendega seotud tegevus on seotud ER konfiguratsiooni elutsükli.

| Roll                                       | Tegevused                                                      | Kirjeldus                                                                                                                                                                                                                  |
|--------------------------------------------|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Elektroonilise aruandluse funktsionaalne konsultant | Looge ja hallake ER-i komponente (mudeleid ja vorminguid).           | Ärimees, kes projekteerib ER Domeen – andmete mudelid, tööstusdisainilahendused vaja malle elektrooniliste dokumentide ja seob neid vastavalt.                                                                           |
| Elektroonilise aruandluse arendaja             | Looge ja hallake andmemudeli vastendusi.                          | Dynamics 365 toimingute spetsialist, kes valib vajalikud Dynamics 365 toimingute andmeallikaid ja seondub ER Domeen – andmete mudelid.                                                                 |
| Raamatupidaja                      | Konfigureerige ER-i parasiitidele viitavaid protsessiga seotud sätteid. | Näiteks on **raamatupidamise juhendaja** rolli, mis võimaldab luua elektrooniline sõnum arvete töötlemiseks kasutada teatud kontode maksta makseviisi ER konfiguratsiooni seaded. |
| Ostureskontro maksuametnik            | Kasutage ER-i parasiite kindlas äriprotsessis.                | Näiteks on **kontodele makstavad maksed sekretär** rolli, mis võimaldab elektrooniliste maksete sõnumite töötlemine arvete puhul genereeritakse põhineb konkreetse makseviisi jaoks seadistatud ER vormi.           |

## <a name="er-configuration-development-lifecycle"></a>ER-i konfiguratsiooni arenduse elutsükkel
Järgmistel ER-iga seotud põhjustel soovitame kujundada ER-i konfiguratsioonid arenduskeskkonnas eraldi Dynamics 365 for Operationsi eksemplarina.

-   Kasutajad rollis **Elektroonilise aruandluse arendaja** või rollis **Elektroonilise aruandluse funktsionaalne konsultant** saavad konfiguratsioone redigeerida ja neid testimise eesmärgil käitada. See stsenaarium võib põhjustada klasside ja tabelite meetodite kasutamise, mis võivad kahjustada äriandmeid ning Dynamics 365 for Operationsi eksemplari toimimist.
-   Klasside ja tabelite meetodite kasutamine ER-i konfiguratsioonide ER-i andmeallikatena ei ole piiratud Dynamics 365 for Operationsi sisestuspunktide ja logitud ettevõtte sisuga. Seega pääsevad äriliselt tundlike andmete juurde kasutajad rolliga **Elektroonilise aruandluse arendaja** või **Elektroonilise aruandluse funktsionaalne konsultant**.

ER konfiguratsioonid, mis on loodud arenduskeskkonnas saate üles laadida et keskkond konfiguratsiooni hindamiseks (õige protsessi integreerimine, tulemuste ja tulemuslikkuse õigsust) ja kvaliteedi tagamise rolli juhitud juurdepääsuõigused õigsuse ja ülesannete jaotus. Selleks saab kasutada funktsioone, mis võimaldavad ER konfiguratsiooni vahetus. Lõpuks tõestatud ER konfiguratsioone saab üles laadida LCS, kus nad saavad jagada tellijatele, ega tootmiskeskkonda sisekasutuseks, nagu näidatud järgmisel joonisel. ![ER konfiguratsiooni elutsükli](./media/ger-configuration-lifecycle.png)

<a name="see-also"></a>Vt ka
--------

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)


