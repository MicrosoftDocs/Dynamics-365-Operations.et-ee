---
title: "Algandmete lähtestamine uues jaemüügikeskkonnas"
description: "See artikkel kirjeldab andmeid, mis luuakse Microsoft Dynamics 365 for Retaili jaemüügimooduli lähtestamisprotsessi käigus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ac4f651cd7e5df912ea2535eafd5e54c11377253
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="initialize-seed-data-in-a-new-retail-environment"></a>Algandmete lähtestamine uues jaemüügikeskkonnas

[!include[banner](includes/banner.md)]


See artikkel kirjeldab andmeid, mis luuakse Microsoft Dynamics 365 for Retaili jaemüügimooduli lähtestamisprotsessi käigus.

Pärast Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu lahenduse Jaemüük juurutamist peate lähtestama jaemüügi konfiguratsiooni, et luua põhilised konfigureerimise andmed. **Oluline.** Enne jaemüügi konfiguratsiooni lähtestamist veenduge, et olete määranud keele ja postiaadressi igale juriidilisele isikule, kus te jaemüügikaupluse seadistate. See etapp tuleb läbida iga juriidilise isiku puhul, mida jaemüügiks kasutate. Jaemüügikonfiguratsiooni lähtestamiseks toimige järgmiselt.

1.  Käivitage Dynamics 365 for Retaili klient.
2.  Klõpsake valikuid **Jaemüük** &gt; **Peakontori seadistamine** &gt; **Parameetrid** &gt; **Jaemüügi parameetrid**.
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

Lisaks lubatakse Dynamics 365 for Retaili andmebaasi jaoks logimine, mis on seotud maksekaardi tööstusharuga (PCI). **Märkus.** On võimalus suvandi Kaupluse andmeedastaja eraldi konfigureerimiseks. See võimalus võimaldab teil suvandi Kaupluse andmeedastaja konfiguratsiooni vaikesätetele lähtestada. Pärast lähtestamise lõpule viimist peate konfigureerima täiendavad jaemüügiandmed. Järgmisena on toodud mõned näited.

-   Jaemüügi parameetrid
-   Kaupluse andmeedastaja parameetrid
-   Jaemüügikanalid
-   Registrid ja seadmed
-   Sortimendid





