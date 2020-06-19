---
title: Inimressursside parameetrite konfigureerimine
description: Mõne inimressursside parameetri sätteid jagatakse ettevõtete vahel, samas kui teiste parameetrite sätted on täiesti ettevõttepõhised. See artikkel selgitab, ettevõttepõhiste inimressursside parameetrite seadistamist.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428729"
---
# <a name="configure-human-resources-parameters"></a>Inimressursside parameetrite konfigureerimine

Mõne inimressursside (HR) parameetri sätteid jagatakse ettevõtete vahel, samas kui teiste parameetrite sätted on täiesti ettevõttepõhised. See artikkel selgitab, ettevõttepõhiste inimressursside parameetrite seadistamist.

Inimressursside (HR) parameetrite määramiseks kasutatakse kahte lehte. Ettevõtetes ühiskasutatavate parameetrite puhul kasutate lehte **Inimressursside ühiskasutusega parameetrid**. Ettevõttekohaste parameetrite (teisisõnu sätted, mis rakenduvad ühele ettevõttele) puhul kasutate lehte **Inimressursside parameetrid**. Lehel **Inimressursside parameetrid** jaotatakse sätted kuue vahekaardi vahel.

-   Üldine
-   Värbamine – see ei sisaldu rakenduses Dynamics 365 Human Resources
-   Kompensatsioon
-   Numbriseeriad
-   Perekondlikel ja meditsiinilistel põhjustel puudumine (FMLA)
-   Töötaja iseteenindus

Iga vahekaart sisaldab teavet, mis on seotud ühe ettevõttega. Sätted vahekaardil **Üldine** määratlevad puudumise, vigastuste ja haiguste ning uute värbamiste kohta käiva teabe ilmumise. Sellel vahekaardil olevad sätted määratlevad ka mõned vaikekirjed, mis ilmuvad töö tegemisel. Täpsemalt võimaldab see vahekaart teil valida värvi, mida rakendatakse avatud puudumiskannetele, määrata aruannetes kasutatava laadilehe, lubada koolituskursuste ja puudumiste registreerimise vaheline integratsioon ning valida puudumiskoodi, mida kasutada selle integratsiooni juhtimiseks. Samuti saate määrata, kui kaua vigastus- ja haigusjuhtude juhtumeid säilitada, ning vaike-ID-numbri, mida kuvatakse uue töötaja palkamisel. 

Vahekaardi **Värbamine** sätted määratlevad dokumendi tüübid, mida kasutatakse kandidaatidele automaatselt vastuse saatmiseks, ja värbamisprojekti, mida kasutatakse soovimatute avalduste puhul (avaldused, mis ei ole kindla värbamisprojektiga seotud). Värbamisprojekti ajalise jaotuse jaoks määratud periood määrab värbamisprojektid, mis on lisatud paanile **Projektide ajaline jaotus** tööruumis **Värbamise haldus**. Avalduse tähtaja hoiatusele määratud perioodi kasutatakse selliste värbamisprojektide kuvamiseks, mis lähenevad avalduse tähtajale paanil **Avalduse tähtaeg on lähenemas** tööruumis **Värbamine**. 

Vahekaardil **Hüvitus** olevad sätted määratlevad, kas kasutajad peavad kinnitama, et nad soovivad fikseeritud või ergutussüsteemi plaani jaoks teavet salvestada. Kui märgite ruudu **Lubada salvestamise valideerimine?**, saavad kasutajad iga kord, kui nad sulgevad hüvitusega seotud lehe, sõnumi, mis küsib, kas nad soovivad kirje salvestada. Mõned lehed hüvituste halduses ei lase kasutajatel teavet kustutada. Seega paludes kasutajatel kinnitada, et nad soovivad teabe salvestada, saate võib-olla piirata salvestatud teabe hulka, mida ei saa hiljem kustutada. Kui ruut **Lubada salvestamise kinnitamine** on tühi, salvestatakse kirjed alati kohe, võimalik, et enne seda, kui kasutaja on lõpetanud. Jõudlushalduse kasutamisel võimaldab vahekaart **Hüvitus** teil valida ka hindamismudeli, mida hindamisel mudelile määratud hüvituse plaanide asemel kasutada. 

### <a name="previously-released-functionality"></a>Varem välja antud funktsioonid

Vahekaardi **Numbriseeria** sätted määravad järjestuse, mida kasutatakse jaotises Inimressursid automaatselt ID-de määramiseks kaupadele, nagu rakendused, puudumise registreerimine, hüvitusprotsessi tulemused, juhtumite numbrid, kursused ja kursuste päevakorrad. Numbriseeria viidete ja koodide säilitamiseks kasutage loendi lehte **Numbriseeriad** (klõpsake valikuid **Organisatsiooni haldus** &gt; **Numbriseeriad** &gt; **Numbriseeriad**).

> [!NOTE]
> Töötundide arv ei tohi ületada 1250 tundi ja töösuhte pikkus ei saa olla pikem kui 12 kuud. Need maksimumväärtused on kooskõlas USA föderaalseadustega. Lõpuks määravad vahekaardi **Töövõtja iseteenindus** sätted teabe, mille juhid saavad oma töövõtjate nimel sisestada.
