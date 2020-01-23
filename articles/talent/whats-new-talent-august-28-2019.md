---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 for Talent (27. august 2019)?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d7e5be0d9ba5e372e57f06fec77326561196626
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899239"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Mis on uut ja mida on muudetud rakenduses Dynamics 365 for Talent (27. august 2019)?

Selles teemas kirjeldatakse Dynamics 365 for Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2447. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Eelvaate funktsioonid on lubatud ainult liivakasti eksemplarides

Kui valmistate ette uue Talenti eksemplari, saate eksemplari tüübiks määrata Tootmine või Liivakast. Liivakasti tüübi eksemplarid võimaldavad uute funktsioonide varajast katsetamist. Kõik olemasolevad Talenti eksemplarid uuendatakse eksemplari tüübiks Tootmine. Kui soovite mõne olemasoleva eksemplari Liivakasti tüübile värskendada, võtke muudatuse taotlemiseks ühendust Toega.

Lisateavet muudatuste avaldamise kohta vt teemast [Talenti ettevalmistamine](./provisioning-talent.md).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Halduri iseteeninduses jõudluse lisateabe kuvamine

Uus suvand võimaldab juhtidel vaadata nii oma otseste kui ka kaudsete alluvate jõudlust. Praegu saavad rea haldurid määrata ja uuendada jõudluse eesmärke ja väljastada uusi arvustusi. Lisaks saavad otsesed juhid ja nende töötajad hallata ja värskendada jõudluse töölehti, mis aitavad tagada sujuva jõudluse ülevaate protsessi. Selle muudatuse rakendamisel saavad juhid vaadata ja hallata lisaks otseste alluvate jõudlusega seotud teabele ka oma kaudsete alluvate jõudlusega seotud teavet.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Juriidiliste isikute kustutamine pole lubatud, kui töötajad on ettevõttes olemas (339849)

Selle muudatusega ei saa te ettevõtteid eemaldada ega kustutada, kui juriidilise isiku töötajad ja muud seotud andmed on olemas.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>Kompensatsioonihalduse ärianalüütika ei ühti hüvitise tööruumiga (322493)

Selles versioonis on kompensatsioonianalüütikat kohandatud, et täpselt kajastada töötajatele määratud plaane.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>Töövoo kohatäide %company% kuvab DATi töötajate palkamisel töövoo kaudu (343905)

Selle versiooni puhul kuvab ettevõtte kohatäide juriidilise isiku, kes on seotud uue töötaja tööga.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>CDSJobPosition üksus kuvab tõrke, kui kuupäev on kehtiv (349387)

Selles versioonis võimaldavad olemi **Ametikoha üksikasjad** ja **Ametikoha kestus** andmeallikad olemil **CDSJobPosition** andmeallikad muuta väljast Common Data Service väljadele **Kuupäev on kehtiv**. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Töötaja töösuhte lõpetamiseks täidetakse viimane tööpäev tööülesande lõppkuupäeval (332496)

See muudatus seab nüüd positsiooni **Ülesande lõppkuupäev** vaikeväärtuseks **Töösuhte lõppkuupäev**. Andmeid sisestades saate neid vaikeväärtusi muuta.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Juriidilised isikud ei ole piiratud palkamisega (338871)
 
See muudatus piirab palkamisprotsessi, et näidata ainult neid juriidilisi isikuid, kellele kasutajal on juurdepääs.  

## <a name="in-preview"></a>Eelvaates

### <a name="streamlined-employee-entry-and-navigation"></a>Sujuvam töötajate sisestamine ja navigeerimine

See funktsioon on nüüd saadaval liivakasti ja prooviversiooni keskkondades. Selle funktsiooni sisselülitamiseks liikuge valikule **Süsteemi administreerimine > Lingid > Häälestus > Süsteemiparameetrid > Eelvaate funktsioonid**. Valige **Täiustatud töötajate vorm ja navigeerimine**. See võimaldab neid muudatusi kõigile kasutajatele. Võite selle suvandi igal ajal välja lülitada.

Lisateavet leiate teemast [Sujuv töötajate sisestamine ja navigeerimine](./streamlined-employee-entry.md).

## <a name="coming-soon"></a>Peagi tulekul

### <a name="platform-update-29"></a>Platvormivärskendus update 29

Platvormivärskenduse 29 kohta lisainfo saamiseks vt [Dynamics 365 for Finance and Operations platvormivärskenduse 29 (oktoober 2019) funktsioonide eelvaade](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
