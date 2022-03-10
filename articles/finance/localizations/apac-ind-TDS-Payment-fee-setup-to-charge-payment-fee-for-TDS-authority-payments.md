---
title: Maksetasude häälestamine TDS-i halduri maksete jaoks
description: See teema kirjeldab, kuidas seadistada maksetasusid, mida arvatakse maha allika (TDS) maksuameti maksetes.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 1c17a00a9c62627e37533b43c38d94d57b00d1eb6c6b55de197dcd6d00d02db6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712191"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>Maksetasude häälestamine TDS-i halduri maksete jaoks

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas seadistada maksetasusid, mida arvatakse maha allika (TDS) maksuameti maksetes.

1. Avage **Ostureskontro \> Makse seadistus \> Maksetasu**.

    [![Maksetasu leht.](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Klõpsake valikut **Uus**, et luua maksetööleht, ja sisestage seejärel nõutavad üksikasjad.
3. Valige **Makse tüüp** väljal tüüp, et valida makse tüüpi:

    - **None**
    - **Viivis** – viivist võetakse TDS-i maksu hankijale tehtud hilinenud maksetelt.
    - **Teised** –Teised maksed võetakse TDS-i maksu hankijale tehtud hilinenud maksetelt.

    Kui valite **Intress** või **Muud**, **Tasu** väljal väärtuseks automaatselt **Pearaamat**.

4. Kui valisite väljal **Intress** või **Teised** väljal **Välja tüüp**, väljal **Põhikonto**, valige pearaamatukonto, et sisestada viivist või muid makse.
5. Sisestage kõik vajalikud üksikasjad.
6. Tegevuspaanil valige **Maksetasu seadistus**, et avada **Maksetasu seadistuse** leht, kus saate seadistada pankade, makseviiside, maksespetsifikatsioonide, valuutade ja ajaintervallide erinevate kombinatsioonide maksetasud.

    [![Maksetasu seadistuse leht.](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Määrake vahekaardi **Ülevaade** väljal **Grupeerimised**, millistele pankadele maksetasu seadistate:

    - **Tabel""** – tasu kehtib konkreetse pangakonto kohta.
    - **Grupp** – tasu kehtib konkreetse pangak grupi kohta.
    - **Kõik** – tasu kehtib kõikide pangakontode puhul.

8. Kui valisite väljal **Tabel** või **Grupp** **Grupeerimised** väljal, valige **Pangaseose** väljal konkreetne pangakonto või pangagrupp, mille jaoks maksetasu seadistate.
9. Väljal **Maksemeetod** valige meetod, mida maksetasu maksmise puhul kasutada.
10. Väljal **Makse täpsustus** valige või sisestage makse täpsustuse kood, mis loodi **Makse täpsustuse** lehel.
    - Suvandit Makse täpsustus kasutatakse elektroonilise ülekande makseviisidega.
12. Valige väljal **Maksu valuuta** makse valuuta, mis aktiveerib tasu. Tasu saab aktiveerida ainult valitud valuutat kasutavad kanded. Kui jätate selle välja tühjaks, aktiveerivad tasu kõik valuutad.
13. Valige **Protsent/Summa** väljal arvutusmeetod. Valikud on **Summa**, **Protsent** ja **Intervall**.
14. Väljal **Tasu summa** määrake tasu summa kas makse protsendina või ühe makse summana.
15. Valige väljas **Maksu valuuta** maksu valuuta.
16. Valige **Üldine** vahekaart valitud bangakonto üksikasjade vaatamiseks või muutmiseks.

    [![Vahekaart Üldine.](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Sisestage **Minimaalne** väljal minimaalne kandesumma, mis aktiveerib tasu.
17. Sisestage **Maksimaaalne** väljal maksimaalne kandesumma, mis aktiveerib tasu.
18. Väljadel **Alates** ja **Kuni kuupäevani** määratlege arvutamiseks kuupäevavahemik.
19. Väljal **Minimaalne tasu** määrake tasu summa kas makse protsendina või ühe makse summana.
20. Valige **Käibemaksugrupp** väljal käibemaksugrupp, mida kasutada tasusumma käibemaksu arvutamiseks.
21. Valige **Käibemaksugrupp** väljal käibemaksugrupp, mida kasutada tasusumma käibemaksu arvutamiseks.
22. Valige vahekaart **Intervall**. 

    [![Intervalli vahekaart.](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Väljal **Päevad** sisestage rahaülekande sisestuskuupäeva (allahindluskuupäeva) ja võlatähe tähtaja vahele jäävate päevade arv.
24. Valige **Protsent/Summa** väljal kas täpsustus on protsent või seatud summa.
25. Väljal **Minimaalne tasu** määrake tasu summa kas makse protsendina või ühe makse summana.
26. Sulgege **Maksetasu seadistuse** leht.
27. Sulgege **Maksetasu** leht.
