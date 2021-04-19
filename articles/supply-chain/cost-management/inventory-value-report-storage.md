---
title: Varude väärtuse talletuse aruanne
description: Selles teemas selgitatakse, kuidas käivitada varude väärtuse talletuse aruanne ja muuta väljund digitaalselt kättesaadavaks kas interaktiivse lehena rakenduses Microsoft Dynamics 365 Supply Chain Management või eksporditud dokumendina ühes paljudest vormingutest.
author: AndersGirke
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f32e175319d93ed1323129f1ea2896a435d8081c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821557"
---
# <a name="inventory-value-storage-report"></a>Varude väärtuse talletuse aruanne

Selles teemas selgitatakse, kuidas käivitada **varude väärtuse talletuse** aruanne ja muuta väljund digitaalselt kättesaadavaks kas interaktiivse lehena rakenduses Microsoft Dynamics 365 Supply Chain Management või eksporditud dokumendina ühes paljudest vormingutest.

Aruande brauseris vaatamisel reguleeritakse veerge ja koondsaldosid dünaamiliselt olenevalt teie konfigureeritud paigutusest. Saate sortida tulemusi, filtreerida neid, minna andmetesse süvitsi ja muud.

Aruande tulemused talletatakse andmeüksuses **Varude väärtus**. Seetõttu saate tulemusi filtreerida ja eksportida eri vormingutesse, näiteks komaeraldusega (CSV) fail või Microsoft Exceli vorming.

**Varude väärtuse talletuse** aruanne on kasulik, kui väljund sisaldab palju ridu. Näiteks on teil 50 000 kaupa ja ladudeks määratud 300 kauplust. Sel juhul sisaldab väljund palju ridu, kui taotlete varude lõppsaldosid kauba, asukoha ja lao kaupa.

> [!NOTE]
> Aruanne ei sisalda aruande paigutuses määratletud vahesummasid. See ei hõlma ka pearaamatu saldosid, isegi kui need on aruande paigutuses määratletud. Vastavusseviimine pearaamatuga tuleb teha proovibilansside abil.

## <a name="turn-on-the-inventory-value-storage-feature"></a>Lülitage sisse funktsioon „Varude väärtuse talletus”

Enne **Varude väärtuse talletuse** aruande loomist peate selle funktsiooni oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul** – kuluhaldus
- **Funktsiooni nimi** – varude väärtuse talletus

## <a name="generate-an-inventory-value-storage-report"></a>Varude väärtuse talletuse aruande loomine

**Varude väärtuse talletuse** aruande loomiseks ja talletamiseks tehke järgmist.

1. Avage **Kuluhaldus \> Päringud ja aruanded \> Varude väärtuse aruande talletus**.
1. Valige suvand **Uus**.
1. Seadke dialoogiboksis **Varude väärtus** järgmised väärtused, et määratleda, millised kirjed aruandesse lisatakse.

    - Sisestage kiirkaardil **Parameetrid** aruandele kordumatu nimi ja kasutage jaotise **Kuupäevaintervall** välju, et määratleda, millised kirjed aruandesse lisatakse. Kuupäevaintervalli määratlemiseks saate valida eelseadistatud vahemiku (aruande loomise kuupäeva põhjal) väljal **Kuupäevaintervalli kood** või valida kindlad kuupäevad väljadel **Alguskuupäev** ja **Lõppkuupäev**.
    - Seadistage kiirkaardil **Kaasatavad kirjed** filtrid ja piirangud, et määratleda, millised andmed aruandesse lisatakse.
    - Määrake kiirkaardil **Käivita taustal** kuidas, millal ja kui sageli aruanne luuakse.

    > [!NOTE]
    > See aruanne käivitatakse alati pakett-töö osana.

1. Valige **OK**, et rakendada oma sätted ja sulgeda dialoogiboks.

Pärast pakett-töö lõpetamist kuvatakse aruanne lehel **Varude väärtuse aruande talletus**. Aruande nägemiseks peate võib-olla lehte värskendama.

## <a name="explore-an-inventory-value-storage-report"></a>Varude väärtuse talletuse aruandega tutvumine

Pärast aruande loomist saate igal ajal seda vaadata ja sellega tutvuda järgmisel viisil.

1. Avage **Kuluhaldus \> Päringud ja aruanded \> Varude väärtuse aruande talletus**.
1. Valige loendist aruanne.
1. Valige **Kuva üksikasjad**, et kuvada aruande sisu.
1. Tutvuge aruandega mis tahes järgmist sammu järgides.

    - Nagu enamiku standardsete lehtede puhul Supply Chain Managementis saate valida peaaegu mis tahes veerupäise, et sortida või filtreerida ruudustikku selle veeru väärtuste järgi.
    - Kasutage välja **Filter**, et filtreerida aruannet mis tahes saadaoleva veeru väärtuse alusel.
    - Kasutage vaatemenüüd (välja **Filter** kohal), et salvestada ja laadida oma sortimise ning filtreerimise lemmikkombinatsioone.

## <a name="export-an-inventory-value-storage-report"></a>Varude väärtuse talletuse aruande eksportimine

Iga loodud aruanne talletatakse andmeüksuses **Varude väärtus**. Saate kasutada Supply Chain Managementi standardseid andmehaldusfunktsioone, et eksportida selle üksuse andmed mis tahes toetatud vormingusse, sh CSV või Exceli vorming.

Järgnevas näites on näha, kuidas eksportida **Varude väärtuse aruande** aruannet.

1. Minge jaotisse **Süsteemihaldus \> Tööruumid \> Andmehaldus**.
1. Valige jaotises **Import/eksport** paan **Eksport**. 
1. Kuvataval lehel **Eksport** saate seadistada eksporditöö. Sisestage esimesena töö grupi nimi.
1. Valige jaotises **Valitud üksused** käsk **Lisa üksus**.
1. Määrake järgmised väljad kuvatavas dialoogiboksis.

    - **Üksuse nimi** – valige **Varude väärtus**.
    - **Sihtandmete vorming** – valige vorming, millesse andmed eksportida.

1. Valige käsk **Lisa**, et lisada uus rida, ja seejärel klõpsake nuppu **Sulge**, et sulgeda dialoogiboks.
1. Tavaliselt ekspordite ühe aruande korraga. Ühe aruande eksportimiseks seadistage selle rea filter, mille te just dialoogiboksis **Päringud** lisasite. Sel viisil saate määratleda, milline **Varude väärtuse** üksuse aruanne kaasatakse teie eksporti. Ühe aruande eksportimiseks seadke järgmised filtri valikud järgmisi samme järgides.

    1. Vahekaardil **Vahemik** valige käsk **Lisa**, et lisada uus rida.
    2. Seadke välja **Tabel** väärtuseks **Varude väärtus**.
    3. Seadke välja **Tuletatud tabel** väärtuseks **Varude väärtus**.
    4. Määrake välja **Väli** väärtuseks väli, mille alusel soovite filtreerida. Tavaliselt kasutate te väljasid **Käivitamise nimi** ja/või **Käivitamise aeg**.
    5. Seadke väli **Kriteeriumid** väärtusele, mida soovite valitud väljal otsida. (Kui valisite eelmises etapis välja **Käivitamise nimi**, on see väärtus aruande nimi. Kui valisite välja **Käivitamise aeg**, on see aruande loomise kellaaeg.)
    6. Vajadusel lisage tabelisse **Vahemik** veel ridu, kuni olete otsitava aruande üheselt identifitseerinud.

1. Valige **OK**, et salvestada oma sätted ja sulgeda dialoogiboks.
1. Oma ekspordi seadistuse salvestamiseks valige **Salvesta**.
1. Valige vahekaardil **Eksportimise suvandid** käsk **Ekspordi kohe**, et luua eksportimise fail.
1. Avanenud lehel **Käivitamise kokkuvõtte** saate vaadata oma ekspordi töö olekut ja eksporditud üksuste loendit. Valige jaotises **Üksuse töötlemise olek** loendist üksus **Varude väärtus** ja seejärel valige suvand **Laadi fail alla**, et laadida alla sellest üksusest eksporditud andmed.

Lisateavet andmete eksportimiseks andmehalduse kasutamise kohta vt [Andmete importimis- ja eksportimistööde ülevaade](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]