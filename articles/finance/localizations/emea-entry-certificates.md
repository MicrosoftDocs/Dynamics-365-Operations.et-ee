---
title: ELi kandesertifikaadid
description: Artikkel annab teavet Euroopa Liidu (EL) kirjesertide kohta.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46a4180163adea72e7d8712ed5ce6a3306e477c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407859"
---
# <a name="eu-entry-certificates"></a>EL-i kandesertifikaadid

[!include [banner](../includes/banner.md)]

Artikkel annab teavet Euroopa Liidu (EL) kirjesertide kohta.

Euroopa Liidu (ELi) kandesertifikaat võimaldab teha järgmisi toiminguid.

-   Looge ja väljastage EL-i kandesertifikaat koos saatelehe või kliendiarvega kaupade või teenuste ELi riikidesse/regioonidesse tarnimiseks.
-   Võtke vastu EL-i kandesertifikaate, mille on allkirjastanud EL-i klient.
-   Laadige üles allkirjastatud EL-i kandesertifikaat, mille saite kliendilt või kolmandalt osapoolelt, kes vastutab kaupade kliendile tarnimise eest.
-   Seostage üleslaaditud EL-i kandesertifikaat kliendiarvega.
-   Värskendage üleslaaditud EL-i kandesertifikaadi olekut.

## <a name="prerequisites"></a>Eeltingimused 
Järgmises tabelis kuvatakse eeltingimused, mis peavad olema asukohakorralduse loomiseks täidetud.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategooria</th>
<th>Eeltingimus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Riik/regioon</td>
<td>Juriidilise isiku peamine aadress peab olema ELi liikmesriigis.</td>
</tr>
<tr class="even">
<td>Seotud seadistustoimingud</td>
<td><ul>
<li>Tehke lehel <strong>Müügireskontro parameetrid</strong> valikud <strong>Luba kandesertifikaadi haldamine</strong> ja <strong>Luba kandesertifikaadi väljastamine</strong>.</li>
<li>Tehke lehe <strong>Kliendid</strong> kiirkaardil <strong>Arve ja tarne</strong> valik <strong>Kandesertifikaat on nõutav</strong>, näitamiseks, et ELi kandesertifikaat on kliendi puhul nõutav. Märkige valik <strong>Väljasta kandesertifikaat</strong>, et väljastada kliendile juriidilise isiku ELi kandesertifikaat.</li>
<li>Valige lehelt <strong>Müügireskontro parameetrid</strong> valiku <strong>Kandesertifikaat</strong> viitele numbriseeria kood.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Seotud kanded</td>
<td><ul>
<li>Looge kliendikonto.</li>
<li>Looge müügitellimus.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>ELi kandesertifikaadi loomine, registreerimine ja üleslaadimine
EL-i kandesertifikaadi saab luua automaatselt või käsitsi. ELi kandesertifikaat luuakse ja prinditakse automaatselt, kui sisestate kliendi saatelehe või arve lehele **Saatelehe sisestamine** või **Arve sisestamine**. Kliendi arve ELi kandesertifikaadi käsitsi loomiseks või uuesti printimiseks kasutage lehte **Arve tööleht**. Lisaks saate sisestada kolmanda osapoole väljastatud EL-i kandesertifikaadi üksikasjad lehele **Kandesertifikaadi tööleht**.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>ELi kandesertifikaadi loomine automaatselt või käsitsi

Saate luua ELi kandesertifikaadi automaatselt, kasutades saatelehte lehel **Kõik müügitellimused** või arvet lehel **Müügitellimus**. ELi kandesertifikaadi käsitsi loomiseks võite kasutada arvet lehel **Arve tööleht**. Kuid enne ELi kandesertifikaadi käsitsi loomist tuleb arve sertifikaadi olekut muuta.

### <a name="registering-an-eu-entry-certificate"></a>ELi kandesertifikaadi registreerimine

Kui registreerimine on vajalik, saate registreerida kolmanda osapoole väljastatud EL-i kandesertifikaadi lehel **Kandesertifikaadi tööleht**.

### <a name="uploading-a-received-eu-entry-certificate"></a>Vastuvõetud ELi kandesertifikaadi üleslaadimine

Kasutage ELi kliendi allkirjaga vastuvõetud ELi kandesertifikaadi üleslaadimiseks lehte **Manused**. Pärast sertifikaadi üleslaadimist saate seostada selle arvega, et tõendada kaupade tarnimist. See tõend on vajalik, kui peate väljastama arve, mis ei sisalda käibemaksu (KM), ja seda kasutatakse ka auditeerimise ajal.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Valikuline: arve sertifikaadi oleku ja printimisoleku uuendamine

Saate uuendada kliendiarve kandesertifikaadi olekut ja printimisolekut, kasutades lehte **Arve tööleht**.

## <a name="technical-information-for-system-administrators"></a>See teave on mõeldud süsteemi administraatoritele.
Kui teil pole juurdepääsu lehtedele, mida kasutatakse selle ülesande täitmiseks, pöörduge oma süsteemiadministraatori poole ja edastage järgmises tabelis antud andmed.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Kategooria</th>
<th>Eeltingimus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Turberollid ja kohustused</td>
<td>Kaupade või teenuste jaoks EL-i kandesertifikaatide häälestamiseks ja loomiseks peate kuuluma turberolli, mis hõlmab järgmisi kohustusi.
<ul>
<li><strong>Müügireskontro ametnik</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Klienditeeninduse esindaja</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Müügiametnik</strong> (TradeSalesClerk)</li>
<li><strong>Lähetusametnik</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>





