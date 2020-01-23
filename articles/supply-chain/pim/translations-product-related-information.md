---
title: Tootega seotud tõlgete KKK
description: Selles teemas kirjeldatakse tõlkeid toote atribuutide tooted ja dimensiooniväärtuste haldamiseks.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysTranslationDetail, SysTranslationLanguage, SysTranslationList, EcoResProductListPage, EcoResProductVariants, EcoResProductDetailsExtended, EcoResProductCreate, EcoResProductDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 201853
ms.assetid: c0286bba-f54b-42de-904c-81fd796bdd1d
ms.search.region: global
ms.search.industry: Product information
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3d7405af3d0de08cb376164f4ecf59b1d0ef3d4
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934719"
---
# <a name="product-related-translations-faq"></a>Tootega seotud tõlgete KKK

[!include [banner](../includes/banner.md)]

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

## <a name="how-do-i-create-translations-for-product-related-information"></a>Kuidas luua tootega seotud teabe tõlkeid?
Tootele tõlke loomiseks tehke järgmist.
1.  Klõpsake valikuid **Tooteteabe haldus** &gt; **Üldine** &gt; **Väljastatud tooted**.
2.  Valige toode ja klõpsake tegumiribal grupis **Keeled** nuppu **Tõlked**.
3.  Valige lehel **Teksti tõlge** väljal **Keel** soovitud keel. Keelte juurde lisamiseks laiendage välja **Keel** ja klõpsake seejärel **OK**.
4.  Grupis **Tõlgitud tekst** sisestage tõlked väljadele **Kirjeldus** ja **Toote nimi**.

Tooteatribuutidele tõlke loomiseks tehke järgmist.
1.  Klõpsake valikuid **Tooteteabe haldus** &gt; **Üldine** &gt; **Väljastatud tooted**.
2.  Jaotises **Seadistus** klõpsake valikut **Atribuudid** ja seejärel valikut **Atribuudid**.
3.  Lehel **Atribuudid** klõpsake valikut **Tõlgi**.
4.  Valige lehel **Teksti tõlge** väljal **Keel** soovitud keel. Keelte juurde lisamiseks laiendage välja **Keel** ja klõpsake seejärel **OK**.
5.  Grupis **Tõlgitud tekst** sisestage tõlked väljadele **Kirjeldus**, **Hüüdnimi** ja **Spikri tekst**.

Tootedimensiooni atribuutidele tõlke loomiseks tehke järgmist.
1.  Klõpsake valikuid **Tooteteabe haldus** &gt; **Üldine** &gt; **Väljastatud tooted**.
2.  Valige toode ja seejärel klõpsake valikut **Tootedimensioonid**.
3.  Valige üks tootedimensioonide linkidest: **Konfiguratsioonid**, **Suurused**, **Värvid** või **Stiil**.
4.  Valige dimensiooni väärtus ja klõpsake valikut **Tõlgi** .
5.  Valige lehel **Teksti tõlge** väljal **Keel** soovitud keel. Keelte juurde lisamiseks laiendage välja **Keel** ja klõpsake seejärel **OK**.
6.  Grupis **Tõlgitud tekst** sisestage tõlked väljadele **Nimi** ja **Kirjeldus**.

## <a name="can-the-names-of-product-variants-be-translated"></a>Tootevariantide nimed tõlgitakse?
Tootevariandid põhinevad väljastatud toote dimensioonidel. Tootevariantide nimed põhinevad tootedimensiooni väärtuste kombinatsioonil. Kui tõlgitakse seostatud toote variandi dimensiooniväärtused, kuvatakse tõlgitud versiooni tootevariandi nimi.  

**Näide**  

Toode on saadaval erineva suurusega ja värvi t-särk ja tootevariandi nimesid põhinevad järgmised andmed:
-   Toote number: \#3
-   Dimensioonide: Suurus ja värv
-   Dimensiooniväärtuste suurus: väike, Keskmine, suur
-   Dimensiooniväärtuste värvi: punane, roheline, must

Dimensiooniväärtustel Väike ja Punane põhinev tootevariandi nimi on **\#3:Väike:Punane**.  

Klient soovib osta mõned väikesed, punane t-särgid ja t-särgi nimi peab arvele prantsuse keeles. Tõlgite dimensiooniväärtused (Väike ja Punane) prantsuse keelde ja tootevariandi nimi on **\#3:Petit:Rouge**.
<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Näpunäide</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kliendi eelistatud keel toimige järgmiselt.
<ol><br/><li>Klõpsake valikuid <strong>Müük ja turundus</strong> &gt; <strong>Üldine</strong> &gt; <strong>Kliendid</strong> &gt; <strong>Kõik</strong> <strong>kliendid</strong>.</li>
<li>Topeltklõpsake klienti, et avada leht <strong>Kliendid</strong> . Vahekaardil <strong>Üldine</strong> väljal <strong>Keel</strong> valige soovitud <strong>keel</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="what-happens-if-a-customer-has-a-preferred-language-for-which-no-translations-are-available"></a>Mis juhtub, kui kliendil on eelistatud keel kohta pole tõlge on olemas?
Kliendi eelistatud keel puuduvad tõlked, kui kuvatakse globaalse keele oma ettevõtte nimed ja kirjeldused.

## <a name="can-i-manage-translations-for-a-series-of-dimension-values-at-the-same-time"></a>Hallata tõlked rea dimensiooniväärtused samal ajal?
Saate hallata dimensiooniväärtuste iga toote tõlked dimensiooniväärtused on tootepõhine. Kui väärtus grupi looge dimensioonigrupp väärtuse ja väärtuste tõlked on lihtsam hallata tõlkeid.   

**Näide**  

Teie ettevõte toodab erineva stiiliga T-särke ja iga stiil on saadaval suurustes väike, keskmine ja suur. Üks dimensioonigrupp väärtus kogutakse suurused. Uue t-särk laadi lisamisel saate seostada seda dimensiooni väärtus grupiga, mida kasutatakse suurused, nii, et kõik suurused on toote. Saate lisada või suuruse väärtus dimensioonigruppi tõlgete igal ajal muuta.  

Variandi tootegrupist tuleb säilitada toote variandi dimensioonigrupp kaudu seotud dimensiooniväärtuse.   
Dimensiooni väärtustegrupi loomiseks tehke järgmist.
1.  Klõpsake valikuid **Tooteteabe haldus** &gt; **Seadistus** &gt; **Variandi grupid**.
2.  Valige **Suurus** **grupid**, **Värvigrupid** või **Stiiligrupid**.
3.  Klõpsake valikut **Uus** ja seejärel sisestage grupi nimi väljale **Suuruse** **grupp**, **Värvigrupp** või **Laadigrupp**. Klõpsake valikuid **Suurused**, **Värvid** või **Stiilid**, et luua gruppide jaoks read.
4.  Lehel **Suuruse** **grupi** read, **Värvi** **grupi** **read** või **Laadigrupi read** klõpsake nuppu **Uus** ja seejärel looge gruppidele suurused, värvid ja laadid.

Dimensioonigrupp väärtus väärtuste tõlked haldamiseks toimige järgmiselt:
1.  Järgige eelmist protseduuri dimensiooniväärtuse grupi loomise kohta, et avada leht **Suurusgrupi read**, **Värvigrupi read** või **Stiiligrupi read**.
2.  Klõpsake valikut **Teksti tõlge**. Lehel **Teksti tõlge** grupis **Tõlgitud tekst** sisestage tõlked väljadele **Nimi** ja **Kirjeldus**.

## <a name="when-can-translations-of-product-related-information-be-managed"></a>Kui teabe tõlked hallatud?
Tootega seotud teabe tõlkeid saab mis tahes ajal hallata. Dimensiooniväärtuse seostatud toote tõlked uuendamisel uuendatakse tootekirjelduse sõltumata sellest, kas toode on kandeid.





