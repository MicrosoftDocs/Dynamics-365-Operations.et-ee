---
title: Dynamics 365 Commerce’i hinnakujunduse mootori kasutamine koos rakendusega Dynamics 365 Sales
description: Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 Commerce’i hinnakujunduse mootorit rakenduses Dynamics 365 Sales müügipakkumiste loomiseks.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594914"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce’i hinnakujunduse mootori kasutamine koos rakendusega Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 Commerce’i hinnakujunduse mootorit rakenduses Dynamics 365 Sales müügipakkumiste loomiseks.

Dynamics 365 Commerce’i hinnakujunduse mootor toetab enamikke ettevõtja ja tarbija vahelisi (B2C) hinnakujunduse stsenaariume, nagu kaupluse tasemel hinnakujundus, alluvusepõhine ja püsikliendipõhine hinnakujundus, sobitamise allahindlused, koguse allahindlused ja läveallahindlused. Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks.

Kui kasutate [topeltkirjutamist](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), on teil oma hinnakujunduse vajaduste jaoks kolm võimalust. Saate kasutada staatilist hinnakujundust, mis pärineb rakenduse Dynamics 365 Sales hindade loendist, rakenduse Dynamics 365 Supply Chain Management hinnakujunduse mootorist või rakenduse Dynamics 365 Commerce hinnakujunduse mootorist. Nende valikute hulgas sobib Commerce’i hinnakujunduse mootor kõige paremini B2C stsenaariumiga.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Salesis Commerce’i hinnakujunduse mootori kasutamine

> [!NOTE]
> Praegu saab Commerce’i hinnakujunduse mootorit kasutada ainult Salesis pakkumise loomisel. Müügitellimuse integratsioon Commerce’i hinnakujunduse mootoriga pole veel saadaval.

Kui kasutajad teevad Salesis müügipakkumisega algust, kopeerib topeltkirjutamise raamistik hinnapakkumise üksikasjad Commerce’i. Mis tahes olemasoleva pakkumise ridade muudatused või mis tahes uuena lisatud pakkumise read kopeeritakse Salesist Commerce’i. Kui kasutajad soovivad kasutada hinnapakkumise hinna määramiseks Commerce’i hinnakujunduse mootorit, saavad nad pakkumise hindade värskendamiseks valida suvandi **Hinnapakkumine**, mis põhinev Commerce’i hinnakujunduse mootoril. Hinnad uuendatakse seejärel automaatselt nii Salesis kui ka Commerce’is.

## <a name="prerequisites"></a>Eeltingimused

- Enne kui saate kasutada Salesis Commerce’i hinnakujunduse mootorit, peate järgima samme teemas [Potentsiaalne kliendist rahaks kaksikkirjutamises](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).
- Peate käsitsi sisestamiseks hindamise kaubandusleppe välja lülitama, järgides järgmisi samme.

    1. Avage Commerce’i keskkonnas jaotis **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
    1. Tühjendage vahekaardil **Hinnad** kiirkaardil **Kaubanduskokkuleppe hindamine** märkeruut **Käsitsi sisestamine**.

## <a name="additional-resources"></a>Lisaressursid

[Potentsiaalne klient-raha ja kaksikkirjutamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)
