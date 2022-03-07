---
title: Päise moodul
description: See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: afdc12230ebad3d5db59c384b2f1066d2c7929339f282ed4880ff967b1fd2d8b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712786"
---
# <a name="header-module"></a>Päisemoodul

[!include [banner](includes/banner.md)]

See teema hõlmab päise mooduleid ja kirjeldab, kuidas lehe päiseid rakenduses Microsoft Dynamics 365 Commerce luua.

Rakenduses Dynamics 365 Commerce konfigureeritakse lehe päis lehe fragmentina, mis sisaldab päise-, reklaambänneri ja küpsistega nõustumise mooduleid. 

Päise moodul sisaldab saidi logo, linke navigeerimise hierarhiale, linke teistele saidi lehekülgedele, ostukorvi ikooni moodulit, soovinimekirja sümbolit, sisselogimise suvandeid ja otsinguriba. Päise moodul optimeeritakse automaatselt seadmele, millega saiti vaadatakse (teisisõnu töölauga seade või mobiilne seade). Näiteks mobiilses seadmes on navigeerimisriba ahendatud nupule **Menüü** (mida nimetatakse mõnikord ka *hamburgerimenüüks*).

Järgmisel pildil on näide päise moodulist avalehel.

![Päise mooduli näide.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Päise mooduli atribuudid

Päise moodul toetab atribuute **Logo pilt**, **Logo link** ja **Minu konto lingid**. 

Lehel logo määratlemiseks kasutatakse atribuute **Logo pilt** ja **Logo link**. Lisateavet vt jaotisest [Logo lisamine](add-logo.md). 

Atribuuti **Minu konto lingid** saab kasutada konto lehtede määratlemiseks, millele saidi omanik soovib päises kiirlinke kuvada.

## <a name="modules-that-are-available-within-a-header-module"></a>Päise moodulis saadaolevad moodulid

Päise moodulis saab kasutada järgmisi mooduleid.

- **Navigeerimismenüü** – navigeerimismenüü tähistab kanali navigeerimishierarhiat ja teisi staatilisi navigeerimislinke. Lisateavet vt teemast [Navigeerimismenüü moodul](nav-menu-module.md).

- **Otsing** – otsingu moodul võimaldab kasutajatel sisestada otsinguterminid toodete otsimiseks. Vaikimisi otsingulehe URL ja otsingupäringu parameetrid peavad olema antud jaotises **Saidi sätted \> Laiendused**. Otsingu moodulil on atribuudid, mis võimaldavad teil vajadusel otsingunupu peita või soovikohaselt sildistada. Otsingumoodul toetab ka automaatse soovitamise valikuid, näiteks nagu toote, võtmesõna ja kategooria otsitulemused.

- **Ostukorvi ikoon** – ostukorvi ikooni moodul tähistab ostukorvi ikooni, mis näitab ostukorvis olevate kaupade arvu igal ajahetkel. Lisateavet vt teemast [Ostukorvi ikooni moodul](cart-icon-module.md).

- **Saidi valija** – saidi valija moodul võimaldab kasutajatel sirvida erinevatel eelmääratletud saitidel, mis põhinevad turul, piirkondadel ja lokaatidel. Lisateabe saamiseks vt [Saidi valija moodul](site-selector.md).

- **Kaupluse valija** – kaupluse valija moodulit saab lisada päise mooduli kaupluse valija pessa. Kasutajad saavad selle abil sirvida ja leida lähedalasuvaid kauplusi. Kasutajad saavad määrata ka eelistatud kaupluse. See kauplus kuvatakse seejärel päises. Kui kaupluse valija moodul on lisatud päise moodulisse, peab selle atribuudi **Režiim** väärtuseks olema seatud **Kaupluste otsimine**. Lisateabe saamiseks vt [Kaupluse valija moodul](store-selector.md).

> [!NOTE]
> - Ostukorvi ikooni mooduli kasutamise tugi päise moodulis on saadaval kui väljalaskes Dynamics 365 Commerce versioonis 10.0.11.
> - Ostukorvi ikooni mooduli kasutamise tugi päise moodulis on saadaval kui väljalaskes Dynamics 365 Commerce versioonis 10.0.14.
> - Ostukorvi ikooni mooduli kasutamise tugi päise moodulis on saadaval kui väljalaskes Dynamics 365 Commerce versioonis 10.0.15.

## <a name="header-module-in-the-adventure-works-theme"></a>Päisemoodul Adventure Worksi kujunduses

Adventure Worksi teemas toetab päisemoodul **mobiilse logo** atribuuti. See atribuut võimaldab määrata logo mobiili vaateportide jaoks. Atribuut **Mobiilne logo** on saadaval mooduli definitsiooni laiendina.

> [!IMPORTANT]
> Adventure Works teema on saadaval alates Dynamics 365 Commerce väljalaske versioonist 10.0.20.

## <a name="create-a-header-fragment-for-a-page"></a>Lehele päise fragmendi loomine

Päise fragmendi loomiseks tehke järgmist.

1. Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.
1. Valige dialoogiboksis **Uus fragment** moodul **Konteiner**, sisestage fragmendi nimi ja valige seejärel **OK**.
1. Valige pesa **Vaikekonteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida ekraan**.
1. Valige pesas **Vaikekonteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodulid **Küpsistega nõustumine**, **Päis** ja **Reklaambänner** ning seejärel valige **OK**.
1. Tehke mooduli **Reklaambänner** atribuutide paanil valikud **Lisa teade** ja **Teade**.
1. Lisage dialoogiaknas **Teade** reklaami tekst ja lingid ning klõpsake seejärel nuppu **OK**.
1. Lisage ja konfigureerige mooduli **Küpsistega nõustumine** atribuutide paanil tekst ja link, mis suunab saidi privaatsuspoliitika lehele.
1. Valige päise mooduli pesas **Navigeerimismenüü** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Navigeerimismenüü** ja klõpsake seejärel **OK**.
1. Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Navigeerimismenüü allikas** valik **Jaemüügiserver**.
1. Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Staatilised menüü-üksused** valikud **Lisa menüü-üksus** ja **Menüü-üksus**. 
1. Sisestage dialoogiboksi **Menüü-üksus** jaotisse **Menüü-üksuse tekst** tekst „Kontakt”.
1. Klõpsake dialoogiboksi **Menüü-üksus** jaotises **Menüü-üksuse lingi sihtkoht** käsku **Lisa link**.
1. Valige dialoogiaknas **Lisa link** saidi lehe „Kontakt” URL ning seejärel valige **OK**.  
1. Tehke dialoogiaknas **Menüü-üksus** valik **OK**.
1. Valige päise mooduli pesas **Otsing** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Otsing** ja klõpsake seejärel **OK**.
1. Konfigureerige otsingumooduli atribuutide paanil vajaduse järgi atribuudid.
1. Valige päise mooduli pesas **Ostukorvi ikoon** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Ostukorvi ikoon** ja klõpsake seejärel **OK**.
1. Konfigureerige ostukorvi ikooni mooduli atribuutide paanil vajaduse järgi atribuudid. Kui soovite, et ostukorvi ikoon kuvaks ostukorvi kokkuvõtet (tuntud ka kui miniostukorv), kui kasutaja hiirt selle kohal hoiab, siis valige **Kuva miniostukorv**.
1. Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Päise igal lehel kuvamise tagamiseks järgige neid samme iga malli jaoks, mis on saidi jaoks loodud.

1. Lisage mooduli **Vaikeleht** pesas **Päis** loodud jaluse fragment.
1. Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukorvi ikooni moodul](cart-icon-module.md)

[Kampaania ribareklaami moodul](add-alert.md)

[Navigeerimismenüü moodul](nav-menu-module.md) 

[Küpsistega nõustumine](cookie-consent-module.md)

[Jalusemoodul](author-footer-module.md)

[Saidi valija moodul](site-selector.md)

[Kaupluse valimise moodul](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
