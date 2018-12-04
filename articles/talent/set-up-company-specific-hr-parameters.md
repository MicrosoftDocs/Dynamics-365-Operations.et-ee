---
title: "Ettevõttekohaste inimressursside (HR) parameetrite seadistamine"
description: "Mõne inimressursside (HR) parameetri sätteid jagatakse ettevõtete vahel, samas kui teiste parameetrite sätted on täiesti ettevõttepõhised. See artikkel selgitab, ettevõttepõhiste inimressursside parameetrite seadistamist."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRMParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: f7ecd72a2a6ba4ba15e412e40508462f6ef0d218
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="set-up-company-specific-human-resources-hr-parameters"></a>Ettevõttekohaste inimressursside (HR) parameetrite seadistamine

[!include [banner](includes/banner.md)]

Mõne inimressursside (HR) parameetri sätteid jagatakse ettevõtete vahel, samas kui teiste parameetrite sätted on täiesti ettevõttepõhised. See artikkel selgitab, ettevõttepõhiste inimressursside parameetrite seadistamist.

Inimressursside (HR) parameetrite määramiseks kasutatakse kahte lehte. Ettevõtetes ühiskasutatavate parameetrite puhul kasutate lehte **Inimressursside ühiskasutusega parameetrid**. Ettevõttekohaste parameetrite (teisisõnu sätted, mis rakenduvad ühele ettevõttele) puhul kasutate lehte **Inimressursside parameetrid**. Lehel **Inimressursside parameetrid** jaotatakse sätted kuue vahekaardi vahel.

-   Üldine
-   Värbamine – see ei sisaldu Dynamics 365 for Talentis
-   Hüvitus
-   Numbriseeriad
-   Perekondlikel ja meditsiinilistel põhjustel puudumine (FMLA)
-   Töötaja iseteenindus

Iga vahekaart sisaldab teavet, mis on seotud ühe ettevõttega. Sätted vahekaardil **Üldine** määratlevad puudumise, vigastuste ja haiguste ning uute värbamiste kohta käiva teabe ilmumise. Sellel vahekaardil olevad sätted määratlevad ka mõned vaikekirjed, mis ilmuvad töö tegemisel. Täpsemalt võimaldab see vahekaart teil valida värvi, mida rakendatakse avatud puudumiskannetele, määrata aruannetes kasutatava laadilehe, lubada koolituskursuste ja puudumiste registreerimise vaheline integratsioon ning valida puudumiskoodi, mida kasutada selle integratsiooni juhtimiseks. Samuti saate määrata, kui kaua vigastus- ja haigusjuhtude juhtumeid säilitada, ning vaike-ID-numbri, mida kuvatakse uue töötaja palkamisel. 

Vahekaardi **Värbamine** sätted määratlevad dokumendi tüübid, mida kasutatakse kandidaatidele automaatselt vastuse saatmiseks, ja värbamisprojekti, mida kasutatakse soovimatute avalduste puhul (avaldused, mis ei ole kindla värbamisprojektiga seotud). Värbamisprojekti ajalise jaotuse jaoks määratud periood määrab värbamisprojektid, mis on lisatud paanile **Projektide ajaline jaotus** tööruumis **Värbamise haldus**. Avalduse tähtaja hoiatusele määratud perioodi kasutatakse selliste värbamisprojektide kuvamiseks, mis lähenevad avalduse tähtajale paanil **Avalduse tähtaeg on lähenemas** tööruumis **Värbamine**. 

Vahekaardil **Hüvitus** olevad sätted määratlevad, kas kasutajad peavad kinnitama, et nad soovivad fikseeritud või ergutussüsteemi plaani jaoks teavet salvestada. Kui märgite ruudu **Lubada salvestamise valideerimine?**, saavad kasutajad iga kord, kui nad sulgevad hüvitusega seotud lehe, sõnumi, mis küsib, kas nad soovivad kirje salvestada. Mõned lehed hüvituste halduses ei lase kasutajatel teavet kustutada. Seega paludes kasutajatel kinnitada, et nad soovivad teabe salvestada, saate võib-olla piirata salvestatud teabe hulka, mida ei saa hiljem kustutada. Kui ruut **Lubada salvestamise kinnitamine** on tühi, salvestatakse kirjed alati kohe, võimalik, et enne seda, kui kasutaja on lõpetanud. Jõudlushalduse kasutamisel võimaldab vahekaart **Hüvitus** teil valida ka hindamismudeli, mida hindamisel mudelile määratud hüvituse plaanide asemel kasutada. 

### <a name="previously-released-functionality"></a>Varem välja antud funktsioonid
Vahekaardi **Numbriseeria** sätted määravad järjestuse, mida kasutatakse jaotises Inimressursid automaatselt ID-de määramiseks kaupadele, nagu rakendused, puudumise registreerimine, hüvitusprotsessi tulemused, juhtumite numbrid, kursused ja kursuste päevakorrad. Numbriseeria viidete ja koodide säilitamiseks kasutage loendi lehte **Numbriseeriad** (klõpsake valikuid **Organisatsiooni haldus** &gt; **Numbriseeriad** &gt; **Numbriseeriad**).

### <a name="if-youre-using-dynamics-365-for-talent"></a>Kui kasutate Dynamics 365 for Talentit
Vahekaardi **Numbriseeria** sätted määravad järjestuse, mida kasutatakse jaotises Inimressursid automaatselt ID-de määramiseks kaupadele, nagu rakendused, puudumise registreerimine, hüvitusprotsessi tulemused, juhtumite numbrid, kursused ja kursuste päevakorrad. Numbriseeria viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad** (klõpsake valikuid **Süsteemihaldus** &gt; **Linkide vahekaart** &gt; **Numbriseeriad** &gt; **Numbriseeriad**). 

Vahekaardi **FMLA** sätted määratlevad, mitu tundi peab töötaja töötama, et saada FMLA eeliseid, sobivuseks nõutava tööaja pikkuse ja töösuhte alguskuupäeva, mida kasutatakse tööaja pikkuse määramiseks. Sätted määratlevad ka FMLA tundide arvu, millele töötajatel õigus on, ja FMLA puhkuste kalendri, mida kasutatakse selleks, et arvutada, mitu FMLA tundi töötajad kasutanud on. Vahekaart **FMLA** on saadaval ainult USA ettevõtetele. 

**Märkus.** Töötundide arv ei tohi ületada 1250 tundi ja töösuhte pikkus ei saa olla pikem kui 12 kuud. Need maksimumväärtused on kooskõlas USA föderaalseadustega. Lõuks määravad vahekaardi **Töötaja iseteenindus** sätted teabe, mille juht saab oma töötajate nimel sisestada.

<a name="additional-resources"></a>Lisaressursid
--------

[Juriidilistele isikutele inimressursside parameetrite seadistamine](set-up-hr-parameters-across-legal-entities.md)




