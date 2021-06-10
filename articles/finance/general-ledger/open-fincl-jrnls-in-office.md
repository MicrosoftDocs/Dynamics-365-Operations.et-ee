---
title: Finantstöölehe mallide avamine Office'is
description: Selles teemas kirjeldatakse probleeme, mis võivad ilmneda kohandatud finantstöölehtede loomisel Microsoft Exceli malli abil.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089453"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="75b29-103">Finantstöölehe mallide avamine Office'is</span><span class="sxs-lookup"><span data-stu-id="75b29-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75b29-104">Selles teemas kirjeldatakse probleeme, mis võivad ilmneda kohandatud finantstöölehtede loomisel Microsoft Exceli malli abil.</span><span class="sxs-lookup"><span data-stu-id="75b29-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="75b29-105">Sümptom</span><span class="sxs-lookup"><span data-stu-id="75b29-105">Symptom</span></span>

<span data-ttu-id="75b29-106">Lõite kohandatud Exceli malli finantstöölehtedele, kuid seda ei kuvata menüüs **Ava read Excelis**.</span><span class="sxs-lookup"><span data-stu-id="75b29-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="75b29-107">Või kui seda kuvatakse menüüs, avatakse selle valimisel mõni muu mall.</span><span class="sxs-lookup"><span data-stu-id="75b29-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="75b29-108">Lahendus</span><span class="sxs-lookup"><span data-stu-id="75b29-108">Resolution</span></span>

<span data-ttu-id="75b29-109">Vaikefunktsioon Ava Excelis kasutab käesoleva lehe juurandmeallikat (tabelit), et määrata, millised Office'i mallid või andmeüksused kuvatakse Exceli menüü **Ava Excelis** suvanditena.</span><span class="sxs-lookup"><span data-stu-id="75b29-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="75b29-110">Selline käitumine ei ole finantstöölehtede puhul ideaalne kasutuskogemus, kuna finantstöölehed kasutavad juurandmeallikaga samu tabeleid (LedgerJournalTable ja LedgerJournalTrans) paljude muud tüüpi töölehtede seast.</span><span class="sxs-lookup"><span data-stu-id="75b29-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="75b29-111">Finantstöölehtede puhul on funktsiooni Ava read Excelis eesmärk kuvada malle, mis on loodud töölehe jaoks, mille kontekstis praegu töötate, näiteks üldine tööleht või maksetööleht.</span><span class="sxs-lookup"><span data-stu-id="75b29-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="75b29-112">Näiteks mall, mis on mõeldud kasutamiseks hankija makse töölehega, on mõeldud jõustama teie esmase konto hankijakontona.</span><span class="sxs-lookup"><span data-stu-id="75b29-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="75b29-113">Kui soovite ülendada malli, et see oleks saadaval menüüs **Ava read Excelis** ja **Ava Excelis**, on lihtne arendajakogemus rakendada liidest **LedgerIJournalExcelTemplate** ja laiendada klassi **DocuTemplateRegistrationBase**.</span><span class="sxs-lookup"><span data-stu-id="75b29-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="75b29-114">Paljud selle lähenemisviisi näited rakendatakse selles süsteemis.</span><span class="sxs-lookup"><span data-stu-id="75b29-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="75b29-115">Üks näide, mida saab kasutada viitena, on liides **LedgerDailyJournalExcelTemplate** mis loodi üldise töölehe (või päevase töölehe) jaoks.</span><span class="sxs-lookup"><span data-stu-id="75b29-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="75b29-116">Kui liides **LedgerIJournalExcelTemplate** on teie mallile rakendatud, filtreeritakse menüüs **Ava read Excelis** mallid teie töölehe tüübi alusel ja kuvatakse ainult mallid, mis on selle töölehe jaoks saadaval.</span><span class="sxs-lookup"><span data-stu-id="75b29-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="75b29-117">Liides pakub ka kinnitusmeetodit, mis tagab, et malli ei saa töölehe jaoks avada, kui see ei vasta kontotüübi nõuetele.</span><span class="sxs-lookup"><span data-stu-id="75b29-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="75b29-118">Näiteks saate määrata, et konto tüüp peab olema **Hankija** või **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="75b29-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="75b29-119">Lisateavet selle funktsiooni kohta vt [Mallide lisamine menüüsse Ava read Excelis](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="75b29-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
