---
title: Laovoogude numbriseeriate konfigureerimine
description: Selles teemas antakse ülevaate funktsioonist, mis annab identifitseerimisnumbri ID-de, voo siltide ID-de, konteineri ID-de ja veokirja ID-de numbriseeria laiendusi.
author: GarmMSFT
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSNumberSequenceExt
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: e9ba06908b9e82763557e98715e495cfaf649753
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574709"
---
# <a name="configure-number-sequences-for-warehouse-flows"></a>Laovoogude numbriseeriate konfigureerimine

[!include [banner](../includes/banner.md)]

Funktsioon *Numbriseeria laiendused* lisab uue konfiguratsiooni lehe numbriseeriate seadistamiseks. See võimaldab GS1-reguleeritud ID-de, sh GS1-eesliidete ja kontrollnumbrite (modulo 10) paindlikku konfiguratsiooni ja jõustab olemasolevate numbriseeriate pikkuse piirangu.

Standardsed numbriseeriate segmendid ei sobi GS1 rakendamiseks, kuna kontrollnumbrit ei arvutata ja ettevõtte GS1-eesliide tuleb käsitsi uuendada.

See funktsioon lisab järgmised funktsioonid.

- Veokirja (BOL) ID-sid saab eelnevalt luua.
- Konteineri seeriaviisilise lähetamise koodi (SSCC) numbrite jaoks saab luua kordumatu numbriseeria.
- GS1-ga ühilduvaid numbriseeriaid saab luua veokirja ja SSCC-numbrite jaoks. Selles funktsioonis on lisatus valmistugi identifitseerimisnumbri ID, konteineri ID, voo sildi ID ja veokirja ID jaoks.
- Identifitseerimisnumbri ID numbrite konfiguratsioon on paindlik. Näiteks saate kaasata või välistada rakenduse identifikaatoreid (AI), nt nullid alguses (00).

See funktsioon hõlbustab kastide sildistamise toetamist ja süsteemi loodud uute numbrite kohandamist.

## <a name="turn-on-the-number-sequence-extensions-feature"></a>Funktsiooni Numbriseeria laiendused sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Numbriseeria laiendused*

## <a name="set-up-the-feature"></a>Funktsiooni seadistamine

Teie süsteemis numbriseeria laienduste seadistamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Sisestage vahekaardi **Üldine** väljale **GS1 ettevõtte eesliide** oma ettevõtte GS1-eesliide. See väärtus mõjutab kõiki numbriseeriaid, kus GS1-eesliide on segmendina kaasatud.
1. Kui soovite luua voo siltide jaoks veokirja numbreid, märkige vahekaardil **Aruanded** ruut **Loo veokirja number voo siltide printimisel**.

    > [!NOTE]
    > See märkeruut on saadaval ainult siis, kui [voo sildi printimise](configure-wave-label-printing.md) funktsioon on sisse lülitatud.

1. Avage jaotis **Laohaldus** \> **Seadistus** \> **Numbriseeria laiendused**
1. Valige toimingupaanilt suvand **Loo vaikeseadistus**. Luuakse GS1-ga ühilduv veokirja numbriseeria ja kolme tüüpi SSCC-i numbriseeriad. Kõik need numbriseeriad arvestavad teie ettevõtte GS1-eesliite pikkust.

    Vaadake lisateavet nende vaikimisi numbriseeriate kohandamise ja/või uute seeriate lisamise kohta järgmisest jaotisest. Saate ka eemaldada seeriaid, mida te ei vaja.

1. Naaske jaotisse **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Valige vahekaardil **Numbriseeriad** vastav numbriseeria laiendus, mida soovite kasutada oma identifitseerimisnumbri ID-de, voo sildi ID-de, konteineri ID-de (sel juhul valige sobiv seeria **SSCC‑18 number**) ja/või veokirja ID-de (sellisel juhul valige seeria **Veokiri**) jaoks numbrite loomiseks. Vaikimisi toetatakse numbriseeria laiendusi ainult nende nelja tüüpi ID-de puhul.

Järgmine kord, kui luuakse uus number ühele neist numbriseeriatest, kasutatakse uut loogikat.

> [!NOTE]
> Kui te ei vali numbriseeria laiendust identifitseerimisnumbri ID jaoks, kasutatakse identifitseerimisnumbri ID-de loomiseks kehtivaid reegleid. Muul juhul kasutatakse teie valitud numbriseeriat. Teised ID-d kasutavad tavalist numbriseeriat, kuni rakendate neile numbriseeria laienduse.

## <a name="create-and-edit-number-sequences"></a>Numbriseeriate loomine ja redigeerimine

Eelmises jaotises lõite numbriseeriate vaikekogumi. Selles jaotises selgitatakse iga numbriseeria määratlemist. Samuti selgitatakse, kuidas luua kohandatud seeriaid ja kuidas redigeerida vaikimisi või kohandatud seeriaid.

Numbriseeriate loomiseks ja redigeerimiseks toimige järgmiselt.

1. Avage jaotis **Laohaldus** \> **Seadistus** \> **Numbriseeria laiendused**.
1. Valige toimingupaanil nupp **Uus**.
1. Sisestage uue seeria nimi väljale **Numbriseeria laiendus**. Väljale **Kirjeldus** sisestage kirjeldus.
1. Kasutage kiirkaardil **Segmendid** tööriistariba nuppe oma numeratsiooni vormingu koostamiseks, lisades, kustutades ja korraldades segmente. Määrake välja **Segment** igal real segmendi tüüp, et määratleda segmendi eesmärk ja sisu. Järgmises tabelis kirjeldatakse saadaolevaid segmentide tüüpe.

    | Segmendi tüüp | Kirjeldus |
    |---|---|
    | Konstant | See segmendi tüüp lisab sama konstandi teksti igale loodud numbrile seerias. Sisestage väljale **Väärtus** nõutav tekst. Välja **Pikkus** pikkus uuendatakse automaatselt väljale **Väärtus** sisestatud teksti pikkuse järgi. |
    | Numbriseeria | Sisestage väljale **Väärtus** numbrimärk (*\#*) iga tähemärgi kohta, mis tuleks loodud seerias kuvada. Numbriseeria võib ise luua pikemaid numbreid, kuid kuvatakse ainult kõige parempoolsemad tähemärgid. Välja **Pikkus** numbrimärkide hulk uuendatakse automaatselt väljale **Väärtus** sisestatud numbrimärkide järgi.<p>SSCC-18 numbrite GS1 nõuete täitmiseks veenduge, et selle segmendi pikkus oleks 16 miinus teie GS1-eesliite pikkus.</p> |
    | GS1 eesliide | See segmendi tüüp lisab väärtuse, mis on määratud lehe **Laohalduse parameetrid** väljal **GS1 ettevõtte eesliide**. Väljal **Väärtus** kuvatakse väärtus, mis on määratud lehel **Laohalduse parameetrid** ja väljal **Pikkus** kuvatakse selles väärtuses olevate tähemärkide arv. Väljad **Väärtus** ja **Pikkus** on kirjutuskaitstud. |
    | Rakenduse identifikaator | Sisestage väljale **Väärtus** rakenduse identifikaator, mille määratleb vastav GS1 poliitika seda tüüpi numbriseeria puhul. Sisestage näiteks *00* SSCC puhul või *420* veokirja puhul. Välja **Pikkus** pikkus uuendatakse automaatselt väljale **Väärtus** sisestatud identifikaatori pikkuse järgi. |
    | Pakkimistüüp | Kaupade puhul, mida on võimalik selgelt tuvastada, lisab see segmendi tüüp vastava ühiku seeriagrupi (lehelt **Ühiku seeriagrupid**) välja väärtuse. (See käitumine vastab identifitseerimisnumbri ID olemasolevale loogikale.) Mitut varude arvestusühikut (SKU) sisaldavate identifitseerimisnumbrite puhul lisab see segmendi tüüp vaikimisi väärtuse *0* (null). Selle segmendi tüübi puhul on välja **Väärtus** väärtuseks alati seatud *P* ja välja **Pikkus** väärtuseks alati *1*.|
    | Kontrollnumber | See segmendi tüüp lisab kontrollnumbri, mis on modulo 10 arvutus. (See käitumine vastab identifitseerimisnumbri ID olemasolevale loogikale.) Selle segmendi tüübi puhul on välja **Väärtus** väärtuseks alati seatud nool (*^*) ja välja **Pikkus** väärtuseks alati *1*. |

1. Oma lõpliku numbrivormingu näite kuvamiseks kontrollige välja **Vorming** kiirkaardi **Segmendid** allosas.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]