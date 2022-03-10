---
title: Dynamics 365 Human Resources infrastruktuuri ühendamine – versiooni 10.0.25 värskendus
description: See teema pakub teavet Microsofti kohta Dynamics 365 Human Resources väljalase 10.0.25, mis toob kaasa esimese infrastruktuuri ühendamise võimaluste laine.
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
ms.openlocfilehash: a80bedd0224f1e31dfec4e9f4c39ad1ed75d7f2f
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024563"
---
# <a name="dynamics-365-human-resources-infrastructure-merge---release-10025-update"></a>Dynamics 365 Human Resources infrastruktuuri ühendamine – versiooni 10.0.25 värskendus

Versioon 10.0.25 toob kaasa esimese infrastruktuuri ühendamise võimaluste laine. Taristu ühendamise käigus Microsoft Dynamics 365 Human Resources liidetakse Finance and Operationsi infrastruktuuriga. Siiski jätkatakse selle litsentsimist iseseisva rakendusena, nagu Dynamics 365 Finance ja Dynamics 365 Supply Chain Management. Lisateabe saamiseks infrastruktuuri ühendamise kohta vt [Dynamics 365 Human Resources infrastruktuuri ühendamise KKK](../human-resources/hr-infrastructure-merge-faq.md).

Ühendamine tagab personaliteenuste kasutajatele järjepidevuse järgmistel viisidel.

- [Keskkonnajuhtimine ja integratsioonid on personali- ning finants- ja tegevusrakenduste vahel kooskõlas.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/consistent-environment-management-integrations-between-human-resources-finance-operations-apps)

    - Hallake keskkondi Microsoft Dynamics Elutsükli teenused, probleemide otsing ja Regression Suite Automation Tool.
    - Seal on üks koodibaas, kus tavapärase One Version värskendusprotsessi osana vabastatakse personaliosakonna uued funktsioonid.
    - Viis, kuidas täiendusi, värskendusi ja kiirparandusi keskkondadele rakendatakse, on ühtlane.

- [Laiendatavuse võimalusi on täiustatud.](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/improve-extensibility-options.md)

    - Saate jätkata kasutamist Microsoft Power Platform tööriistu vastavalt vajadusele pikendada.
    - Funktsionaalsust saate laiendada vormide, tabelite, meetodite ja rakendusliideste (API-de) kaudu.
    - Saate luua ja laiendada üksusi.

    Saadaolevate laiendusvalikute kohta lisateabe saamiseks vt [Ülevaade Dynamics 365 laiendatavusest](../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md).

- [Looge Dynamics 365-s üks inimressursi võimaluste komplekt.](/dynamics365-release-plan/2021wave2/human-resources/create-one-set-human-resources-capabilities-within-dynamics-365.md)

    Versiooni 10.0.25 versioonis on Finance and Operationsi infrastruktuuris kättesaadavaks tehtud funktsionaalsed võimalused, mis eksisteerisid ainult personaliosakonnas. Selleks, et kliendid saaksid neid võimalusi Finance and Operationsi keskkonnas kasutada, peavad funktsioonide halduses olema lubatud järgmised personalifunktsioonid.

    | Funktsiooni nimi | Ülevaade | Väljastamise olek | 
    |--------------|----------|----------------| 
    | Tööaastate arvutamine | Seadistussuvand võimaldab teil valida kuupäeva, mida kasutatakse **Tööaastaid** arvutus. | Üldiselt saadaval | 
    | Töövootoimingute täiustused | See funktsioon pakub töövoo esitamiseks ja kinnitamiseks täiustatud kasutuskogemust. | Üldiselt saadaval | 
    | Jõudluse ülevaadete printimine | Jõudlusülevaateid saate printida PDF-vormingus. | Üldiselt saadaval | 
    | Kohandatud lingid sisse **Juhataja iseteenindus** | Saate luua kohandatud linke, mis kuvatakse rakenduses **Seotud lingid** osa **Juhataja iseteenindus**. | Üldiselt saadaval | 
    | Ettevõtteülene hüvitusevaade | Kasutajad saavad hüvitise plaane vaadata **Juhataja iseteenindus** kõigis juriidilistes isikutes, ilma et peaks ettevõtet vahetama. | Üldiselt saadaval | 
    | Konfigureerige mitu hüvitise taset töökoha järgi\*&dagger; | Töökohad toetavad nüüd mitut hüvitise taset. | Eelversioon | 
    | Ülesannete haldamine\* | Saate luua sisse-, välja- ja üleminekuprotsessi jaoks kontrollnimekirju ja ülesandeid. | Eelversioon | 
    | Sujuvam töövõtjate sisestamine | See funktsioon pakub värskendatud kasutuskogemust olemasoleval **Tööline** lehel. | Eelversioon | 
    | Inimressursside kasutuskogemuse täiustused | Vaadake tabelit järgmises jaotises.  | Eelversioon | 

\* See funktsioon peab olema sisse lülitatud enne **Inimressursside kasutajakogemuse täiustused** tunnusjoon.

&dagger; Seda funktsiooni ei saa pärast lubamist keelata.

## <a name="human-resource-user-experience-enhancements"></a>Inimressursi kasutajakogemuse täiustused

| Funktsiooni nimi | Ülevaade | 
|--------------|----------| 
| Kustuta töösuhe | Saate töötaja töösuhte kustutada. | 
| Tööpered | Saate jälgida tööde rühma, mis hõlmavad sarnast tööd ja nõuavad sarnast koolitust, oskusi, teadmisi ja teadmisi. | 
| Täiendavad töövaldkonnad | Lisati järgmised väljad: **Tööhõive kategooria**, **tüüp**, ja **Tööalane staatus**. | 
| **Töötajad ilma tööta** lehel | Lehel kuvatakse nimekiri töötajatest, kellel pole tööandmeid. | 
| Positsiooni dimensiooni kasutajakogemuse värskendus | Juriidilise isiku kohta positsiooni mõõtmete määramiseks on täiustatud kasutajakogemus. | 
| Aadressi muutus **Personali juhtimine** tööruum | See funktsioon annab loendi kõigist aadressimuudatustest, mis toimusid teatud arvu päevade jooksul, nagu on määratletud **Inimressursi parameetrid** lehel. | 
| Kirjed aeguvad **Personali juhtimine** tööruum | See funktsioon pakub loetelu üksustest, mis on aegunud või aeguvad sertifikaatide, identifitseerimise, katseaja, läbivaatuste või testide jaoks. | 
| **Positsioonihierarhia kinnitamine** lehel | Positsiooniridade hierarhias kontrollitakse ringikujulisi viiteid. | 
| Riigipõhine palgaarvestus | Täiendavad palgaväljad on saadaval aadressil **Töötaja tööhõive** lehel, olenevalt selle juriidilise isiku riigist või piirkonnast, kus töötajad töötavad. | 
| Vastavuse aruandluse täiustused | Täiendavad aruandlusvalikud on saadaval EEO-1, Vets 4212 ja OSHA300a jaoks. | 
| Värskendused **Personali juhtimine** tööruum | Aadresside muudatuste ja aeguvate kirjete jälgimiseks on tehtud värskendusi. Lisaks loetlevad uued vahekaardid töötajate ja ametikohtade toimingud. | 
