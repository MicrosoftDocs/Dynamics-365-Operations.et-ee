---
title: Probleemide tõrkeotsing esmase sünkroonimise ajal
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 10065039fce441d7f96f700ff826d959e96f2479
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410077"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Probleemide tõrkeotsing esmase sünkroonimise ajal

[!include [banner](../../includes/banner.md)]

See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see teavet, mis aitab lahendada lahenduse teadlikkusega seotud probleeme, mis võivad ilmneda esialgse sünkroonimise käigus.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Esmase sünkroonomise tõrgete kontrollimine Finance and Operationsi rakenduses

Pärast vastendamise mallide lubamist peaks vastenduse olekuks olema **Töötab**. Kui olek on **Ei tööta**, ilmnes tõrkeid esmasel sünkroonimisel. Tõrgete kuvamiseks valige lehel **Topeltkirjutus** vahekaart **Esmase sünkroonimise üksikasjad**.

![Esmase sünkroonimise üksikasjade vahekaart](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Esmast sünkroonimist ei saa lõpule viia: 400 vigane päring

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui proovite käivitada vastendust ja esmast sünkroonimist, võidakse kuvada järgmine tõrketeade.

*Kaugserver tagastas tõrke: (400) vigane päring.), AXeksportimisel ilmnes tõrge*

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

![Azure AD rakenduste loend](media/aad_applications.png)

## <a name="self-reference-or-circular-reference-failures-during-initial-synchronization"></a>Eneseviite või ringviite tõrked esmase sünkroonimise ajal

Teile võidakse kuvada tõrketeade, kui mõnel teie vastendustest on eneseviited või ringviited. Tõrked jagunevad järgmistesse kategooriatesse.

- [Üksuse Hankijad V2 vastendamine üksusega msdyn_vendors](#error-vendor-map)
- [Üksuse Kliendid V3 vastendamine üksusega Kontod](#error-customer-map)

## <a name="resolve-an-error-in-vendors-v2-to-msdyn_vendors-entity-mapping"></a><a id="error-vendor-map"></a>Tõrgete lahendamine üksuse Hankijad V2 vastendamisel üksusega msdyn_vendors

Üksuse **Hankijad V2** vastendamisel üksusega **msdyn_vendors** võivad tekkida järgmised esmase sünkroonimise tõrked, kui üksustel on olemas väärtustatud kirjed väljadel **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber**. See juhtub seetõttu, et hankija vastendamisel on **InvoiceVendorAccountNumber** enesele viitav väli ja **PrimaryContactPersonId** ringviitav väli.

*Guidi ei saanud lahendada väljal: <field>. Otsingut ei leitud: <value>. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

Järgnevalt on esitatud mõned näited.

- *Guidi ei saanud lahendada väljal: msdyn_vendorprimarycontactperson.msdyn_contactpersonid. Otsingut ei leitud: 000056. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Guidi ei saanud lahendada väljal: msdyn_invoicevendoraccountnumber.msdyn_vendoraccountnumber. Otsingut ei leitud: V24-1. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/msdn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber eq 'V24-1'*

Kui teil on hankija üksuses nendel väljadel väärtusi sisaldavaid kirjeid, siis järgige alltoodud jaotises esitatud etappe, et esmane sünkroonimine edukalt lõpule viia.

1. Kustutage rakenduses Finance and Operations vastendamisest väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** ning salvestage muudatused.

    1. Liikuge **Hankijad V2 (msdyn_vendors)** topeltkirjutuse vastendamislehele ja valige vahekaart **Üksuse vastendused**. Valige vasakpoolses filtris suvand **Finance and Operationsi rakendused. Hankijad V2**. Valige parempoolses filtris **Müük.Hankija**.

    2. Otsige väärtust **primarycontactperson**, et leida allika väli **PrimaryContactPersonId**.
    
    3. Klõpsake nuppu **Toimingud** ja valige **Kustuta**.
    
        ![enese- või ringviide 3](media/vend_selfref3.png)
    
    4. Välja **InvoiceVendorAccountNumber** kustutamiseks korrake toimingut.
    
        ![enese- või ringviide 4](media/vend-selfref4.png)
    
    5. Salvestage vastendamise muudatused.

2. Keelake üksuse **Hankijad V2** muudatuste jälgimine.

    1. Avage **Andmehaldus \> Andmeüksused**.
    
    2. Valige üksus **Hankijad V2**.
    
    3. Klõpsake menüüribal **Suvandid** ja seejärel **Muudatuste jälgimine**.
    
        ![enese- või ringviide 5](media/selfref_options.png)
    
    4. Klõpsake suvandil **Keela muudatuste jälgimine**.
    
        ![enese- või ringviide 6](media/selfref_tracking.png)

3. Käivitage üksuse **Hankijad V2 (msdyn_vendors)** vastendamise esmane sünkroonimine. Esmane sünkroonimine peaks toimima tõrgeteta.

4. Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastendamise esmane sünkroonimine. Selle vastenduse peate sünkroonima juhul, kui soovite sünkroonida hankijate üksuse põhikontakti välja, kuna ka kontaktide kirjed tuleb esmasünkroonida.

5. Lisage vastendusele **Hankijad V2 (msdyn_vendors)** tagasi väljad **PrimaryContactPersonId** ja **InvoiceVendorAccountNumber** ning salvestage vastendus.

6. Käivitage uuesti üksuse **Hankijad V2 (msdyn_vendors)** vastendamise esmane sünkroonimine. Kõik kirjed sünkroonitakse, kuna muudatuste jälgimine on keelatud.

7. Lubage üksuse **Hankijad V2** muudatuste jälgimine.

## <a name="resolve-an-error-in-customers-v3-to-accounts-entity-mapping"></a><a id="error-customer-map"></a>Tõrgete lahendamine üksuse Kliendid V3 vastendamisel üksusega Kontod

Üksuse **Kliendid V3** vastendamisel üksusega **Kontod** võivad tekkida järgmised esmase sünkroonimise tõrked, kui üksustel on olemas väärtustatud kirjed väljadel **ContactPersonID** ja **InvoiceAccount**. See juhtub seetõttu, et hankija vastendamisel on **InvoiceAccount** enesele viitav väli ja **ContactPersonID** ringviitav väli.

*Guidi ei saanud lahendada väljal: <field>. Otsingut ei leitud: <value>. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/<entity>?$select=<field>&$filter=<field> eq <value>*

- *Guidi ei saanud lahendada väljal: primarycontactid.msdyn_contactpersonid. Otsingut ei leitud: 000056. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/contacts?$select=msdyn_contactpersonid.contactid&$filter=msdyn_contactpersonid eq '000056'*
- *Guidi ei saanud lahendada väljal: msdyn_billingaccount.accountnumber. Otsingut ei leitud: 1206-1. Proovige URL-i, et kontrollida kas viiteandmed on olemas: https://focdsdevtest2.crm.dynamics.com/api/data/v9.0/accounts?$select=accountnumber.account&$filter=accountnumber eq '1206-1'*

Kui teil on kliendi üksuses nendel väljadel väärtusi sisaldavaid kirjeid, siis järgige alltoodud jaotises esitatud etappe, et esmane sünkroonimine edukalt lõpule viia. Seda lähenemist saab kasutada kõikide valmiskujul üksuste, nagu näiteks Kontode ja Kontaktide puhul.

1. Kustutage rakenduses Finance and Operations vastendusest **Kliendid V3 (kontod)** väljad **ContactPersonID** ja **InvoiceAccount** ning salvestage vastendus.

    1. Liikuge **Kliendid V3 (kontod)** topeltkirjutuse vastendamislehele ja valige vahekaart **Üksuse vastendused**. Valige vasakpoolses filtris suvand **Finance and Operationsi rakendus. Kliendid V3**. Valige parempoolses filtris **Common Data Service. Konto**.

    2. Otsige väärtust **contactperson**, et leida allika väli **ContactPersonID**.
    
    3. Klõpsake nuppu **Toimingud** ja valige **Kustuta**.
    
        ![enese- või ringviide 3](media/cust_selfref3.png)
    
    4. Välja **InvoiceAccount** kustutamiseks korrake toimingut.
    
        ![enese- või ringviide](media/cust_selfref4.png)
    
    5. Salvestage vastendamise muudatused.

2. Keelake üksuse **Kliendid V3** muudatuste jälgimine.

    1. Avage **Andmehaldus \> Andmeüksused**.
    
    2. Valige üksus **Kliendid V3**.
    
    3. Klõpsake menüüribal **Suvandid** ja seejärel **Muudatuste jälgimine**.
    
        ![enese- või ringviide 5](media/selfref_options.png)
    
    4. Klõpsake suvandil **Keela muudatuste jälgimine**.
    
        ![enese- või ringviide 6](media/selfref_tracking.png)

3. Käivitage üksuse **Kliendid V3 (kontod)** vastendamise esmane sünkroonimine. Esmane sünkroonimine peaks toimima tõrgeteta.

4. Käivitage üksuse **CDS-i kontaktid V2 (kontaktid)** vastendamise esmane sünkroonimine. Seal on kaks sama nimega vastendust. Valige järgmise kirjeldusega vastendus: **Topeltkirjutamise mall FO.CDS Hankija Kontaktid V2 üksusega CDS.Kontaktid sünkroonimiseks. Vajab uut paketti \[Dynamics365SupplyChainExtended\].** vastenduse vahekaardil **Üksikasjad**.

5. Lisage väljad **InvoiceAccount** ja **ContactPersonId** tagasi vastendusele **Kliendid V3 (Kontod)** ning salvestage vastendus. Nüüd on nii väli **InvoiceAccount** kui ka väli **ContactPersonId** taas osa reaalajas sünkroonimise režiimist. Järgmises etapi käigus viite väljade esmase sünkroonimise lõpule.

6. Käivitage uuesti üksuse **Kliendid V3 (kontod)** vastendamise esmane sünkroonimine. Kuna muudatuste jälgimine on keelatud, siis sünkroonitakse sünkroonimise käivitamisel väljade **InvoiceAccount** ja **ContactPersonId** andmed rakendusest Finance and Operations rakendusega Common Data Service.

7. Väljade **InvoiceAccount** ja **ContactPersonId** andmete sünkroonimiseks rakendusest Common Data Service rakendusega Finance and Operations saate kasutada andmete integreerimise projekti.

    1. Looge rakenduses Power Apps üksuste **Müük. Konto** ja **Finance and Operationsi rakendused. Kliendid V3** vahel andmete integreerimise projekt. Andmete suund peab olema rakendusest Common Data Service rakendusse Finance and Operations.  Kuna **InvoiceAccount** on topeltkirjutuses uus atribuut, siis võiksite selle atribuudi esmase sünkroonimise vahele jätta. Lisateavet vt teemast [Andmete integreerimine teenusesse Common Data Service](https://docs.microsoft.com/power-platform/admin/data-integrator).

        Järgmisel pildil on toodud projekt, mis värskendab väljasid **CustomerAccount** ja **ContactPersonId**.

        ![enese- või ringviide](media/cust_selfref6.png)

    2. Lisage teenuse Common Data Service poolel filtrite all ettevõtte kriteeriumid, kuna rakenduses Finance and Operations värskendatakse vaid filtri kriteeriumidele vastavad kirjed. Filtri lisamiseks klõpsake filtri ikoonil. Dialoogis **Päringu redigeerimine** saate lisada filtri päringu, nagu näiteks **_msdyn_company_value eq '\<guid\>'**. Kui filtri ikooni ei paista, siis saate luua tugiteenuse pileti, et paluda andmete integreerimise meeskonnal lubada teie rentnikus filtri võimalus. Kui te ei sisesta **_msdyn_company_value** jaoks filtri päringut, siis sünkroonitakse kõik kirjed.

        ![enese- või ringviide](media/cust_selfref7.png)

        See viib kirjete esialgse sünkroonimise lõpule.

8. Finance and Operationsi rakenduses üksuse **Kliendid V3** muudatuste jälgimise lubamine.

