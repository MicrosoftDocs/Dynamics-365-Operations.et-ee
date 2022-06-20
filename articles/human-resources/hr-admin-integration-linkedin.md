---
title: LinkedIn talent Hubiga integreerimine
description: See artikkel selgitab, kuidas seadistada integratsiooni Microsofti ja Dynamics 365 Human Resources LinkedIn Anne'i keskuse vahel.
author: jaredha
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df4a0a4dec078392ba835318450f5983a6e95c97
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887743"
---
# <a name="integrate-with-linkedin-talent-hub"></a>LinkedIn talent Hubiga integreerimine

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

> [!IMPORTANT]
> Selles artiklis Dynamics 365 Human Resources kirjeldatud integratsioon ja LinkedIn Anne'i keskus kustutati 31. detsembril 2021. Integreerimisteenus ei ole pärast seda kuupäeva enam saadaval. Organisatsioonid, mis ei kasuta juba integreerimisteenust, ei saa teenust enne pensionile minekut rakendada.

[LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub) on kandidaadi jälgimise süsteemi (ATS) platvorm. See võimaldab teil leida, hallata ja palgata töötajaid ühest kohast. Microsoft Dynamics 365 Human Resourcesi integreerimisel LinkedIn Talent Hubiga saate Human Resourcesis hõlpsalt luua töövõtja kirjed kandidaatide jaoks, kes on palgatud ametikohale.

## <a name="setup"></a>Seadistus

Süsteemiadministraator peab lõpule viima seadistustoimingud, et lubada integreerimist LinkedIn Talent Hubiga. Esmalt peate Power Appsi keskkonnas seadistama kasutaja- ja turberolli, et anda LinkedIn Talent Hubile vajalikud load andmete kirjutamiseks Human Resourcesisse.

### <a name="link-your-environment-to-linkedin-talent-hub"></a>Keskkonna linkimine LinkedIn Talent Hubiga

1. Avage [LinkedIn Talent Hub](https://business.linkedin.com/talent-solutions/talent-hub).

2. Valige kasutaja rippmenüüst **Toote sätted**.

3. Valige vasakpoolsel navigeerimispaanil jaotises **Täpsem** suvand **Integratsioonid**.

4. Valige **Autoriseeri** Microsofti Dynamics 365 Human Resourcesi integratsiooniks.

5. Valige lehel **Dynamics 365 Human Resources** keskkond, millega soovite LinkedIn Talent Hubi linkida ja seejärel valige **Lingi**.

    ![LinkedIn Talent Hubi sisseelamine.](./media/hr-admin-integration-talent-hub-onboarding.jpg)

    > [!NOTE]
    > Saate linkida ainult keskkondadega, kus teie kasutajakontol on administraatori juurdepääs nii Human Resourcesi keskkonnale kui ka seostatud Power Appsi keskkonnale. Kui Human Resourcesi linkide lehel pole loetletud ühtegi keskkonda, veenduge, et teie rentnikus oleks litsentsitud Human Resourcesi keskkond ja et kasutajal, millega olete linkide lehele sissetogitud, oleks administraatori õigused nii Human Resourcesi keskkonnale kui ka Power Appsi keskkonnale.

### <a name="create-a-power-apps-security-role"></a>Power Appsi turberolli loomine

1. Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2. Valige loendist **Keskkonnad** keskkond, mis on seostatud Human Resourcesi keskkonnaga, mida soovite linkida oma LinkedIn Talent Hubi eksemplariga.

3. Valige **Sätted**.

4. Laiendage sõlme **Kasutajad + load** ja valige **Turberollid**.

5. Valige lehe **Turberollid** tööriistaribal **Uus roll**.

6. Sisestage vahekaardil **Üksikasjad** rolli nimi, nt **LinkedIn Talent Hub HRIS-i integreerimine**.

7. Valige vahekaardil **Kohandamine** organisatsioonitaseme luba **Lugemine** järgmistele üksustele:

    - Üksus
    - Field
    - Suhte tüüp

8. Salvestage ja sulgege turberoll.

### <a name="create-a-power-apps-application-user"></a>Power Appsi rakenduse kasutaja loomine

Rakenduse kasutaja tuleb luua LinkedIn Talent Hubi adapteris, et anda adapterile load kandidaadi kirjete kirjutamiseks Power Appsi keskkonda.

1. Avage [Power Platformi halduskeskus](https://admin.powerplatform.microsoft.com).

2. Valige loendist **Keskkonnad** keskkond, mis on seostatud Human Resourcesi keskkonnaga, mida soovite linkida oma LinkedIn Talent Hubi eksemplariga.

3. Valige **Sätted**.

4. Laiendage sõlme **Kasutajad + load** ja valige **Kasutajad**.

5. Valige **Dynamics 365 kasutajate haldamine**.

6. Kasutage ülal olevat ripploendit, et muuta vaikimisi vaade **Lubatud kasutad** vaateks **Rakenduse kasutajad**.

    ![Rakenduse kasutajate vaade.](./media/hr-admin-integration-power-apps-application-users.jpg)

7. Valige tööriistaribal **Uus**.

8. Tehke lehel **Uus kasutaja** järgmist.

    1. Muutke välja **Kasutaja Tüüp** väärtuseks **Rakenduse kasutaja**.
    2. Seadke välja **Kasutajanimi** väärtuseks **Dynamics365 HR LinkedIn HRIS-i integratsioon**.
    3. Määrake välja **Rakenduse ID** väärtuseks **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    4. Sisestage mis tahes väärtus väljadele **Eesnimi**, **Perekonnanimi** ja **Esmane meiliaadress**.
    5. Valige tööriistaribal **Salvesta \& Sule**.

### <a name="assign-a-security-role-to-the-new-user"></a>Turberolli määramine uuele kasutajale

Pärast eelmises jaotises uue rakenduse kasutaja salvestamist ja sulgemist naasete lehele **Kasutajate loend**.

1. Muutke lehel **Kasutajate loend** vaateks **Rakenduse kasutajad**.

2. Valige eelmises jaotises loodud rakenduse kasutaja.

3. Valige tööriistaribal **Rollide haldamine**.

4. Valige integratsiooni jaoks eelnevalt loodud turberoll.

5. Valige nupp **OK**.

### <a name="add-an-azure-active-directory-app-in-human-resources"></a>Azure Active Directory rakenduse lisamine Human Resourcesisse

1. Avage Dynamics 365 Human Resourcesis leht **Azure Active Directory rakendused**.
2. Lisage loendisse uus kirje ja määrake järgmised väljad.

    - **Kliendi ID**: sisestage **3a225c96-d62a-44ce-b3ec-bd4e8e9befef**.
    - **Nimi**: sisestage Power Appsi turberolli nimi, mille eelnevalt lõite, nt **LinkedIn Talent Hub HRIS-i integratsioon**.
    - **Kasutaja ID**: valige kasutaja, kellel on õigus kirjutada andmeid personalihalduses.

### <a name="create-the-table-in-dataverse"></a>Tabeli loomine Dataverse'is

> [!IMPORTANT]
> LinkedIn Talent Hubiga integreerimine sõltub Dataverse for Human Resourcesi virtuaalsetest tabelites. Selle seadistamisetapi eeltingimusena peate konfigureerima virtuaalsed tabeleid. Lisateavet virtuaalsete tabelite konfigureerimise kohta leiate teemast [Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).

1. Avage rakenduses Human Resources leht **Dataverse integratsioon**.

2. Valige vahekaart **Virtuaalsed tabelid**.

3. Filtreerige üksuste loendit üksuse sildi järgi, et leida **LinkedIni ekspoditud kandidaat**.

4. Valige üksus ja seejärel valige **Loo/värskenda**.

## <a name="exporting-candidate-records"></a>Kandidaadi kirjete eksportimine

Pärast häälestuse lõpule viimist saavad värbajad ja Human Resourcesi (HR) professionaalid kasutada LinkedIn Talent Hubi funktsiooni **Ekspordi HRIS-i**, et eksportida palgatud kandidaadi kirjeid LinkedIni Talent Hubist Human Resourcesisse.

### <a name="export-records-from-linkedin-talent-hub"></a>Kirjete eksportimine LinkedIn Talent Hubist

Kui kandidaat on liikunud värbamisprotsessist edasi ja on palgatud, saate eksportida kandidaadi kirje LinkedIn Talent Hubist Human Resourcesisse.

1. Avage LinkedIn Talent Hubis projekt, milleks uue töötaja palkasite.

2. Valige kandidaadi kirje.

3. Valige **Muuda etappi** ja seejärel **Palgatud**.

4. Kandidaadi kolmikpunkti menüüs ( **...**) valige **Ekspordi HRIS-i**.

5. Sisestage paanil **Ekspordi HRIS-i** teave, mis tuleb eksportida.

    - Valige väljal **HRIS-i pakkuja** suvand **Microsoft Dynamics 365 Human Resources**.
    - Valige väljal **Alguskuupäev** väärtus uue töövõtja jaoks.
    - Sisestage väljale **Ametinimetus** uue töövõtja töö ametinimetus.
    - Sisestage väljale **Asukoht** asukoht, kus töövõtja hakkab töötama.
    - Sisestage või kinnitage töövõtja meiliaadress.

![HRIS-i paanile eksportimine LinkedIn Talent Hub`is.](./media/hr-admin-integration-linkedin-talent-hub-export.jpg)

## <a name="complete-onboarding-in-human-resources"></a>Sisseelamise lõpule viimine Human Resourcesis

Kandidaadi kirjed, mis eksporditakse LinkedIn Talent Hubist Human Resourcesisse, kuvatakse lehe **Personalihaldus** jaotises **Palgatavad kandidaadid**.

1. Avage rakenduses Human Resources loendi leht **Personalihaldus**.

2. Valige jaotises **Palgatavad kandidaadid** valitud kandidaadi jaoks suvand **Palka**.

3. Vaadake dialoogiboksis **Uue töötaja palkamine** kirje läbi ja lisage nõutav teave. Samuti saate valida ametikoha numbri, millele kandidaat palgati.

Kui nõutav teave on sisestatud, saate jätkata oma standardsete töövõtja kirjete loomise ja töövõtjate sisseelamise protsessidega.

Imporditakse järgmised üksikasjad ja lisatakse uue töötaja kirjesse.

- Eesnimi
- Perekonnanimi
- Töösuhte alguskuupäev
- Meiliaadress
- Telefoninumber

## <a name="see-also"></a>Vt ka

[Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Mis on Microsoft Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
