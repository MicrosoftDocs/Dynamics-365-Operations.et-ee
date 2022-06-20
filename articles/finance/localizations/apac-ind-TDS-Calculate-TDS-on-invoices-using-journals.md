---
title: TDS-i arvutamine arvetel töölehtede abil
description: Selles artiklis loetletakse töölehtedel allikalt (TDS) maha arvatud maksu arvutamise sammud.
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
ms.openlocfilehash: d9217029a38aa41e42a236d3cfa39993b1bcee4a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863029"
---
# <a name="calculate-tds-on-invoices-using-journals"></a>TDS-i arvutamine arvetel töölehtede abil

[!include [banner](../includes/banner.md)]

Selles artiklis loetletakse töölehtedel allikalt (TDS) maha arvatud maksu arvutamise sammud.

Alustage lehekülje **Üldised töölehed** avamisega (**Pearaamat > Töölehe sisestused > Üldtöölehed**).

[![Päevaraamatud.](./media/apac-ind-TDS-57.png)](./media/apac-ind-TDS-57.png)

1. Looge tööleheread tabelis loetletud töölehevormide abil. Valige konto tüüp ja vastaskonto tüüp ning sisestage kandele summa. 

   > [!NOTE]
   > Valige **Arve kinnitamise tööleht** lehel suvand **Otsi kandeid** ja valige arved, mille kohta TDS arvutada. Saate vaadata loodud arveid **Arveregistri** lehel või **Otsi kandeid** lehel.  

2. Vahekaardil **Üldine** lehel **Töölehe kanded** vaadake või muutke hankijale või kliendile määratud TDS-i vaikegruppi **TDS grupp** väljal. Töölehe ridadel arvutatud TDS-i summa põhineb **TDS-i grupi** väljal loetletud TDS-i maksukoodide jaoks määratletud valemil. 

   > [!NOTE]
   > Väli **Kinnipeetava maksu grupp** ja väli **TCS-i grupp** muutuvad kättesaamatuks, kui valite TDS-grupi **TDS-grupp** väljal. **Kinnipeetava maksu grupi** väli on saadaval ainult lehel **Üldised töölehed** lehel. TDS arvutatakse ainult siis, kui on märgitud **Arvuta kinnipeetav maks** ruut kas **Kõik hankijad** või **Kõik kliendid** lehel.   

3. Valige **Maksuteabe** vahekaart. Valige ettevõttele sellel väljal seadistatud alternatiivsed aadressid, kui vaja. Ettevõtte nime saate vaadata väljal **Nimi**, mis on **Ettevõtte teave** väljagrupis. 

4. Vaadake hankija või kliendi hinnalepete kategooria olemust **Hinna hindamise** väljal, mis on **Kinnipeetava maksu** väljagrupis. Vaadake **Maksukonto number** (**TAN**) väljal kuvatava ettevõtte nime valitud maksude maksukontot.  

5. Valige **Kinnipeetav maks** menüüst **Kinnipeetav maks** et avada **Ajutised kinnipeetava maksu kanded** leht. Järgmised väljad kuvatakse ülemisel paanil **Ajutise kinnipeetava maksu kannete** lehel.

   - **Kinnipeetava maksu summa kokku** - TDS-grupi kande jaoks arvutatud TDS-i kogusumma.

   - Väljal **Väärtus** - Kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent. Koguprotsent põhineb valemil, mis on määratud TDS-grupiga seotud TDS-i maksukoodide jaoks.

   - **Korrigeeritud kinnipeetava maksu summa kokku** - TDS-i grupi kõikide maksukoodide korrigeeritud TDS-i kogusumma.

   - **TDS** - Kui see on valitud, lisatakse kandele TDS-grupp.

  Välja **Ülevaade**, **Üldine**, ja **Kohandamine** vahekaardil **Kinnipeetava maksu kannete** lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.

6. Valige **Lävend** valimine lehe **Lävendd** avamiseks. Vaadake sellel leheküljel konkreetse TDS-i maksukoodiga seotud TDS-i maksukomponendi jaoks määratletud läve limiiti ja erandi läve limiiti.

   Valige **Valemikoostur** et avada **Valemikoosturi** vorm. Vaadake sellel leheküljel konkreetse TDS-i maksukoodi jaoks määratletud valemit. Sulgege **valemikoostur** ja **Ajutise kinnipeetava maksu kannete** lehed et naasta **Töölehe kande** lehele.

8. Sisestage kõik vajalikud üksikasjad. Kinnitage ja sisestage tööleht. Ostuarvetel arvutatud TDS-i summa sisestatakse tasumisele kuuluvale kontole. Müügiarvetel arvutatud TDS-summa sisestatakse tasumisele kuuluvale kontole, mis on määratud igale TDS-i maksukoodile TDS-grupis. TDS-i maksukoodide ostureskontro või müügireskontrod määratletakse **Kinnipeetava maksu koodide** lehel.

9. Valige **Sisestatud kinnipeetav maks**, et avada **Kinnipeetava maksu kannete** leht. Väljal **Väärtus** kuvatakse kande TDS-i arvutamiseks kasutatav koguprotsent.

   Välja **Ülevaade**, **Üldine**, ja **Summa** vahekaardil kinnipeetava maksu kannete lehel kuvatakse TDS-summa ja korrigeeritud TDS-i summa TDS-i grupiga seotud TDS-i maksukoodi kohta.
