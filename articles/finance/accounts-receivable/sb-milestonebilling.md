---
title: Vahe-etapi mallid
description: See artikkel selgitab, kuidas seadistada kordustellimuse arvelduse vahe-eesmärgi arveldusega seotud teavet.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d3c2cf751e4998c73bc3816e5b81e8d5963c8e53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856766"
---
# <a name="milestone-billing"></a>Etapiviisiline arveldus

[!include [banner](../includes/banner.md)]

See artikkel selgitab, kuidas määrata malle kordustellimuse arvelduse vahe-eesmärgi arveldusfunktsioonide jaoks. Vahe-eesmärgi malli iga rea jaoks saate määrata eraldamise protsendi või summa. Seejärel saate vahe-eesmärgi malli määrata arveldusgraafiku kaupadele, mis kasutavad vahe-eesmärgi arveldusfunktsiooni.

## <a name="add-a-template"></a>Malli lisamine

Vahe-eesmärgi malli lisamiseks järgige neid samme.

1. Minge kordustellimuse **arvelduse korduva \> lepingu arvelduse häälestuse \> vahe-eesmärkide \> mallidesse**.
2. Valige suvand **Uus**.
3. Sisestage **vahe-eesmärgi** malli väljale uue malli kordumatu ID.
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. **Valige väljal Eraldamismeetod** eraldamismeetod.
6. Valikuline: **määrake väljal** Kogusumma malli kogusumma.
7. Rea lisamiseks valige käsk **Lisa**. Seejärel valige **uue** rea kaubakood väljal Kaubakood.
8. Vastavalt eraldusmeetodi väljal valitud väärtusele järgige **ühte järgmistest sammudest**:

    - Kui valisite **eraldamismeetodiks** Protsent, määrake **väljal** Protsent iga rea eraldamisprotsent. Kui määrate protsendid, peab väljal Koguprotsent kuvatavate protsentide **summa** olema **100**.
    - Kui valisite **eraldamismeetodiks** Muutuv summa, **määrake** väljal Summa igale reale summa.
    - Kui valisite **eraldamise** meetodiks Võrdse summa, ei pea te summat määrama. Iga rida uuendatakse õige protsendi ja summaga, mis põhineb mallile lisatud kaupade arvul.

9. Valige käsk **Salvesta**.

## <a name="delete-a-template"></a>Malli kustutamine

Vahe-eesmärgi malli kustutamiseks järgige neid samme.

1. Valige üks või mitu kustutamisrida ja seejärel kustuta **.**
2. Kui teil palutakse tegevus kinnitada, valige väärtus **Jah**.

## <a name="milestone-template-fields"></a>Vahe-eesmärgi malli väljad

Vahe-eesmärgi **mallileht** sisaldab järgmisi välju.

| Väli | Kirjeldus |
|-------|-------------| 
| Vahe-etapi mall | Vahe-eesmärgi malli kordumatu ID. |
| Kirjeldus | Vahe-eesmärgi malli kirjeldus. |
| Eraldamismeetod | <p>Valige eraldamismeetod:</p><ul><li>**Valmimisprotsent** – iga rea puhul kasutatakse kumulatiivset lõpetamisväärtust.</li><li>**Protsent** – eraldamiseks saab määrata protsendi summa. Kõigi protsentide summa peab olema 100.</li><li>**Muutuv** summa – summa saab eraldamiseks määrata. Eraldamissumma määratakse kande tasemel.</li><li>**Võrdne summa** – eraldamisprotsendid arvutatakse automaatselt ja jagatakse mallis olevate kaupade vahel võrdselt.</li></ul> |
| Kokku | Määrake malli vahe-eesmärgi summa. |
| **Read** | |
| Kaubakood | Saate valida vahe-eesmärgi malli kaubakoodi. |
| Toote nimi | Kauba nimi. |
| Protsent | <p>Sisestage rea eraldamisprotsent:</p><ul><li>Kui välja **Eraldamismeetod** väärtuseks on **seatud** Protsent, määrake rea protsent.</li><li>Kui eraldamismeetodi **välja** väärtuseks **on seatud Võrdne** summa, jagatakse protsent automaatselt võrdseks protsendiks, mis põhineb mallis olevate kaupade arvul.</li></ul><p>Kõigi protsentide summa peab olema 100.</p><p>Kui päises **on** määratud kogusumma väärtus ja te muudate rea **protsentuaalset** väärtust, **uuendatakse** summa väärtus. Vastupidiselt, kui muudate summa **väärtust**, uuendatakse **protsentuaalset** väärtust.</p> |
| Summa | <p>Eraldussumma reale:</p><ul><li>Kui eraldamismeetodi **välja** väärtuseks on **seatud Muutuv** summa, määrake rea summa.</li><li>Kui eraldamismeetodi **välja** **väärtuseks** on seatud Võrdne summa, jagatakse summa automaatselt võrdseks summaks, **põhinedes** mallis olevate kaupade arvul ja päises määratud kogusumma väärtusel.</li></ul><p>Kõigi summade summa peab olema võrdne päises **määratud** kogusumma väärtusega.</p><p>Kui päises **on** määratud kogusumma väärtus ja te muudate rea **Summa** väärtust, **uuendatakse protsentväärtus**. Vastupidiselt, kui muudate **protsendiväärtust**, uuendatakse **summa** väärtus.</p> |
| **Kogusummad** | |
| Koguprotsent | Protsentide summa. Kõigi protsentide summa peab olema 100. |
| Kokku | Kõigi ridade **summaväärtuste** summa. See summa peab võrduma **päises** määratud kogusumma väärtusega. |
| Järelejäänud summa | Ülejäänud summa. See väärtus arvutatakse päise kogusumma **väärtusena**, millest on lahutatud kõigi **ridade summaväärtuste** summa.|

## <a name="milestone-allocation"></a>Vahe-etapi eraldamine

Enne vahe-eesmärkide funktsioonide kasutamist peaksite need ülesanded lõpule viima.

1. Saate lisada ühe või mitu vahe-eesmärgi malli.
2. Looge arveldusgraafiku grupp. Määrake **vahe-eesmärk** kauba tüübiks ja valige mall.
3. Kauba seadistamise **lehel** (korduvtellimuse arveldamine **\>\> Korduv lepingu arvelduse seadistusüksused \>**), valige kauba häälestuse jaoks kauba seos ja vahe-eesmärgi mall.

Pärast vahe-eesmärkide mallide, arveldusgraafiku gruppide ja kaupade loomist saate luua arveldusgraafiku, mis kasutab vahe-eesmärgi funktsioone.

Vahe-tähtaegu kasutav arveldusgraafiku loomiseks järgige neid samme.

1. Valige arveldusgraafikute **lehe loendist** Kõik/**aktiivsed arveldusgraafikud** uus **·**.
2. Looge lehel **Kõik arveldusgraafikud** uus arveldusgraafik ja määrake kliendi konto ja alguskuupäev.
3. Valige jaotises **Arveldusgraafiku read** suvand **Lisa rida**. Seejärel lisage kauba kood ja seadke kauba tüübi väli **vahe-eesmärgile** **·**.

    Kui kauba jaoks on seadistatud vahe-eesmärgi vaikemall, lisatakse vahe-eesmärgi sündmused automaatselt arveldusgraafiku ridadele. Vahe-eesmärgi ridade lõppkuupäevad on tühjad.

    Kui kauba jaoks pole vahe-eesmärgi malli seadistatud, valige vahe-eesmärgi **eraldamine**. Seejärel valige vahe-eesmärgi **eraldamise** lehel vahe-eesmärgi mall ja tehke nõutavad värskendused. Seejärel valige **Sule**, et naasta arveldusgraafikusse ja lõpetage arveldusgraafiku loomine.

4. Arveldusgraafiku jaoks arvete loomiseks peate värskendama iga vahe-eesmärgi sündmuse lõppkuupäeva. Üksiku arveldusgraafiku puhul saate uuendada vahe-eesmärgi sündmuse lõppkuupäeva arveldusgraafiku ridadel. Mitme arveldusgraafiku värskendamiseks valige suvand **Uuenda lõpetamise kuupäeva protsess**.
5. Pärast lõppkuupäeva uuendamist saate arve luua. Üksiku arveldusgraafiku jaoks valige arve **loomine** lehel **Kõik arveldusgraafikud**. Mitme arveldusgraafiku jaoks arvete loomiseks valige suvand Loo arve **või loo arve** **pakktöötlus perioodiliste** **ülesannete all**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Vahe-eesmärgi eraldamise redigeerimine arveldusgraafiku real

Vahe-eesmärgi eraldamise muutmiseks arveldusgraafiku real järgige neid samme.

1. Valige **arveldusgraafikute** > **kõik** **või** aktiivsed arveldusgraafikud väljal Graafiku number.
2. Jaotises Arveldusgraafiku **read sisestage** kaup, määrake kaubaks **vahe-eesmärk** ja valige vahe-eesmärgi **eraldamine**.
3. Valige vahe-eesmärgi **malli** väljal vahe-eesmärgi mall.
4. Valige **protsess**. Vahe-eesmärgi malli read lisatakse automaatselt arveldusgraafiku ridadele.

## <a name="milestone-allocation-fields"></a>Vahe-eesmärgi eraldamisväljad

Vahe-eesmärgi **eraldamisleht** sisaldab järgmisi välju.

| Väli | Kirjeldus |
|-------|-------------|
| Ülemkaup | Emaüksuse number. |
| Laiendatud hind | <p>Kauba laiendatud hind. Väärtus vastab arveldusgraafiku **rea** netosumma väärtusele.</p></p>Vahe-eesmärgi emakauba vaikeväärtus on vahe-eesmärgi **mallile** määratud kogusumma väärtus. Kui kogusumma on 0 (null), on vaikeväärtus **arveldusgraafiku** rea netosumma väärtus.</p> |
| Vahe-etapi mall | Reaüksuse vahe-eesmärgi malli ID. |
| Malli kirjeldus | Vahe-eesmärgi malli kirjeldus. |
| Eraldamismeetod | Vahe-eesmärgi mallis kasutatav eraldamismeetod. |
| **Read** | Kõigi ridade vaikeväärtused põhinevad valitud vahe-eesmärgi mallil. Saate neid vajadusel muuta. |
| Kaubakood | Vahe-eesmärgi eraldusmalli kaubakood. |
| Toote nimi | Toote nimetus |
| Protsent | <p>Rea eraldamisprotsent. Kõigi protsentide summa peab olema 100.</p><p>Rea protsentväärtuse **muutmisel** uuendatakse **netosumma** väärtus. Vastupidiselt, kui muudate netosumma **väärtust**, uuendatakse **protsent**.</p> |
| Netosumma | <p>Rea eraldamissumma. Kõigi ridade netosummade summa peab olema võrdne **päises** määratud laiendatud hinna väärtusega.</p><p>Rea netosumma **väärtuse** muutmisel uuendatakse **väärtus** Protsent. Vastupidiselt, kui muudate **protsendiväärtust**, uuendatakse **netosumma** väärtus.</p> |
| **Kogusummad** | |
| Koguprotsent | Kõigi ridade **protsendiväärtuste** summa. See summa peab võrduma 100-ga. |
| Kokku | Kõigi ridade **netosumma** väärtuste summa. See summa peab võrduma **päises** määratud laiendatud hinna väärtusega. |
| Järelejäänud summa | Ülejäänud summa. See väärtus arvutatakse päise **laiendatud hinnaväärtusena**, millest on lahutatud kõigi **ridade netosumma** väärtuste summa. Lõppsumma peab olema 0 (null). |
