---
title: Suhtelise tee kasutamine ER-mudelite ja -vormingute andmesidemetes
description: Elektrooniline aruandluse tööriist võimaldab teil määratleda elektroonilise vormingu struktuurid ja seejärel kirjeldada, kuidas neid struktuure tuleb täita.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 321a85c675439b91b99ec5988494d7514a5c53f4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093133"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="c1817-103">Suhtelise tee kasutamine ER-mudelite ja -vormingute andmesidemetes</span><span class="sxs-lookup"><span data-stu-id="c1817-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1817-104">Elektrooniline aruandluse (ER) tööriist võimaldab kasutajatel määratleda elektroonilise vormingu struktuurid ja seejärel kirjeldada, kuidas neid struktuure tuleb täita, kasutades rakenduses olemasolevaid andmeid ja algoritme.</span><span class="sxs-lookup"><span data-stu-id="c1817-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="c1817-105">Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) konfiguratsioonide loomine](electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="c1817-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="c1817-106">Andmevoo määramiseks rakenduse Finance and Operations andmete toomiseks ja selle kasutamiseks elektrooniliste dokumentide loomisel, tuleb teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="c1817-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="c1817-107">Siduge konfigureeritud andmeallikad kujundatud domeenikohase [andmemudeli](general-electronic-reporting.md#data-model-and-model-mapping-components) elementidega.</span><span class="sxs-lookup"><span data-stu-id="c1817-107">Bind configured data sources to elements of the designed domain-specific [data model](general-electronic-reporting.md#data-model-and-model-mapping-components).</span></span> <span data-ttu-id="c1817-108">Mudeli struktuur ja valitud andmeallikad võivad olla osa keerukast hierarhilisest struktuurist.</span><span class="sxs-lookup"><span data-stu-id="c1817-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="c1817-109">Selle tõttu võivad lõplikud sidumised olla üsna suured ja sisaldada mitut erinevat tüüpi elemente (nt seosed, tabelid ja meetodid).</span><span class="sxs-lookup"><span data-stu-id="c1817-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="c1817-110">Sidumised võivad muutuda kehvemini loetavaks ning nende ülevaatamine ja mõistmine võib muutuda üsna keeruliseks, eriti mitteomanike jaoks.</span><span class="sxs-lookup"><span data-stu-id="c1817-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="c1817-111">Siduge andmemudeli elemendid [vormingu](general-electronic-reporting.md#FormatComponentOutbound) komponentidega, et määratleda, millised andmed sisestatakse andmemudelist loodud vormingu väljundisse.</span><span class="sxs-lookup"><span data-stu-id="c1817-111">Bind data model elements with [format](general-electronic-reporting.md#FormatComponentOutbound) components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="c1817-112">ER-i vastenduse kujundaja kasutatavuse parandamiseks on loodud [suhtelise teekonna](er-formula-language.md#relative-path) funktsioon.</span><span class="sxs-lookup"><span data-stu-id="c1817-112">To improve usability of ER mapping designers, the [relative path](er-formula-language.md#relative-path) feature has been released.</span></span> <span data-ttu-id="c1817-113">Vaikimisi on suhtelise tee esindatuse suvand sisse lülitatud kõigi rakenduse Finance and Operations uute eksemplaride jaoks, kus on lubatud ER-i kujundamise kogemus (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span><span class="sxs-lookup"><span data-stu-id="c1817-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="c1817-114">Rakendasime suhtelise tee parameetri, et kasutajad saaksid selle ER-i sidumise esitlusega töötades jätkata täieliku tee kasutamist.</span><span class="sxs-lookup"><span data-stu-id="c1817-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="c1817-115">[![Kasutaja parameetrid](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="c1817-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="c1817-116">Kui suhtelise tee kasutusparameeter on sisse lülitatud, asendab üks @-märk praeguse mudeli elemendi sidumisel tee emaüksuseni.</span><span class="sxs-lookup"><span data-stu-id="c1817-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="c1817-117">Kogu sidumise tee muutub lühemaks, mis muudab kogu vastendamise ilmsemaks ja kergemini mõistetavaks.</span><span class="sxs-lookup"><span data-stu-id="c1817-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="c1817-118">Enamasti ei ole ER-i kujundajas vaja kõigi andmemudelite sidumiste kuvamiseks täiendavat kerimist.</span><span class="sxs-lookup"><span data-stu-id="c1817-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="c1817-119">[![Mudelivastenduse kujundaja](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="c1817-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="c1817-120">Uue ER-i avaldise kujundamise alustamisel tuleb sisestada ainult üks märk, et määratleda seos emaüksuse väljaga.</span><span class="sxs-lookup"><span data-stu-id="c1817-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="c1817-121">[![Valemikoostaja](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="c1817-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="c1817-122">Kui otsustate muuta emamudeli üksuse andmeallikat absoluutse teekasutusega, peate selle mudelkauba ja kõik pesastatud üksused uue andmeallikaga käsitsi uuesti siduma.</span><span class="sxs-lookup"><span data-stu-id="c1817-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="c1817-123">Kui suhtelise tee kasutamine on sisse lülitatud ja te valite emaüksusele sidumiseks uue andmeallika, pakutakse teile valikut kõik selle emaüksuse pesastatud üksused automaatselt ühe klõpsuga uuesti siduda.</span><span class="sxs-lookup"><span data-stu-id="c1817-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="c1817-124">[![Olemasoleva tee asendamise teade](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="c1817-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="c1817-125">Kui kinnitate pesastatud üksuste uuesti sidumise, paigutatakse uus emaüksus igale olemasolevat emaüksust sisaldava pesastatud üksuse teele.</span><span class="sxs-lookup"><span data-stu-id="c1817-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="c1817-126">See funktsioon ei lõhu ER-i raamistiku tagasiühilduvust.</span><span class="sxs-lookup"><span data-stu-id="c1817-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="c1817-127">Selle uue funktsiooniga töötavad kõik varem kavandatud ER-i konfiguratsioonid ja värskendusi ega teisendusi pole vaja.</span><span class="sxs-lookup"><span data-stu-id="c1817-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="c1817-128">Kõik muudatused, mis kaasnevad pesastatud elementide sidumise massilise muutmisega mudelivastendustes, salvestatakse õigesti konfiguratsiooni deltas (muutuste jälg).</span><span class="sxs-lookup"><span data-stu-id="c1817-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="c1817-129">See võimaldab klientidel muuta nende mudelivastenduste tuletatud versiooni aluse mis tahes uuele alusversioonile, mida on selle uue funktsiooniga muudetud.</span><span class="sxs-lookup"><span data-stu-id="c1817-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c1817-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c1817-130">Additional resources</span></span>

[<span data-ttu-id="c1817-131">ER-i valemi keel</span><span class="sxs-lookup"><span data-stu-id="c1817-131">ER formula language</span></span>](er-formula-language.md)
