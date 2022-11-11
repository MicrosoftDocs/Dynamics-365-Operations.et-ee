---
title: Negatiivsete vabade kogustega plaanimine
description: See artikkel selgitab, kui negatiivset vaba kaubavaru käsitletakse.
author: t-benebo
ms.date: 07/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: b4fc8b37fd800e3b4652513f150f9806bf1d5d67
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741118"
---
# <a name="planning-with-negative-on-hand-quantities"></a>Negatiivsete vabade kogustega plaanimine

[!include [banner](../../includes/banner.md)]

Kui süsteem näitab negatiivset kaubavaru kogust, käsitleb planeerimise mootor kogust kui 0 (null), et aidata vältida ületarnet. See funktsioon töötab järgmiselt.

1. Koondplaneerimise kokkuvõtted vabad kogused kattedimensioonide madalaima taseme puhul. (Kui asukoht ei ole *näiteks* laovarude dimensioon, koondab koondplaneerimise laotasemel vabad *kogused* .)
1. Kui laovarude dimensioonide kaubavaru kogus on negatiivne, eeldab süsteem, et vaba kogus on tegelikult 0 (null).

> [!IMPORTANT]
> Planeerimise süsteem võib olla ainult nii täpne kui sisendandmed. Kui sisendandmed on ebatäpsed, näitavad negatiivsed varude kirjed, et Microsoft Dynamics 365 Supply Chain Managementi varude teave on reaalse maailmaga sünkroonist väljas. Seetõttu on planeerimise tulemus vigane. Täpse planeerimise tulemuse saamiseks tuleb minimeerida kirjete arv, mis näitavad negatiivset vaba kogust.

## <a name="example-1"></a>Näide 1

Ladu 13 on konfigureeritud järgmisel viisil.

- **Katvuse kood:** min/max
- **Miinimum:** 15 tükki (tk)
- **Maksimum:** 25 tk

Laovarude dimensioonide madalaim tase on *ladu* ja järgmised vabad kogused salvestatakse *asukoha* tasemel.

- **Tegevuskoht 1, ladu 13, asukoht 1:** 20 tk
- **Tegevuskoht 1, ladu 13, asukoht 2:** &minus;8 tk

Seega on lao 13 kaubavaru kogus 12 tk (= 20 tk &minus; 8 tk).

Sellisel juhul kasutab planeerimise mootor kaubavaru kogust 12 tk lao 13 jaoks.

Tulemuseks on plaanitud tellimus 13 tk (= 25 tk &minus;12 tk), et täita ladu 13 koguselt 12 tk kogusele 25 tk.

## <a name="example-2"></a>Näide 2

Ladu 13 on konfigureeritud järgmisel viisil.

- **Katvuse kood:** min/max
- **Miinimum:** 15 tk
- **Maksimum:** 25 tk

Laovarude dimensioonide madalaim tase on *ladu* ja järgmised vabad kogused salvestatakse *asukoha* tasemel.

- **Tegevuskoht 1, ladu 13, asukoht 1:** 4 tk
- **Tegevuskoht 1, ladu 13, asukoht 2:** &minus;8 tk

Seega on lao 13 kaubavaru kogus &minus;4 tk (= 4 tk &minus; 8 tk). Teisisõnu on see vähem kui 0 (null).

Sellisel juhul eeldab planeerimise mootor, et lao 13 vaba kogus on 0 tk, mitte &minus;4 tk.

Tulemuseks on plaanitud tellimus 25 tk (= 25 tk &minus; 0 tk), et täita ladu 13 koguselt 0 tk kogusele 25 tk.

## <a name="planning-when-there-is-a-reservation-against-negative-on-hand-inventory"></a>Plaanimine negatiivse vaba kaubavaru reserveerimise korral

Kui korrigeerite varusid füüsilise reserveerimise ajal, saate põhjustada olukorra, kus tellimus reserveeritakse füüsiliselt negatiivse kaubavaru suhtes. Sellisel juhul peab teil reserveeritud koguse katteks olema tarne, kuna on olemas füüsiline reserveering. Varude täiendamist on seega vaja, seega loob süsteem kas plaanitud tellimuse koguse täiendamiseks, mida olemasolev vaba kaubavaru ei saanud katta, või katab selle kauba olemasoleva tellimusega.

Seda illustreerib järgmine näidisstsenaarium.

### <a name="example"></a>Näide

Süsteem on konfigureeritud järgmiselt.

- Toode *FG* on olemas ja seda on *10* tk. vaba kaubavaru.
- Toote konfiguratsioon lubab füüsilist negatiivset laovaru.
- Müügitellimus on olemas kogusele *10* tk. toodet *FG*.
- Müügitellimuse kogus reserveeritakse füüsiliselt olemasoleva vaba kaubavaru suhtes.

Seejärel korrigeerite toote FG kogust *nii*, et vaba kaubavaru saab 5. Kuna vaba kaubavaru on 5, reserveeritakse müügitellimuse kogus nüüd kogusega, mis ei ole vaba (oleks sarnane, kui vaba kaubavaru oleks 0 ja sel juhul reserveeritakse müügitellimus negatiivse laovaru suhtes). Kui käivitate nüüd koondplaneerimise, luuakse müügitellimuse tarnimiseks plaanitud tellimus kogusega 5 *FG* jaoks, sest koondplaneerimine kasutab alati olemasolevat tarnet või loob füüsilise reserveerimise tarnimiseks uue plaanitud tellimuse.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
