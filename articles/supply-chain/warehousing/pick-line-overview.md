---
title: Mobiilse seadme menüüelemendi seadistamine komplekteerimisrea ülevaate kuvamiseks
description: Selles teemas selgitatakse, kuidas määratleda, millal kuvatakse mobiilses seadmes laotööd töötlevatele laotöötajatele kõigi tööridade loend. See võimalus võib olla kasulik laotöötajatele, kes vajavad sageli ülevaadet töökäsu komplekteerimisridadest, et nad saaksid komplekteerimisjärjekorda optimeerida.
author: MarkusFogelberg
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6eaba6da313f398c8d30f9a26c959ee971812e21
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818868"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a>Mobiilse seadme menüüelemendi seadistamine komplekteerimisrea ülevaate kuvamiseks

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas konfigureerida suvandeid, mis on seotud komplekteerimisrea ülevaatega mobiilse seadme menüüelementide jaoks, mida kasutatakse komplekteerimistöö töötlemiseks. Komplekteerimisrea ülevaade laseb laotöötajatel vaadata nende kõikide praeguse ülesandega seotud tööridade loendit ja seal valikuid teha. See võimalus aitab töötajatel oma komplekteerimisjärjekorda optimeerida. Funktsioon pakub suvandeid, mis asendavad standardse nupu **Jäta vahele**, mis võimaldab töötajatel read ükshaaval kindlas järjekorras läbi käia. (Selle nupu kasutamise suvand on siiski alles.)

Administraatorid saavad iga menüüelementi ükshaaval konfigureerida, et kontrollida, kuidas, millal ja kus mobiilirakenduses Warehouse Management komplekteerimisrea ülevaade kuvatakse.

## <a name="turn-on-the-work-pick-line-overview-feature"></a>Töö komplekteerimisrea ülevaate funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** _laohaldus_
- **Funktsiooni nimi:** _töö komplekteerimisrea ülevaade_

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a>Menüüelementide konfigureerimine kõiki tööridade loendi kuvamiseks

Mobiilse seadme menüüelemendi seadistamiseks komplekteerimisrea ülevaate kuvamiseks järgige neid samme.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige või looge menüüelement, mis on seotud komplekteerimistööga, ja määrake järgmised väärtused.

    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Jah*
    - **Juhtija:** *kasutaja juhitud* või *süsteemi juhitud*

    Lisateavet selle kohta, kuidas luua menüüelemente ja kasutada mitmesuguseid sätteid, mis on saadaval lehel **Mobiilse seadme menüüelemendid**, leiate teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).

1. Konfigureerige funktsioon kiirkaardil **Üldine**, seades välja **Kuva tööridade loend** väärtuseks üks järgmistest.

    - **Kuva ainult taotlemisel** – töötajad saavad kuvada komplekteerimisloendi, valides mobiilirakenduses Warehouse Management nupu **Hüppa selle juurde**.
    - **Kuva iga komplekteerimise alguses** – töötajatele kuvatakse loend iga kord, kui nad alustavad või viivad komplekteerimisrea lõpule. Samuti saavad nad loendit uuesti vaadata, valides mobiilirakenduses Warehouse Management nupu **Hüppa selle juurde**.
    - **Kuva ainult esimese komplekteerimise alguses** – töötajatele kuvatakse loend iga uue komplekteerimistöö alustamisel, kuid mitte iga rea järel. Samuti saavad nad loendit uuesti vaadata, valides mobiilirakenduses Warehouse Management nupu **Hüppa selle juurde**.
    - **Ära kuva kunagi** – mobiilirakenduses Warehouse Management kuvatakse standardne nupp **Jäta vahele** ning tööridade loendi kuvamine lülitatakse välja. Nupp **Jäta vahele** võimaldab töötajatel read ükshaaval kindlas järjekorras läbi käia. Nad võivad loendi läbi käia nii mitu korda kui vaja, kuni kõik read on töödeldud.

1. Valige toimingupaanil nupp **Salvesta**.

    Kui seate välja **Kuva tööridade loend** väärtuseks mõne muu väärtuse peale *Ära kuva kunagi*, muutub kättesaadavaks toimingupaanil olev nupp **Väljaloend**.

1. Valige toimingupaanil **Väljaloend**.
1. Konfigureerige lehel **Väljaloend** teave, mis kuvatakse laohalduse mobiilirakenduses Warehouse Management iga loendis oleva rea puhul.

    - Välja **Esmane juhtelement** väärtuseks on alati seatud *LineNum*. Seetõttu algab loendi iga rida reanumbriga.
    - Kasutage ülejäänud välju **Kuvaväli**, et lisada vajaduse järgi kuni seitse täiendavat kuvavälja. Valige igal väljal **Kuvaväli** töörea välja nimi. Igal real kuvatakse seejärel selle välja väärtus. Väärtused kuvatakse siin valitud järjekorras. Võite jätta mõned väljad **Kuvaväli** tühjaks, kui teil pole kõiki seitset väärtust vaja.

1. Valige toimingupaanil **Salvesta** ja sulgege siis leht **Väljaloend**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]