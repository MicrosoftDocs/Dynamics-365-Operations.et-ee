---
title: "Ravimi tõlked FAQ"
description: "Selles teemas kirjeldatakse tõlkeid toote atribuutide tooted ja dimensiooniväärtuste haldamiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a9c991a5afaebd10b8812dfc1d67120ed4ebdfd2
ms.lasthandoff: 03/31/2017


---

# <a name="product-related-translations-faq"></a>Ravimi tõlked FAQ

Selles teemas kirjeldatakse tõlkeid toote atribuutide tooted ja dimensiooniväärtuste haldamiseks. 

<a name="what-product-related-data-can-be-translated"></a>Seotud andmete tõlgitakse?
--------------------------------------------

Saate luua tõlgete seotud järgmist:
-   Nimed ja kirjeldused tooted.
-   Kirjelduse, nimede ja toote atribuudiväärtuste spikriteksti.
-   Tootedimensiooni väärtuste nimed ja kirjeldused.

Saate tõlkida tootega seotud teavet mis tahes keelde, mis on lehel **Teksti tõlge** saadaval. Lisateavet leiate järgmisest jaotisest **Kuidas luua tõlkeid tootega seotud teabe kohta**.

## <a name="where-can-i-view-the-translated-information"></a>Kui saate vaadata teisendatud teavet?
Saate vaadata mis tahes välise dokumendi, nt arve, mis kasutab keelt, kui tõlge on olemas tõlked seotud teave.

## <a name="how-do-i-create-translations-for-productrelated-information"></a>Kuidas luua tõlked productrelated saamiseks?
Tootele tõlke loomiseks tehke järgmist.
1.  Klõpsake **toote teabekorraldus**&gt;**levinud**&gt;**vabastatud toodete**.
2.  Valige toode, ja Updatehagi paani ja selle **keeles** nuppu **tõlked**.
3.  Valige lehel **Teksti tõlge** väljal **Keel** soovitud keel. Keelte lisamiseks laiendada selle **keele** väljale ja seejärel klõpsake **OK**.
4.  Grupis **Tõlgitud tekst** sisestage tõlked väljadele **Kirjeldus** ja **Toote nimi**.

Tooteatribuutidele tõlke loomiseks tehke järgmist.
1.  Klõpsake **toote teabekorraldus**&gt;**levinud**&gt;**vabastatud toodete**.
2.  Jaotises **Seadistus** klõpsake valikut **Atribuudid** ja seejärel valikut **Atribuudid**.
3.  Lehel **Atribuudid** klõpsake valikut **Tõlgi**.
4.  Valige lehel **Teksti tõlge** väljal **Keel** soovitud keel. Keelte lisamiseks laiendada selle **keele** väljale ja seejärel klõpsake **OK**.
5.  Grupis **Tõlgitud tekst** sisestage tõlked väljadele **Kirjeldus**, **Hüüdnimi** ja **Spikri tekst**.

Tootedimensiooni atribuutidele tõlke loomiseks tehke järgmist.
1.  Klõpsake **toote teabekorraldus**&gt;**levinud**&gt;**vabastatud toodete**.
2.  Valige toode ja seejärel klõpsake valikut **Tootedimensioonid**.
3.  Valige üks tootedimensioonide linkidest: **Konfiguratsioonid**, **Suurused**, **Värvid** või **Stiil**.
4.  Valige dimensiooni väärtus ja klõpsake valikut **Tõlgi** .
5.  Valige lehel **Teksti tõlge** väljal **Keel** soovitud keel. Keelte lisamiseks laiendada selle **keele** väljale ja seejärel klõpsake **OK**.
6.  Aastal ning **tõlgitud teksti** rühm, sisestage tõlked on **nimi** ja **kirjeldus** väljad.

## <a name="can-the-names-of-product-variants-be-translated"></a>Tootevariantide nimed tõlgitakse?
Tootevariandid põhinevad väljastatud toote dimensioonidel. Tootevariantide nimed põhinevad tootedimensiooni väärtuste kombinatsioonil. Kui tõlgitakse seostatud toote variandi dimensiooniväärtused, kuvatakse tõlgitud versiooni tootevariandi nimi.  

**Näide**  

Toode on saadaval erineva suurusega ja värvi t-särk ja tootevariandi nimesid põhinevad järgmised andmed:
-   Tootekood: \#3
-   Dimensioonide: Suurus ja värv
-   Dimensiooniväärtuste suurus: väike, Keskmine, suur
-   Dimensiooniväärtuste värvi: punane, roheline, must

Toote variandi, mis põhineb dimensiooni nimi väärtused väike ja punane on **\#3:Small:Red**.  

Klient soovib osta mõned väikesed, punane t-särgid ja t-särgi nimi peab arvele prantsuse keeles. Te teisendada, väike ja punane, prantsuse keelde ja toote variandi nimi on **\#3: Petit: Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Tip</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kliendi eelistatud keel toimige järgmiselt.
<ol>  
<li>Klõpsake <strong>müügi- ja</strong>&gt;<strong>levinud</strong>&gt;<strong>hotelli</strong>&gt;<strong>kõik</strong> <strong>hotelli</strong>.</li>
<li>Topeltklõpsake klienti, et avada leht <strong>Kliendid</strong> . Vahekaardil <strong>Üldine</strong> väljal <strong>Keel</strong> valige soovitud <strong>keel</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Mis juhtub, kui kliendil on eelistatud keel kohta pole tõlge on olemas?
Kliendi eelistatud keel puuduvad tõlked, kui kuvatakse globaalse keele oma ettevõtte nimed ja kirjeldused.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Hallata tõlked rea dimensiooniväärtused samal ajal?
Saate hallata dimensiooniväärtuste iga toote tõlked dimensiooniväärtused on tootepõhine. Kui väärtus grupi looge dimensioonigrupp väärtuse ja väärtuste tõlked on lihtsam hallata tõlkeid.   

**Example**  

Teie ettevõte toodab erineva stiiliga T-särke ja iga stiil on saadaval suurustes väike, keskmine ja suur. Üks dimensioonigrupp väärtus kogutakse suurused. Uue t-särk laadi lisamisel saate seostada seda dimensiooni väärtus grupiga, mida kasutatakse suurused, nii, et kõik suurused on toote. Saate lisada või suuruse väärtus dimensioonigruppi tõlgete igal ajal muuta.  

Variandi tootegrupist tuleb säilitada toote variandi dimensioonigrupp kaudu seotud dimensiooniväärtuse.   
Dimensiooni väärtustegrupi loomiseks tehke järgmist.
1.  Klõpsake **toote teabekorraldus**&gt;**install**&gt;**Variant sõprade**.
2.  Valige **Suurus****grupid**, **Värvigrupid** või **Stiiligrupid**.
3.  Klõpsake **uus**, ja seejärel sisestage grupi nimi on **suurus****rühma**, **värvi rühma**, või **laad** välja. Klõpsake valikuid **Suurused**, **Värvid** või **Stiilid**, et luua gruppide jaoks read.
4.  Linnas on **suurus****rühma** read, **värvi****rühma****read**, või **read stiilis** klõpsake valikul **uus**, ja looge suurused, värvid ja stiilid gruppidele.

Dimensioonigrupp väärtus väärtuste tõlked haldamiseks toimige järgmiselt:
1.  Järgige eelmist protseduuri dimensiooniväärtuse grupi loomise kohta, et avada leht **Suurusgrupi read**, **Värvigrupi read** või **Stiiligrupi read**.
2.  Klõpsake valikut **Teksti tõlge**. Aastal ning **teksti tõlge** lehekülg, mis on **tõlgitud teksti** rühm, sisestage tõlked on **nimi** ja **kirjeldus** väljad.

## <a name="when-can-translations-of-productrelated-information-be-managed"></a>Kuna tõlked productrelated teavet hallata?
Tootega seotud teabe tõlkeid saab mis tahes ajal hallata. Dimensiooniväärtuse seostatud toote tõlked uuendamisel uuendatakse tootekirjelduse sõltumata sellest, kas toode on kandeid.




