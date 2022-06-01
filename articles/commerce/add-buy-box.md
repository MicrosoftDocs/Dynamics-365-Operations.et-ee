---
title: Ostukasti moodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eba86cd0fe2790cabed1f091ddc59002d19ae228
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780430"
---
# <a name="buy-box-module"></a>Ostukastimoodul

[!include [banner](includes/banner.md)]

See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

Mõiste *ostukast* viitab tavaliselt toote üksikasjade lehe alale (PDP), mis on lehe kuvatav osa ehk „above the fold” ja mis sisaldab kõige olulisemat teavet, mis on toote ostu tegemiseks vajalik. (Ala, mida nimetatakse inglise keeles „above the fold”, on nähtav, kui leht esmakordselt laeb, ilma et kasutaja peaks hiirega selle nägemiseks kerima.)

Ostukasti moodul on spetsiaalne konteiner, mida kasutatakse kõigi moodulite majutamiseks, mis on toote üksikasjade lehe ostukasti alal näidatud.

Toote üksikasjade lehe URL sisaldab toote ID-d. Kogu teave, mis on vajalik ostukasti mooduli renderdamiseks, tuletatakse sellest toote ID-st. Kui toote ID-d ei ole, siis ostukasti moodulit ei renderdata lehel õigesti. Seetõttu saab ostukasti moodulit kasutada ainult lehtedel, millel on toote kontekst. Selle kasutamiseks lehel, millel ei ole toote konteksti (nt avaleht või turunduse leht), peate tegema täiendavaid kohandusi.

Järgmisel pildil on näide ostukasti moodulist toote üksikasjade lehel.

![Ostukasti mooduli näide.](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a>Ostukasti mooduli atribuudid ja pesad 

Toote üksikasjade lehel on ostukast jaotatud kaheks piirkonnaks: meediumipiirkond vasakul ja sisupiirkond paremal. Vaikimisi on meediumipiirkonna veeru ja sisupiirkonna veeru suhe 2:1. Mobiilsetel seadmetel on kaks piirkonda virnastatud, nii et üks piirkond ilmub teise piirkonna all. Kujundusi saab kasutada veeru laiuse ja virnastamise astme kohandamiseks.

Ostukasti moodul annab toote pealkirja, kirjelduse, hinna ja hinnangud. Samuti laseb see klientidel valida toote variante, millel on erinevad toote atribuudid, nagu suurus, stiil ja värv. Kui tootevariant on valitud, värskendatakse ostukasti teisi atribuute (nt toote kirjeldus ja pildid), et näidata variandi teavet. 

Koguse valija on esitatud, et kliendid saaksid määrata ostetavate kaupade koguse. Maksimaalset kogust, mida saab osta, saab määrata saidi sätetes.

Ostukastist saavad kliendid teha ka selliseid toiminguid nagu toote lisamine ostukorvi, toote lisamine soovinimekirja ja komplekteerimiskoha valimine. Neid toiminguid saab teha toote või toote variandiga. Toote lisamiseks soovinimekirja peab klient olema sisse logitud.

Kujundusi saab kasutada ostukasti tooteatribuutide ja tegevuste juhtelementide eemaldamiseks või muutmiseks. 

## <a name="module-properties"></a>Mooduli atribuudid

- **Pealkirja silt** – see atribuut määratleb toote pealkirjale pealkirja sildi. Kui ostukast on lehe ülaosas, tuleb see atribuut seada väärtusele **h1**, et vastata juurdepääsetavuse standarditele. 

- **Luba soovitused „osta sarnaseid tooteid”** - See atribuut lubab ostukastis kuvada nende toodete linke, mis sarnanevad praegu kuvatava kaubaga. See funktsioon on saadaval kaubanduse väljalaskes 10.0.13 ja uuemas.

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a>Moodulid, mida saab ostukasti moodulis kasutada

- **Meediumigalerii** – seda moodulit kasutatakse toote üksikasjade lehel toote piltide näitamiseks. Selle mooduli kohta lisateabe saamiseks vaadake teemat [Meediumigalerii moodul](media-gallery-module.md).
- **Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas. See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused. Selle mooduli kohta lisateabe saamiseks vaadake teemat [Kaupluse valimise moodul](store-selector.md).
- **Suhtluskanalites jagamine** - Selle mooduli saab lisada ostukasti, et kasutajad saaksid tooteteavet suhtluskanalites jagada. Lisateabe saamiseks vt [Suhtluskanalites jagamise moodul](social-share-module.md).

## <a name="buy-box-module-settings"></a>Ostukasti mooduli sätted

Jaotises **Saidi sätted \> Laiendused** saab konfigureerida järgmisi ostukasti mooduli sätteid.

- **Ostukorvi rea koguse piirang** – selle atribuudi abil määratakse, mitu kaubaühikut võib maksimaalselt ostukorvi lisada. Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.
- **Varud** – varude sätete rakendamise kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).
- **Toote lisamine ostukorvi** - lisateabe saamiseks selle kohta, kuidas rakendada **Toote lisamine ostukorvi** sätteid, vaata [Toote lisamine ostukorvi](add-cart-settings.md).

## <a name="buy-box-module-definition-extensions-in-the-adventure-works-theme"></a>Ostke kastimooduli definitsiooni laiendid Adventure Worksi kujunduses

Ostukasti moodul, mida Adventure Worksi teema pakub, on mooduli definitsiooni laiend, mis toetab tootespetsifikatsioonide mooduli rakendamist PDP ostukastis ühe definitsioonimooduli piires. PDP ostuboksis tootespetsifikatsiooni atribuutide näitamiseks lisage toote spetsifikatsioonimoodul teenindusmooduli pesasse ostuboksi pesas.


> [!IMPORTANT]
> Adventure Works teema on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.


## <a name="commerce-scale-unit-interaction"></a>Commerce Scale Unitiga suhtlemine

Ostukasti moodul toob tooteteavet Commerce Scale Uniti rakendusliideste (API-de) abil. Kogu teabe toomiseks kasutatakse toote ID-d toote üksikasjade lehel.

## <a name="add-a-buy-box-module-to-a-page"></a>Lehele ostukasti mooduli lisamine

Uuele lehele ostukasti mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Dialoogiboksis **Uus fragment** valige moodul **Ostukast**.
1. Avage jaotis **Fragmendi nimi**, sisestage **Ostukasti fragmendi** nimi ja seejärel valige **OK**.
1. Ostuboksi **mooduli meediagalerii** pesas valige ellips (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige meediamoodulis **ja** seejärel valige **OK**.
1. Ostuboksi **mooduli kauplusevalija** pesas valige ellips (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige kauplusevalija **moodul** ja seejärel valige **OK**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Mallid** ja valige uue malli loomiseks **Uus**.
1. Dialoogiaknas **Uus** mall malli nime **all** sisestage **PDP mall** ja seejärel valige **OK**.
1. Kehapesas valige kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.**·**
1. Dialoogiaknas **Vali** moodulid valige vaikelehemoodul **ja** seejärel valige **OK**.
1. Valige vaikelehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.
1. Dialoogiaknas **Vali tükk** valige loodud **karbi tüki** killus ja seejärel valige **OK**.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Dialoogiaknas **Uue lehe loomine** sisestage **jaotises** **Lehe nimi PDP ja** seejärel valige käsk **Edasi.**
1. Valige **valiku Vali mall** all **PDP mall ja** seejärel **edasi**.
1. Valige **valiku Vali paigutus** all lehekülje paigutus (nt Paindlik **paigutus**) ja seejärel klõpsake nuppu **Edasi**.
1. Vaadake **jaotises Ülevaade ja lõpetamine** üle lehe konfiguratsioon. Kui teil on vaja lehekülje teavet redigeerida, valige **Tagasi**. Kui lehekülje teave on õige, valige Loo **leht**.
1. Valige uue lehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.
1. Dialoogiaknas **Vali tükk** valige loodud **karbi tüki** killus ja seejärel valige **OK**.
1. Salvestage ja kuvage lehe eelvaade. Lisage eelvaatelehe URL-ile päringustringi parameeter **?productid=&lt;toote ID&gt;**. Sel viisil kasutatakse eelvaatelehe laadimiseks ja renderdamiseks toote konteksti.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**. Toote üksikasjade lehele peaks ilmuma ostukast.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Kaupluse valimise moodul](store-selector.md)

[Meediumigaleriimoodul](media-gallery-module.md)

[Konteinermoodul](add-container-module.md)

[Ostukorvimoodul](add-cart-module.md)

[Maksmismoodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päisemoodul](author-header-module.md)

[Jalusemoodul](author-footer-module.md)

[Sotsiaalmeedias jagamise moodul](social-share-module.md)

[Lisage toode ostukorvi sätted](add-cart-settings.md)

[Varude saadavuse arvutamine jaemüügikanalite jaoks](calculated-inventory-retail-channels.md)

[SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
