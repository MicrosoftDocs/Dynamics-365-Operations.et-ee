---
title: Topeltkirjutuse seadistamine teenuses Lifecycle Services
description: Selles teemas kirjeldatakse, kuidas seadistada topeltkirjutust uue Finance and Operationsi ja uue Dataverse'i keskkonna vahel teenuse Microsoft Dynamics Lifecycle Services (LCS) kaudu.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683520"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Topeltkirjutuse seadistamine teenuses Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

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
        2. Väljal **Saadaolevad keskkonnad** valige oma Finance and Operationsi andmetega integreeritav keskkond. Loend hõlmab kõiki keskkondi, kus teil on administraatori privileegid.
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
8. Kui keskkonna olekuks on **Juurutatud**, avage keskkonna üksikasjade leht. Jaotises **Dataverse'i keskkonna teave** kuvatakse lingitud Finance and Operationsi ja Dataverse'i keskkonna nimed.

    ![Dataverse keskkonna teabe jaotis](../dual-write/media/lcs_setup_3.png)

9. Keskkonna Finance and Operations administraator peab linkimise lõpule viimiseks logima sisse LCS-i ja valima **Lingi CDS rakendustele**. Keskkonna üksikasjade lehel kuvatakse administraatori kontaktteave.

    Kui linkimine on lõpule viidud, uuendatakse olekuks **Keskonna linkimine on edukalt lõpule viidud**.

10. Tööruumi **Andmete integratsioon** avamiseks Finance and Operationsi keskkonnas ja saadaolevate mallide juhtimiseks valige **Lingi CDS rakendustele**.

    ![Nupp Lingi CDS rakendusele keskkonna Dataverse teabe jaotises](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> LCS-i abil ei saa keskkondade linkimist tühistada. Keskkonna linkimise tühistamiseks avage tööruum **Andmete integratsioon** keskkonnas Finance and Operations ja seejärel valige käsk **Tühista linkimine**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]