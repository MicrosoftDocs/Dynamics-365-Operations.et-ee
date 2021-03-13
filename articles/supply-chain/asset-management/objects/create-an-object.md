---
title: Vara loomine
description: Selles teemas kirjeldatakse, kuidas varasid varahalduses luua.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28c4685c3b6f543324953cd03646d5b15fdb8c59
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019425"
---
# <a name="create-an-asset"></a>Vara loomine

[!include [banner](../../includes/banner.md)]

 

Selles teemas kirjeldatakse, kuidas varasid varahalduses luua.

1. Valige **Varahaldus** > **Ühised** > **Varad** > **Kõik varad** või **Aktiivsed varad**.
2. Klõpsake nuppu **Uus**.
3. Dialoogiaknas **Loo varad** saate sisestada **Vara** (vara ID) ja vara nime andmed. Valige vara kuupäev ja kellaaeg väljal **Jõustunud**. Sellest kuupäevast alates saate vara installida töö asukohta, samuti vara teisaldada ja asendada vara struktuuris.
4. Väljal **vara tüüp** valige vara jaoks vara tüüp (kohustuslik väli). Vajadusel valige vara jaoks **Vara tootja** ja **Vara mudel**. Kui on seadistatud ainult üks toode, valitakse see toode automaatselt väljal **Vara tootja**. Väljadel **Vara tootja** ja **Varamudel** saadaolevad valikud olenevad seadistusest jaotises [Vara tootja ja mudel](../setup-for-objects/product-and-model.md).
5. Grupi **Emaettevõtte vara** väli **Vara** tühi vaikimisi. Vajadusel saate valida emaettevõtte vara ja seejärel täidetakse kõik **Emaettevõtte vara** grupi väljad automaatselt.
    >[!NOTE]  
    >Kui valite emaettevõtte vara, siis on saadaval kaks või kolm vahekaarti: vahekaart **Minu varad** sisaldab varasid, mis on seotud töö asukohtadega, kuhu teid (hooldustöötaja, kes on süsteemi logitud) on määratud. Kui töö asukohti pole seadistatud hooldustöötajale vormil [Hooldustöötajad ja töötajarühmad](../setup-for-objects/workers-and-worker-groups.md), pole vahekaart **Minu varad** nähtav. Vahekaart **Aktiivsed varad** sisaldab kõigi varade loendit, mille vara töötsükli olek on „Aktiivne”. Vahekaardil **Varade vaade** kuvatakse töö asukohtade puuvaade ja nendesse asukohtadesse paigaldatud varad.

6. Teie seadistatud töö vaikeasukohaks soovitatakse vara jaoks väljal **Vara** grupp > **Töö asukoht**. Valige vajadusel mõni muu töö asukoht.

    >[!NOTE]
    >Kui olete vara loonud, saate selle vajadusel paigaldada muule töö asukohale. Töö asukohta saab paigutada ainult ülataseme varasid (praeguse emaettevõtte varata varad). See tähendab, et installite nii ülataseme kui ka kõik valitud töö asukohas olevad tütarvarad. Lisateavet töö asukohtades olevate varade kohta lugege teemast [Töö asukohtade sissejuhatus](../functional-locations/introduction-to-functional-locations.md).

7. Klõpsake valikut **OK**.
8. Lisateabe lisamiseks varale valige vara loendis **Kõik varad** ja klõpsake nuppu **Muuda**.

## <a name="general-information"></a>Üldteave

Töö asukoht, millega vara on seotud, kuvatakse väljal **Töö asukoht**. Kui vara on emaettevõtte vara, kuvatakse varaga seotud tütarüksuste arv väljal **Tütarükused**. Kui vara on olemasoleva vara alamvara, kuvatakse emaettevõtte vara ID väljal **Emaettevõtte vara**.

Saate redigeerida **vara tootja** ja **vara mudeli** teavet vara kohta, mida kasutatakse varuosade, alternatiivsete varuosade ja töö tüüpi vaikeväärtuste haldamiseks. Lisateabe saamiseks vaadake teemat [Vara tootjad ja mudelid](../setup-for-objects/product-and-model.md). Vajadusel saate lisada teabe **Mudeli aasta** ja **Seerianumbri** kohta.

Valikut **Praegune töötsükli olek** kasutatakse selleks, et määrata, kas vara on aktiivne või passiivne. Vara loomisel seatakse etapp alati varaetapi grupi esimesele etapile. Kui olete valmis aktiveerima vara, klõpsake nuppu **Uuenda vara olekut** ja valige töötsükli olek, mille olete määratlenud kui „aktiivne vara” ja klõpsake nuppu **OK.**

**Märkus.** Kui vara väärtuseks on seatud „passiivne”, pole enam võimalik vara töökäske luua. Samuti ei saa planeerida passiivse vara ennetava hoolduse töid.

Väljad **Teenuse tase** ja **Kriitilisus** on seotud vara jaoks loodud töökäskudega. Väljadel kuvatakse vara praeguse seadistuse jaoks arvutatud valikute **Teenusetase** ja **Kriitilisus** arvud. Nende väärtuste seadistamise kohta lugege teemasid [Varade teenusetasemed](../setup-for-objects/object-priorities.md) ja [Vara kriitilisustüübid](../setup-for-objects/object-criticalities.md).

## <a name="asset"></a>Vara

Varale saate teha valiku **Ressurss**. Ressursi valik määratleb, millist kalendrit kasutatakse töökäsu planeerimisel. Ressursi valikut kasutatakse sageli põhivarade puhul. Ressursid ja ressursigrupid seadistatakse valikus **Organisatsiooni haldus** > **Ressursid** > **Ressursigrupid** või **Ressursid**.

Väljal **Põhivara number** saate valida põhivaraga seotava vara. See on oluline, kui teie vara on seotud investeerimisprojektiga.

- Kui vara on seotud põhivaraga, saate luua töökäsu tüübi, mida kasutatakse investeerimisprojektiga seotud töökäskude puhul. 
- Vara põhivarade teave on seotud rakenduse Dynamics 365 Supply Chain Management mooduliga **Põhivarad**. See tähendab, et valikust **Põhivarad** > **Põhivarad** > **Põhivarad** saate ülevaate mooduli Asset Management projektidest, mis võivad olla seotud põhivaraga, kui valite loendist vara ja vaatate sisu paani **Seotud teave**  > jaotisest **Seotud projektid**.


## <a name="details"></a>Üksikasjad

Väljal **Aktiivne alates** kuvatakse kuupäev, mil te vara töötsükli oleku aktiivsesse olekusse uuendasite (lugege varade töötsüklite oleku seadistamise teemat [Vara töötsükli olekud](../setup-for-objects/object-stages.md)). Kui vara ei ole enam aktiivne ja olete vara töötsükli oleku uuendanud passiivseks töötsükli olekuks, kuvatakse väljal **Aktiivne kuni** kuupäev, alates millest on vara passiivne. Vajadusel saate neid kuupäevi käsitsi muuta.

Vajadusel saate sisestada vara asendamise eeldatava kuupäeva väljale **Asenduse kuupäev**. Vara asendamise eeldatava väärtuse saab sisestada väljale **Asendusväärtus**. Näide: saate kasutada asendusteavet selle võrdlemiseks vara hoolduskuludega ja seejärel teha otsuse uue vara ostmiseks, kui olemasoleva vara hoolduskulud kasvavad kiiresti.

## <a name="notes"></a>Märkmed

Saate lisada varaga seotud märkusi kiirkardile **Märkmed**. Enne märkme kirjutamist klõpsake nuppu **Lisa ajatempel**, kui soovite märkmele lisada kasutaja andmed ja kuupäeva/ajatempli.

## <a name="attributes"></a>Atribuudid

Sellel kiirkardil saate seadistada vara atribuutide väärtused. Neid atribuute saab kasutada varaga seotud atribuutide või omaduste (nt suurus, kaal või seadme konfiguratsioon) kirjeldamiseks.

Klõpsake nuppu **Lisa rida** ja valige atribuudi tüüp. Järgmisena sisestage atribuudi tüübiga seotud **Väärtus** ja salvestage kirje.

>[!NOTE] 
>Ülevaate varade atribuutide tüüpidest ja nende seosest varadega valikust **Vara atribuut** ja **Vara atribuudi ülevaade**. Lisateabe saamiseks lugege artiklit [Vara atribuudi ülevaade](../objects/object-specification-overview.md).

## <a name="vendor"></a>Tarnija

Valige kiirkaardil **Hankija** vara hankijakonto. Kui on antud hankijagarantii, saate siia lisada garantiiteabe.

## <a name="address"></a>Kontaktaadress

Kiirkaardile **Aadress** saate sisestada seadme aadressi. Kui varale ei ole aadressi sisestatud, kasutab vara emaettevõtte vara aadressi, kui emaettevõtte varal on aadress. Kui vara hierarhias pole ükski aadress seotud vara või mistahes emaettevõttega, võib kasutada selle töö asukoha aadressi, kuhu vara on paigaldatud. Kui sellel töö asukohal pole sellega seotud aadressi, kasutatakse varas emaettevõtte töö asukoha aadressi.

## <a name="asset-management-plans"></a>Varahalduskavad

Hoolduskavu kasutatakse vara ennetavate hooldustööde planeerimiseks korrapäraste ajavahemike järel. Sellel kiirkaardil saate seadistada valitud vara hoolduskava read. Hoolduskordi saab seadistada erinevatele varadele, mille puhul peate tegema sarnaseid ülesandeid korrapäraste ajavahemike järel. Vahekaardil **Töö asukoha hoolduskavad** kuvatakse selle töö asukohaga seotud hoolduskavad, kuhu vara on paigaldatud.

>[!NOTE]
>Kui kustutate hoolduskava rea või hoolduskorra, mis on seotud varaga üksuses **Kõik varad**, kustutate automaatselt ka kõik hoolduskavad olekuga „Loodud”, mis loodi hoolduskava või hoolduskorraga.

## <a name="functional-location-maintenance-plans"></a>Töö asukoha hoolduskavad

Sellel vahekaardil kuvatakse selle töö asukohaga seotud hoolduskavad ülevaade, kuhu vara on paigaldatud.

## <a name="maintenance-rounds"></a>Hoolduskorrad

Sellel kiirkaardil saate lisada varaga seotud hoolduskordi või neid eemaldada.

## <a name="financial-dimensions"></a>Finantsdimensioonid

Saate valida vara finantsdimensiooni.
