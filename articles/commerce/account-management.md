---
title: Kontohalduse lehed ja moodulid
description: See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: b0f963bcf65ae622522fe52fd59996c6ec0ecf17
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411594"
---
# <a name="account-management-pages-and-modules"></a>Kontohalduse lehed ja moodulid

[!include [banner](includes/banner.md)]

See teema käsitleb kontohalduse lehti ja mooduleid rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Kontohaldus viitab lehtede grupile, mida kasutatakse kasutajakontoga seotud teabe haldamiseks rakenduses Dynamics 365 Commerce. Kontohalduse lehed hõlmavad kontohalduse sihtlehte, kasutajaprofiili lehte, kasutaja aadressi lehte, tellimuste ajaloo lehte, tellimuste üksikasjade lehte, püsikliendi lehte ja soovinimekirja lehte.

### <a name="account-management-landing-page"></a>Kontohalduse sihtleht

Kontohalduse sihtleht kasutab järgmisi mooduleid.

- **Konteiner** – kõik kontohalduse sihtlehe moodulid tuleb asetada konteinerisse. 
- **Konto tervituse paan** – seda moodulit kasutatakse kontohalduse lehe tervitussõnumi esitamiseks. See sisaldab pealkirja atribuute.
- **Konto üldpaan** – seda moodulit saab kasutada kontohalduse lehtede pealkirjade ja linkide esitamiseks, nt lehed "Tellimuste ajalugu" või "Minu profiil". Üldpaani moodulit saab kasutada mistahes lehe paani konfigureerimiseks. Fabrikamis kasutatakse seda moodulit "Tellimuse ajaloo" ja "Minu profiili" lehtede linkideks kontohalduse sihtlehel.
- **Konto soovinimekirja paan** – seda moodulit kasutatakse kliendi soovinimekirjas olevate kaupade kokkuvõtte esitamiseks. Näiteks võib see märkida „Teil on soovinimekirjas 10 eset”. See hõlmab pealkirja ja lingi "Kuva üksikasjad" atribuute. Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber soovinimekirja lehele. 
- **Konto aadressi paan** – seda moodulit kasutatakse kasutaja aadressi kokkuvõtte esitamiseks. Näiteks võib see märkida „Teil on kontole lisatud 2 aadressi”. See hõlmab pealkirja ja lingi "Kuva üksikasjad" atribuute. Link „Kuva üksikasjad” peaks olema konfigureeritud suunama ümber kasutaja aadressi lehele.
- **Konto püsikliendi paan** – seda moodulit kasutatakse püsikliendiprogrammi teabe kuvamiseks ja linkimiseks. Sellel paanil on kaks olekut: ühes olekus kuvatakse lingid püsikliendiprogrammiga liitumiseks, kui kasutaja pole juba liige. Teises olekus kuvatakse lingid, et vaadata püsikliendi üksikasjade lehte, kui kasutaja on juba liige. Atribuudid sisaldavad pealkirja, linki "Registreeru" ja linki "Kuva püsikliendi infot". Link „Kuva püsikliendi infot” peaks olema konfigureeritud suunama ümber püsikliendi lehele. Link „Registreeru” peaks olema konfigureeritud suunama ümber lehele, kus kasutajad saavad püsikliendiprogrammiga liituda. 

### <a name="order-history-page"></a>Tellimuste ajaloo leht

Tellimuste ajaloo leht kasutab tellimuste ajaloo moodulit, et näidata kõiki kasutaja hiljuti esitatud tellimusi.

### <a name="order-details-page"></a>Tellimuse üksikasjade leht

Tellimuste üksikasjade leht pakub iga tellimuse üksikasjalikku teavet ja sellele pääseb ligi tellimuste ajaloo lehelt. See kasutab tellimuse üksikasjade moodulit, mis nõuab tellimuse üksikasjade toomiseks müügi ID-d või kande ID-d.

### <a name="user-profile-page"></a>Kasutajaprofiili leht

Kasutajaprofiili leht näitab kasutajakonto üksikasju, nagu kasutajanimi ja meiliaadress. See kasutab kasutajaprofiili üksikasju ja kasutajaprofiili redigeerimise mooduleid. Kuigi meiliaadressi ei saa eemaldada, saab seda redigeerida. Kasutajaprofiili lehel kuvatakse ka kasutaja eelistused, mis võimaldavad kasutajal valida või loobuda teatud funktsioonidest, nt soovituste loendite isikupärastamine. 

### <a name="user-address-page"></a>Kasutaja aadressi leht

Kasutaja aadressi leht näitab kasutajakontoga seostadatud aadressite loendit. Kasutaja kas edastas need aadressid maksmise ajal või lisas need sellel lehel otse. Kasutaja aadressi moodulit kasutatakse lehel aadresside lisamiseks ja redigeerimiseks, peamise aadressi määramiseks ja olemasolevate aadresside muutmiseks.

### <a name="wish-list-page"></a>Soovinimekirja leht

Soovinimekirja leht näitab kliendi soovinimekirja lisatud esemeid. See kasutab soovinimekirja esemete renderdamiseks soovinimekirja moodulit.

### <a name="loyalty-page"></a>Püsikliendi leht

Püsikliendi leht võimaldab klientidel vaadata oma püsikliendi infot, kui nad on juba püsikliendi programmi liikmed. Nad saavad vaadata ka punkte, mille nad on viimaste tehingutega teeninud ja lunastanud. Leht kasutab püsikliendi üksikasjade moodulit püsikliendi üksikasjade näitamiseks. 

Püsikliendiprogrammiga liitumiseks saab luua püsikliendiprogrammi registreerumise ja püsikliendi tingimuste mooduliga turunduslehe. Kui kasutaja ei ole püsikliendiprogrammi liige, siis võimaldavad need moodulid kasutajal registreeruda.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukastimoodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[Maksmismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]