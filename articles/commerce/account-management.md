---
title: Kontohalduse lehed ja moodulid
description: See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: f9fc3731cd9d21294b0161e1d419f255096d7790
ms.sourcegitcommit: 96bfc20eb748f4090a2b5e1ff9f54997d5a5d359
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/04/2019
ms.locfileid: "2885805"
---
# <a name="account-management-pages-and-modules"></a>Kontohalduse lehed ja moodulid

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Kontohaldus viitab lehtede grupile, mida kasutatakse kasutajakontoga seotud teabe haldamiseks rakenduses Dynamics 365 Commerce. Kontohalduse lehed hõlmavad kontohalduse sihtlehte, kasutajaprofiili lehte, kasutaja aadressi lehte, tellimuste ajaloo lehte, tellimuste üksikasjade lehte, püsikliendi lehte ja soovinimekirja lehte.

### <a name="account-management-landing-page"></a>Kontohalduse sihtleht

Kontohalduse sihtleht kasutab järgmisi mooduleid.

- **Sisupaigutus** – see moodul on konteinermoodul, mis sisaldab kõiki kontohalduse sihtlehe mooduleid.
- **Konto tervituse üksus** – seda moodulit kasutatakse kontohalduse lehe tervitussõnumi esitamiseks. See hõlmab pealkirja ja paani suuruse atribuute. Atribuut **Paani suurus** määrab mooduli laiuse sisupaigutuse moodulis. Väärtused on vahemikus **1** kuni **12**, kus **12** tähistab sisupaigutuse konteineri täielikku laiust.
- **Konto tellimuse esitamise üksus** – seda moodulit kasutatakse kasutajakonto esitatud tellimuste koguarvu näitamiseks. See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute. Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber tellimuste ajaloo lehele.
- **Kontoprofiili paigutuse üksus** – seda moodulit kasutatakse kasutajaprofiili kokkuvõtte esitamiseks. See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute. Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber kasutajaprofiili lehele.
- **Konto soovinimekirja üksus** – seda moodulit kasutatakse kliendi soovinimekirjas olevate kaupade kokkuvõtte esitamiseks. Näiteks võib see märkida „Teil on soovinimekirjas 10 eset”. See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute. Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber soovinimekirja lehele.
- **Konto aadressi üksus** – seda moodulit kasutatakse kasutaja aadressi kokkuvõtte esitamiseks. Näiteks võib see märkida „Teil on kontole lisatud 2 aadressi”. See hõlmab pealkirja, paani suuruse ja üksikasjade kuvamise lingi atribuute. Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber kasutaja aadressi lehele.
- **Konto püsikliendi üksus** – seda moodulit kasutatakse püsikliendiprogrammi teabe kuvamiseks ja linkimiseks. See hõlmab pealkirja, paani suuruse, üksikasjade kuvamise lingi ja liikmeks hakkamise lingi atribuute. Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber püsikliendi lehele. Link „Hakka liikmeks” peaks olema konfigureeritud suunama ümber lehele, kus kasutajad saavad püsikliendiprogrammiga liituda.

### <a name="order-history-page"></a>Tellimuste ajaloo leht

Tellimuste ajaloo leht kasutab tellimuste ajaloo moodulit, et näidata kõiki kasutaja hiljuti esitatud tellimusi.

### <a name="order-details-page"></a>Tellimuse üksikasjade leht

Tellimuste üksikasjade leht pakub iga tellimuse üksikasjalikku teavet ja sellele pääseb ligi tellimuste ajaloo lehelt. See kasutab tellimuse üksikasjade moodulit, mis nõuab tellimuse üksikasjade toomiseks müügi ID-d või kande ID-d.

### <a name="user-profile-page"></a>Kasutajaprofiili leht

Kasutajaprofiili leht näitab kasutajakonto üksikasju, nagu kasutajanimi ja meiliaadress. See kasutab kasutajaprofiili moodulit. Kuigi meiliaadressi ei saa eemaldada, saab seda redigeerida. Kasutajaprofiili lehel kuvatakse ka kasutaja eelistused, mis võimaldavad kasutajal valida või loobuda teatud funktsioonidest, nt soovituste loendite isikupärastamine. 

### <a name="user-address-page"></a>Kasutaja aadressi leht

Kasutaja aadressi leht näitab kasutajakontoga seostadatud aadressite loendit. Kasutaja kas edastas need aadressid maksmise ajal või lisas need sellel lehel otse. Kasutaja aadressi moodulit kasutatakse lehel aadresside lisamiseks ja redigeerimiseks, peamise aadressi määramiseks ja olemasolevate aadresside muutmiseks.

### <a name="wish-list-page"></a>Soovinimekirja leht

Soovinimekirja leht näitab kliendi soovinimekirja lisatud esemeid. See kasutab soovinimekirja esemete renderdamiseks soovinimekirja moodulit.

### <a name="loyalty-page"></a>Püsikliendi leht

Püsikliendi leht võimaldab klientidel liituda püsikliendi programmiga või kui nad on juba püsikliendi programmi liikmed, vaadata oma programmi üksikasju. Nad saavad vaadata ka punkte, mille nad on viimaste tehingutega teeninud ja lunastanud.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvi moodul](add-cart-module.md)

[Maksmise moodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
