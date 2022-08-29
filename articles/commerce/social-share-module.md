---
title: Sotsiaalmeedias jagamise moodul
description: See artikkel käsitleb sotsiaalosa mooduliid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88bc5469e3072b625836cc942efbd2206f6dd6ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284680"
---
# <a name="social-share-module"></a>Sotsiaalmeedias jagamise moodul

[!include [banner](includes/banner.md)]

See artikkel käsitleb sotsiaalosa mooduliid ja kirjeldab, kuidas lisada neid saidi lehtedele moodulis Microsoft Dynamics 365 Commerce.

Suhtlussaidil jagamise moodulid võimaldavad kasutajatel jagada e-kaubanduse saidi URL-e sotsiaalmeedias (nt Facebook, Twitter, Pinterest ja LinkedIn). Saidi URL-e saab jagada ka meili teel. Suhtlussaidil jagamise mooduleid kasutatakse tavaliselt toote üksikasjade lehtedel (PDP-d), et aidata kasutajatel toote teavet jagada.

Iga suhtlussaidil jagamise moodul on konteiner suhtlussaidil jagatava üksuse moodulitele. Iga suhtlussaidil jagatava üksuse mooduit saab konfigureerida nii, et see osutaks konkreetsele sotsiaalmeedia saidile. Integreerimist Facebooki, Twitteri, Pinteresti, LinkedIni ja meiliga toetatakse valmislahendusena. Kui saidi kasutaja valib sotsiaalmeedia sümboli, käivitatakse vastava sotsiaalmeedia saidi jaoks HTML-i iFrame. iFrame'is saab kasutaja sisse logida ja postitada vaadatud lehe sisu.

Iga sotsiaalmeedia platvorm võib küpsiseid jälgida, nii et see moodul nõuab saidi kasutajatelt küpsistega nõustumise teatise aktsepteerimist. Kui küpsistega ei nõustuta, on moodul lehel peidetud. Lisateavet vt teemast [Küpsise vastavus](cookie-compliance.md).

Järgmisel illustratsioonil on toodud näide toote üksikasjade lehel kasutatavast suhtlussaidil jagamise moodulist.

![Suhtlussaidil jagamise mooduli näide.](./media/ecommerce-socialshare.png)

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
1. Ostukaustas **(nõutav)** pesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige sotsiaal **ühiskasutuse moodul** ja seejärel valige **OK**.
1. Valige sotsiaalosa pesal kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige moodul **SocialShare** ja seejärel valige **OK**.
1. Tehke mooduli **Suhtlussait** atribuutide paani jaotises **Paigutus** valik **Horisontaalne**. Lisage pealdis vastavalt vajadusele.
1. Valige lisamoodulis SocialShare kolmikpunkt (**...**) ja seejärel valige **lisamismoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige moodul **SocialShareItem** ja seejärel valige **OK**.
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
