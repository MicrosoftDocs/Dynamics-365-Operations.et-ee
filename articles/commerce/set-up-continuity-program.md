---
title: Kõnekeskuste järjepidevusprogrammide seadistamine
description: Selles artiklis kirjeldatakse, kuidas seadistada kõnekeskuse järjepidevusprogrammi.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCROrderParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 39c3e6d740bff2af27a2fba2ac4c406c01b43a87218fdc1dcfe094c147cd3de3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716146"
---
# <a name="set-up-continuity-programs-for-call-centers"></a>Kõnekeskuste järjepidevusprogrammide seadistamine

[!include [banner](includes/banner.md)]

Selles artiklis kirjeldatakse, kuidas seadistada kõnekeskuse järjepidevusprogrammi.

Järjepidevusprogrammis, mida nimetatakse ka korduva tellimuse programmiks, saavad kliendid korrapäraselt tootesaadetisi eelmääratletud graafiku alusel. Iga saadetis võib sisaldada erinevaid tooteid, nagu raamatuklubi kuu parima raamatu saatmisel, või saadetakse sama toodet korduvalt. Järjepidevusprogrammi seadistamiseks täitke järgmised ülesanded.

1. Seadistage järjepidevuse parameetrid lehel **Kõnekeskuse parameetrid**.
2. Looge järjepidevusprogramm, mis määrab sellised andmed, nagu maksegraafik, saadetiste ajastus ja käsirahaga arveldus. Samuti peate lisama järjepidevusprogrammi kaasatud toodete loendi. Iga toode saab sündmuse ID-koodi, mis määratakse järjestikuselt, alustades arvuga 1. Sündmuse ID-d määravad järjestuse, milles tooteid saadetakse.

    - Kui kliendid saavad iga saadetisega erineva toote, saadetakse tooted järjest nende sündmuse ID alusel, alustades praegusest sündmusest.
    - Kui kliendid saavad iga saadetisega sama toote, sisaldab loend ainult üht toodet ühe sündmuse ID-ga. Sama sündmus ilmneb korduvalt. Saate määrata, mitu korda iga sündmust korratakse.

3. Looge ematoode, mis tähistab ülesandes 2 loodud järjepidevusprogrammi. Kui lisate selle toote müügitellimusele, avaneb leht **Järjepidevus**. Seejärel saate kasutada seda lehte tegeliku järjepideva tellimuse loomiseks. Ematoode ei määra üksikuid tooteid, mida klient iga saadetisega saab.

Kui olete järjepidevusprogrammi seadistanud, nagu eespool kirjeldatud, saate kliendile luua järjepideva tellimuse. Teil võib olla vaja teha ka järgmisi lisahaldustoiminguid.

- **Järjepidevuse praeguse sündmuse perioodi värskendus** – seadistage pakett-töö, mis ütleb süsteemile, milline on praegune sündmuse periood.
- **Järjepidevuse tütartellimuste loomine** – looge järjepidevuse ematellimusest tütartellimused.
- **Järjepidevuse maksete töötlemine** – töödelge arveldust ja teatisi järjepidevuse müügitellimustega seostatud maksete kohta.
- **Järjepidevuse ridade pikendamine** (vajaduse korral) – pikendage nii mitu korda, kui järjepidevat sündmust saab korrata. Saadetiste kordamine võib siis ületada kõnekeskuse parameetrite väljal **Järjepidevuse kordumise lävi** seadistatud limiidi.
- **Järjepidevuse värskendamine** (vajaduse korral) – sünkroonige muudatusi järjepidevusprogrammi ja järjepidevuse emamüügitellimuste vahel.
- **Järjepidevuse põhiridade ja tellimuste sulgemine** – sulgege järjepidevad tellimused.


[!INCLUDE[footer-include](../includes/footer-banner.md)]