---
title: Voog ei ole puhastamiseks kõlblik
description: Voog ei ole puhastamiseks kõlblik
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778502"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>Voog ei ole puhastamiseks kõlblik

Tõrkekood: WaveNotEligibleForCleanup

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Voog %1 ei ole puhastamise jaoks sobilik.

Voo andmeid ei saa puhastada.  

## <a name="cause"></a>Põhjus

Voogu töödeldakse praegu, nagu näitab üks järgmistest tingimustest:

- **Voo staatus** väli on seatud *Teostamisele*.
- Kui valite **Partiitöö** grupis **Voog** vahekaardil **Voog** Tegevuspaanil väli **Olek** ei ole seatud *Lõpetatud*, *Viga* või *Tühistatud*. Seetõttu käitatakse praegu pakett-tööd.

## <a name="resolution"></a>Eraldusvõime

Tegevuspaani vahekaardil **Laine** grupis **Laine** valige **Pakett töö** ja siis järgige üht nendest sammudest:

- Kui välja **Olek** on määratud *Teostamine*: Valige Action Paanil vahekaardil **Partiitöö** grupis **Partiitöö** valige **Vaata ülesandeid**. Edenemist saate jälgida värskendades lehte **Partii ülesanded**.
- Kui välja **Olek** ei ole määratud *Teostamine*: Valige Action Paanil vahekaardil **Partiitöö** grupis **Funktsioonid** valige **Muuda olekut**. Valige väljal **Vali uus olek** *Ootamine*. Seejärel valige **OK**.
