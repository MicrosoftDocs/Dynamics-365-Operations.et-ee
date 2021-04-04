---
title: teenustellimuste loomine käsitsi
description: Hooldustellimusi saate luua käsitsi hoolduslepete või vormi **Hooldustellimused** abil.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b600bc59119a6304fa043240a34051435f8691
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470949"
---
# <a name="create-service-orders-manually"></a>teenustellimuste loomine käsitsi    

[!include [banner](../includes/banner.md)]


Hooldustellimusi saate luua käsitsi hoolduslepete või vormi **Hooldustellimused** abil. teenustellimuse saate luua ka projekti abil.

> [!TIP]
> <P>Hooldustellimuste loomiseks saate kasutada automaatseid protsesse. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Hooldustellimuse käsitsi loomine hooldusleppest

1.  Valige **Teenusehaldus** \> **Üldine** \> **Hoolduslepped** \> **Hoolduslepped**.

2.  Valige teenuslepe või looge uus teenuslepe.

3.  Valige vormi **Hooldustellimuste loomine** avamiseks vahekaardi **Tarnimine** grupis **Loomine** valik **Planeeritud hooldustellimused**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>teenustellimuse käsitsi loomine teenustellimuse vormi abil

1.  Valige **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.

2.  Valige uue hooldustellimuse loomiseks **Uus**.

3.  Looge teenustellimuse jaoks teenustellimuse read.

> [!NOTE]
> <P>Kui on valitud märkeruut <STRONG>Luba hooldusleppeta</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>, saate sisestada kandeid hooldustellimuse ridadelt, sidumata hooldustellimust hooldusleppega. Kui ruut on tühjendatud, tuleb käsitsi loodud teenustellimuse enne teenustellimuse ridade sisestamist siduma projektiga.</P>

## <a name="create-a-service-order-from-a-project"></a>Hooldustellimuse loomine projektist

1.  Valige **Projektihaldus ja raamatupidamine** \> **Üldine** \> **Projektid** \> **Kõik projektid**.

2.  Valige vormi **Projektid** **Toimingupaanil** vahekaart **Halda** \> **Teenus** \> **Hooldustellimused**.

3.  Järgige eelmist protseduuri, et luua hooldustellimus käsitsi vormil **Hooldustellimused**. Väljal **Projekti ID** kuvatakse projekti viide.

> [!NOTE]
> <P>Kui on valitud märkeruut <STRONG>Luba hooldusleppeta</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>, saate sisestada kandeid hooldustellimuse ridadelt, sidumata hooldustellimust hooldusleppega. Kui ruut on tühjendatud, tuleb käsitsi loodud teenustellimuse enne teenustellimuse ridade sisestamist siduma projektiga.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Hooldustellimuse loomine vormilt Müügitellimus

Vormilt **Müügitellimused** saate hooldustellimuse luua viisardi **Loo müügitellimuse põhjal uus hooldustellimus** abil.

1.  Valige **Müük ja turundus** \> **Üldine** \> **Müügitellimused** \> **Kõik müügitellimused**.

2.  Avage asjakohane müügitellimus.

3.  Viisardi **Loo müügitellimuse põhjal uus hooldustellimus** käivitamiseks valige vahekaardil **Müügitellimus** valik **Hooldustellimus**.

4.  Valige **Järgmine \>** ja seejärel tehke lehel **Vali hooldustellimuse jaoks lepe** järgmist.
    
      - Kasutage välja **Hoolduslepe**, et valida hoolduslepe, millega uus hooldustellimus siduda.
    
      - Valikuline: kasutage loendit **Projekti ID**, et siduda hooldustellimus kindla projektiga.

5.  Valige **Järgmine \>** ja seejärel tehke lehel **Loo hooldustellimus** järgmist.
    
      - Sisestage kuupäev ja kellaaeg, millal hoolduskutse algab, väljale **Eelistatud teenuseaeg**.
    
      - Valikuline: saate väljal **Kirjeldus** olevat teksti muuta. Vaikimisi sisaldab see väli hooldusleppe kirjeldust, mille valisite eelmisel lehel.
    
      - Valige väljal **Vastutaja** leppe eest vastutava töötaja ID ja kui teate, siis sisestage ka hoolduskutse kliendi eelistatud tehniku ID.
    
      - Valige väljal **Kontakti ID** kliendi ettevõttest isik, kellega selle hooldustellimuse asjus ühendust võtta.

6.  Valige **Järgmine \>** ja seejärel **Valmis**.


## <a name="see-also"></a>Vt ka

[Teenuse tellimused](service-orders.md)

[Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)

[Teenusetellimuste loomine (klass Vormid)](https://technet.microsoft.com/library/aa553901\(v=ax.60\)) 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]