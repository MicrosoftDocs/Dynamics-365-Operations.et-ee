---
title: Dynamics 365 Commerce’i liivakastikeskkonna valikuliste funktsioonide konfigureerimine
description: See artikkel selgitab, kuidas konfigureerimine valikuliste funktsioonide jaoks sisendkausta Microsoft Dynamics 365 Commerce keskkonnas.
author: josaw1
ms.date: 06/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4935f5f6ee17cba9c09eb79132119a7cbc08d9ad
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270351"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-sandbox-environment"></a>Dynamics 365 Commerce’i liivakastikeskkonna valikuliste funktsioonide konfigureerimine

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas konfigureerimine valikuliste funktsioonide jaoks sisendkausta Microsoft Dynamics 365 Commerce keskkonnas.

## <a name="prerequisites"></a>Eeltingimused

Kui soovite kande meilifunktsiooni demosse saata, peavad olema täidetud järgmised eeltingimused:

- Teil on saadav meiliserver (Simple Mail Transfer Protocol \[SMTP\] server), Microsoft Azure mida saab kasutada kordustellimusest, kus olete edastanud sisendkausta keskkonna.
- Teile on saadaval serveri täielikult kvalifitseeritud domeeni nimi (FQDN)/IP aadress, SMTP pordi number ja autentimise üksikasjad.

## <a name="configure-the-image-back-end"></a>Kujutise konfigureerimine tagaserveris

### <a name="find-your-media-base-url"></a>Oma meedia baas-URL-i leidmine

> [!NOTE]
> Enne, kui saate selle protseduuri lõpule viia, peate täitma sammud [oma saidi häälestamiseks Commerce'iis](cpe-post-provisioning.md#set-up-your-e-commerce-sites).

1. Logige Commerce'i saidiehitajasse sisse, kasutades URL-i, mille märkisite üles, kui te e-kaubanduse lähtestamist ette valmistasite (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).
1. **Avage Fabrikam**, **Adventure Works** või **Adventure Works Businessi** sait, mida soovite kasutada.
1. Valige vasakpoolses menüüs **Meediumiteek**.
1. Valige mis tahes üks pildi vara.
1. Paremal asuval atribuudi kontrollijal leiate **avaliku URL-i** atribuudi. Väärtus on URL. Siin on näide.

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.

1. Asendage viimane identifikaator URL-is (**MA1nQC** ülaltoodud näites) järgneva stringiga: **search?fileName=**.  Siin on näide URL-i väljanägemisest pärast seda muutust:

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    See URL on teie meedia baas-URL. Tehke selle kohta märge.

### <a name="update-the-media-base-url"></a>Meedia baas-URL-i värskendamine

1. Logige Commerce’i peakontorisse sisse.
1. Vasakul asuva menüü abil avage **Moodulid \> Jaemüük ja kaubandus \> Kanali häälestus \> Kanali profiilid**.
1. Valige suvand **Redigeeri**.
1. Suvandis **Profiili atribuudid** asendage atribuudi väärtus **Meedia serveri baas-URL** väärtusega Meedia baas-URL, mille enne lõite.
1. Valige muu kanal nimega **scXXXXXXXXX**.
1. Suvandil **Profiili atribuudid** klõpsake nuppu **Lisa**.
1. Lisatud atribuudi jaoks valige atribuudi võtmeks **Meedia serveri baas-URL**. Atribuudi väärtusena sisestage varem loodud meediumi aluse URL.
1. Valige käsk **Salvesta**.

## <a name="configure-and-test-the-email-server"></a>Meiliserveri konfigureerimine ja testimine

> [!NOTE]
> Sisestatud SMTP-serveri või meiliteenus peab olema juurdepääsetav Azure'i kordustellimusest, mida keskkonna jaoks kasutate.

1. Logige Commerce’i peakontorisse sisse.
1. Avage vasakul oleva menüü abil **Moodulid \> Jaemüük ja kaubandus \> Peakontori häälestus \> Parameetrid \> Meiliparameetrid**.
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

1. Logige Commerce’i peakontorisse sisse.
1. Avage vasakul oleva menüü abil **Moodulid \> Jaemüük ja kaubandus \> Peakontori häälestus \> Parameetrid \> Organisatsiooni meilimallid**.
1. Valige **Näita loendit**.
1. Iga loetletud malli puhul toimige järgmiselt:

    1. Väljale **Saatja meiliaadress** sisestage saatja meiliaadress.
    1. Valikuline: Sisestage väljale **saatja nimi** nimi, mida tuleks saatja nimena kasutada.

1. Valige käsk **Salvesta**.

## <a name="customize-email-templates"></a>Meilimallide kohandamine

Võite soovida kohandada meilimalle, et nad kasutaksid erinevaid pilte. Samuti võite soovida uuendada mallide linke nii, et nad lähevad teie sisendkausta keskkonda. See protseduur selgitab, kuidas vaikimisi malle alla laadida, neid kohandada ja süsteemi malle värskendada.

1. Laadige veebibrauseris alla demo vaikimisi [Microsoft Dynamics 365 Commerce e-kirja mallide sihtfail](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) kohalikku arvutisse. See fail sisaldab järgmisi HTML-dokumente:

    - Tellimuse kinnituse mall
    - Kinkekaardi väljastamise mall
    - Uue tellimuse mall
    - Pakketellimuse mall
    - Tellimuse malli valimine

1. Kohandage malle teksti või HTML-redaktori abil. Vaadake toetatud [sõnede loendit selles](#supported-tokens-in-the-email-template) artiklis hiljem.
1. Logige Commerce’i sisse.
1. Vasakul asuva menüü abil avage **Moodulid \> Organisatsiooni haldus \> Häälestus \> Organisatsiooni meilimallid**.
1. Kõigi mallide nägemiseks laiendage loendit vasakul.
1. Iga malli puhul, mida soovite kohandada, tehke järgmist:

    1. Valige loendist mall.
    1. Jaotises **Meilisõnumi sisu** valige loendist sobiva keele versioon. (Vaikekeel on **en-us**.)
    1. Jaotises **e-kirja sisu** valige **Redigeeri**. Kuvatakse paan **Laadi üles e-kirja mall**.
    1. Valige **Sirvi** ja leidke HTML-fail, millel on kohandatud sisu.
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
| Arveldusaadress   | %customeraddress% |
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
| Toote nimetus           | %lineproductname% |
| Kirjeldus            | %lineproductdescription% |
| Kogus               | %linequantity% |
| Reaühiku hind        | %lineprice% (Kontrolli) |
| reaüksuse kogusumma        | %linenetamount% |
| rea allahindlus          | %linediscount% |
| Lähetuskuupäev              | %lineshipdate% |
| Hanke meetod     | %linedeliverymode% |
| tarneaadress       | %linedeliveryaddress% |
| Rea müügiüksus | %lineunit% |

## <a name="additional-resources"></a>Lisaressursid

[Info keskkonna Dynamics 365 Commerce ettevalmistamine](provisioning-guide.md)

[Einfo Dynamics 365 Commerce keskkonna konfigureerimine](cpe-post-provisioning.md)

[BOPIS-i konfigureerimine Dynamics 365 Commerce sisendkausta keskkonnas](cpe-bopis.md)

[Microsofti elutsükli teenused (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure'i portaal](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce veebisait](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
