---
title: Partii jälgimisega kaupade täiustatud käsitlemine
description: Selles teemas kirjeldatakse täiustusi, mis on tehtud jaemüügiväljavõtete sisestamisprotsessi käigus partii jälgimisega kaupade partiide käsitlemisele.
author: josaw1
manager: AnnBe
ms.date: 05/28/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4456fc3d5bc4547fa8211642b11ca6df455fa187
ms.sourcegitcommit: aec1dcd44274e9b8d0770836598fde5533b7b569
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2019
ms.locfileid: "1617385"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Partii jälgimisega kaupade täiustatud käsitlemine

Microsoft Dynamics 365 for Retaili kassas (POS) ei saa partiinumbreid partii jälgimisega kaupade puhul müügi hetkel jäädvustada. Kui müügiandmed sisestatakse peakontoris klienditellimuste või väljavõtete sisestuse käigus, siis eeldab süsteem Microsoft Dynamics teatud konfiguratsioonide korral, et partii jälgimisega kaupade jaoks on olemas sobivad partiinumbrid ja neid kasutatakse arveldusprotsessis.

Kui toodete jaoks on saadaval sobivad partiinumbrid, kasutavad väljavõtete sisestamise käigus toimuv klienditellimuste arveldamise protsess ja müügitellimuste arveldamise protsess neid partiinumbreid. Vastasel korral ei saa klienditellimuste arveldamise protsess andmeid sisestada ja kassa kasutaja saab tõrketeate. Väljavõtete sisestus läheb siis tõrkeolekusse. See tõrkeolek ilmneb ka siis, kui negatiivsed varud on toodete jaoks sisse lülitatud.

Microsoft Dynamics for Retaili versioonis 10.0.4 ja uuemas versioonis tehtud täiustused aitavad tagada, et kui partii jälgimisega kaupade jaoks on sisse lülitatud negatiivsed varud, ei blokeerita nende kaupade puhul väljavõtete sisestuse kaudu toimuvat klienditellimuste arveldust ega müügitellimuste arveldust, kui varude väärtus on 0 (null) või partiinumber pole saadaval. Kui partiinumbrid pole saadaval, kasutab see uus funktsioon müügiridade jaoks partii vaike-ID-d.

Klienditellimuste jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe **Jaemüügi parameetrid** vahekaardi **Kliendi tellimused** kiirkaardil **Tellimus** väli **Vaikimisi partii ID**.

Väljavõtete sisestamise kaudu tehtava müügitellimuste arvelduse jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe **Jaemüügi parameetrid** vahekaardi **Sisestamine** kiirkaardil **Laoseisu uuendamine** väli **Vaikimisi partii ID**.

> [!NOTE]
> See funktsioon on saadaval ainult juhul, kui konkreetse kaupluse lao ja kaupade jaoks on sisse lülitatud täpsem laohaldus. Uuemas versioonis toetatakse funktsiooni ka selliste stsenaariumite puhul, kus täpsemat laohaldust ei kasutata.
