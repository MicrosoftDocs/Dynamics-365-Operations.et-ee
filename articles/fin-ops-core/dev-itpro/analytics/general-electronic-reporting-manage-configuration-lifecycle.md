---
title: Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine
description: See artikkel kirjeldab, kuidas hallata Dynamics 365 Finance'i elektroonilise aruandluse (ER) konfiguratsioonide töötsüklit.
author: NickSelin
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 0220fa03283119471b3d1f78a23a04ed4036264e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906793"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas hallata Dynamics 365 Finance'i elektroonilise aruandluse (ER) konfiguratsioonide töötsüklit.

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

    - Teisendage dokumendimall ER-i konfiguratsiooniks ja eksportige konfiguratsioon praegusest rakenduse eksemplarist XML-paketina, mille saab salvestada kohalikult või Lifecycle Services-i (LCS).
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

Arenduskeskkonnas kujundatud ER-i konfiguratsioone saab [üles laadida](#data-persistence-consideration) testkeskkonda, et hinnata konfiguratsiooni (õige protsessi integreerimine, tulemuste õigsus ja jõudlus) ja kvaliteedi tagamiseks, nt rolli juhitud juurdepääsuõiguste õigsus ja kohustuste jagamine. Selleks saab kasutada funktsioone, mis lubavad ER-i konfiguratsiooni vahetamise. Tõestatud ER-i konfiguratsioonid saab üles laadida LCS-i, kus neid saab teenuse tellijatega jagada, või neid [importida](#data-persistence-consideration) tootmiskeskkonda ettevõttesiseseks kasutamiseks.

![ER-i konfiguratsiooni elutsükkel.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Andmete püsivuse kaalutlus

ER-i [konfiguratsiooni](general-electronic-reporting.md#Configuration) [versioone](general-electronic-reporting.md#component-versioning) saate eraldi [importida](tasks/er-import-configuration-lifecycle-services.md)oma Finance'i instantsile. ER-konfiguratsiooni uue versiooni importimisel kontrollib süsteem selle konfiguratsiooni mustandi versiooni sisu.

- Kui imporditud versioon on praeguse Finance instantsi selle konfiguratsiooni kõrgeimast versioonist madalam, jääb selle konfiguratsiooni mustandi versiooni sisu samaks.
- Kui imporditud versioon on praeguse Finance instantsi selle konfiguratsiooni mis tahes muust versioonist kõrgem, kopeeritakse imporditud versiooni sisu selle konfiguratsiooni mustandiversiooni, et saate jätkata viimati lõpetatud versiooni redigeerimist.

Kui see konfiguratsioon kuulub praegu aktiveeritud konfiguratsiooni [pakkujale](general-electronic-reporting.md#Provider), on selle konfiguratsiooni mustandversioon teile nähtav **lehe Konfiguratsioonid** kiirkaardil **Versioonid** (**Organisatsiooni administreerimine** > **Elektroonne aruandlus** > **Konfiguratsioonid**). Saate valida konfiguratsiooni mustandiversioon ja selle sisu [muuta](er-quick-start2-customize-report.md#ConfigureDerivedFormat) kasutades vastavat ER-i kujundajat. Kui olete redigeerinud ER-i konfiguratsiooni mustandversiooni, ei vasta selle sisu enam selle konfiguratsiooni kõrgeima versiooni sisule praeguses Finance instantsis. Muudatuste kaotsimineku vältimiseks kuvab süsteem tõrke, et importimine ei saa jätkuda, kuna selle konfiguratsiooni versioon on praeguse Finance instantsi selle konfiguratsiooni kõrgeimast versioonist kõrgem. Kui see juhtub, näiteks vormingu konfiguratsiooni **X** puhul, kuvatakse **vormingu "X" versioon ei ole lõpule viidud** tõrge.

Mustandiversioonis tehtud muudatuste tagasivõtmiseks valige kiirkaardil **Versioonid** oma ER-konfiguratsiooni kõrgeim lõpetatud või ühiskasutusega versioon rahanduses ja seejärel valige suvand **Hangi see versioon**. Valitud versiooni sisu kopeeritakse mustandversiooni.

## <a name="applicability-consideration"></a>Kohaldatavuse kaalumine

Kui kujundate ER-konfiguratsiooni uut versiooni, saate määrata selle [sõltuvuse](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) teistest tarkvarakomponentidest. Seda toimingut peetakse eeltingimuseks konfiguratsiooni versiooni allalaadimise kontrollimiseks ER-i hoidlast või välist XML -faili ja selle versiooni edasiseks kasutamiseks. Kui proovite importida ER-i konfiguratsiooni uut versiooni, kasutab süsteem konfigureeritud eeltingimusi versiooni importimise otstarbel.

Mõnel juhul võite nõuda, et süsteem ignoreeriks konfigureeritud eeltingimusi ER-i konfiguratsioonide uute versioonide importimisel. Et süsteem ignoreeriks importimise ajal eeltingimusi, järgige neid samme.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.
3. Seadke valiku **Jäta toote värskendused ja versiooni eeltingimuse kontroll importimise ajal vahele** valikule **Jah**.

    > [!NOTE]
    > See parameeter on kasutajakohane ja ettevõttekohane.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[ER-i konfiguratsioonide sõltuvuse määramine teistest komponentidest](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
