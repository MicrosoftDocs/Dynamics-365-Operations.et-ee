---
title: Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine
description: See artikkel kirjeldab, kuidas hallata Dynamics 365 Finance’i elektroonilise aruandluse (ER) konfiguratsioonide töötsüklit.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337262"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas hallata [Dynamics](general-electronic-reporting.md) 365 Finance’i elektroonilise aruandluse (ER) [konfiguratsioonide](general-electronic-reporting.md#Configuration) töötsüklit.

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
Järgmistel ER-iga seotud põhjustel soovitame teil kujundada ER konfiguratsioone arenduskeskkonnas eraldi finantside ja toimingute eksemplarina:

- Kasutajad rollis **Elektroonilise aruandluse arendaja** või rollis **Elektroonilise aruandluse funktsionaalne konsultant** saavad konfiguratsioone redigeerida ja neid testimise eesmärgil käitada. See stsenaarium võib põhjustada klasside ja tabelite meetodite kasutamise, mis võivad kahjustada äriandmeid ja eksemplari toimimist.
- Klasside ja tabelite meetodite kasutamine ER-i konfiguratsioonide ER-i andmeallikatena ei ole piiratud sisestuspunktide ja logitud ettevõtte sisuga. Seega pääsevad äriliselt tundlike andmete juurde kasutajad rolliga **Elektroonilise aruandluse arendaja** või **Elektroonilise aruandluse funktsionaalne konsultant**.

Arenduskeskkonnas kujundatud ER-i konfiguratsioone saab [üles laadida](#data-persistence-consideration) testkeskkonda, et hinnata konfiguratsiooni (õige protsessi integreerimine, tulemuste õigsus ja jõudlus) ja kvaliteedi tagamiseks, nt rolli juhitud juurdepääsuõiguste õigsus ja kohustuste jagamine. Selleks saab kasutada funktsioone, mis lubavad ER-i konfiguratsiooni vahetamise. Tõestatud ER-i konfiguratsioonid saab üles laadida LCS-i, kus neid saab teenuse tellijatega jagada, või neid [importida](#data-persistence-consideration) tootmiskeskkonda ettevõttesiseseks kasutamiseks.

![ER-i konfiguratsiooni elutsükkel.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Andmete püsivuse kaalutlus

ER-konfiguratsioonist [saate](tasks/er-import-configuration-lifecycle-services.md) eraldi finantseksemplari [importida](general-electronic-reporting.md#Configuration). ER-konfiguratsiooni uue versiooni importimisel kontrollib süsteem selle konfiguratsiooni mustandi versiooni sisu.

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

## <a name="dependencies-on-other-components"></a>Sõltuvused teistest komponentidest

ER-i konfiguratsioone saab konfigureerida muudest [konfiguratsioonidest](er-download-configurations-global-repo.md#import-filtered-configurations) sõltuvana. Näiteks saate [globaalsest hoidlast importida ER-andmemudeli](er-download-configurations-global-repo.md)[konfiguratsiooni](er-overview-components.md#data-model-component) oma Microsoft Regulatory Configuration Services (RCS) [või Dynamics 365 Finance eksemplari ja seejärel luua imporditud ER-andmemudeli konfiguratsioonist tuletatud ER-vormingu](../../../finance/localizations/rcs-overview.md)[...](er-overview-components.md#format-component)[konfiguratsiooni.](er-quick-start2-customize-report.md#DeriveProvidedFormat) Tuletatud ER-vormingu konfiguratsioon sõltub ER-i põhiandmemudeli konfiguratsioonist.

![Tuletatud ER-vormingu konfiguratsioon lehel Konfiguratsioonid.](./media/ger-configuration-lifecycle-img1.png)

Kui olete vormingu kujundamise lõpetanud, saate muuta ER-vormingu konfiguratsiooni algse versiooni oleku olekust Mustand **olekusse** Lõpetatud **·**. Seejärel saate jagada ER-vormingu konfiguratsiooni lõpetatud versiooni, avaldades [selle](../../../finance/localizations/rcs-global-repo-upload.md) globaalses hoidlas. Seejärel pääsete globaalsele hoidlale juurde mis tahes RCS-i või finantsi pilve eksemplarist. Seejärel saate importida mis tahes ER-i konfiguratsiooni versiooni, mida saab rakendusele globaalsest hoidlast sellesse rakendusse importida.

![Avaldatud ER-vormingu konfiguratsioon konfiguratsioonihoidla lehel.](./media/ger-configuration-lifecycle-img2.png)

Konfiguratsioonisõltuvuse põhjal, kui valite globaalses hoidlas ER-vormingu konfiguratsiooni selle importimiseks vast juurutatud RCS-i või finantseksemplari, leitakse ER-i põhiandmemudeli konfiguratsioon automaatselt globaalsest hoidlast ja imporditakse koos valitud ER-vormingu konfiguratsiooniga põhikonfiguratsioonina.

Samuti saate eksportida oma ER-vormingu konfiguratsiooniversiooni oma praegusest RCS-i või Finantside eksemplarist ning salvestada selle kohalikult XML-failina.

![ER-vormingu konfiguratsiooniversiooni eksportimine XML-ina konfiguratsioonilehel.](./media/ger-configuration-lifecycle-img3.png)

**Kui proovite enne versiooni 10.0.29** finantside versiooni importida ER-i vormingu konfiguratsiooniversiooni sellest XML-failist või mis tahes muust hoidlast mõnda muusse hoidlasse, mis on juurutatud RCS-i või finantseksemplari, mis ei sisalda veel ER konfiguratsioone, ilmneb järgmine erand, mis teavitab teid, et baaskonfiguratsiooni ei ole võimalik saada:

> Järelejäänud lahendamata viiteid<br>
Objekti "Alus\<imported configuration name\>" (,\<globally unique identifier of the missed base configuration\>) viidet\<version of the missed base configuration\> ei saa luua

![ER-vormingu konfiguratsiooniversiooni importimine konfiguratsioonihoidla lehele.](./media/ger-configuration-lifecycle-img4.gif)

**Versioonis 10.0.29** ja uuemas versioonis proovite teha sama konfiguratsiooni importimist, kui praeguses rakenduse eksemplaris või lähtehoidlas, mida praegu kasutate (kui see on olemas), püüab ER framework automaatselt leida globaalsest hoidla vahemälust puuduva põhikonfiguratsiooni nime. Seejärel esitab see puuduva põhikonfiguratsiooni nime ja globaalselt kordumatu IDENTIFIKAATORi (GUID) erandi tekstis.

> Järelejäänud lahendamata viiteid<br>
Objekti "Alus\<imported configuration name\>" (,\<name of the missed base configuration\>) viidet\<globally unique identifier of the missed base configuration\>\<version of the missed base configuration\> ei saa luua

![Konfiguratsioonihoidla lehel ilmnes erand, kui põhikonfiguratsiooni ei leita.](./media/ger-configuration-lifecycle-img5.png)

Antud nime saate kasutada põhikonfiguratsiooni otsimiseks ja seejärel käsitsi importimiseks.

> [!NOTE]
> See uus [valik](er-download-configurations-global-repo.md#open-configurations-repository)[töötab](er-extended-format-lookup.md) ainult siis, kui vähemalt üks kasutaja on juba globaalsesse hoidlasse sisse loginud, kasutades konfiguratsioonihoidlate lehte või üht globaalse hoidla otsinguvälja praeguses finantseksemplaris ja kui globaalse hoidla sisu on vahemällu salvestatud.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[ER-i konfiguratsioonide sõltuvuse määramine teistest komponentidest](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

