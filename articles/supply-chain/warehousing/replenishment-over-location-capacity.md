---
title: Täiendamine üle asukoha võimsuse
description: Selles teemas antakse teavet funktsiooni Täiendamine üle asukoha võimsuse kohta. See funktsioon võimaldab kogu päevast loodavat täiendamistööd ja selle abil saab hallata selle täiendustöö kättesaadavust, tagamaks, et komplekteerimise asukoht jääks varudeta ega ületaks võimsust.
author: mirzaab
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocationLimit
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 6ff9f133010ec4370a99c585259aece4e279f801
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778203"
---
# <a name="replenishment-over-location-capacity"></a>Täiendamine üle asukoha võimsuse

[!include [banner](../includes/banner.md)]

Mõned suurte mahtudega piiratud ruumiga laod peavad lähetama suuremaid kaubakoguseid, kui need mahuvad nende komplekteerimisasukohta. Funktsioon *Täiendamine üle asukoha võimsuse* võimaldab kogu päevast loodavat täiendamistööd ja selle abil saab hallata selle täiendustöö kättesaadavust, tagamaks, et komplekteerimise asukoht jääks varudeta ega ületaks võimsust.

Funktsioon võimaldab luua rohkem täiendustöid, kui mahub asukohta ja see blokeerib täiendustööde lõpuleviimise, kui asukoht on täis. Kuna komplekteerimisasukoha varud langevad alla konfigureeritava läve, muutub rohkem täiendustööd kättesaadavaks.

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a>Funktsiooni Täiendamine üle asukoha võimsuse sisselülitamine

Selle funktsiooni kättesaadavaks muutmiseks lülitage [funktsioonihalduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sisse järgmised funktsioonid (vastavas järjekorras).

1. Organisatsiooni üleorganisatsiooniline töö blokeerimine (tarneahela halduse versiooni 10.0.21 kohaselt on see funktsioon kohustuslik, seega lülitatakse see vaikimisi sisse ja seda ei saa uuesti välja lülitada.)
1. Täiendamine üle asukoha mahutavuse

## <a name="set-up-the-feature-for-the-example-scenario"></a>Funktsiooni häälestamine näidisstsenaariumi jaoks

Sellest jaotisest leiate juhised ja näite selle funktsiooni häälestamise ning näidisandmete ettevalmistamise kohta teemas hiljem esitatud näidisstsenaariumi jaoks.

### <a name="enable-sample-data"></a>Luba näidisandmed

Selle [näidisstsenaariumi](#example-scenario) kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

### <a name="location-profile"></a>Asukohaprofiil

Lubage täiendamine üle võimsuse funktsioon asukohaprofiilis.

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohtade profiilid**.
1. Valige vasakpoolselt paanilt **PICK-06**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake kiirkaardil **Täiendamine** järgmised väärtused.

    - **Ületa asukoha võimsus:** *Jah*

        Kui see on lubatud, lubatakse täiendustööl asukoha maksimaalset võimsust ületada. See võimaldab ka muud väljad kiirkaardil **Täiendamine**.

    - **Töö kättesaadavusläve tüüp:** *Kogus*

        See väli määratleb meetodi, mida kasutatakse, kui rohkem tööd tuleb vabastada. Saate vabastada kas koguse või protsendi järgi.

        - *Protsent* – Valige see suvand, et kasutada protsentuaalset võimsust, mille aluseks on ladustamispiirangud või mahud. Selle suvandi valimine lubab välja **Ületäitumise protsent** ja keelab kaks kogusega seotud välja, **Ületäitumise kogus** ja **Ületäitumise ühik**.

            Seda valikut saate kasutada siis, kui komplekteerimisasukohad kasutavad mahtu.

            Kui see suvand on valitud, määrake väli **Ületäitumise protsent** protsendini, milleni täiendustöö tehakse kättesaadavaks.

        - *Kogus* – Valige see suvand kindla koguse väärtuse kasutamiseks. Selle suvandi valimine keelab välja **Ületäitumise protsent** ja lubab väljad **Ületäitumise kogus** ja **Ületäitumise ühik**.

            Kasutage seda suvandit, kui te ei kasuta täiendatavate asukohtade jaoks mahtu või kui teil on püsikogused, millele soovite asukohta rohkem varusid tuua.

           Kui see suvand on valitud, määrake väljad **Ületäitumise kogus** ja **Ületäitumise ühik** kogusele ja ühikule, mille juures tehakse rohkem täiendustööd kättesaadavaks.

    - **Ületäitumise kogus:** *0,65*

        See väli määratleb koguse, mille juures asukoht täitub üle.

        Töö on saadaval alati, kui asukoha laoseisu ja töö kogus jääb sellest väärtusest allapoole. Kõik sellest väärtusest suuremad täiendustööd blokeeritakse ja blokeerimine tuleb tühistada käsitsi.

        Asukoha ladustamispiirangud võetakse arvesse töökoguse arvutamisel.

    - **Ületäitumise ühik:** *PL*

        See väli määratleb ületäitumise kogused seostatud ühiku.

        Sel juhul tehakse rohkem täiendustööd kättesaadavaks, kui asukoht jõuab 0,65 kaubaaluseni (PL).

    - **Ületäitumise protsent**

        See väli määratleb protsendi, mille juures asukoht täitub üle.

        Töö on saadaval alati, kui asukoha laoseisu ja töö kogus jääb sellest protsendist allapoole. Kõik sellest väärtusest suuremad täiendustöö koguse protsendid blokeeritakse ja blokeerimine tuleb tühistada käsitsi.

        Asukoha ladustamispiirangud võetakse arvesse töökoguse protsendi arvutamisel. Kui asukoha ladustamispiiranguid pole määratletud, arvutatakse töö koguse protsent mahu järgi, kui asukohaprofiilis on määratletud mahupiirangud.

> [!IMPORTANT]
> Kui kasutate juriidilise isiku **USMF** demoandmeid ja eelnevalt lülitasite sisse funktsiooni *Asukoha identifitseerimisnumbri paigutus*, peate näidisstsenaariumi mobiilse seade etappides välja lülitama asukohaprofiili **BULK-06** sätte **Luba identifitseerimisnumbri paigutus**.

### <a name="wave-step-code"></a>Vooetapi kood

> [!NOTE]
> Siin kirjeldatud vooetapi koodi häälestamiseks on võimalik, et peate funktsiooni nimega *Organisatsiooniülene voo etapi kood* sisselülitamiseks kasutama [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

1. Avage **Laohaldus \> Häälestamine \> Vood \> Vooetapi koodid**.
1. Valige **Uus** ja seadke järgmised väärtused.

    - **Vooetapi kood:** *Täiend*
    - **Vooetapi kirjeldus:** *Täiendamine*
    - **Vooetapi tüüp:** *Täiendamine*

1. Valige käsk **Salvesta**.

### <a name="replenishment-template"></a>Täiendamise mall

Täiendamise mallid on reeglistik, mis määrab asikoha täiendamise aja ja viisi.

1. Avage jaotis **Laohaldus \> Seadistus \> Täiendamine \> Täiendamismallid**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige jaotises **Ülevaade** rida, mille välja **Täiendamismalli** väärtuseks on seatud *Nõudluse tõttu täiendamine*.
1. Määrake järgmised väärtused.

    - **Vooetapi kood:** *Täiend*
    - **Luba voo nõudmisel kasutada reserveerimata koguseid:** *Jah*

1. Valige käsk **Salvesta**.

### <a name="wave-template"></a>Voo mall

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Määrake vasakpoolse paani välja **Voomalli tüüp** suvandiks *Lähetamine*.
1. Valige loendist mall **61 Lähetamine**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Seadke kiirkaardil **Üldine** suvandi **Automaatse täiendustöö vabastamine** väärtuseks *Jah*.

    Valige selle suvandi väärtuseks *Jah* nõudlusel põhineva täiendustöö loomiseks ja selle automaatseks väljastamiseks. Selleks peab voomallile lisama täiendusvoo meetodi ja looma täiendamismalli tüübiga **Voo nõue**. Häälestage lehel **Täiendamise mall** täiendamise mall. Täiendamise malli häälestamiseks tuleb lisada voo mallile täiendamise meetod.

1. Otsige kiirkaardi **Meetodid** veerust **Valitud meetodid**, järgmine rida:

    - **Meetodi nimi:** *täiendamine*
    - **Nimi:** *Täiendamine*

1. Seadke selle rea välja **Vooetapi kood** väärtuseks *Täiend*.
1. Valige käsk **Salvesta**.

## <a name="example-scenario"></a>Näidisstsenaarium

Pärast seda, kui olete teinud kõik eelnevalt kirjeldatud näidisandmed kättesaadavaks ja need häälestanud, saate töötada selle stsenaariumi abil, et proovida funktsiooni *Täiendamine üle asukoha võimsuse*. Selles stsenaariumis kuvatavad väärtused eeldavad, et töötate standardsete demo andmetega, et valisite juriidilise isiku **USMF** ja olete ette valmistanud näidiskirjed, mida on selles teemas varem kirjeldatud. See stsenaarium toimib ka näitena selle kohta, kuidas seda funktsiooni saab tootmises kasutada.

### <a name="create-replenishment-work"></a>Täiendustöö loomine

#### <a name="create-sales-order-1"></a>Müügitellimuse 1 loomine

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige tegevuspaanil **Uus**, et avada dialoogiboks uue müügitellimuse loomiseks.
1. Määrake dialoogiboksis järgmised väärtused.

    - **Kliendi konto:** *US-007*
    - **Ladu:** *61*

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. See lisab uue, tühja rea kiirkaardil **Müügitellimuse read**. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *T0100*
    - **Kogus:** *40*

1. Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.
1. Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.
1. Sulgege leht.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Saate teabesõnumi, mis näitab loodud voo ja saadetise ID-d. Luuakse ka täiendusvoog.

    Saate ka hoiatusteate, mis ütleb: "Töö ID XXXX blokeeringut ei saa tühistada, kuna see on lõpuleviimata täiendustöö."

#### <a name="create-sales-order-2"></a>Müügitellimuse 2 loomine

1. Tehke tegevuspaani lehel **Kõik müügitellimused** valik **Uus**, et avada dialoogiboks uue müügitellimuse loomiseks.
1. Määrake dialoogiboksis järgmine väärtus.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *61*

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. See lisab uue, tühja rea kiirkaardil **Müügitellimuse read**. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *T0100*
    - **Kogus:** *60*

1. Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.
1. Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.
1. Sulgege leht.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Saate teabesõnumi, mis näitab loodud voo ja saadetise ID-d. Luuakse ka täiendusvoog.

    Saate ka hoiatusteate, mis ütleb: "Töö ID XXXX blokeeringut ei saa tühistada, kuna see on lõpuleviimata täiendustöö."

#### <a name="create-sales-order-3"></a>Müügitellimuse 3 loomine

1. Tehke tegevuspaani lehel **Kõik müügitellimused** valik **Uus**, et avada dialoogiboks uue müügitellimuse loomiseks.
1. Määrake dialoogiboksis järgmised väärtused.

    - **Kliendi konto:** *US-004*
    - **Ladu:** *61*

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. See lisab uue, tühja rea kiirkaardil **Müügitellimuse read**. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *T0100*
    - **Kogus:** *30*

1. Tehke kiirkaardil **Müügitellimuse read** valik **Varud \> Reserveerimine**.
1. Valige tegevuspaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**.
1. Sulgege leht.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Saate teabesõnumi, mis näitab loodud voo ja saadetise ID-d. Luuakse ka täiendusvoog.

    Saate ka hoiatusteate, mis ütleb: "Töö ID XXXX blokeeringut ei saa tühistada, kuna see on lõpuleviimata täiendustöö."

#### <a name="view-work-details"></a>Kuva töö üksikasjad

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Filtreerige jaotises **Ülevaade** lao *61* veerg **Ladu**.
1. Peaksite nägema, et kolme nõudluse müügitellimuse jaoks loodi seitse töö ID-d.

    - Kolmel seitsmest töö ID-st on *Täiendamise* **Töökäsu tüübi** väärtus ja neljal on *Müügitellimuse* **Töökäsu tüübi** väärtus.
    - Kõik kolm töö ID-d mille *Täiendamise* väärtusel on **Töökäsu tüüp** sama asukohaga *Komplekteerimine* ja *Ladustamine* jaotises **Read**:

        - **Komplekteerimine:** *02A01R5S1B*
        - **Ladustamine:** *06A01R2S1B*

    - Müügitellimuse 1 jaoks loodi kaks töö ID-d.

1. Märkige üles müügitellimuste töö ID-d.

Vabast kogusest olenevalt võivad loodud töökogused veidi erineda. Kuid üldiselt peaksid loodud tööpäised vastama selle stsenaariumi näitele.

#### <a name="on-hand-inventory-license-plate-id"></a>Vaba kaubavaru identifitseerimisnumbri ID

Selle stsenaariumi korral saate hiljem kasutada mobiilirakendust Warehouse Management (või emulaatorit), kus tuleb komplekteerimis- ja täiendusstsenaariumite jaoks tuvastada identifitseerimisnumber.

Identifitseerimisnumbri ID-de hilisemaks leidmiseks toimige järgmiselt.

1. Avage **Laohaldus \> Päringud ja aruanded \> Vabade kaubavarude loend**.
1. Filtripaani avamiseks valige nupp **Kuva filtrid**.
1. Stsenaariumi jaoks identifitseerimisnumbrite saamiseks sisestage järgmised filtreerimiskriteeriumid. Kasutage filtrit *alguses on*.

    - **Kauba kood:** *T0100*
    - **Ladu:** *61*

1. Valige **Rakendamine**.
1. Valige toimingupaanil **Dimensioonid**.
1. Valige kõik väärtused jaotise **Laoala dimensioonid** dialoogiboks **Dimensioonide kuvamine**.
1. Tehke jaotises **Kanded** valik **Kauba kood** ja **Kogus \<\> 0**.
1. Kui olete lõpetanud, valige dialoogiboksi sulgemiseks **OK**.
1. Tabeli **Vabad varud** kuvatakse identifitseerimisnumbrid kaubale *T0100* igas kohas. Märkige üles igale asukohale vastav identifitseerimisnumber, kuna seda teavet on hiljem vaja.
1. Sulgege leht.

### <a name="process-steps"></a>Protsessi etapid

Teete lao asukoha täiendamise esimese kahe töö ID-de jaoks. Töö kolmanda täiendamise töö jaoks blokeeritakse seni, kuni varude tase komplekteerimise asukohas langeb allapoole läve.

#### <a name="replenishment"></a>Täiendamine

1. Logige mobiilirakendusse Warehouse Management sisse lao *61* kasutajana. (Sisestage *61* kasutaja ID-na ja *1* paroolina.)
1. Avage **Varud \> Täiendamine**.

    Teil palutakse esimene täiendustöö lõpule viia. Kuvatakse kaubakood, kogus, asukoht ja komplekteerimise asukoht.

1. Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.
1. Valige nupp **OK** (märke sümbol).

    Süsteem genereerib sihtkoha identifitseerimisnumbri komplekteeritud kauba uue identifitseerimisnumbri jaoks.

1. Valige väärtuse kinnitamiseks **OK**.

    Kuvatakse ladustamistöö, mis juhendab kasutajat paigutama sihtkoha identifitseerimisnumbrit täiendamise asukohta. *Ladustamise* asukoht peab olema **06A01R2S1B**.

1. Kinnitage ladustamise üksikasjad ja valige **OK**.

    Kuvatakse teade "Töö on lõpule viidud" ja kuvatakse järgmise täiendamise komplekteerimisülesande üksikasjad: kauba kood, kogus ja asukoht, kust komplekteerida. Komplekteerimise asukoht on sama, mis esimese täiendamise asukoht. Seetõttu on identifitseerimisnumbril sama identifitseerimisnumbri ID, mida kasutati esimese täiendustöö ülesande jaoks.

1. Korrake eelnevaid samme teise tööülesande täiendustöö lõpuleviimiseks. Koguse ja sihtkoha identifitseerimisnumber erinevad esimese tööülesande kogusest ja sihtkoha identifitseerimisnumbrist.

Pärast teise täiendustöö lõpuleviimist saate teate "Töö on lõpule viidud". Mobiilne seade teavitab teile, et tööd pole saadaval ka siis, kui mõni täiendustöö on alles jäänud. Selline käitumine ilmneb seetõttu, et täiendustöö olekuks on *Hoitakse* ja on seetõttu märgitud väärtuseks **Blokeeritud**.

Olek *Hoitakse* käivitati, kuna komplekteerimise asukoha asukohaprofiili määratluse **Ületäitumise kogus** väärtuseks on *0,65 PL*. Kaks eelmist täiendustöö ülesannet täitsid asukoha peaaegu kauba *T0100* ületäitumise piirini. (Kaubaühiku teisendus kaubale on *1 PL = 100 ühikut* .) Seetõttu põhjustaks järelejäänud täiendustöö asukoha ületäitumispiirangu ületamise.

Kuni asukohast komplekteeritakse mobiilse seadme menüü-üksuses piisavalt varusid nende toomiseks allapoole vabastusläve, jääb see täiendustöö blokeerituks.

#### <a name="sales-order-pick"></a>Müügitellimuse komplekteerimine

Enne kui järelejäänud täiendamistöö ülesannet saab lõpule viia, tuleb komplekteerimise asukohast tühjendada varud tasemeni, milles ülejäänud täiendustöö blokeeringu saaks tühistada. Teisisõnu ei saa vaba kaubavaru koguse summa asukohas ja varude täiendamise kogus ületada **Ületäitumise koguse** väärtust. Kui see summa on ületäitumise kogusest väiksem, tühistatakse järelejäänud täiendustöö blokeering.

1. Logige mobiilirakendusse Warehouse Management sisse lao *61* kasutajana. (Sisestage *61* kasutaja ID-na ja *1* paroolina.)
1. Avage **Väljaminev \> Müügi komplekteerimine**.
1. Sisestage müügitellimuse 1 esimene töö ID.

    Vaadake müügitellimuse töö ID-d, mille kohta varem märkme tegite, lehelt **Töö üksikasjad**. Siia sisestatav töö ID genereerib 10 ea komplekteerimistöö kahest erinvast asukohast.

1. Valige nupp **OK**.

    Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimine esimesest asukohast.

1. Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.
1. Valige nupp **OK** (märke sümbol).

    Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimine teisest asukohast.

1. Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.
1. Valige nupp **OK** (märke sümbol).

    Lehel **Müügitellimused: ladustamine** suunab ära panema mõlemad lõpuleviidud komplekteerimistööd väljaminevasse ettevalmistusasukohta.

1. Valige nupp **OK**.

    Teile kuvatakse teade „Töö lõpule viidud”.

1. Sisestage müügitellimuse 1 teine töö ID.

    Selle töö ID jaoks on ainult üks komplekteerimisülesanne.

1. Valige nupp **OK**.

    Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimiskoht.

1. Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.

    Teie määratud identifitseerimisnumber on üks süsteemi genereeritud identifitseerimisnumbritest täiendustöö ülesandest. Veendumaks, et hõivate õige identifitseerimisnumbri ID, kontrollige varude kaupa, asukohta ja kogust lehelt **Vaba kaubavaru loend**.

1. Valige nupp **OK** (märke sümbol).
1. Kinnitage ladustamisülesande juhised väljaminevasse ettevalmistusasukohta.
1. Valige nupp **OK**.

    Teile kuvatakse teade „Töö lõpule viidud”.

Müügitellimus 2 on komplekteerimisel blokeeritud, kuna sellega seotud täiendusülesanne pole lõpule viidud. Praegu on komplekteerimise asukohas veel 30 ühikut kogust ja müügitellimuse 2 varude täiendamise kogus on 60 ühikut. Vaba kaubavaru ja täiendamise varude summa (90 ühikut) ületab ületäitumise koguse 0,65 PL (või 65 ühikut). Enne täiendustöö lõpuleviimist tuleb komplekteerida müügitellimus 3.

1. Sisestage müügitellimuse 3 töö ID.

    Selle töö ID jaoks on ainult üks komplekteerimisülesanne.

1. Valige nupp **OK**.

    Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimiskoht.

1. Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.

    Teie määratud identifitseerimisnumber on üks süsteemi genereeritud identifitseerimisnumbritest täiendustöö ülesandest. Veendumaks, et hõivate õige identifitseerimisnumbri ID, kontrollige varude kaupa, asukohta ja kogust lehelt **Vaba kaubavaru loend**.

1. Valige nupp **OK** (märke sümbol).
1. Kinnitage ladustamisülesande juhised väljaminevasse ettevalmistusasukohta.
1. Valige nupp **OK**.

    Teile kuvatakse teade „Töö lõpule viidud”.

Kohe, kui vaba kaubavaru koguse summa komplekteerimise asukohas ja täiendamise kogus on alla piirmäära, saate töödelda järelejäänud täiendustööd.

Minge tagasi lehele **Töö üksikasjad** ja märkate, et täiendustöö kättesaadavus täiendamise (müügitellimus 2) viimaseks osaks on *Avatud*, kuna asukohas on nüüd piisavalt ruumi täiendamisega nõustumiseks.

Nüüd saate seda täiendustööd mobiilse seadme kaudu töödelda.

1. Avage **Varud \> Täiendamine**.

    Teil palutakse lõpetada ülejäänud täiendustöö. Kuvatakse kaubakood, kogus, asukoht ja komplekteerimise asukoht.

1. Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.
1. Valige nupp **OK** (märke sümbol).

    Süsteem genereerib sihtkoha identifitseerimisnumbri komplekteeritud kauba uue identifitseerimisnumbri jaoks.

1. Valige väärtuse kinnitamiseks **OK**.

    Kuvatakse ladustamistöö, mis juhendab kasutajat paigutama sihtkoha identifitseerimisnumbrit täiendamise asukohta. *Ladustamise* asukoht peab olema **06A01R2S1B**.

1. Kinnitage ladustamise üksikasjad ja valige **OK**.

    Saate sõnumid "Töö on lõpule viidud" ja "Ühtegi tööd pole saadaval".

Nüüd saate komplekteerida müügitellimuse 2. Selle blokeering tühistati, kui müügitellimusega seotud täiendustöö viidi lõpule.

1. Sisestage müügitellimuse 2 töö ID.

    Selle töö ID jaoks on ainult üks komplekteerimisülesanne.

1. Valige nupp **OK**.

    Ülesandelehel **Müügitellimus: komplekteerimine** kuvatakse kauba kood, kogus ja komplekteerimiskoht.

1. Sisestage väljale **LP** kauba identifitseerimisnumber näidatud asukohas.

    Teie määratud identifitseerimisnumber on süsteemi genereeritud identifitseerimisnumber täiendustöö ülesandest. Veendumaks, et hõivate õige identifitseerimisnumbri ID, kontrollige varude kaupa, asukohta ja kogust lehelt **Vaba kaubavaru loend**.

1. Valige nupp **OK** (märke sümbol).
1. Kinnitage ladustamisülesande juhised väljaminevasse ettevalmistusasukohta.
1. Valige nupp **OK**.

    Teile kuvatakse teade „Töö lõpule viidud”.

## <a name="notes-and-tips"></a>Märkmed ja näpunäited

- See funktsioon töötab kõigi täiendustüüpidega: voo nõudlus, min/max, koormuse nõudlus ja leidmine.
- Soovi korral saate iga tööpäise täiendustöö saadavuse käsitsi alistada lehel **Töö üksikasjad**.
- Kui süsteem määrab täiendustöö kättesaadavuse, võtab see arvesse kõik varud, mis on enne töö lõpuleviimist asukohas juba olemas.
- Müügitellimustöö iga osa on seotud konkreetse täiendustööga. Vastavat müügi töö saadavuse funktsiooni pole.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]