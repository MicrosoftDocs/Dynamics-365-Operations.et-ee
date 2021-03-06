---
title: Suhtlussaidil jagamise moodul
description: See teema hõlmab suhtlussaidil jagamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795353"
---
# <a name="social-share-module"></a>Sotsiaalmeedias jagamise moodul

[!include [banner](includes/banner.md)]

See teema hõlmab suhtlussaidil jagamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Suhtlussaidil jagamise moodulid võimaldavad kasutajatel jagada e-kaubanduse saidi URL-e sotsiaalmeedias (nt Facebook, Twitter, Pinterest ja LinkedIn). Saidi URL-e saab jagada ka meili teel. Suhtlussaidil jagamise mooduleid kasutatakse tavaliselt toote üksikasjade lehtedel (PDP-d), et aidata kasutajatel toote teavet jagada.

Iga suhtlussaidil jagamise moodul on konteiner suhtlussaidil jagatava üksuse moodulitele. Iga suhtlussaidil jagatava üksuse mooduit saab konfigureerida nii, et see osutaks konkreetsele sotsiaalmeedia saidile. Integreerimist Facebooki, Twitteri, Pinteresti, LinkedIni ja meiliga toetatakse valmislahendusena. Kui saidi kasutaja valib sotsiaalmeedia sümboli, käivitatakse vastava sotsiaalmeedia saidi jaoks HTML-i iFrame. iFrame'is saab kasutaja sisse logida ja postitada vaadatud lehe sisu.

Iga sotsiaalmeedia platvorm võib küpsiseid jälgida, nii et see moodul nõuab saidi kasutajatelt küpsistega nõustumise teatise aktsepteerimist. Kui küpsistega ei nõustuta, on moodul lehel peidetud. Lisateavet vt teemast [Küpsise vastavus](cookie-compliance.md).

Järgmisel illustratsioonil on toodud näide toote üksikasjade lehel kasutatavast suhtlussaidil jagamise moodulist.

![Suhtlussaidil jagamise mooduli näide](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Suhtlussaidil jagamise mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Pealdis                  | Tekst | See atribuut määrab mooduli pealdise. |
| Asetus | **Horisontaalne** või **Vertikaalne**  | See atribuut määratleb suhtlussaidil olevate üksuste paigutuse. |

## <a name="social-share-item-module-properties"></a>Suhtlussaidil jagatava üksuse mooduli atribuudid
| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Suhtlusvõrgustik              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **meilirakendus** | Rippmenüü suhtlusvõrgustiku platvormide nimekirjaga. |
| Ikoon |Pilt    | See on pilt, mida kuvatakse vastava suhtlusvõrgustiku korral. Iga platvormi jaoks soovitatava pildi leiate suhtlusvõrgustiku platvormi SDK-st. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Suhtlussaidil jagamise mooduli lisamine ostukasti moodulile

Suhtlussaidil jagamise mooduli lisamiseks ostukasti moodulile tehke järgmist.

1. Valige saidil Fabrikam **Lehed** ja seejärel tehke toote üksikasjade lehe avamiseks valik **Vaike-PDP**. 
1. Valige pesas **Ostukast (nõutav)** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussait** ja klõpsake seejärel **OK**.
1. Valige pesas **Suhtlussait** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussait** ja klõpsake seejärel **OK**.
1. Tehke mooduli **Suhtlussait** atribuutide paani jaotises **Paigutus** valik **Horisontaalne**. Lisage pealdis vastavalt vajadusele.
1. Valige pesas **Suhtlussait** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussaidil jagatav üksus** ja klõpsake seejärel **OK**.
1. Tehke mooduli **Suhtlussaidil jagatav üksus** atribuutide paani jaotises **Suhtlussait** valik **Facebook**.
1. Tehke mooduli **Suhtlussaidil jagatav üksus** atribuutide paani jaotises **Ikoon** valik **+ Lisa pilt**.
1. Valige dialoogiboksis **Meedia valija** rakenduse Facebook logo ja klõpsake seejärel **OK**. Kui rakenduse Facebook logo ei kuvata, valige selle üleslaadimiseks käsk **Laadi üles uus meedium**.
1. Lisage ja konfigureerige täiendavaid mooduleid **Suhtlussaidil jagatav üksus** vastavalt vajadusele.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**. Leht kuvab suhtlussaidil jagamise mooduli.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Ostukastimoodul](add-buy-box.md)

[Küpsise vastavus](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]