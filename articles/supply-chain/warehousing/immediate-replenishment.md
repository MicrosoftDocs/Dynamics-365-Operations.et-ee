---
title: Viivitamatu täiendamine
description: Selles teemas kirjeldatakse, kuidas kasutada viivitamatut täiendamist varude täiendamiseks, kui asukohakorraldusel varude eraldamine nurjub.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSReplenishmentTemplates
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c69a9c9fd595280ba4f05a11409a3e672e4b1691
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017502"
---
# <a name="immediate-replenishment"></a>Viivitamatu täiendamine

[!include [banner](../includes/banner.md)]

Viivitamatu täiendamine võimaldab teil varusid täiendada kohe, kui asukohakorralduse real varude eraldamine nurjub. Täiendamine põhineb asukohakorralduse seadistuse ühel real. Kui varude laoseis pole rea jaoks määratud mõõtühikus, toimub selle mõõtühiku täiendamine kohe.

Viivitamatu täiendamine pakub alternatiivi meetodile, kus varude eraldamine põhineb asukohakorralduses mitmel real, ja kus nõudlus eraldamise lõpus summeeritakse ning täiendatakse mõõtühikus, mille määrab asukohakorralduse viimane rida.

Viivitamatu täiendamise eeliseks on, et täiendamist saab piirata teatud ühikutega ja koguse saab suunata kindlatesse asukohtadesse.

## <a name="business-scenario"></a>Äristsenaarium

Näiteks on teil ladu, kus on eraldi komplekteerimisalad mõõtühikutele „kast” ja „iga”. Soovite komplekteerimisprotsessi optimeerida, komplekteerides võimalikult palju kaste ja seejärel komplekteerides järelejäänud koguse, mis on väiksem kui kast, alal „iga”.

Sel juhul saate kasutada viivitamatut täiendamist. Asukohakorralduses saate seadistada viivitamatu täiendamise kastidele nii, et nõudluse tõttu täiendamist kasutatakse kohe, kui kaste, mida saab nõudluse koguse jaoks komplekteerida, tuleb puudu. Sel viisil optimeerite komplekteerimisprotsessi nii, et komplekteerimine sisaldab võimalikult palju kaste. Viivitamatu täiendamise loob kastide täiendamise ja nõudlust ei edastata. Seega komplekteeritakse kogused mõõtühikus „iga”. Teiste sõnadega, alalt „iga” komplekteeritakse ainult kogused, mis tuleb komplekteerida mõõtühikus „iga” (st, kogused on kastist väiksemad). Kui alas „kast” ilmneb puudujääk, saate kogunõudlusest komplekteerida nii palju kaste, kui võimalik. Seejärel komplekteeritakse ülejäänud kogused alalt „iga”.

## <a name="where-it-applies"></a>Kus see kehtib

Viivitamatut täiendamist kasutatakse laine käivitamise ajal, kui eraldamine nurjub asukohakorralduse rea puhul, millele on seadistatud täiendamise mall.

## <a name="set-up-immediate-replenishment"></a>Viivitamatu täiendamise seadistamine

- Tehke valikud **Laohaldus** \> **Seadistus** \> **Asukohakorraldused** , seejärel valige voo nõude jaoks vahekaardi **Read** loendis **Viivitamatu täiendamise mall** täiendamise mall.

Täiendamise mall rakendatakse, kui asukohakorralduse real ei õnnestu sihtotstarbelist mõõtühikut eraldada.

## <a name="troubleshooting"></a>Tõrkeotsing

Kui asukohakorralduse rea jaoks on viivitamatu täiendamine valitud, kuid kui nõudluse täiendamismallide kasutamisel selle asukohakorralduse rea jaoks täiendustööd ei looda, tuleb uurida kahte peamist põhjust.

- Veenduge, et rakendatav nõudluse täiendamismall on seadistatud kasutama õigeid tüübi **Täiendamine** asukoha- ja töömalle.
- Veenduge, et asukohtades, kus nõudluse täiendamismall otsib täiendamiseks vaba kaubavaru, oleks piisavalt vaba kaubavaru.
