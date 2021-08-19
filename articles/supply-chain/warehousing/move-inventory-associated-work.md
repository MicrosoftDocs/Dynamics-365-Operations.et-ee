---
title: Seostatud tööga varude teisaldamine laohalduses
description: Varude liikumise abil saate otsustada, millistel laotöötajatel on reserveeritud varude teisaldamine lubatud.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorker
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d996886a90037f288e839c54c8c9d932cabb21f19f2aef1552ca82b192c96a51
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736547"
---
# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Seostatud tööga varude teisaldamine laohalduses

[!include [banner](../includes/banner.md)]

Varude liikumise abil saate otsustada, millistel laotöötajatel on reserveeritud varude teisaldamine lubatud. See võimaldab paindlikkust reguleeritud ladudes, kus võite mitte lubada töötajal valida juba loodud komplekteerimistööle uut komplekteerimiskohta. Samuti võimaldab see laojuhil kontrollida, millised võimalused väiksemate kogemustega töötajatel olema peaksid.

Laotöötajate igapäevatoimingute juhtimise paindlikkus võib olla abiks näiteks järgmistes stsenaariumides.

## <a name="scenario-1"></a>1. stsenaarium

Ettevõttel on suhteliselt väike vastuvõtuala ja see on paigutamist ootavate aluste ja kastidega ummistatud. Sellel päeval oodatakse suurt saadetist, seega otsustab vastuvõtuametnik vastuvõtuala tühjendada, viies mõned alused teisele sissetuleva kauba kogumisalale.

## <a name="scenario-2"></a>2. stsenaarium

Kogenud laotöötaja märkab laos võimalust konsolideerida kaubad ühte kohta, selle asemel et hoida neid väikeste kogustena kolmes lähestikku asuvas kohas. Töötaja soovib konsolideerida koguse, viies kõigist neist kohtadest kaubad ühte kohta ja samale litsentsiplaadile.

## <a name="scenario-3"></a>3. stsenaarium

Alus ootab laadimisukse BAYDOOR01 läheduses olevas kogumiskohas (nt STAGE01) teelepanekut. Kuid plaanide muutumise tõttu on veok saabumas laadimisukse BAYDOOR04 juurde. Lähetusametnik on sellest teadlik ja peab korraldama asjad nii, et veok ei peaks ootama laadimist laadimisuksest STAGE01. Lähetusametnik otsustab viia selle saadetise kaubad kogumiskohast STAGE01 kogumiskohta STAGE04, mis on uuele sihtkohale lähemal.

### <a name="current-limitations"></a>Praegused piirangud

Töö reserveerimised, mida saab üle viia, on ainult Müügitellimus, Üleviimistellimuse väljaminek, Üleviimistellimuse sissetulek, Ostutellimus ja Täiendustöö.

Kaupade teisaldamine on piiratud tööridade jagamise vältimiseks. See tähendab, et kui teil on töörida kauba A 100 ühiku kohta asukohast Loc1, siis ei saa teisaldada sealt teise kohta ainult 30 ühikut kaubast A. See tooks kaasa olemasoleva töörea jagamise kogusteks 30 ja 70, kuna asukohad on nüüd erinevad.

Kogumisstsenaariumide puhul, kus litsentsiplaat, millelt kauba teisaldate, või litsentsiplaat, millele kauba teisaldate, on määratud töötellimuse litsentsiplaadiks, on lubatud ainult kogu litsentsiplaadi teisaldamine, et sihtlitsentsiplaati mitte jagada.

Praegu toetatakse ainult liikumist konkreetseks otstarbeks. See tähendab, et reserveeritud varusid ei saa malli mobiilse seadme menüüelementide liikumise kaudu liigutada.

### <a name="set-up-permission-to-move-reserved-inventory-for-individual-workers"></a>Reserveeritud varude teisaldamise õiguse seadistamine eraldi töötajatele

Märkige töötaja puhul, kellel on lubatud reserveeritud varusid teisaldada, ruut **Luba seostatud tööta varude teisaldamine** jaotises **Laohaldus \> Seadistus \> Töötaja**.  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
