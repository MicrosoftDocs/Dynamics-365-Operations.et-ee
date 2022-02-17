---
title: Finance and Operationsi rakenduste värskenduste probleemide tõrkeotsing
description: Selles teemas on tõrkeotsinguteave, mis aitab teil lahendada probleeme, mis on seotud Finance and Operationsi rakenduste täiendustega.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c7c036ef44b0470c9b3f8087e7b5b1e16dde1b34
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062821"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Finance and Operationsi rakenduste värskenduste probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]





See teema pakub tõrkeotsinguteavet finance and Operationsi rakenduste ja rakenduse kahe kirjutamise integreerimiseks Dataverse. Täpsemalt pakub see teavet, mis aitab teil lahendada probleeme, mis on seotud Finance and Operationsi rakenduste uuendamisega.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="database-synchronization-errors"></a>Andmebaasi sünkroonimise tõrked

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Kui proovite kasutada tabelit **DualWriteProjectConfiguration**, võite saada tõrketeate, mis sarnaneb järgmise näitega, et värskendada finance and Operationsi rakendus platvormivärskendusse 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Probleemi lahendamiseks tehke järgmist.

1. Logige sisse rakendus Finance and Operations virtuaalmasinasse (VM).
2. Avage Visual Studio administraatorina ja avage rakendusobjektide puu (AOT).
3. Sisestage otsigusse **DualWriteProjectConfiguration**.
4. AOT-s paremklõpsake valikut **DualWriteProjectConfiguration** ja valige **Lisa uuele projektile**. Vajutage **OK**, et luua uus projekt, mis kasutab vaikesuvandeid.
5. Paremklõpsake Solution Exploreris valikut **Projekti atribuudid** ja seadke **Sünkrooni andmebaasi koostamisel** väärtuseks **Tõene**.
6. Koostage projekt ja kinnitage, et see on edukas.
7. Valige menüüs **Dynamics 365** suvand **Sünkrooni andmebaas**.
8. Täieliku andmebaasi sünkroonimise tegemiseks valige **Sünkrooni**.
9. Kui täielik andmebaasi sünkroonimine õnnestub, käivitage uuesti andmebaasi sünkroonimise etapp Microsoft Dynamics Lifecycle Servicesis (LCS) ja kasutage vastavalt vajadusele käsitsi uuendamise skripte, nii et saate jätkata värskendust.

## <a name="missing-table-columns-issue-on-maps"></a>Puuduvate tabeli veergude probleem vastendustes

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Teile võidakse kuvada lehel **Topeltkirjutus** tõrketeade, mis sarnaneb järgmisele näitele.

*Puuduv allika väli \<field name\> skeemis.*

![Puuduva allika veeru tõrketeate näide.](media/error_missing_field.png)

Probleemi lahendamiseks tehke esmalt need toimingud veendumaks, et veerud oleks tabelis olemas.

1. Logige sisse rakendusse Finance and Operations.
2. Avage **Tööruumid \> Andmehaldus**, valige paan **Raamistiku parameetrid** ja seejärel valige vahekaardil **Tabeli sätted** tabelite värskendamiseks **Värskenda tabeli loend**.
3. Avage **Tööruumid \> Andmehaldus**, valige vahekaart **Andmetabelid** ja veenduge, et tabel oleks loendis toodud. Kui tabelit pole loendis, logige rakendusSe Finance and Operations sisse VM ja veenduge, et tabel oleks saadaval.
4. Avage **tabeli vastendamise** leht **rakenduse Finance and Operations lehelt Topeltkirjutus**.
5. Tabeli vastendustes veergude automaatseks täitmiseks valige **Värskenda tabeli loendit**.

Kui probleem endiselt ei lahene, toimige järgmiselt.

> [!IMPORTANT]
> Need toimingud juhendavad teid tabeli kustutamise ja seejärel uuesti lisamise protsessis. Probleemide vältimiseks järgige kindlasti juhiseid täpselt.

1. Avage rakenduses Finance and Operations suvand **Tööruumi andmehaldus \>** ja valige **paan Andmed**.
2. Leidke tabel, millel pole atribuuti. Klõpsake tööriistaribal nuppu **Muuda sihtmärgi vastendust**.
3. Klõpsake paanil **Kaardil ajastamine sihtkohaks** suvandit **Loo vastendus**.
4. Avage **tabeli vastendamise** leht **rakenduse Finance and Operations lehelt Topeltkirjutus**.
5. Kui atribuuti ei asustata kaardil automaatselt, lisage see käsitsi, klõpsates nuppu **Lisa atribuut** ja seejärel käsku **Salvesta**. 
6. Valige kaart ja klõpsake käsku **Käita**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]