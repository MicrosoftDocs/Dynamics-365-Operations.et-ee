---
title: Lattu väljastamise reegel
description: Selles teemas antakse teavet funktsiooni Lattu väljastamise reegel kohta, mis annab lattu väljastamisel paindlikkuse. See lisab konfiguratsioonisuvandi, mis juhib seda, kas süsteem lubab osaliselt reserveeritud tellimuseridade väljastamist.
author: mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 77714d6bda27d8d29b10177dd87e61839295e47e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823259"
---
# <a name="release-to-warehouse-rule"></a>Lattu väljastamise reegel

[!include [banner](../includes/banner.md)]

Funktsioon *Lattu väljastamise reegel* pakub paindlikkust lattu väljastamisel. See lisab konfiguratsioonisuvandi igale laole. Selle suvandi abil saate määrata, kas selle lao jaoks saab väljastada osaliselt reserveeritud tellimuseridu. See funktsioon töötab koos täiustatud ristlaadimise funktsiooniga olukordades, kus osa tellimuserea kogusest on märgitud tarneallika jaoks, kuid järelejäänud osa saab töödelda laos. Seetõttu saab rea väljastada, et saadaoleva varude koguse töötlemine laos võib jätkuda.

## <a name="turn-on-and-initialize-the-release-to-warehouse-rule-feature"></a>Funktsiooni Lattu väljastamise reegel sisselülitamine ja lähtestamine

### <a name="turn-on-the-feature"></a>Funktsiooni sisselülitamine

Enne funktsiooni *Lattu väljastamise reegel* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Lattu väljastamise reegel*

### <a name="initialize-the-feature"></a>Funktsiooni lähtestamine

Kui funktsioon on teie süsteemis sisse lülitatud, peate selle lähtestama, et seada reegel kõigi ladude õigele esialgsele olekule.

- Ladude puhul, mis pole laohalduse jaoks lubatud, on algselt selle reegli väärtuseks seatud **Pole kohaldatav**.
- Ladude puhul, mis on laohalduse jaoks lubatud, on algselt selle reegli väärtuseks seatud **Osalise reserveerimise lubamine**

Funktsiooni lähtestamiseks ja kõigi ladude jaoks lattu väljastamise reegli määramiseks tehke järgmist.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Valige lehe **Laohalduse parameetrid** vahekaardi **Üldine** jaotises **Ettevõtte teave** link reegli **Lattu väljastamise lähtestamine** jaoks. (Kui seda linki ei kuvata, ei ole funktsioon sisse lülitatud või see on juba lähtestatud.)
1. Kui teil palutakse tegevus kinnitada, valige funktsiooni lähtestamiseks **Jah**.

## <a name="set-the-release-to-warehouse-rule-for-each-warehouse"></a><a name="set-option-warehouse"></a>Iga lao jaoks lattu väljastamise reegli seadmine

Kui funktsioon on sisse lülitatud ja lähtestatud, on kõigil teie ladudel eelmises jaotises kirjeldatud esialgsed sätted. Saate seda sätet üksikute ladude puhul muuta järgmiste etappide abil.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
1. Valige konfigureeritav ladu.
1. Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.
1. Kiirkaardi **Ladu** jaotise **Reserveeringud** väli **Varude reserveerimise nõue** juhib seda, kas tellimuste osaline vabastamine on lubatud. Valida üks järgmistest väärtustest.

    - **Pole kohaldatav** – kui funktsioon lülitatalse esmakordselt sisse ja lähtestatakse, määratakse see väärtus automaatselt kõigile ladudele, mis pole laohalduse jaoks lubatud. Seda ei saa muuta. See väärtus pole saadaval laohalduse jaoks lubatud ladude puhul.
    - **Luba osaline reserveerimine** – tellimusi saab väljastada, kui mis tahes kogus on reserveeritud. Süsteem hindab, kas reserveerimata kogus tuleks märkida täpsemaks ristlaadimiseks ja märgib selle koguse vastavalt vajadusele. Kui märgistust pole, loob süsteem töö ainult reserveeritud koguse jaoks. Kui funktsioon lülitatalse esmakordselt sisse ja lähtestatakse, määratakse see väärtus automaatselt kõigile ladudele, mis on laohalduse jaoks lubatud. See väärtus pole saadaval laohalduse jaoks keelatud ladude puhul.
    - **Nõua täielikku reserveerimist** – tellimusi saab väljastada ainult juhul, kui kogu kogus on reserveeritud. Neid ei saa väljastada, kui täielikku kogust pole füüsiliselt reserveeritud või ristlaadimiseks plaanitud. See väärtus pole saadaval laohalduse jaoks keelatud ladude puhul.

1. Valige käsk **Salvesta**.

## <a name="scenarios"></a>Stsenaariumid

Selles jaotises esitatakse kaks stsenaariumit, mille läbi töötamisel saate teada, mida see funktsioon teeb ja kuidas seda kasutada.

### <a name="make-sample-data-available"></a>Näidisandmete kättesaadavaks tegemine

Nende stsenaariumide kasutamiseks siin määratud näidiskirjete ja -väärtuste abil peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

Neid stsenaariume saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis. Kuid sellisel juhul peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.

### <a name="scenario-1-require-full-release-no-planned-cross-docking"></a><a name="scenario1"></a>1. stsenaarium: nõua täielikku väljastamist (plaanitud ristlaadimist pole)

See stsenaarium näitab, kuidas funktsioon töötab ladude puhul, kus on seatud **Nõua täielikku reserveerimist**.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
1. Määrake lao _62_ välja **Varude reserveerimise nõue** väärtuseks **Nõua täielikku reserveerimist**, nagu kirjeldati selle teema varasemas jaotises [Lattu väljastamise reegli määramine iga lao jaoks](#set-option-warehouse).
1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks _US-004_.
    - Määrake kiirkaardi **Üldine** välja **Ladu** väärtuseks _62_.

1. Valige uue müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Teie uus müügitellimus on avatud. See sisaldab tühja rida jaotise **Müügitellimuse read** ruudustikus. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *2*

1. Valige **Lisa rida**, et lisada uus rida ja seadke järgmised väärtused.

    - **Kauba kood:** *A0002*
    - **Kogus:** *2*

1. Valige esimene tellimuserida ja seejärel valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.
1. Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.
1. Ärge reserveerige teist tellimuserida.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.
1. Pange tähele, et teile kuvatakse järgmine tõrketeade: „Täielik kogus peab olema füüsiliselt reserveeritud.” Seetõttu ei loo süsteem tellimusele ühtegi tööd, saadetist ega koormust.

    > [!NOTE]
    > Sama tõrketeade kuvatakse juhul, kui reserveerite osaliselt teise rea.

### <a name="scenario-2-allow-partial-release"></a>2. stsenaarium: luba osaline väljastamine

See stsenaarium näitab, kuidas funktsioon töötab ladude puhul, kus on seatud **Luba osaline väljastamine**.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
1. Määrake lao _62_ välja **Varude reserveerimise nõue** väärtuseks **Luba osaline reserveerimist**, nagu kirjeldati selle teema varasemas jaotises [Lattu väljastamise reegli määramine iga lao jaoks](#set-option-warehouse).
1. Nagu tegite [eelmises stsenaariumis](#scenario1), avage jaotis **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused** ja looge müügitellimus kliendi konto _US-004_ jaoks laost _62_. Lisage kaks järgmist tellimuserida.

    - **Rida 1:** määrake välja **Kaubakood** väärtuseks _A0001_, välja **Kogus** väärtuseks _2_ ja välja **Ühik** väärtuseks _Pcs_.
    - **Rida 2:** määrake välja **Kaubakood** väärtuseks _A0002_, välja **Kogus** väärtuseks _2_ ja välja **Ühik** väärtuseks _Pcs_.

1. Nagu tegite [eelmises stsenaariumis](#scenario1), reserveerige täielik kogus tellimusereale 1, kuid ärge reserveerige tellimuserida 2.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.
1. Pange tähele, et seekord ei kuvata tõrketeadet. Selle asemel loob süsteem töö, saadetised ja koormused ning kuvab tulemused.
1. Saadetise, koormuse ja töö teabe vaatamiseks kasutage ruudusriku kohal oleva menüü **Ladu** suvandeid.

    - **Rida 1:** saadaval on kolm suvandit – **Saadetise üksikasjad**, **Koormuse üksikasjad** ja **Töö üksikasjad**. Valige iga suvand tellimuse lattu väljastamisel loodud saadetise, koormuse ja töö üksikasjade kuvamiseks.
    - **Rida 2:** saadaval on ainult suvand **Töö üksikasjad**. Valige see ja pange tähele, et tööd ei loodud, kuna laovarusid pole reserveeritud. Seetõttu ei loodud ühtegi saadetist ega koormust.

> [!NOTE]
> Sama tulemus eeldatakse teise rea osalisel reserveerimisel. Sel juhul luuakse töö reserveeritud rea koguse jaoks, kuid mitte reserveerimata koguse jaoks.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]