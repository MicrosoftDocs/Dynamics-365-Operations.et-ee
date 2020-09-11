---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (1. mai 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 1. mai 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 074c678d9d8294aabf4e78b2a6ee0fa53efbaf23
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712276"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (1. mai 2020)

Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3196. Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Uued jõudlushalduse üksused on saadaval andmehaldusraamistikus (DMF)

Järgmised üksused on nüüd saadaval. Kui te ei näe neid üksuseid üksuste loendis, kasutage jaotises **Raamistiku parameetrid > Üksuse sätted > Värskenda üksuste loendit** suvandit **Värskenda üksuseid**.

- **Arutelu pädevus**
- **Arutelu eesmärgid**
- **Arutelu mõõtmine**
- **Arutelu teema**
- **Jõudluse tööraamat**
- **Mõõtmine**
- **Eesmärgi mõõtmine**

Lisaks lisati **Arutelu** üksusele suvandid **Kogusumma** ja **Keskmine summa**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Puhkusetaotluse kommentaaride pikkuse suurendamine (275641)

Puhkusetaotluse kommentaarid võivad nüüd olla pikemad kui 100 tähemärki.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Arvustuste lõppkommentaarid ei ilmu, kui haldur või töötaja on logitud sisse teise ettevõttesse (431688)

Kõik kommentaarid ilmuvad nüüd arvustuste kuvamisel.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Uus töötaja vorm ei toeta kasutaja määratletud linke (390374)

Kasutaja määratletud lingid on nüüd lubatud sujuvas **Töötaja** vormis.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity põhjustab OData API seiskumist (439476)

See muudatus parandab API seiskumise probleemi. Selle tõrke põhjustas duplikaatnimi.

## <a name="in-preview"></a>Eelvaates

## <a name="leave-suspension"></a>Puhkuse peatamine

Saate peatada töövõtja puhkuse Human Resourcesis. Puhkuse peatamine lõpetab puhkuse viitvõlad valitud puhkusetüüpide puhul. Kui peatamine toimub pärast viitvõla töötlemist, loob peatatav puhkus eelmääratud korrigeerimise töötaja puhkusesaldo jaoks. Lisateabe saamiseks vt [Puhkuse peatamine](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Kasutajakogemuse uuendamine viitvõla näitamiseks on peatatud (429550)

Kasutajakogemuses on nüüd näidatud, et plaani viitvõlg on peatatud.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Kindlate puhkusetüüpide puhkuse viitvõla peatamine (272447)

Selles väljalaskes saab inimressursside haldur luua reegli, et peatada selliste töötajate puhkuse viitvõlg, kes on esitanud tasustamata puhkuse taotluse. Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla. Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF-üksus on saadaval viitvõlgade peatamiseks (429549)

Nüüdsest on viitvõlgade peatamiseks saadaval DMF-üksus.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Lisa viitvõlgade peatamisele põhjusekood (429547)

Viitvõla peatamisele on lisatud põhjusekood.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Inimressursside parameetritelt puhkuse ja puudumise parameetritele ülemineku alustamine

Selles väljalaskes on alustatud inimressursside parameetrite kombineerimist puhkuse ja puudumise parameetritega.

## <a name="carry-forward-rules"></a>Edasikandmise reeglid

Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle. Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi. Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Teadaolevad probleemid

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePointi eelvaade ei tööta mõnes keskkonnas

Kui SharePointi talletatud dokumentide dokumendieelvaade ei tööta, proovige järgmist toimingut.

1. Kinnitage, et administraatori kasutajakontol on kasutaja kirjega seotud meiliaadress. Seda teavet saate vaadata lehel **Kasutaja**. Kui meiliaadressi ei ole seadistatud, peate lisama meili ja pakkuja OData Exceli lisandmooduli kaudu. Vaikimisi ei ole Exceli kujunduses meiliaadressi kaasatud. Peate redigeerima Exceli kujundust, lisama kõik väljad, rakendama ja värskendama. Kui olete need toimingud teinud, saate värskendada administraatori kontot.

2. Kui administraatoril on seostatud meilikonto, logige sisse Human Resourcesisse administraatori mandaatidega.

3. Juurdepääs SharePointi manusele dokumendieelvaate käivitamiseks.

4. Logige sisse teise kasutajakontoga, millel on juurdepääs manustele ja kinnitage, et eelvaade töötab ootuspäraselt.

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)