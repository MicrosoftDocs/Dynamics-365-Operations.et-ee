---
title: "teenustellimuste loomine käsitsi"
description: "Hooldustellimusi saate luua käsitsi hoolduslepete või vormi **Hooldustellimused** abil."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a0cc6b2646929776f4efb20474de6b0fc5c4719c
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="create-service-orders-manually"></a>teenustellimuste loomine käsitsi    

[!include [banner](../includes/banner.md)]


Hooldustellimusi saate luua käsitsi hoolduslepete või vormi **Hooldustellimused** abil. teenustellimuse saate luua ka projekti abil.

> [!TIP]
> <P>Hooldustellimuste loomiseks saate kasutada automaatseid protsesse. 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a>Hooldustellimuse käsitsi loomine hooldusleppest

1.  Klõpsake valikut **Hooldushaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldusleppegrupid**.

2.  Valige teenuslepe või looge uus teenuslepe.

3.  Vormi **Hooldustellimuste loomine** avamiseks klõpsake vahekaardi **Tarnimine** grupis **Loomine** valikut **Planeeritud hooldustellimused**.

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a>teenustellimuse käsitsi loomine teenustellimuse vormi abil

1.  Klõpsake valikuid **Teenusehaldus** \> **Üldine** \> **Hooldustellimused** \> **Hooldustellimused**.

2.  Uue teenustellimuse loomiseks vajutage klahve CTRL+N.

3.  Looge teenustellimuse jaoks teenustellimuse read.

> [!NOTE]
> <P>Kui on valitud märkeruut <STRONG>Luba hooldusleppeta</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>, saate sisestada kandeid hooldustellimuse ridadelt, sidumata hooldustellimust hooldusleppega. Kui ruut on tühjendatud, tuleb käsitsi loodud teenustellimuse enne teenustellimuse ridade sisestamist siduma projektiga.</P>

## <a name="create-a-service-order-from-a-project"></a>Hooldustellimuse loomine projektist

1.  Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Üldine** \> **Projektid** \> **Kõik projektid**.

2.  Klõpsake vormi **Projektid** **toimingupaanil** vahekaarti **Halda** \> **Teenus** \> **Hooldustellimused**.

3.  Järgige eelmist protseduuri, et luua hooldustellimus käsitsi vormil **Hooldustellimused**. Väljal **Projekti ID** kuvatakse projekti viide.

> [!NOTE]
> <P>Kui on valitud märkeruut <STRONG>Luba hooldusleppeta</STRONG> vormil <STRONG>Teenuste halduse parameetrid</STRONG>, saate sisestada kandeid hooldustellimuse ridadelt, sidumata hooldustellimust hooldusleppega. Kui ruut on tühjendatud, tuleb käsitsi loodud teenustellimuse enne teenustellimuse ridade sisestamist siduma projektiga.</P>

## <a name="create-a-service-order-from-the-sales-order-form"></a>Hooldustellimuse loomine vormilt Müügitellimus

Vormilt **Müügitellimused** saate hooldustellimuse luua viisardi **Loo müügitellimuse põhjal uus hooldustellimus** abil.

1.  Klõpsake valikuid **Müük ja turundus** \> **Üldine** \> **Müügitellimused** \> **Kõik müügitellimused**.

2.  Avage asjakohane müügitellimus.

3.  Viisardi **Loo müügitellimuse põhjal uus hooldustellimus** käivitamiseks klõpsake vahekaardil **Müügitellimus** valikut **Hooldustellimus**.

4.  Klõpsake valikut **Järgmine \>** ja seejärel tehke lehel **Vali hooldustellimuse jaoks lepe** järgmist.
    
      - Kasutage välja **Hoolduslepe**, et valida hoolduslepe, millega uus hooldustellimus siduda.
    
      - Valikuline: kasutage loendit **Projekti ID**, et siduda hooldustellimus kindla projektiga.

5.  Klõpsake valikut **Järgmine \>** ja seejärel tehke lehel **Loo hooldustellimus** järgmist.
    
      - Sisestage kuupäev ja kellaaeg, millal hoolduskutse algab, väljale **Eelistatud teenuseaeg**.
    
      - Valikuline: saate väljal **Kirjeldus** olevat teksti muuta. Vaikimisi sisaldab see väli hooldusleppe kirjeldust, mille valisite eelmisel lehel.
    
      - Valige väljal **Vastutaja** leppe eest vastutava töötaja ID ja kui teate, siis sisestage ka hoolduskutse kliendi eelistatud tehniku ID.
    
      - Valige väljal **Kontakti ID** kliendi ettevõttest isik, kellega selle hooldustellimuse asjus ühendust võtta.

6.  Klõpsake valikut **Järgmine \>** ja seejärel **Valmis**.


## <a name="see-also"></a>Vt ka

[Teenusetellimused](service-orders.md)

[Hooldustellimuste loomine automaatselt](create-service-orders-automatically.md)

[Teenusetellimuste loomine (klass Vormid)](https://technet.microsoft.com/en-us/library/aa553901\(v=ax.60\)) 


