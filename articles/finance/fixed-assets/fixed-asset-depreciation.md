---
title: Põhivara kulum
description: See artikkel annab ülevaate põhivarade kulumist.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.form: AssetBonus, AssetBookTable
ms.openlocfilehash: 9761fc9846324d1c165274b72033e195bf4ea3e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275291"
---
# <a name="fixed-asset-depreciation"></a>Põhivara kulum

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See artikkel annab ülevaate põhivarade kulumist.

Kulum on perioodiline kanne, mis tavaliselt vähendab bilansis põhivara väärtust ning mis kantakse kuluna tulu ja kulu kontole. Seetõttu kasutatakse bilansis perioodilise kulumi krediteerimiseks tavaliselt põhikontot. Vastaskonto on kontoplaani tulude ja kulude osas olev konto.

Versiooni 10.0.24 **järgi** lubab **lehe** Raamatud suvand Arvuta positiivne kulumivararaamatu konfiguratsioon kulumit debiteerida negatiivse raamatupidamisväärtusega (kreedit) soetatud põhivara.

## <a name="depreciation-adjustment"></a>Kulumi korrigeerimine
Tavaliselt sisestatakse kulumi korrigeerimisena ainult sisestatud kulumikande parandus. Seetõttu seadistatakse nii põhikonto kui ka vastaskonto samamoodi kui kulumikontod. Kulumit võidakse korrigeerida nii positiivse kui ka negatiivse summa võrra, kuid põhikonto (bilansikontona) ja vastaskonto funktsionaalsus (tavaliselt kasumi ja kahjumi kontona) funktsioon jääb samaks.

## <a name="extraordinary-depreciation"></a>Plaaniväline kulum
Plaaniväline kulumi toimib samamoodi kui põhikulum. Seetõttu kasutatakse kulumisumma krediteerimisel bilanssi ja põhivara väärtuse vähendamiseks põhikontot. Vastaskonto on tulu ja kulu konto, kus rahandusperioodi jaoks arvutatud kulum arvestatakse kuluna. 

Plaaniväline kulum toimib põhikulumist sõltumatult. Kui teil on plaaniväline kulum kasutusel eraldi kandetüübina, saate plaanivälist kulumit sisestada ja selle kohta aruandeid koostada tavalisest põhikulumist eraldi.

## <a name="special-depreciation-allowance"></a>Kulumi erihüvitis
Kulumi erihüvitis võimaldab teil lisakulumi summasid arvestada vara esimesel kasulikul elu- ja amortisatsiooniaastal. Kulumi erihüvitis tuleb võtta enne mis tahes muid kulumiarvutusi. Kuna kulumi erihüvitised on sageli tundmatud kuni põhivara tööea hilisema järguni, on mõistlik kasutada seda tüüpi kulumit koos raamatuga, mis ei sisesta pearaamatusse. Saate nende raamatute kandeajaloo kustutamiseks kasutada regulaarset funktsiooni Pearaamatusse sisestamata kannete kustutamine. Seejärel saate kustutada põhivara raamatu kulumiajaloo, sisestada kulumi erihüvitise, kui see on teada, ja seejärel sisestada ülejäänud kulumikanded aasta kohta. 

Loodavate kulumi erihüvitise kirjete arv on piiramatu. Pärast nende kirjete määramist varagrupi raamatule rakendatakse need sellele kulumiraamatule. 

Kulumi erihüvitis sisestatakse protsendi või fikseeritud summana. Kui sisestate kulumisoovitusi, sisestatakse kulumi erihüvitiste kanded raamatusse kulumikannetest eraldi kannetena.

## <a name="depreciation-calendars"></a> Kulumikalendrid
Igal raamatul on kalender, mida kasutatakse põhivarade kulumiarvestusel. Kui te kalendrit raamatus ei näita, kasutab raamat vaikimisi pearaamatu rahanduskalendrit. Raamatule tuleb valida rahanduskalender, kui raamatuga seotud kulumireeglid kasutavad kulumiarvestuseks rahandusaastat. 

Saate luua ühiskasutusega kalendrid, kasutades pearaamatus lehte **Rahanduskalendrid**.

Lisateavet leiate jaotisest [Kulumimeetodid ja kulumiarvestusreeglid](depreciation-methods-conventions.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
