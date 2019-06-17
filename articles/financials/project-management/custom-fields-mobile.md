<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="custom-fields-mobile.md" target-language="et-EE">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>custom-fields-mobile.2a9e5e.4343c875da05641c57b7784bf52f1c814dd26d20.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4343c875da05641c57b7784bf52f1c814dd26d20</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>19859d8566a8c7840066b2c10c6b08b67f1b83f4</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/04/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\financials\project-management\custom-fields-mobile.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source><target logoport:matchpercent="0" state="translated">Kohandatud väljade juurutamine mobiilirakenduses Microsoft Dynamics 365 Project Timesheet iOS-is ja Androidis</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source><target logoport:matchpercent="0" state="translated">Selles teemas on toodud üldised mustrid laienduste kasutamiseks kohandatud väljade juurutamiseks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Kohandatud väljade juurutamine mobiilirakenduses Microsoft Dynamics 365 Project Timesheet iOS-is ja Androidis</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides common patterns for using extensions to implement custom fields.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Selles teemas on toodud üldised mustrid laienduste kasutamiseks kohandatud väljade juurutamiseks.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The following topics are covered:</source><target logoport:matchpercent="80" state="translated" state-qualifier="x-fuzzy-match-unedited">Hõlmab järgmisi teemasid.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The various data types that the custom field framework supports</source><target logoport:matchpercent="0" state="translated">Mitmesugused andmetüübid, mida kohandatud välja raamistik toetab</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</source><target logoport:matchpercent="0" state="translated">Kirjutuskaitstud või redigeeritavate väljade kuvamine ajatabeli kannetel ja kasutaja esitatud väärtuste salvestamine andmebaasi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>How to show read-only fields on the timesheet header</source><target logoport:matchpercent="0" state="translated">Kirjutuskaitstud väljade kuvamine ajatabeli päises</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>How to integrate other custom business logic to enter default values in fields and do additional validation</source><target logoport:matchpercent="0" state="translated">Kohandatud äriloogika integreerimine vaikeväärtuste sisestamiseks väljadesse ja lisakinnituse tegemiseks</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Audience</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Sihtrühm</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</source><target logoport:matchpercent="0" state="translated">See teema on mõeldud arendajatele, kes integreerivad kohandatud välju mobiilirakendusse Microsoft Dynamics 365 Project Timesheet, mis on saadaval Apple iOS-is ja Google Androidis.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The assumption is that readers are familiar with X++ development and project timesheet functionality.</source><target logoport:matchpercent="0" state="translated">Eelduseks on, et lugejad on tuttavad X++ arendusega ja projekti ajatabeli funktsiooniga.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Data contract – TSTimesheetCustomField X++ class</source><target logoport:matchpercent="0" state="translated">Andmeleping – klass TSTimesheetCustomField X++</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>The <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> class is the X++ data contract class that represents information about a custom field for timesheet functionality.</source><target logoport:matchpercent="0" state="translated">Klass <bpt id="p1">**</bpt>TSTimesheetCustomField<ept id="p1">**</ept> X++ andmelepingu klass, mis esitavad teavet ajatabeli funktsiooni kohandatud välja kohta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</source><target logoport:matchpercent="0" state="translated">Kohandatud välja objektide loendid edastatakse nii andmelepingusse TSTimesheetDetails kui ka andmelepingusse TSTimesheetEntry, et kuvada kohandatud väljad mobiilirakenduses.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> - The timesheet header contract.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetDetails<ept id="p1">**</ept> – ajatabeli päise leping.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> - The timesheet transaction contract.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSTimesheetEntry<ept id="p1">**</ept> – ajatabeli kande leping.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Groups of these objects that have the same project information and <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> value constitute a line.</source><target logoport:matchpercent="0" state="translated">Nende objektide grupid, millel sama projekti teave ja väärtus <bpt id="p1">**</bpt>timesheetLineRecId<ept id="p1">**</ept> moodustab rea.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>fieldBaseType (Types)</source><target logoport:matchpercent="0" state="translated">fieldBaseType (tüübid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> property on the <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> object determines the type of the field that appears in the app.</source><target logoport:matchpercent="0" state="translated">Atribuut <bpt id="p1">**</bpt>FieldBaseType<ept id="p1">**</ept> objektis <bpt id="p2">**</bpt>TsTimesheetCustom<ept id="p2">**</ept> määrab rakenduses kuvatava välja tüübi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The following <bpt id="p1">**</bpt>Types<ept id="p1">**</ept> values that are supported.</source><target logoport:matchpercent="0" state="translated">Järgmisi suvandi <bpt id="p1">**</bpt>Tüübid<ept id="p1">**</ept> väärtusi toetatakse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Types value</source><target logoport:matchpercent="0" state="translated">Tüübi väärtus</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Type</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tüüp</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Notes</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Märkmed</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>0</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>String (and Enum)</source><target logoport:matchpercent="0" state="translated">String (ja loetelu)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The field appears as a text field.</source><target logoport:matchpercent="0" state="translated">Väli kuvatakse tekstiväljana.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>1</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Integer</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Täisarv</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The value is shown as a number without decimal places.</source><target logoport:matchpercent="0" state="translated">Väärtus kuvatakse numbrina ilma komakohtadeta.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>2</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">2</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Real</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Tegelik</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The value is shown as a number that has decimal places.</source><target logoport:matchpercent="84" state="translated" state-qualifier="fuzzy-match">Väärtus kuvatakse numbrina koos komakohtadega.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To show the real value as a currency in the app, use the <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept> property.</source><target logoport:matchpercent="0" state="translated">Tegeliku väärtuse kuvamiseks rakenduses valuutana kasutage atribuuti <bpt id="p1">**</bpt>fieldExtenededType<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>You can use the <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> property to set the number of decimal places that are shown.</source><target logoport:matchpercent="0" state="translated">Saate kasutada atribuuti <bpt id="p1">**</bpt>numberOfDecimals<ept id="p1">**</ept> kuvatavate komakohtade arvu määramiseks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>3</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">3</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Date</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kuupäev</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Date formats are determined by the user's <bpt id="p1">**</bpt>Date, times, and number format<ept id="p1">**</ept> setting that is specified under <bpt id="p2">**</bpt>Language and country/region preference<ept id="p2">**</ept> in <bpt id="p3">**</bpt>User options<ept id="p3">**</ept>.</source><target logoport:matchpercent="0" state="translated">Kuupäevavormingud määrab kasutaja säte <bpt id="p1">**</bpt>Kuupäeva, kellaaja ja numbri vorming<ept id="p1">**</ept>, mis on määratud valikuga <bpt id="p2">**</bpt>Keele ja riigi/regiooni eelistused<ept id="p2">**</ept> jaotises <bpt id="p3">**</bpt>Kasutaja suvandid<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>4</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">4</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Boolean</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Kahendmuutuja</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>15</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">15</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>GUID</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">GUID</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>16</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">16</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Int64</source><target logoport:matchpercent="0" state="translated">Int64</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property isn't provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, a free-text field is provided to the user.</source><target logoport:matchpercent="0" state="translated">Kui atribuuti <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> pole objektis <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept>, esitatakse kasutajale vabas vormis teksti väli.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> property can be used to set the maximum string length that users can enter.</source><target logoport:matchpercent="0" state="translated">Atribuuti <bpt id="p1">**</bpt>stringLength<ept id="p1">**</ept> saab kasutada kasutaja sisestatava stringi maksimaalse pikkuse määramiseks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>If the <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> property is provided on the <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept> object, those list elements are the only values that users can select by using option buttons (radio buttons).</source><target logoport:matchpercent="0" state="translated">Kui atribuuti <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> pole objektis <bpt id="p2">**</bpt>TSTimesheetCustomField<ept id="p2">**</ept>, on need loendi elemendid ainsad väärtused, mida kasutajad saavad suvandi nuppudega (raadionuppudega) valida.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In this case, the string field can act as an enum value for the purpose of user entry.</source><target logoport:matchpercent="0" state="translated">Sellisel juhul võib stringiväli toimida loetelu väärtusena kasutaja kirje jaoks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="0" state="translated">Väärtuse salvestamiseks andmebaasi loeteluna vastendage enne andmebaasi salvestamist stringiväärtus käsitsi loetelu väärtusega, kasutades käsuliini (vt näidet allpool selle teema jaotises „Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi”).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>fieldExtendedType (TSCustomFieldExtendedType)</source><target logoport:matchpercent="0" state="translated">fieldExtendedType (TSCustomFieldExtendedType)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>You can use this property to format real values as currency.</source><target logoport:matchpercent="0" state="translated">Seda atribuuti saate kasutada tegelike väärtuste vormindamiseks valuutana.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This approach is applicable only when the <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> value is <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">See lähenemine on rakendatav ainult siis, kui väärtus <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> on <bpt id="p2">**</bpt>Tegelik<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – No formatting is applied.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType:None<ept id="p1">**</ept> – vormindamist ei rakendata.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Currency<ept id="p1">**</ept> – Format the value as currency.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldExtendedType::Valuuta<ept id="p1">**</ept> – väärtus vormindatakse valuutana.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>When currency formatting is active, the <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> field can be used pass the currency code that should be shown in the app.</source><target logoport:matchpercent="0" state="translated">Kui valuuta vormindamine on aktiivne, saab välja <bpt id="p1">**</bpt>stringValue<ept id="p1">**</ept> kasutada valuutakoodi edastamiseks, mis tuleb rakenduses kuvada.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The value is a read-only value.</source><target logoport:matchpercent="0" state="translated">Väärtus on kirjutuskaitstud väärtus.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> field contains the money amount that should be saved to the database.</source><target logoport:matchpercent="0" state="translated">Väli <bpt id="p1">**</bpt>realValue<ept id="p1">**</ept> sisaldab rahasummat, mis tuleb andmebaasi salvestada.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>fieldSection (TSCustomFieldSection)</source><target logoport:matchpercent="0" state="translated">fieldSection (TSCustomFieldSection)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>You can use this property specify where the custom field should appear in the app.</source><target logoport:matchpercent="0" state="translated">Saate kasutada seda atribuuti, et määrata, kus peaks kohandatud väli rakenduses ilmuma.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Header<ept id="p1">**</ept> – The field will appear in the <bpt id="p2">**</bpt>View more details<ept id="p2">**</ept> section in the app.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Päis<ept id="p1">**</ept> – väli kuvatakse rakenduses jaotises <bpt id="p2">**</bpt>Kuva rohkem üksikasju<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>These fields are always read-only.</source><target logoport:matchpercent="83" state="translated" state-qualifier="fuzzy-match">Need väljad on alati kirjutuskaitstud.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><bpt id="p1">**</bpt>TSCustomFieldSection::Line<ept id="p1">**</ept> – The field will appear after all the out-of-box line fields on timesheet entries.</source><target logoport:matchpercent="0" state="translated"><bpt id="p1">**</bpt>TSCustomFieldSection::Rida<ept id="p1">**</ept> – väli kuvatakse kõikide valmis reaväljade järel ajatabeli kannetes.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>These fields can be either editable or read-only.</source><target logoport:matchpercent="0" state="translated">Need väljad võivad olla redigeeritavad või kirjutuskaitstud.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>fieldName (FieldNameShort)</source><target logoport:matchpercent="0" state="translated">fieldName (FieldNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source><target logoport:matchpercent="0" state="translated">See atribuut tuvastab välja, kui rakenduse esitatud väärtused salvestatakse tagasi andmebaasi.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>tableName (TableNameShort)</source><target logoport:matchpercent="0" state="translated">tableName (TableNameShort)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This property identifies the field when values that the app provides are saved back to the database.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">See atribuut tuvastab välja, kui rakenduse esitatud väärtused salvestatakse tagasi andmebaasi.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>isEditable (NoYes)</source><target logoport:matchpercent="0" state="translated">isEditable (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be editable by users.</source><target logoport:matchpercent="0" state="translated">Määrake see atribuut väärtusele <bpt id="p1">**</bpt>Jah<ept id="p1">**</ept>, et määrata, kas välja ajatabeli kande jaotises saavad kasutajad redigeerida.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Set the property to <bpt id="p1">**</bpt>No<ept id="p1">**</ept> to make the field read-only.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">Määrake atribuudi väärtuseks <bpt id="p1">**</bpt>Ei<ept id="p1">**</ept>, et muuta väli kirjutuskaitstuks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>isMandatory (NoYes)</source><target logoport:matchpercent="0" state="translated">isMandatory (NoYes)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Set this property to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept> to specify that the field in the timesheet entry section should be mandatory.</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">Määrake see atribuut väärtusele <bpt id="p1">**</bpt>Jah<ept id="p1">**</ept>, et määrata, kas väli ajatabeli kande jaotises peaks olema kohustuslik.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>label (str)</source><target logoport:matchpercent="0" state="translated">label (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>This property specifies the label that is shown next the field in the app.</source><target logoport:matchpercent="0" state="translated">See atribuut määrab sildi, mis kuvatakse rakenduses välja kõrval.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>stringOptions (List of Strings)</source><target logoport:matchpercent="0" state="translated">stringOptions (List of Strings)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This property is applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="0" state="translated">See atribuut on rakendatav ainult siis, kui <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> on seatud väärtusele <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>If <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept> is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</source><target logoport:matchpercent="0" state="translated">Kui määratud on <bpt id="p1">**</bpt>stringOptions<ept id="p1">**</ept>, määratakse loendis olevate stringidega määratud suvandi nuppudega (raadionuppudega) valitavad stringiväärtused.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</source><target logoport:matchpercent="0" state="translated">Kui ühtegi stringi pole olemas, lubatakse stringiväljas vabas vormis teksti kanne (vt näidet allpool selle teema jaotises „„Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi”).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>stringLength (int)</source><target logoport:matchpercent="0" state="translated">stringLength (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This property specifies the maximum length for a string field.</source><target logoport:matchpercent="0" state="translated">See atribuut määrab stringivälja maksimaalse pikkuse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">See on rakendatav ainult siis, kui <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> on seatud väärtusele <bpt id="p2">**</bpt>String<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>numberOfDecimals (int)</source><target logoport:matchpercent="0" state="translated">numberOfDecimals (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property specifies the number of decimal places that are shown for a real field.</source><target logoport:matchpercent="0" state="translated">See atribuut määrab komakohtade arvu, mida tegeliku välja kohta näidatakse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>It's applicable only when <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> is set to <bpt id="p2">**</bpt>Real<ept id="p2">**</ept>.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">See on rakendatav ainult siis, kui <bpt id="p1">**</bpt>fieldBaseType<ept id="p1">**</ept> on seatud väärtusele <bpt id="p2">**</bpt>Tegelik<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>orderSequence (int)</source><target logoport:matchpercent="0" state="translated">orderSequence (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</source><target logoport:matchpercent="0" state="translated">See atribuut reguleerib järjekorda, milles kohandatud välju rakenduses kuvatakse, kui määratud on rohkem kui üks kohandatud väli.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Fields that have lower numbers are shown first.</source><target logoport:matchpercent="0" state="translated">Pikemate arvudega väljad kuvatakse enne.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>booleanValue (boolean)</source><target logoport:matchpercent="0" state="translated">booleanValue (boolean)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For fields of the <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> type, this property passes the Boolean value of the field between the server and the app.</source><target logoport:matchpercent="0" state="translated">Tüübi <bpt id="p1">**</bpt>Boolean<ept id="p1">**</ept> väljade jaoks saadab see atribuut välja Booleani väärtust serveri ja rakenduse vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>guidValue (guid)</source><target logoport:matchpercent="0" state="translated">guidValue (guid)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>For fields of the <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</source><target logoport:matchpercent="81" state="translated" state-qualifier="fuzzy-match">Tüübi <bpt id="p1">**</bpt>GUID<ept id="p1">**</ept> väljade jaoks saadab see atribuut välja globaalse ainuidentifikaatori (GUID) väärtust serveri ja rakenduse vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>int64Value (int64)</source><target logoport:matchpercent="0" state="translated">int64Value (int64)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>For fields of the <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> type, this property passes the int64 value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Tüübi <bpt id="p1">**</bpt>Int64<ept id="p1">**</ept> väljade jaoks saadab see atribuut välja int64 väärtust serveri ja rakenduse vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>intValue (int)</source><target logoport:matchpercent="0" state="translated">intValue (int)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>For fields of the <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> type, this property passes the int value of the field between the server and the app.</source><target logoport:matchpercent="92" state="translated" state-qualifier="fuzzy-match">Tüübi <bpt id="p1">**</bpt>Int<ept id="p1">**</ept> väljade jaoks saadab see atribuut välja int väärtust serveri ja rakenduse vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>realValue (real)</source><target logoport:matchpercent="0" state="translated">realValue (real)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>For fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type, this property passes the real value of the field between the server and the app .</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Tüübi <bpt id="p1">**</bpt>Tegelik<ept id="p1">**</ept> väljade jaoks saadab see atribuut välja tegelikku väärtust serveri ja rakenduse vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>stringValue (str)</source><target logoport:matchpercent="0" state="translated">stringValue (str)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For fields of the <bpt id="p1">**</bpt>String<ept id="p1">**</ept> type, this property passes the string value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Tüübi <bpt id="p1">**</bpt>String<ept id="p1">**</ept> väljade jaoks saadab see atribuut välja stringi väärtust serveri ja rakenduse vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>It's also used for fields of the <bpt id="p1">**</bpt>Real<ept id="p1">**</ept> type that are formatted as currency.</source><target logoport:matchpercent="0" state="translated">Seda kasutatakse ka tüübi <bpt id="p1">**</bpt>Tegelik<ept id="p1">**</ept> väljade jaoks, mis on vormindatud valuutana.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>For those fields, the property is used to pass the currency code to the app.</source><target logoport:matchpercent="0" state="translated">Nende väljade jaoks kasutatakse atribuuti valuutakoodi saatmiseks rakendusse.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>dateValue (date)</source><target logoport:matchpercent="0" state="translated">dateValue (date)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>For fields of the <bpt id="p1">**</bpt>Date<ept id="p1">**</ept> type, this property passes the date value of the field between the server and the app.</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Tüübi <bpt id="p1">**</bpt>Kuupäev<ept id="p1">**</ept> väljade jaoks saadab see atribuut välja kuupäeva väärtust serveri ja rakenduse vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Show and save a custom field in the timesheet entry section</source><target logoport:matchpercent="0" state="translated">Kohandatud välja kuvamine ja salvestamine ajatabeli kande jaotises</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Below is a screenshot from the mobile app of a timesheet entry creation.</source><target logoport:matchpercent="0" state="translated">All on mobiilirakenduse kuvatõmmis ajatabeli kande loomisest.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</source><target logoport:matchpercent="0" state="translated">See näitab valmis välju ja kohandatud välja suvandi Ajakirje jaotises Kontrollstring, mille loetelu väärtus Teine suvand on juba määratud.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Test string custom field in the app</source><target logoport:matchpercent="0" state="translated">Kontrollstringi kohandatud väli rakenduses</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</source><target logoport:matchpercent="0" state="translated">All on mobiilirakenduse kuvatõmmis, kus kasutaja valib ühe loetelu suvandi, mis on saadaval kohandatud välja Kontrollstring jaoks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The two options are "First option" and "Second option" shown as radio buttons.</source><target logoport:matchpercent="0" state="translated">Need kaks suvandit, Esimene suvand ja Teine suvand, kuvatakse raadionuppudena.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The second option is currently selected.</source><target logoport:matchpercent="0" state="translated">Praegu on valitud teine suvand.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Option buttons (radio buttons) for the Test string custom field</source><target logoport:matchpercent="0" state="translated">Kontrollstringi kohandatud välja suvandi nupud (raadionupud)</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Extend the TSTimesheetLine table so that it has a custom field</source><target logoport:matchpercent="0" state="translated">Tabeli TSTimesheetLine laiendamine, nii et sellel on kohandatud väli</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</source><target logoport:matchpercent="0" state="translated">Tavalises stsenaariumis on tõenäoline, et ajatabeli kande jaotise kohandatud välja andmed salvestatakse tabelisse TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="0" state="translated">Kuid muid tabeleid saab kasutada, kui andmeid saab võtta olemasoleva kirje TSTimesheetTrans põhjal või kui sellel pole konkreetset kirje konteksti (nt kui väli on projekti parameetrites määratud kirjutuskaitstuks).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Note that custom fields don't have to have any backing database records.</source><target logoport:matchpercent="0" state="translated">Pange tähele, et kohandatud väljadel ei pea olema toetavaid andmebaasikirjeid.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>They can be dynamically generated based on X++ logic.</source><target logoport:matchpercent="0" state="translated">Neid saab dünaamiliselt luua X++ loogika põhjal.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</source><target logoport:matchpercent="0" state="translated">See lähenemine võib olla kasulik kirjutuskaitstud stsenaariumide korral (näidet dünaamiliselt loodud kohandatud välja väärtuste kohta vaadake jaotisest „Käsuliini kasutamine klassil TSTimesheetDetails, meetod buildCustomFieldListForHeader ajatabeli üksikasjade täitmiseks”).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Below is a screenshot from Visual Studio of the Application Object Tree.</source><target logoport:matchpercent="0" state="translated">All on kuvatõmmis rakendusobjektide puu rakendusest Visual Studio.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</source><target logoport:matchpercent="0" state="translated">See kuvab tabeli TSTimesheetLine laienduse, kuhu on kohandatud väljana lisatud väli TestLineString.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Line string</source><target logoport:matchpercent="0" state="translated">Reastring</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</source><target logoport:matchpercent="0" state="translated">Käsuliini kasutamine klassi TSTimesheetSettings meetodil buildCustomFieldList välja kuvamiseks ajatabeli kande jaotises</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>This code controls the display settings for the field in the app.</source><target logoport:matchpercent="0" state="translated">See kood reguleerib välja kuvasätteid rakenduses.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source><target logoport:matchpercent="0" state="translated">Näiteks reguleerib see välja tüüpi, silti, seda, kas väli on kohustuslik, ja millises jaotises väli ilmub.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>The following example shows a string field on time entries.</source><target logoport:matchpercent="0" state="translated">Järgmises näites on näha stringiväli ajakirjetel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>This field has two options, <bpt id="p1">**</bpt>First option<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Second option<ept id="p2">**</ept>, that are available via option buttons (radio buttons).</source><target logoport:matchpercent="0" state="translated">Sellel väljal on kaks suvandit, <bpt id="p1">**</bpt>Esimene suvand<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>Teine suvand<ept id="p2">**</ept>, mis on saadaval suvandi nuppude (raadionuppude) kaudu.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The field in the app is associated with the <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept> field that is added to the TSTimesheetLine table.</source><target logoport:matchpercent="0" state="translated">Väli rakenduses on seotud väljaga <bpt id="p1">**</bpt>TestLineString<ept id="p1">**</ept>, mis lisatakse tabelile TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Note the use of the <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> method to simplify the initialization of the custom field properties: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept>, and <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</source><target logoport:matchpercent="0" state="translated">Pange tähele, et kasutatud on meetodit <bpt id="p1">**</bpt>TSTimesheetCustomField::newFromMetatdata()<ept id="p1">**</ept> kohandatud välja atribuutide lähtestamise lihtsustamiseks: <bpt id="p2">**</bpt>fieldBaseType<ept id="p2">**</ept>, <bpt id="p3">**</bpt>tableName<ept id="p3">**</ept>, <bpt id="p4">**</bpt>fieldname<ept id="p4">**</ept>, <bpt id="p5">**</bpt>label<ept id="p5">**</ept>, <bpt id="p6">**</bpt>isEditable<ept id="p6">**</ept>, <bpt id="p7">**</bpt>isMandatory<ept id="p7">**</ept>, <bpt id="p8">**</bpt>stringLength<ept id="p8">**</ept> ja <bpt id="p9">**</bpt>numberOfDecimals<ept id="p9">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>You can also set these parameters manually, as you prefer.</source><target logoport:matchpercent="0" state="translated">Saate neid parameetreid ka eelistuste järgi käsitsi seadistada.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Käsuliini kasutamine klassi TSTimesheetEntry meetodil buildCustomFieldListForEntry väärtuste sisestamiseks ajatabeli kandesse</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> method is used to enter values on the saved timesheet lines in the mobile app.</source><target logoport:matchpercent="0" state="translated">Meetodit <bpt id="p1">**</bpt>buildCustomFieldListForEntry<ept id="p1">**</ept> kasutatakse väärtuste sisestamiseks salvestatud ajatabeli ridadele mobiilirakenduses.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>It takes a TSTimesheetTrans record as a parameter.</source><target logoport:matchpercent="0" state="translated">See kasutab kirjet TSTimesheetTrans parameetrina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source><target logoport:matchpercent="0" state="translated">Välju sellest kirjest saab kasutada kohandatud välja väärtuse täitmiseks rakenduses.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</source><target logoport:matchpercent="0" state="translated">Käsuliini kasutamine klassil TSTimesheetEntryService ajatabeli kande salvestamiseks rakendusest tagasi andmebaasi</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>To save a custom field back to the database in typical usage, you must extend multiple methods:</source><target logoport:matchpercent="0" state="translated">Kohandatud välja salvestamiseks tagasi andmebaasi tavakasutuse korral peate laiendama mitut meetodit.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</source><target logoport:matchpercent="0" state="translated">Meetodit <bpt id="p1">**</bpt>timesheetLineNeedsUpdating<ept id="p1">**</ept> kasutatakse määramaks, kas kasutaja on rakenduses rea kirjet muutnud ja kas see tuleb andmebaasi salvestada.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If performance isn't a concern, this method can be simplified so that it always returns <bpt id="p1">**</bpt>true<ept id="p1">**</ept>.</source><target logoport:matchpercent="0" state="translated">Kui jõudlus pole probleem, saab seda meetodit lihtsustada, et see annaks alati tulemuseks <bpt id="p1">**</bpt>tõene<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>The <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> and <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</source><target logoport:matchpercent="0" state="translated">Meetodeid <bpt id="p1">**</bpt>populateTimesheetLineFromEntryDuringCreate<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>populateTimesheetLineFromEntryDuringUpdate<ept id="p2">**</ept> saab laiendada, nii et need sisestavad väärtused andmebaasikirjesse TSTimesheetLine olemasolevast andmelepingu kirjest TSTimesheetEntry.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</source><target logoport:matchpercent="0" state="translated">Järgnevas näites pange tähele, kuidas on X++ koodiga tehtud vastendamine andmebaasi välja ja kandevälja vahel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> method can also be extended if the custom field that is mapped to the <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> object must write back to the TSTimesheetLineweek database table.</source><target logoport:matchpercent="0" state="translated">Meetodit <bpt id="p1">**</bpt>populateTimesheetWeekFromEntry<ept id="p1">**</ept> saab laiendada ka siis, kui objektiga <bpt id="p2">**</bpt>TSTimesheetEntry<ept id="p2">**</ept> vastendatud kohandatud väli peab värskendama andmebaasi tabelit TSTimesheetLineweek.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The following example saves the <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> or <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> value that the user selects to the database as a raw string value.</source><target logoport:matchpercent="0" state="translated">Järgmises näites salvestatakse kasutaja valitud väärtus <bpt id="p1">**</bpt>firstOption<ept id="p1">**</ept> või <bpt id="p2">**</bpt>secondOption<ept id="p2">**</ept> andmebaasi toorstringi väärtusena.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>If the database field is a field of the <bpt id="p1">**</bpt>Enum<ept id="p1">**</ept> type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</source><target logoport:matchpercent="0" state="translated">Kui andmebaasi väli on tüüp <bpt id="p1">**</bpt>Loetelu<ept id="p1">**</ept>, saan neid väärtusi käsitsi vastendada loetelu väärtusega ja seejärel salvestada need loetelu välja andmebaasi tabelis.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Show a custom field in the timesheet header section</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Kohandatud välja kuvamine ajatabeli päise jaotises</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Below is a screenshot from the mobile app of a user viewing a timesheet.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">All on mobiilirakenduse kuvatõmmis ajatabelit vaatavast kasutajast.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The "More information" button has been selected in the upper-right corner to show the "View more details" option.</source><target logoport:matchpercent="0" state="translated">Ülevalt paremast nurgast on valitud nupp Lisateave, mis kuvab suvandi Kuva rohkem üksikasju.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>View more details command</source><target logoport:matchpercent="77" state="translated" state-qualifier="fuzzy-match">Käsk Kuva rohkem üksikasju</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Below is a screenshot from the mobile app showing the “More” section of a timesheet.</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">All on mobiilirakenduse kuvatõmmis ajatabeli jaotisest Rohkem.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</source><target logoport:matchpercent="0" state="translated">Ajatabeli päise jaotisesse on lisatud kohandatud väli nimega Selle ajatabeli tulususmäär (arvutatud kohandatud väli).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>A read-only value of "0.667" is set on the custom field.</source><target logoport:matchpercent="0" state="translated">Kohandatud väljale on määratud kirjutuskaitstud väärtus 0,667.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>More section</source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match">Jaotis Rohkem</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Extend the TSTimesheetTable table so that it has a custom field</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">Tabeli TSTimesheetTable laiendamine, nii et sellel on kohandatud väli</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Tavalises stsenaariumis on tõenäoline, et päise jaotise kohandatud välja andmed võetakse tabelist TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</source><target logoport:matchpercent="97" state="translated" state-qualifier="fuzzy-match">Kuid muid tabeleid saab kasutada, kui andmeid saab võtta olemasoleva kirje TSTimesheetTable põhjal või kui sellel pole konkreetset kirje konteksti (nt kui väli on projekti parameetrites määratud kirjutuskaitstuks).</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Note that custom fields don't have to have any backing database records.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Pange tähele, et kohandatud väljadel ei pea olema toetavaid andmebaasikirjeid.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>They can be dynamically generated based on X++ logic.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Neid saab dünaamiliselt luua X++ loogika põhjal.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>The example that follows shows this approach.</source><target logoport:matchpercent="0" state="translated">Järgmises näites on näha see lähenemine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Fields in the header section are always read-only in the app.</source><target logoport:matchpercent="0" state="translated">Päise jaotises olevad väljad on rakenduses alati kirjutuskaitstud.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</source><target logoport:matchpercent="89" state="translated" state-qualifier="fuzzy-match">Käsuliini kasutamine klassi TSTimesheetSettings meetodil buildCustomFieldList välja kuvamiseks päise jaotises</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>This code controls the display settings for the field in the app.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">See kood reguleerib välja kuvasätteid rakenduses.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Näiteks reguleerib see välja tüüpi, silti, seda, kas väli on kohustuslik, ja millises jaotises väli ilmub.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>The following example shows a computed value in the header section in the app.</source><target logoport:matchpercent="0" state="translated">Järgmises näites on näha arvutatud väärtus rakenduse päise jaotises.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match">Käsuliini kasutamine klassi TSTimesheetDetails meetodil buildCustomFieldListForHeader ajatabeli üksikasjade täitmiseks</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> method is used to fill in the timesheet header details in the mobile app.</source><target logoport:matchpercent="71" state="translated" state-qualifier="fuzzy-match">Meetodit <bpt id="p1">**</bpt>buildCustomFieldListForHeader<ept id="p1">**</ept> kasutatakse ajatabeli päise üksikasjade sisestamiseks salvestatud ajatabeli ridadele mobiilirakenduses.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>It takes a TSTimesheetTable record as a parameter.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">See kasutab kirjet TSTimesheetTable parameetrina.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Fields from that record can be used to fill in the custom field value in the app.</source>
        <target logoport:matchpercent="0" state="translated" state-qualifier="leveraged-inherited">Välju sellest kirjest saab kasutada kohandatud välja väärtuse täitmiseks rakenduses.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>The following example doesn't read any values from the database.</source><target logoport:matchpercent="0" state="translated">Järgmises näites ei loeta andmebaasist ühtki väärtust.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Instead, it uses X++ logic to generate a computed value that is then shown in the app.</source><target logoport:matchpercent="0" state="translated">Selle asemel kasutab see X++ loogikat arvutatud väärtuse loomiseks, mis kuvatakse seejärel rakenduses.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Other configurability/extensibility opportunities</source><target logoport:matchpercent="0" state="translated">Muud konfigureeritavuse/laiendatavuse võimalused</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Adding additional validation for the app</source><target logoport:matchpercent="0" state="translated">Lisakinnituse lisamine rakendusele</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Existing logic for timesheet functionality at the database level will still work as expected.</source><target logoport:matchpercent="0" state="translated">Ajatabeli funktsiooni olemasolev loogika andmebaasi tasemel töötab endiselt ootuspäraselt.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>To interrupt the completion of save or submit operations and show a specific error message, you can add <bpt id="p1">**</bpt>throw error("message to user")<ept id="p1">**</ept> to the code via a chain of command extension.</source><target logoport:matchpercent="0" state="translated">Salvestamise või esitamise toimingu lõpetamise katkestamiseks ja konkreetse tõrketeate kuvamiseks saate lisada koodile käsuliini laienduse kaudu suvandi <bpt id="p1">**</bpt>kuvatakse tõrge (teade kasutajale)<ept id="p1">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Here are three examples of useful extensible methods:</source><target logoport:matchpercent="0" state="translated">Siin on kolm näidet kasulikest laiendatavatest meetoditest.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>If <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> on the TSTimesheetLine table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during a save operation for a timesheet line, an error message is shown in the mobile app.</source><target logoport:matchpercent="0" state="translated">Kui <bpt id="p1">**</bpt>validateWrite<ept id="p1">**</ept> tabelis TSTimesheetLine annab ajatabeli rea salvestamise ajal tulemuse <bpt id="p2">**</bpt>väär<ept id="p2">**</ept>, kuvatakse mobiilirakenduses tõrketeade.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>If <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> on the TSTimesheetTable table returns <bpt id="p2">**</bpt>false<ept id="p2">**</ept> during timesheet submission in the app, an error message is shown to the user.</source><target logoport:matchpercent="72" state="translated" state-qualifier="fuzzy-match">Kui <bpt id="p1">**</bpt>validateSubmit<ept id="p1">**</ept> tabelis TSTimesheetTable annab ajatabeli esitamise ajal rakenduses tulemuse <bpt id="p2">**</bpt>väär<ept id="p2">**</ept>, kuvatakse kasutajale tõrketeade.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Logic that fills in fields (for example, <bpt id="p1">**</bpt>Line Property<ept id="p1">**</ept>) during the <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> method on the TSTimesheetLine table will still run.</source><target logoport:matchpercent="0" state="translated">Käitatakse siiski loogika, mis täidab väljad (näiteks <bpt id="p1">**</bpt>Rea atribuut<ept id="p1">**</ept>) meetodi <bpt id="p2">**</bpt>insert<ept id="p2">**</ept> ajal tabelis TSTimesheetLine.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Hiding and marking out-of-box fields as read-only via configuration</source><target logoport:matchpercent="0" state="translated">Valmis väljade peitmine ja märkimine kirjutuskaitstuteks konfiguratsiooni kaudu</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</source><target logoport:matchpercent="0" state="translated">Projekti parameetrites saate muuta valmis väljad mobiilirakenduses kirjutuskaitstuks või neid peita.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Set the options in the <bpt id="p1">**</bpt>Mobile timesheets<ept id="p1">**</ept> section on the <bpt id="p2">**</bpt>Timesheet<ept id="p2">**</ept> tab of the <bpt id="p3">**</bpt>Project management and accounting parameters<ept id="p3">**</ept> page.</source><target logoport:matchpercent="0" state="translated">Määrake suvandid jaotises <bpt id="p1">**</bpt>Mobiili ajatabelid<ept id="p1">**</ept> vahekaardil <bpt id="p2">**</bpt>Ajatabel<ept id="p2">**</ept> lehel <bpt id="p3">**</bpt>Projektihalduse ja -arvestuse parameetrid<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Project parameters</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Projekti parameetrid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Changing the activities that are available for selection via extensions</source><target logoport:matchpercent="0" state="translated">Laienduste kaudu valimiseks saadaolevate tegevuste muutmine</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>The activities that are available for selection for a project are filled in via the <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="0" state="translated">Projekti jaoks valimiseks saadaolevad tegevused täidetakse meetoditega <bpt id="p1">**</bpt>getActivitiesForProject()<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>getActivityQuery()<ept id="p2">**</ept> klassis <bpt id="p3">**</bpt>TsTimesheetProjectService<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</source><target logoport:matchpercent="0" state="translated">Selle käitumise muutmiseks saate kasutada käsuliini, et vastendada oma äristsenaarium tegevustega, mis on valimiseks saadaval konkreetse projekti jaoks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Entering a default project category on timesheet entries</source><target logoport:matchpercent="0" state="translated">Projekti vaikekategooria sisestamine ajatabeli kannetele</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Entry of a default project category on timesheet entries occurs at three levels.</source><target logoport:matchpercent="0" state="translated">Projekti vaikekategooria sisestamine ajatabeli kannetele toimub kolmel tasemel.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</source><target logoport:matchpercent="0" state="translated">Käitumise laiendamiseks ühel või kõigil tasemetel võite kasutada käsuliini soovitud tulemuse saavutamiseks.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The following hierarchy is used:</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Arvutamisel kasutatakse järgmist hierarhiat:</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>The app tries to put the default category from the project resource.</source><target logoport:matchpercent="0" state="translated">Rakendus üritab võtta vaikekategooria projektiressursist.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>This default category is set in the <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> and <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> methods in the <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept> class.</source><target logoport:matchpercent="0" state="translated">See vaikekategooria määratakse meetodites <bpt id="p1">**</bpt>getCurrentUserResource<ept id="p1">**</ept> ja <bpt id="p2">**</bpt>getDelegatedResourcesForCurrentUser<ept id="p2">**</ept> klassis <bpt id="p3">**</bpt>TSTimesheetSettingsService<ept id="p3">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</source><target logoport:matchpercent="0" state="translated">Kui projektiressursi tasemel ei pakuta vaikekategooriat, üritab rakendus võtta seda projekti tegevusest.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>This default category is set in the <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="0" state="translated">See vaikekategooria määratakse meetodis <bpt id="p1">**</bpt>getActivitiesForProject<ept id="p1">**</ept> klassis <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</source><target logoport:matchpercent="82" state="translated" state-qualifier="fuzzy-match">Kui projekti tegevuse tasemel ei pakuta vaikekategooriat, võetakse vaikekategooria projekti parameetritest.</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>This default category is set in the <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> method in the <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept> class.</source><target logoport:matchpercent="91" state="translated" state-qualifier="fuzzy-match">See vaikekategooria määratakse meetodis <bpt id="p1">**</bpt>getProjectDetailsbyRule<ept id="p1">**</ept> klassis <bpt id="p2">**</bpt>TSTimesheetProjectService<ept id="p2">**</ept>.</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>