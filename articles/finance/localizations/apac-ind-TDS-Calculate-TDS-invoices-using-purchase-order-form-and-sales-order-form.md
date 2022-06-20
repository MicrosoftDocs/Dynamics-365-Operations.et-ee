---
title: TDS-i arvete arvutamine ostutellimuse vormi ja müügitellimuse vormi abil
description: Selles artiklis loetletakse allika järgi mahaarvatud maksu arvutamise sammud erinevat tüüpi arvetel.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 72883741ee7eed6b0296736c80dd648c882ae53e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853281"
---
# <a name="calculate-tds-invoices-using-purchase-order-form-and-sales-order-form"></a>TDS-i arvete arvutamine ostutellimuse vormi ja müügitellimuse vormi abil

[!include [banner](../includes/banner.md)]

Selles artiklis loetletakse allika järgi mahaarvatud maksu arvutamise sammud erinevat tüüpi arvetel, kasutades ostutellimust, ostutöölehte, **·** **raamtellimust** **ja müügitellimuste lehekülgi**.**·**

1. Looge loetletud lehte kasutades ostutellimus, ostutööleht, ostu raamtellimus või müügitellimus. Sisestage nõutavad üksikasjad.

2. Valige **Seadistus** vahekaart kliendi hinnastja olemuse vaatamiseks. See teave on loetletud **Hinnaastatava olemus** väljal **Kinnipeetava maksu grupp** väljagrupis.

3. Väljal **TDS grupp** vaadake või muutke hankijale või kliendile määratud vaikimisi TDS-i gruppi.

   > [!NOTE]
   > Väli **TCS-grupp** ei ole saadaval, kui valite TDS-grupi **TDS-grupp** väljal. TDS arvutatakse ainult siis, kui on märgitud **Arvuta kinnipeetav maks** ruut kas **Kõik hankijad** või **Kõik kliendid** lehel.  

4. Looge kaubaread vahekaardil **Read** ja sisestage nõutavad üksikasjad.

5. Valige vahekaart **Seadistus** (reatase), et vaadata või muuta päise taseme määratletud TDS-gruppi. TDS-i grupp kuvatakse **TDS-grupi** väljal, mis asub **Kinnipeetava maksu grupi** väljagrupis.

6. Valige **Maksuteave** vahekaart, vajadusel valige ettevõttele sellel väljal seadistatud alternatiivsed aadressid. Ettevõtte nime saate vaadata väljal **Nimi**, mis on **Ettevõtte teave** väljagrupis. 

   Valitud ettevõtte TAN kuvatakse väljal **Maksukonto number** (**TAN**) väljal, **Kinnipeetava maksu** väljagrupi all. 

7. Valige **Kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht. Järgmised väljad kuvatakse ülemisel paanil **Ajutise kinnipeetava maksu kannete** lehel.

   - **Kinnipeetava** **maksu** **summa** **koos** **kokku** - TDS-grupi kande jaoks arvutatud TDS-i kogusumma.

   - Väljal **Väärtus** - Kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent. Koguprotsent põhineb valemil, mis on määratud TDS-grupiga seotud TDS-i maksukoodide jaoks.

   - **Korrigeeritud kinnipeetava maksu summa kokku** - TDS-i grupi kõikide maksukoodide korrigeeritud TDS-i kogusumma.

   - **TDS** - Kui see on valitud, lisatakse kandele TDS-grupp.

Välja **Ülevaade**, **Üldine**, ja **Kohandamine** vahekaardil **Kinnipeetava maksu kannete** lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.

8. Valige **Lävend** valimine lehe **Lävendd** avamiseks. Vaadake sellel leheküljel konkreetse TDS-i maksukoodiga seotud TDS-i maksukomponendi jaoks määratletud lävendi limiiti ja erandi lävendi limiiti.

9. Valige **Valemikoostur** et avada **Valemikoosturi** leht. Vaadake sellel leheküljel konkreetse TDS-i maksukoodi jaoks määratletud valemit. 

10. Sisestage arve. Ostuarvetel arvutatud TDS-i summa sisestatakse ostureskontrole ja müügiarvetel arvutatud TDS-summa sisestatakse müügireskontro kontole, mis on määratud igale TDS-i maksukoodile TDS-grupis. TDS-i maksukoodide ostureskontro või müügireskontrod määratletakse **Kinnipeetava maksu koodide** lehel.

11. Valige **Päring** nupp **> Arve >Sisestatud kinnipeetav maks** nuppu et avada **Kinnipeetava maksu kannete** leht. Väljal **Väärtus** kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.

Väljad **Ülevaade**, **Üldine**, ja **Summa** vahekaardil **Kinnipeetava maksu kannete** lehel kuvavad kande kohta arvutatud TDS-i teabe. Vaadake TDS-i kalkulatsiooniteavet iga TDS-grupiga seotud TDS-i maksukoodi kohta.
