---
title: Elektrooniliste arvete väljastamine teenustes Finance ja Supply Chain Management
description: Selles teemas selgitatakse, kuidas Microsofti teenustes Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmooduli kaudu elektroonilisi arveid väljastada.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 099ebb56710e920f7b1453f32f23f59a80486ebf
ms.sourcegitcommit: 105f65468b45799761c26e5d0ad9df4ff162c38d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5486949"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a>Elektrooniliste arvete väljastamine teenustes Finance ja Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Selles teemas selgitatakse, kuidas Microsofti teenustes Dynamics 365 Finance ja Dynamics 365 Supply Chain Management elektroonilise arvelduse lisandmooduli kaudu elektroonilisi arveid väljastada.


## <a name="feature-activation"></a>Funktsiooni aktiveerimine

Elektroonilise arvelduse lisandmooduli kaudu elektrooniliste arvete väljastamiseks on vaja aktiveerida teenustes Finance and Supply Chain Management funktsiooniviide.

Iga funktsiooniviide vastab konkreetsele elektroonilise arvelduse funktsioonile, mis järgib riigi/regiooni elektroonilise arvelduse nõudeid.

Järgmises tabelis on toodud elektroonilise arvelduse lisandmooduli toetatud funktsiooniviidete loend.

| Nimi                                              | Riik/regioon |
|---------------------------------------------------|----------------|
|Austria elektrooniline arve                        |Austria         |
|Belgia elektrooniline arve                         |Belgia         |
|NF-e föderaalne – Brasiilia elektrooniline arve       |Brasiilia          |
|NFS-e – Brasiilia teenuse (linna) elektrooniline arve|Brasiilia          |
|Taani elektrooniline arve                          |Taani         |
|Egiptuse elektrooniline arve                        |Egiptus           |
|Eesti elektrooniline arve                        |Eesti         |
|Soome elektrooniline arve                         |Soome         |
|Prantsuse elektrooniline arve                          |Prantsusmaa          |
|Saksa elektrooniline arve                          |Saksamaa         |
|PEPPOL – globaalne elektrooniline arve                 |Üldine          |
|Itaalia elektrooniline arve                         |Itaalia           |
|CFDI – Mehhiko elektrooniline arve                  |Mehhiko          |
|Hollandi elektrooniline arve                           |Holland     |
|Norra elektrooniline arve                       |Norra          |
|Hispaania elektrooniline arve                         |Hispaania           |

Kui on olemas elektroonilise arvelduse pärandfunktsioon, mida toetab riigi lokaliseerimise kohaldamisala, võimaldab funktsiooniviite aktiveerimine elektrooniliste arvete väljastamist elektroonilise arvelduse lisandmooduli kaudu ja lülitab pärandfunktsiooni välja.

> [!IMPORTANT]
> Kui elektroonilise arveldamise lisandmooduli integreerimise funktsioon on lubatud, lülitatakse uus elektroonilise arveldamise kogemus vaikimisi välja. Saate kasutada funktsiooni kontseptsiooni valikuliselt uute kogemuste võimaldamiseks juriidilistele isikutele, kasutades riigi-/regiooniomast funktsiooni. Suvand **Globaalne** juhib uut kogemust ülejäänud maakonna/regioonide puhul, mida tabelis konkreetselt pole loetletud.

## <a name="submit-electronic-documents"></a>Elektrooniliste dokumentide edastamine

Elektrooniliste dokumentide edastamisprotsess kajastab ühte andmevahetuspunkti teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahel. Iga edastussündmuse ajal liigub andmevahetus mõlemas suunas.

- **Teenustest Finance ja Supply Chain Management elektroonilise arvelduse lisandmoodulile** – teenused Finance ja Supply Chain Management saadavad abstraktsed arved elektroonilise arvelduse lisandmoodulile. Vastavalt vajadusele saadavad need ka nende muutujate sisu, mis konfigureeriti elektroonilise arvelduse funktsioonide osana.
- **Elektroonilise arvelduse lisandmoodulist teenustesse Finance ja Supply Chain Management** – olenevalt elektroonilise arvelduse funktsioonist saavad teenused Finance ja Supply Chain Management elektroonilise arvelduse lisandmoodulist värskendusi eelnevalt edastatud arvete töötlemistulemuste kohta. Need saavad ka nende muutujate sisu, mis konfigureeriti elektroonilise arvelduse funktsioonide osana.

Elektrooniliste dokumentide edastamiseks elektroonilise arvelduse lisandmoodulile avage teenustes Finance ja Supply Chain Management **Organisatsiooni haldus &gt; Perioodiline &gt; Elektroonilised dokumendid &gt; Edasta elektroonilised dokumendid**

Alguspunkt on sisestatud arve. See arve võib pärineda erinevatest kohtadest, nt müügitellimustest, projektiarvetest või vabas vormis arvetest.

Edastusprotsessi saab käitada käsitsi või taustal.

- **Käsitsi käivitamine** – käsitsi käivitamiseks peate kasutama suvandit **Filter**, et määratleda edastatavate dokumentide vahemik. Lehel **Filtrid** saate konfigureerida enda päringu, et valida sisestatud arved, mis tuleb edastada. Pärast valiku tegemist tuleb teil töötlemine käsitsi käivitada ja oodata, kuni see töö lõpetab. Kui töötlemine on lõpule jõudnud, kuvatakse tegevuskeskuse teates edukalt edastatud elektrooniliste dokumentide arv.
- **Taustal käivitamine** – taustal käivitamiseks ei pea te sisse logima ega edastuse dialoogiboksi avatuna hoidma. Saate ajastada protsessi käivitumise ja määrata käivitumissageduse.

## <a name="view-the-submission-logs"></a>Edastuslogide vaatamine

Teenustes Finance ja Supply Chain Management saate kasutada edastuslogisid, et vaadata elektroonilise arvelduse lisandmoodulile edastatud andmete töötlemise tulemusi. Avage **Organisatsiooni haldus &gt; Perioodiline &gt; Elektroonilised dokumendid &gt; Elektroonilise dokumendi edastus** ja seejärel valige väljal **Dokumendi tüüp** väärtus, et filtreerida logide kuvatavad arvetüübid.

Saadaval on kolm edastuse olekut.

- **Ajastatud** – elektroonilise arvelduse lisandmoodul on teenustelt Finance ja Supply Chain Management edastuse vastu võtnud ning elektroonilise arvelduse funktsiooni töötlemine on pooleli.
- **Lõpule viidud** – elektroonilise arvelduse lisandmoodul töötles elektroonilise arvelduse funktsiooni edukalt, nagu see on konfigureeritud seda käitama.
- **Nurjus** – elektroonilise arvelduse lisandmoodulil ilmnes elektroonilise arvelduse funktsiooni töötlemisel tõrge või protsessi peatas erand.

> [!IMPORTANT]
> Edastuse olek viitab elektroonilise arvelduse lisandmooduli elektroonilise arvelduse funktsiooni töötlemise olekule. See ei viita elektroonilise arve lõplikule olekule.
>
> Näiteks kui elektrooniline arve tuleb kinnitamiseks edastada välisele veebiteenusele, võib edastuse olek olla **Lõpule viidud**, kuid elektroonilise arve olek võib olla **Tagasi lükatud**. Sellisel juhul suutis elektroonilise arvelduse lisandmoodul elektroonilise arvelduse funktsiooni edukalt töödelda nii, nagu see on konfigureeritud seda funktsiooni töötlema. Elektrooniline arve lükati aga tagasi, kuna see ei vastanud arve kinnitamiseks kehtestatud veebiteenuse kriteeriumitele.

Edastuslogide hulka kuuluvad järgmised lisafunktsioonid.

- **Edastuse üksikasjad** – saate vaadata põhiedastuse üksikasju. Visualiseering näitab elektrooniliste arvelduse funktsioonis konfigureeritud tegevuste täielikku käivituslogi. Samuti võimaldab see kasutajatel töötlemise ajal loodud failid alla laadida. Olukordades, kus väline veebiteenus peab arve kinnitama, võimaldatakse kasutajatel arve olekut vaadata.
- **Seotud edastused** – saate vaadata alamedastuste üksikasju.
- **Edastuste tühistamine** – see funktsioon lubab spetsiaalse edastusprotsessi olukordades, kus väline veebiteenus peab elektroonilise arve kinnitama. See juhendab elektroonilise arvelduse lisandmoodulit saatma veebiteenusele kindla sõnumi, mis käseb veebiteenuse andmebaasis kinnitatud elektroonilise arve oleku tühistada.
- **Dokumendi taasedastamine** – saate taasedasta elektroonilise dokumendi, mis on juba elektroonilise arvelduse lisandmoodulile edastatud. Lehel **Edastuse üksikasjad** luuakse täiesti uus logi.
- **Saatke seotud edastus**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
