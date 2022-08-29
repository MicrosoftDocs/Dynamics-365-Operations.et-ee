---
title: Pakktöö loomine
description: Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.
author: matapg007
ms.date: 11/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: matgupta
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
ms.openlocfilehash: 06fb9a18e70c316be97645ba76f9462cd3ccc729
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292446"
---
# <a name="create-a-batch-job"></a>Pakktöö loomine

[!include [banner](../../includes/banner.md)]

Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks. Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate. Kasutage pakett-töö loomiseks järgmist protseduuri. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.


## <a name="create-the-batch-job"></a>Pakett-töö loomine
1. Avage **Navigatsioonipaan > Moodulid > Süsteemihaldus > Päringud > Pakett-tööd**.
2. Valige suvand **Uus**.
3. **Sisestage väljale** Töö kirjeldus pakett-töö kirjeldus.
4. Väljale Plaanitud **alguskuupäev/-kellaaeg** sisestage kuupäev ja kellaaeg, millal pakett-töö peaks käivituma.
5. Valige käsk **Salvesta**.

## <a name="create-a-recurrence"></a>Korduvuse loomine
1. Valige tegevuspaanil pakett-töö **·**.
2. Valige **kordumine**. Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.  
3. Valige nupp **OK**.

## <a name="add-alerts"></a>Teatiste lisamine
1. Valige tegevuspaanil pakett-töö **·**.
2. Valige **teatised**. Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse. Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.   
3. Valige nupp **OK**.

## <a name="add-a-task-to-a-batch-job"></a>Tööülesande lisamine pakett-tööle
1.  Valige pakett-tööde **lehel** suvand **Kuva ülesanded**.
2.  Valige **Ctrl+N** ülesande loomiseks.
3.  Sisestage pakett-töö kirjeldus.
4.  Väljal Ettevõtte **kontod** valige ettevõtte andmebaas, kus ülesannet peaks käitama.
5.  Valige väljal **Klassi** nimi protsess, mida ülesanne peaks käitama. 
6.  Valige ülesandele sobiv partiigrupp.

    Klienditoimingud peavad olema partiigrupile määratud. Need määratakse automaatselt vaikepartiigruppi (nimetatakse ka partiigrupiks Tühi).

7.  Valige **Ctrl+S**, et tööülesanne salvestada.
8.  Et teha valitud ülesanne sõltuvaks töö teisest ülesandest, valige Suvand On tingimuste ruudustik ja järgige seejärel neid samme iga tingimuse puhul, **mida** soovite määratleda:

    1. Valige **ctrl+N** tingimuse loomiseks.
    2. Valige emaülesande ülesande ID.
    3. Valige olek, milleni emaülesanne peab jõudma, enne kui sõltuvat ülesannet saab käitada.
    4. Valige **Ctrl+S**, et tingimus salvestada.

    Kui määrate rohkem kui ühe tingimuse *ja kui kõik* tingimused peavad olema täidetud, enne kui sõltuvat ülesannet saab käitada, valige tingimuse tüüp **Kõik**. Kui sõltuvat ülesannet saab *käitada* pärast mis tahes tingimuste täitmist, valige tingimuse tüüp Mis **tahes**.

9.  Valige, kuidas tuleks ülesande tõrkeid käsitseda. Konkreetse ülesande nurjumise ignoreerimiseks valige vahekaardil **Üldine** **selle** ülesande puhul suvand Ignoreeri toimingu nurjumist. Kui see suvand on valitud, ei põhjusta ülesande nurjumine töö nurjumist. Samuti saate kasutada välja **Suurim uuestisaatmise** katsed, et määrata, mitu korda tuleb ülesannet uuesti proovida, enne kui see loetakse nurjutuks. Hea tava on soovitatav mitte seada väljale Maksimaalne **uuestisisestud** arv väärtuseks, mis on rohkem kui **5**.

    Lisateavet pakett-töö uuestisüümise kohta vt luba [pakett-töö uuesti käivitamine](../retryable-batch.md).

## <a name="adjust-batch-job-status"></a>Pakett-töö oleku reguleerimine
1. Avage **Süsteemihaldus > Päringud > Pakett-tööd**.
2. Valige sobiv pakett-töö.
3. Tegevuspaanil valige pakett-töö **, > funktsioonid > olekut muuta**.
4. Valige asjassepuutuv olek.
    - **Kinnipeetud**: seadke pakett-töö olekuks **kinnipeetud** nii, et see on pakett-töö toiminguajastist kinni peetud. Sama kui *peatus*.
    - **Ootel**: seadistage pakett-töö olekuks **ootel**, et see ootaks pakett-töö ajasti poolt üleskorjamist. Sama kui *mine*.
5. Valige nupp **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
