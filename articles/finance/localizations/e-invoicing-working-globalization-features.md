---
title: Globaliseerimisfunktsiooni komponendid
description: Selles teemas antakse ülevaade globaliseerimisfunktsiooni komponentidest.
author: dkalyuzh
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 87d7dd231b9ccda7761c91f129659c18039f3299
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371904"
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
