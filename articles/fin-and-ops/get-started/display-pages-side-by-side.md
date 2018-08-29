---
title: "Lehtede kuvamine kõrvuti, kasutades funktsiooni Ava uues aknas"
description: "Selles artiklis selgitatakse, kuidas Microsoft Dynamics 365 for Finance and Operationsis lehti kõrvuti kuvada."
author: aneesmsft
manager: AnnBe
ms.date: 09/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 8e3ef29618f11b0f247999e3a24e54bff44bf51a
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a><span data-ttu-id="a8289-103">Lehtede kuvamine kõrvuti, kasutades funktsiooni Ava uues aknas</span><span class="sxs-lookup"><span data-stu-id="a8289-103">Show pages side by side by using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8289-104">Selles artiklis selgitatakse, kuidas Microsoft Dynamics 365 for Finance and Operationsis lehti kõrvuti kuvada.</span><span class="sxs-lookup"><span data-stu-id="a8289-104">This article explains how to display pages side-by-side in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="a8289-105">Microsoft Dynamics 365 for Finance and Operations aitab tõhusalt ülesandeid täita.</span><span class="sxs-lookup"><span data-stu-id="a8289-105">Microsoft Dynamics 365 for Finance and Operations helps you perform tasks efficiently.</span></span> <span data-ttu-id="a8289-106">Mõnikord võib ülesannete kiireks lahendamiseks olla vaja mitut lehte kõrvuti vaadata.</span><span class="sxs-lookup"><span data-stu-id="a8289-106">In some cases, you may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="a8289-107">Näiteks võite soovida kontrollida või sisestada ridu mitmele töölehele.</span><span class="sxs-lookup"><span data-stu-id="a8289-107">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="a8289-108">Tavaliselt on selleks vaja liikuda edasi-tagasi töölehtede loendis kuvatud lehe ja antud töölehe ridu kuvava lehe vahel.</span><span class="sxs-lookup"><span data-stu-id="a8289-108">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="a8289-109">Kuid funktsioon **Ava uues aknas** võimaldab kuvada need lehed kõrvuti, et saaksite oma toiminguid kiiresti teha.</span><span class="sxs-lookup"><span data-stu-id="a8289-109">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span> 

<span data-ttu-id="a8289-110">Jätkates ülal nimetatud näitega, võite ridu vaadates klõpsata ikooni **Ava uues aknas**.</span><span class="sxs-lookup"><span data-stu-id="a8289-110">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span> 

<span data-ttu-id="a8289-111">[![ikoon-ava-uues-aknas](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="a8289-111">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span> 

<span data-ttu-id="a8289-112">Kui klõpsate ikooni **Ava uues aknas**, avaneb ridade leht uues hüpikbrauseris ja seejärel naaseb algne brauser lehele, millel oli kuvatud töölehtede loend.</span><span class="sxs-lookup"><span data-stu-id="a8289-112">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="a8289-113">Seejärel saate kuvada mõlemad lehed kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="a8289-113">You can then display both pages side-by-side.</span></span> <span data-ttu-id="a8289-114">Kui olete töölehe vaatamise lõpetanud, saate muuta valitud töölehte töölehtede loendilehel ja ridade lehel hüpikaknas kuvatakse automaatselt uue valitud töölehe read.</span><span class="sxs-lookup"><span data-stu-id="a8289-114">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span> 

<span data-ttu-id="a8289-115">[![lehtede-kuvamine-kõrvuti](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="a8289-115">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span> 

<span data-ttu-id="a8289-116">Dünaamiline sidumine ja värskendamine toimub neid lehti toetavate andmete vahelise seose abil.</span><span class="sxs-lookup"><span data-stu-id="a8289-116">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="a8289-117">Kui süsteem pole andmete vahelisest seosest teadlik, ei värskendata hüpikakent automaatselt, kui muuta akent, millest see pärines.</span><span class="sxs-lookup"><span data-stu-id="a8289-117">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span> 

<span data-ttu-id="a8289-118">Mõnel lehel on mitu vaadet: näiteks ruudustiku vaade, päise vaade ja üksikasjade vaade.</span><span class="sxs-lookup"><span data-stu-id="a8289-118">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="a8289-119">Ikoon **Ava uues aknas** põhjustab kogu lehe avamise uues brauseris.</span><span class="sxs-lookup"><span data-stu-id="a8289-119">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="a8289-120">Seetõttu ei saa funktsiooniga **Ava uues aknas** sama lehe kahte vaadet kõrvuti hoida.</span><span class="sxs-lookup"><span data-stu-id="a8289-120">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="a8289-121">Kuid peaaegu kõigil sellistel lehtedel on navigeerimisloend, mida võite kirjete vahetamiseks kasutada ja saada samasuguse kogemuse.</span><span class="sxs-lookup"><span data-stu-id="a8289-121">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span> 

<span data-ttu-id="a8289-122">Enne funktsiooni **Ava uues aknas** kasutamist tuleb konfigureerida brauseri hüpikakende blokeerija nii, et see lubaks hüpikaknaid Finance and Operationsi saidi URL-ilt.</span><span class="sxs-lookup"><span data-stu-id="a8289-122">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the Finance and Operations site.</span></span> <span data-ttu-id="a8289-123">Näiteks võib lubada hüpikaknad saidilt \*.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="a8289-123">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span> 

<span data-ttu-id="a8289-124">Funktsioon **Ava uues aknas** on saadaval ainult siis, kui aknas on avatud mitu lehte.</span><span class="sxs-lookup"><span data-stu-id="a8289-124">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="a8289-125">Samuti suletakse hüpikaken automaatselt, kui rohkem lehti pole avatud (st akna viimase lehe sulgemisel).</span><span class="sxs-lookup"><span data-stu-id="a8289-125">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="a8289-126">Finance and Operations suleb avatud lehed ka siis, kui lähete rakenduses teisele alale.</span><span class="sxs-lookup"><span data-stu-id="a8289-126">Finance and Operations also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="a8289-127">Seetõttu, kui teil on hüpikaknad avatud ja lähete rakenduses teisele alale, suletakse hüpikaknad automaatselt, kuna süsteem sulges nendes akendes olevad lehed.</span><span class="sxs-lookup"><span data-stu-id="a8289-127">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span> 

<span data-ttu-id="a8289-128">Hüpikakende ülaribal on kuvatud teave ettevõtte kohta, mille all leht avati, ja see on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="a8289-128">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="a8289-129">Hüpikaknad sõltuvad ka Finance and Operationsi peamisest brauseriaknast.</span><span class="sxs-lookup"><span data-stu-id="a8289-129">The pop-up windows also rely on the main Finance and Operations browser window.</span></span> <span data-ttu-id="a8289-130">Kui peamine aken suletakse või seda värskendatakse, muutuvad kõik hüpikaknad kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="a8289-130">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="a8289-131">See tähendab, et saate neis akendes siiski teavet vaadata, kuid ei saa sellega midagi teha.</span><span class="sxs-lookup"><span data-stu-id="a8289-131">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>




