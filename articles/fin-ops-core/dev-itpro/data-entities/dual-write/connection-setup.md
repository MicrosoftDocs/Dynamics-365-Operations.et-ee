---
title: Topeltkirjutuse häälestamise juhend
description: See artikkel kirjeldab stsenaariume, mida topeltkirjutuse seadistuses toetatakse.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289740"
---
# <a name="guidance-for-dual-write-setup"></a>Topeltkirjutuse häälestamise juhend

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Saate seadistada topeltkirjutuse ühenduse finantside ja operatsioonide keskkonna ning keskkonna Dataverse vahel.

+ Finants **- ja toimingute keskkond** pakub aluseks olevat platvormi finantside **ja toimingute rakenduste** jaoks (Microsoft Dynamics nt 365 Finantsid, Dynamics 365 Supply Chain Management ja Dynamics 365 Commerce).Dynamics 365 Human Resources
+ **Teenuse Dataverse keskkond** loob aluseks oleva platvormi **klientide kaasamise rakenduste** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).


> [!IMPORTANT]
> Dynamics 365 Finance inimressursside moodul toetab topeltkirjutusega ühendusi, Dynamics 365 Human Resources kuid rakendus mitte.

Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.

+ Uute finantside ja toimingute rakenduste puhul algab topeltkirjutuse ühenduse häälestamine elutsükli Microsoft Dynamics teenustes (LCS). Kui teil on Microsoft Power Platformi litsents, saate uue Dataverse'i keskkonna, kui teie rentnikul seda ei ole.
+ Olemasolevate eksemplaride finantside ja toimingute rakenduste jaoks algab topeltkirjutuse ühenduse häälestamine finantside ja toimingute keskkonnas.

Enne üksuse topeltkirjutuse käivitamist saate käivitada algse sünkroonimise, et käsitleda olemasolevaid andmeid mõlemal pool: finantside ja toimingute rakendused ja kliendi kaasamise rakendused. Kui te ei pea nende kahe keskkonna vahel andmeid sünkroonima, saate algse sünkroonimise vahele jätta.

Algse sünkroonimisega saate kopeerida olemasolevad andmed kahesuunaliselt ühest rakendusest teise. Sõltuvalt sellest, millised keskkonnad teil on olemas ja millist tüüpi andmeid on nendes olemas, on mitu seadistuse stsenaariumi.

Toetatud on järgmised seadistusstsenaariumid:

+ [Uus finantside ja toimingute rakenduse eksemplar ning uus kliendi kaasamise rakenduse eksemplar](#new-new)
+ [Uus finantside ja toimingute rakenduse eksemplar ning olemasolev kliendi kaasamise rakenduse eksemplar](#new-existing)
+ [Uus finantside ja toimingute rakenduse eksemplar, kus on andmed ja uus kliendi kaasamise rakenduse eksemplar](#new-data-new)
+ [Uus finantside ja toimingute rakenduse eksemplar, kus on andmed ja olemasolev kliendi kaasamise rakenduse eksemplar](#new-data-existing)
+ [Olemasolev finants- ja toimingute rakenduse eksemplar ning uus kliendikogemuse rakenduse eksemplar](#existing-new)
+ [Olemasolev finants- ja toimingute rakenduse eksemplar ning olemasolev kliendi kaasamise rakenduse eksemplar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Uus finantside ja toimingute rakenduse eksemplar ning uus kliendi kaasamise rakenduse eksemplar

Topeltkirjutuse ühenduse seadistamiseks finants- ja operatsioonide rakenduse uue eksemplari vahel, kus pole andmeid ja kliendi kaasamise rakenduse uut eksemplari, [järgige elutsükli teenuste topeltkirjutuse häälestuse samme](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- Uus, tühi finants ja toimingute keskkond on ette ettevalmistamises.
- On ette valmistatud Customer Engagementi rakenduse uus tühi eksemplar, kus on installitud CRM-i pealahendus.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Uus finantside ja toimingute rakenduse eksemplar ning olemasolev kliendi kaasamise rakenduse eksemplar

Topeltkirjutuse ühenduse seadistamiseks finants- ja operatsioonide rakenduse uue eksemplari vahel, kus pole andmeid ja olemasoleva kliendikogemuse rakenduse eksemplari, [järgige elutsükli teenuste topeltkirjutuse häälestuse samme](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- Uus, tühi finants ja toimingute keskkond on ette ettevalmistamises.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

Et sünkroonida olemasolevaid Dataverse andmeid finantside ja toimingute rakendusega, järgige neid samme.

1. Looge uus ettevõte finantside ja toimingute rakenduses.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näitele ja alternatiivsele lähenemisele vt selle [artikli](#example) näitejaost.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Uus finantside ja toimingute rakenduse eksemplar, kus on andmed ja uus kliendi kaasamise rakenduse eksemplar

Andmetega ja kliendikogemuse rakenduse uue eksemplariga finants- ja operatsioonide rakenduse uue eksemplari vahelise topeltkirjutuse ühenduse loomiseks järgige [käesoleva artikli varasemat etappi A](#new-new) uue finantsi ja toimingute rakenduse eksemplaris ja uues kliendikogemuse rakenduse eksemplaris. Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage finantside ja toimingute rakendus LCS-leheküljelt, logige sisse ja minge seejärel **\> andmehalduse topeltkirjutusse**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Uus finantside ja toimingute rakenduse eksemplar, kus on andmed ja olemasolev kliendi kaasamise rakenduse eksemplar

Andmetega finants- ja operatsioonide rakenduse uue eksemplari ning kliendikogemuse rakenduse olemasoleva eksemplari vahel topeltkirjutuse ühenduse loomiseks järgige [käesoleva artikli varasemat etappi A](#new-existing) uue finantsi ja toimingute rakenduse eksemplaris ja olemasoleva kliendi kaasamise rakenduse eksemplaris. Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage finantside ja toimingute rakendus LCS-leheküljelt, logige sisse ja minge seejärel **\> andmehalduse topeltkirjutusse**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Et sünkroonida olemasolevaid Dataverse andmeid finantside ja toimingute rakendusega, järgige neid samme.

1. Looge uus ettevõte finantside ja toimingute rakenduses.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Olemasolev finants- ja toimingute rakenduse eksemplar ning uus kliendikogemuse rakenduse eksemplar

Finantside ja toimingute rakenduse olemasoleva eksemplari ja kliendi kaasamise rakenduse uue eksemplari vaheline topeltkirjutuse ühendus toimub finantside ja toimingute keskkonnas.

1. [Häälestage ühendus finantside ja toimingute rakendusest](enable-dual-write.md).
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Olemasolev finants- ja toimingute rakenduse eksemplar ning olemasolev kliendi kaasamise rakenduse eksemplar

Finantside ja toimingute rakenduse olemasoleva eksemplari ja kliendi kaasamise rakenduse olemasoleva eksemplari vahel toimub finants- ja toimingukeskkonnas topeltkirjutusega ühenduse seadistus.

1. [Häälestage ühendus finantside ja toimingute rakendusest](enable-dual-write.md).
2. Olemasolevate andmete sünkroonimiseks Dataverse finants- ja operatsioonide rakendusega [jagage andmed](bootstrap-company-data.md)Dataverse kolmetäheline ISO-koodiga.
3. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="example"></a>Näide

Näite leiate teemast [Klientide lubamine V3 – kontaktide tabeli vastendus](enable-entity-map.md#enable-table-map)

Alternatiivse lähenemise saamiseks, mis põhineb igas üksuse andmemahtudel, millel tuleb käitada esialgne sünkroonimine, vaadake teemat [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
