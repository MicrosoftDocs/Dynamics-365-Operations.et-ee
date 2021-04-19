---
title: USMCA päritolusertifikaat
description: Selle funktsiooni abil saate printida Ameerika Ühendriikide-Mehhiko-Kanada leppe (USMCA) nõutava päritoludokumentide sertifikaate.
author: Henrikan
ms.date: 10/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-23
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: e479c7686ab9445b012d335ddc9fc4cdc6b2275c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807700"
---
# <a name="usmca-certification-of-origin"></a>USMCA päritolusertifikaat

[!include [banner](../includes/banner.md)]

Selle funktsiooni abil saate printida Ameerika Ühendriikide-Mehhiko-Kanada leppe (USMCA) nõutava päritoludokumentide sertifikaate.

*USMCA päritoludokumendi sertifikaat* sisaldab minimaalseid andmeid, mis on nõutavad deklaratsiooni jaoks. Mõned andmed võivad olla eeltäidetud enne printimist, kui teised tuleb pärast printimist käsitsi täita. Tariifse sooduskohtlemise saamiseks peab dokument olema täidetud ja importija valduses deklaratsiooni tegemise ajal. Dokumendi võib täita importija, eksportija või tootja.

Saate printida dokumendi ühe saadetise kohta **Kõigi saadetiste** loendi lehelt või **Saadetise üksikasjade** lehelt.

Dokument on kättesaadav ainult siis, kui juriidilise isiku põhiaadress asub on Ameerika Ühendriikides.

Sõltuvalt dokumendi printimise valikust saab dokumenti eeltäita teie süsteemis olevate andmetega. Prinditud dokumendile on võimalik andmeid muuta või neid lisada, eksportides prinditud dokumendi redigeeritud vormingusse, nt Microsoft Word. Pärast eksportimist saate enne deklaratsiooni esitamist rakendada mis tahes vajalikke muudatusi.

## <a name="turn-on-the-usmca-feature"></a>USMCA funktsiooni sisselülitamine

Enne USMCA funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *Transpordihaldus*
- **Funktsiooni nimi:** *USMCA päritoludokumendi sertifikaat*

## <a name="document-content"></a>Dokumendi sisu

USMCA päritoludokumendi sertifikaat sisaldab järgmisi andmeid:

- Aadressi elemendid
- Tõendava osapoole roll
- Üksik saadetis
- Arved
- Tühi periood
- Kauba üksikasjad
- Tõendaja allkiri
- Lehekülgede arv

Lisateavet kõigi nende elementide ja nende väärtuste leidmise kohta leiate selle teema ülejäänud jaotistest.

## <a name="print-a-usmca-certification-of-origin-document"></a>Prindi USMCA päritoludokumendi sertifikaat

USMCA päritoludokumendi sertifikaadi printimiseks tehke järgmist:

1. Tehke üht järgmistest valikutest.
    - Avage **Transpordihaldus > Saadetised > Kõik saadetised** ja valige saadetis, mille jaoks soovite dokumenti printida.
    - Avage **Saadetise üksikasjade** leht saadetise kohta, mille jaoks soovite dokumenti printida (siin on mitu moodust, sh lehelt **Kõik saadetised**).
1. Avage toiminguribal **Saadetised** vahekaart ja valige **Prindi** grupist **USMCA päritolusertifikaat**.
1. Avaneb **Päritolusertifikaadi** dialoogiaken. Tehke järgmistes jaotistes kirjeldatud sätted ja seejärel valige dokumendi loomiseks **OK**.
1. Avatakse dokumendi eelvaade. Dokumendi printimiseks või eksportimiseks vastavalt vajadusele kasutage toiminguribal esitatud käske.

### <a name="certifying-party"></a>Sertifitseeriv pool

Kasuta dokumenti printiva osapoole tüübi tuvastamiseks **Sertifitseeriv pool** ripp-loendit. Määrake, kas sertifitseeriv pool on *eksportija*, *eksportija ja tootja*, *tootja* või *importija*; või jätke see tühjaks, kui sertifitseeriv pool ei ole mitte ükski neist. Teie valitud suvand määratleb, mis prinditakse dokumendi jaotises aadressi osasse.

Teie poolt valitud **Sertifitseeriv pool** kaasatakse prinditud dokumenti.

Dokumenti saab printida nii sissetulevatele kui ka väljaminevatele saadetistele. Valige *Importija* **Sertifitseerivaks pooleks** ainult sissetulevate saadetiste puhul.

Järgmine tabel kirjeldab teabe tüüpe, mis sisalduvad dokumendis vastavalt teie valitud **Sertifitseeriv poolele**.

| Sertifitseeriv pool | Kirjeldus |
|---|---|
| *\[Tühi\]* | Lisab dokumenti järgmised üksikasjad:<ul><li>**Tõendaja üksikasjad**: Kasutab lähetamise lao aadressi üksikasju, kui see on saadaval; vastasel juhul kasutab see kättetoimetamise saidi aadressi, kui see on saadaval; vastasel juhul kasutab see Supply Chain Management-is valitud juriidilise isiku (ettevõtte) aadressi.</li><li>**Eksportija üksikasjad**: tühi</li><li>**Tootja üksikasjad**: tühi</li><li>**Importija üksikasjad**: tühi</li><ul>|
| *Eksportija* | Lisab dokumenti järgmised üksikasjad:<ul><li>**Tõendaja üksikasjad**: Kasutab lähetamise lao aadressi üksikasju, kui see on saadaval; vastasel juhul kasutab see kättetoimetamise saidi aadressi, kui see on saadaval; vastasel juhul kasutab see Supply Chain Management-is valitud juriidilise isiku (ettevõtte) aadressi.</li><li>**Eksportija üksikasjad**: Kasutab juriidilise isiku aadressi üksikasju.</li><li>**Tootja üksikasjad**: tühi</li><li>**Importija üksikasjad**: Kasutab seotud müügitellimuse arve kontot.</li><ul>|
| *Eksportija ja tootja* | Lisab dokumenti järgmised üksikasjad:<ul><li>**Tõendaja üksikasjad**: Kasutab lähetamise lao aadressi üksikasju, kui see on saadaval; vastasel juhul kasutab see kättetoimetamise saidi aadressi, kui see on saadaval; vastasel juhul kasutab see Supply Chain Management-is valitud juriidilise isiku (ettevõtte) aadressi.</li><li>**Eksportija üksikasjad**: Kasutab juriidilise isiku aadressi üksikasju.</li><li>**Tootja üksikasjad**: Kasutab juriidilise isiku aadressi üksikasju.</li><li>**Importija üksikasjad**: Kasutab seotud müügitellimuse arve kontot.</li><ul>|
| *Importija* | Lisab dokumenti järgmised üksikasjad:<ul><li>**Tõendaja üksikasjad**: Kasutab lähetamise lao aadressi üksikasju, kui see on saadaval; vastasel juhul kasutab see kättetoimetamise saidi aadressi, kui see on saadaval; vastasel juhul kasutab see Supply Chain Management-is valitud juriidilise isiku (ettevõtte) aadressi.</li><li>**Eksportija üksikasjad**: tühi</li><li>**Tootja üksikasjad**: tühi</li><li>**Importija üksikasjad**: Kasutab juriidilise isiku aadressi üksikasju.</li><ul>|
| *Tootja* | Lisab dokumenti järgmised üksikasjad:<ul><li>**Tõendaja üksikasjad**: Kasutab lähetamise lao aadressi üksikasju, kui see on saadaval; vastasel juhul kasutab see kättetoimetamise saidi aadressi, kui see on saadaval; vastasel juhul kasutab see Supply Chain Management-is valitud juriidilise isiku aadressi.</li><li>**Eksportija üksikasjad**: tühi</li><li>**Tootja üksikasjad**: Kasutab juriidilise isiku aadressi üksikasju.</li><li>**Importija üksikasjad**: tühi</li><ul>|

### <a name="has-various-producers"></a>Omab erinevaid tootjaid

**Sertifitseeriv pool** ripp-loend määrab dokumendis tootja üksikasjade jaoks kasutatava teksti. Valige üks järgmistest:

- *Erinevad tootjad* - Prindib tootja üksikasjadesse teksti "Erinevad".
- *Saadaval taotluse korral* – Prindib tootja üksikasjadesse teksti "Saadaval importiva asutuse nõudel".

Kui **sertifitseerivaks pooleks** on seatud *eksportija ja tootjale* või *tootja*, siis on **Erinevad tootjad** säte allutatud ja tootja aadressi üksikasjad on samad, mis tõendaja puhul.

### <a name="blanket-period"></a>Tühi periood

Kasutage **Katteperiood alates** ja **Katteperiood kuni** välju, et luua katteperiood, mille jooksul katab dokument mitut identse kauba saadetist, isegi kui dokument prinditakse ainult ühele saadetisele. Saate seada katteperioodi kuupäevad ilma piiranguteta ja need lisatakse dokumenti. Samuti saate need sätted jätta tühjaks või seada need minevikku.

### <a name="is-single-shipment"></a>On üksik saadetis

**Päritolusertifikaadi** dialoogiboksis valige suvandi **Kas on üksik saadetis** väärtuseks üks järgmisest valikutest:

- *Jah* – Lisab arve numbri kõrvale rea "Kas tegemist on üksiku saadetisega: Jah".
- *Ei* - Ei lisa midagi.

## <a name="other-information-included-in-the-document"></a>Muu dokumendis sisalduv teave

Lisaks valikulistele elementidele, mida valite **Päritolusertifikaadi** dialoogiaknas, kaasatakse USMCA päritolusertifikaadi teave ja kohandatud väljad, mis on summeeritud järgmistes lõigetes. Osa sellest teabest tuleb pärast dokumendi loomist käsitsi sisestada.

### <a name="invoice-number"></a>Arve number

Saadetistega seotud müügiarvete ID-d prinditakse dokumendile sõltumata sellest, kas see tekkis. Arve numbrid prinditakse olenemata **Kas tegemist on üksiku saadetisega** valikust.

### <a name="item-details"></a>Kauba üksikasjad

Dokument sisaldab mitut sektsiooni, mis loetlevad kindla kauba üksikasju, mis on järgmised:

- **SKU-kood**: Prindib väljastatud toote kaubakoodi.

- **Kirjeldus**: Prindib kas väljastatud toote kirjelduse või nime. Kui kirjeldus on kasutaja keeles olemas, siis see prinditakse. Kui kirjeldust kasutaja keeles ei eksisteeri, siis prinditakse nimi kasutaja keeles. Kui seda nime ei ole, prinditakse kauba nimi.

- **Ühtlustatud süsteemi (HS) tariifi klassifikatsioon**: Prindib tootega seotud ühtlustatud tariifide graafiku. Saate seadistada need graafikud, minnes **Transpordihaldus \> Seadistus \> Transpordistandard \> Ühtlustatud tariifi graafikud**.

- **Päritolu kriteerium:** Peate selle jaotise andmed käsitsi sisestama, kui dokumendi esimest korda väljastate.

- **Päritoluriik:** Prindib päritoluriigi, mida te rakendate, minnes **Toote teabe haldus \> Seadistus \> Toote vastavus \> Päritoluriik** (vt ka [Päritoluriik](../pim/country-of-origin.md)). Päritoluriigi ISO-kood prinditakse saadetise tarneaadressi ja kauba sihtkoha riigi/regiooni alusel. Kui päritoluriigi andmeid pole seadistatud, naaseb see väärtus tagasi sättele, mis leiti **Väljastatud toode \> Väliskaubandus \> Päritolu** lehelt. Kui ei leita ikka ühtegi päritoluriiki, tuleb pärast dokumendi loomist sisestada päritoluriik käsitsi.

### <a name="certifier-signature-and-date"></a>Tõendaja allkiri ja kuupäev

Peate selle pärast dokumendi loomist käsitsi sisestama.

### <a name="consists-of-number-of-pages"></a>Koosneb lehekülgede arvust

Sertifikaadi allkirjastanud kasutaja peab pärast dokumendi loomist käsitsi sisestama lehekülgede arvu (kinnitamiseks).

### <a name="page-numbers"></a>Leheküljenumbrid

Käesolev lehekülg ja dokumendi allosas prinditavate lehekülgede arv.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]