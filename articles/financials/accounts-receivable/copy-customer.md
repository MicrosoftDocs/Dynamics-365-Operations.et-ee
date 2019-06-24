---
title: Klientide kopeerimine ühiskasutatavate numbriseeriate abil
description: Selles teemas selgitatakse, kuidas kasutada ühiskasutatavaid numbriseeriaid kliendi kopeerimiseks teise juriidilisse isikusse, säilitades sama kliendi ID.
author: mikefalkner
manager: aolson
ms.date: 08/31/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 7a1e6c6e3a995ad745522d58960e850d72c2ee57
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556268"
---
# <a name="copy-customers-by-using-shared-number-sequences"></a>Klientide kopeerimine ühiskasutatavate numbriseeriate abil

[!include [banner](../includes/banner.md)]

Saate kasutada kliendi ID-de määramiseks ühiskasutatavaid numbriseeriaid Ühiskasutatavad numbriseeriad võimaldavad kopeerida kliente ühest juriidilisest isikust teise juriidilisse isikusse, kasutades mõlemas juriidilises isikus samu kliendi ID-sid.

## <a name="setup"></a>Seadistamine

Funktsioon aktiveeritakse kliendi ID-de määramisel ühiskasutatava numbriseeria kasutamisel. Peate kasutama sama numbriseeriat igas juriidilises isikus, kuhu soovite kliendi kopeerida. Kliendi numbriseeriat saate muuta iga juriidilise isiku lehel **Müügireskontro parameetrid**. Valige suvandid **Müügireskontro** \> **Parameetrid** ja seejärel valige vahekaart **Numbriseeriad**.

Samuti saate seadistada kliendi numbriseeriad iga kliendigrupi jaoks. Need numbriseeriad peavad samuti olema ühiskasutuses. Esmalt kasutatakse valitud kliendigrupi numbriseeriat. Kui kliendigrupile pole ühtki numbriseeriat määratud, kasutatakse lehel **Müügireskontro parameetrid** määratud numbriseeriat.

Käsitsi kliendi ID-de kasutamisel saate kliente juriidiliste isikute vahel ka kopeerida. Kui aga püüate kopeerida kliendi juriidilisse isikusse, kus kliendi ID on juba olemas, siis kopeerimisprotsessi ei alustata.

## <a name="copy-a-customer"></a>Kliendi kopeerimine

Kliendi kopeerimiseks valige loendilehelt **Kõik kliendid** suvand **Uus**, et avada dialoogiboks **Kliendi loomine**. Pange tähele, et uut kliendi ID-d ei määrata kohe. See käitumine erineb teenuse Microsoft Dynamics 365 for Finance and Operations eelmiste versioonide käitumisest. Kuna kliendigrupp pole veel valitud, ei saa süsteem määrata kasutamiseks õiget numbriseeriat. Samuti ei saa see kindlaks teha, kas püüate luua uue kliendi või kliendi kopeerida. Seetõttu ei määrata kliendi ID-d enne, kui valite dialoogiboksi alaservast käsu **Salvesta**.

Uue kliendi loomisel saate jätkata kõigi väljade täitmist, nagu seda tavaliselt teete. Kui olete lõpetanud ja valite käsu **Salvesta**, siis näete, et kliendi ID on automaatselt määratud. Käsitsi numbriseeriate puhul näete, et kasutatakse teie käsitsi määratud kliendi ID-d.

Kliendi kopeerimiseks sisestage väljale **Nimi** üks või mitu tähte, mis otsitavat klienti tähistavad. Otsingu dialoogiboksis kuvatakse loend osapooltest, kes võivad olla teie otsitavad kliendid. Mõne osapoole valimisel kuvatakse dialoogiboksi paremas servas lisateave.

- Vahekaardil **Üldine** kuvatakse osapoole telefoninumber ja aadress.
- Vahekaardil **Rollid** kuvatakse rollid, mis võivad valitud osapoolel olla, ja juriidiline isik, kus tal iga roll on.
- Vahekaardil **Maksukohustuslasena registreerimise ID** kuvatakse osapoolele määratud makuskohustuslasena registreerimise ID-d.

Saate osapoole kopeerida ainult siis, kui sellel on kliendi roll ja kui sellel on roll juriidilises isikus, mis pole praegune juriidiline isik. Kui leiate kriteeriumidele vastava osapoole, tehke järgmist.

1. Kuvatakse suvand **Kliendi kopeerimine**. Vaikimisi on selle suvandi säte **Ei**. Kliendi kopeerimiseks praegusse juriidilisse isikusse määrake suvandi sätteks **Jah**. 
2. Kuvatakse väli **Juriidiline isik**. Valige juriidiline isik, millest klient kopeerida. Kui klient on olemas ainult ühes juriidilises isikus, on sellel väljal vaikimisi see juriidiline isik.
3. Valige käsk **Vali**. Luuakse uus klient.

## <a name="validation"></a>Kinnitamine

Kliendi kopeerimisel püüab süsteem salvestada uue kliendi teabe. Kinnitamisi tehakse selleks, et kontrollida, kas kopeeritud andmed on korras. Iga nurjunud kinnitamise korral kuvatakse tõrketeade. Tõrketeated selgitavad, millist teavet tuleb värskendada. Kliendi koopiat ei saa salvestada enne, kui olete kõik kinnitamistõrked kõrvaldanud.

## <a name="copy-a-customer-by-using-tax-exempt-number-search-feature"></a>Kliendi kopeerimine maksuvabastuse numbri otsingu funktsiooni abil

Kliente saab kopeerida ka maksuvabastuse numbri otsingu funktsiooni abil lehe **Kõik kliendid** toimingupaani vahekaardi **Klient** grupis **Registreerimine**. Avanevas dialoogiboksis **Maksuvabastuse numbri otsing** kuvatakse maksuvabastuse numbrid, kliendi ID, kliendi nimi ja juriidiline isik, kus maksuvabastuse ID-d kasutatakse. Kliendi saate kopeerida ainult siis, kui see on juriidilises isikus, mis pole praegune juriidiline isik. Kui olete sellele kriteeriumile vastava kliendi valinud, tehke järgmist.

1. Kuvatakse suvand **Kliendi kopeerimine**. Vaikimisi on selle suvandi säte **Ei**. Kliendi kopeerimiseks praegusse juriidilisse isikusse määrake suvandi sätteks **Jah**. 
2. Valige käsk **Vali**. Luuakse uus klient.
