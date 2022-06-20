---
title: Kontserni parameetrid
description: See artikkel selgitab kontsernisiseseid parameetreid
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7a9b921c7db47fe99981438932e5587f9a18f018
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850521"
---
# <a name="intercompany-parameters"></a>Kontserni parameetrid

[!include [banner](../../includes/banner.md)]

Kontserniettevõttes saate seadistada parameetreid, mis määravad, kuidas kauplete erinevate juriidiliste isikute vahel. Neid parameetreid määravad teie valitud väljad. Saate valida erinevaid kombinatsioone, et kajastada erinevaid kaubandusstsenaariume.

Järgmistes näidetes kirjeldatakse üht kahetasemelist ja üht kolmetasemelist kontsernisisest organisatiooni.

## <a name="example-1-two-level-intercompany-chain"></a>Näide 1: Kahetasemeline kontserniahel

Kontsernisisene organisatsioon hõlmab järgmisi juriidilisi isikuid:

- Juriidiline isik A – Müüb kaupu välisklientidele, kuid ei oma aktsiaid. See juriidiline isik ostab juriidiliselt isikult B.
- Juriidiline isik B – müüb ainult juriidilisele isikule A.

Mõlemad juriidilised isikud saavad üksteisele müüa ja osta.

Selles näites põhineb väliskliendile suunatud algse müügitellimuse hinnakujundus alati müügihinnal. Kontsernisisese müügitellimuse ja ettevõtetevahelise ostutellimuse hinnakujundust kontrollib juriidilise isiku B kontsernisisese müügitellimuse sisemine müügi- või siirdehind.

Väliskliendi tellimuse päise teavet hallatakse algselt müügitellimuselt. Ühtegi kontsernisisese müügitellimuse muudatust ei sünkroonita algse müügitellimusega.

Juriidilisel isikul A Valige hankijate lehelt **Kontsernisisene** **Ostutellimuse poliitikad**. Valige väljagrupis **Algne müügitellimus (otsetarne)** järgnevad väljad:

- **Prindi saateleht automaatselt**
- **Sisesta arve automaatselt**
- **Prindi arve automaatselt**

Valige väljagrupis **Kontsernisisene ostutellimus (otsetarne)** järgnevad väljad:

- **Sisesta arve automaatselt**

Valige grupis **Algne müügitellimus <-> Kontsernisisene ostutellimus** järgnevad väljad:

- **Klienditeave**
- **RMA-kood**

Valige grupis **Algne ostutellimus <-> Kontsernisisene müügitellimus** järgnevad väljad:

- **Klienditeave**
- **RMA-kood**
- **Partii number**
- **Seerianumber**

Juriidilisel isikul B Valige klientide lehelt **Kontsernisisene** **Ostutellimuse poliitikad**. Valige väljagrupis **Kontsernisisese müügitellimuse loomine** järgnevad väljad:

- **Müügitellimuste nummerdamine** : **Ettevõte + algne number**
- **Luba dokumentide kokkuvõtte värskendust algkliendi jaoks**

Valige väljagrupis **Kontsernisiseste müügitellimuste hinnad** järgnevad väljad:

- **Hinna ja allahindluse otsing**
- **Luba hindade redigeerimine**
- **Luba allahindluse redigeerimine**

Valige grupis **Kontsernisisene ostuitellimus \> Kontsernisisene müügitellimus** järgnevad väljad:

- **Partii number**
- **Seerianumber**

## <a name="example-2-three-level-intercompany-chain"></a>Näide 2: Kolmetasemeline kontserniahel

Kontsernisisene organisatsioon hõlmab järgmisi juriidilisi isikuid:

- Juriidiline isik A – müügijuriidiline isik, kes müüb välisklientidele ja ostab juriidiliselt isikult B.
- Juriidiline isik B – tootmise või jaotuse juriidiline isik, kes ei saa tooteid tarnida ja ostab juriidiliselt isikult C.
- Juriidiline isik C – tootmise või jaotuse juriidiline isik, kes tarnib tooteid juriidilisele isikule B.

Juriidiliste isikute B ja C vahelised sisemised siirdehinnad on müügi juriidilise isiku kulul ahela alguses. See on kuluks ka juriidilisele isikule A, kes müüb kaupu välistele klientidele. Siiski põhineb algse müügitellimuse hinnakujundus alati väliskliendile kehtival müügihinnal.

Kontsernisiseste müügi- ja ostutellimuste hinnakujundust kontrollitakse kontsernisisesel müügitellimusel. Seda juhitakse ahela alguses. Seetõttu kontrollib hinda juriidiline isik C, kes müüb juriidilisele isikule B. Kontsernisisese müügitellimuse hinnakujundus põhineb sisemüügil või siirdehindadel, mis on seadistatud juriidilises isikus C.

Väliskliendi tellimuse päise teavet hallatakse algselt müügitellimuselt. Ühtegi kontsernisiseste tellimuste muudatust ei sünkroonita algse müügitellimusega.

Valitud peavad olema järgmised parameetrid:

Juriidilisel isikul A Valige hankijate lehelt **Kontsernisisene** **Ostutellimuse poliitikad**. Valige väljagrupis **Algne müügitellimus (otsetarne)** järgnevad väljad:

- **Prindi saateleht automaatselt**
- **Sisesta arve automaatselt**
- **Prindi arve automaatselt**

Valige väljagrupis **Kontsernisisene ostutellimus (otsetarne)** järgnevad väljad:

- **Sisesta arve automaatselt**

Valige väljagrupis **Algne müügitellimus <-> Kontsernisisene ostutellimus** järgnevad väljad:

- **Klienditeave**
- **RMA-kood**

Valige grupis **Algne ostutellimus <-> Kontsernisisene müügitellimus** järgnevad väljad:

- **Klienditeave**
- **RMA-kood**
- **Partii number**
- **Seerianumber**

Juriidilisel isikul B Valige klientide lehelt **Kontsernisisene** **Ostutellimuse poliitikad**. Valige väljagrupis **Kontsernisisese müügitellimuse loomine** järgnevad väljad:

- **Müügitellimuste nummerdamine** : **Ettevõte + algne number**
- **Luba dokumentide kokkuvõtte värskendust algkliendi jaoks**

Valige grupis **Kontsernisisene ostuitellimus \> Kontsernisisene müügitellimus** järgnevad väljad:

- **Partii number**
- **Seerianumber**

Valige väljagrupis **Kontsernisiseste klientide arvete postitamine** järgnevad väljad:

- **Ühikuhind võrdub omahinnaga**
- **Algse kliendiarve sisestamise käivitamine**

Juriidilisel isikul B Valige hankijate lehelt **Kontsernisisene** **Ostutellimuse poliitikad**. Valige väljagrupis **Algne müügitellimus (otsetarne)** järgnevad väljad:

- **Prindi saateleht automaatselt**
- **Sisesta arve automaatselt**
- **Prindi arve automaatselt**

Valige väljagrupis **Kontsernisisene ostutellimus (otsetarne)** järgnevad väljad:

- **Sisesta arve automaatselt**

Valige väljagrupis **Algne müügitellimus <-> Kontsernisisene ostutellimus** järgnevad väljad:

- **Klienditeave**
- **RMA-kood**
- **Hind ja allahindlus**

Valige grupis **Algne ostutellimus <-> Kontsernisisene müügitellimus** järgnevad väljad:

- **Klienditeave**
- **RMA-kood**
- **Partii number**
- **Seerianumber**

Juriidilisel isikul C Valige klientide lehelt **Kontsernisisene** **Ostutellimuse poliitikad**. Valige väljagrupis **Kontsernisisese müügitellimuse loomine** järgnevad väljad:

- **Müügitellimuste nummerdamine** : **Numbriseeria kood**
- **Luba dokumentide kokkuvõtte värskendust algkliendi jaoks**

Valige väljagrupis **Kontsernisiseste müügitellimuste hinnad** järgnev väli:

- **Hinna ja allahindluse otsing**

Valige väljagrupis **Kontsernisiseste klientide arvete postitamine** järgnevad väljad:

- **Ühikuhind võrdub omahinnaga**
- **Algse kliendiarve sisestamise käivitamine**

Valige väljagrupis **Kontsernisisene müügitellimus <-> Kontsernisisene ostutellimus** järgnevad väljad:

- **Partii number**
- **Seerianumber**

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
