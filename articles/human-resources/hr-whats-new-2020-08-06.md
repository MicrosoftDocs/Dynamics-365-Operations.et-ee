---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (06. august 2020)?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 06. augusti 2020 uusi või muutunud funktsioone.
author: darinkramer
manager: AnnBe
ms.date: 8/06/2020
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
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 94d8291190b6c08c6e0e5241513989354df7939d
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3711838"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (06. august 2020)?

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3444. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="platform-update-1001236-is-now-available"></a>Platvormivärskendus 10.0.12(36) on nüüd saadaval

Lisateavet leiate teemast [Finance and Operationsi rakenduste versiooni 10.0.12 platvormivärskendused (august 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks
 
Välja tulevad soodustuste haldamise üksused. DMF-üksused võimaldavad teil andmeid importida ja eksportida, et lihtsalt soodustuste haldamist konfigureerida. Soodustuste haldamise mall on saadaval andmete teisaldamiseks. Mall ekspordib ja impordib andmeid andmesõltuvuste arvestamiseks järjestikku. Lisateabe saamiseks vt:

- [DMF-üksuse tugi](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis
- [Andmehalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire loob töövoo puhkusetaotluste ostmiseks ja müümiseks (446557)

Lisateabe saamiseks vt:

- [Töötajatele puhkuse ostmise ja müümise lubamine](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
- [Puhkuse ostu ja müügi poliitikate haldamine](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Puhkuse ostmine ja müümine](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>Üksusel „Töötaja postiaadressid V2” on juurdepääs kõikidele piiratud juurdepääsuga juriidilistele isikutele (459126)

Selle muudatusega põhineb üksuse **Töötaja postiaadressid V2** piirang kasutajale antud juriidilise isiku juurdepääsul.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Töövoo e-kirja hüperlink ei ava asjakohaseid arvustusi (437398)

Kui kasutate arvustuse töövoos tulemuslikkuse arvustuse avamiseks kohatäidet, avab nüüd e-kirjas loodud hüperlink valitud kirje.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Uued üksused puhkuse ostmiseks ja müümiseks (473180)

Puhkuse ostmiseks ja müümiseks on nüüd saadaval andmehaldusraamistiku üksused. Lisateavet leiate teemast [Andmehalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Kirjeteabe vaatamisel ja täpsemate filtrite kasutamisel võib kasutaja pääseda juurde teiste töötajate kirjetele (472490)

Selle muudatusega pääsevad töövõtja iseteeninduse kasutajad töövõtja iseteenindust kasutades juurde ainult oma kirjetele. Filtreerimissuvandite muutmise ajal kirjeteabe vaatamisel ei paljastata enam muid andmeid.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Personalihalduse analüüs sisaldab lahkunud töötajate kirjeid (382893)

Selle väljalaskega hõlmab personalihalduse analüüs nüüd ainult aktiivseid töötajaid. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Töövõtja lisatasu suurenemist ei saa töödelda (473125)

See muudatus võimaldab uue lisatasu suurenemise jõustumise kuupäeva muutes lisatasu suurenemisi sisestada.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Arvustuse töövoogu saab alustada rohkem kui üks kord (467541)

Selle muudatusega saate alustada tulemuslikkuse arvustuse töövoogu ainult ühe korra. Halduri oleku puhul ei kuvata enam arvustuse alustamise suvandit.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Puhkusetaotluse töövoog lõpeb kinnitatud puhkusetaotluse tühistamisel tõrkega (472063)

Kui tühistate selles väljalaskes kinnitatud puhkusetaotluse, ei jää taotluse olek enam kinnitatuks ja töövoog jätkub.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Süsteem soovitab malli põhjal uue arvustuse loomisel lahkunud töötajaid (460624)

Selle muudatusega pole lahkunud töötajad enam malli põhjal uute arvustuse loomisel saadaval. Te ei saa luua arvustusi töötajate jaoks, kes pole veel tööle hakanud või kes on töökohalt lahkunud.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Ametikoha hierarhia ringviite tuvastus (415879)

Selle muudatusega põhineb ametikoha hierarhia ringviite tuvastamine ainult ühel ajahetkel. Saate käitada ringviite tuvastamise eri kuupäevade jaoks, et kontrollida, et aruandlusstruktuuris poleks ühtegi ringviidet.

## <a name="buy-and-sell-leave"></a>Puhkuse ostmine ja müümine 

Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta. Seda protsessi hallatakse sageli käsitsi. See funktsioon muudab personaliosakonna jaoks poliitikate ja taotluste haldamise automaatseks. See muudab puhkusehalduse protsessi sujuvamaks ja aitab kõrvaldada vigu. Lisateabe saamiseks vt:

- [Töötajatele puhkuse ostmise ja müümise lubamine](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
- [Puhkuse ostu ja müügi poliitikate haldamine](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-buy-and-sell-leave-policies)
- [Puhkuse ostmine ja müümine](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-buy-sell-leave)

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

## <a name="in-preview"></a>Eelvaates

### <a name="mandatory-fields"></a>Kohustuslikud väljad

Saate muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil. See funktsioon nõuab **Salvestatud vaateid**. Lisateavet salvestatud vaadete kohta leiate siit.

- [Salvestatud vaated – üldine kättesaadavus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
- [Koostage vorme, mis täielikult kasutavad salvestatud vaateid](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Rakendus Human Resources Teamsis

Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams. Nad saavad suhelda botiga, et luua puhkusetaotlusi. Lisateabe saamiseks vt:

- [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis
- [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-üksus on saadaval lisandumise peatamiseks

Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.

## <a name="coming-soon"></a>Peagi tulekul

## <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service'is kaasatud kontroll-loendi üksused

Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Common Data Service'is.

## <a name="known-issues"></a>Teadaolevad probleemid

Tööruumis **Funktsioonihaldus** võidakse kuvada funktsioone, mis on eelvaatefunktsioonidena keelatud, kuigi need on üldiselt kättesaadavad. Allpool on loend üldiselt kättesaadavatest funktsioonidest, mille olek on vale. 

1.  Soodustuste haldus
2.  Juhtumihaldus
3.  Andmebaasi logimine (auditeerimine)
4.  Puhkuse lisandumine ühe ettevõtte või ühe plaani kohta
5.  Puhkuste ja puudumiste lisandumise peatamine
6.  Saldo korrigeerimise põhjusekood ja kommentaar
7.  Puhkuse ostmine ja müümine
8.  Puhkuste ja puudumiste kalender
9.  Puhkuse edasikandmise reeglid
10. Puhkuse lisandumise auditeerimine
11. Puhkuse lisandumise kustutamine
12. Puhkuse lisandumise ümardamine
13. Ühel puhkuseplaanil mitme puhkusetüübi konfigureerimine
14. Eemalolekuaja täiustuste värskendamine
15. Lisandumiste jaoks töövõtja täistööaja vaste kasutamine
16. Ettevõtteülene hüvitusevaade
17. Jõudluse ülevaadete printimine
18. Puhkuse lisandumise parandused

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)