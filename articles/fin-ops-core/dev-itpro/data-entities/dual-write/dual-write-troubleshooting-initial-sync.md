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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172710"
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

## <a name="self-reference-failures-during-initial-synchronization"></a>Eneseviite tõrked esmase sünkroonimise ajal

Teile võidakse kuvada tõrketeade, mis sarnaneb järgmisele näitele, kui mõnel teie vastendustest on eneseviited.

*Hankijatel V2 järgnev tõrge: kirje ID: uus kirje, ErrorMessage: guidi ei saanud lahendada väljal: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. Otsinguväärtust ei leitud: CN-001. Proovige URL-i, et kontrollida kas viiteandmed on olemas: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Seda tüüpi tõrget ilmneb vastenduste esmastel sünkroonimistel, millel on eneseviited. Eelnevas näites viitab välja arve konto hankija üksusele.

Probleemi lahendamiseks peate tõenäoliselt edukaks esmaseks sünkroonimiseks käitama vastendamist kaks korda.

