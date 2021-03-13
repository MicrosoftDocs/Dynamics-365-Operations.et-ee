---
title: Azure'i salvestusruumi konto ja võtmehoidla loomine
description: Selles teemas selgitatakse, kuidas luua Azure'i salvestusruumi kontot ja võtmehoidlat.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: d076aa5230437d1ef90f6b46d49ee4dea526db24
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104225"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="b6af1-103">Azure'i salvestusruumi konto ja võtmehoidla loomine</span><span class="sxs-lookup"><span data-stu-id="b6af1-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="b6af1-104">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="b6af1-104">Prerequisites</span></span>

<span data-ttu-id="b6af1-105">Enne selles teemas kirjeldatud sammude läbimist peate veenduma, et järgmised ülesanded oleksid lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="b6af1-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="b6af1-106">Võtmehoidla ressursi loomine Azure'is.</span><span class="sxs-lookup"><span data-stu-id="b6af1-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="b6af1-107">Lisateavet leiate teemast [Teave Azure'i võtmehoidla kohta](https://docs.microsoft.com/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="b6af1-107">For more information, see [About Azure Key Vault](https://docs.microsoft.com/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="b6af1-108">Azure'i salvestusruumi konto loomine (bloobimälu).</span><span class="sxs-lookup"><span data-stu-id="b6af1-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="b6af1-109">Lisateavet leiate jaotisest [Azure'i salvestusruumi konto haldamine](https://docs.microsoft.com/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="b6af1-109">For more information, see [Maintaining Azure Storage Account](https://docs.microsoft.com/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="b6af1-110">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b6af1-110">Overview</span></span>

<span data-ttu-id="b6af1-111">Selles teemas läbite kaks peamist sammu.</span><span class="sxs-lookup"><span data-stu-id="b6af1-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="b6af1-112">Azure'i salvestusruumi konto seadistamine salvestusruumi konto URI hankimiseks.</span><span class="sxs-lookup"><span data-stu-id="b6af1-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="b6af1-113">Võtmehoidla seadistamine salvestusruumi konto URI talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="b6af1-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="b6af1-114">Azure'i salvestusruumi konto seadistamine salvestusruumi konto URI hankimiseks</span><span class="sxs-lookup"><span data-stu-id="b6af1-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="b6af1-115">Avage salvestusruumi konto, mida kavatsete kasutada koos elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="b6af1-115">Open the storage account that you plan to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="b6af1-116">Avage **Bloobiteenus** \> **Konteinerid** ja looge uus konteiner.</span><span class="sxs-lookup"><span data-stu-id="b6af1-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="b6af1-117">Sisestage konteineri nimi ja seadke välja **Avaliku juurdepääsu tase** väärtuseks **Privaatne(anonüümse juurdepääsuta)**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="b6af1-118">Avage konteiner ja seejärel **Sätted \> Juurdepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="b6af1-119">Valige **Lisa poliitika**, et lisada talletamise juurdepääsupoliitika.</span><span class="sxs-lookup"><span data-stu-id="b6af1-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="b6af1-120">Seadistage väljad **Identifikaator** ja **Load** oma vajaduste järgi.</span><span class="sxs-lookup"><span data-stu-id="b6af1-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="b6af1-121">Väljal **Load** peaksite valima kõik load.</span><span class="sxs-lookup"><span data-stu-id="b6af1-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Bloobimälu loa andmine](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="b6af1-123">Sisestage algus- ja aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="b6af1-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="b6af1-124">Aegumiskuupäev peab olema tulevikus.</span><span class="sxs-lookup"><span data-stu-id="b6af1-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="b6af1-125">Valige **OK** poliitika salvestamiseks ja seejärel salvestage muudatused konteineris.</span><span class="sxs-lookup"><span data-stu-id="b6af1-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="b6af1-126">Naaske salvestusruumi kontole ja avage **Salvestusruumiuurija (eelversioon)**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="b6af1-127">Paremklõpsake konteineril ja valige seejärel **Hangi jagatud juurdepääsu allkiri**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="b6af1-128">Kopeerige ja talletage dialoogiboksis **Jagatud juurdepääsu allkiri** välja **URI** väärtus.</span><span class="sxs-lookup"><span data-stu-id="b6af1-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="b6af1-129">Seda väärtust kasutatakse järgmises sammus ja sellele viidatakse kui *jagatud juurdepääsu allkirja URI-le*.</span><span class="sxs-lookup"><span data-stu-id="b6af1-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI väärtuse valimine ja kopeerimine](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="b6af1-131">Võtmehoidla seadistamine salvestusruumi konto URI talletamiseks</span><span class="sxs-lookup"><span data-stu-id="b6af1-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="b6af1-132">Avage võtmehoidla, mida kavatsete kasutada koos elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="b6af1-132">Open the key vault that you intend to use with the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="b6af1-133">Avage **Sätted** \> **Saladused** ja seejärel valige **Loo/impordi**, et luua uus saladus.</span><span class="sxs-lookup"><span data-stu-id="b6af1-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="b6af1-134">Valige lehel **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="b6af1-135">Sisestage saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="b6af1-135">Enter the name of the secret.</span></span> <span data-ttu-id="b6af1-136">Seda nime kasutatakse teenuse seadistamiseks teenuses Regulatory Configuration Service (RCS) ja sellele viidatakse kui *võtmehoidla saladuse nimele*.</span><span class="sxs-lookup"><span data-stu-id="b6af1-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="b6af1-137">Valige väljal **Väärtus** suvand **Jagatud juurdepääsu allkirja URI** ja seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="b6af1-138">Seadistage juurdepääsupoliitika, et anda elektroonilise arvelduse lisandmoodulile õigel tasemel turvaline juurdepääs loodud saladusele.</span><span class="sxs-lookup"><span data-stu-id="b6af1-138">Set up the access policy to grant the Electronic invoicing add-on the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="b6af1-139">Avage **Sätted \> Juurdepääsupoliitika** ja valige **Lisa juurdepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="b6af1-140">Seadke saladuselubadeks toimingud **Hangi** ja **Loetle**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Teenusele juurdepääsu andmine](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="b6af1-142">Seadke serdilubadeks toimingud **Hangi** ja **Loetle**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Serdiloa andmine](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="b6af1-144">Valige subjekt dialoogiboksis **Subjekt** **elektroonilise arvelduse lisandmooduli** lisamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="b6af1-144">In the **Principal** dialog box, select the principal by adding **Electronic invoicing add-on**.</span></span>
10. <span data-ttu-id="b6af1-145">Valige **Lisa** ja seejärel valige **Salvesta võtmehoidla muudatused**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-145">Select **Add**, and then select **Save Key Vault changes**.</span></span>
11. <span data-ttu-id="b6af1-146">Kopeerige lehel **Ülevaade** võtmehoidla väärtus **DNS-i nimi**.</span><span class="sxs-lookup"><span data-stu-id="b6af1-146">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="b6af1-147">Seda väärtust kasutatakse teenuse seadistamisel RCS-is ja sellele viidatakse kui *võtmehoidla URI-le*.</span><span class="sxs-lookup"><span data-stu-id="b6af1-147">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>
