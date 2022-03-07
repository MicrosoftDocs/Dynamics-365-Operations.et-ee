---
title: Mittevastavuste loomine ja töötlemine
description: Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032f5b712c2be5312524129cd25e655e778f5f44
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580860"
---
# <a name="create-and-process-nonconformances"></a>Mittevastavuste loomine ja töötlemine

[!include [banner](../../includes/banner.md)]

Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal. Mittevastavuse haldust viib tavaliselt läbi kvaliteediametnik. Eeltingimusena peab teil olema saadaval kvaliteettellimus. (Lisateavet kvaliteettellimuse loomise kohta vt teemast [Kaupade kvaliteedi kontrollimine ](inspect-quality-goods.md).)

Enne, kui kasutaja saab mittevastavuse kinnitamist töödelda, peab töötaja olema määratud talle lehel **Kasutajad** oleval väljal **Isik**. Lisaks tuleb enne kasutajal dokumendi märkuste kasutamist kasutajavalikutes seada valik **Luba dokumendi käsitlemine** väärtusele *Jah*.

## <a name="create-a-nonconformance"></a>Mittevastavuse loomine

Mittevastavuse loomiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiakna **Mittevastavuse loomine** väljal **Probleemi tüüp** valige probleemi tüüp, mis kontrollprotsessi käigus leiti.
1. Valige nupp **OK**.

## <a name="approve-or-reject-a-nonconformance"></a>Mittevastavuse kinnitamine või tagasilükkamine

Mittevastavuse kinnitamiseks või tagasilükkamiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.

    > [!NOTE]
    > Saate lisada paranduse ainult kinnitatud mittevastavustele.

1. Tegevuspaanil valige, et mittevastavus kinnitada või **Funktsioonid \> Kinnita mittevastavus**, et mittevastavus kinnitada, või **Funktsioonid \> Keeldu mittevastavusest**, et see tagasi lükata. Kinnitatud mittevastavused saate seostada [seotud toimingutega](../quality-operations.md). Sel viisil saate salvestada töö, mis tehakse mittevastavuse käsitlemise ja paranduste töötlemise osana.
1. Kui teil palutakse tegevus kinnitada, kinnitage oma valik. Jätkamiseks valige **Jah**.

## <a name="add-operations-and-other-details-to-nonconformances"></a>Mittevastavustele toimingute ja muude üksikasjade lisamine

Kui olete mittevastavuse loonud, saate alustada seotud operatsioonide lisamist ja määrata nende operatsioonide kohta lisateavet. Saate lisada seotud tegevusi ainult kinnitatud mittevastavustele.

Lisaks põhiteabele saate operatsioonile lisada ka järgmised üksikasjad:

- **Kaubad** – saate luua nende kaupade loendi, mis tarbitakse paranduse katteks. Näiteks võivad kaubad olla tooted, mis on vajalikud valmistoodangu taastöötlemiseks vajalike seadmete või koostisainete remondiks.
- **Kvaliteedikulud** – saate luua kulude loendi, mis on tekkinud või väljaarvestatud välisallikatele.
- **Ajatabel** – saate luua logi ajast, mil iga töötaja operatsioonile kulutab.

Ülejäänud seaded on valikulised. Iga kauba kulu, kvaliteedikulud ja ajatabel on summeeritud ja operatsioonis näidatud. Te ei saa otse redigeerida operatsiooni välja **Kulu**.

### <a name="create-an-operation-for-a-nonconformance"></a>Operatsiooni loomine mittevastavusele

Mittevastavuse operatsiooni loomiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.

    > [!NOTE]
    > Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.

1. Valige toimingupaanil suvand **Seotud operatsioonid**.
1. Ruudustiku rea lisamiseks valige **seotud toimingute** lehekülje tegevuspaanil suvand **Uus**. Seejärel määrake uuel real järgmised väljad.

    - **Toiming** – valige mittevastavuse jaoks sooritatav toimingu kood.
    - **Põhjus** – sisestage üksikasjalik kirjeldus, mis selgitab operatsiooni vajalikkust.
    - **Müügitellimus** – kui valitud toimingukood on seotud müügitellimuse tüübiga, valige müügitellimus, millega te operatsiooni seote.
    - **Ostutellimus** – kui valitud toimingukood on seotud ostuellimuse tüübiga, valige ostutellimus, millega te operatsiooni seote.

1. Sulgege lehed.

### <a name="add-items-to-an-operation"></a>Kaupade lisamine operatsioonile

Kaupade lisamiseks operatsioonile järgige neid samme.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.

    > [!NOTE]
    > Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.

1. Valige toimingupaanil suvand **Seotud operatsioonid**.
1. Valige leheküljel **Seotud operatsioonid** operatsioon, millele soovite kaupu lisada.
1. Toimingupaanil valige käsk **Kaubad**.
1. Ruudustiku rea lisamiseks valige **seotud toimingute** lehekülje tegevuspaanil suvand **Uus**. Seejärel määrake uuel real järgmised väljad.

    - **Kaubakood** – valige toode, mida tarbitakse valitud operatsiooni osana.
    - **Kogus** – sisestage tarbitavate kaupade arv.

    > [!NOTE]
    > Kauba kulu saate vaadata vahekaardi **Üldine** väljal **Kulu**. Näidatud kulu tuleb leheküljel **Väljastatud toode** seadistatud kulust. Kulu ei saa otse **seotud toimingu kauba lehel** uuendada. Kõigi kaupade kulu, mis on lisatud **seotud toimingu kaupade** lehele, lisatakse automaatselt **seotud toimingute** lehe väljale **Kulu**.

1. Korrake eelmist sammu iga lisakauba puhul, mille peate lisama.
1. Sulgege lehed.

### <a name="add-quality-charges-to-an-operation"></a>Operatsioonile kvaliteedikulude lisamine

Kvaliteedikulude lisamiseks operatsioonile järgige neid samme.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.

    > [!NOTE]
    > Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.

1. Valige toimingupaanil suvand **Seotud operatsioonid**.
1. Valige leheküljel **Seotud operatsioonid** operatsioon, millele soovite kvaliteedikulusid lisada.
1. Valige toimingupaanil suvand **Kvaliteedikulud**.
1. Ruudustiku rea lisamiseks valige **seotud toimingute kulud** lehekülje tegevuspaanil suvand **Uus**. Seejärel määrake uuel real järgmised väljad.

    - **Kulude kood** – valige kvaliteedikulu, mida soovite lisada.
    - **Kirjeldus** – sisestage kulu detailne kirjeldus.
    - **Kulude summa** – sisestage kulude summa.

1. Korrake eelmist sammu iga kulu puhul, mille peate lisama.
1. Sulgege lehed.

> [!NOTE]
> **Kulude väärtuse** väljal olevad summad summeeritakse automaatselt kõigi kvaliteedikulude osas ja lisatakse mis tahes muudele summadele väljal **Kulu** **seotud toimingute** lehel.

### <a name="create-a-timesheet-on-an-operation"></a>Toimingu kohta ajatabeli loomine

Ajatabeli lisamiseks operatsioonile järgige neid samme.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.

    > [!NOTE]
    > Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.

1. Valige toimingupaanil suvand **Seotud operatsioonid**.
1. Valige leheküljel **Seotud operatsioonid** operatsioon, millele soovite ajatabelit lisada.
1. Valige tegevuste paanil käsk **Ajatabel**.
1. Ruudustiku rea lisamiseks valige **seotud toimingute ajatabelid** lehekülje tegevuspaanil suvand **Uus**. Seejärel määrake uuel real järgmised väljad.

    - **Kuupäev** – määrake töö tehtud töö kuupäev. Vaikimisi on see väli seadistatud praegusele kuupäevale.
    - **Töötaja** – valige töötaja, kes tööd tegi. Vaikimisi on selle välja väärtuseks määratud praegusele kasutajale määratud töötaja.
    - **Operatsiooni tunnid** – sisestage valitud operatsiooni ajal töötatud tundide arv.
    - **Arveldatud** – märkige see ruut, kui arvel on kliendile või hankijale arve tasu küsimise aeg.

    > [!NOTE]
    > Kulu saate vaadata vahekaardi **Üldine** väljal **Kulu**. Kulu arvutatakse leheküljel **Varude halduse parameetrid** määratud määra alusel.

1. Korrake eelmist sammu iga ajatabeli rea puhul, mille peate lisama.
1. Sulgege lehed.

> [!NOTE]
> **Kulude väärtuse** väljal olevad summad summeeritakse automaatselt kõigi ajatabeli ridade osas ja lisatakse mis tahes muudele summadele väljal **Kulu** **seotud toimingute** lehel.

## <a name="add-a-correction-to-a-nonconformance"></a>Mittevastavusele paranduste lisamine

Mittevastavusele paranduse lisamiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.

    > [!NOTE]
    > Saate lisada paranduse ainult kinnitatud mittevastavustele.

1. Valige toimingupaanil suvand **Parandused**.
1. Valige tegevuspaanil suvand **Uus**, et lisada rida jaotise **Parandused** tabelisse. Seejärel määrake uuel real järgmised väljad.

    - **Diagnostika** – valige diagnostika tüüp, mis tuvastab parandustüübi, mida loote.
    - **Töötaja** – valige paranduse eest vastutav isik.
    - **Paranduse prioriteet** – valige suvand, et näidata, kuidas parandust prioriteerida (*Madal*, *Tavaline* või *Kõrge*).
    - **Nõutav kuupäev** – sisestage kuupäev, millal parandustegevust taotleti.
    - **Planeeritud kuupäev** – sisestage kuupäev, millal parandus eeldatavalt viiakse lõpule.
    - **Lühiajaline lahendus** – märkige see ruut, kui parandustegevus parandab mittevastavuse ainult lühikese aja jooksul.

1. Sulgege lehed.

## <a name="mark-a-correction-as-completed"></a>Paranduse lõpetatuks märkimine

Mittevastavuse paranduse lõpetatuks märkimiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.

    > [!NOTE]
    > Saate lisada paranduse ainult kinnitatud mittevastavustele.

1. Valige toimingupaanil suvand **Parandused**.
1. Lehel **Parandused**, ruudustikus, valige parandus, mida tahate märkida lõpetatuks.
1. Toimingupaanil valige **Märgi lõpetatuks**.
1. Kui teil palutakse tegevus kinnitada, kinnitage oma valik. Jätkamiseks valige **OK**. Väli **Lõpetamise kuupäev ja kellaaeg** seatakse praegusele kuupäevale ja kellaajale ning ruut **Lõpetatud** on märgitud.
1. Sulgege leht.

## <a name="reopen-a-completed-correction"></a>Lõpetatuks märgitud paranduse uuesti avamine

Lõpetatud paranduse uuesti avamiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.
1. Leidke ja valige loendist mittevastavus, mille soovite uuendada.
1. Valige toimingupaanil suvand **Parandused**.
1. Valige **Parandus** ruudustikus leheküljel Parandused, mille soovite uuesti avada.
1. Toimingupaanil valige käsk **Uuesti avamine**.
1. Kui teil palutakse tegevus kinnitada, kinnitage oma valik. Jätkamiseks valige **OK**. Väärtus tühjendatakse **väljalt Lõpetamise kuupäev** ja kellaaeg ning märkeruut **Lõpetatud** tühjendatakse.
1. Sulgege leht.

Nüüd saate parandusse teha täiendavaid muudatusi või uuendusi. Kui olete parandusega lõpetanud, saate paranduse uuesti lõpetatuks märkida.

## <a name="close-a-nonconformance"></a>Mittevastavuse sulgemine

Mittevastavuse sulgemiseks tehke järgmist.

1. Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.
1. Valige ruudustikust kvaliteettellimus.
1. Valige toimingupaanilt **Päringud \> Mittevastavused**.
1. Valige lehel **Mittevastavused** ruudustikust sihtmärgi mittevastavus.
1. Valige tegevuspaanil suvand **Funktsioonid \> Sulge mittevastavus**.
1. Kui teil palutakse tegevus kinnitada, kinnitage oma valik. Jätkamiseks valige **Jah**.
1. Sulgege lehed.

## <a name="additional-resources"></a>Lisaressursid

- [Kvaliteedijuhtimise ülevaade](../quality-management-processes.md)
- [Kvaliteedi ja mittevastavuse haldamise lubamine](../enable-quality-management.md)
- [Mittevastavuste kinnitamise eest vastutavad töötajad](../quality-responsible-workers.md)
- [Mittevastavuste vahelao tsoonid](../quality-quarantine-zones.md)
- [Mittevastavuste diagnostika tüübid](../quality-diagnostic-types.md)
- [Kvaliteeditasud mittevastavustele](../quality-charges.md)
- [Operatsioonid mittevastavusele](../quality-operations.md)
- [Laoprotsesside kvaliteedijuhtimine](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
