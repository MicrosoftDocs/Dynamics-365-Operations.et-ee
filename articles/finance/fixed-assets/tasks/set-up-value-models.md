---
title: Väärtusmudelite seadistamine
description: See protseduur näitab, kuidas luua uut põhivara raamatut ja seostada seda põhivaragrupiga.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be3b5578bd6509859c36f6a50ea9730e9ef1780e
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890708"
---
# <a name="set-up-value-models"></a>Väärtusmudelite seadistamine

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

See protseduur näitab, kuidas luua uut põhivara raamatut ja seostada seda põhivaragrupiga.

## <a name="create-a-book"></a>Raamatu loomine
1. Avage **põhivarade \>\> seadistusraamatud**.
2. Valige suvand **Uus**.
3. Sisestage **väärtus** väljale Raamat.
4. Sisestage väärtus väljal **Kirjeldus**.
5. Seadke valiku **Arvuta kulum** väärtuseks **Jah**.

    Kui valiku **Arvuta** kulum väärtuseks on seatud **Jah**, kaasatakse seostatud vararaamat kulumisoovi hulka. Kui see on seatud **väärtusele** Ei, siis ei amortiseerita põhivararaamatut automaatselt.

6. Sisestage **või valige väärtus väljal** Kulumireeglid.

    * Alternatiivne kulumireegel on tuntud ka kui kulumi ümberlülitusmeetod. Kulumisoovitus lülitub sellele reeglile, kui alternatiivne reegel arvutab kulumi summa, mis on vaikimisi kulumireegliga võrdne või sellest suurem.
    * Plaaniväliseid kulumireegleid kasutatakse vara täiendava kulumi arvestamiseks ebatavalistes olukordades. Näiteks võite seda kasutada loodusõnnetusest tuleneva kulumi registreerimiseks.
    * Kui valite valiku Loo kulumi korrigeerimised koos aluse korrigeerimistega, luuakse kulumi korrigeerimised põhivara **väärtuse** uuendamisel automaatselt. Muul juhul mõjutab uuendatud vara väärtus ainult tulevasi kulumiarvutusi.

7. Seadke **valikuLe Jah valikuga Kulumi** korrigeerimiste loomine koos aluse **korrigeerimistega.**

    * Vaikimisi sisestatakse põhivararaamatu kanded pearaamatusse. Kuid saate keelata raamatu sisestamise pearaamatusse, seadistades suvandi Sisesta pearaamatusse **valikule** **Ei**. Pearaamatusse sisestamata raamatuid kasutatakse tavaliselt maksuaruandluses. See valik võimaldab teil paindlikum kustutada vararaamatu ajaloolised kanded, sest kandeid pole pearaamatusse kinnitatud.
    * Kui raamat sisestatakse pearaamatusse, on välja Sisestamiskiht väärtuseks vaikimisi määratud Praegune kiht, kui raamat sisestatakse pearaamatusse, ning väärtus Pole, kui raamatut pearaamatusse **ei** **·** **sisestata**. Saate uuendada välja **Sisestuskiht** väärtuse, kui selle raamatu kanded tuleks sisestada teise kihti.

8. Arvutage positiivne kulum.

    * Vaikimisi on valiku **Arvuta positiivne** kulum väärtuseks **seatud** Ei. See säte näitab, et kulum kreditb valitud vararaamatut. Lisaks on mõlemaks valikuks Lubatud soetusmaksumusest kõrgemad raamatupidamislik jääkväärtus ja Luba negatiivsed raamatupidamislik jääkväärtuse valikud valikuid Ei ning sätteid **saab** **·** **sõltumatult** muuta. 
    * Positiivse kulumi arvutamiseks määrake suvandi Arvuta **positiivne** kulum väärtuseks **Jah**. See säte näitab, et kulum debiteerib põhivararaamatut. Kui suvand Arvuta positiivne kulum on seatud väärtusele Jah, seatakse suvand Luba soetusmaksumusest kõrgemat raamatupidamislik jääkväärtust ja Luba negatiivset raamatupidamislik jääkväärtust automaatselt väärtusele Jah ja **need** **·** **·** **·** **lukustatakse**. See lukk aitab tagada, et positiivset kulumit rakendatakse ainult põhivarale, mis soetatud negatiivse raamatupidamisväärtusega (kreedit). 

10. Sisestage **või** valige väärtus väljal Kalender.

    Tuletatud raamatud sisestavad kandeid korraga erinevatesse raamatutesse. Loote kanded peamises raamatus ja sisestamise ajal sisestatakse kande täpne koopia tuletatud raamatusse. Tuletatud raamatu kandeid ei arvutata ümber, seega ei tohiks seda kulumikannete jaoks kasutada.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Raamatu seostamine põhivaragrupiga

1. Valige **põhivaragrupid**.
2. Väljale **Põhivara grupp** sisestage või valige väärtus.
3. Väljale **Tööiga** sisestage number.

    * Kulumiperioodid arvutatakse pärast vara tööea sisestamist.
    * Kulumiarvestusreeglit saab maksuarvestuse jaoks vajalikul viisil seadistada.
    * Rendiga seostatud põhivarade puhul alistatakse välja Tööiga väärtuse vararaamatus ja vara kasulikus tööeal rendiperioodist **väiksem** väärtus. Kui omandiõiguse üleandmise valik on liisinguraamatus seatud väärtusele Jah, on välja Kasulik eluiga väärtus **alati** vara **kasulik** **eluiga**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
