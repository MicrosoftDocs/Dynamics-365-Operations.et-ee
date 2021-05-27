---
title: Tagasimaksehalduse sisestamise seadistus
description: Selles teemas kirjeldatakse, kuidas seadistada sisestamisprofiile. Sisestusprofiile kasutatakse tagasimakse halduse arvutamise ridade sisestuskirjete määramiseks.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: b52a1720077c055d416f04cbbe9ec46cbcf319bc
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020407"
---
# <a name="rebate-management-posting-setup"></a>Tagasimaksehalduse sisestamise seadistus

[!include [banner](../includes/banner.md)]

Tagasimaksehalduse sisestusprofiile kasutatakse tagasimakse halduse arvutamise ridade sisestuskirjete määramiseks. Kui tehingu päises on valitud sisestusprofiil, rakendub see kõigile tehingu ridadele.

See funktsioon töötab kõigis ettevõtetes (juriidilised isikud). Saate määrata ettevõtte, mis kogub nõudeid ja nõuete eest makstakse. Saate seadistada ka erinevaid deebetkontosid ja mahakandmise kreeditkontosid lähtekoha sisestusettevõtte kohta.

Tagasimaksehalduse sisestusreeglite seadistamiseks klientide ja müüjate jaoks minge **Tagasimaksehaldus \> Tagasimakse halduse sisestusseadistus \> Tagasimakse halduse sisestusprofiilid**. Leht **Tagasimaksehalduse sisestusprofiilid** sisaldab loendipaani, mis näitab kõiki olemasolevaid profiile. Saate kasutada tegumipaani nuppe, et lisada profiile loendisse või neid eemaldada.

Selle teema ülejäänud jaotised kirjeldavad, kuidas kasutada saadaolevaid välju profiili loomisel või redigeerimisl.

## <a name="posting-profile-header"></a>Profiili päise sisestamine

Järgmises tabelis kirjeldatakse sätteid, mis on saadaval iga Tagasimaksehalduse sisestusreegli päise jaotises.

| Field | Kirjeldus |
|---|---|
| Sisestusreeglid | Sisestage profiili kordumatu nimi. |
| Kirjeldus | Sisestage profiili kirjeldus |
| Moodul | Valige tagasimaksete ja autoritasude tüüp, millega profiil on seotud (*Klient* või *Müüja*). |
| Tüüp | Valige profiili tüüp (*Tagasimakse* või *Autoritasu*). |
| Makse tüüp | <p>See väli määrab sisestatud tagasimakse väljundi vormingu.<p><p>Kui välja **Tüüp** väärtuseks on seatud *Tagasimakse*, on saadaval järgmised väärtused.</p><ul><li>*Puudub* – vaikimisi sisestamistüüp puudub. Seepärast peate määratlema töötlemisel tüübi.</li><li>*Tasumine ostureskontroga* – tagasimakse sisestamisel luuakse tagasimakse kliendile seadistatud rahaülekande müüja arve.</li><li>*Kliendi mahaarvamised* – tagasimakse sisestamisel luuakse kliendi mahaarvamise tööleht tagasimakse kliendile.</li><li>*Maksuarve kliendi mahaarvamised* – tagasimakse sisestamisel luuakse vabas vormis arve tagasimakse kliendile.</li><li>*Kaubanduskulu* – tagasimakse sisestamisel luuakse kliendi mahaarvamise tööleht tagasimakse kliendile.</li><li>*Aruandlus* – tagasimakse sisestamisel luuakse kliendi mahaarvamise tööleht tagasimakse kliendile.</li></ul><p>Kui välja **Tüüp** väärtuseks on seatud *Litsents*, on saadaval järgmised väärtused.</p><ul><li>*Puudub* – vaikimisi sisestamistüüp puudub. Seepärast peate määratlema töötlemisel tüübi.</li><li>*Tasumine ostureskontroga* – tagasimakse sisestamisel luuakse tagasimakse müüja kontole müüja arve.</li><li>*Aruandlus* – tagasimakse sisestamisel luuakse tagasimakse müüja kontole müüja arve.</li></ul><p>Lisateavet vt järgnevast jaotisest [Maksetüübid](#payment-types). |
| Ettevõte | Valige ettevõte (juriidiline isik), kellele kogunevad eraldised ja kelle nõudeid tasutakse. |

### <a name="payment-types"></a>Maksetüübid

Järgmine tabel võtab kokku, kuidas erinevad välja **Maksetüüp** sätted mõjutavad, kuhu maksed sisestatakse. Makseid saab sisestada kliendikontole, müüja kontole või rahaülekande kontole, sõltuvalt sihtkandest ja tagasimakse tüübist.

| Makse tüüp | Sihtkande tüüp | Tagasimakse tüüp | Makse (arvekonto) |
|---|---|---|---|
| Maksa osturestkonrot kasutades | Hankijaarvete tööleht | Kliendi tagasimakse | Kliendi rahaülekande müüja konto |
| Maksa osturestkonrot kasutades | Hankijaarvete tööleht | Kliendi autoritasu | Hankija konto |
| Maksa osturestkonrot kasutades | Hankijaarvete tööleht | Hankija tagasimakse | Hankija konto |
| Kliendi mahaarvamised | Igapäevane tööleht | Kliendi tagasimakse | Kliendi konto |
| Maksuarve kliendi mahaarvamised | Vabas vormis arve | Kliendi tagasimakse | Kliendi konto |
| Kaubanduskulud | Igapäevane tööleht | Kliendi tagasimakse | Kliendi konto |
| Aruandlus | Igapäevane tööleht | Kliendi tagasimakse | Kliendi konto |
| Aruandlus | Hankijaarvete tööleht | Kliendi autoritasu | Hankija konto |
| Aruandlus | Hankijaarvete tööleht | Hankija tagasimakse | Hankija konto |

> [!NOTE]
> Võtke [tagasimaksehalduse tehinguid](rebate-management-deals.md) seadistades arvesse järgmisi punkte.
>
> - Tehinguid, kus välja **Vastavusseviimine** väärtuseks on määratud *Tehing*, ei saa te sisestamise ajal kasutada dünaamilist tehingu kontot. Peate kasutama määratud kliendi- või müüja kontot.
> - Tehinguid puhul, kus välja **Vastavusseviimine** väärtuseks on seatud *Rida*, saate kasutada sisestusprofiili, mis tasakaalustab tehingu rea dünaamilise tehingu kontoga, sest klient on seadistatud tehingu rea kohta.

## <a name="posting-fasttab"></a>Kiirkaart Sisestamine

Järgmises tabelis kirjeldatakse väljasid, mis on saadaval iga Tagasimaksehalduse sisestusprofiili kiirkaardil **Sisestamine**.

| Field | Kirjeldus |
|---|---|
| Kreediti tüüp | Valige, kas krediteerida pearaamatu kontot, klienti või müüjat. |
| Kreeditkonto | Konto, kuhu krediidisummad tagasimakse eraldiste tegemise ajal kirjendatakse. Seda kontot kasutatakse ka deebetkontona, kui kliendi krediteerimiseks pannakse tagasimakse. |
| Töölehe nimi<br>(Jaotises **Eraldis**) | Valige töölehe nimi, mida kasutada sisestatud eraldise kirjendamiseks. |
| Tüüp | Valige, kas tagasimakse postitada pearaamatu kontole, kliendile või müüjale. Kui päises oleva välja **Maksetüüp** väärtuseks on seatud *Maksuarve kliendi mahaarvamised*, on selle välja väärtuseks seatud *Klient/Müüja*. |
| Lähtekonto kasutamine | <p>Valige üks järgmistest väärtustest.</p><ul><li>*Puudub* – selle väärtuse valimisel peate täpsustama konto väljal **Tagasimakse konto**.</li><li>*Tehingukonto* – kasutage kliendi või müüja kontot, mis on tagasimakse real määratud. Seda väärtust saate valida ainult tehingute puhul, kus välja **Vastavusseviimine** väärtuseks on seatud *Rida* ja tehingu read, kus välja **Konto kood** väärtuseks on *Tabel*. See ei kehti kliendi autoritasu sisestusprofiilide kohta.</li></ul> |
| Tagasimakse konto | Konto, millele tegelikud tagasimaksed sisestatakse |
| Töölehe nimi<br>(Jaotises **Tagasimaksehaldus**) | Valige töölehe nimi, mida kasutada kliendile tagasimakse summa kreeditarve sisestamiseks. See väli ei ole saadaval, kui päises oleva välja **Maksetüüp** väärtuseks on seatud *Maksuarve kliendi mahaarvamised*. |
| Kauba käibemaksugrupp | Määrake, kas tagasimakse on maksustatav. |
| Töölehe nimi<br>(Jaotises **Mahakandmised**) | Kui sisestatud tagasimakse ei võrdu eraldisega, saab erinevuse maha kirjutada. Valige töölehe nimi, mida kasutada sisestatud mahakande kirjendamiseks. |

## <a name="posting-by-company-fasttab"></a>Ettevõtte kiirkaardi kaudu sisestamine

Iga tagasimaksehalduse sisestusprofiili kiirkaart **Ettevõttega sisestamine** võimaldab määrata sisestuskonto, mida kasutab ruudustikus iga ettevõte (juriidiline isik).

Ruudustikus ettevõtete lisamiseks või eemaldamiseks kasutage tööriistariba nuppe. Iga kord, kui lisate tabelile rea, kasutage välja **Ettevõte** juriidilise isiku määramiseks sellele reale. Väli **Nimi** seatakse seejärel automaatselt.

Valige rida iga ettevõtte jaoks ja sisestage seejärel järgmine teave, kasutades ruudustiku all olevaid järgmisi välju.

- **Deebiti tüüp** – valige, kas debiteerida pearaamatu kontot, klienti või müüjat.
- **Deebetkonto** – sisestage konto, kuhu deebetisumma sisestatakse tagasimakse sätete kehtestamisel.
- **Põhikonto** – valige mahakandmiste põhikonto.
