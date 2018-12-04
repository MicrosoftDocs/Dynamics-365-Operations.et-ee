---
title: "Tagastatud kauba osaliste tarnete vastu võtmine"
description: "Osatarned määratakse tagastustellimuse ridade, mitte tagastustellimuse saadetistena."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: f9f596d31f2438a353b02bf939786b284937db86
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="receive-partial-deliveries-of-returned-items"></a>Tagastatud kauba osaliste tarnete vastu võtmine    

[!include [banner](../includes/banner.md)]


Osatarned määratakse tagastustellimuse ridade, mitte tagastustellimuse saadetistena.

See tähendab, et kui saate täiskoguse, mis on näidatud ühel tagastustellimuse real, kuid ei saa midagi teistelt tagastustellimuse ridadelt, siis ei ole tarne osatarne. Kui tagastustellimuse rida nõuab aga konkreetse kauba kümne ühiku tagastamist, kuid teie saate ainult neli, on tegu osatarnega.

Kui tagastussaadetise kogus on väiksem kui tagastustellimuse rea täiskogus, saate saadetise kõrvale panna ja oodata ülejäänud tagastatud koguse saabumist või saate registreerida ja sisestada osakoguse.

## <a name="register-and-post-a-partial-quantity"></a>Osaline koguse registreerimine ja sisestamine

1.  Kui olete valinud saabumisel tagastustellimuse vormil **Saabumise ülevaade – Ladu: %1, Ala: %2, Töölehe nimi: %3**, klõpsake käsku **Alusta saabumistöölehte**, et luua saabumistööleht, ja klõpsake valikuid **Töölehed** \> **Kuva sissetulekute saabumistöölehed**, et avada vorm **Asukoha tööleht**.

2.  Valige töölehe rida, mida soovite kasutada, ja klõpsake seejärel nuppu **Read**, et avada vormi **Töölehe read, asukohad**.

3.  Valige kaubakoodi rida, millele on saabunud ainult osakogus, ja seejärel klõpsake käske **Funktsioonid** \> **Tükelda** vormi **Tükelda** avamiseks.

4.  Väljale **Tükeldatud kogus** sisestage saadud kaubakoguse koguarv ja seejärel klõpsake nuppu **OK**.

5.  Valige vormil **Töölehe read, asukohad** saabunud kaubakoguse rida ja seejärel klõpsake käsku **Postita**. Täiendava koguse saate reale sisestada pärast kaupade saabumist.





