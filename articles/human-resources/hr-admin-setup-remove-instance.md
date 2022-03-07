---
title: Eemalda eksemplar
description: See artikkel selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Human Resources puhul.
author: andreabichsel
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72a5b99150e5ccdf9a542b569c94c64cb95923fd
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053607"
---
# <a name="remove-an-instance"></a>Eemalda eksemplar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel selgitab proovi- või tootmiskeskkonna eemaldamise protsessi rakenduse Microsoft Dynamics 365 Human Resources puhul.

## <a name="remove-a-test-drive-environment"></a>Proovikeskkonna eemaldamine

Rakenduse Human Resources proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga. Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist. 

1. Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)
2. Valige **Keskkonnad**.
3. Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain
4. Valige **Kustuta** ja kinnitage otsus. 

Olemasolev proovikeskkond eemaldatakse. Kui see on eemaldatud, saate registreerida uue proovikeskkonna. 

## <a name="remove-a-production-environment"></a>Tootmiskeskkonna eemaldamine

See artikkel eeldab, et olete ostnud rakenduse Human Resources pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu. 

Kuna üks Human Resourcesi keskkond asub ühes Power Appsi keskkonnas, on kaks valikut. Esimene valik hõlmab kogu Power Appsi keskkonna eemaldamist; teine hõlmab ainult Human Resourcesi eemaldamist. Esimene valik on soovitatav, kui lõite Power Appsi keskkonna spetsiaalselt Human Resourcesi ettevalmistamiseks ja olete just juurutamisega alustanud või te pole loonud integratsioone. Teine suvand on sobiv, kui teil on loodud Power Appsi keskkond, mis on täidetud rikasandmetega, mida kasutatakse Power Appsis ja Power Automate’is.

> [!Important]
> Enne Power Appsi keskkonna eemaldamist veenduge, et seda ei kasutataks rikasandmete integreerimiseks väljaspool rakenduse Human Resources ulatust. Pange tähele, et Power Appsi vaikekeskkondasid ei saa eemaldada. 

Kogu Power Appsi keskkonna eemaldamiseks koos Human Resourcesi ja seotud rakenduste ning voogudega tehke järgmist.

1. Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)
2. Valige **Keskkonnad**.
3. Valige eemaldatav keskkond.
4. Valige **Kustuta** ja kinnitage otsus. 
5. Oodake, kuni kustutamine on lõpule viidud.
6. Logige teenusesse [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks. 
7. Valige keskkonda sisaldav Human Resourcesi projekt. 
8. Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**. 
9. Valige eemaldatav eksemplar. 
10. Valige **Eemalda eksemplar** ja kinnitage otsus.  

Rakenduse Human Resources eemaldamiseks olemasolevast Power Appsi keskkonnast tehke järgmist. Pange tähele, et tugimeeskonna kaasamine ja Human Resourcesi DevOpsi töörühmaga ühenduse võtmine on ajutine, kuni see funktsioon on lubatud otse LCS-is.

1. Eemaldamistaotluse käivitamiseks võtke ühendust toega.
2. Tugimeeskond edastab eemaldamise taotluse Human Resourcesi DevOpsi töörühmale. 
3. Jätkake siis, kui olete saanud kinnituse, et keskkond on eemaldatud.
4. Logige LCS-i sisse, kasutades kontot, mida kasutasite rakenduse Human Resources tellimiseks. 
5. Valige keskkonda sisaldav Human Resourcesi projekt. 
6. Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**. 
7. Valige eksemplar, mille soovite eemaldada (selle juures peaks olema märgitud juurutuse olek **Kustutatud**).
8. Valige **Eemalda eksemplar** ja kinnitage otsus. 

## <a name="recover-a-soft-deleted-environment"></a>Ajutiselt kustutatud keskkonna taastamine

Kui kustutate Power Appsi keskkonna, millega on ühendatud teie Human Resourcesi keskkond, kustutatakse Human Resourcesi olek teenuses Lifecycle Services **ajutiselt**. Sel juhul ei saa kasutajad Human Resourcesiga ühendust luua.

Keskkonna taastamiseks tehke järgmist.

1. Järgige teemas [Power Appsi keskkonna taastamine](/power-platform/admin/recover-environment.md) toodud juhiseid.

2. Human Resourcesi keskkonna taastamiseks võtke ühendust tugiteenusega. Lisateavet leiate teemast [Toe hankimine](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Appsi keskkondi salvestatakse ainult seitse päeva pärast kustutamist. Peate taastama keskkonna seitsme päeva jooksul.


[!INCLUDE[footer-include](../includes/footer-banner.md)]