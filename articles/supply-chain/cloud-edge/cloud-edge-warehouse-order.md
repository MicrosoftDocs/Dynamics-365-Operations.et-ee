---
title: Laotellimused pilv- ja perimeeterskaalaüksuste jaoks
description: See artikkel annab teavet laotellimuse võimaluse kohta, mida kasutatakse laoskaala ühiku töökoormuse osana.
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
ms.openlocfilehash: db254216e6c34b81f83c87a8fda454d0aeb1cece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893522"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a>Laotellimused pilv- ja perimeeterskaalaüksuste jaoks

[!include [banner](../includes/banner.md)]

> [!WARNING]
> Mitte kogu ettevõtte funktsionaalsus ei ole skaalaühikute töökoormuste kasutamisel avalikus eelvaates täielikult toetatud. Kui kasutate kaaluühikuid, kasutage kindlasti ainult neid protsesse, mida see artikkel kirjeldab täpselt toetatud üksustena.

## <a name="what-are-warehouse-orders"></a>Mis on laotellimused?

*Laotellimused* on tellimuse tüüp, mida kasutatakse jaoturite ja mõõtühikute lao juurutamise toetamiseks. Need võimaldavad teil lao töökoormuse skaalaühikus käitamisel võtta vastu varusid.

Laotellimusi kasutatakse nii sissetulevate kui ka väljaminevate laohalduse töötlemistoimingute osana. Need luuakse osana *lattu vabastamise* protsessist, mis lähtestatakse keskusesse.
Sissetulevaks töötlemiseks kasutatakse warehouse mobile app rakendust sissetulevate tellimuste töötlemisel füüsilise vaba kaubavaru registreerimiseks, see on saadaval ostu- ja tootmistellimustele, mis määravad kaaluühiku lao ja kaubad, mis on lubatud kasutada laohalduse protsesse.
Väljaminevaid laotellimusi kasutatakse üleviimis- ja müügitellimuste saadetise laineprotsessi osana.

> [!IMPORTANT]
> Laotellimused on saadaval ainult juurutustes, mis kasutavad [laohaldustöökoormusi pilv- ja perimeeterskaalaüksuste](cloud-edge-workload-warehousing.md) jaoks.

## <a name="create-an-inbound-warehouse-order"></a>Looge sissetuleva lao tellimus

Sissetuleva lao tellimuse loomiseks ostutellimuse protsessi jaoks järgige neid samme.

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
