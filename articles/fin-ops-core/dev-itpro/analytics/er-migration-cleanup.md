---
title: ER-i migratsiooni puhastamine
description: See artikkel selgitab, kuidas saate kasutada ER-i migreerimise puhastusfunktsiooni ER-i mallidega seotud probleemide lahendamiseks.
author: kfend
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: AX 8.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace, ERParameters, ERMigrationCleanup
ms.openlocfilehash: bf32981ed5f43647038018bf2cd98e55ce233b3f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285087"
---
# <a name="er-migration-cleanup"></a>ER-i migratsiooni puhastamine 

[!include[banner](../includes/banner.md)]

Kui haldate oma Finance'i eksemplare, võite valida praeguse eksemplari siirdamise teise asukohta. Näiteks võite oma tootmiseksemplari migreerida uude liivakastikeskkonda. Kui konfigureerisite elektroonilise aruandluse (ER) raamistiku talletama malle Microsoft Azure'i bloobimälus, viitab tabel **DocuValue** uues liivakastikeskkonnas bloobimälu eksemplarile tootmiskeskkonnas. Sellele eksemplarile ei pääse aga juurde liivakastikeskkonnast, sest migreerimisprotsess ei toeta artefaktide migreerimist bloobimälus. Selle asemel eeldatakse, et viitate uues liivakastikeskkonnas sellele liivakastikeskkonna bloobimälu eksemplarile, mis ei oma veel ER-malle.

Kui proovite käitada ER-vormingut, mis kasutab malli äridokumentide loomiseks, ilmneb erand ja teid teavitatakse puuduvast mallist. Samuti soovitatakse teil kasutada ER-puhastuse suvandit, et kustutada malli sisaldav ER-vormingu konfiguratsioon ja see seejärel uuesti importida.

[![ER-vormingu käitamine.](./media/er-migration-cleanup-run.png)](./media/er-migration-cleanup-run.png)

Sarnane tõrge tekib siis, kui liigute lehele **Konfiguratsioonid** (**Organisatsiooni haldus** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**) ja proovite konfiguratsioonipuus kustutada malli kasutava ER-vormingu konfiguratsiooni.

[![ER-vormingu kustutamine.](./media/er-migration-cleanup-delete.png)](./media/er-migration-cleanup-delete.png)

Ligipääsmatute ER-mallidega seotud probleemide lahendamiseks järgige järgmisi etappe.

1.  Avage leht **Organisatsiooni haldus** \> **Perioodiline** \> **Migratsiooni puhastus**.
2.  Valige ER-vormingu konfiguratsioon, mida ei saa käitada ega kustutada.
3.  Valige **Kustuta**.
4.  Kinnitage valitud ER-vormingu konfiguratsiooni kustutamine.
5.  [Importige](download-electronic-reporting-configuration-lcs.md) kustutatud ER-vormingu konfiguratsioon praegusesse Finance'i eksemplari.

## <a name="applicability"></a>Kohaldatavus

> [Oluline] Suvand **Migratsiooni puhastamine** on suunatud vaid sellistele ER-vormingu konfiguratsioonidele, mis sisaldavad ligipääsmatuid ER-vorminguid. Kui kustutate suvandi **Migratsiooni puhastus** abil ER-vormingu konfiguratsiooni, siis kustutab elektrooniline aruandlus konfiguratsiooni artefaktidega seotud mallid ainult rakenduse andmebaasis. Vastavate füüsiliste failide olemasolu bloobimälus ei kontrollita. Eeldatakse, et ühtki sellist faili ei eksisteeri. Seega ei tohiks kasutada suvandit **Migratsiooni puhastus** lehe **Konfiguratsioonid** toodud ER-i konfiguratsiooni kustutamise suvandi alternatiivina. Kasutage suvandit **Migratsiooni puhastus** vaid siis, kui lehel **Konfiguratsioonid** toodud ER-i konfiguratsiooni kustutamise suvandi kasutamine nurjus.
>
> Kui kustutate suvandi **Migratsiooni puhastus** abil ER-vormingu konfiguratsiooni olukorras, kus viidatud mall on bloobimälus saadaval, siis kustutate ainult seotud konfiguratsiooni artefaktid rakenduse andmebaasis. Malli füüsiline fail bloobimälus jääb alles. Faili ülekirjutamine bloobimälus ei ole enam lubatud. Lisateavet vt [KB4557217](https://fix.lcs.dynamics.com/Issue/Details?kb=4557217). Lisaks ei saa te selles keskkonnas migratsiooni puhastust kasutades kustutatud konfiguratsioone enam uuesti importida. Probleemi lahendamiseks peate vastava faili bloobimälus käsitsi tuvastama ja kustutama.

[![ER-vormingu importimine.](./media/er-migration-cleanup-import.png)](./media/er-migration-cleanup-import.png)

Sarnane probleem võib tekkida juhul, kui migreerite oma rakenduse eksemplari muude asukohta, mida on kasutatud migratsiooni sihtkohana enam kui üks kord ning mille kohta on bloobimälus juba ER-malli failid olemas.

Kuna teil võib olla mitu ER-vormingu konfiguratsiooni, võib see protsess olla aeganõudev. Seega tuleks katkiste viidetega mallide automaatseks taastamiseks eelistada [ER-mallide varundusfunktsiooni](er-backup-storage-templates.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
