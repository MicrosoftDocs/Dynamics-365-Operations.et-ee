---
title: Kliendiarve loomine
description: Müügitellimuse kliendiarve on arve, mis on seotud müügiga, ja mille organisatsioon kliendile annab.
author: ShivamPandey-msft
ms.date: 03/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04c26eec8be61d60908bef67c75958287e7e1a01
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/09/2022
ms.locfileid: "9129508"
---
# <a name="create-a-customer-invoice"></a>Kliendiarve loomine

[!include [banner](../includes/banner.md)]

Müügitellimuse **kliendiarve on müügiga** seotud arve, mille organisatsioon kliendile annab. Sellist tüüpi müügiarve luuakse müügitellimuse põhjal, mis sisaldab tellimuse ridu ja kaubakoode. Kauba koodid täpsustatakse ja sisestatakse pearaamatusse. Alammooduli töölehe kirjed pole müügitellimuse kliendiarve puhul saadaval. Lisateabe saamiseks vt [Müügitellimuse arvete loomine](tasks/create-sales-order-invoices.md).

Vabas **vormis** arve ei ole seotud müügitellimusega. See sisaldab tellimuse ridu, mille hulka kuuluvad pearaamatukontod, vaba tekstina sisestatud kirjeldused ja müügihind, mille sisestate. Seda tüüpi arvele ei saa kaubakoodi sisestada. Peate sisestama vastava käibemaksuteabe. Müügi põhikonto on näidatud igal arve real, mille saate jaotada mitmele pearaamatukontole, klõpsates valikut **Summade jaotamine** lehel **Vabas vormis arve**. Lisaks sisestatakse kliendi saldo vabas vormis arve puhul kasutatavatest sisestusreeglitest koondkontole.

Lisateabe saamiseks vt:

[Vabas vormis arvete loomine Vabas vormis arve malli loomine Vabas
](../accounts-receivable/create-free-text-invoice-new.md)[...](../accounts-receivable/create-free-text-invoice-template-new.md)[
 vormis arve malli määramine kliendile Korduvate vabas](tasks/assign-free-text-invoice-template-customer.md)
[vormis arvete loomine ja sisestamine](tasks/post-recurring-free-text-invoices.md)


**Pro forma arve** on arve, mis on ettevalmistatud hinnanguna tegelike arvesummade kohta enne arve sisestamist. Saate printida kas **müügitellimuse kliendiarve** või vabas vormis arve pro forma arve. 

>[!NOTE]
> Süsteemikatkestuse korral müügi pro forma arveprotsessi käigus saab pro forma arve orvuks teha. Orvuks jäänud pro forma arve saab kustutada **perioodilise tööga Kustuta pro forma arved** käsitsi. Avage müügi **ja turunduse > perioodilised > või > käsitsi kustutama pro forma arved**.

## <a name="using-sales-order-customer-invoice-data-entities"></a>Müügitellimuse kliendiarve andmeüksuste kasutamine
Saate kasutada andmeüksuseid müügitellimuse kliendiarve kohta teabe importimiseks ja eksportimiseks. Müügiarve päisel ja müügiarve ridadel oleva teabe jaoks on erinevaid üksusi.

Müügiarve päise teabe jaoks on saadaval järgmised üksused:

- **Müügiarve töölehe päise** üksus (SalesInvoiceJournalHeaderEntity)
- **Müügiarve päiste V2 üksus** (SalesInvoiceHeaderV2Entity)

Soovitame kasutada müügiarve **töölehe päise üksust**, sest see pakub müügipäise importimise ja eksportimise kohta rohkem kogemust. Üksus ei sisalda **käibemaksusummat** (INVOICEHEADERTAMOUNT) veergu, mis näitab müügiarve päise käibemaksuväärtust. Kui teie äristsenaarium nõuab seda teavet, kasutage **müügiarve päisete V2** üksust müügiarve päise teabe importimiseks ja eksportimiseks.

Müügiarve ridade teabe jaoks on saadaval järgmised üksused:

- **Kliendiarve ridade** üksus (BusinessDocumentSalesInvoiceLineItemEntity)
- **Müügiarve ridade V3 üksus** (SalesInvoiceLineV3Entity)

Eksportimiseks kasutatava reaüksuse määratlemisel kaaluge, kas kasutatakse täis- või astmelist tõugamist. Lisaks kaaluge andmete koostist. Müügiarve **ridade V3** üksus toetab keerukamaid stsenaariume (nt vastendamist laoväljadega). Samuti toetab see täistööajaga ekspordi stsenaariume. Astmeliste liinide puhul on soovitatav kasutada kliendiarve **ridade üksust**. Üksus sisaldab palju lihtsamat andmekoostist **kui müügiarve ridade V3** üksus ja seda eelistatakse eriti juhul, kui laovälja integreerimine ei nõuta. Rea üksuste vastendamise toe **erinevuste tõttu on kliendiarve** **ridade üksuse jõudlus tavaliselt kiirem kui müügiarve ridade V3 üksus**.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Eraldi müügitellimustel põhinevate kliendiarvete sisestamine ja printimine
Selle protsessi abil saate koostada müügitellimusel põhineva arve. Seda võib teha, kui otsustate arve kliendile esitada enne kaupade või teenuste tarnimist. 

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** arveldatud kogustega valitud müügitellimusest. Kui kõigi müügitellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**. Kui kogus **Arve jääk** ei ole 0 (null), siis müügitellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid.

Müügitellimuste olekut saab vaadata loendilehel **Kõik müügitellimused**. Lehel **Avatud kliendiarved** saate vaadata sisestatud arveid.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Saatelehtedel ja kuupäevadel põhinevate üksikute kliendiarvete sisestamine ja printimine
Kasutage seda protsessi, kui müügitellimuse kohta on sisestatud vähemalt üks saateleht. Kliendiarve aluseks on need saatelehed ja arve näitab saatelehtedelt pärit koguseid. Finantsteave arve jaoks põhineb teabel, mis sisestatakse, kui sisestate arve. 

Saate luua kliendiarve, mis põhineb saatelehe rea kaupadel, mis on lähetatud kuupäevani, isegi kui kõik konkreetse müügitellimuse kaubad pole lähetatud. Seda saate teha nt siis, kui teie juriidiline isik väljastab igale kliendile ühe arve kuus, mis katab kõik selle kuu tarned. Iga saateleht esindab müügitellimusel olevate kaupade osalist või täielikku väljasaatmist. 

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** tarnitud kogustega valitud saatelehtedelt. Kui kõigi müügitellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**. Kui kogus **Arve jääk** ei ole 0 (null), siis müügitellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid. 

Laokandeid uuendatakse koos arvenumbritega ja olek müügitellimuse väljal **Rea olek** muutub olekuks **Arveldatud**. 

Vaadake müügitellimuste olekut lehel **Kõik müügitellimused**.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Müügitellimuste või saatelehtede konsolideerimine sisestamiseks
Kasutage seda protsessi, kui vähemalt üks müügitellimus on arveldamiseks valmis ja soovite need ühele arvele konsolideerida. 

Saate valida mitu arvet loendilehelt **Müügitellimus** ja kasutage siis nende konsolideerimiseks valikut **Loo arved**. Lehel **Arve sisestamine** saate muuta valiku **Koondtellimus** sätet, et summeerida tellimuse numbri alusel (kui ühe müügitellimuse kohta on mitu saatelehte) või arvekonto alusel (kui ühe arvekonto kohta on mitu müügitellimust). Kasutage nuppu **Korrasta** müügitellimuste konsolideerimiseks ühele arvele valiku **Koondtellimus** sätete põhjal.

## <a name="split-sales-order-invoices-by-site-and-delivery-information"></a>Müügitellimuste arvete tükeldamine saidi- ja tarneteabe alusel
Saate konfigureerida müügitellimuse kliendiarvete **tükeldamise** **saidi või tarneaadressi järgi lehe Müügireskontro parameetrid vahekaardil Koonds uuendamine.** 
 - Valige suvand **Tükelda arve saidi alusel,** et sisestamisel luua üks arve saidi kohta. 
 - Valige suvand **Tükelda arve tarneteabe alusel,** et luua sisestamisel müügitellimuse rea tarneaadressi kohta üks arve. 

## <a name="post-to-revenue-account-for-sales-order-lines-that-have-no-price-and-no-cost"></a>Tulukontole sisestamisel müügitellimuse ridadele, kus hind puudub ja kulu puudub
Teil on võimalus värskendada pearaamatu **tulukontot** **müügitellimuse** ridadel, kus hind ja kulu puudub. Selle teabe häälestamiseks või vaatamiseks **minge** **·** **tulukontole sisestamisele nullhinnaga ja nullkuluga müügitellimuse arve ridade parameetrile pearaamatu ja müügireskontro parameetrite lehe käibemaksu vahekaardil.** (Müügireskontro **> seadistus > Müügireskontro parameetrid**). Valige **Jah**, et uuendada **tulukonto** müügitellimuse arve ridadele, mille hind ja kulu puudub. Kui see suvand on valitud, sisaldab kanne 0,00 kirjet kliendi **saldo** ja tulu sisestustüüpide **kohta**. Tulukonto määratletakse vahekaardi Müügitellimuse **konto** määratlus lehel Varude **sisestamise** parameeter. Kui seda valikut ei valita, ei sisestata hinna- või kuluteabeta ridu **tulukontole**. Selle asemel sisaldab kanne kliendi saldo sisestustüübi jaoks 0,00 **kirjet**.

## <a name="line-creation-sequence-number-information"></a>Rea loomise järjekorranumbri teave
Kliendiarve ridade sisestamisel saate luua jadarea loomise järjekorranumbrid. Rea loomise järjekorranumbrid määratakse sisestusprotsessi käigus. Kui lubate mittejärjenumbrite sisestamist, saate aidata parandada kliendiarvete sisestamise jõudlust. Rea loomise järjekorranumbreid saavad kasutada kolmanda osapoole integratsioonid, mis ootavad järjestikku tellimist. Konsulteerige oma IT-osakonnaga mis tahes laiendite suhtes, mis võivad integreeruda rea loomise järjekorranumbritega.

Selle teabe **häälestamiseks** **·** **või vaatamiseks seadke müügireskontro parameetrite lehel vahekaardil Värskendused suvand Määra kliendiarve ridade sisestamisel järjestikused reanumbrid:**

- Rea loomise järjekorranumbrite **mittejärjekorranumbrite** kasutamiseks määrake suvandiks Ei.
- Seadke valikule **Jah**, et kasutada seerianumbrite nummerdamist. Peate määrama suvandi Jah juriidilistele **isikutele**, kelle peamine aadress on Itaalias. Kui **custInvoiceTransRandLineCreationSeqNumF** **flight** on keelatud, peate selle määrama väärtusele Jah.

## <a name="additional-settings-that-change-the-posting-behavior"></a>Sisestamiskäitumist muutvad lisasätted
Järgmised väljad muudavad sisestamisprotsessi käitumist.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kogus</td>
<td>Valige kogused, millel dokumendi sisestus põhineb. Saadaolevad valikud erinevad olenevalt sisestatava dokumendi tüübist (nt saateleht või arve).
<ul>
<li><strong>Tarni kohe</strong> – valige kõik kogused, mis on sisestatud väljale <strong>Tarni kohe</strong>. Selle suvandi abil saate kinnitada või esitada osalise tellimuse.</li>
<li><strong>Komplekteeritud</strong> – valitakse kõik komplekteeritud kogused.</li>
<li><strong>Kõik</strong> – valitakse kõik müügitellimuse kogused, mida pole veel praeguse dokumenditüübiga värskendatud.</li>
<li><strong>Saateleht</strong> – valitakse kõik saatelehe värskendatud kogused.</li>
<li><strong>Komplekteeritud kogus ja ladustamata tooted</strong> – valitakse kõik komplekteeritud kogused ja kõik ladustamata tooted.</li>
</ul></td>
</tr>
<tr class="even">
<td>Sisestamine</td>
<td><ul>
<li>Selle suvandi valimisel paigutatakse müügitellimus töölehele.</li>
<li>Selle suvandi tühjendamisel prinditakse esialgne müügitellimus. <strong>Märkus</strong>. Kui tegite maksegraafiku leppe, siis esialgsel müügitellimusel maksegraafikut ei kuvata. Maksegraafikud kuvatakse vaid tegelikel müügitellimustel.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Hiline valik</td>
<td>Valige see suvand, kui soovite valitud päringu hiljem rakendada. Seda suvandit kasutatakse pakett-tööde puhul. Päring käivitatakse pakett-töö käivitamisel.</td>
</tr>
<tr class="even">
<td>Vähenda kogust</td>
<td>Selle suvandi valimisel vähendatakse dokumendi sisestamisel automaatselt tarnitud kogust, et tarnitud kogus oleks võrdne saadaoleva varuga.</td>
</tr>
<tr class="odd">
<td>Prindi</td>
<td>Saate valida, millal dokumendid prinditakse.
<ul>
<li><strong>Praegune</strong> – saate printida dokumente pärast iga arve uuendamist.</li>
<li><strong>Pärast</strong> – dokumendid prinditakse pärast kõikide arvete uuendamist.</li>
</ul>
<strong>Märkus.</strong> Väli <strong>Prindi</strong> on saadaval vaid juhul, kui teete valiku <strong>Prindi arve</strong>, <strong>Prindi kinnitus</strong>, <strong>Prindi komplekteerimisleht</strong> või <strong>Prindi saateleht</strong>. Nt peate lehel <strong>Vormi sortimine</strong> seadistama süsteemi teavet arvekonto alusel sortima. Seejärel saate valida suvandi <strong>Pärast</strong>, et printida dokumendid arvekonto alusel sorditud partiina. Vastasel juhul prinditakse dokumendid enne töötlemise lõpule viimist ja dokumente ei sordita lehel <strong>Vormi sortimine</strong> määratud järjestusse.</td>
</tr>
<tr class="even">
<td>Prindi arve</td>
<td>Tehke see valik arve printimiseks. Kui see valik on välja lülitatud, saate sisestada arve ilma seda printimata.</td>
</tr>
<tr class="odd">
<td>Saada meilisõnum</td>
<td>Tehke see valik müügitellimuse arve saatmiseks kliendile meilimanusena pärast arve sisestamist. Manused saadetakse PDF- ja XML-failidena. See valik on saadaval ainult juhul, kui teete valiku <strong>Luba CFD (elektroonilised arved)</strong> lehel <strong>Elektroonilise arve parameetrid</strong>. <strong>Märkus.</strong> (MEX) See juhtelement on saadaval ainult juriidilistele isikutele, kelle peamine aadress on Mehhikos.</td>
</tr>
<tr class="even">
<td>Kasuta prindihalduse sihtkohta</td>
<td>Tehke see valik, et kasutada printimissätteid, mis on määratud kandele, dokumendile või moodulile lehel <strong>Prindihalduse seadistus</strong>.</td>
</tr>
<tr class="odd">
<td>Kontrolli krediidilimiiti</td>
<td>Saate valida teabe, mida krediidilimiidi kontrollimisel tuleb analüüsida.
<ul>
<li><strong>Pole</strong> – krediidilimiidi kontroll ei ole nõutav.</li>
<li><strong>Saldo</strong> – krediidilimiiti kontrollitakse kliendi saldo suhtes.</li>
<li><strong>Saldo + saateleht või toote sissetulek</strong> – krediidilimiiti kontrollitakse kliendi saldo ja tarnete suhtes.</li>
<li><strong>Saldo + kõik</strong> – krediidilimiiti kontrollitakse kliendi saldo, tarnete ja avatud tellimuste suhtes.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kreediti parandus</td>
<td>Selle suvandi valimisel kuvatakse kreeditarve kanded tehingukannetes deebetina.</td>
</tr>
<tr class="odd">
<td>Krediteeri järelejääv kogus</td>
<td>Kui sisestate kreeditarve, valige see suvand järelejäänud koguse tellimusel säilitamiseks. Kui see suvand pole märgitud, määratakse järelejäänud koguseks 0 (null).</td>
</tr>
<tr class="even">
<td>Koondsisestamine</td>
<td>Saate valida mitme müügitellimuse summeerimise viisi.
<ul>
<li><strong>Puudub</strong> – müügitellimusi ei summeerita. Näiteks luuakse iga müügitellimuse kohta eraldi arve.</li>
<li><strong>Arvekonto</strong> – kõik valitud tellimused summeeritakse lehel <strong>Koondsisestamise parameetrid</strong> seadistatud kriteeriumide alusel.</li>
<li><strong>Tellimus</strong> – valitud tellimuste vahemik summeeritakse ühte määratud tellimusse. Tellimuses summeeritakse lehel <strong>Koondsisestamise parameetrid</strong> seadistatud kriteeriumide alusel. Selle valiku korral tuleb valida väärtus väljal <strong>Müügitellimus</strong>.</li>
<li><strong>Automaatkokkuvõte</strong> – kui lehel <strong>Koondsisestamine</strong> on määratud koondsisestamised, summeeritakse kõik valitud tellimused lehel <strong>Koondsisestamise parameetrid</strong> määratud kriteeriumide alusel. Kui koondsisestamisi pole määratud, sisestatakse tellimus eraldi.</li>
<li><strong>Saateleht</strong> – valitud tellimuste vahemik summeeritakse iga saatelehe puhul ühele arvele. Seda valikut saab kasutada ainult juhul, kui on tehtud valik <strong>Saateleht</strong> väljal <strong>Kogus</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
