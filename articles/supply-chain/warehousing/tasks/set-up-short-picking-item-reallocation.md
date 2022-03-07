---
title: Kiirelt komplekteeritava kauba ümberjaotamise häälestus
description: Selles teemas kirjeldatakse, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid.
author: Mirzaab
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fe17246037a35e44d12476f184af3bd4c806022
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565228"
---
# <a name="set-up-short-picking-item-reallocation"></a>Kiirelt komplekteeritava kauba ümberjaotamise häälestus

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid. 

Ümberjaotamisprotsessi juhib **Tööerand** ja seda kasutab lao **töötaja.**

Kasutada on võimalik automaatset, käsitsi või mõlemat ümberjaotamisprotsessi.

- Automaatne ümberjaotamine – asukohadirektiive kasutatakse selleks, et määrata, kas kaubad on saadaval teises asukohas. Võimaluse korral uuendatakse tööd ja lao kasutaja suunatakse alternatiivsesse asukohta.
- Käsitsi ümberjaotamine – võimaldab lao kasutajal valida ühe või mitme asukoha vahel, millel on reserveerimata kaubakoguseid. 
- Automaatne ja käsitsi – kui süsteem ei saa automaatset ümberjaotamist teha ja reserveerimata kogustega asukohti on saadaval, palutakse kasutajal valida asukoht.

## <a name="set-up-work-exceptions"></a>Tööerandite häälestamine
Määratleda saab mitu tööerandit erinevate kauba ümberjaotamise poliitikatega, et laotöötaja saaks valida neist ühe töödeldava saadetise vajaduste põhjal.

Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid.

1. Minge **Navigeerimispaanil** jaotisesse **Laohaldus> Seadistamine> Töö> Töö erandid**.
2. Klõpsake valikut **Uus** 
3. Tippige väärtus väljale **Tööerandi kood**. See on selle erandi pealkiri. Näiteks Puuduva käsitsi valimine.
4. Sisestage väärtus väljale **Kirjeldus**. See on selle erandi kasutuse lühikirjeldus. Näiteks Puuduva valimine – kaup pole saadaval.
5. Tehke väljal **Erandi** tüüp valik **Puuduva valimine**.
6. Märkige ruut **Varude korrigeerimine**. Selle valimisel reguleeritakse varud puuduva valimise asukohas automaatselt väärtusele 0.
7. Valige või sisestage väärtus väljal **Vaikimisi korrigeerimistüübi kood**. Näiteks USMF-is saate valida **Remove Res Adj Out**. Iga korrigeerimise tüübi kood sisaldab nelja omadust: nimi, kirjeldus, lao töölehe nimi ja **Eemalda reserveeringud**. Valiku **Eemalda reserveeringud** lubamisel eemaldatakse ka puuduva valimise tellimuse rea reserveeringud.  
8. Valige väljal **Kauba ümberjaotamine** väärtus, nt Käsitsi. Kui teete valiku Käsitsi või Automaatne ja Käsitsi, peab laotöötajale olema antud võimalus kasutada käsitsi ümberjaotamist.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Töötaja seadistamine käsitsi kauba ümberjaotamist kasutama

Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid.

1. Sulgege leht.
2. Avage **Navigeerimispaneelil** Moodulid > **Laohaldus > Seaditus > Töö**.
3. Klõpsake valikut **Redigeeri**.
4. Valige loendist töötaja. Näiteks Julia Funderburk.
5. Laiendage kiirkaarti **Kasutajad**.
6. Valige loendist **Kasutaja ID**. Näiteks 24.
7. Laiendage kiirkaarti **Töö**.
8. Tehke väljal **Luba käsitsi kauba ümberjaotamine** valik **Jah**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]