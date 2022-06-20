---
title: Finants- ja äritoimingute rakenduste värskenduste probleemide tõrkeotsing
description: See artikkel pakub tõrkeotsingu teavet, mis aitab teil lahendada probleeme, mis on seotud finantside ja toimingute rakenduste täiendustega.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 954268b03be2be90f67dc9b7756f33215856864a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882138"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Finants- ja äritoimingute rakenduste värskenduste probleemide tõrkeotsing

[!include [banner](../../includes/banner.md)]





See artikkel pakub tõrkeotsingu teavet topeltkirjutuse integreerimiseks finantside ja toimingute rakenduste ning rakenduste vahel Dataverse. See annab teavet, mis võib aidata teil lahendada probleeme, mis on seotud finantside ja toimingute rakenduste täiendustega.

> [!IMPORTANT]
> Mõned küsimused, mida see artikkel käsitleb, võivad nõuda kas süsteemiadministraatori rolli või Microsofti Azure Active Directory (Azure AD) rentniku administraatori mandaate. Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.

## <a name="database-synchronization-errors"></a>Andmebaasi sünkroonimise tõrked

**Tõrke parandamiseks nõutav roll:** süsteemiadministraator

Võite saada tõrketeate, **mis sarnaneb järgmise näitega, kui proovite kasutada tabelit DualWriteProjectConfiguration** rakenduse Finantsid ja toimingud uuendamiseks platvormi värskenduseks 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Probleemi lahendamiseks tehke järgmist.

1. Finantside ja toimingute rakenduse virtuaalmasinasse (VM) sisselogimine.
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

1. Logige sisse finantside ja toimingute rakenduse VM-i.
2. Avage **Tööruumid \> Andmehaldus**, valige paan **Raamistiku parameetrid** ja seejärel valige vahekaardil **Tabeli sätted** tabelite värskendamiseks **Värskenda tabeli loend**.
3. Avage **Tööruumid \> Andmehaldus**, valige vahekaart **Andmetabelid** ja veenduge, et tabel oleks loendis toodud. Kui tabelit loendis pole, logige sisse VM-i rakenduse Finantsid ja toimingud puhul ja veenduge, et tabel on saadaval.
4. Avage tabeli **vastendamise** lehekülg topeltkirjutuse **lehelt** finantside ja toimingute rakenduses.
5. Tabeli vastendustes veergude automaatseks täitmiseks valige **Värskenda tabeli loendit**.

Kui probleem endiselt ei lahene, toimige järgmiselt.

> [!IMPORTANT]
> Need toimingud juhendavad teid tabeli kustutamise ja seejärel uuesti lisamise protsessis. Probleemide vältimiseks järgige kindlasti juhiseid täpselt.

1. Avage finantside ja toimingute rakenduses tööruumide andmehaldus **\> ja valige** andmetabelite **paan**.
2. Leidke tabel, millel pole atribuuti. Klõpsake tööriistaribal nuppu **Muuda sihtmärgi vastendust**.
3. Klõpsake paanil **Kaardil ajastamine sihtkohaks** suvandit **Loo vastendus**.
4. Avage tabeli **vastendamise** lehekülg topeltkirjutuse **lehelt** finantside ja toimingute rakenduses.
5. Kui atribuuti ei asustata kaardil automaatselt, lisage see käsitsi, klõpsates nuppu **Lisa atribuut** ja seejärel käsku **Salvesta**. 
6. Valige kaart ja klõpsake käsku **Käita**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]