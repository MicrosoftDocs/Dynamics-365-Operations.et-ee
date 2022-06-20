---
title: Operatsioonide planeerimine
description: See artikkel annab teavet operatsioonide planeerimise kohta. Operatsioonide plaanimine võimaldab anda tootmisprotsessi kohta üldise hinnangu aja jooksul.
author: johanhoffmann
ms.date: 06/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdSchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 198073
ms.assetid: 12c28b11-80aa-4668-b15b-724cb24890bd
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b9ae31b288831d2f3b85bf1996206221e0bdbbd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871887"
---
# <a name="operations-scheduling"></a>Operatsioonide planeerimine

[!include [banner](../includes/banner.md)]

See artikkel annab teavet operatsioonide planeerimise kohta. Operatsioonide plaanimine võimaldab anda tootmisprotsessi kohta üldise hinnangu aja jooksul.

Saate plaanida tootmist operatsiooni ja töö tasandil. Erinevalt tööde plaanimisest ei tükelda operatsioonide plaanimine tootmisprotsessi operatsioone töödeks. Kui soovite kaasata plaanimisse rohkem üksikasju, näiteks teavet praeguse võimsuse kohta, saate käivitada tööde plaanimise pärast operatsioonide plaanimise käivitamist. Saate käivitada ka ainult tööde plaanimise. Tööde plaanimist kasutatakse tavaliselt üksikute tööde plaanimiseks tööde juhtimise moodulis kohe või lühikese ajavahemiku jooksul.

## <a name="components-of-operations-scheduling"></a>Operatsioonide plaanimise komponendid
Operatsioonide plaanimise põhikomponendid on plaanimissuund, ressursside võimsus ja materjali optimeerimine. Operatsioonide plaanimist kasutades on võimalik saavutada järgmised eesmärgid.

-   Plaanimismeetodi juhtimine, plaanides antud kuupäevast edasi või tagasi.
-   Ressursside optimeerimine, plaanides tootmisi ressursside võimsuse alusel. See lähenemisviis aitab välja selgitada ka selle, kui kasutada tuleks alternatiivseid ressursse.
-   Materjalide kasutuse optimeerimine, plaanides tootmisi nõutavate materjalide saadavuse alusel.
-   Viitetootmiste plaanimine ja sünkroonimine. Viitetootmiste kuupäevi korrigeeritakse tootmistellimuse plaani muutmisel.

Operatsioonide plaanimise saate käivitada alles pärast tootmistellimuse kulude hindamist. Kui te pole hindamist käivitanud, käivitatakse see automaatselt enne operatsioonide plaanimise algust. Operatsioonide plaan määrab järgmise teabe.

-   Tootmiseks plaanitud toode
-   Toote konfiguratsioon
-   Tootmisse kaasatud kogused
-   Tootmise algus- ja lõppkuupäev
-   Tootmistoiminguid tegevate ressursside võimsuse reserveeringud

Tootmise operatsioonide jaoks määratakse seadistusaeg, töötlusaeg ja käitusaeg. Pärast operatsioonide plaanimise käivitamist on tootmistellimuse olek **Plaanitud** ja kõik operatsioonid on plaanitud tootmisprotsessiga määratud järjekorras. Arvesse võetakse siiski ainult operatsiooni kestust. Algus- ja lõppaegu ei plaanita.

## <a name="scheduling-direction-and-date"></a>Planeerimissuund ja kuupäev
Planeerimisprotsessis on planeerimissuund põhiline. Tootmist saab plaanida mis tahes kuupäevast edasi või tagasi, olenevalt ajastamise ja planeerimise nõuetest.

-   **Plaanimiskuupäevast edasi** – saate plaanida tootmise alustamise võimalikult vara. Tootmist võib alustada täna, homme või mis tahes kuupäeval tulevikus. Tootmine plaanitakse lõppema kõige varasemal võimalikul kuupäeval tulevikus.
-   **Plaanimiskuupäevast tagasi** – saate plaanida tootmise alustamise võimalikult hilja. Tagasisuunas plaanimine põhineb kuupäeval, millal tootmine tuleb lõpule viia. Graafik loendab sellest kuupäevast tagasi hiliseima võimaliku kuupäevani, millal tootmist saab alustada ja lõpetada siiski õigeaegselt.

## <a name="resource-scheduling"></a>Ressursside plaanimine
Kui käivitate operatsioonide plaanimise, plaanitakse kõik tootmisprotsessi operatsioonid igale operatsioonile määratud ressursi järgi. Peale selle määratakse tootmisprotsessis iga operatsiooni kestus. Kui operatsioonile on määratud ressursigrupp, reserveerib plaanimine võimsuse grupile. Erinevalt siiski tööde plaanimisest ei vali operatsioonide plaanimine grupis kindlaid ressursse. Kui töötate piiratud võimsusega, sõltub graafik tootmise lõpuleviimiseks nõutavate ressursside kättesaadavusest. Operatsioonide plaanimine järgib tootmisprotsessis määratud operatsioonide jada. Plaanimine reserveerib võimsuse ressursigruppides tootmisprotsessis määratletud operatsiooniaegade põhjal. Kaasatud ressursside saadaoleva võimsuse summa määrab ressursigrupi võimsuse. Ressurssides juba olemas olevaid võimsuse reserveerimisi käsitletakse mittesaadava võimsusena. Kui tootmise jaoks ei ole piisavalt võimsust, saab tootmistellimused edasi lükata või isegi peatada. Saate määrata ka tõhususe, mida tootmisse kaasatud ressurssidelt ootate. Tõhusus tuleb määrata ressursi puhul protsendina. Tõhususprotsent korrigeerib ressursi läbilaskevõimet. See korrigeerimine mõjutab ressursi jaoks reserveeritud aega. Selle järgi korrigeeritakse ka ressurssi kasutavate operatsioonide täitmisaegu.

## <a name="operations-scheduling-and-master-planning"></a>Operatsioonide plaanimine ja koondplaneerimine
Operatsioonide graafik juhib ka koondplaneerimist ning määrab materjalivajaduse kalkulatsioonid. Operatsioonide plaanimine võtab arvesse järgmist teavet.

-   **Mahajäämusega tooted**: tooted, mis on plaanitud, vabastatud või alustatud.
-   **Materjali saadavus**: varu, alamkooslused, tarnijad ja hankijad.
-   **Võimsuse saadavus**: tootmiseks vajalikud ressursid

> [!NOTE]
> Kui kasutate mitmelõimelist koondplaneerimist ja operatsioonide planeerimist, siis piiratud võimsust ei arvestata. 

## <a name="cancellations"></a>Tühistamised
Kui käivitate operatsioonide plaanimise, saate tühistada protsessi teatud osi. Need osad on ooteaeg, seadistusaeg, töötlusaeg, kattumisaeg ja transpordiajad.

## <a name="finite-materials"></a>Piiratud materjalid
Kui töötate limiteeritud materjalidega, sõltub plaanimine ka tootmiseks vajalike materjalide saadavusest. Kui tootmiseks pole piisavalt komponente saadaval, saab tootmise edasi lükata. Saate materjalikasutust eelplaanida, määrates materjalid, mis peavad olema tootmise jaoks saadaval. Kui optimeerite nii ressursi võimsust kui ka materjalide saadavust, arvutatakse tootmine nende piirangute alusel. Tootmistellimust ei saa plaanida algama enne, kui võimsus ja materjalid on saadaval samal ajal ja nõutud kogustes.

## <a name="additional-resources"></a>Lisaressursid

[Operatsioonide plaanimise valikud](operation-scheduling-options.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]