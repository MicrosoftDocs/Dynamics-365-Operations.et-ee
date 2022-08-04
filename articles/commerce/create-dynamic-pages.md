---
title: URL-i parameetrite põhjal dünaamiliste e-kaubanduslehtede loomine
description: See artikkel kirjeldab, kuidas seadistada Microsoft Dynamics 365 Commerce URL-parameetritel põhinevat dünaamilist sisu teenindava e-kaubanduse lehe.
author: StuHarg
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.openlocfilehash: 83e20d9fc655a474a11521ec61d0b64d30603181
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169126"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a>URL-i parameetrite põhjal dünaamiliste e-kaubanduslehtede loomine

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada Microsoft Dynamics 365 Commerce URL-parameetritel põhinevat dünaamilist sisu teenindava e-kaubanduse lehe.

E-kaubanduse lehte saab konfigureerida URL-i tee segmendi põhjal erinevat sisu esitama. Seepärast nimetatakse seda lehte dünaamiliseks leheks. Segmenti kasutatakse lehe sisu toomise parameetrina. Näiteks saidikonstruktoris loodud ja nimeline Vieweri nimeline **\_ lehekülg** vastendatakse URL-iga `https://fabrikam.com/blog`. Seejärel saab seda lehte kasutada URL-i tee viimasel segmendil põhineva erineva sisu näitamiseks. URL-i `https://fabrikam.com/blog/article-1` viimane segment on näiteks **artikkel 1**.

Saate ka alistada parameetrilise URL-i segmendi saidikonstruktori lehega. Näiteks saab lehe, mis luuakse saidikonstruktoris ja mille **nimeks on nimeline kokkuvõte\_**, vastendada URL-iga `https://fabrikam.com/blog/about-this-blog`. Kui URL-ile `https://fabrikam.com/blog` on lõpus segmendiks määratud, `/about-this-blog` tagastatakse sel juhul lehe **\_**`/about-this-blog` lõppsegmendi sisu, mitte lehe kasutatava parameetrina.`https://fabrikam.com/blog` 

Dünaamilisele lehele edastatavate parameetrite nimede valimisel ei saa dünaamilise lehe nime, nagu see ilmub URL-is (`/blog` ülaltoodud näites), kasutada parameetri nimena või parameetri nime alamstringina. 

> [!NOTE]
> Dünaamilise lehe sisu hostimise, toomise ja näitamise funktsioon rakendatakse kohandatud mooduli abil. Lisateavet vt teemast [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).

## <a name="set-up-a-dynamic-e-commerce-page"></a>Dünaamilise e-kaubanduse lehe seadistamine

Dünaamilise e-kaubanduse lehe seadistamiseks peate looma dünaamilise lehe ja baas-URL-i ning konfigureerima marsruudi dünaamilisele lehele.

### <a name="create-the-page-that-will-serve-dynamic-content"></a>Dünaamilist sisu esitava lehe loomine

Dünaamilist sisu esitava lehe loomiseks järgige teemas [Uue saidilehe lisamine](add-new-page.md) kirjeldatud etappe. Loodava lehe puhul tuleb rakendada moodul, mis kasutab välisest andmeallikast sisu toomiseks URL-i viimast segmenti. Lisateavet kohandatud mooduli arenduse kohta vt teemast [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).

### <a name="create-the-base-url-for-the-dynamic-page"></a>Dünaamilise lehe baas-URL-i loomine

Commerce'i saidiehitajas dünaamilise lehe baas-URL-i loomiseks järgige neid etappe.

1. Avage **URL-id** ja valige **Uus \> Uus URL**.
1. Tehke dialoogiboksis **Loo uus URL** valik **Sisemine leht**. Sisestage väljale **URL-i tee** tee, mis toimib dünaamilise lehe juurena (selles näites **/blog**). Seejärel valige **Järgmine**.
1. Valige dialoogiboksis **Lehe valimine** dünaamilise lehena kasutamiseks loodud leht ja seejärel valige käsk **Salvesta**.
1. Valige **Avalda**.

### <a name="configure-the-route-to-the-dynamic-page"></a>Dünaamilise lehe marsruudi konfigureerimine

Commerce'i saidiehitajas dünaamilise lehe marsruudi konfigureerimiseks järgige neid etappe.

1. Avage **Saidi sätted \> Laiendused**.
1. Valige jaotises **Parametriseeritud URL-i teed** käsk **Lisa** ja seejärel sisestage URL-i loomisel sisestatud URL-i tee (selles näites **/blog**).
1. Valige käsk **Salvesta ja avalda**.

Kui marsruut on konfigureeritud, tagastavad kõik parametriseeritud URL-i tee taotlused selle URL-iga seotud lehe. Kui mõni taotlus hõlmab lisasegmenti, tagastatakse seostatud leht ja lehe sisu toomiseks kasutatakse parameetrina segmenti. Näiteks annab `https://fabrikam.com/blog/article-1` / `https://fabrikam.com/blog` article-1 parameetri abil toodud **sisu kuvava lehe** tagasi.

## <a name="override-a-parameterized-url-with-a-custom-page"></a>Kohandatud lehega parametriseeritud URL-i alistamine

Commerce'i saidiehitajas kohandatud lehega parametriseeritud URL-i alistamiseks toimige järgmiselt.

1. Avage **URL-id** ja valige **Uus \> Uus URL**.
1. Tehke dialoogiboksis **Loo uus URL** valik **Sisemine leht**. Sisestage väljal **URL-i tee** tee, mis hõlmab alistatavat segmenti (selles näites **/blog/about-this-blog**). Seejärel valige **Järgmine**.
1. Valige dialoogiboksis **Lehe valimine** kohandatud leht ja seejärel valige käsk **Salvesta**.
1. Valige **Avalda**.
1. Kui kohandatud leht ei ole veel avaldatud, avage jaotis **Lehed**, valige kohandatud leht ja seejärel valige käsk **Avalda**.

Pärast kohandatud lehe avaldamist esitatakse see parametriseeritud sisuga dünaamilise lehe asemel.

## <a name="additional-resources"></a>Lisaressursid

[Olemasoleva saidilehe muutmine](modify-existing-page.md)

[Uue saidilehe lisamine](add-new-page.md)

[Lehepaigutuste valimine](select-page-layouts.md)

[SEO metaandmete haldamine](manage-seo-metadata.md)

[Lehe salvestamine, eelvaade ja avaldamine](save-preview-publish-page.md)

[Tootelehe rikastamine](enrich-product-page.md)

[Kategooria sihtlehe rikastamine](enrich-category-page.md)

[Lehe sisu hõlbustusfunktsioonide kinnitamine](verify-accessibility.md)

[Võrgukanali laiendatavus](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
