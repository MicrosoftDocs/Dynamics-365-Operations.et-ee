---
title: Varamõõdikud
description: Teemas selgitatakse varamõõdikute tüüpe rakenduses Asset Management.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783217"
---
# <a name="asset-measures"></a>Varamõõdikud

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Teemas selgitatakse varamõõdikute tüüpe rakenduses Asset Management. Varamõõdikute tüüpe kautatakse varade mõõdikute registreerimiseks (nt tootmistundide arv, varas toodetud kogus). Varatüübid on seotud varamõõdikute tüüpidega. See tähendab, et varamõõdikut saab kasutada vara puhul, kui varamõõdik on seaditatud varas kasutatud varatüübile.

Enne varamõõdikute registreerimist peate smalt looma kasutatavad varamõõdikute tüübid üksuses **Loendur**. Järgmisena saate luua varade mõõdikute registreerimised üksuses **Varamõõdikud**. 

Varamõõdikuid saab kasutada hoolduskavades. Hoolduskava rea tüüp võib olla näiteks „Loendur”, mis on seotud tootmistundide arvu või toodetud kogusega. 

Varamõõdkute registreerimist saab mõõtmise registreerimist saab uuendada käsitsi või automaatselt vastavalt tootmistundidele või toodetud kogusele. Varamõõdikut saab seadistada kasutama ühte kolmest uuendusmeetodist (valitud üksuse **Loendurid** väljal **Uuendamine**):
  
- Käsitsi – peate varamõõdikute väärtused käsitsi registreerima.  
- Tootmistunnid – loendur uuendatakse automaatselt tootmistundide arvu põhjal.  
- Tootmiskogus – loendur uuendatakse automaatselt toodetud koguse põhjal.  

>[!NOTE]
>Toodetud koguse kasutamisel kaasatakse *kõik* registreeritud kaubad mõõdikute registreeringusse – nii õiged kui ka vealised kogused. Vajadusel on alati võimalik teha varamõõdikute käsitsi registreerimisi.

## <a name="create-counter-types-for-asset-counter-registrations"></a>Loenduritüüpie loomine varaloenduri registreeringuteks

1. Valige **Varahaldu** > **Seadistus** > **Vara tüübid** > **Loendurid**.
2. Valige uue varamõõdiku tüübi loomiseks **Uus**.
3. Sisestage ID väljale **Loendur** ja loenduri nimi väljale **Nimi**.
4. Valige kiirkaardil **Üldine** mõõtühik väljal **Ühik**.
5. Valige väljal **Uuuendmine** varamõõdiku jaoks kasutatv uuendusmeetod.
6. Valige „Jah” tumblernupul **Päri loenduri väärtused**, kui varastruktuuris olevad alamvarad peaksid automaatselt pärima emaettevõtte varades tehtud mõõdikute registreeringud.
7. Valige väljal **Kogusumma** summeerimismeetod seda varamõõdiku tüüpi kasutava varamõõdiku jaoks. „Summa” on sandardne valik, mida kasutatakse registreeritud väärtuste pidevalks lisamiseks koguväärtusele. Väärtust „Keskmine” võib kasutada, kui varamõõdik on seadistatud jälgima läve (nt vara temperatuur, vibratsioon või kulumine). 
8. Väljale **Hälve üle** sisestage ülemine tase protsentides, et valideerida, kas varamõõdiku käsitsi registreerimine on eeldatud vahemikus. Valideerimine põhineb olemasolevate varamõõdikute registreeringute lineaarsel suurenemisel.
9. Väljale **Hälve allpool** sisestage alumine tase protsentides, et valideerida, kas varamõõdiku käsitsi registreerimine on eeldatud vahemikus. Valideerimine põhineb olemasolevate varamõõdikute registreeringute lineaarsel vähenemisel.
10. Väljal **Tüüp** valige teate tüüp (teave, hoiatus, tõrge), mis kuvatakse, kui ilmnevad hälbed väljaspool määratletud vahemikku, kui registreerite varamõõdikut käsitsi.
11. Lisage kiirkaardil **Varade tüübid** varade tüübid, mis peaksid olema võimelised kasutama varamõõdikut.
12. Lisage kiirkaardil **Seotud varamõõdikud** need varamõõdikud, mida soovite selle varamõõdiku uuendamisel automaatselt uuendada.


>[!NOTE]
>Seotud varamõõdik uuendatakse automaatselt ainult juhul, kui seotud varamõõdikul on vara tüüp, millega see on seotud varamõõdiku seadistamisel. Näiteks: seadistate varamõõdiku „tootmistundidele” ja lisate varatüübi „Veoauto mootor”. Kui seda varamõõdikut uuendatakse, uuendatakse ka seotud loendur „Õli" sama varamõõdiku väärtustega. Välja **Loenurid** seaditus sisaldab välja „Tunnid” seadistust. Varamõõdiku seose tagamisekes tuleb ka varamõõdikus „Õli” lisada varatüüp „Veoauto mootor” kiirkaardile **Varade tüübid**. Vaadake allolevatelt kuvatõmmistelt näidet tundide ja õli varamõõdiku seadistamise kohta.

Kui väljale **Loendurid** on varade tüübid lisatud varamõõdiku tüübile, siis lisatakse see varamõõdik automaatselt varade tüüpidele kiirkaardil **Loendurid** üksuses [Varade tüübid](../setup-for-objects/object-types.md).

![Joonis 1](media/071-setup-for-objects.png)


