---
title: Tootekogumi moodulid
description: See teema annab ülevaate tootekogumi moodulitest rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785463"
---
# <a name="product-collection-modules"></a>Tootekogumi moodulid  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema annab ülevaate tootekogumi moodulitest rakenduses Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Toote tuvastus on esmane tööriist, mida jaemüüjad kasutavad oma klientidega suhtlemiseks e-kaubanduse veebisaidil. Tootekogumi moodulid aitavad jaemüüjatel luua meeldejäävaid ostlemise kogemusi, pakkudes intuitiivset visuaalset liidest, mida saab kasutada tootekogumite kiireks loomiseks.

Tootekogumi moodulid esindavad füüsilisi tooteid ja teenuseid veebisaidil. Tootekogumi moodul on tavaliselt seotud üksikasjade lehega, kus kliendid saavad osta toodet või teenust või selle kohta lisateavet lugeda. 

Tootekogumite allikad võivad olla järgmised kolme tüüpi loendid.

- Toodete toimetusloendid, mis on toote või toote loendite puhul rakenduses Dynamics 365 Retail käsitsi määratletud seotud toodetena.
- Algoritmilised loendid, nt uute, enim müüdud või populaarsete toodete loendid
- Soovituste loendid, mis põhinevad arvuti õppimisel

Järgmisel joonisel on kujutatud e-kaubanduse saidil kasutatavat erinevat tüüpi tootekogumeid.

![Näide e-kaubanduse saidi erinevatest tootekogumitest](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Kasutage alati tootekogumi mooduleid, et näidata sarnast tüüpi või kujundusega toodete gruppi.

## <a name="product-collection-modules-and-types"></a>Tootekogumi moodulid ja tüübid

Järgmises tabelis kirjeldatakse erinevate tootekogumi moodulite tüüpe rakenduses Dynamics 365 Commerce.

| Tootekogumi moodul  | Tüüp | Kirjeldus |
|----------------------------|------|-------------|
| Kategooria sirvimine            | Kureeritud | Seda tüüpi tootekogumi moodul kasutab navigeerimise kategooria hierarhiat, mille jaemüüja lõi jaemüügi kanali jaoks, et näidata kindlas saidi kategoorias pakutavate toodete sirvimise voogu. |
| Otsingutulemused             | Otsingupäring | Seda tüüpi tootekogumi moodul näitab toodete loendit, mis kõige paremini ühtib kliendi sisestatud otsingupäringuga. |
| Seotud tooted           | Kureeritud | Seda tüüpi tootekogumi moodul näitab toodete loendit, mida kauba haldur on konfigureerinud seotud toodetena jaemüügis autori valitud seose tüübiga. |
| Kureeritud toodete loend      | Kureeritud | Seda tüüpi tootekogumi moodul näitab kohandatud loendeid, mille kaupmehed ja toimetajad on jaemüügis loonud. |
| Uus                        | Algoritmiline | Seda tüüpi tootekogumi moodul kuvab uusimate toodete loendi, mis on valitud kanalitele ja kataloogidele. |
| Enim müüdud               | Algoritmiline | Seda tüüpi tootekogumi moodul näitab toodete loendit, mis on järjestatud kõige suurema hulga müügitehingute alusel. |
| Populaarsed                   | Algoritmiline | Seda tüüpi tootekogumi moodul näitab kõige kõrgema jõudlusega toodete loendit valitud perioodil. |
| Kliendid ostavad sageli koos | Tehisintellekt/masina õppimine | Seda tüüpi tootekogumi moodul kasutab masina õppimist, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mida sageli ostetakse koos valitud tootega. |
| Inimestele meeldib ka           | Tehisintellekt/masina õppimine | Seda tüüpi tootekogumi moodul kasutab masina õppimist, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mis on seotud valitud tootega. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Tootekogumi mooduli lisamine kategooria lehele

Tootekogumi mooduli lisamiseks kategooria lehele järgige neid juhiseid.

1. Rakenduses Dynamics 365 Commerce, minge saidile ja looge leht, mis kasutab sama malli nagu teie vaikimisi kategooria lehekülg.
1. Lehe liigenduses valige pesa **Alamjalus**, valige kolmikpunkt nupp (**...**) ja seejärel valige suvand **Lisa moodul**.
1. Dialoogiaknas **Lisa moodul** valige suvand **Konteiner** ja seejärel valige nupp **OK**.
1. Valige konteineri moodulis kolmikpunkt nupp ja seejärel valige käsk **Lisa moodul**.
1. Dialoogiaknas **Lisa moodul** valige suvand **Tootekogum** ja seejärel valige nupp **OK**.
1. Konfigureerige sätted, valides tootekogumi jaoks sobiv andmeallikas ja sisend.
1. Tootekogumi mooduli atribuutide paanil valige käsk **Lisa tooteloend**.
1. Dialoogiaknas **Vali tooteloendi konfigureerimine** valige loendi tüüp, sisestage kaupade arv ja valige muud loendi tüübi jaoks saadaolevad suvandid. Lisateavet loendi tüüpide kohta leiate järgnevast tabelist. 
1. Valige nupp **OK**.
1. Salvestage leht ja registreerige see.

Järgmine tabel näitab loendi tüüpe, mis on saadaval dialoogiaknas **Vali toote loendi konfigureerimine**.
   
| Tüüp                       | Kirjeldus | Üldine tava | Kontekst, mida saab tuletada lehekülje kontekstist | Kontekst, mille autor saab lehekülje kontekstile alistada |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Tooted kategooriate alusel       | Kindlasse kategooriasse kuuluvate toodete loend. See kategooria määratakse kas lehekülje kontekstist või autori pakutavast kontekstist. | Rikastage kategooria lehte, kodulehte, kassa ja ostukorvi lehte ja tootelehti. | Kategooria | Autori määratud kategooria |
| Seotud tooted           | Toodete loend, mida kauba haldaja on konfigureerinud seotud toodetena jaemüügis seoses seose tüübiga. | Tootelehed, kassa ja ostukorvi leht, soovide leht ja kliendikonto leht | Toode, seose tüüp (kohustuslik)  | Toode, seose tüüp |
| Kureeritud                    | Kohandatud loend, mille kaupmehed ja toimetajad on jaemüügis loonud. | Rikastage kategooria lehte, kodulehte, kassa ja ostukorvi lehte ja tootelehti. | Pole kohaldatav | Loendi valija |
| Algoritmiline                | <ul><li>**Uus** – uusimate toodete loend, mis on valitud kanalitele ja kataloogidele.</li><li>**Enim müüdud** – toodete loend, mis on järjestatud kõige suurema müügi arvu alusel.</li><li>**Populaarsed** – antud perioodi kõrgeima jõudlusega toodete loend.</li></ul> | Koduleht, rikastage kategooria lehte, kassa ja ostukorvi lehti | Kategooria | Autori määratud kategooria |
| Kliendid ostavad sageli koos | Loend, mis kasutab masina õppimist, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mida sageli ostetakse koos valitud tootega. | Toote leheküljed, kassa ja ostukorvi lehed | Toode, ostukorv | Kaasa ostukorvi |
| Inimestele meeldib ka           | Loend, mis kasutab masina õppimist, et analüüsida tarbija ostumustreid ja soovitada seotud kaupu, mis on seotud valitud tootega. | Toote leheküljed, kassa ja ostukorvi lehed | Toode, ostukorv | Pole kohaldatav |

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Karusellmoodul](add-carousel.md)

[Sisurikas plokimoodul](add-content-rich-block.md)

[Sisupaigutusmoodul](add-content-placement-modules.md)

[Konteineri moodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

