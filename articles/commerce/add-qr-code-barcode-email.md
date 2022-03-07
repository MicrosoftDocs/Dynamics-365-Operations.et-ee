---
title: QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele
description: See teema selgitab, kuidas sisestada Microsoft Dynamics 365 Commerce kande- ja sissetulekumeilidesse QR-koodid ja vöötkoodid, mis tähistavad tellimuse ID-sid.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 9a3ab355d6e68221610e48e02e191c1d21f5155db81990d0991a8c353f3f9ecd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729934"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele

[!include [banner](includes/banner.md)]

See teema selgitab, kuidas sisestada Microsoft Dynamics 365 Commerce kande- ja sissetulekumeilidesse QR-koodid ja vöötkoodid, mis tähistavad tellimuse ID-sid.

Saate lihtsalt lisada QR-koodid ja vöötkoodid kande e-kirja, et aidata jaemüügikeskkonnas tellimuse otsinguprotsessi kiirendada. QR-koodide ja vöötkoodide sisestamiseks e-kirja, kasutage HTML **\<img\>** silti, mis taotleb QR-koodi või vöötkoodi pilti loomisest ja renderdamisteenusest. Microsoft ei paku seda teenust. Siiski on palju tasuta või kalleid teenuseid, mis võivad teenindada QR-koode või vöötkoode, mis luuakse dünaamiliselt päringustringis edastatud väärtuse põhjal.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele

E-kaubanduse ostu osana saadetud kande e-kirjale QR-koodi või vöötkoodi sisestamiseks järgige neid samme.

1. Avage kande e-kirja malli lähte-HTML ja lisage HTML-silt, mis osutab teie **\<img\>** QR-koodile või vöötkoodi teenusele. Siin on näide.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Siin on võimalike olekute selgitus:

    - **TEIE\_QR\_KOODI\_VÖÖT\_KOODI\_TEENUS** esindab teie QR-koodi või vöötkoodi teenuse domeeni.
    - **Andmed** tähistab parameetrit, mida QR-kood või vöötkoodi teenus kasutab, et vastu võtta sisu, mida tuleks renderdada QR-koodina või vöötkoodina.

        Sellele **%salesid%** parameetrile peab olema määratud väärtus. Selles näites pange tähele, et väärtust kasutatakse ka pildi asetekstna.

    - **parameeter 1** ja **parameeter 2** esindavad täiendavaid valikulisi parameetreid.

1. Minge rakenduse **Retail ja Commerce  \> Headquarters häälestamise \> parameetrite \> organisatsiooni meilimallidesse** ja laadige värskendatud HTML ülessobivale kande meilimallile.

> [!NOTE]
> Parameetrid võivad QR-koodi ja vöötkoodi teenuse pakkujate vahel erineda. Seetõttu võtke ühendust oma teenusepakkujaga, et kinnitada parameetrid, mille juurde peate väärtused määrama.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>QR-koodi või vöötkoodi lisamine kande- ja kviitungi meilidele 

QR-koodi või vöötkoodi sisestamiseks kviitungi e-kirja, mille saab saata pärast seda, kui ost on tehtud müügikohas (POS), järgige neid samme.

1. Avage kande e-kirja malli lähte-HTML ja lisage HTML-silt, mis osutab teie **\<img\>** QR-koodile või vöötkoodi teenusele. Siin on näide allpool.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Siin on võimalike olekute selgitus:

    - **TEIE\_QR\_KOODI\_VÖÖT\_KOODI\_TEENUS** esindab teie QR-koodi või vöötkoodi teenuse domeeni.
    - **Andmed** tähistab parameetrit, mida QR-kood või vöötkoodi teenus kasutab, et vastu võtta sisu, mida tuleks renderdada QR-koodina või vöötkoodina.

        Sellele **%receiptid%** parameetrile peab olema määratud väärtus. Selles näites pange tähele, et väärtust kasutatakse ka pildi asetekstna.

    - **parameeter 1** ja **parameeter 2** esindavad täiendavaid valikulisi parameetreid.

1. Minge rakenduse **Retail ja Commerce \> Headquarters häälestamise \> parameetrite \> organisatsiooni meilimallidesse** ja laadige värskendatud HTML üles sobivale kande meilimallile **emailivastuvõtja**.

> [!NOTE]
> Parameetrid võivad QR-koodi ja vöötkoodi teenuse pakkujate vahel erineda. Seetõttu võtke ühendust oma teenusepakkujaga, et kinnitada parameetrid, mille juurde peate väärtused määrama.

## <a name="additional-resources"></a>Lisaressursid

[Meilikviitungite saatmine rakendsusest Modern POS (MPOS)](email-receipts.md)

[Meilimallide loomine kandesündmuste jaoks](email-templates-transactions.md)
