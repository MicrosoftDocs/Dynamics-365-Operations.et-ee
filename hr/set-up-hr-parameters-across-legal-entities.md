---
title: Juriidiliste isikutele inimressursside parameetrite seadistamine
description: "Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmSharedParameters
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 51891
ms.assetid: c7d8f58c-d78a-4035-abbf-2b0ce16109fe
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: 5df6079605d2d8d320c38d302e8e5e2cba51a3f1
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-hr-parameters-across-legal-entities"></a>Juriidiliste isikutele inimressursside parameetrite seadistamine

Ettevõtete vahel ühiskasutuses olevate kirjete (nt ametikoha kirjete) puhul tuleb seadistada jagatud parameetrid. See artikkel selgitab juriidiliste isikute vahel inimressursside parameetrite seadistamist.

Mõnd tüüpi kirjeid, nt ametikohakirjeid, ühiskasutatakse kõikides ettevõtetes. Nende kirjete puhul peate seadistama ühiskasutatavad parameetrid. Kasutate näiteks lehte **Inimressursside ühiskasutusega parameetrid**, et seadistada inimressursside parameetrid juriidilistele isikutele. 

Lehel **Inimressursside ühiskasutusega parameetrid** on parameetrid rühmitatud piirkondadeks nende funktsiooni põhjal. 

Vahekaardil **ID** peate valima ID tüübid, mis esindavad lehel loetletud ID-koode. Peate seadistama ID tüübid enne, kui saate töötajatele ID teavet sisestada. Teave isikukoodi, rahvusliku ID-koodi, välismaalase ID-koodi ja isikliku ID-koodi kohta säilitatakse lehel **ID tüüp**. Uus ID tüübi määratlemiseks või vaadata olemasolevate tüüpide loendi, klõpsake **inimressursside**&gt;**Setup**&gt;**kood tüübid**. Saate sisestada lihtsa koodi ja kirjelduse. 

Vahekaardil **Numbriseeriad** saate valida numbriseeriad, mida kasutatakse järgmiste kirjete puhul: Personalinumber, Ametikoht, Kasutajanõude ID, I-9 dokument, Kandidaat, Arutelu, Soodustuse ID ja Personalitoiming (kui see kirje tüüp on lubatud). Numbriseeria viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad**. Selle lehe leidmiseks kasutage lehe otsimise funktsiooni. 

Osutage vahekaardil **Ametikohad**, kas määramisele on saadaval vaikimisi uusi ametikohti.

-   **Alati** – saate määrata töötajate uude asukohta, kui luuakse. Kui luuakse, on **saadaval loovutamise** kuupäeva ja kellaaja kohta ning **üldise** vahekaardil on **positsiooni** lehekülg on automaatselt seatud loomise kuupäev ja kellaaeg.
-   **Mitte kunagi** – töötajaid ei saa ametikohtade loomisel uutele ametikohtadele määrata. Selle suvandi valimisel peata avama lehe **Ametikoht** iga uue ametikoha jaoks kohe, kui see muutub kättesaadavaks, ja sisestama siis vahekaardile **Üldine** suvandi **Määramiseks saadaval **kuupäeva, et lubada töötaja määramine.


<a name="see-also"></a>Vt ka
--------

[Firma kindlad HR parameetrid](set-up-company-specific-hr-parameters.md)


