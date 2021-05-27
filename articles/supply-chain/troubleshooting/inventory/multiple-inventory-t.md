---
title: Mitu varude tehingut partiinumbritele, kui füüsiline värskendamine on keelatud
description: Pärast ostutellimuse rea korrigeerimist luuakse mitu varude tehingut, kui partii numbrirühma suvand Füüsilisel uuendamisel valikus on seatud Ei.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventNumGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1fa54cdfdbc5608fb6c7114dced0f96bab47253e
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026453"
---
# <a name="multiple-inventory-transactions-for-batch-numbers-when-on-physical-update-is-disabled"></a>Mitu varude tehingut partiinumbritele, kui füüsiline värskendamine on keelatud

KB number: 4613390

## <a name="symptoms"></a>Sümptomid

Pärast ostutellimuse rea korrigeerimist luuakse mitu varude tehingut, kui partii numbrirühma suvand **Füüsilisel uuendamisel** valikus on seatud *Ei*.

Kui loote kauba, kus partiinumbri grupi suvand **Füüsilisel uuendamisel** on seatud valikule *Ei*, loob süsteem osturea koguse muutmisel ja ostutellimuse lehe salvestamisel automaatselt uue partiinumbri.

## <a name="resolution"></a>Eraldusvõime

Säte **Füüsilisel uuendamisel** partii numbrigruppidele töötab järgmiselt:

- Kui valiku väärtuseks on määratud *Jah* luuakse uued partiinumbrid alles pärast füüsilist uuendamist (nt kaupade tarnimisel või tarnimisel).
- Kui valikuks on määratud *Ei*, luuakse iga kord, kui toimub rakendatav uuendus, uus partiinumber (nt kui ostutellimusele lisatakse uus kogus).
