---
title: Hankija sertifikaadi säilitamine
description: See artikkel kirjeldab samme, mida hankijad saavad kasutada oma sertide säilitamiseks, kasutades hankija koostöö tööruumi.
author: v-kiarnd
ms.date: 04/27/2021
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 37990292748c363f44d306bda0263dd117808eb1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891433"
---
# <a name="maintain-vendor-certification"></a>Hankija sertifikaadi säilitamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab samme, mida teie hankijad saavad kasutada oma sertide säilitamiseks, kasutades hankija **koostöö tööruumi**. Sertifikaadid võivad olla näiteks Naise Äriettevõte (WBE) või energia- ja keskkonnakujunduse (LEED) ettevõtte juht. Hankijad peavad sisestama sertimisteabe **hankija teabe** tööruumi. Seejärel valivad hankijad suvandi **Veel üksikasju** ja seejärel valige suvand **sertifikaadid**.

## <a name="turn-on-the-vendor-certification-feature"></a>Lülita hankija sertifikaadi funktsioon sisse

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonide halduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) lehte, et kontrollida funktsiooni olekut ja vajaduse korral see lubada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul** - *Ostureskontro*
- **Funktsiooni nimi** - *Hankija koostöö sertimishalduse lubamine*

## <a name="add-a-new-certification"></a>Lisage uus sert

Uue sertifikaadi lisamiseks valige nupp **Lisa**, mis asub **sertifitseerimisruudustiku** kohal **hankija teabe tööruumis**. Sisestage järgmine teave:

- Serdi number
- Serdi tüüp
- Sertifitseerimisorganisatsioon
- Serdi kuupäev
- Võlgnetav summa, kui see on olemas
- Jõustumiskuupäev
- Aegumiskuupäev
- Kommentaarid, valikuline

Kui konkreetse sertifikaadiga on seotud dokumente, saate need siduda nuppu **Dokument** klõpsates.

Sertifikaatidele, mille teie hankijad sellele lehele sisestavad, määratakse allikaks "Hankija". Saate hankija pangakontode all sisestada sertifikaaditeabe oma hankija eest. Teavet kuvatakse siin ja allikat kuvatakse **kliendina**.

Hankijad saavad vajadusel oma sertifikaate redigeerida või kustutada.

## <a name="vendor-collaboration-generated-certification-records"></a>Hankija koostöös loodud sertimiskirjed

Kui hankija on sertimisteabe lisanud, on teave nähtav **Hankijaga koostöös loodud sertifikaadid** lehel. Lehe avamiseks klõpsake käske **Ostureskontro > Päringud > Hankija aruanded > Hankija koostöö loodud sertifikaadid**. Vaikimisi on kõik uued või muudetud sertimiskirjed nähtavad. Ostureskontro ametnik saab muudatusi vaadata ja valideerida teavet kinnitusprotsessi kaudu. Kui teave on kinnitatud, saab leheküljel loetletud sertifikaadi kirje valida ja märkida ülevaadatud kirjeks. Kirje ülevaadatuna märkimine eemaldab selle vaikeloendist.

Kõik sertifikaadi muudatused kuvatakse **Hankija koostöö loodud sertifikaadid** lehel. Kui lehel muudatust ei kuvata, saate seda vaadata, kohandades hankija konto filtreid, kehtivuse lõppkuupäeva vahemikku või valides, kas kaasata teave läbivaadatud sertifitseerimismuudatuste kohta.

