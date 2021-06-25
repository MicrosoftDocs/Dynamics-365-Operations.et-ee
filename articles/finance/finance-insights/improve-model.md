---
title: Prognoosi mudeli parandamine (eelversioon)
description: See teema kirjeldab funktsioone, mida saate kasutada prognoosimise mudelite jõudluse parandamiseks.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 184a1cb5d3851e26b41340b711c51ef38e06eb53
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186638"
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

Mudelisse kaasamiseks väljade valimisel olge teadlik, et loend sisaldab kõiki saadaolevaid välju tabelis Microsoft Dataverse, mis vastendatakse Azure’i andmejärve andmetega. Osasid nendest väljadest **ei** pea valima. Väljad, mida ei peaks valima, jäävad ühte kolmest kategooriast.

- Väli on tabeli Dataverse jaoks nõutav, kuid andmejärves pole selle jaoks toetavaid andmeid.
- Väli on ID ja pole masinõppe funktsiooni jaoks vajalik.
- Väli sisaldab teavet, mis ei ole prognoosimise ajal saadaval.

Järgmistes jaotistes on näidatud väljad, mis on arve ja kliendi üksuste jaoks saadaval, ja loetleb väljad, mida **ei** peaks koolituse ajal valima. Iga sellise välja jaoks määratud kategooria viitab eelmise loendi kategooriatele.
 
### <a name="invoice-dataverse-table"></a>Arve Dataverse'i tabel

Järgmisel joonisel on näidatud arve tabeli jaoks saadaolevad väljad.

[![Arve tabeli jaoks saadaolevad väljad](./media/available-fields.png)](./media/available-fields.png)

Järgmisi välju ei peaks koolituse jaoks valima.

- **Arve konto** (kategooria 2)
- **On suletud** (kategooria 3) – seda välja kasutatakse koolituse (suletud) ja prognoosimise (pole suletud) arvete filtreerimiseks.
- **Nimi** (kategooria 1)
- **Allika ID** (kategooria 2)
- **Allika kirje** (kategooria 2)
- **Allika tabel** (kategooria 2)

### <a name="customer-dataverse-table"></a>Kliendi Dataverse'i tabel

Järgmisel joonisel on näidatud kliendi tabeli jaoks saadaolevad väljad.

[![Kliendi tabeli jaoks saadaolevad väljad](./media/related-entities.png)](./media/related-entities.png)

Järgmist välja ei peaks koolituse jaoks valima.

- **Rea kordumatu võti** (kategooria 2)

## <a name="filters"></a>Filtrid

Filtrid ei toeta praegu kliendi makse prognoosimise stsenaariumit. Seetõttu valige suvand **Jäta see samm vahele** ja jätkake kokkuvõttelehega.

[![Filtritega mudelil keskendumine](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
