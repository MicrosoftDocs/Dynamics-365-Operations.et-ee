---
title: "Hankija nõude konfiguratsioonid"
description: "See teema kirjeldab välju, mis tuleb uue hankija taotluse puhul täita."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendProspectiveVendorRegistrationConfig
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: e9b22a6f846607e8afc5d4f01c685f1364b1c01d
ms.contentlocale: et-ee
ms.lasthandoff: 02/08/2018

---

# <a name="vendor-request-configurations"></a><span data-ttu-id="d61f3-103">Hankija nõude konfiguratsioonid</span><span class="sxs-lookup"><span data-stu-id="d61f3-103">Vendor request configurations</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="d61f3-104">Hankija taotluse lõpetamiseks peab hankija kontaktisik läbima potentsiaalse hankija registreerimisviisardi.</span><span class="sxs-lookup"><span data-stu-id="d61f3-104">To complete a vendor request, a vendor contact person must complete the prospective vendor registration wizard.</span></span>

<span data-ttu-id="d61f3-105">Vormil **Hankija taotluse konfiguratsioonid** saate luua profiile, milles on määratud nõutud ja nähtavad väljad potentsiaalse hankija registreerimisviisardil.</span><span class="sxs-lookup"><span data-stu-id="d61f3-105">In the **Vendor request configurations** form, you can create profiles that specify required fields and visible fields in the prospective vendor registration wizard.</span></span>

<span data-ttu-id="d61f3-106">Hankija registreerimisviisardi alguses küsitakse potentsiaalse hankija kasutajalt, millises riigis/regioonis hankija tegutseb.</span><span class="sxs-lookup"><span data-stu-id="d61f3-106">The vendor registration wizard will start out by asking the prospective vendor user which country/region the vendor is doing business in.</span></span> <span data-ttu-id="d61f3-107">See teave määrab rakendatava konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="d61f3-107">This information determines the applicable configuration.</span></span> <span data-ttu-id="d61f3-108">Kui riigi/regiooni konfiguratsiooni pole määratud, kasutatakse vaikekonfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="d61f3-108">If no specific configuration is defined for a country/region, a default configuration will be used.</span></span>

### <a name="set-up-a-vendor-request-configuration"></a><span data-ttu-id="d61f3-109">Hankija taotluse konfiguratsiooni seadistamine</span><span class="sxs-lookup"><span data-stu-id="d61f3-109">Set up a vendor request configuration</span></span>

<span data-ttu-id="d61f3-110">Vaikimisi on hankija konfiguratsioon saadaval vormil Hankija taotluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="d61f3-110">By default, there is a vendor configuration available in the Vendor request configurations form.</span></span>

<span data-ttu-id="d61f3-111">Vaikekonfiguratsiooni puhul ei saa riiki/regiooni valida, seega ei saa jaotises **Riigid/regioonid** muudatusi teha.</span><span class="sxs-lookup"><span data-stu-id="d61f3-111">It is not possible to select country/regions for the default configuration, so the **Countries/regions** section cannot be changed.</span></span>

1.  <span data-ttu-id="d61f3-112">Klõpsake valikuid **Hanked** > **Seadistamine** > **Hankijad** ja seejärel klõpsake valikut **Hankija taotluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d61f3-112">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="d61f3-113">Loetletud üksustele oleku määramiseks klõpsake vahekaari **Väljad**.</span><span class="sxs-lookup"><span data-stu-id="d61f3-113">Click the **Fields** tab to set the status of the listed fields.</span></span>
-   <span data-ttu-id="d61f3-114">Peidetud (pole nähtav)</span><span class="sxs-lookup"><span data-stu-id="d61f3-114">Hidden (Not visible)</span></span>
-   <span data-ttu-id="d61f3-115">Kuvatud (nähtav, kuid pole kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d61f3-115">Displayed (Visible but not mandatory)</span></span>
-   <span data-ttu-id="d61f3-116">Nõutav (nähtav ja kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d61f3-116">Required (Visible and mandatory)</span></span>
3.  <span data-ttu-id="d61f3-117">Määramaks, kas teksti kuvatakse viisardis ja kas potentsiaalse hankija kasutaja peab enne viisardis järgmise sammu juurde liikumist selle kinnitama, klõpsake vahekaarti **Sisu**.</span><span class="sxs-lookup"><span data-stu-id="d61f3-117">Click the **Content** tab to specify if text is going to be shown on the wizard and if there should be an acknowledgement that the prospective vendor user must accept this before moving to the next step in the wizard.</span></span> <span data-ttu-id="d61f3-118">Kinnitamist küsitakse kõigi nõuete ja tingimuste puhul, millega kasutaja peab enne jätkamist nõustuma.</span><span class="sxs-lookup"><span data-stu-id="d61f3-118">The acknowledgement will be requested for any terms and conditions that the user must accept to continue.</span></span>

<span data-ttu-id="d61f3-119">Võite sisestada ka kinnitusteate, mis kuvatakse, kui viisard on läbitud, samuti saate lisada ühe või mitu küsimustikku.</span><span class="sxs-lookup"><span data-stu-id="d61f3-119">You can also enter a confirmation message that will be displayed when the wizard is finalized, and you can add one or more questionnaires.</span></span>

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a><span data-ttu-id="d61f3-120">Hankija konfiguratsiooni loomine konkreetse riigi/regiooni jaoks</span><span class="sxs-lookup"><span data-stu-id="d61f3-120">Create a vendor configuration for a specific country/region</span></span>
1.  <span data-ttu-id="d61f3-121">Klõpsake valikuid **Hanked** > **Seadistamine** > **Hankijad** ja seejärel klõpsake valikut **Hankija taotluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d61f3-121">Click **Procurement and sourcing** > **Setup** > **Vendors**, and then click **Vendor request configurations**.</span></span>
2.  <span data-ttu-id="d61f3-122">Uue konfiguratsiooni loomiseks klõpsake valikut **Uus** ja sisestage konfiguratsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="d61f3-122">Click **New** to create a new configuration, and provide a name for the configuration.</span></span>
3.  <span data-ttu-id="d61f3-123">Klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d61f3-123">Click **Save**.</span></span>
4.  <span data-ttu-id="d61f3-124">Riigi/regiooni puhul kasutatava konfiguratsiooni valimiseks avage vahekaart **Riik/regioon**.</span><span class="sxs-lookup"><span data-stu-id="d61f3-124">Open the **Country/regions** tab to select the country/region that the configuration should be used for.</span></span>
5.  <span data-ttu-id="d61f3-125">Konfiguratsiooni lõpetamiseks järgige vaikekonfiguratsiooni juhiseid.</span><span class="sxs-lookup"><span data-stu-id="d61f3-125">Complete the configuration by following the guidelines for the default configuration.</span></span>


