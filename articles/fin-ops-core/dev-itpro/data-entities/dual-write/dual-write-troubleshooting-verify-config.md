---
title: Kontrollige topeltkirjutuse konfiguratsiooni Finance and Operationsi rakendustes ja Dataverse’is
description: Selles teemas selgitatakse, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakendustes ja Dataverse'is.
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
ms.openlocfilehash: af746d1d20ddd1552bce797288c6d62d69d7bd16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748845"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="7c423-103">Kontrollige topeltkirjutuse konfiguratsiooni Finance and Operationsi rakendustes ja Dataverse’is</span><span class="sxs-lookup"><span data-stu-id="7c423-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="7c423-104">See teema annab teavet rakendustekomplekti Finance and Operations ja Dataverse’i vahelise andmete topeltkirjutuse integratsiooni tõrkeotsingu kohta.</span><span class="sxs-lookup"><span data-stu-id="7c423-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="7c423-105">Eelkõige selgitab see, kuidas teha kindlaks, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakendustes ja Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="7c423-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="7c423-106">Kontrollimine, kas topeltkirjutus on konfigureeritud Finance and Operationsi rakenduses</span><span class="sxs-lookup"><span data-stu-id="7c423-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="7c423-107">Selleks, et teha kindlaks, kas ridade värskenduse salvestamisel kuvatavad tõrketeated on põhjustatud topeltkirjutusest, kontrollige esmalt, kas topeltkirjutus on konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="7c423-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="7c423-108">Kui teil on administraatori privileegid rakenduses Finance and Operations, avage jaotis **Tööruumid \> Andmehaldus** ja valige paan **Topeltkirjutus**.</span><span class="sxs-lookup"><span data-stu-id="7c423-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="7c423-109">Kui kuvatakse lingitud keskkondade üksikasjad ja kasutatava tabeli vastenduste loend, konfigureeritakse topeltkirjutus.</span><span class="sxs-lookup"><span data-stu-id="7c423-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide korral](media/verify_fin_ops_1.png)

+ <span data-ttu-id="7c423-111">Kui teil ei ole administraatori privileege, kuvatakse tõrketeade *Andmeid ei saa kirjutada üksusele \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="7c423-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="7c423-112">Järgmises näites kirjeldatakse, et rakenduses Finance and Operations ei saa kliendi rida luua, sest topeltkirjutus on konfigureeritud, kuid kliendigruppi ja maksetingimuste viiteandmeid pole teenuses Dataverse olemas.</span><span class="sxs-lookup"><span data-stu-id="7c423-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Rakenduse Finance and Operations ühenduse kontrollimine administraatori privileegide puudumise korral](media/verify_fin_ops_2.png)

<span data-ttu-id="7c423-114">Lisateavet selle kohta, kuidas lahendada probleeme rakenduses Finance and Operations andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="7c423-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="7c423-115">Kontrollimine, kas topeltkirjutus on konfigureeritud Dataverse'is</span><span class="sxs-lookup"><span data-stu-id="7c423-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="7c423-116">Kui andmete loomisel kuvatakse Dataverse’i lehtedel veerg **Ettevõte**, on topeltkirjutus konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="7c423-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Dataverse'i ühenduse kontrollimine](media/verify_cds.png)

<span data-ttu-id="7c423-118">Lisateavet selle kohta, kuidas lahendada probleeme Dataverse'is andmete loomisel, vaadake teemast [Reaalajas sünkroonimise probleemide tõrkeotsing](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="7c423-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="7c423-119">Lisateavet selle kohta, kuidas vaadata tõrke üksikasju, kui Dataverse'is andmete loomisel ilmneb tõrkeid, vaadake teemast [Dataverse'is lisandmooduli jälituslogi lubamine ja kuvamine tõrke üksikasjade vaatamiseks](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="7c423-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]