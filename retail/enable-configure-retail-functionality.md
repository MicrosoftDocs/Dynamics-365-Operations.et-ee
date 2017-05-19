---
title: "Algandmete lähtestamine uues jaemüügikeskkonnas"
description: "See artikkel kirjeldab andmeid, mis luuakse Microsoft Dynamics 365 for Operationsi jaemüügimooduli lähtestamisprotsessi käigus."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 49621
ms.assetid: 4dc762eb-190e-4485-8f55-b0cafc81bc37
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: b5290bb62ab8ad71b06b0478ccaf6dbb61454170
ms.contentlocale: et-ee
ms.lasthandoff: 04/26/2017


---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Algandmete lähtestamine uues jaemüügikeskkonnas

[!include[banner](includes/banner.md)]


See artikkel kirjeldab andmeid, mis luuakse Microsoft Dynamics 365 for Operationsi jaemüügimooduli lähtestamisprotsessi käigus.

Pärast Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu lahenduse Jaemüük juurutamist peate lähtestama jaemüügi konfiguratsiooni, et luua põhilised konfigureerimise andmed. **Oluline.** Enne jaemüügi konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te jaemüügikaupluse seadistate. See etapp tuleb läbida iga juriidilise isiku puhul, mida jaemüügiks kasutate. Jaemüügikonfiguratsiooni lähtestamiseks toimige järgmiselt.

1.  Käivitage Dynamics 365 for Operationsi klient.
2.  Klõpsake valikuid **Jaemüük ja kaubandus** &gt; **Peakontori seadistamine** &gt; **Parameetrid** &gt; **Jaemüügi parameetrid**.
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

Lisaks lubatakse Dynamics Dynamics 365 for Operationsi andmebaasi jaoks logimine, mis on seotud maksekaardi tööstusharuga (PCI). **Märkus.** On võimalus suvandi Kaupluse andmeedastaja eraldi konfigureerimiseks. See võimalus võimaldab teil suvandi Kaupluse andmeedastaja konfiguratsiooni vaikesätetele lähtestada. Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad jaemüügiandmed. Järgmisena on toodud mõned näited.

-   Jaemüügi parameetrid
-   Kaupluse andmeedastaja parameetrid
-   Jaemüügikanalid
-   Registrid ja seadmed
-   Sortimendid





