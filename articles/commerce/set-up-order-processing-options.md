---
title: Kõnekeskuse kanalite seadistamine
description: Selles teemas antakse teavet tellimuste töötlemiste kohta kõnekeskuste puhul, kasutades rakendust Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCROrderParameters, MCRSalesTableOrderHistory, SalesOrderProcessingWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78973
ms.assetid: 09fca083-ac0d-4f30-baf2-bb00a626be12
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28954eab857a06da3978ca362081dfc3c525354d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411750"
---
# <a name="set-up-call-center-channels"></a>Kõnekeskuse kanalite seadistamine

[!include [banner](includes/banner.md)]

Ettevõte saab määratleda Dynamics 365 Commerceis mitu kõnekeskuse kanalit. Kõnekeskuse kanaleid konfigureeritakse valikus **Jaemüük ja kaubandus** \> **Kanalid** \> **Kõnekeskused** \> **Kõik kõnekeskused** ja need on omased kindlale juriidilisele isikule.

Uue kõnekeskuse kanali loomisel määratakse sellele süstemaatiliselt tootmisüksuse number. Kuna kõnekeskused luuakse tootmisüksustena, saavad kasutajad linkida kõnekeskuse kanali erinevate Commerce’i funktsioonidega, nagu sortimentid, kataloogid ja kindlad tarneviisid.

Kõnekeskuse kanalil saab konfigureerida vaikelao. Seejärel, kui sellel kanalil luuakse müügitellimusi, sisestatakse vaikeladu automaatselt müügitellimuse päisesse, välja arvatud juhul, kui müügitellimuse jaoks valitud kliendis on määratletud muu ladu. Sellisel juhul sisestatakse vaikimisi kliendi ladu.

Kõnekeskuse funktsioonide kasutamiseks peavad kasutajad olema lingitud kõnekeskuse kanaliga. Kõik müügitellimused, mille kasutaja loob, lingitakse automaatselt selle kasutaja kõnekeskuse kanaliga. Praegu ei saa ühte kasutajat mitme kõnekeskuse kanaliga korraga linkida.

Kõnekeskuse kanalil saab konfigureerida ka meiliteatise profiili. Profiil määratleb meilimallid, mida kasutatakse meili saatmisel klientidele, kes esitavad tellimusi kõnekeskuse kanali kaudu. Süsteemisündmuste juurde saab konfigureerida meilipäästikuid, näiteks tellimuse esitamise või tellimuse saadetise jaoks.

Enne kui müüki saab õigesti kõnekeskuse kanali kaudu töödelda, tuleb kanali jaoks määratleda õiged [makseviisid](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-payments) ja tarneviisid.

Kõnekeskuse kanali tasemel saate määratleda muud vaikeväärtused, mis on seotud finantsdimensioonidega, mis lingitakse sellel kanalil loodavate tellimustega.

## <a name="options-for-order-processing-behavior"></a>Tellimuse töötlemise käitumise suvandid

Kõnekeskuses loodud müügitellimuste jaoks saadaolevatele funktsioonidele avaldavad suurt mõju kolm sätet selle kõnekeskuse konfiguratsioonis: **Tellimuse lõpetamise lubamine**, **Otsemüügi lubamine** ja **Tellimuse hinnakontrolli lubamine**.

### <a name="enable-order-completion"></a>Tellimuse lõpetamise lubamine

Kõnekeskuse kanali säte **Tellimuse lõpetamise lubamine** mõjutab selle kanali jaoks sisestatud müügitellimuste töötlemise voogu. Kui säte on sisse lülitatud, peavad kõik müügitellimused enne kinnitamist läbima kinnitusreeglite hulga. Saate neid reegleid käivitada, kui valite nupu **Vii lõpule**, mis on lisatud müügitellimuse lehe tegumiribale. Kõik müügitellimused, mis luuakse siis, kui säte **Tellimuse lõpetamise lubamine** on sisse lülitatud, peavad läbima tellimuse lõpetamise protsessi. See protsessi jõustab makse ja makse kinnitamise loogika hõivamist. Lisaks makse jõustamisele saab tellimuse edastamise protsess käivitada [pettuse kontrollid](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-fraud-alerts), mille teie saate süsteemis konfigureerida. Tellimused, mille makse või pettuse kontrolli kinnitamised nurjuvad, pannakse ootele ja neid ei saa täiendavaks töötlemiseks (nagu komplekteerimine või tarnimine) väljastada, kuni ootele paneku põhjustanud probleem on lahendatud.

Kui säte **Tellimuse lõpetamise lubamine** on kõnekeskuse kanali jaoks sisse lülitatud ning müügitellimuses sisestatakse reakaubad ja kanali kasutaja üritab müügitellimuse vormi sulgeda või selle juurest mujale navigeerida ilma esmalt suvandit **Vii lõpule** valimata, jõustab süsteem tellimuse lõpetamise protsessi, avades müügitellimuse kokkuvõtte lehe ja paludes kasutajal tellimuse õigesti esitada. Kui tellimust ei saa koos maksega õigesti esitada, saab kasutaja kasutada [tellimuse ootelepaneku](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) funktsiooni, et panna tellimus ootele. Kui kasutaja üritab tellimust tühistada, peab ta selle õigesti tühistama, kasutades kas funktsiooni Tühista või funktsiooni Kustuta, olenevalt funktsioonist, mida kasutaja turberoll lubab.

Kui säte **Tellimuse lõpetamise lubamine** on kõnekeskuse kanali jaoks sisse lülitatud, jälgitakse tellimusel välja **Makse olek**. Süsteem arvutab **Makse oleku**, kui müügitellimus on esitatud. Ainult tellimustel, millel on kinnitatud makseolek, lubatakse liikuda läbi süsteemi täiendavate tellimuse töötlemise etappide juurde, nagu komplekteerimine ja saatmine. Kui makse on tagasi lükatud, lubatakse tellimuse üksikasjaliku oleku juures lipp **Ära töötle**, mis paneb tellimuse ootele, kuni maksega seotud probleem on lahendatud.

Lisaks, kui säte **Tellimuse lõpetamise lubamine** on sisse lülitatud ning kasutajad loovad müügitellimusi ja nad on reakauba sisestamise režiimis, kuvatakse peamise müügitellimuse päises väli **Allikas**. Välja **Allikas** kasutatakse [kataloogi lähtekoodi](https://docs.microsoft.com/dynamics365/unified-operations/retail/call-center-catalogs) hõivamiseks otseturustamise müügistsenaariumis. Seda koodi saab seejärel kasutada erihindade ja kampaaniate jaoks.

Isegi kui säte **Tellimuse lõpetamise lubamine** on välja lülitatud, saavad kasutajad siiski müügitellimusele lähtekoodi rakendada. Kuid nad peavad väljale **Allikas** juurdepääsu saamiseks esmalt avama müügitellimuse päise üksikasjad. Teisisõnu on vaja teha paar lisaklõpsu. Sama käitumine rakendub funktsioonidele, nagu Saatmine lõpetatud ja Kiirendatud tellimused. Need funktsioonid on saadaval kõigi kõnekeskuses loodud tellimuste jaoks. Kuid kui säte **Tellimuse lõpetamise lubamine** on sisse lülitatud, näevad kasutajad nende funktsioonide konfiguratsiooni müügipäises, kui nad on rea sisestamise vaates. Nad ei pea sobivate sätete ja väljade leidmiseks müügitellimuse päise üksikasjadesse süvitsi minema.

### <a name="enable-direct-selling"></a>Otsemüügi lubamine

Kui säte **Otsemüügi lubamine** on kõnekeskuse kanali jaoks sisse lülitatud, saavad kasutajad kasutada Commerce’i ülesmüügi või ristmüügi funktsioone. Sel juhul kuvatakse tellimuse sisestamise ajal hüpikaken, kus soovitatakse teisi tooteid, mida kõnekeskuse kasutaja saab kliendile pakkuda. Soovitatud tooted põhinevad tootel, mida müügitellimuse real just telliti. Praegu konfigureeritakse ülesmüügi ja ristmüügi soovitusi toodete või kataloogide kauba tasemel. Kui säte **Otsemüügi lubamine** on kõnekeskuse kanalil välja lülitatud, ei kuvata tellimuse sisestamisel hüpikaknaid, isegi juhul kui tellitava kauba jaoks määratleti kehtiv ülesmüük või ristmüük.

Kui säte **Otsemüügi lubamine** on sisse lülitatud, on ka müügitellimuse sisestamise lehe skriptide ja piltide funktsioonid sisse lülitatud. Sel juhul on tellimuse sisestamise ajal lehe paremal küljel saadaval teabepaan. Sellel paneelil kuvatakse skriptid, mis on seotud üldise tellimuse sisestamise protsessiga, rakendatud kataloogi lähtekood või tellitavate kaupadega seotud skriptid. Lisaks saab piltide paneel kuvada tellitavate kaupade tootepildi, kui toote seadistuses on kauba jaoks määratletud pilt.

### <a name="enable-order-price-control"></a>Tellimuse hinnakontrolli lubamine

Kui säte **Tellimuse hinnakontrolli lubamine** on sisse lülitatud, saavad ainult volitatud kasutajad tellimuse sisestamise ajal kauba müügihinda muuta. Muudatused peavad jääma määratletud vahemikesse. Kasutajad, kellel pole õiget volitust, peavad hinna muutmiseks esitama taotluse. Seejärel töödeldakse taotlust läbi süsteemi töövoogude ning suunatakse ülevaatamisse ja kinnitamisse.

## <a name="channel-users"></a>Kanali kasutajad

Kõnekeskuse kanali määratlemisel peate linkima kanali kasutajad kõnekeskusega. Vastasel korral ei saa kõnekeskust süsteemis kasutada. Kui kasutajad logivad Commerce’i sisse ja sisestavad tellimuse sisestamisega seotud lehel müügitellimusi või tagastustellimusi, kontrollitakse nende kasutaja ID-d kõnekeskuse kanali konfiguratsiooni suhtes. Kui kasutaja on lingitud kindla kõnekeskuse kanaliga, pärivad kasutaja loodavad tellimused selle kanali omadused ja vaikeväärtused.

Vaikimisi on lipp **Müük** müügitellimuse päises kõigi kõnekeskuse kasutajate loodavate tellimuste jaoks sisse lülitatud. Tellimused saavad seejärel kasutada ära süsteemi kaubanduse kohast hinda ja kampaaniafunktsioone.


Kasutajad, kes ei ole kõnekeskuse kanaliga lingitud, kasutavad rakenduse Microsoft Dynamics 365 Finance standardseid tellimuse sisestamise funktsioone. Tellimusi, mille need kasutajad sisestavad müügitellimuse sisestamise vormi kaudu, ei tuvastata süstemaatiliselt Commerce’i tellimustena. Lisaks ei kehti sellistele nende kasutajate loodud tellimustele tellimuse lõpetamise töötlemisreeglid, hinnakujunduse loogika ega muud kinnitused, mille saab määratleda kõnekeskuse kanali konfiguratsioonis või kõnekeskuse süsteemiparameetrites.

Kui olete lõpetanud kõnekeskuse kanali konfigureerimise ja kanali kasutajate määratlemise, veenduge soovitud süsteemikäitumise tagamiseks, et kõik vajalikud kõnekeskuse parameetrid oleksid valikus **Jaemüük ja kaubandus** \> **Kanali seadistus** \> **Kõnekeskuse seadistus** \> **Kõnekeskuse parameetrid** määratletud. Veenduge, et ka seotud numbriseeriad oleksid määratletud.

> [!NOTE]
> Kõnekeskuse funktsiooni kasutamiseks peab suvandi **Mitu saajat** konfiguratsioonivõti olema lubatud. Selle konfiguratsioonivõtme leiate **Kaubanduse konfiguratsiooni** võtmetest asukohas **Süsteemihaldus**\> **Seadistus** \> **Litsentsi konfiguratsioon**. See on nõutav kõnekeskuse funktsiooni tõttu, mis sooritab müügitellimuse rea tasemel konfigureeritud tarneaadressi alusel erinevaid valideerimisi. 

