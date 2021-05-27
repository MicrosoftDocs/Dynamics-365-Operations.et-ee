---
title: Pearaamatu kalendri muutmine ja ümbermääramine
description: Selles teemas selgitatakse, kuidas muuta pearaamatule praegu määratud kalendrit ja pearaamatule uue kalendri määramist.
author: kweekley
ms.date: 05/07/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-07
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 052b8944c0a015187d1d7c4ba3db878c52faeeea
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039946"
---
# <a name="change-or-reassign-a-ledger-calendar"></a>Pearaamatu kalendri muutmine ja ümbermääramine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas muuta pearaamatule praegu määratud kalendrit ja pearaamatule uue kalendri määramist.

## <a name="issue"></a>Probleem

Mõnikord peavad ettevõtted kas muutma olemasolevat kalendrit, mis on pearaamatule määratud, või määrama uue kalendri.

## <a name="resolution"></a>Lahendus

Pearaamatu kalendri muutmiseks või uuestimääramiseks on kaks stsenaariumit. Esimene stsenaarium hõlmab olemasoleva kalendri muutmist, mis on juba pearaamatule määratud. Teine stsenaarium hõlmab uue kalendri loomist ja selle määramist pearaamatule. Mõlemaid muudatusi saab teha igal ajal pärast kannete sisestamist pearaamatusse.

### <a name="change-an-existing-fiscal-calendar"></a>Olemasoleva rahanduskalendri muutmine

Olemasoleva kalendri muutmiseks, mis on määratud teie pearaamatule, avage **Pearaamat \> Pearaamatu seadistus \> Pearaamat** ja valige rahanduskalendri link, et avada leht **Pearaamatu kalendrid**.

Kalendris tehtavatel muudatustel on piirangud. Näiteks saate muuta aasta *perioodide* algus- ja lõppkuupäevi, kuid te ei saa kalendris muuta *aasta* algus- ja lõppkuupäevi.

Aasta perioode muutmiseks valige asjakohane kalender ja aasta. Esmalt kustutage nupu **Kustuta periood** abil mõned või kõik olemasolevad tegevusperioodid. Kustutada saab kõik tegevusperioodid, välja arvatud esimese. Seejärel jagage nupu **Jaga periood** abil järelejäänud periood või perioodid uuteks perioodideks, sisestades järgmise perioodi jaoks asjakohase alguskuupäeva.

Pärast kalendri perioodide muutmist peate käitama protsessi **Pearaamatu perioodide ümberarvutamine** igas juriidilises isikus (ettevõttes), millele see kalender on määratud. Kuigi ükski hoiatusteade ei tuleta teile selle etapi lõpuleviimist meelde, on ümberarvutusprotsess nõutav igale pearaamatusse sisestatud kandele määratud perioodi uuendamiseks. Ümberarvutusprotsessi käitamiseks valige iga ettevõtte lehel **Pearaamatu seadistus** protsess **Pearaamatu perioodide ümberarvutamine**.

Kui ümberarvutusprotsessi ei käitata, võidakse proovibilansi või finantsaruande kandesaldod kaasata perioodidesse valesti. Sel juhul saate ümberarvutusprotsessi käitamise abil saldosid igal ajal korrigeerida.

### <a name="assign-a-new-fiscal-calendar"></a>Uue rahanduskalendri määramine

Uue rahanduskalendri määramiseks avage **Pearaamat \> Pearaamatu seadistus \> Pearaamat** ja valige käsk **Redigeeri**, et seada leht **Pearaamat** redigeerimisrežiimi. Seejärel valige väljal **Rahanduskalender** uus rahanduskalender.

Pärast pearaamatu rahanduskalendri muutmist peate käitama protsessi **Pearaamatu perioodide ümberarvutamine**. Kui määrate pearaamatule uue rahanduskalendri, tuletatakse teile teatega selle etapi lõpuleviimist meelde. Kuigi see teade võib jätta mulje, et ümberarvutamisprotsess on valikuline, pole see nii. See on nõutav igale pearaamatusse sisestatud kandele määratud perioodi uuendamiseks. Ümberarvutusprotsessi käitamiseks valige lehel **Pearaamatu seadistus** protsess **Pearaamatu perioodide ümberarvutamine**.

Kui ümberarvutusprotsessi ei käitata, võidakse proovibilansi või finantsaruande kandesaldod kaasata perioodidesse valesti. Sel juhul saate ümberarvutusprotsessi käitamise abil saldosid igal ajal korrigeerida.
