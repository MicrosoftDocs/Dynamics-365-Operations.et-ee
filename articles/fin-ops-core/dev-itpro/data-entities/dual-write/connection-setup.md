---
title: Topeltkirjutuse häälestamise juhend
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
ms.openlocfilehash: 78a7cdc18476a1c523c83c92ca6f354c3ba806dc
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744849"
---
# <a name="guidance-for-dual-write-setup"></a>Topeltkirjutuse häälestamise juhend

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Saate seadistada kaksikkirjutamise seose Finance and Operations keskkonna ja Dataverse keskkonna vahel.

+ **Finance and Operations keskkond** pakub platvormi **Finance and Operations rakendustele** (nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources).
+ **Teenuse Dataverse keskkond** loob aluseks oleva platvormi **klientide kaasamise rakenduste** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Dynamics 365 Financei inimressursside moodul toetab topeltkirjutuse ühendusi, kuid rakendus Dynamics 365 Human Resources ei luba seda.

Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.

+ Uute Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Microsoft Dynamics Lifecycle Servicesiga (LCS). Kui teil on Microsoft Power Platformi litsents, saate uue Dataverse'i keskkonna, kui teie rentnikul seda ei ole.
+ Olemasolevate Finance and Operations rakenduste puhul algab kaksikkirjutamise ühenduse seadistus Finance and Operations keskkonnas.

Enne kui käivitate üksuse topeltkirjutuse, saate käitada algse sünkroonimise, et hallata olemasolevaid andmeid mõlemal poolel: Finance and Operationsi rakendustes ja Customer Engagementi rakendustes. Kui te ei pea nende kahe keskkonna vahel andmeid sünkroonima, saate algse sünkroonimise vahele jätta.

Algse sünkroonimisega saate kopeerida olemasolevad andmed kahesuunaliselt ühest rakendusest teise. Sõltuvalt sellest, millised keskkonnad teil on olemas ja millist tüüpi andmeid on nendes olemas, on mitu seadistuse stsenaariumi.

Toetatud on järgmised seadistusstsenaariumid:

+ [Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#new-new)
+ [Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#new-existing)
+ [Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar](#new-data-new)
+ [Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar](#new-data-existing)
+ [Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#existing-new)
+ [Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar

Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uue eksemplari, millel puuduvad andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- Valmistatakse ette uus tühi Finance and Operations keskkond.
- On ette valmistatud Customer Engagementi rakenduse uus tühi eksemplar, kus on installitud CRM-i pealahendus.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar

Topeltkirjutuse ühenduse seadmiseks Finance and Operationsi rakenduse uude eksemplari, millel puuduvad andmed, ja olemasoleva Customer Engagementi rakenduse eksemplari vahel, järgige etappe jaotises [Topeltkirjutuse seadistus teenuses Lifecycle Services](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- Valmistatakse ette uus tühi Finance and Operations keskkond.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

Olemasolevate Dataverse andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.

1. Looge Finance and Operations rakenduses uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake selles teemas hiljem jaotist [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja uus Customer Engagementi rakenduse eksemplar

Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse uue eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar](#new-new) . Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Uus Finance and Operationsi rakenduse eksemplar, millel on andmed, ja olemasolev Customer Engagementi rakenduse eksemplar

Topeltkirjutuse seose seadistamiseks Finance and Operationsi rakenduse uue eksemplari, millel on andmed, ja Customer Engagementi rakenduse olemasoleva eksemplari vahel, järgige selle teema all varem kirjeldatud etappe jaotises [Uus Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar](#new-existing) . Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage Finance and Operations rakendus LCS lehelt, logige sisse ja seejärel avage **Andmehaldus \> Kaksikkirjutamine**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Olemasolevate Dataverse andmete sünkroonimiseks Finance and Operations rakendusega toimige järgmiselt.

1. Looge Finance and Operations rakenduses uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Olemasolev Finance and Operationsi rakenduse eksemplar ja uus Customer Engagementi rakenduse eksemplar

Olemasoleva Finance and Operationsi rakenduse eksemplari ja uue Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.

1. [Seadistage ühendus Finance and Operationsi rakendusest](enable-dual-write.md).
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev Customer Engagementi rakenduse eksemplar

Olemasoleva Finance and Operationsi rakenduse eksemplari ja olemasoleva Customer Engagementi rakenduse eksemplari vahelise ühenduse topeltkirjutuse seadistus toimub keskkonnas Finance and Operation.

1. [Seadistage ühendus Finance and Operationsi rakendusest](enable-dual-write.md).
2. Olemasolevate Dataverse andmete Finance and Operations rakendusega sünkroonimiseks rakendage [bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist ettevõtte ISO-koodi.
3. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="example"></a>Näide

Näite leiate teemast [Klientide lubamine V3 – kontaktide tabeli vastendus](enable-entity-map.md#enable-table-map)

Alternatiivse lähenemise saamiseks, mis põhineb igas üksuse andmemahtudel, millel tuleb käitada esialgne sünkroonimine, vaadake teemat [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]