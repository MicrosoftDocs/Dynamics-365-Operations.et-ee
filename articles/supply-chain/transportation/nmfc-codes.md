---
title: Riikliku autoveose klassifikatsiooni (NMFC) koodid
description: See teema kirjeldab, kuidas töötada Riikliku autoveose klassifikatsiooni (NMFC) koodidega Microsoftis Dynamics 365 Supply Chain Management
author: Henrikan
ms.date: 04/22/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 8e6aac6b3a8b730b6adc5c3d4410b98c3e8d5090eac866c337ed1d03409ba765
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731147"
---
# <a name="national-motor-freight-classification-nmfc-codes"></a>Riikliku autoveose klassifikatsiooni (NMFC) koodid

[!include [banner](../includes/banner.md)]

Riikliku autoveose klassifikatsiooni (NMFC) koodid aitavad klassifitseerida saadetavaid kaupu. NMFC-kood on tähistus, mida kasutatakse kaupade grupeerimiseks. See võimaldab transpordiettevõtetel hinnata kaupade saatmist, klassifitseerides kaubad, võttes aluseks sellised kaalutlused nagu veoki sobivus, laadimise probleemid, käsitsemisprobleemid ja lähetuse läbimine. Kaubad grupeeritakse ühte 18 veose klassist, kasutades numbreid vahemikus 50 kuni 500. Klass, mille alla kaup grupeeritakse, põhineb nelja transpordiomaduse (tihedus, tihedus, koormus, käsitsemine ja kohustus) hindamisel. Koos määravad need omadused kauba transporditavuse.

NMFC-kood on seotud iga alla laadurikoormuse (LTL) saatmiskaubaga. Näiteks võib sülearvutile määrata NMFC, mis on klassist 2.5, samas kui elektriseadmetele võidakse määrata NMFC, mis on klassist 65.

See funktsioon aitab töötajatel kasutada NMFC-koode LTL-i saadetise kaupade klassifitseerimiseks. Järgmisena on toodud mõned näited.

- Kui teie ettevõte lisab veose kirjelduste veokirjale (BOL), on vedajal aimu sellest, mida veos sisaldab. Veos on oluline klassifikatsioon, kuna paljud transpordiettevõtted tuginevad oma ärimudeli tervenisti veose tüüpidele, mida nad tarnivad.
- See klassifikatsioon võib olla teie ettevõttele oluline, kuna seda kasutatakse antud koormuse kulu määramiseks.
- Teie ettevõte saab tuvastada LTL-logistika ja transpordiettevõtte tulunäitaja.

Selles teemas kirjeldatakse, kuidas töötada NMFC-koodidega rakenduses Microsoft Dynamics 365 Supply Chain Management.

## <a name="prerequisites"></a>Eeltingimused

Enne NMFC-koodide loomiseks peate häälestama kõik LTL-veoklassid, mis tuleb nendega vastendada. LTL-veoseklassid esindavad kaupade kategooriaid, samas kui NMFC-koodid on seotud kindlate kaupadega igasühes 18 veose klassist. Lisateavet selle kohta, kuidas LTL-klassidega töötada, vt jaotist [Klassid alla veokikoormuse (LTL)](ltl-class.md).

## <a name="create-an-nmfc-code"></a>NMFC-koodi loomine

NMFC-koodi loomiseks tehke järgmist.

1. Järgige üht neist sammudest.

    - Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> NMFC-koodid**.
    - Avage **Transpordihaldus \> Seadistused \> Transpordistandardid \> NMFC-koodid**.

1. Valige NMFC-koodi loomiseks **Uus**. Seejärel määrake järgmised väljad.

    - **NMFC kood** – sisestage kauba tüübi kohta NMFC kood.
    - **Nimi** – sisestage NMFC-koodi nimi.
    - **LTL-klass** – valige NMFC-koodiga seostatud LTL-klass.
    - **Veose käsitsemise ühik** – määratlege saadetise vaikimisi käsitsemistüüp.

## <a name="example-set-up-nmfc-codes"></a>Näide: NMFC-koodide häälestamine

Järgmine näide näitab, kuidas seadistada kahte erinevat NMFC-koodi, mida saab kasutada erinevat tüüpi toodetega.

1. Minge jaotisse **Laohaldus \> Seadistus \> Inventar \> NMFC-koodid**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **NMFC kood:** *92.5*
    - **Nimi:** *Arvutid*
    - **LTL klass:** *92.5*
    - **Kauba käsitsemise ühik:** *ühik*

1. Valige toimingupaanil nupp **Salvesta**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **NMFC kood:** *125*
    - **Nimi:** *telefonid*
    - **LTL klass:** *125*
    - **Kauba käsitsemise ühik:** *ühik*

1. Valige toimingupaanil nupp **Salvesta**.

## <a name="additional-resources"></a>Lisaressursid

- [Klassid "Vähem kui koormatäis" (LTL)](ltl-class.md)
- [Veokirja loomine](create-bill-of-lading.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
