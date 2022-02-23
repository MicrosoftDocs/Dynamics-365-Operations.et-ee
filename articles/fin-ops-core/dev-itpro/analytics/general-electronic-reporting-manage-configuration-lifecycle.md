---
title: Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine
description: Selles teemas kirjeldatakse, kuidas hallata Microsoft Dynamics 365 Finance'i lahenduse elektroonilise aruandluse (ER) konfiguratsioonide elutsüklit.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a4741784103817c270c4c7f730753ba59a327d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682619"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas hallata Microsoft Dynamics 365 Finance'i lahenduse elektroonilise aruandluse (ER) konfiguratsioonide elutsüklit.

## <a name="overview"></a>Ülevaade

Elektrooniline aruandlus (ER) on mootor seadusega kehtestatud ja riigipõhiste elektrooniliste dokumentide toetamiseks. Üldjuhul eeldab ER võimalust teha üksiku elektroonilise dokumendi puhul järgmisi toiminguid. Lisateavet leiate jaotisest [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md).

- Elektroonilise dokumendi malli kujundamine.

    - Tuvastage nõutavad andmeallikad, mida saab dokumendis esitada:

        - Alusandmed, nt andmetabelid, andmeüksused ja klassid.
        - protsessipõhised atribuudid, nt käivitamise kuupäev ja kellaaeg ning ajatsoon;
        - kasutaja sisendparameetrid, mille määrab lõppkasutaja käitamisel.

    - Määratlege vajalikud dokumendielemendid ja nende topoloogia lõppdokumendi vormingu määramiseks.
    - Konfigureerige soovitud andmevoog valitud andmeallikatest määratletud dokumendielementidele (andmeallika sidumiste kaudu dokumendivormingu komponentidega) ja määrake protsessi juhtimisloogika.

- Tehke mall kättesaadavaks, et seda saaks teistes eksemplarides kasutada.

    - Teisendage dokumendimall ER-i konfiguratsiooniks ja eksportige konfiguratsioon praegusest rakenduse eksemplarist XML-paketina, mille saab salvestada kohalikult või LCS-i.
    - Teisendage ER-i konfiguratsioon rakenduse dokumendimalliks.
    - Importige kohalikult või LCS-i salvestatud XML-pakett praegusesse eksemplari.

- Kohandage elektroonilise dokumendi malli.

    - Tooge mall LCS-ist praegusesse eksemplari ER-i konfiguratsioonina.
    - Kujundage ER-i konfiguratsioonist kohandatud versioon ja säilitage viide selle alusversioonile.

- Integreerige mall konkreetse äriprotsessiga, nii et see oleks rakenduses saadaval.

    - Konfigureerige sätted nii, et rakendus hakkaks kasutama ER-i konfiguratsiooni, viidates sellele konfiguratsioonile protsessiga seotud parameetris. Näiteks viidake ER-i konfiguratsioonile konkreetses ostureskontro makseviisis, et luua arvete töötlemiseks elektrooniline maksesõnum.

- Kasutage malli kindlas äriprotsessis.

    - Käivitage ER-i konfiguratsioon konkreetses äriprotsessis. Näiteks elektroonilise maksesõnumi loomiseks arvete töötlemiseks, kui on valitud ER-i konfiguratsioonile viitav makseviis.

## <a name="concepts"></a>Mõisted
ER-i konfiguratsiooni elutsükliga on seotud järgmised rollid ja seotud tegevused.

| Roll                                       | Tegevused                                                      | Kirjeldus |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Elektroonilise aruandluse funktsionaalne konsultant | Looge ja hallake ER-i komponente (mudeleid ja vorminguid).           | Äriinimene, kes ER-i domeenipõhised andmemudelid kujundab, kujundab vajalikud elektrooniliste dokumentide mallid ja seob need vastavalt. |
| Elektroonilise aruandluse arendaja             | Looge ja hallake andmemudeli vastendusi.                          | Spetsialist, kes valib vajalikud Finance'i andmeallikad ja seob need ER-i domeenipõhiste andmemudelitega. |
| Raamatupidaja                      | Konfigureerige ER-i parasiitidele viitavaid protsessiga seotud sätteid. | Näiteks roll **Raamatupidaja**, mis võimaldab ER-i konfiguratsiooni sätete kasutamist konkreetses ostureskontro makseviisis arvete töötlemiseks vajaliku elektroonilise maksesõnumi koostamiseks. |
| Ostureskontro maksuametnik            | Kasutage ER-i parasiite kindlas äriprotsessis.                | Näiteks roll **Ostureskontro maksuametnik**, mis võimaldab elektrooniliste maksesõnumite koostamist arvete töötlemiseks, tuginedes konkreetse makseviisi jaoks konfigureeritud ER-i vormingule. |

## <a name="er-configuration-development-lifecycle"></a>ER-i konfiguratsiooni arenduse elutsükkel
Järgmistel ER-iga seotud põhjustel soovitame kujundada ER-i konfiguratsioonid arenduskeskkonnas eraldi Finance and Operationsi eksemplarina.

- Kasutajad rollis **Elektroonilise aruandluse arendaja** või rollis **Elektroonilise aruandluse funktsionaalne konsultant** saavad konfiguratsioone redigeerida ja neid testimise eesmärgil käitada. See stsenaarium võib põhjustada klasside ja tabelite meetodite kasutamise, mis võivad kahjustada äriandmeid ja eksemplari toimimist.
- Klasside ja tabelite meetodite kasutamine ER-i konfiguratsioonide ER-i andmeallikatena ei ole piiratud sisestuspunktide ja logitud ettevõtte sisuga. Seega pääsevad äriliselt tundlike andmete juurde kasutajad rolliga **Elektroonilise aruandluse arendaja** või **Elektroonilise aruandluse funktsionaalne konsultant**.

Arenduskeskkonnas kujundatud ER-i konfiguratsioone saab üles laadida testkeskkonda, et hinnata konfiguratsiooni (õige protsessi integreerimine, tulemuste õigsus ja jõudlus) ja kvaliteedi tagamiseks, nt rolli juhitud juurdepääsuõiguste õigsus ja kohustuste jagamine. Selleks saab kasutada funktsioone, mis lubavad ER-i konfiguratsiooni vahetamise. Lõpuks saab tõestatud ER-i konfiguratsioonid üles laadida kas LCS-i, kus neid saab teenuse tellijatega jagada, või tootmiskeskkonda ettevõttesiseseks kasutamiseks, nt nii, nagu on näidatud järgmisel joonisel.

![ER-i konfiguratsiooni elutsükkel](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)
