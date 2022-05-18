---
title: Dynamics 365 Human Resources infrastruktuuri ühendamise KKK
description: See teema vastab korduma kippuvatele küsimustele infrastruktuuri ühendamise kohta Microsofti ja Dynamics 365 Human Resources finantside ja toimingute rakendustele.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a905d752af2cf8397acb4927aa99edb4c23bfa6a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688116"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources infrastruktuuri ühendamise KKK

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



See teema vastab korduma kippuvatele küsimustele infrastruktuuri ühendamise kohta Microsofti ja Dynamics 365 Human Resources finantside ja toimingute rakendustele.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Mis on Dynamics 365 Human Resources infrastruktuuri ühendamine?

Dynamics 365 Human Resources on eraldiseisev rakendus, mis kasutab rakendusest Finantside ja toimingute rakendustest erinevat infrastruktuuri, nagu Dynamics 365 Finantsid Dynamics 365 Supply Chain Management, Dynamics 365 Commerce ja Dynamics 365 Project Operations. Infrastruktuuri ühendamine toob kaasa Dynamics 365 Human Resources samasse infrastruktuuri nagu teised Finantside ja toimingute rakendused.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktuuri ühendamise väärtus ja eelised

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources oma personalitoimingute haldamiseks. Milliseid soodustusi neist muudatustest näeb?

- Need muudatused eemaldavad Dynamics 365 HR mitme võimaluse komplektiga seotud segadused.
- Need pakuvad nii Microsoft Power Platform laiendatavust kui ka viisi äriloogika ja funktsioonivalikute laiendamiseks.
- Need toovad järjepidevust Dynamics 365 Human Resources muude finantside ja toimingute rakenduste vahel rakenduste elutsükli halduse (QI), Microsoft Dynamics elutsükli teenuste (LCS), geograafilise saadavuse, laiendatavuse ja muu mõistete poolest.
- Need lasevad teil kasutada jagatud teenuseid ja tööriistu ning aitavad kulusid vähendada.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Minu organisatsioon kasutab Moodulit Inimressursid Rakenduses Dynamics 365 Finantsid, Tarneahela haldus, Kaubandus ja Projektitoimingud. Milliseid soodustusi neist muudatustest näeb?

Tehtud võimalused ja investeeringud on nüüd Dynamics 365 Human Resources saadaval klientidele, kes kasutavad inimressursside moodulit rakenduses Dynamics 365 Finance. Mõned neist võimalustest hõlmavad puhkuse- ja puudumiste haldust, soodustuste haldust ja ülesannete haldust.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Kas ma kaotan mis tahes funktsioone või võimalusi, mida praegu kasutan?

Finantside ja toimingute rakendustes on Dynamics 365 Human Resources inimressursside mooduli ja inimressursside vahel funktsionaalne paarsus. Dynamics 365 Human Resources on sarnaste funktsioonide puhul eelistatum. Lisateavet vt [Funktsioonihalduse ülevaatest](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Kas see kogemus minu kasutajate jaoks muutub?

Uusi personalivõimalusi hallatakse funktsioonihalduse kaudu. Kliendid otsustavad, kas nad soovivad neid kasutada. Mõnel juhul võivad võimalused olla muudetud. Sellisel juhul pakutakse dokumentatsioon.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Kuidas mõjutab see muudatus mind, kui olen olemasolev klient ja ma kasutan nii inimressursside moodulit Finantside ja toimingute infrastruktuuris kui Dynamics 365 Human Resources ka kohandatud integratsioonide kaudu?

Dynamics 365 Human Resources Dynamics 365 Finance inimressursside mooduli ja inimressursside mooduli kohandatud integratsioonid pole enam vajalikud. Kõik inimressursside andmed asuvad samas andmebaasis kui teised Finantside ja toimingute rakendused.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Siirded Dynamics 365 Human Resources finantside ja toimingute rakendustesse

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources personalitoimingute haldamiseks. Mida on vaja uuele kogemusele migreerimise jaoks planeerida?

Kui teie organisatsioon kasutab Dynamics 365 Human Resources, kuid ei kasuta muid finantside ja toimingute rakendusi, migreeritakse teie inimressursid keskkonda uude infrastruktuuri. Suurem osa sellest migreerimisprotsessist automatiseeritakse. Teie andmebaasi migreerimiseks ja uue infrastruktuuriga sünkroonimiseks toimuvad protsessid.

Lisaks on tööriistamine olemas, et saate enne tootmiskeskkonna ülekandmist testida siirdeprotsessi ning kontrollida oma andmeid ja kogemust.

Kui teie organisatsioon kasutab nii Dynamics 365 Human Resources nii finantside kui ka operatsioonide rakendusi, peaksite planeerima kinnitamisele rohkem aega, et tagada andmete õige ülekandmine uude keskkonda. Siirded uude infrastruktuuri ühendavad teie Inimressursside keskkonna andmed teie finantside ja toimingute keskkonnaga. Vastuolulised andmed nõuavad siiski kasutaja sisestust, et määratleda konflikti lahendamine. Kasutajad ja administraatorid peavad haldama andmete vastendamist konfliktide korral ja testima migratsiooni liivakastikeskkondades enne tootmiskeskkondade üleviimist.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Minu organisatsioon kasutab Moodulit Inimressursid Rakenduses Dynamics 365 Finantsid, Tarneahela haldus, Kaubandus ja Projektitoimingud. Mida on vaja uuele kogemusele migreerimise jaoks planeerida?

Organisatsioonide puhul, mis kasutavad inimressursside moodulit finantside ja toimingute rakendustes, Dynamics 365 Human Resources rakendatakse teie keskkonnale uued funktsioonifunktsioonid standardse one versiooni uuendamise protsessi kaudu. Võite eeldada, et näete oma keskkonnas uusi funktsioone, kui need iga värskenduse korral kättesaadavaks saavad. Uute funktsioonide sisselülitamiseks saate kasutada funktsioonihaldust, kuid peaksite kavandama nende funktsioonide kinnitamist. Järgige oma keskkonna muude värskenduste valideerimiseks kasutatavaid protsesse. Lisateavet selle kohta, kuidas värskendusi finantside ja toimingute rakendustele rakendatakse, leiate ühest [versioonist](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Millal minu organisatsioon migreeritakse?

Iga organisatsiooni üleviimine sõltub selle praegusest konfiguratsioonist ja valmisolekust uude infrastruktuuri üle minna. Need kuupäevad võivad muutuda.

- Organisatsioonid, mis kasutavad inimressursside moodulit finantside ja toimingute Dynamics 365 Human Resources rakendustes saavad inimressursside funktsiooni osana tavalisest ühe versiooni uuendamise protsessist. Uute funktsioonide muutumine üldiselt kättesaadavaks alates jaanuarist 2022.
- Organisatsioonidel, kes kasutavad ainult rakendust Dynamics 365 Human Resources, on juurdepääs migratsioonitööriistadele, et nad saaksid alustada testimist ja alustada üleviimist alates 2022. aasta keskpaigast. Kuupäev, millal uuele infrastruktuurile migratsioon peab olema lõpetatud, pole veel määratletud. Kuid see on vähemalt üks aasta pärast kuupäeva, mil migreerimistööriista kasutamine muutub kättesaadavaks.
- Nii rakendust Finantsid Dynamics 365 Human Resources ja Toimingud kasutavad organisatsioonidel on juurdepääs migreerimise tööriistale, et nad saaksid alustada testimist ja käivitada siirde alguse 2022. aasta lõpus. Kuupäev, millal uuele infrastruktuurile migratsioon peab olema lõpetatud, pole veel määratletud. Kuid see on vähemalt üks aasta pärast kuupäeva, mil migreerimistööriista kasutamine muutub kättesaadavaks.

Lisateavet Dynamics 365 Human Resources uute funktsioonide kohta vt jaotisest [Mis on uut või muutunud rakenduses Human Resources](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Minu organisatsioon pole veel rakenduses Dynamics 365 Human Resources aktiivne. Kas me peaks koosnema Inimressursside moodulist Finantside ja toimingute rakendustes või rakendusega Dynamics 365 Human Resources pärand infrastruktuuris?

Oluline on kaaluda, milliseid inimressursside funktsionaalsusi on vaja ja millal see funktsionaalsus uues infrastruktuuris saadaval on. Kui organisatsioon vajab personalihalduse põhifunktsioone, mis on praegu saadaval finantside ja toimingute rakenduste inimressursside moodulis uues infrastruktuuris. Funktsiooni paarsus Dynamics 365 Human Resources finantside ja toimingute rakenduste inimressursside mooduli ja rakenduse vahel on eeldatavalt väljast 10.0.25, mis on planeeritud üldiselt kättesaadavaks märtsis 2022. Integreerimisfunktsioonid, nagu rakendus Teams ja Dataverse'i olemi integratsioonid on saadaval hilisemates väljaannetes.

Kui organisatsiooni personalifunktsioonid on saadaval uues infrastruktuuris ajavahemikus, milles organisatsioon hakkab edasi minema, võib olla lihtsam sisse minna inimressursside moodulisse finantside ja toimingute rakendustes. See lihtsustab migreerimist, kuna see on rakenduse Dynamics 365 Human Resources ja klient on juba uues infrastruktuuris sees. Kui organisatsioon otsustab aktiveerida end pärandinfrasktruktuuri rakenduses Dynamics 365 Human Resources, on uuele infrastruktuurile üleminekuks vaja keskkonna migreerimist. Seda saab vältida, kui aktiveerite uues infrastruktuuris.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Kasutan uusi võimalusi, mis on saadaval ainult rakenduses Dynamics 365 Human Resources (nt **Puhkus ja puudumine** ning **Soodustuste haldus**). Kas need võimalused on nüüd saadaval mooduli Finantsid ja toimingud infrastruktuuris Inimressursid?

Jah, kõik moodulid Dynamics 365 Human Resources töötavad nagu finance ja toimingute rakendustes ning funktsioonide paarsus on 100%. Osana üldisest migratsioonistrateegiast klientide jaoks, kes neid võimalusi inimressurssides kasutavad, migreeritakse kliendiandmed nii, et see jätkab tööd finantside ja toimingute infrastruktuuris.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Ma kasutan uusi Dynamics 365 Human Resources soodustuste haldamise võimalusi. Olen loonud kohandatud integratsiooni inimressursside mooduliga finantside ja toimingute infrastruktuuris, et kasutada palgafunktsioone soodustuste andmete abil. Kas need kohandatud integratsioonid on nõutavad edaspidi?

Osana infrastruktuuri ühendamisest tuuakse inimressursside andmed samasse andmebaasi kui teised finantside ja toimingute rakendused. Finantside ja toimingute rakenduste moodulite vahelist integratsiooni enam ei nõuta.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources üht või enamat ISV-lahendust. Kas meie ISV lahendused migreeritakse automaatselt?

Iga sõltumatu tarkvaratootja (ISV) lahenduse üleviimise kogemus varieerub sõltuvalt lahenduse integreerimismeetodist. Microsoft teeb tihedat koostööd ISV -dega, et tagada sujuv üleminek uuele infrastruktuurile.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon kasutab rakendusega Dynamics 365 Human Resources LinkedIn Talent Hub integreerimist. Kas integratsioon jätkab tööd pärast infrastruktuuri muudatuse lõpetamist?

Ei, LinkedIn Talent Hub integreerimine ei tööta pärast uude infrastruktuuri siirdamist. LinkedIn Talent Hubi integratsiooni teenus lõpeb rakenduse Dynamics 365 Human Resources pärandinfrastruktuuriga.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon kasutab Teamside jaoks Human Resources rakendust. Kas rakendus jätkab tööd pärast infrastruktuuri muudatuse lõpetamist?

Jah, Teamsi Human Resources rakendus jätkab tööd pärast uude infrastruktuuri siirdamist.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon on konfigureerinud rakenduses Dynamics 365 Human Resources kohandatud turbe. Kas pärast infrastruktuuri muudatuse lõpetamist rakendatakse endiselt kohandatud turvalisust?

Jah, kohandatud turvakonfiguratsioonid kaasatakse andmete migreerimisel uude infrastruktuuri.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Kasutame andmete integreerijat andmete teisaldamiseks rakenduste Finantsid Dynamics 365 Human Resources ja Toimingud vahel. Kuidas mõjutab see praegu integreeritavaid andmeid?

Praegu rakenduses Dynamics 365 Human Resources olevad inimressursside andmed sünkroonitakse Dataverse'i. Andmete integraatorit saab seejärel kasutada ühepoolese sünkroonimiseks Finantside ja toimingute rakendustega. Pärast siirdeid uude infrastruktuuri on inimressursside andmed finantside ja toimingute rakenduste jaoks omased. Andmeintegraator ei ole enam vajalik andmete sünkroonimiseks Finantside ja toimingute rakenduste ning Inimressursside vahel.

Praegused Dataverse personaliandmete tabelid sünkroonivad jätkuvalt uue infrastruktuuri keskkonnast pärit andmeid. Üksused teisendatakse topeltkirjutuse toetamiseks. Kõik muud andmete integreerimised, mis on konfigureeritud andmeintegraatori kaudu neile tabelitele teiste Dynamics 365 rakenduste jaoks, töötavad jätkuvalt nii, nagu need on praegu konfigureeritud.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Kasutame topeltkirjutust, et teisaldada inimressursside andmeid muude finantside Dataverse ja toimingute rakenduste vahel. Kuidas mõjutab praegu integreeritavaid andmeid uuele infrastruktuurile üleminek?

Inimressursside andmed on uues infrastruktuuris keskkonnas finantside ja toimingute rakenduste jaoks väljaminev. Topeltkirjutust kasutatakse personaliandmete teisaldamiseks uue keskkonna ja Dataverse keskkonna vahel.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Oleme loonud kohandatud integratsioonid rakendusest Dynamics 365 Human Resources ühte või enamasse välissüsteemi. Kas peame pärast infrastruktuuri muutmise lõpuleviimist arendama uusi integratsioone?

See sõltub integratsiooni lõpp-punktist. Lisateavet finantside ja toimingute rakendustes saadaoleva integratsioonitehnoloogiate ja parima integreerimistehnoloogia valiku kohta vt integreerimise [ülevaadet](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Oleme laiendanud Dataverse-i rakendusele Dynamics 365 Human Resources. Kas need laiendused migreeritakse automaatselt?

Kui finantside Dynamics 365 Human Resources ja toimingute keskkonnad, mis liitutakse uue infrastruktuuri keskkonnas, on Dataverse ühendatud sama keskkonnaga, Dataverse jätkatakse kahe rakenduse ühendamist sama keskkonnaga pärast migreerimist. Dataverse'i laienduste jaoks vaja migratsiooni.

Kui aga keskkonnad Dynamics 365 Human Resources Finantsid Dataverse ja Toimingud on praegu ühendatud eraldi keskkondadega, tuleb kaks keskkonda ühendada nii, Dataverse et need on ühendatud uue infrastruktuuri ühe keskkonnaga. Selle Dataverse migreerimise jaoks saab Human Resources lahenduste standardseid Dataverse tabeleid ühendada ja taassünkrooneerida uue Dataverse keskkonnaga. Kõiki Dataverse keskkonna laiendeid ei migreerita automaatselt, vaid need tuleb uues keskkonnas uuesti juurutada. Soovitame Dataverse laiendite haldamiseks kasutada hallatud lahendusi. Lisateavet vt [Sissejuhatus lahendustesse](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Oleme konfigureerinud Microsoft Power Automate vooge ja/või Microsoft Power Apps, mis töötaks rakendusega Dynamics 365 Human Resources. Kas need Microsoft Power Platform komponendid migreeritakse ja töötavad automaatselt pärast infrastruktuuri muudatuse lõpetamist?

Power Apps, Power Automate vood ja muud Microsoft Power Platform kohandamised on Dataverse laienditega sarnased. See, kas need töötavad automaatselt pärast siirdeid uude infrastruktuuri, sõltub sellest, kas Inimressursside rakendus ja finantside ja toimingute rakendused Power Apps on enne migreerimist ühendatud sama keskkonnaga.

Kui rakendused on praegu ühendatud sama Power Apps keskkonnaga, jätkatakse nende ühendamist selle Power Apps keskkonnaga pärast migreerimist uude infrastruktuuri. Sel juhul Power Apps, Power Automate vood ja muud Microsoft Power Platform kohandused jätkavad töötamist ilma lisakonfiguratsioonita. Soovitame Dataverse rakenduse laiendite haldamiseks kasutada hallatud lahendusi. Lisateavet vt [Sissejuhatus lahendustesse](/powerapps/developer/data-platform/introduction-solutions).

Kuid kui Inimressursid rakendus ja finantside ja toimingute rakendused on ühendatud eraldi Power Apps keskkondadega, tuleb need ühendada migreerimise osana. See ülesanne nõuab kõigi Power Apps ja muude kohanduste kordusjuurutamist uues keskkonnas.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Oleme lubanud Dataverse virtuaaltabelid rakenduses Dynamics 365 Human Resources. Mis toimub nende tabelitega migreerimise ajal?

Kui pärast migratsiooni jääb uue infrastruktuuri keskkond alles ühendatud Dataverse keskkonnaga, mis on praegu ühendatud rakendusega Dynamics 365 Human Resources, jätkavad selles keskkonnas loodud Dataverse virtuaalsed tabelid tööd ilma lisakonfiguratsioonita.

Kui aga uue infrastruktuuri keskkond on pärast migratsiooni ühendatud muu Dataverse keskkonnaga, tuleb virtuaalsed tabelid uues Dataverse keskkonnas uuesti luua.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Oleme välja arendanud integratsiooni, kasutades kandidaadi jälgimissüsteemi Applicant Tracking System (ATS) API-d, Payroll API-d, Dataverse virtuaaltabeleid Dynamics 365 Human Resources rakenduses või muid Dataverse Veebi API üksusi. Kas integratsioonid jätkavad tööd pärast infrastruktuuri muudatuse lõpetamist?

Kui pärast migratsiooni jääb uue infrastruktuuri keskkond alles ühendatud Dataverse keskkonnaga, mis on praegu ühendatud rakendusega Dynamics 365 Human Resources, kõik integratsioonid, mis on välja töötatud Dataverse Web API vastu, jätkavad tööd ka pärast migratsiooni.

Kui aga uue infrastruktuuri keskkond on pärast üleviimist ühendatud mõne teise Dataverse keskkonnaga, tuleb kõik Dataverse Web API vastu välja töötatud integratsioonid uuesti konfigureerida, et need saaksid ühenduse uue Dataverse keskkonnaga.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Kas minu keskkonna üleviimisel mõjutab see Azure'i piirkonda?

Eeldatakse, et teie Human Resources keskkond jääb tavaliselt migreerimise ajal samasse Azure'i piirkonda. Ainus erand on see, kui Inimressursid keskkond ühendatakse finantside ja toimingute keskkonnaga, mis on teises regioonis. Sel juhul migreeritakse Inimressursside keskkond Finantside ja toimingute keskkonna Azure'i regiooni.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Minu organisatsioon sõltub ühe või mitme Dynamics 365 Human Resources äriprotsessi töövoogudest. Kas töövood viiakse automaatselt üle?

Jah, töövoo konfiguratsioonid, töövoo ajalugu ja praegused protsessi töövood migreeritakse.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Millised koolitus- ja ressursid on migreerimisprotsessis abiks?

Antakse täielik dokumentatsioon, et kirjeldada üksikasjalikult kõiki migreerimisprotsessi etappe. Sõltuvalt vajadusest võivad saadaval olla ka täiendavad koolitusressursid, nt videod ja töökojad.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Minu organisatsioon on liidese kasutatavuse parandamiseks loonud salvestatud vaated rakendusse Dynamics 365 Human Resources. Kas salvestatud vaated viiakse automaatselt üle?

Jah, salvestatud vaated migreeritakse uude infrastruktuuri.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Me kasutame Dynamics 365 Human Resources-i koos Ceridaniga. Kas Ceridiani integratsioon on saadaval pärast infrastruktuuri muutmise lõpuleviimist? 

Integratsioon Ceridaniga migreeritakse Palgaarvestuse API-põhisesse integratsiooni. Failipõhist integratsiooni, mis on praegu olemas Dynamics 365 Human Resources, ei kannata üle finantside ja toimingute infrastruktuuri. Lisateavet vt [Palgaarvestuse API sissejuhatus](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Kuidas mõjutab migreerimine teenuse värskendusprotsessi?

Pärast migreerumsit on klientidel ALM -i ja teenuste värskenduste osas palju rohkem paindlikkust. Teenuse värskendusi ei rakendata enam automaatselt Human Resources keskkondadele. Selle asemel järgib teenus One Versioni teenuse värskendamise protsesse ja funktsioone. Seetõttu on värskenduste konfiguratsioonivalikud saadaval LCS-i kaudu. Lisateavet leiate teemast [One Version ülevaade](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Kuidas mõjutab migratsioon minu Dynamics 365 Human Resources LCS-projekti?

Siirded uude infrastruktuuri teisaldavad teie keskkondade Dynamics 365 Human Resources halduse LCS-i finantside ja toimingute rakendusprojekti. Kui siirded ühendatakse olemasoleva Dynamics 365 Human Resources finants- ja operatsioonikeskkonnaga, ühendatakse teie Inimressursside LCS-projekt LCS-i rakendusprojektiga Finantsid ja toimingud rakenduse jaoks. Kui kasutate praegu ainult rakendust Dynamics 365 Human Resources, luuakse uus LCS-i rakendusprojekt ja teie olemasolev Human Resources LCS-projekt migreeritakse uude projekti.

Uus projekt on sama tüüpi projekt, mida finantside ja toimingute rakendused kasutavad. Sellel on keskkonnahalduse jaoks samad funktsioonid ja funktsionaalsus. Lisateabe saamiseks vt [Lifecycle Servicesi ressursid](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Oleme oma ülesannete salvestused sidunud äriprotsesside modelleerijaga rakenduses Human Resources. Kuidas äriprotsessi modelleerija migreeritakse ja LCS-i ühendatakse?

LCS-projekti äriprotsesside teegid viiakse üle uude Human Resources LCS-projekti.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Minu organisatsioon kasutab praegu ainult rakendust Dynamics 365 Human Resources. Millised ressursid on saadaval, et saaksime pärast infrastruktuurimuutuse lõpuleviimist arendusvõimaluste kohta rohkem teada saada?

Saadaval Microsoft Power Platform on nii laiendatavuse valikud kui ka finantside ja toimingute laiendatavusvalikud ning neid saab kasutada arendamiseks. Lisateavet vt [Avalehe arendamine ja kohandamine](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Oleme lubanud Dynamics 365 Human Resources funktsioonid. Kas need funktsioonid lubatakse migreerimise ajal automaatselt?

See, kas funktsioon on uues infrastruktuuris automaatselt lubatud, määratakse iga funktsiooni puhul eraldi. See teave kaasatakse funktsiooni dokumentatsiooni.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Mis toimub minu BYOD-andmebaasiga migreerimise ajal?

Importige ja eksportige konfiguratsioone oma andmebaasi (BYOD) toomiseks.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Mis toimub minu Azure Data Lake migreerimise ajal?

Iga eksport, mis on praegu konfigureeritud finantside Azure Data Lake Storage ja toimingute rakendustes, haldab pärast migreerimist sama konfiguratsiooni.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Kasutame praegu Dynamics AX 2012-d. Kas praegu saadaolevaid täiendustööriistu kasutatakse AX 2012 personalimooduli uuendamiseks rakenduseks Dynamics 365 Human Resources?

Jah. Dynamics 365 Human Resources kaasatakse ühendatud koodibaasi ja finantside ja toimingute rakenduste infrastruktuuri. Dynamics AX 2012 Dynamics 365 Human Resources värskendus kasutab sama täiendusteed ja tööriistad, mida kasutatakse finantside ja toimingute rakenduste uusimale versioonile täiendamiseks.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Dokumendi käsitlemist kasutatakse koos rakendusega Dynamics 365 Human Resources. Mis toimub dokumentidega migreerimise ajal?

Dokumendid jäävad olemasolevasse dokumendisalve. Need lisatakse uuesti uuele infrastruktuurile.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Mis toimub pärast migreerimist Dynamics 365 Human Resources konfigureeritud partiitöödega?

Kohaldatavad partiitööd migreeritakse automaatselt uude infrastruktuuri.

## <a name="licensing-impact"></a>Litsentsimise mõju

See dokumentatsioon ei alista ega asenda mis tahes juriidilist dokumentatsiooni, mis hõlmab kasutusõigusi.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Minu organisatsioon kasutab Dynamics 365 Human Resources oma personalitoimingute haldamiseks. Kas meie litsentsimine või kulud muutuvad?

Dynamics 365 Human Resources litsentse ostnud kliente see ei mõjuta. Sellel kliendil puudub litsentside migratsioon. Täiendav liivakasti varude hoidmise üksus (SKU), mis oli spetsiifiline rakendusega Human Resources, ei kehti enam. Selle asemel saavad kliendid valida finantside ja toimingute rakenduste 2. taseme kausta ostmise veidi väiksema kuluga. Inimressursside sisendkausta ostnud olemasolevad kliendid migreeritakse lisakuluta finantside ja toimingute rakenduste järgu 2 kausta.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Minu organisatsioon kasutab Moodulit Inimressursid Rakenduses Dynamics 365 Finantsid, Tarneahela haldus, Kaubandus ja Projektitoimingud. Kas mu litsentsimine või kulud muutuvad?

Dynamics 365 rakenduste olemasolevad kasutajad ja iseseisev Dynamics 365 finance, tarneahela haldus, äri ja projektitoimingud pääsevad inimressurssidele nende litsentside osana kuni veebruarini 2025 või kuni praeguse litsentsilepingu aegumiseni, olenevalt sellest, kumb on varasem. Võite minna varem Human Resources litsentsidele üle, kui see aitab saavutada paremat kulude kokkuhoidu. Alates 2025. veebruarist peavad kõik olemasolevad CSP ja EA kliendid inimressursside mooduli maha võtma ja ostma inimressursside litsentsid, et kasutada uusi võimalusi, mida finantside ja toimingute rakendustele tuuakse.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Minu organisatsioon on reaalajas dynamics 365 Finantsid, Tarneahela haldus, Kaubandus või Projektitoimingud. Kas infrastruktuuri ühendamise toetamiseks on vaja osta täiendavat keskkonda?

Infrastruktuuri muudatuse toetamiseks pole lisakeskkondasid vaja.

