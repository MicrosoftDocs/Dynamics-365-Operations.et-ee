---
title: Süsteemi Go-live KKK
description: Selles teemas loetletakse Dynamics 365 Human Resourcesi juurutusprojekti kasutuselevõtuga seonduvaid korduma kippuvaid küsimusi.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d667d94983d5c8f8e6140259922396d4299a15e3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467580"
---
# <a name="go-live-faq"></a>Süsteemi Go-live KKK 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas loetletakse Dynamics 365 Human Resourcesi juurutusprojekti kasutuselevõtuga seonduvaid korduma kippuvaid küsimusi. 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>Millal ma saan konfigureerida ja taotleda oma töökeskkonda? 

Tavaliselt saab töökeskkonda juurutada pärast järgmiste kriteeriumite täitmist.

- Kõikide kohanduste kood on lõpule viidud.
- Kasutaja nõusoleku testimine (UAT) on lõpule viidud.
- Klient on lahendusele nõusoleku andnud.
- Kasutuselevõttu blokeerivaid probleeme pole. 

Kui kvalifitseeritud kliendid on jõudnud sellesse etappi, töötab Microsoft FastTracki meeskond koos projekti meeskonnaga kasutuselevõtu hindamise tegemiseks. 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>Mis on töökeskkonna juurutamise eeltingimused? 

Eeltingimuste loendi leiate teemast  [Kasutuselevõtuks ettevalmistamine](hr-admin-go-live-prepare.md). 

## <a name="what-is-a-go-live-assessment"></a>Mis on kasutuselevõtu hindamine?  

Kasutuselevõtu hindamine on  [Microsoft FastTracki programmi](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview) osa. Selle läbivaatuse käigus hindab lahenduse arhitekt, kas juurutusprojekt on valmis edukaks üleminekuks ja kasutuselevõtuks. See läbivaatus on kohustuslik kõigile juurutusprojektidele, enne kui saate taotleda töökeskkonna kasutuselevõtmist. 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>Meie liivakastikeskkonnad juurutatakse Kesk-USA andmekeskuses. Soovime, et meie töökeskkonnad oleksid juurutatud Lääne-USA andmekeskuses. Kas ma saan valida Lääne-USA oma töökeskkonna konfiguratsiooni andmekeskuseks? 

LCS ei keela teise andmekeskuse valimist Human Resourcesi keskkonna juurutamisel, kuid soovitame tungivalt mitte valida teist andmekeskust.  

Kui soovite oma töökeskkonda Lääne-USA andmekeskusesse, peaksite esmalt oma liivakastikeskkonnad Lääne-USA andmekeskuses uuesti juurutama, neid katsetama ja andma nõusoleku. 

Lisateavet õige andmekeskuse valimise kohta leiate teemast [Võrgunõuded](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/system-requirements#network-requirements). 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>Mis tasemel juurdepääs mul on Human Resourcesi keskkondade Azure'i ressurssidele?  

Human Resourcesi keskkondade juurdepääs on piiratud. Te ei pääse juurde virtuaalarvutile (VM) või Microsoft Internet Information Servicesi (IIS). Samuti pole teil andmebaasi juurdepääsu Microsoft SQL Server Management Studio kaudu. 

Kuigi te ei pääse oma Azure'i ressurssidele või Dynamics 365 Human Resourcesi keskkonnale juurde otse, on teil täiendavaid funktsioone, mida saate kasutada oma andmetele juurde pääsemiseks.

- Saate juurutada Azure SQL-i andmebaasi oma Azure'i rentnikku ja kasutada oma andmebaasi toomise (BYOD) funktsiooni andmete sünkroonimiseks. Lisateavet leiate teemast [Oma andmebaasi toomine (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database).

- Saate kasutada Dataverse'i integreerimist valitud üksuste sünkroonimiseks Dataverse'i andmebaasi. Lisateavet leiate [Dataverse'i tabelitest](hr-developer-entities.md). 

## <a name="how-often-is-my-production-database-backed-up"></a>Kui tihti minu tööandmebaasi varundatakse? 

Andmebaase kaitstakse automaatse varundusega järgmise sagedusega.

| Varunduse tüüp | Sagedus |
| --- | --- |
| Täielik andmebaasi varundus | Iganädalane |
| Eristav andmebaasi varundus | Iga 12–24 tunni järel |
| Kandelogi varundus | Iga 5–10 minuti järel |

Microsoft säilitab piisavalt varukoopiaid selleks, et lubada ajapunktipõhist taastet (PITR) viimase 14 päeva jooksul. 

Lisateabe saamiseks vt jaotist  [Lisateave SQL-i andmebaasi automaatsete varunduste kohta](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database). 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>Kas ma saan taotleda oma andmebaasi varunduse koopiat? 

Nr Saate esitada andmebaasi värskendamise teenuse taotluse oma töökeskkonna kopeermiseks liivakastikeskkonda. Saate juurutada Azure SQL-i andmebaasi oma Azure'i rentnikku ja kasutada BYOD-i funktsiooni andmete sünkroonimiseks töökeskkonnast. Lisateavet leiate teemast [Oma andmebaasi toomine (BYOD)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database). 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>Kuidas ma saan teisaldada liivakastikeskkonda töökeskkonna selle kasutuselevõtuks? 

Kuna kopeerimise funktsioon ei ole saadaval keskkonna teisaldamiseks liivakastikeskkonnast töökeskkonda, peate kasutama andmepakette andmete teisaldamiseks oma töökeskkonda.  

Soovitame säilitada selge loendi üksustest, mis on konfigureeritud teie liivakastikeskkonnas kogu projekti jooksul. Seejärel katsetage kasutuselevõtuks vajalike andmepakettide ülemineku- ja migreerimisprotsessi. Kui olete kasutuselevõtuks valmis, peate kõik andmepaketid käsitsi töökeskkonda teisaldama. 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>Mida teha, kui minu töökeskkond on maas? 

Töökeskkonna katkestusest teatamiseks järgige juhiseid jaotises  [Töökeskkonna katkestusest teatamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/report-production-outage). 

 ## <a name="see-also"></a>Vt ka

 [Ettevalmistamine süsteemi Go-Live jaoks](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]