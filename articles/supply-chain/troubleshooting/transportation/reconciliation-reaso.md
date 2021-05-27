---
title: Põhikonto saab krediidikontona lisada ainult vastavussebviimise põhjustel
description: Transpordihalduses vastavussebviimise põhjuse häälestamisel saate kreeditkontoks lisada ainult põhikonto.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026425"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a>Põhikonto saab krediidikontona lisada ainult vastavussebviimise põhjustel

KB number: 4603538

## <a name="symptoms"></a>Sümptomid

Transpordihalduses vastavussebviimise põhjuse häälestamisel saate kreeditkontoks lisada ainult põhikonto. Te ei saa krediidikontona lisada kulukeskust ega muid dimensioone. Deebetkonto võimaldab teil siiski valida teisi dimensioone.

## <a name="resolution"></a>Eraldusvõime

Kui vastavusseviimine ei ole hankijale maksmiseks, vaid kindla põhikonto krediteerimiseks, ei luba süsteem teil vastavusseviimise põhjuse häälestamisel valida kreeditkonto jaoks rahalist mõõdet.

Kui konto struktuur nõuab kreediti põhikonto jaoks kindlat finantsdimensiooni väärtust, ei saa tulemuseks saadud hankija töölehte automaatselt sisestada, kuna finantsdimensiooni väärtus puudub. Seega peate esmalt käsitsi määrama kreeditkonto, kasutades **Arve tööleht** lehte.

Kuna kreeditkonto jaoks on vajalik dimensiooniväärtus, ei saa hankija arve töölehte automaatselt sisestada. Pärast dimensiooniväärtuse käsitsi sisestamist peate selle krediidirea põhikontole lisama.
