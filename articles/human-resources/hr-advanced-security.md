---
title: Juurdepääsu piiramine töötajatele juriidilise isiku alusel
description: See artikkel selgitab, kuidas seadistada töötaja juurdepääsu juriidilisele isikule.
author: twheeloc
ms.date: 11/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSharedParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fadd2c34d31bbd259255596c06a8e7517f7a774b
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780298"
---
# <a name="restrict-access-to-workers-by-legal-entity"></a>Juurdepääsu piiramine töötajatele juriidilise isiku alusel

See artikkel selgitab, kuidas seadistada töötaja juurdepääsu juriidilisele isikule.

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Töötajad on tööle võetud juriidilistes isikutes. Järgmisena on toodud mõned näited.

- TheLeb Con on tööle võetud SERVA juriidilises isikus.
- EttEtt on tööle võetud USMF-i juriidilises isikus.
- Alicia Tliber on tööle võetud GLSI ja USMF-i juriidilistes isikutes.

Sõltuvalt kasutaja rollist ettevõttes, võib neil olla vaja juurdepääsu kõigi juriidiliste isikute kõigi töötajate vaatamiseks. Teise võimalusena võib kasutaja olla piiratud, nii et nad saavad vaadata ainult juriidilise isiku töötajaid, neile on juurdepääs. Selleks, et kontrollida, milliseid töötajaid kasutaja saab vaadata, valige **inimressursside jagatud** **parameetrite lehel parameeter Piira juurdepääsu töötaja teabele**.

Näiteks on kasutajal juurdepääs lehele Töötaja **ja** tal on juurdepääs ainult USMF-i juriidilisele isikule. Sel juhul saab kasutaja vaadata järgmist teavet eelnevas loendis nimetatud töötajate kohta:

- Kui töötajateabele juurdepääsu piiramise funktsioon ei ole lubatud, saab kasutaja vaadata Kasutaja teavet pääsu ja pääsu ja pääsu kohta töö tegijaile Ning vaatamiseks töö juures, töö juures, töö juures.
- Kui see funktsioon on lubatud, saab kasutaja vaadata teavet ainult Alicia jaSubjekti kohta, sest need on tööle võetud ka USMF-i juriidilises isikus.

Kuvamisteave on sõltuvalt kasutatavast rakendusest erinev.

## <a name="dynamics-365-human-resources-stand-alone"></a>Dynamics 365 Human Resources Autonoomne

Kui funktsioon juurdepääsu piiramiseks töötaja teabele on lubatud, näeb piiratud kasutaja mõnda töötaja nime sisaldavas loendis tühja väärtust.

Näiteks kasutaja, kellel on juurdepääs ainult USMF-juriidilisele isikule, käitub järgmiselt:

- Aktiivsete **ametikohtade loendis** **on Veerg Töötaja** Konto positsiooni puhul tühi, kuna kasutajal pole juurdepääsu LEGAL-juriidilise isiku töötajatele.
- Kui kasutaja süvitsi töötaja nimes, ilmub tühi **töötaja** lehekülg.

## <a name="dynamics-365-human-resources-on-finance-infrastructure"></a>Dynamics 365 Human Resources finants infrastruktuuris

Kui funktsioon juurdepääsu piiramiseks töötaja teabele on lubatud, näeb piiratud kasutaja töötaja nime mõnes loendis.

Näiteks kasutaja, kellel on juurdepääs ainult USMF-juriidilisele isikule, käitub järgmiselt:

- Aktiivsete **ametikohtade** loendis kuvatakse **veerus Töötaja** Oma nimi. Kui kasutaja kõliseb töötaja nime peale, kuvatakse ainult nimi ja ametinimetus.
- Kui kasutaja süvitsi töötaja nimes, ilmub tühi **töötaja** lehekülg.

> [!TIP]
> Kui kasutate Dynamics 365 inimressursse finantside infrastruktuuris ja soovite, et piiratud kasutajad näeks töötaja nimedes tühje väärtusi, **·** **saate lisada töötajate turbeõigustele juurdepääsu piiramise kasutajarollidele lehel Turbekonfiguratsioon.**

Pärast funktsiooni lubamist peate iga kasutaja jaoks, kelle vaade peab olema piiratud, õiguste vaatamiseks sooritama lisatoiminguid.

1. Valige **kasutaja** lehel kasutaja.
2. Valige kasutajale roll. Suvand **Organisatsioonide määramine** muutub kättesaadavaks.
3. Valige **Organisatsioonide määramine**.
4. Valige uuel leheküljel suvand **Anna juurdepääs konkreetsetele organisatsioonidel** ja seejärel valige organisatsioonid, mille juurdekasutajal peab juurdepääs olema.
5. Korrake samme 2 kuni 4 muude rollide puhul, mis kasutajal on, k.a süsteemi kasutaja roll.

> [!NOTE]
> Juriidilised isikud,le kasutajal on juurdepääs, peavad ühtima kõigi kasutaja rollidega.
