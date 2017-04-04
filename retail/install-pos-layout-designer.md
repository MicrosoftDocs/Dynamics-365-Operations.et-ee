---
title: "Jaemüügikassa paigutuse kujundaja installimine"
description: "Saate kasutada ühe klõpsuga kujundajat, et kujundada kaupluste, registrite, kassapidajate ja juhatajate jaoks režiimis Horisontaalne või režiimis Vertikaalne erinevaid uudse jaemüügikassa (MPOS) ja pilve kassa paigutusi."
author: MargoC
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: RetailTillLayout
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 219684
ms.assetid: 2e2c4eea-c6e2-4912-9832-a6b22416e39f
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b33cbf67c00b6baea4393e82d19300085781af29
ms.lasthandoff: 03/31/2017


---

# <a name="install-the-retail-pos-layout-designer"></a>Jaemüügikassa paigutuse kujundaja installimine

Saate kasutada ühe klõpsuga kujundajat, et kujundada kaupluste, registrite, kassapidajate ja juhatajate jaoks režiimis Horisontaalne või režiimis Vertikaalne erinevaid uudse jaemüügikassa (MPOS) ja pilve kassa paigutusi.

Tänapäevase jamüügikassa (MPOS) või pilve kassa graafilist kujundust juhib kassa paigutus. Paigutus juhib erinevate objektide asukohta. Näited hõlmavad kogupaigutust, kaubavõrgustiku paigutust, kliendi paigutust, makse paigutust ja erinevate menüünuppude paigutust. Paigutused hõlmavad ka töötajatele esitatava müügiliidese üldist ilmet.

## <a name="install-the-oneclick-designer"></a>Paigaldada oneclick disainer
1.  Microsoft Dynamics 365 operatsioonide menüü vasakus ülanurgas navigeerimiseks kasutage **jaemüügi****ja**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS**&gt;**ekraani paigutusega**.
2.  Valige mis tahes paigutus, millel on rakenduse tüüp **Modern POS Windowsi jaoks** või **Pilve POS** ja klõpsake seejärel valikut **Paigutusekujundaja**.
3.  Ühe klõpsuga kujundaja installi käitamiseks klõpsake Internet Exploreri akna alumisse ossa ilmuval teavitusribal käsku **Ava**. (Teistes brauserites võib teavitusriba ilmuda kusagile mujale.)
4.  Ilmuvas teateaknas **Rakenduse käivitamine - turbehoiatus** klõpsake valikut **Käivita**, et installida jaemüügikujundaja host. Installi edenemist näitab edenemisnäidik.
5.  Pärast installi lõpetamist sisestage lehele **Sisselogimine** kujundaja käivitamiseks oma Microsoft 365 for Operationsi kasutajanimi ja parool ning klõpsake seejärel valikut **Sisselogimine**.
6.  Pärast mandaatide kinnitamist ja kujundaja käivitamist saate kujundada oma enda paigutuse või muuta olemasolevat paigutust. [![Üks klõps kujundaja paigutus](./media/screenlayoutdesign_mposdownload-1024x664.png)](./media/screenlayoutdesign_mposdownload.png)

## <a name="troubleshoot-the-installation-of-the-layout-designer"></a>Paigutusekujundaja installimise tõrkeotsing
-   Kui klõpsate valikut **Kujundaja**, ei ilmu allalaadimiseks (või käivitamiseks) installiprogrammi või teie praegused turbesätted ei võimalda teil faili alla laadida. **Lahendused**
    -   Internet Exploreris veenduge, et hüpikakna blokeerija on selle tegevuskoha jaoks keelatud. Klõpsake **sätted**&gt;**Valikud**&gt;**Privaatsus**&gt;**Leia hüpikakende blokeerija**, ja muutke, kui muudatus on vajalik.
    -   Internet Exploreris lisage rakenduse usaldusväärsetele saitidele rakendus Dynamics 365 for Operations. Klõpsake **sätted**&gt;**Valikud**&gt;**turvalisuse**&gt;**usaldusväärsed saidid**&gt;**saidid**&gt;**lisa**.
-   Programm ei käivitu ja teil palutakse hankijaga ühendust võtta. **Lahendus:** Internet Exploreris lisage rakenduse usaldusväärsetele saitidele rakendus Dynamics 365 for Operations. Klõpsake **sätte**&gt;**Valikud**&gt;**turvalisuse**&gt;**usaldusväärsed saidid**&gt;**saidid**&gt;**lisa**.

**Teadaolev probleem:** kujundaja ei tööta õigesti brauserites Google Chrome ja Mozilla Firefox. Töötame selle probleemi lahendamiseks.

<a name="see-also"></a>Vt ka
--------

[Tänapäevase jaemüügikassa konfigureerimine, allalaadimine, installimine ja aktiveerimine](retail-modern-pos-device-activation.md)


