---
title: Juhised topeltkirjutuse häälestamiseks
description: Selle teema all kirjeldatakse stsenaariume, mida toetatakse kaksikkirjutamise seadistuseks.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 10/12/2020
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
ms.openlocfilehash: 2d77a1458f3f4c79b231e6a6d7cc320b8ee1fad9
ms.sourcegitcommit: ee643d651d57560bccae2f99238faa39881f5c64
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/21/2020
ms.locfileid: "4088502"
---
# <a name="guidance-for-how-to-set-up-dual-write"></a>Juhised topeltkirjutuse häälestamiseks

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Saate seadistada kaksikkirjutamise seose Finance and Operations keskkonna ja Common Data Service keskkonna vahel.

+ **Finance and Operationsi keskkond** pakub platvormi **Finance and Operationsi rakendustele** (nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management ja Dynamics 365 Retail).
+ **Common Data Service'i keskkond** loob aluseks oleva platvormi **rakendustekomplekti Customer Engagement** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Finance and Operationsi rakendus Human Resources toetab topeltkirjutuse ühendusi, kuid rakendus Dynamics 365 Human Resources ei luba seda.

Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.

+ Uute Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Microsoft Dynamics Lifecycle Servicesiga (LCS). Kui teil on Power Platformi litsents, saate uue Common Data Service'i keskkonna, kui teie rentnikul seda ei ole.
+ Olemasolevate Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Finance and Operations keskkonnas.

Enne kui käivitate üksuse topeltkirjutuse, saate käitada algse sünkroonimise, et hallata olemasolevaid andmeid Finance and Operationsi ja Customer Engagementi rakenduste mõlemal poolel. Kui te ei pea nende kahe keskkonna vahel andmeid sünkroonima, saate algse sünkroonimise vahele jätta.

Algse sünkroonimisega saate kopeerida olemasolevad andmed kahesuunaliselt ühest rakendusest teise. Sõltuvalt sellest, millised keskkonnad teil on olemas ja millist tüüpi andmeid on nendes keskkondades, on mitu erinevat seadistuse stsenaariumi.

Toetatud on järgmised seadistusstsenaariumid:

+ [Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#new-new)
+ [Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#new-existing)
+ [Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar](#new-data-new)
+ [Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar](#new-data-existing)
+ [Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#existing-new)
+ [Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar

Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uue eksemplari, millel puuduvad andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:

- Valmistatakse ette uus tühi Finance and Operations keskkond.
- On ette valmistatud Customer Engagementi rakenduse uus tühi eksemplar, kus on installitud CRM-i pealahendus.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Üksuse vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar

Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uude eksemplari, millel puuduvad andmed, ja olemasoleva Customer Engagementi rakenduse eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud:

- Valmistatakse ette uus tühi Finance and Operations keskkond.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Üksuse vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.

1. Looge Finance and Operations rakenduses uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar

Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#new-new) . Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar

Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse olemasoleva eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#new-existing) . Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

Olemasolevate Common Data Service andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.

1. Looge Finance and Operations rakenduses uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar

Olemasoleva Finance and Operationsi rakenduse eksemplari ja uue Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.

1. [Seadistage ühendus Finance and Operationsi rakendusest](enable-dual-write.md).
2. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar

Olemasoleva Finance and Operationsi rakenduse eksemplari ja olemasoleva Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.

1. Seadistage ühendus Finance and Operations rakendusest.
2. Olemasolevate Common Data Service andmete Finance and Operations rakendusega sünkroonimiseks rakendage [bootstrap](bootstrap-company-data.md) Common Data Service andmetele, kasutades kolmetähelist ettevõtte ISO-koodi.
3. Käivitage **Esmase sünkroonimise** funktsionaalsus üksustel, millele soovite andmeid sünkroonida.

Näite ja alternatiivse lähenemise saamiseks vt [Näide](#example).

## <a name="example"></a>Näide

Näite leiate teemast [Klientide lubamine V3 – kontaktide üksuse vastenduse](enable-entity-map.md#example-enabling-the-customers-v3contacts-entity-map)

Alternatiivse lähenemise saamiseks andmemahtude põhjal igas üksuses, millel tuleb käitada esialgne sünkroonimine, vaadake teemat [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).
