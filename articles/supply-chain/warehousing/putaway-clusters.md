---
title: Ladustatavad kogumid
description: Kogumite ladustamine pakub võimalust komplekteerida mitu identifitseerimisnumbrit samal ajal ja seejärel neid erinevates asukohtades ladustada. Need võivad olla väga kasulikud jaemüügi ettevõtetele, kus identifitseerimisnumbrid ei ole tavaliselt täis kaubaalused.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5552959068d109bffe32b8074666bcd63b57183a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228437"
---
# <a name="putaway-clusters"></a>Ladustatavad kogumid

[!include [banner](../includes/banner.md)]

Kogumite ladustamine pakub võimalust komplekteerida mitu identifitseerimisnumbrit samal ajal ja seejärel neid erinevates asukohtades ladustada. Seda protsessi nimetatakse sageli *veoringiks*. Ladustatavad kogumid võivad olla väga kasulikud jaemüügi ettevõtetele, kus identifitseerimisnumbrid ei ole tavaliselt täielikult täis kaubaalused. 

## <a name="turn-on-the-cluster-putaway-feature"></a>Kogumite ladustamise funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Kogumi ladustamise funktsioon*

## <a name="setup-for-the-example-scenario"></a>Näite seadistamine

### <a name="cluster-profiles"></a>Kogumiprofiilid

Ladustatava kogumi profiil määrab, kuhu kaup läheb, võttes aluseks asukoha, mis on kaubale sissetuleku ajal määratud. Kui nõutavad on erinevad kogumid, tuleb iga mobiilse seadme menüü-üksuse jaoks luua erineva ladustatava kogumi profiil.

1. Avage **Laohaldus \> Seadistamine \> Mobiilne seade \> Kogumiprofiilid**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake **Päise** vaates järgmised väärtused:

    - **Ladustatava kogumi profiili ID:** *Kogumi ladustamine*
    - **Ladustatava kogumi profiili ID-nimi:** *Kogumi ladustamine*
    - **Kogumi tüüp:** *Ladustatav*
    - **Järjekorranumber:** nõustuge vaikeväärtusega.

1. Valige **Salvesta**, et muuta nõutud väljad kiirkaardil **Üldine** kättesaadavaks.
1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Kogumi määramise ajastus:** *Vastuvõtul*

        See väli määratleb, kas ladustatav kogum tuleb määrata kohe, kui kaup on vastu võetud või kas see tuleks sorteerida hiljem.

    - **Kogumi määramise reegel:** *Käsitsi*

        Väli määrab, kas kogumi peaks määrama süsteem automaatselt või peaks seda kasutaja tegema käsitsi.

    - **Korralduse kood:** jätke see väli tühjaks.
    - **Ladustatava kogumi asukoht:** *Vastuvõtt*

        Saadaval on järgmised väärtused:

        - **Vastuvõtt** –Asukoht leitakse koheselt vastuvõtul.
        - **Suletud kogum** – Asukoht leitakse kui kogum on suletud.
        - **Kasutaja suunatud** – Asukoht leitakse, kui ladustatavast kogumist valitakse identifitseerimisnumber. Sellisel juhul pole ladustamisülesande loomisel ühtegi asukohta määratud. Ladustamise enda ajal peab kasutaja määrama identifitseerimisnumbri või töö ID, et algatada ladustamise etapp. Süsteem leiab seejärel ladustamise asukoha uuesti ja ütleb kasutajale, kuhu panna komplekteeritud kogus.

    - **Kogumi ladustamine kasutaja kohta:** *Ei*

        See väli määratleb, kas kogumite automaatsel määramisel peab iga kogum olema iga kasutaja kohta unikaalne. See on saadaval ainult siis, kui **Kogumi määramise reegli** välja väärtuseks on seatud *Automaatne*.

    - **Ühiku piirang:** jätke see väli tühjaks.

        See väli määratleb ühiku, mis tuleb selle profiili kehtivuseks vastu võtta. Kui väli on jäetud tühjaks, kehtivad kõik ühikud.

    - **Tööüksuse vaheaeg:** *Individuaalne*

        See väli määratleb, kas kõik varud tuleb konsolideerida (kasutades kogumi ID-d ja identifitseerimisnumbrit) ühele identifitseerimisnumbrile, kui kogum on suletud, ja kas see tuleks ladustada ühe identifitseerimisnumbrina või eraldi vastu võetud identifitseerimisnumbritega. See väli pole saadaval, kui välja **Ladustatava kogumi asukoht** väärtuseks on seatud *Vastuvõtt*.

    - **Kogum püsib peamise identifitseerimisnumbrina:** *Ei*

        Kui see suvand on seatud väärtusele *Jah*, siis kui ladustamise toiming on lõpule viidud, muutub kogumi ID peamiseks identifitseerimisnumbriks ja kõik kogumi ID all olevad üksused seotakse selle peamise identifitseerimisnumbriga.

1. **Kogumi sortimise** kiirkaardil saate määratleda ladustamise sortimise kriteeriumid. Valige tööriistaribal **Uus**, et lisada rida ja seejärel seadke sellele järgmised väärtused:

    - **Järjekorranumber:** nõustuge vaikeväärtusega.
    - **Välja nimi:** *WMSLocationId*

        See väli määratleb välja, mida see rida peaks sortimise kriteeriumina kasutama.

    - **Sortimine:** *Tõusev järjestus*

        See väli määrab, kas sortimine peaks toimuma kasvavas või kahanevas järjestuses.

1. Valige **Kogumi töömall** kiirkaardi tööriistaribal **Uus**, et lisada rida ja seejärel seadke sellele järgmised väärtused:

    - **Töötellimuse tüüp:** *ostutellimused*
    - **Töömall:** *61 Ostutellimuse suunamine*

1. Tegevuspaanil valige **Salvesta** ja seejärel valige **Päringu redigeerimine**.
1. Valige **Kogumi ladustamise** dialoogiboksis **Vahemik** vahekaardil suvand **Add**, et lisada päringule teine rida. Seejärel värskendage päringu ridu, nagu näidatud järgmises tabelis.

    | Tabel | Tuletatud tabel | Field | Kriteerium |
    |---|---|---|---|
    | Töö | Töö | Ladu | *61* |
    | Töö | Töö | Töö ID | Jätke see väli tühjaks. |

1. Päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Valige tegevuspaanil **Salvesta** ja sulgege lehekülg.

> [!IMPORTANT]
> Kogumi profiilil olevad väljad, mis kuvatakse tuhmina, kui **Kogumi ID loomine** on seatud valikule *Jah*, ei ole saadaval ja ei arvestata funktsiooni kasutamisel.

### <a name="mobile-device-menu-items"></a>Mobiilse seadme menüü-üksused

Selle funktsiooni jaoks on saadaval kaks uut mobiilse seadme menüükäsku. **Võta vastu ja sordi kogum** menüükäsku kasutatakse saadud kauba sortimiseks ladustatavatesse kogumitesse vastuvõtul. **Ladustatav kogum** menüükäsku kasutatakse, et ladustada kogum pärast selle määramist.

#### <a name="receive-and-sort-cluster"></a>Võta vastu ja sordi kogum

Looge uus mobiilse seadme menüükäsk kauba vastuvõtmiseks ja kogumisse sortimiseks. See menüükäsk loob sissetuleva töö pärast kauba vastuvõtmist, mis näitab, et ladustatavate kogumite puhul kasutatakse vastuvõtvat menüükäsku.

> [!NOTE]
> **Võta vastu ja sordi kogum** menüükäsku saab kasutada järgmiste vastuvõtvate menüükäskudega:
>
> - Vastuvõttev ostutellimuse rida
> - Vastuvõttev ostutellimuse üksus
> - Vastuvõetav koormas olev kaup

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake **Päise** vaates järgmised väärtused:

    - **Menüükäsu nimi:** *Võta vastu ja sordi kogum*
    - **Nimi:** *Võta vastu ja sordi kogum*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Ei*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Töö loomise protsess:** *vastuvõttev ostutellimuse kaup*
    - **Loo litsentsiplaat:** *jah*
    - **Määra ladustatav kogum:** *Jah*

        > [!NOTE]
        > **Kogumi ladustamise määramise** valik on saadaval ainult ühe-etapilise *Töö loomise protsessi* tegevuse vastuvõtmiseks.

    Võtke vastu ülejäänud väljade vaikeväärtused.

1. Valige toimingupaanil nupp **Salvesta**.

#### <a name="cluster-putaway"></a>Kogumi kõrvalepanek

Looge uus mobiilse seadme menüükäsk, et panna kogum ära pärast selle määramist.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake **Päise** vaates järgmised väärtused:

    - **Menüükäsu nimi:** *Kogumi ladustamine*
    - **Pealkiri:** *Kogumi ladustamine*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Jah*

1. Määrake kiirkaardi **Üldine** väljal **Suunaja** väärtuseks *Kogumi ladustamine*. Võtke vastu ülejäänud väljade vaikeväärtused.
1. Kiirkaardil **Tööklassid** seadistage sellele mobiilse seadme menüükäsule kehtiv tööklass:

    - **Tööklassi ID:** *Ost*
    - **Töötellimuse tüüp:** *ostutellimused*

1. Valige toimingupaanil nupp **Salvesta**.

### <a name="mobile-device-menu"></a>Mobiilse seadme menüü

Lisage menüü-üksused, mille äsja lõite mobiilse rakenduse sissetulevale menüüle.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige menüü loendist suvand **Sissetulev**.
1. Otsige üles ja valige loendist **Saadaolevad menüüd ja menüü-üksused** suvand **Võta vastu ja sordi kogum**.
1. Valige parempoolne noolenupp, et nihutada valitud menüü-üksus **Menüüstruktuuri** loendisse.
1. Kasutage üles ja alla noolenuppe, et teisaldada menüü-üksus soovitud asukohta menüüs.
1. Valige toimingupaanil nupp **Salvesta**.
1. Korrake samme 4 kuni 7, et lisada ülejäänud menüü-üksused:

    - Kogumi määramine
    - Kogumi kõrvalepanek

## <a name="example-scenario"></a>Näidisstsenaarium

See stsenaarium simuleerib ladustatava kogumi töötlemist.

### <a name="create-a-purchase-order"></a>Ostutellimuse loomine

1. Avage jaotis **Ostureskontro \> Ostutellimused \> Kõik ostutellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.

    - **Hankija konto:** *1001*
    - **Ladu:** *61*

1. Valige nupp **OK**.

    Ilmub leht **Kõik ostutellimused**.

1. Klõpsake **Kõik ostutellimused** lehe kiirkaardil **Ostutellimuse read** nuppu **Lisa rida**, et lisada järgmised read:

    - Ostutellimuse rida 1:

        - **Kauba kood:** *A0001*
        - **Kogus:** *10*

    - Ostutellimuse rida 2:

        - **Kauba kood:** *A0002*
        - **Kogus:** *20*

    - Ostutellimuse rida 3:

        - **Kauba kood:** *M9215*
        - **Kogus:** *30*

1. Valige toimingupaanil nupp **Salvesta**.
1. Märkige üles ostutellimuse number.

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a>Võtke varud vastu ja pange mobiilselt seadmelt ära

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a>Võtke kaup vastu ja sortige kogumisse

1. Logige laorakendusse sisse kasutajana, kes on lao *61* jaoks seadistatud.
1. Valige peamenüüs suvand **Sissetulev**.
1. **Sissetulev** menüüs valige **Võta vastu ja sordi kogum**.
1. Sisestage väljale **Ponum** ostutellimuse number.
1. Valige **OK** (märkenupp).
1. Valige väli **Kaup**, sisestage kauba number *A0001* ja seejärel valige **OK**.
1. Valige väli **Kogus**, sisestage *10*, kasutades numbriklahvistikku ja märkige seejärel märkeruut.
1. Valige ülesande lehel **Kogus** sisestatud koguse kinnitamiseks **OK** (märkeruut).
1. **Üksuse** ülesande lehel valige **OK**, et kinnitada *A0001* üksuse sisestamine.
1. Valige **Kogumi ID** väli ja sisestage väärtus, et määrata loodavale kogumile ID.

    Siin sisestatud ID-d kasutatakse siis, kui ostutellimuse kaks järelejäänud kaupa on vastu võetud.

1. Valige nupp **OK**.

    Ilmub **Ponum** ülesande leht ja kuvatakse teade "Töö lõpetatud".

    Kaup *A0001* on nüüd *RECV* asukohta vastu võetud ja määratud kogumi ID-le, mille sisestasite sammus 10.

1. Korrake samme 4 kuni 11, et saada ostutellimusest ülejäänud kaks kaupa ja määrata need klastri ID-le:

    - Kauba *A0002* kogus *20*
    - Kauba *M9215* kogus *30*

#### <a name="close-the-cluster"></a>Kogumi sulgemine

Enne kui kogumis olevad kaubad saab ladustada, peab kogum olema suletud.

1. Minge Supply Chain Managementis **Laohaldus \> Töö \> Väljaminev \> Töökogumid**.
1. Otsige **Töökogumid** lehe **Töökogumid** jaotisest **Kogumi ID** väljalt eelnevalt sisestatud kogumi ID-d.
1. Kui kogumit ei ole kuvatud, võib see olla juba suletud. Määramaks, kas kogum suleti, märkige **Kuva suletud töö** valikruut ja otsige eelnevalt sisestatud kogumi ID-d. Seejärel järgige üht neist sammudest.

    - Kui kogum on suletud, jätke selle protseduuri ülejäänud sammud vahele ja liikuge edasi järgmisele protseduurile, [Kogumi ladustamine](#put-the-cluster-away).
    - Kui kogum ei ole suletud, järgige selle protseduuri järelejäänud etappe, et kogum käsitsi sulgeda. Seejärel minge edasi järgmise protseduuri juurde.

1. Valige **Töökogumi** jaotises eelnevalt sisestatud kogumi ID.
1. Valige toimingupaanil nupp **Sule kogum**.

    Pärast seda, kui kogum on suletud, ei kuvata seda enam **Töökogumi** jaotises (välja arvatud juhul, kui **Kuva suletud töö** märkeruut on märgitud).

#### <a name="put-the-cluster-away"></a>Ladusta kogum

1. Logige laorakendusse sisse kasutajana, kes on lao *61* jaoks seadistatud.
1. Valige peamenüüs suvand **Sissetulev**.
1. Valige **Sissetulev** menüüs **Kogumi ladustamine**.
1. Valige **Kogumi ID** ja sisestage kogumi ID, mille sisestasite varasemalt suletud kogumi jaoks.
1. Valige nupp **OK**.

    Kuvatakse leht **Kogumi ladustamine: Komplekteeri**. See näitab kogumi ID-d, komplekteerimise asukohta, kaupu (kuvatakse väärtus *Mitu*) ja kogumi lõppkogus, mis tuleb komplekteerida.

1. Valige nupp **OK**.

    Kuvatakse leht **Kogumi ladustamine: Ladusta**. **Ladusta** juhistes määratletakse kogumi ID, ladustamise asukoht, kaubad, kogus kokku ja identifitseerimisnumbrid kogumis olevate kaupade jaoks.

    Teil on kindlad valikud selle etapi alistamiseks või vahele jätmiseks.

    ![Kogumi ladustamine: Komplekteerimise leht](media/Cluster_putaway-Put.png "Kogumi ladustamine: Komplekteerimise leht")

1. Kogumi ladustamise kinnitamiseks valige **OK**.

    Kuvatakse teade „Kogum on lõpule viidud”.

## <a name="notes-and-tips"></a>Märkmed ja näpunäited

Juhtudel, kus kogumi ID muutub pesastatud kaubaaluse peamiseks identifitseerimisnumbriks, antakse ladustamisasukoht automaatselt, kui kogumi ID on skaneeritud. Täiendavat identifitseerimisnumbrit ei tohi skaneerida, isegi kui identifitseerimisnumbri loomine on seatud käsitsi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]