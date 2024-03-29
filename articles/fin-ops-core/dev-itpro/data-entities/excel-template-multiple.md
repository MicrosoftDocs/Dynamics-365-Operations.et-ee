---
title: Mitme töölehe andmemallid
description: See artikkel kirjeldab, kuidas importida andmeid Exceli andmeüksuse mallide abil finantsidesse ja toimingutesse.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: f0845b111afb18205677b885c91fe1585b24ab14
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108802"
---
# <a name="data-templates-with-multiple-worksheets"></a>Mitme töölehe andmemallid

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Andmehaldus rakenduses toetab andmeüksuste puhul Microsoft Exceli põhiseid malle. Need mallid võivad sisaldada üht või mitut töölehte. Mitme töölehega malle kasutatakse sageli siis, kui andmeid on mugav hallata ühes failis ja importida neid mitmesse andmeüksusse. Selleks näiteks oleks laoalad ja laod.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Faili üks kord üleslaadimine ja kõigi üksustega vastendamine
Oletame näiteks, et meil on üks Exceli fail koos töölehtedega **Laoalad** ja **Laod**. Andmete importimise projekti seadistamiseks lisate esimese andmeüksuse **Laoalad** ja seejärel laadite faili üles. Saate valida selle üksuse puhul töölehena kasutamiseks **Laoalad**.

Teise üksuse, **Laod**, lisamisel vormilt **Faili lisamine** lahkumata võimaldab töölehe otsing valida töölehe **Laod** jälle ilma faili üles laadimata. Ainus põhjus uue faili üleslaadimiseks oleks see, kui töölehe **Laod** andmed oleksid eraldi failis.

![Mitu töölehte.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Töölehe ja üksuse vastenduse fikseerimine

Töölehe vastenduse andmeüksusega imporditöös saab ruudustikust fikseerida. Ruudustiku veerus **Tööleht** kuvatakse vastendatud failist pärit töölehed. Saate valida ripploendist erinevaid töölehti. Kui valitud tööleht on mõne andmeprojekti üksusega juba vastendatud, palub süsteem teil muudatus kinnitada. Soovitame teil kõik vastendused ruudustikus fikseerida.

![Töölehe vastenduse värskendamine.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Uuesti vastendamine uue failiga

Juhul kui andmeprojekti olemasolevate üksuste puhul tuleb üles laadida sama faili uus versioon või täiesti uus fail, peate kasutama funktsiooni **Faili lisamine** ja üksused uuesti lisama, nagu teeksite seda esimest korda. Süsteem kinnitab teie soovi enne jätkamist andmeprojekti olemasolevad üksused üle kirjutada. Üksused, mida uuesti ei lisata (ülekirjutamiseks) säilitavad varasemad vasted eelmisest failist.

## <a name="upload-a-file-using-run-project"></a>Faili üleslaadimine suvandiga Projekti käivitamine

Impordiprojekti käivitamiseks saate Exceli faili üles laadida suvandiga **Projekti käivitamine**. Jälgige hoolikalt, et laadiksite üles ainult failid, millel on samad töölehed kui andmeprojekti andmeüksuste olemasolevatel vastendustel. Kui äsja üleslaaditud failist töölehte ei leita, kuvab süsteem tõrke ja peatab importimise. Kui mõne üksuse puhul tuleb töölehega vastendust muuta, tuleb vastendusi andmeprojektis kõigepealt andmeprojekti sees värskendada, enne kui kasutate faili funktsioonis **Projekti käivitamine**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

