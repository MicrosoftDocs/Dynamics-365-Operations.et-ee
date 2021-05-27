---
title: Viga aruande lõpetamise päevikuna postitamisel
description: Kui postitate aruande lõpetatud päevikuna, kuvatakse tõrketeade, mis ütleb, et tellitud tellitud kogust ei saa vähendada.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 55db7d0033dd66c1b973abf96671a20ab05d61d8
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026428"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Viga aruande lõpetamise päevikuna postitamisel

KB number: 4612891

## <a name="symptoms"></a>Sümptomid

Töölehe **Lõpetatuna kinnitatud** sisestamisel ilmneb tõrge ja kuvatakse järgmine tõrketeade:

> Tellitud kogust ei saa vähendada, kuna pole piisavalt avatud laokandeid, mille olek on Tellitud. Kaubad on ostetud, saadud või registreeritud.

See tõrge ilmneb ainult siis, kui väli **Veakogus** on seadistatud esimesele **Lõpetatuna kinnitatud** reale ja **Hea kogus** väli on seadistatud viimasele reale. Kui **Veakogus** väli on seadistatudviimasele reale, siis tõrkeid ei esine.

## <a name="resolution"></a>Eraldusvõime

Tõrke vältimiseks avage **Tootmise juhtimise parameetrite** leht ja seejärel seadke seal **Üldine** vahekaardil suvandi **Kasvu püsikogus tõrkekogusega** väärtusele *Jah*.
