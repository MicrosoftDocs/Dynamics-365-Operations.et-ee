---
title: Meilikanali konfigureerimine
description: See teema kirjeldab, kuidas konfigureerida meilikanalit elektrooniliste arvete saamiseks.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a5896a033212cf0f29f686eec0ab6fb3bc1d2a6
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371868"
---
# <a name="configure-an-email-channel"></a>Meilikanali konfigureerimine

[!include [banner](../includes/banner.md)]

Kui elektroonilise arveldamise funktsioon, mille lõite impordib elektroonilist hankijaarvet lisatud failidest, mis on saadud meiliga, peaksite konfigureerima e-posti konto kanali.

1. Valige regulatiivses konfiguratsiooniteenuses (RCS) loodud elektroonilise arveldamise funktsioon. Veenduge, et valite versiooni, mille olek on **Mustand**.
2. Vahekaardil Seadistused **valige** lisa **·**.
3. **Valige väljagrupi Uus** funktsiooniseadistuse loomine **ripploendist** Uus suvand Kohandatud **seadistus**.
4. Valige jaotises **Seadistuse** tüüp suvand **Andmekanal**.
5. Sisestage **väljale Andmekanali** valimine suvand **Sissetulev meil**.
6. Valige **Loo**.
7. Valige rida, mille lõite, ja seejärel valige käsk **Redigeeri**.
8. **Seadke jaotise Parameetrid** vahekaardil **Andmekanal** järgmised nõutavad väljad.

    | Väli                | Kirjeldus |
    |----------------------|-------------|
    | Andmekanal         | Sisestage kordumatu nimi andmekanali tuvastamiseks. Nime maksimumpikkus on 10 märki. Sellele viidatakse kommunikatsiooniprotsessi jooksul kohaldatavusreeglites ja ühendatud rakendustes. |
    | Serveri aadress       | Sisestage meiliaadressi pakkuja serveri aadress. Näiteks on pakkuja serveri aadress `https://outlook.live.com` imap-mail.outlook.com. |
    | Serveri port          | Sisestage pordi number, mida meilikonto pakkuja kasutab. Näiteks on pakkuja serveriport `https://outlook.live.com` 993. |
    | Kasutajanime saladus     | Sisestage võti Microsoft Azure Vault-saladus, mis sisaldab meiliaadressi kasutajakonto ID-d. See saladus tuleb luua Võtme vaultis ja seadistada oma teenuse keskkonnas. |
    | Kasutaja parooli saladus | Sisestage võti Vault-saladus, mis sisaldab meiliaadressi kasutajakonto parooli. |
    | Ajalõpp              | Maksimaalne ajalimiit millisekundites (ms), mida süsteem peaks vastuseks ootama. Vaikeväärtus on 10 000 ms (10 sekundit). |
    | Põhikaust          | Määrake meili importimise allikas või kaust, mille kaudu teenus peaks töötlema e-kirju. |
    | Arhiivikaust       | Määrake kaust, kuhu töödeldud meilisõnumid tuleks salvestada. Kui te seda kausta ei määra, loob süsteem selle automaatselt. |
    | Tõrke kaust         | Määrake kaust, kuhu süsteem peaks e-kirjad teisaldama, kui töötlemine nurjub. Kui te seda kausta ei määra, loob süsteem selle automaatselt. |
    | Sõnumi maksimaalne maht     | Sisestage töödeldav üksikteate maksimaalne suurus baitides. Vaikeväärtus on 20,000,000 baiti. |
    | Maksimaalne sõnumite arv   | Sisestage ühe tegevuse jaoks töödeldav sõnumite maksimaalne arv. Kui te ei soovi sõnumite arvu piirata, seadke väärtuseks **0** (null). |
    | Saatja filter          | Sisestage string saatja aadressi järgi filtreerimiseks. Töödeldakse ainult e-kirju, kus saatja aadress vastab filtrile. Väli on valikuline. Mitme saatja aadressi määramiseks kasutage semikooloneid (;) eraldajatena. |
    | Teema filter       | Sisestage teema alusel filtreerimiseks string. Töödeldakse ainult e-kirju, kus teema vastab filtrile. Väli on valikuline. Toetatakse lihtmaski, nagu näiteks **\*smth\*.ext**, kus iga tärn (\*) tähistab iga tähemärgi nulli või rohkem esinemiskordi. |
    | Kuupäevafilter          | Määrake kuupäev, et määrata töödeldavate teadete maksimaalne vanus päevades. Väli on valikuline. Vaikeväärtus on 30 päeva. |
    | Töötlemisrežiim      | <p>Valige üks järgmistest suvanditest, et määrata, kas kõiki meilis manuseid saab koos töödelda või kas iga manust tuleb eraldi töödelda:</p><ul><li><b>Manusena</b> – iga meilisõnumis manuse kohta luuakse uus elektrooniline dokument. Näiteks kui üks meil sisaldab mitut faili, mis sisaldavad e-arve andmeid, loetakse iga fail süsteemis uueks e-arveks.</li><li><b>Meiliga</b> – üks manus on põhimanus ja üks elektrooniline arve luuakse süsteemis. Teisi manuseid saab kasutada tugifailidena.</li></ul> |

9. Lisage jaotises **Manuste** filter faili filtreerimisteave. Töödeldakse ainult määratletud filtrit rahuldavaid manuseid. Näiteks . **\* xml filtreerib** manuseid, mille nimelaiend on .xml. Manuse nime kasutatakse seadistuses Dynamics 365 Finance või Dynamics 365 Supply Chain Management selle ajal.

    - Kui seate eelmises **sammus** välja **Töötlusrežiim** väärtuseks Meiliga, saate siia lisada mitu filtrit. Nimi identifitseerib konkreetse dokumendi.
    - Kui seate välja **Töötlusviis** väärtuseks **Manusega**, saate lisada ainult ühe filtri.

10. Vaadake vahekaardil **Kohaldatavusreeglid** läbi ja uuendage kriteeriume vastavalt vajadusele. Kanali välja väärtus **peab** olema võrdne väärtusega, mille sisestasite **sammus** 8 andmekanali väljale.
11. Valige **Salvesta** ja sulgege leht.