---
title: Partii jälgimisega kaupade täiustatud käsitlemine
description: Selles teemas kirjeldatakse täiustusi, mis on tehtud väljavõtete sisestamisprotsessi käigus partii jälgimisega kaupade partiide käsitlemisele.
author: josaw1
manager: AnnBe
ms.date: 11/04/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: 10
ms.openlocfilehash: ef946df30c68373b83660fce98b472dc94b42719
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989589"
---
# <a name="improved-handling-of-batch-tracked-items"></a>Partii jälgimisega kaupade täiustatud käsitlemine


[!include [banner](includes/banner.md)]


Kassas (POS) ei saa partiinumbreid partii jälgimisega kaupade puhul müügi hetkel jäädvustada. Kui müügiandmed sisestatakse peakontoris klienditellimuste või väljavõtete sisestuse käigus, siis eeldab süsteem Microsoft Dynamics teatud konfiguratsioonide korral, et partii jälgimisega kaupade jaoks on olemas sobivad partiinumbrid ja neid kasutatakse arveldusprotsessis.

Kui toodete jaoks on saadaval sobivad partiinumbrid, kasutavad väljavõtete sisestamise käigus toimuv klienditellimuste arveldamise protsess ja müügitellimuste arveldamise protsess neid partiinumbreid. Vastasel korral ei saa klienditellimuste arveldamise protsess andmeid sisestada ja kassa kasutaja saab tõrketeate. Väljavõtete sisestus läheb siis tõrkeolekusse. See tõrkeolek ilmneb ka siis, kui negatiivsed varud on toodete jaoks sisse lülitatud.

Retaili versioonis 10.0.4 ja uuemates tehtud täiustused aitavad tagada, et kui partii jälgimisega kaupade jaoks on sisse lülitatud negatiivsed varud, ei blokeerita nende kaupade puhul väljavõtete sisestuse kaudu toimuvat klienditellimuste arveldust ega müügitellimuste arveldust, kui varude väärtus on 0 (null) või partiinumber pole saadaval. Kui partiinumbrid pole saadaval, kasutab see uus funktsioon müügiridade jaoks partii vaike-ID-d.

Klienditellimuste jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe **Kaubanduse parameetrid** vahekaardi **Kliendi tellimused** kiirkaardil **Tellimus** väli **Vaikimisi partii ID**.

Väljavõtete sisestamise kaudu tehtava müügitellimuste arvelduse jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe **Kaubanduse parameetrid** vahekaardi **Sisestamine** kiirkaardil **Varude uuendamine** väli **Vaikimisi partii ID**.

> [!NOTE]
> See funktsioon on saadaval ainult juhul, kui konkreetse kaupluse lao ja kaupade jaoks on sisse lülitatud täpsem laohaldus. Uuemas versioonis toetatakse funktsiooni ka selliste stsenaariumite puhul, kus täpsemat laohaldust ei kasutata.

> [!NOTE]
> Partii jälgimisega kaupade täiustatud töötlemise tugi väljavõtte sisestamise ajal võeti täpsemat laohaldust mittekasutavates stsenaariumites kasutusele Retaili versioonis 10.0.5.
