---
title: Uue toote loomine Commerce'is
description: See artikkel kirjeldab, kuidas luua uut toodet tootes Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 654ba19b0bc96ab40c8c27106fd819faa85a4ce8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270177"
---
# <a name="create-a-new-product-in-commerce"></a>Uue toote loomine Commerce'is


[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas luua uut toodet tootes Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Ülevaade

Toodet defineeritakse peamiselt toote numbri, nime ja kirjeldusega. Kuid toote või teenuse kirjeldamiseks on vaja ka muid andmeid.

## <a name="create-a-new-product"></a>Uue toote loomine

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Tooted kategooriate alusel**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige ripploendist **Toote tüüp** kas **Kaup** või **Teenus**.
1. Valige ripploendist **Toote alatüüp** kas **Toode** (kui tootel pole variante) või **Tooteetalon** (kui tootel on variandid).
1. Sisestage väljale **Tootenumber** tootenumber, kui see ei ole juba eelnevalt täidetud.
1. Sisestage toote nimi väljale **Toote nimi**.
1. Sisestage otsingunimi väljale **Otsingunimi**.
1. Valige ripploendist **Jaemüügi kategooria** sobiv kategooria.
1. Kui toode on komplekt, valige **Jah** väljale **Tootekomplekt**.
1. Kui toote alatüüp on tooteetalon, seadistage **Tootedimensiooni grupp** nii, et see sisaldaks toetatud variante. Valikute hulgas on **Värv**, **Suurus**, **Stiil** ja **Konfiguratsioon**. Vajadusel peate võib-olla looma täiendavaid tootedimensioonide gruppide.
1. Valige ripploendist **Konfiguratsiooni tehnoloogia** sobiv valik.
1. Valige nupp **OK**.

Järgmine pilt näitab näidistoote lisamist.

![Toote loomine.](media/create-new-product.png)

Kui toode on lisatud, saab sellele seadistada täiendavaid andmeid, nagu **Toote kirjeldus**, **Variandigrupid**, **Dimensioonigrupid**, **Toote atribuudid** ja **Seotud tooted**.

Järgmine pilt näitab toote täiendavaid üksikasju.

![Toote üksikasjad.](media/create-new-product-2.png)

### <a name="create-product-variants"></a>Tootevariantide loomine

Kui toote alatüüp on **Tooteetalon**, tuleb luua kindlad variandid. 

Toote variantide loomiseks toimige järgmiselt.

1. Klõpsake toimingupaanil suvandit **Toote variandid**.
1. Kui toimingupaanil on variandi grupid valitud, valige **Variandi soovitused*.
1. Valige variandid, mida soovite toote jaoks toetada.
1. Valige **Loo**.

## <a name="release-a-product"></a>Toote väljastamine

Toote müümiseks tuleb see kõigepealt juriidilisele isikule väljastada.

1. Valige toote lehel **Väljasta tooteid**.

    ![Toote väljastus.](media/create-new-product-3.png)

1. Valige väljastatav toode ja seejärel valige **Edasi**.

    ![Valige väljastatav toode.](media/create-new-product-4.png)

1. Valige väljastatav toote variantide komplekt ja seejärel valige **Edasi**.

    ![Valige väljastatavad variandid.](media/create-new-product-5.png)

1. Valige juriidiline isik ja seejärel valige **Edasi**.

    ![Valige juriidiline isik.](media/create-new-product-6.png)

1. Valige **Lõpeta**.

    ![Toote väljastamise lõpetamine.](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>Väljastatud toote konfigureerimine

Kui toode on vabastatud, siis on vajab see täiendavat konfiguratsiooni, mis sisaldab tootele hinna lisamist.

1. Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Väljastatud tooted kategooria alusel**.
1. Valige väljastatud tootele tootekategooria sõlm ja seejärel valige tooteloendist toode.
1. Valige tegevuspaanil nupp **Redigeeri**.
1. Konfigureerige mistahes vajalikud atribuudid jaotises **Ost**, sh **Ühik**, **Hind** ja **Kogus**.
1. Valige toimingupaanil **Kinnita**, et veenduda, et puuduvatele väljadele ei ole esitatud tõrkeid.
1. Valige toimingupaanil nupp **Salvesta**.

Järgmine pilt näitab väljastatud toote konfiguratsiooni näidet.

![Väljastatud toote konfigureerimine.](media/create-new-product-8.png)

## <a name="additional-resources"></a>Lisaressursid

[Juriidiliste isikute loomine](channels-legal-entities.md)

[Variandigrupi loomine](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
