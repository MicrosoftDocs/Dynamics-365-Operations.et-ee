---
title: Käivitage kohandatud X++ skriptid ilma seisakuteta
description: Selles teemas kirjeldatakse, kuidas üles laadida ja käitada juurutatavaid pakette, mis sisaldavad kohandatud X++ skripte ilma süsteemi peatamata.
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
ms.openlocfilehash: fcd0a472fa5116ca0b3a59561b6eeb72181a9113
ms.sourcegitcommit: 44e6875e974a3a1b3e1d7a24c1a3cff3d3697cdc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2022
ms.locfileid: "8088340"
---
# <a name="run-custom-x-scripts-with-zero-downtime"></a>Käivitage kohandatud X++ skriptid ilma seisakuteta

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

See funktsioon võimaldab teil üles laadida ja käivitada juurutatavaid pakette, mis sisaldavad kohandatud X++ skripte, ilma et peaksite läbima Microsoft Dynamics elutsükli teenuseid (LCS) või peatama süsteemi. Seetõttu saate parandada väiksemaid andmete vastuolusid, põhjustamata häirivaid seisakuid.

X++ skripti kasutamise eeliseks väiksemate andmekonsisestuste parandamiseks on see, et süsteem kohandab skripti käivitamisel automaatselt kõiki seotud tabeleid vastavalt vajadusele. Selline lähenemine aitab tagada korrektsiooni terviklikkuse ja aitab minimeerida uute vastuolude esilekuitamise ohtu.

> [!IMPORTANT]
> See funktsioon on mõeldud ainult väiksemate andmekontsernide korrigeerimiseks. Seda ei tohi kasutada järgmistel eesmärkidel ega muudel eesmärkidel:
>
> - Andmekogum
> - Skeemi muudatused
> - Andmemigreerimine või muud pikaajalised protsessid
> - Andmete parandamine, mida saab parandada muul viisil, näiteks regulaarsete äriprotsesside, andmete järjepidevuse tööriistade või muude iseteenindustööriistu abil
>
> Funktsioon võimaldab volitatud kasutajatel olemeid ja nende kirjeid otse muuta, ilma et peaksite käivitama nende olemitega seotud äriloogikat. Need muudatused võivad põhjustada andmete terviklikkuse probleeme. Seetõttu võib teie organisatsioon nõuda, et saaksite enne ja/või pärast skripti käivitamist sise- ja välisaudiitoritelt (või muudelt samaväärsetelt sidusrühmadelt) heakskiidu ja allkirja. Nõuetele vastavuse huvides võib olla vaja mõningaid omadusi mõjutavaid muudatusi avaldada ka välisaruannetes (nt finantsaruanded) või teatada valitsusasutustele. Teie organisatsioon vastutab ainuisikuliselt selle funktsiooni kaudu oma andmetes tehtud muudatuste, nende muudatuste kinnitamise ja allkirjastamise või avalikustamise ning kohaldatavate seaduste järgimise eest. Te kannate kõiki selle funktsiooni kasutamisega kaasnevaid riske.

Kõik süsteemi üles laaditud juurutatavad paketid läbivad kohustusliku töövoo. Ettevaatusabinõuna ja kohustuste eraldamise tagamiseks ei ole juurutatava paketi üleslaadijal lubatud seda töövoo järgmisteks etappideks kinnitada. Teine kasutaja peab selle heaks kiitma. Kuid pärast paketi kinnitamist lubatakse selle üles laadinud kasutajal ülejäänud etapid lõpule viia.

Süsteem nõuab, et kõik juurutatavad paketid läbivad testi. Enne kui skriptil lubatakse tootmisandmetel töötada, peab kasutaja kinnitama, et väljund on õige, valides suvandi **Aktsepteeri testlogi**. Kui väljund pole õige, peab kasutaja märkima paketi nurjunud, valides **Hülga**. Sellisel juhul ei lubata skripti tootmisandmetel töötada.

Iga üleslaaditud pakett salvestatakse süsteemi ja läbib sündmuste määratletud töövoo. Iga sündmuse puhul peab süsteem logi, mis sisaldab ajatemplit ja sündmuse läbiviija isikut. Sel viisil tagab süsteem kontrolljälje.

Nagu järgmisel joonisel on näha, sisaldab süsteem üksikasju selle kohta, kuidas iga juurutatavat paketti X++ käitati ja milliseid olemeid puudutati.

![Skripti üksikasjade leht.](media/script-details.png "Skripti üksikasjade leht")

## <a name="assign-duties-to-users-to-control-access"></a>Juurdepääsu juhtimiseks kasutajatele kohustuste määramine

See funktsioon pakub järgmisi ülesandeid. Administraatorid saavad neid ülesandeid kasutada funktsioonile juurdepääsu kontrollimiseks.

- **Kohandatud skriptide** haldamine – see tollimaks annab võimaluse kohandatud X++ skripte keskkondades üles laadida, testida, kontrollida ja käitada (kasutaja aktsepteerimise testimine \[UAT\] ja tootmine).
- **Kohandatud skriptide** kinnitamine – see kohustus annab võimaluse kinnitada üleslaaditud kohandatud X++ skript. Kinnitamine on kohustuslik samm enne, kui skripti saab testida, kontrollida ja käivitada.

Pahatahtliku tegevuse ohu minimeerimiseks peab iga skripti selgesõnaliselt heaks kiitma muu kasutaja kui selle üles laadinud kasutaja. Enne selle funktsiooni kasutamist oma asutuses peab administraator määrama eelnevad kohustused vähemalt kahele asjakohasele ja väga usaldusväärsele kasutajale. Kuigi ühel kasutajal võivad olla mõlemad kohustused, ei saa see kasutaja siiski oma skripte kinnitada.

## <a name="create-a-deployable-package"></a>Juurutatava paketi loomine

Funktsioon nõuab regulaarset juurutatavat paketti, mida saab luua .Visual Studio Juhised leiate teemast [Juurutatavate mudelite](../deployment/create-apply-deployable-package.md) pakettide loomine.

Juurutatav pakett peab sisaldama täpselt ühte käivitatavat X++ klassi. Teisisõnu peab sellel olema üks klass, mis sisaldab meetodit, millel on järgmine allkiri.

```xpp
public static void main(Args _args)
```

> [!NOTE]
> Põhimeetodi nimi peab olema väiketäht.

## <a name="code-example"></a>Koodi näide

Järgmine koodinäide näitab, kuidas juurutatavat paketti struktureerida.

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

Järgmises loendis kirjeldatakse mõningaid parimaid tavasid skripti edukaks kirjutamiseks, rakendamiseks ja käitamiseks. Nimekiri ei ole ammendav ja seda tuleks pidada ainult juhisteks.

- **Kirjutage** stsenaariumi lõppu edusõnum. Sel viisil näete, et skript töötas eranditult.
- **Lisage** kande ulatuse selgesõnaline käsitlemine.
- **Kasutage** olemasolevat äriloogikat (nt `update()` meetodeid), kuid **ärge** mööda äriloogikast, kasutades `doUpdate()`, `doInsert()` ja `doDelete()` meetodeid. Selline lähenemisviis aitab tagada sõltuvate andmete õige käitlemise. Samuti vähendab see märkimisväärselt andmetega seotud vastuolude ohtu.
- **Kas** kinnitada ettevõtte kontekstis. Selline lähenemine paljastab tavalised vead skripti ajal. Näiteks näitab see, kas skripti käitatakse vales ettevõttes.
- **Kinnita**, et mõjutatud kirjete arv vastab teie ootustele. Selline lähenemine näitab, kas andmed tähestiku ettevalmistamisel süsteemis ootamatult nihkusid.
- **Kasutage** iga skripti jaoks kordumatuid klassinimesid (näiteks lisades nimele viite tööüksusele). See lähenemine takistab skripti üleslaadimisel nime kokkupõrke probleeme. Kui on vaja skripti uut iteratsiooni, andke sellele kindlasti uus nimi.
- **Testige** kõigepealt iga skripti mittetootmiskeskkonnas. Kavandatud mõju ja tahtmatute kõrvaltoimete test seotud andmetele. Veenduge, et kõik äriprotsessid, mis võivad olla mõjutatud, on hiljem edukalt ja täielikult lõpule viidud.

## <a name="upload-and-run-a-deployable-package"></a>Juurutatava paketi üleslaadimine ja käivitamine

Skripti üleslaadimiseks ja käitamiseks kasutage järgmist toimingut.

1. Avage rakenduses Finance and Operations suvand **Süsteemihaldus \> Perioodilised tööülesanded \> Andmebaasi \> kohandatud skriptid**.
1. Valige nupp **Laadi üles**.
1. Valige juurutatav pakett, mille lõite, nagu selles teemas varem kirjeldatud. Teil palutakse määrata skripti eesmärk.
1. Skripti peab nüüd heaks kiitma muu kasutaja kui selle üles laadinud kasutaja. Kinnitaja peab järgima järgmisi juhiseid.

    1. **Avage süsteemi administreerimine \> Perioodiline \> andmebaasibaas \> Kohandatud skriptid**.
    1. Valige kinnitatav skript ja seejärel valige **Üksikasjad**.
    1. Tegevuspaanil **Protsessi töövoog** vahekaardil **Alusta** rühm, valige **Kinnita** või **Keeldu**. Kui valite **Kinnita**, märgitakse skript heakskiidetuks ja see avatakse testimiseks. Kui valite **Keeldu**, on skript lukus. Mõlemal juhul sündmus logitakse ja skripti koopiat hoitakse süsteemis.

1. Skripti tuleb testida, et veenduda, et see teeb seda, mida see on ette nähtud. Testija võib olla sama, mis üleslaadija või kinnitaja, või kolmas kasutaja, kellel on vajalikud õigused. Testija peab järgima järgmisi samme:

    1. **Avage süsteemi administreerimine \> Perioodiline \> andmebaasibaas \> Kohandatud skriptid**.
    1. Valige testitav skript ja seejärel valige **Üksikasjad**.
    1. Tegevuspaanil **Protsessi töövoog** vahekaardil **Test** rühm, valige **Käivitage test**. Skripti käivitatakse ajutise tehingu sees, mille süsteem katkestab erinevate logide ja SQL-lausete kogumise ajal automaatselt.
    1. Kui skript on töötamise lõpetanud, vaadake üle logid ja veenduge, et tulemused vastavad teie ootustele. Järgige üht neist sammudest.

        - Kui olete testi tulemusega rahul, valige **Aktsepteerige testlogi** aastal **Test** rühma peal **Protsessi töövoog** skripti käivitamiseks. Sündmuste logi kajastab skripti testimise fakti ning näitab, kes ja millal seda testis.
        - Kui te ei ole testi tulemusega rahul, valige **Loobu** aastal **Lõpp** rühma peal **Protsessi töövoog** toimingupaani vahekaarti, et takistada skripti käitamist. Süsteem säilitab skripti koopia koos selle ajaloo logiga.

1. Kui olete kindel, et skript vastab teie ootustele, valige **Jookse** aastal **Jookse** rühma peal **Protsessi töövoog** Selle käivitamiseks toimingupaani vahekaarti. See käsk teeb sama, mis eelmine testkäivitus, kuid tehing sooritatakse lõpus.
1. Kui skript on töötamise lõpetanud, kontrollige tulemust ja veenduge, et skript töötas soovitud viisil. Järgige üht neist sammudest.

    - Kui olete tulemusega rahul, valige **Eesmärk lahendatud** aastal **Lõpp** rühma peal **Protsessi töövoog** toimingupaani vahekaart. Sündmuste logi kajastab tõsiasja, et skript töötas edukalt, ja näitab, kes ja millal skripti kinnitas. Skript on salvestatud, kuid see on nüüd lukustatud ja seda ei saa uuesti käivitada.
    - Kui te ei ole tulemusega rahul, valige **Eesmärk lahendamata** aastal **Lõpp** rühma peal **Protsessi töövoog** toimingupaani vahekaart. Sündmuste logi kajastab tõsiasja, et skript ei täitnud ettenähtud eesmärki, ning näitab, kes ja millal skripti käivitas. Skript on salvestatud, kuid see on nüüd lukustatud ja seda ei saa uuesti käivitada. Süsteem ei võta aga skriptitoimingut automaatselt tagasi. Võimalik, et peate kirjutama, importima ja käivitama uue skripti, et tühistada ebaõnnestunud skripti mõju teie süsteemile.

Teie valik viimases etapis määrab skripti lõpliku oleku. Protsessi saate korrata vastavalt vajadusele.

## <a name="upload-and-run-a-deployable-package-through-lcs"></a>LCS-i kaudu juurutatava paketi üleslaadimine ja käivitamine

Selle asemel, et juurutada oma juurutatavat paketti oma Finance and Operationsi rakenduse kasutajaliidese kaudu, nagu on kirjeldatud eelmises jaotises, saate selle üles laadida LCS-i ja kasutada selle juurutamiseks tavapärast protseduuri. Lisateabe saamiseks vt [Installige juurutatavad paketid käsurealt](../deployment/install-deployable-package.md).

Kuigi sellel lähenemisviisil on vähem piiranguid, pakub see vähem vigade kaitset. Lisaks, kuna see nõuab kõigi serverite taaskäivitamist, põhjustab see mõningaid seisakuid.
