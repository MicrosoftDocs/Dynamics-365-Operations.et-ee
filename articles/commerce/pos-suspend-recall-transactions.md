---
title: Peatage ja jätkake kannet müügikohas (POS)
description: Selles teemas selgitatakse, kuidas kasutajad saavad pooleliolevad kanded peatada ja neid hiljem või teises registris jätkata, kasutades rakendust Dynamics 365 Commerce.
author: jblucher
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2efc88cfa7a8cede50969484d275c6fdbb2204dd2f29b3f8c7340d02cb61a79c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737550"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a>Peatage ja jätkake kannet müügikohas (POS)

[!include [banner](includes/banner.md)]


Kassa (POS) kasutajad saavad peatada pooleliolevad kanded ja jätkata neid hiljem või teises registris. Kanded peatatakse sageli registri kiireks vabastamiseks teise ülesande jaoks praeguse kande olekut kaotamata. Näiteks alustab klienditeenindaja kliendi kande töötlemist mobiilses seadmes, kuid peab selle lõpule viima sularahasahtliga kassaaparaadis. Sel juhul saab klienditeenindaja mobiilses seadmes kande peatada ja seejärel kande tagasi kutsuda ja jätkata kassaaparaadis.

## <a name="configure-suspend-and-resume-functionality"></a>Peatamise ja jätkamise funktsiooni konfigureerimine

### <a name="pos-operations"></a>Kassatoimingud

Kaks [kassatoimingut](pos-operations.md) lasevad kassatoes peatada ja jätkata stsenaariume. Saate määrata neid toiminguid kandelehel [nupupaneel](pos-screen-layouts.md) või tervituslehel.

- 503: Peata kanne
- 504: Kutsu kanne tagasi

### <a name="receipt-template"></a>Kviitungimall

Kassat saab konfigureerida prinditud saatelehe loomiseks, kui kanne on peatatud. Seejärel saab selle saatelehe abil kande kiiresti tuvastada ja hiljem tagasi kutsuda.

Kassa saatelehe printida lubamiseks peate lisama jaotise **Peatatud kanne** kviitungi vormingu kaupluse kviitungi profiili. Kviitungi vormingu saate kujundada nii, et see hõlmab või välistab kande üksikasju. Näiteks võib vorming sisaldada vöötkoodi skannimise toetamiseks.

### <a name="receipt-numbering"></a>Kviitungi nummerdamine

Muude kassa kandetüüpide osas, mis loovad prinditud kviitungi, saate määratleda peatatud kannete numbriseeria jaotises **Kviitungi nummerdamine** kaupluse funktsiooniprofiili osas.

### <a name="void-when-closing-shift"></a>Tühista vahetuse sulgemisel

Saate kasutada suvandit **Tühistada vahetuse sulgemisel**, mis nõuab, et kasutajad kas lõpetavad või tühistavad mis tahes peatatud kanded enne nende vahetuse sulgemist. Tegevuse **Sule vahetus** ajal palub kassa kasutajatel vaadata või tühistada kõik laekumata peatatud kanded.

## <a name="suspend-and-resume-a-transaction"></a>Kande peatamine ja jätkamine

### <a name="suspend-a-transaction"></a>Kande peatamine

Kasutajad, kellel on piisavalt õigusi ja selline ekraanipaigutus, mis sisaldab toimingut **Kande peatamine**, saavad kande peatada nii, et seda saab tagasi kutsuda hiljem või teises registris.

Kandeid saab peatada ainult siis, kui nad **ei** sisalda järgmisi ridu:

- Aktiivsed makseread
- Kinkekaardi read (kas kinkekaardi väljastamine või kinkekaardi saldo lisamine)

Peatatud kanne ei mõjuta müügiteavet või kaupluse saadavalolevate varude teavet.

### <a name="resume-a-suspended-transaction"></a>Peatatud kande jätkamine

Peatatud kandeid saab tagasi kutsuda ja jätkata sama poe iga kasutaja, kellel on piisavalt õigusi ja paigutus, mis sisaldab toimingut **Kande tagasikutsumine**.

Peatatud kande kiiresti ja hõlpsasti tagasikutsumiseks skannige prinditud saatelehe vöötkood toimingust **Kande tagasikutsumine** kannete loendi vaatamise ajal.

### <a name="considerations-for-offline-mode"></a>Millega arvestada võrguühenduseta režiimi puhul

- Kandeid, mis on peatatud kassa ühendusrežiimis, ei saa jätkata ühenduseta režiimis, sest andmed ei sünkroonita võrguühenduseta andmebaasi.
- Kui kanne peatada kassa võrguühenduseta režiimis, saab selle tagasi kutsuda võrguühenduseta režiimis juhul, kui kassat ei lülitatud sisse ühendusrežiimi sel ajal, kui kanne oli peatatud. Kassa sisselülitamisel ühendusrežiimi teisaldatakse peatatud kannete andmed võrguühendusega andmebaasi ja eemaldatakse võrguühenduseta andmebaasist. Seetõttu saab kandeid jätkata ainult võrguühendusega režiimis. Kui aktiveerite kassa võrguühenduseta režiimi, ei saa te jätkata peatatud kandeid, kuna need on juba eemaldatud võrguühenduseta andmebaasist.

### <a name="void-a-suspended-transaction"></a>Peatatud kande tühistamine

Saate tühistada peatatud kande kas kande tagasikutsumisega ja seejärel toimingu **Kande tühistamine** teostamisega või valides kande loendist **Kande tagasikutsumine** ja valides suvandi **Tühistamine** rakenduste ribal. Alternatiivina saab kauplus konfigureerida kasutajad valima peatatud kannete tühistamise vahetuse sulgemisel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]