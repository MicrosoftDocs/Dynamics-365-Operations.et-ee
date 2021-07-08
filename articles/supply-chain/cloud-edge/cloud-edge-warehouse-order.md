---
title: Laotellimused pilv- ja perimeeterskaalaüksuste jaoks
description: See teema annab teavet lao tellimuste võimaluse kohta, mida kasutatakse lao skaalaühiku töökoormuse osana.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 080d45170c726cd0351ab344254aa36c1c56ba55
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271252"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Laotellimused pilv- ja perimeeterskaalaüksuste jaoks

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Mitte kogu ettevõtte funktsionaalsus ei ole skaalaühikute töökoormuste kasutamisel avalikus eelvaates täielikult toetatud. Kui kasutate skaalaühikuid, kasutage kindlasti ainult neid protsesse, mida see teema konkreetselt toetab.

## <a name="what-are-warehouse-orders"></a>Mis on laotellimused?

*Laotellimused* on tellimuse tüüp, mis loodi keskuse ja skaalaüksuse lao juurutuste toetamiseks. Need võimaldavad teil lao töökoormuse skaalaühikus käitamisel võtta vastu varusid. Neid kasutatakse praegu ainult ostutellimustega.

Laotellimusi kasutatakse laohalduse töötlemise osana, näiteks kui mobiilirakendust Warehouse Management kasutatakse sissetuleva ostutellimuse töötlemisel füüsilise vaba kaubavaru registreerimiseks. Laotellimused luuakse osana *lattu vabastamise* protsessist, mis on saadaval ostutellimustele, mis määratlevad kaaluühiku lao ja kaubad, mis on lubatud laohaldusprotsesside kasutamiseks.

> [!IMPORTANT]
> Laotellimused on saadaval ainult juurutustes, mis kasutavad [laohaldustöökoormusi pilv- ja perimeeterskaalaüksuste](cloud-edge-workload-warehousing.md) jaoks.

## <a name="create-a-warehouse-order"></a>Laotellimuse loomine

Laotellimuse loomiseks tehke järgmist.

1. Logige sisse keskuses töötavasse rakendusse Microsoft Dynamics 365 Supply Chain Management. (Peate käivitama protsessi *Vabasta lattu* ajal, kui olete keskusesse sisse logitud.)
1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.
1. Seotud laotellimuse ridade vaatamiseks avage vastav ostutellimus, valige jaotises **Ostutellimuse read** rida ja valige seejärel suvand **Ladu \> Laotellimuse read**. Kõigi ridade vaatamiseks avage **Laohaldus \> Päringud ja haldus \> Laotellimuse read**.

Pakett-töö kaudu saate käivitada ka *lattu väljastamise* protsessi, selleks avage **Laohaldus > Lattu väljastamine > Ostutellimuste automaatne väljastamine**. Pakett-töö häälestamisel saate päringu põhjal valida konkreetsed ostutellimuse read. Tavaline stsenaarium oleks häälestada korduv pakett-töö, millega väljastatakse kõik kinnitatud ostutellimuse read, mis saabuvad järgmisel päeval.

## <a name="cancel-a-warehouse-order"></a>Laotellimuse tühistamine

Protsessi *Vabasta lattu* osana on ostutellimuse laokanded seotud laotellimustega ja keskuse poolt värskendamiseks lukus. Kui vabastasite lattu ekslikult või kui teil on mõni muu põhjus laotellimuse ridade loomise tühistamiseks, saate taotleda laotellimuse ridade tühistamise.

Laotellimuse ridade tühistamiseks tehke järgmist.

1. Logige sisse keskuses töötavasse rakenduse Supply Chain Management eksemplari.
1. Avage **Laohaldus \> Päringud ja haldus \> Laotellimuse read**.
1. Valige vastav rida.
1. Valige tegevuspaanil suvand **Tühista laotellimuse read**.

> [!NOTE]
> Ridade tühistamise taotlus lükatakse tagasi kõikide ridade puhul, mis on juba tühistamise ootel või mida töödeldakse aktiivselt laos, mis käitab oma töökoormust skaalaüksusel.

## <a name="monitor-a-warehouse-order"></a>Laotellimuse jälgimine

Vaates **Laotellimuse read** saate jälgida sissetuleva vastuvõtu edenemist, vaadates väärtuseid veerus **Vastuvõtmiseks järelejäänud kogus**. Mobiilirakenduse Warehouse Management abil tehtud tööga seotud üksikasjade vaatamiseks järgige ühte järgmistest sammudest.

- Avage **Laohaldus \> Päringud ja aruanded \> Laotellimuse read** ja kasutage otsitavate ridade leidmiseks filtrit.
- Avage **Hanked \> Ostutellimused \> Kõik ostutellimused** ja avage seotud ostutellimus. Jaotises **Ostutelimuse read** valige üks või mitu rida ja seejärel valige tööriistaribal **Ladu \> Lao sissetuleku kirjed**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
