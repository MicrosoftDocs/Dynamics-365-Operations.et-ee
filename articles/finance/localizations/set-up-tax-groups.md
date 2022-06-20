---
title: Maksugruppide häälestus
description: See artikkel selgitab, kuidas maksugruppe maksuarvutuse teenuses seadistada.
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
ms.openlocfilehash: 89c5670ee7e78f2dc51f128c3ae8d284bb6b925b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862895"
---
# <a name="set-up-tax-groups"></a>Maksugruppide häälestus

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas maksugruppe maksuarvutuse teenuses seadistada. See selgitab ka maksugrupi kohaldatavusreegli maatriksi seadistamist ja ridade konfigureerimist maatriksis.

Maksuarvestuse teenuse maksugruppide mõiste sarnaneb käibemaksugruppide mõistega Microsoft Dynamics teenuses 365 Finance. Need on maksukoodide grupid. Maksuarvestuse teenus kasutab maksukoodide määramiseks maksugrupi ja kauba maksugrupi ristvalikut.

Maksugrupid maksuarvestuse teenuses erinevad finantside käibemaksugruppidest, kuna nende jaoks pole lisaparameetreid, nt **Kasutusmaks** ja **Maksuvaba**. Selle asemel on need parameetrid saadaval maksukoodi tasemel.

> [!IMPORTANT]
> Maksugruppide seadistus maksuarvutuse teenuses on juriidiline isik -prognoositav. Selle seadistuse saate lõpetada regulatiivses konfiguratsiooniteenuses (RCS) ainult üks kord. Kui lubate finantsis maksuarvestuse teenuse, sünkroonitakse maksugrupid valitud juriidilise isiku jaoks automaatselt.

## <a name="set-up-a-tax-group"></a>Maksugrupi loomine

Maksugrupi häälestamiseks järgige neid samme.

1. Logige sisse regulatiivsesse [konfigureerimisteenusesse](https://marketing.configure.global.dynamics.com/).
2. Minge tööruumide **globaliseerimisfunktsiooni** \> **maksuarvutusse.** \> **·**
3. Valige funktsioon ja versioon, mida soovite seadistada, ning seejärel valige käsk **Redigeeri**.
4. **Vahekaardil Üldine** valige **konfiguratsiooni versioon**.
5. **Vahekaardil Maksugrupp** valige suvand **Veeru haldamine**. Kui seadistate käibemaksugruppi esmakordselt, seadistatakse dialoogiboksi **Veeru** haldamine väljad automaatselt.
6. Laiendage vasakul oleval loendil **sõlm Rida** ja märkige ruut **Maksugrupp**.

    ![Käibemaksugrupp, mis on valitud dialoogiboksi Veergude haldamine jaotises Ridade sõlm.](media/select-tax-group.png)

7. Valige paremnoolenupp, et **lisada maksugrupp** paremal olevasse **valitud** veergude loendisse.

    ![Valitud veergude loendisse lisatud maksugrupp.](media/add-tax-group.png)

8. Valige nupp **OK**.

## <a name="configure-a-tax-group"></a>Maksugrupi konfigureerimine

Pärast maksugrupi häälestamist luuakse maksugrupi kohaldatavusreegli maatriks. Maksugrupi konfigureerimiseks saate maatriksile ridu lisada.

1. **Vahekaardil Maksugrupp** valige **lisa**.
2. **Sisestage maksugrupi** nimi väljale Maksugrupp.

    > [!IMPORTANT]
    > Soovitame piirata maksugrupi nime 10 märgiga. See nimi sünkroonitakse finantsiga, mille käibemaksugruppide nimede limiit on 10 märki.

3. **Märkige väljal Maksukoodid** ruut iga maksukoodi puhul, mille soovite maksugruppi kaasata. Ühte maksugruppi saate kaasata mitu maksukoodi.

    ![Maksukoodide väljal on valitud mitu maksukoodi.](media/multiple-tax-codes-selection.png)

4. Korrake samme 1 kuni 3, et lisada rohkem maksugruppe.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
