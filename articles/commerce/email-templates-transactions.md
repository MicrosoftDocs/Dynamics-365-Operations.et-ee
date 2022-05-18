---
title: Meilimallide loomine kandesündmuste jaoks
description: Selles teemas kirjeldatakse, kuidas luua, üles laadida ja konfigureerida meilimalle Microsoft Dynamics 365 Commerce'i kandesündmuste jaoks.
author: bicyclingfool
ms.date: 12/10/2021
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
ms.openlocfilehash: 08e247bac577dc0bb8a4635d61f0082793380da9
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722515"
---
# <a name="create-email-templates-for-transactional-events"></a>Meilimallide loomine kandesündmuste jaoks

[!include [banner](includes/banner.md)]


Selles teemas kirjeldatakse, kuidas luua, üles laadida ja konfigureerida meilimalle Microsoft Dynamics 365 Commerce'i kandesündmuste jaoks.

Dynamics 365 Commerce pakub boksist väljas lahendust meili saatmiseks, mis teavitab kliente kandesündmuste kohta. Näiteks saab e-kirju saata, kui tellimus on paigutatud, on peale võtmiseks valmis või saadetud. Selles teemas kirjeldatakse kandemeilide saatmiseks kasutatavate meilimallide loomist, üleslaadimist ja konfigureerimist.

## <a name="notification-types"></a>Teatise tüübid

Teatisi saab konfigureerida nii, et nad teavitavad kliente meili kaudu, kui konkreetsed sündmused toimuvad tellimuse ja kliendi töötsükli osana. Teatiste konfigureerimiseks peate vastendama meilimalli teatisetüübiga, luues äri meiliteatise profiili. Lisateavet meiliteatise profiilide häälestamise kohta vaata [häälestage meiliteatise profiil](email-notification-profiles.md).

Dynamics 365 Commerce toetab järgmisi teatisetüüpe.

### <a name="order-created"></a>Tellimus loodud

*Loodud tellimuse* teavitustüüp käivitatakse Commerce headquarters`is uue müügitellimuse loomisel.

> [!NOTE]
> Tellimuse loodud teavitustüüpi ei käivitata sularaha- ja kandekannete puhul, mis toimuvad müügikoha (POS) terminalis. Sel juhul luuakse selle asemel meiliga saadetud ja/või prinditud kviitung. Lisateavet vt [Modern POS-i (MPOS) meilikviitungite saatmine](email-receipts.md).

### <a name="order-confirmed"></a>Tellimus on kinnitatud.

*Kinnitatud tellimuse* teatise tüüp käivitatakse, kui Commerce headquarters müügitellimuse jaoks luuakse tellimuse kinnitusdokument.

### <a name="picking-completed"></a>Komplekteerimine on lõpetatud.

*Komplekteerimine on lõpule viidud* teatis käivitatakse, kui Commerce Headquarters`is on tellimus märgitud lõpetatuks.

> [!NOTE]
> Valimise lõpetamise teatise tüüp ei käivitu, kui üksus märgitakse POS-terminalis väljavalituks.

### <a name="packing-completed"></a>Pakkimine on lõpetatud.

*Pakkimine on lõpule viidud* teatis käivitatakse, kui Commerce Headquarters POS-terminalis oleva tellimuse jaoks luuakse saatelehe dokument.

Pakkimise lõpetatud teatise tüüp toetab järgmisi täiendavaid meili kohatäiteid, et lihtsustada "tellimuse järeletulemiseks valmis" ja tehingute meilidest tellimuse otsimise funktsiooni.

| Kohatäite nimi    | Eesmärk |
| ------------------- | ------- |
| `pickupstorename`     | Kaupluse nimi, kus tellimus on pealevõtuks saadaval. |
| `pickupstoreaddress`  | Kaupluse aadress, kus tellimus on pealevõtuks saadaval. |
| `pickupstoreopenfrom` | Pealekorje kaupluse lahtiolekuaeg. |
| `pickupstoreopento` | Pealekorje kaupluse sulgemisaeg. |
| `pickupchannelid`     | Pealekorje kaupluse kanali ID. |
| `packingslipid`      | Pealekorje tellimuse saatelehe ID. |
| `confirmationid`      | Pealekorje tellimuse kinnituse ID. (Seda ID-d nimetatakse vahel kanaliviite ID-ks.) |

Lisateavet kliendi sisseregistreerimise ja tellimuse otsingu funktsioonide kohta vt [Häälestage geotuvastus ja ümbersuunamine](geo-detection-redirection.md) ja [Tellimuste otsingu külalisregistreerimistest lubamine](order-lookup-guest.md).

### <a name="order-ready-for-pickup"></a>Tellimus on kättesaamiseks valmis

*Tellimus on valmis pealekorjeks* teatise tüüp käivitatakse, kui tellimus on märgitud pakituks ja kättetoimetamise viis on seatud **Kliendile kättetoimetamiseks** ühel või enamal tellimuse real.

> [!NOTE]
> Tellimuse järeletulemiseks valmis teatise tüüp on aegunud, eelistades pakkimise lõpetamise teatise tüüpi. See teatise tüüp on kohandatud tarneviisi järgi.

### <a name="order-shipped"></a>Saadetud tellimus

Teatis *Tellimus tarnitud* käivitub, kui arve esitatakse tellimusele, mille tarneviis ei ole poest järeletulemine.

> [!NOTE]
> Tellimuse tarnimise teatise tüüp on aegunud ja arveldatud tellimuse teatise tüüp. See teatise tüüp on kohandatud tarneviisi järgi.

### <a name="order-invoiced"></a>Tellimus on arveldatud

*Tellimus arveldatud* teavitustüüp käivitatakse, kui tellimusele on Commerce headquarters POS-süsteemis esitatud arve.

### <a name="issue-gift-card"></a>Väljasta kinkekaart

*kinkekaardi* teatise tüüp käivitub, kui arveldatakse müügitellimus, mis sisaldab kinkekaardi tüüpi toodet.

> [!NOTE]
> Kinkekaardi väljastamise teavitusmeil saadetakse kinkekaardi saajale. Kinkekaardi saaja on määratud Commerce Headquartersis üksiku müügitellimuse real vahekaardil **Pakkimine** jaotise **Rea üksikasjad** all. Seda saab määrata käsitsi või programmiliselt.

Kinkekaardi väljastamise teatise tüüp toetab järgmisi täiendavaid kohatäitjaid.

| Kohatäite nimi      | Eesmärk |
| --------------------- | ------- |
| `giftcardnumber`        | Kinkekaardi number kinkekaardi tüübi toodete puhul. |
| `availablebalance` | Kinkekaardi järelejäänud saldo. |
| `giftcardmessage`       | Kinkekaardi sõnum kinkekaardi tüübi toodete puhul. |
| `giftcardpin`         | Kinkekaardi isiklik ID-number (PIN-kood) kinkekaardi tüübi toodete puhul. (See kohatäide on omane välistele kinkekaartidele.) |
| `giftcardexpiration`    | Kinkekaardi aegumiskuupäev kinkekaardi tüübi toodete puhul. (See kohatäide on omane välistele kinkekaartidele.) |
| `giftcardrecipientname` | Kinkekaardi saaja nimi kinkekaardi tüübi toodete puhul. |
| `giftcardbuyername`     | Kinkekaardi osta nimi kinkekaardi tüübi toodete puhul. |

Lisateavet kinkekaartide kohta vt [E-commerce'i digitaalsetest kinkekaartidest](digital-gift-cards.md) ja [väliste kinkekaartide toest](dev-itpro/gift-card.md).

### <a name="order-cancellation"></a>Tellimuse tühistamine

*Tellimus tühistamine* teavitustüüp käivitatakse, kui tellimus on Commerce headquarters`is tühistatud.

### <a name="customer-created"></a>Klient on loodud

*Klient loodud* teavitustüüp käivitatakse Commerce headquarters`is uue kliendi üksuse loomisel.

### <a name="b2b-prospect-approved"></a>B2B potentsiaalne klient on heaks kiidetud

*B2B-potentsiaalse kliendi* kinnitatud teatisetüüp käivitatakse, kui potentsiaalse kliendi sisseostmistaotlus on Commerce Headquarters`is kinnitatud. Lisateavet B2B potentsiaalsete klientide kinnitamise või tagasilükkamise kohta vt [häälestage uue äripartneri jaoks administraatori kasutaja](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B potentsiaalse kliendi kinnitatud teatise tüüp toetab järgmisi täiendavaid kohatäitjaid.

| Kohatäite nimi | Eesmärk                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`       | B2B-potentsiaalse kliendi eesnimi selle rakenduse sisestamisel. |
| `lastname`         | B2B-potentsiaalse kliendi perekonnanimi selle rakenduse sisestamisel. |
| `company`          | Taotleja ettevõtte nimi sellisel kujul, nagu see on avaldusse kantud. |
| `email`            | Potentsiaalse kliendi e-kirja aadress nagu see on rakendusse sisestatud.   |
| `zipcode`          | Potentsiaalse kliendi esmase aadressi sihtnumber. |
| `comments`         | Kommentaar, mida potentsiaalne klient on rakendusse sisestanud. |
| `storename`        | Selle kanali nimi, kus potsentsiaalne klient on loodud. |
| `storeurl`         | Vaikimisi tühi. Selle kohatäite kasutamiseks tuleb luua kohandatud laiend. |

### <a name="b2b-prospect-rejected"></a>B2B potentsiaalne klient on tagasi lükatud

*B2B-potentsiaalse kliendi tagasi lükkamise* teatisetüüp käivitatakse, kui potentsiaalse kliendi liitumistaotlus on Commerce Headquarters`is tagasi lükatud. Lisateavet B2B potentsiaalsete klientide kinnitamise või tagasilükkamise kohta vt [häälestage uue äripartneri jaoks administraatori kasutaja](b2b/manage-b2b-users.md#set-up-the-administrator-user-for-a-new-business-partner). 

B2B potentsiaalse kliendi tagasi lükkamise teatise tüüp toetab järgmisi täiendavaid kohatäitjaid.

| Kohatäite nimi | Eesmärk                                                      |
| ---------------- | ------------------------------------------------------------ |
| `firstname`        | B2B-potentsiaalse kliendi eesnimi selle rakenduse sisestamisel. |
| `lastname`         | B2B-potentsiaalse kliendi perekonnanimi selle rakenduse sisestamisel. |
| `company`          | Taotleja ettevõtte nimi sellisel kujul, nagu see on avaldusse kantud. |

## <a name="create-an-email-template"></a>Loo e-kirja mall

Enne kindla kandesündmuse vastendamist meilimallile, peate looma selle malli.

Meilimalli loomiseks tehke järgmist.

1. Avage Commerce'i headquarters, minge **Jaemüük ja Äri \> jaotises \>Organisatsiooni meilimallid** või **Organisatsiooni haldus \> Seadistamine \>  Organisatsiooni meilimallid**.
1. Valige suvand **Uus**.
1. Seadistage jaotises **Üldine** järgmised väljad.

    - **E-kirja ID** – meili ID on malli kordumatu ID. See on väärtus, mis kuvatakse, kui valite sündmusele vastendamiseks malli.
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
> Meilikliendid kehtestavad paigutuse ja stiili piiranguid, mis võivad nõuda sõnumi sisus kasutatava HTML-i ja CSS-i korrigeerimist. Soovitame teil tutvuda HTML-i loomise heade tavadega, mida kõige populaarsemad meilikliendid toetavad.

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

| Kohatäite nimi     | Eesmärk                                                      |
| -------------------- | ------------------------------------------------------------ |
| `customername`         | Tellimuse esitanud kliendi nimi.               |
| `customeraddress`      | Kliendi aadress.                                 |
| `customeremailaddress` | Meiliaadress, mille klient väljaregistreerimise ajal sisestas.     |
| `salesid`              | Müügitellimuse müügi ID.                                   |
| `orderconfirmationid`  | Tellimuse loomisel loodud kanaliülene ID.   |
| `channelid`            | Selle jaemüügi- või veebikanali ID, mille kaudu tellimus esitati. |
| `deliveryname`         | Vaiketarneaadress, mis on laoala kohta sisestatud.         |
| `deliveryaddress`      | Saadetud tellimuste tarneaadress.                     |
| `deliverydate`         | Tarnekuupäev.                                           |
| `shipdate`             | Lähetuskuupäev.                                               |
| `modeofdelivery`       | Tellimuse tarneviis.                              |
| `ordernetamount`       | Tellimuse kogusumma miinus kogu maks.         |
| `discount`            | Tellimuse lõppallahindlus.                            |
| `charges`              | Tellimuse kogukulud.                             |
| `tax`                  | Tellimuse maks kokku.                                 |
| `total`                | Tellimuse kogusumma.                              |
| `storename`            | Poe nimi, kus tellimus esitati.            |
| `storeaddress`         | Tellimuse esitanud poe aadress.              |
| `storeopenfrom`        | Tellimuse esitanud poe lahtiolekuaeg.         |
| `storeopento`          | Tellimuse esitanud poe sulgemisaeg.         |
| `pickupstorename`      | Poe nimi, kust tellimus peale võetakse.\*   |
| `pickupstoreaddress`   | Poe aadress, kust tellimus peale võetakse.\* |
| `pickupopenstorefrom`  | Poe lahtiolekuaeg, kust tellimus peale võetakse.\* |
| `pickupopenstoreto`    | Poe sulgemisaeg, kust tellimus peale võetakse.\* |
| `pickupchannelid`     | Kaupluse kanali ID, mis on määratud kättesaamisviisi jaoks.\* |
| `packingslipid`        | Saatelehe ID, mis loodi tellimuse ridade pakkimisel.\* |

\*Need kohatäited tagastavad andmed ainult siis, kui neid kasutatakse **tellimuse** komplekteerimisteatise tüübi jaoks. 

### <a name="order-line-placeholders-sales-line-level"></a>Tellimuserea kohatäited (müügirea tase)

Järgmised kohatäited toovad ja kuvavad müügitellimuse üksikute toodete (ridade) andmeid.

| Kohatäite nimi               | Eesmärk |
|--------------------------------|-------------------|
| `productid`                      | <p>Toote ID. See ID arvestab variante.</p><p><strong>Märkus:</strong> See kohatäide on reaproduki kasuks aegunud `lineproductrecid`.</p> |
| `lineproductrecid`               | Toote ID. See ID arvestab variante. See tuvastab kordumatult kauba variandi tasemel. |
| `lineitemid`                     | Toote toote-taseme ID. (See ID ei arvesta variante.) |
| `lineproductvariantid`           | Toote variandi ID. |
| `lineproductname`                | Toote nimi. |
| `lineproductdescription`         | Toote kirjeldus. |
| `linequantity`                   | Sellele reale tellitud ühikute arv koos mõõtühikuga (nt **ea** või **paar**). |
| `lineunit`                       | Selle rea mõõtühik. |
| `linequantity_withoutunit`       | Sellele reale tellitud ühikute arv ilma mõõtühikuta. |
| `linequantitypicked`             | Sündmuse **PickOrder** kasutamisel komplekteeritud ühikute arv. Muul juhul **0** (null). |
| `linequantitypicked_withoutunit` | Sündmuse **PickOrder** kasutamisel komplekteeritud ühikute arv ilma mõõtühikuta. Muul juhul **0** (null). |
| `linequantitypacked`             | Sündmuste **PackOrder** ja **Tellimus pealevõtmiseks valmis** kasutamisel pakitud ühikute arv. Muul juhul **0** (null). |
| `linequantitypacked_withoutuom`  | Sündmuste **PackOrder** ja **Tellimus pealevõtmiseks valmis** kasutamisel pakitud ühikute arv ilma mõõtühikuta. Muul juhul **0** (null). |
| `linequantityshipped`            | Alati **0**, välja arvatud juhul, kui kasutatakse kindlaid järgmisel real kirjeldatud sündmusi. |
| `linequantityshipped_withoutuom` | Sündmuse **ShipOrder** kasutamisel komplekteeritud ühikute arv ilma mõõtühikuta. Muul juhul **0** (null). |
| `lineprice`                      | Ühe üksuse hind. |
| `linenetamount`                  | Rea hind pärast ühikute arvu ja allahindluse rakendamist. |
| `linediscount`                   | Üksiku ühiku allahindlus. |
| `lineshipdate`                   | Rea lähetuskuupäev. |
| `linedeliverydate`               | Rea tarnekuupäev. |
| `linedeliverymode`               | Rea tarneviis. |
| `linedeliveryaddress`            | Rea tarneaadress. |
| `linepickupdate`                 | Kliendi määratud komplekteerimiskuupäev tellimuste puhul, mis kasutavad pealevõtmisviise. |
| `linepickuptimeslot`             | Kliendi määratud komplekteerimiskuupäev tellimuste puhul, mis kasutavad pealevõtmisviise. |
| `giftcardnumber`                 | Kinkekaardi number kinkekaardi tüübi toodete puhul. |
| `giftcardbalance`                | Kinkekaardi saldo kinkekaardi tüübi toodete puhul. |
| `giftcardmessage`                | Kinkekaardi sõnum kinkekaardi tüübi toodete puhul. |
| `giftcardpin`                    | Kinkekaardi PIN kinkekaardi tüübi toodete puhul. (See kohatäide on omane välistele kinkekaartidele.) |
| `giftcardexpiration`             | Kinkekaardi aegumiskuupäev kinkekaardi tüübi toodete puhul. (See kohatäide on omane välistele kinkekaartidele.) |
| `giftcardrecipientname`          | Kinkekaardi saaja nimi kinkekaardi tüübi toodete puhul. |
| `giftcardbuyername`              | Kinkekaardi osta nimi kinkekaardi tüübi toodete puhul. |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a>Tellimuserea kohatäidete vorming meilisõnumi sisus

Kui loote meilisõnumi sisus üksikute tellimuseridade HTML-i, pange nende ridade HTML-i ja kohatäidete korduv üksus järgmiste kohatäidete vahele, mis pannakse HTML-kommentaari siltide sisse. Pange tähele, et kohatäited on HTML-i kommentaarisiltide sees.

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

- **%message%** kohatäidet kasutatakse teksti sisestamiseks meili kohatäiteabilis. Tagamaks, et kviitungi sisu oleks õigesti renderdatud, lisage **%message%** kohatäide HTML-iga **&lt;pre&gt;** ja **&lt;pre&gt;** vahele.
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

[Seadistage meilisissetulekud](/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[Meilikviitungite saatmine kaasaegsest kassast ](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
