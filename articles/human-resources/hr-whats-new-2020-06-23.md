---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (25. juuni 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 23. juuni 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 28eecb6289e5e895e860cffa29a55e773c6aadaa
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528713"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. juuni 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3347. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Kui lõpetatud töötaja registreering aegub, tühjendatakse vormilt Puhkuse registreerimine puhkuse tüüp, saldo ja summa (444867)

Selle valiku tegemisel säilitatakse nüüd väljade **Puhkuse tüüp**, **Saldo** ja **Summa** väärtused nende tühjendamise asemel.

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Vale prognoositud saldo uue funktsiooni (Ühe ettevõtte või lepingu puhkuse viitvõlg) lubamisel (456553)

Nüüd kuvatakse õige prognoositud saldo, kui ühe ettevõtte või lepingu puhkuse viitvõlg on lubatud.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Seostega üksused, mille tulemuseks on dubleeritud navigeerimisatribuudid (456486)

Selles väljaandes on parandatud mitme üksuse navigeerimisatribuutidega (seosega) seotud probleem. Tuvastatakse dubleeritud seosed. Need stsenaariumid on kõik parandatud.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Kontsernisisesed kommentaarid tulemuslikkuse hindamises (455536)

Selle parandusega kuvatakse nüüd kontsernisiseseid kommentaare tulemuslikkuse hindamises. Selle muudatusega on parandatud läbivaatajate kommentaaride vaade, mis sisestati sama tulemuslikkuse ülevaate jaoks erinevates ettevõtetes.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Ebakõla hüvituse halduse andmete kuvamisel (432562)

Hüvituse andmete ühtset vaadet säilitatakse nüüd Juhi iseteeninduses. Sõltuvalt sellest, kuidas te liigute töötaja **Hüvituse üksikasjadesse**, kuvatakse juhtidele hüvituse andmeid nüüd ühtselt.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Põhipalgaplaani kehtivuse alguseks on vaikimisi tänane kuupäev (411994)

Hüvituse alguskuupäev määratakse nüüd töötajale määratud ametikoha alguskuupäeva järgi.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Puhkuste ja puudumiste vorm Luba pooliku päeva määratlus on keelatud uue vormi avamisel (452607)

Selle muudatusega lubatakse **Luba pooliku päeva määratlus** senikaua, kuni on olemas uued puhkuse kanded. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Olemisse HcmDiscussionEntity ei saa Exceli kaudu avaldada. Välja TotalRatingScore tõrge (453899)

Saate nüüd värskendada välja **TotalRatingScore** olemi **HCMDiscussionEntity** abil Exceli töövihiku kujundajas.

## <a name="in-preview"></a>Eelvaates

## <a name="database-logging"></a>Andmebaasi logimine

Andmebaasi logimine võimaldab teil kindlaks määrata, milliseid tabeleid ja välju tuleks jälgida. Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise. Saate kasutada andmebaasi logimise võimalusi, et aja jooksul neid muutusi näha. Lisateavet leiate teemast [Andmebaasi logimise konfigureerimine ja haldamine](hr-admin-database-logging.md).

## <a name="mandatory-fields"></a>Kohustuslikud väljad 

Saate nüüd muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil. See funktsioon nõuab **Salvestatud vaateid**.

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

## <a name="configure-the-name-of-employee-self-service"></a>Töövõtja iseteeninduse nime konfigureerimine

Jaotises **Human Resourcesi parameetrid** on saadaval uus suvand, et muuta töövõtja iseteeninduse tööruumi nimi iseteeninduseks.

## <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service'is kaasatud kontroll-loendi üksused

Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Common Data Service'is.

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)