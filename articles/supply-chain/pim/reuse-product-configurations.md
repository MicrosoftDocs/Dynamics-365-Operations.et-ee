---
title: Tootekonfiguratsioonide taaskasutamine
description: Soovi korral saate määrata toote olemasoleva konfiguratsiooni automaatse taaskasutamise. Seejärel, kui kasutaja on konfiguratsiooniseansi lõpule viinud, kontrollib süsteem, kas kasutaja valikule vastav konfiguratsioon on juba olemas. Vastava konfiguratsiooni leidmisel kasutatakse konfiguratsiooni ID-d, vastavat kooslust ja protsessi uuesti.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb4c997e8cf8b2456ffe12a552577902da171cc1
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189840"
---
# <a name="reuse-product-configurations"></a>Tootekonfiguratsioonide taaskasutamine

[!include [banner](../includes/banner.md)]

Soovi korral saate määrata toote olemasoleva konfiguratsiooni automaatse taaskasutamise. Seejärel, kui kasutaja on konfiguratsiooniseansi lõpule viinud, kontrollib süsteem, kas kasutaja valikule vastav konfiguratsioon on juba olemas. Vastava konfiguratsiooni leidmisel kasutatakse konfiguratsiooni ID-d, vastavat kooslust ja protsessi uuesti.

## <a name="requirements-for-reusing-configurations"></a>Konfiguratsioonide taaskasutuse nõuded

Konfiguratsioonide taaskasutamise lubamiseks peate määrama lehel **Tootekonfiguratsiooni mudeli üksikasjad** komponentidele ja atribuutidele järgmise teabe.

-   **Komponendid ja alamkomponendid** – valige kiirkaardi **Üldine** väljal **Taaskasuta konfiguratsioone** suvand **Jah**.
-   **Atribuudid** – valige kiirkaardil **Atribuudid** suvand **Lisa taaskasutusse**. See suvand kuvatakse ainult siis, kui seotud komponendi taaskasutamine on lubatud. Kui te ei vali taaskasutamiseks ühtki atribuuti, kasutatakse konfiguratsiooni alati uuesti, olenemata kasutaja valikutest konfigureerimisseansi ajal. Olemasoleva konfiguratsiooni atribuutide väärtused peavad ühtima kasutaja valikutega. Näiteks kui kasutaja valib konfiguratsiooniseansi ajal värviks **Sinine**, kontrollib süsteem, kas komponendi olemasolevas konfiguratsioonis on värv sinine.

## <a name="resetting-configuration-reuse"></a>Konfiguratsiooni taaskasutuse lähestamine
Konfiguratsiooni taaskasutuse lähtestamisel ei võeta varem loodud konfiguratsioone arvesse. Soovi korral saate konfiguratsiooni taaskasutuse lähtestada, kui kooslust või protsessi on muudetud, kuid seotud atribuute mitte. Saate lähtestada konfiguratsiooni taaskasutuse komponendi kiirkaardil **Üldine**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]