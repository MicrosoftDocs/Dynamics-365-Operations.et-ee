---
title: Identifitseerimisnumbri siltide dokumendi marsruudi valiku paigutus
description: Sellese teemas kirjeldatakse, kuidas kasutada vormindamisviise siltidele väärtuste printimiseks.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.10
ms.openlocfilehash: faf54fec2885f868c66987a7b481559d0c5615d0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838270"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="03fab-103">Identifitseerimisnumbri siltide dokumendi marsruudi valiku paigutus</span><span class="sxs-lookup"><span data-stu-id="03fab-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="03fab-104">See dokumendi marsruudi valiku paigutus määratleb identifitseerimisnumbri siltide paigutuse ja neile prinditavad andmed.</span><span class="sxs-lookup"><span data-stu-id="03fab-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="03fab-105">Saate konfigureerida printimise käivitamispunktid mobiilsideseadme menüü üksuste ja töömallide häälestamisel.</span><span class="sxs-lookup"><span data-stu-id="03fab-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="03fab-106">Tavaolukorras prindivad lao vastuvõtuametnikud identifitseerimisnumbri sildid kohe pärast vastuvõtualale saabuvate kaubaaluste sisu kirjendamist.</span><span class="sxs-lookup"><span data-stu-id="03fab-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="03fab-107">Füüsilised sildid paigaldatakse kaubaalustele.</span><span class="sxs-lookup"><span data-stu-id="03fab-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="03fab-108">Seejärel saab neid kasutada kinnitamiseks järgneva ladustamisprotsessi tulevaste väljaminevate komplekteerimistegevuste käigus.</span><span class="sxs-lookup"><span data-stu-id="03fab-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="03fab-109">Saate printida väga keerukaid silte, eeldusel, et printimisseade suudab tuvastada sellele saadetud teksti.</span><span class="sxs-lookup"><span data-stu-id="03fab-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="03fab-110">Näiteks vöötkoodi sisaldav Zebra programmeerimiskeele (ZPL) paigutus, mis sarnaneb järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="03fab-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="03fab-111">Sildi printimise protsessi käigus asendatakse selle näite tekst `$LicensePlateId$` andmeväärtusega.</span><span class="sxs-lookup"><span data-stu-id="03fab-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="03fab-112">Prinditavate väärtuste nägemiseks avage jaotis **Laohaldus \> Päringud ja aruanded \> Identifitseerimisnumbri sildid**.</span><span class="sxs-lookup"><span data-stu-id="03fab-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="03fab-113">Mitmed laialdaselt kättesaadavad siltide tegemise tööriistad aitavad teil vormindada sildi paigutuse teksti.</span><span class="sxs-lookup"><span data-stu-id="03fab-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="03fab-114">Paljud neist tööriistadest toetavad vormingut `$FieldName$`.</span><span class="sxs-lookup"><span data-stu-id="03fab-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="03fab-115">Lisaks kasutab Microsoft Dynamics 365 Supply Chain Management erivormingu loogikat dokumendi marsruudi valiku paigutuse välja vastenduse osana.</span><span class="sxs-lookup"><span data-stu-id="03fab-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="turn-on-this-feature-for-your-system"></a><span data-ttu-id="03fab-116">Selle funktsiooni sisselülitamine teie süsteemi jaoks</span><span class="sxs-lookup"><span data-stu-id="03fab-116">Turn on this feature for your system</span></span>

<span data-ttu-id="03fab-117">Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsioone, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage sisse funktsioon *Litsentsiplaadi siltide täiustatud paigutused*.</span><span class="sxs-lookup"><span data-stu-id="03fab-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the *Enhanced license plate label layouts* feature.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="03fab-118">Kohandatud numbrivormingud</span><span class="sxs-lookup"><span data-stu-id="03fab-118">Custom number formats</span></span>

<span data-ttu-id="03fab-119">Saate kohandada numbriväljade väärtuste vormingut, mis prinditakse järgmis vorminguga koodide abil.</span><span class="sxs-lookup"><span data-stu-id="03fab-119">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="03fab-120">Siin on selle vormingu kohta selgitus.</span><span class="sxs-lookup"><span data-stu-id="03fab-120">Here is an explanation of this format:</span></span>

- <span data-ttu-id="03fab-121">`FieldName` on andmevälja nimi (nt **Kogus**).</span><span class="sxs-lookup"><span data-stu-id="03fab-121">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="03fab-122">`FormatString` määratleb, kuidas andmeid peab printima.</span><span class="sxs-lookup"><span data-stu-id="03fab-122">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="03fab-123">Järgmistes näidetes kirjeldatakse, kuidas saate kohandada välja töö kogus (**Kogus**).</span><span class="sxs-lookup"><span data-stu-id="03fab-123">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="03fab-124">Kui soovite alati nelja numbrit kuvada (kasutades nulle kohatäitena), kasutage `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="03fab-124">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="03fab-125">Näiteks kui kogus on 10, kuvatakse sildil „0010”.</span><span class="sxs-lookup"><span data-stu-id="03fab-125">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="03fab-126">Kui soovite alati kahte komakohta kuvada, kasutage `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="03fab-126">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="03fab-127">Näiteks kui kogus on 10, kuvatakse sildil „10,00”.</span><span class="sxs-lookup"><span data-stu-id="03fab-127">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="03fab-128">Saadaolevate numbrivormingu stringide täieliku loendi leiate teemast [Kohandatud numbrivormingu stringid](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="03fab-128">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="03fab-129">Kohandatud stringi vormingud</span><span class="sxs-lookup"><span data-stu-id="03fab-129">Custom string formats</span></span>

<span data-ttu-id="03fab-130">Stringi esimesi tähemärke saate eemaldada järgneva välja ja vormingu koodi abil.</span><span class="sxs-lookup"><span data-stu-id="03fab-130">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="03fab-131">Tähemärk `#` tähistab siin vahelejäetavate tähemärkide arvu.</span><span class="sxs-lookup"><span data-stu-id="03fab-131">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="03fab-132">Näiteks konteineri seeriaviisilise lähetamise kood (SSCC) identifitseerimisnumbri printimiseks, mis ei sisalda kahte esimest märki, kasutage `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="03fab-132">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="03fab-133">Sel juhul prinditakse identifitseerimisnumber 0011111111111222221 kujul „11111111111222221”.</span><span class="sxs-lookup"><span data-stu-id="03fab-133">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="03fab-134">Kohandatud kuupäeva/kellaaja vormingud</span><span class="sxs-lookup"><span data-stu-id="03fab-134">Custom date/time formats</span></span>

<span data-ttu-id="03fab-135">Järgmises näites kirjeldatakse, kuidas saate juhtida kuupäevade printimiseks kasutatavat vormingut.</span><span class="sxs-lookup"><span data-stu-id="03fab-135">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="03fab-136">Selles näites prinditakse kuupäev 30. aprill 2020 kujul „30-04-2020”.</span><span class="sxs-lookup"><span data-stu-id="03fab-136">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="03fab-137">Saadaolevate kuupäeva/kellaaja vormingute täieliku loendi leiate teemast [Kohandatud kuupäeva ja kellaaja vormingu stringid](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="03fab-137">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="03fab-138">Üksikute ridade printimine mitmerealistest andmetest</span><span class="sxs-lookup"><span data-stu-id="03fab-138">Print individual lines from multiline data</span></span>

<span data-ttu-id="03fab-139">Kui andmeväli sisaldab mitut rida (st ridu, mis on eraldatud rea jaotustega), saate printida üksiku rea järgmise vormingu abil.</span><span class="sxs-lookup"><span data-stu-id="03fab-139">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="03fab-140">Tähemärk `#` tähistab siin rea numbrit, mida soovite printida.</span><span class="sxs-lookup"><span data-stu-id="03fab-140">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="03fab-141">(Kasutage numbrit 1 esimesel real.)</span><span class="sxs-lookup"><span data-stu-id="03fab-141">(Use 1 for the first line.)</span></span>

<span data-ttu-id="03fab-142">Näiteks kui teie süsteemil on väli `AdditionalAddress`, mis talletab mitmerealise aadressi järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="03fab-142">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="03fab-143">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="03fab-143">Contoso Inc.</span></span>  
<span data-ttu-id="03fab-144">Tänava nimi 123</span><span class="sxs-lookup"><span data-stu-id="03fab-144">123 Street Name</span></span>  
<span data-ttu-id="03fab-145">Mingi linn, mingi riik</span><span class="sxs-lookup"><span data-stu-id="03fab-145">Some City, Some State</span></span>

<span data-ttu-id="03fab-146">Saate printida selle aadressi ühe rea kaupa järgmiste koodide abil.</span><span class="sxs-lookup"><span data-stu-id="03fab-146">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="03fab-147">Kood</span><span class="sxs-lookup"><span data-stu-id="03fab-147">Code</span></span> | <span data-ttu-id="03fab-148">Prinditav tekst</span><span class="sxs-lookup"><span data-stu-id="03fab-148">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="03fab-149">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="03fab-149">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="03fab-150">Tänava nimi 123</span><span class="sxs-lookup"><span data-stu-id="03fab-150">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="03fab-151">Mingi linn, mingi riik</span><span class="sxs-lookup"><span data-stu-id="03fab-151">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="03fab-152">Printimine ja vorming kuvamisviisilt</span><span class="sxs-lookup"><span data-stu-id="03fab-152">Print and format from a display method</span></span>

<span data-ttu-id="03fab-153">Saate printida kuvamisviisi abil, kasutades järgmist vormingut.</span><span class="sxs-lookup"><span data-stu-id="03fab-153">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="03fab-154">Saate kombineerida seda vormingut teiste selles teemas eelnevalt kirjeldatud tüüpidega.</span><span class="sxs-lookup"><span data-stu-id="03fab-154">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="03fab-155">Näiteks kui on teil kuvamisviis nimega `DisplayListOfItemsNumbers()` ja soovite printida selle viisi esimese kaubakoodi.</span><span class="sxs-lookup"><span data-stu-id="03fab-155">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="03fab-156">Sel juhul saate kasutada järgmist koodi.</span><span class="sxs-lookup"><span data-stu-id="03fab-156">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="03fab-157">Lisateave siltide printimise kohta</span><span class="sxs-lookup"><span data-stu-id="03fab-157">More information about how to print labels</span></span>

<span data-ttu-id="03fab-158">Lisateavet siltide seadistamise ja printimise kohta leiate teemast [Identifitseerimisnumbri sildi printimise lubamine](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="03fab-158">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]