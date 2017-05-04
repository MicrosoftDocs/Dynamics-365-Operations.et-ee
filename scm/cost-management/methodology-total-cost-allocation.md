---
title: Kogukulu eraldamise meetod
description: "See artikkel sisaldab juhiseid kogukulu eraldamise (TCA) kohta. TCA on meetod kulude arvutamiseks partiitellimuse peamise valemi üksuse ja valemile määratletud kaastoodete vahel."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c26dcc5a8caa461bce90f931bb5c584f1816526b
ms.lasthandoff: 03/31/2017


---

# <a name="total-cost-allocation-method"></a>Kogukulu eraldamise meetod

See artikkel sisaldab juhiseid kogukulu eraldamise (TCA) kohta. TCA on meetod kulude arvutamiseks partiitellimuse peamise valemi üksuse ja valemile määratletud kaastoodete vahel.

Kogukulude eraldamine (TCA) on meetod kulude arvutamiseks partiitellimuse peamise valemi üksuse ja valemile määratletud kaastoodete vahel. See meetod on dünaamiline. See arvutab kulu valemi üksuse puhul lõpetatuks märgitud koguste ja kaastoodete vahelise kaalutud keskmisena. TCA-d kasutatakse, kulude eraldamisi pole vaja iga partiitellimuse puhul üle vaadata. Kui TCA-d ei kasutata, kasutab valemi arvutus olemasolevat funktsiooni.

## <a name="using-tca-for-coproducts"></a>TCA kasutamine kaastoodete puhul
Siin on mõned juhised TCA kasutamise kohta kaastoodetes.

-   Kui määrate valemiversiooni liuguri **Kogukulude eraldamine** väärtuseks **Jah**, peab kaastoodetel olema omahind, mis on suurem kui 0 (null). Väärtuse saab tuua sama laoala või mitte-laoalapõhise valemi esimese laoala aktiivsest kuluversioonist. See tingimus kinnitatakse valemi kinnitamisel.
-   Kui määrate valemiversiooni liuguri **Kogukulude eraldamine** väärtuseks **Jah** ja järgmised tingimused on tõesed, on kulueralduse meetod **TCA** ja kulueralduse protsent ei muutu.
    -   Lisasite kaastooteid.
    -   Kasutasite kaastoodete puhul teist kulueraldusmeetodit.
-   Kui määrate valemiversiooni liuguri **Kogukulude eraldamine** väärtuseks **Ei** ja järgmised tingimused on tõesed, määratakse kulueralduse meetodiks **Käsitsi** ja kulueralduse protsent ei muutu.
    -   Lisasite kaastooteid.
    -   Kulueralduse protsent on suurem kui 0 (null).
-   Enne, kui on võimalik valemi arvutuse edukas sooritamine, tuleb hinnata kulueralduse protsente. Selle toimingu saab teha käsitsi või kasutades valikut **Eeldatav omahind** lehel **Kaastooted**. **Märkus:** valik **Eeldatav omahind** on saadaval ainult siis, kui liugur **Kogukulude eraldamine** on valemiversiooni puhul asendis **Jah**. Saate vaadata eeldatavat eraldamist, lõpetatuna kinnitatud partiitellimuse kogused vastavad valemis kuvatud kogustele.
-   Kui partiitellimus luuakse käsitsi või plaanitud partiitellimus kinnitatakse, kopeeritakse valemiversiooni liuguri **Kogukulude eraldamine** väärtus partiitellimusse. Kuid seda sätet saab partiitellimuses muuta. Kui liugur **Kogukulude eraldamine** on valemiversiooni puhul asendis **Ei** ja see viiakse siis partiitellimuse puhul asendisse **Jah**, määratakse iga rea puhul, mille olek oli **Käsitsi**, kulueraldusmeetodiks **TCA**. Kulueraldus **Pole** jääb muutmata. Kui liugur **Kogukulude eraldamine** on valemiversiooni puhul asendis **Jah** ja see viiakse siis partiitellimuse puhul asendisse **Ei**, määratakse iga kaastoote puhul, mille tüüp on **Tootmine**, kulueraldusmeetodiks **Käsitsi**. Kõik hinnangulised kulueralduse protsendid jäävad muutmata.
-   Lehel **Kaastoote kulu eraldamine** on näha arvutatud kulueralduse protsent. Selle lehe saate avada loendilehelt **Partiitellimus**. Sellest teabest on abi, kui kajastatavad tooted ja kogused erinevad partiitellimusel plaanitud või käivitatud kogustest. Kui kulu on lõpetatud, kuvatakse need TCA uued protsendieraldused lehel **Kaastoote kulu eraldamine**.

## <a name="calculating-the-burden-for-byproducts"></a>Kõrvalsaaduste koormuse arvutamine
Väli **Kõrvalsaaduse kulu eraldamine** lehel **Kaastooted** on numeraatori väli, mida kasutatakse ainult kõrvalsaaduste puhul. Kaastoodete puhul on selle välja väärtus alati **Pole**. Kõrvalsaaduse ridade puhul määratleb see väli, kuidas kõrvalsaaduse rea kulusumma tootmise kogukulule lisatakse. Valikud on järgmised:

-   **Pole** – selle kõrvalsaaduse sea puhul ei lisata tootmise kogukulule ühtegi summat.
-   **Protsent** – omahind arvutatakse tootmises tarbitud toormaterjalide kogukulu protsendina. Väljale sisestatakse arvutuses kasutatav protsent.
-   **Seeria kohta** – omahind arvutatakse summana tootmistellimuse standardpartii suuruse kohta. See summa ei sõltu tootmises kinnitatud kogusest. Väljale sisestatakse arvutuses kasutatav summa.
-   **Koguse kohta** – omahind arvutatakse summana tootmise valemiüksuse kinnitatud koguse kohta. Väljale sisestatakse arvutuses kasutatav summa.



