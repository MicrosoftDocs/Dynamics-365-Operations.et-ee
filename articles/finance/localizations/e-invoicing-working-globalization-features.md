---
title: Globaliseerimisfunktsiooni komponendid
description: See artikkel annab ülevaate globaliseerimisfunktsiooni komponentidest.
author: gionoder
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 94e2d118c332a15f41f33184f5e44b0fdaccd000
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275222"
---
# <a name="globalization-feature-components"></a>Globaliseerimisfunktsiooni komponendid

[!include [banner](../includes/banner.md)]

Globaliseerimisfunktsioon on komponentide kogum, mis määrab andmete teisendamise reeglid elektroonilise aruandluse (ER) konfiguratsioonides. Need komponendid sisaldavad elektrooniliste dokumentide töötlemise juhiseid ja seejärel nende saatmist väliskanalitesse või nende vastuvõtuks. Need hõlmavad ka tingimusi, mis määratlevad, millal tuleks sissetulevate äriandmete puhul funktsiooni käitada.

Kõik komponendid sõltuvad üksteisest. Globaliseerimisfunktsioonid muudavad selle sõltuvuse loomise ja haldamise lihtsaks ning toetavad komponentide komplekti elutsükli haldust ja versioonimist.

## <a name="access-electronic-invoicing-feature-components"></a>Juurdepääs elektroonilise arveldamise funktsioonikomponentide juurde 

1. Logige oma teenuse Regulatory Configuration Service (RCS) kontole sisse.
2. Tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** valige paan **Elektrooniline arveldus** .

    Globaliseerimisfunktsioonid on mitme komponendiga. Elektroonilise **arveldamise funktsioonide lehel** on iga komponendi jaoks eraldi vahekaart.

    - **Versioon** : see komponent toetab funktsiooni elutsükli haldust. Selle funktsiooni erinevate versioonide oleku haldamiseks saate seda kasutada.
    - **Konfiguratsioonid** – see komponent võimaldab hallata, vaadata ja redigeerida seotud ER-vormingut ja vormingu vastendamise konfiguratsioone, mida kasutatakse müügivõimaluste töötlemisel.
    - **Seadistused** – see komponent võimaldab globaliseerimise teenuste, nt e-arvete teenus, kasutajatel hallata seotud funktsiooni versiooni seadistusi. Seega toetab see paindlike suhtlemise ja vastuste reeglite ülesehitamist.
    - **Keskkonnad** – see komponent võimaldab globaliseerimisteenuste kasutajatel, nt e-arveteenusel, hallata keskkonda, kus kasutatakse funktsiooni versiooni seadistust. Samuti võimaldab see anda autoriseerimise kasutajatele, kellel on juurdepääs funktsiooni versiooni seadistustele.
    - **Organisatsioonid** – see komponent võimaldab kasutajatel jagada oma funktsiooni välisorganisatsioonidega.
    - **Sildid** – see komponent võimaldab teil kasutada sildi funktsioone, mida saab kasutada viite globaliseerimise kavandis.
