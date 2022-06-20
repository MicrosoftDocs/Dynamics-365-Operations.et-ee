---
title: Regulatory Configuration Service (RCS) – RCS-keskkonna kustutamine
description: See artikkel selgitab, kuidas regulatiivse konfiguratsiooniteenuse (RCS) süsteemi administraator saab kustutada RCS-keskkonna ja seotud andmed.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 21e7ee546bb2b712d9424c6bd95e9f9227831bd1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908886"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – RCS-keskkonna kustutamine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas regulatiivse konfiguratsiooniteenuse (RCS) süsteemi administraator saab kustutada RCS-keskkonna ja seotud andmed.

Enne selle artikli protseduuri lõpule viimist peavad olema täidetud järgmised eeltingimused:

- Teile peab RCS-keskkonnas olema määratud **Süsteemiadministraatori** roll.
- **Süsteemiadministraatori** rollile peab olema määratud **RCSDeleteEnvironmentDuty** roll.

## <a name="delete-an-rcs-environment"></a>RCS keskkonna kustutamine

1. Avage RCS ja valige **Elektroonilise aruandluse** tööruumi paan.
2. Jaotises **Seotud lingid** valige suvand **Kustuta RCS-keskkond**.

    ![Kustutage RCS-i keskkonna link jaotisest Seotud lingid.](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. Kuvatavas dialoogiboksis vaadake üle sõnumid keskkonna kustutamise ulatuse kohta.

    ![Teated dialoogiaknas RCS keskkonna kustutamine.](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > RCS-keskkonna kustutamist ei saa tühistada.
    >
    > Toiming kustutab valitud RCS-keskkonna ja kõik seostuvad andmed, sh globaalsesse hoidlasse talletatud funktsioonid ja konfiguratsioonid. Muude organisatsioonidega ühiskasutuses kasutatavad funktsioonid ja konfiguratsioonid sõltuvuste puudumusel lõpetatakse ja kustutatakse. Sõltuvusi omavad funktsioonid ja konfiguratsioonid märgitakse kui katkestatud.

4. Sisestage esitatud väljale RCS-keskkonna globaalselt kordumatu identifikaator (GUID) kinnitamaks soovi kustutada. Keskkonna GUID on kustutamise teates.
5. Valige nupp **Kustuta keskkond**.
    
Teie RCS-keskkond ja kõik seotud andmed on nüüd kustutatud.

> [!IMPORTANT]
> Pärast RCS-keskkonna kustutamist pole võimalik andmeid taastada. Uue RCS-keskkonna saab luua mis tahes saadaolevas RCS-regioonis.
