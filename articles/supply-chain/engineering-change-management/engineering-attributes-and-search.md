---
title: Tehnilised atribuudid ja tehnilise atribuudi otsimine
description: See artikkel selgitab, kuidas saate kasutada tehnikaatribuute kõigi mittestandardste omaduste määramiseks, tagamaks, et kõiki toote koondandmeid saab süsteemis registreerida. Samuti selgitatakse, kuidas saate kasutada tehnilise atribuudi otsingut, et leida tooteid lihtsasti nende registreeritud omaduste alusel.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4b25ab0bfda08b7aa091de8c6833007c586b9c87
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852559"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Tehnilised atribuudid ja tehnilise atribuudi otsimine

[!include [banner](../includes/banner.md)]

Kasutage tehnilisi atribuute kõigi mittestandardsete omaduste määramiseks, tagamaks, et kõiki toote koondandmeid saab süsteemis registreerida. Siis saate kasutada tehnilise atribuudi otsingut, et leida tooteid lihtsasti nende registreeritud omaduste alusel.

## <a name="create-engineering-attributes-and-attribute-types"></a>Tehniliste atribuutide ja tehnilise atribuudi tüüpide loomine

Tavaliselt on tehnilistel toodetel palju omadusi ja atribuute, mida peate talletama. Ehkki saate registreerida atribuute standardseid tootevälju kasutades, saate vajadusel luua ka uusi tehnilisi atribuute. Saate määratleda omaenda *tehnilised atribuudid* ja muuta need osaks tootemääratlusest.

Iga tehniline atribuut peab kuuluma *atribuuditüüpi*. See nõue on olemas, kuna igal tehnilisel atribuudil peab olema *andmetüüp*, mis määrab, millist tüüpi väärtusi see talletada võib. Tehnilise atribuudi tüüp võib olla standardne tüüp (nt vaba tekst, täisarv või kümnendarv) või kohandatud tüüp (nt tekst, mis sisaldab kindlat väärtuste kogumit, mille hulgast valida). Saate määrate igat atribuuditüüpi ükskõik kui paljudele tehnilistele atribuutidele.

### <a name="set-up-engineering-attribute-types"></a>Tehnilise atribuudi tüüpide seadistamine

Tehnilise atribuudi tüübi vaatamiseks, loomiseks või redigeerimiseks toimige järgmiselt.

1. Minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Atribuudid \> Atribuuditüübid**.
1. Valige loendipaanist olemasolev atribuuditüüp või valige toimingupaanil **Uus**, et luua uus atribuuditüüp.
1. Seadistage järgmised väljad.

    - **Atribuuditüübi nimi** – sisestage atribuuditüübi nimi.
    - **Tüüp** – valige standardne andmetüüp (*Valuuta*, *Kuupäev ja kellaaeg*, *Kümnendarv*, *Täisarv*, *Tekst*, *Loogiline muutuja* või *Viide*).
    - **Fikseeritud loend** – see suvand on saadaval ainult juhul, kui seate välja **Tüüp** väärtuseks *Tekst*. Määrake selle väärtuseks *Jah*, et määratleda seda tüüpi atribuutide jaoks kindlad väärtused. Sel juhul luuakse ripploend. Kiirkaarti **Väärtus** saab kasutada, et luua selle atribuuditüübi korral saadaolevad väärtused. Seadke selle suvandi väärtuseks *Ei*, et kasutajad saaksid sisestada mis tahes väärtuse. Sel juhul luuakse sisendiväli.
    - **Väärtuse vahemik** – see valik on saadaval ainult siis, kui seate välja **Tüüp** väärtuseks *Täisarv*, *Kümnendarv* või *Valuuta*. Seadke selle väärtuseks *Jah*, et luua miinimum- ja maksimumväärtus, mis on seda tüüpi atribuutide puhul lubatud. Saate kasutada kiirkaarti **Vahemik**, et määrata miinimum- ja maksimumväärtus ning (valuuta korral) valuuta, mis kehtib teie sisestatud piirangute puhul. Seadke selle suvandi väärtuseks *Ei*, et lubada ükskõik millist väärtust. 
    - **Mõõtühik** – see väli on saadaval ainult siis, kui seate välja **Tüüp** väärtuseks *Täisarv* või *Kümnendarv*. Valige mõõtühik, mis kehtib selle atribuuditüübi korral. Kui ühikut pole vaja, jätke see väli tühjaks.

### <a name="set-up-engineering-attributes"></a>Tehniliste atribuutide seadistamine

Tehnilise atribuudi vaatamiseks, loomiseks või redigeerimiseks toimige järgmiselt.

1. Minge jaotisse **Tehnilise muudatuse haldamine \> Seadistus \> Atribuudid \> Tehnilised atribuudid**.
1. Valige loendipaanist olemasolev atribuut või valige toimingupaanil **Uus**, et luua uus atribuut.
1. Seadistage järgmised väljad.

    - **Nimi** – sisestage atribuudi nimi. See nimi kuvatakse ainult lehel **Tehnilised atribuudid**. Kõikjal mujal süsteemis kuvatakse tavaliselt välja **Sõbralik nimi** väärtus, et atribuuti tuvastada.
    - **Atribuuditüüp** – valige eelmises jaotises määratletud atribuuditüüp.
    - **Sõbralik nimi** – sisestage nimi, mis näitab süsteemis, millise atribuudiga on tegemist (välja arvatud lehel **Tehnilised atribuudid**). 
    - **Kirjeldus** – sisestage atribuudi kirjeldus.
    - **Spikritekst** – sisestage spikritekst, mis annab teistele kasutajatele teada, milleks atribuut mõeldud on.
    - **Vaikeväärtus** – sisestage atribuudi vaikeväärtus. Kuvatavad valikud sõltuvad valitud atribuuditüübist.
    - **Valuuta** – kui valitud atribuuditüüp on valuuta, valige valuuta, mida atribuut aktsepteerib ja milles see väärtuseid kuvab.

1. Kui valitud atribuuditüüp on täisarv või kümnendarv, kuvatakse kiirkaart **Vahemik**. Seadistage sellel kiirkaardil järgmised väljad nii, nagu vaja.

    - **Hälbetegevus** – valige, kuidas süsteem peaks reageerima, kui kasutaja sisestab väärtuse väljaspool määratud vahemikku. Kui valite suvandi *Hoiatus*, kuvatakse hoiatus, kuid kasutaja saab väärtuse salvestada. Kui valite *Pole lubatud*, kuvatakse hoiatus ja väärtust ei saa salvestada enne, kui kasutaja selle parandab.
    - **Miinimum** – sisestage minimaalne soovitatav või aktsepteeritud väärtus.
    - **Maksimum** – sisestage maksimaalne soovitatav või aktsepteeritud väärtus.

### <a name="engineering-attribute-inheritance"></a>Tehnika atribuudi pärilus

Tootestruktuuride nagu materjali arvete (nt koosluste) või valemite puhul saab valitud atribuudid tütarüksustelt kuni emaüksusteni üle vaadata. Võite arvata sellest protsessist kui "pöörd pärilusest."

#### <a name="turn-engineering-attribute-inheritance-on-or-off"></a>Tehnika atribuudi päriluse sisse- või väljalülitamine

See funktsioon nõuab, et tehnika *muudatusehalduse ja* *täiustatud atribuudi pärilus tehnika muudatusehalduse funktsioonide* jaoks oleks teie süsteemi jaoks sisse lülitatud. Üksikasju selle kohta, kuidas neid funktsioone sisse või välja lülitada, vt tehnika [muudatusehalduse ülevaadet](product-engineering-overview.md).

#### <a name="attribute-inheritance-example"></a>Atribuutide päriluse häälestamine

Toiduaine, näiteks porgandikoogi puhul peab süsteem registreerima iga toote allergeeni. Porgandikooki saab süsteemis arvutada kui inseneritoodet, millel on valem. See valem sisaldab porgandikoogi koostisosi nagu näiteks jahu, piima, porgandit ja pähklit. Selles näites on ettevõttes kaks mudelit porgandikoogi jaoks: üks, mis sisaldab laktoosi ja teine, mis mitte.

Laktoosi sisaldaval koogil on koostisosade tasemel järgmised atribuudid:

- Koostisosa "jahu": atribuut "gluteen" = jah
- Koostisosa "piim": atribuut " laktoos" = jah
- Koostisosa "pähklid": atribuut "pähklid" = jah

Laktoosi mitte sisaldaval kook sisaldab laktoosivaba piima ja sel koostisosade tasemel järgmised atribuudid:

- Koostisosa "jahu": atribuut "gluteen" = jah
- Koostisosa "piim": atribuut " laktoos" = ei
- Koostisosa "pähklid": atribuut "pähklid" = jah

Kuna need tooted on enamasti sarnased, võib olla mugav läbida need atribuudid tütartoodetest (need kaks varianti) ematootele (baas porgandikook). "Tagasipööratud päriluse" juurutamiseks saate kasutada *atribuudi päriluse* funktsiooni. See funktsioon on määratud iga [tehnika versiooni](engineering-versions-product-category.md) jaoks.

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Tehniliste atribuutide ühendamine tehnilise toote kategooriaga

Mõned tehnilised atribuudid rakenduvad kõikidele toodetele, samas kui teised on omased üksikutele toodetele või tootekategooriatele. Näiteks ei ole mehaaniliste toodete puhul vaja elektrilisi atribuute. Seetõttu saate seadistada *tehnilise toote kategooriaid*. Tehnilise toote kategooria teeb kindlaks tehniliste atribuutide kogumi, mis peab kuuluma sellesse kategooriasse kuuluvate toodete määratluse hulka. Samuti saate määrata, millised tehnilised atribuudid on kohustuslikud ja kas on olemas vaikeväärtus.

Lisateavet selle kohta, kuidas töötada tehnilise toote kategooriatega, sealhulgas teavet atribuutide ühendamise kohta kategooriatega, leiate teemast [Tehnilised versioonid ja tehnilise toote kategooriad](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Tehniliste atribuutide väärtuste seadistamine

Tehnilise toote kategooriaga seotud tehnilised atribuudid esitatakse, kui loote uue tehnilise toote, mis põhineb sellel kategoorial. Siis saate seada atribuutide väärtused. Hiljem saab neid väärtusi muuta lehel **Tehniline versioon** või tehnilise muudatuse tellimuses tehnilise muudatuse haldamise käigus. Lisateavet vt teemast [Tehniliste toodete muudatuste haldamine](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Tehnilise toote loomine

Tehnilise toote loomiseks avage leht **Väljastatud tooted**. Siis valige toimingupaani vahekaardi **Toode** grupis **Uus** suvand **Tehniline toode**.

Peate määrama tehnilise kategooria, kuhu toode kuulub. Kategooria seab kõik toote vaikeväärtused ja -omadused. See määrab ka tootele rakenduvad atribuudid. Pärast kategooria valimist seatakse atribuutidele väärtused. Seejärel saate neid väärtusi muuta.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Toodete otsimine tehniliste atribuutide väärtuste abil

Saate kasutada tehnilise atribuudi otsingut toodete otsimiseks nende tehniliste atribuutide väärtuste järgi. Seetõttu saate hõlpsalt leida tehnilisi tooteid nende omaduste järgi. Saate otsida toodete seast, mis kuuluvad tehnilise toote kategooriasse, või otsida kõigi tehniliste toodete hulgast.

Otsing on saadaval toote koondandmete lehtedel ja süsteemi kandeüksustes, nt müügitellimustes. Kandeüksuse puhul saate kasutada toote otsimiseks lehte **Tehnilise atribuudi otsing**. Seejärel saate kasutada nuppu **Lisa uue reana**, et lisada toode müügitellimuse ridadele. Otsingutulemustes olevaid tooteid saab lisada ka otse tellimusele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
