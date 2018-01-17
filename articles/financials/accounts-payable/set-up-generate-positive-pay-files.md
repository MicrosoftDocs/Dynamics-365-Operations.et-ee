---
title: Positiivse makse failide seadistamine ja loomine
description: See artikkel selgitab, kuidas positiivset makset seadistada ja positiivse makse faile luua.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: cb5a674472936a52b624c548fd37079d57eb6cb7
ms.openlocfilehash: 9a36b3e7a8e496632ca7041018abe8176a2e4f25
ms.contentlocale: et-ee
ms.lasthandoff: 12/14/2017

---

# <a name="set-up-and-generate-positive-pay-files"></a>Positiivse makse failide seadistamine ja loomine

[!include[banner](../includes/banner.md)]


See artikkel selgitab, kuidas positiivset makset seadistada ja positiivse makse faile luua. 

Positiivse makse seadistamine pangale edastatava elektroonilise tšekkide loendi loomiseks. Tšeki esitamisel pangale võrdleb pank seda tšekkide loendiga. Kui tšekk vastab loendis olevale tšekile, maksab pank selle välja. Kui tšekk ei vasta ühelegi loendis olevale tšekile, võtab pank selle ülevaatamiseks enda kätte.

## <a name="security-for-positive-pay-files"></a>Positiivse makse failide turve
Positiivse makse failides võib olla tundliku loomuga teavet maksesaajate ja tšekisummade kohta. Seetõttu kasutage kindlasti vajalikke turvameetmeid alates failide loomise hetkest kuni nende panka saabumiseni. Positiivse makse failid laaditakse alla teie veebibrauseri määratud asukohta. Kuna positiivsed maksefailid saavad sisaldada tundlikku teavet, on oluline, et ainult volitatud kasutajatel on rakenduses Microsoft Dynamics 365 for Finance and Operations, Enterprise edition juurdepääs selle teabe loomiseks ja vaatamiseks. Järgmise tabelis abil saate määratleda vajalikke õigusi.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Ülesanne</th>
<th>Eesõigus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Saate luua positiivse makse faile loendilehelt <strong>Pangakontod</strong> või lehelt <strong>Pangakontod</strong>.</td>
<td><ul>
<li><strong>Panga positiivse makse teabe haldamine</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Positiivse makse failide loomine juriidiliste isikute ning pangakontode jaoks lehelt <strong>Loo positiivne maksefail</strong>.</td>
<td><ul>
<li><strong>Panga positiivse makse teabe haldamine</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Positiivseid maksefaile saab vaadata lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</td>
<td><strong>Vaata panga positiivset makseteavet mitme juriidilise isiku kohta</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Positiivse maksefaili saab kinnitada lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</td>
<td><strong>Kinnita positiivne maksefail</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Positiivse maksefaili saab tagasi võtta lehelt <strong>Positiivse maksefaili kokkuvõte</strong>.</td>
<td><strong>Positiivse makse faili tagasivõtmine</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Positiivse maksevormingu seadistamine
Positiivse makse failid luuakse andmeüksuste abil. Enne positiivse maksefaili loomist peate seadistama teisendamise sisendvormingu, mida kasutatakse tšeki teabe teisendamiseks pangale sobivasse vormingusse. Lehel **Positiivse makse vorming** saate luua failivormingu identifikaatori ja kirjelduse. Teisenduse sisendvormingu tüüp peab olema XML. Konkreetne vorming oleneb kasutatavast teisendusfailist. Näiteks näidisena kasutatav laiendatava vormingukeele teisenduse (Extensible Stylesheet Language Transformations – XSLT) fail kasutab vormingut **XML-element**. Kasutage toimingut **Laadi teisenduse puhul kasutatav fail üles** teisendusfaili asukoha määramiseks teie panga nõutava vormingu jaoks.

## <a name="example-xslt-file-for-positive-pay-file"></a>Näide: XSLT-fail positiivse makse faili puhul
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
          <xsl:for-each select="Document/BankPositivePayExportEntity">
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Positiivse maksevormingu määramine pangakontole
Iga pangakonto puhul, millele soovite positiivset makseteavet luua, tuleb määrata eelmises osas kirjeldatud positiivse makse vorming. Valige lehelt **Pangakontod** arvele vastav positiivse makse vorming. Sisestage väljale **Positiivse makse alguskuupäev** esimene kuupäev positiivse makse failide loomiseks. On tähtis, et sisestaksite sellele väljale kuupäeva. Vastasel korral lisatakse kõik selle pangakonto puhul kunagi loodud tšekid esimesse positiivse makse faili, mille loote.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Numbriseeria määramine positiivse makse failidele
Igal positiivse makse failil peab olema kordumatu number. Kasutage vahekaarti **Numbriseeriad** lehel **Sularaha- ja pangahalduse parameetrid** positiivse makse failidele numbriseeria loomiseks.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Ühe pangakonto jaoks positiivse makse faili loomine
Saate luua positiivse makse faili üksikule juriidilisele isikule ja üksikule pangakontole. Teavet positiivse makse failide loomise kohta korraga mitmele juriidilisele isikule ja pangakontole leiate järgmisest osast. Positiivse maksefaili loomiseks ühele juriidilisele isikule ja ühele pangakontole avage dialoogiboks **Positiivse maksefaili loomine** lehelt **Pangakontod**. Sisestage väljale **Katkestuskuupäev** viimase tšeki kuupäev, et lisada see positiivsele maksefailile. Kõik tšekid, mida ei ole lisatud positiivsele maksefailile selle tšeki kuupäeva lõpuks, lisatakse faili.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Mitme pangakonto jaoks positiivse makse faili loomine
Positiivse maksefaili loomiseks mitme pangakonto jaoks kasutage perioodilist toimingut **Loo positiivne maksefail**. Valige failile positiivne maksevorming ja määrake, kas luua fail kõikidele juriidilistele isikutele või valitud juriidilisele isikule. Saate luua positiivse maksefaili ka kõikidele pangakontodele, mis kasutavad positiivset maksevormingut, või valitud pangakontole. Sisestage väljale **Katkestuskuupäev** viimase tšeki kuupäev, et lisada see positiivsele maksefailile. Kõik tšekid, mida ei ole lisatud positiivsele maksefailile selle tšeki kuupäeva lõpuks, lisatakse faili.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Positiivse maksefaili loomise tulemuste vaatamine
Pärast seda, kui positiivne maksefail on loodud, saate vaadata tulemusi lehel **Positiivse maksefaili kokkuvõte**. Eraldi tšekkide andmete vaatamiseks kasutage üksikasjalehte **Positiivne maksefail**.

## <a name="confirm-a-positive-pay-file"></a>Positiivse maksefaili kinnitamine
Kui positiivses maksefailis loetletud tšekid on tasutud, saate pangast kinnituskoodi. Seejärel saate positiivse maksefaili kinnitada. Valige lehelt **Positiivse maksefaili kokkuvõte** positiivne maksefail, mille olek on **Loodud**, ja valige siis toiming **Sisesta kinnitus**. Positiivse maksefaili kinnitamisel salvestatakse pangast saadud kinnituskood.

## <a name="recall-a-positive-pay-file"></a>Positiivse makse faili tagasikutsumine
Kui peate positiivse makse faili muutma, saate selle tagasi kutsuda. Valige lehelt **Positiivse maksefaili kokkuvõte** positiivne maksefail, mille olek on **Loodud**, ja valige siis toiming **Võta tagasi**. Igas positiivse makse failis oleva tšeki puhul lähtestatakse väli, mis näitab, kas see tšekk on olnud positiivse makse faili lisatud. Siis saate luua uue positiivse maksefaili, mis sisaldab tagasi võetud tšekki.




