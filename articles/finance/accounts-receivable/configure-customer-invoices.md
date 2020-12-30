---
title: Kliendiarve loomine
description: '**Müügitellimuse kliendiarve** on arve, mis on seotud müügiga, ja mille organisatsioon kliendile annab.'
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f5b9866fc7afba205b84b372c6a204ec4c8f64d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442235"
---
# <a name="create-a-customer-invoice"></a>Kliendiarve loomine

[!include [banner](../includes/banner.md)]

**Müügitellimuse kliendiarve** on arve, mis on seotud müügiga, ja mille organisatsioon kliendile annab. Sellist tüüpi müügiarve luuakse müügitellimuse põhjal, mis sisaldab tellimuse ridu ja kaubakoode. Kauba koodid täpsustatakse ja sisestatakse pearaamatusse. Alammooduli töölehe kirjed pole müügitellimuse kliendiarve puhul saadaval. Lisateabe saamiseks vt [Müügitellimuse arvete loomine](tasks/create-sales-order-invoices.md).

**Vabas vormis arve** pole müügitellimusega seotud. See sisaldab tellimuse ridu, mille hulka kuuluvad pearaamatukontod, vaba tekstina sisestatud kirjeldused ja müügihind, mille sisestate. Seda tüüpi arvele ei saa kaubakoodi sisestada. Peate sisestama vastava käibemaksuteabe. Müügi põhikonto on näidatud igal arve real, mille saate jaotada mitmele pearaamatukontole, klõpsates valikut **Summade jaotamine** lehel **Vabas vormis arve**. Lisaks sisestatakse kliendi saldo vabas vormis arve puhul kasutatavatest sisestusreeglitest koondkontole.

Lisateavet vt 

[Vabateksti arvete loomine](../accounts-receivable/create-free-text-invoice-new.md)

[Vabas vormis arve malli loomine](../accounts-receivable/create-free-text-invoice-template-new.md)

[Vabas vormis arve malli määramine kliendile](tasks/assign-free-text-invoice-template-customer.md)

[Korduvate vabas vormis arvete genereerimine ja sisestamine](tasks/post-recurring-free-text-invoices.md)


**Esialgne arve** on arve, mis on vormistatud hinnanguliste arvesummadega enne arve sisestamist. Saate printida esialgse arve nii müügitellimuse kliendiarve kui ka vabas vormis arve kohta.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a>Eraldi müügitellimustel põhinevate kliendiarvete sisestamine ja printimine
Selle protsessi abil saate koostada müügitellimusel põhineva arve. Seda võib teha, kui otsustate arve kliendile esitada enne kaupade või teenuste tarnimist. 

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** arveldatud kogustega valitud müügitellimusest. Kui kõigi müügitellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**. Kui kogus **Arve jääk** ei ole 0 (null), siis müügitellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid.

Müügitellimuste olekut saab vaadata loendilehel **Kõik müügitellimused**. Lehel **Avatud kliendiarved** saate vaadata sisestatud arveid.

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a>Saatelehtedel ja kuupäevadel põhinevate üksikute kliendiarvete sisestamine ja printimine
Kasutage seda protsessi, kui müügitellimuse kohta on sisestatud vähemalt üks saateleht. Kliendiarve aluseks on need saatelehed ja arve näitab saatelehtedelt pärit koguseid. Finantsteave arve jaoks põhineb teabel, mis sisestatakse, kui sisestate arve. 

Saate luua kliendiarve, mis põhineb saatelehe tähtajaliselt välja saadetud reakaupadel, isegi kui kõik konkreetse müügitellimuse kaubad ei ole veel välja saadetud. Seda saate teha nt siis, kui teie juriidiline isik väljastab igale kliendile ühe arve kuus, mis katab kõik selle kuu tarned. Iga saateleht esindab müügitellimusel olevate kaupade osalist või täielikku väljasaatmist. 

Arve sisestamisel uuendatakse iga kauba kogus väljal **Arve jääk** tarnitud kogustega valitud saatelehtedelt. Kui kõigi müügitellimuse kaupade kogus **Arve jääk** ja **Tarne jääk** on 0 (null), määratakse müügitellimuse olekuks **Arveldatud**. Kui kogus **Arve jääk** ei ole 0 (null), siis müügitellimuse olekut ei muudeta ja sellele saab sisestada täiendavaid arveid. 

Laokandeid uuendatakse koos arvenumbritega ja olek müügitellimuse väljal **Rea olek** muutub olekuks **Arveldatud**. 

Müügitellimuste olekut saab vaadata loendilehel **Kõik müügitellimused**.

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a>Müügitellimuste või saatelehtede konsolideerimine sisestamiseks
Kasutage seda protsessi, kui vähemalt üks müügitellimus on arveldamiseks valmis ja soovite need ühele arvele konsolideerida. 

Saate valida mitu arvet loendilehelt **Müügitellimus** ja kasutage siis nende konsolideerimiseks valikut **Loo arved**. Lehel **Arve sisestamine** saate muuta valiku **Koondtellimus** sätet, et summeerida tellimuse numbri alusel (kui ühe müügitellimuse kohta on mitu saatelehte) või arvekonto alusel (kui ühe arvekonto kohta on mitu müügitellimust). Kasutage nuppu **Korrasta** müügitellimuste konsolideerimiseks ühele arvele valiku **Koondtellimus** sätete põhjal.

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
<li><strong>Pole</strong> – krediidilimiidi kontrollimiseks pole mingit vajadust.</li>
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





