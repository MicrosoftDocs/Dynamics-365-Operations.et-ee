---
title: Andmevaka lähtestamise KKK
description: Selles teemas antakse vastused mõnele korduma kippuvatele küsimustele andmevaka lähtestamise kohta.
author: jinniew
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-05-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7cd96c7bc698986ef1ef07ca88479a3d49f22924
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266605"
---
# <a name="data-mart-resets-faq"></a><span data-ttu-id="4fc42-103">Andmevaka lähtestamise KKK</span><span class="sxs-lookup"><span data-stu-id="4fc42-103">Data mart resets FAQ</span></span>

<span data-ttu-id="4fc42-104">Selles teemas antakse vastused mõnele korduma kippuvatele küsimustele andmevaka lähtestamise kohta.</span><span class="sxs-lookup"><span data-stu-id="4fc42-104">This topic provides answers to some frequently asked questions about data mart resets.</span></span> <span data-ttu-id="4fc42-105">Andmevaka lähtestamine võib olla aeganõudev protsess ja olenevalt olukorrast ei pruugi see olla vajalik lahendus.</span><span class="sxs-lookup"><span data-stu-id="4fc42-105">A reset of the data mart can be a time-consuming process and, depending on the circumstances, might not be the solution that is required.</span></span> <span data-ttu-id="4fc42-106">Seetõttu sisaldab see teema teavet olukorrast, kus andmevaka lähtestamine võib aidata ning ka olukordi, kus ei saa.</span><span class="sxs-lookup"><span data-stu-id="4fc42-106">Therefore, this topic includes information about circumstances where a data mart reset might help and also circumstances where it's unlikely to help.</span></span>

## <a name="what-is-a-data-mart-reset"></a><span data-ttu-id="4fc42-107">Millal lähtestada andmevakka?</span><span class="sxs-lookup"><span data-stu-id="4fc42-107">What is a data mart reset?</span></span>

<span data-ttu-id="4fc42-108">Andmevaka lähtestamine keelab integratsioonitoimingud, kustutab kõik andmevaka andmed ja lubab seejärel integreeruda uuesti.</span><span class="sxs-lookup"><span data-stu-id="4fc42-108">A data mart reset will disable the integration tasks, delete all the data mart data, and then re-enable integration.</span></span>

<span data-ttu-id="4fc42-109">Kindlustamaks, et vanu andmeid ei lisata, saab andmevakka lähtestada alles pärast olemasolevate ülesannete lõpuleviimist.</span><span class="sxs-lookup"><span data-stu-id="4fc42-109">To ensure that old data isn't inserted, a data mart reset can be started only after existing tasks are completed.</span></span> <span data-ttu-id="4fc42-110">Kui proovite lähtestada andmevakka enne kõigi ülesannete lõpetamist, võite saada sõnumi, näiteks: "Andmevaka lähtestamist ei saanud aktiivse ülesande tõttu töödelda.</span><span class="sxs-lookup"><span data-stu-id="4fc42-110">If you try to reset the data mart before all tasks are completed, you might receive a message such as, "The data mart reset was unable to be processed because of an active task.</span></span> <span data-ttu-id="4fc42-111">Proovige hiljem uuesti.”</span><span class="sxs-lookup"><span data-stu-id="4fc42-111">Please try again later."</span></span>

## <a name="when-do-i-have-to-do-a-data-mart-reset"></a><span data-ttu-id="4fc42-112">Millal tuleb andmevakk lähtestada?</span><span class="sxs-lookup"><span data-stu-id="4fc42-112">When do I have to do a data mart reset?</span></span>

<span data-ttu-id="4fc42-113">Kui teie olukorras kehtib üks või mitu järgnevat lauset, võib teie organisatsioonile olla kasulik andmevaka lähtestamine.</span><span class="sxs-lookup"><span data-stu-id="4fc42-113">If one or more of the following statements apply to your situation, your organization can benefit from a data mart reset:</span></span>

- <span data-ttu-id="4fc42-114">Rakenduse andmebaas taastati.</span><span class="sxs-lookup"><span data-stu-id="4fc42-114">The application database was restored.</span></span>
- <span data-ttu-id="4fc42-115">Olete avanud tugipileti ja tugiinsener juhendas teid lähtestama andmevaka tõrkeotsingu sammu osana.</span><span class="sxs-lookup"><span data-stu-id="4fc42-115">You opened a support ticket, and a Support engineer instructed you to reset the data mart as part of a troubleshooting step.</span></span>
 
## <a name="when-is-a-data-mart-reset-inappropriate"></a><span data-ttu-id="4fc42-116">Millal on sobilik andmevakka lähtestada?</span><span class="sxs-lookup"><span data-stu-id="4fc42-116">When is a data mart reset inappropriate?</span></span>

<span data-ttu-id="4fc42-117">Siin on mõned olukorrad, kus me ei soovita andmevakka lähtestada.</span><span class="sxs-lookup"><span data-stu-id="4fc42-117">Here are some of the circumstances where we don't recommend that you reset the data mart:</span></span>

- <span data-ttu-id="4fc42-118">Teil esineb andmete sünkroonimisega seotud jõudlusprobleeme.</span><span class="sxs-lookup"><span data-stu-id="4fc42-118">You're experiencing performance issues that are associated with data synchronization.</span></span>
- <span data-ttu-id="4fc42-119">Teil on mõne järgmise põhjuse tõttu korduv lähtestamise muster.</span><span class="sxs-lookup"><span data-stu-id="4fc42-119">You have a recurring reset pattern for any of the following reasons:</span></span>

    - <span data-ttu-id="4fc42-120">**Puuduvad andmed** – kui märkate, et andmed puuduvad, avage koos Microsoftiga tugipilet, et vaadata üle teie aruande vorming ja võimalikud andmete sünkroonimise probleemid.</span><span class="sxs-lookup"><span data-stu-id="4fc42-120">**Missing data** – If you notice that data is missing, open a support ticket with Microsoft to review your report format and possible data synchronization issues.</span></span>
    - <span data-ttu-id="4fc42-121">**Kinnise integratsiooni olek**</span><span class="sxs-lookup"><span data-stu-id="4fc42-121">**Stuck integration state**</span></span>
    - <span data-ttu-id="4fc42-122">**Aegunud kirjed** – aegunud kirjed ei pruugi andmevaka lähtestamist alati õigustada.</span><span class="sxs-lookup"><span data-stu-id="4fc42-122">**Stale records** – Stale records by themselves don't necessarily justify a data mart reset.</span></span> <span data-ttu-id="4fc42-123">Kui teil on suur andmekomplekt, võtab lähtestamisprotsess aega, kuid tõenäoliselt ei vii see täiustamiseni.</span><span class="sxs-lookup"><span data-stu-id="4fc42-123">If you have a large data set, the reset process will take some time to run but is unlikely to lead to any improvement.</span></span>

## <a name="if-i-reset-the-data-mart-will-i-lose-reports-that-ive-already-designed"></a><span data-ttu-id="4fc42-124">Kui lähtestan andmed marti, kas kaotan aruanded, mis ma juba kujundanud olen?</span><span class="sxs-lookup"><span data-stu-id="4fc42-124">If I reset the data mart, will I lose reports that I've already designed?</span></span>

<span data-ttu-id="4fc42-125">Ei.</span><span class="sxs-lookup"><span data-stu-id="4fc42-125">No.</span></span> <span data-ttu-id="4fc42-126">Teie aruandeid talletatakse SQL-tabelites, mida ei mõjuta andmevaka lähtestamine.</span><span class="sxs-lookup"><span data-stu-id="4fc42-126">Your reports are stored in SQL tables that aren't affected by a data mart reset.</span></span> <span data-ttu-id="4fc42-127">Kui olete mures mõne loodud aruande kaotamise pärast, saate varundada kujundused, mida te ei soovi kaotada.</span><span class="sxs-lookup"><span data-stu-id="4fc42-127">If you're concerned about losing reports that you've designed, you can back up the designs that you don't want to lose.</span></span> <span data-ttu-id="4fc42-128">Kujunduste varundamiseks avage aruandekujundaja ja minge **Ettevõtte \> Ettevõtted \> Koosteüksused \> Eksport**.</span><span class="sxs-lookup"><span data-stu-id="4fc42-128">To back up designs, open Report Designer, and go to **Company \> Companies \> Building Blocks \> Export**.</span></span>
 
## <a name="do-all-users-have-to-exit-the-system-before-i-can-reset-the-data-mart"></a><span data-ttu-id="4fc42-129">Kas kõik kasutajad peavad süsteemist väljuma, enne kui ma andmevakka lähtestan?</span><span class="sxs-lookup"><span data-stu-id="4fc42-129">Do all users have to exit the system before I can reset the data mart?</span></span>

<span data-ttu-id="4fc42-130">Ei.</span><span class="sxs-lookup"><span data-stu-id="4fc42-130">No.</span></span> <span data-ttu-id="4fc42-131">Kasutajad saavad andmevaka lähtestamise ajal süsteemiga tööd jätkata.</span><span class="sxs-lookup"><span data-stu-id="4fc42-131">Users can continue to work in the system during a data mart reset.</span></span> <span data-ttu-id="4fc42-132">Kuid enne lähtestamise lõppu ei pääse kasutajad juurde aruannetele, mis on loodud Financial Reporter abil.</span><span class="sxs-lookup"><span data-stu-id="4fc42-132">However, until the reset is completed, users won't be able to access any reports that were created by using Financial Reporter.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
