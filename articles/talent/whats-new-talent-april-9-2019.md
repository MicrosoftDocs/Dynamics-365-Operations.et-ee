---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (9. aprill, 2019)?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4959f28e0768d43f90a664022c714a126c88e38d
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856420"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-9-2019"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (9. aprill, 2019)?

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Dynamics 365 for Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) integreerimine funktsiooniga "probleemist teavitamine"
Attractis ja Onboardis loovad nüüd lõppkasutajate logitud probleemid, mis on saadetud probleemist teavitamise funktsiooniga, kliendi LCS-i projektis probleemi. Administraatorid saavad seejärel neid probleeme hinnata ja esitada vajadusel Microsoftile. See vastab sellele, kuidas Core HR lõppkasutaja probleeme käsitleb.

### <a name="relevance-search"></a>Asjakohasuse otsing
Talendikaustades saate nüüd kogu kandidaatide andmebaasist otsida teatud oskusi, nimesid või hariduskäiku. Enam ei pea te määratlema, millist osa kandidaatide profiilist te soovite läbi otsida. Attract otsib kogu profiilist ja tõstab esile leitud vasted. Attract otsib ka kõigist kandidaadile saadaolevatest dokumentidest ja järjestab intelligentselt otsingutulemused. Lisaks sellele saate tulemusi filtreerida allika järgi, või selle järgi, kas nad on hõbemedalistid. Lisateabe saamiseks vt [Kandidaatide profiilide otsimine ja vaatamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).

### <a name="prospect-recommendations"></a>Potentsiaalselt sobiva kandidaadi soovitamine
Attract võib and töötaja otsimisele kiire stardi kohe, kui selle käivitate, tehes intelligentseid kandidaatide soovitusi teie organisatsiooni kandidaatide andmebaasist. Soovitused sisaldavad vastavaid kandidaate otsides tuvastatud oskuste ja hariduse infot. Need soovitused kuvatakse vahekaardil **Potentsiaalselt sobivad kandidaadid**, kui olete selle töö värbamisprotsessis lubanud. Lisateavet vt teemast [Potentsiaalselt sobiva kandidaadi soovitamine](https://docs.microsoft.com/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).

### <a name="interviewer-availability-statuses"></a>Vestluse saadavuse olekud
Vestluse planeerijad saavad varsti näha intervjuueerijate olekut **Kontorist väljas, töötab mujal**, mis aitab planeerida intervjueerijatele paremini sobivaid aegu.

### <a name="candidate-interview-experience-save-calendar-invites"></a>Kandidaadi intervjuu kogemus: kalendris kutsete salvestamine
Kandidaadid saavad nüüd oma intervjuu sündmusi alla laadida ja isiklikku kalendrisse salvestada, kasutades kandidaadile intervjuu kokkuvõtte meiliga saadetud .ics faili.

## <a name="changes-in-onboard"></a>Muutused Onboardis

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a>Lifecycle Services (LCS) integreerimine probleemist teavitamise funktsiooniga
Attractis ja Onboardis loovad nüüd lõppkasutajate logitud probleemid, mis on saadetud probleemist teavitamise funktsiooniga, kliendi LCS-i projektis probleemi. Administraatorid saavad seejärel neid probleeme hinnata ja esitada vajadusel Microsoftile. See vastab sellele, kuidas Core HR lõppkasutaja probleeme käsitleb.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused
Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2225.

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a>Muutuvate plaanide aluse protsent laeb vale summa
Selle nädala väljaanne parandab probleemi ergutussüsteemi preemiate laadimisel protsendipõhiseid plaane kasutades.
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a>Viimase töötatud päeva kuupäevavalija ei tööta õigesti
Selle muudatusega parandatakse probleemi: kui kasutaja redigeerib **Töösuhte lõppkuupäeva** ja valib kalendrist kuupäeva, lisatakse päev valikusse.

###  <a name="limit-personnel-action-types-by-the-action-taken"></a>Personali tegevuse tüüpide piiramine sooritatud tegevuse järgi
See muudatus piirab teatud tegevuste sooritamisel kuvatavaid tegevuse tüüpe. Näiteks, kui taotletakse uut ametikohta, kuvatakse tegevuste loendis ainult uue ametikohaga seotud tegevusi. Varem kuvati nii uusi, kui ka muutmise tegevusi. 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a>Töötaja koos hüvitisega üleviimine teise juriidilisse isikusse
See väljaanne võimaldab hüvitise lõpetamist teises juriidilises isikus, kui üleviimine toimub ettevõtete vahel.

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a>Ei ole võimalik valida hüvitist tulevaseks töötamiseks üleviimise ajal
Töötaja uute juriidilisse isikusse üleviimisel saate nüüd määrata hüvitise uuele juriidilisele isikule üleviimise protsessi ajal.

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a>Kasutaja ei saa määrata ametikoha määramise ajal hüvitist
Uue ametikoha määramise lisamine võimaldab nüüd põhipalga kirjete määramise. 

## <a name="in-preview"></a>Eelvaates

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Puhkuse tüüpidele põhjusekoodide määramise lubamine
Organisatsioonid võivad vajada puhkuseavaldustega seotud lisanduvat infot. Nüüd saate määrata puhkuse tüüpidega seotud põhjusekoodid ja lubada töötajatel valida põhjusekood oma puhkuseavaldusele.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Teatud tüüpi puhkusetüüpidele ja puhkuseavaldustele põhjusekoodide nõudmine
Organisatsioonid võivad nõuda teatud puhkusetüüpide korral töötajate esitatud puhkuseavaldustele põhjusekoodide määramist. See võib toimuda vastavalt ettevõtte poliitikale või regulatiivsetele nõuetele. Nüüd saate määrata, milline puhkusetüüp vajab põhjusekoodi ja saate nõuda, et töötaja esitab oma puhkuseavaldusel oma puhkusetüübile põhjusekoodi.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Personaliosakonnale puhkuse ja puudumise kannete nimekirja esitamine
Töötajate puhkuseaja jälgimine ja mõistmine, kuidas puhkus on arvestatud, mitte ainult ei aita personaliosakonnal vastata töötajate küsimustele, vaid võimaldab ka töötajatele täpse puhkusehüvitise. Personaliosakonnal on nüüd uus tehingute vaade (hüvitused, viitvõlad, korrigeerimised ja taotlused), et näha saldode taga olevaid põhjuseid. 

## <a name="coming-soon"></a>Peagi tulekul

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Kasutajaliidesele täiustused töötajate duplikaatide kontrollimiseks
Selle muudatusega tuvastatakse nimeväljade sisestamisel duplikaadid ja olek näitab leitud duplikaatide arvu. Võite uue lehe avamiseks valida antud lingi, et hinnata, kas kasutada tuvastatud vastet. Andmesisestuse katkestamise vältimiseks ei avane duplikaatide vorm automaatselt.

###  <a name="email-support-for-alerts"></a>E-posti tugi teatistele
Platvormi värskendusega 25 saavad kasutajad luua teavituse reegleid, mis saadavad kontaktidele automaatselt sündmuse käivitatud meiliteateid. 
