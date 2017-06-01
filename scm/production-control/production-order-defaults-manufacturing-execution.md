---
title: "Tootmistellimuse vaikesätted tootmise käivitamisel"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: af6e6db2523041dd8dbcef692c252c596802c22d
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Tootmistellimuse vaikesätted tootmise käivitamisel

[!include[banner](../includes/banner.md)]




Enne kui töötajatele anda võimalus teha tootmistööde registreeringuid, peaksite hoolikalt läbi mõtlema kõik sätted leheküljel **Tootmistellimuse vaikesätted**. Kui teie ettevõte kasutab mitme laoala funktsiooni, võite igale laoalale erinevad tootmistellimuse vaikesätted seadistada. Tellimuse vaikesätete integreerimise tootmise juhtimisega saate seadistada järgmistel vahekaartidel leheküljel **Tootmistellimuse vaikesätted**.

-   **Üldine** – tellimuse tootmistööde üldised vaikesätted tootmise käivitamisel.
-   **Alustamine** – tellimuse tootmistööde või toimingute alustamisel kasutatavad vaikesätted.
-   **Toimingud** – tootmisprotsessi ajal tellimuse tootmistöödele või toimingutele ja tagasisidele rakendatud vaikesätted.
-   **Kinnita lõpetamine** – tellimuse vaikesätted, mida rakendatakse viimases tootmistellimuse toimingus lõpetatuks tunnistatud kaupadest teatamisel.
-   **Koguste kinnitamine** – tootmistellimuste alustamise ja tagasiside koguste kinnitamise vaikesätted.

## <a name="types-of-production-jobs"></a>Tootmistööde tüübid
Tootmistööd, mille puhul on nõutav registreerimine, saate valida leheküljel **Töö registreerimine** vahekaardil **Toimingud**. Tavaliselt teevad töötajad registreeringuid seadistus- ja protsessitööde jaoks. Kui tööde planeerimine on rakendatud, saate siiski tootmistellimuse töötlemisel töötajate registreeritavateks töödeks valida ka muid töö tüüpe, näiteks transporditööd. **Oluline:** kontrollige, et kõik asjakohased töö tüübid oleksid valitud. Muidu ei pruugi tööd leheküljel **Töö registreerimine** registreerimiseks saadaval olla. Joondage oma valikud valikutega, mis on tehtud lehekülje **Protsessigrupid** veerus **Töö haldamine**. Kui protsessigrupis on valitud **Töö haldus**, esitatakse töö tüüp tootmistellimuses lõpetatuks. Selline aruandlus ilmneb, kui töö on tootmise käivitamises lõpetatuks kinnitatud. Kui kõik jaotises **Töö haldus** valitud töö tüübid on toimingu lõpetatuks kinnitanud, kinnitatakse ka tootmise käivitamine lõpetatuks. **Märkus.** Mõned töö tüübid võivad tootmistöölehe kaudu käsitsi märgitud olla. Sellisel juhul valige töö tüübile **Töö haldus**, kuid ärge valige töö tüüpi registreerimiseks lehekülje **Tootmistellimuse vaikesätted** vahekaardil **Toimingud**.

## <a name="bom-consumption-and-picking-list-journals"></a>Koosluse tarbimine ja komplekteerimislehe töölehed
Materjalide tarbimise tootmise ajal saab seadistada kas automaatseks või käsitsi. Automaatset tarbimist juhitakse koosluse ridadel seadistatud automaatse tarbimise põhimõtte ning tootmistellimuse vaikesäte välja **Automaatne koosluse tarbimine** sätete põhjal. Automaatset tarbimist saab seadistada selliselt, et see toimuks tootmisetellimuse alustamisel või lõpetatuks kinnitamisel. Teise võimalusena võib see toimuda töö tasemel, kui tööd alustatakse või lõpetatakse.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Materjali tarbimise juhtimine tootmistellimuse käivitamisel

Materjali tarbimist tootmistellimuse käivitamisel saab juhtida vahekaardi **Alustamine** väljal **Automaatne koosluse tarbimine**. Saadaval on järgmised väärtused:

-   **Automaatse tarbimise põhimõte** – tootmistellimuse käivitamisel määratakse tarbitavate materjalide kogused tootmise koosluse ridade automaatse tarbimise põhimõtete järgi. Tootmise käivitamisel tarbitakse ainult neid koosluse ridu, mille automaatse tarbimise põhimõtteks on seatud **Alustamine**.
-   **Alati** – materjale, mille kogused on proportsionaalsed alustatud kogusega, tarbitakse alati.
-   **Mitte kunagi** – materjalide koguseid ei tarbita kunagi.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Materjali tarbimise juhtimine tootmistöö käivitamisel või lõpetamisel

Materjali tarbimist tootmistöö käivitamisel või lõpetamisel saab juhtida vahekaardi **Toimingud** väljal **Automaatne koosluse tarbimine**. Saadaval on järgmised väärtused:

-   **Automaatse tarbimise põhimõte** – tootmistöö koguse käivitamisel või lõpetamisel määratakse tarbitavate materjalide kogused tootmise koosluse ridade automaatse tarbimise põhimõtete järgi. Tarbitakse ainult neid koosluse ridu, mille automaatse tarbimise põhimõtteks on seatud **Alustamine** või **Valmis**.
-   **Alati** – materjale, mille kogused on proportsionaalsed alustatud töö kogusega, tarbitakse alati.
-   **Mitte kunagi** – materjalide koguseid ei tarbita kunagi.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Materjali tarbimise juhtimine tootmistellimuse lõpetamise kinnitamisel

Materjali tarbimist tootmistellimuse lõpetamise kinnitamisel saab juhtida vahekaardi **Kinnita lõpetamine** väljal **Automaatne koosluse tarbimine**. Saadaval on järgmised väärtused:

-   **Automaatse tarbimise põhimõte** – tootmistellimuse lõpetamise kinnitamisel määratakse tarbitavate materjalide kogused tootmise koosluse ridade automaatse tarbimise põhimõtete järgi. Kasutatakse ainult neid koosluse ridu, mille automaatse tarbimise põhimõtteks on seatud **Valmis**.
-   **Alati** – materjale, mille kogused on proportsionaalsed lõpetamise kinnitamise kogusega, tarbitakse alati.
-   **Mitte kunagi** – materjalide koguseid ei tarbita kunagi.





