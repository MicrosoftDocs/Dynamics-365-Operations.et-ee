---
title: Probleemide tõrkeotsing esmase sünkroonimise ajal
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 709a3c332bb6d086910b257fee9cdec8d2bc81a2
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941051"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Probleemide tõrkeotsing esmase sünkroonimise ajal

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Esmase sünkroonomise tõrgete kontrollimine Finance and Operationsi rakenduses

Pärast vastendamise mallide lubamist peaks vastenduse olekuks olema **Töötab**. Kui olek on **Ei tööta**, ilmnes tõrkeid esmasel sünkroonimisel. Tõrgete kuvamiseks valige lehel **Topeltkirjutus** vahekaart **Esmase sünkroonimise üksikasjad**.

![Esmase sünkroonimise üksikasjade vahekaardi tõrge](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Esmast sünkroonimist ei saa lõpule viia: 400 vigane päring

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui proovite käivitada vastendust ja esmast sünkroonimist, võidakse kuvada järgmine tõrketeade.

*(\[Vigane päring\], kaugserver tagastas tõrke: (400) vigane päring.), AX eksportimisel ilmnes tõrge*

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

1. Logige rakenduse Finance and Operations virtuaalarvutisse (VM) sisse.
2. Avage Microsofti halduskonsool.
3. Paanil **Teenused** veenduge, et Microsoft Dynamics 365 andmete importimise/eksportimise raamistiku teenus töötab. Taaskäivitage see, kui see on peatatud, kuna esmane sünkroonimine nõuab seda.

## <a name="initial-synchronization-error-403-forbidden"></a>Esmase sünkroonimise tõrge: 403 keelatud

Teile võidakse kuvada esmase sünkroonimise ajal järgmine tõrketeade.

*(\[Keelatud\], kaugserver tagastas tõrke: (403) keelatud.), AX eksportimisel ilmnes tõrge*

Probleemi lahendamiseks tehke järgmist.

1. Logige rakendusse Finance and Operations sisse.
2. Kustutage lehel **Azure Active Directory rakendused** klient **DtAppID** ja seejärel lisage see uuesti.

![DtAppID klient Azure AD rakenduste loendis](media/aad_applications.png)

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

1. Kustutage rakenduses Finance and Operations vastendusest veerud **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** ning seejärel salvestage vastendus.

    1. Avage **Hankijad V2 (msdyn\_vendors)** topeltkirjutuse vastendamisleht ja seejärel vahekaart **Tabeli vastendused**. Valige vasakpoolses filtris suvand **Finance and Operations apps.Vendors V2**. Valige parempoolses filtris **Müük.Hankija**.
    2. Otsige väärtust **primarycontactperson**, et leida allika veerg **PrimaryContactPersonId**.
    3. Valige **Tegevused** ja seejärel **Kustuta**.

        ![Veeru PrimaryContactPersonId kustutamine](media/vend_selfref3.png)

    4. Veeru **InvoiceVendorAccountNumber** kustutamiseks korrake neid samme.

        ![Veeru InvoiceVendorAccountNumber kustutamine](media/vend-selfref4.png)

    5. Salvestage oma muudatused vastendusse.

2. Lülitage tabeli **Hankijad V2** muudatuste jälgimine välja.

    1. Valige tööruumis **Andmehaldus** paan **Andmetabelid**.
    2. Valige tabel **Hankijad V2**.
    3. Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.

        ![Muudatuse jälgimise suvandi valimine](media/selfref_options.png)

    4. Valige **Keela muudatuste jälgimine**.

        ![Suvandi „Keela muudatuste jälgimine” valimine](media/selfref_tracking.png)

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

1. Kustutage rakenduses Finance and Operations vastendusest **Kliendid V3 (kontod)** veerud **ContactPersonID** ja **InvoiceAccount** ning seejärel salvestage vastendus.

    1. Avage **Kliendid V3 (kontod)** topeltkirjutuse vastendamisleht ja seejärel vahekaart **Tabeli vastendused**. Valige vasakpoolses filtris suvand **Finance and Operations app.Customers V3**. Valige parempoolses filtris **Dataverse.Account**.
    2. Otsige väärtust **contactperson**, et leida allika veerg **ContactPersonID**.
    3. Valige **Tegevused** ja seejärel **Kustuta**.

        ![Veeru ContactPersonID kustutamine](media/cust_selfref3.png)

    4. Veeru **InvoiceAccount** kustutamiseks korrake neid samme.

        ![Veeru InvoiceAccount kustutamine](media/cust_selfref4.png)

    5. Salvestage oma muudatused vastendusse.

2. Lülitage tabeli **Kliendid V3** muudatuste jälgimine välja.

    1. Valige tööruumis **Andmehaldus** paan **Andmetabelid**.
    2. Valige tabel **Kliendid V3**.
    3. Valige tegumipaanilt **Suvandid** ja seejärel **Muudatuste jälgimine**.

        ![Muudatuse jälgimise suvandi valimine](media/selfref_options.png)

    4. Valige **Keela muudatuste jälgimine**.

        ![Suvandi „Keela muudatuste jälgimine” valimine](media/selfref_tracking.png)

3. Käivitage üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine. Esmane sünkroonimine peaks toimima tõrgeteta.
4. Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastenduse esmane sünkroonimine.

    > [!NOTE]
    > Sama nimega vastendusi on kaks. Valige vastendus, millel on vahekaardil **Üksikasjad** järgmine kirjeldus: **Topeltkirjutamise mall üksuse FO.CDS Hankija Kontaktid V2 sünkroonimiseks üksusega CDS.Kontaktid. Vajab uut paketti \[Dynamics365SupplyChainExtended\].**

5. Lisage veerud **InvoiceAccount** ja **ContactPersonId** tagasi vastendusse **Kliendid V3 (Kontod)** ning seejärel salvestage vastendus. Nüüd on nii veerg **InvoiceAccount** kui ka veerg **ContactPersonId** taas osa reaalajas sünkroonimise režiimist. Järgmise sammu käigus esmasünkroonite need veerud.
6. Käivitage uuesti üksuse **Kliendid V3 (kontod)** vastenduse esmane sünkroonimine. Kuna muudatuste jälgimine on välja lülitatud, siis sünkroonitakse väljade **InvoiceAccount** ja **ContactPersonId** andmed rakendusest Finance and Operations rakendusega Dataverse.
7. Väljade **InvoiceAccount** ja **ContactPersonId** andmete sünkroonimiseks rakendusest Dataverse rakendusega Finance and Operations peate kasutama andmeintegratsiooni projekti.

    1. Looge rakenduses Power Apps tabelite **Sales.Account** ja **Finance and Operations apps.Customers V3** vahel andmete integreerimise projekt. Andmete suund peab olema rakendusest Dataverse rakendusse Finance and Operations. Kuna **InvoiceAccount** on topeltkirjutuses uus atribuut, siis võite selle atribuudi esmase sünkroonimise vahele jätta. Lisateavet vt teemast [Andmete integreerimine teenusesse Dataverse](/power-platform/admin/data-integrator).

        Järgmisel illustratsioonil on toodud projekt, mis värskendab väljasid **CustomerAccount** ja **ContactPersonId**.

        ![Andmeintegratsiooni projekt väljade CustomerAccount ja ContactPersonId värskendamiseks](media/cust_selfref6.png)

    2. Lisage teenuse Dataverse poolel filtrite all ettevõtte kriteeriumid, et rakenduses Finance and Operations värskendataks vaid filtri kriteeriumidele vastavaid ridu. Filtri lisamiseks valige filtri nupp. Seejärel saate dialoogiboksis **Päringu redigeerimine** lisada filtri päringu, nagu näiteks **\_msdyn\_company\_value eq '\<guid\>'**. 

        > [MÄRKUS] Kui filtri nuppu ei kuvata, siis saate luua tugiteenusepileti, et paluda andmeintegratsiooni meeskonnal lubada teie rentnikus filtri võimalus.

        Kui te ei sisesta **\_msdyn\_company\_value** jaoks filtri päringut, siis sünkroonitakse kõik read.

        ![Filtri päringu lisamine](media/cust_selfref7.png)

    Ridade esmane sünkroonimine on nüüd lõpule viidud.

8. Lülitage rakenduses Finance and Operations tabeli **Kliendid V3** muudatuste jälgimine tagasi sisse.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]