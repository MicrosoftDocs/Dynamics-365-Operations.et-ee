---
title: Perioodilised kreedidihalduse ülesanded
description: Selles teemas kirjeldatakse perioodilisi toiminguid, mis on osa klientide krediidilimiitide haldamise protsessist.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 53b7cd00b3287f18ba65391842ac259ab2434b86
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735432"
---
# <a name="periodic-credit-management-tasks"></a>Perioodilised kreedidihalduse ülesanded

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse perioodilisi toiminguid, mis on osa klientide krediidilimiitide haldamise protsessist.

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
