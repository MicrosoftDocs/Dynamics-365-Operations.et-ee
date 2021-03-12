---
title: Teenusetellimusele aadressi lisamine
description: Teemas kirjeldatakse, kuidas lisada teenusetellimusele kliendi aadressi.
author: ShylaThompson
manager: tfehr
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6c8f00eb1a1fe2ef3aea22da20ce218d7568f64
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966051"
---
# <a name="add-an-address-to-a-service-order"></a><span data-ttu-id="4159b-103">Teenusetellimusele aadressi lisamine</span><span class="sxs-lookup"><span data-stu-id="4159b-103">Add an address to a service order</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="4159b-104">Teemas kirjeldatakse, kuidas lisada teenusetellimusele kliendi aadressi.</span><span class="sxs-lookup"><span data-stu-id="4159b-104">This topic describes how to add a customer address to a service order.</span></span> <span data-ttu-id="4159b-105">Teenustellimuse loomisel edastatakse aadressiteave projektilt, millele on lisatud teenustellimus.</span><span class="sxs-lookup"><span data-stu-id="4159b-105">When you create a service order, the address information is transferred from the project that the service order is attached to.</span></span> <span data-ttu-id="4159b-106">Siiski saate valida alternatiivse asukoha klientide, hankijate, laoalade, ladude, teenusetellimuste ja projektide aadresside hulgast, mis on juba rakendusse Microsoft Dynamics AX sisestatud.</span><span class="sxs-lookup"><span data-stu-id="4159b-106">However, you can select an alternative location from addresses that are already entered in Microsoft Dynamics AX for customers, vendors, sites, warehouses, service orders, and projects.</span></span>

<span data-ttu-id="4159b-107">Saate ka luua uue aadressi.</span><span class="sxs-lookup"><span data-stu-id="4159b-107">You can also create a new address.</span></span> <span data-ttu-id="4159b-108">Vaikimisi kantakse uus aadress projekti üle.</span><span class="sxs-lookup"><span data-stu-id="4159b-108">By default, the new address is transferred to the project.</span></span> <span data-ttu-id="4159b-109">Siiski saate määrata, et uus aadress on asjakohane vaid teenuse selle eksemplari jaoks.</span><span class="sxs-lookup"><span data-stu-id="4159b-109">However, you can specify that the new address is only relevant for this instance of the service.</span></span> <span data-ttu-id="4159b-110">Sel juhul ei kanta uut aadressi projekti üle.</span><span class="sxs-lookup"><span data-stu-id="4159b-110">If you do, the new address is not transferred to the project.</span></span>

## <a name="create-a-customer-address-for-a-service-order"></a><span data-ttu-id="4159b-111">Kliendi aadressi loomine teenusetellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="4159b-111">Create a customer address for a service order</span></span>

<span data-ttu-id="4159b-112">Teenusetellimusele aadressi lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4159b-112">To add an address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="4159b-113">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="4159b-113">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="4159b-114">Avage teenusetellimus, mille jaoks soovite aadressi luua.</span><span class="sxs-lookup"><span data-stu-id="4159b-114">Open the service order that you want to create an address for.</span></span>

3.  <span data-ttu-id="4159b-115">Klõpsake **tegumiribal** käsku **Redigeeri** ja seejärel valikut **Päisevaade**.</span><span class="sxs-lookup"><span data-stu-id="4159b-115">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="4159b-116">Klõpsake kiirkaardil **Aadress** käsku **Lisa aadress**.</span><span class="sxs-lookup"><span data-stu-id="4159b-116">On the **Address** FastTab, click **Add address**.</span></span>

5.  <span data-ttu-id="4159b-117">Sisestage vormil **Uus aadress** aadressi jaoks kordumatu nimi ja täitke ülejäänud väljad.</span><span class="sxs-lookup"><span data-stu-id="4159b-117">In the **New address** form, enter a unique name for the address and complete the remaining fields.</span></span> 
    

    > [!WARNING]
    > <P><span data-ttu-id="4159b-118">Kui sisestate olemasoleva aadressi nime, kirjutab ülejäänud väljadele sisestatud teave üle olemasoleva aadressi teabe.</span><span class="sxs-lookup"><span data-stu-id="4159b-118">If you enter the same name as an existing address, the information that you enter in the remaining fields will overwrite information for the existing address.</span></span></P>


6.  <span data-ttu-id="4159b-119">Klõpsake **OK**, et kopeerida uus aadress teenusetellimusse.</span><span class="sxs-lookup"><span data-stu-id="4159b-119">Click **OK** to copy the new address to your service order.</span></span>

## <a name="specify-an-alternative-address-on-a-service-order"></a><span data-ttu-id="4159b-120">Teenustellimusele muu aadressi määramine</span><span class="sxs-lookup"><span data-stu-id="4159b-120">Specify an alternative address on a service order</span></span>

<span data-ttu-id="4159b-121">Teenusetellimusele alternatiivse aadressi lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4159b-121">To add an alternative address to a service order, follow these steps:</span></span>

1.  <span data-ttu-id="4159b-122">Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="4159b-122">Click **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="4159b-123">Avage teenusetellimus, mille jaoks soovite alternatiivse aadressi sisestada.</span><span class="sxs-lookup"><span data-stu-id="4159b-123">Open the service order that you want to enter an alternative address for.</span></span>

3.  <span data-ttu-id="4159b-124">Klõpsake **tegumiribal** käsku **Redigeeri** ja seejärel valikut **Päisevaade**.</span><span class="sxs-lookup"><span data-stu-id="4159b-124">On the **Action Pane**, click **Edit**, and then click **Header view**.</span></span>

4.  <span data-ttu-id="4159b-125">Klõpsake kiirkaardil **Aadress** käsku **Muu aadress**.</span><span class="sxs-lookup"><span data-stu-id="4159b-125">On the **Address** FastTab, click **Other address**.</span></span>

5.  <span data-ttu-id="4159b-126">Valige vormi **Aadressi valik** väljal **Kirje tüüp** suvand **Hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="4159b-126">In the **Address selection** form, in the **Record type** field, select **Service orders**.</span></span>

6.  <span data-ttu-id="4159b-127">Valige aadress ja klõpsake **OK**, et kopeerida see teenusetellimusse.</span><span class="sxs-lookup"><span data-stu-id="4159b-127">Select an address, and then click **OK** to copy it to your service order.</span></span>


  


