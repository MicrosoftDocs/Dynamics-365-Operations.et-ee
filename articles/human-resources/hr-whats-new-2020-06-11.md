---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (11. juuni 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 11. juuni 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0720b2024a865fcd42cd80fd905586d626388f8f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418198"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (11. juuni 2020)

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3316. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a>Sujuva töövõtjavormi tõttu ei tööta mõnikord tütarvormi sulgemise (X) nupud (442369)

Kui lubati uus **Töötaja** vorm, ei töötanud mõnikord tütarvormide sulgemise (**X**) nupp. See probleem oli hootine. Pärast vormi juurest lahkumist ja selle juurde naasmist oli võimalik vorm sulgeda. Näiteks võisite valida vasakpoolsest menüüst üksuse ja liikuda tagasi **Töötaja** vormile ning seejärel selle sulgeda. Selle nädala väljaanne lahendab selle probleemi. 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a>Töötaja isikliku kontaktisiku üksus ei ekspordi isiklikke kontakte, millel on emaseosetüüp

Selle väljaande järel ekspordib üksus **Töötaja isikliku kontaktisik** kõiki seosetüüpe.

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a>HcmPositionWorkerAssignmentV2Entity peaks kuuluma vaikimisi Ceridiani palgaarvestuse integreerimise paketi juurde (448506)

Selle muudatuse järel on **HcmPositionWorkerAssignmentV2Entity** saadaval Ceridiani palgaarvestuse integreerimise paketis.

## <a name="in-preview"></a>Eelvaates

## <a name="database-logging"></a>Andmebaasi logimine

Andmebaasi logimise funktsioon võimaldab teil kindlaks määrata, milliseid tabeleid ja välju tuleks jälgida. Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise. Saate kasutada andmebaasi logimise võimalusi, et aja jooksul neid muutusi näha. Lisateavet leiate teemast [Andmebaasi logimise konfigureerimine ja haldamine](hr-admin-database-logging.md).

## <a name="human-resources-application-in-teams"></a>Rakendus Human Resources Teamsis

Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams. Nad saavad suhelda botiga, et luua puhkusetaotlusi. Lisateavet vt teemast [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks
 
Välja tulevad soodustuste haldamise üksused. DMF-üksused võimaldavad teil andmeid importida ja eksportida, et lihtsalt soodustuste haldamist konfigureerida. Soodustuste haldamise mall on saadaval andmete teisaldamiseks. Mall ekspordib ja impordib andmeid andmesõltuvuste arvestamiseks järjestikku.

## <a name="buy-and-sell-leave"></a>Puhkuse ostmine ja müümine 

Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta. Seda protsessi hallatakse sageli käsitsi. See funktsioon muudab personaliosakonna jaoks poliitikate ja taotluste haldamise automaatseks. See muudab puhkusehalduse protsessi sujuvamaks ja aitab kõrvaldada vigu. Lisateabe saamiseks vt:

- [Puhkuse ostu ja müügi poliitikate haldamine](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Puhkuse ostmine ja müümine](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Puhkuse lisandumine üksiku ettevõtte või plaani puhul

Kliendid saavad töödelda lisandumisi üksiku ettevõtte või üksiku puhkuste ja puudumiste plaani puhul. See võimalus muudab lisandumisprotsessi selgemaks selliste klientide puhul, kellel on eri puhkuseaastad või puhkuse lisandumise poliitikad. Lisateavet leiate teemast [Puhkuse lisandumine ettevõtte või puhkuseplaani alusel](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Eemalolekuaja taotlustele manuste lisamine

Manuste lisamise võimalus kinnitatud puhkusetaotlustele on praegust COVID-19 olukorda arvestades väga oluline. Töövõtjad saavad nüüd neid manuseid lisada. Samuti on neil rohkem teavet selle kohta, kuidas puhkusetaotlusi uuendatakse. Lisateavet leiate teemast [Olemasolevale taotlusele manuse lisamine](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Lisandumise peatamisele põhjusekoodi lisamine 

Lisandumise peatamisele on lisatud põhjusekoodid.

## <a name="carry-forward-rules"></a>Edasikandmise reeglid 

Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle. Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi. Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Puhkuse lisandumise peatamine kindlate puhkusetüüpide puhul

Saate luua reegli, et peatada selliste töötajate puhkuse lisandumine, kes on esitanud tasustamata puhkuse taotluse. Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla. Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-üksus on saadaval lisandumise peatamiseks 

Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.

## <a name="coming-soon"></a>Peagi tulekul

## <a name="new-platform-capabilities"></a>Uued platvormi funktsioonid 

Saate muuta väljad kohustuslikuks isikupärastamise kaudu. Selle funktsiooni jaoks peate lubama **Salvestatud vaated**.

## <a name="configure-the-name-of-employee-self-service"></a>Töövõtja iseteeninduse nime konfigureerimine

Rakenduse Human Resources parameetrites on saadaval uus suvand, et muuta töövõtja iseteeninduse tööruumi nimi iseteeninduseks. 

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)