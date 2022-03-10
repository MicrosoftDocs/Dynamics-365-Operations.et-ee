---
title: Topeltkirjutuse häälestamise juhend
description: Selle teema all kirjeldatakse stsenaariume, mida toetatakse kaksikkirjutamise seadistuseks.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6de449b14bcdd82336e3e255bf62ad069d3daaf5
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061600"
---
# <a name="guidance-for-dual-write-setup"></a>Topeltkirjutuse häälestamise juhend

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Saate seadistada topeltkirjutusühenduse finants- ja operatsioonide keskkonna ning Dataverse keskkonna vahel.

+ **Finants- ja operatsioonide keskkond** pakub finance and Operationsi rakenduste **aluseks olevat platvormi**(nt Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Human Resources).
+ **Teenuse Dataverse keskkond** loob aluseks oleva platvormi **klientide kaasamise rakenduste** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Dynamics 365 Financei inimressursside moodul toetab topeltkirjutuse ühendusi, kuid rakendus Dynamics 365 Human Resources ei luba seda.

Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.

+ Finance and Operationsi rakenduste uute eksemplaride puhul algab kahe kirjutamisühenduse seadistamine elutsükli teenustes Microsoft Dynamics (LCS). Kui teil on Microsoft Power Platformi litsents, saate uue Dataverse'i keskkonna, kui teie rentnikul seda ei ole.
+ Olemasolevatel juhtudel Finance and Operationsi rakendused algab topeltkirjutusühenduse seadistamine keskkonnas Finance and Operations.

Enne olemi topeltkirjutuse alustamist saate käivitada algse sünkroonimise, et käsitleda olemasolevaid andmeid mõlemalt poolt: Finance and Operationsi rakendused ja klientide kaasamise rakendused. Kui te ei pea nende kahe keskkonna vahel andmeid sünkroonima, saate algse sünkroonimise vahele jätta.

Algse sünkroonimisega saate kopeerida olemasolevad andmed kahesuunaliselt ühest rakendusest teise. Sõltuvalt sellest, millised keskkonnad teil on olemas ja millist tüüpi andmeid on nendes olemas, on mitu seadistuse stsenaariumi.

Toetatud on järgmised seadistusstsenaariumid:

+ [Uus Finance and Operationsi rakenduse eksemplar ja uus kliendi kaasamise rakenduse eksemplar](#new-new)
+ [Uus Finance and Operationsi rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar](#new-existing)
+ [Uus Finance and Operationsi rakenduse eksemplar, millel on andmed ja uus kliendi kaasamise rakenduse eksemplar](#new-data-new)
+ [Uus Finance and Operationsi rakenduse eksemplar, millel on andmed ja olemasolev kliendi kaasamise rakenduse eksemplar](#new-data-existing)
+ [Olemasolev Finance and Operationsi rakenduse eksemplar ja uus kliendi kaasamise rakenduse eksemplar](#existing-new)
+ [Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Uus Finance and Operationsi rakenduse eksemplar ja uus kliendi kaasamise rakenduse eksemplar

Kahe kirjutamisühenduse loomiseks rakenduse Finance and Operations uue eksemplari vahel, millel pole andmeid, ja kliendi kaasamise rakenduse uue eksemplari vahel järgige Lifecycle Servicesi [topeltkirjutuse seadistuse juhiseid](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- On ette nähtud uus tühi finants- ja toimingute keskkond.
- On ette valmistatud Customer Engagementi rakenduse uus tühi eksemplar, kus on installitud CRM-i pealahendus.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Uus Finance and Operationsi rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar

Kahe kirjutamisühenduse loomiseks rakenduse Finance and Operations uue eksemplari vahel, millel pole andmeid, ja olemasoleva kliendi kaasamise rakenduse eksemplari vahel järgige Lifecycle Servicesi [topeltkirjutuse seadistuse juhiseid](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- On ette nähtud uus tühi finants- ja toimingute keskkond.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

Olemasolevate Dataverse andmete sünkroonimiseks rakendusega Finance and Operations tehke järgmist.

1. Looge rakenduses Finance and Operations uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake selles teemas hiljem jaotist [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Uus Finance and Operationsi rakenduse eksemplar, millel on andmed ja uus kliendi kaasamise rakenduse eksemplar

Andmetega rakenduse Finance and Operations uue eksemplari ja kliendi kaasamise rakenduse uue eksemplari vahelise topeltkirjutusühenduse loomiseks järgige selles teemas [varem jaotises Uue finants- ja toimingute rakenduse eksemplari ja uue kliendi kaasamise rakenduse eksemplari](#new-new) juhiseid. Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage rakendus Finance and Operations LCS lehelt, logige sisse ja seejärel minge **andmehalduse \> topeltkirjutamisse**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Uus Finance and Operationsi rakenduse eksemplar, millel on andmed ja olemasolev kliendi kaasamise rakenduse eksemplar

Andmetega rakenduse Finance and Operations uue eksemplari ja kliendi kaasamise rakenduse olemasoleva eksemplari vahelise topeltkirjutusühenduse loomiseks järgige selles teemas [varem rakenduses A new Finance and Operations eksemplari ja olemasoleva kliendi kaasamise rakenduse eksemplari](#new-existing) juhiseid. Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage rakendus Finance and Operations LCS lehelt, logige sisse ja seejärel minge **andmehalduse \> topeltkirjutamisse**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Olemasolevate Dataverse andmete sünkroonimiseks rakendusega Finance and Operations tehke järgmist.

1. Looge rakenduses Finance and Operations uus ettevõte.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Olemasolev Finance and Operationsi rakenduse eksemplar ja uus kliendi kaasamise rakenduse eksemplar

Topeltkirjutusühenduse seadistamine rakenduse Finance and Operations olemasoleva eksemplari ja kliendi kaasamise rakenduse uue eksemplari vahel toimub finants- ja toimingukeskkonnas.

1. [Ühenduse häälestamine rakendusest](enable-dual-write.md) Finance and Operations.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Olemasolev Finance and Operationsi rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar

Topeltkirjutusühenduse seadistamine rakenduse Finance and Operations olemasoleva eksemplari ja kliendi kaasamise rakenduse olemasoleva eksemplari vahel toimub finants- ja operatsioonikeskkonnas.

1. [Ühenduse häälestamine rakendusest](enable-dual-write.md) Finance and Operations.
2. Olemasolevate Dataverse andmete sünkroonimiseks rakendusega [Finance and Operations käivitage](bootstrap-company-data.md)Dataverse andmed kolmetähelise ISO-ettevõtte koodi abil.
3. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="example"></a>Näide

Näite leiate teemast [Klientide lubamine V3 – kontaktide tabeli vastendus](enable-entity-map.md#enable-table-map)

Alternatiivse lähenemise saamiseks, mis põhineb igas üksuse andmemahtudel, millel tuleb käitada esialgne sünkroonimine, vaadake teemat [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]