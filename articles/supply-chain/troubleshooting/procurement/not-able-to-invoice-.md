---
title: Te ei saa arvet esitada kliendile suunatud müügitellimuse kohta
description: Pärast valiku Sisesta arve automaatne lubamist ei saa te enam algset müügitellimust ja algset otsetarnega ostutellimust esitada.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026435"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Te ei saa arvet esitada kliendile suunatud müügitellimuse kohta

KB number: 4611793

## <a name="symptoms"></a>Sümptomid

Pärast valiku **Sisesta arve automaatne** hankijale lubamist ei saa te enam algset müügitellimust ja algset **otsetarnega** ostutellimust esitada.

## <a name="resolution"></a>Eraldusvõime

Kontsernisiseste ja otsetarnete tellimuste arvete sünkroonimiskäitumist kontrollivad ja jõustavad parameetrid, mida on kirjeldatud jaotises [Parameetrite seadistamine ettevõttevahelise tellimuse postitamiseks](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Pärast nende parameetrite seadistamist peate esmalt esitama arve ettevõttevahelise müügitellimuse kohta. Seejärel sünkroonitakse algsed müügitellimused ja ostutellimused.
