---
title: Kontrollige, et topeltkirjutus oleks konfigureeritud Finance and Operationsi rakendustes ja Common Data Service'is
description: Selles teemas selgitatakse, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakendustes ja Common Data Service'is.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2ddac76871a3ac574a1edcb5446be6c64e5e4682
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997226"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="caeac-103">Kontrollige, et topeltkirjutus oleks konfigureeritud Finance and Operationsi rakendustes ja Common Data Service'is</span><span class="sxs-lookup"><span data-stu-id="caeac-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="caeac-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Common Data Service’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="caeac-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="caeac-105">Eelkõige selgitab see, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakendustes ja Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="caeac-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="caeac-106">Kontrollimine, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="caeac-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="caeac-107">Selleks, et teha kindlaks, kas kirjete värskenduse salvestamisel kuvatavad tõrketeated on põhjustatud topeltkirjutusest, kontrollige esmalt, kas topeltkirjutus on konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="caeac-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="caeac-108">Kui teil on administraatori privileegid rakenduses Finance and Operations, avage jaotis **Tööruumid \> Andmehaldus** ja valige paan **Topeltkirjutus**.</span><span class="sxs-lookup"><span data-stu-id="caeac-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management** , and select the **Dual-write** tile.</span></span> <span data-ttu-id="caeac-109">Kui kuvatakse lingitud keskkondade üksikasjad ja kasutatava üksuse kaartide loend, konfigureeritakse topeltkirjutus.</span><span class="sxs-lookup"><span data-stu-id="caeac-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide korral](media/verify_fin_ops_1.png)

+ <span data-ttu-id="caeac-111">Kui teil ei ole administraatori privileege, kuvatakse tõrketeade *Andmeid ei saa kirjutada üksusele \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="caeac-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="caeac-112">Järgmises näites kirjeldatalse. et rakenduses Finance and Operations ei saa kliendi kirjet luua, sest topeltkirjutus on konfigureeritud, kuid kliendigruppi ja maksetingimuste viiteandmeid pole olemas Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="caeac-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide puudumise korral](media/verify_fin_ops_2.png)

<span data-ttu-id="caeac-114">Lisateavet selle kohta, kuidas lahendada probleeme rakenduses Finance and Operations andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="caeac-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="caeac-115">Kontrollimine, kas topeltkirjutus on konfigureeritud Common Data Service'is</span><span class="sxs-lookup"><span data-stu-id="caeac-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="caeac-116">Kui andmete loomisel kuvatakse Common Data Service'i lehtedel väli **Ettevõte** , on topeltkirjutus konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="caeac-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Common Data Service'i ühenduse kontrollimine](media/verify_cds.png)

<span data-ttu-id="caeac-118">Lisateavet selle kohta, kuidas lahendada probleeme Common Data Service'is andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="caeac-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="caeac-119">Lisateavet selle kohta, kuidas vaadata tõrke üksikasju, kui Common Data Service'is andmete loomisel ilmneb tõrkeid, vaadake teemast [Common Data Service'is lisandmooduli jälituslogi lubamine ja kuvamine tõrke üksikasjade vaatamiseks](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="caeac-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>
