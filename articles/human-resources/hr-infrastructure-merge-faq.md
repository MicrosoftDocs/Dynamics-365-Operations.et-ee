---
title: Dynamics 365 Human Resources infrastruktuuri ühendamise KKK
description: See teema vastab korduma kippuvatele küsimustele infrastruktuuri ühendamise kohta Microsoft Dynamics 365 Human Resources ja Finance and Operations rakenduste jaoks.
author: rachel-profitt
ms.date: 07/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 537917e9a987d701a0c96dfb7592e124e09bb748e4f2f52d39f8d97000c70ae3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711997"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources infrastruktuuri ühendamise KKK

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

See teema vastab korduma kippuvatele küsimustele infrastruktuuri ühendamise kohta Microsoft Dynamics 365 Human Resources ja Finance and Operations rakenduste jaoks.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Mis on Dynamics 365 Human Resources infrastruktuuri ühendamine?

Dynamics 365 Human Resources on eraldi rakendus, mis kasutab Finance and Operations rakendustest erinevat infrastruktuuri nt Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Project Operations. Infrastruktuuri ühendamine toob Dynamics 365 Human Resources samasse infrastruktuuri nagu teised Finance and Operations rakendused.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktuuri ühendamise väärtus ja eelised

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources oma personalitoimingute haldamiseks. Milliseid soodustusi neist muudatustest näeb?

- Need muudatused eemaldavad Dynamics 365 HR mitme võimaluse komplekti.
- Need pakuvad nii Microsoft Power Platform laiendatavust kui ka viisi äriloogika ja funktsioonivalikute laiendamiseks.
- Need toovad järjepidevust rakenduste Dynamics 365 Human Resources ja teiste Finance and Operations vahel rakenduste elutsükli halduse (ALM), Microsoft Dynamics Lifecycle Services (LCS), geograafilise saadavuse, laiendatavuse jne mõistes.
- Need lasevad teil kasutada jagatud teenuseid ja tööriistu ning aitavad kulusid vähendada.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources rakenduses Dynamics 365 Finance, Supply Chain Management, Commerce või Project Operations. Milliseid soodustusi neist muudatustest näeb?

Dynamics 365 Human Resources valmistatud võimalused ja investeeringud on nüüd saadaval klientidele, kes kasutavad Dynamics 365 Finance personalimoodulit. Mõned neist võimalustest hõlmavad puhkuse- ja puudumiste haldust, soodustuste haldust ja ülesannete haldust.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Kas ma kaotan mis tahes funktsioone või võimalusi, mida praegu kasutan?

Rakendustes Dynamics 365 Human Resources ja Finance and Operations personalimooduli vahel on funktsionaalne paarsus. Dynamics 365 Human Resources on sarnaste funktsioonide puhul eelistatum. Lisateavet vt [Funktsioonihalduse ülevaatest](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Kas see kogemus minu kasutajate jaoks muutub?

Uusi personalivõimalusi hallatakse funktsioonihalduse kaudu. Kliendid otsustavad, kas nad soovivad neid kasutada. Mõnel juhul võivad võimalused olla muudetud. Sellisel juhul pakutakse dokumentatsioon.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Kuidas see muudatus mind mõjutab, kui olen olemasolev klient ja kasutan nii Finance and Operations infrastruktuuri personalimoodulit kui ka kohandatud integratsioonide kaudu Dynamics 365 Human Resources?

Dynamics 365 Human Resources ja Dynamics 365 Finance personalimooduli kohandatud integratsioonid pole enam vajalikud. Kõik personaliandmed asuvad samas andmebaasis kui teised Finance and Operations rakendused.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Dynamics 365 Human Resources migratsioon Finance and Operations rakendustesse

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources personalitoimingute haldamiseks. Mida on vaja uuele kogemusele migreerimise jaoks planeerida?

Kui teie organisatsioon kasutab Dynamics 365 Human Resources, kuid ei kasuta muid Finance and Operations rakendusi, migreeritakse teie personalikeskkond uude infrastruktuuri. Suurem osa sellest migreerimisprotsessist automatiseeritakse. Teie andmebaasi migreerimiseks ja uue infrastruktuuriga sünkroonimiseks toimuvad protsessid.

Lisaks on tööriistamine olemas, et saate enne tootmiskeskkonna ülekandmist testida siirdeprotsessi ning kontrollida oma andmeid ja kogemust.

Kui teie organisatsioon kasutab nii Dynamics 365 Human Resources kui ka muid Finance and Operations rakendusi, peaksite kinnitamisele lisama aja, et tagada andmete õige ülekandmine uude keskkonda. Uuele infrastruktuurile migreerimine ühendab teie personalikeskkonna andmed Finance and Operations keskkonnaga. Tööriistad on loodud selleks, et automatiseerida võimalikult palju andmete ühendamise protsessi. Vastuoluliste andmete eksemplarid nõuavad siiski kasutaja sisestust, et määratleda konflikti lahendamine. Kasutajad ja administraatorid peavad haldama andmete vastendamist konfliktide korral ja testima migratsiooni liivakastikeskkondades enne tootmiskeskkonna üleviimist.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources rakenduses Dynamics 365 Finance, Supply Chain Management, Commerce või Project Operations. Mida on vaja uuele kogemusele migreerimise jaoks planeerida?

Organisatsioonid, mis kasutavad Finance and Operations rakendustes personalimoodulit, rakendatakse teie keskkonnas uued Dynamics 365 Human Resources funktsioonid standardse ühe versiooni uuendamise protsessi kaudu. Võite eeldada, et näete oma keskkonnas uusi funktsioone, kui need iga värskenduse korral kättesaadavaks saavad. Funktsioonide haldamise abil saate uusi funktsioone sisse lülitada. Nende funktsioonide kinnitamist peaksite siiski plaanima. Järgige oma keskkonna muude värskenduste valideerimiseks kasutatavaid protsesse. Lisateavet Finance and Operations rakenduste värskenduste rakendamisest vt teemast [Ühe versiooni ülevaade](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Millal minu organisatsioon migreeritakse?

Iga organisatsiooni üleviimine sõltub selle praegusest konfiguratsioonist ja valmisolekust uude infrastruktuuri üle minna. Need kuupäevad võivad muutuda.

- Organisatsioonid, mis kasutavad Finance and Operations rakendustes personalimoodulit saab Dynamics 365 Human Resources personalifunktsioonid tavalise versiooni uuendamise protsessi raames. Uute funktsioonide muutumine üldiselt kättesaadavaks alates oktoober 2021.
- Organisatsioonidel, kes kasutavad praegu ainult rakendust Dynamics 365 Human Resources, on juurdepääs migratsioonitööriistadele, et nad saaksid alustada testimist ja alustada üleviimist alates 2022. aasta keskpaigast. Kuupäev, millal uuele infrastruktuurile migratsioon peab olema lõpetatud, pole veel määratletud. Kuid see on vähemalt üks aasta pärast kuupäeva, mil migreerimistööriista kasutamine muutub kättesaadavaks.
- Organisatsioonidel, kes kasutavad hetkel nii Dynamics 365 Human Resources kui ka Finance and Operations rakendust, on juurdepääs migratsioonitööriistadele, et nad saaksid alustada testimist ja alustada üleviimist alates 2022. aasta lõpust. Kuupäev, millal uuele infrastruktuurile migratsioon peab olema lõpetatud, pole veel määratletud. Kuid see on vähemalt üks aasta pärast kuupäeva, mil migreerimistööriista kasutamine muutub kättesaadavaks.

Lisateavet Dynamics 365 Human Resources uute funktsioonide kohta vt jaotisest [Mis on uut või muutunud rakenduses Human Resources](./hr-admin-whats-new.md).

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Kasutan uusi võimalusi, mis on saadaval ainult rakenduses Dynamics 365 Human Resources (nt **Puhkus ja puudumine** ning **Soodustuste haldus**). Kas need võimalused on nüüd saadaval ka Finance and Operations infrastruktuuri moodulis Human Resources?

Jah, kõik Dynamics 365 Human Resources moodulid töötavad nagu nad on Finance and Operations rakendustes ja funktsioonide paarsus on 100%. Osana üldisest migratsioonistrateegiast klientidele, kes praegu kasutavad neid võimalusi personalitöös, viiakse kliendiandmed üle nii, et need töötaksid jätkuvalt Finance and Operations infrastruktuuriga.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Ma kasutan uusi Dynamics 365 Human Resources soodustuste haldamise võimalusi. Ma lõin kohandatud integratsiooni Finance and Operations infrastruktuuri personalimooduliga, et kasutada soodustuste andmeid palgaarvestuste võimaluste eelistena. Kas need kohandatud integratsioonid on nõutavad edaspidi?

Infrastruktuuri ühinemise osana tuuakse personaliandmed samasse andmebaasi teiste Finance and Operations rakendustega. Finance and Operations rakenduste moodulite vahelist integratsiooni enam ei nõuta.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources üht või enamat ISV-lahendust. Kas meie ISV lahendused migreeritakse automaatselt?

Iga sõltumatu tarkvaratootja (ISV) lahenduse üleviimise kogemus varieerub sõltuvalt lahenduse integreerimismeetodist. Microsoft teeb tihedat koostööd ISV -dega, et tagada sujuv üleminek uuele infrastruktuurile.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon kasutab rakendusega Dynamics 365 Human Resources LinkedIn Talent Hub integreerimist. Kas integratsioon jätkab tööd pärast infrastruktuuri muudatuse lõpetamist?

Jah, LinkedIn Talent Hub integreerimine jätkab tööd pärast uude infrastruktuuri siirdamist.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon kasutab Teamside jaoks Human Resources rakendust. Kas rakendus jätkab tööd pärast infrastruktuuri muudatuse lõpetamist?

Jah, Teamsi Human Resources rakendus jätkab tööd pärast uude infrastruktuuri siirdamist.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon on konfigureerinud rakenduses Dynamics 365 Human Resources kohandatud turbe. Kas pärast infrastruktuuri muudatuse lõpetamist rakendatakse endiselt kohandatud turvalisust?

Jah, kohandatud turvakonfiguratsioonid kaasatakse andmete migreerimisel uude infrastruktuuri.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Kasutame andmete integreerijat andmete teisaldamiseks rakenduste Dynamics 365 Human Resources ja Finance and Operations vahel. Kuidas mõjutab see praegu integreeritavaid andmeid?

Praegu koondunud personaliandmeid sünkroniseeritakse rakenduses Dynamics 365 Human Resources rakendusega Dataverse. Andmete integraatorit saab seejärel kasutada ühesuunaliseks sünkroonimiseks Finance and Operations rakendustega. Pärast migratsiooni uude infrastruktuuri on personaliandmed Finance and Operations rakenduste jaoks omased. Andmete integraator ei ole enam vajalik andmete sünkroonimiseks Finance and Operations rakenduste ja Human Resources vahel.

Praegused Dataverse personaliandmete tabelid sünkroonivad jätkuvalt uue infrastruktuuri keskkonnast pärit andmeid. Üksused teisendatakse topeltkirjutuse toetamiseks. Kõik muud andmete integreerimised, mis on konfigureeritud andmeintegraatori kaudu neile tabelitele teiste Dynamics 365 rakenduste jaoks, töötavad jätkuvalt nii, nagu need on praegu konfigureeritud.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Kasutame topeltkirjutust, et teisaldada personaliandmeid akenduste Dataverse ja Finance and Operations vahel. Kuidas mõjutab praegu integreeritavaid andmeid uuele infrastruktuurile üleminek?

Personaliandmed on natiivsed uue infrastruktuuri keskkonna Finance and Operations rakendustele. Topeltkirjutust kasutatakse personaliandmete teisaldamiseks uue keskkonna ja Dataverse keskkonna vahel.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Oleme loonud kohandatud integratsioonid rakendusest Dynamics 365 Human Resources ühte või enamasse välissüsteemi. Kas peame pärast infrastruktuuri muutmise lõpuleviimist arendama uusi integratsioone?

See sõltub integratsiooni lõpp-punktist. Lisateavet rakendustes Finance and Operations saadaval olevate integreerimistehnoloogiate ja neist parima integratsioonitehnoloogia valimise kohta leiate teemast [Integratsiooni ülevaade](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Oleme laiendanud Dataverse-i rakendusele Dynamics 365 Human Resources. Kas need laiendused migreeritakse automaatselt?

Kui Dynamics 365 Human Resources ja Finance and Operations keskkonnad, mis liituvad uue infrastruktuuri keskkonnaga, on ühendatud sama Dataverse keskkonnaga, jätkatakse kahe rakenduse ühendamist sama Dataverse keskkonnaga pärast migratsiooni. Seetõttu pole Dataverse laienduste jaoks vaja migratsiooni.

Samas, kui Dynamics 365 Human Resources ja Finance and Operations keskkonnad on ühendatud eraldiseisvate Dataverse keskkondadega, peavad kaks Dataverse keskkonda olema ühendatud nii, et nad oleks ühendatud uue infrastruktuuri ühe keskkonnaga. Selle Dataverse migreerimise jaoks saab Human Resources lahenduste standardseid Dataverse tabeleid ühendada ja taassünkrooneerida uue Dataverse keskkonnaga. Kõiki Dataverse keskkonna laiendeid ei migreerita automaatselt, vaid need tuleb uues keskkonnas uuesti juurutada. Soovitame Dataverse laiendite haldamiseks kasutada hallatud lahendusi. Lisateavet vt [Sissejuhatus lahendustesse](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Oleme konfigureerinud Microsoft Power Automate vooge ja/või Microsoft Power Apps, mis töötaks rakendusega Dynamics 365 Human Resources. Kas need Microsoft Power Platform komponendid migreeritakse ja töötavad automaatselt pärast infrastruktuuri muudatuse lõpetamist?

Power Apps, Power Automate vood ja muud Microsoft Power Platform kohandamised on Dataverse laienditega sarnased. See, kas need töötavad pärast uude infrastruktuuri üleviimist automaatselt, sõltub sellest, kas Human Resouces ja Finance and Operations rakendused on enne üleviimist ühendatud sama Power Appsi keskkonnaga.

Kui rakendused on praegu ühendatud sama Power Apps keskkonnaga, jätkatakse nende ühendamist selle Power Apps keskkonnaga pärast migreerimist uude infrastruktuuri. Sel juhul Power Apps, Power Automate vood ja muud Microsoft Power Platform kohandused jätkavad töötamist ilma lisakonfiguratsioonita. Soovitame Dataverse rakenduse laiendite haldamiseks kasutada hallatud lahendusi. Lisateavet vt [Sissejuhatus lahendustesse](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

Kui aga Human Resources rakendus ja Finance and Operations rakendused on ühendatud eraldi Power Apps keskkondadega, tuleb need ühendada migreerimise osana. See ülesanne nõuab kõigi Power Apps ja muude kohanduste kordusjuurutamist uues keskkonnas.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Oleme lubanud Dataverse virtuaaltabelid rakenduses Dynamics 365 Human Resources. Mis toimub nende tabelitega migreerimise ajal?

Kui pärast migratsiooni jääb uue infrastruktuuri keskkond alles ühendatud Dataverse keskkonnaga, mis on praegu ühendatud rakendusega Dynamics 365 Human Resources, jätkavad selles keskkonnas loodud Dataverse virtuaalsed tabelid tööd ilma lisakonfiguratsioonita.

Kui aga uue infrastruktuuri keskkond on pärast migratsiooni ühendatud muu Dataverse keskkonnaga, tuleb virtuaalsed tabelid uues Dataverse keskkonnas uuesti luua.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Oleme välja arendanud integratsiooni, kasutades kandidaadi jälgimissüsteemi Applicant Tracking System (ATS) API-d, Payroll API-d, Dataverse virtuaaltabeleid Dynamics 365 Human Resources rakenduses või muid Dataverse Veebi API üksusi. Kas integratsioonid jätkavad tööd pärast infrastruktuuri muudatuse lõpetamist?

Kui pärast migratsiooni jääb uue infrastruktuuri keskkond alles ühendatud Dataverse keskkonnaga, mis on praegu ühendatud rakendusega Dynamics 365 Human Resources, kõik integratsioonid, mis on välja töötatud Dataverse Web API vastu, jätkavad tööd ka pärast migratsiooni.

Kui aga uue infrastruktuuri keskkond on pärast üleviimist ühendatud mõne teise Dataverse keskkonnaga, tuleb kõik Dataverse Web API vastu välja töötatud integratsioonid uuesti konfigureerida, et need saaksid ühenduse uue Dataverse keskkonnaga.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Kas minu keskkonna üleviimisel mõjutab see Azure'i piirkonda?

Eeldatakse, et teie Human Resources keskkond jääb tavaliselt migreerimise ajal samasse Azure'i piirkonda. Ainus erand esineb siis, kui personalikeskkond liidetakse Finance and Operations keskkonnaga, mis asub teises piirkonnas. Sel juhul migreeritakse Human Resources keskkond Finance and Operations keskkonna Azure'i piirkonda.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Minu organisatsioon sõltub ühe või mitme Dynamics 365 Human Resources äriprotsessi töövoogudest. Kas töövood viiakse automaatselt üle?

Jah, töövoo konfiguratsioonid, töövoo ajalugu ja praegused protsessi töövood migreeritakse.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Millised koolitus- ja ressursid on migreerimisprotsessis abiks?

Antakse täielik dokumentatsioon, et kirjeldada üksikasjalikult kõiki migreerimisprotsessi etappe. Sõltuvalt vajadusest võivad saadaval olla ka täiendavad koolitusressursid, nt videod ja töökojad.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Minu organisatsioon on liidese kasutatavuse parandamiseks loonud salvestatud vaated rakendusse Dynamics 365 Human Resources. Kas salvestatud vaated viiakse automaatselt üle?

Jah, salvestatud vaated migreeritakse uude infrastruktuuri.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Me kasutame Dynamics 365 Human Resources-i koos Ceridaniga. Kas Ceridiani integratsioon on saadaval pärast infrastruktuuri muutmise lõpuleviimist? 

Integratsioon Ceridaniga migreeritakse Palgaarvestuse API-põhisesse integratsiooni. Failipõhist integratsiooni, mis on hetkel rakenduses Dynamics 365 Human Resources olemas, ei migreerita Finance and Operations infrastruktuuri. Lisateavet vt [Palgaarvestuse API sissejuhatus](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Kuidas mõjutab migreerimine teenuse värskendusprotsessi?

Pärast migreerumsit on klientidel ALM -i ja teenuste värskenduste osas palju rohkem paindlikkust. Teenuse värskendusi ei rakendata enam automaatselt Human Resources keskkondadele. Selle asemel järgib teenus One Versioni teenuse värskendamise protsesse ja funktsioone. Seetõttu on värskenduste konfiguratsioonivalikud saadaval LCS-i kaudu. Lisateavet leiate teemast [One Version ülevaade](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Kuidas mõjutab migratsioon minu Dynamics 365 Human Resources LCS-projekti?

Uuele infrastruktuurile migreerimine teisaldab teie Dynamics 365 Human Resources keskkonnahalduse LCS-i rakendusprojekti. Kui migreerimine ühendab Dynamics 365 Human Resources olemasoleva Finance and Operations keskkonnaga, ühendatakse teie Human Resources LCS-projekt rakenduse Finance and Operations LCS-i rakendusprojekti. Kui kasutate praegu ainult rakendust Dynamics 365 Human Resources, luuakse uus LCS-i rakendusprojekt ja teie olemasolev Human Resources LCS-projekt migreeritakse uude projekti.

Uus projekt on sama tüüpi projekt, mida Finance and Operations rakendused kasutavad. Sellel on keskkonnahalduse jaoks samad funktsioonid ja funktsionaalsus. Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Oleme oma ülesannete salvestused sidunud äriprotsesside modelleerijaga rakenduses Human Resources. Kuidas äriprotsessi modelleerija migreeritakse ja LCS-i ühendatakse?

LCS-projekti äriprotsesside teegid viiakse üle uude Human Resources LCS-projekti.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon kasutab praegu ainult rakendust Dynamics 365 Human Resources. Millised ressursid on saadaval, et saaksime pärast infrastruktuurimuutuse lõpuleviimist arendusvõimaluste kohta rohkem teada saada?

Saadaval on nii Microsoft Power Platform kui ka Finance and Operations laiendatavuse valikud ning neid saab kasutada arendamiseks. Lisateavet vt [Avalehe arendamine ja kohandamine](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Oleme lubanud Dynamics 365 Human Resources funktsioonid. Kas need funktsioonid lubatakse migreerimise ajal automaatselt?

See, kas funktsioon on uues infrastruktuuris automaatselt lubatud, määratakse iga funktsiooni puhul eraldi. See teave kaasatakse funktsiooni dokumentatsiooni.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Mis toimub minu BYOD-andmebaasiga migreerimise ajal?

Importige ja eksportige konfiguratsioone oma andmebaasi (BYOD) toomiseks.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Mis toimub minu Azure Data Lake migreerimise ajal?

Iga eksportimine, mis on praegu rakenduste Finance and Operations valikus Azure Data Lake Storage konfigureeritud, haldab pärast migreerimist sama konfiguratsiooni.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Kasutame praegu Dynamics AX 2012-d. Kas praegu saadaolevaid täiendustööriistu kasutatakse AX 2012 personalimooduli uuendamiseks rakenduseks Dynamics 365 Human Resources?

Jah. Dynamics 365 Human Resources kaasatakse Finance and Operations rakenduste ühendatud koodibaasi ja infrastruktuuri. Uuendamine versioonilt Dynamics AX 2012 versioonile Dynamics 365 Human Resources kasutab sama täiendustee ja tööriistu, mida kasutatakse rakenduse Finance and Operations uusimale versioonile üleviimiseks.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Dokumendi käsitlemist kasutatakse koos rakendusega Dynamics 365 Human Resources. Mis toimub dokumentidega migreerimise ajal?

Dokumendid jäävad olemasolevasse dokumendisalve. Need lisatakse uuesti uuele infrastruktuurile.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Mis toimub pärast migreerimist Dynamics 365 Human Resources konfigureeritud partiitöödega?

Kohaldatavad partiitööd migreeritakse automaatselt uude infrastruktuuri.

## <a name="licensing-impact"></a>Litsentsimise mõju

See dokumentatsioon ei alista ega asenda mis tahes juriidilist dokumentatsiooni, mis hõlmab kasutusõigusi.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources oma personalitoimingute haldamiseks. Kas meie litsentsimine või kulud muutuvad?

Dynamics 365 Human Resources litsentse ostnud kliente see ei mõjuta. Sellel kliendil puudub litsentside migratsioon. Täiendav liivakasti varude hoidmise üksus (SKU), mis oli spetsiifiline rakendusega Human Resources, ei kehti enam. Selle asemel saavad kliendid valida rakenduste Finance and Operations 2. taseme liivakasti veidi väiksema maksumusega. Olemasolevad kliendid, kes on ostnud inimressursside liivakasti, viiakse ilma lisatasuta üle Finance and Operations rakenduste 2. järgi liivakasti.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources rakenduses Dynamics 365 Finance, Supply Chain Management, Commerce või Project Operations. Kas mu litsentsimine või kulud muutuvad?

Dynamics 365 rakenduste olemasolevad kasutajad ja Dynamics 365 Finance, Supply Chain Management, Commerce ja Project Operations kasutajad pääsevad Human Resouces juurde nende litsentside osana kuni veebruarini 2025 või kuni praeguse litsentsilepingu aegumiseni, olenevalt sellest, kumb toimub varem. Võite minna varem Human Resources litsentsidele üle, kui see aitab saavutada paremat kulude kokkuhoidu. Alates veebruarist 2025 peavad kõik olemasolevad CSP- ja EA -kliendid personalimooduli maha võtma ja ostma Human Resources litsentsid, et kasutada ära uusi võimalusi, mida rakenduses Finance and Operations pakutakse.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Minu organisatsioon kasutab reaalajas rakendusi Dynamics 365 Finance, Supply Chain Management, Commerce või Project Operations. Kas infrastruktuuri ühendamise toetamiseks on vaja osta täiendavat keskkonda?

Infrastruktuuri muudatuse toetamiseks pole lisakeskkondasid vaja.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Kuhu ma peaks minema, kui mul on toote litsentsimise kohta täiendavaid küsimusi?

Kui teil on litsentsi kohta küsimusi, leiate lisateavet teemast [Biz Apps Hub – D365 hinnakujundus ja litsentsimine](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Kui see teave ei aita teie probleemi lahendada, avage päring LicenseQ abil.
