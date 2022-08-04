---
title: Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine
description: See artikkel annab teavet elutsükli Microsoft Dynamics teenuste (LCS) talletuse amortiseerumise kohta, mis on plaanitud regulatiivse konfiguratsiooniteenuse (RCS) globaalse hoidla väljamineku osana.
author: JaneA07
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, LCS storage, LCS storage deprecation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.19
ms.openlocfilehash: 65d45eaf618075e0c78881634fc77bda0fab277e
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065670"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) kasutamine elektroonilise aruandluse (ER) konfiguratsiooni talletushoidlana on aegunud. See aegumine hõlmab järgmisi muudatusi:

- Microsofti loodud konfiguratsioone, mida kasutatakse Microsoft Dynamics 365 rakendustes, ei avaldata enam LCS-i jagatud vara teegis. Selle asemel avaldatakse need ainult RCS-i globaalse hoidla kaudu. Dynamics AX 2012 konfiguratsioone avaldatakse siiski LCS-is ühiskasutusega varateegis kuni AX 2012. aasta tugitsükli lõpuni.
- Funktsioon, mis võimaldab teil finantside ja toimingute rakendustest ja RCS-st üles laadida konfiguratsioone LCS-i projekti varateeki, inaktiveeritakse. Siiski, saate kasutada LCS-i brauserit konfiguratsioonide üleslaadimiseks Projekti varateeki. Seega saate LCS-ile siiski konfiguratsioone lisada, et neid saaks lisada lahendusepakettidesse.
- Konfiguratsioonide importimine LCS-st on finantside ja toimingute rakendustes ning RCS-is teatud ajal edaspidi saadaval ja toetatud. Siiski, funktsioon lõpuks aegub. (Täpne aegumise kuupäev teatatakse hiljem.)

## <a name="deprecation-notice"></a>Aegumisteatis

LCS-i kasutuse alistus ladustamisena Dynamics 365 Finance - LCS-i [teatise eemaldatud või taunitud funktsioonide kaudu](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Planeeritud aegumiskuupäev on 1. aprill 2022.

## <a name="key-features"></a>Võtmefunktsioonid

- Kasutage RCS-i ER-i konfiguratsioonide ja globaliseerimisfunktsioonide loomiseks ja muutmiseks.
- Lükake konfiguratsioone otse RCS-kujundajast ühendatud rakendusse, nt Dynamics 365 Finance'i keskkonda, nii et saate konfiguratsioonides teha ja katsetada kiiresti muudatusi.
- Keskselt salvestage, jagage ja hallake nii ER-i konfiguratsioonide kui ka globaliseerimisfunktsioonide elutsüklit globaalse hoidla tsentraliseeritud salvestusruumi kaudu.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Juhis ühekordsete ja jooksvate tegevuste jaoks

Selles jaotises kirjeldatakse samme, mis tuleb üks kord lõpule viia. See kirjeldab ka samme, mida tuleb hiljem jooksval alusel täita.

### <a name="one-time-action"></a>Ühekordne tegevus

Importige kõik nõutavad konfiguratsioonid LCS-st RCS-i ja salvestage need RCS-st globaalsesse hoidlasse. Kui kasutate LCS-is tuletatud konfiguratsioonide tallemiseks projektipõhiseid varateeke, tuleb LCS-ile juurdepääsemiseks lõpetada järgmised sammud.

1. Kui RCS-i eksemplar ei ole juba saadaval, tehke üks pakkumine. Lisateavet vt teemast [RCSi ülevaade](rcs-overview.md).
2. Eraldise kantud RCS-eksemplaris registreerige varateegi iga LCS-projekti jaoks, mis sisaldab tuletatud ER-konfiguratsioone, sobiv LCS-i hoidla.
3. Importige ER-konfiguratsioonid LCS-i hoidlatest RCS-i. Lisateabe saamiseks vt teemat [Konfiguratsioonide importimine LCS-ist](/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services).
4. Kui globaalset hoidlat automaatselt ei sisestata, registreerige see RCS-i.
5. Laadige kõik praegusest RCS-eksemplarist tuletatud konfiguratsioonid globaalsesse hoidlasse. Kasutage üleslaadimisel abifunktsiooni **Konfiguratsioonipaketid**. Lisateavet leiad artiklist [RCS globaalne repro üleslaadimine](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Edasi minemine

Kasutage RCS-i visuaalseid kujundajaid järgmistel eesmärkidel.

- Laiendage Microsofti pakutavaid malle.
- Looge uusi konfiguratsioone, mida teie organisatsioon vajab.
- Kohandage e-arvete ja maksuarvestuse teenuse globaliseerimisfunktsioone.

Kasutage globaliseerumise hoidlat järgmistel eesmärkidel.

- Juurdepääs Microsofti loodud konfiguratsioonidele ja globaliseerimisfunktsioonidele.
- Laadige salvestamiseks üles loodud või laiendatud konfiguratsioonid globaalsesse hoidlasse ja jagage neid oma organisatsiooni Dynamics 365 rakenduskeskkondades või väliste organisatsioonidega. Lisateavet vt [ER-i konfiguratsiooni loomine RCS-s ja üleslaadimine globaalsesse hoidlasse](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Kas see muudatus tähendab, et LCS-i ei saa konfiguratsioonide keskseks ladustamiseks kasutada?

Jah. Funktsioon, mis võimaldab teil finantside ja toimingute rakendustest laadida konfiguratsioone LCS-i projekti varateeki, on aegunud. Siiski, saate kasutada LCS-i brauserit konfiguratsioonide üleslaadimiseks Projekti varateeki, nagu vajate.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Ma arvasin, et RCS on globaalsete mallifailide importimise asendushoidla. Ma ei arvanud, et seda kasutatakse konfiguratsioonide talletamiseks. Milline on õige?

RCS on kujundusteenus ER-i konfiguratsioonide loomiseks ja redigeerimiseks. RCS-il on oma hoidla, mida nimetatakse globaalseks hoidlaks. Seda hoidlat kasutatakse RCS-is loodud konfiguratsioonide salvestamiseks. Pärast LCS-i kasutamist talletusena on globaalne hoidla Microsofti konfiguratsioonide jaoks üks allikas. Kõigi LCS-ilt RCS-i nõutav konfiguratsioonide importimiseks ja seejärel nende avaldamine RCS-st globaalsesse hoidlasse tuleb lõpetada ajaline tegevus.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Kuidas ilma LCS-ta konfiguratsioonid talletada nii, et konfiguratsioone "testimine" ja "tootmine" saab hõlpsasti hallata ja üle kanda?

RCS kasutab *ühendatud rakenduse* mõisteid. Seotud rakendus moodustab ühenduse RCS-i ja mis tahes finantside ja toimingute rakenduste vahel. Kuna RCS-i saab kasutada konfiguratsioonide redigeerimiseks, saab ühendatud rakendust kasutada konfiguratsioonide otse kujundajast finantside ja toimingute rakenduste keskkondade tõukamiseks. Seega saate konfiguratsiooni kiiresti muuta ja katsetada, selle asemel et LCS-i projektitasemel talletus läbida.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Kas on näiteid, mis näitavad seadistust ja haldust?

Näiteid pole, kuid saate selles artiklis toodud sammud lõpule viia, et oma konfiguratsioonid üle viia RCS-i globaalsesse hoidlasse.

### <a name="is-rcs-a-prerequisite-to-configure-electronic-reporting"></a>Kas RCS on elektroonilise aruandluse konfigureerimise eeltingimus?

Jah. RCS sisaldab võimalusi, mis toetavad üleilmastumise funktsioonide seadistamist, mida kasutavad globaliseerumisteenused, nagu elektrooniline arveldus ja maksuarvestuse teenus. Kuid teenusel on sama visuaalse kujundaja funktsioon, mis võimaldab teil laiendada või luua uusi ER-i konfiguratsioone. RCS pakub ka elutsükli haldust nii ER-i konfiguratsioonide kui ka globaliseerimisfunktsioonide jaoks.

### <a name="which-regions-can-rcs-be-deployed-in"></a>Millistes piirkondades saab RCS-i kasutusele võtta?

RCS on saadaval järgmistes Azure'i piirkondades:

- USA
- India
- Prantsusmaa
- Euroopa

Lisateavet tootetoe kohta vt [Dynamics Globalization teenuste ülevaade](globalization-services-overview.md). Teavet geograafilise toe kohta vt teemast [Dynamics 365 ja Power Platform: saadavus, andmete asukoht, keel ja lokaliseerimine](https://aka.ms/rcs/D365Productavailabilityguide).

### <a name="whats-the-cost-of-using-rcs"></a>Kui palju maksab RCS-i kasutamine?

RCS-i ja globaliseerimishoidlat pakutakse olemasolevate finantside ja toimingute rakenduselitsentside osana tasuta. RCS-i disainiteenuse kasutamise või konfiguratsioonide globaalsesse hoidlasse salvestamisega ei kaasne eraldi kulusid. Praegu pole konfiguratsioonide või ühendatud rakenduste arvul piiranguid.
