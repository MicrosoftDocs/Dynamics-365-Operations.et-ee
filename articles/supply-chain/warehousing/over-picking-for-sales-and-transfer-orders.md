---
title: Müügitellimuste ja üleviimistellimuste ülekorjamine
description: Selles teemas selgitatakse, kuidas lubada müügitellimuste ja üleviimistellimuste ülekorjamist.
author: GalynaFedorova
ms.date: 07/06/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-06
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 3c6f9d386f79754edce38e4e2cf4c9bfefbce69bdb252e8754f39d909827fa02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722147"
---
# <a name="over-picking-for-sales-orders-and-transfer-orders"></a>Müügitellimuste ja üleviimistellimuste ülekorjamine

[!include [banner](../includes/banner.md)]

See teema esitab stsenaariumi, mis näitab, kuidas lubada kas konkreetsel töötajal või kõigil töötajatel ülevalida. Ülekorjamise protsess võimaldab kontrollitud ülekorjamist komplekteerimistöö ajal.

Lao ülekorjamine on lihtne mõiste. Süsteem võimaldab töötajatel valida rohkem kaupu, kui on tellimuse jaoks määratud. Siiski võtab ta arvesse üleviimistellimuse või müügitellimuse rea tasemel määratud ületarne limiiti. Kui see limiit on ületatud, teatab rakendus Warehouse Management töötajatele, et nad ületavad ületarne limiiti.

Ülevalimise funktsioon aitab minimeerida hooldust ja aitab ka teie seadistuses paindlikuks jääda. Saate määratleda ühe või mitu mobiilsideseadme menüükäsku ja lubada ülekorjamise ainult mõnele neist. Samuti saate takistada valitud töötajatel müügitellimuste ja/või üleviimistellimuste ülekorjamist ilma menüükäske muutmata. Selle asemel saate vastava töötaja seadistustes ühe või mõlemad neist võimalustest välja lülitada.

Ülekorjamise funktsioon aitab töötajatel kaupade noppimisel ja saatmisel aega ja vaeva kokku hoida. Näiteks võimaldab funktsioon töötajatel neid ülesandeid täita:

- Kompenseerib kokkutõmbumise komplekteerimise või lähetuse ajal.
- Vältige komplekteerimisprotsessi ajal pakkematerjali lahtipakkimist.
- Kauba kahjude hüvitamine transpordi ajal.
- Koguse või mõõtühiku hälbe lähetamine.
- Minimeerige koguste katkemist numbrimärkidel.
- Vältige materjalijäätmeid ja kallite materjalide nappust.
- Mõõtke komplekteeritud kogus pärast komplekteerimist (näiteks veoauto kaalumise kaudu).

> [!IMPORTANT]
> Ülekorjamise funktsioon rakendub ainult müügi- ja üleviimistellimuste komplekteerimisele ja töötlemisele. Täiendamine ei toeta ülekorjamist. Täiendustöö käivitamisel ei luba süsteem kasutajatel üle valida.

Selle teema stsenaarium näitab, kuidas ülevalimise funktsiooni seadistada ja kasutada.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Stsenaariumi eeltingimus: demoandmete kättesaadavaks tegemine

Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks *USMF*.

## <a name="scenario-setup"></a>Stsenaariumi häälestus

Enne näitestsenaariumi läbimist peate lubama nii asjaomase töötaja kui ka vastava menüüelemendi ülevalimise.

### <a name="set-up-a-worker-to-allow-for-over-picking"></a>Seadistage töötaja, kes lubab üle korjata

Siin on üldine protseduur töötaja seadistamiseks, et võimaldada eraldi müügitellimuste ja ülekandetellimuste ülevalimist. See konfiguratsioon reguleerib, milline komplekteerimistöötaja saab ülekorjamist teha ja kas see töötaja saab teha ülekorjamist nii üleviimistellimuste kui ka müügitellimuste puhul.

1. Avage jaotis **Laohaldus \> Seadistus \> Töötaja**.
1. Valige loendi paanist **Julia Funderburk**.
1. Valige kiirkaardil **Kasutajad** järgmiste väärtustega rida. Kui need väärtused puuduvad, looge see.

    - **Kasutaja ID:** *24*
    - **Kasutajanimi:** *WH 24*
    - **Vaikeladu:** *24*
    - **Menüü nimi:** *Peamine*

1. Seadke kiirkaardil **Töö** kasutajale *24* järgmised väärtused, kui neid ei ole veel seatud:

    - **Luba müügi ülekirje:** *Jah*
    - **Luba üleviimistellimus komplekteerimise ajal:** *jah*

### <a name="set-up-a-mobile-device-menu-item-to-allow-for-over-picking"></a>Seadistage mobiilseadme menüüelement ülevalimise lubamiseks

Siin on üldine protseduur mobiilseadme menüüelemendi konfigureerimiseks ülevalimise lubamiseks. Sõltuvalt teie ettevõtte nõudmistest mobiilseadmete menüüd kasutava töötaja lubade taseme suhtes võidakse mõned parameetrid sisse või välja lülitada.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige loendipaanil kirje nimega *Müügikorje*. Kui see nimi pole olemasolevatel kirjetel, looge see. Kinnitage või määrake kirjele järgmised väärtused:

    - **Menüükäsu nimi:** *müügi komplekteerimine*
    - **Pealkiri:** *Müügi komplekteerimine*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Jah*
    - **Lavastaja:** *Kasutaja suunal*
    - **Sihtlitsentsiplaadi alistamine:** *jah*
    - **Numbrimärgi alistamine panemise ajal:** *jah*
    - **Hoia töö kasutaja poolt lukustatuna:** *jah*
    - **Luba ülekorje:** *jah*

> [!IMPORTANT]
> Kui asjakohased parameetrid nii töötaja kui ka mobiilseadme menüüelemendi jaoks on lubatud, saab ülevalimist töödelda ainult mobiilseadme kaudu.

## <a name="example-scenario"></a>Näidisstsenaarium

Pärast eeltingimuste, töötaja häälestuse ja menüükäsu häälestuse paika panemist olete valmis selle funktsiooniga töötama.

### <a name="create-a-sales-order-that-allows-for-overdelivery"></a>Ületarnet võimaldava müügitellimuse loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Uue müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *24*

1. Valige nupp **OK**.
1. Avatakse uus müügitellimus. Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega rida.

    - **Kauba kood:** *A0001*
    - **Kogus:** *10*

1. Määrake kiirkaardi **Rea üksikasjad** vahekaardil **Tarne** välja **Ületarne** väärtuseks *10*.
1. Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.
1. Sulgege leht **Reserveerimine**.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

Kui väljalase on lõpule viidud, saate teabesõnumeid, mis näitavad loodud voo ja koormuse ID-sid.

### <a name="get-the-work-id-and-license-plate-number-for-the-new-order"></a>Hankige uue tellimuse jaoks töö ID ja numbrimärk

Kui vabastasite müügitellimuse lattu, oleks süsteem pidanud loonud uue töö-ID, millel on üks korjerida. Töö ID ja numbrimärgi määramise leidmiseks järgige neid samme.

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Otsige ruudustikust **Ülevaade** veergu **Tellimuse number** äsja loodud müügitellimuse kohta. Märkige müügitellimuse kohta vastav töö ID.
1. Valige rida uue müügitellimuse jaoks, et kuvada seotud teave ruudustikus **Read**. Märkige asukoht, kust kaup komplekteeritakse.
1. Avage **Laohaldus \> Päringud ja aruanded \> Vabade kaubavarude loend**.
1. Valige toimingupaanil **Dimensioonid**.
1. **Dimensiooni kuva** dialoogikaknas veenduge, et ruudud **Litsentsiplaat**, **Laduja** **Kaubakood** on märgitud ja seejärel valige **OK**.
1. Määrake paanil **Filter** järgmised filtrid.

    - **Kaubakood** – **üks (mitmest)** – *A0001*
    - **Ladu** – **algab väärtusega** – *24*

1. Valige **Rakendamine**.
1. Märkige üles kuvatavad **litsentsiplaadi** väärtused.

### <a name="over-pick-the-order-by-using-the-warehouse-management-mobile-app"></a>Tellimuse ülevalimine Warehouse Management mobiilirakenduse abil

1. Logige mobiilirakendusse Warehouse Management sisse lao *24* kasutajana.
1. Avage **Väljaminev \> Müügi komplekteerimine**.
1. Sisestage väljale **Töö ID või numbrimärgi** skannimine müügitellimuse jaoks loodud töö ID.
1. Valige **OK** (märke sümbol).
1. Valige **Ülekorje**.
1. Määrake välja **Vali kogus** väärtuseks *14*.
1. Valige **OK** (märke sümbol).

    Lehel **Üle noppimise** saate järgmise teate: "Rea ületarne on 40,00 protsenti, kuid lubatud ületarne on ainult 10,00 protsenti." See teade näitab, et teie sisestatud koguse kogus ületab üleedastuse limiidi. Müügitellimuse rea ületarne limiit on 10 protsenti. Seetõttu saate määratud koguse 10 puhul üle noppida ainult 1-ga kogu noppimiskoguse 11 puhul.

1. Määrake välja **Vali kogus** väärtuseks *11*.
1. Valige **OK** (märke sümbol).
1. Sisestage väljale **Numbrimärk** numbrimärk, mille eelmises jaotises tähele panite.
1. Sisestage väljale **Sihtnumbrimärk** sihtidentifitseerimisnumber. Pange tähele, et kuvatakse komplekteerimise asukoht (*FLOOR-001*), kaup (*A0001*) ja kogus (*11 tk*).
1. Valige **OK** (märke sümbol).
1. Vaadake üle teave lehel **Ostutellimused – sisestatud**. Väli **Loc** peaks näitama, et komplekteeritud kaubad lähevad asukohta *BAYDOOR*.
1. Valige **OK** (märke sümbol).

Lehel **Skanni töö ID / identifitseerimisnumbri ID** teade „Töö lõpule viidud”. See teade näitab, et müügitellimuse töö-ID on lõpule viidud ja ülevalitud kogus ei ületa 10-protsendilist üleedastamise piirmäära.
