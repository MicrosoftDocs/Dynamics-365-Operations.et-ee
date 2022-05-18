---
title: Konsolideerimiskontode grupid ja täiendavad konsolideerimiskontod
description: See teema annab teavet konsolideerimiskonto gruppide ja täiendavate konsolideerimiskontode kohta ning selgitab nende kasutamist.
author: panolte
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerConsolidateAccountGroup
audience: Application User
ms.reviewer: kfend
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5ca7a50fcac53f1636da15b2d7977174b087ac25
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711689"
---
# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolideerimiskonto grupid ja täiendavad konsolideerimiskontod

[!include [banner](../includes/banner.md)]

See teema annab teavet konsolideerimiskonto gruppide ja täiendavate konsolideerimiskontode kohta ning selgitab nende kasutamist.

## <a name="consolidation-account-groups"></a>Konsolideerimiskontode grupid

Konsolideerimiskontode grupid võimaldavad luua gruppe kontodest, mida soovite kasutada andmete konsolideerimiseks. Tavaliselt esindab konsolideerimiskonto grupp valitsuse volitatud kontoplaani. Konsolideerimiskonto grupp saab vastendada ka kontosid grupiga, mille on määranud ettevõtte peakontor. Konsolideerimiskontode grupid leiate mooduli **Konsolideerimised** alast **Häälestus**. Uue grupi lisamisel saate sisestada kontogrupi kordumatu ID ja nime.

## <a name="additional-consolidation-accounts"></a>Täiendavad konsolideerimiskontod
Täiendavad konsolideerimiskontod võimaldavad määrata konto olemasolevast kontoplaanist konsolideerimiskontode gruppi. Seejärel saate määrata konsolideerimiskonto väärtuse ja nime. 

Täiendavad konsolideerimiskontod leiate mooduli **Konsolideerimised** alast **Häälestus**. Uue konsolideerimiskonto loomisel peate määrama järgmise teabe.

-   **Põhikonto** – see väli on otsinguväli, millel kuvatakse kõik lehel valitud kontoplaanil põhinevad põhikontod. Konto valimisel sisestatakse selle nimi automaatselt väljale **Põhikonto nimi**.
-   **Konsolideerimiskontode grupp** – selle väljaga saate valida grupi, millesse konto määrata. Kahel erineval viisil konsolideerimisel peate lisama sama konto kõigisse nelja konsolideerimiskontode gruppi.
-   **Konsolideerimiskonto** – sisestage konsolideerimiskonto väärtus. See väärtus ei pea olema konto kontoplaanilt. See võib olla mis tahes teie nõutud väärtus.
-   **Konsolideerimiskonto nimi** – sisestage konto nimi kujul, nagu soovite seda kuvada päringutes ja aruannetes.
-   **SAT tase** – seda välja kasutatakse Mehhiko maksuasutustele kontoväljavõtete esitamiseks. 

Kui olete konsolideerimiskontode gruppide ja täiendavate konsolideerimiskontode loomise lõpule viinud, saate valida grupi jaotises Võrgus konsolideerimise protsess.


Lisateabe saamiseks vt [Konsolideerimisgruppide ja täiendavate konsolideerimiskontode loomine](../general-ledger/tasks/create-consolidation-groups.md) 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
