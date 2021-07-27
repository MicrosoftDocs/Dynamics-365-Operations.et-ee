---
title: Küpsistega nõustumise moodul
description: See teema hõlmab küpsistega nõustumise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a277ef0634c4ddd5769d278ce6186aac5e84ebfa
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352514"
---
# <a name="cookie-consent-module"></a>Küpsistega nõustumise moodul

[!include [banner](includes/banner.md)]

See teema hõlmab küpsistega nõustumise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Küpsistega nõustumise moodul palub saidi kasutajatel anda nõusolek küpsiste lubamiseks mis tahes funktsiooni või mooduli jaoks, mis jälgib brauseri küpsiseid. Nõusolekut küsitakse saidi esmakordsel sirvimisel brauseri esimesel seansil. Nõusoleku saamisel jälgitakse seda ja saidi kasutajalt ei küsita uuesti nõusolekut. Lisateavet vt teemast [Küpsise vastavus](cookie-compliance.md).

Kui saidi kasutaja küpsise nõusolekut ei anna, ei renderdata lehel ühtegi küpsise nõusolekut nõudvat funktsiooni või moodulit. Näiteks maksmise moodul, suhtlussaidil jagamise moodul ja eelistatud kaupluse funktsioon nõuavad küpsise nõusolekut ja neid ei renderdata, kui saidi kasutaja nõusolekut ei anna. 

Küpsistega nõustumise mooduli saab konfigureerida lehe päise fragmendis, et seda saaks lehe laadimisel jõustada. Küpsistega nõustumise moodulil peaks olema selge teade, mis teavitab saidi kasutajat küpsiste kasutamisest saidil ja peaks esitama saidi privaatsuspoliitika lehele viiva lingi.

Järgmisel joonisel on toodud küpsise nõusoleku teate näide koos saidilehe päises kuvatava saidi privaatsuspoliitika lehele viiva lingiga.
![Küpsistega nõustumise mooduli näide.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Küpsistega nõustumise mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Rikastekst                  | Rikastekst | Määrab saidi kasutajatele kuvatava rikasteksti teatise selle kohta, et sait kasutab brauseri küpsiseid ja et kasutajad peaksid nõustuma küpsiste kasutamisega saidi täielikult funktsioneerimiseks. |
| Lingid | URL | Saidi privaatsuspoliitika lehele saab lisada ühe või mitu linki, mis kirjeldavad saidil jälgitavate küpsiste tüüpe. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Küpsistega nõustumise mooduli lisamine saidi lehtedele

Küpsistega nõustumise mooduli tõhusaks lisamiseks mitmele saidi lehele saab selle lisada ühiskasutusega lehe päise fragmenti. Pärast päise fragmendi lisamist kõigile saidi lehtedele renderdatakse küpsise nõusoleku teatis automaatselt, kui saidi kasutaja liigub esimest korda suvalisele saidi lehele.

Lisateavet päise fragmentide ja -moodulite kohta vt teemast [Päisemoodul](author-header-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Päisemoodul](author-header-module.md) 

[Küpsise vastavus](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]