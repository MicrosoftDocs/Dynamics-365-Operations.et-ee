---
title: Commerce'i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 2c4872cdebc414eaa865af025237bd9e1d14bfd2
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906112"
---
# <a name="configure-optional-features-for-a-commerce-preview-environment"></a>Commerce'i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.

## <a name="prerequisites"></a>Eeltingimused

Kui soovite hinnata ülekande meilifunktsioone, peavad olema täidetud järgmised eeltingimused.

- Teil on meili server saadaval \[SMTP\], mida saab kasutada Microsoft Azure'i tellimusel, kus te eelvaate keskkonda ette valmistate.
- Teile on saadaval serveri täielikult kvalifitseeritud domeeni nimi (FQDN)/IP aadress, SMTP pordi number ja autentimise üksikasjad.

Kui soovite hinnata digitaalse varahalduse funktsioone uusi omni-kanali pilte lisades, peab teil olema oma sisu haldamise süsteemi (CMS) üürniku nimi saadaval. Selle nime leidmise juhised on toodud hiljem selles teemas. >>>(Q: kus on juhised?)

## <a name="configure-the-image-back-end"></a>Kujutise konfigureerimine tagaserveris

### <a name="find-your-media-base-url"></a>Oma meedia baas-URL-i leidmine

> [!NOTE]
> Enne, kui saate selle protseduuri lõpule viia, peate täitma sammud [oma saidi häälestamiseks Commerce'iis](cpe-post-provisioning.md#set-up-your-site-in-commerce).

1. Logige saidi halduse tööriista sisse, kasutades URL-i, mis te tegite, kui te e-kaubanduse lähtestamist ette valmistasite (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).
1. Avage sait **Fabrikam**.
1. Valige vasakpoolses menüüs **Varud**.
1. Valige mis tahes üks pildi vara.
1. Paremal asuval atribuudi kontrollijal leiate **avaliku URL-i** atribuudi. Väärtus on URL. Siin on näide.

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Asendage viimane identifikaator URL-is (**MA1nQC** ülaltoodud näites) järgneva stringiga: **search?fileName=**.  Siin on näide URL-i väljanägemisest pärast seda muutust:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    See URL on teie meedia baas-URL. Tehke selle kohta märge.

### <a name="update-the-media-base-url"></a>Meedia baas-URL-i värskendamine

1. Logige sisse rakendusse Dynamics 365 Retail.
1. Vasakul asuva menüü abil avage **Moodulid \> Jaemüük \> Kanali häälestus \> Kanali profiilid**.
1. Valige suvand **Redigeeri**.
1. Suvandis **Profiili atribuudid** asendage atribuudi väärtus **Meedia serveri baas-URL** väärtusega Meedia baas-URL, mille enne lõite.
1. Valige vasakult loendist teine kanal, mis on kanali **Vaikimisi** all.
1. Suvandil **Profiili atribuudid** klõpsake nuppu **Lisa**.
1. Lisatud atribuudi jaoks valige atribuudi võtmeks **Meedia serveri baas-URL**. Atribuudi väärtusena sisestage varem loodud meediumi aluse URL.
1. Valige käsk **Salvesta**.

## <a name="configure-the-email-server"></a>Meiliserveri konfigureerimine

> [!NOTE]
> Sisestatud SMTP-serveri või meiliteenus peab olema juurdepääsetav Azure'i kordustellimusest, mida keskkonna jaoks kasutate.

1. Jaemüüki sisselogimine
1. Vasakul asuva menüü abil avage **Moodulid \> Süsteemi haldus \> Häälestus \> Meil \> Meili parameetrid**.
1. Sisestage vahekaardi **SMTP-** sätted väljale **Väljamineva meili server** oma SMTP-serveri või e-posti teenuse FQDN või IP-aadress.
1. Sisestage väljale **SMTP pordi number** SMTP pordi number. (Kui te ei kasuta rakendust Secure Sockets Layer \[SSL\]-i, on vaikimisi pordi number **25**.)
1. Autentimise vajadusel sisestage väärtused väljadele **Kasutajanimi** ja **Prool**.
1. Valige käsk **Salvesta**.
1. Valige **Värskenda**.
1. Vahekaardil **testi meili** väljal **e-posti pakkuja** valige **SMTP**.
1. Väljale **Saada** sisestage meiliaadress, millele soovite testmeili saata.
1. Valige **Saada testmeilisõnum**.

## <a name="configure-email-templates"></a>Meilimallide konfigureerimine

Iga kandelise sündmuse jaoks, mille jaoks soovite meile saata, tuleb uuendada meilimalli kehtiva saatja meiliaadressiga.

1. Jaemüüki sisselogimine
1. Vasakul asuva menüü abil avage **Moodulid \> Organisatsiooni haldus \> Häälestus \> Organisatsiooni meilimallid**.
1. Valige **Näita loendit**.
1. Iga loetletud malli puhul toimige järgmiselt:

    1. Väljale **Saatja meiliaadress** sisestage saatja meiliaadress.
    1. Valikuline: Sisestage väljale **saatja nimi** nimi, mida tuleks saatja nimena kasutada.

1. Valige käsk **Salvesta**.

## <a name="customize-email-templates"></a>Meilimallide kohandamine

Võite soovida kohandada meilimalle, et nad kasutaksid erinevaid pilte. Võite ka värskendada linke mallides, et need läheksid teie eelvaate keskkonda. See protseduur selgitab, kuidas vaikimisi malle alla laadida, neid kohandada ja süsteemi malle värskendada.

1. Brauseri abil laadige kohalikku arvutisse [Microsoft Dynamics 365 Commerce eelvaate vaikimisi meilimallide zip-fail](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip). See fail sisaldab järgmisi HTML-dokumente:

    - Tellimuse kinnituse mall
    - Kinkekaardi väljastamise mall
    - Uue tellimuse mall
    - Pakketellimuse mall
    - Tellimuse malli valimine

1. Kohandage malle teksti või HTML-redaktori abil. Vaadake selles teemas hiljem [toetatud märkide](#supported-tokens-in-the-email-template) loendit.
1. Jaemüüki sisselogimine
1. Vasakul asuva menüü abil avage **Moodulid \> Organisatsiooni haldus \> Häälestus \> Organisatsiooni meilimallid**.
1. Kõigi mallide nägemiseks laiendage loendit vasakul.
1. Iga malli puhul, mida soovite kohandada, tehke järgmist:

    1. Valige loendist mall.
    1. Jaotises **Meilisõnumi sisu** valige loendist sobiva keele versioon. (Vaikekeel on **en-us**.)
    1. Jaotises **e-kirja sisu** valige **Redigeeri**. Kuvatakse paan **Laadi üles e-kirja mall**.
    1. Valige **Sirvi**ja leidke HTML-fail, millel on kohandatud sisu.
    1. Valige nupp **Laadi üles**. Teie mall laaditakse süsteemi ja kuvatakse eelvaade.
    1. Valige nupp **OK**.
    1. Valikuline: kohandage malli atribuuti **Teema**.
    1. Valige käsk **Salvesta**.

### <a name="supported-tokens-in-the-email-template"></a>Toetatud märgid meilimallis

Need märgid asendatakse meili renderdamise ajal tegelike väärtustega, mis rakenduvad kliendile ja nende tellimusele.

#### <a name="sales-order"></a>Müügitellimus

Järgmised load rakenduvad üldisele müügitellimusele.

| Märgi nimi | Luba |
|-------------------|-------|
| Tellimuse kood      | %salesid% |
| Kliendi nimi   | %customername% |
| Tarneaadress  | %deliveryaddress% |
| Arveaadress   | %customeraddress% |
| Tellimuse kuupäev        | %shipdate% |
| Tarneviis     | %modeofdelivery% |
| Allahindlus          | %discount% |
| Käibemaks         | %tax% |
| Tellimuse kogusumma       | %total% |

#### <a name="sales-line"></a>Müügirida

Järgmised load on iga toote puhul tellimuses asendatud väärtustega.

> [!NOTE]
> Pange **toote nimekiri – alustage** luba HTML-ploki algusesse, mida korratakse iga toote puhul, ja asetage **toote loend-lõpp** -luba ploki lõppu.

| Märgi nimi      | Luba |
|------------------------|-------|
| Tooteloend - algus   | \<!--%tablebegin.salesline% --\> |
| Tooteloend - lõpp     | \<!--%tableend.salesline%--\> |
| Toote nimi           | %lineproductname% |
| Kirjeldus            | %lineproductdescription% |
| Kogus               | %linequantity% |
| Reaühiku hind        | %lineprice% (kontrollige) |
| reaüksuse kogusumma        | %linenetamount% |
| rea allahindlus          | %linediscount% |
| Lähetuskuupäev              | %lineshipdate% |
| Hanke meetod     | %linedeliverymode% |
| tarneaadress       | %linedeliveryaddress% |
| Rea müügiüksus | %lineunit% |

## <a name="additional-resources"></a>Lisaressursid

[Commerce'i eelvaatekeskkonna ülevaade](cpe-overview.md)

[Commerce'i eelvaatekeskkonna ettevalmistamine](provisioning-guide.md)

[Commerce'i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md)

[Commerce'i eelvaatekeskkonna KKK](cpe-faq.md)

[Microsofti elutsükli teenused (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)

[Abiressursid rakenduse Dynamics 365 Retail jaoks](../retail/index.md)
