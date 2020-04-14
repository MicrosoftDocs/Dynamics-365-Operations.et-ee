---
title: Kohandatud väljade loomine ja nendega töötamine
description: Selles teemas selgitatakse teile, kuidas kasutajaliidese luua kohandatud välju, et rakendus sobiks teie ettevõttega.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: f689bb3ec844459d1dd6e199804a30f3e0cb38bc
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112332"
---
# <a name="create-and-work-with-custom-fields"></a>Kohandatud väljade loomine ja nendega töötamine

[!include [banner](../includes/banner.md)]

Kuigi mitmete äriprotsesside haldamiseks on olemas lai valik valmisvälju, on ettevõttel mõnikord vaja süsteemis jälgida lisateavet. Kuigi nende väljade lisamiseks arendustööriistas laiendustena saab kasutada programmeerijate abi, võimaldab kohandatud väljade funktsioon lisada väljasid otse kasutajaliidese kaudu, võimaldades teil kohandada rakendust oma ettevõttte vajadustele vastavaks veebibrauseri abil.

Kohandatud väljade lisamise võimalus on saadaval platvormivärskenduses 13 ja uuemates. Ainult eriõigustega kasutajatel on juurdepääs sellele funktsioonile.

See video näitab, kui lihtne on lisada lehele kohandatud välja: [Kohandatud väljade lisamine](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Kohandatud väljade loomine

Pärast selle lisateabe tuvastamist, mida rakenduses jälgida soovite, saate sobivale tabelile luua kohandatud välja ja selle uue välja lehele esitada.

Järgmised sammud kirjeldavad kohandatud välja loomist ja selle välja vormile asetamist.

1. Minge vormi juurde, kuhu on vaja uut välja.
2. Kuna lõppeesmärk on kohandatud välja vormile esitamine, on kohandatud väljade loomise sisendpunkt isikupärastamisvõimaluse sees. Avage isikupärastamise tööriistariba, tehes valikud **Suvandid** ja **Vormi isikupärastamine**.
3. Klõpsake suvandeid **Lisa** ja **Väli**.
4. Valige vormi piirkond, kuhu soovite uue välja esitada. Pärast valikuid kuvab dialoogiboks **Väljade lisamine** loendi olemasolevate väljadega, mida saab vormi valitud piirkonda lisada.
5. Veenduge, et soovitud väli ei ole juba loendis. Vastasel korral saate lihtsalt loendist selle välja valida ja klõpsata käsku **Lisa**.
6. Klõpsake kohandatud välja loomise alustamiseks loendi kohal asuvat nuppu **Uue välja loomine**. See avab dialoogiboksi **Uue välja loomine**.

    Kui te ei näe nuppu **Uue välja lisamine**, pole teil selle funktsiooni kasutamiseks vajalikku luba.

7. Sisestage dialoogiboksi **Uue välja loomine** järgmine teave.

    1. Valige andmebaasi tabel, kuhu see väli tuleks lisada. Pange tähele, et ripploendis kuvatakse ainult tabelid, mis toetavad kohandatud välju. Toetatud tabelite tehnilisi üksikasju vaadake allpool asuvast jaotisest.
    2. Valige uue välja andmetüüp. Saadaolevad andmetüübid on märkeruut, kuupäev, kuupäev ja kellaaeg, kümnendarv, arv, märkeloend ja tekst.

        - Andmetüübi tekst valimisel saate määrata ka väljale sisestatava teksti maksimaalse pikkuse.
        - Andmetüübi märkeloend valimisel saate valida ka väljale sisestatavad kehtivad väärtused.

    3. Andke väljale nimi, silt ja spikritekst. Nimi vastab andmebaasis oleva füüsilise välja nimele, silti ja spikriteksti kasutatakse välja esitamiseks kasutajaliidesel.

8. Kui see on ainus väli, mida soovite selle vormi jaoks luua, klõpsake käsku **Salvesta**. Kui soovite luua veel välju, klõpsake käsku **Salvesta ja uus** ja naaske 7. etappi. Pange tähele, et praegu kehtib piirang **20 kohandatud välja tabeli kohta**.
9. Dialoogiboksist **Uue välja loomine** lahkumisel naasete dialoogiboksi **Väljade lisamine**. Äsja lisatud kohandatud väljad märgitakse väljaloendis automaatselt vormile lisatavate väljadena.
10. Märgitud väljade lisamiseks vormi valitud piirkonda klõpsake käsku **Lisa**..
11. **Valikuline:** uute väljade teisaldamiseks valitud piirkonna soovitud asukohta lubage isikupärastamise tööriistaribal režiim **Teisaldamine**. Lisateavet eri isikupärastamisvõimaluste kasutamise kohta vormi teie isikliku kasutuse järgi kohandamiseks vaadake teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md)

## <a name="sharing-custom-fields-with-other-users"></a>Kohandatud väljade jagamine teiste kasutajatega

Pärast kohandatud välja loomist ja selle vormile esitamist võite soovida seda uue väljaga uuendatud lehevaatet jagada ka süsteemi teiste kasutatatega. Seda saab toote isikupärastamisvõimalusi kasutades teha kahel viisil.

- Soovitatav on seda teha süsteemi administraatori kaudu, kes saab isikupärastamise avaldada kõigile kasutajatele või kasutajate alamkogumile. Lisateavet vaadake teemast [Kasutuskogemuse isikupärastamine](personalize-user-experience.md).
- Teise võimalusena saate muudatused (nimega *isikupärastamised*) eksportida, saata need ühele või mitmele kasutajale ja igaüks neist saab muudatused importida. Isikupärastamise tööriistariba suvand **Halda** võimaldab teil isikupärastamisi eksportida ja importida.

## <a name="managing-custom-fields"></a>Kohandatud väljade haldamine

Kõiki kohandatud välju saab süsteemis hallata süsteemihalduse moodulis oleva lehe **Kohandatud väljad** kaudu. Sellel lehel saavad kasutajate juurdepääsu paljudele järgmistele võimalustele.

- Süsteemi kõigi kohandatud väljade loendi vaatamine.
- Olemasolevate kohandatud väljade piiratud redigeerimine.
- Kohandatud väljade kustutamine.
- Kohandatud väljade esitamine andmeüksustele.
- Kohandatud väljade siltide ja spikritekstide tõlgete pakkumine.

### <a name="viewing-all-custom-fields"></a>Kõigi kohandatud väljade vaatamine

Leht **Kohandatud väljad** leht näitab kõiki süsteemis määratletud kohandatud välju. Valige soovitud tabel ja leht näitab selle tabeliga seotud kohandatud väljade värskendatud loendit. Kohandatud välja loendist valimine võimaldab teil vaadata välja üksikasju.

### <a name="editing-custom-fields"></a>Kohandatud väljade redigeerimine

Pärast kohandatud välja loomist saab lehel **Kohandatud väljad** muuta ainult selle välja teatud andmeid.

Muuta *saate* järgmisi atribuute.

- Silt
- Spikritekst
- Pikkus tekstiväljade korral

Te *ei saa* muuta järgmisi atribuute.

- Välja nimi
- Andmetüüp

Märkeloendi väljade korral saate kohandatud väljade kehtivaid väärtusi ümberjärjestada ja uusi väärtusi lisada; märkeloendi välja olemasolevaid väärtusi ei saa aga eemaldada. Pärast konkreetse tabeli väljade redigeerimist klõpsake muutuste salvestamiseks käsku **Rakenda muudatused**.

### <a name="exposing-custom-fields-on-data-entities"></a>Kohandatud väljade esitamine andmeüksustele

Samuti võib oluline olla kohandatud väljade lubamine andmeüksustel nähtav olla. Andmeüksusi kasutatakse funktsioonis [Office’i integreerimise ülevaade](../../dev-itpro/office-integration/office-integration.md) ja andmete importimisel/eksportimisel.

Kohandatud välja andmeüksusel esitamiseks tehke läbi järgmised etapid.

1. Valige kohandatud väli vormil **Kohandatud väljad**.
2. Asjakohaste üksuste vaatamiseks laiendage jaotist **Üksused**.
3. Klõpsake nuppu **Redigeeri**.
4. Muutke välja **Lubatud** nii, et seda valitaks iga üksuse korral, mis peab välja esitama.
5. Valikute salvestamiseks klõpsake käsku **Rakenda muudatused**.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Kohandatud väljade teistes keeltes kuvamise lubamine

Kuna kohandatud väljadele võivad ligipääsu vajada eri keelte kasutajad, suudab leht **Kohandatud väljad** kohandatud välja silti ja spikriteksti teistesse keeltesse tõlkida.

Järgmised etapid kirjeldavad kohandatud väljade teistesse keeltesse tõlkimise protsessi.

1. Valige kohandatud väli lehel **Kohandatud väljad**.
2. Valige toimingupaanil nupp **Tõlked**. See avab on rippmenüü selle välja jaoks olemasolevate tõlgetega.
3. Rippmenüü **Keel** näitab keeli, mille jaoks tõlge on juba olemas.

    Kui soovite olemasolevat tõlget redigeerida, valige menüüst soovitud keel ning muutke sildi ja spikriteksti väärtusi.

    Muul juhul klõpsake nuppu **Lisa keel**, valige menüüst soovitud keel ning sisestage sildi ja spikriteksti tõlgitud väärtused.

4. Kui olete lõpetanud, klõpsake nuppu **OK**.

### <a name="deleting-custom-fields"></a>Kohandatud väljade kustutamine

Harvadel juhtudel võite otsustada, et kohandatud välja ei ole enam vaja. Sel juhul saab süsteemiadministraator välja lehelt **Kohandatud väljad** kustutada. Selleks veenduge, et valitud on õige väli, klõpsake käsku **Kustuta**, klõpsake kustutamise kinnitamiseks nuppu **Jah** ning lõpuks klõpsake käsku **Rakenda muudatused**.

> [!NOTE]
> Seda toimingut ei saa tagasi võtta ning väljaga seotud andmed kustutatakse jäädavalt andmebaasist.

## <a name="appendix"></a>Lisa

### <a name="who-can-create-custom-fields"></a>Kes saab kohandatud välju luua?

Süsteemi kaitsmiseks saavad kohandatud välju vaikimisi luua vaid süsteemiadministraatorid. Sellegipoolest saavad süsteemiadministraatorid turberolli **Käitusaja kohandamise lauskasutaja** abil anda kohandatud väljade loomise õigusi lauskasutajatele, kelle osas organisatsioon õiguste andmist vajalikuks peab. Ilma selle turberollita kasutajad ei saa kohandatud välju luua, kuid saavad süsteemi teiste kasutajate loodud kohandatud välju vaadata ja neid mõjutada.

### <a name="what-tables-support-custom-fields"></a>Millised tabelid toetavad kohandatud välju?

Jõudluse tõttu ja tehnilistel põhjustel võimaldavad praegu kohandatud väljade lisamist vaid järgmisi tingimusi täitvad tabelid.

- Tabel peab olema märgistatud ühena järgmistest gruppidest.

    - Grupeeri
    - Töölehe päis
    - Peamine
    - Muud
    - Parameeter
    - Viide
    - Kande päis

- Tabel ei saa teist tabelit laiendada.
- Tabel ei saa olla märgistatud süsteemitabelina.
- Tabel ei saa olla ajutine tabel.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Kas ma saan arendustööriistades viidata kohandatud väljadele?  

Kohandatud välju saab hallata ainult kasutajaliidese kaudu ja neile ei saa koodi alusel viidata. 
