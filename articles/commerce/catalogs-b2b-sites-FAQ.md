---
title: B2B-saitide Commerce'i kataloogide KKK
description: See artikkel annab vastused korduma kippuvatele kataloogide Microsoft Dynamics 365 Commerce küsimustele.
author: ashishmsft
ms.date: 07/15/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 68c648c5caf2667f413b236dc437fc2c74c40d07
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168981"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>B2B-saitide Commerce'i kataloogide KKK

[!include [banner](includes/banner.md)]

See artikkel annab vastused korduma kippuvatele küsimustele Microsoft Dynamics 365 Commerce [ettevõtete -ettevõtete (B2B) kataloogide kohta](catalogs-b2b-sites.md).

### <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Miks ei saa ma konfigureerida kataloogiomast navigeerimishierarhiat või näha valikut kliendi hierarhia seostamiseks?

Veenduge, **et jaemüügikanalite funktsioonis mitme kataloogi kasutamise lubamine on Commerce headquartersi** **funktsioonihalduse tööruumis** lubatud ja et teie keskkond on Commerce version 10.0.27 või uuem väljalase. Veenduge, et valisite kataloogitüübis **B2B** **·**.

### <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Kas commerce'i saidiloojas saab vaadata kataloogiomast hierarhiat ja rikastada kategoorialehti?

Jah, Ärisaidi looja kasutajad, kellel **on** juurdepääs saidikonstruktori toodete lehele, saavad valida kataloogi ja vaadata kataloogiomast hierarhiat. Kasutajad saavad **leheküljel** Tooted rikastada ka kataloogis määratud kategooria kategooria lehekülge. Lisateavet vaadake teemast [Kategooria sihtlehe rikastamine](enrich-category-page.md). Kui soovite kataloogile omast rikastamist, soovitame teil selle kataloogi jaoks luua selge ja kordumatu navigeerimishierarhia.

### <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Kas B2B ostu saab ühe väljaregistreerimise puhul mitmest kataloogist osta?

Jah, ostud mitmest kataloogist ühe väljaregistreerimise puhul on lubatud. B2B ostlejad saavad kasutada ostukorvi vaates kataloogi indikaatorit, et määrata, millistest kaupadest kataloogid lisati.

### <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Kui B2B ostja ostab sama kaupa erinevatest kataloogidest, siis milline on eeldatav käitumine?

Kuigi antud kasutajal võib olla antud ajal juurdepääs mitmele kataloogile, on eeldamine, et nendes kataloogides toodud tooted on üksteist välistavad. Ideaaljuhul ei tohiks sama toode olla antud kasutaja puhul rohkem kui ühe kataloogi osa.

Kuid kui tekib olukord, kus sama toode kuulub mitmesse kataloogi, haldab süsteem selle toote jaoks mitut ostukorvi rida. Igal kataloogil on eraldi rida. Sama toodet kahest erinevast kataloogist ei ühendata väljaregistreerimise ajal.

### <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Kui B2B ostja ostab, kas on olemas kataloogi saadavuse kinnitus?

Jah. B2B ostjal on lubatud väljaregistreerida ainult juhul, kui kõik ostukorvisolevad kaubad on kehtivatest kataloogidest. Kui mõni ostukorvi toode on aegunud või tagasi võetud kataloogidest, eemaldatakse need ja kasutajat teavitatakse.

### <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Kas otsitakse ja tuvastatakse ostukogemuse ajal kataloogispetsiifilisi (sh seotud ja soovitatud tootekogumeid)?

Jah. Kohe, kui kasutaja valib kindla kataloogi, saab terve ostutee kataloogipõhiseks. See reisikogemus sisaldab toote tuvastamiskogemusi, nagu otsingusoovitused, otsingutulemused, kategooria tulemused, täpsustajad, hinnad, atribuudid ja soovitatud tooted (nt uued, parimate müükidena, trendidena kasutatavad, sageli koos ostetud tooted ja seotud tooted).

### <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Kas B2B ost tuleks osta vaikesortimendist (catalogID=0)?

Ei, B2B-ostjal pole lubatud vaikesortimendist osta. See sortiment on mõeldud ainult anonüümseks sirvimiseks. Kui B2B ostjal puuduvad kataloogi määramised (administratsiooni ootel värskendused), ei saa nad näha ühtegi kataloogi, mille vahel nad saavad valida ja ükski kategooriahierarhia pole nähtaval.

### <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Kas turunduse sisu saab kataloogile omase toote puhul muuta?

Praegu toetatakse toote rikastamist ainult saidi ja kanali tasemel. Teiste sõnadega, kui toode on rikastatud ja mitme kataloogi vahel ühiskasutuses, renderdatakse vastavaid selle toote rikastatud toote üksikasjade lehekülge (PDP) samal viisil läbi kõikide kataloogide. 

### <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Kas kataloogitugi on saadaval nii B2B kui ka ettevõtte ja tarbija (B2C) võrgukanalite jaoks?

Praegu on ärikataloogid mõeldud töötama ainult B2B võrgukanalitega.

### <a name="a-new-customer-was-added-to-the-customer-hierarchy-or-a-new-hierarchy-was-associated-with-the-catalog-but-the-catalog-is-not-available-to-the-user-why"></a>Uus klient lisati kliendi hierarhiasse või seostati kataloogiga uus hierarhia, kuid kataloog pole kasutajale saadaval. Miks?

Veenduge, et käivitate **1010** tööd pärast uue kliendi seostamist olemasoleva kliendihierarhiaga ja kui lõite uue kliendihierarhia. Kliendi hierarhiaga seostatud kataloogid on nähtavad **ainult pärast 1010** töö edukat lõpetamist. Kui kataloog on ka uus, veenduge **, et käivitate nii 1150-töö** (kataloog) **kui ka 1010-tööd**. Nagu mis tahes uue kataloogi puhul, lubage mõnel ajal andmeid kanaliga ja otsinguindeksiga sünkroonida. Kui töö olek on Rakendatud, tähendab see, et andmed sünkroonitakse kanali andmebaasi, kuid andmete sünkroonimiseks otsinguindeksiga on vaja lisaaega. 

### <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Kas me võime seadistada kataloogispetsiifilisi kauba edasi-/edasim müügiüksusi?

Praegu toetatakse ainult seotud toodete funktsioone. Kõnekeskuste jaoks on saadaval kaupade üles- ja ristm müügikonfiguratsioonid.

Järgmisi funktsioone toetatakse ka ainult kõnekeskuste puhul:

- Kataloogi lähtekoodid
- Allika ID-de kasutamine kulude ja vastuse määrade jälgimiseks
- Kataloogipõhine tellimus ja kaubaskriptid
- Kataloogi lehekülje analüüs
- Kataloogi taotlused
- Maksegraafikud
- Lähtekoodil põhinevad tasuta tooted

### <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Kas me võime e-äriportaali kaudu kasutada B2B-tellimuste kataloogi lähtekoode?

Ei. Kataloogi lähtekoodid on toetatud ainult kõnekeskuse kanalite puhul.

## <a name="additional-resources"></a>Lisaressursid

[B2B-saitide Commerce'i kataloogide loomine](catalogs-b2b-sites.md)

[Kataloogi valija moodul](catalog-picker.md)

[B2B-kohanduste Commerce'i kataloogide laiendatavus](catalogs-b2b-sites-dev.md)
