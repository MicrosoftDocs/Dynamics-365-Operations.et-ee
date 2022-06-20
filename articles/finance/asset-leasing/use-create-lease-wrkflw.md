---
title: Rendi kinnitamise töövoogude kasutamine
description: See artikkel selgitab, kuidas kasutada töövooge põhivara liisimise kinnitamiseks ning kuidas jälgida töövoogude olekut ja ajalugu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4205b83919f0b3c30a4b5d8e3290af230f538f39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906438"
---
# <a name="use-lease-approval-workflows"></a>Rendi kinnitamise töövoogude kasutamine

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas kasutada töövooge põhivara liisimise kinnitamiseks ning kuidas jälgida töövoogude olekut ja ajalugu. Töövood aitavad viia rendilepingute kinnitamise halduse vastavusse, pakkudes standardset kinnitamise etappide komplekti ja määrates kindlad kasutajad igat protsessi etappi kinnitama. Kinnitaja saab rendilepingu kinnitada, selle tagasi lükata, taotleda selle muutmist või määrata selle teisele kasutajale kinnitamiseks. Töövood võivad tuua kinnitamise protsessi ka rohkem nähtavust, võimaldades teil nende olekut ja ajalugu jälgida. Lisaks saate vaadata tsentraliseeritud tööloendit, milles loetletakse kindlatele kinnitajatele määratud ülesanded ja kinnitused.

Enne selle protseduuri kasutamist veenduge, et loodud on vähemalt üks rendilepingu kinnitamise töövoog. Kui ühtegi töövoogu pole olemas, looge see. Lisateavet töövoo seadistamise kohta vaadake jaotisest [Rendilepingu kinnitamise töövoogude seadistamine](set-up-lease-wrkflw.md).

1. Rendilepingu esitamine kinnitamiseks. Valige rendi lehel **Raamatu üksikasjad** jaotis **Töövoog** ja seejärel valige **Esita**.
2. Saate lisada kuvatavasse dialoogiaknasse kommentaari. Määratud kinnitaja näeb seda kommentaari koos rendilepinguga. Kui olete kommentaari sisestamise lõpetanud, valige **Esita**. Rendileping esitatakse töövoo süsteemile ja kinnitaja saab selle kinnitamiseks.
3. Kinnitamiseks määratud rendilepingute vaatamiseks avage jaotis **Moodulid \> Üldine \> Tööüksused \> Mulle määratud tööüksused**.
4. Valige lehel **Mulle määratud tööüksused** link selle rendilepingu **Rendi ID**, mida soovite vaadata. Kuvatav lehekülg sõltub rendiraamatutest ja rendi üksikasjadest, millele teil on juurdepääs.
5. Kui olete rendilepingu vaatamise lõpetanud, valige **Töövoog** ja otsustage edasine tegevus. Valikute hulgas on **Kinnita**, **Lükka tagasi**, **Taotle muutmist**, **Delegeeri** ja **Tühista**. Saate valida ka valiku **Kuva ajalugu**, et vaadata valitud rendilepingu kinnituste ajalugu.
6. Pärast tegevuse valimist sisestage tegevuse kirjeldamiseks kommentaar. Kui olete kommentaari sisestamise lõpetanud, valige loendist toiming **Kinnitatud**.
7. Kinnitamise toimingute vaatamiseks minge tagasi lehele **Rendi üksikasjad** lehelt **Rendi kokkuvõte** ja valige seejärel **Töövoog \> Vaata ajalugu**.

    Töövoo tegevusi saate vaadata lehel **Töövoo ajalugu**. Sellel lehel kuvatakse töövoo etapid, mis on konkreetse rendilepingu puhul läbitud. Määratud tööüksuste oleku vaatamiseks võite kasutada ka välja **Tööüksused**.

8. Töövoo peatamiseks valige lehel **Töövoo ajalugu** käsk **Tühista**. Sisestage kuvatavasse dialoogiaknasse kommentaar ja seejärel valige **OK**.
9. Töövoo desaktiveerimiseks või eelnevalt loodud töövoo aktiveerimiseks avage jaotis **Vara rentimine \> Seadistamine \> Rendi töövoog**. Seejärel valige lehel **Tendi töövoog** jaotis **Töövoog \> Versioonid**. Praeguse töövoo passiivseks muutmiseks valige rendilepingu versiooni dialoogiaknas aktiivne rendileping ja seejärel valige **Muuda passiivseks**. Olemasoleva töövoo aktiivseks muutmiseks valige töövoog ja seejärel valige käsk **Muuda aktiivseks**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
