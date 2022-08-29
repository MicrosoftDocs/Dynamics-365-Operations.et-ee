---
title: Pearaamatu kannete sisemiste andmete redigeerimise lubamine
description: See artikkel annab teavet selle kohta, kuidas redigeerida pearaamatukannete siseandmeid.
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 26fc6518f0b4eae815e047db1dbaadd7c56a2e67
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220714"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>Pearaamatu kannete sisemiste andmete redigeerimise lubamine

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]


Raamatupidamiskirjete pearaamatusse sisestamisel kasutatakse välja Kirjeldus **sageli** sisemiste märkuste või dokumentatsiooni talletamiseks. Kui teave on vale, võib see põhjustada segadust ja muuta perioodi lõpu sulgemise keerukamaks. See funktsioon võimaldab raamatupidamisjuhil või raamatupidamise ülevaatajal **parandada** vigu, redigeerides välja Kirjeldus sisestatud kannetel pearaamatus.

Pearaamatusse sisestatud kannete muudatused on piiratud sisemise iseloomuga andmetega. See funktsioon ei luba teil kunagi redigeerida andmeid, nt summasid, sisestuskuupäevi, pearaamatukontosid ja kandevaluutat. Muudatused selles andmetes mõjutavad finantsaruannete välist aruandlust ja tuleb teha ainult uute pearaamatukannete kaudu.

> [!NOTE]
> Dynamics 365 finantsversiooni 10.0.29 puhul on see funktsioon piiratud välja Kirjeldus **redigeerimistega**.

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>Pearaamatukannete siseandmete redigeerimine

Enne pearaamatukannete sisemiste andmete redigeerimist peate **lubama funktsioonihalduse tööruumis** **funktsiooni** Luba pearaamatukannete siseandmete redigeerimist.
Kui funktsioon on lubatud, tuleb sisestatud kandeid redigeeriv kasutaja määrata raamatupidamise haldajale või raamatupidamise ülevaataja rollile. Saate lisada õigusi ka teistele rollidele, kohandades turberolle.

Redigeerimisprotsess on lubatud ainult leheküljel Kande kanded.

1. Minge pearaamatu **päringute ja** > **aruannete kandekannetesse** > **·**.
2. **Dialoogiboksis SysQuery** sisestage kannete valimiseks otsingukriteeriumid.
3. Valige nende kannete read, mida soovite redigeerida, ja seejärel valige **käsk Redigeeri** > **kande sisemisi kandeandmeid**.

    [![Kande kanneteleht.](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
**Iga valitud rea kohta** kuvatakse sisemise kande andmelehel järgmised andmed:
  
  - Pearaamatukonto
  - Konto nimi
  - Vautšer
  - Praegune kirjeldus
  - Uus kirjeldus

    [![Töölehe kanne.](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> Redigeerida **saab ainult** välja Uus kirjeldus. Vaikimisi vastab väärtus välja Praegune kirjeldus **väärtusele**, nii et saate kirjelduses vead kiiresti parandada.

4. Muutke iga **rea** välja Uus kirjeldus või kustutage kirjeldus igalt realt.

   Teise võimalusena, kui mitu rida tuleb värskendada sama väärtusega, järgige neid samme:

      1. Valige redigeeritav rida ja seejärel valige valitud **kirjete hulgivärskendus**.
      2. **Valige redigeeritav väli** väljal Redigeeritav väli. Praegu sisaldab otsing ainult välja **Uus** kirjeldus.
      3. **Sisestage väljale** Uus väärtus uus kirjeldus.
      4. Tehke valik **Värskenda**. Kõik valitud kirjed uuendatakse uue väärtusega.

      [![Valitud kirjete hulgivärskenduse dialoogiboks.](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. **Väljale Redigeerimise põhjus** sisestage märkus, mis selgitaks redigeerimist. See märkus kuvatakse lehel **Kannete redigeerimiste kontrolljälg**.

   Sama kandega saab teha mitu redigeerimist ja iga redigeerimist jälgitakse.

## <a name="audit-trail-of-voucher-edits"></a>Kande redigeerimise kontrolljälg

Kontrolljälge säilitatakse konkreetselt selle funktsiooni kaudu tehtud muudatuste jälgimiseks. Pääsete juurde kande redigeerimise kontrolljäljele kahel viisil:

  - Minge pearaamatu **päringute ja** > **aruannete kandekannetesse** > **·**. Kande päringute lehel valige kande redigeerimise **kande** kontrolljälje redigeerimine **.** > **·** Kontrolljälg kuvatakse ainult valitud kandekirje kohta. 
   
    Päringut avades saate keskenduda kõigile ühele kandekirjele tehtud redigeerimistele.
  
  - Minge pearaamatusse** > kannete **redigeerimiste** > **perioodiliste ülesannete kontrolljälg**. Sisestage dialoogiboksis kriteeriumid kannete määramiseks, mille kohta soovite vaadata redigeerimiste kontrolljälge. Kõigi kannete kontrolljälje vaatamiseks jätke kriteeriumid tühjaks ja valige **OK**. 
    
    Päringut avades saate filtreerida kindlal kuupäeval või konkreetsel kasutajal tehtud muudatusi.

Lehekülje **Redigeerimiste kontrolljälg** näitab järgmist teavet:

- **Loomise kuupäev ja** kellaaeg – redigeerimise kuupäev ja kellaaeg.
- **Muutmise põhjus** – põhjus, miks kasutaja redigeerimise sisestas.
- **Loodud** – redigeerimise teinud kasutaja.

Iga kontrolljälje üksikasjade vaatamiseks minge süvitsi väärtusega **Loodud kuupäev ja** kellaaeg. Lehel **Kuva redigeeritud kande** atribuudid kuvatakse sama teave nagu algsel redigeerimislehel, k.a eelmine kirjeldus ja uuendatud kirjeldus.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
