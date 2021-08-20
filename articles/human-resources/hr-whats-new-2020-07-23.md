---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. juuli 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 23. juuli 2020 uusi või muutunud funktsioone.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 615d18865be20bfdce76d1f39ea73b220c171a8794c01b1ddfe11496fc2a658b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761898"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. juuli 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3416. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Finantsdimensioonide kustutamine positsioonil ei tööta ootuspäraselt (445476)

Dimensioonide eemaldamine positsioonilt eemaldab nüüd need samad positsioonid Dataverse'ist.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Positsioonide puhul, mis pole hierarhias, näidatakse passiivseid positsioone (397257)

Positsioonid, mis on passiivsed (kestus on aegunud), ei ole enam positsioonihierarhias kuvatud **positsioonidena, mis pole hierarhias**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Üksuste LeaveEnrollmentEntity ja HcmWorkerEntity vahel toimuv kontrollimine andmehaldusraamistiku (DMF) importimisel muudab andmete laadimise aeglaseks (442324)

Selles väljalaskes tehtud muudatused suurendavad üksuse **LeaveEnrollmentEntity** jõudlust.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Organisatsioonihalduses pole võimalik isikupärastada (447490)

Selle muudatuse tõttu saate nüüd **organisatsioonihalduses** linke isikupärastada.

## <a name="in-preview"></a>Eelvaates

## <a name="mandatory-fields"></a>Kohustuslikud väljad 

Saate nüüd muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil. See funktsioon nõuab **Salvestatud vaateid**.

## <a name="human-resources-application-in-teams"></a>Rakendus Human Resources Teamsis

Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams. Nad saavad suhelda botiga, et luua puhkusetaotlusi. Lisateavet vt teemast [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks
 
Välja tulevad soodustuste haldamise üksused. DMF-üksused võimaldavad teil andmeid importida ja eksportida, et lihtsalt soodustuste haldamist konfigureerida. Soodustuste haldamise mall on saadaval andmete teisaldamiseks. Mall ekspordib ja impordib andmeid andmesõltuvuste arvestamiseks järjestikku.

## <a name="buy-and-sell-leave"></a>Puhkuse ostmine ja müümine 

Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta. Seda protsessi hallatakse sageli käsitsi. See funktsioon muudab personaliosakonna jaoks poliitikate ja taotluste haldamise automaatseks. See muudab puhkusehalduse protsessi sujuvamaks ja aitab kõrvaldada vigu. Lisateabe saamiseks vt:

- [Puhkuse ostu ja müügi poliitikate haldamine](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Puhkuse ostmine ja müümine](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Puhkuse lisandumine üksiku ettevõtte või plaani puhul

Kliendid saavad töödelda lisandumisi üksiku ettevõtte või üksiku puhkuste ja puudumiste plaani puhul. See võimalus muudab lisandumisprotsessi selgemaks selliste klientide puhul, kellel on eri puhkuseaastad või puhkuse lisandumise poliitikad. Lisateavet leiate teemast [Puhkuse lisandumine ettevõtte või puhkuseplaani alusel](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Puhkusetaotlustele manuste lisamine

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

## <a name="checklist-entities-included-in-dataverse"></a>Dataverse'is kaasatud kontroll-loendi üksused

Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Dataverse'is.

## <a name="platform-changes"></a>Platvormi muudatused

Platvormi värskendus 10.0.12 (36)

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]