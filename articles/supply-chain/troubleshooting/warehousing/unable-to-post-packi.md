---
title: Peatatud müügitellimuse rea saatelehte ei saa sisestada
description: Peatatud müügitellimuse rea saatelehte ei saa sisestada
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462918"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Peatatud müügitellimuse rea saatelehte ei saa sisestada

Tõrkekood: SYS13203

## <a name="symptoms"></a>Sümptomid

Kui proovite sisestada koorma saatelehte, kuvab süsteem järgmise tõrketeate:

> Müügitellimuse rea peatamisel ei saa saatelehte sisestada pärast väljamineva saadetise A koguse kinnitamist ei saa komplekteeritud olla.

## <a name="cause"></a>Põhjus

Ühe või mitme seotud müügitellimuse rea saab peatada, mis tähendab, et süsteem takistab selle müügitellimuse edasist töötlemist. Muu hulgas tähendab see, et süsteem ei sisesta tellimuse saatelehte.

Näiteks võib kasutaja teha otsuse peatada üks või mitu tellimuserida, kuna klient helistas tagasi ja tühistas tellimuse. Kui väljaminev saadetis oli juba kinnitatud, oleks müügitellimust sisaldav saadetis juba laost välja läinud, mis tähendab, et müügitellimuse ridade peatamine ei oma mingit mõju. Kuna saadetist ei ole enam võimalik füüsiliselt peatada, võite eemaldada ka töölt read, et saatelehte sisestada. Siis peate tühistatud tellimust tagastusena käsitlema.

## <a name="resolution"></a>Lahendus

Saatelehe sisestamiseks veenduge, et ükski müügitellimuse rida ei oleks järgmiste sammude abil peatatud.

1. Minge kõigi **müügitellimuste müügi ja \> turunduse kõigi \> müügitellimuste alla**.
1. Otsige ja avage müügitellimus, mille puhul teil on probleeme.
1. Valige kiirkaardil **Müügitellimuse read** müükide tellimuse rida.
1. Kiirkaardil **Rea** üksikasjad avage vahekaart **Üldine** ja veenduge, et välja **Peatatud** väärtuseks on määratud *Ei*.
1. Jätkake tööd seni, kuni kõik vastavad müügiread pole enam peatatud.
1. Proovige uuesti sisestada koorma või müügitellimuse saateleht.
