---
title: Alampearaamatu ülekandmine pearaamatusse
description: See artikkel kirjeldab võimalusi, mis on seotud pearaamatu alammooduli ülekande protsessiga.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: a53b7834271355aaf11c13c3f1886257a97b1da8
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068986"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Alampearaamatu ülekandmine pearaamatusse

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab võimalusi, mis on seotud alamvõtme töölehe kirjete partiide ülekandmise reeglitega.

Versioonis 8.1 tehti muudatusi, et lubada reeglite edastamine, mis võimaldas **Sünkroonsel** valikul iganeda. Lisateavet vt finantside ja [toimingute eemaldatud või taunitud funktsioonidest](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Alampearaamatu partiide edastamiseks on saadaval järgmised valikud.

- **Asünkroonne** – alamraamatu raamatupidamiskannete kandmine pearaamatusse on kavandatud kohe. Pearaamatu kanne salvestatakse kohe, kui ressursid on vabad seda taotlust serveris töötlema.
- **Plaanitud partii** – alammooduli raamatupidamiskirjed, mis tuleb üle kanda, lisatakse pearaamatu töötlemisjärjekorda. Järjekorras olevad kanded töödeldakse sissekannete järjekorras. Iga pearaamatu kanne uuendab kontosid planeeritud ajal, kui ressursid on vabad seda pakett-tööd serveris töötlema.

Versioonil 10.0.8 tehti parandusi **asünkroonse** valiku jõudluse suurendamiseks. See funktsioon on lubatud selle funktsiooni nimega **Alampearaamatu edastamine pearaamatu jõudluse optimeerimiseks**.

Alamraamatu partiide asünkroonse edastamise funktsionaalsus aitab parandada andmete ülekandmist allkirjast pearaamatusse. Väiksemate kannete grupeerimiskogumite ja kannete gruppidesse ülekandmise teel töötleb funktsioon kandeid tõhusamalt. Kannete grupeerimisel kasutatakse tõhusamalt pakktöötluse serveri ressursse.

Asünkroonne alamtööaja partiide ülekanne nõuab, et pakktöötluse server oleks seadistatud, võrgus ja töötaks, kuna pakett-töö toimingud luuakse pakktöötluse serveris koheseks täitmiseks. Kui alammooduli **ülekanne** pearaamatu jõudluse optimeerimise funktsiooni on lubatud, **·** **peab samuti olema lubatud protsessi automatiseerimissüsteemi pakett-töö nimega Protsessi automatiseerimise** pollimise süsteemitöö. Lisateavet vt teemast [Protsessi automatiseerimine](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Tõhususe muutmine paketitasandil kasutab kõigi süsteemi juriidiliste isikute jaoks ühte korduvat partiitööd. Käitusajal luuakse uus pakett-töö, et töödelda nõutud kirjeid, mida pole veel üle kantud. Rohkem sätteid saab kontrollida süsteemihalduse **Protsessi automatiseerimise** leheküljelt. Sel leheküljel saate muuta taustaprotsessi, muuta sagedust ja määratleda perioodi.

Lisateavet protsesside automatiseerimise seadistamise kohta leiate teemat [Protsessi automatiseerimine](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

