---
title: Materjali asendamise tootmises
description: See artikkel kirjeldab, kuidas asendada materjale tootmisprotsessi käigus.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 70171
ms.assetid: ce3b11ef-550e-49b7-8942-2607c2ec3c5c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c2e6c9cc8ed85c8c60539b37fb6c51c96bc2872
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855974"
---
# <a name="material-substitution-in-manufacturing"></a>Materjali asendamise tootmises

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas asendada materjale tootmisprotsessi käigus. 

Tootmisprotsessis materjalide asendamiseks on kolm võimalust.

-   Kuupäeva alusel – üks materjal asendatakse teisega pärast kindlat kuupäeva
-   Koondplaneerimise ajal – valemis olev materjal asendatakse teise materjaliga, kuna see on laost otsas
-   Tootmise ajal – materjal saab laost ootamatult otsa ja asendatakse teise materjaliga

## <a name="substituting-material-by-date"></a>Materjali asendamine kuupäeva alusel
Kaaluge järgmist stsenaariumit: masin, mida ettevõte toodab, sisaldab komponenti, mis aegub hankija kataloogist kahe kuu jooksul. Aegumiskuupäevast edasi pakub hankija uut komponenti, mida saab asendada vana komponendiga. Kehtivuse algus- ja lõppkuupäeva saate luuakse koosluse ridadel. Selle näite puhul seadistage vanade komponentide aegumine, sisestades aegumiskuupäeva väljale **Lõppkuupäev**. Seejärel seadistage koosluses uus, asenduskomponent, nii et see hakkaks kehtima järgmisel päeval pärast vana komponendi aegumist. Selleks sisestage alguskuupäev väljale **Alguskuupäev**.

## <a name="substituting-material-by-planning"></a>Materjali asendamine planeerimisel
Saate materjale planeerimise ajal asendada ainult valemite kasutamise korral, mitte siis, kui kasutate kooslust. Arvestage järgmist stsenaariumi: toiduainete tootmisettevõte valmistab kastet valemi alusel, mis sisaldab 20 koostisosa. Valemi ühe koostisosa saab asendada ühega kahest muust koostisosast. Kuna need kaks koostisosa on aga kallimad kui eelistatud koostisosa, kasutatakse asendamist ainult siis, kui eelistatud koostisosa on otsas. Asendatav materjal on A ning teised kaks materjali on B ja C. Materjali asendamist planeerimisel juhitakse valemiridade väljadega **Plaanigrupp** ja **Prioriteet**. Selle näite puhul saate luua valemiread kolmele materjalile ning seostada valemiread sama plaanigrupiga. Seadistamisel on materjali A valemirida kõrgeima prioriteediga (madalaim number), materjali C valemirida on madalaima prioriteediga ning materjali B valemirea prioriteet jääb kahe teise rea vahele. Kui teil tekib lõppenud kauba nõudlus, teeb koondplaneerimine esmalt kindlaks, kas materjali A nõudluse saab katta. Kui nõudlust ei saa katta, kontrollib koondplaneerimine prioriteedi järjekorras materjale B ja C. Kui materjali B on laos, kasutatakse seda pärast plaanitud partiitellimuse kinnitamist valemis. Kui ühtki materjali laos pole, loob koondplaneerimine plaanitud tellimuse materjalile A. **Märkus.** plaanigrupis valemiridade seadistamisel peate määrama koguse ainult kõrgeima prioriteediga materjalile. Seda kogust kasutatakse plaani kõigi (ka madalama prioriteediga) materjalide nõudluse arvutamisel. Te ei saa määrata erinevaid koguseid plaanigrupis olevatele madalama prioriteediga kaupadele.

## <a name="substituting-material-during-production"></a>Materjali asendamise tootmise ajal
Arvestage järgmist stsenaariumi: keevitustööks on vaja metallplaadi tükki. Töö ajal teavitab laotöötaja masinaoperaatorit, et plaat on laost otsas. Otsustatakse aga, et plaadi saab asendada teise, veidi paksema plaadiga. Nii on võimalik töö lõpetada. Materjali saab lisada kooslusele avatud tootmistellimuse puhul. Kui tootmistellimuse olek on **Alustatud**, palutakse kasutajal tootmise kooslusesse uue kauba lisamisel tellimus ümber hinnata. Kui materjal on lisatud, saab uue kauba kohta luua uue komplekteerimislehe. Te ei pea lisama uut materjali tootmise kooslusse. Selle asemel saate selle lisada otse tootmise komplekteerimislehele. Komplekteerimislehe sisestamisel lisab süsteem materjali tootmise kooslusse.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]