---
title: IoT iseõppimisvõime stsenaariumi seadistamine
description: Selles teemas kirjeldatakse, kuidas konfigureerida stsenaariumi Supply Chain Managementis IoT iseõppimisvõime jaoks.
author: robinarh
manager: AnnBe
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b87a9b73f49e73fe13b98fb11da939c9b30e0f6e
ms.sourcegitcommit: 261b70ea358b2c231e20f320ed8bd6adc1e7d715
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/19/2020
ms.locfileid: "3386506"
---
# <a name="scenario-setup-for-iot-intelligence"></a>IoT iseõppimisvõime stsenaariumi seadistamine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas konfigureerida stsenaariumi Supply Chain Managementis IoT iseõppimisvõime jaoks. Enne, kui saate seadistada stsenaariume, peate [seadistama LCS-i](iot-lcs-setup.md).

Selles teemas konfigureerite stsenaariumi **Seadmete seisakuaeg** teatise loomiseks Supply Chain Managementis masina tõrgete puhul.

## <a name="configure-the-equipment-downtime-scenario-in-supply-chain-management"></a>Stsenaariumi **Seadmete seisakuaeg** konfigureerimine Supply Chain Managementis

Stsenaarium **Seadmete seisakuaeg** vastendab märguande osalisest väljas masina teatiste lävele. Masinat jälgitakse ainult juhul, kui see on selle stsenaariumi jaoks valitud ja on seatud käitama Supply Chain managementis. Kui aeg, millal seade sai viimati märguande osaliselt väljas, on suurem kui teatise lävi, käivitatakse teatis **Masina seisak**. Kui masin töötab edasi kuni järgmise märguande **PartOut** saamiseni käivitatakse teatis **Masin töötab**. Kui masina seisak kestab 30 minutit, käivitatakse uus teatis **Masina seisak**.

Stsenaariumil **Seadmete seisakuaeg** on järgmised sõltuvused.

+ Teatise käivitamiseks tuleb käivitada tootmistellimus vastendatud masinal.
+ Vastendatud masina signaali osaliselt väljas esindav märguanne tuleb saata kordumatu atribuudi nimega IoT-keskusesse.
+ IoT-keskuse sõnum peab sisaldama Unixi millisekundites ajatempli atribuuti.

Stsenaariumi konfigureerimiseks tehke järgmist.

1. Logige sisse Supply Chain Managementi.
2. Lubage IoT iseõppimisvõime funktsiooni lipp. Lisateavet vt [Funktsioonihalduse ülevaatest](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
3. Konfigureerige mõõdikud. Vaadake lisateavet teemast [Kuidas konfigureerida mõõdikuid](iot-metrics-setup.md#configure-metrics).
4. Liikuge jaotisse **Tootmise juhtimine**.
5. Liikuge jaotisse **Seadistus \> IoT iseõppimisvõime \> Stsenaariumide haldus**.
6. Klõpsake paani **Seadmete seisakuaeg** nuppu **Konfigureeri**. Konfigureerimisviisard algab lehega **Seadmete anduri skeemi määratlus**. Selle eesmärk on seadistada skeem Supply Chain Managementis, et see vastaks IoT sõnumite JSON-vormingule. Saate määratleda mitu sõnumiskeemi. Vaadake lisateavet teemast [IoT-keskuse sõnumiskeemi vormingud](iot-schema-format.md). Selles näites sisaldab sõnumi koormus järgmise vorminguga sõnumite partiid.

    ```json
    {
        "timestamp": 1576016821614,
        "payload": [
            {
                "id": "IoTInt.Machine1225.PartOut",
                "timestamp": 1576016821614,
                "value": True
            },
            {
                "id": "IoTInt.Machine1226.PartOut",
                "timestamp": 1576016991616,
                "value": True
            }
        ]
    }
    ```

7. Lisage tabelisse rida.

    1. Määrake välja **Skeemi nimi** väärtuseks **ID**.
    2. Määrake välja **Skeemi tee** väärtuseks **/payload[\*]/id**.
    3. Määrake välja **Kirjeldus** väärtuseks **Sõnumi ID**.

8. Lisage tabelisse rida.

    1. Määrake välja **Skeemi nimi** väärtuseks **Ajatempel**.
    2. Määrake välja **Skeemi tee** väärtuseks **/payload[\*]/timestamp**.
    3. Määrake välja **Kirjeldus** väärtuseks **Sõnumi ajatempel**.

9. Lisage tabelisse rida.

    1. Määrake välja **Skeemi nimi** väärtuseks **Väärtus**.
    2. Määrake välja **Skeemi tee** väärtuseks **/payload[\*]/value**.
    3. Määrake välja **Kirjeldus** väärtuseks **Sõnumi väärtus**.

    Teil pole vaja määratleda sõnumi kõiki atribuute, ainult neid, mida vajate. Selles näites ei loonud te rida üksusele **Juurajatempel**. Üksuse **Juurajatempel** tee oleks **/timestamp**.
  
10. Klõpsake nuppu **Edasi**, et avada leht **Seadmete anduri skeemikaart**.
11. Määrake real **Seadmete ressursi ID** välja **Skeemi nimi** väärtuseks **ID**. Kehtivad väärtused kuvatakse ripploendi tabelis.
12. Määrake rea **UTC-aeg** välja **Skeemi nimi** väärtuseks **Ajatempel**. Kehtivad väärtused kuvatakse ripploendi tabelis.
13. Määrake real **Osaliselt toodetud märguanne** välja **Skeemi nimi** väärtuseks **Väärtus**. Kehtivad väärtused kuvatakse ripploendi tabelis.
14. Klõpsake nuppu **Edasi** lehe **Seadmete ressursi ID konfiguratsioon** jaoks.
15. Selles etapis vastendate IoT-keskuse sõnumi väärtused Supply Chain Managementi ressurssidele.

    1. Lisage tabelis **Märguande andmete väärtused** uus rida ja sisestage veergu **Väärtus** väärtus **IoTInt.Machine1225.PartOut**. Väärtus **IoTInt.Machine1225.PartOut** tuletatakse IoT-keskuse sõnumi JSON-i atribuudist **id**.
    2. Klõpsake valikut **Salvesta**.
    3. Klõpsake tabelis **Ärikirje vastendamine** valikut **Uus**. Välja **Ärikirje tüüp** vaikeväärtus asustatakse automaatselt ja seda ei pea muutma.
    4. Valige veerus **Ärikirje** Supply Chain Managementi masina ressurss, kust selle signaali väärtus saadetakse.
    5. Klõpsake valikut **Salvesta**.
    6. Korrake neid etappe, lisades uue ärikirje vastendamise üksusele **Machine1226**. Saate vastendada mitu signaali andmete väärtust ühele kirjele Supply Chain Managementis.

16. Kasutage veergu **Valitud**, et valida, milliseid masinaid soovite töödelda. Kõiki märguande väärtusi ei pea määratlema ja kõiki masinaid ei pea valima.
17. Klõpsake nuppu **Edasi** lehe **Osaliselt toodetud märguande konfigureerimine** avamiseks.
18. Lisage rida tabelisse **Märguande andmete väärtused** ja seadke suvandi **Väärtu** väärtuseks **Tõene**. Väärtus **Tõene** tuletatakse IoT-keskuse sõnumi JSON-i atribuudist **väärtus**. Saate lisada nii palju väärtusi, kui oma stsenaariumi jaoks vajate.
19. Klõpsake valikut **Salvesta**.
20. Klõpsake nuppu **Edasi**, et avada leht **Seadmete seisakuaja lävi**. Loetletud masinad on varasemalt märguande väärtustele vastendatud masinad. Selles etapis määratlete masina seisaku tuvastamise läve. Näiteks kui seate läve väärtuseks 10, loob Supply Chain Management teatise, kui masinalt ei tule 10 minuti jooksul sõnumit osaliselt väljas.
21. Lehele **Stsenaariumi lubamine** minemiseks klõpsake valikut **Järgmine**. Liigutage liugurit stsenaariumi lubamiseks.
22. Klõpsake nuppu **Lõpeta**.

Stsenaariumi häälestus on lõpule viidud. IoT iseõppimisvõime alustab automaatselt IoT-keskuse sõnumite töötlemist.

## <a name="configure-the-product-quality-scenario-in-supply-chain-management"></a>Stsenaariumi **Toote kvaliteet** konfigureerimine Supply Chain Managementis

Stsenaarium **Toote kvaliteet** loob teatise, kui kauba atribuut jääb määratletud vahemikust väljapoole. Näiteks võib sensor saata iga kauba kaalu IoT-keskusesse. Supply Chain Managementis luuakse teatis, kui kaup on liiga raske või liiga kerge.

Stsenaariumil on järgmised sõltuvused.

+ Tootmistellimus peab töötama vastendatud masinal ja tootma vastendatud partii atribuudiga toodet teatise käivitamiseks.
+ Partii atribuuti esindav märguanne tuleb saata kordumatu atribuudi nimega IoT-keskusesse.
+ IoT-keskuse sõnum peab sisaldama Unixi millisekundites ajatempli atribuuti.

## <a name="configure-the-production-delays-scenario-in-supply-chain-management"></a>Stsenaariumi **Tootmise viivitused** konfigureerimine Supply Chain Managementis

Stsenaarium **Tootmise viivitused** loob teatise, kui tootmise läbilaskevõime langeb alla läve väärtuse. Selle stsenaariumi puhul saadetakse IoT-keskusesse märguanne **PartOut** iga toodetud kauba kohta. Supply Chain Managementis arvutatakse tellimuse viivitus vastavalt sellele, kui pikalt on tootmistellimuse käitamine plaanitud, mitu kaupa tuleks toota, kui kaua tööd on käitatud ja mitu märguannet **PartOut** vastu võetakse. Viivituse teatis luuakse siis, kui selle töö märguannete **PartOut** arv jääb eeldatava väärtuse läve väärtusest allapoole.

Stsenaariumil on järgmised sõltuvused.

+ Teatise käivitamiseks tuleb käivitada tootmistellimus vastendatud masinal.
+ Vastendatud masina signaali osaliselt väljas esindav märguanne tuleb saata kordumatu atribuudi nimega IoT-keskusesse.
+ IoT-keskuse sõnum peab sisaldama Unixi millisekundites ajatempli atribuuti.

## <a name="how-to-disable-a-scenario"></a>Stsenaariumi keelamine

Stsenaariumi keelamiseks järgige neid toiminguid.

1. Liikuge Supply Chain Managementi jaotisse **Tootmise juhtimine \> Häälestamine \> IoT iseõppimisvõime \> Stsenaariumihaldus**.
2. Klõpsake stsenaariumi suvandit **Konfigureerimine**.
3. Klõpsake viisardi viimasele vahekaardile jõudmiseks nuppu **Edasi**.
4. Liigutage liugurit stsenaariumi keelamiseks.
