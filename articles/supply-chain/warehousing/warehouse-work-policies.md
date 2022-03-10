---
title: Tööpoliitikad
description: Selles teemas selgitatakse, kuidas seadistada tööpoliitikat.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1d4ee3f1bffaf00c20758f6a3f399451d3122291
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571157"
---
# <a name="work-policies"></a>Tööpoliitikad

[!include [banner](../includes/banner.md)]

See teema selgitab, kuidas häälestada süsteemi ja mobiilirakendust Warehouse Management, et nad toetaksid tööpoliitikaid. Seda funktsiooni saate kasutada lao kiireks registreerimiseks, loomata ladustamistööd, kui võtate vastu ostu-või üleviimistellimusi või kui lõpetate tootmisprotsesse. See teema annab üldteavet. Üksikasjalikku teavet, mis on seotud litsentsiplaadi vastuvõtmisega, leiate teemast [Litsentsiplaadi vastuvõtmine mobiilirakenduse Warehouse Management kaudu](warehousing-mobile-device-app-license-plate-receiving.md).

Tööpoliitika kontrollib, kas lao töö on loodud, kui toodetud kaup on lõpetatuks kinnitatud või kui kaubad võetakse vastu lao mobiilirakenduse Warehouse Management abil. Seadistage iga tööpoliitika, määratledes tingimused, mille puhul see kehtib: töötellimuse tüübid ja protsessid, lao asukoht ja (valikuliselt) tooted. Näiteks peab toote *A0001* ostutellimuse vastu võtma asukohas *RECV* laos *24*. Hiljem tarbitakse toodet teises protsessi asukohas *RECV*. Sellisel juhul saate seadistada tööpoliitika, et vältida ladustatud töö loomist, kui töötaja teatab tootest *A0001*, kui see saabus asukoha *RECV*.

> [!NOTE]
> - Selleks, et tööpoliitika oleks aktiivne, peate selle määratlema vähemalt ühes asukohas lehe **Tööpoliitikad** FastTab valikus **Lao asukohad**. 
> - Sama asukohta ei saa määrata mitme tööpoliitika jaoks.
> - Mobiilse seadme menüükäskude suvand **Prindi silt** ei prindi tööd loomata litsentsiplaadi silti.

## <a name="activate-the-features-in-your-system"></a>Aktiveerige süsteemi funktsioonid

Selleks, et kõik selles teemas kirjeldatud funktsioonid oleksid teie süsteemis saadaval, lülitage sisse järgmised kaks funktsiooni asukohas [Funktsiooni haldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

- Litsentsiplaadi vastuvõtu täiustused
- Sissetuleva töö tööpoliitika täiustused

## <a name="the-work-policies-page"></a>Tööpoliitikate leht

Tööpoliitikate seadistamiseks avage **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**. Seejärel seadistage igal FastTab-il väljad, nagu on kirjeldatud järgmistes alamosades.

### <a name="the-work-order-types-fasttab"></a>Töötellimuse tüübid FastTab

**Töötellimuse tüübid** FastTab-is saate lisada kõik töötellimuse tüübid ja sellega seotud tööprotsessid, millele tööpoliitika rakendub. Tööpoliitikate jaoks toetatakse järgmisi töötellimuse tüüpe ja seotud tööpoliitikaid.

| Töötellimuse tüüp | Tööprotsess |
|---|---|
| Toormaterjalide komplekteerimine| Kõik seotud protsessid |
| Kaastoodete ja kõrvalsaaduste kõrvalepanek | Kõik seotud protsessid |
| Lõpetatud kaupade ladustamine | Kõik seotud protsessid |
| Üleviimistarne | Litsentsiplaadi vastuvõtt (ja kõrvale panemine) |
| Ostutellimused | <ul><li>Litsentsiplaadi vastuvõtt (ja kõrvale panemine)</li><li>Koormas oleva kauba vastuvõtmine (ja kõrvale panemine)</li><li>Vastuvõttev ostutellimuse rida (ja kõrvaleseadmine)</li><li>Vastuvõttev ostutellimuse üksus (ja kõrvaleseadmine)</li></ul> |

Tööpoliitika seadistamiseks viisil,, et see rakendub mitmele sama töötellimuse tüübi tööprotsessile, lisage iga tööprotsessi jaoks tabelisse eraldi rida.

Määrake iga tabeli rea puhul väli **Töö loomise meetod** ühele järgmistest väärtustest.

- **Mitte kunagi** – see väärtus näitab, et tööpoliitika takistab laotöö loomist valitud töötellimuse tüübi ja seotud tööprotsessi jaoks.
- **Ristlaadimine** — tööpoliitika loob kaudse edasisaatmise töö, kasutades väljal **Ristlaadimise poliitika nimi** valitud poliitikat.

### <a name="the-inventory-locations-fasttab"></a>Varude asukohad FastTab-is

Lisage FastTab **Varude asukohtad** kõik asukohad, kus seda tööpoliitikat rakendada. Kui tööpoliitikaga ei seostu ühtki asukohta, siis ei rakendu tööpoliitika ühelegi protsessile.

Sama asukohta ei saa määrata mitme tööpoliitika jaoks.

Asukoha profiilile määratud lao asukohta saate kasutada ka siis, kui funktsioon **Kasuta litsentsiplaadi jälgimist** ei ole sisse lülitatud. Sel juhul registreerivad töötajad otse vaba kaubavaru.

### <a name="the-products-fasttab"></a>Toodete FastTab

Vahekaardil **Tooted** määrake väli **Toote valik** juhtelemendile, mis tooteid poliitika peaks rakendama:

- **Kõik** — poliitika peaks rakenduma kõikidele toodetele.
- **Valitud** — poliitika peaks rakenduma ainult tabelis loetletud toodetele. Kasutage **Toodete** FastTab tööriistariba toodete tabelisse lisamiseks või sealt eemaldamiseks.

## <a name="default-and-custom-to-locations"></a>Vaikimisi ja kohandatud "sinna" asukohad

> [!NOTE]
> Selles jaotises kirjeldatud funktsioonide kättesaadavaks tegemiseks süsteemis peate sisse lülitama funktsioonid *Litsentsiplaadi täiustuste saamine* ja *Tööpoliitika täiustused sissetuleva töö puhul* asukohas [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Varem toetas süsteem vastuvõtmist ainult iga lao jaoks eraldi seatud vaikimisi asukohas. Kuid mobiilse seadme menüüüksused, mis kasutavad järgmisi töö loomise protsesse, pakuvad nüüd suvandit **Vaikeandmete kasutamine**. See valik võimaldab teil määrata kohandatud asukohta ühele või mitmele menüükäsule. (See suvand oli teatud menüükäsu tüüpide jaoks juba saadaval.)

- Litsentsiplaadi vastuvõtt (ja kõrvale panemine)
- Koormas oleva kauba vastuvõtmine (ja kõrvale panemine)
- Vastuvõttev ostutellimuse rida (ja kõrvaleseadmine)
- Vastuvõttev ostutellimuse üksus (ja kõrvaleseadmine)

**Asukoha** menüü-üksuse säte kirjutab üle lao vastuvõtmise vaikeasukohta kõigi tellimuste puhul, mida töödeldakse selle menüükäsu abil.

Mobiilse seadme menüü-üksuse seadistamiseks, mis toetab vastuvõtmist kohandatud asukohas, toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige või looge menüükäsk, mis kasutab ühte selles jaotises varem loetletud tööloomise protsessidest.
1. Määrake FastTab-il **Üldine** suvandil **Kasutage vaikeandmed** valikut **Jah**.
1. Valige tegumiribal suvand **Vaikeandmed**.
1. Määrake lehel **Vaikeandmed** järgmised väärtused.

    - **Vaikimisi andmeväli:** määrake see väli *asukohta*.
    - **Ladu:** valige sihtladu, mida selle menüükäsuga kasutada.
    - **Asukoht:** see väli loendab kõik valitud lao jaoks saadaolevad asukoha ID-d. Kuid selle välja sättel ei ole tegelikult mingit mõju. Seetõttu saate selle tühjaks jätta. Sellegipoolest saate kasutada loendit, et kinnitada ID, mille peate sisestama väljale **Kindlaksmääratud väärtus**.
    - **Kindlaksmääratud väärtus:** sisestage selle menüükäsuga seotud asukoha ID.

> [!TIP]
> Tööpoliitikat saab rakendada ainult siis, kui kõik vastuvõtvad asukohad on loetletud vastavas tööpoliitika sättes. See nõue rakendub hoolimata sellest, kas kasutate lao vaikeasukohta või kohandatud asukohta.

## <a name="example-scenario-warehouse-receiving"></a>Stsenaariumi näide: lao vastuvõtt

Kõik tooted, mis on vastu võetud *Ostutellimuse kauba vastuvõtmisel (ja ladustamisel)*, peavad olema registreeritud asukohas *FL-001* ja need peavad olema saadaval laos *24*. Siiski ei tohi tööd luua. Tooted, mis on saadud mis tahes muul viisil (s.h kasutades muid mobiilse seadme menüükäske) tuleks registreerida vaikimisi lao vastuvõtvas asukohas (*RECV*) ja töö tuleb luua nagu tavaliselt. (See stsenaarium ei kuva vaikimisi vastuvõtmise häälestust.)

See stsenaarium nõuab järgmisi elemente:

- *Ostutellimuse kauba vastuvõtmine (ja kõrvalepanek)* tööpoliitika protsess asukohas *FL-001*, kõikidele toodetele
- Mobiilse seadme menüükäsk, millel on vaikeandmed ja mis määrab **Välja asukoha** väärtuseks *FL-001*

### <a name="prerequisites"></a>Eeltingimused

Selles stsenaariumis kirjeldatud funktsioonide kättesaadavaks tegemiseks süsteemis peate sisse lülitama funktsioonid *Litsentsiplaadi täiustuste saamine* ja *Tööpoliitika täiustused sissetuleva töö puhul* asukohas [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

See stsenaarium kasutab standardseid demoandmeid. Niisiis, kui soovite selle läbida siin toodud väärtuseid kasutades, peate kasutama süsteemi, kuhu demoandmed on installitud. Peate valima ka juriidilise isiku **USMF**.

### <a name="set-up-a-work-policy"></a>Tööpoliitika häälestamine

1. Minge asukohta **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.
1. Valige suvand **Uus**.
1. Minge väljal **Tööpoliitika nimi** asukohta *Ostukauba ladustamise töö puudub*.
1. Valige käsk **Salvesta**.
1. **Töötellimuse tüüpide** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:

    - **Töötellimuse tüüp:** *ostutellimused*
    - **Tööprotsess:** *vastuvõttev ostutellimuse kaup (ja ladustamine)*
    - **Töö loomise meetod:** *mitte kunagi*
    - **Ristlaadimise poliitika nimi:** jätke see väli tühjaks.

1. **Varude asukohtade** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:

    - **Ladu:** *24*
    - **Asukoht:** *FL-001*

1. **Toodete** FastTab-il seadistage välja **Tootevalik** väärtuseks *Kõik*.
1. Valige käsk **Salvesta**.

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a>Mobiilse seadme menüükäsu häälestus kättesaamise asukoha muutmiseks

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Vasakpoolsel paanil valige olemasolev **Ostu vastuvõtmise** menüükäsk.
1. Määrake FastTab-il **Üldine** suvandil **Kasutage vaikeandmed** valikut *Jah*.
1. Valige käsk **Salvesta**.
1. Valige tegumiribal suvand **Vaikeandmed**.
1. **Vaikeandmete** lehel tegevuspaanil valige **Uus**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:

    - **Vaikimisi andmeväli:** *Asukohta*
    - **Ladu:** *24*
    - **Asukoht:** jätke see väli tühjaks.
    - **Kindlaks määratud väärtus:** *FL-001*

1. Valige käsk **Salvesta**.

### <a name="receive-a-purchase-order-without-creating-work"></a>Ostutellimuse vastuvõtmine tööd loomata

Selles jaotises toodud näites kirjeldatakse, kuidas saada ostutellimuse kaupa, kuid mitte tööd luues asukohas, mis erineb lao jaoks seadistatud vastuvõtmise vaikeasukohast. Selles näites kasutatakse tööpoliitikat ja mobiilse seadme üksust, mille lõite selle stsenaariumiga varem.

#### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Valige suvand **Uus**.
1. Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.

    - **Hankija konto:** *US-101*
    - **Tegevuskoht:** *2*
    - **Ladu:** *24*

1. Dialoogiboksi sulgemiseks ja uue müügitellimuse loomiseks valige **OK**.
1. FastTab **Ostutellimuse ridadel** määrake tühjale reale järgmised väärtused:

    - **Kauba kood:** *A0001*
    - **Kogus:** *1*

1. Valige käsk **Salvesta**.
1. Märkige üles ostutellimuse number.

#### <a name="receive-a-purchase-order"></a>Ostutellimuse vastuvõtmine

1. Logige sisse mobiilses seadmes lattu *24* kasutades *24* kasutaja ID-na ja *1* paroolina.
1. Valige **Sissetulev**.
1. Valige **Ostu vastuvõtmine**. Välja **Asukoht** väärtuseks peab olema seatud *FL-001*.
1. Sisestage eelmises protseduuris loodud ostutellimuse number.
1. Sisestage väljale **Kauba number** väärtus *A0001*.
1. Valige nupp **OK**.
1. Sisestage väljale **Kogus** väärtus *1*.
1. Valige nupp **OK**.

Ostutellimus on nüüd vastu võetud, kuid sellega pole seotud ühtegi tööd. Vaba kaubavaru on värskendatud ja kauba *A0001* kogus *1* on nüüd saadaval asukohas *FL-001*.

## <a name="example-scenario-manufacturing"></a>Stsenaariumi näide: tootmine

Järgmises näites on kaks tootmistellimust: *PRD-001* ja *PRD-002*. Tootmistellimusel *PRD-001* on toiming nimega *Assembler*, kus toode *SC1* on teatatud lõpetatuks asukohale *001*. Tootmistellimusel *PRD-002* on toiming nimega *Värvimine* ja tarbib toodet *SC1* asukohast *001*. Tootmistellimus *PRD-002* tarbib ka toormaterjali *RM1* asukohast *001*. Toormaterjali *RM1* hoitakse laoasukohas *BULK-001* ja komplekteeritakse asukohale *001* laotööga toormaterjali komplekteerimiseks. Komplekteerimistöö luuakse tootmise *PRD-002* väljastamisel.

[![Lao tööpoliitikad.](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)

Kui plaanite selle stsenaariumi jaoks konfigureerida lao tööpoliitika, peaksite arvestama järgmisi punkte.

- Laotöö pole lõpetatud kaupade ladustamiseks vajalik, kui teatate toote *SC1* lõpetatuks tootmistellimusest *PRD-001* asukohale *001*. Seda põhjusel, et tootmistellimuse *PRD-002* toiming *Värvimine* tarbib samas asukohas toodet *SC1*.
- Laotöö on toormaterjali komplekteerimiseks vajalik, et liigutada toormaterjali *RM1* laoasukohast *BULK-001* asukohta *001*.

Siin on näide tööpoliitikast, mida saate nende kaalutluste põhjal seadistada:

- **Tööpoliitika nimi:** *ladustamistööd ei ole*
- **Töötellimuse tüübid:** *lõpetatud kaupade ladustamine* ja *Kaastoote ja kõrvalsaaduse ladustamine*
- **Varude asukohad:** ladu *51* ja asukoht *001*
- **Tooted:** *SC1*

Järgmised näidisstsenaariumid annavad etapiviisilise juhise, kuidas seadistada selle stsenaarium jaoks laotöö poliitikat.

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Näidisstsenaarium: teatage tootmistellimus lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitud

See stsenaarium näitab näidet, kus tootmistellimus teatatakse lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitav.

See stsenaarium kasutab standardseid demoandmeid. Niisiis, kui soovite selle läbida siin toodud väärtuseid kasutades, peate kasutama süsteemi, kuhu demoandmed on installitud. Peate valima ka juriidilise isiku **USMF**.

### <a name="set-up-a-warehouse-work-policy"></a>Lao tööpoliitika seadistamine

Laotoimingud ei hõlma alati laotööd. Tööpoliitika määratlemisel saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades.

1. Minge asukohta **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.
1. Valige suvand **Uus**.
1. Minge väljal **Tööpoliitika nimi** asukohta *Ladustamistöö puudub*.
1. Valige toimingupaanil nupp **Salvesta**.
1. **Töötellimuse tüüpide** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:

    - **Töötellimuse tüüp:** *lõpetatud kaupade ladustamine*
    - **Tööprotsess:** *kõik seotud tööprotsessid*
    - **Töö loomise meetod:** *mitte kunagi*
    - **Ristlaadimise poliitika nimi:** jätke see väli tühjaks.

1. Valige **Lisa** uuesti, et lisada tabelisse teine rida ja seejärel määrake uue rea jaoks järgmised väärtused:

    - **Töötellimuse tüüp:** *kaastoodete ja kõrvalsaaduste ladustamine*
    - **Tööprotsess:** *kõik seotud tööprotsessid*
    - **Töö loomise meetod:** *mitte kunagi*
    - **Ristlaadimise poliitika nimi:** jätke see väli tühjaks.

1. **Varude asukohtade** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:

    - **Ladu:** *51*
    - **Asukoht:** *001*

1. **Toodete** FastTab-il seadistage välja **Tootevalik** väärtuseks *Valitud*.
1. FastTab-il **Tooted** valige käsk **Lisa**, et lisada uus rida tabelisse.
1. Uues reas määrake välja **Kauba number** väärtuseks *L0101*.
1. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-an-output-location"></a>Väljundi asukoha seadistamine

1. Avage **Organisatsiooni haldus \> Ressursid \> Ressursigrupid**.
1. Valige vasakult paneelist ressursigrupp **5102**.
1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Väljastusladu:** *51*
    - **Väljastuskoht:** *001*

1. Valige toimingupaanil nupp **Salvesta**.

> [!NOTE]
> Asukoht *001* pole litsentsiplaadiga juhitav asukoht. Saate seadistada väljundi, mis pole litsentsiplaadiga juhitav, asukoha ainult siis, kui asukohale on olemas vastav tööpoliitika.

### <a name="create-a-production-order-and-report-it-as-finished"></a>Tootmistellimuse loomine ja selle lõpetatuna kinnitamine

1. Avage **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**.
1. Toimingupaanil valige **Uus tootmistellimus**.
1. Seadistage dialoogiaknas **Loo tootmistellimus** välja **Kauba number** väärtuseks *L0101*.
1. Valige tellimuse loomiseks ja dialoogiboksi sulgemiseks **Loo**.

    **Kõik tootmistellimused** lehe tabelisse lisatakse uus tootmistellimus.

    Hoidke uus tootmistellimus valituna.

1. Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Hinda**.
1. Dialoogiaknas **Hinda** lugege hinnangut ja seejärel klõpsake nuppu **OK**, et sulgeda dialoogiaken.
1. Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Alusta**.
1. Seadke dialoogiaknas **Alusta** vahekaardil **Üldine** väli **Automaatne BOM-tarbimine** väärtuseks *Mitte kunagi*.
1. Valige **OK**, et salvestada oma säte ja sulgeda dialoogiaken.
1. Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Kinnita lõpetatuks**.
1. Dialoogiaknas **Lõpetatuks kinnitamine** vahekaardil **Üldine** määrake suvandi **Kinnita tõrge** väärtuseks *Jah*.
1. Valige **OK**, et salvestada oma säte ja sulgeda dialoogiaken.
1. Valige toimingupaani vahekaardil **Ladu** grupis **Seotud teave** üksus **Töö üksikasjad**.

Kui tootmistellimus on lõpetatuks kuulutatud, pole ladustamiseks tööd loodud. Seda käitumist ilmneb, kuna määratletud on tööpoliitika, mis takistab töö loomist, kui toode *L0101* kuulutatakse lõpetatuks asukohale *001*.

## <a name="more-information"></a>Lisateave

Lisateavet mobiilse seadme menüü üksuste kohta vt teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).

Lisateavet, mis on seotud litsentsiplaadi vastuvõtmisega ja tööpoliitikatega, leiate teemast [Litsentsiplaadi vastuvõtmine mobiilirakenduse Warehouse Management kaudu](warehousing-mobile-device-app-license-plate-receiving.md).

Lisateavet sissetuleva koormuse halduse kohta vt teemast [Ostutellimuste sissetulevate koormate laohaldus](inbound-load-handling.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]