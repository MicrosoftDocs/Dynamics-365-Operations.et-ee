---
title: Toode on kannete jaoks ootel
description: Pärast plaanimistellimuste kinnitamist saate tõrketeate, mis kinnitab, et kaup on kannete jaoks ootel.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752606"
---
# <a name="product-is-on-hold-for-transactions"></a>Toode on kannete jaoks ootel

Tõrkekood: SYS13295

## <a name="symptoms"></a>Sümptomid

Pärast plaanitud tellimuste kinnitamist kuvatakse järgmine tõrketeade:

> Kaup %1 on ootel kannete jaoks asukohas %2.

## <a name="cause"></a>Põhjus

Blokeeritud kaupade kirjeldamisel kasutab süsteem tingimusi *blokeeritud*, *peatatud* ja *ootel*. See tõrge tähendab, et kaup on seatud tellimuse vaikesätetes väärtusele **Peatatud**.

Kui kaup on blokeeritud ja te lisate selle ostu- või müügitellimuse reale, saate hoiatusteate. Kui kaup on blokeeritud, näiteks saatelehe või arve sisestamisel, ei saa ostu- või müügitellimuse reaga seotud laokandeid muuta. Saate blokeerida ostetud kauba ja samaaegselt kauba müüa. Sel juhul on märkeruut **Peatatud** ostutellimusel märgitud, kuid kaup pole laovarudes või müügitellimusel blokeeritud.

Järgnevalt on toodud mõned tingimused, mis võivad põhjustada kaubakoodi blokeerimise müügilt.

- Kaup on alles arenduses või tootmises. Seetõttu ei soovi te seda müüa ega reserveerida.
- Olete saanud palju praakkaupu ja vead tuleb parandada enne kauba müümist.

Seda tüüpi juhtumide korral saate vahepealseks ajaks kauba blokeerida, kuni probleem on lahendatud.

Kui kaup on blokeeritud ja koostate tagastustellimuse rea, saate teate. Te ei saa blokeerida kauba seeriaid ega selle saatepartiid. Kui kauba osi peab blokeerima, saate seda teha, varusid teisaldades või blokeerides kogu antud perioodi kaubavaru.

## <a name="resolution"></a>Lahendus

- Avage leht **Kauba tellimuse vaikesätted** leht ja tühjendage märkeruut **Peatatud**.
