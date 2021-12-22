---
title: Mobiilse seadme kasutaja sätted
description: Selles teemas selgitatakse, kuidas hallata mobiilse seadme kasutajasätteid laotöötajate jaoks.
author: Mirzaab
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 13c99854224a6d220e73a43636d85ec1951f8149
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901868"
---
# <a name="mobile-device-user-settings"></a>Mobiilse seadme kasutaja sätted

[!include [banner](../../includes/banner.md)]

Uuel mobiilirakendusel Laohaldus on rakendusekohaste sätete komplekt, mis aitab kohandada kasutuskeskkonda. Kuna rakendust saab kasutada erineva ekraanisuuruse ja konfiguratsiooniga seadmetes (nt tahvelarvutis, telefonis või käsiseadmes), võib olla kasulik neid sätteid lahenduses Microsoft Dynamics 365 Supply Chain Management keskselt hallata.

Funktsioon *Mobiilse seadme kasutajasätted* võimaldab teil määrata globaalsed kasutajasätted, mida kasutatakse kõigis seadmetes. Samuti saate üksikute seadmemarkide, seadmemudelite ja/või töötajate jaoks määrata täpsemad kasutajasätted. Kui töötaja logib sisse rakendusse Laohaldus, toob ja rakendab rakendus kõige spetsiifilisema sätete profiili, mis on lahenduses Supply Chain Management salvestatud asjakohase tootemargi, seadme ja/või kasutaja ID jaoks.

See funktsioon aitab töötajatel kiiremini alustada, kui nad hakkavad kasutama uut seadet. Järgmisena on toodud mõned näited.

- Administraatorid saavad määrata eelistuste standardkomplekti, mis sobib kõige paremini konkreetse tootja seadmetega ja/või konkreetsete seadmemudelitega. Nii saavad töötajad alustada uue seadme kasutamist, ilma et nad peaksid tingimata sätteid muutma.
- Kui ettevõttel on komplekt identseid seadmeid, mida töötajad kasutavad ühiselt, kuvatakse töötajate jaoks nende eelistatud seadistus iga kord, kui nad sisse logivad, isegi kui nad pole konkreetsel päeval valitud kindlat füüsilist seadet mitte kunagi varem kasutanud.
- Lahenduses Supply Chain Management saavad administraatorid vaadata ja redigeerida kõiki salvestatud sätteid isegi üksiktöötajate jaoks. See võimalus aitab neid tõrkeotsingu või uute funktsioonide peenhäälestamise korral.

> [!IMPORTANT]
> Funktsioon *Mobiilse seadme kasutajasätted* toimib ainult uue mobiilirakenduse Laohaldus korral. See ei tööta vana laorakendusega.

## <a name="turn-on-the-mobile-device-user-settings-feature"></a>Mobiilse seadme kasutajasätete funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *uue laorakenduse kasutajasätted, ikoonid ja etapi pealkirjad*

## <a name="create-and-manage-user-settings"></a>Kasutajasätete loomine ja haldamine

Lehel **Mobiilse seadme kasutajasätted** saate luua, vaadata ja hallata iga täpsustasemega sätteprofiile. Kui töötaja redigeerib oma kasutajasätteid uues seadmes esimest korda, lisatakse sellele lehele automaatselt uus profiil, kui seda pole juba olemas. Seejärel värskendatakse seda profiili iga kord, kui töötaja midagi muudab.

Samuti saate määrata sätteprofiili, mis kehtib kõigi seadmemarkide, seadmemudelite ja/või töötajate kohta. Seejärel saate täpsuse suurendamiseks rakendada üksikute tootemarkide, mudelite ja/või töötajate jaoks täpsemad sätted.

Mobiilsete seadmete kasutajasätete loomiseks ja haldamiseks tehke järgmised toimingud.

1. Avage **Warehouse management \> Seadistus \> Mobiilne seade \> Mobiilse seadme kasutajasätted**.
1. Kindla kirje avamiseks valige loendipaanil olemasolev kasutajasätete profiil. Kuid kui soovite luua hoopis uue profiili, valige toimingupaanil **Uus**.

    Iga loendipaani profiil on sildistatud, et tähistada tootemarki, mudelit ja/või kasutaja ID-d, millele profiil rakendub. Üldisematel profiilidel on mõne või iga nimetatud omaduse jaoks määratud väärtus *Kõik*.

1. Seadke uue või valitud sätteprofiili kirje päisejaotises järgmised väljad.

    - **Seadme tootemargi nimi** – valige seadmemargi nimi, millele profiil tuleb rakendada. Kui profiil tuleb rakendada kõigile tootemarkidele, jätke see väli tühjaks. Väärtuste loend sisaldab kõiki teie süsteemis määratud tootemarke. Tootemarkide loendi määramise kohta leiate teavet järgmisest jaotisest.
    - **Seadmemudeli ID** – valige seadmemudel, millele profiil tuleb rakendada. Kui profiil tuleb rakendada valitud tootemargi kõigile mudelitele, jätke see väli tühjaks. Väärtuste loend sisaldab kõiki väljal **Seadme tootemargi nimi** valitud tootemargi jaoks määratud mudeleid. Iga tootemargi mudelite loendi määramise kohta leiate teavet järgmisest jaotisest.
    - **Kasutaja ID** – valige selle laotöötaja kasutaja ID, millele sätteprofiil tuleb rakendada. Kui profiil tuleb rakendada kõigile töötajatele, jätke see väli tühjaks.

1. Määrake kiirkaardil **Üldine** järgmised väljad.

    - **Nupupaigutus** – valige, kuidas tuleb paigutada seadmes nupud. Rakenduse elemendid teisaldatakse nii, et need sobiksid paremini töötaja eelistustega või käelisusega. Saadaolevad suvandid on *All paremal (vaikimisi)*, *All vasakul*, *Üleval paremal* ja *Üleval vasakul*.
    - **Kuva suund** – valige kuva suund, mida tuleb rakenduses vaikimisi rakendada.
    - **Skanni kaameraga** – seadke selle suvandi väärtuseks *Jah*, et kasutada seadme kaamerat selliste sisestusväljade skannimiseks, mille eelistatud sisestusrežiimiks on seatud *Skannimine*. Kui seadmel on sisseehitatud skanner, seadke selle suvandi väärtuseks *Ei*, et kasutada selle asemel skannerit.
    - **Kuva tootefoto** – valige, kas tuleb kuvada tootefotod, kui need on väljastatud toote jaoks saadaval. Tootepiltide lisamise kohta leiate lisateavet teemast [Tootele pildi lisamine](../pim/tasks/add-image-product.md).
    - **Kuva värvikujundus** – valige seadme värvikujundus.
    - **Helitase** – valige seadme helitase. Valige väärtus vahemikus 0 (null) kuni 10. Väärtus *0* tähistab heli puudumist ja väärtus *10* tähistab maksimumhelitugevust. Vaikeväärtus on *4*.
    - **Värisemistase** – valige seadme värisemistase. Valige väärtus vahemikus 0 (null) kuni 5. Väärtus *0* tähistab värina puudumist ja väärtus *5* tähistab maksimumvärinat. Vaikeväärtus on *1*.
    - **Teksti mastaabiprotsent** – määrake tekstisuurus protsendina tavasuurusest. Sisestage väärtus vahemikus 70 ja 400. Väärtus *70* tähistab kõige väiksemat tekstimastaapi ja väärtus *400* tähistab suurimat tekstimastaapi. Vaikeväärtus on *100*.
    - **Nupu mastaabiprotsent** – määrake nupusuurus protsendina tavasuurusest. Sisestage väärtus vahemikus 50 ja 200. Väärtus *50* tähistab kõige väiksemat nupumastaapi ja väärtus *200* tähistab suurimat nupumastaapi. Vaikeväärtus on *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Mobiilsete seadmete tootemarkide loomine ja haldamine

Kasutage lehte **Mobiilsete seadmete tootemargid**, et vaadata, luua ja hallata seadmete tootemarke ja mudeleid, mida saab kasutada teie sätteprofiilidega. Mobiilirakendus toob ja esitab kohaliku tootemargi nime ja mudeli ID automaatselt esimesel korral, kui töötaja muudab asjakohases seadmes sätteid. Seetõttu luuakse enamik neist kirjetest tavaliselt automaatselt. Sellegipoolest saate kõigi selle lehe kirjeid ka hallata. Näiteks saate iga tootemargi ja mudeli jaoks lisada kasulikud kirjeldused, mille abil eristada sarnaseid või raskesti mõistetavaid mudeli-ID-sid.

Mobiilsete seadmete tootemarkide ja mudelite loomiseks ja haldamiseks tehke järgmised toimingud.

1. Avage **Warehouse management \> Seadistus \> Mobiilne seade \> Mobiilse seadme brändid**.
1. Soovitud kirje avamiseks valige loendipaanil mobiilse seadme tootemark. Kuid kui soovite luua hoopis uue tootemargi, valige toimingupaanil **Uus**.
1. Seadke uue või valitud seadmemargi kirje päisejaotises järgmised väljad.

    - **Seadme tootemargi nimi** – seadme tootemargi nimi, näiteks *Microsoft Corporation*.
    - **Kirjeldus** – tootemarkide nimede eristamiseks saate sisestada kirjelduse.

1. Kiirkaardil **Mobiilsete seadmete mudelid** on kuvatud valitud seadmemargi kõik mudelid. Ruudustikus ridade lisamiseks või eemaldamiseks kasutage tööriistariba nuppe. Iga rea jaoks saate määrata järgmised väljad.

    - **Seadmemudeli ID** – seadmemudeli ID, näiteks *Surface Book 2*.
    - **Kirjeldus** – mudelite ID-de eristamiseks saate sisestada kirjelduse.

## <a name="additional-resources"></a>Lisaressursid

- [Laohalduse mobiilirakenduse installimine ja ühendamine](install-configure-warehouse-management-app.md)
- [Warehouse Management mobiilirakendusele astmeikoonide ja pealkirjade määramine](step-icons-titles.md)