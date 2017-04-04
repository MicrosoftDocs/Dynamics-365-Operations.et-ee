---
title: "Kõnekeskuse järjepidevusprogrammi seadistamine"
description: "Selles artiklis kirjeldatakse, kuidas seadistada kõnekeskuse järjepidevusprogrammi."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16081
ms.assetid: 426a9be7-a931-4780-b372-e06f6083dd60
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e32961f2a0e0e41715d98075cbc5777d256eb187
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-a-continuity-program-for-a-call-center"></a>Kõnekeskuse järjepidevusprogrammi seadistamine

Selles artiklis kirjeldatakse, kuidas seadistada kõnekeskuse järjepidevusprogrammi.

Järjepidevusprogrammis, mida nimetatakse ka korduva tellimuse programmiks, saavad kliendid korrapäraselt tootesaadetisi eelmääratletud graafiku alusel. Iga saadetis võib sisaldada erinevaid tooteid, nagu raamatuklubi kuu parima raamatu saatmisel, või saadetakse sama toodet korduvalt. Järjepidevusprogrammi seadistamiseks täitke järgmised ülesanded.

1.  Seadistage järjepidevuse parameetrid lehel **Kõnekeskuse parameetrid**.
2.  Looge järjepidevusprogramm, mis määrab sellised andmed, nagu maksegraafik, saadetiste ajastus ja käsirahaga arveldus. Samuti peate lisama järjepidevusprogrammi kaasatud toodete loendi. Iga toode saab sündmuse ID number, mis määratakse järjestikku, alates 1. Sündmuse ID-de määratlemiseks tagasi saadetud tooted.
    -   Kui kliendid saavad iga saadetisega erineva toote, saadetakse tooted järjest nende sündmuse ID alusel, alustades praegusest sündmusest.
    -   Kui kliendid saavad iga saadetisega sama toote, sisaldab loend ainult üht toodet ühe sündmuse ID-ga. Sama sündmus ilmneb korduvalt. Saate määrata, mitu korda iga sündmust korratakse.

3.  Luua vanema toode, mis esindab järjepidevuse programm loodud ülesande 2. Selle toote lisamisel müügitellimusega, on **järjepidevuse** lehekülg avaneb. Seejärel saate kasutada seda lehte tegeliku järjepideva tellimuse loomiseks. Ematoode ei määra üksikuid tooteid, mida klient iga saadetisega saab.

Kui olete järjepidevusprogrammi seadistanud, nagu eespool kirjeldatud, saate kliendile luua järjepideva tellimuse. Teil võib olla vaja teha ka järgmisi lisahaldustoiminguid.

-   **Järjepidevuse praeguse sündmuse perioodi värskendus** – seadistage pakett-töö, mis ütleb süsteemile, milline on praegune sündmuse periood.
-   **Järjepidevuse tütartellimuste loomine** – looge järjepidevuse ematellimusest tütartellimused.
-   **Järjepidevuse maksete töötlemine** – töödelge arveldust ja teatisi järjepidevuse müügitellimustega seostatud maksete kohta.
-   **Järjepidevuse ridade pikendamine** (vajaduse korral) – pikendage nii mitu korda, kui järjepidevat sündmust saab korrata. Saadetiste kordamine võib siis ületada kõnekeskuse parameetrite väljal **Järjepidevuse kordumise lävi** seadistatud limiidi.
-   **Järjepidevuse värskendamine** (vajaduse korral) – sünkroonige muudatusi järjepidevusprogrammi ja järjepidevuse emamüügitellimuste vahel.
-   **Järjepidevuse põhiridade ja tellimuste sulgemine** – sulgege järjepidevad tellimused.



