---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (21. jaanuar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 01/21/2020
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
ms.search.validFrom: 2020-01-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e9dee64e94c904cfe07c6a7766f6a60b1d60a2db
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528118"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-21-2020"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (21. jaanuar 2020)

[!include [banner](includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles artiklis kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract. Oleme lisanud Attracti funktsiooni, et toetada meie uusimat teadet: [Rakendusega Dynamics 365 Human Resources palju edukamate töötajate loomine](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources/).

### <a name="download-environment-data"></a>Keskkonnaandmete allalaadimine

Administraatorid saavad oma keskkonnaandmed alla laadida. Andmed eksporditakse ZIP-failis tavapärases JSON-vormingus koos kõigi tööde, kandidaatide ja konfiguratsioonidega. Lisateavet vt teemast [Andmete eksportimine Attractist ja Onboardist](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

### <a name="restricting-access-to-environments-for-non-admin-users"></a>Keskkondadele juurdepääsu piiramine mitte-administraatoritest kasutajatele

Administraatorid saavad nüüd piirata mitte-administraatoritest kasutajatele juurdepääsu keskkonnale. Seda tegevust ei saa tagasi võtta. Lisateabe saamiseks vt [Attractile jurdepääsu piiramine](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data#restrict-access-to-attract).

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

### <a name="exporting-onboarding-guides"></a>Sisseelamisjuhendite eksportimine

Kasutajad saavad nüüd eksportida kõik oma sisseelamisjuhendid ja sisseelamismallid Wordi dokumendi vormingus. Lisateavet vt teemast [Andmete eksportimine Attractist ja Onboardist](https://docs.microsoft.com/dynamics365/talent/attract-onboard-export-data).

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2726. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="most-recent-annual-compensation-field-in-verify-employment-form-isnt-consistent-392092"></a>Kõige hiljutisem aastase hüvitise väli töökohale sobivuse kontrollimise vormil ei ole järjepidev (392092)

See väljaanne sisaldab muudatust, mis kuvab järjepidevalt uusimat valuutat, mis põhineb ettevõtte valijal vormil **Töökohale sobivuse kontrollimine**.

### <a name="known-as-field-added-to-the-feedback-recipient-lookup-407789"></a>Tagasiside saaja otsingusse on lisatud väli Tuntud kui (407789)

Tulemuste tagasiside andmisel ei andnud töötajate otsing piisavalt teavet, et otsustada, kas tagasiside läheb õigele isikule. Lisasime veeru **Tuntud kui**, et aidata tuvastada töövõtja kordumatut nime.
 
### <a name="hcmworkerpayrollinfo-record-is-created-without-an-association-to-a-worker-394526"></a>Kirje HcmWorkerPayrollInfo luuakse ilma seotud töötajata (394526)

See väljaanne sisaldab muudatust mitte kirjutada kirjeid HCMWorkerPayrollInfo ilma viiteta töövõtjale.

### <a name="able-to-edit-department-when-navigating-from-position-hierarchy-341001"></a>Osakonna redigeerimise võimalus ametikohtade hierarhiast navigeerimisel (341001)

Kui turvalisus on häälestatud keelama juurdepääsu osakondade redigeerimisele, on redigeerimine navigeerimisel vormile **Osakonnad** keelatud kõigil juhtudel.

## <a name="coming-soon"></a>Peagi tulekul

Uus lahendus Common Data Service on varsti saadaval järgmiste muudatustega.

| Kirjeldus | Muutmine |
| --- | --- |
| Üksuse **Töö/ametikoht** muudatused | <ul><li>Lisatud **Hüvituspiirkond**</li><li>Lisatud **Finantsdimensioonid**</li></ul> |
| Üksuse **Töötaja** muudatused | <ul><li>Lisatud **Nimeseeria**</li><li>Lisatud **Töötab kodust**</li><li>Lisatud **Keel**</li><li>Lisatud **Staaži kuupäev**</li><li>Lisatud **Tähtpäeva kuupäev**</li><li>Lisatud **Värbamise algne kuupäev**</li></ul> |
| Olemi **Tööhõive** muudatused | <ul><li>Lisatud **Finantsdimensioonid**</li><li>Lisatud **Lõpetamise põhjus**</li><li>Suvand **Lõpetamiskuupäev** on nimetatud ümber suvandist **Üleviimise kuupäeva**</li><li>Lisatud **Katseaja kuupäev**</li></ul> |
| Üksuse **Töötaja aadress** muudatused | <ul><li>Lisatud **Tänavanimi**</li><li>Suvandid **Aadressirida 1**, **Aadressirida 2** ja **Aadressirida 3** on märgistatud kasutuselt eemaldamiseks</li></ul> |
| Uued ergutussüsteemi seadistuse üksused | <ul><li>**Muutuva hüvitisplaani tüüp**</li><li>**Kompensatsiooni tulemusplaan**</li><li>**Pensionireeglid**</li><li>**Muutuva hüvitisplaani tase**</li></ul> |
| Uus olem **Töötaja kalendri tööhõive** | <ul><li>Lisatud **Töökalendri üksus**</li></ul> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]