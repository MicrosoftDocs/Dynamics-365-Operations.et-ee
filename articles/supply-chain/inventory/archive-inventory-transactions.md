---
title: Laokannete arhiivimine
description: See artikkel kirjeldab, kuidas arhiveerida laokannete andmeid süsteemi jõudluse parandamiseks.
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c63cdee862e2e22649a3eb58ae37597741770e14
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874097"
---
# <a name="archive-inventory-transactions"></a>Laokannete arhiivimine

[!include [banner](../../includes/banner.md)]

Laokannete tabel (`InventTrans`) kasvab aja jooksul pidevalt ja kasutab aina rohkem andmebaasiruumi. Seetõttu muutuvad tabeli kohta tehtud päringud järk-järgult aeglasemaks. See artikkel kirjeldab, kuidas te saate kasutada laokannete *arhiivi* funktsiooni laokannete andmete arhiveerimiseks, et parandada süsteemi jõudlust.

> [!NOTE]
> Valitud suletud pearaamatu perioodi jooksul saab arhiveerida ainult finantsiliselt värskendatud laokandeid. Arhiivimiseks peavad finantsiliselt uuendatud väljaminevate laokannete väljamineku olek olema *Müüdud* ja sissetulevate laokannete sissetuleku olek peab olema *Ostetud*.

Laokannete arhiivimisel teisaldatakse kõik seonduvad kanded tabelisse `InventTransArchive`. Lao väljaminekukanded ja lao sissetulekukanded arhiveeritakse eraldi kauba ID (`itemId`) ja laodimensiooni ID (`inventDimId`) kombinatsiooni alusel ning pannakse summeeritud väljamineku ja summeeritud sissetuleku kannete hulka.

Kui üks `itemId` ja `inventDimId` kombinatsioon sisaldab ainult ühte sissetuleku- või väljaminekukannet, siis kannet ei arhiivita.

## <a name="turn-on-the-feature-in-your-system"></a>Funktsiooni sisselülitamine teie süsteemis

Kui teie süsteem ei kaasa juba selles artiklis kirjeldatud funktsioone, [minge](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsioonihaldusesse ja lülitage sisse laokannete *arhiivi* funktsioon. Pange tähele, et seda funktsiooni ei saa pärast lubamist enam keelata.

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>Mida on vaja enne laokannete arhiivimist arvesse võtta

Enne laokannete arhiivimist peaksite arvestama järgmiste äristsenaariumiga, sest see toiming mõjutab neid:

- Kui auditeerite laokandeid seonduvatest dokumentidest, nt ostutellimuse ridadest, kuvatakse need arhiivitud kannetena. Arhiveeritud kannete ülevaatamiseks peate avama kausta **Laovarude haldus \> Perioodilised ülesanded \> Puhastamine \> Laokannete arhiiv**.
- Lao sulgemist ei saa arhiivitud perioodide puhul tühistada. Enne, kui saate lao sulgemise tühistada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.
- Standardkulu teisendamist ei saa arhiivitud perioodideks teha. Enne, kui saate standardkulu teisendada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.
- Laokannete arhiivimine mõjutab laokannetest hangitud laoaruandeid. Need aruanded sisaldavad laovarude ajalise jaotuse aruannet ja laovarude väärtuse aruandeid.
- Laovarude prognoose võib mõjutada nende käitamine arhiveeritud perioodide perioodi jooksul.

## <a name="prerequisites"></a>Eeltingimused

Laokandeid saab arhiveerida ainult neil perioodidel, mille puhul on täidetud järgmised tingimused:

- Pearaamatu periood peab olema suletud.
- Lao sulgemine peab olema käitatud arhiivi perioodi lõppkuupäeval või pärast seda.
- Periood peab olema vähemalt üks aasta enne arhiivi perioodi alguskuupäeva.
- Varude ümberarvutusi ei tohi olla.

## <a name="archive-inventory-transactions"></a>Laokannete arhiivimine

Laokannete arhiivimiseks toimige järgmiselt.

1. Avage kaust **Varude haldus** \> **Perioodilised ülesanded** \> **Puhastamine** \> **Laokannete arhiiv**.

    Kuvatakse leht **Laokannete arhiiv** ja sellel kuvatakse arhiivitud protsessikirjete loend.

    ![Laokannete arhiivi leht.](media/archive-inventory-empty.png "Laokannete arhiivi leht")

1. Valige tegevuspaanil laokannete arhiivi loomiseks **Laokannete arhiiv**.
1. Seadke dialoogiboksis **Laokannete arhiiv** kiirkaardil **Parameetrid** järgmised väljad:

    - **Suletud pearaamatu perioodi alguskuupäev** – valige varaseim kande kuupäev arhiivi kaasamiseks.
    - **Suletud pearaamatu perioodi lõppkuupäev** – valige hiliseim kande kuupäev arhiivi kaasamiseks.

    ![Laokannete arhiivi dialoogiboks.](media/archive-inventory-dates.png "Laokannete arhiivi dialoogiboks")

    > [!NOTE]
    > Valida saab ainult [eeltingimustele](#prerequisites) vastavad perioodid.

1. Seadistage kiirkaardil **Käivita taustal** pakett-töötluse üksikasjad vastavalt vajadusele. Järgige teenuse Microsoft Dynamics 365 Supply Chain Management tavalisi pakett-tööde etappe.
1. Valige nupp **OK**.
1. Saate teate, mis palub teil kinnitada, et soovite jätkata. Lugege teade hoolikalt läbi ja valige vastus **Jah**, kui soovite jätkata.

    Saate teate, et teie laokannete arhiivitöö on lisatud pakett-töötluse järjekorda. Töö alustab nüüd valitud perioodi laokannete arhiivimist.

## <a name="view-archived-inventory-transactions"></a>Kuva arhiivitud varude kanded

Lehel **Laokannete arhiiv** kuvatakse teie täielik arhiivimisajalugu. Igal ruudustiku real kuvatakse selline teave nagu arhiivi loomise kuupäev, arhiivi loonud kasutaja ja selle olek.

![Arhiivimisajalugu lehel Laokannete arhiivimine.](media/archive-inventory-full.png "Arhiivimisajalugu lehel Laokannete arhiivimine")

Valige ruudustikus kuvatavate arhiivide filtreerimiseks lehe ülaosas asuvast ripploendist üks järgmistest väärtustest:

- **Aktiivne** – kuvatakse ainult aktiivsed arhiivid, mitte tagasipööratud arhiivid.
- **Kõik** – kuvatakse kõik arhiivid, nii aktiivsed kui ka tagasipööratud.

Iga arhiivi kohta ruudustikus esitatakse järgmine teave:

- **Aktiivne** – märge näitab, et arhiiv on aktiivne.
- **Alguskuupäev** – vanima kande kuupäev, mille saab arhiivi kaasata.
- **Lõppkuupäev** – uusima kande kuupäev, mille saab arhiivi kaasata.
- **Planeerija** – arhiivi loonud kasutajakonto.
- **Teostatud** – arhiivi loomise kuupäev.
- **Tagasipööratud** – märge näitab, et arhiiv on tagasi pööratud.
- **Peata praegune uuendus** – märge näitab, et arhiivimine on pooleli, kuid see on peatatud.
- **Olek** – arhiivi töötlemise olek. Võimalikud väärtused on *Ootel*, *Pooleli* ja *Lõpetatud*.

Ruudustiku kohal tööriistaribal on järgmised nupud, mida saate kasutada valitud arhiiviga töötamiseks:

- **Arhiivitud kanded** – saate vaadata valitud arhiivi kõiki üksikasju. Ilmuval lehel **Arhiivitud kanded** kuvatakse kõik arhiivis olevad kanded.

    ![Leht Arhiivitud kanded.](media/archive-inventory-transactions.png "Leht Arhiivitud kanded")

    Konkreetse kande kohta lisateabe vaatamiseks lehel **Arhiveeritud kanded** valige see ruudustikus ja seejärel valige tegevuspaanil **Arhiivitud kande üksikasjad**. Ilmuval lehel **Arhiivitud kande üksikasjad** kuvatakse selline teave nagu pearaamatu sisestamine, seotud alammooduli viited ja finantsdimensioonid.

- **Peata arhiivimine** – saate peatada praegu töödeldava valitud arhiivi. Peatamine jõustub alles pärast arhiivimisülesande loomist. Seega võib peatamise jõustumine toimuda viivitusega. Kui arhiiv on peatatud, kuvatakse väljal **Peata praegune uuendus** märge.
- **Jätka arhiivimist** – saate jätkata praegu peatatud valitud arhiivi töötlemist.
- **Pööra tagasi** – saate valitud arhiivi tagasi pöörata. Arhiivi saate tagasi pöörata ainult siis, kui selle välja **Olek** väärtuseks on seatud *Lõpetatud*. Kui arhiiv on tagasi pööratud, kuvatakse väljal **Tagasipööratud** märge.

## <a name="extend-your-code-to-support-custom-fields"></a>Koodi laiendamine kohandatud väljade toetamiseks

Kui tabel `InventTrans` sisaldab ühte või mitut kohandatud välja, peate võib-olla koodi nende toetamiseks laiendama, sõltuvalt nende nimest.

- Kui tabeli kohandatud väljadel `InventTrans` on samad välja nimed `InventtransArchive`, mis tabelis, tähendab see, et need on vastendatud 1:1. Seetõttu saate kohandatud väljad lihtsalt tabeli `InventoryArchiveFields` väljagruppi `inventTrans` panna.
- Kui tabeli kohandatud väljade `InventTrans` nimed ei ühti `InventtransArchive` tabeli väljanimedega, peate nende vastendamiseks lisama koodi. Näiteks kui `InventTrans.CreatedDateTime` teil on süsteemiväli kutsutud, `InventTransArchive` peate looma tabelis välja teise nimega (`InventtransArchive.InventTransCreatedDateTime` nt) ja lisama laiendeid klassidele, nagu näidatud järgmises näidiskoodis `InventTransArchiveProcessTask``InventTransArchiveSqlStatementHelper`.

Järgmine näidiskood näitab näidet, kuidas lisada klassile nõutav `InventTransArchiveProcessTask` laiend.

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

Järgmine näidiskood näitab näidet, kuidas lisada klassile nõutav `InventTransArchiveSqlStatementHelper` laiend.

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
