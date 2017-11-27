---
title: "Põhivarade seadistamine"
description: "Selles teemas antakse ülevaade põhivarade mooduli seadistusest."
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13771
ms.assetid: 8be64197-fea1-4a34-8af2-d939919c28b1
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7a578c5198feb8481a77180e3ed95077296f4638
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-fixed-assets"></a>Põhivarade seadistamine

[!include[banner](../includes/banner.md)]


Selles teemas antakse ülevaade põhivarade mooduli seadistusest.

<a name="overview"></a>Ülevaade
--------
Parameetrid juhivad põhivarade mooduli üldist käitumist.

Põhivaragrupid võimaldavad teil varasid grupeerida ja määrata igale gruppi määratud varale atribuute. Raamatud määratakse põhivaragruppidele. Raamatud jälgivad põhivara finantsväärtust aja jooksul, kasutades kulumireeglites määratletud kulumikonfiguratsiooni.

Põhivarad määratakse loomisel gruppi. Vaikimisi määratakse põhivaragrupile määratud raamatud seejärel põhivarale. Põhiraamatusse sisestamiseks konfigureeritud raamatud seostatakse sisestusreeglitega. Pearaamatukontod määratletakse sisestusreeglites iga raamatu kohta ja neid kasutatakse põhivarakannete sisestamisel. 

![FixedAssetsComponentsImage](./media/FAComponents_Updated.png)

## <a name="depreciation-profiles"></a>Kulumireeglid
Esmalt peaksite seadistama kulumireeglid. Kulumireeglites saate konfigureerida, kuidas vara väärtus aja jooksul amortiseerub. Peate määratlema kulumimeetodi, kulumiaasta (kalendriaasta või rahandusaasta) ja kulumi sageduse. Lisateavet vt teemast [Kulumiprofiilide seadistamine ja loomine](tasks/set-up-depreciation-profiles.md)

## <a name="books"></a>Raamatud
Pärast kulumireeglite seadistamist peate looma oma varade jaoks nõutavad raamatud. Iga raamat jälgib vara sõltumatut rahalist elutsüklit. Raamatud saab konfigureerida sisestama seostatud kandeid pearaamatusse. See konfiguratsioon on vaikesäte, kuna seda kasutatakse tavaliselt ettevõtte finantsaruandluses. Raamatud, mis pearaamatusse ei sisesta, sisestavad ainult põhivara alammoodulisse ja neid kasutatakse tavaliselt maksuaruandluses.

Igale raamatule määratakse esmane kulumireegel. Raamatutel on ka alternatiivsed või ülemineku kulumireeglid, kui seda tüüpi reeglid on kohaldatavad. Põhivara raamatu automaatseks kaasamiseks kulumi käitustesse peate lubama suvandi Arvuta kulum. Kui see suvand pole mõne vara puhul valitud, jätab kulumisoovitus vara vahele.

Saate seadistada ka tuletatud raamatuid. Määratud tuletatud kanded sisestatakse tuletatud raamatute suhtes esmase kande täpse koopiana. Seetõttu seadistatakse tuletatud kanded tavaliselt soetuste ja likvideerimiste, mitte kulumikannete jaoks.
Lisateabe saamiseks vt [Raamatute seadistamine](tasks/set-up-value-models.md).

## <a name="fixed-asset-posting-profiles"></a>Põhivarade sisestusreeglid
Pärast raamatute seadistamist saate luua sisestusreeglid. Sisestusreeglid tuleb määratleda raamatu järgi, kuid neid saab määratleda ka üksikasjalikumal tasemel. Näiteks saate määratleda sisestusreeglid raamatu ja põhivaragrupi kombinatsioonile või isegi üksiku põhivara raamatule. Vaikimisi kasutatakse määratletud pearaamatukontosid teie põhivarakannete jaoks.

Peate määratlema pearaamatukontod, mida kasutatakse likvideerimisprotsessides nii likvideerimismüügi kui ka likvideerimise mahakandmise puhul. Likvideerimisel tühistatakse varem sisestatud põhivarakanded algsetel kontodel ja netosummad teisaldatakse vara likvideerimisel sobivale kasumi ja kahjumi kontole. Kannete õigeks tühistamiseks peate seadistama kontod iga kandetüübi puhul, mida oma ettevõttes kasutate. Põhikontoks peaks olema algne konto, mille selle kandetüübi puhul sisestusreeglites seadistasite ja vastaskontoks peaks olema likvideerimiskonto puhul teie kasumi ja kahjumi konto. Erandiks on raamatupidamislik jääkväärtus. Sellisel juhul peaks nii põhi- kui ka vastaskonto olema seadistatud likvideerimiskonto puhul kasumi ja kahjumi kontole. Lisateabe saamiseks vt [Põhivara sisestusprofiilide seadistamine](tasks/set-up-fixed-asset-posting-profiles.md)

## <a name="fixed-asset-groups"></a>Põhivaragruppide tabel
Põhivaragrupp on põhivara loomisel ainus nõutav väli. Selle välja väärtus määratleb vara mitme teabevälja vaikeväärtuse. Raamatud seadistatakse nii, et vaikeraamat on määratud grupi igale varale. Seejärel saate määrata raamatutele atribuudid, mis on omased põhivaragrupile, nt Tööiga ja Kulumiarvestusreegel.

Saate ka määratleda kulumi erihüvitised või lisakulumi põhivaragrupi ja raamatu kindlale kombinatsioonile. Peate määrama kulumi erihüvitisele prioriteedi, et määrata hüvitiste arvutamise järjekorra, kui raamatule on määratud mitu hüvitist. Lisateabe saamiseks vt [Põhivaragruppide seadistamine](tasks/set-up-fixed-asset-groups.md)

## <a name="fixed-asset-parameters"></a>Põhivara parameetrid
Viimane etapp on põhivara parameetrite värskendamine.

Väli **Kapitaliseerimislävi** määratleb amortiseerunud varad. Kui põhivarana on valitud osturida, kuid see ei vasta määratud kapitaliseerimislävele, siis põhivara küll luuakse või värskendatakse, kuid suvandi Arvuta kulum sätteks on Ei. Seetõttu ei amortiseerita vara kulumisoovituste osana automaatselt.

Üks oluline suvand on **Kulumi korrigeerimissummade automaatne loomine likvideerimisel**. Kui valite selle suvandi sätteks **Jah**, korrigeeritakse vara amortiseerumist automaatselt, võttes aluseks kulumisätted vara likvideerimise ajal. Teine valik võimaldab soetussummast maha arvata skontod, kui soetate põhivarasid hankija arvega.

Kiirkaardil Ostutellimused saate konfigureerida, kuidas varasid ostuprotsessi osana luuakse. Esimene valik on Luba vara soetamine ostmiselt. Kui määrate selle suvandi sätteks Jah, toimub vara soetamine arve sisestamisel. Kui määrate selle suvandi sätteks Ei, saate põhivara ikkagi ostutellimusse ja arvesse paigutada, kuid soetamist ei sisestata. Sisestamine tuleb teha eraldi etapina põhivara töölehelt. Suvand Loo vara toote sissetuleku või arve sisestamise ajal võimaldab luua uue vara lennult – nii ei pea see enne kannet olema põhivarana seadistatud. Viimane võimalus Kontrolli põhivarade loomist rea sisestamisel rakendub ainult ostutaotlustele.

Saate konfigureerida põhjusekoode nii, et need on põhivara muudatuste või kindlate põhivarakannete puhul nõutavad.

Viimasena saate vahekaardil Numbriseeriad määratleda põhivarade numbriseeriad. Põhivara numbriseeria saab tühistada põhivaragrupi numbriseeriaga, kui see on määratud.

Lisateavet leiate teemast [Põhivara loomine](tasks/create-fixed-asset.md).


