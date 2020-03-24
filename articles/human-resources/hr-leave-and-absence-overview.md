---
title: Ülevaade
description: Tööruum **Puhkused ja puudumised** Dynamics 365 Human Resourcesis pakub paindlikku raamistikku uute puhkuseplaanide ja taotluste haldamise töövoogude loomiseks ning töötajate intuitiivset iseteeninduse lehte vabade päevade taotlemiseks.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 493bc3abe82103541125914896252b2eae596b38
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3091744"
---
# <a name="overview"></a>Ülevaade

Dynamics 365 Human Resources aitab teil pakkuda oma töötajatele suurepäraseid puhkusesoodustusi. Tööruum **Puhkused ja puudumised** pakub paindlikku raamistikku uute puhkuseplaanide ja taotluste haldamise töövoogude loomiseks ning töötajate intuitiivset iseteeninduse lehte vabade päevade taotlemiseks. Analüüs aitab teie organisatsioonil mõõta ja jälgida puhkuseplaanide saldosid ja kasutust.

## <a name="set-up-leave-and-absence"></a>Puhkuste ja puudumiste seadistamine

Enne oma töötajate jaoks puhkuseplaanide loomist peate läbima paar seadistuse etappi.

- [Puhkuste ja puudumiste parameetrite konfigureerimine](hr-leave-and-absence-parameters.md)
- [Tööajakalendri loomine](hr-leave-and-absence-working-time-calendar.md)
- [Puhkusetaotluse töövoo loomine](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Puhkuseplaanide loomine ja haldamine

Enne töötajale puhkuseplaanide loomist peate looma puhkuste ja puudumiste tüübid. Pärast puhkuseplaani loomist saate töötajaid plaanis registreerida. Saate käivitada ka koondamisprotsessi, luua teatisi ja vaadata oma plaanide analüüsi.

- [Puhkuste ja puudumiste tüüpide konfigureerimine](hr-leave-and-absence-types.md)
- [Puhkuse ja puudumise plaani loomine](hr-leave-and-absence-plans.md)
- [Töötajate puhkuste plaani määramine](hr-leave-and-absence-enroll.md)
- [Puhkuse ja puudumise plaanide koondamine](hr-leave-and-absence-accrue.md)
- [Puhkuste ja puudumiste analüüsi vaatamine](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Eemaloleku aja taotlemine ja taotluste haldamine

Teie töövõtjad võivad esitada eemaloleku aja taotlusi ja saate neid hallata tööruumis **Töövõtja iseteeninduskeskus**.

- [Eemaloleku aja taotlemine](hr-employee-self-service-request-time-off.md)
- [Puhkuse- ja puudumistaotluste haldamine](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Puhkuste ja puudumiste eelvaatefunktsioonid

Saate proovida uusi puhkuste ja puudumiste eelvaatefunktsioone keskkonnas **Liivakast**. Lisateavet eelvaatefunktsioonide sisselülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md). Eelvaatefunktsioonid hõlmavad järgmist.

- **Puhkuste ja puudumiste kalender** – puhkuse ja puudumiste parameetrid liiguvad suvandist **Inimressursside parameetrid** uuele ekraanile, mille nimi **Puhkuste ja puudumiste parameetrid**. Uus ekraan sisaldab uut vahekaarti **Kalender**. See eelvaade võimaldab ainult parameetrite alamkogumit. Pääsete uuele ekraanile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**. Kalendrid hõlmavad järgmist.
  - **Ettevõtte kalender** – kuvab kõik töövõtja eemalolekuaja taotlused. Inimesed rolliga **Inimressursid** pääsevad sellele kalendrile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**.
  - **Halduri töörühma kalender** – kuvab kõik otseste alluvate eemalolekuaja taotlused. Haldurid pääsevad kalendrile ligi vahekaardilt **Minu töörühm** töövõtja iseteeninduse jaotises **Puhkused ja puudumise**. 

- **Puhkuste ja puudumiste puhkuse kalendrid** – puhkuste tüübid sisaldavad uut valikut **Puhkus**, mida kasutatakse koos tööaja kalendriga. Pühade ja sulgemiste määratletud päevad määratakse nüüd tööpäevade loomisel kui **Püha**. Lisandumiste töötlemisel tehakse kalendrile määratud töövõtjatele korrigeerimisi, et arvestada pühadega, mis langevad tööpäevadele.

- **Puhkuse lisandumise auditeerimine** – uus ekraan võimaldab teil vaadata üle, kui lisandumisi on töödeldud ja kustutatud, nii kõikide töövõtjate kui ka üksikute töövõtjate poolt. Pääsete sellele uuele ekraanile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**.

- **Puudumise lisandumise kustutamine** – saate nüüd kustutada konkreetsete puhkuseplaanide lisandumiste kirjed. Pääsete sellele uuele suvandile ligi vahekaardilt **Lingid** tööruumis **Puhkused ja puudumised**. Üksikute töövõtjate puhul kuvatakse see suvand töötaja profiili rühmituses **Puhkused ja puudumised**. 

- **Puhkuse lisandumise ümardamine** – suvandi **Puhkuse tüüp** uued valikud määratlevad, mis tüüpi ümardamise lisandumist tuleks kasutada, koos lisandumise protsessi ajal ümardamise kümnendkoha täpsusega. Lisandumiste töötlemisel rakendatakse lisandumise kirjetele ümardamist ja täpsust. 

- **Mitme puhkuse tüübi konfigureerimine ühes puhkuseplaanis** – puhkuse tüüpide puhkuse lisandumise graafiku uus veerg võimaldab teil määratleda puhkuse ja puudumise plaanis mitu puhkuse tüüpi erinevate lisandumise graafikutega. Eelmine väli **Puhkuse tüüp** on eemaldatud. Töövõtja registreerimisel kuvatakse puhkuse tüüpide saldod nüüd ekraani ülaosa asemel tabelis.

  > [!IMPORTANT]
  > Pärast selle lubamist ei saa seda funktsiooni välja lülitada.

- **Kasutaja lisandumise jaoks töövõtja täistööaja vastet (FTE)** – puhkuste lisandumise graafiku uus veerg võimaldab lisandumiseks kasutada täistööaja vastet. Lisandumiste töötlemisel kasutab rakendus töövõtja esmast ametikohta ja määratud täistööaja vastet, et määrata eelmääratud lisandumise summa.

  > [!NOTE]
  > See funktsioon on saadaval ainult juhul, kui lubate suvandi **Mitme puhkuse tüübi konfigureerimine puhkuseplaanis**. 
