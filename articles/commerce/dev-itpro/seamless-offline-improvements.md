---
title: Kinkekaardi ja krediiditeatise toimingute sujuv võrguühenduseta lülitamine
description: See teema annab ülevaate parandustest, mis pakuvad konkreetsetele maksetüüpidele sujuvat võrguühenduseta lülitust.
author: rubendel
manager: AnnBe
ms.date: 02/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 20120-02-28
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 1ea46ae90dedcc3ad3c3b305bddeb4d98827353a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230664"
---
# <a name="seamless-offline-switch-for-gift-card-and-credit-memo-operations"></a><span data-ttu-id="eba48-103">Kinkekaardi ja krediiditeatise toimingute sujuv võrguühenduseta lülitamine</span><span class="sxs-lookup"><span data-stu-id="eba48-103">Seamless offline switch for gift card and credit memo operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eba48-104">Kui kassa seade kaotab oma ühenduse kanali andmebaasiga, saab enamike pooleli olevate kassatoimingute ja tehingutega jätkata pärast seda, kui müüja saab hoiatusteate ühenduse kadumise kohta.</span><span class="sxs-lookup"><span data-stu-id="eba48-104">If a point of sale (POS) device loses its connection to the channel database, most POS operations and transactions that were in progress can proceed after the cashier receives a warning message about the loss of connectivity.</span></span> <span data-ttu-id="eba48-105">Samas mõnel juhul on tehingutel siiski elemente, mis sõltuvad reaalajas teenusest, ja neid elemente ei toetata, kui kassa on võrguühenduseta.</span><span class="sxs-lookup"><span data-stu-id="eba48-105">However, in some cases, transactions have elements that rely on the real-time service, and those elements aren't supported when the POS is offline.</span></span> <span data-ttu-id="eba48-106">See teema kirjeldab mõnesid funktsioone, mis aitavad vähendada kaotatud ühenduvuse mõju sellistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="eba48-106">This topic describes some functionality that helps reduce the impact of lost connectivity in these scenarios.</span></span>

## <a name="completing-gift-card-transactions-in-offline-mode"></a><span data-ttu-id="eba48-107">Ühenduseta režiimis kinkekaardi kannete lõpetamine</span><span class="sxs-lookup"><span data-stu-id="eba48-107">Completing gift card transactions in offline mode</span></span>

<span data-ttu-id="eba48-108">Sisemised kinkekaardid sõltuvad reaalajas teenusest, kuna kinkekaardi saldo peab olema Microsoft Dynamics 365 Commerce Headquarters\`i keskselt hallatud.</span><span class="sxs-lookup"><span data-stu-id="eba48-108">Internal gift cards depend on the real-time service, because the balance for the gift cards must be centrally maintained in Microsoft Dynamics 365 Commerce Headquarters.</span></span> <span data-ttu-id="eba48-109">Pettuse või muu sünkroonimise probleemide vältimiseks lukustatakse kinkekaardid kohe, kui need on kandesse lisatud.</span><span class="sxs-lookup"><span data-stu-id="eba48-109">To help prevent fraud or other synchronization issues, gift cards are locked as soon as they are added to a transaction.</span></span> <span data-ttu-id="eba48-110">Lukustamise funktsioon tagab, et kinkekaarti ei saaks kasutada samaaegselt mitmes terminalis.</span><span class="sxs-lookup"><span data-stu-id="eba48-110">The locking function ensures that a gift card can't be used on multiple terminals at the same time.</span></span> <span data-ttu-id="eba48-111">Kui kanne on lõpetatud, kinkekaart värskendatakse ja vabastatakse.</span><span class="sxs-lookup"><span data-stu-id="eba48-111">When a transaction is completed, the gift card is updated and unlocked.</span></span>

<span data-ttu-id="eba48-112">Samas kui kassa kaotab ühenduvuse pärast kinkekaardi kandesse lisamist, võib kinkekaardi kasutuskõlbmatuks muutuda.</span><span class="sxs-lookup"><span data-stu-id="eba48-112">However, if the POS loses connectivity after a gift card has been added to a transaction, the gift card can become unusable.</span></span> <span data-ttu-id="eba48-113">Selle olukorra vältimiseks on rakenduses Dynamics 365 Commerce parameeter, mis lubab kinkekaardi rida sisaldavad kanded viia lõpule, kui kassa on võrguühenduseta.</span><span class="sxs-lookup"><span data-stu-id="eba48-113">To help prevent this situation, Dynamics 365 Commerce has a parameter that enables transactions that include a gift card line to be completed while the POS is offline.</span></span> <span data-ttu-id="eba48-114">Kui see parameeter on sisse lülitatud, salvestatakse võrguühenduseta sunnitud kinkekaardi kanded koos võrguühenduseta kannetega ja need sünkroonitakse Commerce Headquartersiga võrguühenduseta kannete sünkroonimisel.</span><span class="sxs-lookup"><span data-stu-id="eba48-114">When this parameter is turned on, gift card transactions that are forced offline will be saved together with offline transactions, and they will be synced to Commerce Headquarters when the offline transactions are synced.</span></span> <span data-ttu-id="eba48-115">Sünkroonimine vabastab ka kinkekaardi, et seda saaks kasutada teises terminalis.</span><span class="sxs-lookup"><span data-stu-id="eba48-115">The synchronization will also unlock the gift card so that it can be used at another terminal.</span></span>

<span data-ttu-id="eba48-116">Et lubada funktsioonil lõpetada kinkekaardi kanded pärast võrguühenduseta režiimi lülitamist, avage vahekaart **Sisestamine** lehel **Commerce’i parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="eba48-116">To enable the functionality to conclude gift card transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="eba48-117">Sellel vahekaardil otsige üles kiirkart **Kinkekaart** ja seadke suvand **Luba ühenduseta režiimis kinkekaardi kannete lõpetamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="eba48-117">On that tab, locate the **Gift card** fasttab and set **Allow concluding gift card transactions in offline mode** to **Yes**.</span></span>

![Võrguühenduseta kinkekaardi seadistamine](../media/gift.png)

<span data-ttu-id="eba48-119">Commerce’i parameetrid on tavaliselt vahemällu talletatud.</span><span class="sxs-lookup"><span data-stu-id="eba48-119">Commerce parameters are typically cached.</span></span> <span data-ttu-id="eba48-120">Seega pärast seda, kui selle parameetri seadistus on värskendatud ja jaotusgraafik on käivitatud sünkroonima muudatuse kanaliga, võib muudatuse jõustumiseks kuluda kuni 24 tundi.</span><span class="sxs-lookup"><span data-stu-id="eba48-120">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="eba48-121">Muudatuse kohe jõustumiseks lähtestage teenus Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="eba48-121">To make the change effective immediately, reset Microsoft Internet Information Services (IIS).</span></span>

## <a name="completing-credit-memo-transactions-in-offline-mode"></a><span data-ttu-id="eba48-122">Võrguühenduseta režiimis krediiditeatise kannete lõpetamine</span><span class="sxs-lookup"><span data-stu-id="eba48-122">Completing credit memo transactions in offline mode</span></span>

<span data-ttu-id="eba48-123">Sarnaselt sisemistele kinkekaartidele on krediiditeatised Commerce Headquartersis keskselt hallatavad.</span><span class="sxs-lookup"><span data-stu-id="eba48-123">Like internal gift cards, credit memos are centrally maintained in Commerce Headquarters.</span></span> <span data-ttu-id="eba48-124">Commerce’il on parameeter, mis lubab krediiditeatise kannete lõpetamist siis, kui kassa on võrguühenduseta.</span><span class="sxs-lookup"><span data-stu-id="eba48-124">Commerce has a parameter that enables credit memo transactions to be completed while the POS is offline.</span></span> <span data-ttu-id="eba48-125">See parameeter toimib sarnaselt eelmises jaotises mainitud kinkekaardi parameetriga.</span><span class="sxs-lookup"><span data-stu-id="eba48-125">This parameter works like the gift card parameter that was mentioned in the previous section.</span></span> <span data-ttu-id="eba48-126">Kui parameeter on sisse lülitatud, sünkroonitakse võrguühenduseta sunnitud krediiditeatise kanded tagasi kanali andmebaasiga, koos teiste kannetega, mis teostati kassa võrguühenduseta olemise ajal.</span><span class="sxs-lookup"><span data-stu-id="eba48-126">When the parameter is turned on, credit memo transactions that are forced offline will be synced back to the channel database, together with other transactions that were performed while the POS was offline.</span></span>

<span data-ttu-id="eba48-127">Et lubada funktsioonil lõpetada krediiditeatise kanded pärast võrguühenduseta režiimi lülitamist, avage vahekaart **Sisestamine** lehel **Commerce’i parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="eba48-127">To enable the functionality to conclude credit memo transactions after switching to offline mode, go to the **Posting** tab on the **Commerce parameters** page.</span></span> <span data-ttu-id="eba48-128">Sellel vahekaardil otsige üles kiirkart **Krediiditeatis** ja seadke suvand **Luba ühenduseta režiimis krediiditeatise kannete lõpetamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="eba48-128">On that tab, locate the **Credit memo** fasttab and set **Allow concluding credit memo transactions in offline mode** to **Yes**.</span></span>

![Võrguühenduseta krediiditeatise seadistamine](../media/creditmemo.png)

<span data-ttu-id="eba48-130">Commerce’i parameetrid on tavaliselt vahemällu talletatud.</span><span class="sxs-lookup"><span data-stu-id="eba48-130">Commerce parameters are typically cached.</span></span> <span data-ttu-id="eba48-131">Seega pärast seda, kui selle parameetri seadistus on värskendatud ja jaotusgraafik on käivitatud sünkroonima muudatuse kanaliga, võib muudatuse jõustumiseks kuluda kuni 24 tundi.</span><span class="sxs-lookup"><span data-stu-id="eba48-131">Therefore, after the setting of this parameter is updated, and the distribution schedule is initiated to sync the change to the channel, the change can take up to 24 hours to take effect.</span></span> <span data-ttu-id="eba48-132">Muudatuse koheselt jõustamiseks lähtestage IIS.</span><span class="sxs-lookup"><span data-stu-id="eba48-132">To make the change effective immediately, reset IIS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eba48-133">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="eba48-133">Related topics</span></span>

- [<span data-ttu-id="eba48-134">Võrguühenduseta kassa funktsioonid</span><span class="sxs-lookup"><span data-stu-id="eba48-134">Offline point of sale (POS) functionality</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-offline-functionality)
- [<span data-ttu-id="eba48-135">Ühendusega ja ühenduseta kassatoimingud</span><span class="sxs-lookup"><span data-stu-id="eba48-135">Online and offline point of sale (POS) operations</span></span>](https://docs.microsoft.com/dynamics365/retail/pos-operations)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]