---
title: Mobiilse seadme kasutaja kontod
description: See teema kirjeldab, kuidas seadistada ja hallata kasutajakontosid, mis võimaldavad töötajatel lao rakendusse sisse logida ja neid kasutada.
author: Mirzaab
ms.date: 09/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-09-15
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c4cb36160e692cc12140b57037d2c9739f7b2ebd
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462666"
---
# <a name="mobile-device-user-accounts"></a>Mobiilse seadme kasutaja kontod

[!include [banner](../includes/banner.md)]

Iga kord, kui töötaja alustab laorakenduse kasutamist, peab ta sisse logima kasutajanime ja parooliga. Kõiki lao rakenduse kasutajaid saab süsteemi iga töötajaga seostada ja laod on tavaliselt seotud iga lao rakenduse kasutajaga. Samuti konfigureeritakse igale töötajale erinevaid valikuid, et luua vaikesätted ja muud laorakenduse kasutamisele asjakohased sätted.

## <a name="set-up-the-required-worker-and-employee-records"></a>Nõutavate töötaja ja tööandja kirjete seadistamine

Enne kui saate lao rakenduse kasutajad seadistada, peab iga töötaja Supply Chain Management töötaja või tööandjana **Inimressursside** moodulis olemas olema.

## <a name="set-up-mobile-device-user-accounts"></a><a name="set-wma-users"></a>Mobiilse seadme kasutaja kontode seadistamine

Pärast vajalike töötajate ja töötajate seadistamist Inimressurssides saate määrata lao rakenduse kasutajad igaühele neist ja seadistada teisi valikuid, mis mõjutavad rakenduse kasutamist.

1. Avage jaotis **Laohaldus \> Seadistus \> Töötaja**.
1. Olemasoleva töötaja redigeerimiseks valige see loendipaanilt. Uue kirje lisamiseks tehke toimingupaanil valik **Uus**.
1. Kui häälestate uut töötajat, järgige neid samme:

    1. Valige väljal **Töötaja** töötajate loendist sihtkasutaja.
    1. Valige käsk **Vali**.
    1. Valige toimingupaanil nupp **Salvesta**.

1. Vaikeprofiili saab kasutada pakkimisjaama laotöötaja juhtimiseks läbi seal vajaliku protsessi. Teise võimalusena saab vaikeprofiili kasutada töötaja eelistatud reeglite sätete salvestamiseks. Määrake FastTab **Profiilil** järgmised väljad:

    - **Konteineri pakkimise poliitika** – valige konteineri pakkimispoliitika, mis määratleb, kuidas pakkejaama konteinereid tuleb töödelda. Siin valitud konteineri pakkimispoliitika eel valitakse töötajale, kui ta avab pakkimisjaama. Lisateavet vt järgmisest blogipostitusest: [Parandatud pakkimisfunktsionaalsus](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/12/01/improved-packing-functionality-dynamics-365-for-operations-1611).
    - **Pakkimisprofiili ID** – valige pakkimisprofiili ID, mis määratleb kasutatava pakkimispoliitika ja konteineri sätted. Kui valitud pakkimisprofiili ID on seostatud konteineri pakkimispoliitikaga, ei saa te sellel lehel **konteineri** pakkimispoliitika sätet muuta.

1. **Vaikimisi pakkejaama** kiirkaardil FastTab määrake järgmised väljad, et määrata vaike-pakkimisjaam, mis rakendub, kui töötaja sisse logib. Vajaduse korral saab töötaja siiski valida teise pakkimisjaama.

    - **Sait** - valige sait, kus vaikepakendamisjaam asub.
    - **Ladu** - valige ladu, kus vaikepakendamisjaam asub.
    - **Asukoht** - valige pakkejaama vaikeasukoht.

1. **Kasutajate** FastTab võimaldab teil valitud töötajale luua mis tahes arvu laorakenduse kasutajakontosid. Iga konto on seotud kindla lao või ladudega. Kasutage tööriistariba, et lisada või eemaldada kasutajakontosid, lähtestada valitud konto parool või määrata laod valitud kontole. Iga kasutaja konto jaoks saate määrata järgmised väljad:

    - **Kasutaja ID** - sisestage kordumatu ID.
    - **Kasutajanimi** - sisestage nimi ID jaoks.
    - **Vaikeladu** – määrake vaikeladu, kus töötaja tavaliselt töötab. Võite kasutada tööriistariba täiendavate ladude määramiseks ja töötaja saab ladusid vahetada, kasutades mobiilse seadme menüü üksuse kaudset tegevust **Muuda lao** kaudset tegevust.
    - **Menüü nimi** - valige juurmenüü, mis on töötaja algusleheks. Võimalus seadistada juurmenüüd igale töötajale on kasulik, kuna see võimaldab teil kontrollida menüüstruktuuri, mida iga töötaja saab kasutada. Näiteks saab menüü töötajate jaoks, kes on aktiivsed ainult väljaminevas alas, kohandada selle ala väljaminevate toimingutega seotud toimingute jaoks.
    - **Passiivne** – valitud märkeruut näitab, et kasutajakonto on passiivne. Kasutajakonto inaktiveeritakse automaatselt, kui töötaja sisestab lao rakenduses reale vale parooli viis korda. Siiski, selle valiku saate märkida ka käsitsi. Kasutaja uuesti aktiivseks avamiseks tühjendage see ruut.

1. Määrake FastTab **Tööl** järgmised väljad:

    - **Luba komplekteerimise asukoha** - määrake see suvand väärtusele *Jah*, et lubada töötajal komplekteerimisetappide asukoht ümber lükata. See võimalus on kasulik juhul, kui füüsiline ladu ei vasta süsteemi pakutavale asukohale.
    - **Luba asukoha ümberkirjutamine** - määrake see suvand väärtusele *Jah*, et lubada töötajal asukoht ümber lükata. See võimalus võib olla kasulik, kui soovitatav maha panemise asukoht on praegu täis või pole saadaval või kui vahetatakse vahetatud asukohti.
    - **Luba müük üle komplekteerimise** – määrake see suvand väärtusele *Jah*, et lubada töötajal müügitellimuste komplekteerimise puhul üle komplekteerimine. Rohkem infot [Müügi- ja üleviimistellimuste ülekomplekteerimine](over-picking-for-sales-and-transfer-orders.md).
    - **Luba müük üle komplekteerimise** – määrake see suvand väärtusele *Jah*, et lubada töötajal müügitellimuste komplekteerimise puhul üle komplekteerimine. Rohkem infot [Müügi- ja üleviimistellimuste ülekomplekteerimine](over-picking-for-sales-and-transfer-orders.md).
    - **Luba lao teisaldamine seostatud tööga** – tehke see valik väärtusele *jah*, et lubada töötajal teisaldada juba reserveeritud või tööga seotud varusid. Rohkem infot vaata [Varude liikumine koos sellega seotud töödega rakenduses Warehouse management](move-inventory-associated-work.md).
    - **Luba kaupade käsitsi ümberasutamist** – määrake see valik valikule *Jah* et lubada töötajal käsitsi ümberasumine lühikese komplekteerimise ajal. Kauba ümberasumine juhendab töötajaid varusid teisest asukohast peale võtma. Kuigi automaatne ümberasumine on saadaval kõigi töötajate jaoks, vajab käsitsi ümberasumine töötaja jaoks selgesõnalist häälestust. Võimalus kontrollida iga töötaja käsitsi ümberpaigutamist võib olla kasulik, kuna see võimaldab kontrollida iga töötaja nähtavust, nt kui kauba komplekteerimine vahelaost või hulgialalt on piiratud usaldusväärsete töötajatega. Lisateavet vt järgmisest blogipostitusest: [automaatne ja käsitsi kauba ümberasumine lühikese komplekteerimise ajal](https://cloudblogs.microsoft.com/dynamics365/no-audience/2016/11/07/automatic-and-manual-item-reallocation-during-the-short-picking-dynamics-365-for-operations-1611/).
    - **On tsüklilise inventuuri ülevaataja** – määrake selle suvandi väärtuseks *Jah*, et muuta töötaja tsüklilise inventuuri ülevaatajaks. Sel juhul kinnitatakse kohe kõik tsükli inventuurid, mida töötaja lao rakenduses teeb. **Maksimum protsendi piirangu**, **Maksimumkoguse piirangu** ja **maksimumväärtuse piirangu** väljad ei ole mõeldud töötajatele, kelle valik on seatud väärtusele *Jah*.
    - **Maksimaalse protsendi piirang** - Sisestage suurim protsent, mille võrra tsükliline inventuur võib erineda oodatavast kogusest, ilma et tsüklilise inventuuri ülevaataja peaks selle kinnitama.
    - **Maksimaalse koguse piirang** - sisestage kogu kogus, mille sisestatud kogus võib oodatud kogusest erineda (ühikutes), ilma et tsükliliseinventuuri ülevaataja nõuaks kinnitamist.
    - **Maksimaalne väärtuse piirang** - Sisestage maksimumsumma, mille võrra varude maksumus võib erineda oodatavast maksumusest, ilma et tsüklilise inventuuri ülevaataja peaks selle kinnitama.

1. Valige toimingupaanil nupp **Salvesta**.
1. Kui te lisate uue kasutaja konto, kuvatakse dialoogiboks **Parooli määramine**, kus saate luua lihtsa parooli, mida kasutaja saab mobiilirakendusse sisselogimiseks kasutada. Sisestage kaks korda lihtparool ja jätkamiseks valige käsk **Salvesta parool**.

## <a name="set-the-language-number-formats-and-time-zone-for-each-warehouse-app-user"></a>Määrake keel, numbrivormingud ja ajavöönd igale laorakenduse kasutajale

Kui töötaja logib Warehouse Management mobile rakenduse sisse, muutub keel, numbrivormingud ja ajavöönd vastavalt töötaja eelistustele. Valitud töötaja konto jaoks sammus 3 valitud sätted [Mobiilseadme kasutajakontode seadistamine](#set-wma-users) jaotises määratlevad kasutatavad sätted. Kui vajate iga kasutaja jaoks eraldi sätteid, kasutage erinevaid töötaja kontosid. Järgmine protseduur näitab, kuidas muuta iga laorakenduse kasutaja keelt, numbrivorminguid ja ajavööndit.

1. Avage jaotis **Laohaldus \> Seadistus \> Töötaja**.
1. Leidke töötaja nimi, kelle soovite häälestada. Veenduge, et töötajal on kõik nõutavad laorakenduse kasutajakontod, mida loetleb FastTab **Kasutajad**. Looge uus töötaja ja/või lisage laorakenduse kasutajakontod vastavalt vajadusele, järgides järgmisi samme [seadme kasutajakontode häälestamise](#set-wma-users) jaotises.
1. Minge jaotisse **Süsteemihaldus \> Kasutajad \> Kasutajad**.
1. Valige kasutajakonto, kus **Isik** veerus kuvatakse sammus 2 leitud töötaja nimi.

    > [!IMPORTANT]
    > **Kasutaja ID** väärtused, mis on loetletud **Kasutajad** lehel *pole* seotud väärtusega, mida näidatakse sammus 1 **Kasutaja** **Töötaja** FastTab lehel.

1. Tegevuspaanil valige **Kasutaja suvandid**.
1. Vahekaardil **Eelistuses** määrake järgmised väljad:

    - **Keel** - valige keel, mida töötaja eelistab. See väli juhib ka lao rakenduses kuvatavat numbrivormingut.
    - **Kuupäev, kellaaeg ja numbrivorming** – valige kuupäeva ja kellaaja vorming, mida töötaja eelistab. Lao rakendus kasutab selle sätte asemel väljal Keel valitud keelega **seostuvat** numbrivormingut.
    - **Ajavöönd** – valige ajavöönd, kus töötaja töötab. See väli mõjutab ajatemplit kõigile registreerimistele, mida töötaja rakenduse abil teeb.

> [!NOTE]
> Mõnel juhul ei suuda laorakendus leida kindlaid töötajasätteid, mis loovad keele, numbrivormingud ja ajavööndi. Kehtivad järgnevad reeglid.
>
> - Kui rakendus ei ole ühendatud Supply Chain Management keskkonnaga (nt rakenduse esmakordsel käivitamisel pärast installimist), kasutatakse kohaliku seadme keelt. Kui seadme keel muutub, muutub ka rakenduse keel. Lisateavet keele konfigureerimise kohta kohaliku seadme jaoks vt oma seadme ja/või operatsioonisüsteemi dokumentatsioonist.
> - Kui rakendus on ühendatud Supply Chain Management keskkonnaga, kuid sisse logitud töötajale pole eelistusi määratud, valitakse keel, numbrivormingud ja ajavöönd konto, mis on seotud kliendi ID-ga, mida seade kasutab Supply Chain Management ühenduse loomiseks. Rohkem infot leiate [Rakenduses Supply Chain Management kasutajakonto loomine ja konfigureerimine](install-configure-warehouse-management-app.md#user-azure-ad).

> [!TIP]
> Kui panete tähele, et lao rakenduse abil tehtud registreerimistele kuvatakse valed ajatemplid, peate võib-olla kohandama ajavööndit, mis on seadistatud kasutajakontole, mida töötajad kasutavad Supply Chain Management rakenduses sissse logimiseks ja/või autentimiseks. Nagu eelnevalt mainitud, võib ajavööndi säte tulla kasutajakontolt, mida kasutatakse lao rakendusse sisselogimiseks, nagu on seadistatud lehel **Töötaja**. Alternatiivselt, kui kasutajakonto pole **töötaja** lehel seatud, võetakse ajavöönd kasutajakontost, mis on seostatud autentimiseks kasutatava kliendi ID-ga, nagu on **[Azure Active Directory rakenduste](install-configure-warehouse-management-app.md)** lehel.
