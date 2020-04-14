---
title: Kopeeri eksemplar
description: Saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida rakenduse Microsoft Dynamics 365 Human Resources andmebaas liivakastikeskkonda.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bb363369994d99f358be0c23cdaf1dbc80b644e5
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092288"
---
# <a name="copy-an-instance"></a>Kopeeri eksemplar

Saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida rakenduse Microsoft Dynamics 365 Human Resources andmebaas liivakastikeskkonda. Kui teil on teine liivakastikeskkond, saate kopeerida andmebaasi ka sellest keskkonnast sihtkohaks olevasse liivakastikeskkonda.

Eksemplari kopeerimiseks peate tagama järgneva.

- Rakenduse Human Resources eksemplar, mida soovite üle kirjutada, peab olema liivakastikeskkond.

- Keskkonnad, millest ja kuhu soovite kopeerida, peavad olema samas piirkonnas. Piirkondade üleselt ei saa kopeerida.

- Peate olema sihtkeskkonnas administraator, et saaksite pärast eksemplari kopeerimist sellesse sisse logida.

- Rakenduse Human Resources andmebaasi kopeerimisel ei kopeerita elemente (rakendusi või andmeid), mis sisalduvad keskkonnas Microsoft PowerApps. Teavet PowerAppsi keskkonnas elementide kopeerimise kohta vt teemast [Keskkonna kopeerimine](https://docs.microsoft.com/power-platform/admin/copy-environment). PowerAppsi keskkond, mida soovite üle kirjutada, peab olema liivakastikeskkond. PowerAppsi tootmiskeskkonna muutmiseks liivakastikeskkonnaks peate olema rentniku üldadministraator. Lisateavet PowerAppsi keskkonna muutmise kohta vt teemast [Eksemplari vahetamine](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>Rakenduse Human Resources andmebaasi kopeerimise mõjud

Rakenduse Human Resources andmebaasi kopeerimisel esinevad järgmised sündmused.

- Kopeerimisprotsess kustutab sihtkeskkonnas olemasoleva andmebaasi. Kui kopeerimisprotsessi lõpetamist ei saa te olemasolevat andmebaasi taastada.

- Sihtkeskkond ei ole saadaval enne, kui kopeerimisprotsess on lõpule viidud.

- Microsoft Azure’i bloobimälu dokumente ei kopeerita ühest keskkonnast teise. Seetõttu ei kopeerita ühtegi lisatud dokumenti ega malli ja need jäävad lähtekeskkonda.

- Ükski kasutaja (v.a administraatorkasutajad ja teised sisemised teenusekasutajate kontod) pole saadaval. Seega saab administraatorkasutaja andmed kustutada või ebaselgeks muuta enne teiste kasutajate tagasi süsteemi lubamist.

- Administraatorkasutaja peab tegema vajalikud konfiguratsiooni muudatused, nagu integratsiooni lõpp-punktide uuesti ühendamine kindlate teenuste või URL-idega.

## <a name="copy-the-human-resources-database"></a>Rakenduse Human Resources andmebaasi kopeerimine

Selle ülesande lõpetamiseks kopeerite esmalt eksemplar ja seejärel logige oma Microsoft Power Platformi halduskeskkonda sisse, et kopeerida PowerAppsi keskkond.

> [!WARNING]
> Eksemplari kopeerimisel andmebaas sihteksemplaris kustutatakse. Sihteksemplar ei ole selle protsessi käigus saadaval.

1. Logige LCS-i sisse ja valige LCS-i projekt, mis sisaldab eksemplari, mida soovite kopeerida.

2. Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.

3. Valige kopeeritav eksemplar ja seejärel valige käsk **Kopeeri**.

4. Valige tööpaanil **Eksemplari kopeerimine** ülekirjutamiseks eksemplar ja seejärel valige käsk **Kopeeri**. Oodake, kuni välja **Kopeerimise olek** väärtus uuendatakse suvandile **Lõpule viidud**.

   ![[Ülekirjutamiseks eksemplari valimine](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Valige **Power Platform** ja logige Microsoft Power Platformi halduskeskusesse sisse.

   ![[Power Platformi valimine](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Valige kopeeritav PowerAppsi keskkond eksemplar ja seejärel valige käsk **Kopeeri**.

7. Kui kopeerimisprotsess on lõpule viidud, logige sihteksemplari sisse ja lubage Common Data Service’i integratsioon. Lisateavet ja juhiseid vt teemast [Common Data Service’i integreerimise konfigureerimine](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

## <a name="data-elements-and-statuses"></a>Andmeelemendid ja olekud

Rakenduse Human Resources eksemplari kopeerimisel järgmisi andmeelemene ei kopeerita.

- Meiliaadressid tabelis **LogisticsElectronicAddress**

- Pakett-töö ajalugu tabelites **BatchJobHistory**, **BatchHistory** ja **BatchConstraintHistory**

- Simple Mail Transfer Protocoli (SMTP) parool tabelis **SysEmailSMTPPassword**

- SMTP-edastusserver tabelis **SysEmailParameters**

- Prindihalduse sätted tabelites **PrintMgmtSettings** ja **PrintMgmtDocInstance**

- Keskkonnale spetsiifilised kirjed tabelites **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** ja **BatchServerGroup**

- Dokumendimanused tabelis DocuValue. Need manused sisaldavad mis tahes Microsoft Office’i malle, mis on lähtekeskkonnas üle kirjutatud

- Ühendusstring tabelis **PersonnelIntegrationConfiguration**

Osasid neist elementidest ei kopeerita, kuna need on keskkonnale spetsiifilised. Näidete hulka kuuluvad kirjed **BatchServerConfig** ja **SysCorpNetPrinters**. Teisi elemente tugiteenusepiletite mahu tõttu ei kopeerita. Näiteks võidakse saata topeltmeile, kuna SMTP on kasutaja aktsepteerimise testimise (liivakasti) keskkonnas endiselt lubatud, kehtetu integreerimise sõnumeid võidakse saata, kuna pakett-tööd on endiselt lubatud, ja kasutajad võivad olla lubatud enne, kui administraatorid saavad teostada värskendamisjärgseid puhastustoiminguid.

Lisaks muutuvad eksemplari kopeerimisel järgmised olekud.

- Kõik kasutajad peale administraatori seatakse olekusse **Keelatud**.

- Kõik pakett-tööd, välja arvatud mõned süsteemi tööd, seatakse olekusse **Kinnipeetud**.

## <a name="environment-admin"></a>Kekkonna administraator

Kõik liivakasti sihtkeskkonna kasutajad (sh administraatorid) asendatakse lähtekeskkonna kasutajatega. Enne eksemplari kopeerimist veenduge, et oleksite sihtkeskkonnas administraator. Kui te seda ei ole, ei saa te pärast kopeerimise lõpetamist liivakasti sihtkeskkonda sisse logida.

Kõik mitte-administraatorist kasutajad liivakasti sihtkeskkonnas keelatakse, et välistada liivakasti keskkonnas soovimatuid sisselogimisi. Administraatorid saavad vajadusel kasutajaid uuesti lubada.
