---
title: Algandmete lähtestamine uutes Commerce'i keskkondades
description: See artikkel kirjeldab andmeid, mis luuakse Dynamics 365 Commercei jaemüügimooduli lähtestamisprotsessi käigus.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8fd0b2743deab758538922f312853b622a512c0a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000736"
---
# <a name="initialize-seed-data-in-new-commerce-environments"></a>Algandmete lähtestamine uutes Commerce'i keskkondades

[!include [banner](includes/banner.md)]

See artikkel kirjeldab andmeid, mis luuakse Dynamics 365 Commercei jaemüügimooduli lähtestamisprotsessi käigus.

Pärast teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu lahenduse Kaubandus juurutamist peate lähtestama kaubanduse konfiguratsiooni, et luua põhilised konfigureerimise andmed.

> [!IMPORTANT]
> Enne kaubanduse konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te kaupluse seadistate. See etapp tuleb läbida iga juriidilise isiku puhul, mida kaubanduses kasutate.

Konfiguratsiooni lähtestamiseks toimige järgmiselt.

1. Käivitage rakenduse Kaubandus klient.
2. Minge jaotisse **Jaemüük ja kaubandus** &gt; **Peakontori seadistamine** &gt; **Parameetrid** &gt; **Kaubanduse parameetrid**.
3. Klõpsake suvandit **Lähtesta**.

Lähtestamine loob järgmised konfiguratsiooni vaikeandmed.

- Kaubanduse andmeedastaja tööd ja alamtööd
- Kaubanduse kanaliskeem
- Kaubanduse jaotuse graafikud
- Ekraani vaikepaigutused, mis hõlmavad nupupaneele, pilte ja kujundusi
- Ajavööndi teave
- Kassa (POS) toimingud
- Kassaload
- Kanali aruanded
- Atribuudi metaandmed
- Üksuse kinnitamise mallid
- Pakett-töö rakenduse Commerce Data Exchange seansiajaloo kustutamiseks

Peale selle lubatakse Kaubanduse andmebaasi jaoks logimine, mis on seotud maksekaardi tööstusharuga (PCI).

> [!NOTE]
> On võimalus suvandi Kaubanduse andmeedastaja eraldi konfigureerimiseks. See võimalus võimaldab teil suvandi Kaubandus andmeedastaja konfiguratsiooni vaikesätetele lähtestada.

Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad kaubandusandmed. Järgmisena on toodud mõned näited.

- Kaubanduse parameetrid
- Kaubanduse andmeedastaja parameetrid
- Kaubanduse kanalid
- Registrid ja seadmed
- Sortimendid
