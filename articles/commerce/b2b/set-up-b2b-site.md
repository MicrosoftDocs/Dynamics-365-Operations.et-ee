---
title: B2B e-kaubanduse saidi seadistamine
description: Selles teemas kirjeldatakse ettevõtetevahelise (B2B) e-kaubanduse saidi loomist lahenduses Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ac6f6511f4f96c00e10369329b2111a46f23d1a2
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035899"
---
# <a name="set-up-a-b2b-e-commerce-site"></a>B2B e-kaubanduse saidi seadistamine

[!include [banner](../../includes/banner.md)]

Ettevõtetevahelised (B2B) e-kaubanduse saidid pakuvad mõningaid võtmefunktsioone, mis optimeerivad töövoogu B2B-kasutaja jaoks. Selles teemas kirjeldatakse B2B e-kaubanduse saidi loomist lahenduses Microsoft Dynamics 365 Commerce. See käib läbi moodulite ja saidisätete, mis tuleb B2B-spetsiifiliste stsenaariumite lubamiseks konfigureerida.

## <a name="prerequisites"></a>Eeltingimused

- B2B e-kaubanduse saidi seadistamiseks peate lubama ja konfigureerima spetsiaalset funktsioonid Commerce'i peakontoris, nii nagu käesolevas teemas kirjeldatakse.
- Põhikogemused, nagu toote tuvastamine, toote üksikasjade lehed, ostukorv ja kassa, kasutavad samu mooduleid, mida kasutatakse ettevõttelt tarbijale (B2C) mõeldud e-kaubanduse saitidel. Saidi autorid peavad olema tuttavad kõigi moodulitega, mida Dynamics 365 Commerce toetab. Lisateabe saamiseks vt [Mooduliteegi ülevaade](../starter-kit-overview.md).
- Käesolevas teemas eeldatakse, et saidi autorid mõistavad Commerce'i saidilooja, mallide, fragmentide ja lehtede põhitõdesid, et nad saaksid sisse lülitada e-kaubanduse saitide B2B-funktsioone.

## <a name="site-level-settings"></a>Saiditasemel sätted

Saiditasemel sätetele pääsete saidiehitaja jaotisest **Saidi sätted \> Laiendused**. B2B-stsenaariumite puhul kehtivad järgmised kaks saiditasemel seadistust.

- **Kliendikonto maksete lubamine** - see atribuut võimaldab kasutajatel maksta tellimuste eest kliendikontosid kasutades. Saadaolevad väärtused on **Lubatud B2B-klientidele**, **Lubatud B2C-klientidele**, **Lubatud kõigile klientidele** ja **Keelatud kõigile klientidele**. Kui teie B2B-sait toetab kliendikontosid, peaksite valima **Lubatud B2C-klientidele**.
- **Tellimuse koguseliste piirangute lubamine** - see atribuut võimaldab teil seada piirangud toodete arvule, mida saab iga toote või kategooria kohta tellida. Saadaolevad väärtused on **Lubatud B2B-klientidele**, **Lubatud B2C-klientidele**, **Lubatud kõigile klientidele** ja **Keelatud kõigile klientidele**.

> [!NOTE]
> Kui täiendate mooduliteegi uusimale versioonile, peate järgima täiendavaid samme tagamaks, et eelnevalt kirjeldatud saidisätted on teie keskkonnas saadaval. Lisateavet leiate jaotisest [Faili app.settings.json värskendamine](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="create-business-partner-sign-up-pages"></a>Äripartnerite registreerumislehted loomine

Äripartneriks saamiseks peavad kasutajad esmalt esitama äripartneri taotluse. Link äripartneri taotluse lehele on saadaval B2B avalehel, nii et kasutajad saavad selle protsessi käivitada. Kui kasutajad on äripartneri taotluse esitanud, saavad nad kinnituse taotluse esitamise kohta. 

### <a name="create-a-business-partner-request-page"></a>Äripartneri taotluse lehe loomine

Äripartneri lehel olevat moodulit **Partneri registreerumine** kasutatakse äripartneriks saamise taotluste esitamiseks. See moodul võimaldab teil koguda kasutajateavet, mis on vajalik registreerumisprotsessi jaoks. Lisaks kasutatakse moodulit **Ärikonto aadress** kasutaja aadressi hõivamiseks.

Äripartneri taotluse lehe häälestamiseks ja konfigureerimiseks saidiloojas järgige neid samme.

1. Looge mall nimega **Registreerumine**. See mall peaks sisaldama järgmisi mooduleid.

    - Partneri registreerumine
    - Lingirida
    - Päis
    - Jalus
    - Sisublokk
    - Tekstiplokk
    - Toodete kogum

1. Kasutage malli **Registreerumine**, et luua leht nimega **Äripartneri taotlus**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** avalehe link ja sisestage lingi tekstiks **Avaleht**.
1. Lisage lahtrisse **Konteiner** moodul **Partneri registreerumine** mooduli **Lingirida** alla. Sisestage mooduli atribuutide paani jaotisesse **Pealkiri** tekst **Saage äripartneriks**.
1. Lisage lahtrisse **Partneri registreerumine** moodul **Ärikonto aadress**.
1. Lisage lahtrisse **Konteiner** moodul **Tekstiplokk** mooduli **Partneri registreerumine** alla. Siin saate määratleda mõned registreerumisprotsessi tingimused.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.

### <a name="create-a-business-partner-request-confirmation-page"></a>Äripartneri taotluse kinnitamise lehe loomine

Kui äripartneri taotlus on esitatud, tuleks kasutajale näidata kinnituslehte taotluse kinnitamiseks. 

Kinnituslehe häälestamiseks ja konfigureerimiseks saidiloojas järgige neid samme.

1. Kasutage varem loodud malli **Registreerumine**, et luua leht nimega **Äripartneri taotluse kinnitamine**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Lisage lahtrisse **Konteiner** moodul **Sisuplokk**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Taotlus esitatud**. Sisestage väljale **Rikastekst** tekst **Teie taotlus on esitatud**. Konfigureerige jaotises **Lingid** avalehe link ja sisestage lingi tekstiks **Tagasi ostlema**.
1. Lisage teine moodul **Konteiner** ja lisage sellele moodul **Tootekogum**.
1. Konfigureerige moodul **Tootekogum** soovitatuste või kategooriate loendiga, mida soovite lehel näidata.
1. Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.

Lingi lisamiseks saidiloojas taotluse kinnituse lehele järgige neid samme.

1. Avage varem loodud leht **Äripartneri taotlus** ja valige **Redigeeri**. 
1. Valige mooduli lahter **Äripartneri registreerumine**. Konfigureerige atribuutide paanil jaotises **Registreerumise kinnituse lehe link** link varem loodud äripartneri taotluse lehele. 
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="add-a-business-partner-request-link-to-the-home-page"></a>Äripartneri taotluse lehe lingi lisamine avalehele

Kui äripartneri taotluse registreerumise ja kinnituse leheküljed on loodud, peate tegema registreerumislehe kättesaadavaks avalehe lingi kaudu. Seda saate teha lisades lingi mistahes avalehe moodulile **Sisuplokk**.

Saidiloojas äripartneri taotluse lingi lisamiseks avalehele toimige järgmiselt.

1. Avage oma saidi avaleht ja valige **Redigeeri**.
1. Valige mooduli lahter **Sisuplokk**. Konfigureerige mooduli atribuutide paanil jaotises **Lingid** link varem loodud äripartneri taotluse lehele ja sisestage lingi tekstiks **Registreeruge äripartneriks** või selle sarnane teks. Vastavalt vajadusele lisage link.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="account-management-landing-page"></a>Kontohalduse sihtleht

Kontohalduse sihtleht sisaldab kogu kontohalduse teavet, mida on vaja nii B2B kui B2C e-kaubanduse saitide puhul. Seda lehekülge saavad vaadata ainult sisse logitud kasutajad.

Saidiloojas B2B kontohalduse lehekülje loomiseks ja konfigureerimiseks järgige neid samme.

1. Looge mall nimega **Kontohaldus**. See mall peaks sisaldama järgmisi mooduleid.

    - Päis
    - Jalus
    - Lingirida
    - Konto tervituspaan
    - Konto üldpaan
    - Kontro aadressipaan
    - Konto soovinimekirja paan
    - Konto aadressipaan
    - Konto püsikliendi paan
    - Konto kliendi saldo paan
    - Konto tellimismallide paan
    - Organisatsiooni kasutajad
    - Äriettevõtete loend
    - Kliendikonto saldo
    - Tellimuse malli read
    - Tellimuse mallide loend
    - Konto arve paan
    - Arvete loend
    - Arve üksikasjad

1. Kasutage malli **Kontohaldus**, et luua leht nimega **Minu konto**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**. 
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** avalehe link ja sisestage lingi tekstiks **Avaleht**.
1. Lisage lahtrisse **Konteiner** moodul **Tervituspaan**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Tervitus**.
1. Lisage lahtrisse **Peamine** teine moodul **Konteiner** (**Konteiner 2**). Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**. Seadke suvandi **Kuvatud tütarüksused** väärtuseks **Kaks**. 
1. Lisage lahtrisse **Konteiner 2** moodul **Konto üldpaan**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Minu profiil**. Konfigureerige jaotises **Lingid** link lehele **Minu profiil**. 
1. Lisage lahtrisse **Konteiner 2** teine moodul **Konto üldpaan**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Tellimuste ajalugu**. Konfigureerige jaotises **Lingid** link tellimuste ajaloo lehele.
1. Lisage lahtrisse **Peamine** teine moodul **Konteiner** (**Konteiner 3**). Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**. Seadke suvandi **Kuvatud tütarüksused** väärtuseks **Kaks**. 
1. Lisage lahtrisse **Konteiner 3** moodul **Konto aadressi paan**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Minu aadress**. Konfigureerige jaotises **Lingid** link lehele **Minu aadress**. 
1. Lisage lahtrisse **Konteiner 3** moodul **Konto soovinimekirja paan**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Minu soovinimekiri**. Konfigureerige jaotises **Lingid** link lehele **Minu soovinimekiri**.
1. Lisage lahtrisse **Peamine** teine moodul **Konteiner** (**Konteiner 4**). Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**. Seadke suvandi **Kuvatud tütarüksused** väärtuseks **Kaks**. 
1. Lisage lahtrisse **Konteiner 4** moodul **Organisatsiooni kasutajad**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Organisatsiooni kasutajad**. 
1. Lisage lahtrisse **Konteiner 4** moodul **Konto kliendisaldo paan**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Konto krediit**. 
1. Lisage lahtrisse **Peamine** teine moodul **Konteiner** (**Konteiner 5**). Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**. Seadke suvandi **Kuvatud tütarüksused** väärtuseks **Kaks**. 
1. Lisage moodulisse **Konteiner 5** moodul **Konto tellimuse mallide paan**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Tellimuste mallid**. 
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

> [!NOTE] 
> Mõned jaotised, mille lisasite sammudes 13 kuni 18, ei ilmu saidilooja lõuendile "saad mida näed" (WYSUWIG), sest need nõuavad sisselogitud B2B kontot.

## <a name="create-and-configure-customer-balance-pages-and-modules"></a>Kliendisaldode lehtede ja moodulite loomine ja konfigureerimine 

Tellimuste eest maksmiseks saab kasutada kliendikontosid. Kliendi kontol saadaolevat saldot saab vaadata kasutaja kontohalduse leheküljelt.

### <a name="create-a-customer-balance-page"></a>Kliendisaldo lehe loomine 

Enne, kui sisse logitud B2B kasutajad saavad vaadata oma kliendisaldot, peate looma kliendisaldo lehe. 

Saidiehitajas kliendisaldo lehe loomiseks toimige järgmiselt.

1. Kasutage varem malli **Kontohaldus**, et luua leht nimega **Kliendisaldo**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** teine moodul **Konteiner** (**Konteiner 3**). Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**. Seadke suvandi **Kuvatud tütarüksused** väärtuseks **Kaks**.
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** link kontohalduse sihtlehele ja sisestage lingi tekstiks **Minu konto**.
1. Lisage lahtrisse **Konteiner** moodul **Kliendi kontosaldo**. Sisestage mooduli atribuutide paanile jaotises **Pealkiri** tekst **Kontosaldo**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.
1. Avage varem loodud kontohalduse sihtleht (**Minu konto**).
1. Lisage mooduli **Konto kliendisaldo paan** paanile link kliendisaldo lehele. 
1. Salvestage ja avaldage leht.

Kliendisaldo leht on nüüd loodud ja kasutajad pääsevad sellele kontohalduse sihtlehelt.

### <a name="configure-a-checkout-page-so-that-the-customer-balance-can-be-used-as-a-form-of-payment"></a>Kassa lehe konfigureerimine nii, et kliendisaldot saaks kasutada makseviisina

Kliendisaldo makseviisina kasutamise lubamiseks on vajalik moodul **Kliendikonto makse**. See moodul tuleks lisada makseviisina ka kassa lehele. Lisateavet kassa lehe ja maksmiseks vajalike moodulite, sealhulgas kõigi makse üksikasjade konfigureerimiseks vajalike moodulite kohta leiate jaotisest [Kassamoodul](../add-checkout-module.md).

Pärast kassa lehe konfigureerimist peate maksejaotisse lisama mooduli **Kliendikonto makse** ja seejärel salvestama ja avaldama lehe. B2B-kasutajad saavad siis e-kaubanduse saidile sisse logida ja kassas tellimustele rakendada oma saadaolevat kliendisaldot.

Lisaks peate veenduma, et jaotises **Saidilooja \> Laiendused** oleks atribuut **Luba kliendikonto maksed** seadistatud olekule **Lubatud B2B-klientide jaoks**.

## <a name="create-order-template-pages"></a>Tellimuse mallide loomine

B2B e-kaubanduse saidi jaoks saab seadistada kaks tellimuse malli lehte: tellimuse mallide loendi leht ja tellimuse malli ridade leht.

Tellimuste mallide loendi leht kuvab kõigi saadaolevate mallide loendit. See seadistatakse mooduli **Tellimuse mallide loend** abil. Tellimuse mallide loendi lehe kaudu saate malli luua või kustutada ja lisada ostukorvi malli üksuseid.

Tellimuse malli ridade leht kuvab tellimuse malli neid üksikasju, mis on valitud tellimuse malli loendi lehel. See seadistatakse mooduli **Tellimuse mallide read** abil. Kui kasutaja valib tellimuse mallide loendi lehel malli nime, kuvatakse tellimuse malli ridade leht ja kuvatakse malli üksikasjad. Kasutaja saab seejärel vaadata ja redigeerida malli üksuseid.

### <a name="create-an-order-templates-list-page"></a>Tellimuse mallide loendi lehe loomine

Saidiehitajas tellimuse malli loendi lehe loomiseks toimige järgmiselt.

1. Kasutage varem malli **Kontohaldus**, et luua leht nimega **Telimuse mallid**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** link kontohalduse sihtlehele ja sisestage lingi tekstiks **Minu konto**.
1. Lisage lahtrisse **Konteiner** moodul **Tellimuse mallide loend**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.
1. Avage varem loodud kontohalduse sihtleht (**Minu konto**).
1. Konfigureerige mooduli **Konto tellimuse mallide paan** atribuutide paanil jaotises **Lingid** link just loodud tellimuse mallide loendi juurde.
1. Salvestage ja avaldage leht.

Tellimuse mallide loendi leht on nüüd loodud ja kasutajad pääsevad sellele kontohalduse sihtlehelt.

### <a name="create-an-order-template-lines-page"></a>Tellimuse mallide ridade lehe loomine

Saidiehitajas tellimuse malli ridade lehe loomiseks toimige järgmiselt.

1. Kasutage varem malli **Kontohaldus**, et luua leht nimega **Telimuse malli read**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** link kontohalduse sihtlehele ja sisestage lingi tekstiks **Minu konto**.
1. Lisage lahtrisse **Konteiner** moodul **Tellimuse malli read**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.

## <a name="onboard-business-partner-users"></a>Ettevõtte äripartneritest kasutajad

Organisatsiooni kasutajate leht võimaldab äripartneri organisatsiooni administraatoril lisada sellest organisatsioonist täiendavaid kasutajaid B2B e-kaubanduse saidile. See seadistatakse mooduli **Äriettevõtte loend** abil. Organisatsiooni kasutajate leheküljelt saab administraator kasutajaid lisada või eemaldada, määratleda kontosaldosid ja taotleda kasutajale väljavõtteid.

Saidiehitajas organisatsiooni kasutajate lehe loomiseks toimige järgmiselt.

1. Kasutage varem malli **Kontohaldus**, et luua leht nimega **Organisatsiooni kasutajad**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** link kontohalduse sihtlehele ja sisestage lingi tekstiks **Minu konto**.
1. Lisage lahtrisse **Konteiner** moodul **Äriettevõtete loend**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Organisatsiooni kasutajad**.
1. Lubage mooduli **Äriettevõtete loend** atribuutide paanil atribuudid **Tabeli sortimine** ja **Tabeli lehitsemine**. Seadke lehekülgede arvuks **5**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.
1. Avage varem loodud kontohalduse sihtleht (**Minu konto**).
1. Konfigureerige mooduli **Organisatsiooni kasutajate paan** atribuutide paanil joatises **Lingid** link just loodud organisatsiooni kasutajate lehe juurde. 
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

## <a name="create-invoice-pages"></a>Arve lehekülgede loomine

Arvete loendi leht kuvab kõigi saadaolevate arvete loendit. See seadistatakse mooduli **InvoicesList** abil. Kasutajad saavad arvete loendi leheküljelt arveid maksta või arveid taotleda. 

Arve üksikasjade lehel kuvatakse arvete loendilehelt valitud arve üksikasjad. See seadistatakse mooduli **Arve üksikasjad** abil. Kui kasutaja valib arvete loendi lehel arve ID, kuvatakse arve üksikasjade leht ja kuvatakse arve üksikasjad.

### <a name="create-an-invoices-list-page"></a>Arvete loendi lehe loomine

Saidiehitajas arvete loendi lehe loomiseks toimige järgmiselt.

1. Kasutage varem malli **Kontohaldus**, et luua leht nimega **Arvete loend**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** link kontohalduse sihtlehele ja sisestage lingi tekstiks **Minu konto**.
1. Lisage lahtrisse **Konteiner** moodul **InvoicesList**. Sisestage mooduli atribuutide paanile jaotisse **Pealkiri** tekst **Arved**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.
1. Avage varem loodud kontohalduse sihtleht (**Minu konto**).
1. Konfigureerige mooduli **Konto arvete paan** atribuutide paanil jaotises **Lingid** link just loodud arvete loendi juurde. 
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.

### <a name="create-an-invoice-details-page"></a>Arve üksikasjade lehe loomine

Saidiehitajas arve üksikasjade lehe loomiseks toimige järgmiselt.

1. Kasutage varem malli **Kontohaldus**, et luua leht nimega **Arve üksikasjad**.
1. Lisage lahtrisse **Päis** päise fragment, mis on saidi päisega eelkonfigureeritud.
1. Lisage lahtrisse **Jalus** jaluse fragment, mis on saidi jalusega eelkonfigureeritud.
1. Lisage lahtrisse **Peamine** moodul **Konteiner**. Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.
1. Lisage pesasse **Konteiner** moodul **Lingirida**. Konfigureerige mooduli atribuutide paanil jaosises **Lingid** link kontohalduse sihtlehele ja sisestage lingi tekstiks **Minu konto**. Seejärel konfigureerige link arvete loendilehele ja sisestage lingi tekstiks **Arvete loendid**.
1. Lisage lahtrisse **Konteiner** moodul **Arve üksikasjad**.
1. Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.
1. Avaldage lehe URL.

## <a name="additional-resources"></a>Lisaressursid

[Mooduliteegi ülevaade](../starter-kit-overview.md)

[Autorluse lehe ülevaade](../authoring-home-overview.md)

[Mallide ja paigutuste ülevaade](../templates-layouts-overview.md)

[Fragmentidega töötamine](../work-with-fragments.md)

[Uue saidilehe lisamine](../add-new-page.md)

[Maksmismoodul](../add-checkout-module.md)

[Sisuploki moodul](../add-hero-module.md)

[Tootekogum](../product-collection-module-overview.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]