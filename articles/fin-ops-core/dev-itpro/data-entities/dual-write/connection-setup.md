---
title: Topeltkirjutuse häälestamise juhend
description: See artikkel kirjeldab stsenaariume, mida topeltkirjutuse seadistuses toetatakse.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: a0d1b4e1f093874a8fd37cf7aadb331cd1e7adc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873145"
---
# <a name="guidance-for-dual-write-setup"></a>Topeltkirjutuse häälestamise juhend

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



Saate seadistada topeltkirjutuse ühenduse Finantside ja toimingute keskkonna ning keskkonna Dataverse vahel.

+ Finantside **ja toimingute keskkond** on finantside ja **toimingute rakenduste aluseks olev** platvorm (Microsoft Dynamics nt 365 Finantsid, Dynamics 365 Supply Chain Management ja Dynamics 365 Commerce).Dynamics 365 Human Resources
+ **Teenuse Dataverse keskkond** loob aluseks oleva platvormi **klientide kaasamise rakenduste** jaoks (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing ja Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> Dynamics 365 Finance inimressursside moodul toetab topeltkirjutusega ühendusi, Dynamics 365 Human Resources kuid rakendus mitte.

Seadistuse mehhanism erineb sõltuvalt teie tellimusest ja keskkonnast.

+ Finantside ja toimingute rakenduste uute eksemplaride puhul algab topeltkirjutuse ühenduse häälestamine elutsükli Microsoft Dynamics teenustes (LCS). Kui teil on Microsoft Power Platformi litsents, saate uue Dataverse'i keskkonna, kui teie rentnikul seda ei ole.
+ Olemasolevate eksemplaride Finance ja Operationsi rakenduste puhul algab topeltkirjutuse ühenduse häälestamine Finantside ja toimingute keskkonnas.

Enne üksuse topeltkirjutuse käivitamist saate käivitada algse sünkroonimise, et käsitleda olemasolevaid andmeid mõlemal pool: finantside ja toimingute rakendused ja kliendi kaasamise rakendused. Kui te ei pea nende kahe keskkonna vahel andmeid sünkroonima, saate algse sünkroonimise vahele jätta.

Algse sünkroonimisega saate kopeerida olemasolevad andmed kahesuunaliselt ühest rakendusest teise. Sõltuvalt sellest, millised keskkonnad teil on olemas ja millist tüüpi andmeid on nendes olemas, on mitu seadistuse stsenaariumi.

Toetatud on järgmised seadistusstsenaariumid:

+ [Uus Finantside ja toimingute rakenduse eksemplar ning uus kliendi kaasamise rakenduse eksemplar](#new-new)
+ [Uus Finantside ja toimingute rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar](#new-existing)
+ [Uus Finantside ja toimingute rakenduse eksemplar, kus on andmed ja uus kliendi kaasamise rakenduse eksemplar](#new-data-new)
+ [Uus Finantside ja toimingute rakenduse eksemplar, kus on andmed ja olemasolev kliendi kaasamise rakenduse eksemplar](#new-data-existing)
+ [Olemasolev Finantside ja toimingute rakenduse eksemplar ning uus kliendi kaasamise rakenduse eksemplar](#existing-new)
+ [Olemasolev finants- ja toimingute rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a> Uus Finantside ja toimingute rakenduse eksemplar ning uus kliendi kaasamise rakenduse eksemplar

Topeltkirjutuse ühenduse seadistamiseks finants- ja operatsioonide rakenduse uue, andmeteta eksemplari ja kliendi kaasamise rakenduse uue eksemplari vahel järgige [elutsükli teenuste topeltkirjutuse häälestuse](lcs-setup.md) samme. Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- Uus, tühi finantside ja toimingute keskkond on ette ettevalmistamises.
- On ette valmistatud Customer Engagementi rakenduse uus tühi eksemplar, kus on installitud CRM-i pealahendus.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a> Uus Finantside ja toimingute rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar

Topeltkirjutuse ühenduse seadistamiseks finants- ja operatsioonide rakenduse uue, andmeteta rakenduse ja olemasoleva kliendikogemuse rakenduse eksemplari vahel järgige [elutsükli teenuste topeltkirjutuse häälestuse samme](lcs-setup.md). Kui ühenduse seadistus on lõpule viidud, toimuvad automaatselt järgmised toimingud.

- Uus, tühi finantside ja toimingute keskkond on ette ettevalmistamises.
- Kaksikkirjutamise ühendus on loodud DAT-ettevõtte andmetele.
- Tabeli vastendused on lubatud reaalajas sünkroonimiseks.

Mõlemad keskkonnad on seejärel valmis reaalaja andmete sünkroonimiseks.

Et sünkroonida olemasolevaid Dataverse andmeid Finantside ja Toimingute rakendusega, järgige neid samme.

1. Uue ettevõtte loomine rakenduse finantside ja toimingute rakenduses.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näitele ja alternatiivsele lähenemisele vt selle [artikli](#example) näitejaost.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a> Uus Finantside ja toimingute rakenduse eksemplar, kus on andmed ja uus kliendi kaasamise rakenduse eksemplar

Andmetega finants- ja operatsioonide rakenduse uue eksemplari vahelise topeltkirjutuse ühenduse loomiseks, mille andmed on kliendikogemuse rakenduse uue eksemplariga, [järgige käesoleva artikli varasemat etappi rakenduses Finantsid](#new-new) ja toimingud ja uues kliendikogemuse rakenduse eksemplaris. Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage finantside ja toimingute rakendus LCS-leheküljelt, logige sisse ja minge seejärel **\> andmehalduse topeltkirjutusse**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a> Uus Finantside ja toimingute rakenduse eksemplar, kus on andmed ja olemasolev kliendi kaasamise rakenduse eksemplar

Andmetega finants- ja operatsioonide rakenduse uue eksemplari vahelise topeltkirjutuse ühenduse loomiseks, mille andmed on kliendikogemuse rakenduse olemasoleva eksemplariga, [järgige käesoleva artikli varasemat etappi rakenduses Finantsid](#new-existing) ja toimingud ja olemasoleva kliendi kaasamise rakenduse eksemplaris. Kui ühenduse häälestus on lõpule viidud, kui soovite andmeid sünkroonida Customer Engagementi rakendusega, toimige järgmiselt.

1. Avage finantside ja toimingute rakendus LCS-leheküljelt, logige sisse ja minge seejärel **\> andmehalduse topeltkirjutusse**.
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Et sünkroonida olemasolevaid Dataverse andmeid Finantside ja Toimingute rakendusega, järgige neid samme.

1. Uue ettevõtte loomine rakenduse finantside ja toimingute rakenduses.
2. Lisage ettevõte kaksikkirjutamise ühenduse seadistusse.
3. Rakendage[Bootstrap](bootstrap-company-data.md) Dataverse andmetele, kasutades kolmetähelist Rahvusvahelise standardiorganisatsiooni (ISO) ettevõttekoodi.
4. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a> Olemasolev Finantside ja toimingute rakenduse eksemplar ning uus kliendi kaasamise rakenduse eksemplar

Finantside ja toimingute rakenduse olemasoleva eksemplari ja kliendi kaasamise rakenduse uue eksemplari vahel toimub finants- ja toimingukeskkonnas topeltkirjutusega ühenduse seadistus.

1. [Häälestage ühendus rakendusest Finantsid ja Toimingud](enable-dual-write.md).
2. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a> Olemasolev finants- ja toimingute rakenduse eksemplar ja olemasolev kliendi kaasamise rakenduse eksemplar

Finantside ja toimingute rakenduse olemasoleva eksemplari ja kliendi kaasamise rakenduse olemasoleva eksemplari vahel toimub finants- ja toimingukeskkonnas topeltkirjutusega ühenduse seadistus.

1. [Häälestage ühendus rakendusest Finantsid ja Toimingud](enable-dual-write.md).
2. Olemasolevate andmete sünkroonimiseks Dataverse rakendusega Finantsid ja Toimingud laiendage [andmed](bootstrap-company-data.md)Dataverse kolmetäheline ISO-koodi kasutades.
3. Käivitage **Esmase sünkroonimise** funktsionaalsus tabelites, millele soovite andmeid sünkroonida.

Linke näidete vaatamiseks ja alternatiivse lähenemise jaoks vaadake jaotist [Näide](#example).

## <a name="example"></a>Näide

Näite leiate teemast [Klientide lubamine V3 – kontaktide tabeli vastendus](enable-entity-map.md#enable-table-map)

Alternatiivse lähenemise saamiseks, mis põhineb igas üksuse andmemahtudel, millel tuleb käitada esialgne sünkroonimine, vaadake teemat [Algse sünkroonimise kaalutlused](initial-sync-guidance.md).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]