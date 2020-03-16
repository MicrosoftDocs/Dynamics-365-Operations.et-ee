---
title: Teatisereeglite loomine
description: Selles teemas antakse teavet teatiste kohta ja selgitatakse, kuidas luua teatisereeglit selliselt, et saaksite teavitusi selliste sündmuste kohta nagu saabuv kuupäev või konkreetne muudatus.
author: tjvass
manager: AnnBe
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 85d4774bc710f0c48b384601e5505f11394cf5d5
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075920"
---
# <a name="create-alert-rules"></a>Teatisereeglite loomine

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Alustamine

Enne teatisreegli loomist otsustage, millal või milliste olukordades te teatisi saada soovite. Teades, millise sündmuse kohta te teatist soovite, saate otsida lehe, millel kuvatakse teatist käivitava sündmuse andmed. Sündmuseks võib olla saabuv kuupäev või teatud toimuv muudatus. Seega peate leidma lehe, kus kuvatakse kas määratud kuupäev, muudetud väli või uus loodud kirje. Alles seda teades saate luua teatisereegli.

Teatisereegli loomisel saate määrata kriteeriumid, mis peavad olema täidetud enne teatise käivitamist. Kriteeriumid on põhimõtteliselt vastavus sündmuse toimumise ja teatud tingimuste täitmise vahel. Sündmuse toimumisel hakkab süsteem teostama kontrolli vastavalt seadistusele.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Teatise pakett-tööde käitamise tagamine

Andmete pakett-tööd muutuvad ja tähtajateatised peavad töötama, et teatise tingimusi töödeldaks ja teatisi saadetaks. Pakett-tööde käitamiseks avage **Süsteemi haldus** > **Perioodilised ülesanded** > **Teatised** ja lisage suvandile **Muutusepõhised teated** ja/või **Tähtajateatised** uus pakett-töö. Kui vajalik on pikk ja sageli töötav pakett-töö, valige **Korduvus** ja määrake **Lõppkuupäev puudub** suvandi **Korduvuse muster** väärtuse **Minutid** jaoks ja **Loendus** **1**.

## <a name="events"></a>Sündmused

Teatisereeglit käivitav sündmus saab olla kas saabuv kuupäev või teatud toimuv muudatus. Sündmuste käivitajad on määratud dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind, kui**. Konkreetsel väljal saadaolevad sündmused sõltuvad valitud käivitajast.

Näiteks, kui seadistate teatisereegli väljale **Alguskuupäev**, on tähtajalised sündmused asjakohased. Seetõttu on selle välja puhul saadaval sündmuse tüüp **tähtaeg on**. Samas näiteks välja **Kulukeskus** puhul pole tähtajaline sündmus asjakohane. Seetõttu pole saadaval sündmuse tüüpi **tähtaeg on**. Selle asemel on saadaval sündmuse tüüp **on muutunud**.

## <a name="event-types"></a>Sündmuste tüübid

Toimuda võivad kolme tüüpi sündmused.

- **Loomis- ja kustutamistüüpi sündmused** – need sündmused käivitavad teatise juhul, kui kirje luuakse või kustutatakse.
- **Värskendamistüüpi sündmused** – need sündmused käivitavad teatise, kui andmed kindlal väljal muutuvad.
- **Tähtaja-tüüpi sündmused** – need sündmused käivitavad teatise, kui kuupäev saabub.
    
Toimuvad muudatused saab käivitada kasutaja. Näiteks kasutaja muudab ostutellimuse tarnekuupäeva. Teise võimalusena võivad muudatused ilmneda protsessi käigus. Näiteks muutub lehe väli **Olek**, et peegeldada süsteemi mitmesuguste protsesside töötsüklit.

## <a name="conditions"></a>Tingimused

Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisel juhul** saate kasutada tingimusi, et kontrollida, millal teid sündmustest teavitatakse.

Näiteks saate määrata, et süsteem peaks teid teavitama, kui ostutellimuste olekut muudetakse, kuid ainult juhul, kui olek on kooskõlas määratud tingimustega. Täpsemalt, soovite saada teatist, kui ostutellimuse olekuks määratakse **Saadud**. See olekumuudatus on sündmus, mis käivitab teatise.

Seejärel peate otsustama, milliste ostutellimuste kohta te teatisi soovite. Näiteks saate valida ühe järgmistest valikutest. Need suvandid määravad teatisereegli tingimused.

- **Praegu valitud kirje** – saate teatise, kui kindla ostutellimuse olek muutub olekuks **Saadud**.
- **Kõik kirjed** – saate teatise, kui muudetakse aktiivses lehe vaates oleva kauba ostutellimuse olekut. Teatud kirjete kogumile reeglite loomiseks saate kasutada lehel saadaolevat täpsemat filtrifunktsiooni. Näiteks saate luua teatise, mis käivitatakse kõigi konkreetse kliendigrupi klientide ostutellimuste puhul.
    
## <a name="expiry-of-rule"></a>Reegli aegumine

Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind kuni** saate määrata, kui kaua teatisereegel aktiivne peaks olema.

## <a name="alert-contents"></a>Teatise sisu

Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisega** saate määrata teema ja sõnumi teksti, mida teatiste puhul peaks kasutatama.

## <a name="user-id"></a>Kasutaja kood

Dialoogiboksi **Loo teatise reegel** kiirkaardil **Teavita mind järgmisega** saate määrata, milline kasutaja peaks teatiseid saama. Vaikimisi on valitud teie kasutaja ID. Teatise saava kasutaja muutmise võimalus on piiratud organisatsiooni administraatoritega.

## <a name="alerts-as-business-events"></a>Teatised ärisündmustena

Teatisi saab saata väliselt ärisündmuste raamistikku kasutades. Teatise loomisel seadke suvand **Organisatsiooniülene** valikule **Ei** ja määrake suvand **Saada väliselt** väärtusele **Jah**. Pärast seda, kui teatis käivitab ärisündmuse, saate käivitada teenusesse Power Automate ehitatud voo, kasutades päästikut **Kui ärisündmus leiab aset** rakenduskomplekti Finance and Operations konnektoris, või saata sündmuse eraldi suvandi **Ärisündmuste kataloog** kaudu otse ärisündmuste lõpp-punktile.

## <a name="create-an-alert-rule"></a>Teatisereegli loomine

0. Tagage teatise pakett-tööde käitamine (vt ülal).
1. Avage leht, mis sisaldab jälgitavaid andmeid.
2. Valige toimingupaani vahekaardil **Suvandid** rühmas **Anna ühiskasutusse** suvand **Teavita mind järgmisega**.
3. Valige jälgitav väli dialoogiboksi **Loo teatise reegel** väljal **Väli**.
4. Valige sündmuse tüüp väljal **Sündmus**.
5. Valige soovitud suvand kiirkaardil **Teavita mind järgmisel juhul**. Kui soovite saata teatise ärisündmusena, veenduge, et suvand **Organisatsiooniülene** oleks seatud valikule **Ei**.
6. Kui teatisereegel peaks passiivseks muutuma kindlal kuupäeval, määrake lõppkuupäev kiirkaardil **Teavita mind kuni**.
7. Kinnitage meilisõnumi teema vaikepealkiri või sisestage uus teema kiirkaardi **Teavita mind järgmisega** väljal **Teema**. Teksti kasutatakse meilisõnumi teema pealkirjana, mille saate teatise käivitamisel. Kui soovite saata teatise ärisündmusena, seadke suvand **Saada väliselt** valikule **Jah**.
8. Sisestage valikuline teade väljale **Teade**. Teksti kasutatakse sõnumina, mille saate teatise käivitamisel.
9. Valige **OK**, et salvestada sätted ja luua teatisereegel.
