---
title: Varamõõdikud
description: Teemas selgitatakse varamõõdikute tüüpe rakenduses Asset Management.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: adadb1df7b41488fad496f937ecbc24e0761e42d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426366"
---
# <a name="counters"></a>Kassad

[!include [banner](../../includes/banner.md)]

Teemas selgitatakse loenduritüüpe rakenduses Asset Management. Loenduritüüpe kasutatakse loendurite registreerimiseks (nt tootmistundide arv, varas toodetud kogus). Varatüübid on seotud loenduritüüpidega. See tähendab, et loendurit saab kasutada vara puhul, kui loendur on seadistatud varas kasutatud varatüübile.

Enne loendurite registreerimist peate esmalt looma kasutatavad loenduritüübid üksuses **Loendurid**. Järgmisena saate luua loendurite registreerimised üksuses **Loendurid**. 

Loendureid saab kasutada hoolduskavades. Hoolduskava rea tüüp võib olla näiteks „Loendur”, mis on seotud tootmistundide arvu või toodetud kogusega. 

Loendurite registreerimist saab mõõtmise registreerimist saab uuendada käsitsi või automaatselt vastavalt tootmistundidele või toodetud kogusele. Loendurit saab seadistada kasutama ühte kolmest uuendusmeetodist (valitud üksuse **Loendurid** väljal **Uuendamine**):
  
- Käsitsi – peate loendurite väärtused käsitsi registreerima.  
- Tootmistunnid – loendur uuendatakse automaatselt tootmistundide arvu põhjal.  
- Tootmiskogus – loendur uuendatakse automaatselt toodetud koguse põhjal.  

>[!NOTE]
>Toodetud koguse kasutamisel kaasatakse *kõik* registreeritud kaubad loenduri registreeringusse – nii õiged kui ka veaga kogused. Vajadusel on alati võimalik teha loendurite käsitsi registreerimisi.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Loenduritüüpie loomine varaloenduri registreeringuteks

1. Valige **Varahaldu** > **Seadistus** > **Vara tüübid** > **Loendurid**.
2. Valige uue loenduritüübi loomiseks **Uus**.
3. Sisestage ID väljale **Loendur** ja loenduri nimi väljale **Nimi**.
4. Valige kiirkaardil **Üldine** loenduri ühik väljal **Ühik**.
5. Valige väljal **Uuendamine** loenduri jaoks kasutatav uuendusmeetod.
6. Valige „Jah” tumblernupul **Päri loenduri väärtused**, kui varastruktuuris olevad alamvarad peaksid automaatselt pärima emaettevõtte varades tehtud loendurite registreeringud.
7. Valige väljal **Kogusumma** summeerimismeetod seda loenduritüüpi kasutava loenduri jaoks. „Summa” on sandardne valik, mida kasutatakse registreeritud väärtuste pidevalks lisamiseks koguväärtusele. Väärtust „Keskmine” võib kasutada, kui loendur on seadistatud jälgima läve (nt vara temperatuur, vibratsioon või kulumine). 
8. Väljale **Hälve üle** sisestage ülemine tase protsentides, et valideerida, kas loenduri käsitsi registreerimine on eeldatud vahemikus. Valideerimine põhineb olemasolevate loendurite registreeringute lineaarsel suurenemisel.
9. Väljale **Hälve alla** sisestage alumine tase protsentides, et valideerida, kas loenduri käsitsi registreerimine on eeldatud vahemikus. Valideerimine põhineb olemasolevate loendurite registreeringute lineaarsel vähenemisel.
10. Väljal **Tüüp** valige teate tüüp (teave, hoiatus, tõrge), mis kuvatakse, kui ilmnevad hälbed väljaspool määratletud vahemikku, kui registreerite loendurit käsitsi.
11. Lisage kiirkaardil **Varade tüübid** varade tüübid, mis peaksid olema võimelised kasutama loendurit.
12. Lisage kiirkaardil **Seotud varaloendurid** see loendur, mida soovite selle loenduri uuendamisel automaatselt uuendada.


>[!NOTE]
>Seotud loendur uuendatakse automaatselt ainult juhul, kui seotud loenduril on vara tüüp, millega see on seotud loenduri seadistamisel. Näiteks: seadistate loenduri „tootmistundidele” ja lisate varatüübi „Veoauto mootor”. Kui seda loendurit uuendatakse, uuendatakse ka seotud loendur „Õli" sama loenduri väärtustega. Välja **Loenurid** seaditus sisaldab välja „Tunnid” seadistust. Loenduri seose tagamiseks tuleb ka loenduris „Õli” lisada varatüüp „Veoauto mootor” kiirkaardile **Varade tüübid**. Vaadake allolevatelt kuvatõmmistelt näidet tundide ja õli loenduri seadistamise kohta.

Kui väljale **Loendurid** on varade tüübid lisatud loenduri tüübile, siis lisatakse see loendur automaatselt varade tüüpidele kiirkaardil **Loendurid** üksuses [Varade tüübid](../setup-for-objects/object-types.md).

![Joonis 1](media/071-setup-for-objects.png)

