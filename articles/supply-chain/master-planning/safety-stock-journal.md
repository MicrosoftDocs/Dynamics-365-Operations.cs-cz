---
title: Použití deníku pojistných zásob pro aktualizaci minimální disponibility položek
description: Toto téma popisuje, jak používat deník pojistných zásob k aktualizaci množství pojistných zásob pro položky výpočtem návrhů minimální disponibility na základě historických transakcí.
author: t-benebo
ms.date: 10/28/2021
ms.topic: article
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, ReqItemTableSetup, ReqItemTable, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-28
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 391f741ee08eb0624e80f5c297009c527e50c14c
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468531"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage-for-items"></a>Použití deníku pojistných zásob pro aktualizaci minimální disponibility položek

[!include [banner](../../includes/banner.md)]

Pojistné zásoby označují dodatečné množství položky uložené ve skladu za účelem snížení rizika, že položka nebude na skladě. Pojistné zásoby se používají jako vyrovnávací v případě příchozích prodejních objednávek, kdy dodavatel nemůže splnit požadované datum expedice odběrateli.

Toto téma popisuje způsob použití deníku pojistných zásob k výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů.

## <a name="overview-of-minimum-coverage-usage"></a>Přehled využití minimální disponibility

Pojistná zásoba je zřízena na stránce **Disponibilita položky** pro každou položku. Různé typy doplnění jsou reprezentovány různými kódy disponibility. (Další informace viz téma [Splnění rezervních zásob položek](safety-stock-replenishment.md) .) Všechny kódy disponibility však používají hodnotu, která je nastavena v poli **Minimum** na stránce **Disponibilita položky** pro každou položku. Pole **Minimum** se dá využít dvě základními způsoby:

- **Minimální množství pro účely min/max** – Tento přístup používá minimální množství spolu s logikou min/max. Platí, když je pole **Kód disponibility** nastaveno na *Min/Max* pro příslušnou položku nebo skupinu disponibility. Množství **Minium** představuje průměrné denní využití vynásobené dobou realizace položky.
- **Minimální množství pro účely plánu zásob** – Tento přístup využívá minimální množství k reprezentaci plánu zásob v kombinaci s prognózami poptávky. Platí, když je pole **Kód disponibility** nastaveno na *Období* nebo *Požadavek* pro příslušnou položku nebo skupinu disponibility. Množství **Minimum** představuje plán zásob, který odráží požadovanou úroveň zákaznických služeb, aby pomohl snížit zásoby, částečné dodávky a dodací lhůty. Minimální množství odráží procento přesnosti prognózy pro danou položku. Nepředstavuje požadovanou pozici zásob.

Hodnotu **Minimum** lze nastavit třemi způsoby:

- Ručně na stránce **Disponibilita položky**
- Prostřednictvím architektury Správa dat (datové entity *Disponibilita položky*)
- Výpočtem pojistné zásoby, který se provádí pomocí deníků pojistných zásob

## <a name="calculate-minimum-coverage-based-on-historical-usage"></a>Vypočítejte minimální disponibilitu na základě historického použití

Deníky pojistných zásob se používají k výpočtu navrhovaného minimálního množství na základě historického použití položky, a to buď pro účely min/max nebo pro účely plánu zásob. Historické použití představuje všechny výdajové transakce během zadaného období. Tyto výdajové transakce zahrnují transakce prodejních objednávek a úpravy zásob. Výpočty také identifikují vliv navrženého minimálního množství na hodnotu zásob a změnu hodnoty zásob oproti současným minimálním množstvím.

Každý řádek deníku pojistných zásob představuje položku a její dimenze disponibility. Tyto řádky deníku jsou vytvořeny a zobrazeny na stránce **Řádky deníku pojistných zásob** (**Hlavní plánování \>Hlavní plánování \> Spustit \>Výpočet pojistné zásoby**). Obchodní proces pro použití deníků pojistných zásob k výpočtu navrhovaných minimálních množství je popsán dále v tomto tématu.

Plánovač používá deník pojistných zásob k výpočtu navrhovaných minimálních množství pro vybrané položky na základě historického použití během vybraných období. Navrhovaná minima lze podle potřeby ručně přepsat a potenciální dopad navrhovaných minim na hodnotu zásob můžete zkontrolovat. Když je deník zaúčtován, automaticky se aktualizují související minimální množství v disponibilitě položky.

### <a name="create-a-new-safety-stock-journal-name"></a>Vytvoření názvu nového deníku pojistných zásob

Než budete moci vygenerovat tento typ deníku, musíte vytvořit alespoň jeden název deníku pojistných zásob. Obvykle můžete použít několik názvů deníků, které vám pomohou oddělit výpočty vašich pojistných zásob.

1. Přejděte do nabídky **Hlavní plánování \> Nastavení \> Názvy deníků pojistných zásob**.
1. V podokně akcí zvolte **Nový**.
1. Na novém řádku nastavte následující pole:

    - **Název** – Zadejte krátký název deníku.
    - **Popis** – Zadejte popis deníku.
    - **Patří skupině uživatelů** – Chcete-li omezit cílovou skupinu pro název aktuálního deníku, vyberte skupinu uživatelů.
    - **Odstranit řádky po zaúčtování** – Zaškrtněte toto políčko, chcete-li ve výchozím nastavení vyčistit řádky deníku při jejich zaúčtování. Políčko vypněte, chcete-li zachovat všechny zaúčtované řádky.

    Pole **Typ deníku** je pouze ke čtení a je přednastaveno na *Pojistná zásoba*.

1. Zavřete stránku.

### <a name="create-a-safety-stock-journal-and-lines"></a>Vytvoření deníku pojistných zásob a řádků

Tento krok vytvoří deník a automaticky do něj přidá řádky. Každý řádek identifikuje položku, její dimenze disponibility a několik vypočtených množství z historie použití. Vypočítaná množství zahrnují průměrný počet výdejů na dobu realizace položky, průměrný počet výdejů za měsíc a měsíční směrodatnou odchylku.

#### <a name="automatically-generate-journal-lines"></a>Automatické generování řádků deníku

Řádky deníku lze automaticky generovat pouze v případě, že v aktuálně zobrazeném deníku neexistují žádné řádky.

Chcete-li automaticky generovat řádky deníku, postupujte podle těchto kroků.

1. Přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> Spustit \> Výpočet pojistných zásob**.
1. V podokně akcí zvolte **Nový**. Vytvoří se nový deník pojistných zásob.
1. Na záložce s náhledem **Podrobnosti záhlaví deníku** zadejte následující pole:

    - **Název** – Vyberte název deníku pojistných zásob, do kterého chcete přidat řádek.
    - **Popis** – Výchozí hodnota je popis názvu deníku, který jste vybrali. Hodnotu v tomto poli však můžete podle potřeby upravit.
    - **Odstranit řádky po zaúčtování** – Zaškrtněte toto políčko, chcete-li vyčistit řádky deníku při jejich zaúčtování. Políčko vypněte, chcete-li zachovat všechny zaúčtované řádky. Nastavení je zděděno z názvu vybraného deníku.

    Pole **Deník** je pouze ke čtení a zobrazuje číslo ID deníku, který vytváříte a do kterého přidáváte řádky.

1. Na záložce s náhledem **Řádky deníku** vyberte na panelu nástrojů příkaz **Vytvořit řádky**.
1. V dialogu **Vytvořit řádky deníku pro navrhované úrovně skladového minima** nastavte následující pole:

    - **Od data** – Vyberte počáteční datum období, pro které mají být výdeje zahrnuty do výpočtu.
    - **Do data** – Vyberte koncové datum období, pro které mají být výdeje zahrnuty do tohoto výpočtu. Mezi datem zahájení a ukončení musejí uplynout alespoň dva měsíce.
    - **Vypočítat směrodatnou odchylku** – Nastavte tuto možnost na *Ano*, chcete-li vypočítat směrodatnou odchylku. Tuto možnost musíte nastavit na *Ano*, když chcete použít možnost **Použít úroveň služeb** při výpočtu návrhu (jak je popsáno dále v tomto tématu).

1. Na záložce s náhledem **Záznamy, které mají být zahrnuty** můžete nastavit filtry a omezení, která definují, jaké položky budou zahrnuty. (Můžete například filtrovat podle hodnoty **Skupina disponibility**.) Výběrem položky **Filtr** otevřete standardní dialogové okno editoru dotazů, kde můžete definovat kritéria výběru, kritéria řazení a spojení. Pole fungují stejně jako u jiných typů dotazů v Microsoft Dynamics 365 Supply Chain Management.
1. Na záložce s náhledem **Spustit na pozadí** zvolte, zda má úloha běžet v dávkovém režimu a/nebo nastavte opakující se rozvrh. Pole fungují stejně jako u jiných typů [prací na pozadí](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Vyberte **OK**. Řádky se vytvoří pro dimenze, které obsahují skladové transakce.

#### <a name="manually-add-or-remove-journal-lines"></a>Ruční přidání nebo odebrání řádků deníku

Řádky deníku můžete kdykoli ručně přidat anebo odebrat (buď po nebo místo automatického generování řádků). Použijte následující tlačítka na panelu nástrojů záložky s náhledem **Řádky deníku**:

- **Nový** – Přidá nový řádek. Poté zadejte hodnotu do každého sloupce, abyste definovali produkt, který se má vypočítat, a na který použijete nová minima. Protože navrhované výpočty minimálních hodnot nejsou k dispozici u ručně přidaných řádků, není pro ně zobrazeno žádné **Vypočítané minimální množství**. Proto musíte ručně zadat hodnoty **Nové minimální množství**. Stále však můžete zobrazit potenciální dopad hodnoty **Nové minimální množství** na hodnotu zásob a potenciální změnu zásob ve srovnání s aktuálně stanoveným minimem.
- **Odstranit** – Odstraní vybraný řádek.
- **Odstranit řádky deníku** – Odstraní všechny řádky v deníku.

### <a name="calculate-a-proposal"></a>Výpočet návrhu

Tento krok vypočítá navrhované minimum pro každý řádek deníku a potenciální dopad řádku na hodnotu zásob. (Navrhované minimum je zobrazeno jako **Vypočítané minimální množství**.) Výpočet můžete provést vícekrát, jak budete potřebovat. Výpočet aktualizuje hodnotu **Vypočítané minimální množství**, která je zobrazena pro všechny řádky deníku.

Zobrazené výpočty neovlivní skutečné hodnoty minimálního množství pro každý produkt, dokud nevyberete v podokně akcí příkaz **Zaúčtovat**. Pak budou hodnoty **Nové minimální množství** použity na každý produkt.

1. Přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> Spustit \> Výpočet pojistných zásob**.
1. Otevřete deník, pro který chcete vypočítat návrh. Případně vytvořte nový deník, jak je popsáno dříve v tomto tématu.
1. Na záložce s náhledem **Řádky deníku** vyberte na panelu nástrojů příkaz **Vypočítat návrh**. (Nemusíte vybrat žádné řádky.)
1. V dialogu **Výpočet návrhu pro minimální úroveň skladových zásob** nastavte následující pole:

    - **Použít průměrný výdej během doby realizace** – Tuto možnost vyberte, chcete-li vygenerovat hodnoty **Vypočítané minimální množství** na základě průměrného výdeje za uvedené období. Poté v poli **Koeficient násobení** zadejte hodnotu, o kterou chcete upravit výsledek podle potřeby. Například zadejte *1,0*, chcete-li použít přesný vypočítaný průměr, nebo *1,1* pro přidání další vyrovnávací zásoby ve výši 10 procent.
    - **Použít úroveň služeb** – Tuto možnost vyberte, chcete-li vypočítat navrhované minimum na základě požadované úrovně služeb. Poté v poli **Úroveň služby** vyberte preferovanou úroveň služeb.
    - **Rozpětí doby realizace** – Zadejte hodnotu, o kterou se prodlouží běžná doba realizace (například pro umožnění administrace).
    - **Použít vypočítané minimální množství jako nové minimální množství** – Nastavte tuto možnost na *Ano*, chcete-li automaticky kopírovat hodnoty ze sloupce **Vypočítané minimální množství** do sloupce **Nové minimální množství** ve všech řádcích po dokončení výpočtu. Pokud tuto možnost nastavíte na *Ne*, bude hodnota **Aktuální minimální množství** zkopírována do sloupce **Nové minimální množství** ve všech řádcích. Poté budete muset ručně upravit hodnoty **Nové minimální množství** podle potřeby.

1. Na záložce s náhledem **Spustit na pozadí** zvolte, zda má úloha běžet v dávkovém režimu a/nebo nastavte opakující se rozvrh. Pole fungují stejně jako u jiných typů [prací na pozadí](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Vyberte **OK**. Výsledky výpočtu jsou uvedeny ve sloupci **Vypočítané minimální množství** na záložce s náhledem **Řádky deníku**. Hodnoty jsou prozatím pouze navrhované – ještě nebyly použity na vaše produkty.

### <a name="update-minimum-quantity"></a>Aktualizace minimálního množství

Libovolný řádek v deníku pojistných zásob můžete vybrat a ručně přepsat hodnotu v poli **Nové minimální množství**.

1. Přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> Spustit \> Výpočet pojistných zásob**.
1. Otevřete deník, který chcete upravit. Případně vytvořte nový deník, jak bylo popsáno dříve.
1. Na záložce s náhledem **Řádky deníku** najděte řádek, který chcete upravit, a poté upravte hodnotu ve sloupci **Nové minimální množství**. Můžete například nastavit hodnotu **Nové minimální množství** tak, aby odpovídala hodnotě **Vypočítané minimální množství**. Pokud má **Vypočítané minimální množství** hodnotu *0* (nula), můžete zadat požadovanou budoucí hodnotu.

### <a name="post-the-new-minimum-quantity-and-validate-the-result"></a>Zaúčtování nového minimálního množství a ověření výsledku

Podle následujícího postupu zaúčtujte nové minimální množství a ověřte výsledek.

1. Přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> Spustit \> Výpočet pojistných zásob**.
1. Otevřete deník pro zaúčtování nových minimálních množství. Případně vytvořte nový deník, jak bylo popsáno dříve.
1. V podokně akcí zvolte **Zaúčtovat**.
1. V dialogu **Zaúčtovat deník** nastavte pole **Převést všechny chyby zaúčtování do nového deníku** podle potřeby. Poté tlačítkem **OK** zaúčtujte deník.
1. Pokud jste změnili **Nové minimální množství** v řádku na záložce s náhledem **Řádky deníku**, můžete změnu potvrdit pomocí následujících kroků:

    1. U řádku, který jste upravili, vyberte odkaz ve sloupci **Číslo položky**.
    1. V dialogu **Informace o produktu** vyberte odkaz v poli **Číslo položky** a otevřete tak související záznam uvolněného produktu.
    1. V podokně akcí na kartě **Plán** ve skupině **Disponibilita** vyberte **Disponibilita položky**.
    1. Všimněte si, že hodnota **Minimum** pro pracoviště a sklad, kterou jste upravili pomocí zaúčtovaného deníku pojistných zásob, byla nyní aktualizována, aby odpovídala vaší úpravě.

## <a name="additional-resources"></a>Další prostředky

- [Splnění rezervních zásob položek](safety-stock-replenishment.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
