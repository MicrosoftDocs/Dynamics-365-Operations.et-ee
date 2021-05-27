---
title: Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas
description: Selle teema all kirjeldatakse, millal ja kuidas seadistada kanali kohta mitme Microsoft Azure Active Directory (Azure AD) äri-tarbija (B2C) üürnikut kasutaja autentimiseks spetsiaalses Dynamics 365 Commerce keskkonnas .
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: c813adb79ae1b78a052332e077393f125830633f
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027718"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas

[!include [banner](includes/banner.md)]

Selle teema all kirjeldatakse, millal ja kuidas seadistada kanali kohta mitme Microsoft Azure Active Directory (Azure AD) äri-tarbija (B2C) üürnikut kasutaja autentimiseks spetsiaalses Dynamics 365 Commerce keskkonnas .

Dynamics 365 Commerce kasutab Azure AD B2C pilve identiteediteenust kasutaja mandaadi ja autentimisvoogude toetamiseks. Kasutajad saavad kasutada autentimise voogusid, et registreeruda, sisse logida ja lähtestada oma parool. Azure AD B2C talletab kasutaja tundliku autentimisteabe, nagu näiteks kasutajanimi ja parool. Kasutajakirje on kordumatu iga B2C rentniku jaoks ja see kasutab kasutajanime (meiliaadressi) mandaate või sotsiaalse identiteedi pakkuja mandaati.

Enamikul juhtudel kasutatakse Kaubanduskeskkonnas Azure AD ühte B2C rentnikku. Kaubanduskliendid saavad seejärel luua ja avaldada mitu saiti samas Kaubanduskeskkonnas ja kõigil nendel saitidel kasutatakse sama kliendimandaati. Kui aga keskkonna saite käsitletakse erinevate kaubamärkidena ja need ilmuvad kasutajatele eraldiseisvate ettevõtetena, saab B2C rentnikku konfigureerida kanalile, mida kasutatakse saidi/kaubamärgi eristamiseks.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Kaalutlused mitme B2C rentniku seadistamiseks kanali kohta

Sageli, kui iga kanalit või saiti käsitletakse eraldiseisva ettevõttena, on parim valik, mis puudutab kasutaja autentimise voogusid Kaubanduses, kasutada eraldiseisvaid juriidilisi isikuid. Kui aga soovite hoida iga kanalit/saiti samas keskkonnas ja juriidilises isikus, kuid soovite iga saidi puhul eraldi kasutaja autentimist, peate enne jätkamist arvestama järgmiste punktidega:

- Kasutajatel on igal kanalil/saidil eraldi mandaat.

    Ühel isikul võib olla kaks eraldi kontot kanali/saidi kohta, sest iga konto on kordumatu sisend eraldi B2C rentnikusse.

- Keskkonnas Microsoft Dynamics tagastatakse globaalsete kirjete otsingutel eraldi kliendikirjed.

    Kui kasutaja kasutab sama meiliaadressi kõigil kanalitel/saitidel, tagastavad globaalse kliendiotsingu tulemused iga kanali/saidi kohta. (Kuvatakse kanali indikaator.)

- Aadressiraamatut saab kasutada kasutajate rühmitamiseks, nii et neid saab jälgida kanalite kaupa.
- Kliendi kirjete arv kanali kohta võib suureneda ja see suurenemine võib mõjutada globaalse kliendiotsingu jõudlust.
- B2C rentnikud peavad olema kanaliga hoolikalt vastendatud, et aidata vältida olukordi, kus kliendid registreerivad vale rentniku. Vastasel juhul võib tekkida segadus või jälgimisprobleem.

Järgmisel joonisel on kujutatud mitut B2C rentnikku Kaubanduskeskkonnas.

![Mitu B2C rentnikku Kaubanduskeskkonnas](media/MultiB2C_In_Environment.png)

Kui otsustate, et teie ettevõte vajab kanali kohta eraldiseisvaid B2C rentnikke samas Kaubanduskeskkonnas, täitke selle funktsiooni taotlemiseks järgmiste jaotiste protseduurid.

## <a name="configure-b2c-tenants-in-your-environment"></a>B2C rentnike konfigureerimine oma keskkonnas

B2C rentnike konfigureerimiseks oma keskkonnas täitke selle jaotise vastavad protseduurid.

### <a name="add-an-azure-ad-b2c-tenant"></a>Lisa Azure AD B2C rentnik

Et lisada Azure AD B2C rentnik oma keskkonda, toimige järgmiselt.

1. Logige sisse oma keskkonna Kaubanduse saidiehitusse süsteemi administraatorina. Azure AD B2C rentnike konfigureerimiseks peate olema Kaubanduskeskkonna süsteemiadministraator.
1. Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.
1. Valige **B2C sätted** ja seejärel valige **Halda**.
1. Valige **Lisa B2C rakendus** ja siis sisestage järgmine teave:

    - **Rakenduse nimi**: sisestage nimi, mida tuleks rakenduse Kaubandus haldamise kontekstis kasutada. Soovitame kasutada rakenduse nime, mille valisite, kui seadistasite Azure AD B2C rakenduse portaalis Azure. Sel viisil saate aidata vähendada segadust, kui te haldate B2C rentnikke Kaubanduses.
    - **Rentniku nimi**: sisestage B2C rentniku nimi, nagu see kuvatakse portaalis Azure.
    - **Unustatud parooli poliitika ID**: sisestage poliitika ID (portaali Azure poliitika nimi).
    - **Registreerumise poliitika ID**: sisestage poliitika ID (portaali Azure poliitika nimi).
    - **Kliendi GUID**: sisestage Azure AD B2C rentniku ID, nagu see kuvatakse portaalis Azure (mitte B2C rentniku rakenduse ID).
    - **Profiili redigeerimise poliitika ID**: sisestage poliitika ID (portaali Azure poliitika nimi).

1. Kui olete selle teabe sisestamise lõpetanud, valige muudatuste salvestamiseks **OK**. Teie uus Azure AD B2C rentnik peaks nüüd ilmuma loendisse **B2C rakenduste haldamine**.

> [!NOTE]
> Peaksite jätma tühjaks väljad **Ulatus**, **Mitteinteraktiivse poliitika ID**, **Mitteinteraktiivse kliendi ID**, **Sisselogimise kohandatud domeeni** ja **Registreerimise poliitika ID**, kui Dynamics 365 Commerce meeskond ei käsi teil neid seada.


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Azure AD B2C rentniku haldamine või kustutamine

1. Logige sisse oma keskkonna Kaubanduse saidiehitusse süsteemi administraatorina. Azure AD B2C rentnike konfigureerimiseks peate olema Kaubanduskeskkonna süsteemiadministraator.
1. Vasakpoolsel navigeerimispaanil valige suvand **Rentniku sätted** selle laiendamiseks.
1. Valige **B2C sätted** ja seejärel valige **Halda**.
1. B2C rentniku redigeerimiseks valige selle kõrval olev pliiatsisümbol. B2C üürniku kustutamiseks valige selle kõrval prügikastisümbol.
1. Valige **Salvesta** ja seejärel valige muudatuste aktiveerimiseks käsk **Avalda** .

> [!WARNING]
> Kui B2C rentnik on konfigureeritud aktiivse/avaldatud saidi jaoks, võivad kasutajad olla registreerunud, kasutades rentniku kontosid. Kui kustutate konfigureeritud rentniku **Rentniku sätete \> B2C rentniku** menüüs, eemaldate selle B2C rentniku seose saitidega, mis on seotud mis tahes selle rentniku kanalitega. Sel juhul ei saa teie kasutajad enam oma kontodele sisse logida. Seetõttu olge äärmiselt ettevaatlikud, kui kustutate konfigureeritud rentniku.
>
> Kui konfigureeritud rentnik on kustutatud, jätkatakse B2C rentniku ja kirjete säilitamist, kuid selle rentniku Kaubandussüsteemi konfiguratsioon muutub või eemaldatakse. Kasutajad, kes proovivad registreeruda või saidile sisse logida, loovad uue kontokirje vaikimisi või äsja seotud B2C rentnikule, kes on konfigureeritud saidi kanalile.

## <a name="configure-your-channel-with-a-b2c-tenant"></a>Kanali konfigureerimine B2C rentnikuga

1. Logige sisse oma keskkonna Kaubanduse saidiehitusse süsteemi administraatorina. Azure AD B2C rentnike konfigureerimiseks peate olema Kaubanduskeskkonna süsteemiadministraator.
1. Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.
1. Valige **Kanalid** ja siis valige konfigureerimiseks kanal.
1. Valige parempoolsel omaduste paanil väljal **Vali B2C rakendus** selle kanali jaoks konfigureeritud Azure AD B2C rentnik.
1. Valige tegumiribal **Salvesta ja avalda**, et kinnitada uus või värskendatud konfiguratsioon.

> [!WARNING]
> Kui muudate kanalile määratud B2C rakendust, eemaldate praegused viited, mis on loodud kõigile kasutajatele, kes on juba keskkonda sisse loginud. Sellisel juhul ei ole kasutajatele saadaval ükski praegu määratud B2C rakendusega seotud mandaat. Seetõttu muutke kanali Azure AD B2C konfiguratsiooni ainult siis, kui seadistate kanalit esimest korda ja kasutajad ei ole saanud registreeruda. Vastasel juhul võib juhtuda, et kasutajad peavad uue Azure AD B2C rentniku kirje loomiseks uuesti sisse logima.
## <a name="additional-resources"></a>Lisaressursid

[Domeeninime konfigureerimine](configure-your-domain-name.md)

[Uue e-kaubanduse rentniku juurutamine](deploy-ecommerce-site.md)

[E-kaubanduse saidi loomine](create-ecommerce-site.md)

[Dynamics 365 Commerce'i saidi seostamine võrgukanaliga](associate-site-online-store.md)

[Robots.txt-failide haldamine](manage-robots-txt-files.md)

[Üleslaadimise URL suunab ümber hulgi](upload-bulk-redirects.md)

[B2C rentniku seadistus Kaubanduses](set-up-B2C-tenant.md)

[Kasutaja sisselogimiseks kohandatud lehtede seadistamine](custom-pages-user-logins.md)

[Sisuedastusvõrgu (CDN) toe lisamine](add-cdn-support.md)

[Asukohapõhise poetuvastuse lubamine](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
