---
title: Tõrkeotsingu probleemid algse sünkroonimine ajal
description: See artikkel pakub tõrkeotsingu teavet, mis võib aidata teil lahendada probleeme, mis võivad ilmneda algse sünkroonimise ajal.
author: RamaKrishnamoorthy
ms.date: 06/24/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: d9d74eea90cc2dfca2d5decf6e5cd1d7f52da2a8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289480"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Tõrkeotsingu probleemid algse sünkroonimine ajal

[!include [banner](../../includes/banner.md)]



See artikkel pakub tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning Dataverse. Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.

> [!IMPORTANT]
> Mõned küsimused, mida see artikkel käsitleb, võivad nõuda kas süsteemiadministraatori rolli või Microsofti Azure Active Directory (Azure AD) rentniku administraatori mandaate. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Kontrollige finantside ja toimingute rakenduses algse sünkroonimise tõrkeid.

Pärast vastendamise mallide lubamist peaks vastenduse olekuks olema **Töötab**. Kui olek on **Ei tööta**, ilmnes tõrkeid esmasel sünkroonimisel. Tõrgete kuvamiseks valige lehel **Topeltkirjutus** vahekaart **Esmase sünkroonimise üksikasjad**.

![Esmase sünkroonimise üksikasjade vahekaardi tõrge.](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Esmast sünkroonimist ei saa lõpule viia: 400 vigane päring

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui proovite käivitada vastendust ja esmast sünkroonimist, võidakse kuvada järgmine tõrketeade.

*(\[Vigane päring\], kaugserver tagastas tõrke: (400) vigane päring.), AX eksportimisel ilmnes tõrge.*

Siin on tabeli täieliku tõrketeate näide.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Kui see tõrge ilmneb järjepidevalt ja te ei saa esmast sünkroonimist lõpule viia, toimige probleemi lahendamiseks järgmiselt.

1. Finantside ja toimingute rakenduse virtuaalmasinasse (VM) sisselogimine.
2. Avage Microsofti halduskonsool.
3. Paanil **Teenused** veenduge, et Microsoft Dynamics 365 andmete importimise/eksportimise raamistiku teenus töötab. Taaskäivitage see, kui see on peatatud, kuna esmane sünkroonimine nõuab seda.

## <a name="initial-synchronization-error-403-forbidden"></a>Esmase sünkroonimise tõrge: 403 keelatud

Teile võidakse kuvada esmase sünkroonimise ajal järgmine tõrketeade.

*(\[Keelatud\], kaugserver tagastas tõrke: (403) keelatud.), AX eksportimisel ilmnes tõrge*

Probleemi lahendamiseks tehke järgmist.

1. Logige sisse finantside ja toimingute rakendusse.
2. Kustutage lehel **Azure Active Directory rakendused** klient **DtAppID** ja seejärel lisage see uuesti.

![DtAppID klient Azure AD rakenduste loendis.](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Eneseviite või ringviite tõrked esmase sünkroonimise ajal

Teile võidakse kuvada tõrketeade, kui mõnel teie vastendustest on eneseviited või ringviited. Tõrked jagunevad järgmistesse kategooriatesse.

- [Tõrked tabeli Hankijad V2 vastendamisel üksusega msdyn_vendors](#error-vendor-map)
- [Tõrked tabeli Kliendid V3 vastendamisel üksusega Kontod](#error-customer-map)

## <a name="resolve-errors-in-the-vendors-v2tomsdyn_vendors-table-mapping"></a><a id="error-vendor-map"></a>Tõrgete lahendamine tabeli Hankijad V2 vastendamisel üksusega msdyn_vendors

Üksuse **Hankijad V2** vastendamisel üksusega **msdyn\_vendors** võivad ilmneda esmase sünkroonimise tõrked, kui tabelitel on olemasolevaid ridu, mille veerud **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** sisaldavad väärtusi. Tõrked ilmnevad seetõttu, et hankija vastendamisel on **InvoiceVendorAccountNumber** enesele viitav veerg ja **PrimaryContactPersonId** ringviitav väli.

Ilmnenud tõrketeated kuvatakse järgmises vormis.

*Guidi ei saanud lahendada väljal: \<field\>. Otsingut ei leitud: \<value\>. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Järgmisena on toodud mõned näited.

- *Guidi ei saanud lahendada väljal: msdyn\_vendorprimarycontactperson.msdyn\_contactpersonid. Otsingut ei leitud: 000056. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Guidi ei saanud lahendada väljal: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Otsingut ei leitud: V24-1. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'`*

Kui hankija tabelis on read, mille veerud **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** sisaldavad väärtusi, siis järgige neid samme, et esmane sünkroonimine lõpule viia.

1. Kustutage finantside ja toimingute rakenduses **vastendusest veerud PrimaryContactPersonId** **ja InvoiceVendorAccountNumber** ning seejärel salvestage vastendus.

    1. Topeltkirjutuse vastendamise **lehel hankijate V2 (msdandmiku\_ hankijad)** **jaoks valige tabeli vastenduste vahekaardi vasakpoolses filtris** **finantside ja toimingute rakendused. Hankijad V2**. Valige parempoolses filtris **Müük.Hankija**.
    2. Otsige väärtust **primarycontactperson**, et leida allika veerg **PrimaryContactPersonId**.
    3. Valige **Tegevused** ja seejärel **Kustuta**.

        ![Veeru PrimaryContactPersonId kustutamine.](media/vend_selfref3.png)

    4. Veeru **InvoiceVendorAccountNumber** kustutamiseks korrake neid samme.

        ![Veeru InvoiceVendorAccountNumber kustutamine.](media/vend-selfref4.png)

    5. Salvestage oma muudatused vastendusse.

2. Lülitage tabeli **Hankijad V2** muudatuste jälgimine välja.

    1. Valige tööruumis **Andmehaldus** paan **Andmetabelid**.
    2. Valige tabel **Hankijad V2**.
    3. Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.

        ![Muudatuse jälgimise suvandi valimine.](media/selfref_options.png)

    4. Valige **Keela muudatuste jälgimine**.

        ![Suvandi „Keela muudatuste jälgimine” valimine.](media/selfref_tracking.png)

3. Käivitage üksuse **Hankijad V2 (msdyn\_vendors)** vastenduse esmane sünkroonimine. Esmane sünkroonimine peaks toimima tõrgeteta.
4. Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastenduse esmane sünkroonimine. Selle vastenduse peate sünkroonima juhul, kui soovite sünkroonida hankijate tabeli põhikontakti veergu, kuna ka kontaktiread tuleb esmasünkroonida.
5. Lisage veerud **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** tagasi vastendusse **Hankijad V2 (msdyn\_vendors)** ning seejärel salvestage vastendus.
6. Käivitage uuesti üksuse **Hankijad V2 (msdyn\_vendors)** vastenduse esmane sünkroonimine. Kuna muudatuste jälgimine on välja lülitatud, sünkroonitakse kõik read.
7. Lülitage tabeli **Hankijad V2** muudatuste jälgimine tagasi sisse.

## <a name="resolve-errors-in-the-customers-v3toaccounts-table-mapping"></a><a id="error-customer-map"></a>Tõrgete lahendamine tabeli Kliendid V3 vastendamisel üksusega Kontod

Üksuse **Kliendid V3** vastendamisel üksusega **Kontod** võivad ilmneda esmase sünkroonimise tõrked, kui tabelitel on olemasolevaid ridu, mille veerud **ContactPersonID** ja **InvoiceAccount** sisaldavad väärtusi. Need tõrked ilmnevad seetõttu, et hankija vastendamisel on **InvoiceAccount** enesele viitav veerg ja **ContactPersonID** ringviitav veerg.

Ilmnenud tõrketeated kuvatakse järgmises vormis.

*Guidi ei saanud lahendada väljal: \<field\>. Otsingut ei leitud: \<value\>. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>`*

Järgmisena on toodud mõned näited.

- *Guidi ei saanud lahendada väljal: primarycontactid.msdyn\_contactpersonid. Otsingut ei leitud: 000056. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'`*
- *Guidi ei saanud lahendada väljal: msdyn\_billingaccount.accountnumber. Otsingut ei leitud: 1206-1. Proovige seda URL-i, et kontrollida kas viiteandmed on olemas: `https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'`*

Kui kliendi tabelis on read, mille veerud **ContactPersonID** ja **InvoiceAccount** sisaldavad väärtusi, siis järgige neid samme, et esmane sünkroonimine lõpule viia. Seda meetodit saate kasutada kõikide valmiskujul tabelite puhul, nagu näiteks **Kontod** ja **Kontaktid**.

1. Finantside ja toimingute rakenduses kustutage **veerud ContactPersonID** ja **InvoiceAccount** **klientide V3 (kontode)** vastendusest ja seejärel salvestage vastendus.

    1. **Klientide V3 (** kontod) topeltkirjutuse vastendamise lehel valige **tabeli vastenduste vahekaardi vasakpoolses filtris** finantside **ja toimingute rakendus. Kliendid V3**. Valige parempoolses filtris **Dataverse.Account**.
    2. Otsige väärtust **contactperson**, et leida allika veerg **ContactPersonID**.
    3. Valige **Tegevused** ja seejärel **Kustuta**.

        ![Veeru ContactPersonID kustutamine.](media/cust_selfref3.png)

    4. Veeru **InvoiceAccount** kustutamiseks korrake neid samme.

        ![Veeru InvoiceAccount kustutamine.](media/cust_selfref4.png)

    5. Salvestage oma muudatused vastendusse.

2. Lülitage tabeli **Kliendid V3** muudatuste jälgimine välja.

    1. Valige tööruumis **Andmehaldus** paan **Andmetabelid**.
    2. Valige tabel **Kliendid V3**.
    3. Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.

        ![Muudatuse jälgimise suvandi valimine.](media/selfref_options.png)

    4. Valige **Keela muudatuste jälgimine**.

        ![Suvandi „Keela muudatuste jälgimine” valimine.](media/selfref_tracking.png)

3. Käivitage üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine. Esmane sünkroonimine peaks toimima tõrgeteta.
4. Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastenduse esmane sünkroonimine.

    > [!NOTE]
    > Sama nimega vastendusi on kaks. Valige vastendus, millel on vahekaardil **Üksikasjad** järgmine kirjeldus: **Topeltkirjutamise mall üksuse FO.CDS Hankija Kontaktid V2 sünkroonimiseks üksusega CDS.Kontaktid. Vajab uut paketti \[Dynamics365SupplyChainExtended\].**

5. Lisage veerud **InvoiceAccount** ja **ContactPersonId** tagasi vastendusse **Kliendid V3 (Kontod)** ning seejärel salvestage vastendus. Nüüd on nii veerg **InvoiceAccount** kui ka veerg **ContactPersonId** taas osa reaalajas sünkroonimise režiimist. Järgmise sammu käigus esmasünkroonite need veerud.
6. Käivitage uuesti üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine. Kuna muudatuste jälitamine on välja lülitatud **, sünkroonitakse InvoiceAccount** **ja ContactPersonId** andmed finantside ja toimingute rakendusest rakendusesse Dataverse.
7. InvoiceAccount ja ContactPersonId **andmete sünkroonimiseks finantside** ja toimingute rakendusest peate kasutama andmete integreerimisprojekti.**·** Dataverse

    1. Looge Power Apps andmete integreerimise projekt Müügi.konto **ja finantside ning** **toimingute rakenduste vahel. Klientide V3-tabelid**. Andmesuund peab olema finantside Dataverse ja toimingute rakendusest. Kuna **InvoiceAccount** on topeltkirjutuses uus atribuut, siis võite selle atribuudi esmase sünkroonimise vahele jätta. Lisateavet vt teemast [Andmete integreerimine teenusesse Dataverse](/power-platform/admin/data-integrator).

        Järgmisel illustratsioonil on toodud projekt, mis värskendab väljasid **CustomerAccount** ja **ContactPersonId**.

        ![Andmeintegratsiooni projekt väljade CustomerAccount ja ContactPersonId värskendamiseks.](media/cust_selfref6.png)

    2. Lisage ettevõtte kriteeriumid filtrile Dataverse poolel, nii et finantside ja toimingute rakenduses uuendatakse ainult read, mis vastavad filtri kriteeriumidele. Filtri lisamiseks valige filtri nupp. Seejärel saate dialoogiboksis **Päringu redigeerimine** lisada filtri päringu, nagu näiteks **\_msdyn\_company\_value eq '\<guid\>'**.

        > [MÄRKUS] Kui filtri nuppu ei kuvata, siis saate luua tugiteenusepileti, et paluda andmeintegratsiooni meeskonnal lubada teie rentnikus filtri võimalus.

        Kui te ei sisesta **\_msdyn\_company\_value** jaoks filtri päringut, siis sünkroonitakse kõik read.

        ![Filtri päringu lisamine.](media/cust_selfref7.png)

    Ridade esmane sünkroonimine on nüüd lõpule viidud.

8. Lülitage finantside ja toimingute rakenduses muudatuste jälitamine tagasi tabeli **Klientide V3** jaoks.

## <a name="initial-sync-failures-on-maps-with-more-than-10-lookup-fields"></a>Algse sünkroonimise tõrked rohkem kui 10 otsinguväljaga vastetel

Võite saada järgmise tõrketeate, kui proovite käitada **klientide V3 – kontode**, **müügitellimuste** vastenduste või muu enam kui 10 otsinguväljaga vastendusi:

*CRMExport: paketi täitmine on lõpule viidud. Tõrke kirjeldus 5 katset võtta andmeid https://xxxxx//datasets/yyyyy/tables/accounts/items? $select=accountnumber, address2_city, address2_country, ... (msdyn_company/cdm_companyid eq ID)&$orderby=accountnumber asc nurjus.*

Otsingupiirangu tõttu päringus nurjub esialgne sünkroonimine, kui üksuse vastendamine sisaldab rohkem kui 10 otsingut. Lisateavet vt teemast [Seotud tabelikirjete toomine päringuga](/powerapps/developer/common-data-service/webapi/retrieve-related-entities-query).

Selle probleemi lahendamiseks tehke järgmist:

1. Eemaldage valikulised otsinguväljad topeltkirjutuse üksuse kaardist, et otsingute arv oleks 10 või vähem.
2. Salvestage kaart ja sünkroonige esialgne.
3. Kui esimese sammu esialgne sünkroonimine õnnestus, lisage ülejäänud otsinguväljad ja eemaldage esimeses sammus sünkroonitud otsinguväljad. Kontrollige, et otsinguväljade arv oleks 10 või vähem. Salvestage kaart ja käitage esialgne sünkroonimine.
4. Korrake neid samme, kuni kõik otsinguväljad on sünkroonitud.
5. Lisage kõik otsinguväljad tagasi kaardile, salvestage kaart ja käivitage kaart käsuga **Jäta algne sünkroonimine vahele**.

See protsess võimaldab kaardi reaalajas sünkroonimisrežiimi jaoks.

## <a name="known-issue-during-initial-sync-of-party-postal-addresses-and-party-electronic-addresses"></a>Teadaolev probleem osapoole postiaadresside ja osapoole elektrooniliste aadresside esmasel sünkroonimisel

Kui proovite käivitada osapoole postiaadresside ja osapoole elektrooniliste aadresside algset sünkroniseerimist, võidakse kuvada järgmine tõrketeade:

*Osapoole numbrit Dataverse`ist ei leitud.*

Finantside ja toimingute rakendustes on **DirPartyCDSEntity** häälestatud vahemik, mis filtreerib isiku ja organisatsiooni **tüüpi** osapooli **·**. Selle tulemusena **CDS-i osapoolte - msdyn_parties** vastendamine ei sünkrooni teist tüüpi osapooli, sh **juriidilist isikut** ja **tootmisüksust**. Kui algne sünkroonimine töötab **CDS Party postiaadresside (msdyn_partypostaladdresses)** või **Party Contacts V3 (msdyn_partyelectronicaddresses)** puhul, võidakse kuvada tõrge.

Töötame parandusega, et eemaldada finantside ja toimingute üksusest osapoole tüübi vahemik, nii et igat tüüpi osapooled saavad edukalt sünkroonida Dataverse.

## <a name="are-there-any-performance-issues-while-running-initial-sync-for-customers-or-contacts-data"></a>Kas klientide või kontaktide andmete algsel sünkroonimisel ilmnes jõudlusprobleeme?

Kui olete käivitanud **kliendi** andmete esmase sünkroonimise ja **Kliendi** vastendused on käivitatud ning seejärel käivitate **Kontaktid** andmete esmase sünkroonimise, võivad värskendustel olla jõudlusprobleemid tabelite sisestamisel **LogisticsPostalAddress** ja **LogisticsElectronicAddress** tabelitesse **Kontaktid** aadressides. Sama globaalset postiaadressi ja elektroonilist aadressitabelit jälgitakse **KohandKlientV3Üksus** ja **HankHankijaV2Üksus** puhul ja topeltkirjutus püüab luua rohkem päringuid, et kirjutada andmeid teisele poolele. Kui olete **kliendi** algse sünkroonimise juba käitanud, siis peatage vastav kaart **Kontaktide** andmete algse sünkroonimise ajal. Tehke sama asja **hankija** andmete jaoks. Kui esialgne sünkroonimine on lõpetatud, saate käivitada kõik kaardid, jättes algse sünkroonimise vahele.

## <a name="float-data-type-that-has-a-zero-value-cant-be-synchronized"></a>Nullväärtusega andmetüüpi ei saa sünkroonida.

Esialgne sünkroonimine võib nurjuda kirjete puhul, mille hinnaväljal on nullväärtus, **nt Fikseeritud makse summa** või **Summa** kandevaluutas. Sel juhul kuvatakse tõrketeade, mis sarnaneb järgmise näitega:

*Sisendparameetrite valideerimisel ilmnes tõrge: Microsoft.OData.ODataException: literaal ’000000’ ei saa teisendada eeldatavaks tüübiks’Edm. Kümnendkoha,...*

Probleem on seotud väärtusega **Language locale** lähteandmete **vormingute all** andmehalduse **moodulis**. Muutke välja **Language loke väärtuseks** **En-us** ja proovige uuesti.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

