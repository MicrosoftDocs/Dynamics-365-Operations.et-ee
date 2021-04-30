---
title: Azure'i salvestusruumi konto ja võtmehoidla loomine
description: Selles teemas selgitatakse, kuidas luua Azure'i salvestusruumi kontot ja võtmehoidlat.
author: gionoder
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2786d350fde2399aadb35dc653bc15123e0e6d91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893798"
---
# <a name="create-an-azure-storage-account-and-a-key-vault"></a><span data-ttu-id="591b1-103">Azure'i salvestusruumi konto ja võtmehoidla loomine</span><span class="sxs-lookup"><span data-stu-id="591b1-103">Create an Azure storage account and a key vault</span></span>

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="591b1-104">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="591b1-104">Prerequisites</span></span>

<span data-ttu-id="591b1-105">Enne selles teemas kirjeldatud sammude läbimist peate veenduma, et järgmised ülesanded oleksid lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="591b1-105">Before you can complete the steps in this topic, you must make sure that the following tasks have been completed:</span></span>

- <span data-ttu-id="591b1-106">Võtmehoidla ressursi loomine Azure'is.</span><span class="sxs-lookup"><span data-stu-id="591b1-106">Create a key vault resource in Azure.</span></span> <span data-ttu-id="591b1-107">Lisateavet leiate teemast [Teave Azure'i võtmehoidla kohta](/azure/key-vault/general/overview).</span><span class="sxs-lookup"><span data-stu-id="591b1-107">For more information, see [About Azure Key Vault](/azure/key-vault/general/overview).</span></span>
- <span data-ttu-id="591b1-108">Azure'i salvestusruumi konto loomine (bloobimälu).</span><span class="sxs-lookup"><span data-stu-id="591b1-108">Create an Azure storage account (Blob storage).</span></span> <span data-ttu-id="591b1-109">Lisateavet leiate jaotisest [Azure'i salvestusruumi konto haldamine](/azure/storage/blobs/).</span><span class="sxs-lookup"><span data-stu-id="591b1-109">For more information, see [Maintaining Azure Storage Account](/azure/storage/blobs/).</span></span>

## <a name="overview"></a><span data-ttu-id="591b1-110">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="591b1-110">Overview</span></span>

<span data-ttu-id="591b1-111">Selles teemas läbite kaks peamist sammu.</span><span class="sxs-lookup"><span data-stu-id="591b1-111">In this topic, you will complete two main steps:</span></span>

- <span data-ttu-id="591b1-112">Azure'i salvestusruumi konto seadistamine salvestusruumi konto URI hankimiseks.</span><span class="sxs-lookup"><span data-stu-id="591b1-112">Set up the Azure storage account to get the storage account URI.</span></span>
- <span data-ttu-id="591b1-113">Võtmehoidla seadistamine salvestusruumi konto URI talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="591b1-113">Set up the key vault to store the storage account URI.</span></span>

## <a name="set-up-the-azure-storage-account-to-get-the-storage-account-uri"></a><span data-ttu-id="591b1-114">Azure'i salvestusruumi konto seadistamine salvestusruumi konto URI hankimiseks</span><span class="sxs-lookup"><span data-stu-id="591b1-114">Set up the Azure storage account to get the storage account URI</span></span>

1. <span data-ttu-id="591b1-115">Avage salvestusruumi konto, mida kavatsete kasutada koos elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="591b1-115">Open the storage account that you plan to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="591b1-116">Avage **Bloobiteenus** \> **Konteinerid** ja looge uus konteiner.</span><span class="sxs-lookup"><span data-stu-id="591b1-116">Go to **Blob service** \> **Containers**, and create a new container.</span></span>
3. <span data-ttu-id="591b1-117">Sisestage konteineri nimi ja seadke välja **Avaliku juurdepääsu tase** väärtuseks **Privaatne(anonüümse juurdepääsuta)**.</span><span class="sxs-lookup"><span data-stu-id="591b1-117">Enter a name for the container, and set the **Public access level** field to **Private (no anonymous access)**.</span></span>
4. <span data-ttu-id="591b1-118">Avage konteiner ja seejärel **Sätted \> Juurdepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="591b1-118">Open the container, and go to **Settings \> Access policy**.</span></span>
5. <span data-ttu-id="591b1-119">Valige **Lisa poliitika**, et lisada talletamise juurdepääsupoliitika.</span><span class="sxs-lookup"><span data-stu-id="591b1-119">Select **Add policy** to add a stored access policy.</span></span>
6. <span data-ttu-id="591b1-120">Seadistage väljad **Identifikaator** ja **Load** oma vajaduste järgi.</span><span class="sxs-lookup"><span data-stu-id="591b1-120">Set the **Identifier** and **Permissions** fields as appropriate.</span></span> <span data-ttu-id="591b1-121">Väljal **Load** peaksite valima kõik load.</span><span class="sxs-lookup"><span data-stu-id="591b1-121">In the **Permissions** field, you should select all permissions.</span></span>

    ![Bloobimälu loa andmine](media/e-Invoicing-services-create-azure-resources-grant-blob-permissions.png)

7. <span data-ttu-id="591b1-123">Sisestage algus- ja aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="591b1-123">Enter the start and expiry dates.</span></span> <span data-ttu-id="591b1-124">Aegumiskuupäev peab olema tulevikus.</span><span class="sxs-lookup"><span data-stu-id="591b1-124">The expiry date should be in future.</span></span>
8. <span data-ttu-id="591b1-125">Valige **OK** poliitika salvestamiseks ja seejärel salvestage muudatused konteineris.</span><span class="sxs-lookup"><span data-stu-id="591b1-125">Select **OK** to save the policy, and then save your changes to the container.</span></span>
9. <span data-ttu-id="591b1-126">Naaske salvestusruumi kontole ja avage **Salvestusruumiuurija (eelversioon)**.</span><span class="sxs-lookup"><span data-stu-id="591b1-126">Return to the storage account, and open **Storage Explorer (preview)**.</span></span>
10. <span data-ttu-id="591b1-127">Paremklõpsake konteineril ja valige seejärel **Hangi jagatud juurdepääsu allkiri**.</span><span class="sxs-lookup"><span data-stu-id="591b1-127">Right-click the container, and then select **Get Shared Access Signature**.</span></span>
11. <span data-ttu-id="591b1-128">Kopeerige ja talletage dialoogiboksis **Jagatud juurdepääsu allkiri** välja **URI** väärtus.</span><span class="sxs-lookup"><span data-stu-id="591b1-128">In the **Shared Access Signature** dialog box, copy and store the value in the **URI** field.</span></span> <span data-ttu-id="591b1-129">Seda väärtust kasutatakse järgmises sammus ja sellele viidatakse kui *jagatud juurdepääsu allkirja URI-le*.</span><span class="sxs-lookup"><span data-stu-id="591b1-129">This value will be used in the next procedure and will be referred to as the *shared access signature URI*.</span></span>

    ![URI väärtuse valimine ja kopeerimine](media/e-Invoicing-services-create-azure-resources-select-and-copy-uri.png)

## <a name="set-up-the-key-vault-to-store-the-storage-account-uri"></a><span data-ttu-id="591b1-131">Võtmehoidla seadistamine salvestusruumi konto URI talletamiseks</span><span class="sxs-lookup"><span data-stu-id="591b1-131">Set up the key vault to store the storage account URI</span></span>

1. <span data-ttu-id="591b1-132">Avage võtmehoidla, mida kavatsete kasutada koos elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="591b1-132">Open the key vault that you intend to use with Electronic invoicing.</span></span>
2. <span data-ttu-id="591b1-133">Avage **Sätted** \> **Saladused** ja seejärel valige **Loo/impordi**, et luua uus saladus.</span><span class="sxs-lookup"><span data-stu-id="591b1-133">Go to **Settings** \> **Secrets**, and then select **Generate/Import** to create a new secret.</span></span>
3. <span data-ttu-id="591b1-134">Valige lehel **Saladuse loomine** väljal **Üleslaadimissuvandid** väärtus **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="591b1-134">On the **Create a secret** page, in the **Upload options** field, select **Manual**.</span></span>
4. <span data-ttu-id="591b1-135">Sisestage saladuse nimi.</span><span class="sxs-lookup"><span data-stu-id="591b1-135">Enter the name of the secret.</span></span> <span data-ttu-id="591b1-136">Seda nime kasutatakse teenuse seadistamiseks teenuses Regulatory Configuration Service (RCS) ja sellele viidatakse kui *võtmehoidla saladuse nimele*.</span><span class="sxs-lookup"><span data-stu-id="591b1-136">This name will be used during setup of the service in Regulatory Configuration Service (RCS) and will be referred to as the *key vault secret name*.</span></span>
5. <span data-ttu-id="591b1-137">Valige väljal **Väärtus** suvand **Jagatud juurdepääsu allkirja URI** ja seejärel valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="591b1-137">In the **Value** field, select **Shared Access Signature URI**, and then select **Create**.</span></span>
6. <span data-ttu-id="591b1-138">Seadistage juurdepääsupoliitika, et anda elektroonilise arvelduse lisandmoodulile õigel tasemel turvaline juurdepääs loodud saladusele.</span><span class="sxs-lookup"><span data-stu-id="591b1-138">Set up the access policy to grant Electronic invoicing the correct level of secure access to the secret you created.</span></span> <span data-ttu-id="591b1-139">Avage **Sätted \> Juurdepääsupoliitika** ja valige **Lisa juurdepääsupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="591b1-139">Go to **Settings \> Access policy**, and select **Add Access Policy**.</span></span>
7. <span data-ttu-id="591b1-140">Seadke saladuselubadeks toimingud **Hangi** ja **Loetle**.</span><span class="sxs-lookup"><span data-stu-id="591b1-140">Set the secret permissions for the **Get** and **List** operations.</span></span>

    ![Teenusele juurdepääsu andmine](media/e-Invoicing-services-create-azure-resources-grant-service-access.png)

8. <span data-ttu-id="591b1-142">Seadke serdilubadeks toimingud **Hangi** ja **Loetle**.</span><span class="sxs-lookup"><span data-stu-id="591b1-142">Set the certificate permissions for **Get** and **List** operations.</span></span>

    ![Serdiloa andmine](media/e-Invoicing-services-create-azure-resources-grant-certificate-permission.png)

9. <span data-ttu-id="591b1-144">Väljal **Valige subjekt**, valige **Pole valitud**.</span><span class="sxs-lookup"><span data-stu-id="591b1-144">In the **Select principal** field, select **None selected**.</span></span>
10. <span data-ttu-id="591b1-145">Valige subjekt dialoogiboksis **Subjekt** **elektroonilise arvelduse lisandmooduli** lisamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="591b1-145">In the **Principal** dialog box, select the principal by adding **e-Invoicing Service**.</span></span>
11. <span data-ttu-id="591b1-146">Valige **Lisa** ja seejärel valige **Salvesta võtmehoidla muudatused**.</span><span class="sxs-lookup"><span data-stu-id="591b1-146">Select **Add**, and then select **Save Key Vault changes**.</span></span>
12. <span data-ttu-id="591b1-147">Kopeerige lehel **Ülevaade** võtmehoidla väärtus **DNS-i nimi**.</span><span class="sxs-lookup"><span data-stu-id="591b1-147">On the **Overview** page, copy the **DNS name** value for the key vault.</span></span> <span data-ttu-id="591b1-148">Seda väärtust kasutatakse teenuse seadistamisel RCS-is ja sellele viidatakse kui *võtmehoidla URI-le*.</span><span class="sxs-lookup"><span data-stu-id="591b1-148">This value will be used during setup of the service in RCS and will be referred as the *key vault URI*.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]