---
title: Dynamics 365 Human Resources infrastruktuuri ühendamine – väljast 10.0.25 värskendus
description: See teema annab teavet Microsoft Release Dynamics 365 Human Resources 10.0.25 kohta, mis toob kaasa infrastruktuuri ühendamise esimese võimaluste voo.
author: twheeloc
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d574f760960241e4d79a988b1b671f224cb345f
ms.sourcegitcommit: 6f6ec4f4ff595bf81f0b8b83f66442d5456efa87
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/25/2022
ms.locfileid: "8487790"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources infrastruktuuri ühendamine – väljast 10.0.25 värskendus

10.0.25 vabastamine toob infrastruktuuri ühendamiseks esimese võimaluste voo. Infrastruktuuri ühendamise ajal ühendatakse Microsoft Dynamics 365 Human Resources Finantside ja Toimingute infrastruktuuriga. Kuid seda litsentsitakse siiski ka edaspidi sõltumatu rakendusena Dynamics 365 Finance Dynamics 365 Supply Chain Management. Lisateavet infrastruktuuri ühendamise kohta vt infrastruktuuri ühendamise [Dynamics 365 Human Resources KKK-st](../human-resources/hr-infrastructure-merge-faq.md).

Ühendamine tagab inimressursside kasutajate jaoks järjepidevuse järgmistel viisidel:

- [Keskkonnahaldus ja integratsioonid on inimressursside ning finantside ja toimingute rakenduste vahel järjepidevad.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Hallake keskkondi elutsükli Microsoft Dynamics teenustes, väljastamisotsingus ja .Regression Suite Automation Tool
    - On olemas üks koodibaas, kus Inimressursid uued funktsioonid vabastatakse osana tavalisest ühe versiooni uuendamise protsessist.
    - Täienduste, värskenduste ja kiirparanduste rakendamist keskkondades on kooskõlaline.

- [Laiendatavusvalikud on täiustatud.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options)

    - Saate vajadusel jätkata tööriistade Microsoft Power Platform kasutamist, et laiendada.
    - Funktsiooni saate laiendada vormide, tabelite, meetodite ja rakendusliideste (API-d) kaudu.
    - Saate üksuseid luua ja laiendada.

    Lisateavet saadaoleva laiendusvalikute kohta vt [Dynamics 365 laiendatavusest ülevaadet](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Dynamics 365-is luuakse üks inimressursside võimaluste kogum.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/create-one-set-human-resources-capabilities-within-dynamics-365)

    Väljaandes 10.0.25 on funktsionaalsed võimalused, mis eksisteerisid ainult Inimressurssides, teha kättesaadavaks Finantside ja Toimingute infrastruktuuris. Et kliendid neid võimalusi finantside ja toimingute keskkonnas ära kasutaks, peavad funktsioonihalduses olema lubatud järgmised inimressursside funktsioonid.

    | Funktsiooni nimi | Ülevaade | Väljastamise olek | 
    |--------------|----------|----------------| 
    | Tööaastate arvutamine | Seadistussuvand võimaldab teil valida kuupäeva, mida kasutatakse teenuseaastate **arvutamiseks**. | Üldiselt saadaval | 
    | Töövootoimingute täiustused | See funktsioon pakub täiustatud kasutajakogemust töövoo esitamiseks ja kinnitamiseks. | Üldiselt saadaval | 
    | Jõudluse ülevaadete printimine | Jõudluse ülevaate saate printida PDF-vormingus. | Üldiselt saadaval | 
    | Kohandatud lingid halduri **iseteeninduses** | Saate luua kohandatud linke, mis kuvatakse halduri **iseteeninduse** jaotises Seotud **lingid**. | Üldiselt saadaval | 
    | Ettevõtteülene hüvitusevaade | Kasutajad saavad vaadata tasuplaane juhataja **iseteeninduses** kõigi juriidiliste isikute lõikes, ilma et oleks vaja ettevõtteid vahetada. | Üldiselt saadaval | 
    | Mitme hüvitustaseme konfigureerimine töö järgi\*&dagger; | Nüüd toetavad tööd mitut hüvitustaset. | Eelversioon | 
    | Ülesandehaldus\* | Saate luua kontroll-loendeid ja ülesandeid põhi- ja maharegistreerimise ning üleminekuprotsessi jaoks. | Eelversioon | 
    | Sujuvam töövõtjate sisestamine | See funktsioon pakub värskendatud kasutajakogemust olemasoleval **lehel** Töötaja. | Eelversioon | 
    | Inimressursside kasutuskogemuse täiustused | Vt järgmise jaotise tabelit.  | Eelversioon | 

\* See funktsioon peab olema sisse lülitatud enne inimressursside **kasutajakogemuse täiustuste funktsiooni**.

&dagger; Seda funktsiooni ei saa pärast lubamist keelata.

## <a name="human-resource-user-experience-enhancements"></a>Inimressursside kasutajakogemuse täiustused

| Funktsiooni nimi | Ülevaade | 
|--------------|----------| 
| Kustuta töösuhe | Saate kustutada töötaja töösuhte. | 
| Töö pered | Saate jälgida gruppi sarnaseid töid, mis hõlmavad sarnaseid töid ja mis nõuavad sarnast koolitus-, oskus-, teadmisi ja oskusteavet. | 
| Täiendavad tööhõiveväljad | Lisati järgmised väljad: **Tööhõive kategooria**, **Tööhõive tüüp** ja **Tööhõive olek**. | 
| **Tööletööleheta** töötajad | Lehel kuvatakse töötajate loend, kellel pole tööhõivekirjet. | 
| Ametikoha dimensiooni kasutajakogemuse värskendus | Täiustatud kasutajakogemus on olemas ametikoha dimensioonide määramiseks juriidilise isiku kohta. | 
| Personalihalduse tööruumi **aadressimuutused** | See funktsioon loendab kõik aadressimuudatused, mis toimusid määratud arvu päevade jooksul, nagu määratud **inimressursside parameetrite** lehel. | 
| Aeguvad kirjed personalihalduse **tööruumis** | See funktsioon annab loendi kaupadest, mis on aegunud või aeguvad sertide, tunnuste, katseaja, skriiningute või testide jaoks. | 
| **Ametikoha hierarhia kinnitamise** leht | Ringviidete kontroll positsioonirea hierarhias. | 
| Riigipõhine palgateave | Täiendavad palgaväljad on saadaval töötaja **tööhõive** lehel, sõltuvalt selle juriidilise isiku riigist või regioonist, kus töötajad on palgatud. | 
| Vastavuse aruandluse täiustused | Täiendavad aruandlusvalikud on saadaval rakendustele EEO-1, Vets 4212 ja OSHA300a. | 
| Personalihalduse tööruumi **värskendused** | Aadressimuudatuste ja aegumiskirjete jälgimiseks on uuendused tehtud. Lisaks loetletakse uute vahekaartide abil töötaja ja ametikoha tegevused. | 
