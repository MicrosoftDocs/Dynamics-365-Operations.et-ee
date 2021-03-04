---
title: Prognoosi mudeli parandamine (eelversioon)
description: See teema kirjeldab funktsioone, mida saate kasutada prognoosimise mudelite jõudluse parandamiseks.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646075"
---
# <a name="improve-the-prediction-model-preview"></a>Prognoosi mudeli parandamine (eelversioon)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See teema kirjeldab funktsioone, mida saate kasutada prognoosimise mudelite jõudluse parandamiseks. Oma mudelit saate hakata täiustama tööruumis **Kliendimakse prognoosid** rakenduses Microsoft Dynamics 365 Finance. Parandamise sammud viiakse seejärel lõpule AI Builderis.

## <a name="select-historical-outcomes"></a>Ajalooliste tulemuste valimine

Esmalt valite ühe või mitu kolmest arve võimalikust tulemusest: **õigel ajal**, **hilja** ja **väga hilja**. Valida tuleb kõik kolm tulemust. Kui tühjendate mis tahes tulemuse valiku, filtreeritakse arved koolitusprotsessist välja ja prognoosi täpsus väheneb.

[![Tulemuste kinnitamine](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Kui teie organisatsioon nõuab ainult kaht tulemust, muutke variantide **hilja** ja **väga hilja** lävendiks null (0) päeva. Sel viisil saate ahendada prognoosid tõhusalt binaarsesse olekusse **õigel ajal** või **hilinenud**.

## <a name="select-fields"></a>Vali väljad

Mudelisse kaasamiseks väljade valimisel olge teadlik, et loend sisaldab kõiki saadaolevaid välju üksuses Common Data Service, mis vastendatakse Azure’i andmejärve andmetega. Osasid nendest väljadest **ei** pea valima. Väljad, mida ei peaks valima, jäävad ühte kolmest kategooriast.

- Väli on üksuse Common Data Service jaoks nõutav, kuid andmejärves pole selle jaoks toetavaid andmeid.
- Väli on ID ja pole masinõppe funktsiooni jaoks vajalik.
- Väli sisaldab teavet, mis ei ole prognoosimise ajal saadaval.

Järgmistes jaotistes on näidatud väljad, mis on arve ja kliendi üksuste jaoks saadaval, ja loetleb väljad, mida **ei** peaks koolituse ajal valima. Iga sellise välja jaoks määratud kategooria viitab eelmise loendi kategooriatele.
 
### <a name="invoice-common-data-model-entity"></a>Arve ühise andmemudeli üksus

Järgmisel joonisel on näidatud arve üksuse jaoks saadaolevad väljad.

[![Arve üksuse jaoks saadaolevad väljad](./media/available-fields.png)](./media/available-fields.png)

Järgmisi välju ei peaks koolituse jaoks valima.

- **Arve konto** (kategooria 2)
- **On suletud** (kategooria 3) – seda välja kasutatakse koolituse (suletud) ja prognoosimise (pole suletud) arvete filtreerimiseks.
- **Nimi** (kategooria 1)
- **Allika ID** (kategooria 2)
- **Allika kirje** (kategooria 2)
- **Allika tabel** (kategooria 2)

### <a name="customer-common-data-model-entity"></a>Kliendi ühise andmemudeli üksus

Järgmisel joonisel on näidatud kliendi üksuse jaoks saadaolevad väljad.

[![Kliendi üksuse jaoks saadaolevad väljad](./media/related-entities.png)](./media/related-entities.png)

Järgmist välja ei peaks koolituse jaoks valima.

- **Rea kordumatu võti** (kategooria 2)

## <a name="filters"></a>Filtrid

Filtrid ei toeta praegu kliendi makse prognoosimise stsenaariumit. Seetõttu valige suvand **Jäta see samm vahele** ja jätkake kokkuvõttelehega.

[![Filtritega mudelil keskendumine](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Privaatsusavaldus
Eelvaated 1) võivad kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 Finance and Operations teenus; 2) ei ole hõlmatud selle teenuse teenusetaseme leppes; 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud; 4) on piiratud toega.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]