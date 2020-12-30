---
title: Lehtede kõrvuti kuvamine, kasutades uue akna funktsioonis nuppu „Ava“
description: Selles artiklis selgitatakse, kuidas kuvada lehti kõrvuti.
author: aneesmsft
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b770fe44e4e12c515ca53def697fa345ce3eba3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694441"
---
# <a name="show-pages-side-by-side-using-the-open-in-new-window-feature"></a><span data-ttu-id="c77e7-103">Lehtede kõrvuti kuvamine, kasutades uue akna funktsioonis nuppu „Ava“</span><span class="sxs-lookup"><span data-stu-id="c77e7-103">Show pages side-by-side using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c77e7-104">Selles artiklis selgitatakse, kuidas kuvada lehti kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="c77e7-104">This article explains how to display pages side-by-side.</span></span>

<span data-ttu-id="c77e7-105">Mõnikord võib ülesannete kiireks lahendamiseks olla vaja mitut lehte kõrvuti vaadata.</span><span class="sxs-lookup"><span data-stu-id="c77e7-105">You may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="c77e7-106">Näiteks võite soovida kontrollida või sisestada ridu mitmele töölehele.</span><span class="sxs-lookup"><span data-stu-id="c77e7-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="c77e7-107">Tavaliselt on rohkem kui ühel töölehel ridade kinnitamiseks või sisestamiseks vaja liikuda edasi-tagasi töölehtede loendis kuvatud lehe ja antud töölehe ridu kuvava lehe vahel.</span><span class="sxs-lookup"><span data-stu-id="c77e7-107">Typically, to validate or enter lines in more than one journal, you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="c77e7-108">Kuid funktsioon **Ava uues aknas** võimaldab kuvada need lehed kõrvuti, et saaksite oma toiminguid kiiresti teha.</span><span class="sxs-lookup"><span data-stu-id="c77e7-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="c77e7-109">Jätkates ülal nimetatud näitega, võite ridu vaadates klõpsata ikooni **Ava uues aknas**.</span><span class="sxs-lookup"><span data-stu-id="c77e7-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="c77e7-110">[![Klõpsake ikooni Ava uues aknas.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="c77e7-110">[![Click the Open in new window icon.](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="c77e7-111">Kui klõpsate ikooni **Ava uues aknas**, avaneb ridade leht uues hüpikbrauseris ja seejärel naaseb algne brauser lehele, millel oli kuvatud töölehtede loend.</span><span class="sxs-lookup"><span data-stu-id="c77e7-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="c77e7-112">Seejärel saate kuvada mõlemad lehed kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="c77e7-112">You can then display both pages side-by-side.</span></span> <span data-ttu-id="c77e7-113">Kui olete töölehe vaatamise lõpetanud, saate muuta valitud töölehte töölehtede loendilehel ja ridade lehel hüpikaknas kuvatakse automaatselt uue valitud töölehe read.</span><span class="sxs-lookup"><span data-stu-id="c77e7-113">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="c77e7-114">[![Saate kuvada lehed kõrvuti.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="c77e7-114">[![You can display pages side-by-side.](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="c77e7-115">Dünaamiline sidumine ja värskendamine toimub neid lehti toetavate andmete vahelise seose abil.</span><span class="sxs-lookup"><span data-stu-id="c77e7-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="c77e7-116">Kui süsteem pole andmete vahelisest seosest teadlik, ei värskendata hüpikakent automaatselt, kui muuta akent, millest see pärines.</span><span class="sxs-lookup"><span data-stu-id="c77e7-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="c77e7-117">Mõnel lehel on mitu vaadet: näiteks ruudustiku vaade, päise vaade ja üksikasjade vaade.</span><span class="sxs-lookup"><span data-stu-id="c77e7-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="c77e7-118">Ikoon **Ava uues aknas** põhjustab kogu lehe avamise uues brauseris.</span><span class="sxs-lookup"><span data-stu-id="c77e7-118">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="c77e7-119">Seetõttu ei saa funktsiooniga **Ava uues aknas** sama lehe kahte vaadet kõrvuti hoida.</span><span class="sxs-lookup"><span data-stu-id="c77e7-119">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="c77e7-120">Kuid peaaegu kõigil sellistel lehtedel on navigeerimisloend, mida võite kirjete vahetamiseks kasutada ja saada samasuguse kogemuse.</span><span class="sxs-lookup"><span data-stu-id="c77e7-120">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="c77e7-121">Enne funktsiooni **Ava uues aknas** kasutamist tuleb konfigureerida brauseri hüpikakende blokeerija nii, et see lubaks hüpikaknaid saidi URL-ilt.</span><span class="sxs-lookup"><span data-stu-id="c77e7-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="c77e7-122">Näiteks võib lubada hüpikaknad saidilt \*.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="c77e7-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="c77e7-123">Funktsioon **Ava uues aknas** on saadaval ainult siis, kui aknas on avatud mitu lehte.</span><span class="sxs-lookup"><span data-stu-id="c77e7-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="c77e7-124">Samuti suletakse hüpikaken automaatselt, kui rohkem lehti pole avatud (st akna viimase lehe sulgemisel).</span><span class="sxs-lookup"><span data-stu-id="c77e7-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="c77e7-125">Süsteem suleb avatud lehed ka siis, kui lähete rakenduses teisele alale.</span><span class="sxs-lookup"><span data-stu-id="c77e7-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="c77e7-126">Seetõttu, kui teil on hüpikaknad avatud ja lähete rakenduses teisele alale, suletakse hüpikaknad automaatselt, kuna süsteem sulges nendes akendes olevad lehed.</span><span class="sxs-lookup"><span data-stu-id="c77e7-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span>

<span data-ttu-id="c77e7-127">Hüpikakende ülaribal on kuvatud teave ettevõtte kohta, mille all leht avati, ja see on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="c77e7-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="c77e7-128">Hüpikaknad sõltuvad ka peamisest brauseriaknast.</span><span class="sxs-lookup"><span data-stu-id="c77e7-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="c77e7-129">Kui peamine aken suletakse või seda värskendatakse, muutuvad kõik hüpikaknad kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="c77e7-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="c77e7-130">Selle olukorra ilmnemisel saate neis akendes siiski teavet vaadata, kuid ei saa sellega midagi teha.</span><span class="sxs-lookup"><span data-stu-id="c77e7-130">If this situation occurs, you can still view the information in these windows, but you will not be able to interact with it.</span></span>
