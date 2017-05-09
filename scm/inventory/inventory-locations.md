---
title: Lao asukohad
description: "Lao asukohti kasutatakse üldise ladustamisega (WMS I) määramiseks, kus kaubad on WMS I laos ladustatud ja kust need seal komplekteeritakse."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WMSLocation
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: cdf9eaeba076576d4adaa5fb5e18cd5a3f1c7b2d
ms.lasthandoff: 03/31/2017


---

# <a name="inventory-locations"></a>Lao asukohad

[!include[banner](../includes/banner.md)]


Lao asukohti kasutatakse üldise ladustamisega (WMS I) määramiseks, kus kaubad on WMS I laos ladustatud ja kust need seal komplekteeritakse.

See teema kehtib mooduli Varude haldus funktsioonide puhul. See ei kehti mooduli Laohaldus funktsioonidele.

Mõiste asukoht viitab kohale, kus kaupu hoiundatakse ja kust võetakse.

Iga asukoha puhul tuleb määrata ka koht, kuhu kaup paigutatakse. Vaikimisi on need samad. Tavaliselt paigutatakse ja luuakse kaubad asukoha samalt küljelt, kuid see pole alati nii. Näiteks need kaubad, mis on ladustatud aktiivses laoriiulis, sisestatakse ühele riiulireale, kuid tuuakse teiselt. Põhisisend antakse asukoha nime järgi, mis määratletakse tavaliselt selle koordinaatidega: laud, riiulirida, sektsioon, riiul ja koht. Selle nime või ID saab lehel Lao asukoht sisestada käsitsi või luua asukoha koordinaatide põhjal: näiteks 01-02-03-4, kui riiulirida on 1, sektsioon 2, riiul 3, koht 4.
Asukoha atribuudid
-------------------

Asukohal on järgmised tunnused:
-   Suurus (kõrgus, laius ja sügavus ja sellest tulenevalt maht)
-   Ladu, riiulirida, sektsioon, riiul ja koht.
-   Asukoha tüüp (hulgiasukoht, komplekteerimise asukoht, saabumisala, väljastusala, tootmissisendi asukoht, kontrolliasukoht või kanbani lõppladu)

Selleks et kontrollida, kas operaator on valinud konkreetse kauba jaoks õige asukoha, saab võrgusüsteemides kasutada kontrollteksti. Kontrollteksti võib luua kas käsitsi või valida vaikimisi.

## <a name="sort-codes"></a>Sortimiskoodid
Sortimiskoode kasutatakse varudest kaupade komplekteerimiseks vajalikku teavet (sh komplekteerimisjärjekord) kirjeldavate komplekteerimisridade töötlemiseks. Sortimiskoode saab määrata riiuliridade ja muude koordinaatide aluse või määrata asukohale käsitsi.

## <a name="blocked-locations"></a>Blokeeritud asukohad
Mõnikord on vaja näidata, et asukoht on teatud ajaks blokeeritud, näiteks paranduste võimaldamiseks. Mõnikord aga on vaja näidata ainult sissetuleku või väljamineku blokeerimist.
Puu struktuur
--------------

Lehel Lao asukohad saate vaadata lao paigutust puustruktuuril, tuginedes lao asukohtade koordinaatidele määratud kuvavormingus.
Lao asukohtade haldamine lao vormi kaudu
---------------------------------------------------

Asukohad saab kopeerida ühest laost teise ja asukohti luua viisardi abil. Enne viisardi käivitamist veenduge, et oleksite määratlenud lehel Ladu vaikeasukohtade nimed.



<a name="see-also"></a>Vt ka
--------

[Uue laopaigutuse loomine (tegevuse juhis)](https://ax.help.dynamics.com/en/wiki/create-a-new-warehouse-layout/)



