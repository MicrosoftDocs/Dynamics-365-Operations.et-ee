---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (28. mai 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c386025843edef83d229a42d3f2314678fadae20
ms.sourcegitcommit: beddfba095c23b3265f0004f5124c4e9dc6404cc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411926"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (28. mai 2020)

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3287. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>Üksus LeaveRequest ei tööta, kui lubate puhkuseplaani kohta mitu tüüpi (447498)

Antud muudatusega seoses on nüüd mitme puhkusetüübi lubamisel antud tõrke parandamiseks saadaval üksus **LeaveEnrollmentV2Entity**.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Partiisisalduse vähendamise funktsioon (eelvaade) (446619)

Antud funktsiooni lubamisel võite oodata partii raamistiku tabelites blokeerimise vähenemist ülesannete valimisel ja tööde lõpetamisel.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict takistab töötaja salvestamisel kirje redigeerimist jaotises Inimesed (427915)

See muudatus parandab tõrke, mis esineb uue töötaja lisamisel, aadressi uuendamisel ja keele-eelistuse muutmisel. Selles ainulaadses stsenaariumis kuvatakse tõrge, mis näitab, et kirjet ei õnnestunud värskendada. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Kinnitatud puhkusetaotlusele ei saa lisada manust uuesti esitamiseks (425407)

See muudatus võimaldab nüüd lisada kinnitatud puhkusetaotlustele lisasid.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Kasutaja saab sisestada töötaja hüvituse muu juriidilise isiku vormil (409529)

See muudatus keelab hüvituse valikud, vältimaks kogemata vale juriidilise isiku jaoks hüvituse kirjete lisamist.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Tõrge töötaja ülekandmisel, kui töötaja ametikohale määramise kuupäev on enne ametikoha kestuse ajavahemikku (429402)

Antud stsenaariumis töötaja ülekandmisega seotud tõrketeateid on värskendatud, et anda paremini edasi probleemi lahendamiseks vajalikke muudatusi.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Manuse võimalus töötaja iseteeninduses soodustuste registreerimisel
 
Nüüd saate lisada soodustuste registreerimise protsessi käigus manuseid iga plaani kohta, millesse töötaja registreerub. Seejärel saate manuseid kuvada vormis **Töötaja registreeritud soodustus**.

## <a name="in-preview"></a>Eelvaates

## <a name="human-resources-application-in-teams"></a>Rakendus Human Resources Teamsis

Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams. Nad saavad suhelda botiga, et luua puhkusetaotlusi. Lisateavet vt teemast [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="leave-suspension"></a>Puhkuse peatamine

Saate peatada töövõtja puhkuse Human Resourcesis. Puhkuse peatamine lõpetab puhkuse viitvõlad valitud puhkusetüüpide puhul. Kui peatamine toimub pärast viitvõla töötlemist, loob peatatav puhkus eelmääratud korrigeerimise töötaja puhkusesaldo jaoks. Lisateabe saamiseks vt [Puhkuse peatamine](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Kasutajakogemuse uuendamine viitvõla näitamiseks on peatatud (429550)

Kasutajakogemuses on nüüd näidatud, et plaani viitvõlg on peatatud.

## <a name="coming-soon"></a>Peagi tulekul

## <a name="database-logging-in-preview-in-june"></a>Andmebaasi logimine (eelvaates juunis)

Andmebaasi logimise funktsioon võimaldab teil kindlaks määrata, millist tabelit ja milliseid välju tuleks jälgida. Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise. Muudatuste ajas muutumise nägemiseks on saadaval päringu võimalused.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Puhkuse ost ja müük (eelvaates 1. juunil)

Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta. Seda protsessi hallatakse sageli käsitsi. See funktsioon pakub personaliosakonnale auomaatsemat viisi poliiside ja taotluste haldamiseks ja aitab kõrvaldada vigasid, korrastades puhkusehalduse protsessi.

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks
 
Välja tulevad soodustuste haldamise üksused. DMF-üksused võimaldavad andmeid importida ja eksportida soodustuste halduse lihtsaks konfigureerimiseks. Soodustuste haldamise mall on saadaval ka andmete teisaldamiseks. Mall ekspordib ja impordib andmeid järjestikusel moel vastavalt andmesõltuvustele.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Lisa viitvõlgade peatamisele põhjusekood (1. juuni)

Viitvõla peatamisele on lisatud põhjusekood.

## <a name="carry-forward-rules-june-1"></a>Edasikandmise reeglid (1. juuni)

Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle. Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi. Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Kindlate puhkusetüüpide puhkuse viitvõla peatamine (1. juuni)

Selles väljalaskes saab inimressursside haldur luua reegli, et peatada selliste töötajate puhkuse viitvõlg, kes on esitanud tasustamata puhkuse taotluse. Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla. Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF-üksus on saadaval viitvõlgade peatamiseks (1. juuni)

Nüüdsest on viitvõlgade peatamiseks saadaval DMF-üksus.