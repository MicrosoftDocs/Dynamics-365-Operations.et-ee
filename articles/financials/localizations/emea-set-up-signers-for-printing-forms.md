---
title: Prinditud vormide allkirjastajate seadistamine
description: "Juriidiliste isikute puhul Tšehhi Vabariigis, Eestis, Ungaris, Leedus, Lätis, Poolas ja Venemaal saate seadistada allkirjastajaid ja õigusi klientidele ning hankijatele, kes prindivad dokumente nagu arved ja kassaorderid."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 263464
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 51449f2f8448a493ebf7e4496cebdb90d902869a
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="set-up-signers-for-print-forms"></a>Prinditud vormide allkirjastajate seadistamine

[!INCLUDE [banner](../includes/banner.md)]

Juriidiliste isikute puhul Tšehhi Vabariigis, Eestis, Ungaris, Leedus, Lätis, Poolas ja Venemaal saate seadistada allkirjastajaid ja õigusi klientidele ning hankijatele, kes prindivad dokumente nagu arved ja kassaorderid.

<a name="set-up-default-values"></a>Vaikeväärtuste seadistamine
---------------------

Ettevõtte prinditavate dokumentide allkirjastajate seadistamiseks kasutage lehte **Ametiisikud**. Saate seadistada allkirjastajaid ja nende õigusi nii ettevõtte kui ka klientide või hankijate puhul, olenevalt dokumendi tüübist. Järgmises tabelis kirjeldatakse lehe **Ametiisikud** vahekaarte.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vahekaart</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Üldine</td>
<td>Lisage ametikohti ja seotud teavet allkirjastajate (direktor ja pearaamatupidaja) kohta, kes võivad kõikvõimalikke prinditud dokumente allkirjastada.</td>
</tr>
<tr class="even">
<td>Pearaamat</td>
<td>Lisage ametikoht ja seotud teave allkirjastajate kohta, kes võivad allkirjastada järgmisi rahavoogudega seotud ettevõttesiseseid finantsdokumente.
<ul>
<li>Kassaorderid</li>
<li>Ettemaksuaruanne</li>
<li>Kassaraamatu leht</li>
<li>Loendusväljavõte</li>
<li>Viitvõlad<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Müügitellimused</td>
<td>Lisage ametikohti ja seotud teavet allkirjastajate kohta, kes võivad allkirjastada järgmisi klientidega seotud väljaminevaid põhidokumente.
<ul>
<li>Maksearve</em></li>
<li>Arve</li>
<li>Faktuurarve<em></li>
<li>Arve – kreeditarve</li>
<li>Faktuurarve – kreeditarve</em></li>
<li>Maksukande faktuurarve (klient)<em></li>
</ul></td>
</tr>
<tr class="even">
<td>Ostutellimused</td>
<td>Lisage ametikohti ja seotud teavet allkirjastajate kohta, kes võivad allkirjastada järgmisi hankijatega seotud sissetulevaid põhidokumente.
<ul>
<li>Arve</li>
<li>Faktuurarve</em></li>
<li>Arve – kreeditarve</li>
<li>Faktuurarve – kreeditarve<em></li>
<li>Maksearve</em></li>
<li>Maksukande faktuurarve (hankija)<em></li>
</ul></td>
</tr>
<tr class="odd">
<td>Laokaupade haldus</td>
<td>Lisage ametikohti ja seotud teavet allkirjastajate kohta, kes võivad allkirjastada järgmisi laodokumente, kui kliendile väljastatakse või hankijalt saadakse materiaalseid varasid.
<ul>
<li>Väljasta müügitellimuse (M-15) saateleht</em></li>
<li>Korv. order / Sisset. order</li>
<li>Väljasta üleviimistellimuse (M-15) saateleht*</li>
</ul></td>
</tr>
</tbody>
</table>

\* See dokumendi tüüp on saadaval ainult juriidilistele isikutele, kelle esmane aadress on Venemaal. Järgmises tabelis kirjeldatakse lehe **Ametiisikud** välju.

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
<td>Ametikoht</td>
<td>Valige allkirjastaja ametinimetus.</td>
</tr>
<tr class="even">
<td>Nimi</td>
<td>Valige allkirjastaja nimi. Loendis olevad nimed tulevad kas tabelist Kontaktid või tabelist Töötajad, olenevalt allkirjastaja tüübist (st olenevalt sellest, kas märkeruut <strong>Meie</strong> on valitud). Kui allkirjastaja nime ei ole loendis, siis sisestage allkirjastaja täielik nimi käsitsi.</td>
</tr>
<tr class="odd">
<td>Ametinimetus</td>
<td>Valige allkirjastaja ametinimetus. Kui allkirjastaja ametinimetust pole loendis, siis sisestage allkirjastaja ametinimetus käsitsi.</td>
</tr>
<tr class="even">
<td>Konto kood</td>
<td>Valige, kas allkirjastaja saab allkirjastada kõiki valitud dokumenditüübiga dokumente või ainult konkreetse kliendi või hankija dokumente.</td>
</tr>
<tr class="odd">
<td>Konto seos</td>
<td>Valige kliendi või hankija konto, mis on seotud valitud konto koodiga. See väli on saadaval ainult siis, kui teete väljal <strong>Konto kood</strong> valiku <strong>Kirje</strong>.</td>
</tr>
<tr class="even">
<td>Meie</td>
<td>Valitud märkeruut näitab, et ametikoht on sisemine.</td>
</tr>
<tr class="odd">
<td>Seos laohoonega</td>
<td>Valige, kas allkirjastaja on määratud kõigile ladudele või ainult konkreetsele laole. Valikud on järgmised:
<ul>
<li><strong>Kõik</strong> – allkirjastaja on määratud kõigile ladudele.</li>
<li><strong>Kirje</strong> – allkirjastaja on määratud konkreetsele laole.</li>
</ul></td>
</tr>
<tr class="even">
<td>Ladu</td>
<td>Valige lao kood, mis vastab laole, millele allkirjastaja määratud on. See väli on saadaval ainult siis, kui teete väljal <strong>Seos laoga</strong> valiku <strong>Kirje</strong>.</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-number-sequence-code-for-officials"></a>Ametiisikute numbriseeria häälestamine
Saate määrata numbriseeria koodi ametiisikutele lehe **Juriidilised isikud** jaotises **Numbriseeriad**. Valige viitele **Ametiisikute seansi ID** numbriseeria kood.

## <a name="modify-signers-in-primary-documents"></a>Põhidokumentidel allkirjastajate muutmine
Ametiisikute funktsioon näitab vaikimisi eelmääratud allkirjastajaid tabelis Ametiisikud. Lehel **Arve sisestamine** vahekaardil **Ametiisikud** saate muuta allkirjastaja nime ja ametinimetust põhidokumendil järgmiste dokumenditüüpide puhul.

-   Kliendiarve
-   Hankija arve
-   Lähetuse üleviimistellimus
-   Kassaorder

**Märkus:** pärast dokumendi sisestamist ei saa ametiisikuid muuta.




