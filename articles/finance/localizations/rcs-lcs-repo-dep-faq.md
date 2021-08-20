---
title: Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine
description: See teema annab teavet Microsoft Dynamics Lifecycle Services (LCS) talletuse amortiseerumise kohta, mis on plaanitud Regulatory Configuration Service (RCS) globaalse hoidla väljamineku osana.
author: JaneA07
ms.date: 05/25/2021
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
ms.openlocfilehash: 7a738af04da4425e76bd3b224400f91bc4eb8364d323da67ea457eaba9e65643
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782194"
---
# <a name="regulatory-configuration-service-rcs--lifecycle-services-lcs-storage-deprecation"></a>Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine

[!include [banner](../includes/banner.md)]

Microsoft Dynamics Lifecycle Services (LCS) kasutamine elektroonilise aruandluse (ER) konfiguratsiooni talletushoidlana on aegunud. See aegumine hõlmab järgmisi muudatusi:

- Microsofti loodud konfiguratsioone, mida kasutatakse Microsoft Dynamics 365 rakendustes, ei avaldata enam LCS-i jagatud vara teegis. Selle asemel avaldatakse need ainult RCS-i globaalse hoidla kaudu. Dynamics AX 2012 konfiguratsioone avaldatakse siiski LCS-is ühiskasutusega varateegis kuni AX 2012. aasta tugitsükli lõpuni.
- Funktsioon, mis võimaldab teil rakendustest ja RCS-st üles laadida konfiguratsioone LCS-i projekti Finance and Operations varateeki, inaktiveeritakse. Siiski, saate kasutada LCS-i brauserit konfiguratsioonide üleslaadimiseks Projekti varateeki. Seega saate LCS-ile siiski konfiguratsioone lisada, et neid saaks lisada lahendusepakettidesse.
- Konfiguratsioonide importimine LCS-st on rakendustes Finance and Operations ja RCS teatud ajal saadaval ja toetatud. Siiski, funktsioon lõpuks aegub. (Täpne aegumise kuupäev teatatakse hiljem.)

## <a name="deprecation-notice"></a>Aegumisteatis

LCS-i kasutuse aegumine ladustamiseks oli edastatud [Eemaldatud või aegunud Dynamics 365 Finance - LCD aegumise teatis](../get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Planeeritud aegumiskuupäev on 1. aprill 2022.

## <a name="key-features"></a>Võtmefunktsioonid

- Konfiguratsioonide loomiseks ja redigeerimiseks saate kasutada RCS-i. Seejärel saate neid konfiguratsioone otse kujundajast ühendatud rakendusse tõugata. Seega saate konfiguratsioone kiiresti muuta ja testida.
- Globaalne hoidla on kõigi ER-konfiguratsioonide keskne talletus.

## <a name="guidance-for-one-time-and-ongoing-actions"></a>Juhis ühekordsete ja jooksvate tegevuste jaoks

Selles jaotises kirjeldatakse samme, mis tuleb üks kord lõpule viia. See kirjeldab ka samme, mida tuleb hiljem jooksval alusel täita.

### <a name="one-time-action"></a>Ühekordne tegevus

Importige kõik nõutavad konfiguratsioonid LCS-st RCS-i ja salvestage need RCS-st globaalsesse hoidlasse. Kui kasutate LCS-is tuletatud konfiguratsioonide tallemiseks projektipõhiseid varateeke, tuleb LCS-ile juurdepääsemiseks lõpetada järgmised sammud.

1. Kui RCS-i eksemplar ei ole juba saadaval, tehke üks pakkumine. Lisateavet vt teemast [RCSi ülevaade](rcs-overview.md).
2. Eraldise kantud RCS-eksemplaris registreerige varateegi iga LCS-projekti jaoks, mis sisaldab tuletatud ER-konfiguratsioone, sobiv LCS-i hoidla.
3. Importige ER-konfiguratsioonid LCS-i hoidlatest RCS-i. Lisateabe saamiseks vt teemat [Konfiguratsioonide importimine LCS-ist](../../dev-itpro/analytics/tasks/er-import-configuration-lifecycle-services.md).
4. Kui globaalset hoidlat automaatselt ei sisestata, registreerige see RCS-i.
5. Laadige kõik praegusest RCS-eksemplarist tuletatud konfiguratsioonid globaalsesse hoidlasse. Kasutage **Konfiguratsioonipakette, mis võimaldavad kasutajal üles laadida kõik konfiguratsioonid GR-sse ühe toiminguna** funktsioonis, mis aitavad üleslaadimist. Lisateavet leiad artiklist [RCS globaalne repro üleslaadimine](rcs-global-repo-upload.md).

### <a name="going-forward"></a>Edasi minemine

Kasutage kõikide uute konfiguratsioonide loomiseks RCS-i visuaalseid kujundajaid. Siis laadige konfiguratsioonid globaalsesse hoidlasse. Lisateavet vt [ER-i konfiguratsiooni loomine RCS-s ja üleslaadimine globaalsesse hoidlasse](rcs-global-repo-upload.md).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="does-this-change-mean-that-lcs-cant-be-used-as-central-storage-for-configurations"></a>Kas see muudatus tähendab, et LCS-i ei saa konfiguratsioonide keskseks ladustamiseks kasutada?

Jah. Funktsioon, mis võimaldab teil konfiguratsioone üles laadida LCS-i projekti varateeki rakendusest Finance and Operations, inaktiveeritakse. Siiski, saate kasutada LCS-i brauserit konfiguratsioonide üleslaadimiseks Projekti varateeki, nagu vajate.

### <a name="i-thought-that-rcs-was-a-replacement-repository-for-importing-global-template-files-i-didnt-think-that-its-used-to-store-configurations-which-is-correct"></a>Ma arvasin, et RCS on globaalsete mallifailide importimise asendushoidla. Ma ei arvanud, et seda kasutatakse konfiguratsioonide talletamiseks. Milline on õige?

RCS on kujundusteenus ER-i konfiguratsioonide loomiseks ja redigeerimiseks. RCS-il on oma hoidla, mida nimetatakse globaalseks hoidlaks. Seda hoidlat kasutatakse RCS-is loodud konfiguratsioonide salvestamiseks. Pärast LCS-i kasutamist talletusena on globaalne hoidla Microsofti konfiguratsioonide jaoks üks allikas. Kõigi LCS-ilt RCS-i nõutav konfiguratsioonide importimiseks ja seejärel nende avaldamine RCS-st globaalsesse hoidlasse tuleb lõpetada ajaline tegevus.

### <a name="without-lcs-what-is-the-suggested-way-to-store-configurations-so-that-test-and-production-configurations-can-easily-be-managed-and-transferred"></a>Kuidas ilma LCS-ta konfiguratsioonid talletada nii, et konfiguratsioone "testimine" ja "tootmine" saab hõlpsasti hallata ja üle kanda?

RCS kasutab *ühendatud rakenduse* mõisteid. Seotud rakendus moodustab ühenduse RCS-i ja mis tahes rakenduste Finance and Operations eksemplari vahel. Kuna RCS-i saab kasutada konfiguratsioonide redigeerimiseks, saab ühendatud rakendust kasutada konfiguratsioonide tõukamiseks otse kujundajast Finance and Operations rakenduste keskkonda. Seega saate konfiguratsiooni kiiresti muuta ja katsetada, selle asemel et LCS-i projektitasemel talletus läbida.

### <a name="are-there-any-examples-that-show-the-setup-and-management"></a>Kas on näiteid, mis näitavad seadistust ja haldust?

Näiteid pole, kuid saate selles teemas varasemad sammud lõpule viia, et oma konfiguratsioonid üle viia RCS-i globaalsesse hoidlasse.
