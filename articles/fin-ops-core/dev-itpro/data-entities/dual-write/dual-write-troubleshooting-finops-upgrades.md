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
ms.openlocfilehash: 53df00de82b101aa02160d865a9c3bbebcfcae15
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275460"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="b5422-103">Finance and Operationsi rakenduste täiendustega seotud probleemide tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="b5422-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="b5422-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="b5422-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="b5422-105">Eelkõige annab see teema teavet, mis aitab lahendada Finance and Operationsi rakenduste täiendustega seotud probleeme.</span><span class="sxs-lookup"><span data-stu-id="b5422-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5422-106">Mõne selles teemas käsitletava probleemi korral on nõutav kas süsteemiadministraatori roll või Microsoft Azure Active Directory (Azure AD) rentniku administraatori mandaat.</span><span class="sxs-lookup"><span data-stu-id="b5422-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="b5422-107">Kõigis probleeme kirjeldavates jaotistes täpsustatakse, kas konkreetne roll või mandaat on nõutav.</span><span class="sxs-lookup"><span data-stu-id="b5422-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="b5422-108">Andmebaasi sünkroonimise tõrked</span><span class="sxs-lookup"><span data-stu-id="b5422-108">Database synchronization errors</span></span>

<span data-ttu-id="b5422-109">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="b5422-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b5422-110">Teile võidakse kuvada tõrketeade, mis sarnaneb järgmisele näitele, kui püüate kasutada üksust **DualWriteProjectConfiguration** rakenduse Finance and Operations Platform Update 30 värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b5422-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="b5422-111">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b5422-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="b5422-112">Logige rakenduse Finance and Operations virtuaalarvutisse (VM) sisse.</span><span class="sxs-lookup"><span data-stu-id="b5422-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b5422-113">Avage Visual Studio administraatorina ja avage rakendusobjektide puu (AOT).</span><span class="sxs-lookup"><span data-stu-id="b5422-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="b5422-114">Sisestage otsigusse **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="b5422-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="b5422-115">AOT-s paremklõpsake valikut **DualWriteProjectConfiguration** ja valige **Lisa uuele projektile**.</span><span class="sxs-lookup"><span data-stu-id="b5422-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="b5422-116">Vajutage **OK**, et luua uus projekt, mis kasutab vaikesuvandeid.</span><span class="sxs-lookup"><span data-stu-id="b5422-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="b5422-117">Paremklõpsake Solution Exploreris valikut **Projekti atribuudid** ja seadke **Sünkrooni andmebaasi koostamisel** väärtuseks **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="b5422-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="b5422-118">Koostage projekt ja kinnitage, et see on edukas.</span><span class="sxs-lookup"><span data-stu-id="b5422-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="b5422-119">Valige menüüs **Dynamics 365** suvand **Sünkrooni andmebaas**.</span><span class="sxs-lookup"><span data-stu-id="b5422-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="b5422-120">Täieliku andmebaasi sünkroonimise tegemiseks valige **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="b5422-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="b5422-121">Kui täielik andmebaasi sünkroonimine õnnestub, käivitage uuesti andmebaasi sünkroonimise etapp Microsoft Dynamics Lifecycle Servicesis (LCS) ja kasutage vastavalt vajadusele käsitsi uuendamise skripte, nii et saate jätkata värskendust.</span><span class="sxs-lookup"><span data-stu-id="b5422-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="b5422-122">Puuduva üksuse välja probleem vastendusel</span><span class="sxs-lookup"><span data-stu-id="b5422-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="b5422-123">**Tõrke parandamiseks nõutav roll:** süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="b5422-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="b5422-124">Teile võidakse kuvada lehel **Topeltkirjutus** tõrketeade, mis sarnaneb järgmisele näitele.</span><span class="sxs-lookup"><span data-stu-id="b5422-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="b5422-125">*Puuduv allika väli \<välja nimi\> skeemis.*</span><span class="sxs-lookup"><span data-stu-id="b5422-125">*Missing source field \<field name\> in the schema.*</span></span>

![Puuduva allika välja tõrketeate näide](media/error_missing_field.png)

<span data-ttu-id="b5422-127">Probleemi lahendamiseks tehke esmalt need toimingud veendumaks, et väljad on olemis.</span><span class="sxs-lookup"><span data-stu-id="b5422-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="b5422-128">Logige rakenduse Finance and Operations VM-i sisse.</span><span class="sxs-lookup"><span data-stu-id="b5422-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="b5422-129">Avage **Tööruumid \> Andmehaldus**, valige paan **Raamistiku parameetrid** ja seejärel valige vahekaardil **Üksuse sätted** üksuste värskendamiseks **Värskenda üksuste loend**.</span><span class="sxs-lookup"><span data-stu-id="b5422-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="b5422-130">Avage **Tööruumid \> Andmehaldus**, valige vahekaart **Andmeüksused** ja veenduge, et üksus on loendis.</span><span class="sxs-lookup"><span data-stu-id="b5422-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="b5422-131">Kui olemit pole loendis, logige rakenduse Finance and Operations VM-i sisse ja veenduge, et üksus oleks saadaval.</span><span class="sxs-lookup"><span data-stu-id="b5422-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="b5422-132">Avage rakenduse Finance and Operations lehel **Topeltkirjutus** leht **Üksuse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="b5422-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="b5422-133">Üksuse vastendustes väljade automaatseks täitmiseks valige **Värskenda üksuste loendit**.</span><span class="sxs-lookup"><span data-stu-id="b5422-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="b5422-134">Kui probleem endiselt ei lahene, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b5422-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5422-135">Need toimingud juhendavad teid üksuse kustutamise ja seejärel uuesti lisamise protsessis.</span><span class="sxs-lookup"><span data-stu-id="b5422-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="b5422-136">Probleemide vältimiseks järgige kindlasti juhiseid täpselt.</span><span class="sxs-lookup"><span data-stu-id="b5422-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="b5422-137">Avage rakenduses Finance and Operations **Tööruumid \> Andmehaldus** ja valige paan **Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="b5422-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="b5422-138">Leidke üksus, millel pole atribuuti.</span><span class="sxs-lookup"><span data-stu-id="b5422-138">Find the entity that is missing the attribute.</span></span> <span data-ttu-id="b5422-139">Klõpsake tööriistaribal nuppu **Muuda sihtmärgi vastendust**.</span><span class="sxs-lookup"><span data-stu-id="b5422-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="b5422-140">Klõpsake paanil **Kaardil ajastamine sihtkohaks** suvandit **Loo vastendus**.</span><span class="sxs-lookup"><span data-stu-id="b5422-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="b5422-141">Avage rakenduse Finance and Operations lehel **Topeltkirjutus** leht **Üksuse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="b5422-141">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="b5422-142">Kui atribuuti ei asustata kaardil automaatselt, lisage see käsitsi, klõpsates nuppu **Lisa atribuut** ja seejärel käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b5422-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="b5422-143">Valige kaart ja klõpsake käsku **Käita**.</span><span class="sxs-lookup"><span data-stu-id="b5422-143">Select the map and click **Run**.</span></span>
