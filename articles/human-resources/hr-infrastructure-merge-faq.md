---
title: Dynamics 365 Human Resources infrastruktuuri ühendamise KKK
description: See artikkel vastab korduma kippuvatele küsimustele infrastruktuuri ühendamise kohta Microsofti ja Dynamics 365 Human Resources finantside ja toimingute rakenduste kohta.
author: twheeloc
ms.date: 09/13/2021
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
ms.openlocfilehash: 32698d887b4d228ded588984b09068e3e2fef9a4
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702063"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources infrastruktuuri ühendamise KKK

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="what-is-dynamics-365-human-resources"></a>Mis on Dynamics 365 Human Resources?

Microsoft Dynamics 365 Human Resources pakub tööriistu, mis aitavad inimressursside töörühmadel organisatsioonilist alandust suurendada, töötajakogemust muuta ja optimeerida inimressursside programme, et luua töökoha, kus inimesed ja ettevõte saavad areneda. Lisateavet vt Dynamics 365 Human Resources teemast [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Töötajakogemuste teisendamine.** Säilitage tipptöötajad, volitades juhatajaid ja töötajaid ühendatud iseteeninduskogemuste kaudu, mis juhtida kaasamist ja kasvu.
- **Optimeerige inimressursside programme.** Vähendada tegevuskulusid ning luua töötajatega seotud puhkus ja puudumine, aeg, soodustus ja kompensatsiooni haldusprogrammid.
- **Organisatsioonilise alandsuse suurendamine.** Lubage inimressurssidel töötada arukusega, mida ettevõte vajab inimeste andmete Dataverse Microsoft Power Platform abil ja tsentraliseerituks ning laiendada hõlpsasti Dynamics 365 Human Resources.
- **Saate avastada tööjõuülevaated.** Saate andmepõhiste otsuste langetada läbi võime analüüsida ja visualiseerida mis tahes seadmes salvestatud rikaste armatuurlaudade andmeid.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktuuri ühendamise väärtus ja eelised

### <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Mis on Dynamics 365 Human Resources infrastruktuuri ühendamine?

Dynamics 365 kahes erinevas infrastruktuuris on praegu kaks eraldi inimressursside funktsioonikomplekti:

- **Dynamics 365 Human Resources**– eraldi rakendus, mida käitatakse iseseisvas infrastruktuuris. Rakenduse käivitamisel eraldati infrastruktuur muudest Dynamics 365 toimingute rakendustest. Meie kliendid kasutavad seda rakendust organisatsiooni alandsuse suurendamiseks, inimressursside programmide optimeerimiseks, töötajakogemuste teisendamiseks ja tööjõuülevaadete saamiseks.
- **Inimressursside moodul** – võimaluste pärandkomplekt, mis oli eelnevalt osa Unified Operationsi litsentsimise varude raamatupidamisühikust (SKU). Inimressursside moodul töötab finantside ja toimingute infrastruktuuris, mis on sama kõigis toimingute rakendustes. Nende rakenduste hulka kuuluvad Dynamics 365 Finance ja Dynamics 365 Project Operations Dynamics 365 Supply Chain Management. Kliendid said inimressursside võimalused Dynamics 365 Finance või <a0/& osana Dynamics 365 Supply Chain Management.

Viimase kolme aasta jooksul pole Microsoft lisanud inimressursside moodulile uusi võimalusi ega täiustusi. Selle asemel on meie hiljutised investeeringud rakendusele keskenud Dynamics 365 Human Resources.

Neid kahte võimaluste kogumeid samale infrastruktuurile viies aitame klientidel saada järgmisi soodustusi:

- Viimase kolme aasta jooksul lisatud täiustused Dynamics 365 Human Resources, sh täiustatud puhkus ja puudumine, soodustushaldus ja aruandlus.
- Täiustatud laiendatavus läbi ja Microsoft Power Platform võime laiendada äriloogikat lehekülgede isikupärastamiseks.
- Täiustatud juurutamine, uuendused ja hooldus, mis on järjepidevad rakenduse töötsükli halduses (OLEVAD), elutsükli teenused, geograafiline saadavus jne.
- Rohkem lisakulu, kui meie tehnikameeskond kasutab jagatud teenuseid, tööriistamist ja vähendatud platvormi kulusid.

See siirde mõjutab kliente, kes kasutavad praegu kas moodulit Dynamics 365 Human Resources Hr või pärandi inimressursside moodulit.

## <a name="glossary-of-terms-used-in-this-faq"></a>Selles KKK-s kasutatavate terminite sõnastik

- **Dynamics 365 Human Resources**: meie praegune ja tulevane toode, mis pakub inimressursside võimalusi turule.
- **Inimressursside moodul** – pärandvõimaluste kogum, mis oli eelnevalt litsentsitud ühendatud operatsioonide pakkumisega. Võimalused on lubatud, kui kliendil on Dynamics 365 Finance või Dynamics 365 Supply Chain Management.
- **Finantside ja toimingute infrastruktuurid** – arendusarhitektuur, mida kasutatakse operatsioonides, sh Dynamics 365 Finance ja Dynamics 365 Supply Chain Management Dynamics 365 Project Operations. Seda infrastruktuuri kasutatakse edasisuunas. Selles KKK-s viitab termin *ühendatud infrastruktuur* finants- ja toimingute keskkonnale.
- **Inimressursside infrastruktuur** – arendusarhitektuur, mida rakenduse jaoks ajalooliselt Dynamics 365 Human Resources kasutati. Infrastruktuuri ühendamise projekt toob finantside Dynamics 365 Human Resources ja toimingute infrastruktuuri. Autonoomset infrastruktuuri ei saa enam kasutada.

## <a name="general-questions-about-the-infrastructure-merge"></a>Üldised küsimused infrastruktuuri ühendamise kohta

### <a name="will-customers-lose-any-features-or-capabilities"></a>Kas kliendid kaotavad mis tahes funktsioone või võimalusi?

Meie eesmärk on vähendada siirde mõju klientidele. Me ei eemalda ühtegi funktsiooni ega võimalusi. Inimressursside mooduli vahel on funktsionaalne Dynamics 365 Human Resources paarsus. Kui funktsioon on olemas mõlemas infrastruktuuris, Dynamics 365 Human Resources kasutatakse seda kogemust.

### <a name="will-the-user-experience-change"></a>Kas kasutajakogemus muutub?

Kasutajakogemus on kooskõlas standardse Dynamics 365 platvormikogemusega. Kuigi armatuurlauda ja menüüde üldkogemus jääb sarnased, joondada see standardse Dynamics 365 Finance App Experience’iga. Navigeerimine hõlmab nii mooduleid kui ka tööruume, lubab lemmikuid jne. Tööruumid Dynamics 365 Human Resources, nt Personalihaldus **ja** Inimesed **·**, ühendatakse finantside ja toimingute infrastruktuuri. Tulevikus tarnitakse uued võimalused Funktsioonihalduse kaudu, mille abil kliendid saavad vaadata uusi funktsioone ja otsustada, milliseid neid kasutada soovite. Lisateavet vt Funktsioonihalduse ülevaatest [ja](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) Kasutajaliidese [dokumentatsioonist](../fin-ops-core/fin-ops/get-started/user-interface-elements.md?toc=/dynamics365/human-resources/toc.json).

### <a name="when-will-the-dynamics-365-human-resources-infrastructure-merge-be-completed"></a>Millal infrastruktuuri Dynamics 365 Human Resources ühendamine lõpule viiakse?

Infrastruktuuri ühendamine toimub faasides, andes klientidele aega vajalike sammude plaanimiseks ja täitmiseks. Dynamics 2021 väljastusvoos 2 alustasime väljapööramist. Plaanime lõpetada kõik tootearenduse katsed selle projekti jaoks 2022. aasta väljalaskevoo 2 lõpuks. Pange tähele, et ajajooni tuleb muuta. Kõige ajasemat teavet vt [väljalaskeplaanidest](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="what-training-and-resources-will-be-available-to-help-with-the-infrastructure-merge"></a>Millised koolitus- ja ressursiressursid on infrastruktuuri ühendamisel abiks?

Esitage dokumentatsioon, mis kirjeldab üksikasjalikult infrastruktuuri ühendamise protsessi etappe. Anname täiendavad koolitusressursid, nagu näiteks videod ja töötoad, mis on vajalikud klientide ja partnerite sujuvaks üleminekuks.

### <a name="will-there-be-changes-in-development-capabilities-after-the-infrastructure-merge-is-completed"></a>Kas arendusvõimalustes tuleb pärast infrastruktuuri ühendamist teha muudatusi?

Lisateavet arendusvõimaluste kohta vt "Avalehe [arendamine ja kohandamine"](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

## <a name="feature-availability-questions"></a>Funktsiooni saadavuse küsimused

### <a name="will-the-linkedin-talent-hub-integration-work-on-the-finance-and-operations-infrastructure"></a>Kas LinkedIn Anne’i keskuse integreerimine töötab finantside ja operatsioonide infrastruktuuris?

Ei, LinkedIn Anne’i keskuse integratsioon ei ole ühendatud infrastruktuuri osa. Avaliku rakenduse programmeerimisliidesed (API-d) on saadaval integratsioonide ehitamiseks värbamis- ja kandidaadi jälgimise lahendustega. Kliendid, kes plaanivad kasutada LinkedIn Anne’i keskust peaksid töötama koos Oma Microsofti partneriga, et integreerida, kasutades antud API-sid. Lisateavet kandidaadi jälgimissüsteemi (ATS) integratsiooni API-de kohta vt kandidaadi [jälgimissüsteemi integreerimise API sissejuhatusest](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-capabilities-that-are-currently-available-only-in-dynamics-365-human-resources-for-example-leave-management-and-benefits-management-be-available-after-the-merge-is-completed"></a>Kas praegu saadaolevad võimalused (Dynamics 365 Human Resources nt puhkuste haldus ja soodustuste haldus) on pärast ühendamist saadaval?

Jah. Kõiki Dynamics 365 Human Resources rakenduse võimalusi tuuakse finantside ja toimingute infrastruktuuri. Funktsioonid tehakse kättesaadavaks etapiviisilise lähenemise puhul. Ühendatud infrastruktuuri funktsiooni saadavaloleku ajastatud teabe saamiseks vaadake väljalaskeplaane regulaarselt [üle](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-finance).

### <a name="will-ceridian-integrations-with-dynamics-365-human-resources-be-available-after-the-infrastructure-merge-is-completed"></a>Kas Ceridani integratsioonid on Dynamics 365 Human Resources pärast infrastruktuuri ühendamise lõpetamist saadaval?

Ceridani protsess loob V2 integratsiooni, mis Dynamics 365 Human Resources kasutab ära palga API-sid. Failipõhist integratsiooni, mis on praegu olemas Dynamics 365 Human Resources, ei kannata üle finantside ja toimingute infrastruktuuri. Lisateavet vt [Palgaarvestuse API sissejuhatus](./hr-admin-integration-payroll-api-introduction.md).

### <a name="will-applicant-tracking-or-onboardingoffboarding-of-employees-functionality-be-included"></a>Kas kaasata tuleks kandidaadi jälgimine või töötaja funktsiooni sisse- või väljalülitamine?

Varasemates väljalasetes oleme loonud ATS-integratsiooni API, et võimaldada partneritel ja klientidel luua ATS-integratsioonid Inimressurssidega. ATS-iga seotud lisafunktsioonid muutusid kättesaadavaks 2022. voos 1. Jätkame nende API-de täiustamist tulevastes väljalasetes.

Inimressursside funktsioon, mis on praegu finantside ja toimingute infrastruktuuris olemas, sisaldab mõningaid värbamishalduse funktsioone, mida pole olemas Dynamics 365 Human Resources. Kui infrastruktuuri ühendamine on lõpule viidud, on see funktsioon saadaval kõigi Inimressursside klientide jaoks. See funktsioon pakub kergeid ATS-i funktsioone. Kuid me ei plaani seda funktsiooni tulevikus laiendada. Kliendid, kes vajavad täpsemat funktsiooni, saavad kasutada partneri ATS-integratsiooni. Lisateavet ATS-integratsiooni API-de kohta vt kandidaadi [jälgimissüsteemi integratsiooni API sissejuhatusest](./hr-admin-integration-ats-api-introduction.md).

### <a name="will-the-dynamics-ax-2012-upgrade-tools-be-used-to-upgrade-the-hr-module-in-ax-2012-to-the-dynamics-365-human-resources-app"></a>Kas Dynamics AX 2012 täiendustööriistu kasutatakse AX inimressursside mooduli täiendamiseks rakenduses 2012 Dynamics 365 Human Resources rakenduseks?

Jah. Versioonilt Dynamics AX 2012 Dynamics 365 Human Resources versioonitäiendus järgib sama täiendustee ja tööriistade versiooni, mida kasutatakse dynamics 365 toimingute rakenduste (nt Dynamics 365 Finantsid või ) uusimale versioonile täiendamiseks Dynamics 365 Supply Chain Management.

Lisateavet finantside ja toimingute infrastruktuuri migreerimise kohta vt Inimressursside [kliendi migratsiooni KKK-st](./customer-migration.md).
