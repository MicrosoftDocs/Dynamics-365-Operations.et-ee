---
title: Kategooriataotlused hankijatelt
description: Selles teemas kirjeldatakse, kuidas hankijad saavad taotleda hankekategooriaid oma konto jaoks. Siin kirjeldatakse ka hankeagentide täidetud kinnitusprotsessi.
author: Henrikan
ms.date: 04/19/2021
ms.topic: article
ms.search.form: VendRequestNewCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5d06f05ca27ed8fe58a9a24fcde8c0082662b866
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103091"
---
# <a name="category-requests-from-vendors"></a>Kategooriataotlused hankijatelt

[!include [banner](../includes/banner.md)]

Kategooria nõudeprotsess lubab hankijatel taotleda uute hankekategooriate seostamist nende kontoga. Neid hankekategooriaid saab seejärel kasutada seotud hankeprotsessides. (Lisateavet vt teemast [Tootekataloogide ülevaade](procurement-catalogs.md).)

Kategooriataotlused algatavad hankijad **hankija teabe** tööruumis. Seejärel esitatakse need teie agentuurile ülevaatamiseks ja kinnitamiseks. Kinnitatud kategooriad lisatakse hankija konto hankekategooriate loendisse.

## <a name="turn-the-category-requests-from-vendors-feature-on-or-off"></a>Lülita kategooriataotlused hankijate funktsioonist sisse või välja

Tarneahela halduse versiooni 10.0.25 puhul lülitatakse see funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, *otsides hankekategooriate hankekategooriaid hankija koostöö funktsiooni kaudu Funktsioonihalduse* tööruumis [...](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Kui see funktsioon on sisse lülitatud, saate hankekategooriaid hankija kontodele käsitsi lisada. Lisateabe saamiseks vt jaotist [Kindlatele hankekategooriatele hankijate kinnitamine](tasks/approve-vendors-specific-procurement-categories.md).

## <a name="vendor-collaboration-requirements"></a>Hankija koostöö nõuded

Enne kui hankija saab kategooriataotlustega suhelda, tuleb seda seadistada hankija koostöö funktsionaalsuse tarbeks.

Hankijal peab olema vähemalt üks hankija koostöö rakenduse kasutaja. Kategooriataotlusi saavad luua ja esitada ainult teenusepakkujate kasutajad, kellel on turberoll *hankija kasutajad (väline)*.

Lisateavet vaadake teemast [„Hankija koostöö seadistamine ja haldamine”](set-up-maintain-vendor-collaboration.md).

## <a name="set-up-the-vendor-category-request-workflow"></a>Hankija kategooria taotluse töövoo seadistamine

*Hankija kategooria taotluse* töövoog peab olema häälestatud hanketöövoogudes. Hankijad esitavad uued kategooriataotlused, mille saate üle vaadata ja kinnitada. Taotletud hankekategooriad lisatakse hankija kontole pärast kategooriataotluse heaks kiitmist.

Järgmine näide näitab, kuidas seadistada lihtsat *Hankija kategooria taotluse* töövoogu, milles on üks kinnitaja. Peate läbi vaatama oma sisemised protsessid, määramaks oma asutuse jaoks sobiv töövoo seadistus.

1. Valige seaded **Hanked \>, Seadistus, \> Hangete töövood**.
1. Valige toimingupaanil nupp **Uus**.
1. Valige dialoogiboksis **Hankija kategooria taotluse töövoog**, et avada töövoo redaktor.
1. Logige töövooredaktorisse sisse.
1. Toimingupaanil valige **Atribuudid**.
1. Sisestage **töövoo atribuutide lehel** väljale **Edastusjuhised** juhise tekst. Juhised on kategooriataotluse edastamisel hankijatele nähtavad.
1. Sulgege leht **Atribuudid**.
1. Lohistage **uue kategooriataotluse kinnitamise** töövoo element lõuendile.
1. Lohistage link töövoo **elemendist Alusta töövoogu** **Uue kategooriataotluse töövoo** elemendile.
1. Lohistage link töövooelemendist **Kinnita uus kategooriataotlus** töövooelementi **Töövooelemendi lõpetamine**.
1. Tehke topeltkoputus (või topeltklõpsake) töövooelemendile **taotluse töövoo kinnitamine**.
1. Valige ja hoidke all (või paremklõpsake) töövooelemendile **1. etapp** ja seejärel valige suvand **Atribuudid**.
1. Sisestage **töövoo atribuutide lehel** väljale **Tööelemendi subjekt** juhise tekst. See tekst kuvatakse teile määratud **Subjektiväljal** **Mulle määratud tööüksuste** lehel väärtusena.
1. Väljale **Tööüksuse juhised** sisestage juhise tekst. Juhised on kinnitajatele nähtavad, kui nad valivad kategooriataotluse tegevuspaanil **Töövoo** suvandi.
1. Vasakul paanil klõpsake nuppu **Määramine**.
1. Seadke vahekaardil **Määramistüüp** suvand **Töövooelemendile kasutajate määramine** väärtusele *Kasutaja*.
1. Valige **Kasutaja** vahekaardil loendist **Saadaval kasutajad** kinnitaja. Näiteks valige kasutaja hankeosakonnast.
1. Valige paremnoole nupp (**\>**) et liigutada kinnitaja **Valitud kasutajate** loendisse.
1. Sulgege leht **Atribuudid**.
1. Valige **Salvesta ja sule**.
1. Sisestage väljale **Versioonimärkmed** märkused töövoo kohta.
1. Valige töövoo salvestamiseks **OK**.
1. Kui olete valmis töövoogu testima, valige suvand **Aktiveeri uus versioon**. Muul juhul valige suvand **Ära aktiveeri uut versiooni**.
1. Töövoo lõpule viimiseks valige **OK**.

> [!TIP]
> Kui teie asutus ei nõua kategooriataotluste kinnitamist, peaksite töövoo konfigureerima automaatseks kinnitamiseks.

Lisateavet töövoogude häälestamise kohta vt teemast [Töövoosüsteemi ülevaade](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).

## <a name="create-and-submit-a-category-request"></a>Kategooriataotluse loomine ja esitamine

See jaotis kirjeldab, kuidas hankijad saavad kasutada **hankija teabe tööruumi** kategooriataotluste loomiseks, redigeerimiseks, vaatamiseks ja esitamiseks.

### <a name="start-a-new-request"></a>Uue taotluse alustamine

Uue kategooriataotluse käivitamiseks järgige neid samme.

1. Valige **hankija teabe** tööruumis **kategooriataotluste** paan.
1. Valige **kategooriataotluste** lehel tegevuspaanil **uue kategooriataotluse suvand**.
1. Leidke dialoogiboksis **Uus kategooria** kategooria, mille soovite rakendada, kui kasutate navigeerimiseks puud ja/või loendi ülaosas asuvat filtrit. Märkige ruut iga vastava kategooria puhul.

    Pidage meeles järgmiseid punkte.

    - Kategooriad, mis on teie hankija kontol praegu aktiivsed, kuvatakse valituna nii, et neid ei saa eemaldada.
    - Saate ühes kategooria taotluses taotleda mitut hankekategooriat.

1. Valige päringumustandi loomiseks **OK**.

    Uus mustanditaotlus kuvatakse nüüd **kategooria taotluste** lehel.

1. Avage uus mustanditaotlus selle läbivaatamiseks ja redigeerimiseks vastavalt vajadusele.

    - Praegu taotluses kaasatud kategooriate loendi vaatamiseks valige kiirkaart **Taotletud kategooriad**.
    - Oma aktiivsete kategooriate vaatamiseks avage lehe paremal küljel **aktiivsete kategooriate** factbox.
    - Kategooria lisamiseks taotlusele valige suvand **lisa** tööriistaribal, mis paikneb kiirkaardil **Taotletud kategooriad**.
    - Kategooria eemaldamiseks taotlusest valige kategooria kiirkaardil **Taotletud kategooriad** ja valige tööriistaribal käsk **Eemalda**.
    - Taotlusele dokumendi lisamiseks valige **tegevuspaanil** manused. Manustatud dokumendid on kinnitajatele saadaval, kui nad kategooriataotluse üle vaatavad.
    - Taotlusele lisatud dokumendi eemaldamiseks valige **tegevuspaanil** manused. Valige eemaldatav dokument ja seejärel valige tegevuspaanil käsk **Kustuta**.

1. Kui olete taotluse esitamiseks valmis, valige käsk **Edasta** tegevuspaanil. Vastasel juhul sulgege leht ja jätke vahele selle protseduuri ülejäänud etapid. Seejärel saate hiljem taotluse juurde tagasi pöörduda.
1. Lugege kõiki kuvatavaid edastusjuhiseid ja valige käsk **Esita**.
1. Sisestage vajalik lisateave kasti **Kommentaar**. Päringu lõpule viimiseks valige **Esita**.

### <a name="edit-a-draft-or-recalled-request"></a>Mustandi või tagasikutsutud taotluse redigeerimine

Mustandi või tagasikutsutud kategooria taotluse redigeerimiseks järgige neid samme.

1. Valige **hankija teabe** tööruumis **kategooriataotluste** paan.
1. Valige selle avamiseks mustand või tagasikutsutud taotlus.
1. Redigeerige taotlust vastavalt vajadusele ja seejärel kas sulgege see või esitage see eelmises protseduuris kirjeldatud viisil.

### <a name="submit-a-draft-or-recalled-request"></a>Mustandi või tagasikutsutud taotluse esitamine

Mustandi või tagasikutsutud kategooria taotluse esitamiseks järgige neid samme.

1. Valige **hankija teabe** tööruumis **kategooriataotluste** paan.
1. Valige mustand või tagasikutsutud taotlus, mille soovite edastada.
1. Valige toimingupaanil käsk **Esita**.
1. Lugege kõiki kuvatavaid edastusjuhiseid ja valige käsk **Esita**.
1. Sisestage vajalik lisateave kasti **Kommentaar**. Päringu lõpule viimiseks valige **Esita**.

    Kategooriataotluse olek muudetakse ühele järgmistest väärtustest:

    - _Ülevaatamise ootel_ – taotlus on töövoos.
    - _Kinnitamine on pooleli_ – kinnitus on nõutav.

### <a name="recall-a-submitted-request-that-hasnt-yet-been-approved"></a>Veel kinnitamata esitatud taotluse tagasikutsumine

Esitatud, kuid veel kinnitamata kategooriataotluse tagasikutsumiseks järgige neid samme.

1. Valige **hankija teabe** tööruumis **kategooriataotluste** paan.
1. Valige ootel taotlus, mille soovite tagasi kutsuda.
1. Toimingupaanil valige käsk **Tagasi kutsumine**.
1. Sisestage vajalik lisateave kasti **Sisesta kommentaar**. Päringu lõpule viimiseks valige **Esita**.

    Kategooriapäringu olek muudetakse olekuks _Lõpetatud_. Taotlus jääb sellesse olekusse seni, kuni selle kustutate või uuesti esitate.

### <a name="delete-a-draft-or-recalled-request"></a>Mustandi või tagasikutsutud taotluse kustutamine

Mustandi või tagasikutsutud kategooria taotluse kustutamiseks järgige neid samme.

1. Valige **hankija teabe** tööruumis **kategooriataotluste** paan.
1. Valige mustand või tagasikutsutud taotlus, mille soovite kustutada.
1. Valige tegumiribal suvand **Kustuta**.
1. Toimingu kinnitamiseks valige **Jah**.

### <a name="view-completed-requests"></a>Lõpuleviidud taotluste kuvamine

Lõpuleviidud taotluste vaatamiseks avage **hankijateabe** tööruum ja valige **kategooriataotluste** paan. Lõpule viidud kategooriataotlustel on üks järgmistest olekutest:

- _Kinnitatud_ – taotluse on kinnitatud. Uute lisatud kategooriate vaatamiseks minge tagasi **hankija teabe tööruumi**, avage vasakpaanil ripploend **Veel üksikasju** ja valige seejärel **kategooriad**.
- _Tagasi lükatud_ – taotlus lükati tagasi. Saate vajadusel luua uue kategooriataotluse.

## <a name="review-category-requests"></a>Kategooriataotluste ülevaade

See jaotis selgitab, kuidas hankijate esitatud kategooriataotlusi kinnitada, tagasi lükata ja delegeerida ning kuidas vaadata lõpetatud taotlusi. Need töövoo tegevused kehtivad kogu kategooria taotlusele.

### <a name="view-category-requests"></a>Kategooriataotluste kuvamine

Kategooriataotluste kuvamiseks järgige neid samme.

1. Valige **Hange ja hankijad \> Hankijad \> Hankijate koostööpäringud \> Kategooriataotlused**.

    Kuvatakse **kategooriataotluste** leht. Vaikimisi lehevaade näitab kategooriataotlusi, mille olekuks on *Tegevuse ootel*.

1. Kõigi taotluste vaatamiseks valige väljal *Kuva taotlused* suvand **Kõik**.
1. Avage taotlus selle läbivaatamiseks ja redigeerimiseks vastavalt vajadusele.

    - Praegu taotluses kaasatud kategooriate loendi vaatamiseks valige kiirkaart **Taotletud kategooriad**.
    - Aktiivsete kategooriate vaatamiseks avage lehe paremal küljel **aktiivsete kategooriate** factbox.
    - Dokumentide esitamise korral näitab tegevuspaani nupp **Manused** (paberklipp) lisatud dokumentide arvu. Seotud dokumentide vaatamiseks valige nupp **Manused**. Seejärel valige vaatamiseks dokument ja valige selle vaatamiseks suvand **Ava**.
    - Taotlusele dokumendi lisamiseks valige **tegevuspaanil** manused. Manustatud dokumendid on kinnitajatele saadaval, kui nad kategooriataotluse üle vaatavad.
    - Taotlusele lisatud dokumendi eemaldamiseks valige **tegevuspaanil** manused. Valige eemaldatav dokument ja seejärel valige tegevuspaanil käsk **Kustuta**.
    - Valige toimingupaanil **Töövoog** töövoo ajaloo kuvamiseks. Valige töövoo valikutes suvand **Veel** ja seejärel suvand **Töövoo ajalugu**. Kuvatakse **töövoo ajaloo** leht.

### <a name="approve-a-pending-category-request"></a>Ootel kategooriataotluse kinnitamine

Ootel ootel kategooriataotluse kinnitamiseks järgige neid samme.

1. Valige **Hange ja hankijad \> Hankijad \> Hankijate koostööpäringud \> Kategooriataotlused**.
1. Valige ootel taotlus kinnitamiseks.
1. Kategooriataotluste ülevaatamine.
1. Valikuline: valige kiirkaardil **Üldine**, väljal **Põhjuse kood** sobiv põhjuse kood. Seejärel sisestage põhjusekoodi kohta kommentaar väljale **Põhjuse kommentaar**.
1. Valige tegevuste paanil käsk **Töövoog**.
1. Valige töövoo valikutes **Kinnita**.
1. Sisestage vajalik lisateave väljale **Kommentaar**. Päringu lõpule viimiseks valige **Kinnita**.

    Kategooriataotluse olek muudetakse olekuks _Kinnitatud_ ja hankekategooriad lisatakse hankija kontole.

### <a name="reject-a-pending-category-request"></a>Ootel kategooriataotluse tagasi lükkamine

Ootel ootel kategooriataotluse tagasi lükkamiseks järgige neid samme.

1. Valige **Hange ja hankijad \> Hankijad \> Hankijate koostööpäringud \> Kategooriataotlused**.
1. Valige ootel taotlus tagasi lükkamiseks.
1. Kategooriataotluste ülevaatamine.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Valige kiirkaardil **Üldine**, väljal **Põhjuse kood** sobiv põhjuse kood. Seejärel sisestage põhjusekoodi kohta kommentaar väljale **Põhjuse kommentaar**.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige tegevuste paanil käsk **Töövoog**.
1. Valige töövoo valikutes suvand **Veel** ja seejärel suvand **Lükka tagasi**.
1. Sisestage vajalik lisateave väljale **Kommentaar**. Päringu lõpule viimiseks valige **Lükka tagasi**.

    Kategooriapäringu olek muudetakse olekuks _Tagasi lükatud_. Sel juhul saab hankija vastavalt vajadusele luua uue kategooriataotluse.

### <a name="delegate-a-pending-category-request"></a>Ootel kategooriataotluse delegeerimine

Ootel kategooriataotluse delegeerimiseks teisele kasutajale järgige neid samme.

1. Valige **Hange ja hankijad \> Hankijad \> Hankijate koostööpäringud \> Kategooriataotlused**.
1. Valige ootel taotlus, mille soovite kinnitada.
1. Valige tegevuste paanil käsk **Töövoog**.
1. Valige töövoo valikutes suvand **Veel** ja seejärel suvand **Delegeeri**.
1. Valige **väljal Kasutaja** kasutaja, et määrata ülevaatamiseks kategooriataotlus.
1. Sisestage vajalik lisateave väljale **Kommentaar**.
1. Delegeerimise lõpule viimiseks valige **Delegeeri**. Valitud kasutaja saab nüüd kategooriataotluse üle vaadata.

### <a name="view-procurement-categories-for-a-vendor"></a>Hankija hankekategooriate kuvamine

Selleks, et kuvada hankija hankekategooriaid pärast kategooriapäringu heakskiitmist, tehke järgmist.

1. Avage **Hanked \> Hankijad \> Kõik hankijad**.
1. Valige lehel **Kõik hankijad** hankija, kelle hankekategooriaid soovite vaadata.
1. Valige toimingupaanil vahekaart **Üldine** ning valige rühmas **Seadistamine** suvand **Kategooriad**.

    Kuvatakse leht **Kategooriad**. **Hanke** kiirkaart näitab hankekategooriaid, mis lisati kategooriataotluse kaudu.

1. Vajadusel saate **hanke** kiirkaardil muudatusi teha. Näiteks saate seada **hankija kategooria oleku** välja väärtusele _Eelistatud_.
