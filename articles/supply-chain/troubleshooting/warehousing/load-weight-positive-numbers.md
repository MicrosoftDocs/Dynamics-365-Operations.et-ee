---
title: Koorma kaal võib sisaldada ainult positiivseid numbreid
description: Töö töötlemisel asukohtade vahel võite saada vea koorma kaalu ja värskenduse tühistamise kohta. Probleemi lahendamiseks tehke järgmist.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8ea1f6679a521e3e8683b8e5f18f509e98044414
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476108"
---
# <a name="load-weight-error-and-update-canceled-when-processing-work-between-locations"></a>Koorma kaalu tõrge ja värskendamine tühistati töö töötlemisel asukohtade vahel

## <a name="symptoms"></a>Sümptomid

Te saate selle tõrketeate, kui avatud töö puhul töötlete tööd pakkimisasukohtades vaheasukohtadesse või vaheasukohtadest dokkimisasukohtadesse:

> Välja 'Koorma kaal'(=%1) võib sisaldada ainult positiivseid numbreid. Uuendus on tühistatud.

## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks minge **Süsteemi administreerimise \> Perioodilised ülesanded \> Andmebaas \> Järjepidevuse kontroll** ja käivitage protsess **Lao koormuse kaalu järjepidevuse kontrollimiseks**.
