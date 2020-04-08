---
title: Finance and Operationsi rakenduste täiendustega seotud probleemide tõrkeotsing
description: Selles teemas antakse tõrkeotsingu teavet, mis aitab lahendada Finance and Operationsi rakenduste täiendustega seotud probleeme.
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172873"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Finance and Operationsi rakenduste täiendustega seotud probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]



See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta. Eelkõige annab see teema teavet, mis aitab lahendada Finance and Operationsi rakenduste täiendustega seotud probleeme.

> [!IMPORTANT]
> Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="database-synchronization-errors"></a>Andmebaasi sünkroonimise tõrked

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Teile võidakse kuvada tõrketeade, mis sarnaneb järgmisele näitele, kui püüate kasutada üksust **DualWriteProjectConfiguration** rakenduse Finance and Operations Platform Update 30 värskendamiseks.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Probleemi lahendamiseks tehke järgmist.

1. Logige rakenduse Finance and Operations virtuaalarvutisse (VM) sisse.
2. Avage Visual Studio administraatorina ja avage rakendusobjektide puu (AOT).
3. Sisestage otsigusse **DualWriteProjectConfiguration**.
4. AOT-s paremklõpsake valikut **DualWriteProjectConfiguration** ja valige **Lisa uuele projektile**. Vajutage **OK**, et luua uus projekt, mis kasutab vaikesuvandeid.
5. Paremklõpsake Solution Exploreris valikut **Projekti atribuudid** ja seadke **Sünkrooni andmebaasi koostamisel** väärtuseks **Tõene**.
6. Koostage projekt ja kinnitage, et see on edukas.
7. Valige menüüs **Dynamics 365** suvand **Sünkrooni andmebaas**.
8. Täieliku andmebaasi sünkroonimise tegemiseks valige **Sünkrooni**.
9. Kui täielik andmebaasi sünkroonimine õnnestub, käivitage uuesti andmebaasi sünkroonimise etapp Microsoft Dynamics Lifecycle Servicesis (LCS) ja kasutage vastavalt vajadusele käsitsi uuendamise skripte, nii et saate jätkata värskendust.

## <a name="missing-entity-fields-issue-on-maps"></a>Puuduva üksuse välja probleem vastendusel

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Teile võidakse kuvada lehel **Topeltkirjutus** tõrketeade, mis sarnaneb järgmisele näitele.

*Puuduv allika väli \<välja nimi\> skeemis.*

![Puuduva allika välja tõrketeate näide](media/error_missing_field.png)

Probleemi lahendamiseks tehke esmalt need toimingud veendumaks, et väljad on olemis.

1. Logige rakenduse Finance and Operations VM-i sisse.
2. Avage **Tööruumid \> Andmehaldus**, valige paan **Raamistiku parameetrid** ja seejärel valige vahekaardil **Üksuse sätted** üksuste värskendamiseks **Värskenda üksuste loend**.
3. Avage **Tööruumid \> Andmehaldus**, valige vahekaart **Andmeüksused** ja veenduge, et üksus on loendis. Kui olemit pole loendis, logige rakenduse Finance and Operations VM-i sisse ja veenduge, et üksus oleks saadaval.
4. Avage rakenduse Finance and Operations lehel **Topeltkirjutus** leht **Üksuse vastendamine**.
5. Üksuse vastendustes väljade automaatseks täitmiseks valige **Värskenda üksuste loendit**.

Kui probleem endiselt ei lahene, toimige järgmiselt.

> [!IMPORTANT]
> Need toimingud juhendavad teid üksuse kustutamise ja seejärel uuesti lisamise protsessis. Probleemide vältimiseks järgige kindlasti juhiseid täpselt.

1. Avage rakenduses Finance and Operations **Tööruumid \> Andmehaldus** ja valige paan **Andmeüksused**.
2. Leidke väljalt puuduv üksus. Märkige sihtüksus, vahetabeli nimi, olemi nimi ja muud veeru väärtused.
3. Kui mõni teie töötlemisgruppidest sõltub sellest üksusest, tehke enne üksuse kustutamist vajalikud toimingud töötlemisgruppide jaoks.
4. Kustutage väljalt puuduv üksus.
5. Valige **Uus**ja lisage olem uuesti. Määrake väärtused, mille märkisite etapis 2.
6. Avage rakenduse Finance and Operations lehel **Topeltkirjutus** leht **Üksuse vastendamine**.
7. Üksuse vastendustes väljade automaatseks täitmiseks valige **Värskenda üksuste loendit**.
