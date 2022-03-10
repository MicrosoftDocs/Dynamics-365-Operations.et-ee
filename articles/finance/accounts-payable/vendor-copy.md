---
title: Hankijate kopeerimine ühiskasutatavate numbriseeriate abil
description: Selles teemas selgitatakse, kuidas kasutada ühiskasutatavaid numbriseeriaid hankija kopeerimiseks teise juriidilisse isikusse, säilitades sama hankija ID.
author: sunfzam
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4cea8269082b39e2374ffb3c3dc82def8ce35679
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358461"
---
# <a name="copy-vendors-by-using-shared-number-sequences"></a>Hankijate kopeerimine ühiskasutatavate numbriseeriate abil

[!include [banner](../includes/banner.md)]

Saate kasutada hankija ID-de määramiseks ühiskasutatavaid numbriseeriaid Ühiskasutatavad numbriseeriad võimaldavad kopeerida hankijaid ühest juriidilisest isikust teise juriidilisse isikusse, kasutades mõlemas juriidilises isikus samu hankija ID-sid.

## <a name="setup"></a>Seadistamine

Funktsioon aktiveeritakse hankija ID-de määramisel ühiskasutatava numbriseeria kasutamisel. Peate kasutama sama numbriseeriat igas juriidilises isikus, kuhu soovite hankija kopeerida. Hankija numbriseeriat saate muuta iga juriidilise isiku lehel **Ostureskontro parameetrid**. Valige suvandid **Ostureskontro** \> **Seadistus** \> **Ostureskontro parameetrid** ja seejärel valige vahekaart **Numbriseeriad**.

Samuti saate seadistada hankija numbriseeriad iga hankijagrupi jaoks. Need numbriseeriad peavad samuti olema ühiskasutuses. Esmalt kasutatakse valitud hankijagrupi numbriseeriat. Kui hankijagrupile pole ühtki numbriseeriat määratud, kasutatakse lehel **Ostureskontro parameetrid** määratud numbriseeriat.

Käsitsi hankija ID-de kasutamisel saate hankijaid juriidiliste isikute vahel ka kopeerida. Kui aga püüate kopeerida hankija juriidilisse isikusse, kus hankija ID on juba olemas, siis kopeerimisprotsessi ei alustata.

## <a name="copy-a-vendor"></a>Hankija kopeerimine

Hankija kopeerimiseks valige loendilehel **Kõik hankijad** suvand **Uus**, et avada leht **Kõik hankijad, uus kirje**. Uut hankija ID-d ei määrata kohe. See käitumine erineb eelmiste versioonide käitumisest. Kuna hankijagrupp pole veel valitud, ei saa kasutamiseks määrata õiget numbriseeriat. Samuti ei saa see kindlaks teha, kas püüate luua uue hankija või hankija kopeerida. Seetõttu ei määrata hankija ID-d enne, kui valite lehe alaservast käsu **Salvesta**.

Uue hankija loomisel saate jätkata kõigi väljade täitmist, nagu seda tavaliselt teete. Kui olete lõpetanud ja valite käsu **Salvesta**, määratakse hankija ID automaatselt. Käsitsi numbriseeriate puhul näete, et kasutatakse teie käsitsi määratud hankija ID-d.

Hankija kopeerimiseks sisestage väljale **Nimi** üks või mitu tähte, mis otsitavat hankijat tähistavad. Otsingu dialoogiboksis kuvatakse loend osapooltest, kes võivad olla teie otsitavad hankijad. Mõne osapoole valimisel kuvatakse dialoogiboksi paremas servas lisateave.

- Vahekaardil **Üldine** kuvatakse osapoole telefoninumber ja aadress.
- Vahekaardil **Rollid** kuvatakse rollid, mis võivad valitud osapoolel olla, ja juriidiline isik, kus tal iga roll on.
- Vahekaardil **Maksukohustuslasena registreerimise ID** kuvatakse osapoolele määratud makuskohustuslasena registreerimise ID-d.

Saate osapoole kopeerida ainult siis, kui sellel on hankija roll ja kui sellel on roll juriidilises isikus, mis pole praegune juriidiline isik. Kui leiate kriteeriumidele vastava osapoole, tehke järgmist.

1. Kuvatakse suvand **Hankija kopeerimine**. Vaikimisi on selle suvandi säte **Ei**. Hankija kopeerimiseks praegusse juriidilisse isikusse määrake suvandi sätteks **Jah**. 
2. Kuvatakse väli **Juriidiline isik**. Valige juriidiline isik, millest hankija kopeerida. Kui hankija on olemas ainult ühes juriidilises isikus, on sellel väljal vaikimisi see juriidiline isik.
3. Valige käsk **Vali**. Luuakse uus hankija.

## <a name="validation"></a>Kinnitamine

Hankija kopeerimisel püütakse salvestada uue hankija teave. Kinnitamisi tehakse selleks, et kontrollida, kas kopeeritud andmed on korras. Iga nurjunud kinnitamise korral kuvatakse tõrketeade. Tõrketeated selgitavad, millist teavet tuleb värskendada. Hankija koopiat ei saa salvestada enne, kui olete kõik kinnitamistõrked kõrvaldanud.

## <a name="copy-a-vendor-by-using-the-tax-exempt-number-search-feature"></a>Hankija kopeerimine maksuvabastuse numbri otsingu funktsiooni abil

Hankijaid saab kopeerida ka **maksuvabastuse numbri** otsingu funktsiooni abil lehe **Kõik hankijad** toimingupaani vahekaardi **Hankija** rühmas **Registreerimine**. Avanevas dialoogiboksis **Maksuvabastuse numbri otsing** kuvatakse maksuvabastuse numbrid, hankija ID, hankija nimi ja juriidiline isik, kus maksuvabastuse ID-d kasutatakse. Hankija saate kopeerida ainult siis, kui see on juriidilises isikus, mis pole praegune juriidiline isik. Kui olete sellele kriteeriumile vastava hankija valinud, tehke järgmist.

1. Kuvatakse suvand **Hankija kopeerimine**. Vaikimisi on selle suvandi säte **Ei**. Hankija kopeerimiseks praegusse juriidilisse isikusse määrake suvandi sätteks **Jah**.
2. Valige käsk **Vali**. Luuakse uus hankija.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
