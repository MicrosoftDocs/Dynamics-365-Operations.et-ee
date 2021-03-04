---
title: Laorakenduse sündmused
description: Selles teemas kirjeldatakse laorakenduse sündmusetöötlust, mida kasutatakse pakett-töö osana laorakenduse sündmuseteadete töötlemiseks.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileDeviceQueueEvent
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 210008c4a1366773f465c59b38eca30f11f0b38c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426119"
---
# <a name="warehouse-app-event-processing"></a>Laorakenduse sündmusetöötlus

[!include [banner](../includes/banner.md)]

Rakenduses Supply Chain Management töötavad pakett-tööd saavad kasutada laorakenduse sündmuste töötlemise järjekorrast pärit andmeid, et reageerida äramärgitud sündmustele nii, nagu vaja. See funktsioon lisab järjekorda asjakohased sündmused, reageerimaks kindlat tüüpi tegevustele, mida rakendust kasutavad töötajad teevad. Näide on see, kui funktsiooni **Üleviimistellimuste loomine ja töötlemine laorakenduses** kasutamisel luuakse ja värskendatakse üleviimistellimuse päist ja ridu peidetult ajal, mil süsteem käitab pakett-tööd **Laorakenduse sündmuste töötlemine**.

## <a name="enable-the-process-warehouse-app-events-feature"></a>Laorakenduse sündmuste töötlemise funktsiooni lubamine

Enne selle funktsiooni kasutamist tuleb see teie süsteemis lubada. Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada. Laorakenduse sündmuste töötlemise funktsioon on loetletud järgmiselt.

- **Moodul** – laohaldus
- **Funktsiooni nimi** – laorakenduse sündmuste töötlemine

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Pakett-töö seadistamine laorakenduse sündmuste töötlemiseks

### <a name="process-warehouse-app-events"></a>Laorakenduse sündmuste töötlemine

Seadistage ajastatud pakett-töö laorakenduse sündmuste töötlemiseks üleviimistellimuse loomise ja reavärskenduste jaoks.

1. Avage **Laohaldus \> Perioodilised ülesanded \> Laorakenduse sündmuste töötlemine**.
1. Avaneb laorakenduse sündmuste töötlemise dialoogiboks. Laiendage kiirkaart **Käivita taustal** ja seadke suvandi **Pakktöötlus** väärtuseks **Jah**.
1. Valige kiirkaardil **Käivita taustal** suvand **Kordumine**.
1. Avaneb dialoogiboks **Kordumise määratlemine**. Seadistage käivitusgraafik oma ettevõtte vajaduste järgi.
1. Valige **OK**, et naasta dialoogiboksi **Laorakenduse sündmuste töötlemine**.
1. Valige **OK** dialoogiboksis **Laorakenduse sündmuste töötlemine**, et lisada pakett-töö pakktöötluse järjekorda.

## <a name="query-warehouse-app-events"></a>Laorakenduse sündmuste pärimine

Saate vaadata sündmuste järjekorda ja laorakenduse loodud sündmuseteateid, avades **Laohaldus \> Päringud ja aruanded \> Mobiilse seadme logid \> Laorakenduse sündmused**.

## <a name="the-standard-event-queue-process"></a>Standardne sündmuste järjekorra protsess

Laorakenduse sündmuste järjekorda kasutatakse tavaliselt järgmises kirjeldatud voos.

1. Sündmus lisatakse järjekorda koos sündmuseteatega. Uue teate olek on esialgu **Ootel**, mis tähendab, et pakett-töö **Laorakenduse sündmuste töötlemine** ei võta teadet vastu ega töötle seda.
1. Niipea, kui teate olekuks määratakse **Järjekorras**, võtab pakett-töö **Laorakenduse töötlemine** sündmuse ette ja töötleb seda.
1. Pakett-töö määrab sündmuse olekuks kas **Lõpetatud** või **Nurjus** sõltuvalt sellest, kas soovitud protsess oli võimalik.
1. Kui kõik seotud sündmuseteated on **lõpetatud**, kustutatakse sündmus järjekorrast.

 Üksikasjaliku näite leiate teemast [Protsess „Üleviimistellimuse loomine laorakenduses”](create-transfer-order-from-warehouse-app.md).

## <a name="handle-event-errors"></a>Sündmusetõrgete käsitlemine

Laosündmuse töötlemise osana ei saa taotletud teate tegevus pakett-tööst protsesse vastu võtta. Sellisel juhul määratakse sündmusteate olekuks **Nurjus**. Saate kasutada **pakett-töö logi** teavet, et saada teada põhjused ja parandada võimalikud probleemid.

Üksikasjaliku näite leiate teemast [Üleviimistellimuse loomine laorakenduses](create-transfer-order-from-warehouse-app.md).

Laorakenduse nurjunud sündmuseteate lähtestamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Päringud ja aruanded \> Mobiilse seadme logid \> Laorakenduse sündmused**.
1. Otsige üles ja valige kiirkaardil **Laorakenduse sündmusteated** asjakohane sündmus, mille olek veerus **Sündmuse olek** on **Nurjus**.
1. Valige lehe **Laorakenduse sündmuseteated** tööriistaribalt suvand **Lähtesta**.
1. Jätkake tööd seni, kuni kõik asjakohased teated on lähtestatud.

Saate samuti eemaldada **nurjunud** sündmuseteate, kasutades lehe **Laorakenduse sündmusteated** tööriistaribal suvandit **Kustuta**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]