---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (08. juuli 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 8. juuli 2020 uusi või muutunud funktsioone.
author: andreabichsel
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 433eef4f11f385e85648d137521996a47a8ffd7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053919"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (8. juuli 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3382. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="database-logging"></a>Andmebaasi logimine

Andmebaasi logimine võimaldab teil kindlaks määrata, milliseid tabeleid ja välju tuleks jälgida. Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise. Saate kasutada andmebaasi logimise võimalusi, et aja jooksul neid muutusi näha. Lisateavet leiate teemast [Andmebaasi logimise konfigureerimine ja haldamine](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Töövõtja iseteeninduse nime konfigureerimine

Saate nüüd jaotises **Human Resources' parameetrites** muuta tööruumi **Töövõtja iseteenindus** nimeks **Iseteenindus**. Lisateavet leiate teemast [Töövõtja iseteeninduse tööruumi nime muutmine](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Soodustuste halduse avatud registreerimise juurdepääs väljaspool perioodi

Selles väljalaskes on parandatud viga, kus töötajad saavad juurdepääsu soodustuste avatud registreerimisele väljaspool registreerimisperioodi või ilma elusündmuseta. Selle tulemusena, kui vajate avatud registreerimise demo töövõtja iseteeninduses, peate kohandama avatud registreerimise kuupäevi tänaseks (või varasemaks), et muuta see kättesaadavaks. Seda sätet saate muuta jaotises **Soodustuste haldus > Reeglite ja valikute perioodid**.

## <a name="email-employee-enrollment-confirmation"></a>Töövõtja registreerimise kinnituse saatmine meili teel

Nüüd saate pärast soodustuste valimist töövõtjatele meile saata. Saate saata vaikimisi sõnumi või kasutada organisatsiooni meilimalli. Need sätted on jaotises **Inimressursside parameetrid > Soodustuste haldus**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Tühistatud puhkust kuvatakse endiselt inimeste tööruumi tulevase vaba aja all (441358)

Tühistatud puhkust ei kuvata enam tulevase vaba aja all puhkuse kaartidel tööruumis **Inimesed**.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Osakonna üksuse atribuuti ei saa kasutada PositionV2 üksuses (456486)

Nüüd saate lisada osakonna ilma topeltseost loomata.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity peaks kasutama pensioni plaanide puhul ainult arvutatud välja (459779)

Üksuse **PayrollWorkerEnrolledBenefitDetailEntity** eksportimisel määratleb eksportimine, kas see peaks kasutama arvutatud välja määra tabeli alusel või kasutama kindlustamistabeli välja **ContributionAmountCur**. Andmeüksuse kasutatav loogika kasutab määra tabelit olukordades, kus rakendus seda tavaliselt ei tee. See loogika põhjustab üksuse eksportimist, et tagastada null-väärtus selle veeru jaoks, kuna arvutuse määra tabelit pole ja toode ei luba kliendil seda määrata.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Segased tõlked Tšehhi keeles personalihalduses ja töövõtjate iseteeninduses (400276)

Selles väljalaskes on parandatud tõlked **Ettevõtte kataloog**, **Järgmine registreeritud kursus**, **Töö** ja **Ametikoht**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>Tabelis WorkCalendarEmployment pole loodud ja muudetud süsteemi väljad lubatud (460171)

Loodud ja muudetud süsteemi väljad on nüüd lubatud Human Resourcesi tabelis **WorkCalendarEmployment**.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Tühi viite erand tulevase töövõtja palkamise ja üksikasjade lisamise jaoks (455475)

Selles väljalaskes on parandatud tõrge (tühi viide) sujuvamas töövõtjate sisestamises, kui palkate töövõtja suvandi **Palkamise ja üksikasjade lisamine** abil.

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a>Dataverse'i töövõtja üksuses tehtud muudatused ei kajastu Human Resourcesis (455652)

Dataverse'i üksuse **Töövõtja** järgmistel väljadel tehtud muudatused kuvatakse nüüd Human Resourcesis.

- **Töötab kodus**
- **Staaž kuupäeval**
- **Tähtpäeva kuupäev**
- **Värbamise algne kuupäev**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Õige hüvituse tase ei ole vaikimisi ametikohale määratud töö alusel (394136)

Selle muudatusega on õiged hüvituse taseme vaikimisi jaotise **Hüvituse plaani määramine** suvandite **Ametikoha üksikasjad** ja **Alguskuupäev** kirjete **Kehtib alates** põhjal.

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

Kliendid saavad töödelda lisandumisi üksiku ettevõtte või üksiku puhkuste ja puudumiste plaani puhul. See võimalus muudab lisandumisprotsessi selgemaks selliste klientide puhul, kellel on eri puhkuseaastad või puhkuse viitvõla poliitikad. Lisateavet leiate teemast [Puhkuse lisandumine ettevõtte või puhkuseplaani alusel](hr-leave-and-absence-accrue.md).

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

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]