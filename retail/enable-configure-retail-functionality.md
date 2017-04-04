---
title: "Uus jaemüügi keskkonnas seemne andmete lähtestamine"
description: "Selles artiklis kirjeldatakse Microsoft Dynamics 365 toiminguteks - jaemüügi initsialiseerimise käigus loodud andmed."
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
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 137c675781cf75d9ce621a84c89224019c161362
ms.lasthandoff: 03/31/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Uus jaemüügi keskkonnas seemne andmete lähtestamine

Selles artiklis kirjeldatakse Microsoft Dynamics 365 toiminguteks - jaemüügi initsialiseerimise käigus loodud andmed.

Pärast Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu lahenduse Jaemüük juurutamist peate lähtestama jaemüügi konfiguratsiooni, et luua põhilised konfigureerimise andmed. **Oluline.** Enne jaemüügi konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te jaemüügikaupluse seadistate. See etapp tuleb läbida iga juriidilise isiku puhul, mida jaemüügiks kasutate. Jaemüügikonfiguratsiooni lähtestamiseks toimige järgmiselt.

1.  Käivitage Dynamics 365 toimingud kliendi jaoks.
2.  Klõpsake **hulgi- ja kaubanduse**&gt;**peakorteri seadistus**&gt;**parameetrid**&gt;**hulgi parameetrid**.
3.  Klõpsake suvandit **Lähtesta**.

Lähtestamine loob järgmised konfiguratsiooni vaikeandmed.

-   Kaupluse andmeedastaja tööd ja alamtööd
-   Jaemüügikanali skeem
-   Jaemüügi jaotusgraafikud
-   Ekraani vaikepaigutused, mis hõlmavad nupupaneele, pilte ja kujundusi
-   Ajavööndi teave
-   Kassa (POS) toimingud
-   Kassaload
-   Kanali aruanded
-   Atribuudi metaandmed
-   Üksuse kinnitamise mallid
-   Pakett-töö rakenduse Commerce Data Exchange seansi ajaloo kustutamiseks

Lisaks sisse, mis on seotud Maksekaartide sektoris (PCI) on lubatud Dynamics 365 operatsioonide andmebaasi. **Märkus.** On võimalus suvandi Kaupluse andmeedastaja eraldi konfigureerimiseks. See võimalus võimaldab teil suvandi Kaupluse andmeedastaja konfiguratsiooni vaikesätetele lähtestada. Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad jaemüügiandmed. Järgmisena on toodud mõned näited.

-   Jaemüügi parameetrid
-   Kaupluse andmeedastaja parameetrid
-   Jaemüügikanalid
-   Registrid ja seadmed
-   Sortimendid



