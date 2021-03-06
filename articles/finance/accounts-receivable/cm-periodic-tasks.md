---
title: Perioodilised krediidihalduse ülesanded
description: See teema kirjeldab perioodilisi toiminguid, mis on vajalikud klientide krediidilimiitide haldamise protsessis.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e5d1ad7b0b151d67bd96513e9ce0c82c172a601
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835288"
---
# <a name="periodic-credit-management-tasks"></a>Perioodilised kreedidihalduse ülesanded

[!include [banner](../includes/banner.md)]

See teema kirjeldab perioodilisi toiminguid, mis on vajalikud klientide krediidilimiitide haldamise protsessis.

## <a name="update-risk-scores"></a>Värskenda riskiskoore

Kui ärid arenevad ja asjaolud muutuvad, võivad ka antud kliendi krediidiriskid muutuda. Oma klientide jaoks sobivate krediidilimiitide säilitamiseks peate perioodiliselt läbi vaatama iga riskiskoori kriteeriumid ja värskendama iga kliendi punktisummad. Järgmisi punktisummasid saate värskendada lehel **Riskiskooride värskendamine** (**Krediidihaldus ja võlanõuded \> Perioodilised ülesanded \> Krediidihaldus \> Riskiskooride värskendamine**). Töödeldakse ka kõiki kasutaja määratletud arvutusi.

- **Maksmise keskmine päevade arv** – see skoor on keskmine päevade arv, mis kliendil arvete maksmiseks kulub.
- **Klient alates** – see skoor on aastate arv, mil klient on teie organisatsiooni klient.
- **Äritegevuses alates** – see skoor on aastate arv, mil klient on äritegevuses olnud. See kasutab väärtust väljal **Ettevõtluse algus** lehel **Kliendid**.
- **Laekumata müügi päevad** – see skoor põhineb müügireskontro saldol, müügitulul ja eelmise 12-kuulise perioodi päevade arvul.
- **Keskmine saldo** – see punktisumma põhineb eelmise 12-kuulise perioodi müügireskontro saldol.
- **Krediidihalduse grupp**, **Konto olek** ja **Riik** – need punktisummad kasutavad kliendi teavet.

## <a name="update-customer-balance-statistics"></a>Kliendi saldo statistika värskendamine

Saate käivitada protsessi **Kliendi saldo statistika värskendamine**, et värskendada saldo statistika arvutust, mis kuvatakse lehel **Saldo statistika päring**. Seda teavet kasutatakse riskiskooride ja krediidistatistika kiirinfo väärtuste kuvamiseks lehel **Klient**.

Protsessi käivitamisel uuendatakse kliendi saldo statistikat ühe kliendi kohta. Pakett-töö seadistamiseks mitme kliendi protsessi käitamiseks saate kasutada lehte **Saldo statistika arvutamine** (**Krediidihaldus \> Perioodilised ülesanded \> Saldo statistika arvutamine**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]