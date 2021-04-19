---
title: Meilimallide loomine kandesündmuste jaoks
description: Selles teemas kirjeldatakse, kuidas luua, üles laadida ja konfigureerida meilimalle Microsoft Dynamics 365 Commerce'i kandesündmuste jaoks.
author: bicyclingfool
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 55597e83a930fc7d8bcc4c0cf09abc82cb666b25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792627"
---
# <a name="create-email-templates-for-transactional-events"></a>Meilimallide loomine kandesündmuste jaoks

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua, üles laadida ja konfigureerida meilimalle Microsoft Dynamics 365 Commerce'i kandesündmuste jaoks.

## <a name="overview"></a>Ülevaade

Dynamics 365 Commerce pakub valmislahendust meilide saatmiseks, mis teavitavad kliente kandesündmustest (näiteks kui tellimus sisestatakse,kui tellimus on pealevõtmiseks valmis või kui tellimus on saadetud). Selles teemas kirjeldatakse kandemeilide saatmiseks kasutatavate meilimallide loomist, üleslaadimist ja konfigureerimist.

## <a name="create-an-email-template"></a>Loo e-kirja mall

Enne kindla kandesündmuse vastendamist meilimallile, peate looma selle malli.

Meilimalli loomiseks tehke järgmist.

1. Avage Commerce'i headquarters, minge **Jaemüük ja Äri \> jaotises \>Organisatsiooni meilimallid** või **Organisatsiooni haldus \> Seadistamine \>  Organisatsiooni meilimallid**.
1. Valige suvand **Uus**.
1. Seadistage jaotises **Üldine** järgmised väljad.

    - **Meili ID** – meili ID on selle malli kordumatu identifikaator ja see väärtus kuvatakse siis, kui valite malli sündmusele vastendamiseks.
    - **Meili kirjeldus** – saate kasutada seda valikulist välja malli kirjelduse lisamiseks. Sisestatav väärtus kuvatakse ainult Commerce'i peakontoris.
    - **Saatja nimi** – sisestatav nimi kuvatakse suurema osa meiliklientide puhul väljal „saatja”.
    - **Saatja meiliaadress** – sisestage meiliaadress, mida tuleks kasutada selle malli abil saadetavate meilide puhul.
    - **Vaikekeele kood** – see väli määrab vaikimisi saadetava meili lokaliseeritud versiooni, kui seda malli rakendav kanal pole määranud ühtegi keelt.

1. Jaotises **Meilisõnumi sisu** valige **Uus**.
1. Sisestage väljale **Keel** meilimalli keel. Hiljem saate lisada rohkem keeli ja lokaliseeritud malle.
1. Sisestage väljale **Teema** meilisõnumi teema, mida kuvatakse meili teema väljal.
1. Meilimalli üleslaadimiseks valige **Redigeeri**.

## <a name="create-an-email-message-body-by-using-html"></a>Meilisõnumi sisu loomine HTML-i abil

Teie meilisõnumi sisu koosneb HTML-ist. Võite kasutada mis tahes paigutust, laadi ja kaubamärki, mida HTML ja tekstisisene kaskaadlaadistik (CSS) võimaldavad. Saate kasutada ka pilte, kui hostite neid avalikult kättesaadavas lõpp-punktis veebis. Pildi lisamiseks sisestage pildi URL sildile **src** HTML-i atribuut **&lt;img&gt;**.

> [!NOTE]
> Meilikliendid kehtestavad paigutuse ja stiili piiranguid, mis võivad nõuda sõnumi sisus kasutatava HTML-i ja CSS-i korrigeerimist. Soovitame teil tutvuda HTML-i loomise heade tavadega, mida toetavad kõige levinumad meilikliendid.

## <a name="add-placeholders-to-the-email-message-body"></a>Meilisõnumi sisule kohatäidete lisamine

Teie meil võib sisaldada kohatäiteid, mis asendatakse kliendi- ja kandepõhiste väärtustega meili loomisel. Kohatäited on alati protsendimärkide (%) vahel ja sisestatakse otse HTML-dokumenti.

Siin on näide.

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a>Tellimuse kohatäited (müügitellimuse tase)

Järgmised kohatäited toovad ja kuvavad müügitellimuse tasemel määratletud andmeid (vastupidiselt müügirea tasemele).

| Kohatäite nimi     | Kohatäite väärtus                                            |
| -------------------- | ------------------------------------------------------------ |
| customername         | Tellimuse esitanud kliendi nimi.               |
| salesid              | Müügitellimuse müügi ID.                                   |
| deliveryaddress      | Saadetud tellimuste tarneaadress.                     |
| customeraddress      | Kliendi aadress.                                 |
| kliendimeiliaadress | Meiliaadress, mille klient väljaregistreerimise ajal sisestas.     |
| deliverydate         | Tarnekuupäev.                                           |
| shipdate             | Lähetuskuupäev.                                               |
| modeofdelivery       | Tellimuse tarneviis.                              |
| lisakulud              | Tellimuse kogukulud.                             |
| maks                  | Tellimuse maks kokku.                                 |
| kokku                | Tellimuse kogusumma.                              |
| ordernetamount       | Tellimuse kogusumma miinus kogu maks.         |
| allahindlus             | Tellimuse lõppallahindlus.                            |
| storename            | Poe nimi, kus tellimus esitati.            |
| storeaddress         | Tellimuse esitanud poe aadress.              |
| storeopenfrom        | Tellimuse esitanud poe lahtiolekuaeg.         |
| storeopento          | Tellimuse esitanud poe sulgemisaeg.         |
| pickupstorename      | Poe nimi, kust tellimus peale võetakse.     |
| pickupstoreaddress   | Poe aadress, kust tellimus peale võetakse.  |
| pickupopenstorefrom  | Poe lahtiolekuaeg, kust tellimus peale võetakse. |
| pickupopenstoreto    | Poe sulgemisaeg, kust tellimus peale võetakse. |

### <a name="order-line-placeholders-sales-line-level"></a>Tellimuserea kohatäited (müügirea tase)

Järgmised kohatäited toovad ja kuvavad müügitellimuse üksikute toodete (ridade) andmeid.

| Kohatäite nimi               | Kohatäite väärtus |
|--------------------------------|-------------------|
| productid                      | Selle rea toote ID. |
| lineproductname                | Toote nimi. |
| lineproductdescription         | Toote kirjeldus. |
| linequantity                   | Sellele reale tellitud ühikute arv koos mõõtühikuga (nt **ea** või **paar**). |
| lineunit                       | Selle rea mõõtühik. |
| linequantity_withoutunit       | Sellele reale tellitud ühikute arv ilma mõõtühikuta. |
| linequantitypicked             | Sündmuse **PickOrder** kasutamisel komplekteeritud ühikute arv. Muul juhul **0** (null). |
| linequantitypicked_withoutunit | Sündmuse **PickOrder** kasutamisel komplekteeritud ühikute arv ilma mõõtühikuta. Muul juhul **0** (null). |
| linequantitypacked             | Sündmuste **PackOrder** ja **Tellimus pealevõtmiseks valmis** kasutamisel pakitud ühikute arv. Muul juhul **0** (null). |
| linequantitypacked_withoutuom  | Sündmuste **PackOrder** ja **Tellimus pealevõtmiseks valmis** kasutamisel pakitud ühikute arv ilma mõõtühikuta. Muul juhul **0** (null). |
| linequantityshipped            | Alati **0**, välja arvatud juhul, kui kasutatakse kindlaid järgmisel real kirjeldatud sündmusi. |
| linequantityshipped_withoutuom | Sündmuse **ShipOrder** kasutamisel komplekteeritud ühikute arv ilma mõõtühikuta. Muul juhul **0** (null). |
| lineprice                      | Ühe üksuse hind. |
| linenetamount                  | Rea hind pärast ühikute arvu ja allahindluse rakendamist. |
| linediscount                   | Üksiku ühiku allahindlus. |
| lineshipdate                   | Rea lähetuskuupäev. |
| linedeliverydate               | Rea tarnekuupäev. |
| linedeliverymode               | Rea tarneviis. |
| linedeliveryaddress            | Rea tarneaadress. |
| giftcardnumber                 | Kinkekaardi number kinkekaardi tüübi toodete puhul. |
| giftcardbalance                | Kinkekaardi saldo kinkekaardi tüübi toodete puhul. |
| giftcardmessage                | Kinkekaardi sõnum kinkekaardi tüübi toodete puhul. |
| giftcardpin                    | Kinkekaardi isiklik ID-number (PIN-kood) kinkekaardi tüübi toodete puhul. (See kohatäide on omane välistele kinkekaartidele.) |
| giftcardexpiration             | Kinkekaardi aegumiskuupäev kinkekaardi tüübi toodete puhul. (See kohatäide on omane välistele kinkekaartidele.) |
| giftcardrecipientname          | Kinkekaardi saaja nimi kinkekaardi tüübi toodete puhul. |
| giftcardbuyername              | Kinkekaardi osta nimi kinkekaardi tüübi toodete puhul. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Tellimuserea kohatäidete vorming meilisõnumi sisus

Kui loote meilisõnumi sisus üksikute tellimuseridade HTML-i, pange nende ridade HTML-i ja kohatäidete korduv üksus järgmiste kohatäidete vahele, mis pannakse HTML-kommentaari siltide sisse.

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

Siin on näide.

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a>Saadetud kviitungite malli loomine

Kviitungeid saab saata klientidele, kes teevad oste jaemüügikassas (POS). Üldiselt sarnanevad meili teel saadetava kviitungi malli loomise etapid muude kandesündmuste mallide loomisega. Kuid järgmisi muudatusi on vaja teha.

- Kviitungi tekst sisestatakse meili kohatäite **%message%** abil. Tagamaks, et kviitungi sisu oleks õigesti renderdatud, lisage **%message%** kohatäide HTML-iga **&lt;pre&gt;** ja **&lt;pre&gt;** vahele.
- Kohatäitjat **%receiptid%** saab kasutada QR-koodi või vöötkoodi näitamiseks, mis tähistab kviitungi ID-d. (QR-koodid ja vöötkoodid on dünaamiliselt loodud ja neid teenuseid teenuseid loonud kolmanda osapoole teenus.) Lisateavet selle kohta, kuidas kuvada QR-kood või vöötkood meiliga saadetud kviitungis, vt [Lisa QR-kood või vöötkood kande- ja kviitungi meilidele](add-qr-code-barcode-email.md).

## <a name="upload-the-email-html"></a>Meili HTML-i üleslaadimine

Pärast meili sisu HTML-i loomist ja testimist, tuleb see üles laadida Commerce'i peakontorisse. Praegu ei saa meili HTML-i eksportida. Seetõttu peate oma HTML-i põhikoopiat säilitama väljaspool Commerce'i peakontorit.

Uue või redigeeritud meilimalli HTML-i üleslaadimiseks toimige järgmiselt.

1. Avage Commerce'i peakontori jaotis **Jaemüük ja kaubandus \> Peakontori seadistamine \> Organisatsiooni meilimallid**.
1. Valige keele rida, mille jaoks soovite HTML-i lisada või asendada. Teiseks võimaluseks on valida suvand **Uus** uue keele jaoks rea loomiseks.
1. Valige suvand **Redigeeri**.
1. Kuvatavas dialoogiboksis tehke valik **Sirvi**. Sirvige HTML-dokumendini, mida soovite üles laadida, valige see ja seejärel valige **Ava**.
1. Valige nupp **Laadi üles**.
1. Pärast meili HTML-i kuvamist eelvaate aknas valige **OK**.
1. Kontrollige, et real on ruut **On sisu** märgitud.

Kui olete Commerce'i peakontori juba meili saatmiseks konfigureerinud, saadetakse teie uus või värskendatud meil kõigile klientidele, kes sooritavad kande, mis käivitab mallile vastendatud sündmuse.

Lisateavet Dynamics 365 Commerce'is meilide konfigureerimise kohta vt teemast [Meili konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md).

## <a name="additional-resources"></a>Lisaressursid 

[Meiliteatise profiili seadistamine](email-notification-profiles.md)

[Meilisõnumi konfigureerimine ja saatmine](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[Seadistage meilisissetulekud](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Meilikviitungite saatmine kaasaegsest kassast ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
