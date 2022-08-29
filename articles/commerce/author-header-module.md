---
title: Päisemoodul
description: See artikkel katab päisemoodulid ja kirjeldab, kuidas luua lehekülje päiseid moodulis Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 63c298f36f64f2e107d3df3c0c5f3b6445546aa1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275781"
---
# <a name="header-module"></a>Päisemoodul

[!include [banner](includes/banner.md)]

See artikkel katab päisemoodulid ja kirjeldab, kuidas luua lehekülje päiseid moodulis Microsoft Dynamics 365 Commerce.

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
1. Dialoogiaknas **Vali** tükk valige **konteinerimoodul**, sisestage killu nimi ja seejärel valige **OK**.
1. Valige pesa **Vaikekonteiner** ja seejärel määrake parempoolsel atribuutide paanil atribuudi **Laius** väärtuseks **Täida ekraan**.
1. **Valige konteineri vaikepesas** kolmikpunkt (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali moodulid** valige küpsistega **nõustumine**, **päis ja** **Kampaania lisamoodulid** ning seejärel valige **OK**.
1. Tehke mooduli **Reklaambänner** atribuutide paanil valikud **Lisa teade** ja **Teade**.
1. Lisage dialoogiaknas **Teade** reklaami tekst ja lingid ning klõpsake seejärel nuppu **OK**.
1. Lisage ja konfigureerige mooduli **Küpsistega nõustumine** atribuutide paanil tekst ja link, mis suunab saidi privaatsuspoliitika lehele.
1. Päisemooduli **navigeerimismenüü** pesas valige ellips (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige navigeerimismenüü **ja** seejärel valige **OK**.
1. Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Navigeerimismenüü allikas** valik **Jaemüügiserver**.
1. Tehke navigeerimismenüü mooduli atribuudipaani jaotises **Staatilised menüü-üksused** valikud **Lisa menüü-üksus** ja **Menüü-üksus**. 
1. Sisestage dialoogiboksi **Menüü-üksus** jaotisse **Menüü-üksuse tekst** tekst „Kontakt”.
1. Klõpsake dialoogiboksi **Menüü-üksus** jaotises **Menüü-üksuse lingi sihtkoht** käsku **Lisa link**.
1. Valige dialoogiaknas **Lisa link** saidi lehe „Kontakt” URL ning seejärel valige **OK**.  
1. Tehke dialoogiaknas **Menüü-üksus** valik **OK**.
1. Päisemooduli **otsingupesas** valige ellips (**...**) ja seejärel valige **lisamoodul**.
1. Dialoogiaknas **Vali** moodulid valige otsingumoodul **ja** seejärel valige **OK**.
1. Konfigureerige otsingumooduli atribuutide paanil vajaduse järgi atribuudid.
1. Päisemooduli **ostukorvi ikoonipesas valige ellips (**...**) ja seejärel valige lisamoodul** **.**
1. Dialoogiaknas **Vali** moodulid valige ostukorvi **ikoonimoodul** ja seejärel valige **OK**.
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
