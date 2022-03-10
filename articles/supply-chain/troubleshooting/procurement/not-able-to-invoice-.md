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
ms.openlocfilehash: 30c485be79be5ebbec8b51272b8bbe6e0c7df9d81bbaaaef316dbfede03abf68
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756747"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a>Te ei saa arvet esitada kliendile suunatud müügitellimuse kohta

KB number: 4611793

## <a name="symptoms"></a>Sümptomid

Pärast valiku **Sisesta arve automaatne** hankijale lubamist ei saa te enam algset müügitellimust ja algset **otsetarnega** ostutellimust esitada.

## <a name="resolution"></a>Eraldusvõime

Kontsernisiseste ja otsetarnete tellimuste arvete sünkroonimiskäitumist kontrollivad ja jõustavad parameetrid, mida on kirjeldatud jaotises [Parameetrite seadistamine ettevõttevahelise tellimuse postitamiseks](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).

Pärast nende parameetrite seadistamist peate esmalt esitama arve ettevõttevahelise müügitellimuse kohta. Seejärel sünkroonitakse algsed müügitellimused ja ostutellimused.
