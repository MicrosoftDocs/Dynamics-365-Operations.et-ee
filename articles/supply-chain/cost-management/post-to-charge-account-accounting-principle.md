---
title: Sisesta kulukonto raamatupidamispõhimõttesse
description: See artikkel annab ülevaate kulukonto raamatupidamispõhimõtese sisestamise kohta.
author: rachel-profitt
ms.date: 05/02/2022
ms.topic: article
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-05-02
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: c03109baaa341b25af70840b791ddf04f692fb1a
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016561"
---
# <a name="post-to-charge-account-accounting-principle"></a>Sisesta kulukonto raamatupidamispõhimõttesse

Kulude *konto raamatupidamispõhimõtte* sisestamine võimaldab teil kontoda ja viia vastavusse erinevused, mis ilmnevad ühiku hinnas füüsilise ja finantsilise sisestuse, ostetud kaupade kaudsete kulude või ostutellimuse kulude vahel.

Kaks konfiguratsiooni ostureskontro **kulude** koodide jaoks kulude koodi lehel (**\>\>** Ostureskontro kulude häälestuse kulude kood) võivad põhjustada ostutellimuse, mis mõjutavad laovarade hindamist:

- Kulude koodide **puhul** *·* **·** *·*, kus deebeti tüübi välja väärtuseks on seatud Kaup ja kreediti tüübi väli on seatud pearaamatukontole, toimib absorbtsioonikontoks valitud pearaamatukonto laovariatsiooni kontona.
- Kulude **koodide** *·* **·** *puhul, kus deebeti tüübi väli on seadistatud väärtusele Kaup ja välja Kreedit tüüp väärtuseks on seatud Klient/* Hankija, arvestuseks võetakse kulu materjalikuluna ja kasutatakse kauba laovariatsiooni kontot.

## <a name="european-special-accounting-rule"></a>Euroopa eri raamatupidamisreegel

Euroopas kasutatakse konto *raamatupidamispõhimõtte sisestamisel* sageli spetsiaalse raamatupidamisreegli sisseseadmiseks. Näiteks kasutatakse tavaliselt ühte järgmistest meetoditest varude muudatuste arvesse võtta:

- **Müügimeetodi kulu –** seda meetodit toetab standardne lao sisestusreeglite konfiguratsioon. *Maksmiskontole* sisestamise raamatupidamispõhimõte pole nõutav.
- **Kulumeetodi olemus –** väiksemad organisatsioonid kasutavad sageli seda meetodit. See koosneb tavaliselt järgmistest sammudest:

    1. Kaubad või teenused kulutakse sissetuleku ajal täielikult.
    2. Perioodi lõpus tehakse tsükliline loendus.
    3. Koguse ja väärtuse käsitsi korrigeerimine sisestatakse varudesse. (Vastaskonto on laovariatsiooni konto, mis tasakaalustab sammus 1 sisestatud kulu. Seetõttu näete laoväärtuse muutust ainult sellel kontol.)

Tasukontole *sisestamise põhimõte* võimaldab teil kaks sisestust täielikult automatiseerida. Sel viisil saate perioodi lõpu sulgemise korrigeerimise käsitsi sisestamise eemaldada.

## <a name="enable-the-post-to-charge-account-accounting-principle"></a>Kulukonto raamatupidamispõhimõtte sisestamise lubamine

Kulukonto raamatupidamispõhimõtte *sisestamise lubamiseks* järgige neid samme.

1. Avage **Ostureskontro \> Seadistus \> Ostureskontro parameetrid**.
2. Määrake vahekaardil Arve kiirkaardil **Arve** suvand **Sisesta pearaamatu tasukontole** suvandile **Jah**.*·*
3. Sulgege leht.

## <a name="prerequisites-and-recommended-parameters-for-the-post-to-charge-account-accounting-principle"></a>Eeltingimused ja soovitatavad parameetrid konto raamatupidamispõhimõtte sisestamiseks

Kui plaanite arvestada ostukulusid ja laovariatsioone, peavad olema täidetud järgmised eeltingimused:

- Ostureskontro **parameetrite** **lehe** arve vahekaardil (**\>\> Ostureskontro seadistuse ostureskontro parameetrid)** **peab pearaamatusse** sisestamise suvand olema seatud väärtusele *Jah.*
- Lehel Kauba **mudeligrupid** (**Kuluhalduse \>\>** varude raamatupidamispoliitikad häälestage kauba mudeligrupid) *peavad* kõik järgmised valikud olema seadistatud valikule Jah iga asjakohase mudeligrupi puhul, mis sisaldab kaupu, mis on ostutellimuses.

    - Sisesta füüsiline ladu
    - Sisesta finantsiline laovaru
    - Kumuleerimise kohustus toote sissetulekul

- **Hankeparameetrite** **lehe** vahekaardil Tarne (hankeparameetrid) (**\>\>** hanke häälestamise hankeparameetrid) **·** *tuleb toote sissetuleku kulude loomise suvandi väärtuseks seada Jah.*
- Varude ja **laohalduse** parameetrite **lehe** vahekaardil Varude arvestus (**\>\> varude ja laohalduse parameetrid)** tuleb suvand Sisesta **saateleht pearaamatusse** seada väärtusele *Jah.*
- Sisestuslehe **(Laohalduse** seadistuse **·** **\>\>\>** sisestamise sisestamine) vahekaardil Ostutellimus tuleb igale asjassepuutuvale kaubale kehtivad põhikontod määrata iga järgmise sisestamistüübi puhul:

    - Ostu kulud, arvele kandmata
    - Toote ostu kulu
    - Lao muudatus

## <a name="example-scenario-1-change-in-unit-cost-price"></a>Näide 1. stsenaarium: ühiku omahinna muutus

Selle näite stsenaariumi puhul on eeltingimused järgmised:

- FIFO kulumudel

Järgmine toiming annab näite, mis näitab, mis juhtub, kui muudate ühiku omahinda ostutellimusel.

1. Looge ostutellimus kogusele 1 kaubast, mille ühiku hind on 100,00.
2. Kinnitage ostutellimus.
3. Sisestage toote sissetulek ostutellimusele.
4. Kinnitage kanne toote sissetulekul. Järgmine tabel näitab näidiskannet.

    | Sisestamistüüp | Põhikonto | Põhikonto nimi | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Füüsiline/finantsne? | Summa |
    |---|---|---|---|---|---|---|---|
    | Ost, lao muutus | 600170 | Lao variatsiooni materjalid | Kulu | Krediit | Nr | Füüsiline | -100,00 |
    | Saadud ostetud materjalide kulu | 140100 | Materjalide laoseis | Vara | Deebet | Jah | Füüsiline | 100.00 |
    | Ostu kulud, arvele kandmata | 600180 | Materjali sissetulekud | Kulu | Deebet | Jah | Füüsiline | 100.00 |
    | Ost, tekkepõhine | 200140 | Tekkepõhised ostud | Kohustus | Krediit | Jah | Füüsiline | -100,00 |

5. Sisestage arve ostutellimusele, mille värskendatud ühikuhind on 110,00.
6. Saate kinnitada arve kande. Järgmine tabel näitab näidiskannet.

    | Sisestamistüüp | Põhikonto | Põhikonto nimi | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Füüsiline/finantsne? | Summa |
    |---|---|---|---|---|---|---|---|
    | Ost, lao muutus | 600170 | Lao variatsiooni materjalid | Kulu | Krediit | Nr | Financial | -10,00 |
    | Saadud ostetud materjalide kulu | 140100 | Materjalide laoseis | Vara | Deebet | Jah | Financial | -100,00 |
    | Ostu kulud, arvele kandmata | 600180 | Materjali sissetulekud | Kulu | Deebet | Jah | Financial | -100,00 |
    | Ost, tekkepõhine | 200140 | Tekkepõhised ostud | Kohustus | Krediit | Jah | Financial | 100.00 |
    | Arveldatud ostetud materjalide kulu | 140100 | Materjalide laoseis | Vara | Deebet | Nr | Financial | 110.00 |
    | Toote ostu kulu | 600180 | Materjalide sissetulek | Kulu | Krediit | Nr | Financial | 110.00 |
    | Hankija saldo | 211000 | Ostureskontro kaubandus | Kohustus | Krediit | Nr | Financial | -110.00 |

## <a name="example-2-charges-and-indirect-costs-on-the-purchase-order"></a>Näide 2: ostutellimuse tasud ja kaudsed kulud

Selle näite stsenaariumi puhul on eeltingimused järgmised:

- FIFO kuluarvestusmudel
- **Kulude kood 1: deebetkauba** ja kreediti pearaamatukonto 10% jaoks
- **Kulude kood 2: deebetkaup** ja kreediti klient/hankija 10,00 proportsionaalselt
- **Kaudne kulu:** 2,00% lisatud ostuhinnale

Järgmine toiming annab näite, mis näitab, mis juhtub, kui kaasate ostutellimusele kulud ja kaudsed kulud.

1. Looge ostutellimus kogusele 1 kaubast, mille ühiku hind on 100,00.
2. Lisage 10 protsendi jaoks üks tasukood, mis debiteerib kaupa ja krediteerib pearaamatut.
3. Lisage üks tasukood summale 10,00, mis debiteerib kaupa ja krediteerib klienti/hankijat.
4. Eraldage kulud ostutellimuse ridadele.
5. Kinnitage ostutellimus.
6. Sisestage toote sissetulek ostutellimusele.
7. Kinnitage kanne toote sissetulekul. Järgmine tabel näitab näidiskannet.

    | Sisestamistüüp | Põhikonto | Põhikonto nimi | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Füüsiline või finants | Summa |
    |---|---|---|---|---|---|---|---|
    | Ost, lao muutus | 600170 | Lao variatsiooni materjalid | Kulu | Krediit | Nr | Füüsiline | -110.00 |
    | Eeldatav absorbeeritud kaudne kulu | 600520 | Väljastatud kaudsed kulud | Kulu | Krediit | Jah | Füüsiline | -2.40 |
    | Ostu veos | 600120 | Veose/transpordi kulud | Kulu | Krediit | Nr | Füüsiline | -10,00 |
    | Saadud ostetud materjalide kulu | 140100 | Materjalide laoseis | Vara | Deebet | Jah | Füüsiline | 122.40 |
    | Ostu kulud, arvele kandmata | 600180 | Materjali sissetulekud | Kulu | Deebet | Jah | Füüsiline | 110.00 |
    | Ost, tekkepõhine | 200140 | Tekkepõhised ostud | Kohustus | Krediit | Jah | Füüsiline | -110.00 |

8. Sisestage ostutellimuse arve.
9. Saate kinnitada arve kande. Järgmine tabel näitab näidiskannet.

    | Sisestamistüüp | Põhikonto | Põhikonto nimi | Konto tüüp | Deebet/kreedit? | Kliiringukonto | Füüsiline/finantsne? | Summa |
    |---|---|---|---|---|---|---|---|
    | Ost, lao muutus | 600170 | Lao variatsiooni materjalid | Kulu | Krediit | Nr | Financial | 0.00 |
    | Eeldatav absorbeeritud kaudne kulu | 600520 | Väljastatud kaudsed kulud | Kulu | Deebet | Jah | Financial | 2.40 |
    | Absorbeeritud kaudne kulu | 600520 | Väljastatud kaudsed kulud | Kulu | Deebet | Nr | Financial | -2.40 |
    | Saadud ostetud materjalide kulu | 140100 | Materjalide laoseis | Vara | Krediit | Jah | Financial | -110.00 |
    | Ostu kulud, arvele kandmata | 600180 | Materjali sissetulekud | Kulu | Krediit | Jah | Financial | -110.00 |
    | Ost, tekkepõhine | 200140 | Tekkepõhised ostud | Kohustus | Deebet | Jah | Financial | 110.00 |
    | Arveldatud ostetud materjalide kulu | 140100 | Materjalide laoseis | Vara | Deebet | Nr | Financial | 110.00 |
    | Toote ostu kulu | 600180 | Materjalide sissetulek | Kulu | Krediit | Nr | Financial | 110.00 |
    | Hankija saldo | 211000 | Ostureskontro kaubandus | Kohustus | Krediit | Nr | Financial | -110.00 |
