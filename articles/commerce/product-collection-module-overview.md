---
title: Tootekogumi moodulid
description: See teema annab ülevaate tootekogumi moodulitest rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2d19cac142b870d8ecc677665443602b0a8837d2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411545"
---
# <a name="product-collection-modules"></a>Tootekogumi moodulid


[!include [banner](includes/banner.md)]

See teema annab ülevaate tootekogumi moodulitest rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Toote tuvastus on esmane tööriist, mida jaemüüjad kasutavad oma klientidega suhtlemiseks e-kaubanduse veebisaidil. Tootekogumi moodulid aitavad jaemüüjatel luua meeldejäävaid ostlemise kogemusi, pakkudes intuitiivset visuaalset liidest, mida saab kasutada tootekogumite kiireks loomiseks.

Tootekogumi moodulid esindavad füüsilisi tooteid ja teenuseid veebisaidil. Tootekogumi moodul on tavaliselt seotud üksikasjade lehega, kus kliendid saavad osta toodet või teenust või selle kohta lisateavet lugeda. 

Tootekogumite allikad võivad olla järgmised nelja tüüpi loendid.

- Toodete toimetusloendid, mis on toote või toote loendite puhul rakenduses Dynamics 365 Commerce käsitsi määratletud seotud toodetena.
- Algoritmilised loendid, nt uute, enim müüdud või populaarsete toodete loendid
- Soovituste loendid, mis põhinevad arvuti õppimisel
- Isikupärastamise loendid, mis toetavad kliendi isikupärastatud tulemusi. Isikupärastatud tulemuste nägemiseks peavad kliendid olema e-kaubanduse saidile sisse logitud. Külaliskasutajad ei näe isikupärastatud tulemusi. Kliendid saavad isikupärastamisest loobuda [kontohalduse lehel](account-management.md).

Järgmisel joonisel on kujutatud e-kaubanduse saidil kasutatavat erinevat tüüpi tootekogumeid.

![Näide e-kaubanduse saidi erinevatest tootekogumitest](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Kasutage alati tootekogumi mooduleid, et näidata sarnast tüüpi toodete gruppi.

## <a name="product-collection-modules-and-types"></a>Tootekogumi moodulid ja tüübid

Järgmises tabelis kirjeldatakse erinevate tootekogumi moodulite tüüpe rakenduses Dynamics 365 Commerce.

| Tootekogumi moodul  | Tüüp | Kirjeldus |
|----------------------------|------|-------------|
| Kategooria                   | Kategooria | Selles moodulis kuvatakse kategooria toodete loend, mis on määratletud navigeerimiskategooria hierarhia poolt, mille jaemüüja on kanali jaoks loonud. |
| Seotud tooted           | Kureeritud | See moodul näitab toodete loendit, mida kauba haldur on konfigureerinud seotud toodetena rakenduses Commerce autori valitud seose tüübi jaoks. |
| Otsingutulemused             | Otsingupäring | Seda tüüpi tootekogumi moodul näitab toodete loendit, mis kõige paremini ühtib kliendi sisestatud otsingupäringuga. |
| Kureeritud toodete loend      | Kureeritud | See moodul kuvab kohandatud loendi, mille kaupmehed ja toimetajad on rakenduses Commerce loonud. |
| Uus                        | Algoritmiline | See moodul kuvab uusimate toodete loendi, mis on kanalitele ja kataloogidele valitud. See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi. |
| Enim müüdud               | Algoritmiline | See moodul kuvab toodete loendi, mis on järjestatud kõige suurema müügi arvu alusel. See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi. |
| Populaarsed                   | Algoritmiline | See moodul kuvab antud perioodi kõrgeima jõudlusega toodete loendi. See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi. |
| Kliendid ostavad sageli koos | Tehisintellekt/masina õppimine | See moodul kasutab masinõpet, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mida sageli ostetakse koos valitud tootega. See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi. |
| Inimestele meeldib ka           | Tehisintellekt/masina õppimine | See moodul kasutab masinõpet, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mis on seotud valitud tootega. See loend võib kuvada sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi. |
| Valib teile              | Tehisintellekt/masina õppimine | See moodul kasutab masinõpet, et analüüsida sisselogitud kasutaja ostumustreid ja pakkuda isikupärastatud soovitusi, mis põhinevad nendel ostumustritel. Külalisekasutaja jaoks on see loend ahendatud. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Tootekogumi mooduli lisamine kategooria lehele

Tootekogumi mooduli lisamiseks kategooria lehele järgige neid juhiseid.

1. Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.
1. Valige dialoogiboksis **Vali mall** sama mall, mida kasutab teie kategooria vaikeleht. Sisestage jaotises **Lehe nimi** sobiv nimi ja seejärel valige **OK**.
1. Valige pesas **Alamjalus** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.
1. Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.
1. Valige dialoogiboksis **Lisa moodul** moodul **Tootekogum** ja klõpsake seejärel **OK**.  
1. Tootekogumi mooduli atribuutide paanil valige käsk **Lisa tooteloend**.
1. Valige dialoogiboksis **Vali tooteloendi konfiguratsioon** loendi tüüp ja allikas ning sisestage kaupade arv. Konfigureerige kõik muud loendi tüübi puhul saadaolevad suvandid. Lisateavet loendi tüüpide kohta leiate järgnevast tabelist. 
1. Valige nupp **OK**.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

Järgmine tabel näitab loendi tüüpe, mis on saadaval dialoogiaknas **Vali toote loendi konfigureerimine**.

| Tüüp                       | Kirjeldus | Kasutus | Lehe kontekst | Spetsiifiline kontekst | Isikupärastamine |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Tooted kategooriate alusel       | Kindlasse kategooriasse kuuluvate toodete loend. See kategooria määratakse kas lehekülje kontekstist või autori pakutavast kontekstist. | Seda tüüpi loendit saab kasutada mis tahes lehel (nt avaleht, kategooria leht, turunduse leht või toote üksikasjade leht \[PDP\]), et edendada kindlat tootekategooriat. | Lehe konteksti kategooria, kui see on saadaval (nt kategooria leht) | Autor võib anda loendi konteksti jaoks kindla kategooria. | Pole kohaldatav |
| Seotud tooted           | Toodete loend, mille kauba haldaja on konfigureerinud seotud toodetena seoses seose tüübiga rakenduses Commerce. | Seda tüüpi loendit kasutatakse peamiselt PDP-del, kuid seda saab kasutada mis tahes lehel, kui on esitatud ülemtoode. | Toode lehelt, seose tüüp (kohustuslik) | Toote saab valida valijas ja seose tüüp on kasutusel. | Pole kohaldatav |
| Kureeritud                    | Kohandatud loend, mille kaupmehed ja toimetajad on rakenduses Commerce loonud. | Rikastage kategooria lehte, kodulehte, kassa ja ostukorvi lehte ja tootelehti. | Pole kohaldatav | Pole kohaldatav | Pole kohaldatav |
| Algoritmiline                | <ul><li>**Uus** – uusimate toodete loend, mis on valitud kanalitele ja kataloogidele.</li><li>**Enim müüdud** – toodete loend, mis on järjestatud kõige suurema müügi arvu alusel.</li><li>**Populaarsed** – antud perioodi kõrgeima jõudlusega toodete loend.</li></ul> | Koduleht, rikastage kategooria lehte, kassa ja ostukorvi lehti | Lehe konteksti kategooria (nt kategooria leht) | Saidi autori määratud kategooria | Toetatud |
| Kliendid ostavad sageli koos | Loend, mis kasutab masinõpet, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mida sageli ostetakse koos valitud tootega. | See loendi tüüp on kohaldatav ainult ostukorvi lehele. | Ostukorv | Pole kohaldatav | Toetatud |
| Inimestele meeldib ka           | Loend, mis kasutab masina õppimist, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mis on seotud valitud tootega. | Seda loendi tüüpi kasutatakse PDP-del, et kuvada tooted, mida teised kliendid on ostnud. | Toote kontekst lehelt | Saidi autori sisestatud toode | Toetatud |
| Valib teile              | Loend, mis kasutab kliendi eelistuste määramiseks masinõpet. | Seda tüüpi loendit saab kasutada mis tahes lehel. | Pole kohaldatav| Pole kohaldatav | Toetatud | 

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](starter-kit-overview.md)

[Karusellmoodul](add-carousel.md)

[Sisu rikasplokimoodul](add-content-rich-block.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Tootesoovituste ülevaade](product-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]