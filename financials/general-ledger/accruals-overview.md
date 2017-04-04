---
title: "Viitvõlgade ülevaade"
description: "Selles artiklis kirjeldatakse viitvõlgu ning antakse teavet nende seadistamise ja kannete loomise kohta."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerAccuralTable
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14131
ms.assetid: 0489b59a-37a7-4a78-87bf-4b597e9efad9
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 328a4a7bef32ee8634e4a9f4854ebe78fcc99f6d
ms.lasthandoff: 03/31/2017


---

# <a name="accruals-overview"></a>Viitvõlgade ülevaade

Selles artiklis kirjeldatakse viitvõlgu ning antakse teavet nende seadistamise ja kannete loomise kohta.

Viitvõlgu kasutatakse tekkepõhises arvestuses tulu jälgimiseks, mis on tuvastatud selle teenimise perioodil, mitte makse saamisel, ja kulude jälgimiseks, mis on tuvastatud nende toimumisel, mitte makse tegemisel.

## <a name="accrual-schemes"></a>Viitvõlgade skeemid
Viitvõlgade skeeme kasutatakse edasilükatud tulu ja kulude määramiseks ja sama viitvõlgade skeemi saab kasutada nii tulu kui ka kulude puhul. Pearaamatu viitvõlad jaotavad tööleherea kulud või tulu nii, et kulud ja tulud tuvastatakse kindlatel perioodidel. Lehel **Viitvõlgade skeem** määrate viitvõla skeemi rakendamisel kasutatava deebet- ja kreeditkonto.

-   **Deebet** – teie määratav põhikonto, mis asendab töölehekande real deebeti põhikonto. Seda kontot kasutatakse ka viitvõla tagasivõtmiseks pearaamatu tekkepõhiste kannete põhjal.
-   **Kreedit** – teie määratav põhikonto, mis asendab töölehekande real kreediti põhikonto. Seda kontot kasutatakse ka viitvõla tagasivõtmiseks pearaamatu tekkepõhiste kannete põhjal.

Pärast kasutatavate kontode määratlemist saate määrata, kuidas kandenumber tekkepõhiste kannete loomisel luuakse. Samuti saate määrata, kui tihti kandeid esineb, kannete loomise arvu ja millal kanded sisestatakse. Pärast viitvõlgade skeemi loomist saate seda pearaamatu viitvõlgade funktsiooni abil kasutada mõnel töölehel.

## <a name="ledger-accruals"></a>Pearaamatu viitvõlad
Töölehe sisestamisel saate klõpsata suvandit **Pearaamatu viitvõlad** menüüs **Funktsioonid**. Seejärel näete viitvõlgade skeemi valimisel töölehe baassummat, mis jaotatakse viitvõlgade skeemis määratud perioodiks. Näiteks kui töötaja kindlustus kogu aasta jaanuaris maksate ja summa on 12 000, peab tunnete kulul iga kuu. Saate valida alguskuupäeva. Saate ka määrata, kas kogunenud summa põhineb kontol või vastaskontol. Kui olete teinud oma valikud, klõpsake **tehingute** saate vaadata kõiki kandeid, mis on loodud põhineb viitvõla. Näiteks kui 12000 kindlustust jagunevad aasta näete 1000 kaupa. Pärast žurnaali konteerimist saate vaadata kannete abil on **kande** päring lehekülje. Viitvõlgade skeemi ei saa (nt kui tegemist on arve müügitellimuse või ostutellimuse arve), saate ettemakstud summa ja remondikulu summa debiteerida. Seejärel saate viitvõlgade skeemi rakendamisel valida suvandi **Vastaskonto**.


