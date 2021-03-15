---
title: Puudumiste registreerimine jaotises Tööajaarvestus
description: Teema kirjeldab, kuidas hallata puudumiste registreerimisi jaotises Tööajaarvestus.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12a61f23ac5a16000275e53d3901c8aea202bab0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966626"
---
# <a name="absence-registration-in-time-and-attendance"></a>Puudumiste registreerimine jaotises Tööajaarvestus

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse puudumise mõisteid ja selgitatakse, kuidas käsitleda puudumisi jaotises Tööajaarvestus.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Puudumine, mis põhineb tavapärastel töötundidel

Puudumiseks peetakse aega, mille jooksul töötajad tavapärase tööaja jooksul tööd ei tee. Tavapärane tööaeg on määratud töötaja standardses tööajareeglis.

Näiteks on töötajal päevapõhine reegel, mis hõlmab sisseregistreerimist kell 07:00 ja väljaregistreerimist kell 15:00. Kui töötaja registreerub sisse kell 09:00, märgitakse ta sel päeval vahemikus 07:00–09:00 puudunuks.

Sel juhul palutakse töötajatel sisestada puudumise põhjus. Põhjuse määramiseks saavad töötajad valida puudumiskoodi.

## <a name="absence-codes"></a>Puudumiste koodid

Puudumiskoodid määratlevad mitmesugust tüüpi puudumisi. Puudumiskoodid määrab ettevõte.

Puudumiskoodidele saab rakendada mitmesuguseid reegleid. Näiteks saab konfigureerida puudumiskoodi nii, et see vähendaks või suurendaks palka.

Näiteks määratleb ettevõte puudumiskoodi **Hilinemine**, mida töötajad kasutavad põhjuseta hilinemise puhul. Ettevõte määratleb ka puudumiskoodi **Ettevõttesisene kursus**, millega töötajad märgivad ettevõttesisestel kursustel osalemisele kuluva aja. Puudumiskoodid saab seadistada nii, et koodi **Hilinemine** puhul vähendatakse töötaja tasu, ent koodi **Ettevõttesisene kursus** puhul mitte.

Saate seadistada automaatsed puudumiskoodid. Neid puudumiskoode saab kasutada töötaja aja arvutamiseks juhul, kui puudumist ei registreerita. Töötaja tööajareegel määrab, kas kasutatakse standard- või paindaja puudumiskoodi.

### <a name="set-up-standard-time-and-flex-time"></a>Standard- ja paindaja seadistamine

- Konfigureerige standard- ja paindaja parameetrid lehe **Tööajaarvestus** valikutega **Puudumise automaatne sisestamine** ja **Paindaja automaatne sisestamine**.

## <a name="absence-groups"></a>Puudumistegrupid

Puudumiskoodid rühmitatakse puudumisgruppidesse. Puudumisgrupid võimaldavad rühmitada sarnaste omadustega puudumiskoode. Näiteks võite rühmitada põhjusega puudumiste koodid või arsti juures käimise, vandekohtunikukohustuse ja lapse haigusega seotud puudumise koodid.

## <a name="planned-absence"></a>Planeeritud puudumine

Kui teate, et töötaja puudub konkreetse perioodi jooksul, näiteks puhkuse tõttu, võite kasutada planeeritud puudumist. Planeeritud puudumise seadistamiseks konfigureerige puudumiskood nii, et see võtaks arvesse planeeritud puudumist. Kui seadistate planeeritud puudumise, ei küsita teilt puudumise perioodi ajal kasutaja registreeritud tööaja arvestamisel puudumiskoodi. Planeeritud puudumise saab määratleda üksiku töötaja jaoks või määrata pakett-töö, mis võimaldab töötajate planeeritud puudumisi hulgi värskendada.

### <a name="set-up-planned-absence"></a>Planeeritud puudumise seadistamine

1. Valige **Inimressursid** &gt; **Töötajad** &gt; **Töövõtjad** ja seejärel valige töövõtja.
2. Valige **Aeg** &gt; **Ajamäärangud** &gt; **Puudumisaja registreerimine** ja seadistage planeeritud puudumine.

## <a name="interrupted-planned-absence"></a>Katkestatud plaanitud puudumine

Kui rakendate planeeritud puudumise seadistamisel suvandi **Katkesta** ja töötaja logib planeeritud puudumise perioodi jooksul sisse, siis planeeritud puudumine katkestatakse. Planeeritud puudumisele lisatakse märge **Katkestatud** ja see ei mõjuta tulevasi arvutusi.

### <a name="set-up-a-planned-absence-for-interruption"></a>Planeeritud puudumise katkestamise seadistamine

1. Avage leht **Puudumisaja registreerimine**, nagu on kirjeldatud planeeritud puudumise seadistamise protseduuris.
2. Valige suvand **Katkesta**.

Suvand **Katkesta** rakendub juhul, kui aeg registreeritakse tööde juhtimise terminalis või seadmes. Suvand ei kehti juhul, kui registreerimised sisestatakse arvutus- ja kinnituslehtedel või lehel **Elektrooniline kellakaart**.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Puudumise kasutamise näited paindreegli puhul

Järgmised kolm näidet selgitavad, kuidas arvutatakse puudumist paindperioode hõlmava reegli puhul.

Näited kasutavad järgmist reeglit.

| Sisseregistreerimine | Standardaeg    | Paus             | Standardaeg | Paind-        | Väljaregistreerimine | Paind+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 08:00     | 09:00–11:30 | 11.30–12.00 | 12.00–15.00 | 15.00–16.00 | 16.00      | 16.00–18.00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>1. näide: väljalogimine paindaja jooksul

Töötaja teeb sisseregistreerimise kell 08:00 ja väljaregistreerimise kell 15:30. Kuna töötaja teeb väljaregistreerimise paindaja miinusperioodi jooksul, ei arvutata sel juhul puudumist ning töötaja paindaja saldost lahutatakse pool tundi.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>2. näide: väljalogimine standardaja jooksul

Töötaja teeb sisseregistreerimise kell 08:00 ja väljaregistreerimise kell 14:30. Kuna töötaja teeb väljaregistreerumise standardajal, arvutatakse puudumine vahemikus 14.30–16.00 ja registreeritakse puudumisaeg 1,5 tundi. Perioodi puudumiskood on nõutav.

### <a name="example-3-signing-out-during-a-flex-period"></a>3. näide: väljalogimine paindaja plussperioodi jooksul

Töötaja teeb sisseregistreerimise kell 08:00 ja väljaregistreerimise kell 16:30. Kuna töötaja teeb väljaregistreerimise paindaja plussperioodi jooksul, ei arvutata sel juhul puudumist ning töötaja paindaja saldole lisatakse pool tundi.

## <a name="absence-in-the-calculation-and-approval-process"></a>Puudumine arvutamis- ja kinnitamisprotsessis

Töötaja registreeritud tööaeg tuleb arvutada ja kinnitada, enne kui selle saab tasuüksusena palgasüsteemi edastada.

Kinnitaja saab muuta töötaja registreeritud tööaega. Kinnitaja saab isegi muuta töötaja registreeritud puudumisi. Kui kinnitaja sisestab käsitsi puudumiskoodiga ajaperioodi, ei tühista tööajaarvestuse parameetrite vaikepuudumiskood selle perioodi puudumiskoodi.

Näiteks teeb töötaja sisseregistreerimise kell 10:00 ja valib puudumiskood, mis näitab, et ta jäi hiljaks. Hiljem teavitab töötaja juhatajat sellest, et ta käis 08:00–10:00 arsti juures. Arsti juures käimine ei peaks põhjustama töötaja palga vähendamist. Seetõttu võib juhataja sellisel juhul kaht puudutud tundi (08:00–10:00) muuta, sisestades käsitsi puudumiskoodi, mis viitab haigusele.

### <a name="calculate-and-approve-absence"></a>Puudumisaja arvutamine ja kinnitamine

- Valige **Tööajaarvestus** &gt; **Ülevaatamine ja kinnitamine** &gt; **Kinnitamine või arvutamine**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]