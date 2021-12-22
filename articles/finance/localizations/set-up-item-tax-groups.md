---
title: Saate häälestada kauba maksugruppe.
description: See teema kirjeldab, kuidas seadistada kauba maksugruppe maksuarvestuse teenuses.
author: wangchen
ms.date: 11/30/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable, TaxData
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-10-26
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 88dd8e2fd9d4d4e5172dcc7b1bd27a70a2f59f03
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883897"
---
# <a name="set-up-item-tax-groups"></a>Saate häälestada kauba maksugruppe.

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada kauba maksugruppe maksuarvestuse teenuses. See selgitab ka, kuidas seadistada kauba maksugrupi kohaldatavusreegli maatriksit ja konfigureerida ridu maatriksis.

Kauba maksugruppide mõiste maksuarvestuse teenuses sarnaneb kauba käibemaksugruppide mõistega Microsoftis Dynamics 365 Finance. Need on maksukoodide grupid. Maksuarvestuse teenus kasutab maksukoodide määramiseks maksugrupi ja kauba maksugrupi ristvalikut.

> [!IMPORTANT]
> Kauba maksugruppide seadistus maksuarvestuse teenuses on juriidiline isik -prognoositav. Selle seadistuse saate lõpetada regulatiivses konfiguratsiooniteenuses (RCS) ainult üks kord. Kui lubate finantsis maksuarvestuse teenuse, sünkroonitakse valitud juriidilise isiku kauba maksugrupid automaatselt.

## <a name="set-up-an-item-tax-group"></a>Kauba käibemaksugrupi seadistamine 

Kauba käibemaksugrupi häälestamiseks järgige neid samme.

1. Logige sisse [regulatiivsesse konfigureerimisteenusesse](https://marketing.configure.global.dynamics.com/).
2. Minge **tööruumide** \> **globaliseerimisfunktsiooni** \> **maksuarvutusse.**
3. Valige funktsioon ja versioon, mida soovite seadistada, ning seejärel valige **käsk** Redigeeri.
4. Vahekaardil **Üldine** valige **konfiguratsiooni** versioon.
5. Vahekaardil **Kauba käibemaksugrupp** valige **veerg** Haldamine. Kui seadistate kauba käibemaksugruppi esmakordselt, seadistatakse väljad dialoogiboksis Veeru haldamine **automaatselt**.
6. Laiendage vasakul oleval loendil **sõlm Rida** ja märkige ruut kauba **maksugrupi** jaoks.

    ![Dialoogiboksi Veergude haldamine jaotises Read valitud kauba maksugrupp.](media/select-item-tax-group.png)

7. Valige paremnoolenupp, **et lisada kauba** käibemaksugrupp paremal **olevasse** valitud veergude loendisse.

    ![Valitud veergude loendisse lisatud kauba maksugrupp.](media/add-item-tax-group.png)

8. Valige nupp **OK**.

## <a name="configure-an-item-tax-group"></a>Kauba maksugrupi konfigureerimine

Pärast kauba maksugrupi seadistamist luuakse kohaldatavusreegli maatriks. Kauba käibemaksugrupi konfigureerimiseks saate maatriksile ridu lisada.

1. Valige **vahekaardil Kauba** maksugrupp suvand **Lisa**.
2. Sisestage **kauba** käibemaksugrupi nimi väljale Kauba käibemaksugrupp.

    > [!IMPORTANT]
    > Soovitame piirata kauba maksugrupi nime kuni 10 märgini. See nimi sünkroonitakse finantsiga, mille kauba käibemaksugruppide nimede limiit on 10 märki.

3. Märkige **väljal** Maksukoodid ruut iga maksukoodi puhul, mille soovite kauba käibemaksugruppi kaasata. Ühte kauba käibemaksugruppi saate kaasata mitu maksukoodi.

    ![Maksukoodide väljal on valitud mitu maksukoodi.](media/multiple-tax-codes-selection.png)

4. Kauba maksugruppide lisamiseks korrake samme 1 kuni 3.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
