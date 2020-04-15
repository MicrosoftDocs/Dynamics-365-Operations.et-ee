---
title: Digitaalallkirjade seadistamine
description: Kasutage seda protseduuri digitaalallkirjade seadistamiseks.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b8b248481f04856fe15dadbc245caae5330ef8f
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140532"
---
# <a name="set-up-electronic-signatures"></a>Digitaalallkirjade seadistamine

[!include [banner](../../includes/banner.md)]

Kasutage seda protseduuri digitaalallkirjade seadistamiseks. Elektronallkiri kinnitab isiku, kes käivitab või kinnitab protsessi. Selle protseduuri loomiseks kasutati demoettevõtte DAT andmeid.


## <a name="enable-the-electronic-signature-configuration-key"></a>Digitaalallkirja konfiguratsioonivõtme lubamine
1. Minge jaotisse Süsteemihaldus > Seadistus > Litsentsi konfiguratsioon.
2. Laiendage puul üksust Administreerimine.
    * Kontrollige, kas ruut Digitaalallkirjastamine on märgitud.  
    * Kui ruut Digitaalallkirjastamine ei ole märgitud, peate lubama hooldusrežiimi. Hooldusrežiimi saab selles keskkonnas lubada, käivitades teenustes Lifecycle Services hooldustöö või kasutades kohalikult tööriista Deployment.Setup.  
3. Sulgege leht.

## <a name="set-up-electronic-signature-parameters"></a>Digitaalallkirja parameetrite seadistamine
1. Minge jaotisse Organisatsiooni haldamine > Seadistus > Digitaalallkirjastamine > Digitaalallkirjastamise parameetrid.
2. Klõpsake nuppu Redigeeri.
3. Sisestage väärtus väljale Teade.
    * Sisestage teatis, mille allkirjastajad saavad allkirja nõudes. Saate sisestada mis tahes teksti. Tavaliselt kirjeldatakse kasutajale dokumendi elektronallkirjastamist.  
    * Kui soovite sisestada teate teksti ka muudes keeltes, klõpsake nuppu Tõlked.  
4. Klõpsake nuppu Salvesta.
5. Sulgege leht.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Digitaalallkirjadele põhjusekoodide seadistamine
1. Minge jaotisse Organisatsiooni haldamine > Seadistus > Digitaalallkirjastamine > Digitaalallkirjastamise põhjusekoodid.
2. Klõpsake valikut Uus.
    * Põhjusekoodid peab seadistama enne elektronallkirjade kasutamist. Dokumendi allkirjastamisel on vajalik kehtiv põhjusekood.     Allkirjastaja valib põhjusekoodi elektronallkirja eesmärgile viitamiseks. Põhjusekoodi saab kasutada näiteks seaduslikule kinnitusele viitamiseks.  
3. Sisestage väärtus väljale Põhjusekood.
4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Vajaduse korral sisestage täiendavad põhjusekoodid.  
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.

## <a name="require-electronic-signatures-for-existing-processes"></a>Olemasolevate protsesside digitaalalkirjastamise nõudmine
1. Minge jaotisse Organisatsiooni haldamine > Seadistus > Digitaalallkirjastamine > Digitaalallkirjastamise nõuded.
2. Otsige loendist ja valige soovitud kirje.
    * Saate valida digitaalallkirjastamist nõudev protsess.  
3. Valige või tühjendage ruut Allkiri nõutav.
    * Korrake neid etappe iga digitaalallkirjastamist nõudva protsessi puhul.  
4. Klõpsake nuppu Salvesta.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Digitaalallkirjastamiseks kohandatud nõude loomine
1. Klõpsake valikut Uus.
2. Valige või tühjendage ruut Allkiri nõutav.
3. Sisestage väljale Nimi digitaalallkirjastamist nõudva protsessi nimi.
4. Klõpsake väljal Tabeli nimi otsingu avamiseks ripploendi nuppu.
5. Leidke ja valige loendist tabel, kuhu allkirjastatavad andmed salvestada.
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake väljal Välja nimi otsingu avamiseks ripploendi nuppu.
8. Leidke ja valige loendist tabeli välja nimi, mida soovite jälgida.
9. Klõpsake loendis valitud real olevat linki.
    * Määrake allkirjanõude kord.     Valige suvand Alati, kui allkiri on nõutav välja andmete muutumisel.     Valige suvand Ainult, kui allkiri on nõutav ainult teatud tingimustel. Suvandi Ainult valimisel peate valima ka ühe järgmistest suvanditest: Kirje sisestamisel, Kirje värskendamisel või Kirje kustutamisel.  
10. Klõpsake nuppu Salvesta.
11. Sulgege leht.

