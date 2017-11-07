---
title: "Konsolideerimiskontode grupid ja täiendavad konsolideerimiskontod"
description: "See teema annab teavet konsolideerimiskontode gruppide ja täiendavate konsolideerimiskontode kohta ning selgitab nende kasutamist Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: eb69b8def1d0a4fc296ccf44490af6c70591cb7b
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Konsolideerimiskontode grupid ja täiendavad konsolideerimiskontod

[!include[banner](../includes/banner.md)]


See teema annab teavet konsolideerimiskontode gruppide ja täiendavate konsolideerimiskontode kohta ning selgitab nende kasutamist Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis.

<a name="consolidation-account-groups"></a>Konsolideerimiskontode grupid
----------------------------

Konsolideerimiskontode grupid võimaldavad luua gruppe kontodest, mida soovite kasutada andmete konsolideerimiseks. Enamasti kujutab konsolideerimiskontode grupp riiklikul tasandil kontoplaani või vastendab kontod grupiga, mille on määratlenud ettevõtte peakontorid. Konsolideerimiskontode grupid leiate mooduli **Konsolideerimised** alast **Häälestus**. Uue kontogrupi lisamisel sisestage selle jaoks kordumatu identifikaator ja nimi.

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




