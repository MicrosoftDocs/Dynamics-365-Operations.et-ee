---
title: Kopeeri eksemplar
description: Saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida rakenduse Microsoft Dynamics 365 Human Resources andmebaas liivakastikeskkonda.
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 935c2e6cb45df193e6cbf70634f3561154c6fe38
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178529"
---
# <a name="copy-an-instance"></a>Kopeeri eksemplar

_**Rakendub:** inimressursid autonoomsel infrastruktuuril_ 

> [!NOTE]
> Alates 2022. juunist saab Inimressursside keskkondi juurutada ainult finantside ja toimingute rakenduse infrastruktuuris. Lisateavet vt inimressursside ettevalmistamisest [finantside ja toimingute infrastruktuuris](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finantside ja toimingute taristu ei toeta kopeerimiseksemplari funktsiooni. Saate juurutada uusi keskkondi ja kasutada koopiate loomiseks andmebaasi liikumisi. Lisateavet iseteeninduse juurutuste kohta vt iseteeninduse [juurutuse ülevaatest](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Lisateavet andmebaasi liikumiste kohta finantside ja toimingute infrastruktuuris vt Andmebaasi tegemistoimingute [avalehelt](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida rakenduse Microsoft Dynamics 365 Human Resources andmebaas liivakastikeskkonda. Kui teil on teine liivakastikeskkond, saate kopeerida andmebaasi ka sellest keskkonnast sihtkohaks olevasse liivakastikeskkonda.

Eksemplari kopeerimiseks pidage meeles järgmisi nõuandeid.

- Rakenduse Human Resources eksemplar, mida soovite üle kirjutada, peab olema liivakastikeskkond.

- Keskkonnad, millest ja kuhu soovite kopeerida, peavad olema samas piirkonnas. Piirkondade üleselt ei saa kopeerida.

- Peate olema sihtkeskkonnas administraator, et saaksite pärast eksemplari kopeerimist sellesse sisse logida.

- Rakenduse Human Resources andmebaasi kopeerimisel ei kopeerita elemente (rakendusi või andmeid), mis sisalduvad keskkonnas Microsoft Power Apps. Teavet Power Appsi keskkonnas elementide kopeerimise kohta vt teemast [Keskkonna kopeerimine](/power-platform/admin/copy-environment). Power Appsi keskkond, mida soovite üle kirjutada, peab olema liivakastikeskkond. Power Appsi tootmiskeskkonna muutmiseks liivakastikeskkonnaks peate olema rentniku üldadministraator. Lisateavet Power Appsi keskkonna muutmise kohta vt teemast [Eksemplari vahetamine](/dynamics365/admin/switch-instance).

- Kui kopeerite eksemplari oma liivakastikeskkonda ja soovite oma liivakastikeskkonda integreerida Dataverse'iga, peate uuesti rakendama kohandatud väljad Dataverse'i tabelitele. Lugege teemat [Kohandatud väljade rakendamine teenuses Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Rakenduse Human Resources andmebaasi kopeerimise mõjud

Rakenduse Human Resources andmebaasi kopeerimisel esinevad järgmised sündmused.

- Kopeerimisprotsess kustutab sihtkeskkonnas olemasoleva andmebaasi. Kui kopeerimisprotsessi lõpetamist ei saa te olemasolevat andmebaasi taastada.

- Sihtkeskkond ei ole saadaval enne, kui kopeerimisprotsess on lõpule viidud.

- Microsoft Azure’i bloobimälu dokumente ei kopeerita ühest keskkonnast teise. Selle tulemusena ei kopeerita ühtegi lisatud dokumenti ega malli ja need jäävad lähtekeskkonda.

- Kõik kasutajad, v.a need, kellel on turberoll "Süsteemiadministraator" ja teised siseteenuse kasutajakontod, pole saadaval. Administraatorkasutaja saab andmeid kustutada enne teiste kasutajate süsteemi tagasi lubamist.

- Iga kasutaja, kellel on turvaroll "Süsteemihaldur", peab tegema vajalikud konfiguratsioonimuudatused, näiteks ühendama integratsiooni lõpp-punktid uuesti teatud teenuste või URL-idega.

## <a name="copy-the-human-resources-database"></a>Rakenduse Human Resources andmebaasi kopeerimine

Selle ülesande lõpetamiseks kopeerite esmalt eksemplar ja seejärel logige oma Microsoft Power Platformi halduskeskkonda sisse, et kopeerida Power Appsi keskkond.

> [!WARNING]
> Eksemplari kopeerimisel andmebaas sihteksemplaris kustutatakse. Sihteksemplar ei ole selle protsessi käigus saadaval.

1. Logige LCS-i sisse ja valige LCS-i projekt, mis sisaldab eksemplari, mida soovite kopeerida.

2. Valige oma LCS-i projektis paan **Rakenduse Human Resources haldus**.

3. Valige kopeeritav eksemplar ja seejärel valige käsk **Kopeeri**.

4. Valige tööpaanil **Eksemplari kopeerimine** ülekirjutamiseks eksemplar ja seejärel valige käsk **Kopeeri**. Oodake, kuni **olekuväli** Kopeeri uuendatakse väärtusele **Lõpetatud**.

   ![[Valige ülekirjutamiseks eksemplar.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Valige **Power Platform** ja logige Microsoft Power Platformi halduskeskusesse sisse.

   ![[Vali.Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Valige kopeeritav Power Appsi keskkond eksemplar ja seejärel valige käsk **Kopeeri**.

Lisateavet keskkonna kopeerimise kohta Power Apps vt teemast [Keskkonna kopeerimine](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Kui kopeerimisprotsess on lõpule viidud, logige sihteksemplari sisse ja lubage Dataverse’i integratsioon. Lisateavet ja juhiseid vt teemast [Dataverse’i integreerimise konfigureerimine](./hr-admin-integration-common-data-service.md).

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

Osasid neist elementidest ei kopeerita, kuna need on keskkonnale spetsiifilised. Näidete hulka kuuluvad kirjed **BatchServerConfig** ja **SysCorpNetPrinters**. Teisi elemente tugiteenusepiletite mahu tõttu ei kopeerita. Näide:

- Topeltmeile võidakse saata, kuna SMTP on kasutaja nõusoleku testimise (liivakasti) keskkonnas endiselt lubatud.

- Sobimatuid integratsiooniteated võidakse saata, kuna pakett-tööd on endiselt lubatud.

- Kasutajad võivad olla lubatud enne, kui administraatorid saavad teha värskendamisjärgseid puhastustoiminguid.

Samuti muutuvad eksemplari kopeerimisel järgmised olekud.

- Kõik kasutajad, v.a need, kellel on turberoll "Süsteemiadministraator" on seatud olekusse **Ei ole lubatud**.

- Kõik pakett-tööd, välja arvatud mõned süsteemi tööd, seatakse olekusse **Kinnipeetud**.

## <a name="environment-admin"></a>Kekkonna administraator

Kõik liivakasti sihtkeskkonna kasutajad (sh administraatorid) asendatakse lähtekeskkonna kasutajatega. Enne eksemplari kopeerimist veenduge, et oleksite lähtekeskkonnas administraator. Kui te seda ei tee, ei saa te pärast kopeerimise lõpetamist sihtkausta keskkonda sisse logida.

Kõik mitte-administraatorist kasutajad liivakasti sihtkeskkonnas keelatakse, et välistada liivakasti keskkonnas soovimatuid sisselogimisi. Administraatorid saavad vajadusel kasutajaid uuesti lubada.

## <a name="apply-custom-fields-to-dataverse"></a>Kohandatud väljade rakendamine teenuses Dataverse

Kui kopeerite eksemplari oma liivakastikeskkonda ja soovite oma liivakastikeskkonda integreerida Dataverse'iga, peate uuesti rakendama kohandatud väljad Dataverse'i tabelitele.

Iga Dataverse'i tabelites avatud kohandatud välja puhul tehke järgmist.

1. Minge kohandatud väljale ja valige **Redigeeri**.

2. Tühistage väli **Lubatud** iga cdm_* üksuse jaoks, millel kohandatud väli on lubatud.

3. Valige **Rakenda muudatused**.

4. Valige uuesti käsk **Redigeeri**.

5. Valige väli **Lubatud** iga cdm_* üksuse jaoks, millel kohandatud väli on lubatud.

6. Valige uuesti **Rakenda muudatused**.

Valiku tühistamine, muudatuste rakendamine, uuesti valimine ja muudatuste uuesti rakendamine palub skeemil teha teenuses Dataverse värskendusi kohandatud väljade kaasamiseks.

Lisateavet kohandatud väljade kohta leiate teemast [Kohandatud väljade loomine ja nendega töötamine](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Vt ka

[Human Resources ettevalmistus](hr-admin-setup-provision.md)</br>
[Eemalda eksemplar](hr-admin-setup-remove-instance.md)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
