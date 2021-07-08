---
title: Elektroonilise aruandluse täiustatud valemiredaktor
description: See teema kirjeldab, kuidas täiustatud valemiredaktorit saab kasutada avaldiste konfigureerimiseks elektroonilise aruandluse (ER) mudeli vastendamise ja vormindamise komponentide jaoks.
author: NickSelin
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: f7f80928e1d3f5d4892f72d4bd2fd09b70a26c1f
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270703"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="821d7-103">Elektroonilise aruandluse täiustatud valemiredaktor</span><span class="sxs-lookup"><span data-stu-id="821d7-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="821d7-104">Lisaks [Elektroonilise aruandluse](general-electronic-reporting.md) [valemiredaktorile](general-electronic-reporting-formula-designer.md) saate täpsema elektroonilise aruandluse valemi redaktori abil parandada elektroonilise aruandluse (ER) avaldiste konfigureerimise kogemust.</span><span class="sxs-lookup"><span data-stu-id="821d7-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="821d7-105">Täiustatud redaktor on brauseril põhinev ja seda kasutab [Monaco Editor](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="821d7-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="821d7-106">Selles teemas kirjeldatakse kõige sagedamini kasutatavaid täpsemaid redaktori funktsioone:</span><span class="sxs-lookup"><span data-stu-id="821d7-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="821d7-107">Koodi isevormindamine</span><span class="sxs-lookup"><span data-stu-id="821d7-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="821d7-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="821d7-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="821d7-109">Koodi loomine</span><span class="sxs-lookup"><span data-stu-id="821d7-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="821d7-110">Koodis liikumine</span><span class="sxs-lookup"><span data-stu-id="821d7-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="821d7-111">Koodi struktureerimine</span><span class="sxs-lookup"><span data-stu-id="821d7-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="821d7-112">Otsi ja asenda</span><span class="sxs-lookup"><span data-stu-id="821d7-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="821d7-113">Andmete kleepimine</span><span class="sxs-lookup"><span data-stu-id="821d7-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="821d7-114">Süntaksi värving</span><span class="sxs-lookup"><span data-stu-id="821d7-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="821d7-115"><a name="ActivateAdvEditor">Täpsema valemiredaktori aktiveerimine</a></span><span class="sxs-lookup"><span data-stu-id="821d7-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="821d7-116">Tehke järgmised sammud, et alustada oma Microsofti Dynamics 365 Finance eksemplaris täpsema valemiredaktori kasutamist.</span><span class="sxs-lookup"><span data-stu-id="821d7-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="821d7-117">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="821d7-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="821d7-118">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="821d7-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="821d7-119">Seadke dialoogiboksi **Kasutaja parameetrid** jaotise **Käivitamise jälitus** valiku **Luba täpsem valemiredaktor** parameetriks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="821d7-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="821d7-120">[![Kasutajaparameetrite dialoogiboks, kus Luba täpsema valemiredaktori parameeter on esile tõstetud](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="821d7-120">[![User parameters dialog box, Enable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="821d7-121">Pange tähele, et see parameeter on kasutajakohane ja ettevõttekohane.</span><span class="sxs-lookup"><span data-stu-id="821d7-121">Be aware that this parameter is user specific and company specific.</span></span>

<span data-ttu-id="821d7-122">Alates Microsoft Dynamics 365 Finance versioonist 10.0.19 saate vaikimisi kontrollida, millist ER valemiredaktorit pakutakse.</span><span class="sxs-lookup"><span data-stu-id="821d7-122">Starting in Microsoft Dynamics 365 Finance version 10.0.19, you can control what ER formula editor is offered by default.</span></span> <span data-ttu-id="821d7-123">Viige lõpule järgmised sammud, et lubada täiustatud valemiredaktor kõikidele kasutajatele ja ettevõtetele praeguses Finance eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="821d7-123">Complete the following steps to enable the advanced formula editor for all users and companies of the current Finance instance.</span></span>

1.  <span data-ttu-id="821d7-124">Avage tööruum **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="821d7-124">Open the **Feature management** workspace.</span></span>
2.  <span data-ttu-id="821d7-125">Leidke ja valige funktsioon **Määra kõigi loendis kasutajate jaoks vaikeväärtuseks ER-i täpsem valemiredaktor** ning seejärel valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="821d7-125">Find and select the feature **Set the ER advanced formula editor as the default one for all users** in the list, and then select **Enable now**.</span></span>
3.  <span data-ttu-id="821d7-126">Avage **Organisatsiooni haldamine** > **Elektrooniline aruandlus** > **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="821d7-126">Go to **Organization administration** > **Electronic reporting** > **Configurations**.</span></span>
4.  <span data-ttu-id="821d7-127">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="821d7-127">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
5.  <span data-ttu-id="821d7-128">Leidke dialoogiboksis **Kasutaja parameetrid** parameeter **Keela täpsem valemiredaktor** ja veenduge, et selle väärtuseks oleks määratud **Ei**.</span><span class="sxs-lookup"><span data-stu-id="821d7-128">In the **User parameters** dialog box, find the **Disable advanced formula editor** parameter and verify that it is set to **No**.</span></span>

<span data-ttu-id="821d7-129">[![Kasutajaparameetrite dialoogiboks, kus Keela täpsema valemiredaktori parameeter on esile tõstetud](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span><span class="sxs-lookup"><span data-stu-id="821d7-129">[![User parameters dialog box, Disable advanced formula editor parameter highlighted](./media/ER-AdvEditor-Activate2.png)](./media/ER-AdvEditor-Activate2.png)</span></span>

> [!NOTE]
> <span data-ttu-id="821d7-130">Parameetrite **Luba täpsem valemiredaktor** ja **Keela täpsem valemiredaktor** väärtused hoitakse eraldi iga kasutaja jaoks ja neid pakutakse dialoogiboksis **Kasutajaparameetrid** sõltuvalt **Määra ER-i täpsema valemiredaktori vaikimisi kõigi kasutajate** funktsiooni olekust.</span><span class="sxs-lookup"><span data-stu-id="821d7-130">The values of the parameters **Enable advanced formula editor** and **Disable advanced formula editor** are kept separate for each user and offered on the **User parameters** dialog box depending on the status of the **Set the ER advanced formula editor as the default one for all users** feature.</span></span>

## <a name=""></a><span data-ttu-id="821d7-131"><a name="Autoformatting">Koodi isevormindamine</a></span><span class="sxs-lookup"><span data-stu-id="821d7-131"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="821d7-132">Kui kirjutate mitut rida koodi sisaldava keeruka avaldise, on uue sisestatud rea taande aluseks eelmise rea taane.</span><span class="sxs-lookup"><span data-stu-id="821d7-132">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="821d7-133">Saate valida read ja muuta nende taanet, vajutades klahvi **TAB** või klahvikombinatsiooni **SHIFT +TAB**.</span><span class="sxs-lookup"><span data-stu-id="821d7-133">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="821d7-134">[![ER-i valemiredaktori gif, kus kuvatakse ridade valimine ja taande muutmine](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="821d7-134">[![ER formula editor gif showing selecting lines and changing the indentation](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="821d7-135">Automaatvormindus võimaldab teil säilitada kogu avaldise hästi vormindatuna, et muuta edasine hooldus lihtsamaks ja lihtsustada konfigureerimise loogika mõistmist.</span><span class="sxs-lookup"><span data-stu-id="821d7-135">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="821d7-136"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="821d7-136"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="821d7-137">Redaktoris on sõnalõpetamise funtsioon, mis aitab teil avaldist kiiremini kirjutada ja vältida kirjavigu.</span><span class="sxs-lookup"><span data-stu-id="821d7-137">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="821d7-138">Uue teksti lisamisel pakub redaktor automaatselt loendit funktsioonidest, mis esinevad teie sisestatud märkidega ER-funktsioonides.</span><span class="sxs-lookup"><span data-stu-id="821d7-138">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="821d7-139">Saate käivitada IntelliSense'i ka konfigureeritud avaldise suvalises asukohas, vajutades **CTRL + tühik**.</span><span class="sxs-lookup"><span data-stu-id="821d7-139">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="821d7-140">[![ER-i valemiredaktori gif, mis näitab IntelliSense'i käivitamist](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="821d7-140">[![ER formula editor gif showing triggering IntelliSense](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="821d7-141"><a name="CodeCompletion">Koodi lõpetamine</a></span><span class="sxs-lookup"><span data-stu-id="821d7-141"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="821d7-142">Redaktor annab automaatselt koodi lõpetamise:</span><span class="sxs-lookup"><span data-stu-id="821d7-142">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="821d7-143">lisades lõpusulu, kui sisestatakse algussulg, hoides kursorit sulgude sees.</span><span class="sxs-lookup"><span data-stu-id="821d7-143">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="821d7-144">Teise ülakoma sisestamine, kui esimene on sisestatud, hoides kursorit ülakomade vahel.</span><span class="sxs-lookup"><span data-stu-id="821d7-144">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="821d7-145">Teise jutumärgi sisestamine, kui esimene on sisestatud, hoides kursorit jutumärkide sees.</span><span class="sxs-lookup"><span data-stu-id="821d7-145">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="821d7-146">[![ER-i valemiredaktori gif, kus kuvatakse koodi lõpuleviimiseks automaatselt redaktor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="821d7-146">[![ER formula editor gif showing the editor automatically providing code completion](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="821d7-147">Kui osutate sisestatud sulule, tõstetakse selle paari teine sulg automaatselt esile, et näidata nende sees olevat vormelit.</span><span class="sxs-lookup"><span data-stu-id="821d7-147">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="821d7-148"><a name="CodeNavigation">Koodis liikumine</a></span><span class="sxs-lookup"><span data-stu-id="821d7-148"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="821d7-149">Saate otsida oma avaldises sümboleid või ridu, tippides käsu **Mine** või kasutades käsupaletti või kontekstimenüüd.</span><span class="sxs-lookup"><span data-stu-id="821d7-149">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="821d7-150">Näiteks, et hüpata reale **8**, tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="821d7-150">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="821d7-151">Vajutage **Ctrl + G** sisestage väärtus **8** ja vajutage seejärel sisestusklahvi **Enter**.</span><span class="sxs-lookup"><span data-stu-id="821d7-151">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="821d7-152">- või -</span><span class="sxs-lookup"><span data-stu-id="821d7-152">-or-</span></span>

- <span data-ttu-id="821d7-153">Vajutage klahvi **F1**, tippige **G**, valige **Mine reale** sisestage väärtus **8** vajutage sisestusklahvi (**Enter**).</span><span class="sxs-lookup"><span data-stu-id="821d7-153">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="821d7-154">[![ER-i valemiredaktori gif, mis näitab, kuidas avaldise osi käsureapaleti abil leida](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="821d7-154">[![ER formula editor gif showing how to locate parts of an expression using the command palette](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="821d7-155"><a name="CodeStructuring">Koodi struktureerimine</a></span><span class="sxs-lookup"><span data-stu-id="821d7-155"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="821d7-156">Mõne funktsiooni, nt [IF](er-functions-logical-if.md) või [CASE](er-functions-logical-case.md) kood on automaatselt struktureeritud.</span><span class="sxs-lookup"><span data-stu-id="821d7-156">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="821d7-157">Saate laiendada ja ahendada selle koodi kõiki ahendatavaid kohti, et vähendada avaldise redigeeritavat osa, et keskenduda ainult koodijupile, mis nõuab teie tähelepanu.</span><span class="sxs-lookup"><span data-stu-id="821d7-157">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="821d7-158">Selle jaoks saab kasutada funktsiooni Lülita ahendamine/laiendamine käske.</span><span class="sxs-lookup"><span data-stu-id="821d7-158">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="821d7-159">Näiteks kõigi piirkondade ahendamiseks tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="821d7-159">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="821d7-160">Vajutage **CTRL + K**</span><span class="sxs-lookup"><span data-stu-id="821d7-160">Press **Ctrl+K**</span></span>

  <span data-ttu-id="821d7-161">- või -</span><span class="sxs-lookup"><span data-stu-id="821d7-161">-or-</span></span>

- <span data-ttu-id="821d7-162">Vajutage klahvi **F1**, vajutage **FO**, valige **Ahenda kõik** ja seejärel vajutage sisestusklahvi **Enter**.</span><span class="sxs-lookup"><span data-stu-id="821d7-162">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="821d7-163">Kõigi piirkondade ahendamiseks tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="821d7-163">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="821d7-164">Vajutage **CTRL + J**</span><span class="sxs-lookup"><span data-stu-id="821d7-164">Press **Ctrl+J**</span></span>

  <span data-ttu-id="821d7-165">- või -</span><span class="sxs-lookup"><span data-stu-id="821d7-165">-or-</span></span>
  
- <span data-ttu-id="821d7-166">Vajutage klahvi **F1**, tippige **UN**, valige **Laienda kõik** ja seejärel vajutage sisestusklahvi **Enter**.</span><span class="sxs-lookup"><span data-stu-id="821d7-166">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="821d7-167">[![ER-i valemiredaktori gif, mis näitab kuvatavat koodi](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="821d7-167">[![ER formula editor gif showing code being unfolded](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="821d7-168"><a name="FindAndReplace">Otsi ja asenda</a></span><span class="sxs-lookup"><span data-stu-id="821d7-168"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="821d7-169">Teatud teksti otsimiseks valige oma avaldises tekst ja tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="821d7-169">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="821d7-170">Vajutage **CTRL + F** ja vajutage seejärel **F3**, et leida valitud teksti järgmine esinemiskord või vajutage eelmise esinemiskorra leidmiseks klahvikombinatsiooni **SHIFT + F3**.</span><span class="sxs-lookup"><span data-stu-id="821d7-170">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="821d7-171">- või -</span><span class="sxs-lookup"><span data-stu-id="821d7-171">-or-</span></span>
  
- <span data-ttu-id="821d7-172">Vajutage klahvi **F1**, tippige **F** ja seejärel valige valitud teksti otsimiseks vajalik suvand.</span><span class="sxs-lookup"><span data-stu-id="821d7-172">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="821d7-173">Teatud teksti esinemiskordade asendamiseks valige oma avaldises tekst ja tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="821d7-173">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="821d7-174">Vajutage **CTRL + H**.</span><span class="sxs-lookup"><span data-stu-id="821d7-174">Press **Ctrl+H**.</span></span> <span data-ttu-id="821d7-175">Sisestage asetekst ja valige asenduse suvand, et asendada valitud tekst või selle teksti kõik esinemisjuhud praeguses avaldises.</span><span class="sxs-lookup"><span data-stu-id="821d7-175">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="821d7-176">- või -</span><span class="sxs-lookup"><span data-stu-id="821d7-176">-or-</span></span>
  
- <span data-ttu-id="821d7-177">Vajutage klahvi **F1**, tippige **R** ja seejärel valige valitud teksti asendamiseks vajalik suvand.</span><span class="sxs-lookup"><span data-stu-id="821d7-177">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="821d7-178">Sisestage asetekst ja valige asenduse suvand, et asendada valitud tekst või selle teksti kõik esinemisjuhud praeguses avaldises.</span><span class="sxs-lookup"><span data-stu-id="821d7-178">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="821d7-179">Teatud teksti kõigi esinemiskordade asendamiseks valige oma avaldises tekst ja tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="821d7-179">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="821d7-180">Vajutage **CTRL + 2** ja sisestage seejärel alternatiivne tekst.</span><span class="sxs-lookup"><span data-stu-id="821d7-180">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="821d7-181">- või -</span><span class="sxs-lookup"><span data-stu-id="821d7-181">-or-</span></span>
  
- <span data-ttu-id="821d7-182">Vajutage klahvi **F1**, tippige **C** ja seejärel valige valitud teksti muutmiseks vajalik suvand.</span><span class="sxs-lookup"><span data-stu-id="821d7-182">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="821d7-183">Sisestage alternatiivne tekst.</span><span class="sxs-lookup"><span data-stu-id="821d7-183">Enter the alternative text.</span></span>

<span data-ttu-id="821d7-184">[![ER-i valemiredaktori gif, mis näitab otsingut ja asendust](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="821d7-184">[![ER formula editor gif showing find and replace](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="821d7-185"><a name="DataPasting">Andmeallikad ja funktsioonide kleepimine</a></span><span class="sxs-lookup"><span data-stu-id="821d7-185"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="821d7-186">Saate valida **Lisa andmeallikas**, mis kleebib praegusele avaldisele andmeallika, mis on praegu valitud **Andmeallika** vasakul paanil.</span><span class="sxs-lookup"><span data-stu-id="821d7-186">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="821d7-187">Samamoodi saate valida **Lisa funktsioon**, mis kleebib praegusele avaldisele funktsiooni, mis on praegu valitud **Funktsioonide** paremal paanil.</span><span class="sxs-lookup"><span data-stu-id="821d7-187">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="821d7-188">Kui kasutate ER-i valemiredaktorit, kleebitakse valitud funktsioon või valitud andmeallikas alati konfigureeritud avaldise lõppu.</span><span class="sxs-lookup"><span data-stu-id="821d7-188">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="821d7-189">Kui kasutate täiustatud ER-i valemiredaktorit, saab valitud funktsiooni või valitud andmeallika alati kleepida konfigureeritud avaldise mis tahes ossa.</span><span class="sxs-lookup"><span data-stu-id="821d7-189">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="821d7-190">Peate kasutama kursorit, et määrata, kuhu soovite andmed kleepida.</span><span class="sxs-lookup"><span data-stu-id="821d7-190">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="821d7-191">[![ER-i valemiredaktori gif, kus kuvatakse andmeallika lisamine ja funktsiooni kleepimine](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="821d7-191">[![ER formula editor gif showing adding a data source and pasting a function](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="821d7-192"><a name="SyntaxColorization">Süntaksi värving</a></span><span class="sxs-lookup"><span data-stu-id="821d7-192"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="821d7-193">Praegu kasutatakse erinevaid värve järgmiste avaldiste osade esiletõstmiseks:</span><span class="sxs-lookup"><span data-stu-id="821d7-193">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="821d7-194">Kahekordsetes sulgudes olev tekst, mis võib tähistada teksti konstandi sildi ID-d.</span><span class="sxs-lookup"><span data-stu-id="821d7-194">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="821d7-195">[![ER valemiredaktor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="821d7-195">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="821d7-196">Kitsendused</span><span class="sxs-lookup"><span data-stu-id="821d7-196">Limitations</span></span>

<span data-ttu-id="821d7-197">Redaktorit toetavad praegu järgmised veebibrauserid:</span><span class="sxs-lookup"><span data-stu-id="821d7-197">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="821d7-198">Chrome</span><span class="sxs-lookup"><span data-stu-id="821d7-198">Chrome</span></span>
- <span data-ttu-id="821d7-199">Edge</span><span class="sxs-lookup"><span data-stu-id="821d7-199">Edge</span></span>
- <span data-ttu-id="821d7-200">Firefox</span><span class="sxs-lookup"><span data-stu-id="821d7-200">Firefox</span></span>
- <span data-ttu-id="821d7-201">Opera</span><span class="sxs-lookup"><span data-stu-id="821d7-201">Opera</span></span>
- <span data-ttu-id="821d7-202">Safari</span><span class="sxs-lookup"><span data-stu-id="821d7-202">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="821d7-203">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="821d7-203">Additional resources</span></span>

- [<span data-ttu-id="821d7-204">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="821d7-204">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="821d7-205">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="821d7-205">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="821d7-206">Monaco redaktor</span><span class="sxs-lookup"><span data-stu-id="821d7-206">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
