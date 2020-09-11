---
title: Kaksikkirjutamise seadistuse toetatud stsenaariumid
description: Selle teema all kirjeldatakse stsenaariume, mida toetatakse kaksikkirjutamise seadistuseks.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706248"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Kaksikkirjutamise seadistuse toetatud stsenaariumid

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Saate seadistada kaksikkirjutamise seose Finance and Operations keskkonna ja Common Data Service keskkonna vahel.

+ **Finance and Operationsi keskkond** pakub platvormi **Finance and Operationsi rakendustele** (nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management ja Dynamics 365 Retail).
+ **Common Data Service keskkond** loob aluseks oleva platvormi **mudeljuhitud Dynamics 365 rakenduste** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Finance and Operationsi rakendus Human Resources toetab topeltkirjutuse ühendusi, kuid rakendus Dynamics 365 Human Resources ei luba seda.

Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.

+ Uute Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Microsoft Dynamics Lifecycle Servicesiga (LCS). Kui teil on Microsoft Power Platformi litsents, saate uue Common Data Service'i keskkonna, kui teie rentnikul seda ei ole.
+ Olemasolevate Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Finance and Operations keskkonnas.

Toetatud on järgmised seadistusstsenaariumid:

+ [Uus Finance and Operations rakenduse eksemplar ja uus mudeljuhitud rakenduse eksemplar](#new-new)
+ [Uus Finance and Operations rakenduse eksemplar ja olemasoleva mudeljuhitud rakenduse eksemplar](#new-existing)
+ [Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja uus mudeljuhitud rakenduse eksemplar](#new-demo-new)
+ [Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja olemasolev mudeljuhitud rakenduse eksemplar](#new-demo-existing)
+ [Olemasolev Finance and Operations rakenduse eksemplar ja uus või olemasolev mudeljuhitud rakenduse eksemplar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Uus Finance and Operations rakenduse eksemplar ja uus mudeljuhitud rakenduse eksemplar

Kaksikkirjutamise ühenduse seadmiseks Finance and Operations rakenduse uue eksemplari, millel puuduvad andmed ja uue mudeljuhitud rakenduse eksemplari vahel rakenduses Dynamics 365 järgige [Kaksikkirjutamise seadistuse teenuse Lifecycle Services etappe](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:

- Valmistatakse ette uus tühi Finance and Operations keskkond.
- On ette valmistatud mudeljuhitud rakenduse uus tühi eksemplar, kus on installitud CRM pealahendus.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Üksuse vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Uus Finance and Operations rakenduse eksemplar ja olemasoleva mudeljuhitud rakenduse eksemplar

Kaksikkirjutamise ühenduse seadmiseks Finance and Operations rakenduse uue eksemplari, millel puuduvad andmed ja olemasoleva mudeljuhitud rakenduse eksemplari vahel rakenduses Dynamics 365 järgige [Kaksikkirjutamise seadistuse Lifecycle Servicesi etappe](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:

- Valmistatakse ette uus tühi Finance and Operations keskkond.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Üksuse vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.

1. Looge Finance and Operations rakenduses uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.

Kuna kaksikkirjutamine on reaalajas sünkroonimise režiimis, hakkavad Common Data Service andmed automaatselt liikuma Finance and Operations rakendusse.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja uus mudeljuhitud rakenduse eksemplar

Kaksikkirjutamise seose seadistamiseks Finance and Operations rakenduse uue eksemplari, millel on demoandmed, ja mudeljuhitud rakenduse uus eksemplari vahel rakenduses Dynamics 365 järgige selles teema all varem kirjeldatud etappe jaotises [Uus Finance and Operations rakenduse eksemplar ja uus mudeljuhitud rakenduse eksemplar](#new-new) . Kui ühenduse häälestus on lõpule viidud, kui soovite demoandmeid sünkroonida mudeljuhitud rakendusega, toimige järgmiselt.

1. Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Uus Finance and Operations rakenduse eksemplar, millel on demoandmed, ja olemasolev mudeljuhitud rakenduse eksemplar

Kaksikkirjutamise seose seadistamiseks Finance and Operations rakenduse uue eksemplari, millel on demoandmed, ja mudeljuhitud rakenduse olemasoleva eksemplari vahel rakenduses Dynamics 365 järgige selles teema all varem kirjeldatud etappe jaotises [Uus Finance and Operations rakenduse eksemplar ja olemasolev mudeljuhitud rakenduse eksemplar](#new-existing) . Kui ühenduse häälestus on lõpule viidud, kui soovite demoandmeid sünkroonida mudeljuhitud rakendusega, toimige järgmiselt.

1. Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.

1. Looge Finance and Operations rakenduses uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.

Kuna kaksikkirjutamine on reaalajas sünkroonimise režiimis, hakkavad Common Data Service andmed automaatselt liikuma Finance and Operations rakendusse.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Olemasolev Finance and Operations rakenduse eksemplar ja uus või olemasolev mudeljuhitud rakenduse eksemplar

Olemasoleva Finance and Operations rakenduse eksemplari ja rakenduses Dynamics 365 mudeljuhitud rakenduse uue või olemasoleva eksemplari vahelise ühenduse kaksikkirjutamise seadistus toimub Finants-ja töökeskkonnas.

1. Seadistage ühendus Finance and Operations rakendusest.
2. Olemasolevate Common Data Service andmete Finance and Operations rakendusega sünkroonimiseks rakendage [bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist ettevõtte ISO-koodi.

Kuna kaksikkirjutamine on reaalajas sünkroonimise režiimis, hakkavad Common Data Service andmed automaatselt liikuma Finance and Operations rakendusse.
