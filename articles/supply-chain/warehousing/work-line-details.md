---
title: Töörea üksikasjad
description: Selles teemas antakse teavet lehe Töörea üksikasjade lehe kohta, mis näitab teie süsteemi üksikute tööridade põhjalikku, sorditavat ja filtreeritavat loendit.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bcb340b21e06b294a40784bf3a1da71b0daf7655
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426636"
---
# <a name="work-line-details"></a>Töörea üksikasjad

[!include [banner](../includes/banner.md)]

Leht **Töörea üksikasjad** näitab teie süsteemi üksikute tööridade põhjalikku, sorditavat ja filtreeritavat loendit. See annab täieliku ülevaate laos plaanitavast ja teostatud tööst. Saate hõlpsalt vahetada kõigi tööridade ja ainult avatud tööridade vaatamise vahel. Iga rea kohta esitatud üksikasjad sisaldavad töö olekut, kaubakoodi, asukohta, töö kogust, koorma ID-d ja saadetise ID-d.

## <a name="turn-on-the-work-line-details-feature"></a>Töörea üksikasjade funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Töörea üksikasjad*

## <a name="open-and-use-the-work-line-details-page"></a>Töörea üksikasjade lehe avamine ja kasutamine

Töörea üksikasjade loendi kuvamiseks avage jaotis **Laohaldus \> Töö \> Töörea üksikasjad**. Siit saate teha järgmisi toiminguid.

- Saate kasutada välja **Filter**, et otsida ridu, mille mis tahes saadaoleval parameetril on kindel väärtus. (Saadaolevate parameetrite hulka kuuluvad paljud parameetrid, mida ei kuvata ruudustiku veergudena.)
- Suletud ridade kuvamiseks või peitmiseks kasutake märkeruutu **Kuva suletud**.
- Valige **Kuva dimensioonid**, et avada dialoogiboks **Dimensioonide kuvamine**, kus saate valida, kas kuvada või peita ruudustiku erinevaid dimensiooni veergusid.
- Valige mis tahes veeru päis menüü avamiseks, kus saate valida, kas sortida või filtreerida loendit selle veeru väärtuste alusel.
- Valige töörida ja seejärel valige **Asukoha muutmine**, et avada dialoogiboks, kus saate muuta selle töörea asukohta. Teie määratud asukoht alistab selle asukohakorralduse häälestuse.
- Valige töörida ja seejärel valige **Töörea tühistamine**, et avada dialoogiaken, kus saate vähendada selle töörea kogust osaliselt või täielikult.
- Korrigeerige koguseid.
- Vaadake mis tahes töörea taga olevaid kandeid.

## <a name="try-out-the-feature"></a>Funktsiooni katsetamine

Sellest jaotisest leiate kolmeosalise demo, mis näitab, kuidas töötada töörea üksikasjadega.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Selle demo kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Seda demo saate kasutada ka juhistena, kui töötate tootmissüsteemis. Kuid peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Veendumine, et stsenaariumi häälestus sisaldaks piisavalt vabu varusid

Kui töötate demoandmetega **USMF**, peaksite esmalt veenduma, et teie süsteem oleks seadistatud nii, et igas vastavas komplekteerimise asukohas oleks saadaval piisavalt varusid. Selle demo puhul on eelduseks, et saadaval oleks järgmised varud.

- **Kaup M9200:** 45 ea. (või rohkem)
- **Kaup M9202:** 10 ea. (või rohkem)

Järgige neid etappe, et kontrollida, kas piisavalt varusid on saadaval ja teha vajalikke korrigeerimisi.

1. Avage jaotis **Laohaldus \> Häälestus \> Asukohakorraldus** ja määratlege, milliseid komplekteerimise asukohti kasutatakse müügitellimuste komplekteerimiseks laos 51. (Lisateavet vaadake teemast [Laotöö juhtimine, kasutades töömalle ja asukohakorraldusi](control-warehouse-location-directives.md).)
1. Kontrollige varude tasemeid vastavates asukohtades.
1. Korrigeerige varu vastavalt vajadusele. Varude korrigeerimiseks saate luua käsitsi liikumisi, kasutada täiendamist või rakendada mis tahes muud voogu.

### <a name="part-1-create-picking-work"></a>1. osa: komplekteerimistöö loomine

Enne töö loomise alustamist veenduge, et teie ladu on seadistatud nii, et see vastaks töötaotlustele oodatud viisil.

Komplekteerimistöö loomiseks järgige neid etappe.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige **Uus**, et avada dialoogiboks **Müügitellimuse loomine**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks _US-001_.
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks _51_.

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Teie uus müügitellimus on avatud. See lisab uue tühja rea ruudustikku **Müügitellimuse read**. Määrake sellel tellimuse real järgmised väärtused.

    - **Kauba kood:** _M9200_
    - **Kogus:** _20_
    - **Ühik:** _ea_

1. Valige uus tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine** lehe **Reserveerimine** avamiseks.
1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**. Süsteem loob saadetise, lisab selle uuele koormusele ja loob vajaliku töö.
1. Looge teine müügitellimus sama kliendi konto ja lao jaoks, mida kasutasite esimese tellimuse jaoks. Lisage sellele tellimusele kaks järgmist tellimuse rida.

    - **Rida 1:** määrake välja **Kaubakood** väärtuseks _M9200_, välja **Kogus** väärtuseks _25_ ja välja **Ühik** väärtuseks _ea_.
    - **Rida 2:** määrake välja **Kaubakood** väärtuseks _M9202_, välja **Kogus** väärtuseks _10_ ja välja **Ühik** väärtuseks _ea_.

1. Korrake etappe 6–8, et reserveerida varud iga tellimuserea jaoks (ükshaaval) ja seejärel korrake etappi 9 tellimuse vabastamiseks lattu.

### <a name="part-2-change-the-location-for-a-work-line"></a>2. osa: töörea asukoha muutmine

1. Avage jaotis **Laohaldus \> Töö \> Töörea üksikasjad**.
1. Otsige üles ja valige üks selle demo jaoks loodud tööridadest.
1. Valige **Asukoha muutmine** dialoogiboksi **Vali uus asukoht** avamiseks.
1. Valige dialoogiboksi **Vali uus asukoht** väljal **Asukoht** töörea jaoks uus asukoht.
1. Valige **OK**, et rakendada oma muudatus ja sulgeda dialoogiboks.

> [!IMPORTANT]
> Asukohamuudatusi saate esitada ainult juhul, kui uues asukohas on saadaval piisavalt vaba varu (komplekteerimiseks) või kui see läbib asukoha tüübi kinnitamise (ladustamiseks).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>3. osa: töörea koguse muutmine või töörea tühistamine

1. Avage jaotis **Laohaldus \> Töö \> Töörea üksikasjad**.
1. Otsige üles ja valige üks selle demo jaoks loodud tööridadest. Võtke arvesse, et saate tühistada või muuta koguseid ainult nendel tööridadel, kus töö tüüp on _komplekteerimine_.
1. Valige **Töörea tühistamine** dialoogiboksi **Tühistatav kogus** avamiseks.
1. Muutke dialoogiboksis **Tühistatav kogus** välja **Kogus** väärtust, et määrata kogus, mis tuleks *lahutada* kogusest, mis on praegu sellele reale määratud. Vaikimisi kuvatakse väljal **Kogus** täielikku kogust.

    - Kui tühistate täieliku koguse, muudetakse väärtus **Töö olek** olekusse _Tühistatud_, kuid väljal **Töö kogus** kuvatakse jätkuvalt algset väärtust.
    - Kui tühistate ainult osa kogusest, värskendatakse välja **Töö kogus**, et see kuvaks uut väärtust, kuid väärtus **Töö olek** ei muutu.

1. Valige **OK**, et rakendada oma muudatus ja sulgeda dialoogiboks.

> [!IMPORTANT]
> Kui tühistate ainult osa töörea kogusest, peate eemaldama aegunud koguse ka koormuse realt. Vastasel juhul, kui alatarne on õigesti seadistatud, ei saa koormuse rida kinnitada saatmiseks.
