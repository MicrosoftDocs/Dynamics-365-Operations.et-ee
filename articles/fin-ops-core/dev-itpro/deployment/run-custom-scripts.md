---
title: Kohandatud X++ skriptide käitamine ilma katkestusteta
description: See artikkel kirjeldab, kuidas laadida üles ja käitada juurutatavaid pakette, mis sisaldavad kohandatud X++ skripte ilma süsteemi peatamiseta.
author: AndersGirke
ms.date: 12/16/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-12-16
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ff01e2ff8ec105603bb91e0b555301f36e8985b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867325"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Kohandatud X++ skriptide käitamine ilma katkestusteta

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

See funktsioon võimaldab teil üles laadida ja käitada juurutatavaid pakette, mis sisaldavad kohandatud X++ Microsoft Dynamics skripte ilma elutsükli teenuste (LCS) läbimata või süsteemi peatamiseta. Seega saate parandada väheolulisi andmete vasturääkivusi, ilma et see põhjustaks katkestavat mahaminekut.

X++ skripti kasutamise eelis väiksemate andmete vasturikkumise parandamiseks on see, et süsteem korrigeerib skripti käitamisel automaatselt kõik seotud tabelid. See lähenemine aitab tagada paranduse tervikluse ja aitab vähendada uute vasturääkivuste tutvustamise riski.

> [!IMPORTANT]
> See funktsioon on mõeldud ainult väheolude andmete vasturääkivuse parandamisele. Seda ei tohi kasutada järgmisel otstarbel ega mis tahes muul otstarbel:
>
> - Andmekogum
> - Skeemi muudatused
> - Andmete migratsioon või muud pikaajalised protsessid
> - Andmete parandamine, mida saab parandada muude vahendite kaudu, nt regulaarsed äriprotsessid, andmete ühtsuse tööriistad või muud iseteenindustööriistad
>
> See funktsioon võimaldab volitatud kasutajatel üksusi ja nende kirjeid otse muuta ilma nende üksustega seotud äriloogikat käivitamata. Need muudatused võivad põhjustada andmete terviklikkuse probleeme. Seetõttu võib teie organisatsioon nõuda kinnitust ja allkirjastamist sise- ja välisaudiitidelt (või teistelt võrdväärsetelt sidusgruppidelt) enne ja/või pärast skripti käivitamist. Vastavuse tagamiseks võivad mõnda omadusi mõjutavad muudatused olla ka välised aruanded (nt finantsaruanded) või esitada need valitsusasutusele. Teie organisatsioon vastutab ainuisikuliselt muudatuste eest, mis selle funktsiooni kaudu andmetes tehakse, nende muudatuste kinnitamise ja äramärkimise või avaldamise eest ning vastavuse eest kehtivate seadustega. Teie kannate kõiki selle funktsiooni kasutamise riskeid.

Kõik süsteemi üleslaaditud juurutatavad paketid läbivad kohustusliku töövoo. Ohutuspõhimõttena ja kohustuste jagamise kindlustamiseks ei ole kasutajal, kes lähetatava paketi üles laadib, seda töövoos etappide kaupa kinnitada. Teine kasutaja peab selle kinnitama. Kuid pärast paketi heaks kiitmist lubatakse kasutajal, kes paketi üles laadis, viia lõpule ülejäänud sammud.

Süsteem nõuab, et kõik juurutatavad paketid läbiks test käituse. Enne kui skriptil lubatakse tootmisandmeid käitada, peab kasutaja kinnitama, et väljund on õige, valides aktsepteeri **testlogi**. Kui väljaminek ei ole õige, peab kasutaja paki valides valides ebaõnnestunud pakendi **märgistama**. Sellisel juhul ei lubata skripti tootmisandmetel käitada.

Iga üleslaaditud pakett salvestatakse süsteemis ja see läbib määratletud sündmuste töövoo. Iga sündmuse puhul säilitab süsteem logi, mis sisaldab ajatempli ja sündmuse sooritanud isiku ID-d. Sel viisil tagab süsteem kontrolljälje olemasolu.

Nagu järgmine näide näitab, pakub süsteem üksikasju selle kohta, kuidas iga juurutatav pakett X++is käivitati ja milliseid üksusi puudutati.

![Skripti üksikasjade leht.](media/script-details.png "Skripti üksikasjade leht")

## <a name="assign-duties-to-users-to-control-access"></a>Kohustuste määramine kasutajatele juurdepääsu juhtimisele

See funktsioon tagab järgmised kohustused. Administraatorid saavad neid kohustusi kasutada funktsioonile juurdepääsu halduse abi saamiseks.

- **Kohandatud skriptide hooldamine** – see kohustus annab võimaluse laadida üles, katsetada, kontrollida ja käitada kohandatud X++ skripte keskkondades (\[kasutaja nõustumise UAT\] ja tootmise testimine).
- **Kohandatud skriptide kinnitamine** – see kohustus annab võimaluse kinnitada üleslaaditud kohandatud X++ skript. Kinnitamine on kohustuslik samm enne mis tahes skripti katsetada, kontrollida ja käivitada.

Selleks, et vähendada pahatahtliku tegevuse riski, peab iga skripti selgesõnaliselt kinnitanud kasutaja, kes selle üles laadis. Enne, kui saate seda funktsiooni teie organisatsioonis kasutada, peab administraator määrama eelnevad kohustused vähemalt kahele asjassepuutuvale ja väga usaldusväärsele kasutajale. Kuigi ühel kasutajal võivad olla mõlemad kohustused, ei saa ta siiski oma skripte kinnitada.

## <a name="create-a-deployable-package"></a>Juurutatava paketi loomine

Selle funktsiooni jaoks on vaja regulaarset juurutatavat paketti, mille saab luua Visual Studio. Juhiseid vt teemast [Juurutatavate mudelite pakendite loomine](../deployment/create-apply-deployable-package.md).

Juurutatav pakett peab sisaldama täpselt ühte käivitatavat X++ klassi. Teisisõnu peab sellel olema üks klass, mis sisaldab järgmise allkirjaga meetodit.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Põhimeetodi nimi peab olema väiketäht.

## <a name="code-example"></a>Koodi näide

Järgmine koodi näide näitab, kuidas juurutatavat pakendit saab strukturdada.

```xpp
class MyScriptClassForIssueXYZ
{
    public static void main(Args _args)
    {
        if (curExt() != 'DAT')
        {
            throw error("This script must run in the DAT company!");
        }

        ttsbegin;

        MyTable myTable;

        update_recordset myTable
            setting myField = 17
            where myTable.myReference == 'xyz';

        if (myTable.RowCount() != 1)
        {
            throw error("Not updating the expected row!");
        }

        info("Success");
  
        ttscommit;
    }

}
```

## <a name="best-practices"></a>Head tavad

Järgmine loend kirjeldab mõnda head tava skripti edukaks kirjutamiseks, rakendamiseks ja käivitamiseks. Loend ei ole ammendav ja seda tuleks käsitleda ainult juhistena.

- **Kirjuta** skripti lõppu eduteade. Sel viisil saate näha, et skript käivitati ilma eranditeta.
- **Lisage** kande ulatuse selgesõnaline käsitsemine.
- **Kasutage** olemasolevat äriloogikat, nt `update()` meetodeid, kuid **ärge** mööduge äriloogikast, kasutades `doUpdate()`, `doInsert()` ja meetodeid `doDelete()`. See lähenemine aitab tagada, et sõltuvaid andmeid käsitletakse õigesti. See vähendab märkimisväärselt ka edasiste andmete vasturääkivuse riski.
- **Kinnitage** ettevõtte sisu. See lähenemine seab skripti käitamisel tavalised vead. Näiteks on näha, kas skripti käitatakse vales ettevõttes.
- **Kas** kinnitage, et mõjutatud kirjete arv vastab teie ootustele. Selline lähenemine näitab, kas skripti ettevalmistamisel nihutati ootamatult andmeid süsteemis.
- **Kasutage** iga skripti jaoks kordumatuid klassinimesid (näiteks kui kaasate nimes viite tööüksusele). See lähenemine takistab skripti üleslaadimisel nime kaldkriipsu probleeme. Kui skripti uus iteratsioon on nõutav, andke sellele uus nimi.
- **Testige** esmalt kõiki mittetootmiskeskkonnas skripte. Kavandatud mõju ja soovimatute kõrvalefektide katse seotud andmetele. Veenduge, et kõiki äriprotsesse, mida see võib mõjutada, saab edukalt ja täielikult lõpule viia pärast.

## <a name="upload-and-run-a-deployable-package"></a>Juurutatava paketi üleslaadimine ja käitamine

Kasutage skripti üles- ja käivitamiseks järgmist protseduuri.

1. Minge oma finantside ja toimingute rakenduse süsteemihalduse perioodiliste **\> ülesannete andmebaasi \>\> kohandatud skriptide juurde**.
1. Valige nupp **Laadi üles**.
1. Valige juurutatav pakett, mille lõite selles artiklis varem kirjeldatud viisil. Teil palutakse määrata skripti eesmärk.
1. Skripti peab nüüd kinnitanud teine kasutaja, kes selle üles laadis. Kinnitaja peab läbima järgmised sammud.

    1. Minge süsteemihalduse **perioodilise andmebaasi \>\> kohandatud \> skriptide.**
    1. Valige kinnitamiseks skript ja seejärel **üksikasjad**.
    1. Valige tegevuspaani vahekaardil **Protsessi töövoog** grupis **Start (Käivita**) suvand Kinnita **või** Lükka **tagasi**. Kui valite **Kinnita**, märgitakse skript kui kinnitatud ja see on testimiseks lukus. Kui valite **Lükka** tagasi, on skript lukus. Mõlemal juhul logitakse sündmus ja skripti koopia säilitatakse süsteemis.

1. Skripti tuleb katsetada, et veenduda, kas see on mõeldud selleks, et teha seda. Tester võib olla sama mis üleslaadija või kinnitaja või kolmas kasutaja, kellel on vajalikud õigused. Katsetaja peab läbima järgmised sammud.

    1. Minge süsteemihalduse **perioodilise andmebaasi \>\> kohandatud \> skriptide.**
    1. Valige testitav skript ja seejärel **üksikasjad**.
    1. Tegevuspaani vahekaardil Protsessi **töövoog** grupis **Katse** valige suvand Käivita **test**. Skript käivitatakse ajutise kande sees, mille süsteem katkestab automaatselt, kogudes erinevaid logisid ja SQL-lauseid.
    1. Kui skript on töö lõpetanud, vaadake logid üle ja kontrollige, et tulemused vastavad teie ootustele. Järgige üht neist sammudest.

        - Kui olete katsetulemusega nõus, **·** **·** **valige** tegevuspaani vahekaardil Protsessi töövoog suvand Aktsepteeri testlogi, et skripti käivitada. Sündmustelogi näitab, et skripti on testitud ning see näitab, kes seda testis ja millal.
        - Kui te ei ole katsetulemusega rahul, valige tegevuspaani vahekaardil Protsessi töövoog grupis Lõpp suvand Jahmatav, **·** **·** **et** skript ei töötaks. Süsteem säilitab skripti koopia koos selle ajaloo logiga.

1. Kui olete kindel, et skript vastab teie ootustele, **·** **·** **valige** käivitamiseks tegevuspaani vahekaardil Töövoo protsess grupis Käivita. See käsk teeb sama asja nagu eelmine katse käitamine, kuid kanne toimub lõpus.
1. Kui skript on töö lõpetanud, kontrollige tulemust ja kinnitage, et skript toimis nii, nagu soovite. Järgige üht neist sammudest.

    - Kui olete tulemusega rahul, **valige tegevuspaani** **·** **vahekaardil Protsessi töövoog grupis** Lõpp lahendatud eesmärk. Sündmustelogi peegeldab asjaolu, et skript õnnestus, ja see näitab, kes skripti kontrollis ja millal. Skript on salvestatud, kuid on nüüd lukustatud ja seda ei saa uuesti käivitada.
    - Kui te ei ole tulemusega rahul, **valige** **·** **tegevuspaani** vahekaardil Protsessi töövoog grupis Lahendamata eesmärk. Sündmustelogi peegeldab asjaolu, et skript ei täitnud selle otstarvet, ja see näitab, kes skripti käivitas ja millal. Skript on salvestatud, kuid on nüüd lukustatud ja seda ei saa uuesti käivitada. Kuid süsteem ei võta skripti tegevust automaatselt tagasi. Teil võib olla vaja kirjutada, importida ja käitada uus skript, et tagasi võtta ebaõnnestunud skripti süsteemile mõju.

Teie valik viimases etapis määratleb skripti lõpliku oleku. Võite protsessi vajadusel korrata.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>Juurutatava paketi üleslaadimine ja käitamine LCS-i kaudu

Selle asemel, et juurutada oma juurutatav pakett finantside ja toimingute rakenduse kasutajaliidese kaudu, nagu kirjeldatud eelmises jaotises, saate selle LCS-i üles laadida ja kasutada selle juurutamiseks tavaprotseduuri. Lisateavet vt käsurealt [juurutatavate pakendite installimine](../deployment/install-deployable-package.md).

Kuigi lähenemisel on vähem piiranguid, pakub see vähem veakaitset. Lisaks, kuna see nõuab kõigi serverite taaskäivitamist, põhjustab see veidi downtime'i.
