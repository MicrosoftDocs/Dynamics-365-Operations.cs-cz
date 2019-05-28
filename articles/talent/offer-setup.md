---
title: Nastavení správy nabídek
description: Toto téma popisuje, jak nastavit nabídky v aplikaci Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fa0e5d30c06db16e105631e492af022acfcfd66
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517513"
---
# <a name="set-up-offer-management"></a>Nastavení správy nabídek 

[!include [banner](includes/banner.md)]

Když je kandidát posunut do fáze nabídky v aplikaci Dynamics 365 for Talent: Attract, musíte zajistit, aby bylo možné nabídky kandidátům rychle vytvořit, schválit podle potřeby a zaslat kandidátovi. Vzhledem k tomu, že většina nabídek je standardní, lze je vytvořit z opětovně použitelných šablon. V aplikaci Attract budou všechny nabídky sbaleny do balíčku nabídky, což je kolekce jednoho nebo více dokumentů nabídky. 

Toto téma uvádí seznam všech kroků, které by měl správce aplikace Attract provést pro nastavení různých šablon balíčku nabídky jako součást funkce správy nabídky v aplikaci Attract. Uživatelé bez role správce nemají přístup k těmto funkcím.

>[!NOTE]
> Funkce správy nabídky jsou k dispozici jako součást doplňku komplexního náboru.

## <a name="offer-data"></a>Data nabídky 

Data nabídky jsou nejmenší jednotkou uvnitř šablony balíčku nabídky. Typická nabídka se skládá ze standardního textu a sady hodnot. Sady hodnot jsou pouze kusy, které se mohou změnit mezi nabídkami. Během vytváření nabídky je nejdůležitějším aspektem, na který se tvůrce nabídky může zaměřit, seznam zástupných textů dat nabídky v šabloně balíčku nabídky. Pro nastavení dat nabídky postupujte takto.

1.  Přejděte na možnost **Správa nabídky**.

1.  Rozbalte část **Knihovna** v levém navigačním podokně a pak přejděte na **Data nabídky**.

    >[!NOTE]
    > Na stránce **Data nabídky** jsou části **Podrobnosti o kandidátovi** a **Podrobnosti o práci**. Attract poskytuje několik vestavěných zástupných textů pro data nabídky.
    
    > Existují části na stránce pro uspořádání různých zástupných textů dat nabídky do logických skupin. Tyto části mohou pomoci s údržbou dat nabídky a naplňováním dat během procesu vytváření nabídky.

1.  Chcete-li vytvořit novou část dat nabídky, klikněte na **Přidat sekci** a zadejte jedinečný název pro sekci.

1.  Chcete-li přidat zástupné texty dat nabídky pro jakoukoliv část, klikněte na **Přidat data nabídky** a zadejte jedinečný název pro zástupný text.

1.  Chcete-li upravit název jakékoliv části, podržte ukazatel myši nad názvem části a aktualizujte název.

1.  Chcete-li upravit název jakéhokoliv existujícího zástupného textu dat nabídky, nejprve se ujistěte, zda zástupný text již není součástí nějaké šablony. Potom ukazatelem myši najeďte nad název zástupného textu dat nabídky a aktualizujte název podle potřeby.

1. Chcete-li odstranit existující zástupný text dat nabídky, nejprve se ujistěte, zda zástupný text není součástí jiné šablony. Potom ukazatelem myši najeďte nad zástupný text a když se objeví ikona koše, klikněte na koš pro odstranění zástupného textu dat nabídky.
    >[!NOTE]
    > Můžete vidět, kolika šablon je zástupný text dat nabídky součástí podle číselného ukazatele vedle každých dat nabídky. 

1. Chcete-li odstranit jakoukoliv část, najeďte myší nad název. Pokud se v žádné šabloně neobjeví žádný zástupný text dat nabídky v části, můžete ho smazat kliknutím na ikonu koše. 
    >[!NOTE]
    > Odstraněním části budou také odstraněny všechny zástupné texty dat nabídky v rámci této části.

Jakmile byly nastaveny zástupné texty dat nabídky, můžete je použít v jakékoli šabloně dokumentu Zástupné texty dat nabídky nejsou omezeny na určitou šablonu - stejnou sadu lze použít ve všech šablonách.

## <a name="offer-data-rules"></a>Pravidla dat nabídky

Většina organizací má pravidla pro vytváření nabídek. Například organizace může požadovat, aby maximální roční mzdová nabídka pro konkrétní kombinaci místa a úrovně služebního věku byla v určitém rozsahu, nebo aby existovalo jen několik konkrétních hodnot možných pro úroveň nabídky pro nově přijatého zaměstnance. Attract aktuálně podporuje všechna taková pravidla dat pomocí souboru CSV.

Chcete-li připravit CSV soubor pravidel dat, postupujte takto.

1.  Určete zástupný text dat nabídky pro sadu pravidel. Například **Roční mzda**.

1.  Určete závislé hodnoty zástupného textu dat nabídky. Například **Místo výkonu práce** a **Úroveň**.

1.  Určete sloupce 1 a 2 jako **Místo výkonu práce** a **Úroveň**.

1.  Chcete-li načíst hodnotu rozsahu, udělejte ze sloupců 3 a 4 **roční mzdu**. Chcete-li načíst konkrétní hodnotu místo rozsahu , udělejte **roční mzdu** pouze ze sloupce 3.

1.  Naplňte soubor aplikace Microsoft Excel na základě vašich požadovaných rolí.

1.  Ujistěte se, že každý řádek je jedinečnou kombinací všech hodnot spojených dohromady.

1.  Uložte soubor jako CSV formát.

Chcete-li odeslat soubor pravidel dat nabídky, postupujte takto.

1.  Přejděte na možnost **Správa nabídky**.

1.  Rozbalte část **Knihovna** v levém navigačním podokně a pak přejděte na **Pravidla dat nabídky**.

1.  Klikněte na možnost **Nová sada dat** a zobrazte dialogové okno **Odeslat**.

1.  Zadejte jedinečný název pro sadu pravidel a poté odešlete uložený soubor CSV.

1.  Klikněte na položku **Přidat**.
    Sada pravidel bude zpracována na pozadí a po dokončení budete upozorněni v aplikaci a e-mailem.

    Budete upozorněni, pokud dojde k chybám při zpracování odeslání. Můžete poté stáhnout protokol chyb, opravit soubor a odeslat ho znovu.

1.  Klikněte na tlačítko s třemi tečkami (**...**), pokud chcete stáhnout sadu pravidel a odeslat sadu hodnot. Po aktualizaci můžete odeslat soubor znovu.

1.  Pokud se definovaný zástupný text nepoužívá v jiné šabloně dokumentu, můžete odstranit stávající odeslání sady pravidel.

>[!NOTE]
> - Každý zástupný text může mít pouze jednu jedinečnou sadu sloupců, na které je závislý. Například pokud je **Roční mzda** závislá na **místu výkonu práce** a **úrovni**, nelze odeslat jinou sadu pravidel, kde **roční mzda** závisí na odlišné sadě sloupců.

> - Můžete stáhnout vzorové sady pravidel dat nabídky na kartě **Ukázky** na stránce **Pravidla dat nabídky**.

> - Když tvůrce nabídky přepíše hodnoty, které jsou doporučeny pravidly dat nabídky, nabídka je označena jako nestandardní a workflow schvalování nabídek bude nařízeno.

## <a name="document-templates"></a>Šablony dokumentů

Šablona dokumentu s nabídkou může pomoct správcům s vytvářením dopisů s nabídkou. Šablona dokumentu s nabídkou je kombinací textu, který bude součástí nabídky, a definovaných zástupných textů dat nabídky. 

Chcete-li vytvořit šablonu dokumentu nabídky, postupujte takto.

1.  Přejděte na možnost **Správa nabídky**.

1.  Rozbalte část **Knihovna** v levém navigačním podokně a přejděte na **Šablony**.

    Stránka **Šablony** zobrazí seznam šablon dokumentů, které již byly definovány.

1.  Chcete-li vytvořit novou šablonu dokumentu, klikněte na **Nová šablona**.

1.  Zadejte jedinečný název pro šablonu a klikněte na **Vytvořit**.

1.  Použijte editoru formátovaného textu nebo upravte obsah dokumentu nabídky. Můžete vložit tabulky, obrázky a hypertextové odkazy pomocí možností dostupných v horní části textového editoru.

1.  Do dokumentu šablony nabídky můžete vložit zástupné texty dat nabídky pomocí:

    - Přetažením z pravého podokna.

    - Použitím hashtagu k zástupnému textu dat nabídky přímo na pozici. Napište **\#** a poté začněte psát název zástupného textu dat nabídky. Možnosti se zobrazí v rozevíracím seznamu. Klikněte nebo stiskněte **Enter** pro vložení zástupného textu dat nabídky.

    >[!NOTE]
    > - Chcete-li přidružit zástupný text do šablony dokumentu nabídky, aniž byste odkryli jeho hodnotu kandidátovi, najeďte myší nad zástupný text dat nabídky a klikněte na ikonu **špendlíku**. To posune zástupný text do části **Připnutá data nabídky** šablony dokumentu nabídky. Pro odepnutí postupujte podle stejných kroků, ale v seznamu zástupných textů dat nabídky klikněte na **Odepnout**.

    > - Chcete-li zobrazit seznam aktivních zástupných textů dat nabídky, přepněte na kartu **Aktivní** v pravém podokně.

    > - Pokud vložíte zástupný text, který je řízen sadou pravidel dat nabídky, zobrazí se závislost tohoto zástupného textu dat nabídky na jiných hodnotách.

    > - Popřípadě můžete **importovat** obsah ze souboru DOCX na svůj místní počítač a podle potřeby ho upravit. Tímto způsobem nemusíte zadávat veškerý obsah v editoru.

1. Chcete-li zobrazit náhled dokumentu nabídky, použijte možnost **Náhled** v horní části stránky.

1. Chcete-li kontrolovat, zda tvůrce nabídky může upravovat obsah dokumentu s nabídkou, použijte možnost **Spravovat oprávnění** v horní části stránky. Pokud chcete, aby mohl tvůrce nabídky pouze vkládat zástupné texty, nikoliv upravovat text, nastavte hodnotu oprávnění na **Ne**.

1. Kliknutím na tlačítko **Uložit** uložte svůj průběh. Šablona bude uložena ve stavu konceptu.

1. Chcete-li dokončit a označit dokument jako zveřejněný, klikněte na **Dokončit**.

1. Můžete zobrazit, které šablony dokumentu jsou momentálně aktivní, v režimu konceptu a archivované a již nepoužívané v cílovém rozhraní knihovny šablon dokumentů.

>[!NOTE]
> Můžete odstranit všechny šablony dokumentu s nabídkou, které nejsou součástí stávající šablony balíčku nabídky.


## <a name="offer-package-templates"></a>Šablony balíčku nabídky

Balíčky nabídky jsou artefakty nabídky, které jsou sdíleny s kandidáty a které se skládají z kombinace jedné nebo více šablon dokumentů s nabídkou. Chcete-li vytvořit balíček, postupujte takto.

1.  Přejděte na možnost **Správa nabídky**.

1.  Přejděte na **Balíčky** z levého navigačního podokna.

    Zobrazí se seznam aktivních šablon balíčků, které jsou k dispozici k použití pro tvůrce nabídky.

1.  Chcete-li vytvořit nová balíček s nabídkou, klikněte na **Nový balíček**.

1.  Zadejte jedinečný název a klikněte na **Vytvořit**.

1.  Klikněte na možnost **Přidat šablonu**.

    >[!NOTE]
    > - Můžete zvolit vytvoření nové šablony nebo si vybrat jednu z již existujících šablon.

    > - Pokud si zvolíte přidání existující šablony, musíte se ujistit, že šablona dokumentu nabídky byla uložena, dokončena a označena jako aktivní.
    
    > - Můžete si vybrat tolik šablon dokumentu, kolik chcete. 
    
1.  Klikněte na **Hotovo** pro návrat na položku **Správa balíčku**.

    Můžete konfigurovat posloupnost dokumentů a také označit, zda je při vytváření nabídky požadován konkrétní dokument nabídky. Tvůrce nabídky bude mít možnost odstranit dokumenty označené jako **Nevyžadované**.

1. Chcete-li uložit šablonu balíčku nabídky, aby byla použitelná pro všechny tvůrce nabídky, klikněte na tlačítko **Uložit a publikovat**.

   Chcete-li zobrazit koncepty šablon balíčku nabídky, přejděte na kartu **Koncepty**. Pokud je provedena změna šablony balíčku nabídky, musí být uložena a znovu publikována.

## <a name="configure-an-offer-process"></a>Konfigurace procesu nabídky

Existuje několik částí procesu vytváření nabídky, které může konfigurovat správce aplikace Attract.

- **Schválení nabídky** – Zvolte, zda jsou schválení nabídky požadována předtím, než může být nabídka odeslána kandidátovi. Jako správce můžete také rozhodnout, zda ke všem schválením nabídky dojde ve workflow postupného nebo souběžného schvalování. Můžete také přikázat, zda musí schvalovatelé nabídky přidat komentář ke svému schválení nabídky. Schválení nabídky jsou povinná pro všechny nestandardní nabídky.

- **Vypršení nabídky kandidátovi** -Jako správce můžete určit, zda mají všechny nabídky datum vypršení platnosti, a pokud ano, jaký by mě být výchozí posun pro datum vypršení platnosti. Můžete také nastavit, zda kandidáti mohou odmítnout nabídku.

- **Elektronické podpisy** -jako správce můžete také zvolit metodu, kterou mohou uchazeči používat k podepisování nabídek.
    - Adobe Sign - všechny nabídky budou odeslány a podepisovány pomocí Adobe Sign. Každý autor nabídky, který ji publikuje, musí mít připojený účet Adobe Sign k aplikaci Attract. Ohledně licencí Adobe Sign a bezplatných zkušebních verzí navštivte tento [odkaz](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

    - DocuSign - všechny nabídky budou odeslány a podepisovány pomocí DocuSign. Každý autor nabídky, který ji publikuje, musí mít připojený účet DocuSign k aplikaci Attract. 
    
    - ESign – Toto je výchozí možnost poskytovaná přímo po vybalení, kde může uživatel podepsat nabídku zadáním svého jména a iniciál.


Další informace o procesu vytváření nabídky naleznete v tématu [Vytvoření, schválení a podepisování nabídek](./creating-offers.md).
