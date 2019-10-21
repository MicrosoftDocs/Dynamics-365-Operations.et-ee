---
title: Algandmete lähtestamine uutes Retaili keskkondades
description: See artikkel kirjeldab andmeid, mis luuakse Dynamics 365 Retaili jaemüügimooduli lähtestamisprotsessi käigus.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 49b21d81437ebd7cc55076444ee71ae1143bfac0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025512"
---
# <a name="initialize-seed-data-in-new-retail-environments"></a>Algandmete lähtestamine uutes Retaili keskkondades

[!include [banner](includes/banner.md)]

See artikkel kirjeldab andmeid, mis luuakse Dynamics 365 Retaili jaemüügimooduli lähtestamisprotsessi käigus.

Pärast teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu lahenduse Jaemüük juurutamist peate lähtestama jaemüügi konfiguratsiooni, et luua põhilised konfigureerimise andmed.

> [!IMPORTANT]
> Enne jaemüügi konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te jaemüügikaupluse seadistate. See etapp tuleb läbida iga juriidilise isiku puhul, mida jaemüügiks kasutate.

Jaemüügikonfiguratsiooni lähtestamiseks toimige järgmiselt.

1. Käivitage rakenduse Retail klient.
2. Klõpsake valikuid **Jaemüük** &gt; **Peakontori seadistamine** &gt; **Parameetrid** &gt; **Jaemüügi parameetrid**.
3. Klõpsake suvandit **Lähtesta**.

Lähtestamine loob järgmised konfiguratsiooni vaikeandmed.

- Kaupluse andmeedastaja tööd ja alamtööd
- Jaemüügikanali skeem
- Jaemüügi jaotusgraafikud
- Ekraani vaikepaigutused, mis hõlmavad nupupaneele, pilte ja kujundusi
- Ajavööndi teave
- Kassa (POS) toimingud
- Kassaload
- Kanali aruanded
- Atribuudi metaandmed
- Üksuse kinnitamise mallid
- Pakett-töö rakenduse Commerce Data Exchange seansiajaloo kustutamiseks

Peale selle lubatakse Retaili andmebaasi jaoks logimine, mis on seotud maksekaardi tööstusharuga (PCI).

> [!NOTE]
> On võimalus suvandi Kaupluse andmeedastaja eraldi konfigureerimiseks. See võimalus võimaldab teil suvandi Kaupluse andmeedastaja konfiguratsiooni vaikesätetele lähtestada.

Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad jaemüügiandmed. Järgmisena on toodud mõned näited.

- Jaemüügi parameetrid
- Kaupluse andmeedastaja parameetrid
- Jaemüügikanalid
- Registrid ja seadmed
- Sortimendid
