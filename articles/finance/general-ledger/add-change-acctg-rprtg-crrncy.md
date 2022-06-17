---
title: Arvestus- või aruandlusvaluuta muutmine
description: Selles artiklis selgitatakse, kuidas muuta arvestus- või aruandlusvaluutat või lisada aruandlusvaluuta pearaamatu seadistusse.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b02432c8e0bdf52c2a588f67a581b78e682b1bf8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904610"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Arvestus- või aruandlusvaluuta muutmine

[!include [banner](../includes/banner.md)]

Selles artiklis selgitatakse, kuidas muuta arvestus- või aruandlusvaluutat või lisada aruandlusvaluuta pearaamatu seadistusse.

## <a name="symptom"></a>Sümptom

Te soovite muuta arvestus- või aruandlusvaluutat või lisada aruandlusvaluuta pearaamatu häälestusse. See toimub tavaliselt järgmiste stsenaariumide korral.

- Juriidilise isiku seadistamisel määrati vale arvestus- või aruandlusvaluuta. Te soovite nüüd seda valuutat muuta.
- Juriidilise isiku seadistamisel määrati aruandlusvaluuta, kuid organisatsioon soovib nüüd aruandlusvaluuta eemaldada.
- Organisatsioon täiendab või migreerib rakendusele Microsoft Dynamics 365 Finance ja soovib muuta arvestus- või aruandlusvaluutat.

Organisatsioon, kes varem ei kasutanud topeltvaluuta võimalust, soovib seda kasutama hakata. See probleem ilmneb tavaliselt järgmiste stsenaariumide korral.

- Juriidilise isiku seadistamisel ei määratud aruandlusvaluutat. (Aruandlusvaluuta on valikuline.) Te soovite nüüd lisada aruandlusvaluuta.

## <a name="resolution"></a>Lahendus

Kõige olulisem kaalutlus on see, kas pearaamatu seadistamiseks on juriidilises isikus sisestatud kandeid (tegelikke või eelarvelisi). **Kui juriidilises isikus on sisestatud kandeid (tegelikke või eelarvelisi), ei saa arvestus- või aruandlusvaluutat muuta.** Sõltuvalt sellest, kas kanded on sisestatud, tehke ühes järgmistest jaotisest esitatud etapid.

### <a name="no-transactions-have-been-posted"></a>Ühtki kannet pole sisestatud

1. Avage juriidilises isikus, kelle jaoks valuutasid uuendate, **Pearaamat \> Pearaamatu seadistus \> Pearaamat**.
2. Valige lehel **Pearaamat** käsk **Redigeeri**.
3. Valige kiirkaardil **Valuuta** juriidilise isiku puhul kasutatav arvestusvaluuta ja aruandlusvaluuta.
4. Valige käsk **Salvesta**.

Kui lehel **Pearaamat** pole arvestusvaluuta ja aruandlusvaluuta väljad saadaval, on juriidilises isikus sisestatud vähemalt üks kanne (tegelik või eelarveline). Seega ei saa valuutasid muuta. Sellisel juhul järgige järgmises jaotises esitatud etappe.

### <a name="transactions-have-been-posted"></a>Kanded on sisestatud

**Kui juriidilises isikus on sisestatud kandeid, on ainus viis arvestus- ja aruandlusvaluutade muutmiseks või lisamiseks uue juriidilise isiku loomine, millele on õiged valuutad.** Selle protsessi hõlbustamiseks võimaldab süsteemi andmehaldus kopeerida seadistuskirjed ja põhikirjed praegusest juriidilisest isikust uude juriidilisse isikusse.

Arvestus- või aruandlusvaluuta muudatused on ulatuslikud. Need ei mõjuta mitte ainult pearaamatut, vaid ka kõiki alammooduleid (müügireskontro, ostureskontro, varud, projekt jne), kõiki sõltumatu tarkvaratootja (ISV) lahendusi ja kõiki teie tehtud laiendusi, mis summasid salvestavad.

Iga summa leidmisel ja teisendamisel erinevasse valuutasse võivad tekkida vead. Seetõttu ei kinnita tehniline töörühm skripti, mis muudab või lisab arvestus- ja aruandlusvaluutasid. Lisaks, kuigi varem rakenduse Microsoft Dynamics AX 2012 jaoks saadaval olnud tööriist laseb teil muuta või lisada arvestus- ja aruandlusvaluutasid, loeti see tööriist nii AX 2012 R3 kui ka Finance'i jaoks iganenuks.

Järgige neid etappe, et kopeerida seadistus- ja koondandmed praegusest juriidilisest isikust uude juriidilisse isikusse.

1. Avage **Tööruumid \> Andmehaldus**.
2. Valige grupis **Import/eksport** üksus **Mallid**.
3. Veenduge, et mallid on saadaval. Kui ühtki malli pole saadaval, valige **Vaikemallide laadimine** ja oodake, kuni mallid luuakse.
4. Naaske tööruumi **Andmehaldus**.
5. Valige **Juriidilisse isikusse kopeerimine**.
6. Sisestage grupi nimi ja kirjeldus.
7. Valige väljal **Algne juriidiline isik** juriidiline isik, millest andmed kopeeritakse.
8. Valige kiirkaardil **Juriidilised sihtisikud** üksus **Juriidiliste isikute loomine**, et luua uus juriidiline isik, millesse saate kopeerida algse juriidilise isiku andmed. Andmete kopeerimiseks olemasolevasse juriidilisse isikusse valige **Vali olemasolev**.
9. Valikuline: määrake välja **Kopeeri numbriseeriad** väärtuseks **Jah**. (See etapp on soovitatav andmete kopeerimisel.)
10. Valige alal **Valitud üksused** käsk **Lisa mall**.
11. Valige kasutatavad mallid. Uue juriidilise isiku jaoks soovitatavate mallide hulgas on **025 – Pearaamat** ja **Finantsid**. Soovitame teil üle vaadata kõik muud saadaolevad mallid, et teha kindlaks, kas mõni neist vastab teie nõuetele.
12. Valige **Juriidilisse isikusse kopeerimine** pakktöötluse alustamiseks, millega luuakse valitud üksused ja kopeeritakse need juriidilisse sihtisikusse.
13. Pärast töötluse lõpuleviimist, kuid enne mis tahes kande sisestamist, avage pearaamat ja uuendage arvestus- ja aruandlusvaluutasid käesolevas artiklis eespool kirjeldatud viisil.

Kui lõite uue juriidilise isiku, et saaksite muuta arvestus- või aruandlusvaluutat, veenduge, et vana juriidilise isiku valuutades algsaldod teisendatakse uutesse valuutadesse.

Eelmisi etappe kirjeldavat videot vt [Juriidilisse isikusse kopeerimine](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
