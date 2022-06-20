---
title: Dynamics 365 Commerce’i hinnakujunduse mootori kasutamine koos rakendusega Dynamics 365 Sales
description: See artikkel kirjeldab, kuidas kasutada Microsoft Dynamics 365 Commerce hinnakujundusmootorit müügipakkumiste loomiseks Dynamics 365 müügis.
author: ShalabhjainMSFT
ms.date: 11/19/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 11a164ec15c8b7a69172a153b961011a8b324712
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881390"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a>Dynamics 365 Commerce’i hinnakujunduse mootori kasutamine koos rakendusega Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas kasutada Microsoft Dynamics 365 Commerce hinnakujundusmootorit müügipakkumiste loomiseks Dynamics 365 müügis.

Dynamics 365 Commerce’i hinnakujunduse mootor toetab enamikke ettevõtja ja tarbija vahelisi (B2C) hinnakujunduse stsenaariume, nagu kaupluse tasemel hinnakujundus, alluvusepõhine ja püsikliendipõhine hinnakujundus, sobitamise allahindlused, koguse allahindlused ja läveallahindlused. Hinnakujunduse mootor kasutab keerukaid reegleid antud pakkumisele või tellimusele parima hinna määramiseks.

Kui kasutate [topeltkirjutamist](./dual-write-overview.md), on teil oma hinnakujunduse vajaduste jaoks kolm võimalust. Saate kasutada staatilist hinnakujundust, mis pärineb rakenduse Dynamics 365 Sales hindade loendist, rakenduse Dynamics 365 Supply Chain Management hinnakujunduse mootorist või rakenduse Dynamics 365 Commerce hinnakujunduse mootorist. Nende valikute hulgas sobib Commerce’i hinnakujunduse mootor kõige paremini B2C stsenaariumiga.

## <a name="use-the-commerce-pricing-engine-in-sales"></a>Salesis Commerce’i hinnakujunduse mootori kasutamine

> [!NOTE]
> Praegu saab Commerce’i hinnakujunduse mootorit kasutada ainult Salesis pakkumise loomisel. Müügitellimuse integratsioon Commerce’i hinnakujunduse mootoriga pole veel saadaval.

Kui kasutajad teevad Salesis müügipakkumisega algust, kopeerib topeltkirjutamise raamistik hinnapakkumise üksikasjad Commerce’i. Mis tahes olemasoleva pakkumise ridade muudatused või mis tahes uuena lisatud pakkumise read kopeeritakse Salesist Commerce’i. Kui kasutajad soovivad kasutada hinnapakkumise hinna määramiseks Commerce’i hinnakujunduse mootorit, saavad nad pakkumise hindade värskendamiseks valida suvandi **Hinnapakkumine**, mis põhinev Commerce’i hinnakujunduse mootoril. Hinnad uuendatakse seejärel automaatselt nii Salesis kui ka Commerce’is.

## <a name="prerequisites"></a>Eeltingimused

- Enne kui saate kasutada Salesis Commerce’i hinnakujunduse mootorit, peate järgima samme teemas [Potentsiaalne kliendist rahaks kaksikkirjutamises](./dual-write-prospect-to-cash.md).
- Peate käsitsi sisestamiseks hindamise kaubandusleppe välja lülitama, järgides järgmisi samme.

    1. Avage Commerce’i keskkonnas jaotis **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.
    1. Tühjendage vahekaardil **Hinnad** kiirkaardil **Kaubanduskokkuleppe hindamine** märkeruut **Käsitsi sisestamine**.

## <a name="additional-resources"></a>Lisaressursid

[Potentsiaalne klient-raha ja kaksikkirjutamine](./dual-write-prospect-to-cash.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]