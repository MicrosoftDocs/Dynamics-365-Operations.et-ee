---
title: Regulatory Configuration Service (RCS) – RCS-keskkonna kustutamine
description: See teema kirjeldab, kuidas Regulatory Configuration Service (RCS) teenuse süsteemi administraator saab kustutada RCS-keskkonda ja seotud andmeid.
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
ms.openlocfilehash: cf82abbe5493eac9665323738441fa016205e9ef
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355003"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a>Regulatory Configuration Service (RCS) – RCS-keskkonna kustutamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas Regulatory Configuration Service (RCS) teenuse süsteemi administraator saab kustutada RCS-keskkonda ja seotud andmeid.

Enne selles teemas kirjeldatud protseduuri lõpetamist peavad täidetud olema järgmised eeltingimused:

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
