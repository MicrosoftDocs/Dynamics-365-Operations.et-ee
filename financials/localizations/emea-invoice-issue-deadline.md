---
title: "Arve väljastamise tähtaeg"
description: "Selles artiklis kirjeldatakse, kuidas seadistada parameetreid kliendiarvete ja hankijaarvete väljastamistähtaegade arvutamiseks Euroopa Liidus (ELis)."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10923
ms.assetid: 64ea3343-df94-4a52-b839-6328c8a282bd
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 6121be0dd02659e4e8466b0c1381678be64fefc2
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-issue-deadline"></a>Arve väljastamise tähtaeg

Selles artiklis kirjeldatakse, kuidas seadistada parameetreid kliendiarvete ja hankijaarvete väljastamistähtaegade arvutamiseks Euroopa Liidus (ELis).

Euroopa Liidu (EL) direktiiv 45/2010 ja muud direktiivid nõuavad, et ELi-siseste saadetiste eest tuleb esitada arve enne tarnele järgneva kuu viieteistkümnendat kuupäeva. Samas võivad igal ELi riigil olla kodumaiste tarnete puhul erinevad arve esitamise tähtajad. Arve väljastamise tähtaja funktsiooni abil saate sobitada kuupäevavahemiku riigi/regiooni tüübiga. Seejärel arvutatakse kõigi konkreetset tüüpi riiki/regiooni saadetavate või sealt lähetatavate saadetiste arve väljastamise tähtaeg, kasutades määratud kuupäevavahemikus määratud reegleid. Lisaks on võimalik saada kõik konkreetse arve väljastamise tähtajaga saatelehed, filtreerida perioodiliste müügiarvete esitamisel arve väljastamise tähtaja alusel ja kontrollida müügiarve väljastamise kuupäeva arve sisestamise ajal. Saate seadistada kuupäevavahemiku koodi ja seejärel saate seadistada arve väljastamise kuupäeva arvutusreegli, määrates kuupäevavahemiku koodi riigi/regiooni tüübile. Arvutusreeglit kasutatakse arvete väljastamise tähtaja arvutamiseks järgmiste kannete puhul.

-   ELi-sisesed saadetised
-   Riigisisesed saadetised ELi liikmesriigis

Saate seadistada ka kuupäeva juhtelemendid, mis aitab tagada, et kliendiarved ja kreeditarved kliendi kannete puhul luuakse määratud perioodil pärast tarnet.

## <a name="prerequisites"></a>Eeltingimused 
Järgmises tabelis on eeltingimused, mis peavad olema täidetud, enne kui arve väljastamise tähtaja funktsiooni kasutada saab.

| Kategooria            | Eeltingimus                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Riik/regioon      | Juriidilise isiku peamine aadress peab olema ELi liikmesriigis.                                                                                                                                                                                                                                                                                                                    |
| Seostuvad seadistustoimingud | Seadistage lehel **Kuupäevavahemikud** kuupäevavahemik, mida kasutatakse arve väljastamise tähtaja arvutamisel. (Klõpsake **kasutatava**&gt;**Pearaamatu seadistamine**&gt;**tänaseks järel**.) Kohta ning **väliskaubanduse parameetrid** lehele, luua väliskaubanduse atribuudid mõnes riigis või piirkonnas. (Klõpsake **maksu**&gt;**install**&gt;**väliskaubanduse**&gt;**väliskaubanduse parameetrid**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Arve väljastamise tähtaja arvutusreegel
Lehel **Arve väljastamise tähtaja arvutuse seadistamine** saate seadistada arve väljastamise tähtaja arvutusreegli, määrates riigi/regiooni tüübile kuupäevavahemiku koodi.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Kuupäeva juhtelemendi parameetrite seadistamine kliendiarvete ja kreeditarvete jaoks
Saate seadistada kuupäeva juhtelemendi parameetrid, mis aitab tagada, et kliendiarved ja kreeditarved kliendi kannete puhul luuakse määratud perioodil pärast tarnet. Leiate need parameetrid alalt **Arve kuupäevade juhtelement** lehel **Müügireskontro parameetrid**.

## <a name="example"></a>Näide
Saate seadistada Microsoft Dynamics 365 operatsioonide arvutamiseks arve väljastamisest otse kuupäevad-Siseste lähetuste tarne toimetatakse järgneva kuu viieteistkümnendat, luua kuupäeva intervalli koodi ja arvutamise reeglit on järgmised sätted.

### <a name="date-interval-code"></a>Kuupäevaintervalli kood

| Väli                                                           | Väärtus                           |
|-----------------------------------------------------------------|---------------------------------|
| Kuupäevaintervalli kood                                              | 15-NM                           |
| Kirjeldus                                                     | Järgmise kuu viieteistkümnes kuupäev |
| Enne (väljagrupis **Kuni kuupäevani**)                         | Kuu                           |
| Algus/lõpp (väljagrupis **Kuni kuupäevani**)                      | Lõpp                             |
| +/- (väljagrupis **Kuni kuupäevani**)                            | 15                              |
| Päevad, kuud, aastad või perioodid (väljagrupis **Kuni kuupäevani**) | Päevi                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Arve väljastamise tähtaja arvutusreegel

| Väli               | Väärtus                                                     |
|---------------------|-----------------------------------------------------------|
| Riigi/regiooni tüüp | **EL**                                                    |
| Alguskuupäev          | Sisestage kuupäev, millal see seadistuse rida jõustub. |
| Kuupäevaintervalli kood  | **15-NM**                                                 |

## <a name="next-steps"></a>Järgmised sammud
Pärast seda, kui olete lõpetanud parameetrite seadistamise arve väljastustähtaegade arvutamiseks, saate luua ja sisestada järgmisi kandeid arvete väljastustähtaegade automaatseks arvutamiseks ja uuendamiseks.

-   **Müügitellimused** – kui loote müügitellimuse ja sisestate saatelehe, arvutatakse arve väljastustähtaeg ja see uuendatakse saatelehel. Tähtaeg arvutatakse kuupäevaintervalli, mis on seotud selle riigi määratud müügitellimuse tarneaadress. Pärast selle saatelehe sisestamist saate kontrollida arve väljastamisest tähtajaga on **arve väljastamise tähtaeg** sisse-välja ning **saatelehe tööleht** lehekülg. (Klõpsake **müügi- ja**&gt;**Müügitellimus**&gt;**tellida saatmine**&gt;**saatelehe**.) Saate vaadata kõigi saatelehtede, ei ole arvel ja arve väljastamisest õigeaegselt edasi ning **saatelehtede arveldamata** lehel. (Klõpsake **müügi- ja**&gt;**Müügitellimus**&gt;**tellida saatmine**&gt;**saatelehtede arveldamata**.)
-   **Ostutellimused** – kui loote ostutellimuse ja sisestate toote sissetuleku, arvutatakse arve väljastustähtaeg ja see uuendatakse toote sissetulekul. Tähtaeg arvutatakse kuupäevavahemiku alusel, mis on seotud hankija peamise aadressi riigiga/regiooniga. Pärast toote sissetuleku sisestamist saate kontrollida arve väljastamise tähtaega lehe **Toote sissetuleku tööleht** väljal **Arve väljastamise tähtaeg**. (Klõpsake **hanke ja mis hangivad**&gt;**ostutellimuste**&gt;**kes kauba vastu**&gt;**toote sissetulek**.) Kuvatakse toote kõik laekumised, mis ei ole arveldatud ja arve väljastamisest õigeaegselt edasi ning **toote sissetulekute arveldamata** lehel. (Klõpsake **hanke ja mis hangivad**&gt;**ostutellimuste**&gt;**kes kauba vastu**&gt;**toote sissetulekute arveldamata**.)

## <a name="technical-information-for-system-administrators"></a>See teave on mõeldud süsteemi administraatoritele.
Kui teil pole juurdepääsu lehtedele, mida selles artiklis nimetatud ülesannete täitmiseks kasutatakse, pöörduge oma süsteemiadministraatori poole ja edastage järgmises tabelis antud andmed.

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
<td>Konfiguratsioonivõtmed</td>
<td>Klõpsake <strong>süsteemi halduse</strong>&gt;<strong>install</strong>&gt;<strong>Licensing</strong>&gt;<strong>litsents konfiguratsiooni</strong>. Klõpsake konfiguratsioonivõtit <strong>Pearaamat</strong>.</td>
</tr>
<tr class="even">
<td>Turberollid ja kohustused</td>
<td>Selle ülesande sooritamiseks peate olema turberolli liige, mis hõlmab järgmisi kohustusi.
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (arve ja sularahaprotsessi lubamine)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (arve ja makseprotsessi lubamine)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Turberollid ja privileegid</td>
<td>Selle ülesande sooritamiseks peate olema turberolli liige, mis hõlmab järgmisi privileege.
<ul>
<li><strong>CustPackingSlipJournalView</strong> (müügisaatelehtede vaatamine)</li>
<li><strong>VendPackingSlipJournalView</strong> (toote sissetulekute töölehe kuvamine ostutellimuses)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (arve väljastustähtaegade arvutamine)</li>
</ul></td>
</tr>
</tbody>
</table>




