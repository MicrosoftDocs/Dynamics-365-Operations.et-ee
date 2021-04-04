---
title: Topeltkirjutuse häälestus teenustest Lifecycle Services
description: Selles teemas selgitatakse, kuidas häälestada topeltkirjutuse ühendust teenusest Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6971c8e2d5fa03c2991b9a3054c638cff6322c8b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567716"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Topeltkirjutuse häälestus teenustest Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse, kuidas seadistada topeltkirjutust uue Finance and Operationsi ja uue Dataverse'i keskkonna vahel teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.

## <a name="prerequisites"></a>Eeltingimused

Topeltkirjutuse ühenduse seadistamiseks peate olema administraator.

+ Teil peab olema juurdepääs rentnikule.
+ Peate olema administraator nii Finance and Operationsi kui ka Dataverse'i keskkonnas.

## <a name="set-up-a-dual-write-connection"></a>Topeltkirjutuse ühenduse seadistamine

Topeltkirjutuse ühenduse seadistamiseks tehke järgmist.

1. Avage LCS-is oma projekt.
2. Uue keskkonna juurutamiseks valige **Konfigureeri**.
3. Valige versioon. 
4. Valige topoloogia. Kui saadaval on ainult üks topoloogia, valitakse see automaatselt.
5. Viige lõpule esimesed toimingud viisardis **Juurutussätted**.
6. Vahekaardil **Dataverse** järgige ühte järgnevatest toimingutest.

    - Kui teie rentniku jaoks on Dataverse'i keskkond juba ette valmistatud, saate selle valida.

        1. Määrake suvandi **Dataverse'i konfigureerimine** väärtuseks **Jah**.
        2. Veerus **Saadaolevad keskkonnad** valige oma Finance and Operationsi andmetega integreeritav keskkond. Loend hõlmab kõiki keskkondi, kus teil on administraatori privileegid.
        3. Tingimustega nõustumise näitamiseks märkige ruut **Nõustu**.

        ![Vahekaart Dataverse, kui teie rentniku jaoks on 'Dataversei keskkond juba ette valmistatud](../dual-write/media/lcs_setup_1.png)

    - Kui teie rentnikul ei ole veel Dataverse'i keskkonda, luuakse uus keskkond.

        1. Määrake suvandi **Dataverse'i konfigureerimine** väärtuseks **Jah**.
        2. Sisestage Dataverse'i keskkonnale nimi.
        3. Valige keskkonna juurutamise piirkond.
        4. Valida keskkonna vaikekeel ja -valuuta.

            > [!NOTE]
            > Keelt ja valuutat ei saa hiljem muuta.

        5. Tingimustega nõustumise näitamiseks märkige ruut **Nõustu**.

        ![Vahekaart Dataverse, kui teie rentnikul ei ole veel Dataverse'i keskkonda](../dual-write/media/lcs_setup_2.png)

7. Viige lõpule järelejäänud toimingud viisardis **Juurutussätted**.
8. Kui keskkonna olekuks on **Juurutatud**, avage keskkonna üksikasjade leht. Jaotises **Power Platformi integreerimine** kuvatakse lingitud Finance and Operationsi ja Dataverse’i keskkonna nimed.

    ![Power Platformi integreerimise jaotis](../dual-write/media/lcs_setup_3.png)

9. Keskkonna Finance and Operations administraator peab linkimise lõpule viimiseks logima sisse LCS-i ja valima **Lingi CDS rakendustele**. Keskkonna üksikasjade lehel kuvatakse administraatori kontaktteave.

    Kui linkimine on lõpule viidud, uuendatakse olekuks **Keskonna linkimine on edukalt lõpule viidud**.

10. Tööruumi **Andmete integratsioon** avamiseks Finance and Operationsi keskkonnas ja saadaolevate mallide juhtimiseks valige **Lingi CDS rakendustele**.

    ![Nupp Lingi CDS rakendustele Power Platformi teabe jaotises](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> LCS-i abil ei saa keskkondade linkimist tühistada. Keskkonna linkimise tühistamiseks avage tööruum **Andmete integratsioon** keskkonnas Finance and Operations ja seejärel valige käsk **Tühista linkimine**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]