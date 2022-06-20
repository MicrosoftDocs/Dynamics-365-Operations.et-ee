---
title: Lävelimiit ja erandi lävelimiit
description: See artikkel kirjeldab lähtekohas (TDS) mahaarvatud maksude läve ja erandi piiranguid.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: aceebad08b5454b64059e7ef374b9634bad35c37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877932"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Lävelimiit ja erandi lävelimiit

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab lähtekohas (TDS) mahaarvatud maksude läve ja erandi piiranguid. Arvete ja maksete TDS arvutatakse alati, võttes arvesse läve piirmäära ja erandi piirmäära, mis on määratletud TDS-i maksu komponentidele **kinnipeetava maksu komponentide** lehel. TDS-i maksukomponendid seotakse TDS-i maksukoodidega, mis sisalduvad TDS-i maksugruppides. TDS-i maksugrupid on seotud hankijate ja klientidega, et arvutada TDS arve- või maksetasemel.

TDS arvutatakse juhul, kui hankija kindla TDS-grupiga sisestatud kande summa või kumulatiivsed kanded ületavad **kinnipeetava maksu komponentide** lehel määratud läve piiri. TDS-i ei arvutata enne, kui kumulatiivne kandesumma ületab määratud läve piiri.

Kui TDS-komponendi lävilimiidile on määratud erandi läve limiit, siis arvutatakse TDS siis, kui konkreetne kandesumma ületab erandi läve piiri isegi juhul, kui kumulatiivne kandesumma ei ületa määratud läve piirmäära.

### <a name="example"></a>Näide
Maksukomponent nimega TDS on seadistatud ja seotud TDS-i maksugrupiga Peatöövõtja. Lävi on määratletud kui 50 000 ja TDS-maksukomponendi puhul on erandi lävi määratletud kui 20 000. TDS-i grupi töövõtja määratletakse vaikegrupina TDS hankijale 1.

Ostuarve 001 sisestatakse hankijale 1 summale 10000. TDS-i arve jaoks ei arvutata, kuna arve summa ei ületanud läve piirmäära või erandi läve limiiti. Ostuarve 002 sisestatakse hankijale 1 summale 25 000. TDS arvutatakse arve jaoks, kuna arve summa on ületanud erandlävendi piiri. Ostuarve 003 sisestatakse hankijale 1 summale 20 000. TDS arvutatakse arve kohta, sest hankijale väljastatud kolme arve arve kogusumma ületab lävipiiri. TDS arvutatakse kõigi hankijale väljastatud arvete alusel, mille kohta TDS ei ole varem arvutatud. Seepärast arvutatakse TDS 30 000-st, mis on arve kogusumma 001 ja 003.

TDS-kannetes TDS-i maksukoodiga seotud TDS-i maksukomponendile määratud läve limiidi ja erandi läve limiidi ignoreerimiseks märkige ära **Ei arvesta läve** ruut. Läve limiiti ei kasutata TDS-i maksukoodides TDS-grupis, mille jaoks on märkeruut **Ei arvesta läve**.

Kui mõne arve jaoks on valitud mõne kindla TDS-grupi jaoks märkeruut **Ei arvestata läve** kuid see pole valitud muude arvete jaoks, mis loodi konkreetse hankija/kliendi jaoks, võib TDS-i arvutamine ilma mõne arve lävepiiri kahe silma vahele jätta, võttes arvesse kumulatiivset summat kõigil arvetel, mille puhul TDS-i pole varemarvutatud.

Näiteks läve limiit on 25 000. Hankija A jaoks luuakse järgmised arved.

- Arve 1 – 20 000 – (**Ei arvesta läve** ruut ei ole valitud): TDS-i ei arvutata.

- Arve 2 – 4 000 – (**Ei arvesta läve** ruut on valitud): TDS-i ei arvutata 4 000.

- Arve 2 – 3000 – (**Ei arvesta läve** ruut ei ole valitud): TDS arvutatakse kumulatiivse arve summana, st 27 000 (20 000+4000+3000) ületanud läve piiri. TDS arvutatakse arvete kumulatiivsest summast, mille alusel TDS ei ole varem arvutatud, st 23 000 (20000+3000).
