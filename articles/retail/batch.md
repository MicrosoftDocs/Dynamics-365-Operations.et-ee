<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="batch.md" target-language="et-EE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>batch.e70006.4456fc3d5bc4547fa8211642b11ca6df455fa187.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4456fc3d5bc4547fa8211642b11ca6df455fa187</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>aec1dcd44274e9b8d0770836598fde5533b7b569</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/03/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\batch.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Improved handling of batch-tracked items</source><target logoport:matchpercent="0" state="translated">Partii jälgimisega kaupade täiustatud käsitlemine</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the improvements that have been made to the handling of batches for batch-tracked items during the Retail statement posting process.</source><target logoport:matchpercent="0" state="translated">Selles teemas kirjeldatakse täiustusi, mis on tehtud jaemüügiväljavõtete sisestamisprotsessi käigus partii jälgimisega kaupade partiide käsitlemisele.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Improved handling of batch-tracked items</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Partii jälgimisega kaupade täiustatud käsitlemine</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>In Microsoft Dynamics 365 for Retail Point of Sale (POS), batch numbers can't be captured for batch-tracked items at the time of sale.</source><target logoport:matchpercent="0" state="translated">Microsoft Dynamics 365 for Retaili kassas (POS) ei saa partiinumbreid partii jälgimisega kaupade puhul müügi hetkel jäädvustada.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>However, for specific configurations, when sales are posted in the headquarters through customer orders or statement posting, the Microsoft Dynamics system expects that valid batch numbers for batch-tracked items exist, and that they will be used during the invoicing process.</source><target logoport:matchpercent="0" state="translated">Kui müügiandmed sisestatakse peakontoris klienditellimuste või väljavõtete sisestuse käigus, siis eeldab süsteem Microsoft Dynamics teatud konfiguratsioonide korral, et partii jälgimisega kaupade jaoks on olemas sobivad partiinumbrid ja neid kasutatakse arveldusprotsessis.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>If valid batch numbers are available for products, the customer order invoicing process and the sales order invoicing process from statement posting use them.</source><target logoport:matchpercent="0" state="translated">Kui toodete jaoks on saadaval sobivad partiinumbrid, kasutavad väljavõtete sisestamise käigus toimuv klienditellimuste arveldamise protsess ja müügitellimuste arveldamise protsess neid partiinumbreid.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Otherwise, the customer order invoicing process can't post, and the POS user receives an error message.</source><target logoport:matchpercent="0" state="translated">Vastasel korral ei saa klienditellimuste arveldamise protsess andmeid sisestada ja kassa kasutaja saab tõrketeate.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Statement posting then goes into an error state.</source><target logoport:matchpercent="0" state="translated">Väljavõtete sisestus läheb siis tõrkeolekusse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This error state occurs even when negative inventory has been turned on for the products.</source><target logoport:matchpercent="0" state="translated">See tõrkeolek ilmneb ka siis, kui negatiivsed varud on toodete jaoks sisse lülitatud.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Improvements that have been made in Microsoft Dynamics for Retail version 10.0.4 and later help guarantee that, when negative inventory is turned on for batch-tracked items, customer order invoicing and sales order invoicing through statement posting aren't blocked for those items if the inventory is 0 (zero) or a batch number isn't available.</source><target logoport:matchpercent="0" state="translated">Microsoft Dynamics for Retaili versioonis 10.0.4 ja uuemas versioonis tehtud täiustused aitavad tagada, et kui partii jälgimisega kaupade jaoks on sisse lülitatud negatiivsed varud, ei blokeerita nende kaupade puhul väljavõtete sisestuse kaudu toimuvat klienditellimuste arveldust ega müügitellimuste arveldust, kui varude väärtus on 0 (null) või partiinumber pole saadaval.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The new functionality uses a default batch ID for the sales lines when batch numbers aren't available.</source><target logoport:matchpercent="0" state="translated">Kui partiinumbrid pole saadaval, kasutab see uus funktsioon müügiridade jaoks partii vaike-ID-d.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>To define the default batch ID that is used for customer orders, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Customer orders<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Order<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="0" state="translated">Klienditellimuste jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe <bpt id="p1">**</bpt>Jaemüügi parameetrid<ept id="p1">**</ept> vahekaardi <bpt id="p2">**</bpt>Kliendi tellimused<ept id="p2">**</ept> kiirkaardil <bpt id="p3">**</bpt>Tellimus<ept id="p3">**</ept> väli <bpt id="p4">**</bpt>Vaikimisi partii ID<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>To define the default batch ID that is used for sales order invoicing through statement posting, on the <bpt id="p1">**</bpt>Retail parameters<ept id="p1">**</ept> page, on the <bpt id="p2">**</bpt>Posting<ept id="p2">**</ept> tab, on the <bpt id="p3">**</bpt>Inventory update<ept id="p3">**</ept> FastTab, set the <bpt id="p4">**</bpt>Default batch id<ept id="p4">**</ept> field.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Väljavõtete sisestamise kaudu tehtava müügitellimuste arvelduse jaoks kasutatava partii vaike-ID määratlemiseks määrake lehe <bpt id="p1">**</bpt>Jaemüügi parameetrid<ept id="p1">**</ept> vahekaardi <bpt id="p2">**</bpt>Sisestamine<ept id="p2">**</ept> kiirkaardil <bpt id="p3">**</bpt>Laoseisu uuendamine<ept id="p3">**</ept> väli <bpt id="p4">**</bpt>Vaikimisi partii ID<ept id="p4">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This functionality is available only when advanced warehousing is turned on for the specific store warehouse and items.</source><target logoport:matchpercent="0" state="translated">See funktsioon on saadaval ainult juhul, kui konkreetse kaupluse lao ja kaupade jaoks on sisse lülitatud täpsem laohaldus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In a later release, the functionality will also be supported for scenarios where advanced warehouse management isn't used.</source><target logoport:matchpercent="0" state="translated">Uuemas versioonis toetatakse funktsiooni ka selliste stsenaariumite puhul, kus täpsemat laohaldust ei kasutata.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>