---
title: Positiivse makse failide seadistamine ja loomine
description: See teema selgitab, kuidas positiivset makset seadistada ja positiivse makse faile luua.
author: panolte
manager: AnnBe
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 82f7c8947bcc2dab394ea24e28a3631cc8682e5a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442314"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="677a4-103">Positiivse makse failide seadistamine ja loomine</span><span class="sxs-lookup"><span data-stu-id="677a4-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="677a4-104">See teema selgitab, kuidas positiivset makset seadistada ja positiivse makse faile luua.</span><span class="sxs-lookup"><span data-stu-id="677a4-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="677a4-105">Positiivse makse seadistamine pangale edastatava elektroonilise tšekkide loendi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="677a4-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="677a4-106">Tšeki esitamisel pangale võrdleb pank seda tšekkide loendiga.</span><span class="sxs-lookup"><span data-stu-id="677a4-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="677a4-107">Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja.</span><span class="sxs-lookup"><span data-stu-id="677a4-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="677a4-108">Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.</span><span class="sxs-lookup"><span data-stu-id="677a4-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="677a4-109">Positiivse makse failide turve</span><span class="sxs-lookup"><span data-stu-id="677a4-109">Security for positive pay files</span></span>
<span data-ttu-id="677a4-110">Positiivse makse failides võib olla tundliku loomuga teavet maksesaajate ja tšekisummade kohta.</span><span class="sxs-lookup"><span data-stu-id="677a4-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="677a4-111">Seetõttu kasutage kindlasti vajalikke turvameetmeid alates failide loomise hetkest kuni nende panka saabumiseni.</span><span class="sxs-lookup"><span data-stu-id="677a4-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="677a4-112">Positiivse makse failid laaditakse alla teie veebibrauseri määratud asukohta.</span><span class="sxs-lookup"><span data-stu-id="677a4-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="677a4-113">Positiivse makse failides võib olla tundlikke andmeid, seega on tähtis, et ainult autoriseeritud kasutajatel oleks juurdepääs selle teabe loomiseks ja vaatamiseks Microsoft Dynamics 365 Financeis.</span><span class="sxs-lookup"><span data-stu-id="677a4-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="677a4-114">Järgmise tabelis abil saate määratleda vajalikke õigusi.</span><span class="sxs-lookup"><span data-stu-id="677a4-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="677a4-115">Ülesanne</span><span class="sxs-lookup"><span data-stu-id="677a4-115">Task</span></span></th>
<th><span data-ttu-id="677a4-116">Eesõigus</span><span class="sxs-lookup"><span data-stu-id="677a4-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="677a4-117">Saate luua positiivse makse faile loendilehelt <strong>Pangakontod</strong> või lehelt <strong>Pangakontod</strong>.</span><span class="sxs-lookup"><span data-stu-id="677a4-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="677a4-118"><strong>Panga positiivse makse teabe haldamine</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="677a4-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="677a4-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="677a4-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="677a4-120">Positiivse makse failide loomine juriidiliste isikute ning pangakontode jaoks lehelt <strong>Loo positiivne maksefail</strong>.</span><span class="sxs-lookup"><span data-stu-id="677a4-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="677a4-121"><strong>Panga positiivse makse teabe haldamine</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="677a4-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="677a4-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="677a4-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="677a4-123">Positiivseid maksefaile saab vaadata lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</span><span class="sxs-lookup"><span data-stu-id="677a4-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="677a4-124"><strong>Vaata panga positiivset makseteavet mitme juriidilise isiku kohta</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="677a4-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="677a4-125">Positiivse maksefaili saab kinnitada lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</span><span class="sxs-lookup"><span data-stu-id="677a4-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="677a4-126"><strong>Kinnita positiivne maksefail</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="677a4-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="677a4-127">Positiivse maksefaili saab tagasi võtta lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</span><span class="sxs-lookup"><span data-stu-id="677a4-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="677a4-128"><strong>Positiivse makse faili tagasivõtmine</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="677a4-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="677a4-129">Positiivse maksevormingu seadistamine</span><span class="sxs-lookup"><span data-stu-id="677a4-129">Set up a positive pay format</span></span>
<span data-ttu-id="677a4-130">Positiivse makse failid luuakse andmeüksuste abil.</span><span class="sxs-lookup"><span data-stu-id="677a4-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="677a4-131">Enne positiivse maksefaili loomist peate seadistama teisendamise sisendvormingu, mida kasutatakse tšeki teabe teisendamiseks pangale sobivasse vormingusse.</span><span class="sxs-lookup"><span data-stu-id="677a4-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="677a4-132">Lehel **Positiivse makse vorming** saate luua failivormingu identifikaatori ja kirjelduse.</span><span class="sxs-lookup"><span data-stu-id="677a4-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="677a4-133">Teisenduse sisendvormingu tüüp peab olema XML.</span><span class="sxs-lookup"><span data-stu-id="677a4-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="677a4-134">Konkreetne vorming oleneb kasutatavast teisendusfailist.</span><span class="sxs-lookup"><span data-stu-id="677a4-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="677a4-135">Näiteks näidisena kasutatav laiendatava vormingukeele teisenduse (Extensible Stylesheet Language Transformations – XSLT) fail kasutab vormingut **XML-element**.</span><span class="sxs-lookup"><span data-stu-id="677a4-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="677a4-136">Kasutage toimingut **Laadi teisenduse puhul kasutatav fail üles** teisendusfaili asukoha määramiseks teie panga nõutava vormingu jaoks.</span><span class="sxs-lookup"><span data-stu-id="677a4-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="677a4-137">Näide: XSLT-fail positiivse makse faili puhul</span><span class="sxs-lookup"><span data-stu-id="677a4-137">Example: XSLT file for positive pay file</span></span>

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="677a4-138">Positiivse maksevormingu määramine pangakontole</span><span class="sxs-lookup"><span data-stu-id="677a4-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="677a4-139">Iga pangakonto puhul, millele soovite positiivset makseteavet luua, tuleb määrata eelmises osas kirjeldatud positiivse makse vorming.</span><span class="sxs-lookup"><span data-stu-id="677a4-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="677a4-140">Valige lehelt **Pangakontod** arvele vastav positiivse makse vorming.</span><span class="sxs-lookup"><span data-stu-id="677a4-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="677a4-141">Sisestage väljale **Positiivse makse alguskuupäev** esimene kuupäev positiivse makse failide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="677a4-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="677a4-142">On tähtis, et sisestaksite sellele väljale kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="677a4-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="677a4-143">Vastasel korral lisatakse kõik selle pangakonto puhul kunagi loodud tšekid esimesse positiivse makse faili, mille loote.</span><span class="sxs-lookup"><span data-stu-id="677a4-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="677a4-144">Numbriseeria määramine positiivse makse failidele</span><span class="sxs-lookup"><span data-stu-id="677a4-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="677a4-145">Igal positiivse makse failil peab olema kordumatu number.</span><span class="sxs-lookup"><span data-stu-id="677a4-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="677a4-146">Kasutage vahekaarti **Numbriseeriad** lehel **Sularaha- ja pangahalduse parameetrid** positiivse makse failidele numbriseeria loomiseks.</span><span class="sxs-lookup"><span data-stu-id="677a4-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="677a4-147">Ühe pangakonto jaoks positiivse makse faili loomine</span><span class="sxs-lookup"><span data-stu-id="677a4-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="677a4-148">Saate luua positiivse makse faili üksikule juriidilisele isikule ja üksikule pangakontole.</span><span class="sxs-lookup"><span data-stu-id="677a4-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="677a4-149">Teavet positiivse makse failide loomise kohta korraga mitmele juriidilisele isikule ja pangakontole leiate järgmisest osast.</span><span class="sxs-lookup"><span data-stu-id="677a4-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="677a4-150">Positiivse maksefaili loomiseks ühele juriidilisele isikule ja ühele pangakontole avage dialoogiboks **Positiivse maksefaili loomine** lehelt **Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="677a4-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="677a4-151">Sisestage väljale **Katkestuskuupäev** viimase tšeki kuupäev, et lisada see positiivsele maksefailile.</span><span class="sxs-lookup"><span data-stu-id="677a4-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="677a4-152">Kõik tšekid, mida ei ole lisatud positiivsele maksefailile selle tšeki kuupäeva lõpuks, lisatakse faili.</span><span class="sxs-lookup"><span data-stu-id="677a4-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="677a4-153">Mitme pangakonto jaoks positiivse makse faili loomine</span><span class="sxs-lookup"><span data-stu-id="677a4-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="677a4-154">Positiivse maksefaili loomiseks mitme pangakonto jaoks kasutage perioodilist toimingut **Loo positiivne maksefail**.</span><span class="sxs-lookup"><span data-stu-id="677a4-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="677a4-155">Valige failile positiivne maksevorming ja määrake, kas luua fail kõikidele juriidilistele isikutele või valitud juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="677a4-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="677a4-156">Saate luua positiivse maksefaili ka kõikidele pangakontodele, mis kasutavad positiivset maksevormingut, või valitud pangakontole.</span><span class="sxs-lookup"><span data-stu-id="677a4-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="677a4-157">Sisestage väljale **Katkestuskuupäev** viimase tšeki kuupäev, et lisada see positiivsele maksefailile.</span><span class="sxs-lookup"><span data-stu-id="677a4-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="677a4-158">Kõik tšekid, mida ei ole lisatud positiivsele maksefailile selle tšeki kuupäeva lõpuks, lisatakse faili.</span><span class="sxs-lookup"><span data-stu-id="677a4-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="677a4-159">Positiivse maksefaili loomise tulemuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="677a4-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="677a4-160">Pärast seda, kui positiivne maksefail on loodud, saate vaadata tulemusi lehel **Positiivse maksefaili kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="677a4-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="677a4-161">Eraldi tšekkide andmete vaatamiseks kasutage üksikasjalehte **Positiivne maksefail**.</span><span class="sxs-lookup"><span data-stu-id="677a4-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="677a4-162">Positiivse maksefaili kinnitamine</span><span class="sxs-lookup"><span data-stu-id="677a4-162">Confirm a positive pay file</span></span>
<span data-ttu-id="677a4-163">Kui positiivses maksefailis loetletud tšekid on tasutud, saate pangast kinnituskoodi.</span><span class="sxs-lookup"><span data-stu-id="677a4-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="677a4-164">Seejärel saate positiivse maksefaili kinnitada.</span><span class="sxs-lookup"><span data-stu-id="677a4-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="677a4-165">Valige lehelt **Positiivse maksefaili kokkuvõte** positiivne maksefail, mille olek on **Loodud**, ja valige siis toiming **Sisesta kinnitus**.</span><span class="sxs-lookup"><span data-stu-id="677a4-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="677a4-166">Positiivse maksefaili kinnitamisel salvestatakse pangast saadud kinnituskood.</span><span class="sxs-lookup"><span data-stu-id="677a4-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="677a4-167">Positiivse makse faili tagasikutsumine</span><span class="sxs-lookup"><span data-stu-id="677a4-167">Recall a positive pay file</span></span>
<span data-ttu-id="677a4-168">Kui peate positiivse makse faili muutma, saate selle tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="677a4-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="677a4-169">Valige lehelt **Positiivse maksefaili kokkuvõte** positiivne maksefail, mille olek on **Loodud**, ja valige siis toiming **Võta tagasi**.</span><span class="sxs-lookup"><span data-stu-id="677a4-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="677a4-170">Igas positiivse makse failis oleva tšeki puhul lähtestatakse väli, mis näitab, kas see tšekk on olnud positiivse makse faili lisatud.</span><span class="sxs-lookup"><span data-stu-id="677a4-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="677a4-171">Siis saate luua uue positiivse maksefaili, mis sisaldab tagasi võetud tšekki.</span><span class="sxs-lookup"><span data-stu-id="677a4-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>



