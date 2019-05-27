---
title: Pakkumiste halduse seadistamine
description: Selles teemas kirjeldatakse, kuidas rakenduses Talent pakkumisi seadistada.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fa0e5d30c06db16e105631e492af022acfcfd66
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517795"
---
# <a name="set-up-offer-management"></a>Pakkumiste halduse seadistamine 

[!include [banner](includes/banner.md)]

Kui kandidaat viiakse rakenduses Dynamics 365 for Talent: Attract pakkumise etappi, peate tagama, et pakkumisi saab kandidaadi jaoks kiiresti luua, vajadusel kinnitada ja kandidaadile saata. Kuna enamik pakkumisi on standardsed, saab neid luua korduvkasutatavate mallidega. Rakenduses Attract on kõik pakkumised koos pakkumise paketis, mis on ühest või enama pakkumisdokumendiga kogum. 

Selles teemas loetletakse kõik etapid, mida Attracti administraator peab järgima, et seadistada erinevad pakkumise paketi mallid osana Attracti pakkumiste haldamise võimalusest. Administraatori rollita kasutajatel puudub juurdepääs nendele võimalustele.

>[!NOTE]
> Pakkumise haldamise võimalused on saadaval osana tervikliku värbamise lisandmoodulist.

## <a name="offer-data"></a>Pakkumisandmed 

Pakkumisandmed on pakkumise paketi malli väikseim üksus. Tavaline pakkumine koosneb standardsest tekstist ja väärtuste komplektist. Väärtuste komplektid on ainsad asjad, mis võivad pakkumiste vahel muutuda. Pakkumise loomise ajal on kõige olulisem aspekt, millele pakkumise looja saab keskenduda, pakkumise paketi mallis olev pakkumisandmete kohatäidete loend. Pakkumisandmete seadistamiseks tehke järgmist.

1.  Valige **Pakkumise haldamine**

1.  Laiendage jaotist **Teek** vasakul navigeerimispaanil, seejärel avage **Pakkumisandmed**.

    >[!NOTE]
    > **Pakkumisandmete** lehel on **Kandidaadi andmete** ja **Töö üksikasjade** jaotised. Attract pakub ka mõned nö. kastist väljaspool pakkumisandmete kohatäited.
    
    > Lehel on jaotised erinevate pakkumisandmete kohatäidete korraldamiseks loogilistesse gruppidesse. Need jaotised aitavad pakkumise loomise protsessis säilitada pakkumisandmeid ja andmeid asustada.

1.  Uue pakkumisandmete jaotise loomiseks klõpsake **Jaotise lisamine** ja sisestage jaotisele kordumatu nimi.

1.  Mis tahes jaotisele pakkumisandmete kohatäite lisamiseks klõpsake **Pakkumisandmete lisamine** ja sisestage kohatäitele kordumatu nimi.

1.  Jaotise nime muutmiseks liikuge hiirega üle jaotise nime ja värskendage seda.

1.  Mis tahes olemasoleva pakkumisandmete kohatäite nime muutmiseks veenduge kõigepealt, et kohatäide ei ole juba osa mõnest mallist. Seejärel liikuge hiirega üle pakkumisandmete kohatäite nime ja värskendage seda vajadusel.

1. Mis tahes olemasoleva pakkumisandmete kohatäite kustutamiseks veenduge kõigepealt, et kohatäide ei ole osa mõnest teisest mallist. Seejärel liikuga hiirega üle kohatäite ja prügikastiikooni kuvamisel klõpsake pakkumisandmete kohatäite kustutamiseks prügikastiikoonil.
    >[!NOTE]
    > Saate iga pakkumisandme kõrval oleva numbri järgi vaadata, mitme malli osa pakkumisandmete kohatäide on. 

1. Mis tahes jaotise kustutamiseks liikuge hiirega üle selle nime. Kui ükski jaotises olevatest pakkumisandmete kohatäidetest ei ole üheski mallis, saate kustutamiseks klõpsata prügikastiikoonil. 
    >[!NOTE]
    > Jaotise kustutamine kustutab ka kõik jaotises olevad pakkumisandmete kohatäited.

Kui pakkumisandmete kohatäited on seadistatud, saate neid kasutada igal dokumendimallil. Pakkumisandmete kohatäited ei ole piiratud kindla malliga – sama komplekti saab kasutada kõikides mallides.

## <a name="offer-data-rules"></a>Pakkumisandmete reeglid

Enamikel organisatsioonidel on pakkumiste loomise reeglid. Näiteks võib organisatsioon nõuda, et konkreetse asukoha ja staažitaseme kombinatsiooni maksimaalne aastapalga pakkumine peab olema teatud vahemikus või et uue töötaja pakkumistasemele saab lisada vaid mõned konkreetsed väärtused. Rakendus Attract toetab praegu kõiki selliseid andmereegleid CSV-failiga.

Andmereeglite CSV-faili loomiseks tehke järgmist.

1.  Määratlege määratud reegli pakkumisandmete kohatäide. Näiteks **Aastapalk**.

1.  Tuvastage sõltuvad pakkumisandmete kohatäite väärtused. Näiteks **Töö asukoht** ja **Tase**.

1.  Määrake veerud 1 ja 2 kui **Töö asukoht** ja **Tase**.

1.  Vahemiku väärtuse üleslaadimiseks tehke veergudest 3 ja 4 **Aastapalk**. Vahemiku asemel mõne kindla väärtuse üleslaadimiseks tehke vaid veerust 3 **Aastapalk**.

1.  Asustage nõutavate rollide põhjal Microsoft Exceli fail.

1.  Tagage, et iga rida on kõigi kokkupandud väärtuste kordumatu kombinatsioon.

1.  Salvestage fail CSV vormingus.

Pakkumisandmete reeglite faili üleslaadimiseks tehke järgmist.

1.  Valige **Pakkumise haldamine**

1.  Laiendage jaotist **Teek** vasakul navigeerimispaanil, seejärel avage **Pakkumisandmete reeglid**.

1.  Klõpsake **Uus andmekogum**, et kuvada **Üleslaadimise** dialoogiboks.

1.  Määrake reeglistikule kordumatu nimi ja seejärel laadige salvestatud CSV-fail üles.

1.  Klõpsake vahekaarti **Lisa**.
    Reeglistiku töödeldakse taustal ning teid teavitatakse rakenduses ja e-posti teel, kui see on lõpule jõudnud.

    Teid teavitatakse, kui üleslaadimise töötlemisel ilmneb tõrkeid. Seejärel saate alla laadida tõrkelogi, faili ära parandada ja uuesti üles laadida.

1.  Kasutage kolmikpunkti nupu (**...**) suvandit, kui soovite reeglistiku alla laadida ja väärtuste kogumit värskendada. Pärast värskendamist saate faili uuesti üles laadida.

1.  Saate olemasoleva üleslaetud reeglistiku kustutada, kui määratletud kohatäidet ei kasutata teistes dokumendimallides.

>[!NOTE]
> - Igal kohatäitel saab olla vaid üks kordumatu veergude komplekt, millest see sõltub. Näiteks kui **Aastapalk** sõltub **Töö asukohast** ja **Tasemest**, ei saa üles laadida teist reeglistikku, kus **Aastapalk** sõltub teistsugustest veergudest.

> - Saate **Näidiste** vahekaardilt **Pakkumisandmete reeglite** lehel alla laadida pakkumisandmete reeglistiku näidised.

> - Kui pakkumise looja asendab pakkumisandmete reeglite soovitatud väärtused, märgistatakse pakkumine ebastandardseks ja volitatakse pakkumise kinnitamise töövoog.

## <a name="document-templates"></a>Dokumendimallid

Pakkumise dokumendimall aitab administraatoritel pakkumiskirju koostada. Pakkumise dokumendimall on nii pakkumise osaks oleva teksti kui ka määratud pakkumisandmete kohatäidete kombinatsioon. 

Pakkumise dokumendimalli loomiseks tehke järgmist.

1.  Valige **Pakkumise haldamine**

1.  Laiendage jaotist **Teek** vasakul navigeerimispaanil ja seejärel avage **Mallid**.

    **Mallide** lehekülg kuvab loendi juba määratletud dokumendimallidest.

1.  Uue dokumendimalli loomiseks klõpsake **Uus mall**.

1.  Sisestage malli jaoks kordumatu nimi ja klõpsake **Loo**.

1.  Pakkumise dokumendi sisu lisamiseks või redigeerimiseks kasutage RTF-redaktorit. Saate tekstiredaktori ülaosas olevate suvanditega lisada tabeleid, pilte ja hüperlinke.

1.  Saate pakkumise dokumendimalli pakkumisandmete kohatäiteid sisestada järgmiselt.

    - Pukseerides parempoolselt paanilt.

    - Lisades pakkumisandmete kohatäite otse selle kohale. Sisestades **\#** ja hakates seejärel sisestama pakkumisandmete kohatäite nime. Valikud ilmuvad rippmenüü loendis. Pakkumisandmete kohatäite sisestamiseks klõpsake või vajutage **Sisestamine**.

    >[!NOTE]
    > - Kohatäite seostamiseks pakkumise dokumendimalliga, selle väärtust kandidaadile avaldamata, liikuge hiirega üle pakkumisandmete kohatäite ja klõpsake ikooni **Kinnita**. See lükkab kohatäite pakkumise dokumendimalli **Kinnitatud pakkumisandmete** jaotisesse. Eemaldamiseks järgige samu juhiseid, kuid klõpsake pakkumisandmete kohatäidete loendis **Eemalda**.

    > - Aktiivsete pakkumisandmete kohatäidete kuvamiseks minge paempoolse paani vahekaardile **Aktiivne**.

    > - Lisades kohatäitja, mida juhib pakkumisandmete reeglistik, näete selle pakkumisandmete kohatäite sõltumist teistes väärtustes.

    > - Teise võimalusena saate **Importida** sisu .docx failist oma arvutisse ja vastavalt vajadusele redigeerida. Nii ei ole teil vaja redaktoris kogu sisu trükkida.

1. Pakkumise dokumendi eelvaate kuvamiseks kasutage **Eelvaate** suvandit lehe ülaosas.

1. Määramaks, kas pakkumise looja saab pakkumise dokumendi sisu redigeerida, kasutage lehe ülaosas olevat suvandit **Loa haldamine**. Kui soovite, et pakkumise looja saaks sisestada vaid kohatäite väärtuseid, kuid mitte redigeerida teksti, määrake loa väärtuseks **Ei**.

1. Progressi salvestamiseks klõpsake **Salvesta**. Mall salvestatakse mustandi olekus.

1. Lõpetamiseks ja dokumendi avaldatuks märkimiseks klõpsake **Lõpeta**.

1. Saate dokumendimallide teegist vaadata, missugused dokumendimallid on aktiveeritud, mustandirežiimis ning missugused on arhiveeritud ja ei ole enam kasutuses.

>[!NOTE]
> Saate kustutada mis tahes pakkumise dokumendimalli, mis ei ole osa olemasolevast pakkumise paketi mallist.


## <a name="offer-package-templates"></a>Pakkumise paketi mallid

Pakkumise paketid pakkumise artefaktid, mida kandidaatidega jagatakse ning need koosnevad ühe või enama pakkumise dokumendimalli kombinatsioonist. Pakkumise paketi loomiseks tehke järgmist.

1.  Valige **Pakkumise haldamine**

1.  Valige vasakult navigeerimispaneelilt **Paketid**.

    Kuvatakse loend pakkumise loojatele saadaolevatest aktiivsetest paketimallidest.

1.  Uue pakkumise paketi loomiseks klõpsake **Uus pakett**.

1.  Sisestage kordumatu nimi ja klõpsake **Loo**.

1.  Klõpsake **Lisa mall**.

    >[!NOTE]
    > - Võite luua uue malli või valida olemasolevate seast.

    > - Kui soovite lisada olemasoleva malli, peate veenduma, et pakkumise dokumendimall salvestati, lõpetati ja selle olek märgiti aktiivseks.
    
    > - Saate valida nii palju dokumendimalle kui soovite. 
    
1.  Klõpsake **Valmis**, et naasta **Pakettide haldamisse**.

    Saate konfigureerida dokumentide järjestuse ja märkida, kas konkreetne pakkumise dokument on pakkumise loomisel vajalik. Pakkumise loojal on võimalus kustutada dokumendid, mis on märgistatud kui **Pole nõutav**.

1. Pakkumise paketimalli salvestamiseks nii, et seda saaksid kasutada kõik pakkumise loojad, klõpsake **Salvesta ja avalda**.

   Pakkumise paketimallide mustandite vaatamiseks minge vahekaardile **Mustandid**. Kui pakkumise paketimalli muudetakse, tuleb see uuesti salvestada ja avaldada.

## <a name="configure-an-offer-process"></a>Pakkumisprotsessi konfigureerimine

Rakenduse Attract administraator saab konfigureerida mitut pakkumise loomise protsessi osa.

- **Pakkumise kinnitamised** – valige, kas pakkumise kinnitamised on enne pakkumise kliendile saatmist nõutud. Adminstraatorina saate otsustada ka seda, kas kõik pakkumise kinnitamised toimuvad järjestikkusel viisil või paralleelse kinnitamise töövooga. Samuti saate määrata, kas pakkumise kinnitajatel tuleb kinnitusele lisada kommentaar. Pakkumise kinnitamised on kohustuslikud kõigile ebastandardsetele pakkumistele.

- **Kandidaadi pakkumise kogemus** – administraatorina saate valida, kas määrata kõigile pakkumistele aegumiskuupäev ja kui, siis milline peaks olema aegumiskuupäeva vaikevastasus. Saate konfigureerida ka selle, kas kandidaat saab pakkumisest keelduda.

- **Elektronallkirjad** -administraatorina saate määrata ka meetodi, mille abil kandidaatid saavad pakkumistele allkirju anda.
    - Adobe Sign - kõik pakkumispaketid saadetakse ja allkirjastatakse rakenduse Adobe Sign abil. Iga pakkumise looja, kes pakkumise avaldab, peab ühendama oma Adobe Sign’i konto rakendusega Attract. Adobe Signi litsentside ja tasuta prooviperioodi puhul külastage seda [linki](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

    - DocuSign – kõik pakkumispaketid saadetakse ja allkirjastatakse rakenduse DocuSign abil. Iga pakkumise looja, kes pakkumise avaldab, peab ühendama oma DocuSigni konto rakendusega Attract. 
    
    - ESign – see on valmiskujul esitatud vaikesäte, kus kasutaja saab oma nime ja initsiaalide sisestamisega pakkumise allkirjastada.


Pakkumise loomise protsessi kohta lisateabe saamiseks vt [Loomine, kinnitamine ja pakkumiste allkirjastamine](./creating-offers.md).
