---
title: Varude puhvrite ja varude tasemete konfigureerimine
description: See artikkel selgitab, kuidas konfigureerida laopuhvriid ja laotasemeid, mis määravad laovarude saadavuse sõnumside saitidel Microsoft Dynamics 365 Commerce.
author: boycezhu
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: acfe71f7fb55f1bc701297bb3949e91d6450d9e9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853789"
---
# <a name="configure-inventory-buffers-and-inventory-levels"></a>Varude puhvrite ja varude tasemete konfigureerimine

[!include [banner](includes/banner.md)]

See artikkel selgitab, kuidas konfigureerida laopuhvriid ja laotasemeid, mis määratlevad laovarude saadavuse kohta saitidel sõnumite Microsoft Dynamics 365 Commerce saatmise.

Dynamics 365 Commerce'i peakorter hõlmab varude andmeid ja mitmesuguseid kanaleid, nagu näiteks kassarakendused, e-poe kauplused ja muud kohandatud integreeritud rakendused, mis liigutavad varusid asünkroonsel viisil. Seetõttu ei ole Commerce'i peakorteri vaba kaubavaru lehe, kassa kasutajaliidese ja e-poe kaupluste kaubavaru saadavuse API-de kaudu hangitud vaba kaubavaru väärtused reaalajas alati täiesti täpsed.

E-poe kauplustes tegelike kaubavaru väärtuste kuvamise asemel eelistavad paljud jaemüüjad kuvada teadet kauba saadavuse oleku kohta (nt „Olemas“ või „Otsas“), et anda klientidele teada, kas kaup on ostmiseks saadaval või potentsiaalselt laost otsas. Selle lähenemise puhul määravad varude puhvrid ja varude tasemed kindlaks, milline varude saadavuse teade tuleb teha kättesaadavaks ja konfigureerida.

## <a name="prerequisite-turn-on-the-inventory-buffers-and-inventory-levels-feature"></a>Eeltingimus: lülitage sisse varude puhvrite ja varude tasemete funktsioon

Varude puhvrite ja varude tasemete funktsiooni kontrollitakse Commerce'i peakorteris funktsioonihalduse kaudu. Funktsiooni sisselülitamiseks toimige järgmiselt.

1. Minge jaotisse **Süsteemihaldus** \> **Tööruumid** \> **Funktsioonihaldus**.
1. Otsige üles funktsioon **Luba varude puhvrid ja varude tasemed**, valige vastav rida ja seejärel **Luba kohe**.

Kui funktsioon on sisse lülitatud, siis leiate varude tasemed jaotises **Jaemüük ja kaubandus \> Varude haldus**.

## <a name="create-and-configure-an-inventory-level-profile"></a>Varude taseme profiili loomine ja konfigureerimine

*Varude taseme profiil* määratleb, kas antud tootekoguse olek on olemas, otsas või mõni muu kohandatud olek. Te saate luua ja konfigureerida ühe juriidilise isiku kohta mitu varude taseme profiili. Iga profiil koosneb varude tasemete kogumist ja igat taset määratlevad *vahemik*, *kood* ja *silt*.

- **Vahemik** – iga vahemik määratletakse väärtuste *algkogus* ja *lõppkogus* alusel. Koguse väärtus jääb vahemikku juhul, kui selle väärtus on suurem kui antud vahemiku algkogus ja väiksem kui lõppkogus.
- **Kood** – kood on taset tähistav siselühend. Otse varude API-dega integreerivad kliendid saavad kasutada koode selleks, et luua vastava varude taseme jaoks täiendavaid loogikaid. Näiteks saavad nad lülitada toote ostusaadavuse välja, kui varude taseme kood on **OOS** („otsas“).
- **Silt** – silt on tähenduslik kliendile suunatud teade, mis annab klientidele e-poe kaupluse saidil teada varude taseme.

### <a name="create-an-inventory-level-profile"></a>Varude taseme profiili loomine

Varude taseme profiili loomiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus** \> **Varude haldus** \> **Varude tasemed**.
1. Valige toimingupaanil suvand **Uus** ja seejärel sisestage väärtused väljadele **Profiili ID** ja **Kirjeldus**.
1. Uue taseme lisamiseks valige kiirkaardil **Vahemikud** suvand **Lisa** ja seejärel sisestage väärtused antud taseme veergudele **Algkogus**, **Lõppkogus**, **Kood** ja **Silt**. Korrake seda etappi täiendavate tasemete lisamiseks. Vajadusel saate väärtuseid andmeruudustikus redigeerida või valida taseme eemaldamiseks käsu **Kustuta**.
1. Valige toimingupaanil nupp **Salvesta**.

Kui uus profiil on loodud, siis lähtestatakse automaatselt kaks varude taset.

- **OOS** – tase „otsas“, kui vahemiku alampiir on negatiivne lõpmatus. Selle taseme kohta ei saa muuta algkogust ega koodi.
- **AVAIL** – tase „olemas“, kus vahemiku ülempiir on lõpmatus. Selle taseme kohta ei saa muuta lõppkogust ega koodi.

> [!NOTE]
> Vahemike vahel ei tohi olla profiili määratluses tühimikke ega kattuvusi.

Silditeate lokaliseeritud stringide konfigureerimiseks saate kasutada toimingupaanil nuppu **Tõlked**. Lokaliseeritud stringide kanalitega integreerimiseks peate käitama jaotusgraafiku töö **1110** (**Globaalne konfiguratsioon**).

### <a name="configure-an-inventory-level-profile"></a>Varude taseme profiili konfigureerimine

Varude taseme profiili saate konfigureerida tootekategooria tasemel või üksiktoote tasemel. Kui toote kohta on varude taseme profiil konfigureeritud, siis määratakse varude tase lingitud profiilis määratletud vahemike alusel. Muul juhul määratakse varude tase „olemas“ või „otsas“ vastavalt sellele, kas toote vaba kaubavaru kogus on positiivne.

Kategooria varude taseme profiili konfigureerimiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus** \> **Tooted ja kategooriad** \> **Kaubanduse tootehierarhia**.
1. Valige kategooria, mille kohta konfigureerida varude tase.
1. Valige kiirkaardil **Müüdava toote atribuudid** juriidiline isik.
1. Valige jaotises **Commerce'i varud** väljal **Varude taseme profiil** üks eelmääratletud varude taseme profiilidest.

Selleks, et lisada kategooriataseme profiili väärtus kategooria alustoodetele, saate kasutada toimingupaanil nuppu **Uuenda tooteid**. Lisateavet vt teemast [Tootekategooriate ja toodete haldamine](category-management-product-creation.md).

Väljastatud toote varude taseme profiili konfigureerimiseks toimige järgmiselt.

1. Tehke valik **Jaemüük ja kaubandus** \> **Tooted ja kategooriad** \> **Väljastatud tooted kategooria järgi**.
1. Valige toode ja avage seejärel toote üksikasjade leht.
1. Valige kiirkaardil **Müük** jaotises **Commerce'i varud** väljal **Varude taseme profiil** üks eelmääratletud varude taseme profiilidest.

Uue toote loomisel seadistatakse välja **Varude taseme profiil**, nagu ka paljude teiste tootetaseme atribuutide, väärtuseks selle kategooria väärtus, mis on konfigureeritud tootega seotud kategooriaga.

> [!NOTE]
> Varude taseme profiil on juriidilise isiku põhine atribuut. Sama kategooria või toote varude taseme profiil võib erinevate juriidiliste isikute puhul erineda.

Varude taseme profiilide konfiguratsioonide kanalitega sünkroonimiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus** \> **Jaemüügi ja kaubanduse IT** \> **Jaotusgraafik**.
1. Käivitage jaotusgraagik **1040** (**Toode**).

## <a name="configure-an-inventory-buffer"></a>Varude puhvri konfigureerimine

*Varude puhver* on kasutaja määratletud väärtus, mis lahutab kauba täiendava koguse algkogusest, et arvutada välja eeldatav kogus. Eeldatav kogus annab jaemüüjatele ohutu puhvri, et nad ei müüks toodet rohkem kui on tegelikult vaba kaubavaru raames saadaval. Varude puhvri profiili saate konfigureerida tootekategooria tasemel või üksiktoote tasemel. Kui varude puhvrid ei ole täpsustatud, siis kasutatakse vaikeväärtust **0** (null).

Kategooria varude puhvri profiili konfigureerimiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus** \> **Tooted ja kategooriad** \> **Kaubanduse tootehierarhia**.
1. Valige kategooria, mille kohta konfigureerida varude puhver.
1. Valige kiirkaardil **Müüdava toote atribuudid** juriidiline isik.
1. Sisestage jaotise **Commerce'i varud** välja **Varude puhver** positiivne väärtus.

Selleks, et lisada kategooriataseme puhvri väärtus kategooria alustoodetele, saate kasutada toimingupaanil nuppu **Uuenda tooteid**. Lisateavet vt teemast [Tootekategooriate ja toodete haldamine](category-management-product-creation.md).

Väljastatud toote varude puhvri profiili konfigureerimiseks toimige järgmiselt.

1. Tehke valik **Jaemüük ja kaubandus** \> **Tooted ja kategooriad** \> **Väljastatud tooted kategooria järgi**.
1. Valige toode ja avage seejärel toote üksikasjade leht.
1. Sisestage kiirkaardi **Müük** jaotise **Commerce'i varud** väljale **Varude puhver** positiivne väärtus.

Uue toote loomisel seadistatakse välja **Varude puhver** väärtuseks selle kategooria väärtus, mis on konfigureeritud tootega seotud kategooriaga.

> [!NOTE]
> Kui toote kohta on konfigureeritud nii varude puhver kui ka varude tase, siis kasutatakse varude taseme vahemiku arvutamiseks toote eeldatavat kogust (st algkogus miinus puhverväärtus).

Varude puhvrite konfiguratsioonide kanalitega sünkroonimiseks toimige järgmiselt.

1. Avage **Jaemüük ja kaubandus** \> **Jaemüügi ja kaubanduse IT** \> **Jaotusgraafik**.
1. Käivitage jaotusgraagik **1040** (**Toode**).

## <a name="use-inventory-buffers-and-inventory-levels-in-e-commerce-scenario"></a>Varude puhvrite ja varude tasemete kasutamine e-poe stsenaariumis

Kaubanduse saidiehitaja kasutab varude puhvri ja varude taseme võimalusi Commerce'i peakorteris selleks, et määrata kindlaks e-kaubanduse saitidel kasutatavad varude saadavuse sõnumid. Lisateavet vt teemast [Varude sätete rakendamine](inventory-settings.md).

Teise võimalusena saate kolmanda isiku e-kaubanduse lahendusega integreerimise korral kasutada API-sid **GetEstimatedAvailability** ja **GetEstimatedProductWarehouseAvailability**, et kuvada oma e-kaubanduse stsenaariumis toote varude saadavus. Antud API-de kohta lisateabe saamiseks vt teemat [Jaemüügikanalite jaoks varude saadavuse arvutamine](calculated-inventory-retail-channels.md).

Varude puhvrite ja varude tasemete juurutamine võimaldab neil API-del tagastada kogu saadaolevate väärtuste ja saadaolevate füüsiliste väärtuste alusel määratletud varude taseme koodid ja silditeated. API-sid saab täiendavalt veelgi konfigureerida, et need määratleksid, kas teatega koos esitatakse ka varude kogus ning kas saadaolevast kogusest lahutatakse varude puhvri väärtus.

Toote kättesaadavuse API-de vastuse konfigureerimiseks toimige järgmiselt.

1. Minge jaotisse **Jaemüük ja kaubandus** \> **Peakontori seadistamine** \> **Parameetrid** \> **Kaubanduse parameetrid**.
1. Valige väärtus jaotise **Kaupluse varud** vahekaardi **Varud** väljal **Toote saadavuse API-d e-kaubanduses**.
1. Sätete kanalil rakendamiseks käivitage jaotusgraafiku töö **1110** (**Globaalne konfiguratsioon**).

## <a name="additional-resources"></a>Lisaressursid

[Tootekategooriate ja toodete haldamine](category-management-product-creation.md)

[Varude sätete rakendamine](inventory-settings.md)

[Varude saadavuse arvutamine jaemüügikanalite jaoks](calculated-inventory-retail-channels.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
