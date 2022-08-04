---
title: Eemalda eksemplar
description: See artikkel kirjeldab testdraivi või Microsofti tootmiskeskkonna eemaldamise protsessi Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178468"
---
# <a name="remove-an-instance"></a>Eemalda eksemplar

_**Rakendub:** inimressursid autonoomsel infrastruktuuril_ 

> [!NOTE]
> Alates 2022. juulist ei saa uusi inimressursid keskkondi eraldi inimressursside infrastruktuuris Microsoft Dynamics ette luua ja uusi elutsükli teenuste (LCS) projekte ei saa selles luua. Kliendid saavad inimressursside keskkondi kasutusele võtta finantside ja toimingute infrastruktuuris. Lisateavet vt inimressursside ettevalmistamisest [finantside ja toimingute infrastruktuuris](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finantside ja toimingute rakenduse infrastruktuur toetab keskkonna kustutamist. Lisateavet keskkonna kustutamise kohta vt keskkonna [kustutamine](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

See artikkel selgitab microsofti testdraivi või tootmiskeskkonna eemaldamise protsessi Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Proovikeskkonna eemaldamine

Rakenduse Human Resources proovikeskkonnad on ette valmistatud 60-päevase aegumispoliitikaga. Kuid proovikeskkondade omanikel on võimalus lõpetada prooviversioon varakult, tehes järgmist. 

1. Avage [Power Apps Halduskeskus](https://admin.businessplatform.microsoft.com/)
2. Valige **Keskkonnad**.
3. Valige proovikeskkond, millel on vormingult sarnane nimi järgmisega: TestDrive – alias@domain
4. Valige **Kustuta** ja kinnitage otsus. 

Olemasolev proovikeskkond eemaldatakse. Kui see on eemaldatud, saate registreerida uue proovikeskkonna. 

## <a name="remove-a-production-environment"></a>Tootmiskeskkonna eemaldamine

See artikkel eeldab, et olete ostnud rakenduse Human Resources pilvelahenduse pakkuja (CSP) või ettevõtte arhitektuuri (AE) lepingu kaudu. 

Kuna üks Inimressursid keskkond sisaldub ühes Power Apps keskkonnas, on keskkonna eemaldamisel vaja arvestada kahe valikuga: 
- **Eemalda kogu Power Apps keskkond.** Seda valikut eelistatakse siis Power Apps, kui keskkond loodi Inimressursside ressursina kasutamiseks, rakendamine on just alanud või kui teil ei ole kindlaks määratud integratsiooni.  
- **Eemalda ainult inimressursid.** See valik on sobiv, kui on loodud Power Apps keskkond, mis on asustatud andmetega, mida kasutatakse ja Microsoft Power Apps Power Automate.


> [!Important]
> Enne keskkonna eemaldamist Power Apps veenduge, et seda ei kasutata andmete integratsiooniks väljaspool Inimressursside ulatust. Pange tähele, et Power Appsi vaikekeskkondasid ei saa eemaldada. 

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

Kui kustutate keskkonna Power Apps, millega teie inimressursid keskkond on ühendatud, kustutatakse LCS-i inimressursside keskkonna olek **Kerge**. Sel juhul ei saa kasutajad Human Resourcesiga ühendust luua.

Keskkonna taastamiseks tehke järgmist.

1. Järgige teemas [Power Appsi keskkonna taastamine](/power-platform/admin/recover-environment) toodud juhiseid.

2. Human Resourcesi keskkonna taastamiseks võtke ühendust tugiteenusega. Lisateavet leiate teemast [Toe hankimine](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Appsi keskkondi salvestatakse ainult seitse päeva pärast kustutamist. Peate taastama keskkonna 7-päevase perioodi jooksul.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
