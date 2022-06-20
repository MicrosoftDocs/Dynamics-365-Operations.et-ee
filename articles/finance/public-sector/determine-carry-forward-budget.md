---
title: Värskenda edasisuunatud eelarvet pärast ostutellimuste ja arvete vähendamist
description: See artikkel kirjeldab, kuidas kontrollida, mis juhtub edasikaateelarvega ostutellimuste tühistamisel või alandamisel ja arvete alandamisel.
author: TaylorVH
ms.date: 02/11/2022
ms.topic: article
ms.search.form: LedgerFund
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-savanh
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2022-02-01
ms.openlocfilehash: 7f0ef0ffdf697609e811f754b4378b1f7a81c494
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897954"
---
# <a name="update-the-carry-forward-budget-after-reductions-in-purchase-orders-and-invoices"></a>Värskenda edasisuunatud eelarvet pärast ostutellimuste ja arvete vähendamist

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See artikkel kirjeldab, kuidas kontrollida, mis juhtub edasikaateelarvega ostutellimuste tühistamisel või alandamisel ja arvete alandamisel.

Lisateavet selle kohta, kuidas ostutellimusi aasta lõpus töödeldakse, vt [ostutellimuste töötlemine aasta lõpus](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end).

## <a name="turn-carry-forward-budget-reductions-for-invoice-variances-on-or-off"></a>Arvehälvete edasikaatmise eelarve vähendamise sisse- või väljalülitamine

Süsteem saab alati uuendada edasik selles eelarves, kui ostutellimus on tühistatud või vähendatud. Kui aga soovite edasikantseelarvet arve vähendamisel uuendada, peate lülitama sisse edasikantseelarve vähendamise, kui arvet ostutellimuse vastu vähendatakse *hälbefunktsiooniga*. Administraatorid saavad selle funktsiooni sisse ja välja lülitada, otsides seda Funktsioonihalduse **[tööruumis](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)**.

## <a name="purchase-order-reductions-and-cancellations"></a>Ostutellimuse vähendamised ja tühistamised

Sõltumata sellest, *kas* vähenda edasik jätkake eelarvet, kui arvet ostutellimuse vastu vähendatakse hälbe funktsiooniga, mis on sisse lülitatud, uuendatakse edasikantse eelarvet, kui kvalifitseeruv ostutellimus tühistatakse või vähendatakse. Saate seadistada igale pearaamatu fondile vastamiseks ühel järgmistest viisidest:

- Säilita edasikäägitud eelarve selle loomisel.
- Tühistatud või vähendatud summa eemaldamiseks korrigeerige automaatselt edasikaateelarvet.

Automaatseks eelarve korrigeerimiseks on saadaval ainult ostutellimuse read, mille jaotused sisaldavad fondi. Automaatne eelarve korrigeerimine toimub siis, kui ostutellimus on lõpetatud või ostutellimuse vähendamine kinnitatud.

## <a name="invoice-reductions"></a>Arvete vähendamised

*Kui* arve ostutellimusega seotud arve vähendamisel on hälbefunktsiooniga vähendatud, saate määrata, kas iga fond peaks arve vähendamisel vähendama edasikaateelarvet, lisaks ostutellimuse vähendamisele või tühistamisele. Arve peab olema ostutellimuse jaoks, mille eelarve on edasikarvestuseks. Vähendused hõlmavad hinnahälbeid, tasu hälbeid ja maksuhälbeid. Kui edasikaattud ostutellimust vähendatakse arveldamise ajal, luuakse hälve. Arve sisestamisel vähendatakse ostutellimuse pandiõiguste summat. See funktsioon loob ka automaatse eelarve korrigeerimise hälbe summa jaoks.

Kui vähendage *edasik* vormis eelarvet, kui arvet ostutellimuse vastu vähendatakse hälbefunktsiooniga, lülitatakse edasikaatmiseelarvet selles stsenaariumis vähendada. Seetõttu jääb hälbe summa järelejäänud edasikantseelarve maha.

## <a name="configure-the-carry-forward-budget-options-for-each-fund"></a>Konfigureerige igale fondile edasisuunas eelarve valikud.

Järgige neid samme iga pearaamatu fondi puhul, mis peaks saama vähendada edasikaateelarvet ostutellimuse või arve vähendamisel.

1. Minge pearaamatu **kontoplaani \> fondidele \>\>**.
1. Valige fond, mida soovite seadistada.
1. Veenduge **, et jaotises Ostutellimuse aasta lõpu** **protsess oleks valitud aasta lõpu suvandi Alistamine väärtuseks** Jah *·*.
1. Määrake **jaotises Edasikaateelarve** eelarve **, et eelarve** ennistada, kui edasik liiklev ostutellimus on vajaduse järgi tühistatud või vähendatud. Sätetel on veidi erinevad mõjud, sõltuvalt sellest, *kas* vähenda edasikaateelarvet, kui arvet ostutellimuse vastu vähendatakse, nii et hälbe funktsioon lülitatakse teie süsteemis sisse.

    - Kui funktsioon on välja lülitatud, reageerib süsteem ainult tühistatud või vähendatud ostutellimustele. Suvandi sätted töötavad järgmiselt:

        - *Ei* – süsteem loob eelarve registreerimiskande tühistatud või vähendatud ostutellimuste järelejäänud saldo kohta.
        - *Jah* – süsteem lubab ostutellimusi tühistada või vähendada, kuid ei loo eelarve registrikirjet. Edasikarbimiseelarve jääb tarbimiseks teistele dokumentidele alles.

    - Kui funktsioon on sisse lülitatud, reageerib süsteem nii arve hälvetele kui ka tühistatud või vähendatud ostutellimustele. Suvandi sätted töötavad järgmiselt:

        - *Ei* : arve hälvete puhul loob süsteem eelarve registreerimiskande ostutellimuse suhtes hälbe vähendamise summa puhul. Tühistatud või vähendatud ostutellimuste korral on sellel sättel sama mõju, kui funktsioon on välja lülitatud.
        - *Jah* – süsteem lubab arve hälvete puhul arve vähendamist, kuid ei loo eelarve registrikirjet. Edasikarbimiseelarve jääb tarbimiseks teistele dokumentidele alles. Tühistatud või vähendatud ostutellimuste korral on sellel sättel sama mõju, kui funktsioon on välja lülitatud.

## <a name="additional-resources"></a>Lisaressursid

- [Ostutellimuste töötlemine aasta lõpus](/dynamicsax-2012/appuser-itpro/process-purchase-orders-at-year-end)
- [Eelarvereservide haldamine](general-budget-reservation-tasks.md)
- [Vahendid avalikus sektoris](funds-public-sector.md)
- [Fondi häälestus avalikus sektoris](tasks/set-up-fund-public-sector.md)
