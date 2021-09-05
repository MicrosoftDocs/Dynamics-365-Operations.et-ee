---
title: GS1-vöötkoodid ja QR-koodid
description: See teema kirjeldab, kuidas seadistada GS1 vöötkoode ja QR-koode nii, et silte saab laos skannida.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ef28fcaf308225a78bcbac42f591e6b24b21b1b1
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384533"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1-vöötkoodid ja QR-koodid

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Laotöötajad peavad mobiilse seadme skanneri kasutamisel kauba, paleti või konteineri liikumise registreerimiseks täitma mitu ülesannet. Need ülesanded võivad hõlmata nii vöötkoodide skannimist kui ka teabe käsitsi sisestamist mobiilsesse seadmesse. Vöötkoodid kasutavad ettevõtteomast vormingut, mille määratlete ja haldate Microsoft Dynamics 365 Supply Chain Management abil.

GS1 vöötkood ja QR-koodi vormingud lähetussiltide jaoks töötati välja globaalse standardi andmiseks ettevõtetevaheliseks andmevahetuseks. GS1-vormingud mitte ainult ei kodeeri andmeid, vaid lubavad kasutada ka *rakenduse identifikaatorite* eelmääratletud loendit andmete tähenduse määratlemiseks. GS1-standard määrab andmevormingu ja erinevad andmed, mida seda saab kasutada kodeerimiseks. Erinevalt vanematest vöötkoodidest, võib GS1 vöötkoodil olla mitu andmeelementi. Seetõttu võib ühe vöötkoodi skannimine hõivada mitut tüüpi tooteteavet, nagu näiteks partiid ja aegumiskuupäeva.

GS1-tugi Supply Chain Management lihtsustab märgatavalt skannimisprotsessi ladudes, kus kaubaalused ja konteinerid on GS1-vormingus koodide abil märgistatud. Laotöötajad saavad kogu vajaliku teabe ekstraktida ühe GS1 vöötkoodi skannimisega. Eemaldades vajaduse teha mitu skannimist ja/või sisestada teavet käsitsi, aitavad GS1 vöötkoodid vähendada ülesannetega seostatud aega. Ühtlasi aitavad need ka parandada täpsust.

Logistikahaldurid peavad seadistama nõutava rakenduse identifikaatorite loendi ja seostama iga neist sobiva mobiilse seadme menüü-üksustega. Rakenduse identifikaatoreid saab seejärel kasutada läbi ladude globaalse sättena teisaldamisel ja pakkimisel. Seetõttu, on kõigil saadetise siltidel ühtne vorm.

Kui pole teisiti määratud, kasutab see teema terminit *vöötkood* et viidata nii vöötkoodile kui ka QR-koodidele.

## <a name="turn-on-the-gs1-feature"></a>Funktsiooni GS1 sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *GS1 vöötkoodide skannimine*

## <a name="set-up-global-gs1-options"></a>Globaalsete GS1-i suvandite seadistamine

**Warehouse management parameetrite** lehel on sätted, mis loovad globaalsed GS1-suvandid.

Globaalsete GS1 suvandite seadistamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Kiirkaardil **Vöötkoodid** määrake järgmised väljad:

    - **FNC1 märk** – määrake märgid, mida tuleks vöötkoodi sõelumisel eesliitena tõlgendada.
    - **Andmemaatriks märk** – määrake märgid, mida tuleks tõlgendada eesliitena, kui andmemaatriksit sõelutakse.
    - **QR koodi märk** – määrake märgid, mida tuleks vöötkoodi sõelumisel eesliitena tõlgendada.
    - **Grupieraldaja** – määrake märk, mis tuvastab vöötkoodi või QR-koodi eraldiseisvad osad.
    - **Maksimaalne identifikaatori pikkus** – määrake rakenduse ID lubatud maksimaalne märkide arv.

> [!NOTE]
> Eesliited ütlevad süsteemile, et vöötkood krüptitakse vastavalt GS1 standardile. Kuni kolme eesliite (**FNC1 märk**, **Andmemaatriksi märk** ja **QR-koodi märk**) ja saab kasutada üheaegselt erinevatel eesmärkidel.

## <a name="gs1-application-identifiers"></a>GS1 rakenduse identifikaatorid

GS1-vormingud mitte ainult ei kodeeri andmeid, vaid lubavad kasutada ka rakenduse identifikaatorite eelmääratletud loendit andmete tähenduse määratlemiseks. Logistikahaldurid peavad seadistama nõutava rakenduse identifikaatorite loendi ja seostama iga neist sobiva mobiilse seadme menüü-üksustega. Rakenduse identifikaatoreid saab seejärel kasutada läbi ladude globaalse sättena teisaldamisel ja pakkimisel. Seetõttu, on kõigil saadetise siltidel ühtne vorm.

Süsteem kasutab andmeid, eriti eelmääratletud rakenduse identifikaatoreid, et kehtestada reeglid, mida tuleks rakendada vastava skannitud teabe tükile.

Iga rakenduse identifikaator annab süsteemile signaali, et skannitud vöötkoodi järgnevaid märke tuleks käsitleda krüptitud teabe blokina. Rakenduse ID seadistus määrab, kuidas süsteem peaks vöötkoodi tõlgendama ja salvestama selle väärtusena süsteemis.

Logistikahaldurid saavad kasutada standardseid rahvusvahelisi rakenduse identifikaatoreid ja/või luua oma identifikaatoreid.

### <a name="load-the-standard-application-identifiers"></a>Laadi rakenduse standardsed identifikaatorid

Kiireks alustamiseks saate laadida ühiste rahvusvaheliste rakenduse idendifikaatorite loendi. Seejärel saate loendit vajaduse korral laiendada või redigeerida.

Rakenduse standardsete ID-de laadimiseks järgige neid samme.

1. Minge **Warehouse management \> seadistuse \> GS1 \> GS1 rakenduse identifikaatoritele**.
1. Valige toimingupaanilt suvand **Loo vaikeseadistus**.

> [!WARNING]
> **Vaikeseadistuse loomise** käsk kustutab kõik praegu määratletud rakenduse ID-d ja asendab need standardloendiga. Kuid pärast vaikeseadistuse laadimist saate loendit vastavalt vajadusele kohandada.

### <a name="set-up-custom-application-identifiers"></a>Kohandatud rakenduse ID-de loomine

Kui mõned või kõik rakenduse identifikaatorid, mida teie ettevõte kasutab, erinevad standardkomplektist, saate luua nullist või kohandada standardikomplekti vastavalt vajadusele.

Oma GS1 rakenduse identifikaatorite häälestamiseks ja kohandamiseks järgige neid samme.

1. Minge **Warehouse management \> seadistuse \> GS1 \> GS1 rakenduse identifikaatoritele**.
1. Järgige üht neist sammudest.

    - Uue identifikaatori loomiseks: valige toimingupaanilt suvand **Uus**.
    - Olemasoleva ID redigeerimiseks: valige ID ja seejärel valige tegevuspaanil käsk **Redigeeri**.

1. Seadke uue või identifikaatori jaoks järgmised väljad:

    - **Rakenduse identifikaator**– sisestage rakenduse ID-kood rakenduse identifikaatorisse. Tavaliselt on see kood kahekohaline täisarv, kuid see võib olla ka pikem. Kümnendkoha puhul näitab viimane number komakohtade arvu. Lisateabe saamiseks vaadake selle loendi hiljem märkeruudu **Koma** kirjeldust.
    - **Kirjeldus** – sisestage identifikaatori lühikirjeldus.
    - **Fikseeritud pikkus** – märkige see ruut, kui selle rakenduse ID abil skannitud väärtustel on fikseeritud arv märke. Kui väärtuste pikkus on muutuv, tühjendage see ruut. Sellisel juhul peate määrama väärtuse lõpu, kasutades grupieraldaja märki, mille määrasite **Warehouse management parameetrite** lehel.
    - **Pikkus** - Sisestage maksimaalne märkide arv, mis võivad ilmuda selle rakenduse identifikaatori abil skannitud väärtustes. Kui ruut **Fikseeritud pikkus** on märgitud, eeldatakse täpselt seda märkide arvu.
    - **Tüüp** - valige väärtuse tüüp, mida selle rakenduse ID abil skannitakse (*numbriline*, *täht* või *kuupäev*). Kuupäevade puhul on eeldatav vorming YYMMDD (ilma tühikute või sidekriipsudeta).
    - **Kümnendkoht** - Märkige see ruut, kui väärtus sisaldab kaudset kümnendkohta. Kui see ruut on märgitud, kasutab süsteem rakenduse ID viimast numbrit kümnendkohtade arvu määramiseks. Kui rakenduse ID on näiteks *3205*, tõlgendatakse väärtuse kõige parempoolset viit numbrit koma järel.

> [!NOTE]
> **Warehouse management parameetrite** lehel määratud grupieraldaja on valikuline, kui rakenduse identifikaatoriga jälgitav väärtus on fikseeritud pikkusega või kui selle pikkus on suurendatud (st kui pikkus võrdub rakenduse ID jaoks seadistatud **pikkuse** väärtusega).

## <a name="establish-the-generic-gs1-setup"></a>Üldise GS1 häälestuse häälestamine

Üldise GS1 häälestus loob ühiste vastenduste kogumi. Need vastendused vastavad igale mobiilirakenduse asjakohasele sisendväljale rakenduse identifikaatoriga, mis kontrollib, kuidas skannitud vöötkoodide väärtusi tuleb sellel väljal tõlgendada ja talletada. Vaikimisi kehtivad need sätted kõigi mobiilse seadme menüü-üksuste skannimise puhul. Ühe või mitme konkreetse välja koodi saab siiski üle kirjutada konkreetsele menüü üksusele määratud GS1 poliitikaga.

Üldise GS1 seadistusega saab korraga skannida ainult üht väärtust. Seega, kui soovite ühe skannimisega laadida mitu väljaväärtust, peate seadistama GS1 poliitika vastavatele menüü-üksustele.

Lisateavet GS1 poliitikate kohta leiate järgmisest jaotisest.

### <a name="load-the-standard-generic-gs1-setup"></a>Laadi standardne üldine GS1 häälestus

**GS1 üldine seadistus** leht võimaldab teil laadida standardse vastenduste komplekti mobiilse seadme väljade ja standardsete rakenduse identifikaatorite vahel, mille on loonud vaikeseadistus.

Üldise GS1 häälestuse loomiseks minge **Warehouse management \> seadistuse \> GS1 \> GS1 üldisesse seadistusse**. Seejärel valige käsk **Loo vaikeseadistus**, et määrata igale mobiiliseadme menüü-üksustes tavaliselt kasutatavale väljale automaatselt sobiv rakenduse ID.

> [!WARNING]
> Kui mõni üldine GS1 seadistus on juba olemas, kustutab **vaikeseadistuse** loomise käsk selle täielikult ja laadib standardseadistuse.

### <a name="customize-the-standard-generic-gs1-setup"></a>Kohandage standardset üldist GS1 häälestust

GS1 üldise seadistuse kohandamiseks järgige neid samme.

1. Minge **Warehouse management \> seadistuse \> GS1 \> GS1 üldine seadistus**.
1. Järgige üht neist sammudest.

    - Uue vastenduse loomiseks: valige toimingupaanilt suvand **Uus**.
    - Olemasoleva vastenduse redigeerimiseks: valige vastendamine ja seejärel valige tegevuspaanil käsk **Redigeeri**.

1. Seadke uue või valitud vastenduse jaoks järgmised väljad:

    - **Väli** - valige või sisestage mobiilirakenduse sisendväli, millele sissetuleva väärtus peaks olema määratud. Väärtus pole kuvatav nimi, mida töötajad näevad. Selle asemel on see võtme nimi, mis määratakse aluseks oleva koodi väljale. Vaikeseadistus annab väljade kogumi, mis on ilmselt kasulik, ning kaasab intuitiivsete võtmenimed igale väljale ja vastavad programmistatud funktsioonid. Teil võib siiski olla vaja oma arenduspartneritele teada saada õigeid valikuid oma rakendusse.
    - **Rakenduse ID** - valige rakendatav rakenduse ID, nagu määratud **GS1 rakenduse ID-d** lehel. Identifikaator määrab, kuidas tuleks vöötkoodi tõlgendada ja salvestada väärtusena nimelise välja jaoks. Pärast rakenduse ID valimist kuvatakse **Kirjeldus** väljal selle kirjeldust.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Saate häälestada GS1 poliitikaid, mida saate mobiilse seadme menüü-üksustele määrata

Standardi GS1 eesmärk on võimaldada töötajatel ühe vöötkoodi skannimisel laadida mitu väärtust. Selle eesmärgi saavutamiseks peavad logistikahaldurid seadistama GS1 poliitika, mis teavitab süsteemi mitme väärtusega vöötkoodide tõlgendamisest. Hiljem saate määrata poliitikad mobiilse seadme menüü-üksustele, et kontrollida, kuidas vöötkoodi tuleb tõlgendada, kui töötajad seda skannivad, kui nad kasutavad konkreetset menüükäsku.

Kui menüükäsu jaoks ei ole GS1 poliitikat määratud, saab süsteem hõivata ainult ühe väärtuse. See väärtus rakendatakse mobiilse rakenduse sisenditele, mis valitakse siis, kui töötaja skannib, nagu on määratud üldises GS1 häälestuses. Kui menüü üksusele on määratud GS1 poliitika, kasutab süsteem siiski üldist GS1 häälestust, et vastendada esimene vöötkoodi väärtus valitud väljale. Seejärel saab see hõivata lisaväljaväärtusi, nagu on määratud rakendatava poliitikaga.

### <a name="load-the-standard-specific-gs1-policies"></a>Laadi standardsed konkreetsed GS1-poliitikad

Kiireks alustamiseks saate laadida GS1 poliitikad. Seejärel saate poliitikaid vajaduse korral laiendada või redigeerida.

Rakenduse standardsete ID-de laadimiseks järgige neid samme.

1. Avage **Warehouse management \> Seadistus \> GS1 \> GS1 poliitika**.
1. Valige toimingupaanilt suvand **Loo vaikeseadistus**.

> [!WARNING]
> **Vaikeseadistuse loomise** käsk kustutab kõik praegu määratletud poliitikad ja asendab need standardse poliitikate seadistamisega. Kuid pärast vaikeseadistuse laadimist saate poliitikaid vastavalt vajadusele kohandada.

### <a name="set-up-custom-specific-gs1-policies"></a>Saate häälestada kohandatud konkreetseid GS1-poliitikaid

Oma GS1-poliitikate häälestamiseks ja kohandamiseks järgige neid samme.

1. Avage **Warehouse management \> Seadistus \> GS1 \> GS1 poliitika**.
1. Järgige üht neist sammudest.

    - Uue poliitika loomiseks: valige toimingupaanilt suvand **Uus**.
    - Olemasoleva poliitika redigeerimiseks: valige see poliitika loendipaanilt.

1. Määrake uue või valitud poliitika päises järgmised väärtused:

    - **Poliitika nimi** – sisestage poliitikale nimi.
    - **Kirjeldus** – sisestage poliitika lühikirjeldus.

1. Päise all oleval kiirkaardil vastendage väljade nimed rakenduse identifikaatoriga nagu praeguse poliitika puhul on nõutud. Kasutage järgmisi nuppe tööriistaribal, et lisada ja eemaldada kirjeid vastavalt vajadustele. Määrake igas reas järgmised väljad.

    - **Väli** - valige või sisestage mobiilirakenduse sisendväli, millele sissetuleva väärtus peaks olema määratud. Väärtus pole kuvatav nimi, mida töötajad näevad. Selle asemel on see võtme nimi, mis määratakse aluseks oleva koodi väljale. Vaikeseadistus annab väljade kogumi, mis on ilmselt kasulik, ning kaasab intuitiivsete võtmenimed igale väljale ja vastavad programmistatud funktsioonid. Teil võib siiski olla vaja oma arenduspartneritele teada saada õigeid valikuid oma rakendusse.
    - **Rakenduse ID** - valige rakendatav rakenduse ID, nagu määratud **GS1 rakenduse ID-d** lehel. Identifikaator määrab, kuidas tuleks vöötkoodi tõlgendada ja salvestada väärtusena nimelise välja jaoks. Pärast rakenduse ID valimist kuvatakse **Kirjeldus** väljal selle kirjeldust.
    - **Sortimine**– iga mitme väärtusega vöötkood hõlmab rakenduse identifikaatorite seeriat, millest igaühele järgneb väärtus. Rakendatav GS1 poliitika tuvastab, milline rakenduse identifikaator on vastendatud igale andmebaasi väljale. Siiski, kui vöötkood kasutab sama rakenduse ID-d rohkem kui üks kord, kasutab süsteem järjekorda, milles rakenduse ID-d ilmuvad koodis nende vastendamiseks väljadega. Ridade puhul, mis jagavad rakenduse ID-d ühe või mitme reaga, kasutage seda välja ühtivate ridade töötlemise järjestuse loomiseks. Esimesena töödeldakse rida, mille sortimisväärtus on madalaim.

> [!NOTE]
> Vöötkoodide puhul, mis sisaldavad rohkem kui üht ja sama rakenduse ID-d, *peate* kasutama **sortimisel** loomiseks sortimisvälja.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1 poliitikate määramine mobiilse seadme menüü-üksustele

Vaikimisi annavad kõik mobiilse seadme menüü-üksused sisendväljad, kus töötajad saavad üldise GS1 häälestuse kohaselt skannida ühte väärtust. Kui soovite, et töötajad saaksid skannida ühe skannimisel mis tahes mobiilse seadme menüü-üksuse jaoks rohkem kui ühte välja väärtust, peate järgmiste sammude abil määrama GS1 poliitika.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Saate luua või avada menüükäsu.
1. Kiirkaardil **Üldine** seadke **GS1 poliitika** väli rakenduv poliitika menüü üksusele.

## <a name="gs1-setup-example"></a>GS1 seadistuse näide

See näide kehtib süsteemi kohta, kus GS1 valikud on seadistatud viisil:

- **Warehouse management parameetrite** lehel luuakse järgmised globaalsätted:

  - **FNC1 märk:** *\]C1*
  - **Grupi eraldaja:** *\~*

- **GS1 rakenduse ID-d** lehel on selle näite puhul asjakohased järgmised rakenduse ID-d.

    | Rakenduse identifikaator | Kirjeldus | Fikseeritud pikkus | Pikkus | Tüüp | Kümnendkoht |
    |---|---|---|---|---|---|
    | 1 | GTIN | Valitud | 14 | Numbriline | Tühjendatud |
    | 10 | Partii number | Tühjendatud | 20 | Tähtnumbriline | Tühjendatud |
    | 17 | Aegumiskuupäev | Valitud | 6 | Kuupäev | Tühjendatud |
    | 30 | Koguse vastuvõtmine | Tühjendatud | 8 | Numbriline | Tühjendatud |

- **Üldisel GS1 seadistus** lehel on selle näite puhul asjakohased üldise GS1 poliitika järgmised sätted.

    | Field | Rakenduse identifikaator | Kirjeldus |
    |---|---|---|
    | ItemId | 1 | GTIN |

- **GS1 poliitika** lehel on poliitika, kus **poliitika nime** väli on seatud väärtusele *Ostu vastuvõtmine*. Poliitika hõlmab järgmisi ridu.

    | Field | Rakenduse identifikaator | Kirjeldus | Sorteerimine |
    |---|---|---|---|
    | Aegumiskuupäev | 17 | Aegumiskuupäev | 0 |
    | InventariPartiiId | 10 | Partii number | 0 |
    | Kogus | 30 | Koguse vastuvõtmine | 0 |

- **Mobiilse seadme menüü-üksuste** lehel on menüü käsk nimega *Ostu vastuvõtmine*. Selle **GS1 poliitika** väli on seatud väärtusele *Ostu vastuvõtmine*.

Kui ostutellimuse kaubad on lattu saabunud, järgib töötaja neid samme.

1. Valige mobiilse seadme menüüelement **Ostu ladustamine**.
1. Sisestage ostutellimuse number.
1. Valige väli **Kaup** ja skannige järgmine vöötkood: *\]C10100000012345678\~3030\~10b1\~17220215*.

Selle näite jaoks loodud sätete tõttu sõelub süsteem skannitud vöötkoodi järgmisel viisil.

| Välja võti | Rakenduse ID | Väärtus | Paberraha |
|---|---|---|---|
| ItemId | 1 | 00000012345678 | Kuna töötaja skanniti väljale **Kaup**, vastendatakse vöötkoodi esimene väärtus selle väljaga. Vastendamine võetakse GS1 üldisest seadistusest. |
| Kogus | 30 | 30 | Kuna ühe skannimisega fikseeritakse mitu välja väärtust, võetakse see vastendamine ja kõik ülejäänud vastendamised GS1 poliitikast, mis on määratud menüükäsu **Ostu vastuvõtt**. See väärtus on saadud kogus. |
| InventariPartiiId | 10 | b1 | See väärtus on vaikesäte. |
| Aegumiskuupäev | 17 | 220215 | Kuupäevavorming on AAKKPP. Seepärast on aegumiskuupäev 15. veebruar 2022. |

Seejärel registreeritakse sissetulek ja pärast üksikut skannimist sisestatakse vastavad andmebaasi väärtused.
