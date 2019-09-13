---
title: Tarbimise registreerimine
description: Selles teemas tutvustatakse, kuidas varahalduses tarbimist registreerida.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7f785b0935b952d6de68fd120a3639077ad124bd
ms.sourcegitcommit: c0b581e4c647b6c47bc14d1d7bfe267832afecba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1913081"
---
# <a name="register-consumption"></a>Tarbimise registreerimine

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Kui hooldustöö on töökäsus lõpetatud, on järgmine etapp tarbimiste registreeringute tegemine ja töölehtedele sisestamine. Saate registreeringuid teha järgmiste tarbimise tüüpide kohta: tunnid, kaubad ja kulud. Eri tarbimise tüübid on registreeritud ja sisestatud lehele **Töökäsu töölehed**. Töölehe seadistust funktsioonis **Varahaldus** kasutatakse eraldi töölehtede loomiseks ja sisestamiseks tundide, kaupade ja kulude jaoks moodulis **Projektihaldus ja raamatupidamine**.

Saate töökäsule prognoosi ridu lisada või neid kustutada. Töökäsu töötsükli oleku seadistus, seotud projektitüüp ja seotud projektitüübi oleku reeglid määravad ära, kas saate töölehele ridu lisada või redigeerida. Lisateavet töökäsu töötsükli olekute ja seotud projekti etappide kohta lugege teemast [Projektihalduse ja raamatupidamisega integreerimine](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

>[!NOTE]
>Töökäsu töötsükli olekule on võimalik seadistada automaatne töölehtede sisestamine. Lisateabe saamiseks vaadake teemat [Töökäsu töötsükli olekud](../setup-for-work-orders/work-order-lifecycle-states.md).

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk ja klõpsake **Töölehed**.

3. Klõpsake **Kopeeri prognoosist**, et edastada mis tahes prognoosi read, mis võivad olla seotud töökäsuga. Saate valida milliseid tarbimise ridu soovite edastada.

4. Vajaduse korral saate lisada tarbimise ridu seotud kiirkaardil, kui klõpsate **Lisa rida** ja täidate rea andmetega.

5. Töölehe ridade valideerimiseks enne sisestamist klõpsake **Valideeri töölehed**.

6. Töölehe ridade sisestamiseks klõpsake **Sisestage töölehed**.

7. Pärast tarbimise töölehtede sisestamist, saate värskendada töökäsu töötsükli olekut, näiteks olekule "Lõpetatud", mis näitab, et töökäsk on lõpetatud.

- Lehe **Töökäsu töölehed** ülaosas asuval väljal **Kuva** valige milliseid töölehe ridu soovite näha: kõik, sisestamata või sisestatud. Sisestatud töölehtedel on märgitud märkeruut **Sisestatud**.  
- Kui kaubaread on loodud töökäsu töölehel, edastatakse kaubaga seotud tootedimensioonid ja jälgimisdimensioonid automaatselt töölehe reale.  

Alloleval kuvatõmmisel kuvatakse näidet tunni ja kauba registreeringutest töökäsul suvandis **Töökäsu töölehed**.

![Joonis 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Töökäskude tundide eraldamine mitme töökäsu tööga

Kui töökäsk sisaldab mitut töökäsu tööd, saate registreerida töötunnid, kui kasutate funktsiooni **Eralda tunnid**, mis tähendab, et ühe tunni registreerimise rea võib võrdselt jagada iga töökäsu töö jaoks.

1. Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik Töökäsud** või **Aktiivsed töökäsud**.

2. Valige töökäsk ja klõpsake **Töölehed**.

3. Valige loendist tunni registreerimise rida, mida soovite eraldada ja klõpsake **Eralda tunnid**.

4. Dialoogis **Eralda tunnid töökäsu hooldustöödel** kuvatakse väljal **Töötaja** automaatselt selle töötaja nime, kes on sisse logitud. Vajaduse korral saate valida teise töötaja.

5. Valige tunni registreerimise jaoks kategooria väljal **Kategooria**.

6. Sisestage väljale **Tunnid** eraldatavad töötunnid.

![Joonis 2](media/02-consumption.png)

7. Klõpsake valikut **OK**.

*Näide*: alloleval kuvatõmmisel kuvatakse töökäsu töölehe read, mis sisaldavad kolme töökäsu tööd. Esimene rida, mis sisaldab kolme töötundi, on eraldatud ja üks töötund on registreeritud iga töökäsu töö kohta. Pärast kolme tunni registreerimise rea loomist saate valida, mida teha algse tunni registreerimise reaga (näite esimene rida). Saate selle jätta selliseks nagu ta on või selle kustutada. 

![Joonis 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Tarbimise registreerimiste finantsdimensioonid

Kui teete tarbimise registreeringuid, lisatakse eri registreerimise tüüpidega seotud finantsdimensioonid registreeringutele kindlas järjekorras. 

*Töö ja kulu registreeringud*: esimesena lisatakse finantsdimensioonid töölehe päisest, kui neid on. Järgmisena lisatakse seotud töökäsu projekti finantsdimensioonid. Viimasena lisatakse ressursi (töötaja) finantsdimensioonid.

*Kauba registreeringud*: esimesena lisatakse finantsdimensioonid töölehe päisest, kui neid on. Seejärel lisatakse seotud töökäsu projekti finantsdimensioonid. Järgmisena lisatakse koha finantsdimensioonid. Viimasena lisatakse kauba finantsdimensioonid.

>[!NOTE]
>Kõigi kolme registreerimise tüübi puhul on finantsdimensioonide kombinatsioon valideeritud ja kehtetud kombinatsioonid jäetakse tühjaks. See on standardne seadistus rakenduses Dynamics 365 for Finance and Operations.
